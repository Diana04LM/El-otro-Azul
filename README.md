<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>El Otro Azul — Revista Azul 1894–1896</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400;1,600&family=EB+Garamond:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
<style>
/* ── VARIABLES ──────────────────────────────────── */
:root {
  --cream:    #EDE8DF;
  --cream-dk: #E0D9CE;
  --blue:     #8AA4C3;
  --blue-lt:  #B5CADF;
  --blue-dk:  #6B8DAD;
  --navy:     #1B2A44;
  --navy-lt:  #2C3E58;
  --text:     #2A3545;
  --muted:    #6B7D93;
  --white:    #FAF8F4;
  --gold:     #C4A96D;

  --serif-display: 'Cormorant Garamond', Georgia, serif;
  --serif-body:    'EB Garamond', Georgia, serif;
}

/* ── RESET & BASE ───────────────────────────────── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  font-family: var(--serif-body);
  font-size: 18px;
  line-height: 1.7;
  background: var(--cream);
  color: var(--text);
  min-height: 100vh;
}
img { display: block; max-width: 100%; }
a { color: var(--navy); text-decoration: none; }
a:hover { text-decoration: underline; }

/* ── NAVIGATION ─────────────────────────────────── */
nav {
  position: sticky;
  top: 0;
  z-index: 100;
  background: var(--navy);
  border-bottom: 2px solid var(--blue);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 2rem;
  height: 56px;
}
.nav-brand {
  font-family: var(--serif-display);
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--blue-lt);
  letter-spacing: 0.05em;
  white-space: nowrap;
}
.nav-tabs {
  display: flex;
  gap: 0.25rem;
  list-style: none;
}
.nav-tabs li button {
  background: none;
  border: none;
  color: var(--blue-lt);
  font-family: var(--serif-body);
  font-size: 0.95rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  cursor: pointer;
  padding: 0.5rem 1.1rem;
  border-bottom: 2px solid transparent;
  transition: color 0.2s, border-color 0.2s;
}
.nav-tabs li button:hover,
.nav-tabs li button.active {
  color: var(--white);
  border-bottom-color: var(--gold);
}

/* ── SECTIONS ───────────────────────────────────── */
.page { display: none; animation: fadeIn 0.35s ease; }
.page.active { display: block; }
@keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; } }

/* ── HERO ───────────────────────────────────────── */
.hero {
  position: relative;
  background: var(--navy);
  color: var(--white);
  padding: 5rem 2rem 4rem;
  text-align: center;
  overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 60% 80% at 30% 50%, rgba(138,164,195,0.18) 0%, transparent 70%),
    radial-gradient(ellipse 40% 60% at 75% 40%, rgba(138,164,195,0.10) 0%, transparent 60%);
}
.hero-label {
  font-size: 0.8rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--blue-lt);
  margin-bottom: 1.5rem;
  position: relative;
}
.hero h1 {
  font-family: var(--serif-display);
  font-size: clamp(3.5rem, 10vw, 6.5rem);
  font-weight: 300;
  line-height: 1;
  letter-spacing: 0.04em;
  color: var(--white);
  position: relative;
}
.hero h1 em {
  color: var(--blue-lt);
  font-style: italic;
}
.hero-sub {
  font-family: var(--serif-display);
  font-size: 1.1rem;
  color: var(--blue-lt);
  margin-top: 1rem;
  letter-spacing: 0.08em;
  position: relative;
}
.hero-desc {
  max-width: 640px;
  margin: 2rem auto 0;
  font-size: 1.05rem;
  color: rgba(255,255,255,0.75);
  position: relative;
  font-style: italic;
}
.stats-bar {
  display: flex;
  justify-content: center;
  gap: 3rem;
  margin-top: 3.5rem;
  flex-wrap: wrap;
  position: relative;
}
.stat { text-align: center; }
.stat-num {
  font-family: var(--serif-display);
  font-size: 3rem;
  font-weight: 300;
  color: var(--blue-lt);
  line-height: 1;
}
.stat-lbl {
  font-size: 0.75rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
  margin-top: 0.25rem;
}
.hero-divider {
  width: 60px;
  height: 1px;
  background: var(--gold);
  margin: 3rem auto 0;
  position: relative;
}

/* ── SECTION HEADER ─────────────────────────────── */
.section-header {
  max-width: 900px;
  margin: 0 auto;
  padding: 3.5rem 2rem 2rem;
  text-align: center;
}
.section-label {
  font-size: 0.75rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--blue-dk);
  margin-bottom: 0.75rem;
}
.section-title {
  font-family: var(--serif-display);
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 300;
  color: var(--navy);
  line-height: 1.2;
}
.section-intro {
  max-width: 600px;
  margin: 1rem auto 0;
  color: var(--muted);
  font-style: italic;
}

/* ── AUTHORS GRID ───────────────────────────────── */
.authors-container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 1rem 1.5rem 4rem;
}
.authors-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.25rem;
}
.author-card {
  background: var(--white);
  border: 1px solid var(--blue-lt);
  border-radius: 2px;
  cursor: pointer;
  transition: box-shadow 0.25s, transform 0.25s;
  overflow: hidden;
}
.author-card:hover {
  box-shadow: 0 8px 28px rgba(27,42,68,0.12);
  transform: translateY(-2px);
}
.author-card.open {
  grid-column: 1 / -1;
  transform: none;
  cursor: default;
}
.author-card-header {
  padding: 1.5rem 1.75rem;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 1rem;
  cursor: pointer;
}
.author-genre-badge {
  display: inline-block;
  font-size: 0.65rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  background: var(--blue-lt);
  color: var(--navy);
  padding: 0.2rem 0.6rem;
  border-radius: 2px;
  margin-bottom: 0.5rem;
}
.author-name {
  font-family: var(--serif-display);
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--navy);
  line-height: 1.2;
}
.author-origin {
  font-size: 0.85rem;
  color: var(--muted);
  margin-top: 0.25rem;
  font-style: italic;
}
.author-card-arrow {
  font-size: 1.2rem;
  color: var(--blue-dk);
  transition: transform 0.25s;
  flex-shrink: 0;
  margin-top: 0.25rem;
}
.author-card.open .author-card-arrow { transform: rotate(90deg); }

/* Author expanded panel */
.author-panel {
  display: none;
  border-top: 1px solid var(--blue-lt);
}
.author-card.open .author-panel { display: block; }
.author-panel-inner {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 0;
  min-height: 400px;
}
.author-bio-col {
  background: var(--navy);
  color: var(--white);
  padding: 2rem 2rem;
}
.author-bio-col h3 {
  font-family: var(--serif-display);
  font-size: 1.8rem;
  font-weight: 300;
  color: var(--blue-lt);
  margin-bottom: 0.25rem;
}
.author-bio-col .bio-origin {
  font-size: 0.8rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--blue);
  margin-bottom: 1.25rem;
  padding-bottom: 1.25rem;
  border-bottom: 1px solid rgba(138,164,195,0.3);
}
.author-bio-text {
  font-size: 0.95rem;
  line-height: 1.75;
  color: rgba(255,255,255,0.82);
}
.author-texts-col {
  padding: 2rem;
  background: var(--cream);
  overflow-y: auto;
  max-height: 70vh;
}
.texts-list-title {
  font-size: 0.7rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 1rem;
}
.text-item {
  border-bottom: 1px solid var(--cream-dk);
  padding: 0.75rem 0;
}
.text-item:last-child { border-bottom: none; }
.text-item-btn {
  background: none;
  border: none;
  cursor: pointer;
  text-align: left;
  width: 100%;
  padding: 0;
}
.text-item-title {
  font-family: var(--serif-display);
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--navy);
  font-style: italic;
}
.text-item-ref {
  font-size: 0.78rem;
  color: var(--muted);
  letter-spacing: 0.05em;
}
.text-item-btn:hover .text-item-title { color: var(--blue-dk); text-decoration: underline; }
.text-content {
  display: none;
  margin-top: 1rem;
  padding: 1.5rem;
  background: var(--white);
  border-left: 3px solid var(--blue);
  border-radius: 0 2px 2px 0;
}
.text-content.open { display: block; }
.text-content p {
  margin-bottom: 1rem;
  font-size: 0.97rem;
  line-height: 1.8;
}
.text-content p:last-child { margin-bottom: 0; }
/* Poetry styles */
.poem-stanza {
  margin-bottom: 1.25rem;
  font-style: italic;
  font-size: 0.97rem;
  line-height: 2;
}
.poem-stanza:last-child { margin-bottom: 0; }

/* ── REVISTA AZUL PAGE ──────────────────────────── */
.revista-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 1rem 2rem 5rem;
}
.revista-block {
  background: var(--white);
  border-radius: 2px;
  padding: 2.5rem;
  margin-bottom: 2rem;
  border-left: 4px solid var(--blue);
}
.revista-block h2 {
  font-family: var(--serif-display);
  font-size: 1.8rem;
  font-weight: 400;
  color: var(--navy);
  margin-bottom: 1rem;
}
.revista-block h3 {
  font-family: var(--serif-display);
  font-size: 1.3rem;
  font-weight: 400;
  color: var(--navy);
  margin: 1.5rem 0 0.5rem;
}
.revista-block p {
  margin-bottom: 1rem;
  line-height: 1.85;
  color: var(--text);
}
.revista-block p:last-child { margin-bottom: 0; }
.revista-block em { font-style: italic; color: var(--navy-lt); }
.revista-block strong { font-weight: 600; color: var(--navy); }
.quote-block {
  border-left: 3px solid var(--gold);
  padding-left: 1.5rem;
  margin: 1.5rem 0;
  font-style: italic;
  color: var(--navy-lt);
  font-size: 1.05rem;
}

