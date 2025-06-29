# AdminAI
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Admin AI - Professional AI Solutions</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #7c3aed; /* Purple */
      --bg-color: #000000;
      --text-color: #ffffff;
      --secondary-color: #1f1f1f;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg-color);
      color: var(--text-color);
      font-family: 'Poppins', sans-serif;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: var(--secondary-color);
      padding: 20px 40px;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      font-weight: 600;
      color: var(--primary-color);
      font-size: 1.8em;
    }

    nav {
      display: flex;
      gap: 20px;
    }

    nav a {
      text-decoration: none;
      color: var(--text-color);
      font-weight: 500;
      transition: color 0.3s;
    }

    nav a:hover {
      color: var(--primary-color);
    }

    section {
      padding: 80px 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .hero {
      text-align: center;
      padding-top: 60px;
    }

    .hero h2 {
      font-size: 3em;
      margin-bottom: 20px;
      background: linear-gradient(90deg, var(--primary-color), #a78bfa);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: fadeIn 2s ease forwards;
      opacity: 0;
    }

    .hero p {
      font-size: 1.2em;
      max-width: 700px;
      margin: 20px auto;
      color: #d1d5db;
    }

    .section-title {
      font-size: 2.5em;
      color: var(--primary-color);
      margin-bottom: 30px;
      text-align: center;
    }

    .categories, .creativity {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }

    .card {
      background: var(--secondary-color);
      padding: 30px;
      border-radius: 8px;
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
    }

    .card h3 {
      color: var(--primary-color);
      margin-bottom: 15px;
    }

    .card p {
      color: #d1d5db;
      font-size: 0.95em;
    }

    form {
      background: var(--secondary-color);
      padding: 30px;
      border-radius: 8px;
      max-width: 600px;
      margin: 0 auto;
    }

    form input, form textarea {
      width: 100%;
      padding: 15px;
      margin-bottom: 20px;
      border: none;
      border-radius: 5px;
      font-size: 1em;
      background: #333;
      color: var(--text-color);
    }

    form button {
      background: var(--primary-color);
      color: var(--text-color);
      border: none;
      padding: 15px 30px;
      font-size: 1em;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    form button:hover {
      background: #a78bfa;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: var(--secondary-color);
      color: #d1d5db;
      margin-top: 50px;
    }

    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(30px); }
      100% { opacity: 1; transform: translateY(0);}
    }

    @media (max-width: 768px) {
      .hero h2 {
        font-size: 2.2em;
      }
      .section-title {
        font-size: 2em;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>AdminAI</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#categories">Categories</a>
      <a href="#creativity">Our Creativity</a>
      <a href="#contact">Contact Us</a>
    </nav>
  </header>

  <section id="home" class="hero">
    <h2 id="welcome-text">Welcome - Get a Professional Website</h2>
    <p>We build powerful AI-driven solutions and modern websites that help businesses thrive in the digital era.</p>
  </section>

  <section id="categories">
    <h2 class="section-title">Categories</h2>
    <div class="categories">
      <div class="card">
        <h3>AI Agents</h3>
        <p>Custom-built AI agents tailored to specific industries and processes.</p>
      </div>
      <div class="card">
        <h3>Web Development</h3>
        <p>Modern, responsive websites built with cutting-edge technology.</p>
      </div>
      <div class="card">
        <h3>Automation</h3>
        <p>Streamline workflows with intelligent automation solutions.</p>
      </div>
    </div>
  </section>

  <section id="creativity">
    <h2 class="section-title">Our Creativity</h2>
    <div class="creativity">
      <div class="card">
        <h3>Innovative Design</h3>
        <p>We blend aesthetic design with functionality to create stunning digital experiences.</p>
      </div>
      <div class="card">
        <h3>Smart Solutions</h3>
        <p>From smart bots to intelligent apps, our solutions solve real business challenges.</p>
      </div>
      <div class="card">
        <h3>Future-Ready</h3>
        <p>Our technologies are built to scale and adapt as your business grows.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2 class="section-title">Contact Us</h2>
    <form action="#" method="post">
      <input type="text" name="name" placeholder="Your Name" required/>
      <input type="email" name="email" placeholder="Your Email" required/>
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    &copy; 2025 AdminAI. All rights reserved.
  </footer>

  <script>
    // Simple typewriter animation for welcome text
    const text = "Welcome - Get a Professional Website";
    const el = document.getElementById('welcome-text');
    let index = 0;
    el.textContent = "";

    function typeWriter() {
      if (index < text.length) {
        el.textContent += text.charAt(index);
        index++;
        setTimeout(typeWriter, 50);
      }
    }
    window.onload = typeWriter;
  </script>
</body>
</html>
