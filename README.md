# 4Set-Up-ss
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RGB Setup Store</title>
  <link rel="stylesheet" href="styles.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
</head>
<body>
  <header class="header">
    <h1 class="logo">RGB Setup Store</h1>
    <nav>
      <ul class="nav-links">
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Productos</a></li>
        <li><a href="#">Ofertas</a></li>
        <li><a href="#">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h2>Haz tu setup más épico 🔥</h2>
    <p>Luces RGB, accesorios y todo lo que necesitas para tu espacio gamer, sin gastar una fortuna.</p>
    <button class="btn">Ver productos</button>
  </section>

  <section class="productos">
    <h2>Productos Destacados</h2>
    <div class="grid">
      <div class="card">
        <img src="https://cdn.pixabay.com/photo/2020/09/07/21/46/rgb-light-5552498_1280.jpg" alt="Luces RGB">
        <h3>Luces RGB</h3>
        <p class="precio">€19.99</p>
        <button class="btn">Comprar</button>
      </div>
      <div class="card">
        <img src="https://cdn.pixabay.com/photo/2019/10/25/14/23/keyboard-4573110_1280.jpg" alt="Alfombrilla Gamer">
        <h3>Alfombrilla Gamer XL</h3>
        <p class="precio">€14.99</p>
        <button class="btn">Comprar</button>
      </div>
      <div class="card">
        <img src="https://cdn.pixabay.com/photo/2016/11/29/13/02/monitor-1869656_1280.jpg" alt="Brazo para monitor">
        <h3>Brazo para Monitor</h3>
        <p class="precio">€29.99</p>
        <button class="btn">Comprar</button>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 RGB Setup Store | Hecho con 💜 por gamers, para gamers</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  font-family: 'Orbitron', sans-serif;
  background: radial-gradient(circle at top, #0a0a0f, #050505);
  color: #fff;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: rgba(0, 0, 0, 0.6);
  border-bottom: 2px solid #0ff;
  box-shadow: 0 0 20px #0ff;
}

.logo {
  color: #0ff;
  text-shadow: 0 0 10px #0ff;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  transition: 0.3s;
}

.nav-links a:hover {
  color: #0ff;
  text-shadow: 0 0 5px #0ff;
}

.hero {
  text-align: center;
  padding: 5rem 2rem;
  background: linear-gradient(180deg, rgba(0,255,255,0.1), rgba(255,0,255,0.05));
}

.hero h2 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: #0ff;
  text-shadow: 0 0 20px #0ff;
}

.btn {
  background: linear-gradient(90deg, #0ff, #f0f);
  border: none;
  color: #fff;
  padding: 0.8rem 2rem;
  font-size: 1rem;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s;
  box-shadow: 0 0 20px #0ff;
}

.btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 30px #f0f;
}

.productos {
  text-align: center;
  padding: 3rem 2rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.card {
  background: rgba(255,255,255,0.05);
  border-radius: 15px;
  padding: 1rem;
  box-shadow: 0 0 15px rgba(0,255,255,0.3);
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 25px #f0f;
}

.card img {
  width: 100%;
  border-radius: 10px;
}

.precio {
  color: #0ff;
  font-size: 1.2rem;
}

footer {
  text-align: center;
  padding: 2rem;
  background: rgba(0,0,0,0.7);
  border-top: 2px solid #f0f;
}
// Efecto sutil RGB al pasar el ratón por botones
document.querySelectorAll('.btn').forEach(btn => {
  btn.addEventListener('mousemove', e => {
    const x = e.offsetX;
    const y = e.offsetY;
    btn.style.background = `radial-gradient(circle at ${x}px ${y}px, #0ff, #f0f)`;
  });
  btn.addEventListener('mouseleave', () => {
    btn.style.background = 'linear-gradient(90deg, #0ff, #f0f)';
  });
});
