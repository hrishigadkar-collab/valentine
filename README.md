

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Special Message for You</title>
    <style>
        body {
            background-color: #ffe4e1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 50px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            z-index: 1;
        }

        h1 { color: #ff4d6d; font-size: 2.5rem; }
        
        .buttons {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        #yesBtn { background-color: #ff4d6d; color: white; }
        #noBtn { background-color: #888; color: white; position: absolute; }

        .hearts { position: absolute; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; }
    </style>
</head>
<body>

    <div class="container">
        <h1 id="question">Will you be mine forever? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">YES!</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <script>
        // Function to make the "No" button run away
        function moveButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        // What happens when she clicks Yes
        function celebrate() {
            document.getElementById('question').innerHTML = "I knew you'd say Yes! I love you! 💍🌹";
            document.querySelector('.buttons').style.display = 'none';
            document.body.style.backgroundColor = '#ffb3c1';
            
            // Basic confetti effect alert
            alert("Check your messages! I have something else for you ❤️");
        }
    </script>
</body>
</html>
