<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Programme d'Immigration Canada</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #fff;
      color: #333;
    }
    header {
      background-color: #d52b1e;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      background-color: #f5f5f5;
      padding: 10px;
      flex-wrap: wrap;
    }
    nav a {
      margin: 0 15px;
      text-decoration: none;
      color: #d52b1e;
      font-weight: bold;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      color: #d52b1e;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-width: 500px;
    }
    input, textarea, button {
      padding: 10px;
      font-size: 1rem;
    }
    button {
      background-color: #d52b1e;
      color: white;
      border: none;
      cursor: pointer;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #f5f5f5;
      font-size: 0.9rem;
    }
    .carousel {
      position: relative;
      max-width: 1000px;
      margin: auto;
      overflow: hidden;
    }
    .carousel-images {
      display: flex;
      transition: transform 0.5s ease-in-out;
    }
    .carousel-images img {
      width: 100%;
      flex-shrink: 0;
    }
    .blog-post {
      margin-bottom: 20px;
      padding: 20px;
      background-color: #f9f9f9;
      border-left: 5px solid #d52b1e;
    }
    .blog-post h3 {
      margin-top: 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Programme d'Immigration au Canada</h1>
    <p>Ouvrez la porte à de nouvelles opportunités</p>
  </header>

  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#pourquoi">Pourquoi le Canada</a>
    <a href="#blog">Blog</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="accueil">
    <h2>Bienvenue</h2>
    <p>Notre programme vous aide à immigrer légalement et efficacement au Canada. Bénéficiez d’un accompagnement professionnel tout au long du processus.</p>

    <div class="carousel">
      <div class="carousel-images" id="carouselImages">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Flag_of_Canada_%28Pantone%29.svg" alt="Canada 1">
        <img src="https://upload.wikimedia.org/wikipedia/commons/e/e0/Ottawa_-_ON_-_Parliament_Hill3.jpg" alt="Canada 2">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/44/Toronto_skyline_from_Centre_Island.jpg" alt="Canada 3">
      </div>
    </div>
  </section>

  <section id="pourquoi">
    <h2>Pourquoi immigrer au Canada ?</h2>
    <ul>
      <li>Qualité de vie exceptionnelle</li>
      <li>Opportunités économiques</li>
      <li>Santé et éducation de haut niveau</li>
      <li>Société inclusive et multiculturelle</li>
    </ul>
  </section>

  <section id="blog">
    <h2>Notre Blog</h2>
    <div class="blog-post">
      <h3>Comment bien préparer votre dossier d'immigration</h3>
      <p>Découvrez les étapes clés pour constituer un dossier solide et éviter les erreurs fréquentes.</p>
    </div>
    <div class="blog-post">
      <h3>Les métiers les plus recherchés au Canada en 2025</h3>
      <p>Infirmiers, développeurs, soudeurs... Voici les secteurs qui recrutent massivement.</p>
    </div>
    <div class="blog-post">
      <h3>Vivre au Canada : témoignages de nouveaux arrivants</h3>
      <p>Ils ont tout quitté pour une nouvelle vie. Lisez leurs histoires inspirantes.</p>
    </div>
  </section>

  <section id="contact">
    <h2>Contactez-nous</h2>
    <form onsubmit="envoyerMessage(event)">
      <input type="text" placeholder="Votre nom" required>
      <input type="email" placeholder="Votre email" required>
      <textarea placeholder="Votre message" required></textarea>
      <button type="submit">Envoyer</button>
    </form>
  </section>

  <footer>
    &copy; 2025 programmedimmigration.com - Tous droits réservés
  </footer>

  <script>
    function envoyerMessage(e) {
      e.preventDefault();
      alert("Message envoyé avec succès ! Nous vous contacterons bientôt.");
    }

    // Carrousel auto défilant
    let index = 0;
    const images = document.getElementById('carouselImages');
    const total = images.children.length;

    setInterval(() => {
      index = (index + 1) % total;
      images.style.transform = `translateX(-${index * 100}%)`;
    }, 3000);
  </script>
</body>
</html>
