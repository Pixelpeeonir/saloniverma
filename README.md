<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Saloni Verma — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Nunito:wght@400;600;700;800&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
:root {
  --pink: #ff6eb4;
  --purple: #a855f7;
  --cyan: #22d3ee;
  --yellow: #fbbf24;
  --green: #4ade80;
  --dark: #0f0a1e;
  --card: #1a1035;
  --card2: #160d2e;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  background: var(--dark);
  font-family: 'Nunito', sans-serif;
  overflow-x: hidden;
  min-height: 100vh;
}

/* Animated star bg */
.stars {
  position: fixed;
  inset: 0;
  z-index: 0;
  overflow: hidden;
}
.star {
  position: absolute;
  border-radius: 50%;
  background: white;
  animation: twinkle var(--d) ease-in-out infinite alternate;
  opacity: 0.6;
}
@keyframes twinkle {
  from { opacity: 0.1; transform: scale(0.8); }
  to   { opacity: 0.9; transform: scale(1.2); }
}

.container {
  max-width: 860px;
  margin: 0 auto;
  padding: 30px 20px 60px;
  position: relative;
  z-index: 1;
}

/* ── HERO ── */
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  margin-bottom: 35px;
}

/* Cartoon girl SVG wrapper */
.cartoon-wrap {
  position: relative;
  width: 200px;
  height: 200px;
  margin-bottom: 5px;
}

/* Floating animation */
.cartoon-wrap svg {
  animation: float 3s ease-in-out infinite;
  filter: drop-shadow(0 8px 24px rgba(168,85,247,0.5));
}
@keyframes float {
  0%,100% { transform: translateY(0); }
  50%      { transform: translateY(-14px); }
}

/* Glow ring behind character */
.cartoon-wrap::before {
  content: '';
  position: absolute;
  bottom: 10px; left: 50%;
  transform: translateX(-50%);
  width: 100px; height: 20px;
  background: radial-gradient(ellipse, rgba(168,85,247,0.5), transparent 70%);
  border-radius: 50%;
  animation: shadowPulse 3s ease-in-out infinite;
}
@keyframes shadowPulse {
  0%,100% { opacity: 0.6; width: 100px; }
  50%      { opacity: 0.2; width: 70px; }
}

/* Name */
.hero-name {
  font-family: 'Fredoka One', cursive;
  font-size: clamp(32px, 7vw, 52px);
  background: linear-gradient(135deg, var(--pink), var(--purple), var(--cyan));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-align: center;
  letter-spacing: 1px;
  animation: nameGlow 3s ease-in-out infinite alternate;
}
@keyframes nameGlow {
  from { filter: drop-shadow(0 0 8px rgba(255,110,180,0.4)); }
  to   { filter: drop-shadow(0 0 20px rgba(168,85,247,0.7)); }
}

/* Typing bar */
.typing-bar {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(168,85,247,0.4);
  border-radius: 30px;
  padding: 8px 24px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 15px;
  color: var(--cyan);
  min-width: 280px;
  text-align: center;
}

/* Status pills */
.pills {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 6px;
}
.pill {
  padding: 5px 14px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: 700;
  border: 1.5px solid;
  animation: pillBounce 2s ease-in-out infinite;
}
.pill:nth-child(2) { animation-delay: 0.3s; }
.pill:nth-child(3) { animation-delay: 0.6s; }
@keyframes pillBounce {
  0%,100% { transform: translateY(0); }
  50%      { transform: translateY(-4px); }
}
.p-pink   { color:var(--pink);   border-color:var(--pink);   background:rgba(255,110,180,0.1); }
.p-purple { color:var(--purple); border-color:var(--purple); background:rgba(168,85,247,0.1); }
.p-cyan   { color:var(--cyan);   border-color:var(--cyan);   background:rgba(34,211,238,0.1); }

/* ── SECTION ── */
.section { margin: 28px 0; animation: slideUp 0.6s ease both; }
@keyframes slideUp {
  from { opacity:0; transform:translateY(24px); }
  to   { opacity:1; transform:translateY(0); }
}
.section:nth-child(1){animation-delay:.1s}
.section:nth-child(2){animation-delay:.2s}
.section:nth-child(3){animation-delay:.3s}
.section:nth-child(4){animation-delay:.4s}
.section:nth-child(5){animation-delay:.5s}
.section:nth-child(6){animation-delay:.6s}

