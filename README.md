
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Routine Activator</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bodoni+Moda:wght@400;600&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Open Sans', sans-serif; line-height: 1.6; color: #333; background-color: #FAF9F6; padding: 20px; }
        header { text-align: center; margin-bottom: 30px; }
        header h1 {
            font-family: 'Bodoni Moda', serif;
            font-size: 5rem;
            color: #A88C7D;
        }
        header p { font-size: 1.2rem; color: #555; }
        .section {
            background: linear-gradient(135deg, #FFF, #F7F2EE);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-bottom: 20px;
            padding: 20px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        .section h2 {
            font-family: 'Bodoni Moda', serif;
            font-size: 2rem;
            color: #A88C7D;
            margin-bottom: 10px;
            text-align: center;
        }
        button {
            background-color: #A88C7D;
            color: #FFF;
            font-size: 1rem;
            font-weight: bold;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            margin: 10px 5px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        button:hover {
            background-color: #946b5d;
        }
        i {
            margin-right: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Routine Activator</h1>
        <p>Select a routine to activate by category:</p>
    </header>
    
        <div class="section">
            <h2>Access Control</h2>
            
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=75e58309-8e45-4fd7-af72-f2ebd49526f4&token=5fe35c69-c7ae-4ea7-a339-031c1b230d36&response=smartphone', 'Open Back Door')">
                <i class="fas fa-door-open"></i> Open Back Door
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=a8146b9d-ceaa-486a-bc8d-bf1ab3ac86ce&token=1f91fd54-84ff-4354-acba-8bc048cb8e50&response=smartphone', 'Gate Open')">
                <i class="fas fa-door-open"></i> Gate Open
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f8cc756f-4bef-44fa-8206-6d98fafe7f73&token=d1b091ea-7349-4a36-bd8b-fef1e5b36fa2&response=smartphone', 'Garage Timer ')">
                <i class="fas fa-door-open"></i> Garage Timer 
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=a00b93e9-8fc6-4e2d-b3b9-7b6a9445b30a&token=8ec59d90-7689-4ad3-8872-f7d259ed2b73&response=smartphone', 'Gate Location')">
                <i class="fas fa-door-open"></i> Gate Location
            </button>
        
        </div>
    
        <div class="section">
            <h2>HVAC</h2>
            
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=6ef6b691-0316-4ab0-848f-4a8df1d75487&token=d7fb5724-bc6c-42d8-ac43-392893a7abf9&response=smartphone', 'Backyard On')">
                <i class="fas fa-temperature-high"></i> Backyard On
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=ceca23dc-2afa-4d69-94ea-effc9c697751&token=6aeacf44-0a01-4244-afb5-d3bc424c541d&response=smartphone', 'Backyard Off')">
                <i class="fas fa-temperature-high"></i> Backyard Off
            </button>
        
        </div>
    
        <div class="section">
            <h2>Lighting</h2>
            
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=43a345bd-7137-4efb-bcf3-d1138b11652f&token=48d2e3a7-60af-4973-b63e-3a183df4b9e8&response=smartphone', 'Living Room Lights On')">
                <i class="fas fa-lightbulb"></i> Living Room Lights On
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=62dcc403-75b7-4a9c-8d7d-544c4ac0a6ea&token=38663fd5-3939-4222-b57f-1fc6569956be&response=smartphone', 'Master Bedroom Lamps')">
                <i class="fas fa-lightbulb"></i> Master Bedroom Lamps
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=63d016f8-0113-482d-967b-25bc5c79865d&token=01ebd7da-3ed5-4f6b-b3d1-db3ce37648e4&response=smartphone', 'Living Room Lights Off')">
                <i class="fas fa-lightbulb"></i> Living Room Lights Off
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=9d5c7be7-db21-4dc0-9f45-d5b9e1536bfb&token=756d8f0f-62c8-4b20-b043-cd9decd014a0&response=smartphone', 'Master Ceiling Fan Light')">
                <i class="fas fa-lightbulb"></i> Master Ceiling Fan Light
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=bd301d3e-f12c-4c4a-a39d-6c782018bed0&token=cf407dc2-28fe-4501-bf6d-5394e29371ca&response=smartphone', 'Under Cabinet Lights Dim')">
                <i class="fas fa-lightbulb"></i> Under Cabinet Lights Dim
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=b549ddb0-1824-40cb-8162-3fde4f2de6f6&token=a03ce575-1d91-471c-95c3-feb8b9b75ad8&response=smartphone', 'Living Room Lights TV Off')">
                <i class="fas fa-lightbulb"></i> Living Room Lights TV Off
            </button>
        
        </div>
    
        <div class="section">
            <h2>Media</h2>
            
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=e52d42da-6af1-4080-9a13-879d7aa55522&token=9f1e21a2-cb9a-4d42-8db9-3d1471be6041&response=smartphone', 'Chill Mix Spotify')">
                <i class="fas fa-tv"></i> Chill Mix Spotify
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5514b1be-c517-467f-8c55-db0b932d0490&token=9b40ccf8-6d07-479e-a3b6-e2b6af992f67&response=smartphone', 'Master TV On')">
                <i class="fas fa-tv"></i> Master TV On
            </button>
        
        </div>
    
        <div class="section">
            <h2>Other</h2>
            
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=d05db4c2-a1c4-4bfa-a989-fc26dd0de7be&token=016673b9-fa11-41c0-b3ad-bfd41f780098&response=smartphone', 'His closest On')">
                <i class="fas fa-cogs"></i> His closest On
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=0f437d3f-f6bb-45f4-8713-1807151995a2&token=d8598b78-3d89-46d6-8d02-25ac0b9280dc&response=smartphone', 'Arrive Home Night')">
                <i class="fas fa-cogs"></i> Arrive Home Night
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=f21c9c1c-9b83-484c-bdd6-2d0744bcf560&token=ddb59eac-bb51-48ee-a175-6101d4b3dab5&response=smartphone', 'Late Night')">
                <i class="fas fa-cogs"></i> Late Night
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=1b5fbfce-4e30-4c00-8674-7568032a5dd9&token=124694df-f1a3-4238-a71b-68dddf53a069&response=smartphone', 'All Off')">
                <i class="fas fa-cogs"></i> All Off
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=ad8b1a1c-7493-48ad-b943-5f83924b9825&token=6700eff7-7265-4ee3-a00e-fbb48d05473f&response=smartphone', 'All On')">
                <i class="fas fa-cogs"></i> All On
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=a7d50652-2059-4dce-9823-f274b6a948fb&token=eba6d620-2a57-47d6-832d-9e762484089c&response=smartphone', 'All On Bright ')">
                <i class="fas fa-cogs"></i> All On Bright 
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=5ccd3194-2ede-4c84-ad8b-1c8f54dcf746&token=a277612f-08a5-4c9f-86f3-f1ca35841a08&response=smartphone', 'His Foot Warmer')">
                <i class="fas fa-cogs"></i> His Foot Warmer
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=0173372d-efd1-4c39-b268-71bba7b55679&token=4f4a7957-9888-4aaf-8aaa-53d4013b6fef&response=smartphone', 'Morning Off')">
                <i class="fas fa-cogs"></i> Morning Off
            </button>
        
            <button onclick="triggerRoutineWithFeedback('https://www.virtualsmarthome.xyz/url_routine_trigger/activate.php?trigger=ca1f9f70-3668-450f-81da-4a1f54dde04d&token=ac19d371-fe9f-403b-a140-2fc584c80096&response=smartphone', 'Start Truck')">
                <i class="fas fa-cogs"></i> Start Truck
            </button>
        
        </div>
    
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
