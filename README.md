<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Klasseninfo – Sekundarschule</title>
<style>
  :root{
    --bg: #f3f5f7;          /* helles Grau */
    --card: #ffffff;        /* Karten-Hintergrund */
    --text: #1e1e1e;        /* Grundtext */
    --muted: #6b7280;       /* Sekundärtext */
    --brand: #4CAF50;       /* Grün (Akzent) */
    --brand-dark:#2e7d32;   /* dunkleres Grün für Hover */
    --ink: #111827;         /* fast schwarz */
    --anthra:#2b2f36;       /* Anthrazit */
    --danger:#e53935;       /* Löschen */
    --shadow: 0 10px 24px rgba(17,24,39,.08), 0 2px 6px rgba(17,24,39,.04);
    --radius: 14px;
  }

  *{box-sizing:border-box}
  html,body{margin:0;padding:0;background:var(--bg);color:var(--text);font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif}

  /* Header / Topbar */
  header{
    position:sticky; top:0; z-index:1000;
    background: linear-gradient(90deg,var(--anthra), #1f242b);
    color:#fff; box-shadow: var(--shadow);
  }
  .top{
    max-width:1100px; margin:0 auto; padding:14px 20px;
    display:flex; align-items:center; justify-content:space-between; gap:16px;
  }
  .brand{display:flex; align-items:center; gap:12px; font-weight:700; letter-spacing:.2px}
  .brand svg{width:34px; height:34px; flex:0 0 34px}
  nav{display:flex; gap:12px; flex-wrap:wrap}
  nav a{color:#e5e7eb; text-decoration:none; padding:8px 12px; border-radius:10px}
  nav a:hover{background:rgba(255,255,255,.08)}
  .actions{display:flex; gap:10px}
  .btn{
    appearance:none; border:none; border-radius:10px; padding:10px 14px; cursor:pointer; font-weight:600;
    transition:transform .05s ease, background .2s ease, opacity .2s ease;
  }
  .btn:active{transform:translateY(1px)}
  .btn-primary{background:var(--brand); color:#fff}
  .btn-primary:hover{background:var(--brand-dark)}
  .btn-danger{background:var(--danger); color:#fff}
  .btn-ghost{background:transparent; color:#e5e7eb}
  .btn-ghost:hover{background:rgba(255,255,255,.08)}

  /* Containers */
  .wrap{max-width:1100px; margin:24px auto; padding:0 20px}
  .hero{
    background: linear-gradient(135deg,#eaf6ec 0%, #ffffff 60%);
    border:1px solid #e5efe7; border-radius: var(--radius);
    padding:18px 18px; display:flex; align-items:center; gap:14px; margin-top:18px;
  }
  .hero .title{font-size:clamp(18px,2vw,22px); font-weight:800; color:var(--anthra)}
  .hero .sub{color:var(--muted); font-size:14px}

  /* Login card */
  #login{
    max-width:520px; margin:28px auto;
    background:var(--card); border-radius: var(--radius); box-shadow: var(--shadow);
    padding:22px;
  }
  .field{display:flex; flex-direction:column; gap:6px; margin:10px 0}
  label{font-size:13px; color:var(--muted)}
  input, select{
    border:1px solid #d1d5db; border-radius:10px; padding:12px 12px; background:#fff; font-size:15px;
  }
  input:focus, select:focus{outline:2px solid #a5d6a7; border-color:#a5d6a7}

  /* Content */
  #content{display:none}
  .grid{display:grid; grid-template-columns:1fr; gap:18px}
  @media (min-width:880px){ .grid{grid-template-columns:1fr 1fr} }
  .card{
    background:var(--card); border-radius: var(--radius); box-shadow: var(--shadow); overflow:hidden;
    display:flex; flex-direction:column;
  }
  .card-head{
    background:linear-gradient(180deg,#f7faf7 0,#fff 100%);
    border-bottom:1px solid #e5efe7; padding:14px 16px; display:flex; align-items:center; justify-content:space-between; gap:10px;
  }
  .card-title{display:flex; align-items:center; gap:10px; font-weight:800; color:var(--anthra)}
  .card-title svg{width:22px; height:22px}
  .card-body{padding:16px}
  .muted{color:var(--muted); font-size:14px}

  .list .item{
    border:1px solid #edf2ef; background:#fcfdfc; padding:12px; border-radius:12px; margin-bottom:10px;
    display:flex; align-items:flex-start; justify-content:space-between; gap:10px;
  }
  .item .main{display:flex; flex-direction:column; gap:4px}
  .badge{display:inline-flex; align-items:center; gap:6px; padding:4px 10px; border-radius:999px; background:#eaf6ec; color:#1b5e20; font-size:12px; font-weight:700}
  .pill{display:inline-flex; padding:2px 8px; border-radius:999px; background:#eef2f7; color:#374151; font-size:12px}

  .img-row{display:flex; flex-wrap:wrap; gap:10px}
  .img-row img{
    width:160px; max-width:100%; border-radius:12px; border:1px solid #e6ece8;
    box-shadow: 0 3px 10px rgba(0,0,0,.06);
  }

  .form-row{display:grid; grid-template-columns:1fr 1fr; gap:10px}
  .form-row > .full{grid-column:1 / -1}

  .hide{display:none}

  /* Footer note */
  footer{color:var(--muted); font-size:12px; text-align:center; padding:24px 0}
</style>
</head>
<body>

<header>
  <div class="top">
    <div class="brand">
      <!-- Einfaches „Schullogo“ als SVG -->
      <svg viewBox="0 0 64 64" aria-hidden="true">
        <circle cx="32" cy="32" r="30" fill="#4CAF50"></circle>
        <path d="M16 36l16-9 16 9-16 9-16-9zM16 28l16-9 16 9" fill="#ffffff" opacity=".9"></path>
      </svg>
      <div>Klasseninfo • Sekundarschule</div>
    </div>
    <nav aria-label="Navigation">
      <a href="#hw">Hausaufgaben</a>
      <a href="#eltern">Eltern</a>
      <a href="#plaene">Pläne</a>
    </nav>
    <div class="actions">
      <button class="btn btn-ghost" id="welcome" style="display:none"></button>
      <button class="btn btn-danger" id="logoutBtn" style="display:none" onclick="logout()">Logout</button>
    </div>
  </div>
</header>

<div class="wrap">
  <div class="hero">
    <div>
      <div class="title">Interne Klassenplattform</div>
      <div class="sub">Anmelden, dann Inhalte sehen. Admin kann Einträge hinzufügen und löschen. Alles lokal gespeichert (kostenlos, ohne Server).</div>
    </div>
  </div>

  <!-- LOGIN CARD -->
  <section id="login">
    <h2 style="margin:0 0 6px 0; font-weight:800; color:var(--anthra)"># ANMELDEN</h2>
    <div class="muted" style="margin-bottom:12px">Bitte Benutzername, Passwort und geheime ID eingeben.</div>
    <div class="field">
      <label for="username">Benutzername</label>
      <input id="username" placeholder="z. B. Max" />
    </div>
    <div class="field">
      <label for="password">Passwort</label>
      <input id="password" type="password" placeholder="••••••" />
    </div>
    <div class="field">
      <label for="userid">Geheime ID</label>
      <input id="userid" placeholder="z. B. 025" />
    </div>
    <div style="display:flex; gap:10px; margin-top:6px">
      <button class="btn btn-primary" onclick="login()">Anmelden</button>
      <button class="btn" onclick="clearInputs()" style="background:#e5e7eb; color:#111827">Zurücksetzen</button>
    </div>
    <div id="loginError" class="muted" style="color:#e53935; margin-top:10px"></div>
  </section>

  <!-- CONTENT -->
  <section id="content" class="grid" aria-live="polite" aria-busy="false">
    <!-- Hausaufgaben -->
    <article class="card" id="hw">
      <div class="card-head">
        <div class="card-title">
          <!-- Buch Icon -->
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20" stroke-width="1.6"/><path d="M6.5 2H20v17H6.5A2.5 2.5 0 0 0 4 21.5V4.5A2.5 2.5 0 0 1 6.5 2z" stroke-width="1.6"/></svg>
          <span>Hausaufgaben</span>
        </div>
        <button id="btnHausaufgaben" class="btn btn-primary hide" onclick="toggle('hwForm')">Neu</button>
      </div>
      <div class="card-body">
        <div id="hwForm" class="hide">
          <div class="form-row">
            <div>
              <label>Fach</label>
              <select id="fach">
                <option>Mathe</option><option>Deutsch</option><option>Englisch</option><option>Biologie</option><option>Chemie</option>
              </select>
            </div>
            <div>
              <label>Typ</label>
              <select id="typ">
                <option>Buch</option><option>Arbeitsheft</option><option>Übung</option>
              </select>
            </div>
            <div>
              <label>Seite</label>
              <input id="seite" inputmode="numeric" placeholder="z. B. 52" />
            </div>
            <div>
              <label>Nummer</label>
              <input id="nummer" inputmode="numeric" placeholder="z. B. 3a–c" />
            </div>
            <div class="full">
              <label>Abgabe bis</label>
              <input id="deadline" type="date" />
            </div>
          </div>
          <div style="margin-top:8px">
            <button class="btn btn-primary" onclick="saveHomework()">Speichern</button>
            <button class="btn" style="background:#e5e7eb;color:#111827" onclick="toggle('hwForm')">Abbrechen</button>
          </div>
          <hr style="border:none;border-top:1px solid #edf2ef; margin:14px 0">
        </div>

        <div id="hausaufgabenList" class="list muted">Noch keine Einträge.</div>
      </div>
    </article>

    <!-- Elternsprechtage -->
    <article class="card" id="eltern">
      <div class="card-head">
        <div class="card-title">
          <!-- Kalender Icon -->
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="3" y="4" width="18" height="18" rx="2" ry="2" stroke-width="1.6"/><line x1="16" y1="2" x2="16" y2="6" stroke-width="1.6"/><line x1="8" y1="2" x2="8" y2="6" stroke-width="1.6"/><line x1="3" y1="10" x2="21" y2="10" stroke-width="1.6"/></svg>
          <span>Elternsprechtage</span>
        </div>
        <button id="btnEltern" class="btn btn-primary hide" onclick="toggle('elternForm')">Neu</button>
      </div>
      <div class="card-body">
        <div id="elternForm" class="hide">
          <div class="form-row">
            <div>
              <label>Datum</label>
              <input id="elternDatum" type="date" />
            </div>
            <div>
              <label>Uhrzeit</label>
              <input id="elternUhrzeit" type="time" />
            </div>
            <div class="full">
              <label>Bemerkung</label>
              <input id="elternInfo" placeholder="z. B. Klasse 7a – Raum 204" />
            </div>
          </div>
          <div style="margin-top:8px">
            <button class="btn btn-primary" onclick="saveParent()">Speichern</button>
            <button class="btn" style="background:#e5e7eb;color:#111827" onclick="toggle('elternForm')">Abbrechen</button>
          </div>
          <hr style="border:none;border-top:1px solid #edf2ef; margin:14px 0">
        </div>

        <div id="elternList" class="list muted">Noch keine Termine.</div>
      </div>
    </article>

    <!-- Pläne -->
    <article class="card" id="plaene">
      <div class="card-head">
        <div class="card-title">
          <!-- Map/Plan Icon -->
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M9.5 3 3 5.5v15L9.5 18l5 2.5L21 18V3l-6.5 2.5-5-2.5Z" stroke-width="1.6"/><path d="M9.5 3v15M14.5 5.5v15" stroke-width="1.2"/></svg>
          <span>Pläne</span>
        </div>
        <button id="btnPlaene" class="btn btn-primary hide" onclick="toggle('plaeneForm')">Neu</button>
      </div>
      <div class="card-body">
        <div id="plaeneForm" class="hide">
          <div class="form-row">
            <div class="full">
              <label>Bild-URL</label>
              <input id="plaeneUrl" placeholder="https://…/plan.png" />
            </div>
          </div>
          <div style="margin-top:8px">
            <button class="btn btn-primary" onclick="savePlan()">Speichern</button>
            <button class="btn" style="background:#e5e7eb;color:#111827" onclick="toggle('plaeneForm')">Abbrechen</button>
          </div>
          <hr style="border:none;border-top:1px solid #edf2ef; margin:14px 0">
        </div>

        <div id="plaeneList" class="img-row muted">Noch keine Pläne.</div>
      </div>
    </article>
  </section>

  <footer>
    © Klasseninfo – rein lokal gespeichert. Für sensible Daten bitte echte Auth/Server nutzen.
  </footer>
</div>

<script>
  // Demo-Nutzer
  const users = [
    { username:"Max",  password:"123", id:"025", role:"admin"  },
    { username:"Lisa", password:"456", id:"024", role:"viewer" }
  ];

  // Utilities
  const $$ = sel => document.querySelector(sel);
  function toggle(id){ const el = document.getElementById(id); if(el) el.classList.toggle('hide'); }
  function clearInputs(){ ['username','password','userid'].forEach(i=>{$$('#'+i).value='';}); $$('#loginError').textContent='' }

  // Auth
  function login(){
    const uname = $$('#username').value.trim();
    const pass  = $$('#password').value;
    const sec   = $$('#userid').value.trim();

    // Einzelne Checks für klarere Fehlermeldungen
    const byUser = users.find(u => u.username === uname);
    if(!byUser){ return showLoginError('Unbekannter Benutzername.'); }
    if(byUser.password !== pass){ return showLoginError('Falsches Passwort.'); }
    if(byUser.id !== sec){ return showLoginError('Falsche geheime ID.'); }

    localStorage.setItem('role', byUser.role);
    localStorage.setItem('username', byUser.username);

    // UI freischalten
    $$('#login').style.display='none';
    $$('#content').style.display='grid';
    $$('#welcome').style.display='inline-block';
    $$('#welcome').textContent = 'Hallo, ' + byUser.username;
    $$('#logoutBtn').style.display='inline-block';

    if(byUser.role === 'admin'){
      ['btnHausaufgaben','btnEltern','btnPlaene'].forEach(id => document.getElementById(id).classList.remove('hide'));
    }
    loadData();
  }

  function logout(){
    localStorage.removeItem('role');
    localStorage.removeItem('username');
    location.reload();
  }

  function showLoginError(msg){ $$('#loginError').textContent = msg; }

  // Daten speichern/lesen
  function saveHomework(){
    if(localStorage.getItem('role')!=='admin'){ return alert('Keine Berechtigung!'); }
    const hw = {
      fach: $$('#fach').value,
      typ: $$('#typ').value,
      seite: $$('#seite').value.trim(),
      nummer: $$('#nummer').value.trim(),
      deadline: $$('#deadline').value
    };
    if(!hw.seite || !hw.nummer){ return alert('Bitte Seite und Nummer angeben.'); }
    const list = JSON.parse(localStorage.getItem('hausaufgaben')||'[]');
    list.push(hw);
    localStorage.setItem('hausaufgaben', JSON.stringify(list));
    toggle('hwForm'); loadData();
  }

  function saveParent(){
    if(localStorage.getItem('role')!=='admin'){ return alert('Keine Berechtigung!'); }
    const t = {
      datum: $$('#elternDatum').value,
      uhrzeit: $$('#elternUhrzeit').value,
      info: ($$('#elternInfo').value||'').trim()
    };
    if(!t.datum || !t.uhrzeit){ return alert('Bitte Datum und Uhrzeit angeben.'); }
    const list = JSON.parse(localStorage.getItem('eltern')||'[]');
    list.push(t);
    localStorage.setItem('eltern', JSON.stringify(list));
    toggle('elternForm'); loadData();
  }

  function savePlan(){
    if(localStorage.getItem('role')!=='admin'){ return alert('Keine Berechtigung!'); }
    const url = ($$('#plaeneUrl').value||'').trim();
    if(!url){ return alert('Bitte eine Bild-URL eingeben.'); }
    const list = JSON.parse(localStorage.getItem('plaene')||'[]');
    list.push(url);
    localStorage.setItem('plaene', JSON.stringify(list));
    toggle('plaeneForm'); loadData();
  }

  function deleteItem(key, index){
    if(localStorage.getItem('role')!=='admin'){ return alert('Keine Berechtigung!'); }
    const list = JSON.parse(localStorage.getItem(key)||'[]');
    list.splice(index,1);
    localStorage.setItem(key, JSON.stringify(list));
    loadData();
  }

  function loadData(){
    // Hausaufgaben
    const hwDiv = $$('#hausaufgabenList');
    const hws   = JSON.parse(localStorage.getItem('hausaufgaben')||'[]');
    hwDiv.innerHTML = '';
    if(hws.length===0){ hwDiv.textContent='Noch keine Einträge.'; }
    hws.forEach((hw,i)=>{
      const wrap = document.createElement('div'); wrap.className='item';
      const main = document.createElement('div'); main.className='main';
      const top  = document.createElement('div');
      top.innerHTML = `<span class="badge">${hw.fach}</span> <span class="pill">${hw.typ}</span>`;
      const body = document.createElement('div');
      const deadline = hw.deadline ? ` • bis <strong>${hw.deadline}</strong>` : '';
      body.innerHTML = `Seite <strong>${hw.seite}</strong>, Nr. <strong>${hw.nummer}</strong>${deadline}`;
      main.appendChild(top); main.appendChild(body);
      wrap.appendChild(main);

      if(localStorage.getItem('role')==='admin'){
        const del = document.createElement('button');
        del.className='btn btn-danger';
        del.textContent='Löschen';
        del.onclick=()=>deleteItem('hausaufgaben',i);
        wrap.appendChild(del);
      }
      hwDiv.appendChild(wrap);
    });

    // Eltern
    const elDiv = $$('#elternList');
    const els   = JSON.parse(localStorage.getItem('eltern')||'[]');
    elDiv.innerHTML = '';
    if(els.length===0){ elDiv.textContent='Noch keine Termine.'; }
    els.forEach((t,i)=>{
      const wrap = document.createElement('div'); wrap.className='item';
      const main = document.createElement('div'); main.className='main';
      const top  = document.createElement('div'); top.innerHTML=`<span class="badge">Termin</span>`;
      const body = document.createElement('div'); body.innerHTML = `<strong>${t.datum}</strong> • ${t.uhrzeit} ${t.info?('• '+t.info):''}`;
      main.appendChild(top); main.appendChild(body); wrap.appendChild(main);
      if(localStorage.getItem('role')==='admin'){
        const del = document.createElement('button'); del.className='btn btn-danger'; del.textContent='Löschen';
        del.onclick=()=>deleteItem('eltern',i); wrap.appendChild(del);
      }
      elDiv.appendChild(wrap);
    });

    // Pläne
    const plDiv = $$('#plaeneList');
    const pls   = JSON.parse(localStorage.getItem('plaene')||'[]');
    plDiv.innerHTML = '';
    if(pls.length===0){
      const p = document.createElement('div'); p.className='muted'; p.textContent='Noch keine Pläne.';
      plDiv.appendChild(p);
    } else {
      pls.forEach((url,i)=>{
        const box = document.createElement('div'); box.style.position='relative';
        const img = document.createElement('img'); img.src = url; img.alt='Plan';
        box.appendChild(img);
        if(localStorage.getItem('role')==='admin'){
          const del = document.createElement('button'); del.className='btn btn-danger'; del.textContent='Löschen';
          del.style.position='absolute'; del.style.top='8px'; del.style.right='8px';
          del.onclick=()=>deleteItem('plaene',i); box.appendChild(del);
        }
        plDiv.appendChild(box);
      });
    }
  }

  // Auto-login (wenn noch in localStorage)
  (function init(){
    const role = localStorage.getItem('role');
    const name = localStorage.getItem('username');
    if(role && name){
      // Login-UI ausblenden, Content zeigen
      $$('#login').style.display='none';
      $$('#content').style.display='grid';
      $$('#welcome').style.display='inline-block';
      $$('#welcome').textContent = 'Hallo, ' + name;
      $$('#logoutBtn').style.display='inline-block';
      if(role==='admin'){
        ['btnHausaufgaben','btnEltern','btnPlaene'].forEach(id => document.getElementById(id).classList.remove('hide'));
      }
      loadData();
    }
  })();
</script>
</body>
</html>
