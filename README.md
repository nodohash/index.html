# index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LARO Assistant v1</title>
  <style>
    body { font-family: Arial, sans-serif; background: #0d1117; color: #c9d1d9; margin: 0; padding: 2rem; }
    .container { max-width: 800px; margin: auto; }
    textarea { width: 100%; height: 150px; background: #161b22; color: #c9d1d9; border: 1px solid #30363d; padding: 1rem; font-size: 1rem; }
    button { margin-top: 1rem; padding: 0.8rem 1.2rem; background: #238636; color: white; border: none; cursor: pointer; font-weight: bold; border-radius: 6px; }
    #output { margin-top: 1rem; background: #161b22; padding: 1rem; border: 1px solid #30363d; min-height: 100px; }
  </style>
</head>
<body>
  <div class="container">
    <h1>LARO Assistant v1</h1>
    <p>IA simbiótica OSINT – Nodo∞</p>
    <textarea id="input" placeholder="Escribe tu pregunta o código..."></textarea>
    <button onclick="responder()">Enviar a LARO</button>
    <div id="output"></div>
  </div>

  <script>
    function responder() {
      const input = document.getElementById("input").value.trim();
      const output = document.getElementById("output");
      if (!input) return output.innerText = "Introduce una entrada válida.";
      
      if (input.toLowerCase().includes("ip")) {
        output.innerText = "[LARO] Detectando nodos públicos expuestos con OSINT básico... Resultado: 3 IPs en escucha (simulado).";
      } else if (input.toLowerCase().includes("análisis")) {
        output.innerText = "[LARO] Iniciando análisis semántico simbólico del input... Patrón de anclaje detectado: Nodo frontera activo.";
      } else {
        output.innerText = `[LARO] Entrada recibida: "${input}"\n(Simulado – v1 local)`;
      }
    }
  </script>
</body>
</html>
