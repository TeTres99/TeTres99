<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Me perdonas?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .progress {
            width: 300px;
            height: 30px;
            background-color: #f3f3f3;
            border-radius: 15px;
            overflow: hidden;
            margin: 20px auto;
        }
        .progress-bar {
            height: 100%;
            background-color: #4CAF50;
            width: 50%;
            text-align: center;
            color: white;
            line-height: 30px;
        }
        .button-container button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>¿Me perdonas?</h1>
    <div class="progress">
        <div id="progressBar" class="progress-bar">50%</div>
    </div>
    <div class="button-container">
        <button onclick="increaseNo()">No</button>
        <button onclick="increaseYes()">Sí</button>
    </div>
    <p id="message"></p>

    <script>
        let progress = 50;

        function increaseNo() {
            if (progress < 100) {
                progress += 5;
                document.getElementById("progressBar").style.width = progress + "%";
                document.getElementById("progressBar").innerText = progress + "%";
            }
        }

        function increaseYes() {
            document.getElementById("message").innerText = "Yo sabía que ibas a perdonarme.";
            document.getElementById("progressBar").style.width = "100%";
            document.getElementById("progressBar").innerText = "100%";
        }
    </script>
</body>
</html>
