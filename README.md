Um Abschnitte zu lesen Doppelt Auf Feil drücken
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Staten Island — Ultimate Digital Poster</title>
<meta name="description" content="Interactive poster about Staten Island with attractions, facts, translations, map, dark/light mode, and audio support." />
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
header { display:flex; align-items:center; gap:18px; margin:18px 0 26px 0; flex-wrap: wrap; }
header .emoji { font-size:50px; filter: drop-shadow(0 5px 12px rgba(34,211,248,.35)); }
h1 { font-size: clamp(28px, 6vw, 56px); margin:0; line-height:1.05; }
.subtitle { color: var(--muted); margin-top:8px; font-size:clamp(14px,2.2vw,18px); }

nav { margin-left:auto; display:flex; gap:12px; flex-wrap: wrap; }
nav a { color: var(--accent); font-weight:600; text-decoration:none; }
nav a:hover { text-decoration: underline; }

.hero-img { width:100%; max-height:450px; object-fit:cover; border-radius:20px; margin-bottom:24px; border:2px solid var(--accent); box-shadow: var(--shadow); }

.controls { display:flex; gap:12px; flex-wrap:wrap; margin-bottom:20px; }
input.search { padding:8px 12px; border-radius:12px; border:1px solid var(--muted); flex:1; }
button.global-toggle { background: var(--accent); border:none; border-radius:12px; padding:8px 14px; cursor:pointer; font-weight:600; }

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

