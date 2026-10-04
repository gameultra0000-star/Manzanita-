
# Manzanita-
te amo mucho
index.html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Una pequeña pregunta...</title>
  <style>
    * { box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 100%);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0;
      padding: 20px;
    }
    .card {
      background: rgba(255, 255, 255, 0.9);
      border-radius: 20px;
      padding: 30px;
      width: 100%;
      max-width: 400px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
    }
    h1 { color: #333; font-size: 1.5rem; margin-bottom: 20px; }
    p { color: #666; font-size: 1rem; line-height: 1.5; }
    .btn {
      background-color: #ff6b81;
      color: white;
      border: none;
      padding: 12px 24px;
      margin: 8px 0;
      border-radius: 25px;
      font-size: 1rem;
      font-weight: bold;
      width: 100%;
      cursor: pointer;
      transition: background 0.3s;
    }
    .btn:hover { background-color: #ff4757; }
    .screen { display: none; }
    .active { display: block; }
  </style>
</head>
<body>

  <div class="card">
    <!-- PANTALLA 1: Inicio / Misión -->
    <div id="pantalla1" class="screen active">
      <h1>¡Hola! 👋</h1>
      <p>Tienes una mini misión para desbloquear un mensaje secreto.</p>
      <button class="btn" onclick="siguientePantalla('pantalla2')">Aceptar misión 🚀</button>
    </div>

    <!-- PANTALLA 2: Pregunta divertida -->
    <div id="pantalla2" class="screen">
      <h1>Nivel 1 🎮</h1>
      <p>Para continuar, selecciona la opción correcta:</p>
      <button class="btn" onclick="siguientePantalla('pantalla3')">Opción 1: Pasar un buen rato leyendo esto ✨</button>
      <button class="btn" onclick="siguientePantalla('pantalla3')">Opción 2: Descubrir el secreto 🙈</button>
    </div>

    <!-- PANTALLA 3: La Revelación -->
    <div id="pantalla3" class="screen">
      <h1>¡Nivel completado! 🎉</h1>
      <p style="font-size: 1.2rem; font-weight: bold; color: #ff4757;">
        Tengo algo importante que decirte... <br><br>
        ¡Me gustas mucho! 💖
      </p>
      <p>Espero que esta pequeña sorpresa te saque una sonrisa.</p>
    </div>
  </div>

  <script>
    function siguientePantalla(idPantalla) {
      // Oculta todas las pantallas
      const pantallas = document.querySelectorAll('.screen');
      pantallas.forEach(p => p.classList.remove('active'));
      
      // Muestra la pantalla seleccionada
      document.getElementById(idPantalla).classList.add('active');
    }
  </script>

</body>
</html>
