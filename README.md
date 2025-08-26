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

    .ring{
      position:absolute; inset: -60px auto auto -60px; width:180px; height:180px; border-radius:999px;
      background: radial-gradient(closest-side, rgba(34,211,238,.18), transparent 70%);
      pointer-events:none; filter: blur(1px);
    }
    .gallery{
      display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px;margin-top:12px
    }
    .gallery img{width:100%;height:220px;object-fit:cover;border-radius:14px;border:1px solid rgba(148,163,184,.25);box-shadow: var(--shadow)}
    footer{
      text-align:center;
      margin:40px 0 20px;
      font-weight:700;
      font-size:18px;
      color:#f9fafb;
    }
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
          <li><strong>Staten Island Ferry</strong> — A free boat ride that offers fantastic views of the New York skyline and the Statue of Liberty.</li>
          <li><strong>Snug Harbor Cultural Center & Botanical Garden</strong> — A historic campus featuring gardens, art galleries, and museums.</li>
          <li><strong>Historic Richmond Town</strong> — An open-air museum village that demonstrates life in colonial times.</li>
          <li><strong>Fort Wadsworth & Verrazzano-Narrows Bridge</strong> — A Civil War–era fortress beneath one of the world’s longest suspension bridges.</li>
        </ul>
      </section>

      <section class="card facts">
        <div class="ring"></div>
        <h2>Fast Facts</h2>
        <ul class="list">
          <li><strong>Nickname:</strong> Staten Island is often called “The Borough of Parks.”</li>
          <li><strong>Highest Point in NYC:</strong> Todt Hill reaches about 410 feet (125 m).</li>
          <li><strong>Iconic Crossing:</strong> The Verrazzano-Narrows Bridge connects Staten Island to Brooklyn.</li>
        </ul>
      </section>

      <section class="card population">
        <div class="ring"></div>
        <h2>Population</h2>
        <p>Staten Island has approximately <strong>495,747</strong> residents (2020 U.S. Census). It is the least populous of NYC’s five boroughs but one of the greenest by land area.</p>
      </section>

      <section class="card map">
        <div class="ring"></div>
        <h2>Where is it?</h2>
        <p>Staten Island lies southwest of Manhattan across New York Harbor and just north of New Jersey. It is connected to Brooklyn by the Verrazzano-Narrows Bridge and to New Jersey by several smaller bridges.</p>
        <iframe width="100%" height="300" style="border:0" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14"></iframe>
      </section>

      <section class="card pictures">
        <div class="ring"></div>
        <h2>Pictures</h2>
        <div class="gallery">
          <img src="images/IMG_2292.jpeg" alt="Staten Island Picture 1">
          <img src="images/IMG_2293.jpeg" alt="Staten Island Picture 2">
          <img src="images/IMG_2294.jpeg" alt="Staten Island Picture 3">
          <img src="images/IMG_2295.jpeg" alt="Staten Island Picture 4">
        </div>
      </section>
    </div>

    <footer>
      Erstellt von Marlon Leuchtmann, Paul Weisenbilder 8d
    </footer>
  </div>
</body>
</html>
