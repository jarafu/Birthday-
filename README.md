<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Bernys 💖</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400;1,700&family=Quicksand:wght@300;400;500;600;700&display=swap');

:root {
–pink-light: #ffe0f0;
–pink-mid: #ffb3d9;
–pink-deep: #ff6eb4;
–purple-soft: #e8d5f5;
–purple-mid: #c084fc;
–purple-deep: #9333ea;
–rose: #fb7185;
–gold: #fbbf24;
–cream: #fff9fb;
–glass-bg: rgba(255,255,255,0.18);
–glass-border: rgba(255,255,255,0.4);
–shadow-pink: rgba(255,110,180,0.25);
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
font-family: ‘Quicksand’, sans-serif;
background: linear-gradient(135deg, #ffe0f0 0%, #f3e8ff 35%, #fce4ec 60%, #ede9fe 100%);
min-height: 100vh;
overflow-x: hidden;
color: #5b2d6e;
cursor: default;
}

/* ─── ANIMATED BACKGROUND MESH ─── */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background:
radial-gradient(ellipse at 20% 20%, rgba(255,182,217,0.45) 0%, transparent 55%),
radial-gradient(ellipse at 80% 80%, rgba(196,130,252,0.35) 0%, transparent 55%),
radial-gradient(ellipse at 60% 10%, rgba(251,113,133,0.25) 0%, transparent 45%);
animation: meshShift 12s ease-in-out infinite alternate;
pointer-events: none;
z-index: 0;
}
@keyframes meshShift {
0%   { opacity: 1; transform: scale(1) rotate(0deg); }
100% { opacity: 0.8; transform: scale(1.06) rotate(2deg); }
}

/* ─── FLOATING HEARTS ─── */
#hearts-canvas {
position: fixed;
inset: 0;
pointer-events: none;
z-index: 1;
}

/* ─── LAYOUT ─── */
.page {
position: relative;
z-index: 2;
max-width: 860px;
margin: 0 auto;
padding: 2rem 1.2rem 5rem;
}

/* ─── GLASS CARD ─── */
.card {
background: var(–glass-bg);
border: 1.5px solid var(–glass-border);
border-radius: 28px;
backdrop-filter: blur(18px);
-webkit-backdrop-filter: blur(18px);
box-shadow: 0 8px 40px var(–shadow-pink), 0 1px 0 rgba(255,255,255,0.6) inset;
padding: 2.4rem 2rem;
margin-bottom: 2rem;
transition: transform 0.35s ease, box-shadow 0.35s ease;
}
.card:hover {
transform: translateY(-4px) scale(1.01);
box-shadow: 0 16px 56px var(–shadow-pink), 0 1px 0 rgba(255,255,255,0.7) inset;
}

/* ─── HERO ─── */
.hero {
text-align: center;
padding: 3.5rem 2rem 3rem;
position: relative;
overflow: hidden;
}
.hero::after {
content: ‘’;
position: absolute;
inset: -40%;
background: radial-gradient(circle at 50% 40%, rgba(255,110,180,0.18) 0%, transparent 65%);
animation: heroPulse 4s ease-in-out infinite;
pointer-events: none;
}
@keyframes heroPulse {
0%, 100% { opacity: 0.6; transform: scale(1); }
50%       { opacity: 1;   transform: scale(1.08); }
}

.bird-bounce {
font-size: 3.5rem;
display: inline-block;
animation: birdBounce 1.8s ease-in-out infinite;
filter: drop-shadow(0 4px 12px rgba(255,110,180,0.5));
}
@keyframes birdBounce {
0%, 100% { transform: translateY(0) rotate(-6deg); }
50%       { transform: translateY(-18px) rotate(6deg); }
}

