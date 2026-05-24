<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bhanu Prakash Rokkam – GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #050810;
    --surface: #0b0f1a;
    --card: #0e1424;
    --border: #1a2540;
    --border-glow: #1e3a6e;
    --accent: #4f8ef7;
    --accent2: #00d4aa;
    --accent3: #f7a84f;
    --accent4: #c084fc;
    --text: #e8edf8;
    --muted: #6b7a9a;
    --dim: #3a4460;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(79,142,247,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79,142,247,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    z-index: 0;
    pointer-events: none;
  }

  .wrapper {
    position: relative;
    z-index: 1;
    max-width: 900px;
    margin: 0 auto;
    padding: 3rem 2rem;
  }

  /* === HERO === */
  .hero {
    text-align: center;
    padding: 4rem 0 3rem;
    position: relative;
  }

  .hero-orb {
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(79,142,247,0.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-tag {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--accent2);
    border: 1px solid rgba(0,212,170,0.3);
    padding: 4px 14px;
    border-radius: 20px;
    margin-bottom: 1.5rem;
    letter-spacing: 2px;
    text-transform: uppercase;
    animation: fadeUp 0.6s ease both;
  }

  .hero h1 {
    font-size: clamp(2.2rem, 5vw, 3.5rem);
    font-weight: 800;
    line-height: 1.1;
    margin-bottom: 1rem;
    animation: fadeUp 0.6s 0.1s ease both;
  }

  .hero h1 .name-glow {
    background: linear-gradient(135deg, #4f8ef7, #00d4aa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-subtitle {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 2rem;
    animation: fadeUp 0.6s 0.2s ease both;
    letter-spacing: 0.5px;
  }

  .hero-subtitle .cursor {
    display: inline-block;
    width: 8px; height: 14px;
    background: var(--accent);
    margin-left: 4px;
    vertical-align: middle;
    animation: blink 1s infinite;
  }

  .hero-badges {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    animation: fadeUp 0.6s 0.3s ease both;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 12px;
    font-weight: 600;
    padding: 6px 14px;
    border-radius: 6px;
    border: 1px solid;
    letter-spacing: 0.3px;
  }

  .badge-blue { color: #93bbfc; border-color: rgba(79,142,247,0.4); background: rgba(79,142,247,0.08); }
  .badge-green { color: #5eead4; border-color: rgba(0,212,170,0.4); background: rgba(0,212,170,0.08); }
  .badge-amber { color: #fbbf24; border-color: rgba(247,168,79,0.4); background: rgba(247,168,79,0.08); }
  .badge-purple { color: #d8b4fe; border-color: rgba(192,132,252,0.4); background: rgba(192,132,252,0.08); }

  /* === SECTION HEADERS === */
  .section {
    margin-top: 4rem;
    animation: fadeUp 0.6s ease both;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 1.5rem;
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border-glow), transparent);
  }

  .section-title {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 3px;
    text-transform: uppercase;
  }

  .section-num {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--dim);
    letter-spacing: 1px;
  }

  /* === ABOUT CARD === */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  .about-item {
    background: var(--card);
    padding: 1.25rem 1.5rem;
    display: flex;
    align-items: flex-start;
    gap: 12px;
  }

  .about-icon {
    font-size: 20px;
    margin-top: 2px;
    flex-shrink: 0;
  }

  .about-label {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 3px;
  }

  .about-value {
    font-size: 13px;
    color: var(--text);
    font-weight: 600;
  }

  /* === TECH STACK === */
  .stack-categories {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .stack-category-label {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .stack-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    padding: 6px 14px;
    border-radius: 6px;
    border: 1px solid var(--border-glow);
    background: var(--card);
    color: var(--text);
    transition: all 0.2s ease;
    cursor: default;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .pill:hover {
    border-color: var(--accent);
    background: rgba(79,142,247,0.1);
    color: #93bbfc;
    transform: translateY(-2px);
  }

  .pill-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* === PROJECTS === */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1rem;
  }

  @media (max-width: 640px) {
    .projects-grid { grid-template-columns: 1fr; }
    .about-grid { grid-template-columns: 1fr; }
  }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }

  .project-card.blue::before { background: linear-gradient(90deg, transparent, #4f8ef7, transparent); }
  .project-card.green::before { background: linear-gradient(90deg, transparent, #00d4aa, transparent); }
  .project-card.purple::before { background: linear-gradient(90deg, transparent, #c084fc, transparent); }

  .project-card:hover {
    border-color: var(--border-glow);
    transform: translateY(-4px);
  }

  .project-emoji {
    font-size: 1.75rem;
    margin-bottom: 12px;
    display: block;
  }

  .project-title {
    font-size: 15px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
  }

  .project-desc {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 14px;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
  }

  .tag {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    border-radius: 4px;
    background: rgba(79,142,247,0.1);
    color: #93bbfc;
    border: 1px solid rgba(79,142,247,0.25);
  }

  .tag.green { background: rgba(0,212,170,0.1); color: #5eead4; border-color: rgba(0,212,170,0.25); }
  .tag.purple { background: rgba(192,132,252,0.1); color: #d8b4fe; border-color: rgba(192,132,252,0.25); }

  /* === PROJECT FEATURES === */
  .feat {
    display: flex;
    align-items: center;
    gap: 6px;
    font-size: 11px;
    color: var(--muted);
    margin-bottom: 4px;
  }

  .feat-dot {
    width: 4px; height: 4px;
    border-radius: 50%;
    background: var(--accent2);
    flex-shrink: 0;
  }

  /* === CERTIFICATIONS === */
  .certs-list {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .cert-item {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    display: flex;
    align-items: center;
    gap: 14px;
    transition: border-color 0.2s;
  }

  .cert-item:hover { border-color: var(--border-glow); }

  .cert-icon {
    width: 36px; height: 36px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    flex-shrink: 0;
  }

  .cert-icon.amber { background: rgba(247,168,79,0.15); }
  .cert-icon.blue { background: rgba(79,142,247,0.15); }
  .cert-icon.green { background: rgba(0,212,170,0.15); }

  .cert-name {
    font-size: 13px;
    font-weight: 600;
    color: var(--text);
  }

  .cert-org {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    margin-top: 2px;
    letter-spacing: 0.5px;
  }

  /* === STATS CARDS === */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-bottom: 1rem;
  }

  .stat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.25rem;
    text-align: center;
  }

  .stat-num {
    font-size: 2rem;
    font-weight: 800;
    line-height: 1;
    margin-bottom: 4px;
  }

  .stat-label {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  /* === GITHUB IMAGES === */
  .gh-images {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .gh-img-row {
    display: flex;
    gap: 12px;
  }

  .gh-img-wrap {
    flex: 1;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    padding: 8px;
  }

  .gh-img-wrap img {
    width: 100%;
    border-radius: 6px;
    display: block;
  }

  .gh-img-wrap.full {
    width: 100%;
  }

  /* === CONNECT === */
  .connect-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .connect-card::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 50% 0%, rgba(79,142,247,0.08) 0%, transparent 60%);
    pointer-events: none;
  }

  .connect-title {
    font-size: 1.4rem;
    font-weight: 800;
    margin-bottom: 8px;
  }

  .connect-sub {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--muted);
    margin-bottom: 1.5rem;
  }

  .connect-links {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 700;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.2s;
  }

  .connect-btn:hover { transform: translateY(-2px); }

  .btn-linkedin { background: rgba(10,102,194,0.15); color: #60a5fa; border-color: rgba(10,102,194,0.4); }
  .btn-github { background: rgba(255,255,255,0.05); color: var(--text); border-color: var(--border-glow); }
  .btn-github:hover { background: rgba(255,255,255,0.1); }

  /* === FOOTER === */
  .footer {
    margin-top: 4rem;
    padding: 2rem 0;
    text-align: center;
    border-top: 1px solid var(--border);
  }

  .footer-quote {
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 8px;
  }

  .footer-quote span {
    background: linear-gradient(135deg, #4f8ef7, #00d4aa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .footer-sub {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    color: var(--dim);
  }

  /* === ANIMATIONS === */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  @keyframes pulse-glow {
    0%, 100% { box-shadow: 0 0 0 0 rgba(79,142,247,0); }
    50% { box-shadow: 0 0 20px 4px rgba(79,142,247,0.15); }
  }

  .animate-pulse { animation: pulse-glow 3s ease infinite; }

  /* Staggered section animations */
  .section:nth-child(1) { animation-delay: 0.1s; }
  .section:nth-child(2) { animation-delay: 0.2s; }
  .section:nth-child(3) { animation-delay: 0.3s; }
  .section:nth-child(4) { animation-delay: 0.4s; }
  .section:nth-child(5) { animation-delay: 0.5s; }
  .section:nth-child(6) { animation-delay: 0.6s; }

  /* === DIVIDER === */
  .divider {
    display: flex;
    align-items: center;
    gap: 12px;
    margin: 3rem 0;
  }
  .divider-line { flex: 1; height: 1px; background: var(--border); }
  .divider-dot { width: 4px; height: 4px; border-radius: 50%; background: var(--accent); }

</style>
</head>
<body>
<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-orb"></div>
    <div class="hero-tag">// Available for Collaboration</div>
    <h1>
      Hi, I'm<br>
      <span class="name-glow">Bhanu Prakash Rokkam</span>
    </h1>
    <p class="hero-subtitle">
      AI &amp; ML Student &nbsp;·&nbsp; Python Developer &nbsp;·&nbsp; Building Real-World AI Solutions
      <span class="cursor"></span>
    </p>
    <div class="hero-badges">
      <span class="badge badge-blue">🎓 B.Tech CSE (AI &amp; ML) · 2027</span>
      <span class="badge badge-green">🏫 ANITS, Vizag</span>
      <span class="badge badge-amber">📍 India</span>
      <span class="badge badge-purple">🌱 Currently Learning</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">01</span>
      <span class="section-title">About</span>
      <div class="section-line"></div>
    </div>
    <div class="about-grid">
      <div class="about-item">
        <span class="about-icon">💡</span>
        <div>
          <div class="about-label">Focus</div>
          <div class="about-value">AI, ML &amp; Automation</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">🛠️</span>
        <div>
          <div class="about-label">Primary Language</div>
          <div class="about-value">Python</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">🚀</span>
        <div>
          <div class="about-label">Currently Exploring</div>
          <div class="about-value">Advanced AI &amp; Full Stack Dev</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">⚡</span>
        <div>
          <div class="about-label">Passion</div>
          <div class="about-value">Real-World AI Solutions</div>
        </div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">02</span>
      <span class="section-title">Tech Stack</span>
      <div class="section-line"></div>
    </div>
    <div class="stack-categories">
      <div>
        <div class="stack-category-label">Languages</div>
        <div class="stack-pills">
          <div class="pill"><span class="pill-dot" style="background:#3776AB"></span>Python</div>
          <div class="pill"><span class="pill-dot" style="background:#ED8B00"></span>Core Java</div>
          <div class="pill"><span class="pill-dot" style="background:#4479A1"></span>MySQL</div>
        </div>
      </div>
      <div>
        <div class="stack-category-label">Web Development</div>
        <div class="stack-pills">
          <div class="pill"><span class="pill-dot" style="background:#E34F26"></span>HTML5</div>
          <div class="pill"><span class="pill-dot" style="background:#1572B6"></span>CSS3</div>
          <div class="pill"><span class="pill-dot" style="background:#F7DF1E"></span>JavaScript</div>
        </div>
      </div>
      <div>
        <div class="stack-category-label">AI / ML Tools</div>
        <div class="stack-pills">
          <div class="pill"><span class="pill-dot" style="background:#5C3EE8"></span>OpenCV</div>
          <div class="pill"><span class="pill-dot" style="background:#013243"></span>NumPy</div>
          <div class="pill"><span class="pill-dot" style="background:#FF4B4B"></span>Streamlit</div>
          <div class="pill"><span class="pill-dot" style="background:#00d4aa"></span>CNN / DNN</div>
          <div class="pill"><span class="pill-dot" style="background:#c084fc"></span>Caffe Models</div>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">03</span>
      <span class="section-title">Featured Projects</span>
      <div class="section-line"></div>
    </div>
    <div class="projects-grid">

      <div class="project-card blue animate-pulse">
        <span class="project-emoji">🌍</span>
        <div class="project-title">Tourism Planner</div>
        <p class="project-desc">AI-powered planner that predicts crowd density and suggests optimal travel timings &amp; alternatives.</p>
        <div style="margin-bottom:12px">
          <div class="feat"><span class="feat-dot"></span>Crowd density prediction</div>
          <div class="feat"><span class="feat-dot"></span>Smart timing suggestions</div>
          <div class="feat"><span class="feat-dot"></span>Alt destination engine</div>
        </div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">HTML</span>
          <span class="tag">CSS</span>
          <span class="tag">JS</span>
        </div>
      </div>

      <div class="project-card green">
        <span class="project-emoji">📈</span>
        <div class="project-title">TradingView MCP Scanner</div>
        <p class="project-desc">AI scanner collecting RSI &amp; OHLCV market data via CDP. Covers crypto, stocks &amp; forex.</p>
        <div style="margin-bottom:12px">
          <div class="feat"><span class="feat-dot" style="background:#4f8ef7"></span>Bullish / Bearish / Neutral</div>
          <div class="feat"><span class="feat-dot" style="background:#4f8ef7"></span>Auto JSON market reports</div>
          <div class="feat"><span class="feat-dot" style="background:#4f8ef7"></span>Multi-asset analysis</div>
        </div>
        <div class="project-tags">
          <span class="tag green">Python</span>
          <span class="tag green">CDP</span>
          <span class="tag green">JSON</span>
        </div>
      </div>

      <div class="project-card purple">
        <span class="project-emoji">🎨</span>
        <div class="project-title">B&amp;W Colorization</div>
        <p class="project-desc">AI colorization system using CNN and OpenCV DNN with a Streamlit web interface.</p>
        <div style="margin-bottom:12px">
          <div class="feat"><span class="feat-dot" style="background:#c084fc"></span>Realistic colorization</div>
          <div class="feat"><span class="feat-dot" style="background:#c084fc"></span>Streamlit web UI</div>
          <div class="feat"><span class="feat-dot" style="background:#c084fc"></span>Caffe model integration</div>
        </div>
        <div class="project-tags">
          <span class="tag purple">OpenCV</span>
          <span class="tag purple">CNN</span>
          <span class="tag purple">Streamlit</span>
        </div>
      </div>

    </div>
  </div>

  <!-- CERTIFICATIONS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">04</span>
      <span class="section-title">Certifications</span>
      <div class="section-line"></div>
    </div>
    <div class="certs-list">
      <div class="cert-item">
        <div class="cert-icon amber">🏅</div>
        <div>
          <div class="cert-name">Prompt Engineering with GitHub</div>
          <div class="cert-org">Simplilearn SkillUp</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon blue">☁️</div>
        <div>
          <div class="cert-name">AWS Generative AI</div>
          <div class="cert-org">AWS Training &amp; Certification</div>
        </div>
      </div>
      <div class="cert-item">
        <div class="cert-icon green">🔐</div>
        <div>
          <div class="cert-name">Intro to Cybersecurity Awareness</div>
          <div class="cert-org">HP LIFE &amp; HP Foundation</div>
        </div>
      </div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">05</span>
      <span class="section-title">GitHub Stats</span>
      <div class="section-line"></div>
    </div>
    <div class="gh-images">
      <div class="gh-img-row">
        <div class="gh-img-wrap">
          <img src="https://github-readme-stats.vercel.app/api?username=prakashh1206&show_icons=true&theme=tokyonight&bg_color=0e1424&title_color=4f8ef7&text_color=e8edf8&icon_color=00d4aa&border_color=1a2540&hide_border=false" alt="GitHub Stats" loading="lazy" />
        </div>
        <div class="gh-img-wrap">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=prakashh1206&layout=compact&theme=tokyonight&bg_color=0e1424&title_color=4f8ef7&text_color=e8edf8&border_color=1a2540" alt="Top Languages" loading="lazy" />
        </div>
      </div>
      <div class="gh-img-wrap full">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=prakashh1206&theme=tokyonight&background=0e1424&stroke=1a2540&ring=4f8ef7&fire=00d4aa&currStreakLabel=4f8ef7&border=1a2540" alt="GitHub Streak" loading="lazy" />
      </div>
      <div class="gh-img-wrap full">
        <img src="https://github-profile-trophy.vercel.app/?username=prakashh1206&theme=onedark&no-bg=true&no-frame=true&column=6&row=1" alt="GitHub Trophies" loading="lazy" />
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-header">
      <span class="section-num">06</span>
      <span class="section-title">Connect</span>
      <div class="section-line"></div>
    </div>
    <div class="connect-card">
      <div class="connect-title">Let's Build Something Together</div>
      <p class="connect-sub">// Open to collaborations, AI projects, and opportunities</p>
      <div class="connect-links">
        <a href="https://linkedin.com/in/bhanuprakashrokkam" class="connect-btn btn-linkedin">
          🔗 LinkedIn
        </a>
        <a href="https://github.com/prakashh1206" class="connect-btn btn-github">
          ⬡ GitHub · prakashh1206
        </a>
      </div>
      <div style="margin-top:16px">
        <img src="https://komarev.com/ghpvc/?username=prakashh1206&color=4f8ef7&style=flat-square&label=PROFILE+VIEWS" alt="Profile Views" />
      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-quote">⭐ <span>"Building AI solutions that solve real-world problems."</span></div>
    <div class="footer-sub">// Bhanu Prakash Rokkam · ANITS, Vizag, India · 2027</div>
  </div>

</div>
</body>
</html>
