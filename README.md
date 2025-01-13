<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Dashboard</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #121212;
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            transition: background-color 0.3s, color 0.3s;
        }
        .dashboard-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            width: 90%;
            max-width: 600px;
        }
        @media (max-width: 600px) {
            .dashboard-container {
                grid-template-columns: 1fr;
            }
            .tile {
                padding: 20px;
                min-height: 150px;
            }
            .button-group button {
                font-size: 1rem;
                padding: 10px 15px;
            }
        }
        .global-controls {
            margin: 20px 0;
            display: flex;
            gap: 20px;
        }
        .global-controls button {
            padding: 10px 20px;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            transition: background-color 0.3s;
        }
        .global-controls button:hover {
            background-color: #45a049;
        }
        .global-controls button.off {
            background-color: #f44336;
        }
        .global-controls button.off:hover {
            background-color: #e53935;
        }
        .tile {
            background-color: #1E1E1E;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 30px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            min-height: 200px;
        }
        .tile:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }
        .tile i {
            font-size: 3rem;
            margin-bottom: 10px;
            color: #4CAF50;
        }
        .tile h3 {
            font-size: 1.5rem;
            margin: 10px 0;
            text-align: center;
        }
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        .button-group button {
            border: none;
            border-radius: 10px;
            padding: 15px 20px;
            cursor: pointer;
            font-size: 1.2rem;
        }
        .button-on {
            background-color: #4CAF50;
            color: white;
        }
        .button-off {
            background-color: #f44336;
            color: white;
        }
    </style>
</head>
<body>
    <h1>Routine Dashboard</h1>

    <!-- Global Controls -->
    <div class="global-controls">
        <button onclick="toggleAll('on')">Turn Everything ON</button>
        <button class="off" onclick="toggleAll('off')">Turn Everything OFF</button>
    </div>

    <!-- Dashboard Tiles -->
    <div class="dashboard-container">
        <!-- Kitchen Group Tile -->
        <div class="tile">
            <i class="fas fa-blender"></i>
            <h3>Kitchen Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://example.com/kitchen-on')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://example.com/kitchen-off')">Off</button>
            </div>
        </div>

        <!-- Living Room Group Tile -->
        <div class="tile">
            <i class="fas fa-couch"></i>
            <h3>Living Room Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://example.com/living-room-on')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://example.com/living-room-off')">Off</button>
            </div>
        </div>

        <!-- Office Group Tile -->
        <div class="tile">
            <i class="fas fa-chair"></i>
            <h3>Office Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://example.com/office-on')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://example.com/office-off')">Off</button>
            </div>
        </div>
    </div>

    <script>
        // Trigger a specific routine
        function triggerRoutine(url) {
            alert("Triggering routine...");
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert("Routine triggered successfully!");
                    } else {
                        alert("Failed to trigger routine.");
                    }
                })
                .catch(() => {
                    alert("Error connecting to the routine.");
                });
        }

        // Global ON/OFF toggle
        function toggleAll(action) {
            const urls = [
                'https://example.com/kitchen-on',
                'https://example.com/living-room-on',
                'https://example.com/office-on'
            ];
            if (action === 'off') {
                urls[0] = 'https://example.com/kitchen-off';
                urls[1] = 'https://example.com/living-room-off';
                urls[2] = 'https://example.com/office-off';
            }
            urls.forEach(url => triggerRoutine(url));
        }
    </script>
</body>
</html>
