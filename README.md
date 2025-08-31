<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Staten Island — Immersive Digital Poster</title>

<!-- Neue Schriftarten -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;800&family=Nunito:wght@300;400;600;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #0f172a;
  --card: #111827;
  --text: #e5e7eb;
  --muted: #94a3b8;
  --accent: #38bdf8;
  --accent-2: #22d3ee;
  --gradient: linear-gradient(135deg, #22d3ee, #38bdf8, #0ea5e9);
  --shadow: 0 15px 40px rgba(0,0,0,.35);
  --radius: 22px;
  --glass: rgba(255,255,255,0.05);
  --neon: #0ff;
}
body.light-mode {
  --bg: #f1f5f9;
  --card: #ffffff;
  --text: #0f172a;
  --muted: #475569;
  --accent: #0ea5e9;
  --accent-2: #06b6d4;
  --gradient: linear-gradient(135deg, #0ea5e9, #06b6d4, #38bdf8);
  --shadow: 0 15px 40px rgba(0,0,0,.15);
  --glass: rgba(255,255,255,0.7);
}
*{box-sizing:border-box;scroll-behavior:smooth;}
body {
  margin:0; 
  font-family: 'Nunito', system-ui, sans-serif;
  background: var(--bg);
  color: var(--text);
  transition: background .6s, color .6s;
}
.wrap { max-width:1200px; margin:0 auto; padding:32px; }
header { display:flex; align-items:center; gap:20px; margin:20px 0 30px 0; }
header .emoji { font-size:56px; animation: float 3s ease-in-out infinite; }
@keyframes float { 0%,100%{transform:translateY(0);} 50%{transform:translateY(-8px);} }
h1 { font-size: clamp(34px, 6vw, 68px); margin:0; line-height:1.05; font-family: "Playfair Display", serif; background: var(--gradient); -webkit-background-clip:text; color:transparent; }
.subtitle { color: var(--muted); margin-top:8px; font-size:clamp(14px,2vw,20px); font-family:'Nunito', sans-serif; }

.hero-img { width:100%; max-height:480px; object-fit:cover; border-radius:24px; margin-bottom:28px; border:3px solid var(--accent); box-shadow: var(--shadow); transition: transform .5s; }
.hero-img:hover { transform: scale(1.03); }

.grid { display:grid; gap:20px; grid-template-columns: repeat(12,1fr); }
.card {
  grid-column: span 12;
  background: var(--glass);
  border:1px solid rgba(148,163,184,.2);
  border-radius: var(--radius);
  padding: 22px; 
  box-shadow: var(--shadow);
  backdrop-filter: blur(12px);
  transition: transform .3s, box-shadow .3s, background .3s;
  position:relative;
}
.card:hover { 
  transform: translateY(-6px); 
  box-shadow: 0 25px 50px rgba(0,0,0,.45);
  border:1px solid var(--accent);
}
.card h2 { 
  margin:0 0 14px 0; 
  font-size: clamp(20px, 3vw, 30px); 
  font-family: "Playfair Display", serif;
  cursor:pointer; 
  display:flex; justify-content:space-between; align-items:center; 
  transition: color .3s, text-shadow .3s;
}
.card h2:hover { color: var(--accent); text-shadow: 0 0 12px var(--accent); }
.card p, .card li { margin:0; color:var(--text); font-family:'Nunito', sans-serif; }
.list { margin-top:6px; padding:0; list-style:none; }
.list li { background: rgba(15,23,42,.45); border:1px solid rgba(148,163,184,.15); padding:14px 16px; border-radius:16px; margin-bottom:10px; cursor:pointer; transition: all .3s; font-family:'Nunito', sans-serif; }
.list li:hover { background: rgba(15,23,42,.65); transform: translateX(6px); }

.translation { display:none; margin-top:6px; font-size:14px; color: var(--accent-2); font-family:'Nunito', sans-serif; }

.gallery { display:grid; grid-template-columns: repeat(auto-fit,minmax(260px,1fr)); gap:18px; margin-top:14px; }
.gallery img { width:100%; height:220px; object-fit:cover; border-radius:16px; border:2px solid rgba(148,163,184,.25); transition: transform .4s, box-shadow .4s; }
.gallery img:hover { transform: scale(1.08); box-shadow: 0 10px 28px rgba(56,189,248,.5); }

.toggle-dark { position:fixed; top:20px; right:20px; background: var(--gradient); color:#fff; padding:12px 18px; border:none; border-radius:999px; cursor:pointer; font-weight:700; box-shadow: var(--shadow); transition: transform .3s; z-index:1000; font-family:'Nunito', sans-serif; }
.toggle-dark:hover { transform: scale(1.05); }

footer {
  text-align:center; margin:60px 0 30px; font-size:20px; font-weight:800;
  color: var(--neon); text-shadow: 0 0 10px var(--neon), 0 0 14px var(--neon);
  animation: flicker 2.5s infinite alternate;
  font-family: "Playfair Display", serif;
}
@keyframes flicker { 0%{opacity:.8;} 100%{opacity:1;} }

.arrow { display:inline-block; transition: transform .25s ease; }

.map iframe { border-radius: 16px; border: 3px solid var(--accent); }

.back-to-top {
  position:fixed; bottom:25px; right:25px; 
  background: var(--gradient); color:#fff; 
  padding:14px 18px; border-radius:50%; 
  cursor:pointer; font-size:20px; font-weight:800; 
  box-shadow: var(--shadow); display:none; 
  transition: transform .3s;
  font-family:'Nunito', sans-serif;
}
.back-to-top:hover { transform: scale(1.1); }

@media(max-width:900px){
  .attractions, .facts, .population, .map, .pictures, .movies { grid-column: span 12; }
}
</style>
</head>
<body>
<button class="toggle-dark" id="darkToggle">☀️ / 🌙</button>

<div class="wrap">
  <header>
    <div class="emoji">🗽</div>
    <div>
      <h1>Staten Island</h1>
      <div class="subtitle">The greenest borough of NYC — parks, history, and breathtaking harbor views.</div>
    </div>
  </header>

  <!-- Hero Image -->
  <img src="IMG_2296.jpeg" alt="Staten Island Hero" class="hero-img">

  <div class="grid">
    <section class="card attractions">
      <h2>Top Attractions <span class="arrow">▼</span></h2>
      <ul class="list">
        <li>Staten Island Ferry offers a free ride across New York Harbor. <span class="translation">→ Die Staten Island Fähre bietet eine kostenlose Fahrt über den New Yorker Hafen.</span></li>
        <li>Snug Harbor Cultural Center & Botanical Garden showcase historic buildings and gardens. <span class="translation">→ Snug Harbor Cultural Center & Botanischer Garten zeigen historische Gebäude und Gärten.</span></li>
        <li>Historic Richmond Town presents colonial life with museums and live demonstrations. <span class="translation">→ Historic Richmond Town zeigt das koloniale Leben mit Museen und Vorführungen.</span></li>
        <li>Fort Wadsworth sits beneath the iconic Verrazzano-Narrows Bridge. <span class="translation">→ Fort Wadsworth liegt unter der berühmten Verrazzano-Narrows-Brücke.</span></li>
        <li>Staten Island Greenbelt offers over 2000 acres of parks and hiking trails. <span class="translation">→ Staten Island Greenbelt bietet über 2000 Hektar Parkflächen und Wanderwege.</span></li>
        <li>Staten Island Zoo features exotic animals and a reptile house. <span class="translation">→ Staten Island Zoo hat exotische Tiere und ein eigenes Reptilienhaus.</span></li>
      </ul>
    </section>

    <section class="card facts">
      <h2>Fast Facts <span class="arrow">▼</span></h2>
      <ul class="list">
        <li>Nickname: “The Borough of Parks”. <span class="translation">→ Spitzname: „The Borough of Parks“.</span></li>
        <li>Todt Hill is the highest natural point in NYC (~125 m). <span class="translation">→ Todt Hill ist der höchste natürliche Punkt in NYC (~125 m).</span></li>
        <li>Verrazzano-Narrows Bridge connects Staten Island to Brooklyn. <span class="translation">→ Die Verrazzano-Narrows-Brücke verbindet Staten Island mit Brooklyn.</span></li>
        <li>Staten Island has 26 km of coastline. <span class="translation">→ Staten Island hat 26 km Küstenlinie.</span></li>
        <li>Staten Island is the greenest NYC borough with over 20% forest coverage. <span class="translation">→ Staten Island ist der grünste Bezirk NYCs mit über 20% Waldfläche.</span></li>
        <li>Snug Harbor was originally a home for retired sailors. <span class="translation">→ Snug Harbor war ursprünglich ein Heim für pensionierte Seeleute.</span></li>
      </ul>
    </section>

    <section class="card population">
      <h2>Population <span class="arrow">▼</span></h2>
      <p>Approx. 495,747 (2020 Census), the least populous NYC borough. <span class="translation">→ Ca. 495.747 (Volkszählung 2020), der am wenigsten bevölkerte Bezirk NYCs.</span></p>
    </section>

    <section class="card map">
      <h2>Where is it? <span class="arrow">▼</span></h2>
      <p>Southwest of Manhattan, north of New Jersey, connected by bridges. <span class="translation">→ Südwestlich von Manhattan, nördlich von New Jersey, verbunden durch Brücken.</span></p>
      <iframe width="100%" height="300" style="border:0" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14"></iframe>
    </section>

    <section class="card pictures">
      <h2>Pictures <span class="arrow">▼</span></h2>
      <div class="gallery">
        <img src="IMG_2294.jpeg" alt="Image 1">
        <img src="IMG_2292.jpeg" alt="Image 2">
        <img src="IMG_2293.jpeg" alt="Image 3">
        <img src="IMG_2295.jpeg" alt="Image 4">
      </div>
    </section>

    <section class="card movies">
      <h2>Staten Island in Film & TV <span class="arrow">▼</span></h2>
      <ul class="list">
        <li>*The Irishman* (2019, Martin Scorsese) – scenes filmed on Staten Island. 
          <span class="translation">→ *The Irishman* (2019, Martin Scorsese) – Szenen wurden auf Staten Island gedreht.</span>
        </li>
        <li>*War of the Worlds* (2005, with Tom Cruise) – includes Staten Island locations. 
          <span class="translation">→ *Krieg der Welten* (2005, mit Tom Cruise) – einige Szenen spielen auf Staten Island.</span>
        </li>
        <li>*Goodfellas* (1990) – classic mafia film shot partly on Staten Island. 
          <span class="translation">→ *Goodfellas* (1990) – Mafia-Klassiker, teilweise auf Staten Island gedreht.</span>
        </li>
        <li>*Working Girl* (1988, with Harrison Ford & Melanie Griffith). 
          <span class="translation">→ *Die Waffen der Frauen* (1988, mit Harrison Ford & Melanie Griffith).</span>
        </li>
        <li>*Staten Island Summer* (2015, Netflix comedy). 
          <span class="translation">→ *Staten Island Summer* (2015, Netflix-Komödie).</span>
        </li>
      </ul>
    </section>
  </div>
</div>

<footer>✨ Erstellt von Marlon Leuchtmann & Paul Weisenbilder (8d) ✨</footer>

<button class="back-to-top" id="backTop">↑</button>

<script>
// Translation toggle
document.querySelectorAll('.list li').forEach(li => {
  li.addEventListener('click', ()=> {
    const trans = li.querySelector('.translation');
    trans.style.display = trans.style.display === 'block' ? 'none' : 'block';
  });
});

// Dark Mode
document.getElementById('darkToggle').addEventListener('click', ()=>{
  document.body.classList.toggle('light-mode');
});

// Collapsible Cards
document.querySelectorAll('.card h2').forEach(h2 => {
  const content = h2.nextElementSibling;
  h2.addEventListener('click', () => {
    if(content.style.display === 'none' || content.style.display === ''){
      content.style.display = 'block';
      h2.querySelector('.arrow').style.transform = 'rotate(180deg)';
    } else {
      content.style.display = 'none';
      h2.querySelector('.arrow').style.transform = 'rotate(0deg)';
    }
  });
  if(content) content.style.display = 'none';
});

// Back to Top
const backTop = document.getElementById('backTop');
window.addEventListener('scroll', ()=>{
  if(window.scrollY > 300){
    backTop.style.display = 'block';
  } else {
    backTop.style.display = 'none';
  }
});
backTop.addEventListener('click', ()=>{
  window.scrollTo({top:0, behavior:'smooth'});
});
</script>
</body>
</html>