/* ── DATA PAGE ──────────────────────────────────── */
.datos-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 1.5rem 5rem;
}
.datos-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  margin-bottom: 1.5rem;
}
.datos-grid.single { grid-template-columns: 1fr; }
@media (max-width: 680px) { .datos-grid { grid-template-columns: 1fr; } }
.chart-card {
  background: var(--white);
  border-radius: 2px;
  padding: 1.75rem;
  border: 1px solid var(--blue-lt);
}
.chart-card h3 {
  font-family: var(--serif-display);
  font-size: 1.2rem;
  color: var(--navy);
  margin-bottom: 1.25rem;
  font-weight: 400;
  font-style: italic;
}
/* Bar chart */
.bar-chart { display: flex; flex-direction: column; gap: 0.6rem; }
.bar-row { display: flex; align-items: center; gap: 0.75rem; }
.bar-lbl {
  font-size: 0.8rem;
  color: var(--muted);
  width: 160px;
  flex-shrink: 0;
  text-align: right;
  font-style: italic;
}
.bar-track {
  flex: 1;
  background: var(--cream-dk);
  border-radius: 2px;
  height: 20px;
  position: relative;
  overflow: hidden;
}
.bar-fill {
  height: 100%;
  background: var(--blue);
  border-radius: 2px;
  transition: width 1s ease;
}
.bar-val {
  font-size: 0.8rem;
  color: var(--navy);
  font-weight: 600;
  min-width: 24px;
}
/* Donut chart */
.donut-wrap { display: flex; align-items: center; gap: 2rem; }
.donut-legend { display: flex; flex-direction: column; gap: 0.6rem; }
.legend-item { display: flex; align-items: center; gap: 0.5rem; font-size: 0.85rem; color: var(--text); }
.legend-dot { width: 12px; height: 12px; border-radius: 50%; flex-shrink: 0; }
/* Timeline */
.timeline { display: flex; flex-direction: column; gap: 0; }
.tl-row { display: flex; align-items: center; gap: 0.75rem; padding: 0.4rem 0; border-bottom: 1px dashed var(--cream-dk); }
.tl-row:last-child { border-bottom: none; }
.tl-name { font-size: 0.82rem; color: var(--muted); width: 165px; flex-shrink: 0; text-align: right; font-style: italic; }
.tl-track {
  flex: 1;
  height: 10px;
  background: var(--cream-dk);
  border-radius: 5px;
  position: relative;
}
.tl-bar {
  position: absolute;
  top: 0;
  height: 100%;
  border-radius: 5px;
  background: var(--blue);
}
.tl-years { font-size: 0.75rem; color: var(--muted); min-width: 80px; }
/* Volumes table */
.vol-table { width: 100%; border-collapse: collapse; font-size: 0.88rem; }
.vol-table th {
  text-align: left;
  font-size: 0.7rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  border-bottom: 2px solid var(--blue-lt);
  padding: 0.4rem 0.6rem;
}
.vol-table td {
  padding: 0.45rem 0.6rem;
  border-bottom: 1px solid var(--cream-dk);
  color: var(--text);
  vertical-align: top;
}
.vol-table tr:last-child td { border-bottom: none; }
.vol-table td:first-child { font-style: italic; color: var(--navy); }
.genre-badge {
  font-size: 0.65rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 0.1rem 0.4rem;
  border-radius: 2px;
  background: var(--blue-lt);
  color: var(--navy);
}
.genre-badge.lirica { background: #D4C5E8; color: #4A2A6A; }
.country-badges { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 0.5rem; }
.country-badge {
  font-size: 0.72rem;
  padding: 0.15rem 0.5rem;
  background: var(--navy);
  color: var(--blue-lt);
  border-radius: 2px;
}

/* ── FOOTER ─────────────────────────────────────── */
footer {
  background: var(--navy);
  color: rgba(255,255,255,0.45);
  text-align: center;
  padding: 2rem;
  font-size: 0.85rem;
  font-style: italic;
}
footer em { color: var(--blue-lt); font-style: normal; }

/* ── RESPONSIVE ──────────────────────────────────── */
@media (max-width: 720px) {
  nav { padding: 0 1rem; }
  .nav-brand { font-size: 1rem; }
  .nav-tabs li button { padding: 0.5rem 0.6rem; font-size: 0.8rem; }
  .author-panel-inner { grid-template-columns: 1fr; }
  .author-texts-col { max-height: none; }
  .bar-lbl { width: 110px; }
  .tl-name { width: 110px; }
}
</style>
</head>
<body>

<!-- ── NAVIGATION ──────────────────────────────── -->
<nav>
  <span class="nav-brand">El Otro Azul</span>
  <ul class="nav-tabs">
    <li><button class="active" onclick="showPage('inicio', this)">Inicio</button></li>
    <li><button onclick="showPage('autoras', this)">Autoras</button></li>
    <li><button onclick="showPage('revista', this)">Revista Azul</button></li>
    <li><button onclick="showPage('datos', this)">Datos</button></li>
  </ul>
</nav>

<!-- ══════════════════════════════════════════════ -->
<!-- PAGE: INICIO                                   -->
<!-- ══════════════════════════════════════════════ -->
<section id="page-inicio" class="page active">
  <div class="hero">
    <p class="hero-label">Proyecto de recuperación de textos</p>
    <h1><em>El Otro</em> Azul</h1>
    <p class="hero-sub">Revista Azul · México, 1894–1896</p>
    <p class="hero-desc">
      Una antología crítica que rescata las voces femeninas publicadas en la <em>Revista Azul</em>,
      emblemática publicación del modernismo hispanoamericano. Ocho escritoras de México, Cuba,
      España, Venezuela y Rumania, cuya obra narrativa y lírica mereció un lugar en sus páginas.
    </p>
    <div class="stats-bar">
      <div class="stat"><div class="stat-num">8</div><div class="stat-lbl">Autoras</div></div>
      <div class="stat"><div class="stat-num">12</div><div class="stat-lbl">Textos Narrativos</div></div>
      <div class="stat"><div class="stat-num">28</div><div class="stat-lbl">Poemas</div></div>
      <div class="stat"><div class="stat-num">5</div><div class="stat-lbl">Países</div></div>
    </div>
    <div class="hero-divider"></div>
  </div>

  <div class="section-header">
    <p class="section-label">El proyecto</p>
    <h2 class="section-title">Voces recuperadas</h2>
    <p class="section-intro">
      Navega las secciones para explorar los textos, conocer a las autoras,
      leer sobre la <em>Revista Azul</em> y consultar el análisis de datos del corpus.
    </p>
  </div>

  <!-- Quick author preview cards for homepage -->
  <div class="authors-container">
    <div class="authors-grid" id="home-grid"></div>
  </div>
</section>

<!-- ══════════════════════════════════════════════ -->
<!-- PAGE: AUTORAS                                  -->
<!-- ══════════════════════════════════════════════ -->
<section id="page-autoras" class="page">
  <div class="section-header">
    <p class="section-label">Antología</p>
    <h2 class="section-title">Las Autoras</h2>
    <p class="section-intro">Selecciona una autora para leer su biografía y sus textos.</p>
  </div>
  <div class="authors-container">
    <div class="authors-grid" id="autoras-grid"></div>
  </div>
</section>

<!-- ══════════════════════════════════════════════ -->
<!-- PAGE: REVISTA AZUL                             -->
<!-- ══════════════════════════════════════════════ -->
<section id="page-revista" class="page">
  <div class="section-header">
    <p class="section-label">Contexto</p>
    <h2 class="section-title">La Revista Azul</h2>
    <p class="section-intro">Historia, relevancia y el lugar de las escritoras en sus páginas.</p>
  </div>
  <div class="revista-container">

    <div class="revista-block">
      <h2>¿Qué fue la <em>Revista Azul</em>?</h2>
      <p>
        La <em>Revista Azul</em> fue una publicación literaria mexicana que circuló entre 1894 y 1896,
        dirigida por Manuel Gutiérrez Nájera y Carlos Díaz Dufoo. Considerada el órgano central del
        modernismo literario en México, el azul de su nombre era un guiño declarado a la estética
        de Rubén Darío: el color del arte, del ideal, del ensueño.
      </p>
      <p>
        Se publicó como suplemento dominical del periódico <em>El Partido Liberal</em> y reunió,
        en sus poco más de dos años de existencia, a las voces más relevantes del modernismo
        hispanoamericano. Sus páginas fueron un espacio de diálogo transnacional: textos originales
        en español coexistían con traducciones del francés, el inglés y el alemán.
      </p>
      <div class="quote-block">
        "El azul es el color del ensueño, de la lejanía, del ideal. Pintamos con él nuestras ilusiones."
        <br>— Manuel Gutiérrez Nájera
      </div>
      <h3>Años de publicación</h3>
      <p>
        La revista apareció entre el 6 de mayo de 1894 y el 1 de octubre de 1896. Fueron en total
        cinco tomos y ciento veintidós números, hasta que la muerte de Gutiérrez Nájera en febrero
        de 1895 marcó el inicio de su declive, aunque la publicación continuó hasta su cierre definitivo.
      </p>
    </div>

    <div class="revista-block">
      <h2>Las escritoras en sus páginas</h2>
      <p>
        Aunque la <em>Revista Azul</em> ha sido estudiada principalmente como espacio de consagración
        masculina —Gutiérrez Nájera, Salvador Díaz Mirón, Justo Sierra, Amado Nervo—,
        sus páginas albergaron también las voces de escritoras que, con mayor o menor continuidad,
        publicaron narrativa, lírica y crónica.
      </p>
      <p>
        Este proyecto de recuperación se propone visibilizar ese "otro azul": el corpus femenino
        de la revista. Las ocho autoras aquí reunidas publicaron en distintos tomos y volúmenes,
        y representan geografías diversas: México, Cuba, España, Venezuela y Rumania.
        Sus géneros, registros y estilos son igualmente variados: del naturalismo de Emilia Pardo Bazán
        al simbolismo de Juana Borrero, del romanticismo tardío de Laura Méndez de Cuenca
        al modernismo costumbrista de María Enriqueta Camarillo.
      </p>
      <h3>Criterios de selección</h3>
      <p>
        Se incluyeron en esta antología todos los textos firmados por mujeres que fue posible
        localizar en los cinco tomos de la <em>Revista Azul</em>. La recopilación se realizó
        consultando la colección digitalizada disponible, y los textos se transcriben siguiendo
        la ortografía y puntuación originales, con mínimas correcciones de erratas evidentes.
      </p>
    </div>

    <div class="revista-block">
      <h2>El modernismo y la escritura femenina</h2>
      <p>
        El modernismo hispanoamericano ha sido históricamente narrado como un movimiento de
        <em>poetas-sacerdotes</em>, casi siempre masculinos. Sin embargo, la participación de
        las escritoras en sus publicaciones fue significativa, aunque frecuentemente marginal
        en términos de cantidad y de reconocimiento crítico posterior.
      </p>
      <p>
        Las autoras recogidas en esta antología muestran que las mujeres no fueron meras
        receptoras pasivas del modernismo, sino agentes activas en su configuración. Juana Borrero,
        por ejemplo, desarrolló un universo poético propio —marcado por la melancolía, el deseo
        y la muerte— antes de morir a los diecinueve años. Laura Méndez de Cuenca exploró
        en el soneto formas de pensamiento filosófico y político que la emparentan con la
        <em>poesía de ideas</em> más que con el esteticismo decorativo del modernismo canónico.
      </p>
      <p>
        Emilia Pardo Bazán, la única escritora española del corpus, publicó en la <em>Revista Azul</em>
        desde España, lo que revela la dimensión transatlántica de la publicación mexicana
        y su lugar central en la cultura letrada del fin de siglo.
      </p>
      <h3>La <em>Revista Azul</em> como espacio transnacional</h3>
      <p>
        La presencia de Carmen Sylva (reina de Rumania), Polita de Lima (Venezuela) y
        Mercedes Matamoros (Cuba) junto a las mexicanas Méndez de Cuenca y Camarillo, y
        las cubanas Borrero y Vázquez, convierte a la <em>Revista Azul</em> en un espacio
        de circulación literaria que desbordó ampliamente las fronteras nacionales.
        Recuperar estos textos es también recuperar una historia de lecturas y conexiones
        que el canon literario ha tendido a invisibilizar.
      </p>
    </div>

    <div class="revista-block">
      <h2>Sobre este proyecto</h2>
      <p>
        <em>El Otro Azul</em> es un proyecto de recuperación y edición crítica de los textos
        femeninos publicados en la <em>Revista Azul</em> (1894–1896). El corpus está compuesto
        por 40 textos de 8 autoras, con un total de 12 piezas de narrativa y 28 poemas.
      </p>
      <p>
        El proyecto se propone no solo la recuperación textual, sino también el análisis de
        las condiciones de publicación, los géneros cultivados, las temáticas recurrentes y
        los vínculos intertextuales que articulan este corpus con la producción literaria
        femenina del fin de siglo en el ámbito hispanoamericano.
      </p>
      <p>
        <strong>Edición:</strong> Diana López
      </p>
    </div>

  </div>
</section>

<!-- ══════════════════════════════════════════════ -->
<!-- PAGE: DATOS                                    -->
<!-- ══════════════════════════════════════════════ -->
<section id="page-datos" class="page">
  <div class="section-header">
    <p class="section-label">Análisis</p>
    <h2 class="section-title">Análisis de Datos</h2>
    <p class="section-intro">Distribución del corpus por autora, género, país y tomos de la <em>Revista Azul</em>.</p>
  </div>
  <div class="datos-container">

    <!-- Row 1: texts per author + genre split -->
    <div class="datos-grid">
      <div class="chart-card">
        <h3>Textos por autora</h3>
        <div class="bar-chart" id="chart-textos"></div>
      </div>
      <div class="chart-card">
        <h3>Distribución por género literario</h3>
        <div class="donut-wrap">
          <svg id="donut-genre" width="130" height="130" viewBox="0 0 130 130"></svg>
          <div class="donut-legend" id="legend-genre"></div>
        </div>
      </div>
    </div>

    <!-- Row 2: country + timeline -->
    <div class="datos-grid">
      <div class="chart-card">
        <h3>Autoras por país</h3>
        <div class="donut-wrap">
          <svg id="donut-country" width="130" height="130" viewBox="0 0 130 130"></svg>
          <div class="donut-legend" id="legend-country"></div>
        </div>
      </div>
      <div class="chart-card">
        <h3>Línea de tiempo de las autoras</h3>
        <div class="timeline" id="chart-timeline"></div>
      </div>
    </div>

    <!-- Row 3: full texts table -->
    <div class="datos-grid single">
      <div class="chart-card">
        <h3>Índice completo — textos y referencias en la <em>Revista Azul</em></h3>
        <div style="overflow-x:auto">
          <table class="vol-table" id="vol-table"></table>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ── FOOTER ─────────────────────────────────── -->
<footer>
  <em>El Otro Azul</em> · Proyecto de recuperación de textos de la <em>Revista Azul</em> (1894–1896) · Edición de Diana López
</footer>

<!-- ══════════════════════════════════════════════ -->
<!-- DATA & LOGIC                                   -->
<!-- ══════════════════════════════════════════════ -->
<script>
// ── DATA ─────────────────────────────────────────
const AUTHORS = [
  {
    id: "carmen-sylva",
    nombre: "Carmen Sylva",
    pais: "Rumania",
    anos: "1843–1916",
    genero: "Narrativa",
    bio: `Isabel de Wied se convirtió en reina consorte de Rumania en 1881 tras su matrimonio con Carlos Hohenzollern. Es conocida mundialmente por su pseudónimo literario Carmen Sylva con el que publicó su vasta obra literaria. Fue una figura sobresaliente que unió la soberanía política con una importante carrera intelectual.\n\nPublicó su obra en francés y alemán. Destacan su novela Ein Gebet / Es klopft: Zwei Novellen (1887), sus libros de cuentos Poveştile unei regine (1906) y Pelesch-Märchen (1882) y su obra lírica Balladen und Romanzen (1851). Su labor como reina se enfocó en promover la enseñanza en Rumania, creó numerosas escuelas y estableció un centro de formación en música, dibujo y pintura para jóvenes. Después de la guerra ruso-turca de 1878 fundó un asilo para ciegos.`,
    textos: [
      {
        titulo: "Cuentos de una reina: La madre de Esteban el Grande",
        tipo: "narrativa",
        ref: "Tomo X",
        contenido: `
          <p>En la Moldavia septentrional, entre Piatra y Folticeni, se ven sobre una montaña cercana a la ribera, las ruinas de una antigua aldea, llamada Niamtz, de la que subsiste poco más que nada. La pequeña ciudad que se extiende al pie de la eminencia, ha sido construida casi enteramente con las piedras de la orgullosa fortaleza.</p>
          <p>En otros tiempos esta plaza tenía fama que alcanzaba lejos y pasaba por inexpugnable cuando servía de residencia a Esteban, el poderoso príncipe de Moldavia. Había dado cincuenta batallas y después de cada victoria, levantaba una iglesia para expresar al cielo su gratitud.</p>
          <p>Ese día un nuevo y ardiente combate se había trabado, y se podían seguir las peripecias desde las almenas de la fortaleza. En la aldea, dos mujeres habían permanecido en espera; una era la esposa de Esteban, la otra, su madre. La joven princesa dejaba correr sus lágrimas por sus rosadas mejillas. No ocurría lo mismo con su madre, que permanecía de pie, inmóvil, los ojos fijos en el horizonte.</p>
          <p>—¡Oh, mi madre, van a matarlo!</p>
          <p>—Esteban obtendrá la victoria antes de que termine el día.</p>
          <p>De repente se escuchó el galope de un caballo y fuertes golpes en la puerta de la fortaleza.</p>
          <p>—¿Quién golpea? —preguntó la anciana sin abrir.</p>
          <p>—Esteban, tu hijo.</p>
          <p>—¡Mi hijo! ¿Quién eres tú, extranjero? Mi hijo nunca vuelve sino victorioso. Mi hijo está lejos de aquí, arrojando a los enemigos. Tú no entrarás; puesto que no sabes vencer, busca una muerte heroica sobre el campo de batalla; entonces seré para ti una madre y ornaré de flores tu sepulcro.</p>
          <p>Esteban bajó un instante la cabeza bajo el peso de la vergüenza, pero en seguida echando hacia atrás su flotante cabellera, sonó su cuerno y lanzó en la sombra sonidos capaces de resucitar a los muertos; su desbandado ejército se ordenó y se estrechó a su alrededor. Con la rapidez del huracán descendió de la montaña lanzándose de nuevo entre los enemigos, los batió y los derrotó por completo.</p>
          <p>De nuevo Esteban llevó el cuerno a la boca y lanzó una alegre fanfarria. Desde que distinguió a su madre, puso un pie en la tierra e inclinándose delante de ella le dijo:</p>
          <p>—Madre mía, es a ti a quien debo esta victoria.</p>
          <p>Y por la primera vez los ojos de esta mujer se humedecieron, estremeciéndose sus labios mientras que el héroe recibía en sus brazos a su joven esposa.</p>
        `
      }
    ]
  },
  {
    id: "emilia-pardo-bazan",
    nombre: "Emilia Pardo Bazán",
    pais: "España",
    anos: "1851–1921",
    genero: "Narrativa",
    bio: `Nació en La Coruña, España el 16 de septiembre de 1851. Como hija única de una familia aristocrática recibió una educación excepcional. Desde temprana edad mostró una fuerte inclinación hacia la literatura; comenzó a leer a los ocho años, compuso sus primeros versos a los nueve y publicó su primer cuento a los quince.\n\nEmilia Pardo Bazán se convirtió en una figura central del naturalismo en España tras publicar La cuestión palpitante (1883). Fundó la revista Nuevo Teatro Crítico y dirigió el proyecto editorial "Biblioteca de la Mujer". A lo largo de su vida escribió cerca de 600 cuentos. Fue la primera mujer en presidir la Sección de Literatura de Madrid (1906) y la primera en ser nombrada catedrática de Literatura Contemporánea en la Universidad Central (1916). En 1908 el rey Alfonso XIII le otorgó el título de Condesa.`,
    textos: [
      {
        titulo: "Mi suicidio",
        tipo: "narrativa",
        ref: "Tomo II, Vol. 23",
        contenido: `
          <p>Muerta ella; tendida sin movimiento en el horrible ataúd de barnizada caoba, ¿qué me restaba ya en el mundo? En ella tenía yo mi luz, mi regocijo, mi ilusión, mi delicia toda, y desaparecer así, de súbito arrebatada en la flor de su juventud, era tanto como decirme: "Pues me amas, sígueme".</p>
          <p>Determinado a realizar mi propósito, quise llevarlo a cabo en aquel mismo aposento donde se deslizaron tantas horas de ventura. Al entrar, me pareció que ella, viva y sonriente, acudía como otras veces a mi encuentro. Allí estaba el amplio sofá donde nos sentábamos, tan juntos como si fuese estrechísimo; allí la butaca donde se aislaba en los cortos instantes de enfado pueril; allí la gorgona de irisado vidrio con las últimas flores, ya secas y pálidas, que su mano dispusiera artísticamente.</p>
          <p>Encendí la lámpara y todas las bujías de los candelabros. Se me ocurrió que allí dentro estarían mis cartas, mis recuerdos. Descerrajé con violencia el primoroso mueblecillo. Solo en uno de los cajoncitos había cartas. A la segunda carta, un indefinible malestar cruzó por mi imaginación. A la cuarta carta, ni sombra de duda pudo quedarme: la carta se había escrito a otro.</p>
          <p>Repasé el resto del paquete. Ninguna de las epístolas que contenía había sido dirigida a mí. Las que yo recibiera y restituyera con religiosidad, probablemente se encontraban incorporadas a la ceniza de la chimenea; y las que como un tesoro <em>ella</em> había conservado siempre señalaban, tan exactamente como la brújula señala el polo, la dirección verdadera del corazón que yo juzgara orientado hacia el mío.</p>
          <p>Lágrimas de rabia escaldaron mis pupilas; me coloqué frente al retrato; empuñé la pistola, alcé el cañón y apuntando fríamente, con los dos tiros, reventé los dos verdes y lumínicos ojos que me fascinaban.</p>
        `
      },
      {
        titulo: "Implacable Kronos",
        tipo: "narrativa",
        ref: "Tomo III, Vol. 11",
        contenido: `
          <p>¡Qué juventud y qué edad madura tan laboriosas las de don Zoilo Terrón! Sin una hora de descanso, vivió don Zoilo no como la ostra —al fin la ostra no trabaja—, sino como la polilla que roe y roe, y no sale de su rincón, no despliega nunca sus alas buscando lo que las mariposas: luz, calor solar y entreabiertas flores.</p>
          <p>Solo cuando se encontró poderoso, dueño de la riqueza que de antemano se propuso obtener, entró a cuentas consigo mismo y advirtió que no había disfrutado nada: "He sido una bestia de carga. Es preciso que yo me case, que tenga familia... y además, que mi mujer me guste mucho... tanto como me gusta Casildita Ramírez, la viuda que vive en el segundo piso".</p>
          <p>Don Zoilo subió a la casa de la linda viuda. Estaba Casildita, cuando recibió la declaración del opulento don Zoilo, más mona que de costumbre, porque la sorpresa y la malicia hacían chispear sus grandes ojos morunos. Oyó las extremosas palabras del vecino, y respondió:</p>
          <p>—A la verdad, lo que usted me propone, para penitencia es atroz. Si tuviese usted diez añitos menos. ¡Pero está usted más gris que las ratas y más desdentado que un serrucho viejo!</p>
          <p>Salió don Zoilo desazonadísimo y, de pronto, se le ocurrió que con dinero se compra también dientes y pelo. El mejor dentista de Madrid lo amuebló espléndidamente con una doble fila de mondados piñones. Después, el peluquero francés hizo pasar su cabellera del gris amarillento al negro de carbón profundo. El ortopédico con una faja-corsé completó la restauración: don Zoilo quedó hecho un petimetre.</p>
          <p>Casildita le contempló con evidente asombro y dijo con un sonreír que era el abrirse de una rosa:</p>
          <p>—El caso es que no puedo complacerle... Hará cosa de quince días que estuvo aquí con la misma pretensión su señor papá, empeñado en pedir mi mano... y después de dar calabazas a una persona más respetable que usted, no es cosa de decirle a usted que sí.</p>
        `
      },
      {
        titulo: "Voz de la sangre",
        tipo: "narrativa",
        ref: "Tomo III, Vol. 18",
        contenido: `
          <p>Si hubo matrimonios felices, pocos tanto como el de Sabino y Leonarda. Conformes en gustos, edad y hacienda, de alegre humor y rebosando de salud; lo único que les faltaba era un hijo.</p>
          <p>Un día alteró la tranquilidad de Leonarda la llegada intempestiva de la única hermana de Leonarda, pálida, desfigurada, llorosa y triste. A los tres o cuatro días salieron juntos la señorita y el matrimonio a pasar temporada en la casa de campo. Lo que se comentó bastante fue que al volver trajesen consigo una niña preciosa, con la cual se volvía loca Leonarda, que aseguraba haberla dado a luz en París.</p>
          <p>La verdad es que cualquiera se enorgullecería de tener una hija como Aurora. Una belleza singular; una inteligencia, una dulzura, una discreción que asombraban; y sobre todo eso que no se define: el atractivo, el encanto, el don de atraer a cuantos la rodeaban.</p>
          <p>Habían pasado años sin que Aurora aceptase los homenajes de ningún pretendiente, cuando apareció un caballero que solicitó hablar a solas con los padres. Sus primeras palabras fueron para decir que allí tenían a un gran culpable, al seductor de la hermana de Leonarda y padre de Aurora, dispuesto a reparar sus faltas, recogiendo a la niña y ofreciéndole su amparo, fortuna y nombre.</p>
          <p>Sabino dijo que dejarían libre a Aurora. El caballero se ocultó detrás de un cortinaje. Entró Aurora, y al preguntarle por el desconocido, respondió que le había parecido la persona más agradable que había visto en su vida.</p>
          <p>—¿Vivirías contenta con él?</p>
          <p>—¡Mira, papá… puede que sí! Esto es un sentimiento, y lo que se siente no se piensa.</p>
          <p>—¡Figúrate que ese señor fuese tu verdadero padre!</p>
          <p>—¿Mi padre? ¡Eso sí que no puedo figurármelo! Como padre, ni le he mirado... ¡ni podría mirarle nunca!</p>
          <p>El desconocido salió del escondite mostrando un rostro color de cera: "Ya sé cuál es mi castigo. Miradas todo lo convertía en oro, yo todo lo convierto en pecado."</p>
          <p>—Tal vez —indicó la compasiva Leonarda—, el atractivo que ejerce usted sobre esa criatura sea voz de la sangre.</p>
          <p>—Si es voz de la sangre, es voz que maldice —respondió el tenorio, saludando y saliendo abrumado por el dolor.</p>
        `
      },
      {
        titulo: "La cabeza a componer",
        tipo: "narrativa",
        ref: "Tomo III, Vol. 26",
        contenido: `
          <p>Érase un hombre a quien le daba malísimos ratos su cabeza: jaquecas nerviosas, aturdimientos, mareos y zumbidos; la aguda sensación de un clavo que le perforaba los sesos; dudas, cavilaciones y agitados pensamientos que le hacían enloquecerse.</p>
          <p>El primer doctor comprobó que todo el cerebro se encontraba en sobreexcitación, y aplicando medicamentos emolientes logró una somnolencia que hizo al paciente mucho bien. Un segundo operador practicó la extirpación de la potencia imaginativa o fantasía. No más ensueños, no más quimeras. Al apagarse los fuegos artificiales de la imaginación, el enfermo se quedó al pronto sosegado. Pero no tardó en notar que la cabeza continuaba descompuesta.</p>
          <p>Lo mismo que su antecesor, el tercer doctor miró y remiró, y vino a decir que lo que debía suprimirse era la razón ergotista y puntiaguda. Sin encomendarse a Dios ni al diablo, practicó la extirpación de la razón y de la facultad discursiva.</p>
          <p>Lo malo fue que pasado algún tiempo reaparecieron las molestias. El cuarto y más ilustre médico, desenvainando los no menos infalibles chirimbolos de bruñido acero, exclamó que de poco servía haber eliminado la imaginación y la razón si dejaban persistir la maldita memoria, causa de todas nuestras penas. Y rebanó diestra y rápidamente la memoria.</p>
          <p>Desde entonces, la cabeza fue una delicia. Ni volvió a doler, ni a calentarse, ni a perturbarse, ni a decir: "aquí me tienes", como que estaba hueca, vacía, limpia del todo. Al ex-enfermo le pusieron de apodo "el idiota", pero él, tendido al sol, respirando el aire puro, durmiendo a ratos, digiriendo, vegetando, era feliz.</p>
        `
      },
      {
        titulo: "La caja de oro",
        tipo: "narrativa",
        ref: "Tomo IV, Vol. 1",
        contenido: `
          <p>Siempre la había visto sobre su mesa, al alcance de su mano bonita, que a veces se entretenía en acariciar la tapa suavemente; pero no me era posible averiguar lo que encerraba aquella caja de filigrana de oro con esmaltes finísimos.</p>
          <p>Me mostré perdidamente enamorado de la dueña, cuando solo lo estaba de la cajita de oro; cortejé en apariencia a una mujer, cuando solo cortejaba un secreto. Un día que algunas fingidas lágrimas acreditaron mis celos, vi a la dueña demudarse, temblar, palidecer, echarme al cuello los brazos, y exclamar por fin:</p>
          <p>—¡Qué no haría yo por ti! Lo has querido, pues que así sea. Ahora mismo verás lo que hay en la caja.</p>
          <p>Apretó un resorte: la tapa se alzó, y divisé en el fondo unas cuantas bolitas del tamaño como guisantes, blanquecinas, secas. Ella, reprimiendo un gemido, dijo solemnemente:</p>
          <p>—Esas píldoras me las vendió un curandero que realizaba curas casi milagrosas. Me aseguró que tomando una al sentirme enferma tenía asegurada la vida. Solo me advirtió que si las apartaba de mí o las enseñaba a alguien perdían su virtud. Te empeñaste en averiguar... lo conseguiste. Para mí vales tú más que la salud y la vida.</p>
          <p>Me quedé frío. Logrando mi empeño, no encontraba dentro de la cajita sino el desencanto de una poderosa hechicería y el cargo de conciencia del daño causado. Al fin cayó en el sepulcro, sin que ni los recursos de la ciencia ni mis cuidados consiguieran salvarla. De cuantas memorias quiso legarme su afecto, solo recogí la caja de oro. Un químico amigo mío analizó las píldoras y se echó a reír:</p>
          <p>—Ya podía usted figurarse que las píldoras eran de miga de pan. El curandero mandó que no las viese nadie… para que a nadie se le ocurriese analizarlas. ¡El maldito análisis lo saca todo!</p>
        `
      },
      {
        titulo: "La cena de Jesucristo",
        tipo: "narrativa",
        ref: "Tomo IV, Vol. 15",
        contenido: `
          <p>Había un hombre lleno de fe, que creía a pies juntillas cuanto nos enseñan la religión y la moral, y sin embargo tenía horas de desaliento porque le parecía que el cielo dista mucho de la tierra. Persuadido de que el claustro está más cerca del cielo, Eudoro entró de novicio en los Carmelitas. Espantó a sus hermanos el fervor de su vida monástica.</p>
          <p>Eudoro se retiró a su casa y se dedicó a una vida activa y modesta. Cierta noche, pasando por una calle desierta, vio a un hombre que se defendía contra tres que ya le tenían acorralado e iban a darle muerte. Reconoció a su enemigo, tuvo un instante de fluctuación, y al final cargó con valor, obligando a los asesinos a emprender precipitada fuga.</p>
          <p>Casi llegaba a la puerta de su casa cuando le salió al camino un mendigo, descalzo, harapiento, encorvado, pidiéndole algo de comer. "Me caigo de necesidad" —gemía. Eudoro, tomándole de la mano: "Vente conmigo —le dijo—, partiremos la cena y dormirás al abrigo".</p>
          <p>Al entrar en el comedor, pudo ver la cara del pobre que le esperaba, sentado a la mesa: ni era viejo, ni feo; en cuanto a edad, representaba unos treinta años, y su rostro oval y su cabellera rubia eran de admirable belleza.</p>
          <p>Así que hubo saciado el hambre, el mendigo tomó el pan que estaba sobre la mesa, lo partió y ofreció la mitad a Eudoro. Al ejecutar tan sencilla acción, Eudoro advirtió una imperceptible claridad que, naciendo en las sienes, rodeaba toda la cabeza del mendigo.</p>
          <p>Eudoro se levantó con ímpetu irresistible y postrando su rostro contra el suelo, vino a besar y a empapar de lágrimas los pies del mendigo, conociendo que era Cristo, Hijo de Dios.</p>
          <p>—Yo vago siempre por las calles —respondió lentamente Cristo—. Cada noche quiero cenar con el que durante el día haya vuelto bien por mal y perdonado de todo corazón a su enemigo. Por eso me acuesto sin cenar tantas noches.</p>
        `
      },
      {
        titulo: "La maga primavera",
        tipo: "narrativa",
        ref: "Tomo IV, Vol. 19",
        contenido: `
          <p>Me tocó en la frente con su varita; desperté y contemplé un espectáculo digno de ser contado por millonésima vez, después de tanto como ya lo han ensalzado los poetas.</p>
          <p>Era el deshielo. De los montes caía derretida y apresurada la nieve. Los gérmenes, estremecidos por la dulce humedad, bullían impacientes y rompían la negra costra de la tierra, vistiéndola de un manto de terciopelo verde. En los vallecillos, los frutales estaban literalmente bordados con flecos de flor. En los jardines, las lilas aspiraban con deleite el aire fresco; las primeras rosas entreabrían su apretado capullo.</p>
          <p>¡Qué de júbilo, qué de rumores y de músicas invisibles en todas partes! El mar, que antes gemía lúgubremente, ahora tenía, en el ruido con que se estrellaba en la playa, cadencias prolongadas e inefables, arrullos como de sirena; su color, antes de plomo, era el azul del zafiro oriental.</p>
          <p>A la puerta de una cabaña vi aparecerse una mocita como de dieciséis años, de corto zagalejo y descalzos pies, con una cántara de barro. De allí a poco, volvió por el mismo caminito, y ya no venía sola: la acompañaba un mocetón atezado y robusto. El brazo de él rodeaba el talle de ella que, encendida en rubor, bajaba los ojos al suelo. El agua de la cántara se vertía gota a gota.</p>
          <p>—También la humanidad, como la naturaleza, resucita al conjuro de la maga —pensé, considerando a la pareja dichosa.</p>
          <p>Y cuando la idea de esta resurrección me sonreía como una promesa de ventura, se evaporaron las visiones, y solo vi el calendario suspendido en la pared. ¡Año todo él de invierno, del invierno de mi existencia! Para mí no existía la maga.</p>
        `
      },
      {
        titulo: "Memento",
        tipo: "narrativa",
        ref: "Tomo V, Vol. 13",
        contenido: `
          <p>El recuerdo más vivaz de mis tiempos estudiantiles —dijo el doctor sonriendo a la evocación—, no es el de varios amorcillos, aventuras y lances parecidos a los que puede contar todo el mundo. Lo que no olvido es la tertulia de mi tía Gabriela, doncella anciana a quien acompañaban todas las tardes tres viejas apolilladas, igualmente aspirantes a la palma sobre el ataúd.</p>
          <p>De las solteronas, Candidita era la más joven, pues no había cumplido los sesenta y tres. Lo que en ella pudo agradar fue su seráfica condición: una alta dosis de credulidad y buena fe. Cuanta paparrucha inverosímil se me antojase inventar, la tragaba Candidita sin esfuerzo.</p>
          <p>A fin de animar la tertulia, se me ocurrió leer en alto versos y novelas románticas. Auditorio semejante no lo ha soñado ningún lector. Las exclamaciones me interrumpían: "Ese pillo ¿se equivoca y toma el veneno? ¡Castigo de Dios!", "¡Al fin le da la puñalada!", "¡Infame!".</p>
          <p>Llegó el plazo en que yo tenía que emprender mi viaje a la corte para cursar el doctorado. Di la noticia a mis solteronas. Mi tía Gabriela, sin perder el compás de la dignidad, se puso temblona. Doña Peregrina manoteó, protestó, bufó y se echó a llorar. Doña Aparición suspiró y dijo: "Un joven de estas prendas, naturalmente, ¡va a lucir en la corte!" Candidita, inmóvil, guardó silencio.</p>
          <p>De repente, en el primer descanso de la escalera, escuché un ahogado sollozo; unos brazos débiles me rodearon el cuello, y una cara fría como la nieve se pegó a mis barbas. Comprendí de golpe... me quedé más volado y compadecido que si viese a mi propia madre de rodillas ante mí.</p>
          <p>—¡Ah, eso sí! Porque la caridad tiene sus límites —Y ahora, que también soy viejo yo, suelo acordarme de Candidita... ¡Pobre mujer!</p>
        `
      },
      {
        titulo: "El palacio de Artasar",
        tipo: "narrativa",
        ref: "Tomo V, Vol. 15",
        contenido: `
          <p>Después de Salomón, el rey más poderoso y opulento de la tierra fue, sin duda, Artasar, descendiente directo de uno de aquellos tres magos que vinieron a postrarse en el establo de Belén, guiados por la luz de una estrella misteriosa.</p>
          <p>Artasar ansiaba construir un palacio nunca visto, que eclipsase al que Salomón edificó. Convocó a los más famosos arquitectos de su reino y de los vecinos, pero en los ojos de Artasar ninguno de ellos encontró gracia. Cuando ya desesperaba, le pidió audiencia un hombre anciano demacrado, de larga barba, de humilde aspecto, que traía bajo el brazo un rollo de papel. Apenas el monarca fijó los ojos en el plano, batió palmas saltando de júbilo: aquello era su sueño interpretado por un mágico que leía en su mente.</p>
          <p>Al cabo de un año, plazo fijado por el arquitecto, Artasar quiso ver las obras. Grande fue su sorpresa, fuerte su cólera, al no advertir por ninguna parte señales de jardines ni de palacio. Mandó que trajesen al arquitecto, con propósito de hacerle desollar. El viejo se presentó tan humilde como el primer día y dio esta respuesta extraña:</p>
          <p>—El palacio que deseabas está construido, ¡oh rey!, y si quieres venir conmigo, te lo voy a mostrar en seguida.</p>
          <p>Salieron juntos y pronto llegaron a las orillas de un inmenso lago natural. El sol se ponía; el firmamento aparecía rojo, esplendente. Y el arquitecto, tomando de la mano a Artasar, le dijo:</p>
          <p>—Los tesoros que me has confiado, los he repartido entre los miserables. Mas no por eso he dejado de alzarte el palacio. Mira… ¿no lo ves? Allí lo tienes, ¡en el cielo se levanta ahora tu palacio!</p>
          <p>Y Artasar miró, y vio efectivamente de entre las nubes de grana surgir un maravilloso edificio sobre columnas de plata, bronce y alabastro. Y Artasar, transportado, se arrodilló a los pies del arquitecto y los besó, con el alma inundada de gozo.</p>
        `
      }
    ]
  },
  {
    id: "esther-lucila-vazquez",
    nombre: "Esther Lucila Vázquez",
    pais: "Cuba",
    anos: "1860–1906",
    genero: "Lírica",
    bio: `Fue una poeta cubana cuyos sonetos destacan por su forma clásica y el tratamiento modernista de sus temas, como el ansia de la inmortalidad y el ideal de belleza. Parte de su obra poética fue recuperada en la antología Poetisas cubanas (1985) por Ediciones Letras Cubanas, en la que se incluyen los poemas "Vespertino", "Inmortal", "Perlas", "A la poesía" y "Rosas".\n\nSu contexto histórico se vio marcado por las dos grandes guerras por la independencia cubana: la Guerra de los Diez Años (1868-1878) y la Guerra de Independencia (1895-1898). Con la llegada del modernismo en los años ochenta, las poetas cubanas recibieron cierta libertad creativa. Algunas empezaron a publicar frecuentemente en revistas como El Fígaro.`,
    textos: [
      {
        titulo: "El buitre herido",
        tipo: "lirica",
        ref: "Tomo III, Vol. 9",
        contenido: `
          <p style="font-size:0.85rem;color:var(--muted);margin-bottom:1rem;">(del inglés de Ana C. Linch)</p>
          <div class="poem-stanza">
            El soberano buitre estaba solo,<br>
            de las ruinas como único señor,<br>
            y de Egipto las tétricas pirámides<br>
            sombreaban del desierto la extensión.<br><br>
            En el ave orgullosa la mirada<br>
            detuvo, breve instante, el cazador,<br>
            y en la callada soledad, vibrante<br>
            la bala, al elevarse resonó.<br><br>
            En el mullido pecho tuvo entrada,<br>
            cerca del indomable corazón,<br>
            y la encendida sangre, gota a gota,<br>
            a la amarilla arena descendió.<br><br>
            Sin conmoverse a la mortal herida,<br>
            sin exhalar un grito de dolor,<br>
            el buitre desplegó las luengas alas<br>
            y, sereno, en el aire se tendió.<br><br>
            Hacia el éter azul alzando el vuelo,<br>
            sin detener un punto la ascensión,<br>
            tranquilo se alejaba de la tierra,<br>
            y al fin en lontananza se perdió.
          </div>
          <div class="poem-stanza">
            ¡Oh, corazón herido! ¡alma doliente!<br>
            no pliegues, no, las voladoras alas,<br>
            mirando en torno las siniestras sombras<br>
            de tus desvanecidas esperanzas.<br><br>
            El vuelo tiende, como hiciera el ave,<br>
            y la llanura celestial alcanza,<br>
            donde no llegan dardos de la suerte,<br>
            donde se goza de apacible calma.<br><br>
            ¡Levántate! Aunque brame la tormenta,<br>
            ascienda lejos de la vida amarga,<br>
            a donde hay puro y sosegado ambiente,<br>
            donde hay un cielo que te brinda entrada.<br><br>
            Y como se borró la oscura forma<br>
            en la fúlgida luz de la mañana,<br>
            desaparecerán tus hondas penas,<br>
            si en la infinita claridad te bañas.
          </div>
        `
      }
    ]
  },
  {
    id: "juana-borrero",
    nombre: "Juana Borrero",
    pais: "Cuba",
    anos: "1877–1896",
    genero: "Lírica",
    bio: `Fue una destacada escritora y pintora cubana, considerada un prodigio de las letras en su país. Nació en un entorno familiar con una fuerte presencia intelectual; su padre, Esteban Borrero, médico y poeta, fomentó su formación artística desde temprana edad. Juana Borrero falleció con tan solo diecinueve años.\n\nComenzó a escribir versos a los siete años, aunque durante su vida solo llegó a publicar un libro titulado Rimas (1895); el resto de su obra quedó dispersa en revistas como La Habana elegante, El Fígaro y Revista de Cayo Hueso. Su obra se caracteriza por paisajes interiores, una sensibilidad melancólica y una lucha entre el sueño y la vigilia. Además de su producción literaria, Borrero fue una pintora sobresaliente. Fue apodada la "Virgen triste" por el poeta Julián del Casal.`,
    textos: [
      {
        titulo: "Los astros",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 24",
        contenido: `
          <div class="poem-stanza">
            En la callada noche, cuando la sombra extiende<br>
            sobre la tierra muda su velo misterioso,<br>
            y arriba, en las alturas del éter anchuroso<br>
            sembrado de luceros el firmamento esplende.<br><br>
            Mi alma soñadora que al infinito asciende,<br>
            escucha, sumergida en éxtasis dichoso,<br>
            hablar a las estrellas su idioma cadencioso<br>
            tan dulce, que tan solo mi espíritu lo entiende.<br><br>
            A mis oídos llega desvanecido y flébil<br>
            el eco de esas voces como el murmullo débil<br>
            que una dulzura vaga, indefinible encierra.<br><br>
            De su prisión terrena mi espíritu se evade,<br>
            y un inefable goce mi corazón invade<br>
            sintiéndome muy lejos de la mezquina tierra.
          </div>
        `
      },
      {
        titulo: "En el templo",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 24",
        contenido: `
          <div class="poem-stanza">
            Se llena de creyentes el templo solitario<br>
            y a los acordes graves del órgano sonoro,<br>
            se mezclan en la atmósfera serena del santuario<br>
            las voces cristalinas que vibran en el coro.<br><br>
            Entre las blancas nubes que arroja el incensario<br>
            miro con las pupilas nubladas por el lloro,<br>
            que el sacerdote humilde de pie junto al sagrario<br>
            entre las manos puras eleva el cáliz de oro.<br><br>
            Y así como el incienso que ante la imagen flota<br>
            impregna de sutiles perfumes el ambiente,<br>
            perfuma tu recuerdo mi mente visionaria.<br><br>
            Y de mis labios trémulos y suplicantes brota<br>
            tu nombre idolatrado que vibra dulcemente<br>
            mezclado con las frases que forman mi plegaria.
          </div>
        `
      },
      {
        titulo: "Rêve",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 24",
        contenido: `
          <div class="poem-stanza">
            Debe su dulce voz ser persuasiva<br>
            y soñadora y triste su mirada;<br>
            debe tener la frente pensativa<br>
            por un halo de ensueños circundada.<br><br>
            Su alma genial, cual pálida cautiva,<br>
            de un astro esplendoroso desterrada,<br>
            sueña con una nube fugitiva<br>
            y con el traje de crespón de un hada.<br><br>
            Cuando la ronda azul de los delirios<br>
            disipa sus nostálgicos martirios<br>
            borrando del pesar la oscura huella.<br><br>
            Él se acuerda en la noche silenciosa<br>
            de aquella virgencita misteriosa<br>
            que dejó abandonada en una estrella.
          </div>
        `
      },
      {
        titulo: "Vorrei Morir",
        tipo: "lirica",
        ref: "Tomo V, Vol. 7",
        contenido: `
          <div class="poem-stanza">
            Quiero morir cuando al nacer la aurora<br>
            su clara lumbre sobre el mundo vierte,<br>
            cuando por vez postrera me despierte<br>
            la caricia del sol abrazadora.<br><br>
            Quiero, al finalizar mi última hora,<br>
            cuando me invada el hielo de la muerte,<br>
            sentir que se doblega el cuerpo inerte<br>
            inundado de luz deslumbradora.<br><br>
            ¡Morir entonces! Cuando el sol naciente<br>
            con su fecundo resplandor ahuyente<br>
            de la fúnebre noche la tristeza.<br><br>
            Cuando radiante de hermosura y vida,<br>
            al cerrarme los ojos, me despida<br>
            con un grito de amor ¡Naturaleza!
          </div>
        `
      },
      {
        titulo: "Sol poniente",
        tipo: "lirica",
        ref: "Tomo V, Vol. 11",
        contenido: `
          <div class="poem-stanza">
            Con el alma cubierta de luto<br>
            te escribo estos versos,<br>
            que vuelan errantes buscando el albergue<br>
            que les brinda piadoso tu pecho.<br><br>
            Mientras surge en el fondo del alma<br>
            como un rayo de sol tu recuerdo.<br><br>
            ¡Fúlgidas quimeras<br>
            que nutrí con mi llanto de fuego,<br>
            esperanzas de dicha, más dulces<br>
            que la hermosa promesa del Cielo!<br><br>
            El ocaso distante se enciende<br>
            con rojizos fulgores de incendio<br>
            y un último rayo del sol moribundo<br>
            que atraviesa un celaje de fuego,<br>
            tenue se difunde<br>
            en la gasa opalina del cielo.<br><br>
            Contemplando la luz del poniente<br>
            me parece mirar tus cabellos<br>
            y surge a mis ojos tu imagen, radiosa<br>
            como el hada que inspira mis ensueños.
          </div>
        `
      },
      {
        titulo: "Rondel",
        tipo: "lirica",
        ref: "Tomo V, Vol. 13",
        contenido: `
          <div class="poem-stanza">
            La virgen de noble frente<br>
            y de mirada sombría,<br>
            evocaba noche y día<br>
            la memoria del ausente.<br><br>
            A veces en su agonía<br>
            lo llamaba tiernamente,<br>
            la virgen de noble frente<br>
            y de mirada sombría.<br><br>
            Y al ver su inútil porfía<br>
            derramaba lloro ardiente,<br>
            la virgen de noble frente<br>
            y de mirada sombría.
          </div>
        `
      },
      {
        titulo: "Himno de vida",
        tipo: "lirica",
        ref: "Tomo V, Vol. 19",
        contenido: `
          <div class="poem-stanza">
            En el misterio de la selva hojosa<br>
            extiende Amor su imperio dominante,<br>
            allí al posarse en el clavel fragante<br>
            se enciende de placer la mariposa.<br><br>
            Allí la abeja ardiente y afanosa<br>
            liba la miel del lirio palpitante,<br>
            y el aura lleva el polen fecundante<br>
            al cáliz virgen de la fresca rosa.<br><br>
            ¿Oís ese rumor que, de la umbría,<br>
            como vago concierto, se levanta<br>
            cuando aparece el luminar del día?<br><br>
            ¡Es que a su luz enciéndese Natura<br>
            y en dulce voz su desposorio canta<br>
            con el astro que vívido fulgura!
          </div>
        `
      }
    ]
  },
  {
    id: "laura-mendez-de-cuenca",
    nombre: "Laura Méndez de Cuenca",
    pais: "México",
    anos: "1853–1928",
    genero: "Lírica",
    bio: `Fue una figura excepcional en la historia literaria de México, considerada como una de las escritoras más importantes del país a finales del siglo XIX y principios del XX. Destacó como poeta, narradora, pedagoga, editora y periodista. Se graduó de la Escuela de Artes y Oficios para mujeres en 1873 y del Conservatorio de Música en 1875.\n\nDedicó una gran parte de su vida a la educación y fue enviada por el gobierno mexicano al extranjero para estudiar distintos sistemas educativos. Llegó a ser miembro del Consejo Superior de Educación Pública. Su obra literaria abarca poesía, cuento, novela, ensayo y crónicas de viaje; fue comparada con Sor Juana Inés de la Cruz por su gran talento lírico. Entre su obra más destacada está la novela El espejo de Amarilis (1902) y la colección de cuentos Simplezas (1910). Cofundó y editó la Revista Hispanoamericana, publicación bilingüe de gran alcance.`,
    textos: [
      {
        titulo: "Fe",
        tipo: "lirica",
        ref: "Tomo I, Vol. 11",
        contenido: `
          <div class="poem-stanza">
            Cuando es albor la inútil existencia<br>
            y el corazón al goce está despierto,<br>
            con la pompa del sol en el desierto<br>
            iluminas del niño la conciencia.<br><br>
            Mas váse con los años la inocencia,<br>
            tórnase estepa el cultivado huerto,<br>
            y en la pendiente del abismo incierto<br>
            no concedes al hombre tu presencia.<br><br>
            Mito de la cobarde fantasía,<br>
            febril espectro del delirio insano<br>
            que finge sombras en mitad del día.<br><br>
            Del no ser vuelve al insondable arcano,<br>
            ¡Que en tanto pones tasa a la alegría<br>
            en nada alivias el dolor humano!
          </div>
        `
      },
      {
        titulo: "Cuarto Menguante",
        tipo: "lirica",
        ref: "Tomo I, Vol. 15",
        contenido: `
          <div class="poem-stanza">
            Azota el viento la callejuela;<br>
            junto a la cuna la esposa vela,<br>
            entretenida con su labor;<br>
            y al otro extremo del gabinete,<br>
            puesto de codos en el bufete,<br>
            con su fastidio lucha el señor.<br><br>
            Ella recuerda su vida toda:<br>
            la incomparable noche de boda,<br>
            la fugitiva luna de miel;<br>
            mas él se aburre de aquella calma,<br>
            de aquella vida quieta del alma.<br>
            Ella suspira; bosteza él.
          </div>
        `
      },
      {
        titulo: "Mesalina",
        tipo: "lirica",
        ref: "Tomo I, Vol. 20",
        contenido: `
          <div class="poem-stanza">
            Tus ojos vuelven a los pasados días,<br>
            ¡Oh, mujer! y repasa en la memoria,<br>
            el tropel de culpadas alegrías<br>
            que componen el libro de tu historia.<br><br>
            No intentes disculparte: si amargura<br>
            en vasos de oro tu destino escancia,<br>
            ¿Quién si no tú rasgó la vestidura<br>
            para acortar al vicio la distancia?<br><br>
            Tú, con despego criminal que aterra,<br>
            apartas tu regazo al pequeñuelo:<br>
            ¡Pobres hijos que arrojas en la tierra<br>
            a la dudosa protección del cielo!
          </div>
        `
      },
      {
        titulo: "Tentación",
        tipo: "lirica",
        ref: "Tomo II, Vol. 2",
        contenido: `
          <div class="poem-stanza">
            El Tetrarca magnífico de Oriente<br>
            de amor habla a la virgen Idumea,<br>
            al borde de un torrente<br>
            de la feraz Judea:<br><br>
            "Pastora, escucha de mi amor el ruego;<br>
            oye latir dentro del pecho mío<br>
            un corazón de fuego,<br>
            aterido de frío".<br><br>
            Vente conmigo; que me den tus ojos<br>
            azules de turquesa, luz y abrigo:<br>
            te lo pido de hinojos,<br>
            vente, vente conmigo.
          </div>
        `
      },
      {
        titulo: "Nieblas",
        tipo: "lirica",
        ref: "Tomo II, Vol. 6",
        contenido: `
          <div class="poem-stanza">
            En el alma la queja comprimida<br>
            y henchidos corazón y pensamiento<br>
            del congojoso tedio de la vida.<br>
            Así te espero, humano sufrimiento.<br><br>
            ¡Ay! ni cedes, ni menguas, ni te paras,<br>
            ¡Alerta siempre y sin cesar hambriento!<br>
            Pues ni en flaqueza femenil reparas,<br>
            no vaciles, que altiva y arrogante<br>
            despreciaré los golpes que preparas.
          </div>
        `
      },
      {
        titulo: "¡Oh, corazón!",
        tipo: "lirica",
        ref: "Tomo II, Vol. 11",
        contenido: `
          <div class="poem-stanza">
            ¡Oh, corazón! ¿qué vales ni que puedes<br>
            de este vivir en el artero abismo,<br>
            si siendo presa de mundanas redes<br>
            eres siervo y señor a un tiempo mismo?<br><br>
            ¿Eres luz y verdad? ¿Eres arcilla?<br>
            Guardas lo eterno, o lo mudable y breve.<br>
            ¿Qué vínculo, qué lazo hay en tu esencia<br>
            entre el yo pensador y el sentimiento?<br><br>
            Penumbra o claridad, verdad o mito,<br>
            vives, palpitas, gozas y padeces;<br>
            por el amor confiesas lo infinito,<br>
            revelas el Infierno si aborreces.
          </div>
        `
      },
      {
        titulo: "Sombras",
        tipo: "lirica",
        ref: "Tomo II, Vol. 22",
        contenido: `
          <div class="poem-stanza">
            ¡Ay!, que el llanto estancado en la pupila<br>
            hallar no puede apetecido cauce;<br>
            y me doblo al pensar que me aniquila<br>
            como la rama del doliente sauce.<br><br>
            Véanse en caleidoscópico miraje<br>
            las dichas muertas, las promesas vanas;<br>
            la juventud que se apercibe al viaje<br>
            se lleva sueños y me deja canas.
          </div>
        `
      },
      {
        titulo: "Salve",
        tipo: "lirica",
        ref: "Tomo III, Vol. 22",
        contenido: `
          <div class="poem-stanza">
            ¡Qué triste enero, pálido y frío!<br>
            El viento zumba, cuaja el rocío<br>
            que brilla en perlas en el maizal.<br><br>
            Adiós ardiente noche de junio,<br>
            vierte hoy sus galas el plenilunio<br>
            en luz de nieve por la ciudad.<br><br>
            Salve viajera de lontananza,<br>
            consoladora, dulce esperanza,<br>
            salve si vienes a mí esta vez.<br><br>
            Cuando ya el seno de amor no salta,<br>
            ¡Para el descanso qué poco falta!<br>
            ¡Qué poco falta para morir!
          </div>
        `
      },
      {
        titulo: "Lágrimas",
        tipo: "lirica",
        ref: "Tomo III, Vol. 4",
        contenido: `
          <div class="poem-stanza">
            No el llanto acerbo que mis ojos riega<br>
            mires rodar con calma indiferente,<br>
            pues que si helado a mis pupilas llega<br>
            brota del corazón rojo y candente.<br><br>
            Cuando en el yermo de la triste vida<br>
            no hay un dolor que el corazón no guarde,<br>
            la muerta fe del alma adolorida<br>
            habla más que una lágrima cobarde.
          </div>
        `
      },
      {
        titulo: "En el álbum de María",
        tipo: "lirica",
        ref: "Tomo III, Vol. 24",
        contenido: `
          <div class="poem-stanza">
            Rosas de Chipre entretejed, poetas<br>
            en el altar de la mujer altiva;<br>
            y ante la niña casta y pensativa<br>
            guardad la lira y deshojad violetas.
          </div>
        `
      }
    ]
  },
  {
    id: "maria-enriqueta-camarillo",
    nombre: "María Enriqueta Camarillo",
    pais: "México",
    anos: "1872–1968",
    genero: "Narrativa y Lírica",
    bio: `Fue una artista y escritora mexicana; destacó principalmente como poeta, novelista y cuentista, aunque su talento se extendió a la música y las artes plásticas. Originaria de Veracruz, Camarillo inició su formación artística en el Conservatorio Nacional de Música y obtuvo el diploma de Maestra de Piano, con el que llegó a desempeñarse como concertista.\n\nSu carrera literaria comenzó en 1902 cuando se publicó su primer libro de poesía Las consecuencias de un sueño. Entre su vasta obra literaria resaltan los libros escolares Rosas de la infancia (1914-1916), premiados en la Exposición Iberoamericana de Sevilla; su poemario Rumores de mi huerto (1908) y su novela El secreto (1922). Fue nominada al Premio Nobel de Literatura en 1951. Asimismo, fue nombrada Socia Correspondiente de la Real Academia Hispanoamericana de Ciencias y Artes de Cádiz y recibió altas condecoraciones de España, como el Lazo de Isabel la Católica y la Gran Cruz de Alfonso X, El Sabio.`,
    textos: [
      {
        titulo: "El maestro Floriani",
        tipo: "narrativa",
        ref: "Tomo II, Vol. 11",
        contenido: `
          <p>Es triste el invierno, pero cuando al calor de la chimenea se reúnen los amigos para pasar las veladas en animada plática, se olvidan los rigores de la nieve que afuera cae monótonamente. Una de tantas noches, uno de los concurrentes dijo: "A mi vez les contaré una historia, y bien cierta pues es nada menos que un episodio de mi vida".</p>
          <p>—Hace ya tanto tiempo y, sin embargo, lo recuerdo cual si fuese ahora mismo. Aquella clase de piano que me traía loco, la extraña influencia que llegó a ejercer sobre mi ánimo, el viejo conservatorio que casi derruido por el peso de los años se ostentaba medio sombrío en el fondo de aquella callejuela solitaria; y sobre todo, aquellas dulces veladas transcurridas al lado del maestro Floriani.</p>
          <p>Aquel Floriani era un Apolo. De haber sido yo pintor le habría rogado que me sirviese de modelo. Era alto, escultórico, la frente noble y espaciosa, la nariz griega, la boca regular medio escondida bajo el negrísimo bigote, los magníficos ojos, negros también, rasgados, melancólicos, apasionados, soñadores. La mirada de aquellos ojos ardientes se inspiraba en la música y bebía en rayos y fulgores las ondas sonoras.</p>
          <p>El maestro no se concretaba solo a enseñarnos a mover los dedos con más o menos precisión. Su profundo estudio había revelado que las almas elevadas interpretan de mejor manera las grandes obras clásicas; y basado en ese lógico principio, educábamos también el alma, leyéndonos para ello a Dante, a Homero, a Virgilio y al Tasso.</p>
          <p>Una noche fría y lluviosa llegué al conservatorio. ¿Qué sucede? les pregunté asombrado a mis compañeros. "Nada, casi nada, me contestó uno con voz dolorosamente sarcástica; poca cosa: que el maestro Floriani parte para Francia, donde le llaman para dar una clase en el conservatorio de París, y nos deja".</p>
          <p>Esa noche desplegó su fantasía de un modo brillante y deslumbrador. Habló como pocas veces había hablado. Y a instancias nuestras se sentó al piano y tocó a cada uno lo que quiso; yo casi ebrio por el exceso de tantas impresiones, bruscamente me levanté de mi asiento, llegué al piano y, abrazando al maestro con arrebato irresistible, suspiré más que dije estas palabras: "El piano ha muerto para mí; jamás volveré a tocarlo".</p>
          <p>Hoy ya soy viejo. Cuando escucho a mi pequeña Lili que con sus deditos color de rosa intenta modular en el piano algún cantarcillo, una oleada del pasado viene a orear mi cansado cerebro, y olvidando por un momento las realidades de la vida, me echo a soñar como entonces. De pronto, la impresión producida en mi frente por un beso tibio me saca de mi silencio. Es mi pequeñita Lili que me pregunta con dulce curiosidad: "Papá, ¿quién es Floriani?" —Floriani eres tú ahora, vida mía, dame otro beso.</p>
        `
      },
      {
        titulo: "Danza",
        tipo: "lirica",
        ref: "Tomo II, Vol. 13",
        contenido: `
          <div class="poem-stanza">
            Llora el violín gimiendo entristecido;<br>
            y de su amarga pena,<br>
            la flauta alegre con desdén se ríe:<br>
            ¿Qué le importa esa queja?<br><br>
            Y al compás de la música, danzando<br>
            se cruzan las parejas.<br>
            Ya se tejen febriles, ya se enlazan,<br>
            ya forman la cadena;<br>
            ya se mecen con lánguido abandono<br>
            como espigas que ondean.<br><br>
            ¡Siga la danza! ¡Que las almas vibren<br>
            como vibran las cuerdas!<br>
            Y al ritmo de las notas, van y vienen<br>
            girando las parejas;<br>
            arrastradas en loco torbellino,<br>
            pisando flores muertas.
          </div>
        `
      },
      {
        titulo: "Hastío",
        tipo: "lirica",
        ref: "Tomo II, Vol. 16",
        contenido: `
          <div class="poem-stanza">
            Junto al borde musgoso del estanque,<br>
            donde crecen los juncos y la yedra,<br>
            la barca llena de hojas amarillas<br>
            dormita con las ondas que la besan.<br><br>
            Es el invierno, cuando el Bóreas loco<br>
            arrastra con furor las hojas secas;<br>
            cuando mueren las aves dentro del nido,<br>
            y los nidos destroza la tormenta.<br><br>
            ¡Qué tarde tan helada! con sus brumas<br>
            mi amor ya moribundo se congela,<br>
            quisiera darle vida con mi aliento,<br>
            ¡Pero el Bóreas lo mata y se lo lleva!
          </div>
        `
      },
      {
        titulo: "Alborada de mayo",
        tipo: "lirica",
        ref: "Tomo III, Vol. 9",
        contenido: `
          <div class="poem-stanza">
            El alegre y pequeño campanario<br>
            parece estar envuelto en suave gasa,<br>
            ¡Es que amanece! todo está escondido<br>
            atrás de la bruma blanca.<br><br>
            Y en las huertas de dulces pomarrosas,<br>
            subidos en la tapia,<br>
            cantan los gallos en alegre coro<br>
            ¡Himnos de amor a la gentil mañana!<br><br>
            ¡Oh, dulce dueño de mi amor, aún duermes!<br>
            ¡Aún velados están por las pestañas<br>
            esos ojos que alumbran de mi vida<br>
            la sonriente mañana!
          </div>
        `
      },
      {
        titulo: "Hojas",
        tipo: "lirica",
        ref: "Tomo III, Vol. 19",
        contenido: `
          <div class="poem-stanza">
            Sopló el viento… ¡y cayeron en el río!<br>
            ¡Miradlas! van en pos de otras orillas;<br>
            esas horas oscuras, son barquillas<br>
            cargadas de rocío.<br><br>
            Cada hoja lleva en su color su historia:<br>
            las hojas de laurel encierran gloria;<br>
            las hojas de ciprés y cinerarias<br>
            las hojas funerarias;<br>
            las hojas del sauz son el olvido.
          </div>
        `
      },
      {
        titulo: "LIED",
        tipo: "lirica",
        ref: "Tomo III, Vol. 23",
        contenido: `
          <div class="poem-stanza">
            Despierta y canta el día,<br>
            y el sol, desde los cielos,<br>
            acaricia la tierra<br>
            con sus rayos de fuego.<br><br>
            Al oído acarician<br>
            con su rumor tan tierno,<br>
            las frases amorosas,<br>
            la música y los versos.<br><br>
            Y aleteando en las sienes<br>
            mi triste pensamiento<br>
            acaricia tu nombre<br>
            unido a tu recuerdo.
          </div>
        `
      },
      {
        titulo: "Invernal",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 10",
        contenido: `
          <div class="poem-stanza">
            ¡No te duermas! El viento de diciembre<br>
            no rozará con su ala<br>
            tu frente soñadora y pensativa,<br>
            ya cerré la ventana.<br><br>
            Mas el cierzo y la nieve no penetran<br>
            donde mora el amor, a donde se ama;<br>
            ¿Dices que hay nieve hasta en los blandos nidos?<br>
            ¡Pero eso es en los nidos, no en las almas!<br><br>
            Cuando me muera entonces piensa mucho<br>
            al derramar tus lágrimas,<br>
            en los nidos sin cantos y sin aves<br>
            que ruedan por el suelo entre la escarcha.
          </div>
        `
      },
      {
        titulo: "Sin alas",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 17",
        contenido: `
          <div class="poem-stanza">
            Yo no envidio las alas de las aves<br>
            que llegan en su vuelo al firmamento;<br>
            ni tampoco las velas de las naves<br>
            que son alas batidas por el viento.<br><br>
            Ala ninguna que levante el vuelo<br>
            por bosques o por mares<br>
            envidio que me lleve hasta sus lares,<br>
            para oír tu cantar o tu lamento,<br>
            ¡me basta nada más mi pensamiento!
          </div>
        `
      },
      {
        titulo: "Mi carta",
        tipo: "lirica",
        ref: "Tomo IV, Vol. 26",
        contenido: `
          <div class="poem-stanza">
            Y la cierro; y en el sobre<br>
            donde la guardo, sonriendo,<br>
            le pongo estas dulces frases:<br>
            "En su país, a mi dueño".<br><br>
            Y después, enternecida,<br>
            la miro, le doy un beso,<br>
            la pongo en mi alma un instante<br>
            ¡y se la doy al cartero!<br><br>
            ¡Oh, mi carta! vuela errante<br>
            por ignorados desiertos;<br>
            allá va, cruzando montes<br>
            y sendas y vericuetos.
          </div>
        `
      },
      {
        titulo: "A unos ojos",
        tipo: "lirica",
        ref: "Tomo V, Vol. 23",
        contenido: `
          <div class="poem-stanza">
            ¡Tristes ojos errabundos<br>
            que exploran lejanos mundos!<br>
            Aunque ellos estén abiertos<br>
            no me parecen despiertos.<br><br>
            Los miro siempre abismados,<br>
            y si se cierran, cansados,<br>
            me parece que están muertos.<br><br>
            Son tus ojos que semejan<br>
            grandes gotas de rocío<br>
            que de algún cáliz rodaron.<br>
            Estrellas que a ti bajaron<br>
            ¡En una noche de estío!
          </div>
        `
      }
    ]
  },
  {
    id: "mercedes-matamoros",
    nombre: "Mercedes Matamoros",
    pais: "Cuba",
    anos: "1851–1906",
    genero: "Lírica",
    bio: `Nació en Cienfuegos, Cuba el 13 de marzo de 1851. Comenzó su carrera como escritora a los dieciséis años cuando publicó sus primeros folletines, sonetos y crónicas costumbristas en la prensa de La Habana. En 1878 se consagró no solo como poeta, sino también como una traductora consolidada de figuras como Lord Byron, Thomas Moore, André Chénier y Goethe.\n\nEntre sus obras más destacadas se encuentran Poesías completas (1892) y El último amor de Safo (1902), esta última antología sobresale por su lírica, en la que explora el deseo femenino con una franqueza inusual para su época. Asimismo, Mercedes Matamoros ejerció como maestra después de las dificultades financieras que experimentó su familia.`,
    textos: [
      {
        titulo: "Himno matinal",
        tipo: "lirica",
        ref: "Tomo II, Vol. 12",
        contenido: `
          <div class="poem-stanza">
            Se oye el rumor suavísimo y lejano<br>
            de un mar que exhala endechas gemidoras,<br>
            y las cañas de azúcar cimbradoras<br>
            rompen en dulce música en el llano.<br><br>
            Sus hojas mueven el plátano lozano,<br>
            se estremecen las palmas vibradoras;<br>
            el gallo anuncia las primeras horas,<br>
            bulle el torrente bajo el cielo indiano.<br><br>
            Abre el aura cantando armoniosa<br>
            de blancas nubes los flotantes linos,<br>
            y al asomar el Sol la faz gloriosa.<br><br>
            Ante el himno de amor que lo saluda,<br>
            cual ave herida que olvidó sus trinos<br>
            solo mi alma permanece muda.
          </div>
        `
      }
    ]
  },
  {
    id: "polita-de-lima",
    nombre: "Polita de Lima",
    pais: "Venezuela",
    anos: "1869–1944",
    genero: "Narrativa",
    bio: `Fue una de las figuras intelectuales y culturales más influyentes de Venezuela. Su educación se formó en el colegio Welgelegen de Curazao, donde se ganó el apodo de "mi granito de oro" por su brillantez académica. Su trayectoria profesional abarca la literatura, el periodismo y el activismo cívico.\n\nPolita de Lima fundó y dirigió las revistas El Chistoso (1894), Flores y Letras (1894) y Médanos y Leyendas (1920). Como escritora publicó los poemarios Átomos (1897), Sueños rítmicos (1917) y Poemas (1924). Destaca también su novela Ladrón de sal (1938) y su obra teatral Agar (1907). En 1913 fue proclamada Princesa del Parnaso Venezolano por votación popular. En 1890 fundó la Sociedad Alegría, grupo que buscaba animar a la juventud y crear preocupación por la cultura. Fue galardonada con la Medalla de Instrucción Pública y la Orden del Busto del Libertador.`,
    textos: [
      {
        titulo: "Un cuento a Mina",
        tipo: "narrativa",
        ref: "Tomo V, Vol. 9",
        contenido: `
          <p>¿Qué escriba un cuento a lo Catulle Mendés, como aquel del "ala del ángel", símbolo de la inocencia que remonta el vuelo? ¿Qué te dedique una narración fantástica a lo Rubén Darío, donde viaje un príncipe azul en su carro de oro en pos de la esquiva reina Esperanza?</p>
          <p>¡Ah, cabecita de alondra! Es que no sabes tú que esas líneas que te parecen tan sencillas son obra de una imaginación poderosa; es que no es fácil como te supones trazar esos cuadritos de medias tintas.</p>
          <p>Mas, ¿cómo esquivarme, negándome a dar cumplida satisfacción a tu deseo, si has estudiado con especial constancia tu lección de violoncello y me exiges el premio, apoyada tu cabeza negra en la cabeza de tu instrumento favorito? Óyelo, pues, hermanita querida.</p>
          <p>¡Oh, y que era un gran músico! y el violoncello en sus manos parecía una urna de notas nunca oídas. Y él tenía una amada rubia como una espiga de sol, de un gran parecido a la Beatriz ideal llorada por el poeta de Florencia. Y un día en que las nubes del espacio fueron más azules y más límpida la luz de los astros, se vio entre auras impalpables y aromosas subir al cielo una nubecita blanca, blanquísima, en la forma de una paloma; y era el alma de la niña rubia, la bien amada del artista músico. Mas ella, al romper el aire con sus alas, le consoló diciendo: "No llores, mi adorado; la ausencia es eterna para los que no saben amar; el amor tiene eslabones con la eternidad, y yo viviré en las cuerdas de tu violoncello".</p>
          <p>¡La noche de la gran ovación! El escenario resplandece, el músico se presenta, el ruido de los aplausos atruena. La mano blanca del artista levanta el arco; pero al oprimir las cuerdas, un gemido agudo, penetrante, lastimero, una sola dolorosa nota, un golpe seco como de algo que estalla.</p>
          <p>Y se vio surgir del violoncello una nubecita blanca, en la forma de una paloma, y al partir el aire con sus alas se deshizo en lágrimas que humedecieron las cuerdas dejándolas insonoras por siempre jamás.</p>
        `
      }
    ]
  }
];

// ── UTILITY ───────────────────────────────────────
function showPage(id, btn) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  document.querySelectorAll('.nav-tabs button').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  // Initialize charts lazily
  if (id === 'datos' && !window.chartsBuilt) { buildCharts(); window.chartsBuilt = true; }
}

