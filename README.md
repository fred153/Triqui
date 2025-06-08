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
    function  crear_malla_vacia(){
      const malla = [];
      for(let i = 0;i<3;i++){
        const fila=[];
        for(let j = 0; j<3;j++){
          fila.push(" ");
        }
        malla.push(fila);
      }
      return malla;
    }
    function mallaAgregar(malla, a, b, c) {
      const mallaNueva = malla.map(fila => fila.slice());
      if (mallaNueva[b][c] !== " ") {
        return mallaNueva;
      }
      mallaNueva[b][c] = `[${a}]`;
      return mallaNueva;
    }
    function buscar_nodo(arbol, valor, nivel = 0) {
      if (arbol.valor === valor) {
        return { encontrado: true, nivel: nivel };
      }
      if (arbol.hijos && arbol.hijos.length > 0) {
        for (let i = 0; i < arbol.hijos.length; i++) {
          const resultado = buscar_nodo(arbol.hijos[i], valor, nivel + 1);
          if (resultado.encontrado) {
            return resultado;
          }
        }
      }
      return { encontrado: false, nivel: nivel };
    }
  </script>

</body>
</html>

