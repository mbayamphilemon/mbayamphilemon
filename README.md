 <html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mbayam Guelbe Philémon — Data Analyst & Développeur</title>
<meta name="description" content="Portfolio de Mbayam Guelbe Philémon, ingénieur informaticien, data analyst et développeur web & mobile.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<!-- Bootstrap (navbar / collapse menu + utilities) -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<!-- AOS (animations au scroll) -->
<link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
<style>
  :root{
    --bg:#0d1017;
    --bg-alt:#12161f;
    --surface:#1a1f2b;
    --border:#272e3d;
    --border-soft:#1f2530;
    --text:#eef0f4;
    --text-muted:#8991a3;
    --text-dim:#565e70;
    --accent:#3ecf8e;
    --accent-soft:#3ecf8e1a;
    --accent-2:#e8a33d;
    --radius:10px;
    --maxw:1080px;
    --bs-body-bg:var(--bg);
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--text);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.mono{font-family:'IBM Plex Mono', monospace;}
  a{color:inherit;}
  img{max-width:100%;display:block;}
  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 28px;}
  ::selection{background:var(--accent); color:#0a0d12;}

  @keyframes rise{
    from{opacity:0; transform:translateY(14px);}
    to{opacity:1; transform:translateY(0);}
  }
  @media (prefers-reduced-motion: reduce){
    *{animation:none !important; transition:none !important;}
  }

  /* ---- navbar (Bootstrap) ---- */
  .navbar{
    background:rgba(13,16,23,0.86) !important;
    backdrop-filter:blur(12px);
    border-bottom:1px solid var(--border-soft);
    padding-top:14px; padding-bottom:14px;
  }
  .navbar-brand{font-family:'IBM Plex Mono',monospace; font-size:15px; font-weight:500; color:var(--text) !important;}
  .navbar-brand span{color:var(--accent);}
  .navbar .nav-link{
    color:var(--text-muted) !important; font-size:14.5px; margin:0 4px;
    position:relative; transition:color .15s;
  }
  .navbar .nav-link::after{
    content:""; position:absolute; left:12px; right:12px; bottom:2px; height:1px;
    background:var(--accent); transform:scaleX(0); transition:transform .2s ease;
  }
  .navbar .nav-link:hover{color:var(--text) !important;}
  .navbar .nav-link:hover::after{transform:scaleX(1);}
  .navbar-toggler{
    border-color:var(--border) !important; padding:6px 9px;
  }
  .navbar-toggler:focus{box-shadow:0 0 0 3px var(--accent-soft);}
  .navbar-toggler-icon{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3e%3cpath stroke='%23eef0f4' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e") !important;
  }
  @media(max-width:991px){
    .navbar-collapse{
      background:var(--bg-alt); border:1px solid var(--border-soft);
      border-radius:10px; margin-top:14px; padding:10px 16px;
    }
    .navbar .nav-link{padding:10px 4px; border-bottom:1px solid var(--border-soft);}
    .navbar .nav-link:last-child{border-bottom:none;}
  }

  /* ---- hero ---- */
  .hero{
    position:relative;
    padding:104px 0 92px;
    border-bottom:1px solid var(--border-soft);
    overflow:hidden;
    background:
      radial-gradient(560px 320px at 82% 8%, var(--accent-soft), transparent 70%),
      radial-gradient(420px 280px at 15% 95%, #e8a33d14, transparent 70%);
  }
  .hero-grid{
    display:grid;
    grid-template-columns:1fr 216px;
    gap:56px;
    align-items:center;
    position:relative;
  }
  .eyebrow{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px; color:var(--accent);
    margin:0 0 18px;
    display:flex; align-items:center; gap:9px;
  }
  .eyebrow::before{
    content:""; width:7px; height:7px; border-radius:50%;
    background:var(--accent); box-shadow:0 0 0 3px var(--accent-soft);
    animation:pulse 2s ease-in-out infinite;
  }
  @keyframes pulse{
    0%,100%{box-shadow:0 0 0 3px var(--accent-soft);}
    50%{box-shadow:0 0 0 6px var(--accent-soft);}
  }
  .hero h1{
    font-size:clamp(32px, 4.4vw, 48px);
    line-height:1.14;
    margin:0 0 14px;
    font-weight:600;
    letter-spacing:-0.015em;
  }
  .hero .role{
    font-size:17px;
    color:var(--text-muted);
    margin:0 0 22px;
    font-family:'IBM Plex Mono',monospace;
  }
  .hero p.bio{
    max-width:60ch;
    color:#c6cbd6;
    font-size:16px;
    margin:0 0 32px;
  }
  .cta-row{display:flex; gap:14px; flex-wrap:wrap;}
  .btn-custom{
    display:inline-flex; align-items:center; gap:8px;
    padding:12px 22px; border-radius:8px;
    font-size:14px; font-weight:500; text-decoration:none;
    border:1px solid transparent;
    transition:transform .15s ease, border-color .15s, box-shadow .15s;
  }
  .btn-primary-custom{background:var(--accent); color:#0a0d12;}
  .btn-primary-custom:hover{transform:translateY(-2px); box-shadow:0 8px 24px -8px #3ecf8e55; color:#0a0d12;}
  .btn-ghost-custom{border-color:var(--border); color:var(--text);}
  .btn-ghost-custom:hover{border-color:var(--text-dim); transform:translateY(-2px); color:var(--text);}

  .avatar-wrap{
    width:196px; height:196px; border-radius:16px;
    overflow:hidden; border:1px solid var(--border);
    background:var(--surface);
    justify-self:end;
    position:relative;
  }
  .avatar-wrap::after{
    content:""; position:absolute; inset:0; border-radius:16px;
    box-shadow:inset 0 0 0 1px #ffffff0d;
  }
  .avatar-wrap img{width:100%; height:100%; object-fit:cover;}
  @media(max-width:640px){
    .hero-grid{grid-template-columns:1fr; text-align:left;}
    .avatar-wrap{justify-self:start; width:132px; height:132px;}
  }

  /* ---- stats ---- */
  .stats{
    border-bottom:1px solid var(--border-soft);
    background:var(--bg-alt);
  }
  .stats-row{
    display:grid; grid-template-columns:repeat(4,1fr);
    padding:26px 0;
  }
  .stat{padding:0 22px; border-left:1px solid var(--border-soft); transition:transform .2s ease;}
  .stat:hover{transform:translateY(-3px);}
  .stat:first-child{border-left:none; padding-left:0;}
  .stat .num{font-family:'IBM Plex Mono',monospace; font-size:25px; color:var(--accent); font-weight:600;}
  .stat .label{font-size:12.5px; color:var(--text-muted); margin-top:4px;}
  @media(max-width:720px){
    .stats-row{grid-template-columns:1fr 1fr; gap:20px 0;}
    .stat{border-left:none; padding:0;}
  }

  /* ---- section shared ---- */
  section{padding:92px 0;}
  .section-head{margin-bottom:52px;}
  .section-tag{font-family:'IBM Plex Mono',monospace; color:var(--accent); font-size:13px; margin:0 0 10px;}
  .section-head h2{font-size:29px; margin:0; font-weight:600; letter-spacing:-0.01em;}

  /* ---- about / skills ---- */
  .about-grid{display:grid; grid-template-columns:1.1fr 1fr; gap:60px;}
  .about-grid p{color:#c6cbd6; font-size:15.5px; max-width:56ch;}
  .skill-groups{display:flex; flex-direction:column; gap:28px;}
  .skill-group-label{font-size:13px; color:var(--text-muted); font-family:'IBM Plex Mono',monospace; margin-bottom:11px;}
  .tags{display:flex; flex-wrap:wrap; gap:8px;}
  .tag{
    font-family:'IBM Plex Mono',monospace; font-size:12.5px;
    padding:6px 12px; border-radius:6px;
    background:var(--surface); border:1px solid var(--border); color:#c6cbd6;
    transition:border-color .15s, color .15s, transform .15s;
  }
  .tag:hover{border-color:var(--accent); color:var(--text); transform:translateY(-2px);}
  @media(max-width:800px){.about-grid{grid-template-columns:1fr;}}

  /* ---- projects ---- */
  .project{
    border-top:1px solid var(--border-soft);
    padding:60px 0;
  }
  .project-head{max-width:680px; margin-bottom:30px;}
  .project-index{font-family:'IBM Plex Mono',monospace; color:var(--accent-2); font-size:13px; margin:0 0 10px;}
  .project-title{font-size:23px; font-weight:600; margin:0 0 13px; letter-spacing:-0.01em;}
  .project-desc{color:#c6cbd6; font-size:15px; margin:0 0 18px; max-width:58ch;}
  .project-tags{display:flex; flex-wrap:wrap; gap:7px; margin-bottom:16px;}
  .project-links{display:flex; gap:16px; font-size:14px;}
  .project-links a{text-decoration:none; color:var(--accent); border-bottom:1px solid transparent; font-weight:500;}
  .project-links a:hover{border-color:var(--accent);}

  .gallery{display:grid; grid-template-columns:1.5fr 1fr; grid-template-rows:1fr 1fr; gap:10px; height:360px;}
  .gallery a{border-radius:10px; overflow:hidden; border:1px solid var(--border); background:var(--surface); display:block;}
  .gallery a.feature{grid-row:1/3;}
  .gallery img{width:100%; height:100%; object-fit:cover; transition:transform .35s ease;}
  .gallery a:hover img{transform:scale(1.045);}
  .gallery.single{height:auto; grid-template-columns:1fr; grid-template-rows:auto;}
  .gallery.single a{aspect-ratio:16/9;}
  @media(max-width:680px){
    .gallery{grid-template-columns:1fr 1fr; height:auto; grid-auto-rows:150px;}
    .gallery a.feature{grid-row:auto; grid-column:1/3; aspect-ratio:16/9; height:auto;}
  }

  /* ---- contact ---- */
  .contact-grid{display:grid; grid-template-columns:0.9fr 1.1fr; gap:60px;}
  .contact-info p{color:#c6cbd6; font-size:15.5px; max-width:44ch;}
  .contact-links{margin-top:24px; display:flex; flex-direction:column; gap:12px; font-size:14.5px;}
  .contact-links a{text-decoration:none; color:var(--text); display:flex; gap:10px; align-items:center; transition:color .15s, transform .15s;}
  .contact-links a:hover{color:var(--accent); transform:translateX(3px);}
  form{display:flex; flex-direction:column; gap:16px;}
  .field label{display:block; font-size:13px; color:var(--text-muted); margin-bottom:6px; font-family:'IBM Plex Mono',monospace;}
  .field input, .field textarea{
    width:100%; background:var(--surface); border:1px solid var(--border);
    border-radius:8px; padding:12px 14px; color:var(--text); font-size:14.5px;
    font-family:'IBM Plex Sans',sans-serif;
    transition:border-color .15s;
  }
  .field input:focus, .field textarea:focus{outline:2px solid var(--accent); outline-offset:1px; border-color:var(--accent);}
  .field textarea{resize:vertical; min-height:120px;}
  .form-error{font-size:13px; color:#f0876b; display:none;}
  .form-note{font-size:12.5px; color:var(--text-dim); margin-top:6px;}
  @media(max-width:800px){.contact-grid{grid-template-columns:1fr;}}

  footer{
    border-top:1px solid var(--border-soft);
    padding:32px 0; font-size:13px; color:var(--text-dim);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px;
  }
</style>
</head>
<body>

<nav class="navbar navbar-expand-lg navbar-dark sticky-top">
  <div class="wrap d-flex w-100 align-items-center">
    <a class="navbar-brand" href="#">mbayam<span>.</span>philemon</a>
    <button class="navbar-toggler ms-auto" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav" aria-controls="mainNav" aria-expanded="false" aria-label="Ouvrir le menu">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse flex-grow-0 ms-auto" id="mainNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link" href="#about">À propos</a></li>
        <li class="nav-item"><a class="nav-link" href="#projets">Projets</a></li>
        <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>

<section class="hero">
  <div class="wrap hero-grid">
    <div data-aos="fade-right" data-aos-duration="600">
      <p class="eyebrow">Disponible pour de nouvelles missions</p>
      <h1>Mbayam Guelbe Philémon</h1>
      <p class="role">Ingénieur informaticien · Data Analyst · Développeur Web &amp; Mobile</p>
      <p class="bio">Je transforme des données brutes en informations exploitables pour la prise de décision : nettoyage, modélisation, mesures DAX et dashboards Power BI / Excel. Diplômé en Informatique (génie logiciel) à l'ENASTIC, N'Djaména — passionné de Data Science.</p>
      <div class="cta-row">
        <a href="#projets" class="btn-custom btn-primary-custom">Voir mes projets</a>
        <a href="#contact" class="btn-custom btn-ghost-custom">Me contacter</a>
        <a href="https://github.com/mbayamphilemon" target="_blank" rel="noopener" class="btn-custom btn-ghost-custom">GitHub ↗</a>
      </div>
    </div>
    <div class="avatar-wrap" data-aos="fade-left" data-aos-duration="600" data-aos-delay="100">
      <img src="https://avatars.githubusercontent.com/u/321174916?v=4" alt="Photo de Mbayam Guelbe Philémon">
    </div>
  </div>
</section>

<div class="stats">
  <div class="wrap stats-row">
    <div class="stat" data-aos="fade-up" data-aos-delay="0"><div class="num">04</div><div class="label">Projets data documentés</div></div>
    <div class="stat" data-aos="fade-up" data-aos-delay="80"><div class="num">05</div><div class="label">Dépôts publics GitHub</div></div>
    <div class="stat" data-aos="fade-up" data-aos-delay="160"><div class="num">6+</div><div class="label">Outils maîtrisés</div></div>
    <div class="stat" data-aos="fade-up" data-aos-delay="240"><div class="num">N'Dj</div><div class="label">Basé à N'Djaména, Tchad</div></div>
  </div>
</div>

<section id="about">
  <div class="wrap about-grid">
    <div data-aos="fade-up">
      <p class="section-tag">01 — À propos</p>
      <h2 style="margin-bottom:18px;">De la donnée brute à la décision</h2>
      <p>Ingénieur informaticien de formation, je me spécialise dans l'analyse de données : je nettoie, modélise et visualise des jeux de données pour en extraire des indicateurs utiles à la prise de décision business. Je conçois aussi des applications web et mobiles, ce qui me permet de livrer des projets de bout en bout — de la base de données à l'interface finale.</p>
      <p>Chaque projet ci-dessous part d'un cahier des charges réel : nettoyage avec Power Query, modélisation en étoile, mesures DAX, puis dashboards interactifs pensés pour une direction ou un service métier.</p>
    </div>
    <div class="skill-groups" data-aos="fade-up" data-aos-delay="120">
      <div>
        <div class="skill-group-label">Data & BI</div>
        <div class="tags">
          <span class="tag">Excel</span>
          <span class="tag">Power Query</span>
          <span class="tag">Power BI</span>
          <span class="tag">DAX</span>
          <span class="tag">SQL</span>
          <span class="tag">PostgreSQL</span>
        </div>
      </div>
      <div>
        <div class="skill-group-label">Développement</div>
        <div class="tags">
          <span class="tag">Web</span>
          <span class="tag">Mobile</span>
          <span class="tag">Git / GitHub</span>
        </div>
      </div>
      <div>
        <div class="skill-group-label">Méthode</div>
        <div class="tags">
          <span class="tag">Modélisation en étoile</span>
          <span class="tag">Nettoyage de données</span>
          <span class="tag">KPI & reporting</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="projets" style="background:var(--bg-alt); border-top:1px solid var(--border-soft); border-bottom:1px solid var(--border-soft);">
  <div class="wrap">
    <div class="section-head" data-aos="fade-up">
      <p class="section-tag">02 — Projets</p>
      <h2>Projets récents</h2>
    </div>

    <!-- Project 1 -->
    <div class="project">
      <div class="project-head" data-aos="fade-up">
        <p class="project-index">Projet 01</p>
        <h3 class="project-title">Analyse des ventes — Power BI</h3>
        <p class="project-desc">Dashboard décisionnel en 4 pages pour une entreprise de distribution : chiffre d'affaires, rentabilité, performance des commerciaux et comportement des segments clients. Modèle en étoile, mesures DAX et nettoyage Power Query.</p>
        <div class="project-tags">
          <span class="tag">Power BI</span><span class="tag">Power Query</span><span class="tag">DAX</span><span class="tag">Excel</span>
        </div>
      </div>
      <div class="gallery" data-aos="fade-up" data-aos-delay="100">
        <a class="feature" href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/performance%20commerciale.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/performance%20commerciale.jpg" alt="Performance commerciale — dashboard Power BI"></a>
        <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20par%20produit.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20par%20produit.jpg" alt="Analyse par produit"></a>
        <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20commerciaux.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20commerciaux.jpg" alt="Analyse des commerciaux"></a>
      </div>
    </div>

    <!-- Project 2 -->
    <div class="project">
      <div class="project-head" data-aos="fade-up">
        <p class="project-index">Projet 02</p>
        <h3 class="project-title">HR Analytics — Power BI</h3>
        <p class="project-desc">Dashboard RH interactif sur une base synthétique de 2 500 employés : structure des effectifs, turnover, rémunération et écarts salariaux. Modélisation avec dimension temporelle et mesures DAX dédiées.</p>
        <div class="project-tags">
          <span class="tag">Power BI</span><span class="tag">Power Query</span><span class="tag">DAX</span>
        </div>
      </div>
      <div class="gallery" data-aos="fade-up" data-aos-delay="100">
        <a class="feature" href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/vue%20d%27ensemble%20RH.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/vue%20d%27ensemble%20RH.png" alt="Vue d'ensemble RH"></a>
        <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/turnover.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/turnover.png" alt="Analyse du turnover"></a>
        <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/renumeration.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/renumeration.png" alt="Analyse de la rémunération"></a>
      </div>
    </div>

    <!-- Project 3 -->
    <div class="project">
      <div class="project-head" data-aos="fade-up">
        <p class="project-index">Projet 03</p>
        <h3 class="project-title">Analyse commerciale — Excel</h3>
        <p class="project-desc">Transformation de données commerciales brutes en informations décisionnelles : nettoyage, tableaux croisés dynamiques, KPI (marge, panier moyen, taux de marge) et dashboard interactif construit entièrement dans Excel.</p>
        <div class="project-tags">
          <span class="tag">Excel</span><span class="tag">Power Query</span><span class="tag">TCD</span>
        </div>
      </div>
      <div class="gallery single" data-aos="fade-up" data-aos-delay="100">
        <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-Excel---Analyses-ventes-/main/DASHBOARD.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-Excel---Analyses-ventes-/main/DASHBOARD.png" alt="Dashboard Excel — analyse des ventes"></a>
      </div>
    </div>

    <!-- Project 4 -->
    <div class="project">
      <div class="project-head" data-aos="fade-up">
        <p class="project-index">Projet 04</p>
        <h3 class="project-title">Exploitation minière au Mali — SQL &amp; PostgreSQL</h3>
        <p class="project-desc">Exploration d'une base relationnelle représentant des sites miniers : production, ressources humaines, équipements et exportations. Jointures, agrégations et classements pour répondre à des questions métier concrètes.</p>
        <div class="project-tags">
          <span class="tag">SQL</span><span class="tag">PostgreSQL</span>
        </div>
        <div class="project-links">
          <a href="https://mbayamphilemon.github.io/Projet-SQL-Exploitation-Minier/" target="_blank" rel="noopener">Démo en ligne ↗</a>

            <a href="https://mbayamphilemon.github.io/mbayamphilemon/CV.png" target="_blank" rel="noopener">Mon CV ↗</a>
          
        </div>
      </div>
    </div>

  </div>
</section>

<section id="contact">
  <div class="wrap contact-grid">
    <div class="contact-info" data-aos="fade-right">
      <p class="section-tag">03 — Contact</p>
      <h2 style="margin-bottom:18px;">Travaillons ensemble</h2>
      <p>Disponible pour des missions de data analyse, de reporting Power BI/Excel ou de développement web &amp; mobile. Le formulaire ouvre directement votre messagerie — répondez-y comme à un e-mail classique.</p>
      <div class="contact-links">
        <a href="mailto:mbayamphilemon@gmail.com">✉ mbayamphilemon@gmail.com</a>
        <a href="https://wa.me/23560387787" target="_blank" rel="noopener">↗ WhatsApp — +235 60 38 77 87</a>
        <a href="https://github.com/mbayamphilemon" target="_blank" rel="noopener">↗ github.com/mbayamphilemon</a>
      </div>
    </div>
    <form id="contactForm" onsubmit="return sendMail(event)" data-aos="fade-left">
      <div class="field">
        <label for="name">Nom</label>
        <input type="text" id="name" name="name" placeholder="Votre nom" required>
      </div>
      <div class="field">
        <label for="email">E-mail</label>
        <input type="email" id="email" name="email" placeholder="vous@entreprise.com" required>
      </div>
      <div class="field">
        <label for="message">Message</label>
        <textarea id="message" name="message" placeholder="Décrivez votre besoin ou votre offre..." required></textarea>
      </div>
      <p class="form-error" id="formError">Merci de remplir tous les champs avec une adresse e-mail valide.</p>
      <button type="submit" class="btn-custom btn-primary-custom" style="align-self:flex-start; border:none; cursor:pointer;">Envoyer le message</button>
      <p class="form-note">Ouvre votre application de messagerie par défaut (mailto:).</p>
    </form>
  </div>
</section>

<footer class="wrap">
  <span>© <span id="year"></span> Mbayam Guelbe Philémon</span>
  <span>N'Djaména, Tchad</span>
</footer>

<!-- Bootstrap JS (gère le menu mobile via data-bs-toggle, fiable sur Android) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<!-- AOS (animations au scroll) -->
<script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
<script>
  AOS.init({ once: true, duration: 600, easing: 'ease-out' });

  document.getElementById('year').textContent = new Date().getFullYear();

  // Ferme le menu mobile après le clic sur un lien (comportement attendu sur Android/iOS)
  document.querySelectorAll('#mainNav .nav-link').forEach(function(link){
    link.addEventListener('click', function(){
      var collapseEl = document.getElementById('mainNav');
      var instance = bootstrap.Collapse.getOrCreateInstance(collapseEl);
      instance.hide();
    });
  });

  function sendMail(e){
    e.preventDefault();
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();
    const message = document.getElementById('message').value.trim();
    const errorEl = document.getElementById('formError');
    const emailOk = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);

    if(!name || !message || !emailOk){
      errorEl.style.display = 'block';
      return false;
    }
    errorEl.style.display = 'none';

    const to = 'mbayamphilemon@gmail.com';
    const subject = encodeURIComponent('Contact portfolio — ' + name);
    const body = encodeURIComponent(message + '\n\n— ' + name + ' (' + email + ')');
    window.location.href = 'mailto:' + to + '?subject=' + subject + '&body=' + body;
    return false;
  }
</script>

</body>
</html>