// ── RENDER AUTHOR CARDS ───────────────────────────
function renderAuthors(containerId, mini) {
  const container = document.getElementById(containerId);
  container.innerHTML = '';
  AUTHORS.forEach((a, ai) => {
    const card = document.createElement('div');
    card.className = 'author-card';
    card.id = containerId + '-card-' + a.id;

    const textsCount = a.textos.length;
    const narrative = a.textos.filter(t => t.tipo === 'narrativa').length;
    const lyric     = a.textos.filter(t => t.tipo === 'lirica').length;

    card.innerHTML = `
      <div class="author-card-header" onclick="toggleAuthor('${containerId}', '${a.id}')">
        <div>
          <div class="author-genre-badge">${a.genero}</div>
          <div class="author-name">${a.nombre}</div>
          <div class="author-origin">${a.pais} · ${a.anos}</div>
          <div style="font-size:0.78rem;color:var(--muted);margin-top:0.4rem;">${textsCount} texto${textsCount>1?'s':''} →</div>
        </div>
        <div class="author-card-arrow">›</div>
      </div>
      <div class="author-panel">
        <div class="author-panel-inner">
          <div class="author-bio-col">
            <h3>${a.nombre}</h3>
            <div class="bio-origin">${a.pais} · ${a.anos}</div>
            <div class="author-bio-text">${a.bio.replace(/\n\n/g,'</p><p>').replace(/^/,'<p>').replace(/$/,'</p>')}</div>
          </div>
          <div class="author-texts-col">
            <div class="texts-list-title">Textos en la Revista Azul</div>
            ${a.textos.map((t, ti) => `
              <div class="text-item">
                <button class="text-item-btn" onclick="toggleText('${containerId}','${a.id}',${ti})">
                  <div class="text-item-title">${t.titulo}</div>
                  <div class="text-item-ref">${t.ref}</div>
                </button>
                <div class="text-content" id="${containerId}-${a.id}-text-${ti}">
                  ${t.contenido}
                </div>
              </div>
            `).join('')}
          </div>
        </div>
      </div>
    `;
    container.appendChild(card);
  });
}

