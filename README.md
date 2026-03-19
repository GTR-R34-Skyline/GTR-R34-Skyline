<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>M. Shashank — Midnight Purple R34</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Share+Tech+Mono&family=Exo+2:wght@300;400;700;900&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }

  :root {
    --bg: #09050f;
    --bg2: #0e0818;
    --bg3: #130c1e;
    --panel: #160f22;
    --border: #241646;
    --border-hot: #c9a227;
    --gtr-red: #c9a227;
    --gtr-red-dim: #8a6d18;
    --gtr-silver: #c4b8e0;
    --gtr-chrome: #e8e0f4;
    --accent: #f0ecff;
    --muted: #5a4a7a;
    --faint: #1e1232;
    --mono: 'Share Tech Mono', monospace;
    --head: 'Exo 2', sans-serif;
    --body: 'Rajdhani', sans-serif;
  }

  html { background: var(--bg); color: var(--accent); font-family: var(--body); font-size: 16px; scroll-behavior: smooth; }

  /* SCAN LINE OVERLAY */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(180,120,255,0.018) 2px,
      rgba(180,120,255,0.018) 4px
    );
    pointer-events: none;
    z-index: 9999;
  }

  /* CARBON FIBER TEXTURE */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      repeating-linear-gradient(45deg, rgba(160,100,255,0.018) 0px, rgba(160,100,255,0.018) 1px, transparent 1px, transparent 8px),
      repeating-linear-gradient(-45deg, rgba(160,100,255,0.018) 0px, rgba(160,100,255,0.018) 1px, transparent 1px, transparent 8px);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px 80px;
    position: relative;
    z-index: 1;
  }

  /* ─── HEADER ─── */
  .hero {
    padding: 60px 0 40px;
    position: relative;
  }

  .hero-top::before {
    content: '';
    position: absolute;
    left: -80px;
    top: 20px;
    width: 400px;
    height: 300px;
    background: radial-gradient(ellipse at center, rgba(100,40,200,0.12) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .hero-top {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 24px;
    margin-bottom: 32px;
  }

  .chassis-id {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--gtr-red);
    letter-spacing: 0.18em;
    text-transform: uppercase;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .chassis-id::before {
    content: '';
    display: inline-block;
    width: 24px;
    height: 1px;
    background: var(--gtr-red);
  }

  .hero-name {
    font-family: var(--head);
    font-size: clamp(48px, 8vw, 88px);
    font-weight: 900;
    line-height: 0.9;
    letter-spacing: -0.03em;
    color: var(--gtr-chrome);
    text-shadow:
      0 0 80px rgba(140,80,255,0.18),
      0 0 160px rgba(201,162,39,0.08),
      0 2px 0 rgba(0,0,0,0.9);
  }

  .hero-name span {
    color: var(--gtr-red);
  }

  .tagline {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 0.1em;
    margin-top: 14px;
    line-height: 1.8;
  }

  .tagline strong {
    color: var(--gtr-silver);
    font-weight: 400;
  }

  /* TACHOMETER-STYLE BADGE */
  .gtr-badge {
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.2em;
    color: var(--gtr-red);
    border: 1px solid var(--gtr-red-dim);
    padding: 6px 14px;
    text-transform: uppercase;
    position: relative;
    flex-shrink: 0;
    background: rgba(201,162,39,0.07);
    clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%);
    overflow: hidden;
  }

  @keyframes goldShimmer {
    0% { left: -100%; }
    100% { left: 200%; }
  }

  .gtr-badge::after {
    content: '';
    position: absolute;
    top: 0; bottom: 0;
    left: -100%;
    width: 60%;
    background: linear-gradient(90deg, transparent, rgba(255,220,80,0.25), transparent);
    animation: goldShimmer 3s ease-in-out infinite;
  }

  /* LINKS BAR */
  .links-bar {
    display: flex;
    gap: 2px;
    flex-wrap: wrap;
    margin-top: 28px;
  }

  .links-bar a {
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    color: var(--muted);
    padding: 7px 18px;
    border: 1px solid var(--border);
    background: var(--panel);
    transition: all 0.2s ease;
    clip-path: polygon(6px 0%, 100% 0%, calc(100% - 6px) 100%, 0% 100%);
  }

  .links-bar a:hover {
    color: var(--gtr-chrome);
    border-color: var(--gtr-red-dim);
    background: rgba(200,57,43,0.08);
  }

  /* HORIZONTAL RULE — racing stripe */
  .stripe {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gtr-red) 30%, var(--gtr-red) 70%, transparent);
    margin: 8px 0 48px;
    position: relative;
    box-shadow: 0 0 12px rgba(201,162,39,0.3);
  }
  .stripe::after {
    content: '';
    position: absolute;
    top: 3px;
    left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(120,60,220,0.3) 30%, rgba(120,60,220,0.3) 70%, transparent);
  }

  /* ─── SECTION LABEL ─── */
  .section-label {
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gtr-red);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── PHILOSOPHY ─── */
  .philosophy {
    margin-bottom: 56px;
  }

  .philosophy-quote {
    font-family: var(--head);
    font-size: clamp(22px, 4vw, 32px);
    font-weight: 700;
    line-height: 1.3;
    color: var(--gtr-chrome);
    padding: 32px 32px 32px 40px;
    border-left: 3px solid var(--gtr-red);
    background: var(--panel);
    margin-bottom: 28px;
    position: relative;
    clip-path: polygon(0 0, 100% 0, 100% calc(100% - 12px), calc(100% - 12px) 100%, 0 100%);
  }

  .philosophy-quote::before {
    content: '"';
    position: absolute;
    top: 8px;
    left: 16px;
    font-size: 48px;
    color: var(--gtr-red-dim);
    font-family: var(--head);
    line-height: 1;
  }

  .philosophy-quote em {
    color: var(--gtr-red);
    font-style: normal;
  }

  .principles {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 2px;
  }

  .principle {
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 16px 20px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--gtr-silver);
    position: relative;
    letter-spacing: 0.05em;
    transition: all 0.2s;
  }

  .principle::before {
    content: attr(data-n);
    position: absolute;
    top: 10px;
    right: 14px;
    font-size: 20px;
    font-weight: 700;
    color: var(--faint);
    font-family: var(--head);
    line-height: 1;
  }

  .principle:hover {
    border-color: var(--gtr-red-dim);
    background: rgba(200,57,43,0.05);
  }

  /* ─── TECH STACK — RPM GAUGES ─── */
  .stack {
    margin-bottom: 56px;
  }

  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2px;
  }

  .stack-group {
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 20px;
  }

  .stack-group-title {
    font-family: var(--mono);
    font-size: 9px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gtr-red);
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  .skill-pill {
    display: inline-block;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--gtr-silver);
    background: var(--faint);
    border: 1px solid var(--border);
    padding: 4px 10px;
    margin: 3px 2px;
    letter-spacing: 0.06em;
    clip-path: polygon(4px 0%, 100% 0%, calc(100% - 4px) 100%, 0% 100%);
    transition: all 0.15s;
  }
  .skill-pill:hover {
    color: var(--gtr-chrome);
    border-color: var(--gtr-red-dim);
    background: rgba(200,57,43,0.07);
  }

  /* ─── BUILDS — DATA PANELS ─── */
  .builds {
    margin-bottom: 56px;
  }

  .build-card {
    border: 1px solid var(--border);
    background: var(--panel);
    margin-bottom: 2px;
    padding: 24px 28px;
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 0 28px;
    align-items: start;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }

  .build-card::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--gtr-red);
    transform: scaleY(0);
    transition: transform 0.25s ease;
    transform-origin: bottom;
  }

  .build-card:hover::before { transform: scaleY(1); }
  .build-card:hover { border-color: var(--gtr-red-dim); }

  .build-num {
    font-family: var(--head);
    font-size: 36px;
    font-weight: 900;
    color: var(--faint);
    line-height: 1;
    user-select: none;
    transition: color 0.2s;
    min-width: 52px;
  }

  .build-card:hover .build-num { color: var(--gtr-red-dim); }

  .build-title {
    font-family: var(--head);
    font-size: 20px;
    font-weight: 700;
    color: var(--gtr-chrome);
    margin-bottom: 6px;
    letter-spacing: 0.02em;
  }

  .build-desc {
    font-family: var(--body);
    font-size: 15px;
    color: var(--gtr-silver);
    line-height: 1.6;
    margin-bottom: 10px;
  }

  .build-tag {
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.15em;
    color: var(--gtr-red);
    text-transform: uppercase;
    border: 1px solid var(--gtr-red-dim);
    padding: 2px 8px;
    margin-right: 6px;
    display: inline-block;
    background: rgba(200,57,43,0.06);
    clip-path: polygon(3px 0%, 100% 0%, calc(100% - 3px) 100%, 0% 100%);
  }

  /* ─── RESEARCH ─── */
  .research {
    margin-bottom: 56px;
  }

  .research-list {
    list-style: none;
  }

  .research-item {
    display: flex;
    align-items: baseline;
    gap: 16px;
    padding: 14px 0;
    border-bottom: 1px solid var(--border);
    font-family: var(--body);
    font-size: 15px;
    color: var(--gtr-silver);
    transition: color 0.2s;
  }

  .research-item:hover { color: var(--gtr-chrome); }

  .research-item::before {
    content: '◆';
    font-size: 8px;
    color: var(--gtr-red);
    flex-shrink: 0;
    position: relative;
    top: -1px;
  }

  /* ─── BUILD PRINCIPLES ─── */
  .build-principles {
    margin-bottom: 56px;
  }

  .principles-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
  }

  .bp-item {
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 20px 24px;
    font-family: var(--body);
    font-size: 15px;
    color: var(--gtr-silver);
    line-height: 1.6;
    position: relative;
    padding-left: 36px;
    transition: all 0.2s;
  }

  .bp-item::before {
    content: '//';
    position: absolute;
    left: 14px;
    top: 20px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--gtr-red);
    letter-spacing: -2px;
  }

  .tier-label {
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--muted);
    padding: 18px 0 10px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .tier-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .build-status-live {
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.15em;
    color: #7fba5a;
    text-transform: uppercase;
    margin-left: 4px;
    display: inline-block;
  }

  .compact-card { padding: 16px 22px; }
  .compact-card .build-desc { font-size: 13px; margin-bottom: 8px; }

  .bp-item:hover {
    border-color: var(--gtr-red-dim);
    color: var(--gtr-chrome);
  }

  /* ─── STATUS / FOOTER ─── */
  .status {
    margin-top: 64px;
    padding: 32px;
    border: 1px solid var(--border);
    background: var(--panel);
    text-align: center;
    position: relative;
    clip-path: polygon(12px 0%, 100% 0%, calc(100% - 12px) 100%, 0% 100%);
  }

  .status-line {
    font-family: var(--head);
    font-size: clamp(18px, 3vw, 26px);
    font-weight: 700;
    color: var(--gtr-chrome);
    margin-bottom: 6px;
    letter-spacing: 0.04em;
  }

  .status-line span {
    color: var(--gtr-red);
  }

  .status-sub {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-top: 16px;
    padding-top: 14px;
    border-top: 1px solid var(--border);
  }

  /* CORNER MARKS */
  .corner-mark {
    position: absolute;
    width: 12px;
    height: 12px;
    border-color: var(--gtr-red-dim);
    border-style: solid;
  }
  .cm-tl { top: -1px; left: -1px; border-width: 2px 0 0 2px; }
  .cm-tr { top: -1px; right: -1px; border-width: 2px 2px 0 0; }
  .cm-bl { bottom: -1px; left: -1px; border-width: 0 0 2px 2px; }
  .cm-br { bottom: -1px; right: -1px; border-width: 0 2px 2px 0; }

  /* TELEMETRY BAR */
  .telemetry {
    display: flex;
    gap: 0;
    margin-bottom: 48px;
    font-family: var(--mono);
    font-size: 10px;
    letter-spacing: 0.1em;
    border: 1px solid var(--border);
    overflow: hidden;
  }

  .telem-item {
    flex: 1;
    padding: 10px 16px;
    border-right: 1px solid var(--border);
    display: flex;
    flex-direction: column;
    gap: 4px;
    background: var(--panel);
  }

  .telem-item:last-child { border-right: none; }
  .telem-label { color: var(--muted); font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase; }
  .telem-value { color: var(--gtr-chrome); font-size: 16px; font-family: var(--head); font-weight: 700; letter-spacing: 0.05em; }
  .telem-value span { color: var(--gtr-red); font-size: 10px; }

  /* ANIMATIONS */
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  .blink { animation: blink 2s ease-in-out infinite; }

  @keyframes scan {
    0% { top: -2px; }
    100% { top: 100%; }
  }

  .hero::after {
    content: '';
    position: absolute;
    left: 0; right: 0;
    height: 80px;
    background: linear-gradient(0deg, transparent, rgba(140,80,255,0.05), transparent);
    top: -80px;
    animation: scan 6s linear infinite;
    pointer-events: none;
  }

  @media (max-width: 600px) {
    .principles-grid { grid-template-columns: 1fr; }
    .build-card { grid-template-columns: 1fr; gap: 8px; }
    .build-num { font-size: 24px; }
    .telemetry { flex-wrap: wrap; }
    .telem-item { min-width: 50%; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <header class="hero">
    <div class="hero-top">
      <div>
        <div class="chassis-id">BNR34 · MIDNIGHT PURPLE II · TE37 GOLD</div>
        <h1 class="hero-name">M. <span>Shashank</span></h1>
        <p class="tagline">
          <strong>High-Performance Systems</strong> &nbsp;·&nbsp; AI / ML &nbsp;·&nbsp; Full-Stack Engineering<br/>
          <strong>Student by timeline. Engineer by default. Systems thinker by habit.</strong>
        </p>
        <div class="links-bar">
          <a href="https://portfolio1-steel-kappa.vercel.app/" target="_blank">Portfolio</a>
          <a href="https://www.linkedin.com/in/shashank-murari-rb26dett/" target="_blank">LinkedIn</a>
          <a href="https://scholar.google.com/citations?user=YOUR_ID" target="_blank">Scholar</a>
        </div>
      </div>
      <div class="gtr-badge blink">GTR&nbsp;MODE&nbsp;ACTIVE</div>
    </div>
  </header>

  <!-- TELEMETRY BAR -->
  <div class="telemetry">
    <div class="telem-item">
      <div class="telem-label">Stack Depth</div>
      <div class="telem-value">4 <span>Layers</span></div>
    </div>
    <div class="telem-item">
      <div class="telem-label">Active Builds</div>
      <div class="telem-value">28 <span>Repos</span></div>
    </div>
    <div class="telem-item">
      <div class="telem-label">Research Papers</div>
      <div class="telem-value">4 <span>Published</span></div>
    </div>
    <div class="telem-item">
      <div class="telem-label">Build Philosophy</div>
      <div class="telem-value">GTR <span>Mode</span></div>
    </div>
  </div>

  <!-- PHILOSOPHY -->
  <section class="philosophy">
    <div class="section-label">Platform Philosophy</div>
    <div class="philosophy-quote">
      The Nissan GTR wasn't built to be flashy.<br/>
      It was built to <em>outperform machines twice its price</em><br/>
      through engineering discipline.
    </div>
    <div class="principles">
      <div class="principle" data-n="01">Systems over scripts</div>
      <div class="principle" data-n="02">Explainability over magic</div>
      <div class="principle" data-n="03">Reliability over demos</div>
      <div class="principle" data-n="04">Performance where it matters</div>
    </div>
  </section>

  <div class="stripe"></div>

  <!-- TECH STACK -->
  <section class="stack">
    <div class="section-label">Engineering Stack</div>
    <div class="stack-grid">
      <div class="stack-group">
        <div class="stack-group-title">⬡ Powertrain · Core Skills</div>
        <span class="skill-pill">Python</span>
        <span class="skill-pill">TypeScript</span>
        <span class="skill-pill">SQL</span>
        <span class="skill-pill">C</span>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">⬡ Chassis · Frameworks</div>
        <span class="skill-pill">React</span>
        <span class="skill-pill">FastAPI</span>
        <span class="skill-pill">Node.js</span>
        <span class="skill-pill">Expo</span>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">⬡ Control Systems · AI / ML</div>
        <span class="skill-pill">XGBoost</span>
        <span class="skill-pill">ANN</span>
        <span class="skill-pill">SHAP</span>
        <span class="skill-pill">Model Eval</span>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">⬡ Track Env · Infrastructure</div>
        <span class="skill-pill">Linux</span>
        <span class="skill-pill">Docker</span>
        <span class="skill-pill">Git</span>
        <span class="skill-pill">Cloud-Native</span>
      </div>
    </div>
  </section>

  <div class="stripe"></div>

  <!-- BUILDS -->
  <section class="builds">
    <div class="section-label">Garage — Full Build Log</div>

    <div class="tier-label">▸ Flagship Builds</div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">01</div>
      <div>
        <div class="build-title">AgriHub v2</div>
        <div class="build-desc">Full-stack AI-driven platform for Indian agriculture — enabling farmers, researchers, and agri-stakeholders with insights, tools, and data-driven decision support. Expo mobile app + FastAPI backend + marketplace architecture.</div>
        <span class="build-tag">AI / ML</span>
        <span class="build-tag">Expo</span>
        <span class="build-tag">FastAPI</span>
        <span class="build-tag">Full-Stack</span>
        <span class="build-status-live">● ACTIVE</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">02</div>
      <div>
        <div class="build-title">Verdic AI 2.0</div>
        <div class="build-desc">Second-generation AI-powered legal case management and intelligence platform. Scalable architecture, structured workflows, AI-assisted legal insights. Built to replace the prototype with production-grade systems.</div>
        <span class="build-tag">NLP</span>
        <span class="build-tag">Legal Tech</span>
        <span class="build-tag">Systems Design</span>
        <span class="build-tag">TypeScript</span>
        <span class="build-status-live">● ACTIVE</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">03</div>
      <div>
        <div class="build-title">E.R. Homie</div>
        <div class="build-desc">Private platform — embrace-home. Systems-first home intelligence build. Details under wraps.</div>
        <span class="build-tag">Private</span>
        <span class="build-tag">TypeScript</span>
        <span class="build-status-live">● ACTIVE</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">04</div>
      <div>
        <div class="build-title">DSC BluePrints 2026</div>
        <div class="build-desc">Official website for BluePrints 2026 — private, in active development. Event-scale platform build.</div>
        <span class="build-tag">Private</span>
        <span class="build-tag">TypeScript</span>
        <span class="build-status-live">● ACTIVE</span>
      </div>
    </div>

    <div class="tier-label">▸ Shipped Builds</div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">05</div>
      <div>
        <div class="build-title">Beneficiary Credit Scoring</div>
        <div class="build-desc">AI/ML-based credit scoring with income verification using alternative consumption data. Explainable risk-based direct digital lending — SHAP-driven transparency, not black-box decisions.</div>
        <span class="build-tag">XGBoost</span>
        <span class="build-tag">SHAP</span>
        <span class="build-tag">Fintech</span>
        <span class="build-tag">Python</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">06</div>
      <div>
        <div class="build-title">Jharkhand Tourism Platform</div>
        <div class="build-desc">AI-powered digital tourism for Jharkhand — personalized itineraries, verified local services, sustainable community-driven experiences. Includes a separate provider registration platform.</div>
        <span class="build-tag">AI</span>
        <span class="build-tag">Geo</span>
        <span class="build-tag">Sustainability</span>
        <span class="build-tag">TypeScript</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">07</div>
      <div>
        <div class="build-title">Zobot Fusion</div>
        <div class="build-desc">AI-powered skill, productivity, and support engine integrated with Zoho SalesIQ Zobot. Intelligent automation and insights pipeline for enterprise sales workflows.</div>
        <span class="build-tag">AI Agents</span>
        <span class="build-tag">Zoho</span>
        <span class="build-tag">Automation</span>
        <span class="build-tag">TypeScript</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">08</div>
      <div>
        <div class="build-title">Place-Me</div>
        <div class="build-desc">Placement and opportunity discovery platform. TypeScript-based, focused on structured job-match workflows.</div>
        <span class="build-tag">TypeScript</span>
        <span class="build-tag">Platform</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">09</div>
      <div>
        <div class="build-title">Jarvis</div>
        <div class="build-desc">Python-based personal automation assistant. Local intelligence layer — command-driven, no fluff.</div>
        <span class="build-tag">Python</span>
        <span class="build-tag">Automation</span>
        <span class="build-tag">CLI</span>
      </div>
    </div>

    <div class="tier-label">▸ Research & ML Builds</div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">10</div>
      <div>
        <div class="build-title">Credit Risk Assessment — IITM Hackathon</div>
        <div class="build-desc">Real-time credit risk assessment system built for IITM Hackathon PS3. Full data pipeline, feature engineering, and ML models under competitive constraints.</div>
        <span class="build-tag">Python</span>
        <span class="build-tag">ML Pipeline</span>
        <span class="build-tag">Hackathon</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">11</div>
      <div>
        <div class="build-title">Moon Craters &amp; Boulders Detector</div>
        <div class="build-desc">Python application analyzing lunar surface imagery to detect craters and boulders. Preprocessing, model inference, and a lightweight web-app interface for results.</div>
        <span class="build-tag">CV</span>
        <span class="build-tag">Python</span>
        <span class="build-tag">Inference</span>
      </div>
    </div>

    <div class="build-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">12</div>
      <div>
        <div class="build-title">Loan Payment Prediction Model</div>
        <div class="build-desc">ML model predicting loan repayment outcomes — on-time vs overdue/default — using historical financial and applicant data.</div>
        <span class="build-tag">ML</span>
        <span class="build-tag">Fintech</span>
        <span class="build-tag">Classification</span>
      </div>
    </div>

    <div class="tier-label">▸ Portfolio & Interface Experiments</div>

    <div class="build-card compact-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">13</div>
      <div>
        <div class="build-title">GTR-R34 Skyline Portfolio</div>
        <div class="build-desc">Nissan R34 GT-R themed personal portfolio — this aesthetic, shipped as a site.</div>
        <span class="build-tag">TypeScript</span><span class="build-tag">Design</span>
      </div>
    </div>

    <div class="build-card compact-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">14</div>
      <div>
        <div class="build-title">Portfolio CLI</div>
        <div class="build-desc">Linux terminal-themed portfolio — navigate experience through a command-line interface.</div>
        <span class="build-tag">TypeScript</span><span class="build-tag">CLI</span>
      </div>
    </div>

    <div class="build-card compact-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">15</div>
      <div>
        <div class="build-title">EventHub — ECLearnix</div>
        <div class="build-desc">React event listing app with filtering, scheduling, speaker views, and FAQ system.</div>
        <span class="build-tag">React</span><span class="build-tag">TypeScript</span>
      </div>
    </div>

    <div class="build-card compact-card">
      <div class="corner-mark cm-tl"></div><div class="corner-mark cm-br"></div>
      <div class="build-num">16</div>
      <div>
        <div class="build-title">Supermarket Billing System</div>
        <div class="build-desc">Python billing app with database-backed inventory and real-world retail transaction simulation.</div>
        <span class="build-tag">Python</span><span class="build-tag">DB</span>
      </div>
    </div>

  </section>

  <div class="stripe"></div>

  <!-- RESEARCH -->
  <section class="research">
    <div class="section-label">R&amp;D Division — Research Output</div>
    <p style="font-family: var(--mono); font-size: 12px; color: var(--muted); margin-bottom: 24px; letter-spacing: 0.05em;">Research treated as an R&amp;D division — useful only if it ships.</p>
    <ul class="research-list">
      <li class="research-item">Machine Learning &amp; Data Analytics for Sustainable Environment</li>
      <li class="research-item">AGRIHUB: AI for Indian Agriculture</li>
      <li class="research-item">EcoTrack: Smart Waste Collection Navigator</li>
      <li class="research-item">Gesture Interpretation into Tamil Linguistics using ANN</li>
    </ul>
  </section>

  <div class="stripe"></div>

  <!-- BUILD PRINCIPLES -->
  <section class="build-principles">
    <div class="section-label">Build Principles</div>
    <div class="principles-grid">
      <div class="bp-item">Architect for failure, not success</div>
      <div class="bp-item">Make systems debuggable before making them clever</div>
      <div class="bp-item">If it can't be explained, it can't be trusted</div>
      <div class="bp-item">Research without deployment is unfinished work</div>
    </div>
  </section>

  <!-- STATUS -->
  <div class="status">
    <div class="corner-mark cm-tl"></div>
    <div class="corner-mark cm-tr"></div>
    <div class="corner-mark cm-bl"></div>
    <div class="corner-mark cm-br"></div>
    <div class="status-line">Student by timeline. <span>Engineer</span> by default.</div>
    <div class="status-line">Systems thinker <span>by habit</span>.</div>
    <div class="status-sub">GTR isn't a car. It's a design mindset. &nbsp;◆&nbsp; MIDNIGHT PURPLE II · TE37 GOLD · RB26DETT</div>
  </div>

</div>
</body>
</html>
