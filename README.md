<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Activator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        h1 {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
            text-align: center;
            margin: 0;
        }
        p {
            text-align: center;
            font-size: 1.2em;
            margin: 20px;
        }
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
            border-radius: 5px;
        }
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
            border-radius: 5px;
            background-color: #fff;
            overflow: hidden;
        }
        .category h2 {
            margin: 0;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }
        .category-content {
            display: none;
            padding: 15px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 10px 15px;
            font-size: 1em;
            cursor: pointer;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease-in-out;
        }
        button:hover {
            background-color: #45a049;
            transform: scale(1.05);
            box-shadow: 0px 6px 10px rgba(0, 0, 0, 0.15);
        }
        button:active {
            background-color: #3e8e41;
            transform: scale(0.95);
            box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
        }
        .dark-mode {
            background-color: #333;
            color: #f4f4f9;
        }
        .dark-mode h1, .dark-mode h2 {
            background-color: #222;
        }
        .dark-mode button {
            background-color: #666;
            color: #fff;
        }
    </style>
</head>
<body>
    <h1>Routine Activator</h1>
    <p>Search for routines or click a category to activate a routine.</p>
    <div class="controls">
        <input type="text" id="search" placeholder="Search routines..." onkeyup="filterButtons()">
        <button onclick="toggleDarkMode()">Toggle Dark Mode</button>
    </div>
    <div class="button-container">
        <!-- Lighting Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">Lighting</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger1')" title="Turns on the living room lights">Living Room On</button>
                <button onclick="triggerRoutine('https://example.com/trigger2')" title="Turns off all lights">All Off</button>
            </div>
        </div>
        <!-- Media Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">Media</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger3')" title="Plays Chill Mix on Spotify">Chill Mix Spotify</button>
                <button onclick="triggerRoutine('https://example.com/trigger4')" title="Turns off the living room TV">Living Room TV Off</button>
            </div>
        </div>
        <!-- HVAC Category -->
        <div class="category">
            <h2 onclick="toggleCategory(this)">HVAC</h2>
            <div class="category-content">
                <button onclick="triggerRoutine('https://example.com/trigger5')" title="Turns on the heater">Heater On</button>
                <button onclick="triggerRoutine('https://example.com/trigger6')" title="Turns off the heater">Heater Off</button>
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
            content.style.display = content.style.display === 'none' || !content.style.display ? 'block' : 'none';
        }

        // Dark mode toggle
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
        }
    </script>
</body>
</html>