function toggleAuthor(containerId, authorId) {
  const card = document.getElementById(containerId + '-card-' + authorId);
  const isOpen = card.classList.contains('open');
  // Close all in this container
  document.querySelectorAll('#' + containerId + ' .author-card').forEach(c => c.classList.remove('open'));
  if (!isOpen) card.classList.add('open');
}

function toggleText(containerId, authorId, idx) {
  const el = document.getElementById(`${containerId}-${authorId}-text-${idx}`);
  el.classList.toggle('open');
}

// ── DATA VISUALIZATIONS ───────────────────────────
function buildCharts() {

  // 1. Bar chart: texts per author
  const barData = AUTHORS.map(a => ({ name: a.nombre.split(' ').slice(0,2).join(' '), val: a.textos.length }));
  const maxVal = Math.max(...barData.map(d => d.val));
  const barContainer = document.getElementById('chart-textos');
  barData.forEach(d => {
    const pct = Math.round((d.val / maxVal) * 100);
    barContainer.innerHTML += `
      <div class="bar-row">
        <div class="bar-lbl">${d.name}</div>
        <div class="bar-track"><div class="bar-fill" style="width:${pct}%"></div></div>
        <div class="bar-val">${d.val}</div>
      </div>`;
  });

  // 2. Donut: genre
  const narrative = AUTHORS.reduce((s,a) => s + a.textos.filter(t=>t.tipo==='narrativa').length, 0);
  const lyric     = AUTHORS.reduce((s,a) => s + a.textos.filter(t=>t.tipo==='lirica').length, 0);
  drawDonut('donut-genre', 'legend-genre',
    [{ label:'Narrativa', val: narrative, color: '#8AA4C3' },
     { label:'Lírica',    val: lyric,     color: '#C4A96D' }]);

  // 3. Donut: country
  const countryMap = {};
  AUTHORS.forEach(a => { countryMap[a.pais] = (countryMap[a.pais]||0)+1; });
  const countryColors = { 'México':'#8AA4C3', 'Cuba':'#6B8DAD', 'España':'#C4A96D', 'Venezuela':'#B5CADF', 'Rumania':'#D4C5E8' };
  drawDonut('donut-country', 'legend-country',
    Object.entries(countryMap).map(([l,v]) => ({ label:l, val:v, color: countryColors[l]||'#ccc' })));

  // 4. Timeline
  const minYear = 1840, maxYear = 1970;
  const tlContainer = document.getElementById('chart-timeline');
  AUTHORS.forEach(a => {
    const [b, d] = a.anos.split('–').map(Number);
    const left = ((b - minYear) / (maxYear - minYear)) * 100;
    const width = ((d - b) / (maxYear - minYear)) * 100;
    tlContainer.innerHTML += `
      <div class="tl-row">
        <div class="tl-name">${a.nombre.split(' ').slice(0,2).join(' ')}</div>
        <div class="tl-track">
          <div class="tl-bar" style="left:${left}%;width:${width}%"></div>
        </div>
        <div class="tl-years">${a.anos}</div>
      </div>`;
  });

  // 5. Index table
  const table = document.getElementById('vol-table');
  table.innerHTML = `<thead><tr><th>Título</th><th>Autora</th><th>Tipo</th><th>Referencia</th></tr></thead><tbody></tbody>`;
  const tbody = table.querySelector('tbody');
  AUTHORS.forEach(a => {
    a.textos.forEach(t => {
      const row = document.createElement('tr');
      row.innerHTML = `
        <td>${t.titulo}</td>
        <td style="font-style:normal;color:var(--muted)">${a.nombre}</td>
        <td><span class="genre-badge ${t.tipo==='lirica'?'lirica':''}">${t.tipo==='lirica'?'Lírica':'Narrativa'}</span></td>
        <td style="font-style:normal;color:var(--muted)">${t.ref}</td>`;
      tbody.appendChild(row);
    });
  });
}

