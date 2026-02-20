<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Jatothu Bichu – GitHub Profile Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@300;400;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0a0e1a;
    --surface: #0f1629;
    --card: #131a2e;
    --border: #1e2d4d;
    --accent1: #00d4ff;
    --accent2: #7c3aed;
    --accent3: #10b981;
    --accent4: #f59e0b;
    --text: #e2e8f0;
    --muted: #64748b;
    --glow1: rgba(0,212,255,0.15);
    --glow2: rgba(124,58,237,0.15);
  }
  * { margin:0; padding:0; box-sizing:border-box; }
  
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
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 50px 50px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 20px 80px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 60px 20px 40px;
    position: relative;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 50%; transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse, rgba(0,212,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .avatar-ring {
    display: inline-block;
    width: 110px; height: 110px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent1), var(--accent2));
    padding: 3px;
    margin-bottom: 24px;
    animation: spin-ring 8s linear infinite;
    box-shadow: 0 0 30px rgba(0,212,255,0.4);
  }
  .avatar-inner {
    width: 100%; height: 100%;
    border-radius: 50%;
    background: var(--bg);
    display: flex; align-items: center; justify-content: center;
    font-size: 48px;
  }
  @keyframes spin-ring {
    0% { box-shadow: 0 0 20px rgba(0,212,255,0.4), 0 0 60px rgba(0,212,255,0.1); }
    50% { box-shadow: 0 0 40px rgba(124,58,237,0.5), 0 0 80px rgba(124,58,237,0.2); }
    100% { box-shadow: 0 0 20px rgba(0,212,255,0.4), 0 0 60px rgba(0,212,255,0.1); }
  }

  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 800;
    background: linear-gradient(135deg, #fff 0%, var(--accent1) 50%, var(--accent2) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    letter-spacing: -1px;
    margin-bottom: 8px;
  }

  .typing-container {
    height: 36px;
    margin: 16px auto;
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.1rem;
    color: var(--accent1);
  }
  #typing-text::after {
    content: '|';
    animation: blink 0.7s infinite;
    color: var(--accent1);
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  .badge-row {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin: 20px 0;
  }
  .badge {
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 0.75rem;
    font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 0.05em;
    border: 1px solid;
    transition: all 0.3s;
    cursor: default;
  }
  .badge:hover { transform: translateY(-2px); }
  .badge-blue { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.4); color: var(--accent1); }
  .badge-purple { background: rgba(124,58,237,0.1); border-color: rgba(124,58,237,0.4); color: #a78bfa; }
  .badge-green { background: rgba(16,185,129,0.1); border-color: rgba(16,185,129,0.4); color: var(--accent3); }

  .social-links {
    display: flex; gap: 12px; justify-content: center; margin-top: 20px;
  }
  .social-btn {
    display: flex; align-items: center; gap: 8px;
    padding: 10px 20px;
    border-radius: 8px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    font-weight: 600;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.3s;
    cursor: pointer;
  }
  .social-btn:hover { transform: translateY(-3px); }
  .btn-linkedin { background: rgba(0,119,181,0.15); border-color: rgba(0,119,181,0.5); color: #60a5fa; }
  .btn-linkedin:hover { background: rgba(0,119,181,0.3); box-shadow: 0 8px 25px rgba(0,119,181,0.3); }
  .btn-github { background: rgba(255,255,255,0.05); border-color: rgba(255,255,255,0.2); color: #e2e8f0; }
  .btn-github:hover { background: rgba(255,255,255,0.12); box-shadow: 0 8px 25px rgba(255,255,255,0.1); }
  .btn-mail { background: rgba(234,67,53,0.15); border-color: rgba(234,67,53,0.4); color: #f87171; }
  .btn-mail:hover { background: rgba(234,67,53,0.25); box-shadow: 0 8px 25px rgba(234,67,53,0.2); }

  /* ── SECTION ── */
  .section { margin: 40px 0; }
  .section-header {
    display: flex; align-items: center; gap: 12px;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
    position: relative;
  }
  .section-header::after {
    content: '';
    position: absolute;
    bottom: -1px; left: 0;
    width: 60px; height: 2px;
    background: linear-gradient(90deg, var(--accent1), transparent);
  }
  .section-title {
    font-size: 1.15rem;
    font-weight: 700;
    color: #fff;
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }
  .section-icon { font-size: 1.2rem; }

  /* ── SKILLS ── */
  .skills-grid {
    display: flex; flex-wrap: wrap; gap: 10px;
  }
  .skill-chip {
    display: flex; align-items: center; gap: 6px;
    padding: 7px 14px;
    border-radius: 6px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.78rem;
    font-weight: 600;
    border: 1px solid var(--border);
    background: var(--card);
    transition: all 0.3s;
    cursor: default;
    position: relative;
    overflow: hidden;
  }
  .skill-chip::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, transparent, rgba(255,255,255,0.03));
    opacity: 0;
    transition: opacity 0.3s;
  }
  .skill-chip:hover::before { opacity: 1; }
  .skill-chip:hover {
    border-color: var(--accent1);
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(0,212,255,0.15);
    color: var(--accent1);
  }
  .skill-dot {
    width: 8px; height: 8px; border-radius: 50%;
    flex-shrink: 0;
  }

  /* ── STATS CARDS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 14px;
  }
  .stat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent1), var(--accent2));
  }
  .stat-card:hover {
    border-color: rgba(0,212,255,0.3);
    transform: translateY(-4px);
    box-shadow: 0 10px 30px rgba(0,212,255,0.1);
  }
  .stat-num {
    font-family: 'Space Mono', monospace;
    font-size: 2rem;
    font-weight: 700;
    background: linear-gradient(135deg, var(--accent1), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .stat-label {
    font-size: 0.75rem;
    color: var(--muted);
    margin-top: 4px;
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
  }
  @media(max-width:600px){ .projects-grid { grid-template-columns: 1fr; } }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: all 0.3s;
    cursor: pointer;
    position: relative;
    overflow: hidden;
  }
  .project-card::after {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--glow1), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
  .project-card:hover::after { opacity: 1; }
  .project-card:hover {
    border-color: rgba(0,212,255,0.3);
    transform: translateY(-4px);
    box-shadow: 0 15px 35px rgba(0,0,0,0.4);
  }
  .project-icon { font-size: 1.8rem; margin-bottom: 10px; }
  .project-name {
    font-size: 0.95rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 6px;
  }
  .project-desc {
    font-size: 0.78rem;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 12px;
  }
  .project-tags {
    display: flex; flex-wrap: wrap; gap: 6px;
  }
  .project-tag {
    padding: 2px 8px;
    border-radius: 4px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.68rem;
    background: rgba(0,212,255,0.08);
    border: 1px solid rgba(0,212,255,0.2);
    color: var(--accent1);
  }
  .project-meta {
    display: flex; align-items: center; gap: 12px;
    margin-top: 12px; font-size: 0.75rem; color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
  }

  /* ── ACTIVITY ── */
  .activity-bar {
    display: flex; align-items: center; gap: 12px; margin-bottom: 12px;
  }
  .activity-label {
    font-size: 0.78rem;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    min-width: 100px;
    text-align: right;
  }
  .bar-track {
    flex: 1;
    height: 8px;
    background: var(--border);
    border-radius: 4px;
    overflow: hidden;
  }
  .bar-fill {
    height: 100%;
    border-radius: 4px;
    transition: width 1.5s cubic-bezier(0.4,0,0.2,1);
    width: 0;
  }
  .bar-pct {
    font-size: 0.75rem;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    min-width: 36px;
  }

  /* ── STREAK / CONTRIBUTION ── */
  .contribution-grid {
    display: grid;
    grid-template-columns: repeat(52, 1fr);
    gap: 3px;
    margin-top: 10px;
  }
  .contrib-cell {
    aspect-ratio: 1;
    border-radius: 2px;
    background: var(--border);
    transition: all 0.2s;
    cursor: pointer;
  }
  .contrib-cell:hover { transform: scale(1.5); z-index: 10; position: relative; }
  .contrib-0 { background: #161b22; }
  .contrib-1 { background: #0e4429; }
  .contrib-2 { background: #006d32; }
  .contrib-3 { background: #26a641; }
  .contrib-4 { background: #39d353; }

  /* ── INTERESTS ── */
  .interests-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 12px;
  }
  .interest-item {
    display: flex; align-items: center; gap: 12px;
    padding: 14px 16px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    transition: all 0.3s;
  }
  .interest-item:hover {
    border-color: var(--accent1);
    background: rgba(0,212,255,0.05);
    transform: translateX(4px);
  }
  .interest-emoji { font-size: 1.4rem; }
  .interest-text { font-size: 0.85rem; color: var(--text); font-weight: 600; }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 40px 0 0;
    border-top: 1px solid var(--border);
    margin-top: 50px;
  }
  .visitor-badge {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 24px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 30px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    color: var(--muted);
  }
  .visitor-count {
    color: var(--accent1);
    font-weight: 700;
  }

  /* ── COPY README PANEL ── */
  .readme-toggle {
    position: fixed;
    bottom: 24px; right: 24px;
    background: linear-gradient(135deg, var(--accent1), var(--accent2));
    color: #000;
    border: none;
    border-radius: 50px;
    padding: 14px 24px;
    font-family: 'Syne', sans-serif;
    font-size: 0.9rem;
    font-weight: 700;
    cursor: pointer;
    box-shadow: 0 8px 25px rgba(0,212,255,0.4);
    z-index: 100;
    transition: all 0.3s;
  }
  .readme-toggle:hover { transform: scale(1.05); box-shadow: 0 12px 35px rgba(0,212,255,0.5); }

  .readme-panel {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.85);
    z-index: 200;
    display: none;
    align-items: center;
    justify-content: center;
    padding: 20px;
  }
  .readme-panel.open { display: flex; }
  .readme-box {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 16px;
    width: 100%; max-width: 760px;
    max-height: 85vh;
    display: flex; flex-direction: column;
    overflow: hidden;
  }
  .readme-toolbar {
    display: flex; align-items: center; justify-content: space-between;
    padding: 16px 20px;
    border-bottom: 1px solid var(--border);
    background: var(--card);
  }
  .readme-toolbar span {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.85rem;
    color: var(--accent1);
  }
  .toolbar-btns { display: flex; gap: 10px; }
  .copy-btn, .close-btn {
    padding: 7px 16px;
    border-radius: 6px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
    border: none;
    transition: all 0.2s;
  }
  .copy-btn { background: var(--accent1); color: #000; }
  .copy-btn:hover { background: #fff; }
  .close-btn { background: var(--border); color: var(--text); }
  .close-btn:hover { background: #333; }
  .readme-content {
    overflow-y: auto;
    padding: 20px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem;
    line-height: 1.8;
    color: #8b949e;
    white-space: pre-wrap;
    word-break: break-all;
  }
  .readme-content .kw { color: var(--accent1); }

  /* animations */
  .fade-in { opacity: 0; transform: translateY(20px); animation: fadeIn 0.6s forwards; }
  @keyframes fadeIn { to { opacity:1; transform: translateY(0); } }
  .d1{animation-delay:0.1s} .d2{animation-delay:0.2s} .d3{animation-delay:0.3s}
  .d4{animation-delay:0.4s} .d5{animation-delay:0.5s} .d6{animation-delay:0.6s}
</style>
</head>
<body>

<div class="container">

  <!-- HERO -->
  <div class="hero fade-in">
    <div class="avatar-ring">
      <div class="avatar-inner">🤖</div>
    </div>
    <h1>Jatothu Bichu</h1>
    <div class="typing-container">
      <span id="typing-text"></span>
    </div>
    <div class="badge-row">
      <span class="badge badge-blue">🎓 Final Year B.Tech</span>
      <span class="badge badge-purple">🤖 AI & ML Engineer</span>
      <span class="badge badge-green">📍 Hyderabad, India</span>
    </div>
    <div class="social-links">
      <a class="social-btn btn-linkedin" href="#">🔗 LinkedIn</a>
      <a class="social-btn btn-github" href="#">💻 GitHub</a>
      <a class="social-btn btn-mail" href="#">✉ Email</a>
    </div>
  </div>

  <!-- STATS -->
  <div class="section fade-in d1">
    <div class="section-header">
      <span class="section-icon">📊</span>
      <span class="section-title">GitHub Stats</span>
    </div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-num" data-count="96">0</div>
        <div class="stat-label">Contributions</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-count="3">0</div>
        <div class="stat-label">Repositories</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-count="43">0</div>
        <div class="stat-label">Stars Earned</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-count="95">0%</div>
        <div class="stat-label">ML Accuracy</div>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section fade-in d2">
    <div class="section-header">
      <span class="section-icon">💻</span>
      <span class="section-title">Tech Stack</span>
    </div>
    <div class="skills-grid" id="skills-grid"></div>
  </div>

  <!-- LANGUAGE BREAKDOWN -->
  <div class="section fade-in d3">
    <div class="section-header">
      <span class="section-icon">🔥</span>
      <span class="section-title">Language Breakdown</span>
    </div>
    <div id="lang-bars"></div>
  </div>

  <!-- PROJECTS -->
  <div class="section fade-in d4">
    <div class="section-header">
      <span class="section-icon">🚀</span>
      <span class="section-title">Featured Projects</span>
    </div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-icon">🛡️</div>
        <div class="project-name">Adaptive Cyber Threat Detection</div>
        <div class="project-desc">RL agent using Deep Q-Network to detect network intrusions with 95% accuracy in real-time data streams.</div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">RL</span>
          <span class="project-tag">DQN</span>
          <span class="project-tag">TensorFlow</span>
        </div>
        <div class="project-meta">
          <span>⭐ 18</span><span>🔴 HTML</span><span>Final Year</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">🎬</div>
        <div class="project-name">Movie Recommendation System</div>
        <div class="project-desc">Hybrid collaborative + content-based filtering with SVD for personalized movie suggestions.</div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">NLP</span>
          <span class="project-tag">ML</span>
          <span class="project-tag">SVD</span>
        </div>
        <div class="project-meta">
          <span>⭐ 12</span><span>🟡 Python</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon">💬</div>
        <div class="project-name">Anonymous Opinion Website</div>
        <div class="project-desc">Full-stack anonymous feedback platform with privacy-first design and responsive components.</div>
        <div class="project-tags">
          <span class="project-tag">HTML</span>
          <span class="project-tag">CSS</span>
          <span class="project-tag">JavaScript</span>
        </div>
        <div class="project-meta">
          <span>⭐ 7</span><span>🟠 JavaScript</span>
        </div>
      </div>
      <div class="project-card" style="border-style:dashed; opacity:0.6; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:8px; min-height:160px;">
        <div style="font-size:2rem">✨</div>
        <div style="font-size:0.85rem; color:var(--muted)">More coming soon...</div>
      </div>
    </div>
  </div>

  <!-- CONTRIBUTION GRAPH -->
  <div class="section fade-in d5">
    <div class="section-header">
      <span class="section-icon">📈</span>
      <span class="section-title">Contribution Activity</span>
    </div>
    <div class="contribution-grid" id="contrib-grid"></div>
    <div style="display:flex;align-items:center;gap:6px;margin-top:10px;justify-content:flex-end;font-size:0.72rem;color:var(--muted);font-family:'JetBrains Mono',monospace;">
      Less 
      <div style="width:10px;height:10px;border-radius:2px;background:#161b22"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:#0e4429"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:#006d32"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:#26a641"></div>
      <div style="width:10px;height:10px;border-radius:2px;background:#39d353"></div>
      More
    </div>
  </div>

  <!-- INTERESTS -->
  <div class="section fade-in d6">
    <div class="section-header">
      <span class="section-icon">🔍</span>
      <span class="section-title">Areas of Interest</span>
    </div>
    <div class="interests-list">
      <div class="interest-item"><span class="interest-emoji">🤖</span><span class="interest-text">Reinforcement Learning</span></div>
      <div class="interest-item"><span class="interest-emoji">🔐</span><span class="interest-text">Cybersecurity AI</span></div>
      <div class="interest-item"><span class="interest-emoji">💬</span><span class="interest-text">Natural Language Processing</span></div>
      <div class="interest-item"><span class="interest-emoji">📊</span><span class="interest-text">Deep Learning & Neural Nets</span></div>
      <div class="interest-item"><span class="interest-emoji">🌐</span><span class="interest-text">Full Stack Development</span></div>
      <div class="interest-item"><span class="interest-emoji">📡</span><span class="interest-text">Data Science & Analytics</span></div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="visitor-badge">
      👁️ Profile Views: <span class="visitor-count" id="visitor-count">0</span>
    </div>
    <p style="margin-top:16px;font-size:0.75rem;color:var(--muted);font-family:'JetBrains Mono',monospace;">
      ⚡ Building tomorrow's AI, one commit at a time
    </p>
  </div>

</div>

<!-- COPY README BUTTON -->
<button class="readme-toggle" onclick="openReadme()">📋 Copy README.md</button>

<!-- README PANEL -->
<div class="readme-panel" id="readme-panel">
  <div class="readme-box">
    <div class="readme-toolbar">
      <span>📄 README.md — Copy & paste into your GitHub profile repo</span>
      <div class="toolbar-btns">
        <button class="copy-btn" onclick="copyReadme()">⎘ Copy All</button>
        <button class="close-btn" onclick="closeReadme()">✕ Close</button>
      </div>
    </div>
    <div class="readme-content" id="readme-content"></div>
  </div>
</div>

<script>
// ── TYPING ANIMATION ──
const lines = [
  "AI & ML Engineer 🤖",
  "Reinforcement Learning 🎯",
  "Cybersecurity AI 🔐",
  "Building Intelligent Systems ⚡",
  "Python • Java • Deep Learning"
];
let lineIdx = 0, charIdx = 0, deleting = false;
const el = document.getElementById('typing-text');
function type() {
  const cur = lines[lineIdx];
  if (!deleting) {
    el.textContent = cur.slice(0, ++charIdx);
    if (charIdx === cur.length) { deleting = true; setTimeout(type, 1800); return; }
  } else {
    el.textContent = cur.slice(0, --charIdx);
    if (charIdx === 0) { deleting = false; lineIdx = (lineIdx+1) % lines.length; }
  }
  setTimeout(type, deleting ? 40 : 80);
}
type();

// ── SKILLS ──
const skills = [
  {name:"Python",color:"#3670A0"},{name:"Java",color:"#ED8B00"},{name:"C",color:"#00599C"},
  {name:"JavaScript",color:"#F7DF1E"},{name:"HTML5",color:"#E34F26"},{name:"CSS3",color:"#1572B6"},
  {name:"TensorFlow",color:"#FF6F00"},{name:"Keras",color:"#D00000"},{name:"PyTorch",color:"#EE4C2C"},
  {name:"scikit-learn",color:"#F7931E"},{name:"NumPy",color:"#013243"},{name:"Pandas",color:"#150458"},
  {name:"Flask",color:"#00d4ff"},{name:"Spring Boot",color:"#6DB33F"},{name:"MySQL",color:"#4479A1"},
  {name:"SQLite",color:"#07405e"},{name:"Git",color:"#F05033"},{name:"Jupyter",color:"#FA0F00"},
  {name:"Google Colab",color:"#F9A825"},{name:"Deep Learning",color:"#7c3aed"},
  {name:"NLP",color:"#10b981"},{name:"Reinforcement RL",color:"#f59e0b"},
];
const grid = document.getElementById('skills-grid');
skills.forEach(s => {
  const chip = document.createElement('div');
  chip.className = 'skill-chip';
  chip.innerHTML = `<span class="skill-dot" style="background:${s.color}"></span>${s.name}`;
  grid.appendChild(chip);
});

// ── LANGUAGE BARS ──
const langs = [
  {name:"Python", pct:52, color:"#3670A0"},
  {name:"Java", pct:22, color:"#ED8B00"},
  {name:"JavaScript", pct:14, color:"#F7DF1E"},
  {name:"HTML/CSS", pct:8, color:"#E34F26"},
  {name:"C", pct:4, color:"#00599C"},
];
const barsEl = document.getElementById('lang-bars');
langs.forEach(l => {
  barsEl.innerHTML += `
    <div class="activity-bar">
      <span class="activity-label">${l.name}</span>
      <div class="bar-track"><div class="bar-fill" style="background:${l.color}" data-pct="${l.pct}"></div></div>
      <span class="bar-pct">${l.pct}%</span>
    </div>`;
});
setTimeout(() => {
  document.querySelectorAll('.bar-fill').forEach(b => {
    b.style.width = b.dataset.pct + '%';
  });
}, 400);

// ── COUNTER ANIMATION ──
function animateCount(el, target, suffix='') {
  let start = 0, step = target / 50;
  const timer = setInterval(() => {
    start = Math.min(start + step, target);
    el.textContent = Math.floor(start) + suffix;
    if (start >= target) clearInterval(timer);
  }, 30);
}
setTimeout(() => {
  document.querySelectorAll('.stat-num').forEach(el => {
    const count = parseInt(el.dataset.count);
    const suffix = el.dataset.count.includes('%') ? '' : '';
    const orig = el.dataset.count;
    animateCount(el, count, orig.endsWith('%') ? '%' : '');
  });
  animateCount(document.getElementById('visitor-count'), 247);
}, 600);

// ── CONTRIBUTION GRID ──
const cgrid = document.getElementById('contrib-grid');
const levels = [0,0,0,0,1,1,2,2,3,4];
for(let i=0;i<364;i++){
  const cell = document.createElement('div');
  const r = Math.random();
  const lvl = r < 0.6 ? 0 : r < 0.75 ? 1 : r < 0.87 ? 2 : r < 0.95 ? 3 : 4;
  cell.className = `contrib-cell contrib-${lvl}`;
  cgrid.appendChild(cell);
}

// ── README PANEL ──
const readmeText = `<h1 align="center">👋 Hi, I'm Jatothu Bichu</h1>

<h3 align="center">🚀 AI & Machine Learning Engineer</h3>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&pause=1000&color=00D4FF&center=true&width=500&lines=AI+%26+ML+Engineer+%F0%9F%A4%96;Reinforcement+Learning+%F0%9F%8E%AF;Cybersecurity+AI+%F0%9F%94%90;Building+Intelligent+Systems+%E2%9A%A1;Python+%E2%80%A2+Java+%E2%80%A2+Deep+Learning"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/🎓_Final_Year_B.Tech-%230a0e1a?style=for-the-badge&color=00D4FF&labelColor=0f1629"/>
  <img src="https://img.shields.io/badge/🤖_AI_%26_ML_Engineer-%230a0e1a?style=for-the-badge&color=7c3aed&labelColor=0f1629"/>
  <img src="https://img.shields.io/badge/📍_Hyderabad_India-%230a0e1a?style=for-the-badge&color=10b981&labelColor=0f1629"/>
</p>

---

<h3 align="center">🌐 Connect With Me:</h3>
<p align="center">
  <a href="https://linkedin.com/in/bichujatothu">
    <img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://github.com/jatothubichu12-cpu">
    <img src="https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="mailto:jatothubichu12@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

---

<h3 align="center">💻 Tech Stack:</h3>

<p align="center"><b>Languages</b></p>
<p align="center">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54"/>
  <img src="https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white"/>
  <img src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E"/>
  <img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white"/>
</p>

<p align="center"><b>AI / ML Libraries</b></p>
<p align="center">
  <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white"/>
</p>

<p align="center"><b>Frameworks & Tools</b></p>
<p align="center">
  <img src="https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/springboot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white"/>
  <img src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/VS%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google%20Colab-%23F9A825.svg?style=for-the-badge&logo=googlecolab&logoColor=white"/>
</p>

---

<h3 align="center">📊 GitHub Stats:</h3>
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=jatothubichu12-cpu&theme=tokyonight&show_icons=true&hide_border=true&count_private=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=jatothubichu12-cpu&theme=tokyonight&layout=compact&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=jatothubichu12-cpu&theme=tokyonight&hide_border=true"/>
</p>

---

<h3 align="center">🏆 GitHub Trophies:</h3>
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=jatothubichu12-cpu&theme=tokyonight&no-frame=true&column=6&margin-w=4"/>
</p>

---

<h3 align="center">🔍 Areas of Interest:</h3>
<p align="center">
🤖 Reinforcement Learning &nbsp;&nbsp; 🔐 Cybersecurity AI &nbsp;&nbsp; 💬 NLP
</p>
<p align="center">
📊 Deep Learning &nbsp;&nbsp; 🌐 Full Stack Dev &nbsp;&nbsp; 📡 Data Science
</p>

---

<p align="center">
  <img src="https://visitcount.itsvg.in/api?id=jatothubichu12-cpu&icon=0&color=1"/>
</p>

<p align="center">
  <i>⚡ Building tomorrow's AI, one commit at a time</i>
</p>`;

document.getElementById('readme-content').textContent = readmeText;

function openReadme() { document.getElementById('readme-panel').classList.add('open'); }
function closeReadme() { document.getElementById('readme-panel').classList.remove('open'); }
function copyReadme() {
  navigator.clipboard.writeText(readmeText).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ Copied!';
    setTimeout(() => btn.textContent = '⎘ Copy All', 2000);
  });
}
document.getElementById('readme-panel').addEventListener('click', function(e){
  if(e.target === this) closeReadme();
});
</script>
</body>
</html>
`;
