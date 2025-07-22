<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pastelería Dulce Tentación</title>
  <style>
    /* RESET */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #fff8f0;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #ff6f61;
      color: white;
      text-align: center;
      padding: 30px 20px;
    }

    header h1 {
      font-size: 3rem;
    }

    nav {
      background-color: #ffb347;
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 10px 0;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #333;
    }

    main {
      max-width: 1200px;
      margin: 20px auto;
      padding: 0 20px;
    }

    .search-container {
      text-align: center;
      margin-bottom: 30px;
    }

    .search-container input {
      width: 60%;
      padding: 10px;
      font-size: 1rem;
      border: 2px solid #ffb347;
      border-radius: 5px;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .card {
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .card-body {
      padding: 15px;
    }

    .card-body h3 {
      color: #ff6f61;
      margin-bottom: 10px;
    }

    .card-body p {
      margin-bottom: 10px;
    }

    .price {
      font-weight: bold;
      color: #4CAF50;
    }

    footer {
      background-color: #ff6f61;
      color: white;
      text-align: center;
      padding: 20px 10px;
      margin-top: 40px;
    }

    /* FORMULARIO */
    .contact-form {
      margin-top: 40px;
      background: #ffe5d9;
      padding: 20px;
      border-radius: 10px;
    }

    .contact-form h2 {
      margin-bottom: 15px;
      color: #ff6f61;
    }

    .contact-form input, .contact-form textarea, .contact-form button {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      border: 1px solid #ddd;
      border-radius: 5px;
      font-size: 1rem;
    }

    .contact-form button {
      background-color: #ffb347;
      color: white;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .contact-form button:hover {
      background-color: #ff6f61;
    }
  </style>
</head>
<body>
  <header>
    <h1>Pastelería Dulce Tentación</h1>
    <p>Delicias artesanales para cada ocasión</p>
  </header>

  <nav>
    <a href="#productos">Productos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <main>
    <div class="search-container">
      <input type="text" id="search" placeholder="Buscar productos...">
    </div>

    <section id="productos" class="products">
      <!-- Productos -->
      <div class="card">
        <img src="https://via.placeholder.com/300x180?text=Pastel+Chocolate" alt="Pastel de Chocolate">
        <div class="card-body">
          <h3>Pastel de Chocolate</h3>
          <p>Bizcocho húmedo con ganache de chocolate belga y fresas frescas.</p>
          <p class="price">$350 MXN</p>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180?text=Cheesecake+Frutos+Rojos" alt="Cheesecake de Frutos Rojos">
        <div class="card-body">
          <h3>Cheesecake Frutos Rojos</h3>
          <p>Base crujiente de galleta, relleno cremoso y topping de frutos rojos.</p>
          <p class="price">$280 MXN</p>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180?text=Brownies+de+Nuez" alt="Brownies de Nuez">
        <div class="card-body">
          <h3>Brownies de Nuez</h3>
          <p>Intensos en chocolate, con nueces caramelizadas en la superficie.</p>
          <p class="price">$50 MXN c/u</p>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180?text=Cupcakes+Varios" alt="Cupcakes">
        <div class="card-body">
          <h3>Cupcakes Surtidos</h3>
          <p>Pack de 6 cupcakes de vainilla, chocolate y red velvet con decoración.</p>
          <p class="price">$180 MXN</p>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180?text=Macarons" alt="Macarons">
        <div class="card-body">
          <h3>Macarons</h3>
          <p>Coloridos y delicados macarons franceses en caja de 12 piezas.</p>
          <p class="price">$250 MXN</p>
        </div>
      </div>
    </section>

    <section id="contacto" class="contact-form">
      <h2>Contáctanos</h2>
      <form>
        <input type="text" placeholder="Tu nombre" required>
        <input type="email" placeholder="Tu correo" required>
        <textarea rows="5" placeholder="Tu mensaje o pedido..." required></textarea>
        <button type="submit">Enviar mensaje</button>
      </form>
    </section>
  </main>

  <footer>
    <p>© 2025 Pastelería Dulce Tentación | Todos los derechos reservados</p>
  </footer>

  <script>
    // Buscador en vivo
    const searchInput = document.getElementById('search');
    searchInput.addEventListener('input', () => {
      const filter = searchInput.value.toLowerCase();
      const cards = document.querySelectorAll('.card');
      cards.forEach(card => {
        const text = card.innerText.toLowerCase();
        card.style.display = text.includes(filter) ? '' : 'none';
      });
    });
  </script>
</body>
</html>
