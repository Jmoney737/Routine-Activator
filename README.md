<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Dashboard</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bodoni+Moda:wght@400;600&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Open Sans', sans-serif; line-height: 1.6; color: #333; background-color: #FAF9F6; }
        header {
            background: #A88C7D;
            color: #FFF;
            text-align: center;
            padding: 20px 0;
            margin-bottom: 20px;
        }
        header h1 {
            font-family: 'Bodoni Moda', serif;
            font-size: 3rem;
        }
        .dashboard-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }
        .card {
            background: linear-gradient(135deg, #FFF, #F7F2EE);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
        }
        .card i {
            font-size: 2.5rem;
            color: #A88C7D;
            margin-bottom: 15px;
        }
        .card button {
            background-color: #A88C7D;
            color: #FFF;
            font-size: 1rem;
            font-weight: bold;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .card button:hover {
            background-color: #946b5d;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            background: #A88C7D;
            color: #FFF;
        }
    </style>
</head>
<body>
    <header>
        <h1>Routine Dashboard</h1>
        <p>Quickly activate your routines below</p>
    </header>
    
    <div class="dashboard-container">
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Kitchen Group On</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5846a7ff-8452-4c2f-81c7-65792b5cfbcb&token=57d238c9-34e8-4bdd-9bd8-76f34bbeb544', 'Kitchen Group On')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Kitchen Group Off</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111&token=5405bd16-657c-487b-a635-5422deae8015', 'Kitchen Group Off')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Living Room Group On</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=39168a11-14c6-4bfb-8504-a73578a37555&token=a2b9357b-2a6a-4277-b2ac-3fe59fc0a80e', 'Living Room Group On')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Living Room Group Off</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c&token=f34fc986-2182-4d80-816e-4cb08e3f7578', 'Living Room Group Off')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Office Group On</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=747403c7-9a9f-4a47-9a80-0f6923b5c4d0&token=50f5e41a-50c5-4802-9d4f-a673d38c2491', 'Office Group On')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <p>Office Group Off</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f909cd87-e74a-4c94-bf0a-91d88c567111&token=5405bd16-657c-487b-a635-5422deae8015', 'Office Group Off')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-tv"></i>
            <p>Living Room TV Off</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1f805a37-03bd-404d-b781-0d7c4f8a051c&token=f34fc986-2182-4d80-816e-4cb08e3f7578', 'Living Room TV Off')">Activate</button>
        </div>
        <div class="card">
            <i class="fas fa-cogs"></i>
            <p>His Foot Warmer</p>
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5ccd3194-2ede-4c84-ad8b-1c8f54dcf746&token=a277612f-08a5-4c9f-86f3-f1ca35841a08', 'His Foot Warmer')">Activate</button>
        </div>
    </div>
    
    <footer>
        <p>&copy; 2025 Routine Dashboard</p>
    </footer>
    
    <script>
        function triggerRoutineWithFeedback(url, name) {
            fetch(url)
                .then(response => {
                    if (response.ok) {
                        alert(`${name} activated successfully!`);
                    } else {
                        alert(`Failed to activate ${name}. Please try again later.`);
                    }
                })
                .catch(() => alert(`Error activating ${name}. Check your connection or contact support.`));
        }
    </script>
</body>
</html>
