<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>City Design — Futuristic UI</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-dark: #0c0f1a;
      --bg-card: rgba(255, 255, 255, 0.08);
      --glass: rgba(255, 255, 255, 0.16);
      --accent: #00eaff;
      --accent2: #9c59ff;
      --text-light: #e8e8e8;
      --radius: 18px;
      --blur: 18px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: radial-gradient(circle at top, #1b2238, #090b14 70%);
      color: var(--text-light);
      overflow-x: hidden;
    }

    /* ===================== NAVBAR ===================== */
    header {
      width: 100%;
      padding: 22px 50px;
      position: fixed;
      top: 0;
      left: 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
      backdrop-filter: blur(18px);
      background: rgba(255, 255, 255, 0.04);
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
      z-index: 999;
    }

    .logo {
      font-size: 28px;
      font-weight: 800;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: 1px;
    }

    nav a {
      margin: 0 16px;
      text-decoration: none;
      font-weight: 400;
      color: var(--text-light);
      transition: 0.25s;
    }

    nav a:hover {
      color: var(--accent);
      text-shadow: 0 0 12px var(--accent);
    }

    /* ===================== HERO ===================== */
    .hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 0 20px;
      position: relative;
    }

    .hero h1 {
      font-size: 4rem;
      font-weight: 800;
      margin-bottom: 15px;
      background: linear-gradient(90deg, #fff, var(--accent));
      -webkit-background-clip: text;
      color: transparent;
      animation: float 4s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-18px); }
    }

    .hero p {
      max-width: 650px;
      font-size: 1.1rem;
      opacity: 0.85;
    }

    /* Floating Neon Orb */
    .orb {
      position: absolute;
      width: 320px;
      height: 320px;
      background: radial-gradient(circle, var(--accent2), transparent 70%);
      top: -50px;
      left: -50px;
      filter: blur(60px);
      animation: rotate 12s linear infinite;
      opacity: 0.45;
    }

    .orb2 {
      position: absolute;
      width: 300px;
      height: 300px;
      background: radial-gradient(circle, var(--accent), transparent 80%);
      bottom: -40px;
      right: -40px;
      filter: blur(70px);
      animation: rotate 14s linear infinite reverse;
      opacity: 0.35;
    }

    @keyframes rotate {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    /* ===================== CARD SECTION ===================== */
    .section {
      padding: 120px 40px;
      max-width: 1100px;
      margin: auto;
    }

    .card {
      background: var(--glass);
      backdrop-filter: blur(var(--blur));
      border-radius: var(--radius);
      padding: 40px;
      margin-top: 50px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      box-shadow: 0 0 40px rgba(0, 0, 0, 0.35);
      animation: rise 1.2s ease-out;
    }

    @keyframes rise {
      from { transform: translateY(60px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 25px;
    }

    th, td {
      padding: 16px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.15);
      text-align: center;
    }

    th {
      color: var(--accent);
      font-size: 1.1rem;
    }

    /* ===================== FOOTER ===================== */
    footer {
      text-align: center;
      padding: 40px;
      opacity: 0.6;
      margin-top: 100px;
    }
  </style>
</head>

<body>
  <header>
    <div class="logo">CITY DESIGN</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#course">Course</a>
      <a href="#team">Team</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- HERO SECTION -->
  <section class="hero" id="home">
    <div class="orb"></div>
    <div class="orb2"></div>
    <h1>Next-Gen City Design</h1>
    <p>A futuristic portfolio showcasing modern UI, neon effects, glassmorphism, animations, and immersive visuals for your DAA project.</p>
  </section>

  <!-- COURSE SECTION -->
  <section class="section" id="course">
    <div class="card">
      <h2>📘 Course Information</h2>
      <p><strong>Course:</strong> DAA (Design & Analysis of Algorithms)</p>
      <p><strong>Course Code:</strong> 24ECSC205</p>
      <p><strong>Instructor:</strong> Prof. Prakash Hegade</p>
      <p><strong>University:</strong> KLE Technological University</p>
      <p><strong>Topic:</strong> City Design</p>
    </div>
  </section>

  <!-- TEAM SECTION -->
  <section class="section" id="team">
    <div class="card">
      <h2>👥 Team Members</h2>
      <table>
        <tr><th>Name</th><th>USN</th></tr>
        <tr><td>Amogh Pai</td><td>01fe23bcs217</td></tr>
        <tr><td>Bhoomika Malagar</td><td>01fe23bcs216</td></tr>
        <tr><td>Saanvi Shetty</td><td>01fe23bcs227</td></tr>
        <tr><td>Ramya Rao</td><td>01fe23bcs243</td></tr>
      </table>
    </div>
  </section>

  <footer id="contact">© 2025 City Design Project — Built with Futuristic UI</footer>
</body>
</html>
