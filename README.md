<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Activator</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <style>
        /* General Styles */
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, #f4f4f9, #e8e8f0);
            color: #333;
            margin: 0;
            padding: 0;
        }
        h1 {
            text-align: center;
            background-color: #4CAF50;
            color: white;
            padding: 20px;
            margin: 0;
            font-size: 2.5em;
            font-weight: bold;
            border-radius: 0 0 15px 15px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        p {
            text-align: center;
            font-size: 1.2em;
            margin: 20px;
        }

        /* Controls */
        .controls {
            text-align: center;
            margin-bottom: 20px;
        }
        #search {
            padding: 10px;
            width: 60%;
            max-width: 400px;
            font-size: 1em;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }

        /* Categories */
        .button-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }
        .category {
            width: 90%;
            max-width: 800px;
            margin: 20px auto;
            border: 1px solid #ddd;
            border-radius: 15px;
            background-color: #fff;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        .category h2 {
            margin: 0;
            padding: 15px;
            font-size: 1.5em;
            font-weight: bold;
            color: white;
            background-color: #4CAF50;
            border-radius: 15px 15px 0 0;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .category h2:hover {
            background-color: #45a049;
        }

        /* Expanding Categories */
        .category-content {
            display: none;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            max-height: 0;
            padding: 15px;
        }
        .category-content.active {
            display: block;
            max-height: 500px; /* Adjust this value as needed */
        }

        /* Buttons */
        button {
            display: flex;
            align-items: center;
            gap: 10px;
            justify-content: center;
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white;
            border: none;
            border-radius: 10px;
            padding: 10px 20px;
            font-size: 1.2em;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease-in-out;
        }
        button:hover {
            transform: scale(1.05);
            box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.15);
        }
        button:active {
            transform: scale(0.95);
            box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <h1>Routine Activator</h1>
    <p>Search for routines or click a category to expand and activate a routine.</p>
    <div class="controls">
        <input type="text" id="search" placeholder="Search routines..." onkeyup="filterButtons()">
    </div>
    <div class="button-container">
        <!-- Lighting Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">Lighting</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger1')">
                    <i class="fas fa-lightbulb"></i> Living Room On
                </button>
                <button onclick="triggerRoutine('https://example.com/trigger2')">
                    <i class="fas fa-power-off"></i> All Off
                </button>
            </div>
        </div>
        <!-- Media Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">Media</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger3')">
                    <i class="fas fa-music"></i> Chill Mix Spotify
                </button>
                <button onclick="triggerRoutine('https://example.com/trigger4')">
                    <i class="fas fa-tv"></i> Living Room TV Off
                </button>
            </div>
        </div>
        <!-- HVAC Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">HVAC</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger5')">
                    <i class="fas fa-fire"></i> Heater On
                </button>
                <button onclick="triggerRoutine('https://example.com/trigger6')">
                    <i class="fas fa-snowflake"></i> Heater Off
                </button>
            </div>
        </div>
    </div>

    <script>
        // Dynamic button filter
        function filterButtons() {
            const query = document.getElementById('search').value.toLowerCase();
            const buttons = document.querySelectorAll('.category-content button');
            buttons.forEach(button => {
                button.style.display = button.textContent.toLowerCase().includes(query) ? '' : 'none';
            });
        }

        // Routine trigger with feedback
        function triggerRoutine(url) {
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert("Routine activated successfully!");
                    } else {
                        alert("Failed to activate routine. Try again.");
                    }
                })
                .catch(err => alert("Error: " + err.message));
        }

        // Category toggle
        function toggleCategory(header) {
            const content = header.nextElementSibling;
            content.classList.toggle('active');
        }
    </script>
</body>
</html>