.sec-title {
  font-family: 'Fredoka One', cursive;
  font-size: 18px;
  color: var(--yellow);
  margin-bottom: 14px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.sec-title::after {
  content:'';
  flex:1;
  height:2px;
  background: linear-gradient(90deg, var(--yellow), transparent);
  border-radius: 2px;
}

/* ── ABOUT CARD ── */
.about-card {
  background: var(--card);
  border: 1.5px solid rgba(168,85,247,0.3);
  border-radius: 20px;
  padding: 22px 28px;
  box-shadow: 0 0 30px rgba(168,85,247,0.1);
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px 30px;
}
@media(max-width:500px){ .about-card{grid-template-columns:1fr;} }

.about-row { display:flex; gap:8px; align-items:flex-start; font-size:14px; }
.about-key { color: var(--purple); font-weight:700; min-width:80px; }
.about-val { color: #d4b8ff; }

/* ── SKILLS ── */
.skills-wrap {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.skill-row {
  background: var(--card);
  border: 1.5px solid rgba(34,211,238,0.2);
  border-radius: 16px;
  padding: 16px 20px;
  transition: transform 0.3s, box-shadow 0.3s;
}
.skill-row:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(34,211,238,0.15);
}
.skill-cat {
  font-size: 12px;
  color: var(--cyan);
  font-weight: 700;
  margin-bottom: 12px;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.icons-row {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.icon-chip {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5px;
  padding: 10px 14px;
  border-radius: 12px;
  border: 1.5px solid rgba(255,255,255,0.08);
  background: rgba(255,255,255,0.03);
  cursor: default;
  transition: all 0.3s;
  min-width: 70px;
}
.icon-chip:hover {
  transform: translateY(-5px) scale(1.08);
  border-color: var(--pink);
  box-shadow: 0 8px 20px rgba(255,110,180,0.25);
}
.icon-chip svg, .icon-chip img { width:32px; height:32px; }
.icon-chip span {
  font-size: 11px;
  font-weight: 700;
  color: #c4aaff;
}

/* ── STATS ── */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 14px;
}
.stat-card {
  background: var(--card);
  border: 1.5px solid rgba(251,191,36,0.2);
  border-radius: 16px;
  padding: 20px;
  text-align: center;
  transition: all 0.3s;
}
.stat-card:hover {
  border-color: var(--yellow);
  box-shadow: 0 0 25px rgba(251,191,36,0.2);
  transform: translateY(-4px);
}
.stat-emoji { font-size: 26px; display:block; margin-bottom:8px; }
.stat-num {
  font-family: 'Fredoka One', cursive;
  font-size: 30px;
  color: var(--yellow);
  display: block;
}
.stat-label { font-size: 12px; color: #a88ee0; font-weight:700; margin-top:4px; }

/* ── SOCIAL ── */
.social-grid {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
}
.social-btn {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 12px 22px;
  border-radius: 14px;
  font-family: 'Nunito', sans-serif;
  font-weight: 800;
  font-size: 15px;
  text-decoration: none;
  border: 2px solid;
  transition: all 0.3s;
}
.social-btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 30px currentColor;
}
.btn-gh  { color:#fff;     border-color:#ffffff55; background:#ffffff11; }
.btn-li  { color:#0a66c2;  border-color:#0a66c255; background:#0a66c211; }

/* ── QUOTE ── */
.quote-card {
  background: linear-gradient(135deg, rgba(255,110,180,0.08), rgba(168,85,247,0.08));
  border: 2px solid rgba(255,110,180,0.3);
  border-radius: 20px;
  padding: 24px 30px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.quote-card::before {
  content: '❝';
  position: absolute;
  top: -10px; left: 14px;
  font-size: 80px;
  color: rgba(255,110,180,0.1);
  font-family: serif;
}
.quote-text {
  font-size: 17px;
  font-weight: 700;
  color: var(--pink);
  line-height: 1.7;
}
.quote-author {
  margin-top: 10px;
  font-size: 13px;
  color: #a88ee0;
}

/* ── DIVIDER ── */
hr.div {
  border:none;
  height:2px;
  background: linear-gradient(90deg, transparent, var(--purple), transparent);
  margin: 10px 0;
  opacity: 0.4;
}

/* ── FOOTER ── */
.footer {
  text-align: center;
  padding-top: 20px;
  color: #6b5a9e;
  font-size: 13px;
}
.visitor {
  display: inline-block;
  background: rgba(168,85,247,0.1);
  border: 1.5px solid var(--purple);
  padding: 5px 16px;
  border-radius: 20px;
  color: var(--purple);
  font-weight: 700;
  margin-top: 8px;
}
</style>
</head>
<body>

<!-- Starfield -->
<div class="stars" id="stars"></div>

<div class="container">

  <!-- ── HERO ── -->
  <div class="hero">

    <!-- Cartoon girl with laptop -->
    <div class="cartoon-wrap">
      <svg viewBox="0 0 200 200" width="200" height="200" xmlns="http://www.w3.org/2000/svg">
        <!-- Desk -->
        <rect x="20" y="158" width="160" height="10" rx="5" fill="#2d1b69"/>
        <rect x="40" y="168" width="8" height="22" rx="3" fill="#2d1b69"/>
        <rect x="152" y="168" width="8" height="22" rx="3" fill="#2d1b69"/>

        <!-- Laptop base -->
        <rect x="50" y="140" width="100" height="20" rx="4" fill="#1e1b4b"/>
        <rect x="52" y="142" width="96" height="16" rx="3" fill="#312e81"/>
        <!-- Keyboard detail -->
        <rect x="58" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="66" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="74" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="82" y="146" width="6" height="4" rx="1" fill="#7c3aed" opacity="0.9"/>
        <rect x="90" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="98" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="106" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="114" y="146" width="6" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="122" y="146" width="14" height="4" rx="1" fill="#4338ca" opacity="0.8"/>
        <rect x="62" y="152" width="76" height="3" rx="1" fill="#4338ca" opacity="0.6"/>

        <!-- Laptop screen -->
        <rect x="48" y="90" width="104" height="52" rx="6" fill="#0f0a1e"/>
        <rect x="50" y="92" width="100" height="48" rx="4" fill="#1a0a3e"/>
        <!-- Screen glow -->
        <rect x="50" y="92" width="100" height="48" rx="4" fill="url(#screenGlow)" opacity="0.7"/>
        <!-- Code lines on screen -->
        <rect x="56" y="100" width="40" height="3" rx="1.5" fill="#a855f7" opacity="0.9"/>
        <rect x="56" y="106" width="60" height="3" rx="1.5" fill="#22d3ee" opacity="0.8"/>
        <rect x="62" y="112" width="50" height="3" rx="1.5" fill="#4ade80" opacity="0.7"/>
        <rect x="62" y="118" width="35" height="3" rx="1.5" fill="#ff6eb4" opacity="0.9"/>
        <rect x="56" y="124" width="55" height="3" rx="1.5" fill="#fbbf24" opacity="0.7"/>
        <!-- Cursor blink -->
        <rect x="115" y="124" width="2" height="10" rx="1" fill="#ffffff" opacity="0.9">
          <animate attributeName="opacity" values="0.9;0;0.9" dur="1s" repeatCount="indefinite"/>
        </rect>
        <!-- Screen shine -->
        <line x1="52" y1="94" x2="70" y2="94" stroke="white" stroke-width="1" opacity="0.15"/>

        <!-- Girl body -->
        <!-- Dress/top - purple -->
        <ellipse cx="100" cy="130" rx="22" ry="14" fill="#7c3aed"/>
        <rect x="78" y="115" width="44" height="18" rx="8" fill="#7c3aed"/>
        <!-- Collar detail -->
        <path d="M92 115 Q100 122 108 115" stroke="#a855f7" stroke-width="2" fill="none"/>

        <!-- Arms -->
        <!-- Right arm typing -->
        <path d="M122 122 Q135 128 138 138" stroke="#ffb899" stroke-width="8" stroke-linecap="round" fill="none"/>
        <!-- Left arm typing -->
        <path d="M78 122 Q65 128 62 138" stroke="#ffb899" stroke-width="8" stroke-linecap="round" fill="none"/>
        <!-- Hands -->
        <circle cx="138" cy="140" r="6" fill="#ffb899"/>
        <circle cx="62" cy="140" r="6" fill="#ffb899"/>

        <!-- Neck -->
        <rect x="95" y="105" width="10" height="12" rx="5" fill="#ffb899"/>

        <!-- Head -->
        <ellipse cx="100" cy="88" rx="24" ry="26" fill="#ffb899"/>

        <!-- Hair - long with highlights -->
        <ellipse cx="100" cy="70" rx="24" ry="12" fill="#3b1a6e"/>
        <path d="M76 78 Q68 110 72 130" stroke="#3b1a6e" stroke-width="14" stroke-linecap="round" fill="none"/>
        <path d="M124 78 Q132 110 128 130" stroke="#3b1a6e" stroke-width="14" stroke-linecap="round" fill="none"/>
        <!-- Hair highlights -->
        <path d="M80 72 Q76 90 78 110" stroke="#6d28d9" stroke-width="3" stroke-linecap="round" fill="none" opacity="0.6"/>
        <!-- Hair clip -->
        <ellipse cx="82" cy="80" rx="5" ry="3" fill="#ff6eb4" transform="rotate(-20,82,80)"/>
        <ellipse cx="86" cy="77" rx="3" ry="2" fill="#ff6eb4" transform="rotate(-20,86,77)"/>

        <!-- Eyes with sparkles -->
        <ellipse cx="91" cy="88" rx="5" ry="6" fill="white"/>
        <ellipse cx="109" cy="88" rx="5" ry="6" fill="white"/>
        <ellipse cx="92" cy="89" rx="3.5" ry="4" fill="#5b21b6"/>
        <ellipse cx="110" cy="89" rx="3.5" ry="4" fill="#5b21b6"/>
        <circle cx="92" cy="88" r="2" fill="#1e1b4b"/>
        <circle cx="110" cy="88" r="2" fill="#1e1b4b"/>
        <!-- Eye shine -->
        <circle cx="94" cy="87" r="1.2" fill="white"/>
        <circle cx="112" cy="87" r="1.2" fill="white"/>
        <!-- Eyelashes -->
        <line x1="87" y1="83" x2="86" y2="81" stroke="#3b1a6e" stroke-width="1.5"/>
        <line x1="91" y1="82" x2="91" y2="80" stroke="#3b1a6e" stroke-width="1.5"/>
        <line x1="95" y1="83" x2="96" y2="81" stroke="#3b1a6e" stroke-width="1.5"/>
        <line x1="105" y1="83" x2="104" y2="81" stroke="#3b1a6e" stroke-width="1.5"/>
        <line x1="109" y1="82" x2="109" y2="80" stroke="#3b1a6e" stroke-width="1.5"/>
        <line x1="113" y1="83" x2="114" y2="81" stroke="#3b1a6e" stroke-width="1.5"/>

        <!-- Eyebrows -->
        <path d="M87 82 Q91 79 96 81" stroke="#3b1a6e" stroke-width="2" fill="none" stroke-linecap="round"/>
        <path d="M104 81 Q109 79 113 82" stroke="#3b1a6e" stroke-width="2" fill="none" stroke-linecap="round"/>

        <!-- Blush -->
        <ellipse cx="83" cy="95" rx="6" ry="4" fill="#ffadd6" opacity="0.5"/>
        <ellipse cx="117" cy="95" rx="6" ry="4" fill="#ffadd6" opacity="0.5"/>

        <!-- Smile -->
        <path d="M93 100 Q100 106 107 100" stroke="#d97b9a" stroke-width="2" fill="none" stroke-linecap="round"/>

        <!-- Headphones -->
        <path d="M76 83 Q76 62 100 62 Q124 62 124 83" stroke="#4c1d95" stroke-width="5" fill="none"/>
        <rect x="72" y="81" width="8" height="14" rx="4" fill="#7c3aed"/>
        <rect x="120" y="81" width="8" height="14" rx="4" fill="#7c3aed"/>
        <!-- Headphone detail -->
        <rect x="73" y="83" width="6" height="10" rx="3" fill="#a855f7" opacity="0.6"/>
        <rect x="121" y="83" width="6" height="10" rx="3" fill="#a855f7" opacity="0.6"/>

        <!-- Floating sparkles -->
        <text x="148" y="80" font-size="14" fill="#fbbf24" opacity="0.9">
          ✦<animate attributeName="opacity" values="0.9;0.2;0.9" dur="2s" repeatCount="indefinite"/>
        </text>
        <text x="30" y="100" font-size="10" fill="#ff6eb4" opacity="0.8">
          ✦<animate attributeName="opacity" values="0.8;0.1;0.8" dur="1.5s" repeatCount="indefinite"/>
        </text>
        <text x="155" y="115" font-size="8" fill="#22d3ee" opacity="0.9">
          ✦<animate attributeName="opacity" values="0.9;0.2;0.9" dur="2.5s" repeatCount="indefinite"/>
        </text>
        <text x="22" y="78" font-size="12" fill="#a855f7" opacity="0.7">
          ⋆<animate attributeName="opacity" values="0.7;0.1;0.7" dur="3s" repeatCount="indefinite"/>
        </text>
        <!-- Code bubbles -->
        <text x="138" y="100" font-size="9" fill="#4ade80" opacity="0.8" font-family="monospace">
          &lt;/&gt;<animate attributeName="opacity" values="0.8;0.2;0.8" dur="2s" repeatCount="indefinite"/>
        </text>
        <text x="18" y="120" font-size="8" fill="#22d3ee" opacity="0.7" font-family="monospace">
          {}<animate attributeName="opacity" values="0.7;0.1;0.7" dur="2.5s" repeatCount="indefinite"/>
        </text>

        <!-- Defs -->
        <defs>
          <linearGradient id="screenGlow" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#a855f7" stop-opacity="0.3"/>
            <stop offset="100%" stop-color="#22d3ee" stop-opacity="0.1"/>
          </linearGradient>
        </defs>
      </svg>
    </div>

    <div class="hero-name">Saloni Verma</div>

    <div class="typing-bar">
      <span id="typer">Android App Developer 📱</span><span style="color:var(--pink);animation:blink 0.7s infinite">|</span>
    </div>

    <div class="pills">
      <span class="pill p-pink">📱 Android Dev</span>
      <span class="pill p-purple">🦋 Flutter Dev</span>
      <span class="pill p-cyan">☕ Java Engineer</span>
    </div>
  </div>

  <hr class="div"/>

  <!-- ── ABOUT ── -->
  <div class="section">
    <div class="sec-title">💫 whoami</div>
    <div class="about-card">
      <div class="about-row"><span class="about-key">👩‍💻 Role</span><span class="about-val">Android App Developer · Flutter Dev · Java Engineer</span></div>
      <div class="about-row"><span class="about-key">📍 City</span><span class="about-val">The City of Taj 🕌 — Agra, UP</span></div>
      <div class="about-row"><span class="about-key">⚡ Status</span><span class="about-val">Currently caffeinated ☕ & building something cool</span></div>
      <div class="about-row"><span class="about-key">😈 Mood</span><span class="about-val">git push --force (always)</span></div>
    </div>
  </div>

  <!-- ── SKILLS ── -->
  <div class="section">
    <div class="sec-title">🛠️ Skills & Tech Stack</div>
    <div class="skills-wrap">

      <div class="skill-row">
        <div class="skill-cat">⚡ Languages</div>
        <div class="icons-row">
          <!-- HTML -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M5 3l1.8 20.4L16 26l9.2-2.6L27 3H5z" fill="#e44d26"/><path d="M16 24.4l7.5-2.1 1.6-17.7H16v19.8z" fill="#f16529"/><path d="M11 11h5V8.5H8.3l.4 4.5H16V11h-5zm.5 5.5H9l.3 3.8 6.7 1.9v-2.6l-3.7-1-.3-2.1z" fill="#ebebeb"/><path d="M16 11v2.5h4.8l-.4 5.3-4.4 1.2v2.6l6.7-1.9.1-.9L23.7 8H16v3z" fill="#fff"/></svg>
            <span>HTML</span>
          </div>
          <!-- CSS -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M5 3l1.8 20.4L16 26l9.2-2.6L27 3H5z" fill="#1572b6"/><path d="M16 24.4l7.5-2.1 1.6-17.7H16v19.8z" fill="#33a9dc"/><path d="M11.1 13.5H16V11H8.6l.4 5.2H16v-2.7h-4.9zm-1 7l.3 3.4L16 25.4v-2.7l-3.7-1-.2-2.2H9.8z" fill="#ebebeb"/><path d="M16 13.5v2.7h4.5l-.4 5.3-4.1 1.1v2.7l6.5-1.8.9-10.1H16zm0-2.5h7.5l.3-2.5H16V11z" fill="#fff"/></svg>
            <span>CSS</span>
          </div>
          <!-- JavaScript -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><rect width="32" height="32" rx="4" fill="#f7df1e"/><path d="M9.5 25.5l2.3-1.4c.4.8.8 1.4 1.7 1.4.9 0 1.4-.3 1.4-1.7V16h2.8v7.9c0 2.8-1.6 4-4 4-2.1 0-3.3-1.1-4.2-2.4zm9.5-.4l2.3-1.4c.6 1 1.3 1.7 2.7 1.7 1.1 0 1.8-.6 1.8-1.3 0-.9-.7-1.2-2-1.8l-.7-.3c-2-.9-3.3-2-3.3-4.3 0-2.1 1.6-3.7 4.2-3.7 1.8 0 3.1.6 4 2.3l-2.2 1.4c-.5-.9-1-1.2-1.8-1.2-.8 0-1.3.5-1.3 1.2 0 .8.5 1.1 1.7 1.6l.7.3c2.3 1 3.7 2.1 3.7 4.4 0 2.5-2 3.9-4.6 3.9-2.6 0-4.2-1.2-5.1-2.8z"/></svg>
            <span>JS</span>
          </div>
          <!-- Java -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M12.3 23.7s-1.1.6.8.8c2.2.3 3.4.2 5.9-.2 0 0 .6.4 1.5.8-5.5 2.4-12.5-.1-8.2-1.4zm-.7-3.2s-1.3.9.7 1.1c2.5.3 4.4.3 7.8-.4 0 0 .4.4 1.1.7-6.9 2-14.6.2-9.6-1.4z" fill="#4e7896"/><path d="M17.1 13.9c1.4 1.6-.4 3-.4 3s3.5-1.8 1.9-4c-1.5-2.1-2.7-3.1 3.6-6.6 0 0-9.8 2.5-5.1 7.6z" fill="#f89820"/><path d="M23.9 26.2s.8.7-.9 1.2c-3.2.9-13.4 1.2-16.2 0-1-.4.9-1 1.5-1.1.6-.1 1-.1 1-.1-1.1-.8-7.4 1.6-3.2 2.3 11.6 1.9 21.2-.9 17.8-2.3zm-11.6-8.5s-5.1 1.2-1.8 1.6c1.4.2 4.1.1 6.6-.1 2.1-.2 4.1-.5 4.1-.5s-.7.3-1.2.6c-4.9 1.3-14.4.7-11.6-.6 2.3-1.1 3.9-.9 3.9-1zm8.9 5s3.7-1.9 2-3.5c-1.6-1.5-3.1-.5-3.1-.5s.8-.4 1.8.3c1 .8.6 1.8-2.6 2.7-3.3 1-.8 1.5 1.9 1z" fill="#4e7896"/><path d="M18.4 4s2.9 2.9-2.8 7.4C11 15 14.7 17.3 15.6 20c-2.3-2.1-4-3.9-2.9-5.6 1.7-2.6 6.4-3.8 5.7-10.4z" fill="#f89820"/><path d="M12.8 28.9c4.9.3 12.5-.2 12.7-2.3 0 0-.3.9-4.1 1.5-4.2.7-9.4.6-12.5.2 0 0 .6.5 3.9.6z" fill="#4e7896"/></svg>
            <span>Java</span>
          </div>
          <!-- Dart -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M7.8 24.2l-1.5-1.6L8.7 8.5 22.2 6l1.8 1.7-16.2 16.5z" fill="#01579b"/><path d="M8.7 8.5L22.2 6l3.7 3.8-15 1.4L8.7 8.5z" fill="#40c4ff"/><path d="M6.3 22.6L9.9 11.2l-2.1-.9-1.5 12.3z" fill="#40c4ff"/><path d="M9.9 11.2l1 9.8 13.6-11.2-3.2-3.8-11.4 5.2z" fill="#29b6f6"/><path d="M10.9 21l3 3 11.2-2.1-4.6-2.8-9.6 1.9z" fill="#01579b"/><path d="M13.9 24l9.6-1.9 2.5-11.9-12.1 13.8z" fill="#40c4ff"/></svg>
            <span>Dart</span>
          </div>
          <!-- C -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><circle cx="16" cy="16" r="14" fill="#5c6bc0"/><path d="M22.5 20.3c-.7.4-1.5.7-2.3.9-.8.2-1.7.3-2.6.3-2.6 0-4.6-.7-6-2.1-1.4-1.4-2.1-3.4-2.1-5.8 0-2.5.7-4.5 2.2-6s3.6-2.2 6.3-2.2c.8 0 1.6.1 2.3.3.7.2 1.4.4 1.9.7v3.5c-.6-.4-1.3-.8-1.9-1-.6-.2-1.3-.4-2-.4-1.5 0-2.7.5-3.5 1.5-.8 1-1.2 2.4-1.2 4.2s.4 3.1 1.2 4c.8.9 2 1.4 3.5 1.4.7 0 1.4-.1 2-.4.6-.2 1.3-.6 1.9-1.1l.3 1.2z" fill="white"/></svg>
            <span>C</span>
          </div>
        </div>
      </div>

      <div class="skill-row">
        <div class="skill-cat">📱 Mobile & Frameworks</div>
        <div class="icons-row">
          <!-- Flutter -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M13.4 2L3 12.5l3.8 3.8 14.2-14.3H13.4z" fill="#42a5f5"/><path d="M13.4 2h7.6L9.7 13.2 5.9 9.4 13.4 2z" fill="#42a5f5"/><path d="M3 12.5l3.8 3.8 3.9-3.1L9.8 12 13.4 2 5.9 9.4 3 12.5z" fill="#42a5f5" opacity="0.5"/><path d="M16 16l-3.9 3.9 3.9 3.8 7.7-7.7H16z" fill="#1565c0"/><path d="M12.1 19.9l3.9 3.8-3.8 3.9-3.9-3.9 3.8-3.8z" fill="#42a5f5"/><path d="M12.2 27.6l3.8-3.9-3.9-3.8-3.8 3.9 3.9 3.8z" fill="#0d47a1"/></svg>
            <span>Flutter</span>
          </div>
          <!-- Android -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M6.7 11.5C5.2 11.5 4 12.7 4 14.2v7.3c0 1.5 1.2 2.7 2.7 2.7s2.7-1.2 2.7-2.7v-7.3c0-1.5-1.2-2.7-2.7-2.7zm18.6 0c-1.5 0-2.7 1.2-2.7 2.7v7.3c0 1.5 1.2 2.7 2.7 2.7s2.7-1.2 2.7-2.7v-7.3c0-1.5-1.2-2.7-2.7-2.7z" fill="#a4c639"/><path d="M9.8 24.2c0 .9.7 1.6 1.6 1.6h1.3V29c0 1.1.9 2 2 2s2-.9 2-2v-3.2h2V29c0 1.1.9 2 2 2s2-.9 2-2v-3.2h1.3c.9 0 1.6-.7 1.6-1.6V11.7H9.8v12.5z" fill="#a4c639"/><path d="M20.4 5.1L21.8 3c.2-.3.1-.7-.2-.8-.3-.2-.7-.1-.8.2l-1.5 2.2C18.2 4.2 17.1 4 16 4s-2.2.2-3.3.6L11.2 2.4c-.2-.3-.6-.4-.8-.2-.3.2-.4.6-.2.8l1.4 2.1C9.5 6.4 8 8.5 8 11h16c0-2.5-1.4-4.6-3.6-5.9zM13.5 9c-.6 0-1-.4-1-1s.4-1 1-1 1 .4 1 1-.4 1-1 1zm5 0c-.6 0-1-.4-1-1s.4-1 1-1 1 .4 1 1-.4 1-1 1z" fill="#a4c639"/></svg>
            <span>Android</span>
          </div>
        </div>
      </div>

      <div class="skill-row">
        <div class="skill-cat">🎨 Design & Tools</div>
        <div class="icons-row">
          <!-- UI/UX / Figma -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><rect x="10" y="4" width="12" height="24" rx="6" fill="#0acf83"/><circle cx="16" cy="16" r="5" fill="#1abcfe"/><path d="M10 4h6v12h-6V4z" fill="#ff7262"/><path d="M10 16h6v6a6 6 0 0 1-6-6z" fill="#a259ff"/><path d="M16 4h6a6 6 0 0 1 0 12h-6V4z" fill="#f24e1e"/></svg>
            <span>UI/UX</span>
          </div>
          <!-- Gen AI -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><circle cx="16" cy="16" r="13" fill="#7c3aed"/><circle cx="16" cy="16" r="7" fill="none" stroke="#a855f7" stroke-width="1.5"/><circle cx="16" cy="16" r="3" fill="#c084fc"/><line x1="16" y1="3" x2="16" y2="9" stroke="#a855f7" stroke-width="1.5"/><line x1="16" y1="23" x2="16" y2="29" stroke="#a855f7" stroke-width="1.5"/><line x1="3" y1="16" x2="9" y2="16" stroke="#a855f7" stroke-width="1.5"/><line x1="23" y1="16" x2="29" y2="16" stroke="#a855f7" stroke-width="1.5"/><line x1="7" y1="7" x2="11" y2="11" stroke="#a855f7" stroke-width="1.5"/><line x1="21" y1="21" x2="25" y2="25" stroke="#a855f7" stroke-width="1.5"/><line x1="25" y1="7" x2="21" y2="11" stroke="#a855f7" stroke-width="1.5"/><line x1="11" y1="21" x2="7" y2="25" stroke="#a855f7" stroke-width="1.5"/></svg>
            <span>Gen AI</span>
          </div>
          <!-- Git -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M29.5 14.7L17.3 2.5c-1.3-1.3-3.5-1.3-4.8 0l-2.4 2.4 3 3c.7-.3 1.5-.1 2.1.4.6.6.7 1.4.4 2.1l2.9 2.9c.7-.3 1.5-.1 2.1.4 1 1 1 2.6 0 3.6-1 1-2.6 1-3.6 0-.6-.6-.8-1.5-.5-2.2l-2.7-2.7v7.1c.4.2.8.4 1.1.8 1 1 1 2.6 0 3.6-1 1-2.6 1-3.6 0-1-1-1-2.6 0-3.6.4-.4.9-.7 1.5-.8V12.5c-.6-.1-1.1-.4-1.5-.8-.6-.6-.8-1.5-.5-2.2L7.9 6.5l-5.4 5.4c-1.3 1.3-1.3 3.5 0 4.8L14.7 29c1.3 1.3 3.5 1.3 4.8 0l10-10c1.3-1.3 1.3-3.5 0-4.8v.5z" fill="#f05033"/></svg>
            <span>Git</span>
          </div>
          <!-- GitHub -->
          <div class="icon-chip">
            <svg viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M16 2C8.27 2 2 8.27 2 16c0 6.18 4.01 11.43 9.57 13.29.7.13.96-.3.96-.67 0-.33-.01-1.43-.02-2.6-3.89.85-4.71-1.87-4.71-1.87-.64-1.61-1.55-2.04-1.55-2.04-1.27-.87.1-.85.1-.85 1.4.1 2.14 1.44 2.14 1.44 1.24 2.13 3.27 1.52 4.06 1.16.13-.9.49-1.52.89-1.87-3.1-.35-6.36-1.55-6.36-6.9 0-1.52.54-2.77 1.43-3.74-.14-.35-.62-1.77.14-3.68 0 0 1.17-.37 3.83 1.43 1.11-.31 2.3-.46 3.48-.47 1.18 0 2.37.16 3.48.47 2.66-1.8 3.83-1.43 3.83-1.43.76 1.92.28 3.33.14 3.68.89.97 1.43 2.22 1.43 3.74 0 5.36-3.27 6.54-6.38 6.88.5.43.95 1.29.95 2.6 0 1.87-.02 3.38-.02 3.84 0 .37.25.81.96.67C25.99 27.43 30 22.18 30 16c0-7.73-6.27-14-14-14z" fill="white"/></svg>
            <span>GitHub</span>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- ── STATS ── -->
  <div class="section">
    <div class="sec-title">📊 My Numbers</div>
    <div class="stats-grid">
      <div class="stat-card">
        <span class="stat-emoji">🚀</span>
        <span class="stat-num" id="s1">0</span>
        <div class="stat-label">Projects Built</div>
      </div>
      <div class="stat-card">
        <span class="stat-emoji">💻</span>
        <span class="stat-num" id="s2">0</span>
        <div class="stat-label">Total Commits</div>
      </div>
      <div class="stat-card">
        <span class="stat-emoji">🐛</span>
        <span class="stat-num" id="s3">0</span>
        <div class="stat-label">Bugs Squashed</div>
      </div>
      <div class="stat-card">
        <span class="stat-emoji">☕</span>
        <span class="stat-num" id="s4">∞</span>
        <div class="stat-label">Coffees Consumed</div>
      </div>
    </div>
  </div>

  <!-- ── QUOTE ── -->
  <div class="section">
    <div class="quote-card">
      <div class="quote-text">"I don't have bugs, I have hidden features." 🐛✨<br>
      <span style="font-size:14px; color:#c4aaff;">— Saloni Verma, probably at 3 AM from Agra 🕌</span></div>
    </div>
  </div>

  <!-- ── SOCIAL ── -->
  <div class="section">
    <div class="sec-title">🌐 Find Me</div>
    <div class="social-grid">
      <a href="https://github.com/saloniverma" target="_blank" class="social-btn btn-gh">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"/></svg>
        GitHub
      </a>
      <a href="https://linkedin.com/in/saloni-verma" target="_blank" class="social-btn btn-li">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div>⚡ Made with 💜 from The City of Taj 🕌</div>
    <div class="visitor">👁️ Visitors: 1,337</div>
  </div>

</div>

<style>
@keyframes blink { 50% { opacity: 0; } }
</style>

<script>
// Stars
const starsEl = document.getElementById('stars');
for (let i = 0; i < 120; i++) {
  const s = document.createElement('div');
  s.className = 'star';
  const size = Math.random() * 3 + 1;
  s.style.cssText = `
    width:${size}px; height:${size}px;
    top:${Math.random()*100}%;
    left:${Math.random()*100}%;
    --d:${1.5+Math.random()*3}s;
    animation-delay:${Math.random()*3}s;
  `;
  starsEl.appendChild(s);
}

// Typing
const lines = [
  "Android App Developer 📱",
  "Flutter Developer 🦋",
  "Java Engineer ☕",
  "UI/UX Designer 🎨",
  "Gen AI Explorer 🤖",
  "from Agra with 💜"
];
let li = 0, ci = 0, del = false;
const typer = document.getElementById('typer');
function tick() {
  const cur = lines[li];
  if (!del) {
    typer.textContent = cur.slice(0, ++ci);
    if (ci === cur.length) { del = true; setTimeout(tick, 1800); return; }
  } else {
    typer.textContent = cur.slice(0, --ci);
    if (ci === 0) { del = false; li = (li+1) % lines.length; }
  }
  setTimeout(tick, del ? 45 : 90);
}
tick();

// Counters
function count(id, to) {
  let n = 0;
  const el = document.getElementById(id);
  if (!el || el.textContent === '∞') return;
  const step = Math.max(1, Math.floor(to / 50));
  const iv = setInterval(() => {
    n = Math.min(n + step, to);
    el.textContent = n + '+';
    if (n >= to) clearInterval(iv);
  }, 30);
}
setTimeout(() => {
  count('s1', 10);
  count('s2', 200);
  count('s3', 500);
}, 600);
</script>
</body>
</html>