function drawDonut(svgId, legendId, data) {
  const total = data.reduce((s, d) => s + d.val, 0);
  const svg = document.getElementById(svgId);
  const cx = 65, cy = 65, r = 50, ri = 30;
  let angle = -Math.PI / 2;
  let paths = '';
  data.forEach(d => {
    const slice = (d.val / total) * 2 * Math.PI;
    const x1 = cx + r * Math.cos(angle), y1 = cy + r * Math.sin(angle);
    const x2 = cx + r * Math.cos(angle + slice), y2 = cy + r * Math.sin(angle + slice);
    const ix1 = cx + ri * Math.cos(angle), iy1 = cy + ri * Math.sin(angle);
    const ix2 = cx + ri * Math.cos(angle + slice), iy2 = cy + ri * Math.sin(angle + slice);
    const large = slice > Math.PI ? 1 : 0;
    paths += `<path d="M${x1},${y1} A${r},${r} 0 ${large} 1 ${x2},${y2} L${ix2},${iy2} A${ri},${ri} 0 ${large} 0 ${ix1},${iy1} Z" fill="${d.color}" stroke="var(--white)" stroke-width="2"/>`;
    angle += slice;
  });
  svg.innerHTML = paths;

  const legend = document.getElementById(legendId);
  legend.innerHTML = data.map(d => `
    <div class="legend-item">
      <div class="legend-dot" style="background:${d.color}"></div>
      <span>${d.label}: <strong>${d.val}</strong></span>
    </div>`).join('');
}

// ── INIT ──────────────────────────────────────────
renderAuthors('home-grid');
renderAuthors('autoras-grid');
</script>
</body>
</html>
