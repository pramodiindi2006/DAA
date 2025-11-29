<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>City Design — Portfolio</title>
  <meta name="description" content="City Design — DAA Project portfolio with interactive AI assistant, animations and responsive layout">
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#2e2e2e; --card:#fff; --accent:#03dffc; --muted:#cfcfcf; --glass: rgba(255,255,255,0.06);
      --radius:14px;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Montserat,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial}

    body{background:linear-gradient(180deg,#333 0%, #2b2b2b 40%); color:#111}

    header{background:var(--accent); padding:18px 40px; display:flex; align-items:center; justify-content:space-between; box-shadow:0 2px 0 rgba(0,0,0,.3)}
    .logo{font-family:'Playfair Display',serif; font-weight:700; font-size:28px; color:#002; letter-spacing:1px}
    nav{display:flex; gap:20px}
    nav a{color:#022; text-decoration:none; font-weight:600}

    .hero{padding:56px 24px; text-align:center; color:var(--card);}
    .hero h1{font-size:48px; margin:0 0 8px; color:#fff; text-shadow:0 6px 18px rgba(0,0,0,.6)}
    .hero p{color:var(--muted); margin:0 0 18px}

    .container{max-width:1100px;margin:28px auto;padding:28px;background:var(--card); border-radius:16px; box-shadow:0 10px 30px rgba(0,0,0,.4)}
    .intro{padding:20px 36px; text-align:center}
    .intro h2{margin:8px 0 6px; font-family:'Playfair Display';}

    table{width:80%; margin:22px auto;border-collapse:collapse;font-weight:600}
    th,td{border:1px solid #ccc;padding:16px;text-align:center}
    th{background:#efefef}

    /* floating AI assistant button */
    .assistant-btn{position:fixed; right:26px; bottom:26px; background:var(--accent); border-radius:999px; box-shadow:0 8px 30px rgba(3,223,252,.12); padding:14px 18px; cursor:pointer; display:flex; gap:10px; align-items:center}
    .assistant-btn span{font-weight:700}

    /* Chat panel */
    .chat-panel{position:fixed; right:26px; bottom:86px; width:360px; max-width:calc(100% - 60px); background:linear-gradient(180deg,#0f1720,#0c1013); color:#fff; border-radius:12px; box-shadow:0 18px 48px rgba(0,0,0,.6); overflow:hidden; transform:translateY(20px); opacity:0; pointer-events:none; transition:all .28s ease}
    .chat-panel.open{transform:translateY(0); opacity:1; pointer-events:auto}
    .chat-header{padding:12px 14px; font-weight:700; background:rgba(255,255,255,0.04)}
    .messages{padding:12px; height:260px; overflow:auto; display:flex; flex-direction:column; gap:10px}
    .msg{max-width:82%; padding:10px 12px; border-radius:10px}
    .msg.user{align-self:flex-end; background:#03dffc; color:#001}
    .msg.bot{align-self:flex-start; background:#121212; color:#eee}
    .chat-input{display:flex; gap:8px;padding:10px; border-top:1px solid rgba(255,255,255,0.02)}
    .chat-input input{flex:1;padding:10px;border-radius:8px;border:0}
    .chat-input button{padding:10px 12px;border-radius:8px;border:0;background:var(--accent);cursor:pointer}

    /* responsive */
    @media (max-width:900px){
      .hero h1{font-size:34px}
      table{width:95%}
      header{padding:12px}
    }

    /* subtle animation */
    .glow{display:inline-block;padding:6px 14px;background:rgba(0,0,0,.35); border-radius:12px; box-shadow:0 8px 30px rgba(0,0,0,.6)}

    /* smooth entrance for container */
    .container{transform:translateY(16px); opacity:0; animation:enter .6s forwards .15s}
    @keyframes enter{to{transform:none;opacity:1}}

    /* cool striped top bar */
    .top-stripe{height:6px;background:repeating-linear-gradient(90deg, rgba(0,0,0,.08) 0 8px, rgba(255,255,255,.02) 8px 16px)}
  </style>
</head>
<body>
  <div class="top-stripe"></div>
  <header>
    <div class="logo">CITY DESIGN</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#project">Project</a>
      <a href="#team">Team</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <h1>Introduction</h1>
    <p class="glow">Clean, responsive portfolio for your DAA project — built with accessibility and modern UI in mind</p>
  </section>

  <main class="container" role="main">
    <section id="about" class="intro">
      <h2>Course: DAA — Project</h2>
      <p><strong>Course Code:</strong> 24ECSC205 &nbsp; • &nbsp; <strong>Instructor:</strong> Prof. Prakash Hegade</p>
      <p style="max-width:700px;margin:12px auto;color:#333;">University: KLE Technological University<br>Topic: City Design</p>
    </section>

    <section id="team">
      <table>
        <thead>
          <tr><th>Name</th><th>USN</th></tr>
        </thead>
        <tbody>
          <tr><td>Amogh Pai</td><td>01fe23bcs217</td></tr>
          <tr><td>Bhoomika Malagar</td><td>01fe23bcs216</td></tr>
          <tr><td>Saanvi Shetty</td><td>01fe23bcs227</td></tr>
          <tr><td>Ramya Rao</td><td>01fe23bcs243</td></tr>
        </tbody>
      </table>
    </section>
  </main>

  <!-- AI assistant button + panel -->
  <div class="assistant-btn" id="assistantBtn" aria-label="Open assistant" title="Ask the AI">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" style="transform:translateY(-2px)"><path d="M12 2a7 7 0 100 14 7 7 0 000-14z" fill="#001" opacity=".12"/><path d="M12 3.5a6 6 0 100 12 6 6 0 000-12z" fill="#001" opacity=".07"/><circle cx="12" cy="12" r="3.2" fill="#001"/></svg>
    <span>AI</span>
  </div>

  <div class="chat-panel" id="chatPanel" aria-hidden="true">
    <div class="chat-header">Project Assistant — tips & code snippets</div>
    <div class="messages" id="messages" role="log" aria-live="polite"></div>
    <div class="chat-input">
      <input id="chatInput" placeholder="Ask: how to add another page?" aria-label="Type your question">
      <button id="sendBtn">Send</button>
    </div>
  </div>

  <script>
    // small UI interactions + fake AI typing demo + guidance on integrating real AI
    const assistantBtn = document.getElementById('assistantBtn');
    const chatPanel = document.getElementById('chatPanel');
    const messages = document.getElementById('messages');
    const input = document.getElementById('chatInput');
    const sendBtn = document.getElementById('sendBtn');

    assistantBtn.addEventListener('click', ()=>{
      chatPanel.classList.toggle('open');
      chatPanel.setAttribute('aria-hidden', !chatPanel.classList.contains('open'));
      if(chatPanel.classList.contains('open')) input.focus();
    });

    function appendMsg(text, who='bot'){
      const d = document.createElement('div'); d.className = 'msg '+(who==='user'?'user':'bot'); d.textContent = text; messages.appendChild(d); messages.scrollTop = messages.scrollHeight;
    }

    function fakeTypingReply(q){
      appendMsg(q,'user');
      // show 'typing' then real reply
      const typing = document.createElement('div'); typing.className='msg bot'; typing.textContent='Typing...'; messages.appendChild(typing); messages.scrollTop = messages.scrollHeight;
      setTimeout(()=>{
        typing.textContent = 'Nice question! To add another page: create a new HTML (e.g. project.html), push to your repo and link it from the nav. For AI features, host a small serverless endpoint and call it from here — see comments in the file.';
        messages.scrollTop = messages.scrollHeight;
      },900);
    }

    sendBtn.addEventListener('click', ()=>{ if(input.value.trim()) { fakeTypingReply(input.value.trim()); input.value=''; } });
    input.addEventListener('keypress', (e)=>{ if(e.key==='Enter'){ sendBtn.click(); } });

    // --- Notes for integrating a real AI (do not put API keys in client-side code) ---
    /*
      1) Create a serverless function (Netlify, Vercel, Cloudflare Workers) that stores your secret OPENAI_KEY.
      2) The function accepts POST with {message:"..."} and forwards to OpenAI, returning a safe response.
      3) In the client (this file) call fetch('/.netlify/functions/ai', {method:'POST', body:JSON.stringify({message})})
      4) Show the returned text in chat using appendMsg(resp,'bot')

      Example (serverless - Node):
        const fetch = require('node-fetch');
        exports.handler = async (event) => {
          const { message } = JSON.parse(event.body);
          const res = await fetch('https://api.openai.com/v1/chat/completions', {
            method:'POST', headers:{'Content-Type':'application/json','Authorization':'Bearer '+process.env.OPENAI_KEY},
            body: JSON.stringify({ model:'gpt-4o-mini', messages:[{role:'user', content:message}] })
          });
          const data = await res.json();
          const reply = data.choices?.[0]?.message?.content || 'Sorry, no response';
          return { statusCode:200, body: JSON.stringify({reply}) };
        };

      Important: Keep keys secret and rate-limit user requests in your function.
    */

  </script>
</body>
</html>
