<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        h1 {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
            margin: 0;
        }
        p {
            font-size: 1.2em;
            margin: 20px;
        }
        .button-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 20px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 15px 20px;
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
    </style>
</head>
<body>
    <h1>Routine Activator</h1>
    <p>Click on a button to activate the corresponding routine.</p>
    <div class="button-container">

        <button onclick="window.open('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f&token=48d2e3a7-60af-4973-b63e-3a183df4b9e8&response=html', '_blank')">
            NFC 1 - Living Room On
        </button>
    
        <button onclick="window.open('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=d05db4c2-a1c4-4bfa-a989-fc26dd0de7be&token=016673b9-fa11-41c0-b3ad-bfd41f780098&response=html', '_blank')">
            NFC 2 - His Closet On
        </button>
    
        <!-- Additional buttons go here -->

    </div>
</body>
</html>
