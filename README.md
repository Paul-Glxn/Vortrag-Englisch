<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Staten Island — Digital Poster (Deluxe Max)</title>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #071020;
      --muted: #94a3b8;
      --text: #f1f5f9;
      --accent: #38bdf8;
      --accent-2: #22d3ee;
      --green: #34d399;
      --gold: #fbbf24;
      --shadow: 0 14px 40px rgba(2,6,23,.7);
      --radius: 16px;
      --card-grad: linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;background:radial-gradient(1000px 500px at 10% 0%, rgba(34,211,238,.06), transparent 40%), radial-gradient(1000px 500px at 90% -10%, rgba(56,189,248,.04), transparent 40%), var(--bg);color:var(--text);-webkit-font-smoothing:antialiased}

    .wrap{max-width:1100px;margin:20px auto;padding:28px}
    header{display:flex;align-items:center;gap:18px;margin:6px 0 22px 0}
    header .emoji{font-size:64px;filter: drop-shadow(0 12px 24px rgba(34,211,248,.12));transform:translateY(-2px)}
    h1{font-size: clamp(34px, 6vw, 64px);line-height:1;margin:0;background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent}
    .subtitle{color:var(--muted);margin-top:6px;font-size:clamp(15px,2.2vw,18px)}

    .grid{display:grid;gap:18px;grid-template-columns: repeat(12, 1fr)}
    .card{grid-column: span 12;background:var(--card-grad);border:1px solid rgba(148,163,184,.08);border-radius: var(--radius);padding:20px;box-shadow:var(--shadow);position:relative;overflow:visible}
    .card h2{margin:0 0 12px 0;font-size: clamp(18px, 3vw, 26px);display:flex;align-items:center;gap:12px}
    .card .accent-bar{position:absolute;left:0;top:0;height:8px;width:60px;border-top-left-radius:var(--radius);border-bottom-right-radius:8px}

    .sentence{background:rgba(255,255,255,0.02); border:1px solid rgba(148,163,184,.06); padding:14px; border-radius:12px; display:flex; flex-direction:column; gap:10px;margin-bottom:12px;opacity:0;transform:translateY(8px);animation:fadeInUp .5s forwards}
    .sentence:nth-of-type(1){animation-delay:.05s}
    .sentence:nth-of-type(2){animation-delay:.12s}
    .sentence:nth-of-type(3){animation-delay:.19s}
    .sentence:nth-of-type(4){animation-delay:.26s}
    .sentence:nth-of-type(5){animation-delay:.33s}
    .sentence-text{line-height:1.45;font-size:1.02rem}

    .translate-row{display:flex;gap:12px;align-items:center}
    .translate-btn{background:linear-gradient(90deg,var(--accent),var(--accent-2));border:none;color:#032;font-weight:700;padding:8px 12px;border-radius:999px;cursor:pointer;display:inline-flex;align-items:center;gap:8px;box-shadow:0 8px 18px rgba(34,211,238,.08);transition:transform .16s ease}
    .translate-btn:active{transform:translateY(1px) scale(.997)}
    .translate-btn .arrow{display:inline-block;transition:transform .24s cubic-bezier(.2,.9,.2,1)}

    .translation{overflow:hidden;max-height:0;transition:max-height .32s cubic-bezier(.2,.9,.2,1),padding .28s; background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));border-radius:10px;padding:0 12px;margin-top:6px;border:1px solid rgba(148,163,184,.06)}
    .translation.open{padding:10px 12px;max-height:240px}
    .translation p{margin:0;color:#e6eef7}

    /* category accents */
    .accent-park{background:linear-gradient(90deg,var(--green),#60a5fa)}
    .accent-fact{background:linear-gradient(90deg,var(--gold),var(--accent))}
    .accent-pop{background:linear-gradient(90deg,var(--accent),#7c3aed)}
    .accent-map{background:linear-gradient(90deg,#60a5fa,var(--accent-2))}

    /* glossary chips */
    .glossary{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
    .chip{background:rgba(255,255,255,0.03);padding:8px 10px;border-radius:999px;border:1px solid rgba(148,163,184,.06);font-weight:600;color:var(--muted)}

    /* mini-infographic */
    .chart{display:flex;gap:12px;align-items:center;margin-top:10px}
    .chart svg{width:100%;max-width:480px;height:140px}
    .chart .note{color:var(--muted);font-size:0.9rem}

    iframe{box-shadow:0 18px 50px rgba(2,6,23,.6);border-radius:10px;border:1px solid rgba(148,163,184,.04)}

    footer{margin-top:30px;text-align:center}
    footer .reflex{font-style:italic;color:var(--muted);margin-bottom:8px}
    footer .credit{font-weight:900;font-size:1.15rem;background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent}

    @keyframes fadeInUp{to{opacity:1;transform:none}}

    @media(max-width:900px){.grid{grid-template-columns:1fr}.card{padding:16px}}
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
        <div class="accent-bar accent-park"></div>
        <h2>🏞️ Top Attractions</h2>

        <div class="sentence">
          <div class="sentence-text">The Staten Island Ferry offers a free ride with panoramic views of Manhattan and the Statue of Liberty.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Die Staten Island Ferry bietet eine kostenlose Fahrt mit Panoramablick auf Manhattan und die Freiheitsstatue."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Snug Harbor Cultural Center & Botanical Garden is a historic campus with gardens, museums, and cultural programs for visitors of all ages.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Das Snug Harbor Cultural Center & Botanische Garten ist ein historisches Gelände mit Gärten, Museen und Kulturprogrammen für Besucher jeden Alters."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Historic Richmond Town is a living history village where colonial life is recreated through restored buildings and demonstrations.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Historic Richmond Town ist ein lebendiges Freilichtmuseum, in dem das koloniale Leben durch restaurierte Gebäude und Vorführungen dargestellt wird."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Fort Wadsworth lies beneath the Verrazzano-Narrows Bridge and preserves military sites with sweeping views of the harbor.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Fort Wadsworth liegt unter der Verrazzano-Narrows Bridge und bewahrt militärische Stätten mit weitem Blick über den Hafen."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

      </section>

      <section class="card">
        <div class="accent-bar accent-fact"></div>
        <h2>📌 Fast Facts</h2>

        <div class="sentence">
          <div class="sentence-text">Staten Island is nicknamed “The Borough of Parks” because of its many green spaces and nature preserves.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Staten Island trägt den Spitznamen „The Borough of Parks“ wegen seiner vielen Grünflächen und Naturschutzgebiete."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Todt Hill, rising about 410 feet (125 meters), is the highest natural point in New York City.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Der Todt Hill mit etwa 125 Metern Höhe ist der höchste natürliche Punkt in New York City."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">The Verrazzano-Narrows Bridge connects Staten Island to Brooklyn and serves as a major gateway to the city.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Die Verrazzano-Narrows Bridge verbindet Staten Island mit Brooklyn und dient als wichtiges Tor zur Stadt."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

      </section>

      <section class="card">
        <div class="accent-bar accent-pop"></div>
        <h2>👥 Population</h2>

        <div class="sentence">
          <div class="sentence-text">According to the 2020 U.S. Census, Staten Island had about 495,747 residents, making it the least populous borough of New York City.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Laut der US-Volkszählung 2020 hatte Staten Island etwa 495.747 Einwohner und ist damit der am wenigsten bevölkerte Stadtbezirk von New York City."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>

          <div class="chart" aria-hidden="true">
            <svg viewBox="0 0 600 140" role="img" aria-label="Population comparison chart">
              <defs>
                <linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#60a5fa"/><stop offset="1" stop-color="#38bdf8"/></linearGradient>
                <linearGradient id="g2" x1="0" x2="1"><stop offset="0" stop-color="#93c5fd"/><stop offset="1" stop-color="#7dd3fc"/></linearGradient>
                <linearGradient id="highlight" x1="0" x2="1"><stop offset="0" stop-color="#34d399"/><stop offset="1" stop-color="#22c55e"/></linearGradient>
              </defs>
              <g font-family="Inter, Arial, sans-serif" font-size="12" fill="#cbd5e1">
                <text x="8" y="20">Manhattan</text>
                <rect x="110" y="8" width="430" height="18" rx="9" fill="url(#g1)"/>
                <text x="8" y="50">Brooklyn</text>
                <rect x="110" y="38" width="520" height="18" rx="9" fill="url(#g2)"/>
                <text x="8" y="80">Queens</text>
                <rect x="110" y="68" width="480" height="18" rx="9" fill="url(#g2)"/>
                <text x="8" y="110">Bronx</text>
                <rect x="110" y="98" width="320" height="18" rx="9" fill="url(#g2)"/>
                <text x="8" y="140">Staten Island</text>
                <rect x="110" y="128" width="260" height="18" rx="9" fill="url(#highlight)"/>
                <text x="540" y="128" fill="#cbd5e1" font-size="11">~495k</text>
              </g>
            </svg>
            <div class="note">Population comparison — Staten Island highlighted (approx.).</div>
          </div>

        </div>
      </section>

      <section class="card">
        <div class="accent-bar accent-map"></div>
        <h2>🗺️ Where is it?</h2>
        <div class="sentence">
          <div class="sentence-text">Staten Island lies southwest of Manhattan across New York Harbor and just north of New Jersey.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Staten Island liegt südwestlich von Manhattan am New Yorker Hafen und direkt nördlich von New Jersey."><span class="arrow">➜</span> Deutsch</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <iframe width="100%" height="300" style="border:0;margin-top:12px;border-radius:10px" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14" title="Staten Island map"></iframe>

        <div style="margin-top:12px;color:var(--muted);font-size:0.95rem">Tip: Click the "Deutsch" buttons to reveal polished German translations. The mini-chart compares borough populations for quick context.</div>

        <div class="glossary" aria-hidden="true">
          <div class="chip">Ferry = Fähre</div>
          <div class="chip">Borough = Stadtbezirk</div>
          <div class="chip">Harbor = Hafen</div>
          <div class="chip">Preserve = Schutzgebiet</div>
          <div class="chip">Historic = historisch</div>
        </div>

      </section>

    </div>

    <footer>
      <div class="reflex">This poster was created to present Staten Island bilingually, combining geography, history, and language practice.</div>
      <div class="reflex">Dieses Poster wurde zweisprachig gestaltet, um Geografie, Geschichte und Sprachpraxis zu verbinden.</div>
      <div class="credit">Erstellt von Marlon Leuchtmann, Paul Weisenbilder — Klasse 8d</div>
    </footer>
  </div>

  <script>
    // Toggle translations with smooth expand and accessible updates
    document.querySelectorAll('.translate-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        const parentSentence = btn.closest('.sentence');
        const box = parentSentence.querySelector('.translation');
        const p = box.querySelector('p');
        const text = btn.dataset.translation || '';
        p.textContent = text;
        const isOpen = box.classList.toggle('open');
        box.setAttribute('aria-hidden', String(!isOpen));
        btn.querySelector('.arrow').style.transform = isOpen ? 'rotate(90deg)' : 'rotate(0deg)';
        // Announce for screen readers (simple)
        if (isOpen) {
          btn.setAttribute('aria-label', 'Close German translation');
        } else {
          btn.setAttribute('aria-label', 'Open German translation');
        }
      });

      btn.addEventListener('keydown', (ev) => {
        if (ev.key === 'Enter' || ev.key === ' ') { ev.preventDefault(); btn.click(); }
      });
    });

    // small enhancement: animate headings on load
    document.querySelectorAll('.card h2').forEach((h, i) => {
      h.style.opacity = 0;
      h.style.transform = 'translateY(6px)';
      setTimeout(()=>{h.style.transition='all .45s cubic-bezier(.2,.9,.2,1)';h.style.opacity=1;h.style.transform='none'}, 120 + i*80);
    });
  </script>
</body>
</html>
