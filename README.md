<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PececitasTV</title>
  <style>
    :root {
      --azul-agua: #8dd9e6;
      --verde-pastel: #a8e6cf;
      --rosa-pastel: #ffd3e6;
      --amarillo-pastel: #fff8b0;
    }

    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: var(--azul-agua);
      overflow-x: hidden;
    }

    header {
      background: white;
      padding: 10px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    header img {
      height: 60px;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      display: flex;
      gap: 15px;
    }

    nav ul li {
      display: inline;
    }

    nav ul li a {
      text-decoration: none;
      color: #333;
      font-weight: bold;
      padding: 8px 12px;
      background-color: var(--verde-pastel);
      border-radius: 8px;
      transition: background-color 0.3s;
    }

    nav ul li a:hover {
      background-color: var(--rosa-pastel);
    }

    .hero {
      text-align: center;
      padding: 60px 20px;
      background-color: var(--amarillo-pastel);
    }

    .hero h1 {
      font-size: 2.5rem;
      color: #2c3e50;
    }

    .hero p {
      font-size: 1.2rem;
      color: #333;
      max-width: 700px;
      margin: 0 auto;
    }

    section {
      padding: 40px 20px;
      background: white;
    }

    footer {
      text-align: center;
      background: #f1f1f1;
      padding: 20px;
      font-size: 0.9rem;
      color: #555;
    }

    /* Animaciones */
    .bubbles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      overflow: hidden;
    }

    .bubble {
      position: absolute;
      bottom: -100px;
      width: 20px;
      height: 20px;
      background: rgba(255, 255, 255, 0.5);
      border-radius: 50%;
      animation: rise 10s infinite ease-in;
    }

    @keyframes rise {
      0% { transform: translateY(0) scale(1); opacity: 1; }
      100% { transform: translateY(-1000px) scale(0.5); opacity: 0; }
    }
  </style>
</head>
<body>
  <header>
    <img src="/logo-pececitas.png" alt="Pececitas TV">
    <nav>
      <ul>
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#programacion">Programación</a></li>
        <li><a href="#noticias">Noticias</a></li>
        <li><a href="#juegos">Juegos</a></li>
        <li><a href="#videos">Videos</a></li>
        <li><a href="#contacto">Contacto</a></li>
        <li><a href="#horarios">Horarios</a></li>
        <li><a href="#sobre">Sobre Nosotros</a></li>
      </ul>
    </nav>
  </header>

  <div class="bubbles"></div>

  <section class="hero" id="inicio">
    <h1>Bienvenidos a PececitasTV</h1>
    <p>El canal infantil en español dedicado a cuidar, educar y divertir a nuestros niños hispanos en EE.UU. y Canadá.</p>
  </section>

  <section id="sobre">
    <h2>Sobre Nosotros</h2>
    <p>Como parte del compromiso que tiene Hemisphere Media Group de servir y entretener a la comunidad hispana [...truncado para espacio...]</p>
  </section>

  <footer>
    Copyright © 2015. Hemisphere Media Group, Inc. Todos los derechos reservados.
  </footer>

  <script>
    // Crear burbujas animadas
    const container = document.querySelector('.bubbles');
    for (let i = 0; i < 30; i++) {
      const bubble = document.createElement('div');
      bubble.classList.add('bubble');
      bubble.style.left = `${Math.random() * 100}%`;
      bubble.style.animationDuration = `${6 + Math.random() * 6}s`;
      bubble.style.width = bubble.style.height = `${10 + Math.random() * 20}px`;
      container.appendChild(bubble);
    }
  </script>
</body>
</html>
