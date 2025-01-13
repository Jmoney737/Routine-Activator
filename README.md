<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tile-Based Routine Dashboard</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #121212;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .dashboard-container {
            display: grid;
            grid-template-columns: repeat(2, 150px);
            gap: 20px;
            justify-content: center;
        }
        .tile {
            background-color: #1E1E1E;
            border-radius: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 15px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .tile:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }
        .tile i {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        .tile h3 {
            font-size: 1rem;
            text-align: center;
        }
        .button-group {
            margin-top: 10px;
            display: flex;
            gap: 10px;
        }
        .button-group button {
            border: none;
            border-radius: 10px;
            padding: 5px 10px;
            cursor: pointer;
            font-size: 0.8rem;
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
    <div class="dashboard-container">
        <!-- Kitchen Group Tile -->
        <div class="tile" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb')">
            <i class="fas fa-utensils"></i>
            <h3>Kitchen Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb', this)">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111', this)">Off</button>
            </div>
        </div>

        <!-- Living Room Group Tile -->
        <div class="tile">
            <i class="fas fa-couch"></i>
            <h3>Living Room Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=39168a11-14c6-4bfb-8504-a73578a37555', this)">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c', this)">Off</button>
            </div>
        </div>

        <!-- NFC Tile -->
        <div class="tile">
            <i class="fas fa-wave-square"></i>
            <h3>NFC - Living Room</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f', this)">On</button>
            </div>
        </div>

        <!-- Office Group Tile -->
        <div class="tile">
            <i class="fas fa-briefcase"></i>
            <h3>Office Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=747403c7-9a9f-4a47-9a80-0f6923b5c4d0', this)">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=e458094d-4c7a-42b8-8d7c-61b0bcaca741', this)">Off</button>
            </div>
        </div>
    </div>

    <script>
        function triggerRoutine(url, button) {
            button.innerText = "Processing...";
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert("Routine triggered successfully!");
                    }
                })
                .finally(() => {
                    button.innerText = button.classList.contains("button-on") ? "On" : "Off";
                });
        }
    </script>
</body>
</html>
