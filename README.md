<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UI Website</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f9f9f9;
      color: #333;
    }

    header {
      background: #1e293b;
      color: white;
      padding: 15px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    header h1 {
      font-size: 24px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      font-weight: 500;
    }

    nav a:hover {
      text-decoration: underline;
    }

    .hero {
      text-align: center;
      padding: 100px 20px;
      background: linear-gradient(to right, #2563eb, #3b82f6);
      color: white;
    }

    .hero h2 {
      font-size: 48px;
      margin-bottom: 15px;
    }

    .hero p {
      font-size: 18px;
      margin-bottom: 30px;
    }

    .btn {
      background: white;
      color: #2563eb;
      padding: 12px 25px;
      border-radius: 6px;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
      border: none;
    }

    .btn:hover {
      background: #e2e8f0;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 60px 40px;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0px 3px 6px rgba(0,0,0,0.1);
      text-align: center;
    }

    .card h3 {
      margin-bottom: 15px;
      font-size: 20px;
      color: #2563eb;
    }

    footer {
      background: #1e293b;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 50px;
    }
  </style>
</head>
<body>

  <header>
    <h1>My UI Website</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Features</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Clean UI Design</h2>
    <p>Modern, responsive, and easy-to-use interface for your website.</p>
    <button class="btn">Get Started</button>
  </section>

  <section class="features">
    <div class="card">
      <h3>⚡ Fast</h3>
      <p>Lightweight and optimized for performance.</p>
    </div>
    <div class="card">
      <h3>🎨 Beautiful</h3>
      <p>Minimalist and modern user interface design.</p>
    </div>
    <div class="card">
      <h3>📱 Responsive</h3>
      <p>Works seamlessly on mobile, tablet, and desktop.</p>
    </div>
  </section>

  <footer>
    <p>© 2025 My UI Website. All rights reserved.</p>
  </footer>

</body>
</html>