.hero-title {
font-family: ‘Playfair Display’, serif;
font-size: clamp(2.6rem, 8vw, 4.8rem);
font-weight: 700;
line-height: 1.15;
background: linear-gradient(135deg, #e11d74 0%, #9333ea 50%, #fb7185 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
letter-spacing: -0.5px;
margin: 0.6rem 0 0.4rem;
animation: titleAppear 1s cubic-bezier(0.22,1,0.36,1) forwards;
opacity: 0;
transform: translateY(30px);
}
@keyframes titleAppear {
to { opacity: 1; transform: translateY(0); }
}

.hero-subtitle {
font-size: clamp(1.1rem, 3.5vw, 1.5rem);
font-weight: 600;
color: var(–purple-deep);
letter-spacing: 0.5px;
animation: titleAppear 1s 0.25s cubic-bezier(0.22,1,0.36,1) forwards;
opacity: 0;
transform: translateY(20px);
}

.hero-divider {
margin: 1.4rem auto;
width: 80px;
height: 3px;
background: linear-gradient(90deg, transparent, var(–pink-deep), var(–purple-mid), transparent);
border-radius: 99px;
animation: titleAppear 1s 0.45s forwards;
opacity: 0;
}

/* ─── TYPEWRITER ─── */
.typewriter-wrap {
font-family: ‘Playfair Display’, serif;
font-style: italic;
font-size: clamp(1rem, 2.8vw, 1.25rem);
color: #7c3aed;
line-height: 1.75;
text-align: center;
min-height: 5.5em;
animation: titleAppear 1s 0.65s forwards;
opacity: 0;
transform: translateY(10px);
}
#typewriter-cursor {
display: inline-block;
width: 2px;
height: 1.1em;
background: var(–pink-deep);
margin-left: 2px;
vertical-align: text-bottom;
animation: blink 0.75s step-end infinite;
}
@keyframes blink {
0%, 100% { opacity: 1; } 50% { opacity: 0; }
}

/* ─── SECTION TITLES ─── */
.section-title {
font-family: ‘Playfair Display’, serif;
font-size: clamp(1.5rem, 4vw, 2rem);
font-weight: 700;
text-align: center;
margin-bottom: 1.4rem;
background: linear-gradient(135deg, #be185d, #7c3aed);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

/* ─── ROMANTIC MESSAGE ─── */
.romantic-text {
font-size: clamp(0.97rem, 2.5vw, 1.12rem);
line-height: 1.9;
color: #6b21a8;
text-align: center;
}
.romantic-text .highlight {
font-family: ‘Playfair Display’, serif;
font-style: italic;
color: #be185d;
font-weight: 600;
}

/* ─── MEME SECTION ─── */
.meme-card {
background: linear-gradient(135deg, rgba(255,228,235,0.6), rgba(237,233,254,0.6));
}
.meme-line {
display: flex;
align-items: flex-start;
gap: 0.8rem;
padding: 0.95rem 1rem;
border-radius: 14px;
background: rgba(255,255,255,0.45);
margin-bottom: 0.85rem;
border: 1px solid rgba(255,255,255,0.55);
font-size: clamp(0.93rem, 2.4vw, 1.05rem);
color: #5b2d6e;
line-height: 1.6;
transition: transform 0.25s ease, background 0.25s ease;
}
.meme-line:hover {
transform: translateX(6px);
background: rgba(255,255,255,0.65);
}
.meme-line:last-child { margin-bottom: 0; }
.meme-emoji { font-size: 1.6rem; flex-shrink: 0; margin-top: 1px; }

/* ─── REASONS LIST ─── */
.reasons-list { list-style: none; }
.reason-item {
display: flex;
align-items: flex-start;
gap: 0.9rem;
padding: 0.9rem 1rem;
border-radius: 14px;
background: rgba(255,255,255,0.35);
margin-bottom: 0.75rem;
border: 1px solid rgba(255,255,255,0.5);
font-size: clamp(0.93rem, 2.4vw, 1.05rem);
color: #5b2d6e;
line-height: 1.65;
opacity: 0;
transform: translateX(-30px);
transition: transform 0.3s ease, background 0.25s ease;
}
.reason-item.visible {
animation: slideIn 0.55s cubic-bezier(0.22,1,0.36,1) forwards;
}
.reason-item:hover {
background: rgba(255,255,255,0.55);
transform: translateX(5px) !important;
}
@keyframes slideIn {
to { opacity: 1; transform: translateX(0); }
}
.reason-num {
font-family: ‘Playfair Display’, serif;
font-weight: 700;
font-size: 1.2rem;
color: var(–pink-deep);
flex-shrink: 0;
margin-top: 1px;
}

/* ─── SURPRISE BUTTON ─── */
.surprise-wrap { text-align: center; }
.btn-surprise {
display: inline-block;
padding: 1rem 2.6rem;
font-family: ‘Quicksand’, sans-serif;
font-size: 1.15rem;
font-weight: 700;
color: #fff;
background: linear-gradient(135deg, #e11d74, #9333ea, #fb7185);
background-size: 200% 200%;
border: none;
border-radius: 50px;
cursor: pointer;
letter-spacing: 0.4px;
box-shadow: 0 6px 28px rgba(225,29,116,0.4), 0 2px 0 rgba(255,255,255,0.25) inset;
animation: gradShift 3s ease infinite;
transition: transform 0.25s ease, box-shadow 0.25s ease;
position: relative;
overflow: hidden;
}
.btn-surprise::before {
content: ‘’;
position: absolute;
inset: 0;
background: rgba(255,255,255,0);
transition: background 0.2s;
}
.btn-surprise:hover {
transform: scale(1.06) translateY(-2px);
box-shadow: 0 12px 40px rgba(225,29,116,0.5), 0 2px 0 rgba(255,255,255,0.3) inset;
}
.btn-surprise:active { transform: scale(0.97); }
@keyframes gradShift {
0%   { background-position: 0% 50%; }
50%  { background-position: 100% 50%; }
100% { background-position: 0% 50%; }
}

/* ─── SURPRISE REVEAL ─── */
#surprise-msg {
display: none;
margin-top: 1.8rem;
padding: 1.8rem;
border-radius: 20px;
background: linear-gradient(135deg, rgba(255,182,217,0.4), rgba(196,130,252,0.4));
border: 1.5px solid rgba(255,255,255,0.6);
text-align: center;
font-family: ‘Playfair Display’, serif;
font-style: italic;
font-size: clamp(1.05rem, 2.8vw, 1.25rem);
color: #6b21a8;
line-height: 1.8;
animation: surpriseReveal 0.7s cubic-bezier(0.22,1,0.36,1) forwards;
}
@keyframes surpriseReveal {
from { opacity: 0; transform: scale(0.85) translateY(20px); }
to   { opacity: 1; transform: scale(1) translateY(0); }
}
#surprise-msg .big-heart {
font-size: 2.5rem;
display: block;
margin-bottom: 0.7rem;
animation: bigHeartBeat 1s ease-in-out infinite;
}
@keyframes bigHeartBeat {
0%, 100% { transform: scale(1); }
30%       { transform: scale(1.25); }
60%       { transform: scale(0.95); }
}

/* ─── SCREEN GLOW ─── */
#screen-glow {
position: fixed;
inset: 0;
pointer-events: none;
z-index: 999;
background: radial-gradient(circle at 50% 50%, rgba(255,110,180,0.28), transparent 65%);
opacity: 0;
transition: opacity 0.4s ease;
}
#screen-glow.active {
animation: glowPulse 1.8s ease-out forwards;
}
@keyframes glowPulse {
0%   { opacity: 0; }
20%  { opacity: 1; }
100% { opacity: 0; }
}

