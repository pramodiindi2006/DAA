<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Next-Gen City Design</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">

<style>
:root{
  --accent:#00eaff;--accent2:#9c59ff;--txt:#eaeaea;
}
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins,sans-serif;scroll-behavior:smooth;}
body{
  background:#0b0e17;color:var(--txt);overflow-x:hidden;position:relative;
}

/* Header */
header{
  position:fixed;top:0;left:0;width:100%;
  padding:14px 40px;display:flex;justify-content:space-between;align-items:center;
  backdrop-filter:blur(12px);background:rgba(255,255,255,0.05);
  border-bottom:1px solid rgba(255,255,255,0.08);z-index:20;
  animation:drop 1s ease;
}
@keyframes drop{from{transform:translateY(-70px);opacity:0;}to{transform:translateY(0);opacity:1;}}
.logo{
  font-size:26px;font-weight:800;
  background:linear-gradient(90deg,var(--accent),var(--accent2));
  -webkit-background-clip:text;color:transparent;
}
nav a{
  margin:0 12px;color:var(--txt);text-decoration:none;
  transition:.3s;font-size:0.95rem;
}
nav a:hover{color:var(--accent);text-shadow:0 0 12px var(--accent);}

/* Hero */
.hero{
  height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;
  background:url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?q=80&w=1920') center/cover fixed;
  position:relative;overflow:hidden;
}
.hero h1{
  font-size:3.3rem;font-weight:800;
  background:linear-gradient(90deg,#fff,var(--accent));
  -webkit-background-clip:text;color:transparent;
  animation:fadeUp 1.2s ease;
}
.hero p{font-size:1rem;max-width:550px;opacity:0.85;margin-top:10px;}
@keyframes fadeUp{from{opacity:0;transform:translateY(30px);}to{opacity:1;transform:translateY(0);}}

/* Particle FX */
.particle{
  position:fixed;width:5px;height:5px;background:var(--accent);border-radius:50%;opacity:.7;
  animation:rise linear infinite;
}
@keyframes rise{from{transform:translateY(100vh);}to{transform:translateY(-20vh);}}

/* Sections */
.section{
  max-width:1050px;margin:auto;padding:55px 20px;
  animation:fadeSec .9s ease;
}
@keyframes fadeSec{from{opacity:0;transform:translateY(35px);}to{opacity:1;transform:translateY(0);}}

/* Cards */
.card{
  background:rgba(255,255,255,0.07);
  border:1px solid rgba(255,255,255,0.1);
  padding:32px;border-radius:16px;
  backdrop-filter:blur(14px);
  box-shadow:0 0 35px #0006;
  animation:floatIn 1s ease;
}
@keyframes floatIn{from{opacity:0;transform:translateY(40px);}to{opacity:1;transform:translateY(0);}}

/* Team Grid */
.team-grid{
  margin-top:25px;
  display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:20px;
}
.team-card{
  height:190px;perspective:1200px;position:relative;cursor:pointer;
}
.team-card-inner{
  position:absolute;width:100%;height:100%;border-radius:15px;
  transition:transform .75s;
  background:rgba(255,255,255,0.08);backdrop-filter:blur(10px);
  border:1px solid rgba(255,255,255,0.15);
}
.team-card:hover .team-card-inner{
  transform:scale(1.05) translateY(-5px);
  box-shadow:0 0 20px var(--accent2);
}
.team-card .front, .team-card .back{
  position:absolute;width:100%;height:100%;
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  padding:15px;text-align:center;
}
.team-card h3{margin-bottom:6px;font-size:1.05rem;}

.team-box{
  margin-top:10px;padding:8px 14px;border-radius:12px;
  background:linear-gradient(90deg,var(--accent),var(--accent2));color:#000;
  font-weight:600;font-size:0.9rem;text-decoration:none;
  transition:transform .3s;
}
.team-box:hover{transform:scale(1.08);}

/* Footer */
footer{text-align:center;padding:35px;opacity:0.6;font-size:0.9rem;}
</style>
</head>

<body>

<div id="particles"></div>

<header>
  <div class="logo">CITY DESIGN</div>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#course">Course</a>
    <a href="#team">Team</a>
  </nav>
</header>

<section class="hero" id="home">
  <h1>Next-Gen City Design</h1>
  <p>A compact futuristic smart-city model powered by algorithms.</p>
</section>

<section class="section" id="about">
  <div class="card">
    <h2>About the Project</h2><br>
    <p>This smart-city model integrates DAA concepts to solve traffic, water, emergency routing, and resource management using algorithmic principles.</p>
  </div>
</section>

<section class="section" id="course">
  <div class="card">
    <h2>Course Information</h2><br>
    <p><b>Course:</b> DAA — 24ECSC205</p>
    <p><b>Instructor:</b> Prof. Prakash Hegade</p>
    <p><b>University:</b> KLE Technological University</p>
  </div>
</section>

<section class="section" id="team">
  <div class="card">
    <h2>Team Members</h2>
    <div class="team-grid">

      <div class="team-card">
        <div class="team-card-inner">
          <div class="front">
            <h3>Pramod S Indi</h3>
            <p>Traffic Optimization</p>
            <a class="team-box" href="pramod.html">Open</a>
          </div>
        </div>
      </div>

      <div class="team-card">
        <div class="team-card-inner">
          <div class="front">
            <h3>Parvatappa J Wani</h3>
            <p>Water System</p>
            <a class="team-box" href="parvatappa.html">Open</a>
          </div>
        </div>
      </div>

      <div class="team-card">
        <div class="team-card-inner">
          <div class="front">
            <h3>Sujal S Gowda</h3>
            <p>Emergency Routing</p>
            <a class="team-box" href="sujal.html">Open</a>
          </div>
        </div>
      </div>

      <div class="team-card">
        <div class="team-card-inner">
          <div class="front">
            <h3>Santosh Chikaraddi</h3>
            <p>AI Waste Routing</p>
            <a class="team-box" href="santosh.html">Open</a>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<footer>© 2025 Next-Gen City Design</footer>

<script>
const cont=document.getElementById("particles");
for(let i=0;i<45;i++){
  const p=document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=6+Math.random()*10+"s";
  p.style.animationDelay=Math.random()*4+"s";
  cont.appendChild(p);
}
</script>

</body>
</html>
