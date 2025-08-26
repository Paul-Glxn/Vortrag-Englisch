<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Staten Island — Digital Poster</title>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0f172a;
      --card: #111827;
      --muted: #94a3b8;
      --text: #e5e7eb;
      --accent-blue: #38bdf8;
      --accent-green: #4ade80;
      --accent-orange: #fb923c;
      --accent-purple: #c084fc;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: Inter, system-ui, sans-serif;
      background: radial-gradient(1200px 600px at 10% 0%, rgba(34,211,238,.12), transparent 60%),
                  radial-gradient(1200px 600px at 90% -10%, rgba(56,189,248,.10), transparent 60%),
                  var(--bg);
      color: var(--text);
    }
    .wrap{max-width:1100px;margin:0 auto;padding:28px}
    header{display:flex;align-items:center;gap:18px;margin:18px 0 26px 0}
    header .emoji{font-size:46px;filter: drop-shadow(0 5px 12px rgba(34,211,238,.25));}
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
    .card h2{
      margin:0 0 12px 0;
      font-size: clamp(18px, 3.2vw, 28px);
      display:flex;align-items:center;gap:10px;
    }
    .sentence{
      margin:12px 0;
      padding:12px 14px;
      border-radius:14px;
      background:rgba(15,23,42,.45);
      border:1px solid rgba(148,163,184,.15);
      cursor:pointer;
      transition: background .25s;
    }
    .sentence:hover{background:rgba(30,41,59,.55)}
    .translation{display:none;color:var(--muted);margin-top:6px;font-size:15px}
    .sentence.open .translation{display:block}
    .arrow{float:right;transition: transform .25s ease}
    .sentence.open .arrow{transform:rotate(90deg)}

    .attractions h2{color:var(--accent-blue)}
    .facts h2{color:var(--accent-green)}
    .population h2{color:var(--accent-orange)}
    .map h2{color:var(--accent-purple)}

    .attractions{grid-column: span 7}
    .facts{grid-column: span 5}
    .population{grid-column: span 5}
    .map{grid-column: span 7}

    @media (max-width: 900px){
      .attractions,.facts,.population,.map{grid-column: span 12}
    }

    .nyc-map{
      margin-top:12px;
      background:#0f172a;
      padding:10px;
      border-radius:12px;
      border:1px solid rgba(148,163,184,.25);
      display:flex;justify-content:center;
    }
    .nyc-map svg{width:160px;height:auto}

    .selfcheck{
      margin-top:28px;
      padding:20px;
      border-radius:var(--radius);
      background:rgba(255,255,255,.04);
      border:1px solid rgba(148,163,184,.15);
    }
    .selfcheck h3{margin:0 0 12px 0}
    .selfcheck label{display:block;margin:8px 0;cursor:pointer}

    footer{
      margin-top:40px;
      text-align:center;
      font-weight:800;
      font-size:18px;
      color:#facc15;
      text-shadow:0 0 8px rgba(250,204,21,.6);
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
        <h2>🌊 Top Attractions</h2>
        <div class="sentence">
          Staten Island Ferry offers a free ride with views of the skyline and the Statue of Liberty.
          <span class="arrow">▶</span>
          <div class="translation">Die Staten Island Ferry bietet eine kostenlose Fahrt mit Blick auf die Skyline und die Freiheitsstatue.</div>
        </div>
        <div class="sentence">
          Snug Harbor Cultural Center & Botanical Garden features historic buildings, gardens, and museums.
          <span class="arrow">▶</span>
          <div class="translation">Das Snug Harbor Cultural Center & der Botanische Garten zeigen historische Gebäude, Gärten und Museen.</div>
        </div>
        <div class="sentence">
          Historic Richmond Town is a living history village that showcases colonial life.
          <span class="arrow">▶</span>
          <div class="translation">Historic Richmond Town ist ein Freilichtmuseum, das das koloniale Leben zeigt.</div>
        </div>
        <div class="sentence">
          Fort Wadsworth beneath the Verrazzano-Narrows Bridge is one of the oldest military sites in the U.S.
          <span class="arrow">▶</span>
          <div class="translation">Fort Wadsworth unter der Verrazzano-Narrows Bridge ist eine der ältesten Militäranlagen der USA.</div>
        </div>
      </section>

      <section class="card facts">
        <h2>📊 Fast Facts</h2>
        <div class="sentence">
          Staten Island is nicknamed “The Borough of Parks” because of its many green spaces.
          <span class="arrow">▶</span>
          <div class="translation">Staten Island wird wegen seiner vielen Grünflächen „The Borough of Parks“ genannt.</div>
        </div>
        <div class="sentence">
          The highest natural point in New York City is Todt Hill, located on Staten Island (~125 m).
          <span class="arrow">▶</span>
          <div class="translation">Der höchste Punkt in New York City ist der Todt Hill auf Staten Island (~125 m).</div>
        </div>
        <div class="sentence">
          The Verrazzano-Narrows Bridge connects Staten Island with Brooklyn.
          <span class="arrow">▶</span>
          <div class="translation">Die Verrazzano-Narrows Bridge verbindet Staten Island mit Brooklyn.</div>
        </div>
      </section>

      <section class="card population">
        <h2>👥 Population</h2>
        <div class="sentence">
          Staten Island has about 495,747 residents according to the 2020 U.S. Census.
          <span class="arrow">▶</span>
          <div class="translation">Staten Island hat etwa 495.747 Einwohner laut der Volkszählung 2020.</div>
        </div>
        <div class="sentence">
          It is the least populous of New York City’s five boroughs but one of the greenest by area.
          <span class="arrow">▶</span>
          <div class="translation">Es ist der bevölkerungsärmste Bezirk von New York City, aber einer der grünsten nach Fläche.</div>
        </div>
      </section>

      <section class="card map">
        <h2>🗺️ Where is it?</h2>
        <div class="sentence">
          Staten Island lies southwest of Manhattan, across New York Harbor, and north of New Jersey.
          <span class="arrow">▶</span>
          <div class="translation">Staten Island liegt südwestlich von Manhattan, am New Yorker Hafen und nördlich von New Jersey.</div>
        </div>
        <div class="sentence">
          The borough is connected to Brooklyn by the Verrazzano-Narrows Bridge and to New Jersey by several other bridges.
          <span class="arrow">▶</span>
          <div class="translation">Der Bezirk ist mit Brooklyn durch die Verrazzano-Narrows Bridge und mit New Jersey durch mehrere andere Brücken verbunden.</div>
        </div>

        <div class="nyc-map">
          <!-- Mini NYC Map with Staten Island highlighted -->
          <svg viewBox="0 0 200 150">
            <path d="M50 100 L70 110 L90 105 L85 125 L60 120 Z" fill="#38bdf8" stroke="#fff" stroke-width="2"/>
            <text x="60" y="115" font-size="10" fill="white">Staten Island</text>
            <circle cx="130" cy="60" r="30" fill="rgba(255,255,255,0.05)" stroke="#94a3b8"/>
            <text x="118" y="60" font-size="10" fill="#94a3b8">Manhattan</text>
          </svg>
        </div>
      </section>
    </div>

    <div class="selfcheck card">
      <h3>✅ Self-Check</h3>
      <label><input type="checkbox"> I can name at least 2 attractions of Staten Island.</label>
      <label><input type="checkbox"> I know why Staten Island is called “The Borough of Parks”.</label>
      <label><input type="checkbox"> I can explain where Staten Island is located.</label>
    </div>

    <footer>
      Erstellt von Marlon Leuchtmann, Paul Weisenbilder 8d
    </footer>
  </div>

  <script>
    document.querySelectorAll('.sentence').forEach(el=>{
      el.addEventListener('click', ()=>{
        el.classList.toggle('open');
      });
    });
  </script>
</body>
</html>
