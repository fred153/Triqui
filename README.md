<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>TRIQUI</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 40px;
    }

    h1 {
      margin-bottom: 30px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 76px);
      grid-template-rows: repeat(3, 76px);
      gap: 10px;
      justify-content: center;
      margin-bottom: 76px;
    }

    .grid button {
      width: 76px;
      height: 76px;
      font-size: 32px;
      cursor: pointer;
    }

    #label {
      font-size: 36px;
      color: #333;
    }
  </style>
</head>
<body>

  <h1>Título de la Página</h1>

  <div class="grid">
    <button onclick="accion(1)"></button>
    <button onclick="accion(2)"></button>
    <button onclick="accion(3)"></button>
    <button onclick="accion(4)"></button>
    <button onclick="accion(5)"></button>
    <button onclick="accion(6)"></button>
    <button onclick="accion(7)"></button>
    <button onclick="accion(8)"></button>
    <button onclick="accion(9)"></button>
  </div>

  <div id="label">Tu Turno</div>

  <script>
    function accion(num) {
      document.getElementById("label").textContent = "Presionaste el botón " + num;
    }
  </script>

</body>
</html>

