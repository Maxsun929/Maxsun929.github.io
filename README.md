<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maxine Sun — Early Childhood Educator</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --sage: #5a7a62;
    --sage-light: #e8f0ea;
    --sage-mid: #9ab5a0;
    --warm: #f7f3ee;
    --warm-deep: #ede7dd;
    --ink: #1e2820;
    --ink-mid: #4a5c4e;
    --ink-light: #7a8c7d;
    --cream: #faf8f5;
    --gold: #c9a96e;
    --gold-light: #f5ead8;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    font-size: 16px;
    line-height: 1.7;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.2rem 4rem;
    background: rgba(250, 248, 245, 0.92);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid rgba(90, 122, 98, 0.12);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem;
    font-weight: 400;
    color: var(--ink);
    letter-spacing: 0.02em;
  }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    text-decoration: none; color: var(--ink-mid);
    font-size: 0.8rem; font-weight: 400;
    letter-spacing: 0.12em; text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sage); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
  }
  .hero-text {
    padding: 8rem 4rem 8rem 4rem;
  }
  .hero-tag {
    display: inline-block;
    font-size: 0.72rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--sage); font-weight: 500;
    background: var(--sage-light);
    padding: 0.4rem 1rem;
    border-radius: 2rem;
    margin-bottom: 2rem;
  }
  .hero h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 5vw, 4.8rem);
    font-weight: 300;
    line-height: 1.1;
    color: var(--ink);
    margin-bottom: 1.5rem;
  }
  .hero h1 em {
    font-style: italic;
    color: var(--sage);
  }
  .hero-sub {
    font-size: 1rem; color: var(--ink-mid);
    max-width: 380px; line-height: 1.8;
    margin-bottom: 2.5rem;
  }
  .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    display: inline-block;
    background: var(--sage); color: white;
    padding: 0.85rem 2rem;
    border-radius: 2rem;
    text-decoration: none;
    font-size: 0.85rem; font-weight: 500;
    letter-spacing: 0.04em;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: #4a6852; transform: translateY(-1px); }
  .btn-outline {
    display: inline-block;
    border: 1.5px solid var(--sage-mid); color: var(--sage);
    padding: 0.85rem 2rem;
    border-radius: 2rem;
    text-decoration: none;
    font-size: 0.85rem; font-weight: 400;
    transition: all 0.2s;
  }
  .btn-outline:hover { background: var(--sage-light); }

  .hero-panel {
    background: var(--sage-light);
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero-panel::before {
    content: '';
    position: absolute; top: -80px; right: -80px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: rgba(90,122,98,0.08);
  }
  .hero-panel::after {
    content: '';
    position: absolute; bottom: -60px; left: -60px;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: rgba(201,169,110,0.1);
  }
  .avatar-ring {
    width: 180px; height: 180px;
    border-radius: 50%;
    background: var(--sage);
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 2rem;
    font-family: 'Cormorant Garamond', serif;
    font-size: 4.5rem; font-weight: 300; color: white;
    letter-spacing: -0.02em;
    position: relative; z-index: 1;
  }
  .hero-stats {
    display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;
    width: 100%; max-width: 300px;
    position: relative; z-index: 1;
  }
  .stat-card {
    background: white;
    border-radius: 1rem;
    padding: 1.2rem;
    text-align: center;
  }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2rem; font-weight: 600; color: var(--sage);
    line-height: 1;
  }
  .stat-label {
    font-size: 0.72rem; color: var(--ink-light);
    text-transform: uppercase; letter-spacing: 0.1em;
    margin-top: 0.3rem;
  }

  /* SECTIONS */
  section { padding: 6rem 4rem; }
  .section-inner { max-width: 1100px; margin: 0 auto; }
  .section-label {
    font-size: 0.72rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--sage); font-weight: 500; margin-bottom: 0.75rem;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 3.5vw, 2.8rem);
    font-weight: 300; color: var(--ink);
    margin-bottom: 3rem;
    max-width: 500px;
  }

  /* ABOUT */
  #about { background: white; }
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 5rem; align-items: start;
  }
  .about-text p {
    color: var(--ink-mid); margin-bottom: 1.2rem; font-size: 1rem;
  }
  .about-highlights { display: flex; flex-direction: column; gap: 1rem; }
  .highlight-item {
    display: flex; gap: 1rem; align-items: flex-start;
    padding: 1.2rem;
    background: var(--warm);
    border-radius: 0.75rem;
    border-left: 3px solid var(--sage);
  }
  .hi-icon {
    width: 36px; height: 36px; flex-shrink: 0;
    background: var(--sage-light);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem;
  }
  .hi-text strong { display: block; font-size: 0.9rem; font-weight: 500; color: var(--ink); }
  .hi-text span { font-size: 0.82rem; color: var(--ink-light); }

  /* PLACEMENT */
  #placement { background: var(--warm); }
  .placement-card {
    background: white;
    border-radius: 1.25rem;
    padding: 2.5rem;
    margin-bottom: 2rem;
    border: 1px solid rgba(90,122,98,0.12);
  }
  .placement-header {
    display: flex; justify-content: space-between; align-items: flex-start;
    margin-bottom: 1.5rem; flex-wrap: wrap; gap: 1rem;
  }
  .placement-org { font-family: 'Cormorant Garamond', serif; font-size: 1.6rem; font-weight: 400; }
  .placement-badge {
    background: var(--sage-light); color: var(--sage);
    font-size: 0.75rem; font-weight: 500;
    padding: 0.4rem 1rem; border-radius: 2rem;
    letter-spacing: 0.06em;
  }
  .placement-meta { color: var(--ink-light); font-size: 0.88rem; margin-bottom: 1.5rem; }
  .placement-detail-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem; margin-bottom: 1.5rem;
  }
  .pd-item {
    padding: 1rem;
    background: var(--warm);
    border-radius: 0.75rem;
  }
  .pd-label { font-size: 0.72rem; text-transform: uppercase; letter-spacing: 0.1em; color: var(--ink-light); margin-bottom: 0.3rem; }
  .pd-value { font-size: 0.95rem; font-weight: 500; color: var(--ink); }
  .task-chips { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .chip {
    background: var(--gold-light); color: #7a5e38;
    font-size: 0.78rem; padding: 0.3rem 0.85rem;
    border-radius: 2rem; font-weight: 400;
  }

  /* EXPERIENCE */
  #experience { background: white; }
  .exp-list { display: flex; flex-direction: column; gap: 0; }
  .exp-item {
    display: grid; grid-template-columns: 180px 1fr;
    gap: 2rem; padding: 2rem 0;
    border-bottom: 1px solid var(--warm-deep);
    align-items: start;
  }
  .exp-item:last-child { border-bottom: none; }
  .exp-date { font-size: 0.82rem; color: var(--ink-light); padding-top: 0.25rem; }
  .exp-role { font-family: 'Cormorant Garamond', serif; font-size: 1.3rem; font-weight: 400; margin-bottom: 0.2rem; }
  .exp-org { font-size: 0.85rem; color: var(--sage); font-weight: 500; margin-bottom: 0.75rem; }
  .exp-points { list-style: none; }
  .exp-points li {
    font-size: 0.9rem; color: var(--ink-mid);
    padding: 0.25rem 0 0.25rem 1.2rem;
    position: relative;
  }
  .exp-points li::before {
    content: ''; position: absolute; left: 0; top: 0.7rem;
    width: 5px; height: 5px; border-radius: 50%;
    background: var(--sage-mid);
  }

  /* CREDENTIALS */
  #credentials { background: var(--warm); }
  .cred-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1.25rem; }
  .cred-card {
    background: white; border-radius: 1rem;
    padding: 1.5rem;
    border: 1px solid rgba(90,122,98,0.1);
    transition: transform 0.2s;
  }
  .cred-card:hover { transform: translateY(-3px); }
  .cred-icon { font-size: 1.5rem; margin-bottom: 0.8rem; }
  .cred-title { font-size: 0.92rem; font-weight: 500; color: var(--ink); margin-bottom: 0.3rem; }
  .cred-sub { font-size: 0.8rem; color: var(--ink-light); }
  .cred-new {
    display: inline-block; font-size: 0.65rem; font-weight: 500;
    background: var(--sage); color: white;
    padding: 0.2rem 0.6rem; border-radius: 2rem;
    letter-spacing: 0.08em; margin-left: 0.5rem;
    vertical-align: middle;
  }

  /* EDUCATION */
  #education { background: white; }
  .edu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .edu-card {
    background: var(--sage-light);
    border-radius: 1.25rem; padding: 2rem;
    position: relative; overflow: hidden;
  }
  .edu-card::after {
    content: '';
    position: absolute; bottom: -20px; right: -20px;
    width: 80px; height: 80px;
    border-radius: 50%;
    background: rgba(90,122,98,0.12);
  }
  .edu-degree { font-family: 'Cormorant Garamond', serif; font-size: 1.35rem; font-weight: 400; margin-bottom: 0.3rem; }
  .edu-uni { font-size: 0.85rem; color: var(--sage); font-weight: 500; margin-bottom: 0.2rem; }
  .edu-year { font-size: 0.8rem; color: var(--ink-light); }

  /* SKILLS */
  #skills { background: var(--ink); }
  #skills .section-label { color: var(--sage-mid); }
  #skills .section-title { color: white; }
  .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1.5rem; }
  .skill-group h4 {
    font-size: 0.72rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--sage-mid); margin-bottom: 1rem;
  }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .skill-tag {
    background: rgba(255,255,255,0.07);
    color: rgba(255,255,255,0.75);
    font-size: 0.8rem; padding: 0.35rem 0.85rem;
    border-radius: 2rem;
    border: 1px solid rgba(255,255,255,0.1);
  }
  .lang-list { display: flex; flex-direction: column; gap: 0.5rem; }
  .lang-item {
    display: flex; justify-content: space-between; align-items: center;
    color: rgba(255,255,255,0.75); font-size: 0.88rem;
  }
  .lang-dot { width: 6px; height: 6px; background: var(--sage-mid); border-radius: 50%; }

  /* CONTACT */
  #contact { background: var(--sage); }
  .contact-inner { max-width: 700px; margin: 0 auto; text-align: center; }
  .contact-inner .section-label { color: rgba(255,255,255,0.6); }
  .contact-inner .section-title { color: white; max-width: 100%; margin: 0 auto 1.5rem; }
  .contact-sub { color: rgba(255,255,255,0.75); margin-bottom: 3rem; font-size: 1rem; }
  .contact-links { display: flex; justify-content: center; flex-wrap: wrap; gap: 1.5rem; }
  .contact-link {
    display: flex; align-items: center; gap: 0.6rem;
    color: white; text-decoration: none;
    font-size: 0.9rem; font-weight: 400;
    background: rgba(255,255,255,0.12);
    padding: 0.75rem 1.5rem;
    border-radius: 2rem;
    border: 1px solid rgba(255,255,255,0.2);
    transition: background 0.2s;
  }
  .contact-link:hover { background: rgba(255,255,255,0.22); }

  /* FOOTER */
  footer {
    background: var(--ink); color: var(--ink-light);
    text-align: center; padding: 2rem 4rem;
    font-size: 0.8rem;
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { gap: 1.5rem; }
    .hero { grid-template-columns: 1fr; }
    .hero-panel { display: none; }
    .hero-text { padding: 6rem 1.5rem 4rem; }
    section { padding: 4rem 1.5rem; }
    .about-grid, .edu-grid { grid-template-columns: 1fr; }
    .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
    .exp-date { padding-top: 0; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-logo">Maxine Sun</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#placement">Placement</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#credentials">Credentials</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-text">
    <div class="hero-tag">Early Childhood Educator</div>
    <h1>Nurturing <em>curious</em> minds through play</h1>
    <p class="hero-sub">
      Graduate educator specialising in the 3–5 years preschool setting. Committed to play-based learning, meaningful documentation, and genuine connections with children and families.
    </p>
    <div class="hero-ctas">
      <a href="#placement" class="btn-primary">View My Placement</a>
      <a href="#contact" class="btn-outline">Get in Touch</a>
    </div>
  </div>
  <div class="hero-panel">
    <div class="avatar-ring">M</div>
    <div class="hero-stats">
      <div class="stat-card">
        <div class="stat-num">30</div>
        <div class="stat-label">Placement days</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">3–5</div>
        <div class="stat-label">Age range</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">3</div>
        <div class="stat-label">Languages</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">EYLF</div>
        <div class="stat-label">Framework</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <p class="section-label">Who I am</p>
    <h2 class="section-title">A caring, curious educator in the making</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I'm Maxine, an Early Childhood educator candidate currently completing my Graduate Diploma of Education at Southern Cross University. I bring a genuine passion for play-based learning, positive behaviour guidance, and creating inclusive environments where every child feels seen and valued.
        </p>
        <p>
          My background spans early childhood placement, research assistance, PTE tutoring, and customer experience — each role deepening my ability to listen, adapt, and connect with people from all walks of life. I'm trilingual in English, Mandarin, and Korean, which has been a real asset in building trust with diverse families.
        </p>
        <p>
          I'm actively seeking educator roles in an exceeding-rated early learning service where I can continue growing alongside a strong, collaborative team.
        </p>
      </div>
      <div class="about-highlights">
        <div class="highlight-item">
          <div class="hi-icon">🎨</div>
          <div class="hi-text">
            <strong>Play-based learning advocate</strong>
            <span>Designing engaging, child-led experiences rooted in EYLF principles</span>
          </div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">📋</div>
          <div class="hi-text">
            <strong>Skilled documentor</strong>
            <span>Observations, learning stories, lesson plans & developmental summaries</span>
          </div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">🤝</div>
          <div class="hi-text">
            <strong>Family-centred approach</strong>
            <span>Building genuine partnerships with families through open communication</span>
          </div>
        </div>
        <div class="highlight-item">
          <div class="hi-icon">🌏</div>
          <div class="hi-text">
            <strong>Culturally inclusive</strong>
            <span>Fluent in English, Mandarin & Korean — supporting diverse communities</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PLACEMENT -->
<section id="placement">
  <div class="section-inner">
    <p class="section-label">Professional Experience</p>
    <h2 class="section-title">Hands-on teaching in an Exceeding setting</h2>
    <div class="placement-card">
      <div class="placement-header">
        <div class="placement-org">Busy Bees at Yokine</div>
        <div class="placement-badge">TCHR6008 — 30-Day Placement</div>
      </div>
      <div class="placement-meta">Perth, Western Australia &nbsp;·&nbsp; May – June 2026 &nbsp;·&nbsp; Kindy Room (3–5 years)</div>
      <div class="placement-detail-grid">
        <div class="pd-item">
          <div class="pd-label">Primary Room</div>
          <div class="pd-value">Kindy (3–5 years)</div>
        </div>
        <div class="pd-item">
          <div class="pd-label">Additional Experience</div>
          <div class="pd-value">Toddler Room (combined)</div>
        </div>
        <div class="pd-item">
          <div class="pd-label">Framework</div>
          <div class="pd-value">EYLF V2.0</div>
        </div>
        <div class="pd-item">
          <div class="pd-label">Duration</div>
          <div class="pd-value">30 placement days</div>
        </div>
      </div>
      <p style="font-size:0.9rem; color:var(--ink-mid); margin-bottom:1.2rem;">
        Completed a 30-day professional placement at Busy Bees Yokine, primarily working in the 3–5 kindy room and gaining valuable cross-age experience in the toddler room during combined-room sessions. Throughout the placement I took on an active teaching role, planning and leading daily learning experiences while building genuine, trusting relationships with children and their families.
      </p>
      <p style="font-size:0.75rem; text-transform:uppercase; letter-spacing:0.1em; color:var(--ink-light); margin-bottom:0.6rem;">What I did during placement</p>
      <div class="task-chips">
        <span class="chip">Led daily learning experiences</span>
        <span class="chip">Wrote daily observations</span>
        <span class="chip">Developed lesson plans</span>
        <span class="chip">Children's developmental plans</span>
        <span class="chip">Portfolio documentation</span>
        <span class="chip">Critical reflections (4Rs model)</span>
        <span class="chip">EYLF outcome planning</span>
        <span class="chip">Planned & taught half/full days</span>
        <span class="chip">Indoor & outdoor environment setup</span>
        <span class="chip">Family communication</span>
        <span class="chip">Positive behaviour guidance</span>
        <span class="chip">Learning summaries for families</span>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-inner">
    <p class="section-label">Work History</p>
    <h2 class="section-title">Experience across education &amp; beyond</h2>
    <div class="exp-list">
      <div class="exp-item">
        <div class="exp-date">May 2025 – Present</div>
        <div>
          <div class="exp-role">PTE Tutor</div>
          <div class="exp-org">Freelance · Sydney & Perth</div>
          <ul class="exp-points">
            <li>Support students' English communication, pronunciation, and academic writing in a nurturing, inclusive environment</li>
            <li>Develop structured learning plans tailored to individual styles and goals</li>
            <li>Provide constructive feedback that significantly improves student engagement and confidence</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-date">Dec 2025 – Present</div>
        <div>
          <div class="exp-role">Sales Specialist</div>
          <div class="exp-org">Apple · Perth</div>
          <ul class="exp-points">
            <li>Build genuine connections through needs-based conversations, delivering inclusive and thoughtful experiences</li>
            <li>Collaborate closely with team members to support one another and maintain a welcoming environment</li>
            <li>Develop patience and problem-solving through resolving customer concerns calmly and efficiently</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-date">Oct 2024 – Oct 2025</div>
        <div>
          <div class="exp-role">Research Assistant</div>
          <div class="exp-org">Western Sydney University · Sydney</div>
          <ul class="exp-points">
            <li>Conducted observations and interviews, developing strong skills in monitoring and documenting behaviours</li>
            <li>Planned and documented research processes, building expertise in record-keeping aligned with curriculum quality principles</li>
            <li>Translated complex technical information into clear, approachable explanations for project participants</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CREDENTIALS -->
<section id="credentials">
  <div class="section-inner">
    <p class="section-label">Certifications & Checks</p>
    <h2 class="section-title">Compliant, trained, and ready</h2>
    <div class="cred-grid">
      <div class="cred-card">
        <div class="cred-icon">🛡️</div>
        <div class="cred-title">WA Working with Children Check</div>
        <div class="cred-sub">Department of Communities, WA</div>
      </div>
      <div class="cred-card">
        <div class="cred-icon">🚨</div>
        <div class="cred-title">First Aid — HLTAID012 <span class="cred-new">New</span></div>
        <div class="cred-sub">Provide First Aid in an Education & Care Setting · ABC First Aid · June 2026</div>
      </div>
      <div class="cred-card">
        <div class="cred-icon">🍃</div>
        <div class="cred-title">ASCIA Anaphylaxis Training</div>
        <div class="cred-sub">Children's Education & Care Setting</div>
      </div>
      <div class="cred-card">
        <div class="cred-icon">🧡</div>
        <div class="cred-title">Child Protection Awareness Training</div>
        <div class="cred-sub">Nationally recognised</div>
      </div>
      <div class="cred-card">
        <div class="cred-icon">✅</div>
        <div class="cred-title">National Child Safety Training</div>
        <div class="cred-sub">Current</div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-inner">
    <p class="section-label">Education</p>
    <h2 class="section-title">Academic foundation</h2>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="edu-degree">Graduate Diploma of Education</div>
        <div class="edu-uni">Southern Cross University, Perth</div>
        <div class="edu-year">Oct 2025 – Oct 2026 &nbsp;·&nbsp; In progress</div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">Bachelor of Arts</div>
        <div class="edu-uni">University of Sydney</div>
        <div class="edu-year">Completed</div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-inner">
    <p class="section-label">Skills & Strengths</p>
    <h2 class="section-title">What I bring to your team</h2>
    <div class="skills-grid">
      <div class="skill-group">
        <h4>Child-centred practice</h4>
        <div class="skill-tags">
          <span class="skill-tag">Supervision (0–5 yrs)</span>
          <span class="skill-tag">Play-based learning</span>
          <span class="skill-tag">Positive behaviour guidance</span>
          <span class="skill-tag">Inclusive environments</span>
          <span class="skill-tag">Routine management</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Documentation</h4>
        <div class="skill-tags">
          <span class="skill-tag">Observations</span>
          <span class="skill-tag">Learning stories</span>
          <span class="skill-tag">Lesson plans</span>
          <span class="skill-tag">Developmental plans</span>
          <span class="skill-tag">Critical reflections</span>
          <span class="skill-tag">EYLF outcome mapping</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Professional</h4>
        <div class="skill-tags">
          <span class="skill-tag">Teamwork & collaboration</span>
          <span class="skill-tag">Active listening</span>
          <span class="skill-tag">Empathy & patience</span>
          <span class="skill-tag">Problem-solving</span>
          <span class="skill-tag">Adaptability</span>
          <span class="skill-tag">Time management</span>
        </div>
      </div>
      <div class="skill-group">
        <h4>Languages</h4>
        <div class="lang-list">
          <div class="lang-item"><span>English</span><span class="lang-dot"></span></div>
          <div class="lang-item"><span>Mandarin Chinese</span><span class="lang-dot"></span></div>
          <div class="lang-item"><span>Korean</span><span class="lang-dot"></span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="contact-inner">
      <p class="section-label">Get in touch</p>
      <h2 class="section-title">Let's talk about working together</h2>
      <p class="contact-sub">I'm actively looking for educator roles in Perth. If you're a centre with a warm, collaborative team, I'd love to hear from you.</p>
      <div class="contact-links">
        <a href="mailto:maxsun929@gmail.com" class="contact-link">✉️ maxsun929@gmail.com</a>
        <a href="tel:0402239856" class="contact-link">📞 0402 239 856</a>
        <a href="https://www.linkedin.com/in/max-sun-94b50a172" target="_blank" class="contact-link">🔗 LinkedIn</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>© 2026 Maxine Sun · Early Childhood Educator · Perth, WA</p>
</footer>

</body>
</html>
