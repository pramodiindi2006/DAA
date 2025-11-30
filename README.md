<!-- Enhanced Next‑Gen City Design Homepage with Memes & Animations -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Next‑Gen City Design</title>
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
      animation: slideDown 1.2s ease-out;
    }

    @keyframes slideDown {
      from { transform: translateY(-100px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
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

    /* Floating Meme Animation */
    .floating-meme {
      position: absolute;
      bottom: 20px;
      right: 20px;
      width: 130px;
      animation: memeFloat 4s infinite ease-in-out;
      opacity: 0.9;
    }

    @keyframes memeFloat {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

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

    .meme-section img {
      width: 60%;
      border-radius: 20px;
      margin-top: 20px;
      box-shadow: 0 0 25px rgba(255,255,255,0.2);
      animation: memePop 1s ease-out;
    }

    @keyframes memePop {
      from { transform: scale(0.6); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    .section {
      padding: 70px 20px;
      max-width: 1100px;
      margin: auto;
    }

    .card {
      background: var(--glass);
      backdrop-filter: blur(var(--blur));
      border-radius: var(--radius);
      padding: 40px;
      margin-top: 40px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      box-shadow: 0 0 40px rgba(0, 0, 0, 0.35);
      animation: rise 1.2s ease-out;
    }

    @keyframes rise {
      from { transform: translateY(60px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    .team-grid {
      margin-top: 30px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 25px;
    }

    .team-card {
      background: rgba(255, 255, 255, 0.08);
      padding: 25px;
      border-radius: 18px;
      text-align: center;
      transition: 0.35s;
      border: 1px solid rgba(255, 255, 255, 0.15);
      position: relative;
      overflow: hidden;
      transform-style: preserve-3d;
    }

    .team-card:hover {
      transform: translateY(-12px) scale(1.07);
      box-shadow: 0 0 30px var(--accent), 0 0 60px var(--accent2);
      border-color: var(--accent);
    }

    footer {
      text-align: center;
      padding: 40px;
      opacity: 0.6;
      margin-top: 100px;
    }
  .team-box {
      display: block;
      margin-top: 15px;
      padding: 12px;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      border-radius: 14px;
      text-align: center;
      font-weight: 600;
      color: #000;
      text-decoration: none;
      transition: 0.3s;
    }

    .team-box:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px var(--accent2);
      color: #fff;
    }

.team-card {
      background: rgba(255, 255, 255, 0.08);
      padding: 25px;
      border-radius: 18px;
      text-align: center;
      transition: 0.4s ease;
      border: 1px solid rgba(255, 255, 255, 0.15);
      position: relative;
      overflow: hidden;
    }

    .team-card:hover {
      transform: translateY(-14px) scale(1.08);
      box-shadow: 0 0 25px var(--accent), 0 0 55px var(--accent2);
      border-color: var(--accent);
    }

    /* Glow Border Animation */
    .team-card::before {
      content: "";
      position: absolute;
      top: -2px;
      left: -2px;
      right: -2px;
      bottom: -2px;
      z-index: -1;
      background: linear-gradient(120deg, var(--accent), var(--accent2), var(--accent));
      background-size: 300% 300%;
      border-radius: inherit;
      animation: glowMove 6s infinite linear;
      opacity: 0;
      transition: opacity 0.3s;
    }

    .team-card:hover::before {
      opacity: 1;
    }

    @keyframes glowMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Smooth Fade-in Sections */
    .section {
      animation: fadeSection 1.2s ease-out;
    }

    @keyframes fadeSection {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

/* Parallax Hero Background */
    .hero {
      background: url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?q=80&w=1920') center/cover fixed;
      border-bottom: 2px solid rgba(255,255,255,0.1);
    }

    /* Floating Particles */
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
      z-index: -1;
    }

    .particle {
      position: absolute;
      width: 6px;
      height: 6px;
      background: var(--accent);
      border-radius: 50%;
      opacity: 0.7;
      animation: floatUp linear infinite;
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 0.2; }
      100% { transform: translateY(-120vh); opacity: 1; }
    }

/* 3D Flip Card Effect */
    .team-card {
      perspective: 1200px;
      position: relative;
      padding: 0;
      height: 220px;
    }

    .team-card-inner {
      position: absolute;
      width: 100%;
      height: 100%;
      transition: transform 0.9s;
      transform-style: preserve-3d;
      border-radius: 18px;
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.2);
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(12px);
    }

    .team-card:hover .team-card-inner {
      transform: rotateY(180deg);
    }

    .card-front, .card-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .card-front h3, .card-back h3 { margin-bottom: 10px; }

    .card-back {
      transform: rotateY(180deg);
      background: linear-gradient(120deg, var(--accent), var(--accent2));
      color: #000;
    }

</style>
</head>

<body>

  <!-- Particle Container -->
  <div class="particles" id="particles"></div>
  <header>
    <div class="logo">CITY DESIGN</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#course">Course</a>
      <a href="#about">About</a>
      <a href="#team">Team</a>
    </nav>
  </header>

  <!-- About Section Added -->
  <section class="section" id="about">
    <div class="card">
      <h2>🌆 About the Project</h2><br>
      <p>
        The <b>Next‑Gen City Design</b> project is a futuristic smart‑city model built by integrating
        key principles from the <b>Design & Analysis of Algorithms (DAA)</b> course. Our goal is to
        demonstrate how algorithmic thinking can solve real‑world urban challenges — from optimized
        traffic flow and emergency routing to resource‑efficient water management and AI‑driven waste
        collection systems.
      </p>
      <br>
      <p>
        Each subsystem in this city is represented by one team member, where we use data structures,
        graph algorithms, greedy strategies, and dynamic programming concepts to build scalable and
        efficient solutions. This mini‑project showcases how modern cities can become smarter,
        greener, and more responsive through the power of algorithms.
      </p>
    </div>
  </section>

  <!-- Existing Hero Section -->

  <section class="hero" id="home">
    <h1>Next‑Gen City Design</h1>
    <p>A futuristic, algorithm‑driven smart city model with creativity & modern animations.</p>
  </section>

  <section class="section" id="course">
    <div class="card">
      <h2>📘 Course Information</h2><br>
      <p><b>Course:</b> Design & Analysis of Algorithms — 24ECSC205</p>
      <p><b>Instructor:</b> Prof. Prakash Hegade</p>
      <p><b>University:</b> KLE Technological University</p>
      <p><b>Topic:</b> Smart City Design using Algorithms</p>
    </div>
  </section>

  <section class="section" id="team">
    <div class="card">
      <h2>👥 Team Members</h2>

      <div class="team-grid">
        <!-- Team Card 1 -->
        <div class="team-card">
          <div class="team-card-inner">
            <div class="card-front">
              <div class="avatar"></div>
              <h3>Pramod S Indi</h3>
              <p>Smart Traffic Optimization System</p>
              <a class="team-box" href="pramod.html">Open Project Page</a>
            </div>
            <div class="card-back">
              <h3>Pramod S Indi</h3>
              <p>Details & Resources</p>
              <a class="team-box" href="pramod.html">View Page</a>
            </div>
          </div>
        </div>

        <!-- Team Card 2 -->
        <div class="team-card">
          <div class="team-card-inner">
            <div class="card-front">
              <div class="avatar"></div>
              <h3>Parvatappa J Wani</h3>
              <p>Smart Water Management System</p>
              <a class="team-box" href="parvatappa.html">Open Project Page</a>
            </div>
            <div class="card-back">
              <h3>Parvatappa J Wani</h3>
              <p>Details & Resources</p>
              <a class="team-box" href="parvatappa.html">View Page</a>
            </div>
          </div>
        </div>

        <!-- Team Card 3 -->
        <div class="team-card">
          <div class="team-card-inner">
            <div class="card-front">
              <div class="avatar"></div>
              <h3>Sujal S Gowda</h3>
              <p>Emergency Response Routing</p>
              <a class="team-box" href="sujal.html">Open Project Page</a>
            </div>
            <div class="card-back">
              <h3>Sujal S Gowda</h3>
              <p>Details & Resources</p>
              <a class="team-box" href="sujal.html">View Page</a>
            </div>
          </div>
        </div>

        <!-- Team Card 4 -->
        <div class="team-card">
          <div class="team-card-inner">
            <div class="card-front">
              <div class="avatar"></div>
              <h3>Santosh Chikaraddi</h3>
              <p>AI‑Driven Waste Collection & Routing</p>
              <a class="team-box" href="santosh.html">Open Project Page</a>
            </div>
            <div class="card-back">
              <h3>Santosh Chikaraddi</h3>
              <p>Details & Resources</p>
              <a class="team-box" href="santosh.html">View Page</a>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <footer>
    © 2025 Next-Gen City Design — DAA Project
  </footer>
    © 2025 Next-Gen City Design — DAA Project
  </footer>

<script>
    // Generate Floating Particles
    const container = document.getElementById('particles');
    for (let i = 0; i < 40; i++) {
      const dot = document.createElement('div');
      dot.classList.add('particle');
      dot.style.left = Math.random() * 100 + 'vw';
      dot.style.bottom = '-20px';
      dot.style.animationDuration = 10 + Math.random() * 15 + 's';
      dot.style.animationDelay = Math.random() * 5 + 's';
      container.appendChild(dot);
    }
  </script>

</body>
</html>
