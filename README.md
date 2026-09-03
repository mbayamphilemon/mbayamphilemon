 <!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mbayam Guelbe Philémon — Data Analyst & Développeur</title>
<meta name="description" content="Portfolio de Mbayam Guelbe Philémon, ingénieur informaticien, data analyst et développeur web & mobile.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=IBM+Plex+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#10131a;
    --bg-alt:#161a23;
    --surface:#1c212c;
    --surface-2:#20263280;
    --border:#2a3040;
    --text:#eceef3;
    --text-muted:#8891a3;
    --text-dim:#5c6478;
    --accent:#3ecf8e;
    --accent-dim:#3ecf8e33;
    --accent-2:#e8a33d;
    --radius:10px;
    --maxw:1080px;
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

  /* ---- nav ---- */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(16,19,26,0.86);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--border);
  }
  nav.wrap{
    display:flex; align-items:center; justify-content:space-between;
    height:64px;
  }
  .logo{font-family:'IBM Plex Mono',monospace; font-size:15px; font-weight:500; letter-spacing:0.02em; text-decoration:none;}
  .logo span{color:var(--accent);}
  .navlinks{display:flex; gap:32px; font-size:14px; color:var(--text-muted);}
  .navlinks a{text-decoration:none; transition:color .15s;}
  .navlinks a:hover{color:var(--text);}
  .navbtn{display:none; background:none; border:1px solid var(--border); color:var(--text); border-radius:8px; padding:7px 10px; font-size:13px;}
  @media(max-width:720px){
    .navlinks{display:none;}
    .navbtn{display:block;}
  }

  /* ---- hero ---- */
  .hero{
    padding:96px 0 88px;
    border-bottom:1px solid var(--border);
  }
  .hero-grid{
    display:grid;
    grid-template-columns:1fr 220px;
    gap:56px;
    align-items:center;
  }
  .eyebrow{
    font-family:'IBM Plex Mono',monospace;
    font-size:13px; color:var(--accent);
    margin:0 0 18px;
  }
  .hero h1{
    font-size:clamp(30px, 4.2vw, 46px);
    line-height:1.15;
    margin:0 0 14px;
    font-weight:600;
    letter-spacing:-0.01em;
  }
  .hero .role{
    font-size:17px;
    color:var(--text-muted);
    margin:0 0 22px;
    font-family:'IBM Plex Mono',monospace;
  }
  .hero p.bio{
    max-width:60ch;
    color:#c3c8d4;
    font-size:16px;
    margin:0 0 30px;
  }
  .cta-row{display:flex; gap:14px; flex-wrap:wrap;}
  .btn{
    display:inline-flex; align-items:center; gap:8px;
    padding:12px 20px; border-radius:8px;
    font-size:14px; font-weight:500; text-decoration:none;
    border:1px solid transparent;
    transition:transform .12s ease, border-color .15s;
  }
  .btn-primary{background:var(--accent); color:#0a0d12;}
  .btn-primary:hover{transform:translateY(-1px);}
  .btn-ghost{border-color:var(--border); color:var(--text);}
  .btn-ghost:hover{border-color:var(--text-dim);}

  .avatar-wrap{
    width:200px; height:200px; border-radius:14px;
    overflow:hidden; border:1px solid var(--border);
    background:var(--surface);
    justify-self:end;
  }
  .avatar-wrap img{width:100%; height:100%; object-fit:cover;}
  @media(max-width:640px){
    .hero-grid{grid-template-columns:1fr; text-align:left;}
    .avatar-wrap{justify-self:start; width:140px; height:140px;}
  }

  /* ---- stats ---- */
  .stats{
    border-bottom:1px solid var(--border);
    background:var(--bg-alt);
  }
  .stats-row{
    display:grid; grid-template-columns:repeat(4,1fr);
    padding:28px 0;
  }
  .stat{padding:0 20px; border-left:1px solid var(--border);}
  .stat:first-child{border-left:none; padding-left:0;}
  .stat .num{font-family:'IBM Plex Mono',monospace; font-size:26px; color:var(--accent); font-weight:600;}
  .stat .label{font-size:13px; color:var(--text-muted); margin-top:4px;}
  @media(max-width:720px){
    .stats-row{grid-template-columns:1fr 1fr; gap:20px 0;}
    .stat{border-left:none; padding:0;}
  }

  /* ---- section shared ---- */
  section{padding:88px 0;}
  .section-head{margin-bottom:48px;}
  .section-tag{font-family:'IBM Plex Mono',monospace; color:var(--accent); font-size:13px; margin:0 0 10px;}
  .section-head h2{font-size:28px; margin:0; font-weight:600;}

  /* ---- about / skills ---- */
  .about-grid{display:grid; grid-template-columns:1.1fr 1fr; gap:56px;}
  .about-grid p{color:#c3c8d4; font-size:15.5px; max-width:56ch;}
  .skill-groups{display:flex; flex-direction:column; gap:26px;}
  .skill-group-label{font-size:13px; color:var(--text-muted); font-family:'IBM Plex Mono',monospace; margin-bottom:10px;}
  .tags{display:flex; flex-wrap:wrap; gap:8px;}
  .tag{
    font-family:'IBM Plex Mono',monospace; font-size:12.5px;
    padding:6px 11px; border-radius:6px;
    background:var(--surface); border:1px solid var(--border); color:#c3c8d4;
  }
  @media(max-width:800px){.about-grid{grid-template-columns:1fr;}}

  /* ---- projects ---- */
  .project{
    border-top:1px solid var(--border);
    padding:56px 0;
    display:grid;
    grid-template-columns:0.9fr 1.1fr;
    gap:48px;
    align-items:start;
  }
  .project:nth-child(even){grid-template-columns:1.1fr 0.9fr;}
  .project:nth-child(even) .project-media{order:2;}
  .project-index{font-family:'IBM Plex Mono',monospace; color:var(--text-dim); font-size:13px; margin:0 0 10px;}
  .project-title{font-size:22px; font-weight:600; margin:0 0 12px;}
  .project-desc{color:#c3c8d4; font-size:15px; margin:0 0 18px; max-width:52ch;}
  .project-tags{display:flex; flex-wrap:wrap; gap:7px; margin-bottom:20px;}
  .project-links{display:flex; gap:16px; font-size:14px;}
  .project-links a{text-decoration:none; color:var(--accent); border-bottom:1px solid transparent;}
  .project-links a:hover{border-color:var(--accent);}
  .gallery{display:grid; grid-template-columns:1fr 1fr; gap:8px;}
  .gallery a{border-radius:8px; overflow:hidden; border:1px solid var(--border); aspect-ratio:4/3; background:var(--surface);}
  .gallery img{width:100%; height:100%; object-fit:cover; transition:transform .3s;}
  .gallery a:hover img{transform:scale(1.04);}
  .gallery.single{grid-template-columns:1fr;}
  .code-preview{
    border:1px solid var(--border); border-radius:8px; background:var(--surface);
    padding:22px; font-family:'IBM Plex Mono',monospace; font-size:12.5px; color:#8fd6b2;
    overflow-x:auto; white-space:pre;
  }
  @media(max-width:760px){
    .project, .project:nth-child(even){grid-template-columns:1fr;}
    .project:nth-child(even) .project-media{order:0;}
  }

  /* ---- contact ---- */
  .contact-grid{display:grid; grid-template-columns:0.9fr 1.1fr; gap:56px;}
  .contact-info p{color:#c3c8d4; font-size:15.5px; max-width:44ch;}
  .contact-links{margin-top:22px; display:flex; flex-direction:column; gap:10px; font-size:14.5px;}
  .contact-links a{text-decoration:none; color:var(--text); display:flex; gap:10px; align-items:center;}
  .contact-links a:hover{color:var(--accent);}
  form{display:flex; flex-direction:column; gap:16px;}
  .field label{display:block; font-size:13px; color:var(--text-muted); margin-bottom:6px; font-family:'IBM Plex Mono',monospace;}
  .field input, .field textarea{
    width:100%; background:var(--surface); border:1px solid var(--border);
    border-radius:8px; padding:12px 14px; color:var(--text); font-size:14.5px;
    font-family:'IBM Plex Sans',sans-serif;
  }
  .field input:focus, .field textarea:focus{outline:2px solid var(--accent); outline-offset:1px; border-color:var(--accent);}
  .field textarea{resize:vertical; min-height:120px;}
  .form-error{font-size:13px; color:#f0876b; display:none;}
  .form-note{font-size:12.5px; color:var(--text-dim); margin-top:6px;}
  @media(max-width:800px){.contact-grid{grid-template-columns:1fr;}}

  footer{
    border-top:1px solid var(--border);
    padding:32px 0; font-size:13px; color:var(--text-dim);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px;
  }
</style>
</head>
<body>

<header>
  <nav class="wrap">
    <a href="#" class="logo">mbayam<span>.</span>philemon</a>
    <div class="navlinks">
      <a href="#about">À propos</a>
      <a href="#projets">Projets</a>
      <a href="#contact">Contact</a>
    </div>
    <button class="navbtn" onclick="document.getElementById('mobilenav').classList.toggle('open')">Menu</button>
  </nav>
  <div id="mobilenav" style="display:none;" class="wrap"></div>
</header>

<section class="hero">
  <div class="wrap hero-grid">
    <div>
      <p class="eyebrow">Data analyst · Ingénieur informaticien</p>
      <h1>Mbayam Guelbe Philémon</h1>
      <p class="role">Ingénieur informaticien · Data Analyst · Développeur Web &amp; Mobile</p>
      <p class="bio">Je transforme des données brutes en informations exploitables pour la prise de décision : nettoyage, modélisation, mesures DAX et dashboards Power BI / Excel. Diplômé en Informatique (génie logiciel) à l'ENASTIC, N'Djaména — passionné de Data Science.</p>
      <div class="cta-row">
        <a href="#projets" class="btn btn-primary">Voir mes projets</a>
        <a href="#contact" class="btn btn-ghost">Me contacter</a>
        <a href="https://github.com/mbayamphilemon" target="_blank" rel="noopener" class="btn btn-ghost">GitHub ↗</a>
      </div>
    </div>
    <div class="avatar-wrap">
      <img src="https://avatars.githubusercontent.com/u/321174916?v=4" alt="Photo de Mbayam Guelbe Philémon">
    </div>
  </div>
</section>

<div class="stats">
  <div class="wrap stats-row">
    <div class="stat"><div class="num">04</div><div class="label">Projets data documentés</div></div>
    <div class="stat"><div class="num">05</div><div class="label">Dépôts publics GitHub</div></div>
    <div class="stat"><div class="num">6+</div><div class="label">Outils maîtrisés</div></div>
    <div class="stat"><div class="num">N'Dj</div><div class="label">Basé à N'Djaména, Tchad</div></div>
  </div>
</div>

<section id="about">
  <div class="wrap about-grid">
    <div>
      <p class="section-tag">01 — À propos</p>
      <h2 style="margin-bottom:18px;">De la donnée brute à la décision</h2>
      <p>Ingénieur informaticien de formation, je me spécialise dans l'analyse de données : je nettoie, modélise et visualise des jeux de données pour en extraire des indicateurs utiles à la prise de décision business. Je conçois aussi des applications web et mobiles, ce qui me permet de livrer des projets de bout en bout — de la base de données à l'interface finale.</p>
      <p>Chaque projet ci-dessous part d'un cahier des charges réel : nettoyage avec Power Query, modélisation en étoile, mesures DAX, puis dashboards interactifs pensés pour une direction ou un service métier.</p>
    </div>
    <div class="skill-groups">
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

<section id="projets" style="background:var(--bg-alt); border-top:1px solid var(--border); border-bottom:1px solid var(--border);">
  <div class="wrap">
    <div class="section-head">
      <p class="section-tag">02 — Projets</p>
      <h2>Projets récents</h2>
    </div>

    <!-- Project 1 -->
    <div class="project">
      <div class="project-media">
        <div class="gallery">
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/performance%20commerciale.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/performance%20commerciale.jpg" alt="Performance commerciale — dashboard Power BI"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20par%20produit.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20par%20produit.jpg" alt="Analyse par produit"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20commerciaux.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20commerciaux.jpg" alt="Analyse des commerciaux"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20clients%20et%20paiement.jpg" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-Analyse-vente/main/analyse%20des%20clients%20et%20paiement.jpg" alt="Analyse des clients et des paiements"></a>
        </div>
      </div>
      <div class="project-body">
        <p class="project-index">Projet 01</p>
        <h3 class="project-title">Analyse des ventes — Power BI</h3>
        <p class="project-desc">Dashboard décisionnel en 4 pages pour une entreprise de distribution : chiffre d'affaires, rentabilité, performance des commerciaux et comportement des segments clients. Modèle en étoile, mesures DAX et nettoyage Power Query.</p>
        <div class="project-tags">
          <span class="tag">Power BI</span><span class="tag">Power Query</span><span class="tag">DAX</span><span class="tag">Excel</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/mbayamphilemon/Projet-PowerBI-Analyse-vente" target="_blank" rel="noopener">Voir le code ↗</a>
        </div>
      </div>
    </div>

    <!-- Project 2 -->
    <div class="project">
      <div class="project-media">
        <div class="gallery">
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/vue%20d%27ensemble%20RH.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/vue%20d%27ensemble%20RH.png" alt="Vue d'ensemble RH"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/turnover.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/turnover.png" alt="Analyse du turnover"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/renumeration.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/renumeration.png" alt="Analyse de la rémunération"></a>
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/analyse%20employes.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-PowerBI-RH/main/analyse%20employes.png" alt="Analyse des employés"></a>
        </div>
      </div>
      <div class="project-body">
        <p class="project-index">Projet 02</p>
        <h3 class="project-title">HR Analytics — Power BI</h3>
        <p class="project-desc">Dashboard RH interactif sur une base synthétique de 2 500 employés : structure des effectifs, turnover, rémunération et écarts salariaux. Modélisation avec dimension temporelle et mesures DAX dédiées.</p>
        <div class="project-tags">
          <span class="tag">Power BI</span><span class="tag">Power Query</span><span class="tag">DAX</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/mbayamphilemon/Projet-PowerBI-RH" target="_blank" rel="noopener">Voir le code ↗</a>
        </div>
      </div>
    </div>

    <!-- Project 3 -->
    <div class="project">
      <div class="project-media">
        <div class="gallery single">
          <a href="https://raw.githubusercontent.com/mbayamphilemon/Projet-Excel---Analyses-ventes-/main/DASHBOARD.png" target="_blank" rel="noopener"><img loading="lazy" src="https://raw.githubusercontent.com/mbayamphilemon/Projet-Excel---Analyses-ventes-/main/DASHBOARD.png" alt="Dashboard Excel — analyse des ventes"></a>
        </div>
      </div>
      <div class="project-body">
        <p class="project-index">Projet 03</p>
        <h3 class="project-title">Analyse commerciale — Excel</h3>
        <p class="project-desc">Transformation de données commerciales brutes en informations décisionnelles : nettoyage, tableaux croisés dynamiques, KPI (marge, panier moyen, taux de marge) et dashboard interactif construit entièrement dans Excel.</p>
        <div class="project-tags">
          <span class="tag">Excel</span><span class="tag">Power Query</span><span class="tag">TCD</span>
        </div>
        <div class="project-links">
          <a href="https://github.com/mbayamphilemon/Projet-Excel---Analyses-ventes-" target="_blank" rel="noopener">Voir le code ↗</a>
        </div>
      </div>
    </div>

    <!-- Project 4 -->
    <div class="project">
      <div class="project-media">
        <div class="code-preview">SELECT s.site, SUM(p.quantite) AS production
FROM productions p
JOIN sites_miniers s ON s.site_id = p.site_id
WHERE EXTRACT(YEAR FROM p.date_production) = 2024
GROUP BY s.site
HAVING SUM(p.quantite) > 400
ORDER BY production DESC;

-- Fekola : 610.50 tonnes
-- Loulo  : 536.00 tonnes
-- Morila : 410.40 tonnes</div>
      </div>
      <div class="project-body">
        <p class="project-index">Projet 04</p>
        <h3 class="project-title">Exploitation minière au Mali — SQL &amp; PostgreSQL</h3>
        <p class="project-desc">Exploration d'une base relationnelle représentant des sites miniers : production, ressources humaines, équipements et exportations. Jointures, agrégations et classements pour répondre à des questions métier concrètes.</p>
        <div class="project-tags">
          <span class="tag">SQL</span><span class="tag">PostgreSQL</span>
        </div>
        <div class="project-links">
          <a href="https://mbayamphilemon.github.io/Projet-SQL-Exploitation-Minier/" target="_blank" rel="noopener">Démo en ligne ↗</a>
          <a href="https://github.com/mbayamphilemon/Projet-SQL-Exploitation-Minier" target="_blank" rel="noopener">Voir le code ↗</a>
        </div>
      </div>
    </div>

  </div>
</section>

<section id="contact">
  <div class="wrap contact-grid">
    <div class="contact-info">
      <p class="section-tag">03 — Contact</p>
      <h2 style="margin-bottom:18px;">Travaillons ensemble</h2>
      <p>Disponible pour des missions de data analyse, de reporting Power BI/Excel ou de développement web &amp; mobile. Le formulaire ouvre directement votre messagerie — répondez-y comme à un e-mail classique.</p>
      <div class="contact-links">
        <a href="mailto:VOTRE-EMAIL@exemple.com">✉ VOTRE-EMAIL@exemple.com</a>
        <a href="https://github.com/mbayamphilemon" target="_blank" rel="noopener">↗ github.com/mbayamphilemon</a>
      </div>
    </div>
    <form id="contactForm" onsubmit="return sendMail(event)">
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
      <button type="submit" class="btn btn-primary" style="align-self:flex-start;">Envoyer le message</button>
      <p class="form-note">Ouvre votre application de messagerie par défaut (mailto:).</p>
    </form>
  </div>
</section>

<footer class="wrap">
  <span>© <span id="year"></span> Mbayam Guelbe Philémon</span>
  <span>N'Djaména, Tchad</span>
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

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
