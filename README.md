<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Team Showcase</title>

<style>

/* ====== GLOBAL PAGE STYLING ====== */
body {
  background: #0a0f1a;
  margin: 0;
  font-family: "Poppins", sans-serif;
  color: white;
  text-align: center;
}

/* ====== TEAM SECTION ====== */
.team-section {
  padding: 20px 0; /* Reduced gap */
}

.team-title {
  font-size: 32px;
  margin-bottom: 10px; /* Tighter gap */
  color: #00eaff;
  font-weight: 700;
  text-shadow: 0 0 10px cyan, 0 0 20px #00eaff;
  letter-spacing: 1px;
  animation: titleGlow 3s infinite alternate;
}

@keyframes titleGlow {
  from { text-shadow: 0 0 10px cyan; }
  to { text-shadow: 0 0 20px #00eaff; }
}

/* ====== TEAM CARDS ====== */
.team-container {
  display: flex;
  justify-content: center;
  gap: 15px; /* Smaller space between cards */
  flex-wrap: wrap;
  margin-top: 10px;
}

.team-card {
  background: rgba(255, 255, 255, 0.06);
  border: 2px solid rgba(0, 255, 255, 0.6);
  border-radius: 16px;
  padding: 15px 10px;
  width: 170px;
  transition: 0.35s;
  box-shadow: 0 0 16px rgba(0, 255, 255, 0.3);
  backdrop-filter: blur(6px);
  transform-style: preserve-3d;
}

.team-card:hover {
  transform: scale(1.07) rotate3d(1, 1, 0, 10deg);
  box-shadow: 0 0 25px cyan, 0 0 40px #00eaff;
  border-color: #00eaff;
}

/* ====== AVATAR CIRCLE ====== */
.avatar {
  width: 75px;
  height: 75px;
  margin: 0 auto 10px;
  border-radius: 50%;
  border: 3px solid cyan;
  animation: avatarGlow 3s infinite alternate;
}

@keyframes avatarGlow {
  from { box-shadow: 0 0 10px cyan; }
  to { box-shadow: 0 0 22px #00eaff; }
}

/* ====== NAME TEXT ====== */
.team-card h3 {
  margin: 5px 0 0;
  font-size: 17px; /* More visible */
  font-weight: 600;
  color: #fff;
}

</style>
</head>

<body>

<section class="team-section">
  <h2 class="team-title">DAA AND NEXT GEN CITY DESIGN</h2>

  <div class="team-container">

  <div class="team-card">
      <div class="avatar"></div>
      <h3>Pramod S Indi</h3>
    </div>

  <div class="team-card">
      <div class="avatar"></div>
      <h3>Parvatappa J Wani</h3>
    </div>

  <div class="team-card">
      <div class="avatar"></div>
      <h3>Sujal S Gowda</h3>
    </div>

  <div class="team-card">
      <div class="avatar"></div>
      <h3>Santosh Chikaraddi</h3>
    </div>

  </div>
</section>

</body>
</html>
