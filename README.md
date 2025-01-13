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
        .light-mode {
            background-color: #f9f9f9;
            color: #121212;
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
    <!-- Global Controls -->
    <div class="global-controls">
        <button onclick="toggleAll('on')">Turn Everything ON</button>
        <button class="off" onclick="toggleAll('off')">Turn Everything OFF</button>
        <button onclick="toggleTheme()">Toggle Theme</button>
    </div>

    <div class="dashboard-container">
        <!-- Kitchen Group -->
        <div class="tile">
            <i class="fas fa-utensils"></i>
            <h3>Kitchen Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb&token=57d238c9-34e8-4bdd-9bd8-76f34bbeb544&response=html')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111&token=5405bd16-657c-487b-a635-5422deae8015&response=html')">Off</button>
            </div>
        </div>

        <!-- Living Room Group -->
        <div class="tile">
            <i class="fas fa-couch"></i>
            <h3>Living Room Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=39168a11-14c6-4bfb-8504-a73578a37555&token=a2b9357b-2a6a-4277-b2ac-3fe59fc0a80e&response=html')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c&token=f34fc986-2182-4d80-816e-4cb08e3f7578&response=html')">Off</button>
            </div>
        </div>

        <!--Living Room TV -->
        <div class="tile">
            <i class="fas fa-tv"></i>
            <h3>NFC - Living Room</h3>
            <div class="button-group">
                   <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f&token=48d2e3a7-60af-4973-b63e-3a183df4b9e8&response=html')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=b549ddb0-1824-40cb-8162-3fde4f2de6f6&token=a03ce575-1d91-471c-95c3-feb8b9b75ad8&response=html')">Off</button>
            </div>
        </div>

        <!-- Office Group -->
        <div class="tile">
            <i class="fas fa-chair"></i>
            <h3>Office Group</h3>
            <div class="button-group">
                <button class="button-on" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=747403c7-9a9f-4a47-9a80-0f6923b5c4d0&token=50f5e41a-50c5-4802-9d4f-a673d38c2491&response=html')">On</button>
                <button class="button-off" onclick="triggerRoutine('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=e458094d-4c7a-42b8-8d7c-61b0bcaca741&token=1549d5d9-19ef-4a9c-bb1f-9a2f055e6a82&response=html')">Off</button>
            </div>
        </div>
    </div>

    <script>
        function toggleAll(action) {
    const urls = [
        // Kitchen Group
        action === 'on'
            ? 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb'
            : 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111',
        
        // Living Room Group
        action === 'on'
            ? 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=39168a11-14c6-4bfb-8504-a73578a37555'
            : 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c',
        
        // NFC - Living Room
        action === 'on'
            ? 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f'
            : 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=b549ddb0-1824-40cb-8162-3fde4f2de6f6',

        // Office Group
        action === 'on'
            ? 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=747403c7-9a9f-4a47-9a80-0f6923b5c4d0'
            : 'https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=e458094d-4c7a-42b8-8d7c-61b0bcaca741'
    ];

    urls.forEach(url => triggerRoutine(url));
}
    </script>
</body>
</html>
