Um Abschnitte zu lesen Doppelt Auf Feil drücken
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Staten Island — Ultimate Digital Poster um Abschnitte zu Öffnen Doppelt klicken</title>
<meta name="description" content="A high-end interactive poster about Staten Island with attractions, facts, population, map, inline translations, dark/light mode, and hover animations." />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0f172a;
  --card: #111827;
  --text: #e5e7eb;
  --muted: #94a3b8;
  --accent: #38bdf8;
  --accent-2: #22d3ee;
  --shadow: 0 10px 30px rgba(0,0,0,.35);
  --radius: 18px;
  --neon: #0ff;
}
body.light-mode {
  --bg: #e5e7eb;
  --card: #ffffff;
  --text: #111827;
  --muted: #6b7280;
  --accent: #0ea5e9;
  --accent-2: #06b6d4;
  --shadow: 0 10px 30px rgba(0,0,0,.15);
}
* { box-sizing: border-box; }
body {
  margin:0; font-family: Inter, system-ui, sans-serif;
  background: linear-gradient(120deg, rgba(34,211,238,.08), rgba(56,189,248,.08)),
              radial-gradient(circle at 10% 10%, rgba(56,189,248,.2), transparent 70%),
              var(--bg);
  color: var(--text);
  transition: background .5s, color .5s;
}
.wrap { max-width:1100px; margin:0 auto; padding:28px; }
header { display:flex; align-items:center; gap:18px; margin:18px 0 26px 0; }
header .emoji { font-size:50px; filter: drop-shadow(0 5px 12px rgba(34,211,248,.35)); }
h1 { font-size: clamp(28px, 6vw, 56px); margin:0; line-height:1.05; }
.subtitle { color: var(--muted); margin-top:8px; font-size:clamp(14px,2.2vw,18px); }

.hero-img { width:100%; max-height:450px; object-fit:cover; border-radius:20px; margin-bottom:24px; border:2px solid var(--accent); box-shadow: var(--shadow); }

.grid { display:grid; gap:18px; grid-template-columns: repeat(12,1fr); }
.card {
  grid-column: span 12;
  background: linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.02));
  border:1px solid rgba(148,163,184,.15);
  border-radius: var(--radius);
  padding: 20px; 
  box-shadow: var(--shadow);
  position:relative;
  overflow:hidden;
  transition: transform .3s, box-shadow .3s, background .3s;
}
.card:hover { 
  transform: translateY(-4px); 
  box-shadow: 0 20px 40px rgba(0,0,0,.4);
  background: linear-gradient(180deg, rgba(56,189,248,.05), rgba(56,189,248,.02));
}
.card h2 { margin:0 0 10px 0; font-size: clamp(18px, 3.2vw, 28px); cursor:pointer; display:flex; justify-content:space-between; align-items:center; transition: color .3s, text-shadow .3s; }
.card h2:hover { color: var(--accent); text-shadow: 0 0 8px var(--accent); }
.card p, .card li { margin:0; color:#d1d5db; }
.list { margin-top:6px; }
.list li { background: rgba(15,23,42,.45); border:1px solid rgba(148,163,184,.15); padding:12px 14px; border-radius:14px; margin-bottom:8px; cursor:pointer; transition: background .3s; }
.list li:hover { background: rgba(15,23,42,.6); }

.translation { display:none; margin-top:4px; font-size:14px; color: var(--accent-2); }

.gallery { display:grid; grid-template-columns: repeat(auto-fit,minmax(240px,1fr)); gap:16px; margin-top:12px; }
.gallery img { width:100%; height:200px; object-fit:cover; border-radius:14px; border:1px solid rgba(148,163,184,.25); transition: transform .3s, box-shadow .3s; }
.gallery img:hover { transform: scale(1.05); box-shadow: 0 8px 20px rgba(56,189,248,.4); }

.toggle-dark { position:fixed; top:16px; right:16px; background: var(--accent); color:#000; padding:10px 16px; border-radius:999px; cursor:pointer; font-weight:600; box-shadow: var(--shadow); }

footer {
  text-align:center; margin-top:40px; font-size:18px; font-weight:800;
  color: var(--neon); text-shadow: 0 0 8px var(--neon), 0 0 12px var(--neon);
}

.arrow { display:inline-block; transition: transform .25s ease; }

.map iframe { border-radius: 12px; border: 2px solid var(--accent); }

@media(max-width:900px){
  .attractions, .facts, .population, .map, .pictures{ grid-column: span 12; }
}
</style>
</head>
<body>
<button class="toggle-dark" id="darkToggle">Toggle Dark/Light</button>

<div class="wrap">
  <header>
    <div class="emoji">🗽</div>
    <div>
      <h1>Staten Island</h1>
      <div class="subtitle">One of New York City's five boroughs — parks, history, and harbor views.</div>
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
  </div>
</div>

<footer>Erstellt Von Marlon Leuchtmann, Paul Weisenbilder 8d</footer>

<script>
const toggle = document.querySelectorAll('.list li');
toggle.forEach(li => {
  li.addEventListener('click', ()=> {
    const trans = li.querySelector('.translation');
    trans.style.display = trans.style.display === 'block' ? 'none' : 'block';
  });
});

document.getElementById('darkToggle').addEventListener('click', ()=>{
  document.body.classList.toggle('light-mode');
});

// Collapsible Cards
const cards = document.querySelectorAll('.card h2');
cards.forEach(h2 => {
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
  if(h2.parentElement.querySelector('.list') || h2.parentElement.querySelector('p')){
    content.style.display = 'none';
  }
});
</script>
</body>
</html>
