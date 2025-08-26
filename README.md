<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Staten Island — Digital Poster (Deluxe Max + Interactive)</title>
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
      --shadow: 0 16px 48px rgba(2,6,23,.7);
      --radius: 16px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;background:linear-gradient(180deg, rgba(6,10,23,1) 0%, rgba(7,16,32,1) 40%, rgba(2,6,23,1) 100%);color:var(--text);-webkit-font-smoothing:antialiased;overflow-y:scroll}

    /* subtle animated background lines */
    body::before{content:"";position:fixed;inset:0;background-image:linear-gradient(90deg, rgba(56,189,248,0.03) 1px, transparent 1px);background-size:180px 180px;pointer-events:none;opacity:0.8;animation:moveGrid 30s linear infinite}
    @keyframes moveGrid{from{transform:translateY(0)}to{transform:translateY(-120px)}}

    .wrap{max-width:1200px;margin:20px auto;padding:28px}
    header{display:flex;align-items:center;gap:18px;margin:8px 0 22px 0}
    header .emoji{font-size:64px;filter: drop-shadow(0 12px 28px rgba(34,211,248,.12));transform:translateY(-2px)}
    h1{font-size: clamp(34px, 6vw, 64px);line-height:1;margin:0;background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent}
    .subtitle{color:var(--muted);margin-top:6px;font-size:clamp(15px,2.2vw,18px)}

    .grid{display:grid;gap:18px;grid-template-columns: repeat(12, 1fr)}
    .card{grid-column: span 12;background:rgba(255,255,255,0.02);border:1px solid rgba(148,163,184,.06);border-radius: var(--radius);padding:18px;box-shadow:var(--shadow);position:relative;overflow:visible}
    .card h2{margin:0 0 12px 0;font-size: clamp(18px, 3vw, 26px);display:flex;align-items:center;gap:12px}
    .card .accent-bar{position:absolute;left:0;top:0;height:8px;width:60px;border-top-left-radius:var(--radius);border-bottom-right-radius:8px}

    .sentence{background:rgba(255,255,255,0.02); border:1px solid rgba(148,163,184,.04); padding:14px; border-radius:12px; display:flex; flex-direction:column; gap:10px;margin-bottom:12px}
    .sentence-text{line-height:1.5;font-size:1.02rem}

    .translate-row{display:flex;gap:10px;align-items:center}
    .translate-btn{background:linear-gradient(90deg,var(--accent),var(--accent-2));border:none;color:#032;font-weight:700;padding:8px 12px;border-radius:999px;cursor:pointer;display:inline-flex;align-items:center;gap:8px;box-shadow:0 8px 20px rgba(34,211,248,.06);transition:transform .12s ease}
    .translate-btn:active{transform:translateY(1px)}
    .arrow{display:inline-block;transition:transform .24s cubic-bezier(.2,.9,.2,1)}
    .speak-btn{background:transparent;border:1px solid rgba(148,163,184,.06);padding:8px;border-radius:999px;color:var(--muted);cursor:pointer}

    .translation{overflow:hidden;max-height:0;transition:max-height .34s cubic-bezier(.2,.9,.2,1),padding .28s; background:linear-gradient(180deg, rgba(255,255,255,.01), transparent);border-radius:10px;padding:0 12px;margin-top:6px;border:1px solid rgba(148,163,184,.04)}
    .translation.open{padding:10px 12px;max-height:260px}
    .translation p{margin:0;color:#e6eef7}

    .timeline{display:flex;gap:12px;align-items:flex-start;margin-top:12px}
    .timeline .event{flex:1;background:rgba(255,255,255,0.01);border:1px solid rgba(148,163,184,.04);padding:12px;border-radius:10px}
    .timeline .year{font-weight:800;color:var(--accent-2);font-size:1.05rem}

    .quiz{margin-top:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), transparent);padding:12px;border-radius:10px;border:1px solid rgba(148,163,184,.04)}
    .quiz h3{margin:0 0 8px 0}
    .options{display:flex;flex-direction:column;gap:8px;margin-top:8px}
    .option{background:rgba(255,255,255,0.02);border:1px solid rgba(148,163,184,.04);padding:10px;border-radius:8px;cursor:pointer}
    .option.correct{border-color:var(--green);background:linear-gradient(90deg,rgba(52,211,153,0.08),transparent)}
    .option.wrong{border-color:#fb7185;background:linear-gradient(90deg,rgba(251,113,133,0.04),transparent)}

    .chart{display:flex;gap:12px;align-items:center;margin-top:10px}
    .chart svg{width:100%;max-width:480px;height:120px}

    iframe{box-shadow:0 18px 50px rgba(2,6,23,.6);border-radius:10px;border:1px solid rgba(148,163,184,.04)}

    .glossary{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
    .chip{background:rgba(255,255,255,0.02);padding:8px 10px;border-radius:999px;border:1px solid rgba(148,163,184,.04);font-weight:700;color:var(--muted)}

    footer{margin-top:30px;text-align:center}
    footer .reflex{font-style:italic;color:var(--muted);margin-bottom:8px}
    footer .credit{font-weight:900;font-size:1.15rem;background:linear-gradient(90deg,var(--accent),var(--accent-2));-webkit-background-clip:text;background-clip:text;color:transparent}

    @media(max-width:900px){.grid{grid-template-columns:1fr}.timeline{flex-direction:column}}
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
        <div class="accent-bar" style="background:linear-gradient(90deg,#34d399,#60a5fa)"></div>
        <h2>🏞️ Top Attractions</h2>

        <div class="sentence">
          <div class="sentence-text">The Staten Island Ferry offers a free ride with panoramic views of Manhattan and the Statue of Liberty.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Die Staten Island Ferry bietet eine kostenlose Fahrt mit Panoramablick auf Manhattan und die Freiheitsstatue."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Die Staten Island Ferry bietet eine kostenlose Fahrt mit Panoramablick auf Manhattan und die Freiheitsstatue." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Snug Harbor Cultural Center & Botanical Garden is a historic campus with gardens, museums, and cultural programs for visitors of all ages.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Das Snug Harbor Cultural Center & Botanische Garten ist ein historisches Gelände mit Gärten, Museen und Kulturprogrammen für Besucher jeden Alters."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Das Snug Harbor Cultural Center und der Botanische Garten sind ein historisches Gelände mit Gärten, Museen und Kulturprogrammen für Besucher jeden Alters." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Historic Richmond Town is a living history village where colonial life is recreated through restored buildings and demonstrations.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Historic Richmond Town ist ein lebendiges Freilichtmuseum, in dem das koloniale Leben durch restaurierte Gebäude und Vorführungen dargestellt wird."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Historic Richmond Town ist ein lebendiges Freilichtmuseum, in dem das koloniale Leben durch restaurierte Gebäude und Vorführungen dargestellt wird." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Fort Wadsworth lies beneath the Verrazzano-Narrows Bridge and preserves military sites with sweeping views of the harbor.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Fort Wadsworth liegt unter der Verrazzano-Narrows Bridge und bewahrt militärische Stätten mit weitem Blick über den Hafen."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Fort Wadsworth liegt unter der Verrazzano-Narrows Bridge und bewahrt militärische Stätten mit weitem Blick über den Hafen." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

      </section>

      <section class="card">
        <div class="accent-bar" style="background:linear-gradient(90deg,#fbbf24,#38bdf8)"></div>
        <h2>📌 Fast Facts</h2>

        <div class="sentence">
          <div class="sentence-text">Staten Island is nicknamed “The Borough of Parks” because of its many green spaces and nature preserves.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Staten Island trägt den Spitznamen ‚The Borough of Parks‘ wegen seiner vielen Grünflächen und Naturschutzgebiete."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Staten Island trägt den Spitznamen The Borough of Parks wegen seiner vielen Grünflächen und Naturschutzgebiete." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">Todt Hill, rising about 410 feet (125 meters), is the highest natural point in New York City.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Der Todt Hill mit etwa 125 Metern Höhe ist der höchste natürliche Punkt in New York City."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Der Todt Hill mit etwa 125 Metern Höhe ist der höchste natürliche Punkt in New York City." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <div class="sentence">
          <div class="sentence-text">The Verrazzano-Narrows Bridge connects Staten Island to Brooklyn and serves as a major gateway to the city.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Die Verrazzano-Narrows Bridge verbindet Staten Island mit Brooklyn und dient als wichtiges Tor zur Stadt."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Die Verrazzano-Narrows Bridge verbindet Staten Island mit Brooklyn und dient als wichtiges Tor zur Stadt." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

      </section>

      <section class="card">
        <div class="accent-bar" style="background:linear-gradient(90deg,#7c3aed,#38bdf8)"></div>
        <h2>👥 Population</h2>

        <div class="sentence">
          <div class="sentence-text">According to the 2020 U.S. Census, Staten Island had about 495,747 residents, making it the least populous borough of New York City.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Laut der US-Volkszählung 2020 hatte Staten Island etwa 495.747 Einwohner und ist damit der am wenigsten bevölkerte Stadtbezirk von New York City."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Laut der US-Volkszählung 2020 hatte Staten Island etwa 495.747 Einwohner und ist damit der am wenigsten bevölkerte Stadtbezirk von New York City." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>

          <div class="chart" aria-hidden="true">
            <svg viewBox="0 0 600 120" role="img" aria-label="Population comparison chart">
              <defs>
                <linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#60a5fa"/><stop offset="1" stop-color="#38bdf8"/></linearGradient>
                <linearGradient id="highlight" x1="0" x2="1"><stop offset="0" stop-color="#34d399"/><stop offset="1" stop-color="#22c55e"/></linearGradient>
              </defs>
              <g font-family="Inter, Arial, sans-serif" font-size="11" fill="#cbd5e1">
                <text x="8" y="18">Manhattan</text>
                <rect x="110" y="6" width="460" height="14" rx="7" fill="url(#g1)"/>
                <text x="8" y="44">Brooklyn</text>
                <rect x="110" y="32" width="540" height="14" rx="7" fill="url(#g1)"/>
                <text x="8" y="70">Queens</text>
                <rect x="110" y="58" width="500" height="14" rx="7" fill="url(#g1)"/>
                <text x="8" y="96">Bronx</text>
                <rect x="110" y="84" width="360" height="14" rx="7" fill="url(#g1)"/>
                <text x="8" y="122">Staten Island</text>
                <rect x="110" y="110" width="270" height="14" rx="7" fill="url(#highlight)"/>
                <text x="392" y="122" fill="#cbd5e1" font-size="11">~495k</text>
              </g>
            </svg>
            <div class="note">Population comparison — Staten Island highlighted (approx.).</div>
          </div>

        </div>
      </section>

      <section class="card">
        <div class="accent-bar" style="background:linear-gradient(90deg,#60a5fa,#22d3ee)"></div>
        <h2>🗺️ Where is it?</h2>
        <div class="sentence">
          <div class="sentence-text">Staten Island lies southwest of Manhattan across New York Harbor and just north of New Jersey.</div>
          <div class="translate-row">
            <button class="translate-btn" data-translation="Staten Island liegt südwestlich von Manhattan am New Yorker Hafen und direkt nördlich von New Jersey."><span class="arrow">➜</span> Deutsch</button>
            <button class="speak-btn" data-speech="Staten Island liegt südwestlich von Manhattan am New Yorker Hafen und direkt nördlich von New Jersey." title="Play German" aria-label="Play German pronunciation">🔊</button>
          </div>
          <div class="translation" aria-hidden="true"><p></p></div>
        </div>

        <iframe width="100%" height="320" style="border:0;margin-top:12px;border-radius:10px" loading="lazy" src="https://www.openstreetmap.org/export/embed.html?bbox=-74.33%2C40.47%2C-74.02%2C40.67&amp;layer=mapnik&amp;marker=40.58%2C-74.14" title="Staten Island map"></iframe>

        <div style="margin-top:12px;color:var(--muted);font-size:0.95rem">Tip: Click the "Deutsch" buttons to reveal polished German translations. Use the speaker icon to hear the German text spoken (works in modern browsers).</div>

        <div class="glossary" aria-hidden="true">
          <div class="chip">Ferry = Fähre</div>
          <div class="chip">Borough = Stadtbezirk</div>
          <div class="chip">Harbor = Hafen</div>
          <div class="chip">Preserve = Schutzgebiet</div>
          <div class="chip">Historic = historisch</div>
        </div>

        <div class="timeline" aria-hidden="true">
          <div class="event"><div class="year">1660</div><div class="desc">European settlement begins in the area around Staten Island.</div></div>
          <div class="event"><div class="year">1760s</div><div class="desc">Richmond Town grows as a commercial and civic center.</div></div>
          <div class="event"><div class="year">1861–1865</div><div class="desc">Fort Wadsworth plays a defensive role during the Civil War era.</div></div>
          <div class="event"><div class="year">1964</div><div class="desc">Verrazzano-Narrows Bridge opens, connecting Staten Island to Brooklyn.</div></div>
        </div>

        <div class="quiz" aria-hidden="false">
          <h3>Quick Quiz</h3>
          <div>Which structure connects Staten Island to Brooklyn?</div>
          <div class="options">
            <button class="option" data-correct="false">Brooklyn Bridge</button>
            <button class="option" data-correct="false">Manhattan Bridge</button>
            <button class="option" data-correct="true">Verrazzano-Narrows Bridge</button>
            <button class="option" data-correct="false">George Washington Bridge</button>
          </div>
          <div id="quiz-feedback" style="margin-top:10px;color:var(--muted)">Select an answer to check.</div>
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
    // Translation toggle + smooth expand
    document.querySelectorAll('.translate-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        const sentence = btn.closest('.sentence');
        const box = sentence.querySelector('.translation');
        const p = box.querySelector('p');
        p.textContent = btn.dataset.translation || '';
        const open = box.classList.toggle('open');
        box.setAttribute('aria-hidden', String(!open));
        btn.querySelector('.arrow').style.transform = open ? 'rotate(90deg)' : 'rotate(0deg)';
        btn.setAttribute('aria-pressed', String(open));
      });
    });

    // Speech: use Web Speech API (if available)
    document.querySelectorAll('.speak-btn').forEach(btn => {
      btn.addEventListener('click', async () => {
        const text = btn.dataset.speech || '';
        if (!('speechSynthesis' in window)) {
          alert('Speech synthesis not supported in this browser.');
          return;
        }
        // stop any current speech
        window.speechSynthesis.cancel();
        const utter = new SpeechSynthesisUtterance(text);
        // prefer a German voice if available
        const voices = window.speechSynthesis.getVoices();
        const german = voices.find(v => /de|german/i.test(v.lang)) || voices.find(v => /de|german/i.test(v.name));
        if (german) utter.voice = german;
        utter.rate = 0.95; utter.pitch = 1;
        window.speechSynthesis.speak(utter);
      });
    });

    // Quiz logic
    document.querySelectorAll('.quiz .option').forEach(opt => {
      opt.addEventListener('click', () => {
        const correct = opt.dataset.correct === 'true';
        document.querySelectorAll('.quiz .option').forEach(o => { o.classList.remove('correct','wrong'); o.disabled = true; });
        if (correct) {
          opt.classList.add('correct');
          document.getElementById('quiz-feedback').textContent = 'Correct — well done! ✅';
        } else {
          opt.classList.add('wrong');
          const right = document.querySelector('.quiz .option[data-correct="true"]');
          right.classList.add('correct');
          document.getElementById('quiz-feedback').textContent = 'Not quite — the correct answer is highlighted.';
        }
      });
    });

    // small progressive enhancement: ensure voices are loaded for some browsers
    if ('speechSynthesis' in window) {
      window.speechSynthesis.getVoices();
    }

    // Parallax-ish slight movement for header on scroll
    window.addEventListener('scroll', () => {
      const y = window.scrollY;
      const emoji = document.querySelector('header .emoji');
      if (emoji) emoji.style.transform = `translateY(${Math.min(12, y/20)}px)`;
    });
  </script>
</body>
</html>
