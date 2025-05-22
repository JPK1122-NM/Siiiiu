# Siiiiu
Cristiano Ronaldo dos Santos Aveiro 
<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Cristiano Ronaldo - A Lenda Viva</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-dark: #121212;
      --bg-light: #f2f2f2;
      --text-dark: #fff;
      --text-light: #000;
      --accent: gold;
      --transition: 0.4s ease;
    }

    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-dark);
      transition: background-color var(--transition), color var(--transition);
    }

    header {
      background: url('https://upload.wikimedia.org/wikipedia/commons/8/8c/Cristiano_Ronaldo_2018.jpg') center/cover no-repeat;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    header h1 {
      font-size: 3em;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 12px;
      animation: slideDown 1.5s ease-in-out;
    }

    nav {
      background: #1a1a1a;
      display: flex;
      justify-content: center;
      padding: 15px;
      flex-wrap: wrap;
    }

    nav a {
      color: var(--accent);
      text-decoration: none;
      margin: 0 20px;
      font-weight: 600;
      transition: color var(--transition);
    }

    nav a:hover {
      color: orange;
    }

    .toggle-mode {
      position: absolute;
      top: 20px;
      right: 20px;
      background: var(--accent);
      color: #000;
      border: none;
      padding: 10px 15px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
      transition: background var(--transition);
    }

    section {
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      transition: all 1s ease;
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      color: var(--accent);
      font-size: 2em;
      margin-bottom: 20px;
    }

    ul {
      padding-left: 20px;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }

    .gallery img {
      width: 100%;
      max-width: 300px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
      transition: transform 0.3s ease;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    .videos iframe {
      width: 100%;
      max-width: 600px;
      height: 315px;
      margin: 20px 0;
      border-radius: 12px;
      border: none;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #1a1a1a;
      color: #aaa;
    }

    @keyframes slideDown {
      from {
        transform: translateY(-50px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 2em;
      }
      nav {
        flex-direction: column;
        gap: 10px;
      }
    }
  </style>
</head>
<body>
  <button class="toggle-mode" onclick="toggleMode()">Modo Claro/Escuro</button>

  <header>
    <h1>Cristiano Ronaldo - A Lenda Viva</h1>
  </header>

  <nav>
    <a href="#biografia">Biografia</a>
    <a href="#carreira">Carreira</a>
    <a href="#conquistas">Conquistas</a>
    <a href="#fotos">Fotos</a>
    <a href="#videos">Vídeos</a>
  </nav>

  <section id="biografia">
    <h2>Biografia</h2>
    <p>Cristiano Ronaldo dos Santos Aveiro nasceu em 5 de fevereiro de 1985, em Funchal, Madeira, Portugal. Desde pequeno mostrou talento e paixão pelo futebol...</p>
  </section>

  <section id="carreira">
    <h2>Carreira</h2>
    <p>Passou por grandes clubes como Sporting, Manchester United, Real Madrid, Juventus e atualmente no Al-Nassr. Pela seleção portuguesa, conquistou a Euro 2016 e a Liga das Nações.</p>
  </section>

  <section id="conquistas">
    <h2>Conquistas</h2>
    <ul>
      <li>5x Liga dos Campeões da UEFA</li>
      <li>7x Campeonatos Nacionais</li>
      <li>5x Bola de Ouro</li>
      <li>Eurocopa 2016</li>
      <li>Liga das Nações 2019</li>
      <li>Maior artilheiro da história da Liga dos Campeões</li>
      <li>Mais de 800 gols na carreira</li>
    </ul>
  </section>

  <section id="fotos" class="gallery">
    <h2>Fotos</h2>
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/Cristiano_Ronaldo_2017.jpg" alt="Cristiano Ronaldo 2017">
    <img src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Cristiano_Ronaldo_2013.jpg" alt="Cristiano Ronaldo 2013">
  </section>

  <section id="videos" class="videos">
    <h2>Vídeos</h2>
    <iframe src="https://www.youtube.com/embed/1I5ZMmrOfnA" title="Cristiano Ronaldo - Goals & Skills"></iframe>
    <iframe src="https://www.youtube.com/embed/Ly7N2gV2qkY" title="Cristiano Ronaldo - Documentário"></iframe>
  </section>

  <footer>
    <p>Site feito para fins educativos - Todos os direitos das imagens e vídeos são de seus respectivos donos.</p>
  </footer>

  <script>
    // Scroll animation
    const sections = document.querySelectorAll('section');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.1 });
    sections.forEach(section => observer.observe(section));

    // Toggle light/dark mode
    let darkMode = true;
    function toggleMode() {
      darkMode = !darkMode;
      document.body.style.backgroundColor = darkMode ? '#121212' : '#f2f2f2';
      document.body.style.color = darkMode ? '#fff' : '#000';
    }
  </script>
</body>
</html>
