# Calculadora-tempo
Calculadora tempo
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Tempo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input[type="number"] {
            width: 100px;
            padding: 5px;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        #result {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h2>Calculadora de Tempo</h2>
    <label for="frequency">Frequência (bpm):</label>
    <input type="number" id="frequency">
    <label for="intervals">Número de Intervalos:</label>
    <input type="number" id="intervals">
    <button onclick="calculateTime()">Calcular</button>
    <div id="result"></div>

    <script>
        function calculateTime() {
            var frequency = document.getElementById('frequency').value;
            var intervals = document.getElementById('intervals').value;
            var totalTime = (intervals * 60) / frequency;
            document.getElementById('result').innerText = 'Tempo Total (s): ' + totalTime.toFixed(2);
        }
    </script>
</body>
</html>
