<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Beautiful UI Website</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Segoe UI", sans-serif;
    }

    body {
      background: linear-gradient(135deg, #3b82f6, #9333ea);
      color: #fff;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      backdrop-filter: blur(15px);
      background: rgba(255, 255, 255, 0.1);
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-radius: 0 0 20px 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
    }

    header h1 {
      font-size: 24px;
      font-weight: bold;
    }

    nav a {
      color: #fff;
      margin-left: 20px;
      text-decoration: none;
      font-weight: 500;
      transition: 0.3s;
    }

    nav a:hover {
      color: #ffe082;
    }

    .hero {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 60px 20px;
    }

    .hero h2 {
      font-size: 52px;
      font-weight: 700;
      margin-bottom: 20px;
      text-shadow: 0px 3px 10px rgba(0,0,0,0.3);
    }

    .hero p {
      font-size: 18px;
      max-width: 600px;
      margin-bottom: 30px;
      line-height: 1.6;
    }

    .btn {
      background: linear-gradient(135deg, #06b6d4, #3b82f6);
      padding: 15px 35px;
      border-radius: 30px;
      border: none;
      color: white;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0px 4px 15px rgba(0,0,0,0.2);
      transition: transform 0.2s;
    }

    .btn:hover {
      transform: scale(1.05);
    }

    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
      padding: 60px 40px;
    }

    .card {
      backdrop-filter: blur(20px);
      background: rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      padding: 40px 25px;
      text-align: center;
      box-shadow: 0 8px 25px rgba(0,0,0,0.3);
      transition: transform 0.3s, background 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
      background: rgba(255, 255, 255, 0.25);
    }

    .card h3 {
      font-size: 22px;
      margin-bottom: 15px;
      color: #ffe082;
    }

    .card p {
      font-size: 16px;
      line-height: 1.5;
      color: #f3f4f6;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0,0,0,0.3);
      border-radius: 20px 20px 0 0;
      font-size: 14px;
      backdrop-filter: blur(10px);
    }
  </style>
</head>
<body>

  <header>
    <h1>✨ Surface UI</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Features</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Beautiful Surface Design</h2>
    <p>
      A modern, glassmorphic UI design with depth, shadows, and smooth gradients.  
      Inspired by clean Surface-style aesthetics for web applications.
    </p>
    <button class="btn">Get Started</button>
  </section>

  <section class="features">
    <div class="card">
      <h3>⚡ Fast Performance</h3>
      <p>Optimized with lightweight design for smooth user experience.</p>
    </div>
    <div class="card">
      <h3>🎨 Modern Aesthetics</h3>
      <p>Glassmorphism, gradients, and smooth shadows create a premium feel.</p>
    </div>
    <div class="card">
      <h3>📱 Fully Responsive</h3>
      <p>Adapts seamlessly to mobile, tablet, and desktop devices.</p>
    </div>
  </section>

  <footer>
    <p>© 2025 Surface UI Website. All Rights Reserved.</p>
  </footer>

</body>
</html>
