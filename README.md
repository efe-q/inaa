<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Benimle Barışır mısın?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            background-color: #f8e8e8;
            font-family: Arial, sans-serif;
            position: relative;
            overflow: hidden;
        }
        h1 {
            margin-bottom: 20px;
        }
        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            width: 500px;
            height: 50px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            position: absolute;
        }
        #yes {
            background-color: #4CAF50;
            color: white;
            position: relative;
        }
        #no {
            background-color: #FF4136;
            color: white;
        }
    </style>
</head>
<body>
    <h1>Benimle barışır mısın? ❤️</h1>
    <div class="buttons">
        <button id="yes" onclick="alert('Yaa güzel bebeğim benim ❤️')">Evet</button>
        <button id="no">Hayır</button>
    </div>

    <script>
        const noButton = document.getElementById('no');
        const yesButton = document.getElementById('yes');

        noButton.style.left = `${yesButton.offsetLeft + yesButton.offsetWidth + 20}px`;
        noButton.style.top = `${yesButton.offsetTop}px`;

        noButton.addEventListener('mouseover', () => {
            const maxX = window.innerWidth - noButton.clientWidth - 300; // Sağda sınır
            const maxY = window.innerHeight - noButton.clientHeight - 300; // Altta sınır
            const minx = 300; // Solda sınır    
            let newX = Math.random() * maxX;
            let newY = Math.random() * maxY;


            newX = Math.max(1, Math.min(newX, maxX));
            newY = Math.max(1, Math.min(newY, maxY));

            noButton.style.left = `${newX}px`;
            noButton.style.top = `${newY}px`;
        });
    </script>
</body>
</html>