.translation { display:none; margin-top:4px; font-size:14px; color: var(--accent-2); display:flex; align-items:center; gap:8px; }
.speak-btn { cursor:pointer; font-size:16px; background: var(--accent); color:#000; border:none; border-radius:50%; width:26px; height:26px; display:flex; align-items:center; justify-content:center; box-shadow: var(--shadow); transition: transform .2s; }
.speak-btn:hover { transform: scale(1.15); }

.gallery { display:grid; grid-template-columns: repeat(auto-fit,minmax(240px,1fr)); gap:16px; margin-top:12px; }
.gallery img { width:100%; height:200px; object-fit:cover; border-radius:14px; border:1px solid rgba(148,163,184,.25); transition: transform .3s, box-shadow .3s; }
.gallery img:hover { transform: scale(1.05); box-shadow: 0 8px 20px rgba(56,189,248,.4); }

.toggle-dark { position:fixed; top:16px; right:16px; background: var(--accent); color:#000; padding:10px 16px; border-radius:999px; cursor:pointer; font-weight:600; box-shadow: var(--shadow); }

footer {
  text-align:center; margin-top:40px; font-size:18px; font-weight:800;
  color: var(--neon); text-shadow: 0 0 8px var(--neon), 0 0 12px var(--neon);
}

.arrow { display:inline-block; transition: transform .25s ease; }

/* Slide animation */
.collapsible { max-height:0; overflow:hidden; transition:max-height .5s ease, padding .3s; }
.collapsible.open { max-height:2000px; padding-top:8px; }

/* Responsive */
@media(max-width:900px){
  .attractions, .facts, .population, .map, .pictures{ grid-column: span 12; }
  nav { justify-content: center; }
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
    <nav>
      <a href="#attractions">Attractions</a>
      <a href="#facts">Facts</a>
      <a href="#population">Population</a>
      <a href="#map">Map</a>
      <a href="#pictures">Pictures</a>
    </nav>
  </header>

  <!-- Controls -->
  <div class="controls">
    <input type="text" class="search" id="search" placeholder="Search attractions & facts...">
    <button class="global-toggle" id="toggleAllTranslations">Deutsch anzeigen</button>
  </div>

  <!-- Hero Image -->
  <img src="IMG_2296.jpeg" alt="Staten Island Hero" class="hero-img">

  <div class="grid">
    <section class="card attractions" id="attractions">
      <h2>Top Attractions <span class="arrow">▼</span></h2>
      <ul class="list collapsible">
        <li>Staten Island Ferry offers a free ride across New York Harbor. 
          <div class="translation">→ Die Staten Island Fähre bietet eine kostenlose Fahrt über den New Yorker Hafen. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </li>
        <li>Snug Harbor Cultural Center & Botanical Garden showcase historic buildings and gardens. 
          <div class="translation">→ Snug Harbor Cultural Center & Botanischer Garten zeigen historische Gebäude und Gärten. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </li>
        <li>Historic Richmond Town presents colonial life with museums and live demonstrations. 
          <div class="translation">→ Historic Richmond Town zeigt das koloniale Leben mit Museen und Vorführungen. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </li>
      </ul>
    </section>

    <section class="card facts" id="facts">
      <h2>Fast Facts <span class="arrow">▼</span></h2>
      <ul class="list collapsible">
        <li>Nickname: “The Borough of Parks”.
          <div class="translation">→ Spitzname: „The Borough of Parks“. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </li>
        <li>Todt Hill is the highest natural point in NYC (~125 m).
          <div class="translation">→ Todt Hill ist der höchste natürliche Punkt in NYC (~125 m). 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </li>
      </ul>
    </section>

    <section class="card population" id="population">
      <h2>Population <span class="arrow">▼</span></h2>
      <div class="collapsible">
        <p>Approx. 495,747 (2020 Census), the least populous NYC borough. 
          <div class="translation">→ Ca. 495.747 (Volkszählung 2020), der am wenigsten bevölkerte Bezirk NYCs. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </p>
      </div>
    </section>

    <section class="card map" id="map">
      <h2>Where is it? <span class="arrow">▼</span></h2>
      <div class="collapsible">
        <p>Southwest of Manhattan, north of New Jersey, connected by bridges. 
          <div class="translation">→ Südwestlich von Manhattan, nördlich von New Jersey, verbunden durch Brücken. 
            <button class="speak-btn" aria-label="Vorlesen auf Deutsch">🔊</button>
          </div>
        </p>
        <iframe width="100%" height="300" style="border:0" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14"></iframe>
      </div>
    </section>

    <section class="card pictures" id="pictures">
      <h2>Pictures <span class="arrow">▼</span></h2>
      <div class="gallery collapsible">
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
// Dark/Light Mode
document.getElementById('darkToggle').addEventListener('click', ()=>{
  document.body.classList.toggle('light-mode');
});

// Collapsible Sections mit Slide-Animation
document.querySelectorAll('.card h2').forEach(h2=>{
  const content = h2.nextElementSibling;
  content.classList.add('collapsible');
  h2.addEventListener('click',()=>{
    content.classList.toggle('open');
    h2.querySelector('.arrow').style.transform = content.classList.contains('open') ? 'rotate(180deg)' : 'rotate(0deg)';
  });
});

// Vorlese-Funktion
function speak(text){
  const utterance = new SpeechSynthesisUtterance(text);
  utterance.lang = 'de-DE';
  speechSynthesis.cancel();
  speechSynthesis.speak(utterance);
}
document.querySelectorAll('.speak-btn').forEach(btn=>{
  btn.addEventListener('click',(e)=>{
    e.stopPropagation();
    const text = btn.parentElement.textContent.replace("→","").replace("🔊","").trim();
    speak(text);
  });
});

// Globaler Toggle Deutsch
document.getElementById('toggleAllTranslations').addEventListener('click',()=>{
  const btn = document.getElementById('toggleAllTranslations');
  const showing = btn.dataset.showing === "true";
  document.querySelectorAll('.translation').forEach(t=>{
    t.style.display = showing ? 'none' : 'flex';
  });
  btn.textContent = showing ? "Deutsch anzeigen" : "Deutsch ausblenden";
  btn.dataset.showing = (!showing).toString();
});

// Suchfunktion
document.getElementById('search').addEventListener('input',(e)=>{
  const val = e.target.value.toLowerCase();
  document.querySelectorAll('.list li').forEach(li=>{
    const text = li.textContent.toLowerCase();
    li.style.display = text.includes(val) ? 'block' : 'none';
  });
});
</script>
</body>
</html>
