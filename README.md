# juris-quest
Tracking daily quests, LNAT experience points, and Jurisprudence mastery on the path to the Oxford Dragon's Lair. Level up or stay a peasant. "SHAW"
# 🐲 PROJECT: JURIS QUEST v1.0 ⚖️
> **SYSTEM STATUS:** [ONLINE] | **PLAYER:** Qasim | **FACTION:** Oxford Law 

---

## 🎭 THE DRAGON'S GREETING
```text
          
              
                         "Halt, mortal! I am the Guardian of the 
                          Oxford Vault. You seek the ancient 
                          knowledge of Jurisprudence? Prove your 
                          worth through the Daily Quests, or 
                          suffer the flame of procrastination!"
                                        *SHAW!*      
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JURIS QUEST: SHAW EDITION</title>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Orbitron:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --blood-red: #ff0000;
            --pure-white: #ffffff;
            --deep-black: #000000;
        }

        body, html {
            background-color: var(--deep-black);
            color: var(--pure-white);
            font-family: 'Orbitron', sans-serif;
            margin: 0;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .screen {
            display: none;
            flex-direction: column;
            align-items: center;
            text-align: center;
            width: 90%;
            max-width: 600px;
            animation: fadeIn 0.8s ease-in-out;
        }

        .active { display: flex; }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        /* --- BUTTON STYLES --- */
        .btn {
            background: none;
            border: 2px solid var(--pure-white);
            color: var(--pure-white);
            padding: 15px 30px;
            font-family: 'Press Start 2P', cursive;
            font-size: 12px;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 20px;
        }

        .btn:hover {
            background: var(--pure-white);
            color: var(--deep-black);
            box-shadow: 0 0 20px var(--pure-white);
        }

        /* --- DRAGON ANIMATION --- */
        .dragon {
            font-size: 120px;
            filter: drop-shadow(0 0 15px var(--blood-red));
            animation: dragonFloat 2s ease-in-out infinite;
            margin-bottom: 20px;
        }

        @keyframes dragonFloat {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }

        .dragon-text {
            color: var(--blood-red);
            font-family: 'Press Start 2P', cursive;
            font-size: 14px;
            line-height: 1.8;
            margin: 20px 0;
            text-transform: uppercase;
        }

        /* --- TASK LIST --- */
        .quest-item {
            border-bottom: 1px solid #333;
            padding: 15px;
            width: 100%;
            display: flex;
            align-items: center;
        }

        input[type="checkbox"] {
            width: 20px;
            height: 20px;
            margin-right: 15px;
            accent-color: var(--blood-red);
        }
    </style>
</head>
<body>

    <div id="screen-gate" class="screen active">
        <h1 style="font-family: 'Press Start 2P'; font-size: 18px;">JURIS QUEST</h1>
        <p>CAUTION: CANDIDATE QASIM DETECTED</p>
        <button class="btn" onclick="showScreen('screen-dragon')">ENTER THE VAULT</button>
    </div>

    <div id="screen-dragon" class="screen">
        <div class="dragon">🐲</div>
        <div class="dragon-text" id="dragon-msg">
            "YOU DARE ENTER OXFORD'S DOMAIN?<br>THE LNAT IS A PIT OF FIRE.<br>JURISPRUDENCE IS THE DRAGON'S BREATH."
        </div>
        <button class="btn" onclick="showScreen('screen-tasks')">SHAW</button>
    </div>

    <div id="screen-tasks" class="screen">
        <h2 style="font-family: 'Press Start 2P'; font-size: 14px;">DAILY SCROLLS</h2>
        
        <div class="quest-item">
            <input type="checkbox"> <span>LNAT: Logical Fallacy Training</span>
        </div>
        <div class="quest-item">
            <input type="checkbox"> <span>READ: Hart's Concept of Law</span>
        </div>
        <div class="quest-item">
            <input type="checkbox"> <span>BOSS: Personal Statement Edit</span>
        </div>

        <button class="btn" onclick="showScreen('screen-gate')" style="border-color: #444; font-size: 8px; margin-top: 50px;">LOGOUT</button>
    </div>

    <script>
        function showScreen(screenId) {
            // Hide all screens
            document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
            // Show the chosen one
            document.getElementById(screenId).classList.add('active');
        }
    </script>
</body>
</html>
