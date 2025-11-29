
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

    .team-card .avatar {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      background: radial-gradient(circle, var(--accent2), transparent);
      margin: auto;
      margin-bottom: 15px;
      box-shadow: 0 0 12px var(--accent2);
    }

    .team-card a {
      margin-top: 10px;
      display: inline-block;
      padding: 8px 14px;
      border-radius: 14px;
      background: var(--accent);
      color: #000;
      font-weight: 600;
      text-decoration: none;
      transition: 0.3s;
    }

    .team-card a:hover {
      background: var(--accent2);
      color: #fff;
    }

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
    </nav>
  </header>

  <section class="hero" id="home">
    <h1>Next‑Gen City Design</h1>
    <p>A futuristic, algorithm‑driven smart city model built using Design & Analysis of Algorithms.</p>
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
      <div class="team-card">
          <div class="avatar"></div>
          <h3>Pramod S Indi</h3>
          <p>Smart Traffic Optimization System</p>
          <a href="pramod.html">View Page</a>
        </div>

   <div class="team-card">
          <div class="avatar"></div>
          <h3>Parvatappa J Wani</h3>
          <p>Smart Water Management System</p>
          <a href="parvatappa.html">View Page</a>
        </div>

   <div class="team-card">
          <div class="avatar"></div>
          <h3>Sujal S Gowda</h3>
          <p>Emergency Response Routing</p>
          <a href="sujal.html">View Page</a>
        </div>
        <div class="team-card">
          <div class="avatar"></div>
          <h3>Santosh Chikaraddi</h3>
          <p>AI-Driven Waste Collection & Routing</p>
          <a href="santosh.html">View Page</a>
        </div>

   </div>
    </div>
  </section>

  <footer>
    © 2025 Next-Gen City Design — Built for DAA Project
  </footer>

</body>
</html>






<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pramod – Smart Traffic Optimization</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-dark: #0c0f1a;
      --glass: rgba(255, 255, 255, 0.16);
      --accent: #00eaff;
      --accent2: #9c59ff;
      --text-light: #e8e8e8;
      --radius: 18px;
      --blur: 18px;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: "Poppins", sans-serif; }
    body {
      background: radial-gradient(circle at top, #1b2238, #090b14 70%);
      color: var(--text-light);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
    .card {
      max-width: 900px;
      width: 100%;
      background: var(--glass);
      backdrop-filter: blur(var(--blur));
      border-radius: var(--radius);
      padding: 40px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      box-shadow: 0 0 40px rgba(0, 0, 0, 0.35);
    }
    .badge {
      display: inline-block;
      padding: 6px 14px;
      border-radius: 999px;
      background: rgba(0, 234, 255, 0.1);
      color: var(--accent);
      font-size: 0.8rem;
      margin-bottom: 12px;
    }
    h1 {
      font-size: 2.4rem;
      margin-bottom: 6px;
      background: linear-gradient(90deg, #fff, var(--accent));
      -webkit-background-clip: text;
      color: transparent;
    }
    h2 { margin-top: 24px; margin-bottom: 8px; font-size: 1.3rem; }
    p { margin-bottom: 8px; opacity: 0.9; }
    ul { margin-left: 18px; margin-top: 6px; }
    li { margin-bottom: 4px; }
    .back-link {
      margin-top: 24px;
      display: inline-block;
      padding: 8px 16px;
      border-radius: 16px;
      background: var(--accent);
      color: #000;
      font-weight: 600;
      text-decoration: none;
    }
    .back-link:hover { background: var(--accent2); color: #fff; }
  </style>
</head>
<body>
  <main class="card">
    <span class="badge">Next‑Gen City Design · DAA Project</span>
    <h1>Pramod S Indi</h1>
    <p><b>Module:</b> Smart Traffic Optimization System</p>
    <h2>Problem Statement</h2>
  <p>Describe the traffic congestion problem your module focuses on, such as peak‑hour jams, long waiting times at signals, or inefficient routing.</p>

  <h2>Algorithms Used</h2>
    <ul>
      <li>Shortest path (e.g., Dijkstra / BFS) for real‑time route suggestions.</li>
      <li>Greedy or dynamic programming logic for adaptive signal timing.</li>
      <li>Graph modelling of city junctions and roads.</li>
    </ul>
  <h2>Key Features</h2>
    <ul>
      <li>Dynamic green‑time allocation based on live traffic density.</li>
      <li>Priority routes for ambulances and emergency vehicles.</li>
      <li>Dashboard to visualize congestion heatmaps.</li>
    </ul>

   <h2>Time & Space Complexity</h2>
  <p>Explain complexity of your core algorithms, for example Dijkstra running in \(O(E \log V)\) time and \(O(V)\) space.</p>

  <a href="index.html" class="back-link">← Back to Home</a>
  </main>
</body>
</html>




