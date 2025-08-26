<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Staten Island — Digital Poster (Final)</title>
  <meta name="description" content="Polished bilingual poster: English sentences with elegant German translations on click." />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0f172a;
      --muted: #94a3b8;
      --text: #f1f5f9;
      --accent: #38bdf8;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
      --translate-bg: rgba(34, 211, 238, 0.1);
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;background:radial-gradient(1200px 600px at 10% 0%, rgba(34,211,238,.12), transparent 60%), radial-gradient(1200px 600px at 90% -10%, rgba(56,189,248,.10), transparent 60%), var(--bg);color:var(--text)}
    .wrap{max-width:1000px;margin:0 auto;padding:28px}
    header{display:flex;align-items:center;gap:18px;margin:18px 0 26px 0}
    header .emoji{font-size:44px;filter: drop-shadow(0 5px 12px rgba(34,211,238,.25));}
    h1{font-size: clamp(32px, 6vw, 56px);line-height:1.05;margin:0}
    .subtitle{color:var(--muted);margin-top:8px;font-size:clamp(15px,2.2vw,19px)}

    .grid{display:grid;gap:20px;grid-template-columns: repeat(12, 1fr)}
    .card{grid-column: span 12;background: rgba(255,255,255,.03);border:1px solid rgba(148,163,184,.15);border-radius: var(--radius);padding:22px;box-shadow: var(--shadow)}
    .card h2{margin:0 0 12px 0;font-size: clamp(20px, 3vw, 28px)}

    .sentence{background:rgba(15,23,42,.55); border:1px solid rgba(148,163,184,.2); padding:14px; border-radius:14px; display:flex; flex-direction:column; gap:8px}
    .sentence-text{line-height:1.4}
    .translate-btn{align-self:flex-start;background:var(--accent);border:none;color:#0f172a;font-weight:600;padding:6px 12px;border-radius:999px;cursor:pointer;box-shadow:var(--shadow);font-size:14px;display:flex;align-items:center;gap:6px;transition:background .2s}
    .translate-btn:hover{background:#22d3ee}
    .translate-btn .arrow{transition:transform .25s ease}
    .translation{margin-top:6px;background:var(--translate-bg);padding:10px;border-radius:10px;border:1px solid rgba(148,163,184,.2);display:none;font-size:0.95rem;color:#e2e8f0}
    .translation.open{display:block}

    @media(max-width:900px){.grid{grid-template-columns:1fr}}
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
      <section class="card">
        <h2>Top Attractions</h2>
        <div class="sentence">
          <div class="sentence-text">The Staten Island Ferry offers a free ride with panoramic views of Manhattan and the Statue of Liberty.</div>
          <button class="translate-btn" data-translation="Die Staten Island Ferry bietet eine kostenlose Fahrt mit Panoramablick auf Manhattan und die Freiheitsstatue."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <div class="sentence">
          <div class="sentence-text">Snug Harbor Cultural Center & Botanical Garden is a historic campus with gardens, museums, and cultural programs.</div>
          <button class="translate-btn" data-translation="Das Snug Harbor Cultural Center & Botanische Garten ist ein historisches Gelände mit Gärten, Museen und Kulturprogrammen."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <div class="sentence">
          <div class="sentence-text">Historic Richmond Town is a living history village where colonial life is recreated through restored buildings and demonstrations.</div>
          <button class="translate-btn" data-translation="Historic Richmond Town ist ein lebendiges Freilichtmuseum, in dem das koloniale Leben durch restaurierte Gebäude und Vorführungen dargestellt wird."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <div class="sentence">
          <div class="sentence-text">Fort Wadsworth lies beneath the Verrazzano-Narrows Bridge and preserves military sites with sweeping views of the harbor.</div>
          <button class="translate-btn" data-translation="Fort Wadsworth liegt unter der Verrazzano-Narrows Bridge und bewahrt militärische Stätten mit weitem Blick über den Hafen."><span class="arrow">➜</span> Deutsch</button>
        </div>
      </section>

      <section class="card">
        <h2>Fast Facts</h2>
        <div class="sentence">
          <div class="sentence-text">Staten Island is nicknamed “The Borough of Parks” because of its many green spaces and nature preserves.</div>
          <button class="translate-btn" data-translation="Staten Island trägt den Spitznamen „The Borough of Parks“, wegen seiner vielen Grünflächen und Naturschutzgebiete."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <div class="sentence">
          <div class="sentence-text">Todt Hill, rising about 410 feet (125 meters), is the highest natural point in New York City.</div>
          <button class="translate-btn" data-translation="Der Todt Hill mit etwa 125 Metern Höhe ist der höchste natürliche Punkt in New York City."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <div class="sentence">
          <div class="sentence-text">The Verrazzano-Narrows Bridge connects Staten Island to Brooklyn and serves as a major gateway to the city.</div>
          <button class="translate-btn" data-translation="Die Verrazzano-Narrows Bridge verbindet Staten Island mit Brooklyn und dient als wichtiges Tor zur Stadt."><span class="arrow">➜</span> Deutsch</button>
        </div>
      </section>

      <section class="card">
        <h2>Population</h2>
        <div class="sentence">
          <div class="sentence-text">According to the 2020 U.S. Census, Staten Island had about 495,747 residents, making it the least populous borough of New York City.</div>
          <button class="translate-btn" data-translation="Laut der US-Volkszählung 2020 hatte Staten Island etwa 495.747 Einwohner und ist damit der am wenigsten bevölkerte Stadtbezirk von New York City."><span class="arrow">➜</span> Deutsch</button>
        </div>
      </section>

      <section class="card">
        <h2>Where is it?</h2>
        <div class="sentence">
          <div class="sentence-text">Staten Island lies southwest of Manhattan across New York Harbor and just north of New Jersey.</div>
          <button class="translate-btn" data-translation="Staten Island liegt südwestlich von Manhattan am New Yorker Hafen und direkt nördlich von New Jersey."><span class="arrow">➜</span> Deutsch</button>
        </div>
        <iframe width="100%" height="280" style="border:0;margin-top:14px;border-radius:12px" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14"></iframe>
      </section>
    </div>
  </div>

  <script>
    document.querySelectorAll('.translate-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        const parent = btn.closest('.sentence');
        let trans = parent.querySelector('.translation');
        if (!trans) {
          trans = document.createElement('div');
          trans.className = 'translation';
          trans.textContent = btn.dataset.translation;
          parent.appendChild(trans);
        }
        const isOpen = trans.classList.toggle('open');
        btn.querySelector('.arrow').style.transform = isOpen ? 'rotate(90deg)' : 'rotate(0deg)';
      });
    });
  </script>
</body>
</html>
