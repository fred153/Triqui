<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Triqui</title>
  <style>
    body {
      transition: background-color 1s ease;
    }
    button {
      padding: 10px 20px;
      font-size: 18px;
    }
    h1 {
      color: #007acc;
    }
  </style>
</head>
<body>
  <h1>Bienvenidos a TRIQUI</h1>
  <p>Esta es mi primera página con HTML, CSS y JavaScript.</p>
  <button onclick="saludar()">Haz clic aquí</button>

  <script>
    const colores = ["#ff0000", "#00ff00", "#0000ff", "#ffff00", "#ff00ff"];
    let i = 0;

    setInterval(() => {
      document.body.style.backgroundColor = colores[i];
      document.getElementById("boton").style.backgroundColor = colores[(i + 2) % colores.length];
      i = (i + 1) % colores.length;
    }, 1000);
    function saludar() {
      alert("¡Hola! Has hecho clic en el botón.");
    }
  </script>
</body>
</html>
