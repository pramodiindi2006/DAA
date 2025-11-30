<!-- Compact & Enhanced Next‑Gen City Design Homepage -->
<!-- NOTE: Your full upgraded version with reduced spacing, vertical layout, advanced animations/effects -->

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Next‑Gen City Design</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">

<style>
  :root {
    --bg-dark: #06070e;
    --accent: #00eaff;
    --accent2: #b05bff;
    --glass: rgba(255,255,255,0.12);
    --radius: 16px;
  }

  * { margin:0; padding:0; box-sizing:border-box; font-family:Poppins, sans-serif; }
  body {
    background: linear-gradient(160deg,#0b0f19,#020309);
    color: #e9e9e9;
    overflow-x:hidden;
  }

  /* HEADER */
  header {
    position:fixed; top:0; left:0; width:100%; padding:14px 32px;
    background:rgba(255,255,255,0.05); backdrop-filter:blur(14px);
    border-bottom:1px solid rgba(255,255,255,0.1);
    z-index:999; display:flex; justify-content:space-between; align-items:center;
    animation:fadeDown 0.8s ease;
  }
  @keyframes fadeDown { from{opacity:0; transform:translateY(-40px);} to{opacity:1; transform:translateY(0);} }

  .logo {
    font-size:26px; font-weight:800;
    background:linear-gradient(90deg,#fff,var(--accent)); -webkit-background-clip:text; color:transparent;
  }

  nav a {
    margin:0 10px; text-decoration:none; color:#eaeaea; font-weight:300;
    transition:0.2s;
  }
  nav a:hover { color:var(--accent); }

  /* SIMPLE VERTICAL COMPACT SECTION */
  .section {
    width:100%; max-width:900px; margin:70px auto 40px auto; padding:25px;
    background:var(--glass); backdrop-filter:blur(12px);
    border-radius:var(--radius);
    border:1px solid rgba(255,255,255,0.12);
    animation:fadeIn 0.9s ease;
  }
  @keyframes fadeIn { from{opacity:0; transform:translateY(40px);} to{opacity:1; transform:translateY(0);} }

  h2 { margin-bottom:8px; }
  p { line-height:1.45; opacity:0.9; }

  /* HERO */
  .hero {
    height:70vh; margin-top:80px;
    display:flex; flex-direction:column; justify-content:center; align-items:center;
    text-align:center; padding:10px;
    background:url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?q=80&w=1920') center/cover fixed;
    border-bottom:1px solid rgba(255,255,255,0.08);
  }
  .hero h1 {
    font-size:3rem; background:linear-gradient(90deg,#fff,var(--accent));
    -webkit-background-clip:text; color:transparent;
    animation:fadePop 1s ease;
  }
  @keyframes fadePop{from{opacity:0; transform:scale(0.7);}to{opacity:1; transform:scale(1);}}

  /* CITY IMAGE VERTICAL */
  .city-img {
    width:100%; border-radius:16px; margin-top:12px;
    box-shadow:0 0 20px rgba(0,0,0,0.5);
    animation:slideUp 1s ease;
  }
  @keyframes slideUp { from{opacity:0; transform:translateY(40px);} to{opacity:1; transform:translateY(0);} }

  /* TEAM GRID (COMPACT) */
  .team-grid {
    display:grid; grid-template-columns:1fr 1fr; gap:18px; margin-top:14px;
  }
  .team-card {
    background:rgba(255,255,255,0.08); padding:18px; border-radius:14px;
    border:1px solid rgba(255,255,255,0.15); text-align:center;
    transition:0.3s; position:relative;
  }
  .team-card:hover {
    transform:translateY(-5px);
    box-shadow:0 0 25px var(--accent);
  }

  .team-box {
    display:inline-block; margin-top:10px; padding:8px 14px;
    background:linear-gradient(90deg,var(--accent),var(--accent2));
    border-radius:12px; color:#000; text-decoration:none;
    font-weight:600; font-size:0.9rem;
    transition:0.3s;
  }
  .team-box:hover { transform:scale(1.05); color:#fff; }

  footer { text-align:center; opacity:0.6; padding:30px; margin-top:20px; }

  /* ADVANCED FLOATING PARTICLES */
  .particles { position:fixed; top:0; left:0; width:100%; height:100%; pointer-events:none; overflow:hidden; z-index:-1; }
  .particle {
    position:absolute; width:4px; height:4px; background:var(--accent);
    border-radius:50%; opacity:0.7;
    animation:floatUp linear infinite;
  }
  @keyframes floatUp { from{transform:translateY(40vh);} to{transform:translateY(-120vh);} }
</style>
</head>

<body>
<div class="particles" id="particles"></div>

<header>
  <div class="logo">CITY DESIGN</div>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#city">City</a>
    <a href="#team">Team</a>
  </nav>
</header>

<section class="hero" id="home">
  <h1>Next‑Gen City Design</h1>
  <p>Compact, vertical, futuristic — powered by DAA algorithms.</p>
</section>

<section class="section" id="about">
  <h2>🌆 About the Project</h2>
  <p>
    This upgraded smart‑city model integrates <b>DAA algorithms</b> for traffic optimization,
    water distribution, emergency routing, and AI‑driven waste collection. Now redesigned in a
    compact vertical layout with advanced animations.
  </p>
</section>

<section class="section" id="city">
  <h2>🏙️ City Layout (Vertical)</h2>
  <p>The city map is preserved exactly as requested — placed in a taller vertical frame.</p>
  <img src="city.jpg" class="city-img">
</section>

<section class="section" id="team">
  <h2>👥 Team Members</h2>
  <div class="team-grid">

    <div class="team-card">
      <h3>Pramod S Indi</h3>
      <p>Smart Traffic Optimization</p>
      <a href="pramod.html" class="team-box">Open</a>
    </div>

    <div class="team-card">
      <h3>Parvatappa J Wani</h3>
      <p>Smart Water System</p>
      <a href="parvatappa.html" class="team-box">Open</a>
    </div>

    <div class="team-card">
      <h3>Sujal S Gowda</h3>
      <p>Emergency Routing</p>
      <a href="sujal.html" class="team-box">Open</a>
    </div>

    <div class="team-card">
      <h3>Santosh Chikaraddi</h3>
      <p>AI Waste Collection</p>
      <a href="santosh.html" class="team-box">Open</a>
    </div>

  </div>
</section>

<footer>© 2025 Next‑Gen City Design — DAA Project</footer>

<script>
  // Advanced Floating Particles (More, Faster, Dynamic)
  const particles = document.getElementById('particles');
  for (let i = 0; i < 60; i++) {
    const p = document.createElement('div');
    p.classList.add('particle');
    p.style.left = Math.random()*100 + 'vw';
    p.style.top = Math.random()*100 + 'vh';
    p.style.animationDuration = (6 + Math.random()*10) + 's';
    p.style.opacity = 0.3 + Math.random()*0.7;
    particles.appendChild(p);
  }
</script>

</body>
</html>