/* ─── CONFETTI CANVAS ─── */
#confetti-canvas {
position: fixed;
inset: 0;
pointer-events: none;
z-index: 998;
}

/* ─── MUSIC PLAYER ─── */
.music-bar {
display: flex;
align-items: center;
gap: 1rem;
justify-content: center;
padding: 1rem 1.5rem;
}
.btn-music {
width: 52px;
height: 52px;
border-radius: 50%;
border: 2px solid rgba(255,255,255,0.6);
background: linear-gradient(135deg, #ff6eb4, #9333ea);
color: #fff;
font-size: 1.3rem;
cursor: pointer;
display: flex;
align-items: center;
justify-content: center;
box-shadow: 0 4px 16px rgba(255,110,180,0.35);
transition: transform 0.2s ease, box-shadow 0.2s ease;
flex-shrink: 0;
}
.btn-music:hover {
transform: scale(1.1);
box-shadow: 0 8px 24px rgba(255,110,180,0.5);
}
.music-label {
font-size: 0.92rem;
color: #7c3aed;
font-weight: 500;
}
.music-wave {
display: flex;
align-items: center;
gap: 3px;
height: 24px;
}
.wave-bar {
width: 4px;
border-radius: 4px;
background: linear-gradient(180deg, #ff6eb4, #9333ea);
animation: waveDance 1s ease-in-out infinite;
height: 8px;
}
.wave-bar:nth-child(1) { animation-delay: 0s;    }
.wave-bar:nth-child(2) { animation-delay: 0.15s; }
.wave-bar:nth-child(3) { animation-delay: 0.3s;  }
.wave-bar:nth-child(4) { animation-delay: 0.45s; }
.wave-bar:nth-child(5) { animation-delay: 0.6s;  }
.wave-bar.playing {
animation: waveDanceTall 0.6s ease-in-out infinite alternate;
}
.wave-bar:nth-child(1).playing { animation-delay: 0s;    height: 14px; }
.wave-bar:nth-child(2).playing { animation-delay: 0.12s; height: 22px; }
.wave-bar:nth-child(3).playing { animation-delay: 0.08s; height: 18px; }
.wave-bar:nth-child(4).playing { animation-delay: 0.2s;  height: 24px; }
.wave-bar:nth-child(5).playing { animation-delay: 0.05s; height: 12px; }
@keyframes waveDanceTall {
from { transform: scaleY(0.4); }
to   { transform: scaleY(1); }
}
@keyframes waveDance {
0%, 100% { transform: scaleY(0.5); }
50%       { transform: scaleY(1.1); }
}

/* ─── FOOTER ─── */
.footer {
text-align: center;
font-size: 0.88rem;
color: #a855f7;
margin-top: 1rem;
padding-bottom: 1rem;
opacity: 0.75;
}
.footer span { font-size: 1rem; }

/* ─── RESPONSIVE ─── */
@media (max-width: 520px) {
.card { padding: 1.8rem 1.2rem; }
.hero { padding: 2.5rem 1rem 2rem; }
}
</style>

</head>
<body>

<!-- Floating hearts -->

<canvas id="hearts-canvas"></canvas>

<!-- Confetti -->

<canvas id="confetti-canvas"></canvas>

<!-- Screen glow overlay -->

<div id="screen-glow"></div>

<div class="page">

  <!-- ── HERO ── -->

  <div class="card hero">
    <div class="bird-bounce">🐦</div>
    <h1 class="hero-title">Happy Birthday Bernys 💖</h1>
    <p class="hero-subtitle">My Bubwa Birdling 🐦💕</p>
    <div class="hero-divider"></div>
    <div class="typewriter-wrap">
      <span id="typewriter-text"></span><span id="typewriter-cursor"></span>
    </div>
  </div>

  <!-- ── ROMANTIC MESSAGE ── -->

  <div class="card">
    <h2 class="section-title">A Word From My Heart 🌸</h2>
    <p class="romantic-text">
      There are people who walk into your life quietly, and then there is you — who apparently decided to walk in
      <span class="highlight">singing</span>, 
      rearrange all the furniture, and somehow make everything look better.<br><br>
      You are the kind of rare that doesn't know it's rare. The kind that laughs too freely, loves too genuinely,
      and makes ordinary Tuesday evenings feel like something worth remembering.<br><br>
      On your birthday, I want you to know: <span class="highlight">the world is genuinely better with you in it.</span>
      Not in a greeting-card way — in the actual, specific, irreplaceable way that only <em>you</em> can be.
    </p>
  </div>

  <!-- ── MEME / FUNNY ── -->

  <div class="card meme-card">
    <h2 class="section-title">The Honest Section 😭✨</h2>

```
<div class="meme-line">
  <span class="meme-emoji">🧠</span>
  <span>
    Bernys is so <strong>naturally brilliant</strong> that she once convinced everyone around her she was struggling — 
    just to make the rest of us feel better. Iconic, really. Unmatched humility. Nobel Prize pending.
  </span>
</div>

<div class="meme-line">
  <span class="meme-emoji">🐦</span>
  <span>
    "Bubwa Birdling" is a name with <strong>zero chill</strong> and <strong>maximum charm</strong> — 
    exactly like the person it describes. You didn't choose the Birdling life. The Birdling life chose you. 
    And honestly? Correct choice.
  </span>
</div>

<div class="meme-line">
  <span class="meme-emoji">🎂</span>
  <span>
    Another year older, <strong>zero percent more ordinary.</strong>
    Scientists are baffled. Mathematicians gave up. You just keep being you, which is frankly unfair to the rest of humanity.
  </span>
</div>
```

  </div>

  <!-- ── REASONS ── -->

  <div class="card">
    <h2 class="section-title">Why You're Genuinely Amazing 💫</h2>
    <ul class="reasons-list" id="reasons-list">
      <li class="reason-item">
        <span class="reason-num">01</span>
        <span>Your laugh is the kind that makes strangers in a room feel like they missed a joke they desperately want to be in on.</span>
      </li>
      <li class="reason-item">
        <span class="reason-num">02</span>
        <span>You carry warmth the way the sun does — not by trying, but just by showing up. And it always reaches people.</span>
      </li>
      <li class="reason-item">
        <span class="reason-num">03</span>
        <span>You have the rare ability to make someone feel truly seen — like their words actually landed somewhere safe.</span>
      </li>
      <li class="reason-item">
        <span class="reason-num">04</span>
        <span>Your stubbornness is actually quiet strength wearing a disguise. It's pulled you through more than most would admit.</span>
      </li>
      <li class="reason-item">
        <span class="reason-num">05</span>
        <span>You dream without apology. That takes more courage than people realize, and you do it like it's nothing.</span>
      </li>
      <li class="reason-item">
        <span class="reason-num">06</span>
        <span>Somehow, you make kindness look effortless — and that's the most powerful kind of kindness there is.</span>
      </li>
    </ul>
  </div>

  <!-- ── SURPRISE ── -->

  <div class="card surprise-wrap">
    <h2 class="section-title">There's Something Else… 🎁</h2>
    <p style="text-align:center; margin-bottom:1.5rem; color:#7c3aed; font-size:0.97rem;">
      (This one's just between us.)
    </p>
    <button class="btn-surprise" id="btn-surprise" onclick="revealSurprise()">
      Click for Surprise 🎁
    </button>

```
<div id="surprise-msg">
  <span class="big-heart">💖</span>
  Here it is, quietly and without fuss:<br><br>
  <em>You are someone I am genuinely, completely, ridiculously grateful exists.</em><br><br>
  Not just today. Every day. But especially today — because today you get to be celebrated,
  and that feels exactly right for someone who deserves it as much as you do.<br><br>
  Happy Birthday, Bernys Bubwa Birdling. 🐦✨<br>
  May this year give back everything you give to the world — and then some.
</div>
```

  </div>

  <!-- ── MUSIC ── -->

  <div class="card">
    <div class="music-bar">
      <button class="btn-music" id="btn-music" onclick="toggleMusic()" title="Play music">▶</button>
      <div>
        <div class="music-label">Birthday Ambience 🎵</div>
        <div style="font-size:0.8rem; color:#a855f7; margin-top:2px;">Press play for the full experience</div>
      </div>
      <div class="music-wave" id="music-wave">
        <div class="wave-bar"></div>
        <div class="wave-bar"></div>
        <div class="wave-bar"></div>
        <div class="wave-bar"></div>
        <div class="wave-bar"></div>
      </div>
    </div>
    <!-- Web Audio API tone generator — no external files needed -->
    <audio id="bg-audio" loop></audio>
  </div>

  <div class="footer">
    Made with <span>💖</span> for the one and only Bernys · <span>🐦</span>
  </div>
</div>

<script>
/* ═══════════════════════════════════════════
   FLOATING HEARTS
═══════════════════════════════════════════ */
(function() {
  const canvas = document.getElementById('hearts-canvas');
  const ctx = canvas.getContext('2d');
  let hearts = [];

  function resize() {
    canvas.width  = window.innerWidth;
    canvas.height = window.innerHeight;
  }
  resize();
  window.addEventListener('resize', resize);

  function heartPath(ctx, x, y, size) {
    ctx.save();
    ctx.translate(x, y);
    ctx.beginPath();
    const s = size / 30;
    ctx.moveTo(0, -5 * s);
    ctx.bezierCurveTo(5 * s, -15 * s,  20 * s, -5 * s, 0, 10 * s);
    ctx.bezierCurveTo(-20 * s, -5 * s, -5 * s, -15 * s, 0, -5 * s);
    ctx.closePath();
    ctx.restore();
  }

  const COLORS = ['#ff6eb4','#fb7185','#c084fc','#f9a8d4','#e879f9','#fda4af'];

  function spawnHeart() {
    hearts.push({
      x: Math.random() * window.innerWidth,
      y: window.innerHeight + 20,
      size: 8 + Math.random() * 18,
      speed: 0.6 + Math.random() * 1.2,
      drift: (Math.random() - 0.5) * 0.6,
      alpha: 0.3 + Math.random() * 0.5,
      color: COLORS[Math.floor(Math.random() * COLORS.length)],
      rot: (Math.random() - 0.5) * 0.04,
      angle: 0,
    });
  }

  let frame = 0;
  function animate() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    frame++;
    if (frame % 28 === 0) spawnHeart();

    hearts = hearts.filter(h => h.y > -60);
    for (const h of hearts) {
      h.y -= h.speed;
      h.x += h.drift + Math.sin(h.y * 0.02) * 0.4;
      h.angle += h.rot;

      ctx.save();
      ctx.globalAlpha = h.alpha;
      ctx.translate(h.x, h.y);
      ctx.rotate(h.angle);
      heartPath(ctx, 0, 0, h.size);
      ctx.fillStyle = h.color;
      ctx.fill();
      ctx.restore();
    }
    requestAnimationFrame(animate);
  }
  for (let i = 0; i < 8; i++) {
    const h = {
      x: Math.random() * window.innerWidth,
      y: Math.random() * window.innerHeight,
      size: 8 + Math.random() * 18,
      speed: 0.6 + Math.random() * 1.2,
      drift: (Math.random() - 0.5) * 0.6,
      alpha: 0.3 + Math.random() * 0.5,
      color: COLORS[Math.floor(Math.random() * COLORS.length)],
      rot: (Math.random() - 0.5) * 0.04,
      angle: 0,
    };
    hearts.push(h);
  }
  animate();
})();

/* ═══════════════════════════════════════════
   TYPEWRITER
═══════════════════════════════════════════ */
(function() {
  const msg = "Every birthday should feel like the universe is finally pausing to say: 'You — yes, you — were a really good idea.' And you, Bernys, were a magnificent one. 💖";
  const el = document.getElementById('typewriter-text');
  let i = 0;
  function type() {
    if (i <= msg.length) {
      el.textContent = msg.slice(0, i);
      i++;
      setTimeout(type, i === 1 ? 600 : 36 + Math.random() * 18);
    }
  }
  setTimeout(type, 1200);
})();

/* ═══════════════════════════════════════════
   REASONS SCROLL ANIMATION
═══════════════════════════════════════════ */
(function() {
  const items = document.querySelectorAll('.reason-item');
  const observer = new IntersectionObserver(entries => {
    entries.forEach((entry, _) => {
      if (entry.isIntersecting) {
        const idx = Array.from(items).indexOf(entry.target);
        setTimeout(() => entry.target.classList.add('visible'), idx * 120);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.2 });
  items.forEach(item => observer.observe(item));
})();

/* ═══════════════════════════════════════════
   CONFETTI
═══════════════════════════════════════════ */
const confettiCanvas = document.getElementById('confetti-canvas');
const confCtx = confettiCanvas.getContext('2d');
let confettiParticles = [];

function resizeConfetti() {
  confettiCanvas.width  = window.innerWidth;
  confettiCanvas.height = window.innerHeight;
}
resizeConfetti();
window.addEventListener('resize', resizeConfetti);

const CONF_COLORS = ['#ff6eb4','#fb7185','#c084fc','#fbbf24','#34d399','#60a5fa','#f472b6','#a78bfa'];

function spawnConfetti(x, y) {
  for (let i = 0; i < 120; i++) {
    confettiParticles.push({
      x: x ?? confettiCanvas.width / 2,
      y: y ?? confettiCanvas.height / 3,
      vx: (Math.random() - 0.5) * 14,
      vy: -8 - Math.random() * 10,
      gravity: 0.38,
      rot: Math.random() * 360,
      rotSpeed: (Math.random() - 0.5) * 8,
      size: 6 + Math.random() * 8,
      color: CONF_COLORS[Math.floor(Math.random() * CONF_COLORS.length)],
      alpha: 1,
      shape: Math.random() > 0.5 ? 'rect' : 'circle',
    });
  }
}

let confRunning = false;
function runConfetti() {
  if (!confRunning) return;
  confCtx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height);
  confettiParticles = confettiParticles.filter(p => p.alpha > 0.02);

  for (const p of confettiParticles) {
    p.x  += p.vx;
    p.y  += p.vy;
    p.vy += p.gravity;
    p.vx *= 0.99;
    p.rot += p.rotSpeed;
    if (p.y > confettiCanvas.height * 0.4) p.alpha -= 0.012;

    confCtx.save();
    confCtx.globalAlpha = Math.max(0, p.alpha);
    confCtx.translate(p.x, p.y);
    confCtx.rotate(p.rot * Math.PI / 180);
    confCtx.fillStyle = p.color;
    if (p.shape === 'rect') {
      confCtx.fillRect(-p.size / 2, -p.size / 4, p.size, p.size / 2);
    } else {
      confCtx.beginPath();
      confCtx.arc(0, 0, p.size / 2, 0, Math.PI * 2);
      confCtx.fill();
    }
    confCtx.restore();
  }

  if (confettiParticles.length > 0) requestAnimationFrame(runConfetti);
  else { confRunning = false; confCtx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height); }
}

/* ═══════════════════════════════════════════
   SURPRISE REVEAL
═══════════════════════════════════════════ */
function revealSurprise() {
  const msg = document.getElementById('surprise-msg');
  const btn = document.getElementById('btn-surprise');
  const glow = document.getElementById('screen-glow');

  // Show message
  msg.style.display = 'block';
  btn.style.display = 'none';

  // Confetti burst
  const btnRect = btn.getBoundingClientRect();
  spawnConfetti(btnRect.left + btnRect.width / 2, btnRect.top + btnRect.height / 2);
  confRunning = true;
  runConfetti();

  // Glow
  glow.classList.remove('active');
  void glow.offsetWidth;
  glow.classList.add('active');
  setTimeout(() => glow.classList.remove('active'), 2000);
}

/* ═══════════════════════════════════════════
   MUSIC (Web Audio API — no external files)
═══════════════════════════════════════════ */
let audioCtx = null;
let musicNodes = [];
let musicPlaying = false;

function buildMelody(ctx) {
  // Gentle ambient birthday-ish tones using oscillators
  const notes = [261.63, 329.63, 392, 329.63, 261.63, 293.66, 349.23, 392, 349.23, 293.66];
  const master = ctx.createGain();
  master.gain.setValueAtTime(0.08, ctx.currentTime);
  master.connect(ctx.destination);

  const reverb = ctx.createConvolver();
  const revBuf = ctx.createBuffer(2, ctx.sampleRate * 2, ctx.sampleRate);
  for (let ch = 0; ch < 2; ch++) {
    const d = revBuf.getChannelData(ch);
    for (let i = 0; i < d.length; i++) d[i] = (Math.random() * 2 - 1) * Math.pow(1 - i / d.length, 3);
  }
  reverb.buffer = revBuf;
  reverb.connect(master);

  let time = ctx.currentTime;
  const step = 0.85;
  const allNodes = [];

  function scheduleLoop() {
    notes.forEach((freq, idx) => {
      const osc = ctx.createOscillator();
      const gain = ctx.createGain();
      osc.type = 'sine';
      osc.frequency.setValueAtTime(freq, time + idx * step);
      gain.gain.setValueAtTime(0, time + idx * step);
      gain.gain.linearRampToValueAtTime(0.5, time + idx * step + 0.08);
      gain.gain.linearRampToValueAtTime(0, time + idx * step + step * 0.8);
      osc.connect(gain);
      gain.connect(reverb);
      osc.start(time + idx * step);
      osc.stop(time + idx * step + step);
      allNodes.push(osc, gain);
    });
    time += notes.length * step;

    // Subtle pad underneath
    const pad = ctx.createOscillator();
    const padGain = ctx.createGain();
    pad.type = 'sine';
    pad.frequency.value = 130.81;
    padGain.gain.setValueAtTime(0.12, ctx.currentTime);
    pad.connect(padGain);
    padGain.connect(master);
    pad.start();
    allNodes.push(pad, padGain, master, reverb);
    return allNodes;
  }
  return scheduleLoop();
}

function toggleMusic() {
  const btn = document.getElementById('btn-music');
  const waveBars = document.querySelectorAll('.wave-bar');

  if (!musicPlaying) {
    if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
    if (audioCtx.state === 'suspended') audioCtx.resume();
    musicNodes = buildMelody(audioCtx);
    musicPlaying = true;
    btn.textContent = '⏸';
    waveBars.forEach(b => b.classList.add('playing'));
  } else {
    if (audioCtx) {
      musicNodes.forEach(n => { try { n.stop ? n.stop() : n.disconnect(); } catch(_) {} });
      musicNodes = [];
      audioCtx.close();
      audioCtx = null;
    }
    musicPlaying = false;
    btn.textContent = '▶';
    waveBars.forEach(b => b.classList.remove('playing'));
  }
}
</script>

</body>
</html>
CC
