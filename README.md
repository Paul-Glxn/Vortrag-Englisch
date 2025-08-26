<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Staten Island — Digital Poster</title>
  <meta name="description" content="A one-page poster about Staten Island with attractions, fast facts, population, and map. Includes German translation drawer." />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0f172a;
      --card: #111827;
      --muted: #94a3b8;
      --text: #e5e7eb;
      --accent: #38bdf8;
      --accent-2: #22d3ee;
      --ring: rgba(56,189,248,.35);
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      background: radial-gradient(1200px 600px at 10% 0%, rgba(34,211,238,.12), transparent 60%),
                  radial-gradient(1200px 600px at 90% -10%, rgba(56,189,248,.10), transparent 60%),
                  var(--bg);
      color: var(--text);
    }
    .wrap{max-width:1100px;margin:0 auto;padding:28px}
    header{
      display:flex;align-items:center;gap:18px;margin:18px 0 26px 0
    }
    header .emoji{font-size:40px;filter: drop-shadow(0 5px 12px rgba(34,211,238,.25));}
    h1{font-size: clamp(28px, 6vw, 56px); line-height:1.05; margin:0}
    .subtitle{color:var(--muted);margin-top:8px;font-size:clamp(14px,2.2vw,18px)}

    .grid{display:grid;gap:18px;grid-template-columns: repeat(12, 1fr)}
    .card{
      grid-column: span 12;
      background: linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.02));
      border:1px solid rgba(148,163,184,.15);
      border-radius: var(--radius);
      padding: 20px 20px 18px;
      box-shadow: var(--shadow);
      position:relative;
      overflow:hidden;
    }
    .card h2{margin:0 0 10px 0;font-size: clamp(18px, 3.2vw, 28px)}
    .card p{margin:0;color:#d1d5db}
    .list{display:grid; gap:10px; margin-top:6px}
    .list li{background:rgba(15,23,42,.45); border:1px solid rgba(148,163,184,.15); padding:12px 14px; border-radius:14px}

    .attractions{grid-column: span 7}
    .facts{grid-column: span 5}
    .population{grid-column: span 5}
    .map{grid-column: span 7}
    .pictures{grid-column: span 12}

    @media (max-width: 900px){
      .attractions,.facts,.population,.map,.pictures{grid-column: span 12}
    }

    .note{color: var(--muted); font-size:13px; margin-top:12px}

    .translate-toggle{
      position: fixed; bottom: 16px; left: 50%; transform: translateX(-50%);
      background: linear-gradient(180deg, rgba(34,211,238,.12), rgba(56,189,248,.10));
      border:1px solid rgba(56,189,248,.35);
      padding: 10px 14px; border-radius: 999px; cursor: pointer; color:#e0f2fe;
      display:flex; align-items:center; gap:10px; box-shadow: var(--shadow);
      backdrop-filter: blur(6px);
    }
    .translate-toggle span{font-weight:600}
    .translate-toggle .arrow{display:inline-block; transition: transform .25s ease}
    .drawer{
      position: fixed; left:0; right:0; bottom:0; background: rgba(2,6,23,.92);
      border-top: 1px solid rgba(148,163,184,.2);
      transform: translateY(100%);
      transition: transform .35s ease; box-shadow: var(--shadow);
      max-height: 70vh; /* Scrollbar fix */
      overflow-y: auto;
    }
    .drawer.open{transform: translateY(0)}
    .drawer .inner{max-width:1100px;margin:0 auto;padding:18px 28px}
    .drawer h3{margin:0 0 8px 0}
    .drawer p,.drawer li{color:#d1d5db}

    .ring{
      position:absolute; inset: -60px auto auto -60px; width:180px; height:180px; border-radius:999px;
      background: radial-gradient(closest-side, rgba(34,211,238,.18), transparent 70%);
      pointer-events:none; filter: blur(1px);
    }
    .gallery{
      display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px;margin-top:12px
    }
    .gallery img{width:100%;height:200px;object-fit:cover;border-radius:14px;border:1px solid rgba(148,163,184,.25)}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="emoji">🗽</div>
      <div>
        <h1>Staten Island</h1>
        <div class="subtitle">One of New York City's five boroughs — parks, history, and harbor views.</div>
      </div>
    </header>

    <div class="grid">
      <section class="card attractions">
        <div class="ring"></div>
        <h2>Top Attractions</h2>
        <ul class="list">
          <li><strong>Staten Island Ferry</strong> — Free ride with skyline and Statue of Liberty views.</li>
          <li><strong>Snug Harbor Cultural Center & Botanical Garden</strong> — Historic campus, gardens, and museums.</li>
          <li><strong>Historic Richmond Town</strong> — Living history village showcasing colonial life.</li>
          <li><strong>Fort Wadsworth & Verrazzano-Narrows Bridge</strong> — Civil War-era fort beneath an iconic span.</li>
        </ul>
      </section>

      <section class="card facts">
        <div class="ring"></div>
        <h2>Fast Facts</h2>
        <ul class="list">
          <li><strong>Nickname:</strong> “The Borough of Parks.”</li>
          <li><strong>Highest point in NYC:</strong> Todt Hill (~410 ft / ~125 m).</li>
          <li><strong>Iconic crossing:</strong> Verrazzano-Narrows Bridge links Staten Island to Brooklyn.</li>
        </ul>
      </section>

      <section class="card population">
        <div class="ring"></div>
        <h2>Population</h2>
        <p>Approx. <strong>495,747</strong> (2020 U.S. Census). Staten Island is the least populous of NYC’s five boroughs, yet one of the greenest by area.</p>
      </section>

      <section class="card map">
        <div class="ring"></div>
        <h2>Where is it?</h2>
        <p>Southwest of Manhattan, across New York Harbor; north of New Jersey. Connected by the Verrazzano-Narrows Bridge (to Brooklyn) and several bridges to New Jersey.</p>
        <iframe width="100%" height="300" style="border:0" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14"></iframe>
      </section>

      <section class="card pictures">
        <div class="ring"></div>
        <h2>Pictures</h2>
        <div class="gallery">
          <img src="https://upload.wikimedia.org/wikipedia/commons/1/1e/Staten_Island_Ferry_St._George.jpg" alt="Staten Island Ferry">
          <img src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Verrazzano-Narrows_Bridge_2.jpg" alt="Verrazzano-Narrows Bridge">
          <img src="https://upload.wikimedia.org/wikipedia/commons/2/27/Snug_Harbor_Cultural_Center.jpg" alt="Snug Harbor Cultural Center">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Historic_Richmond_Town.jpg" alt="Historic Richmond Town">
        </div>
      </section>
    </div>
  </div>

  <button class="translate-toggle" id="toggle">
    <span>Deutsch</span>
    <svg class="arrow" width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M6 9l6 6 6-6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
  </button>

  <aside class="drawer" id="drawer">
    <div class="inner">
      <h3>Staten Island — Zusammenfassung (Deutsch)</h3>
      <p><strong>Lage:</strong> Südwestlich von Manhattan am New Yorker Hafen; nördlich von New Jersey.</p>
      <h4>Sehenswürdigkeiten</h4>
      <ul>
        <li><strong>Staten Island Ferry</strong> — Kostenfreie Fahrt mit Blick auf Skyline und Freiheitsstatue.</li>
        <li><strong>Snug Harbor & Botanischer Garten</strong> — Historisches Gelände mit Gärten und Museen.</li>
        <li><strong>Historic Richmond Town</strong> — Freilichtmuseum zum kolonialen Leben.</li>
        <li><strong>Fort Wadsworth & Verrazzano-Narrows Bridge</strong> — Festung aus dem 19. Jh.</li>
      </ul>
      <h4>Bewundernswerte Fakten</h4>
      <ul>
        <li><strong>Spitzname:</strong> „The Borough of Parks“.</li>
        <li><strong>Höchster Punkt:</strong> Todt Hill (~125 m).</li>
        <li><strong>Verbindung:</strong> Verrazzano-Narrows Bridge nach Brooklyn.</li>
      </ul>
      <h4>Bevölkerung</h4>
      <p>Ungefähr <strong>495.747</strong> (Volkszählung 2020).</p>
    </div>
  </aside>

  <script>
    const toggle = document.getElementById('toggle');
    const drawer = document.getElementById('drawer');
    const arrow = toggle.querySelector('.arrow');
    toggle.addEventListener('click', ()=>{
      const open = drawer.classList.toggle('open');
      arrow.style.transform = open ? 'rotate(180deg)' : 'rotate(0deg)';
    });
  </script>
</body>
</html>
