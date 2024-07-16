<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marquee Text Display</title>
    <style>
        body {
            background-color: black;
            color: red;
            text-align: center;
            margin: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        #textInput {
            width: 80%;
            padding: 10px;
            font-size: 16px;
            margin-bottom: 20px;
            border: none;
            border-radius: 5px;
            text-align: center;
            background-color: black; /* Cor de fundo do campo de entrada */
            color: red; /* Cor do texto do campo de entrada */
            border: 1px solid red; /* Bordas vermelhas para destacar */
        }
        #displayArea {
            width: 100%;
            color: red;
        }
    </style>
</head>
<body>
    <div id="inputContainer">
        <input type="text" id="textInput" placeholder="Paste your text here">
    </div>
    <div id="displayArea">
	<hr style="width: 0.2%; border-color: red;">
        <h1><marquee id="marquee" scrollamount="50" direction="left" loop="infinite"></marquee></h1>
	
    </div>
    <script>
        document.getElementById('textInput').addEventListener('input', function() {
            document.getElementById('marquee').innerText = this.value;
            document.getElementById('inputContainer').style.display = 'none';
        });
    </script>
</body>
</html>
