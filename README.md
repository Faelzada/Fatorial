<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatorial</title>
    <style>
        body{
            background-color:rgb(18, 94, 156) ;
            color: white;
            text-align: center;
            font-family: 'Gill Sans', 'Gill Sans MT', 'Trebuchet MS', sans-serif
        }
    </style>
</head>
<body>
    <h1>Fatorial</h1>
    <label for="number">Digite um número:</label>
    <input type="number" id="number" min="0">
    <button onclick="calculateFactorial()">Calcular</button>
    <p id="result">Resultado:</p>

    <script>
        function calculateFactorial() {
            var number = document.getElementById('number').value;
            var result = factorial(number);
            document.getElementById('result').innerText = 'O fatorial de ' + number + ' é ' + result;
        }

        function factorial(n) {
            if (n < 0) return -1;
            else if (n == 0) return 1;
            else return (n * factorial(n - 1));
        }
    </script>
</body>
</html>
