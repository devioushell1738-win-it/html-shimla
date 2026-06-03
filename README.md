<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Shimla — Into the Wild Himalayas</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Barlow+Condensed:wght@300;400;600;700&family=Barlow:wght@300;400&display=swap" rel="stylesheet"/>
<style>
:root{--pine:#1a2e1a;--snow:#f4f0eb;--mist:#c8d8d0;--frost:#7aa89a;--gold:#d4a84b;--rust:#b5451b;--ink:#0e1a12}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--ink);color:var(--snow);font-family:'Barlow',sans-serif;font-weight:300;overflow-x:hidden}
.hero{position:relative;height:100vh;min-height:680px;display:flex;flex-direction:column;justify-content:flex-end;overflow:hidden}
.hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse at 70% 30%,rgba(122,168,154,.18) 0%,transparent 60%),radial-gradient(ellipse at 20% 80%,rgba(181,69,27,.12) 0%,transparent 50%),linear-gradient(170deg,#0e1a12 0%,#1a2e1a 40%,#0e1a12 100%);z-index:0}
.mountains{position:absolute;bottom:0;left:0;right:0;height:55%;z-index:1}
.mountains svg{width:100%;height:100%}
.snow-layer{position:absolute;inset:0;z-index:2;pointer-events:none;overflow:hidden}
.flake{position:absolute;top:-10px;width:4px;height:4px;border-radius:50%;background:rgba(244,240,235,.6);animation:snowfall linear infinite}
@keyframes snowfall{to{transform:translateY(110vh) translateX(30px);opacity:0}}
.flake:nth-child(1){left:5%;width:3px;height:3px;animation-duration:8s}
.flake:nth-child(2){left:15%;width:2px;height:2px;animation-duration:11s;animation-delay:2s}
.flake:nth-child(3){left:25%;animation-duration:9s;animation-delay:1s}
.flake:nth-child(4){left:35%;width:2px;height:2px;animation-duration:13s;animation-delay:3s}
.flake:nth-child(5){left:45%;width:3px;height:3px;animation-duration:10s;animation-delay:.5s}
.flake:nth-child(6){left:55%;width:2px;height:2px;animation-duration:12s;animation-delay:4s}
.flake:nth-child(7){left:65%;animation-duration:8s;animation-delay:1.5s}
.flake:nth-child(8){left:75%;width:3px;height:3px;animation-duration:11s;animation-delay:2.5s}
.flake:nth-child(9){left:85%;width:2px;height:2px;animation-duration:9s;animation-delay:5s}
.flake:nth-child(10){left:92%;width:3px;height:3px;animation-duration:14s}
.hero-content{position:relative;z-index:10;padding:0 6vw 7vh}
.hero-tag{font-family:'Barlow Condensed',sans-serif;font-size:.75rem;letter-spacing:.35em;text-transform:uppercase;color:var(--gold);margin-bottom:1.2rem;opacity:0;animation:fadeUp .8s ease forwards .3s}
.hero-title{font-family:'Playfair Display',serif;font-size:clamp(3.5rem,9vw,8.5rem);font-weight:900;line-height:.92;letter-spacing:-.02em;color:var(--snow);opacity:0;animation:fadeUp .9s ease forwards .5s}
.hero-title em{font-style:italic;color:var(--frost)}
.hero-subtitle{margin-top:1.8rem;font-size:1.05rem;color:var(--mist);max-width:420px;line-height:1.7;opacity:0;animation:fadeUp .9s ease forwards .75s}
.hero-cta{margin-top:2.5rem;display:inline-block;font-family:'Barlow Condensed',sans-serif;font-size:.85rem;font-weight:600;letter-spacing:.2em;text-transform:uppercase;color:var(--ink);background:var(--gold);padding:1rem 2.4rem;text-decoration:none;position:relative;overflow:hidden;transition:color .3s;opacity:0;animation:fadeUp .9s ease forwards 1s}
.hero-cta::before{content:'';position:absolute;inset:0;background:var(--rust);transform:translateX(-101%);transition:transform .4s cubic-bezier(.4,0,0,1)}
.hero-cta:hover::before{transform:translateX(0)}
.hero-cta span{position:relative;z-index:1}
.hero-cta:hover{color:var(--snow)}
.elevation-badge{position:absolute;top:2.5rem;right:6vw;z-index:10;text-align:right;opacity:0;animation:fadeUp .8s ease forwards 1.2s}
.elevation-badge .num{font-family:'Playfair Display',serif;font-size:3.5rem;font-weight:700;color:var(--gold);line-height:1}
.elevation-badge .label{font-family:'Barlow Condensed',sans-serif;font-size:.7rem;letter-spacing:.25em;text-transform:uppercase;color:var(--mist)}
@keyframes fadeUp{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}
.strip{background:var(--gold);color:var(--ink);font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:.78rem;letter-spacing:.25em;text-transform:uppercase;padding:.9rem 0;overflow:hidden;white-space:nowrap}
.strip-inner{display:inline-flex;gap:3rem;animation:marquee 22s linear infinite}
.strip-inner span::before{content:'✦ '}
@keyframes marquee{from{transform:translateX(0)}to{transform:translateX(-50%)}}
section{padding:7rem 6vw}
.section-tag{font-family:'Barlow Condensed',sans-serif;font-size:.72rem;letter-spacing:.3em;text-transform:uppercase;color:var(--gold);margin-bottom:.8rem}
.section-heading{font-family:'Playfair Display',serif;font-size:clamp(2rem,4.5vw,3.8rem);font-weight:700;line-height:1.1;color:var(--snow)}
.section-heading em{font-style:italic;color:var(--frost)}
.about{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center;border-top:1px solid rgba(244,240,235,.08)}
.about-card{background:linear-gradient(135deg,var(--pine) 0%,#0e1a12 100%);border:1px solid rgba(122,168,154,.2);padding:3rem}
.compass{width:120px;height:120px;margin:0 auto 2rem;display:block;animation:spin 20s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
.stats-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:2.5rem}
.stat{border-left:2px solid var(--gold);padding-left:1rem}
.stat-num{font-family:'Playfair Display',serif;font-size:2.2rem;font-weight:700;color:var(--gold);line-height:1}
.stat-label{font-size:.78rem;color:var(--mist);margin-top:.2rem}
.about-text p{color:rgba(244,240,235,.75);line-height:1.85;font-size:1rem;margin-bottom:1.5rem}
.adventures{background:var(--pine)}
.adventures-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:4rem;flex-wrap:wrap;gap:1.5rem}
.cards-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5px}
.adventure-card{position:relative;aspect-ratio:3/4;overflow:hidden;cursor:pointer;background:var(--ink)}
.adventure-card:first-child{aspect-ratio:unset;grid-row:span 2}
.card-bg{position:absolute;inset:0;transition:transform .6s cubic-bezier(.4,0,0,1)}
.adventure-card:hover .card-bg{transform:scale(1.06)}
.card-bg-1{background:url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=800&q=80') center/cover no-repeat}
.card-bg-2{background:url('https://images.unsplash.com/photo-1551524559-8af4e6624178?w=800&q=80') center/cover no-repeat}
.card-bg-3{background:url('https://images.unsplash.com/photo-1474487548417-781cb71495f3?w=800&q=80') center/cover no-repeat}
.card-bg-4{background:url('https://images.unsplash.com/photo-1448375240586-882707db888b?w=800&q=80') center/cover no-repeat}
.card-icon{position:absolute;top:1.5rem;left:1.5rem;width:48px;height:48px;border:1px solid rgba(212,168,75,.4);display:flex;align-items:center;justify-content:center;font-size:1.4rem;background:rgba(14,26,18,.6);backdrop-filter:blur(4px)}
.card-info{position:absolute;bottom:0;left:0;right:0;padding:2rem 1.8rem}
.card-difficulty{font-family:'Barlow Condensed',sans-serif;font-size:.65rem;letter-spacing:.3em;text-transform:uppercase;color:var(--gold);margin-bottom:.5rem}
.card-name{font-family:'Playfair Display',serif;font-size:1.5rem;font-weight:700;line-height:1.15;color:var(--snow)}
.card-desc{font-size:.82rem;color:var(--mist);margin-top:.5rem;line-height:1.5}
.itinerary{border-top:1px solid rgba(244,240,235,.08)}
.timeline{margin-top:4rem;position:relative}
.timeline::before{content:'';position:absolute;left:3.5rem;top:0;bottom:0;width:1px;background:linear-gradient(to bottom,var(--gold),transparent)}
.timeline-item{display:grid;grid-template-columns:7rem 1fr;gap:2rem;margin-bottom:3.5rem;position:relative}
.day-label{text-align:right;padding-top:.1rem;position:relative}
.day-label::after{content:'';position:absolute;right:-2.5rem;top:.5rem;width:10px;height:10px;border-radius:50%;background:var(--gold);border:2px solid var(--ink);box-shadow:0 0 0 4px rgba(212,168,75,.2)}
.day-num{font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;color:var(--gold);line-height:1}
.day-text{font-family:'Barlow Condensed',sans-serif;font-size:.65rem;letter-spacing:.2em;text-transform:uppercase;color:var(--mist)}
.day-content h3{font-family:'Playfair Display',serif;font-size:1.4rem;font-weight:700;color:var(--snow);margin-bottom:.6rem}
.day-content p{color:rgba(244,240,235,.65);font-size:.9rem;line-height:1.8}
.day-tags{display:flex;flex-wrap:wrap;gap:.5rem;margin-top:1rem}
.day-tag{font-family:'Barlow Condensed',sans-serif;font-size:.65rem;letter-spacing:.15em;text-transform:uppercase;padding:.3rem .8rem;border:1px solid rgba(122,168,154,.3);color:var(--frost)}
.essentials{background:var(--pine);display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start}
.pack-list{margin-top:2.5rem;list-style:none}
.pack-list li{display:flex;align-items:center;gap:1rem;padding:1rem 0;border-bottom:1px solid rgba(244,240,235,.06);font-size:.92rem;color:rgba(244,240,235,.75)}
.pack-list li::before{content:attr(data-icon);font-size:1.2rem;flex-shrink:0}
.best-time-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:.8rem;margin-top:2.5rem}
.month-card{padding:1rem;text-align:center;border:1px solid rgba(244,240,235,.06)}
.month-card.peak{background:rgba(212,168,75,.1);border-color:rgba(212,168,75,.3)}
.month-name{font-family:'Barlow Condensed',sans-serif;font-size:.7rem;letter-spacing:.15em;text-transform:uppercase;color:var(--mist)}
.month-card.peak .month-name{color:var(--gold)}
.month-icon{font-size:1.5rem;margin:.4rem 0}
.quote-section{text-align:center;padding:6rem 6vw 8rem;background:var(--ink);border-top:1px solid rgba(244,240,235,.06);position:relative;overflow:hidden}
.quote-section::before{content:'"';position:absolute;top:-2rem;left:50%;transform:translateX(-50%);font-family:'Playfair Display',serif;font-size:18rem;color:rgba(122,168,154,.04);line-height:1;pointer-events:none}
.quote-text{font-family:'Playfair Display',serif;font-style:italic;font-size:clamp(1.5rem,3.5vw,2.8rem);color:var(--snow);max-width:750px;margin:0 auto;line-height:1.45;position:relative}
.quote-attr{margin-top:2rem;font-family:'Barlow Condensed',sans-serif;font-size:.75rem;letter-spacing:.3em;text-transform:uppercase;color:var(--gold)}
footer{background:var(--pine);padding:2rem 6vw;display:flex;justify-content:space-between;align-items:center;font-family:'Barlow Condensed',sans-serif;font-size:.72rem;letter-spacing:.15em;text-transform:uppercase;color:rgba(244,240,235,.35);flex-wrap:wrap;gap:1rem}
footer span{color:var(--gold)}
.reveal{opacity:0;transform:translateY(30px);transition:opacity .8s ease,transform .8s ease}
.reveal.visible{opacity:1;transform:translateY(0)}
@media(max-width:860px){.about{grid-template-columns:1fr;gap:3rem}.cards-grid{grid-template-columns:1fr 1fr}.adventure-card:first-child{grid-column:span 2;aspect-ratio:16/9;grid-row:auto}.essentials{grid-template-columns:1fr;gap:3rem}}
@media(max-width:560px){.cards-grid{grid-template-columns:1fr}.adventure-card:first-child{grid-column:auto;aspect-ratio:3/4}.timeline::before{left:2.8rem}.timeline-item{grid-template-columns:5.5rem 1fr;gap:1.2rem}}
</style>
</head>
<body>

<div style="position:fixed;top:1.2rem;left:1.5rem;z-index:9998;font-family:'Barlow Condensed',sans-serif;font-size:.7rem;letter-spacing:.2em;text-transform:uppercase;color:rgba(244,240,235,.5);">Made by <span style="color:#d4a84b;">Saayaansh Arun</span></div>

<section class="hero">
  <div class="hero-bg"></div>
  <div class="snow-layer">
    <div class="flake"></div><div class="flake"></div><div class="flake"></div>
    <div class="flake"></div><div class="flake"></div><div class="flake"></div>
    <div class="flake"></div><div class="flake"></div><div class="flake"></div>
    <div class="flake"></div>
  </div>
  <div class="mountains">
    <svg viewBox="0 0 1440 500" preserveAspectRatio="xMidYMax slice" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <linearGradient id="mg" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%" stop-color="#7aa89a" stop-opacity="0.3"/>
          <stop offset="100%" stop-color="#0e1a12" stop-opacity="0"/>
        </linearGradient>
      </defs>
      <polygon points="0,500 0,300 80,240 160,290 240,210 320,260 400,180 480,240 560,170 640,220 720,150 800,210 880,160 960,230 1040,175 1120,250 1200,190 1280,240 1360,200 1440,260 1440,500" fill="#0f2018" opacity="0.9"/>
      <polygon points="400,180 422,202 378,202" fill="#c8d8d0" opacity="0.5"/>
      <polygon points="720,150 748,180 692,180" fill="#c8d8d0" opacity="0.6"/>
      <polygon points="880,160 905,187 855,187" fill="#c8d8d0" opacity="0.5"/>
      <polygon points="0,500 0,380 100,340 200,370 320,310 440,360 580,290 700,350 820,300 940,355 1060,305 1180,360 1300,320 1440,370 1440,500" fill="#1a2e1a" opacity="0.95"/>
      <polygon points="0,500 0,430 150,400 300,420 500,390 650,420 800,400 950,430 1100,405 1300,425 1440,410 1440,500" fill="#0e1f12"/>
      <rect x="0" y="440" width="1440" height="60" fill="url(#mg)" opacity="0.4"/>
    </svg>
  </div>
  <div class="elevation-badge">
    <div class="num">7,200</div>
    <div class="label">Feet Above Sea Level</div>
  </div>
  <div class="hero-content">
    <p class="hero-tag">Dream Vacation · Himachal Pradesh, India</p>
    <h1 class="hero-title">Into the<br/><em>Wild</em><br/>Shimla</h1>
    <p class="hero-subtitle">Where colonial ridges meet ancient pines, and every trail leads to a horizon untouched by time.</p>
    <a href="#" class="hero-cta" onclick="document.getElementById('break-screen').style.display='flex';return false;"><span>Plan the Expedition</span></a>
  </div>
</section>

<div class="strip">
  <div class="strip-inner">
    <span>Jakhu Peak Trek</span><span>Himalayan Views</span><span>Kufri Adventure</span>
    <span>Mall Road Wanders</span><span>Green Valley Trails</span><span>Heritage Railway</span>
    <span>Snow Season</span><span>Pine Forest Camps</span>
    <span>Jakhu Peak Trek</span><span>Himalayan Views</span><span>Kufri Adventure</span>
    <span>Mall Road Wanders</span><span>Green Valley Trails</span><span>Heritage Railway</span>
    <span>Snow Season</span><span>Pine Forest Camps</span>
  </div>
</div>

<section class="about reveal">
  <div>
    <div class="about-card">
      <svg class="compass" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="60" cy="60" r="58" stroke="rgba(122,168,154,0.3)" stroke-width="1"/>
        <circle cx="60" cy="60" r="48" stroke="rgba(212,168,75,0.15)" stroke-width="1" stroke-dasharray="4 4"/>
        <circle cx="60" cy="60" r="4" fill="#d4a84b"/>
        <polygon points="60,10 63,58 60,55 57,58" fill="#d4a84b"/>
        <polygon points="60,110 57,62 60,65 63,62" fill="rgba(200,216,208,0.4)"/>
        <polygon points="10,60 58,57 55,60 58,63" fill="rgba(200,216,208,0.4)"/>
        <polygon points="110,60 62,63 65,60 62,57" fill="rgba(200,216,208,0.4)"/>
        <text x="60" y="7" text-anchor="middle" fill="#d4a84b" font-family="Barlow Condensed" font-size="7" letter-spacing="2">N</text>
        <text x="60" y="116" text-anchor="middle" fill="rgba(200,216,208,0.5)" font-family="Barlow Condensed" font-size="7">S</text>
        <text x="5" y="63" text-anchor="middle" fill="rgba(200,216,208,0.5)" font-family="Barlow Condensed" font-size="7">W</text>
        <text x="115" y="63" text-anchor="middle" fill="rgba(200,216,208,0.5)" font-family="Barlow Condensed" font-size="7">E</text>
      </svg>
      <div class="stats-grid">
        <div class="stat"><div class="stat-num">8+</div><div class="stat-label">Trek Routes</div></div>
        <div class="stat"><div class="stat-num">25°C</div><div class="stat-label">Avg Summer High</div></div>
        <div class="stat"><div class="stat-num">1864</div><div class="stat-label">Founded as Capital</div></div>
        <div class="stat"><div class="stat-num">96km</div><div class="stat-label">Toy Train Ride</div></div>
      </div>
    </div>
  </div>
  <div class="about-text">
    <p class="section-tag">The Destination</p>
    <h2 class="section-heading">Queen of <em>the Hills</em></h2>
    <br/>
    <p>Shimla sits at the crown of Himachal Pradesh, draped in thick forests of rhododendron and deodar cedar. Once the summer capital of British India, this ridge-top city hides its wildest secrets in the trails that plunge into mist-filled valleys.</p>
    <p>The adventure here isn't just vertical — it's temporal. You walk between Victorian spires and ancient Hanuman temples, between snowfields in January and wildflower meadows in June. No two days share the same altitude, the same light, or the same story.</p>
    <p>This is not a beach you return to every year. This is a mountain you spend a lifetime learning.</p>
  </div>
</section>

<section class="adventures" id="adventures">
  <div class="adventures-header reveal">
    <div>
      <p class="section-tag">What Awaits You</p>
      <h2 class="section-heading">Choose Your<br/><em>Adventure</em></h2>
    </div>
    <p style="max-width:300px;color:rgba(244,240,235,.55);font-size:.88rem;line-height:1.7;">Every ridge has a trail. Every trail has a story. Pick the one that scares you just enough.</p>
  </div>
  <div class="cards-grid reveal">
    <div class="adventure-card">
      <div class="card-bg card-bg-1"></div>
      <div class="card-icon">🏔</div>
      <div class="card-info">
        <div class="card-difficulty">Hard · 6–7 hrs</div>
        <div class="card-name">Jakhu Peak Summit</div>
        <div class="card-desc">The highest point in Shimla at 8,048 ft. Ancient Hanuman temple at the summit. Panoramic Himalayan views reward the breathless climb.</div>
      </div>
    </div>
    <div class="adventure-card">
      <div class="card-bg card-bg-2"></div>
      <div class="card-icon">🎿</div>
      <div class="card-info">
        <div class="card-difficulty">Moderate · All Day</div>
        <div class="card-name">Kufri Snow Trails</div>
        <div class="card-desc">14 km from Shimla. Skiing and snowboarding in winter. Trekking through Himalayan National Park in summer.</div>
      </div>
    </div>
    <div class="adventure-card">
      <div class="card-bg card-bg-3"></div>
      <div class="card-icon">🚂</div>
      <div class="card-info">
        <div class="card-difficulty">Easy · 5–6 hrs</div>
        <div class="card-name">Kalka–Shimla Railway</div>
        <div class="card-desc">UNESCO Heritage toy train through 102 tunnels. Arguably the most scenic rail journey in Asia. Book the Vista Dome for full views.</div>
      </div>
    </div>
    <div class="adventure-card">
      <div class="card-bg card-bg-4"></div>
      <div class="card-icon">🌲</div>
      <div class="card-info">
        <div class="card-difficulty">Easy · Half Day</div>
        <div class="card-name">Green Valley Walk</div>
        <div class="card-desc">Dense cedar forests with a hidden waterfall. Best at dawn when mist hangs between the trees like silk curtains.</div>
      </div>
    </div>
  </div>
</section>

<section class="itinerary">
  <div class="reveal">
    <p class="section-tag">The Journey</p>
    <h2 class="section-heading">7-Day <em>Expedition</em></h2>
  </div>
  <div class="timeline reveal">
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">01</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Arrival &amp; Mall Road Reconnoitre</h3>
        <p>Touch down in Shimla via the Kalka–Shimla toy train. Check into your heritage hotel on the Ridge. Walk Mall Road at dusk as the Himalayas turn amber behind the Christ Church spire.</p>
        <div class="day-tags"><span class="day-tag">Scenic Train</span><span class="day-tag">Mall Road</span><span class="day-tag">Colonial Architecture</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">02</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Jakhu Peak Assault</h3>
        <p>Early morning climb to the Jakhu summit through rhododendron forest. At the top — 360° views of the Himalayan ranges. Beware the resident langurs; they will steal your snacks.</p>
        <div class="day-tags"><span class="day-tag">Trekking</span><span class="day-tag">Sunrise Views</span><span class="day-tag">Temple Visit</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">03</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Kufri &amp; High-Altitude Meadows</h3>
        <p>Drive to Kufri for skiing or pony trekking depending on the season. Explore Himalayan Nature Park — home to snow leopards, pheasants, and red pandas.</p>
        <div class="day-tags"><span class="day-tag">Skiing / Trekking</span><span class="day-tag">Wildlife</span><span class="day-tag">Mountain Cuisine</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">04</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Chail Palace &amp; World's Highest Cricket Ground</h3>
        <p>Visit the highest cricket ground on Earth at 2,444m. Explore the Chail Wildlife Sanctuary and spend the night in the palace — once a Maharaja's private retreat.</p>
        <div class="day-tags"><span class="day-tag">Heritage</span><span class="day-tag">Wildlife Sanctuary</span><span class="day-tag">Palace Stay</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">05</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Narkanda Ski Slopes</h3>
        <p>65 km drive to Narkanda at 9,100 ft. Skiing on pristine slopes in winter. In summer, witness apple orchards heavy with fruit against a Himalayan backdrop.</p>
        <div class="day-tags"><span class="day-tag">High Altitude</span><span class="day-tag">Adventure Sports</span><span class="day-tag">Apple Orchards</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">06</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Glen Forest &amp; Annandale</h3>
        <p>A slow wandering day through Shimla's forested gorge. Perfect for birdwatching and picnics beneath ancient deodars. Cricket at Annandale in the afternoon.</p>
        <div class="day-tags"><span class="day-tag">Forest Walk</span><span class="day-tag">Birdwatching</span><span class="day-tag">Leisure</span></div>
      </div>
    </div>
    <div class="timeline-item">
      <div class="day-label"><div class="day-num">07</div><div class="day-text">Day</div></div>
      <div class="day-content">
        <h3>Sunrise, Farewell &amp; Descent</h3>
        <p>Final sunrise from Jakhu or Prospect Hill. One last chai on the Ridge. The toy train takes you back through 102 tunnels — each one a goodbye to the mountains.</p>
        <div class="day-tags"><span class="day-tag">Sunrise</span><span class="day-tag">Toy Train</span><span class="day-tag">Departure</span></div>
      </div>
    </div>
  </div>
</section>

<section class="essentials reveal">
  <div>
    <p class="section-tag">Pack Smart</p>
    <h2 class="section-heading">What to<br/><em>Bring</em></h2>
    <ul class="pack-list">
      <li data-icon="🥾">Sturdy ankle-support trekking boots</li>
      <li data-icon="🧥">Thermal layers + waterproof outer shell</li>
      <li data-icon="🎒">30–40L daypack with rain cover</li>
      <li data-icon="🔦">Headlamp with spare batteries</li>
      <li data-icon="💊">Altitude sickness medication (Diamox)</li>
      <li data-icon="🧴">High SPF sunscreen — UV is fierce at altitude</li>
      <li data-icon="📷">Camera with extra memory cards</li>
      <li data-icon="💧">Insulated water bottle (1.5L minimum)</li>
    </ul>
  </div>
  <div>
    <p class="section-tag">Plan Around Nature</p>
    <h2 class="section-heading">Best Time<br/>to <em>Go</em></h2>
    <div class="best-time-grid">
      <div class="month-card"><div class="month-name">Dec–Feb</div><div class="month-icon">❄️</div></div>
      <div class="month-card peak"><div class="month-name">Mar–Apr</div><div class="month-icon">🌸</div></div>
      <div class="month-card peak"><div class="month-name">May–Jun</div><div class="month-icon">☀️</div></div>
      <div class="month-card"><div class="month-name">Jul–Aug</div><div class="month-icon">🌧️</div></div>
      <div class="month-card peak"><div class="month-name">Sep–Oct</div><div class="month-icon">🍂</div></div>
      <div class="month-card"><div class="month-name">Nov</div><div class="month-icon">🌫️</div></div>
    </div>
    <p style="margin-top:1.5rem;font-size:.8rem;color:rgba(244,240,235,.45);line-height:1.7;"><span style="color:var(--gold)">✦ Highlighted</span> months offer clear skies and comfortable trails. March–June for blooms; September–October for crisp golden light.</p>
  </div>
</section>

<div class="quote-section reveal">
  <p class="quote-text">The mountains are calling and I must go — but Shimla makes sure you never quite want to leave.</p>
  <p class="quote-attr">✦ &nbsp; Your Dream Vacation Awaits &nbsp; ✦</p>
</div>

<footer>
  <div>Shimla Adventure Guide &nbsp;·&nbsp; Himachal Pradesh, India</div>
  <div><span>7,200 ft</span> above the ordinary</div>
</footer>

<div id="break-screen" style="display:none;position:fixed;inset:0;background:var(--ink);z-index:9999;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:2rem;">
  <div style="font-size:5rem;margin-bottom:1.5rem;animation:bob 2s ease-in-out infinite">🙏</div>
  <h2 style="font-family:'Playfair Display',serif;font-size:clamp(1.8rem,5vw,3.5rem);font-weight:900;color:var(--snow);margin-bottom:1rem;">Give the Developer<br/><em style="color:var(--frost)">a Break</em></h2>
  <p style="color:var(--mist);font-size:1rem;max-width:380px;line-height:1.7;margin-bottom:2.5rem;">This feature is still being built. The developer is probably trekking Jakhu Peak right now. Please check back later. 🏔</p>
  <a href="#" onclick="document.getElementById('break-screen').style.display='none';return false;" style="font-family:'Barlow Condensed',sans-serif;font-size:.85rem;font-weight:600;letter-spacing:.2em;text-transform:uppercase;color:var(--ink);background:var(--gold);padding:1rem 2.4rem;text-decoration:none;transition:background .3s;" onmouseover="this.style.background='#b5451b';this.style.color='#f4f0eb'" onmouseout="this.style.background='#d4a84b';this.style.color='var(--ink)'">← Go Back</a>
</div>
<style>@keyframes bob{0%,100%{transform:translateY(0)}50%{transform:translateY(-14px)}}</style>
<script>
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible') });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
</script>
</body>
</html>
