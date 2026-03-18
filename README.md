[index.html](https://github.com/user-attachments/files/26086144/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zeyad Elsayed | Network & Security Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #050a0f;
    --surface: #0a1520;
    --border: #0f2535;
    --accent: #00d4ff;
    --accent2: #00ff88;
    --text: #c8dde8;
    --muted: #4a6a7a;
    --white: #e8f4f8;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    overflow-x: hidden;
  }

  /* Grid background */
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

  /* Glow orb */
  body::after {
    content: '';
    position: fixed;
    top: -200px;
    right: -200px;
    width: 600px;
    height: 600px;
    background: radial-gradient(circle, rgba(0,212,255,0.08) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }

  /* NAV */
  nav {
    padding: 1.5rem 0;
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    background: rgba(5,10,15,0.9);
    backdrop-filter: blur(12px);
    z-index: 100;
  }

  nav .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    color: var(--accent);
    letter-spacing: 0.1em;
  }

  .logo span { color: var(--muted); }

  nav ul {
    list-style: none;
    display: flex;
    gap: 2rem;
  }

  nav a {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.1em;
    transition: color 0.3s;
  }

  nav a:hover { color: var(--accent); }

  /* HERO */
  .hero {
    padding: 8rem 0 6rem;
    position: relative;
  }

  .hero-tag {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--accent2);
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .hero-tag::before {
    content: '';
    display: inline-block;
    width: 30px;
    height: 1px;
    background: var(--accent2);
  }

  h1 {
    font-size: clamp(3rem, 8vw, 6rem);
    font-weight: 800;
    line-height: 0.95;
    color: var(--white);
    margin-bottom: 1.5rem;
  }

  h1 .line2 {
    color: var(--accent);
    display: block;
    -webkit-text-stroke: 1px var(--accent);
    color: transparent;
  }

  .hero-desc {
    font-size: 1.1rem;
    color: var(--muted);
    max-width: 540px;
    line-height: 1.7;
    margin-bottom: 2.5rem;
  }

  .hero-links {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn {
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    padding: 0.8rem 1.8rem;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: all 0.3s;
    border: 1px solid;
  }

  .btn-primary {
    background: var(--accent);
    color: var(--bg);
    border-color: var(--accent);
  }

  .btn-primary:hover {
    background: transparent;
    color: var(--accent);
  }

  .btn-outline {
    background: transparent;
    color: var(--text);
    border-color: var(--border);
  }

  .btn-outline:hover {
    border-color: var(--accent);
    color: var(--accent);
  }

  /* STATUS BADGE */
  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent2);
    background: rgba(0,255,136,0.08);
    border: 1px solid rgba(0,255,136,0.2);
    padding: 0.4rem 0.8rem;
    letter-spacing: 0.1em;
    margin-bottom: 2rem;
  }

  .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--accent2);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  /* SECTION */
  section { padding: 5rem 0; }

  .section-header {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 3rem;
  }

  .section-num {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent);
    letter-spacing: 0.2em;
  }

  h2 {
    font-size: 2rem;
    font-weight: 800;
    color: var(--white);
  }

  .section-header::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    margin-left: 1rem;
  }

  /* SKILLS GRID */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .skill-card {
    background: var(--surface);
    padding: 2rem;
    transition: background 0.3s;
  }

  .skill-card:hover { background: #0d1e2e; }

  .skill-icon {
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .skill-card h3 {
    font-size: 0.85rem;
    color: var(--accent);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1rem;
    font-family: 'Space Mono', monospace;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .tag {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    padding: 0.25rem 0.6rem;
    background: rgba(0,212,255,0.06);
    border: 1px solid rgba(0,212,255,0.15);
    color: var(--text);
    letter-spacing: 0.05em;
  }

  /* EXPERIENCE */
  .exp-timeline { position: relative; }

  .exp-timeline::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), var(--border));
  }

  .exp-item {
    padding-left: 2.5rem;
    margin-bottom: 3rem;
    position: relative;
    animation: fadeUp 0.6s ease both;
  }

  .exp-item::before {
    content: '';
    position: absolute;
    left: -4px;
    top: 6px;
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 12px var(--accent);
  }

  .exp-date {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent2);
    letter-spacing: 0.1em;
    margin-bottom: 0.4rem;
  }

  .exp-title {
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 0.25rem;
  }

  .exp-org {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--muted);
    margin-bottom: 1rem;
    letter-spacing: 0.05em;
  }

  .exp-desc {
    font-size: 0.9rem;
    color: var(--text);
    line-height: 1.7;
  }

  .exp-bullets {
    list-style: none;
    margin-top: 0.75rem;
  }

  .exp-bullets li {
    font-size: 0.85rem;
    color: var(--text);
    line-height: 1.6;
    padding: 0.2rem 0;
    padding-left: 1rem;
    position: relative;
  }

  .exp-bullets li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--accent);
  }

  /* CERTIFICATIONS */
  .cert-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1rem;
  }

  .cert-card {
    border: 1px solid var(--border);
    padding: 1.5rem;
    background: var(--surface);
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }

  .cert-card:hover { border-color: var(--accent); }

  .cert-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s;
  }

  .cert-card:hover::before { transform: scaleX(1); }

  .cert-badge {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    color: var(--accent);
    background: rgba(0,212,255,0.08);
    border: 1px solid rgba(0,212,255,0.2);
    padding: 0.2rem 0.5rem;
    display: inline-block;
    margin-bottom: 0.75rem;
    letter-spacing: 0.1em;
  }

  .cert-card h3 {
    font-size: 1rem;
    color: var(--white);
    margin-bottom: 0.25rem;
  }

  .cert-card p {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  /* CONTACT */
  .contact-section {
    border-top: 1px solid var(--border);
    padding: 5rem 0;
  }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .contact-text h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }

  .contact-text p {
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 2rem;
  }

  .contact-items { display: flex; flex-direction: column; gap: 1rem; }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    color: var(--text);
  }

  .contact-item .ci-label {
    color: var(--muted);
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    min-width: 60px;
  }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--border);
    padding: 1.5rem 0;
    text-align: center;
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 0.1em;
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .fade-in {
    animation: fadeUp 0.8s ease both;
  }

  .fade-in:nth-child(1) { animation-delay: 0.1s; }
  .fade-in:nth-child(2) { animation-delay: 0.2s; }
  .fade-in:nth-child(3) { animation-delay: 0.3s; }
  .fade-in:nth-child(4) { animation-delay: 0.4s; }

  /* Scanline effect */
  .hero::after {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, rgba(0,212,255,0.4), transparent);
    animation: scan 4s ease-in-out infinite;
  }

  @keyframes scan {
    0% { top: 0; opacity: 1; }
    100% { top: 100%; opacity: 0; }
  }

  @media (max-width: 768px) {
    .contact-grid { grid-template-columns: 1fr; gap: 2rem; }
    nav ul { display: none; }
    h1 { font-size: 3rem; }
  }

  /* ── HERO ABOUT BLOCK ── */
  .hero-about {
    margin-top: 2.5rem;
    max-width: 640px;
    background: rgba(0,212,255,0.04);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 1.75rem 2rem;
  }

  .hero-about-top {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1.2rem;
  }

  .hero-about-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    color: var(--accent);
  }

  .hero-about-quote {
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--white);
    line-height: 1.5;
    margin-bottom: 1rem;
  }

  .hero-about-desc {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.8;
    margin-bottom: 0;
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
    gap: 1rem;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 2rem;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, background 0.3s;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s;
  }

  .project-card:hover { background: #0d1e2e; border-color: rgba(0,212,255,0.3); }
  .project-card:hover::before { transform: scaleX(1); }

  .project-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1.2rem;
  }

  .project-icon { font-size: 2.2rem; }

  .project-meta { display: flex; gap: 0.5rem; flex-wrap: wrap; justify-content: flex-end; }

  .project-badge {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.08em;
    padding: 0.2rem 0.55rem;
    background: rgba(0,212,255,0.08);
    border: 1px solid rgba(0,212,255,0.2);
    color: var(--accent);
  }

  .badge-green {
    background: rgba(0,255,136,0.08);
    border-color: rgba(0,255,136,0.2);
    color: var(--accent2);
  }

  .project-title {
    font-size: 1.15rem;
    font-weight: 800;
    color: var(--white);
    margin-bottom: 0.75rem;
  }

  .project-desc {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.8;
    margin-bottom: 1.2rem;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 1.5rem;
  }

  .project-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 0.75rem;
    padding-top: 1.2rem;
    border-top: 1px solid var(--border);
  }

  .project-download {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.08em;
    color: var(--bg);
    background: var(--accent);
    padding: 0.5rem 1.2rem;
    text-decoration: none;
    border: 1px solid var(--accent);
    transition: all 0.3s;
  }

  .project-download:hover {
    background: transparent;
    color: var(--accent);
  }

  .project-tool {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  /* ── SERVICES ── */
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .service-card {
    background: var(--surface);
    padding: 2rem;
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
  }

  .service-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s;
  }

  .service-card:hover { background: #0d1e2e; }
  .service-card:hover::before { transform: scaleX(1); }

  .service-icon {
    font-size: 2rem;
    margin-bottom: 1rem;
    display: block;
  }

  .service-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    font-weight: 700;
    color: var(--accent);
    letter-spacing: 0.05em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
  }

  .service-desc {
    font-size: 0.88rem;
    color: var(--muted);
    line-height: 1.8;
    margin-bottom: 1rem;
  }

  .service-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  /* ── LANG TOGGLE ── */
  .usp-top-row {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    margin-bottom: 0;
  }

  .usp-top-row .section-header { margin-bottom: 0 !important; }
  .usp-top-row .section-header::after { display: none; }

  .lang-toggle-wrap {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 0.35rem 0.75rem;
    flex-shrink: 0;
  }

  .lang-btn {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    color: var(--muted);
    background: transparent;
    border: none;
    cursor: pointer;
    padding: 0.2rem 0.4rem;
    transition: color 0.25s;
  }

  .lang-btn.active {
    color: var(--accent);
  }

  .lang-btn:hover { color: var(--accent); }

  .lang-sep {
    color: var(--border);
    font-size: 0.8rem;
    user-select: none;
  }

  /* ── USP SECTION ── */
  .usp-section { padding: 5rem 0; }

  .usp-core-banner {
    background: rgba(0,212,255,0.04);
    border: 1px solid var(--border);
    border-right: 3px solid var(--accent);
    padding: 2rem 2.5rem;
    margin-bottom: 3rem;
    position: relative;
    overflow: hidden;
  }

  .usp-core-banner::after {
    content: 'USP';
    position: absolute;
    left: 1rem;
    top: 50%;
    transform: translateY(-50%);
    font-family: 'Space Mono', monospace;
    font-size: 5rem;
    font-weight: 900;
    color: rgba(0,212,255,0.03);
    pointer-events: none;
  }

  .usp-core-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--accent);
    letter-spacing: 0.15em;
    margin-bottom: 0.75rem;
  }

  .usp-quote-mark {
    font-family: 'Space Mono', monospace;
    font-size: 2.2rem;
    color: var(--accent);
    line-height: 0;
    vertical-align: -0.3em;
    opacity: 0.8;
    margin: 0 4px;
  }

  .usp-core-banner h3 {
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 0.75rem;
    line-height: 1.5;
  }

  .usp-core-banner p {
    font-size: 0.9rem;
    color: var(--muted);
    line-height: 1.85;
    max-width: 680px;
  }

  .usp-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
    gap: 1.5px;
    background: var(--border);
    border: 1px solid var(--border);
    margin-bottom: 3rem;
  }

  .usp-card {
    background: var(--surface);
    padding: 1.75rem;
    transition: background 0.3s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }

  .usp-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s;
  }

  .usp-card:hover { background: #0d1e2e; }
  .usp-card:hover::before { transform: scaleX(1); }

  .usp-num {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    color: var(--accent);
    opacity: 0.5;
    letter-spacing: 0.15em;
    margin-bottom: 0.75rem;
  }

  .usp-icon {
    font-size: 1.8rem;
    margin-bottom: 0.75rem;
    display: block;
  }

  .usp-title {
    font-size: 0.9rem;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 0.6rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    font-size: 0.78rem;
  }

  .usp-desc {
    font-size: 0.85rem;
    color: var(--muted);
    line-height: 1.75;
    margin-bottom: 0.75rem;
  }

  .usp-tag {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    padding: 0.2rem 0.55rem;
    letter-spacing: 0.05em;
  }

  .tag-blue  { background: rgba(0,212,255,0.08); color: var(--accent); border: 1px solid rgba(0,212,255,0.2); }
  .tag-orange{ background: rgba(255,107,53,0.1); color: #ff6b35; border: 1px solid rgba(255,107,53,0.2); }
  .tag-green { background: rgba(0,255,136,0.08); color: var(--accent2); border: 1px solid rgba(0,255,136,0.2); }
  .tag-gold  { background: rgba(255,215,0,0.08); color: #ffd700; border: 1px solid rgba(255,215,0,0.2); }

  /* Competency bars */
  .usp-skills-wrap { margin-top: 1rem; }

  .usp-skills-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    color: var(--accent);
    margin-bottom: 1.5rem;
  }

  .usp-skill-row {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 0.9rem;
  }

  .usp-skill-name {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--text);
    width: 200px;
    flex-shrink: 0;
    text-align: right;
  }

  .usp-bar-bg {
    flex: 1;
    height: 4px;
    background: rgba(255,255,255,0.06);
    border-radius: 2px;
    overflow: hidden;
  }

  .usp-bar-fill {
    height: 100%;
    border-radius: 2px;
    animation: barGrow 1.4s ease both;
  }

  @keyframes barGrow {
    from { width: 0 !important; }
  }

  .usp-pct {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    color: var(--accent);
    width: 36px;
    flex-shrink: 0;
  }
</style>
</head>
<body>

<nav>
  <div class="container">
    <div class="logo">ZE<span>//</span>PORTFOLIO</div>
    <ul>
      <li><a href="#about">ABOUT</a></li>
      <li><a href="#skills">SKILLS</a></li>
      <li><a href="#experience">EXPERIENCE</a></li>
      <li><a href="#certs">CERTS</a></li>
      <li><a href="#usp">ABOUT ME</a></li>
      <li><a href="#projects">PROJECTS</a></li>
      <li><a href="#services">SERVICES</a></li>
      <li><a href="#contact">CONTACT</a></li>
    </ul>
  </div>
</nav>

<main>
  <div class="container">

    <!-- HERO -->
    <section class="hero" id="about">
      <div class="status-badge fade-in">
        <span class="dot"></span>
        AVAILABLE FOR WORK · ENTRY-LEVEL
      </div>
      <div class="hero-tag fade-in">Network & Security Engineer</div>
      <h1 class="fade-in">ZEYAD<br><span class="line2">ELSAYED</span></h1>

      <p class="hero-desc fade-in">
        Computer Information graduate from Tanta University with CCNA, MCSA, and Network Security certifications. Passionate about enterprise networking, SOC operations, and building secure, resilient IT environments.
      </p>

      <!-- ABOUT ME — inline in hero -->
      <div class="hero-about fade-in" id="usp">

        <!-- Language Toggle -->
        <div class="hero-about-top">
          <span class="hero-about-label lang-en">🎯 ABOUT ME</span>
          <span class="hero-about-label lang-ar" style="display:none; font-family:'Cairo',sans-serif;">🎯 نبذة عني</span>
          <div class="lang-toggle-wrap" style="margin-right:auto;">
            <button class="lang-btn active" id="btnEn" onclick="setLang('en')">EN</button>
            <span class="lang-sep">|</span>
            <button class="lang-btn" id="btnAr" onclick="setLang('ar')">عربي</button>
          </div>
        </div>

        <!-- EN -->
        <p class="hero-about-quote lang-en">
          <span class="usp-quote-mark">"</span>I Am the First Line of Defense — I Detect Threats Before They Cost You<span class="usp-quote-mark">"</span>
        </p>
        <p class="hero-about-desc lang-en">
          I don't just monitor events — I transform chaotic data into actionable security intelligence.
          I combine analytical speed with technical depth to identify real threats from thousands of alerts,
          while maintaining operational continuity and protecting organizational assets around the clock.
        </p>

        <!-- AR -->
        <p class="hero-about-quote lang-ar" style="display:none; direction:rtl; font-family:'Cairo',sans-serif; text-align:right;">
          <span class="usp-quote-mark">"</span>أنا خط الدفاع الأول — أكتشف التهديدات قبل أن تُكلّف<span class="usp-quote-mark">"</span>
        </p>
        <p class="hero-about-desc lang-ar" style="display:none; direction:rtl; font-family:'Cairo',sans-serif; text-align:right;">
          لا أكتفي بمراقبة الأحداث — أحوّل البيانات الفوضوية إلى استخبارات أمنية قابلة للتنفيذ.
          أجمع بين السرعة التحليلية والعمق التقني لتحديد التهديدات الحقيقية من آلاف التنبيهات،
          مع الحفاظ على استمرارية العمليات وحماية أصول المؤسسة على مدار الساعة.
        </p>

      </div>
      <div class="hero-links fade-in">
        <a href="#contact" class="btn btn-primary">GET IN TOUCH</a>
        <a href="#experience" class="btn btn-outline">VIEW EXPERIENCE</a>
      </div>
    </section>

    <!-- EDUCATION -->
    <section>
      <div class="section-header">
        <span class="section-num">01</span>
        <h2>Education</h2>
      </div>
      <div class="exp-item">
        <div class="exp-date">GRADUATED 2026</div>
        <div class="exp-title">Bachelor of Computers and Information</div>
        <div class="exp-org">Tanta University · Faculty of Computers and Information</div>
        <p class="exp-desc">Relevant coursework: Computer Networks, Operating Systems, Database Management, Information Security.</p>
      </div>
    </section>

    <!-- CERTIFICATIONS -->
    <section id="certs">
      <div class="section-header">
        <span class="section-num">02</span>
        <h2>Certifications</h2>
      </div>
      <div class="cert-grid">
        <div class="cert-card">
          <span class="cert-badge">CISCO</span>
          <h3>CCNA</h3>
          <p>Cisco Certified Network Associate</p>
          <p style="margin-top:0.4rem; color: var(--accent2);">AUC · Aug 2023 – Jan 2024</p>
        </div>
        <div class="cert-card">
          <span class="cert-badge">MICROSOFT</span>
          <h3>MCSA</h3>
          <p>Microsoft Certified Solutions Associate</p>
          <p style="margin-top:0.4rem; color: var(--accent2);">Feb 2024 – Apr 2024</p>
        </div>
        <div class="cert-card">
          <span class="cert-badge">SECURITY</span>
          <h3>Network Security & Cyber Operations</h3>
          <p>Specialized cybersecurity certification</p>
          <p style="margin-top:0.4rem; color: var(--accent2);">May 2024</p>
        </div>
      </div>
    </section>

    <!-- EXPERIENCE -->
    <section id="experience">
      <div class="section-header">
        <span class="section-num">03</span>
        <h2>Experience</h2>
      </div>
      <div class="exp-timeline">
        <div class="exp-item">
          <div class="exp-date">FEB 2025 — PRESENT</div>
          <div class="exp-title">Information Security Analyst Trainee</div>
          <div class="exp-org">Digital Egypt Pioneers Initiative (DEPI) · 6-Month Program</div>
          <p class="exp-desc">Comprehensive training in Infrastructure & Security focusing on Information Security Analysis.</p>
          <ul class="exp-bullets">
            <li>SOC Essential Concepts & Security Operations Management</li>
            <li>Vulnerability Management & Cyber Threat Analysis (IoCs, Attack Methodology)</li>
            <li>Incident Detection with SIEM tools and log analysis</li>
            <li>Incident Response & Management, Reporting & Communication</li>
            <li>Capstone Project with Prompt Engineering focus</li>
          </ul>
        </div>
        <div class="exp-item">
          <div class="exp-date">MAY 2024 — JUL 2024</div>
          <div class="exp-title">Cyber Operations Intern</div>
          <div class="exp-org">National Telecommunication Institute (NTI)</div>
          <p class="exp-desc">Hands-on experience in cybersecurity operations within a real SOC environment.</p>
          <ul class="exp-bullets">
            <li>Monitored network traffic and security alerts using SIEM tools</li>
            <li>Analyzed security logs and investigated suspicious activities</li>
            <li>Assisted implementation of firewall rules, IDS/IPS, and access controls</li>
            <li>Participated in vulnerability assessments and threat detection exercises</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <div class="section-header">
        <span class="section-num">04</span>
        <h2>Technical Skills</h2>
      </div>
      <div class="skills-grid">
        <div class="skill-card fade-in">
          <div class="skill-icon">🌐</div>
          <h3>Networking</h3>
          <div class="skill-tags">
            <span class="tag">TCP/IP</span>
            <span class="tag">OSI Model</span>
            <span class="tag">Routing & Switching</span>
            <span class="tag">VLANs</span>
            <span class="tag">STP</span>
            <span class="tag">HSRP</span>
            <span class="tag">OSPF</span>
            <span class="tag">EIGRP</span>
            <span class="tag">RIP</span>
            <span class="tag">DHCP</span>
            <span class="tag">DNS</span>
            <span class="tag">NAT</span>
            <span class="tag">VPN</span>
            <span class="tag">LAN/WAN</span>
          </div>
        </div>
        <div class="skill-card fade-in">
          <div class="skill-icon">🛡️</div>
          <h3>Network Security</h3>
          <div class="skill-tags">
            <span class="tag">Firewalls</span>
            <span class="tag">IDS/IPS</span>
            <span class="tag">ACLs</span>
            <span class="tag">Port Security</span>
            <span class="tag">SOC Concepts</span>
            <span class="tag">Threat Detection</span>
            <span class="tag">SIEM (Splunk)</span>
            <span class="tag">Incident Response</span>
            <span class="tag">Vulnerability Mgmt</span>
          </div>
        </div>
        <div class="skill-card fade-in">
          <div class="skill-icon">🖥️</div>
          <h3>Windows Server</h3>
          <div class="skill-tags">
            <span class="tag">Active Directory</span>
            <span class="tag">Group Policy</span>
            <span class="tag">DHCP/DNS Server</span>
            <span class="tag">User Management</span>
            <span class="tag">File & Print Services</span>
            <span class="tag">Backup & Recovery</span>
          </div>
        </div>
        <div class="skill-card fade-in">
          <div class="skill-icon">⚙️</div>
          <h3>Tools & Platforms</h3>
          <div class="skill-tags">
            <span class="tag">Cisco Packet Tracer</span>
            <span class="tag">GNS3</span>
            <span class="tag">Wireshark</span>
            <span class="tag">VMware</span>
            <span class="tag">VirtualBox</span>
            <span class="tag">Splunk</span>
            <span class="tag">Cisco IOS</span>
          </div>
        </div>
      </div>
    </section>

    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="section-header">
        <span class="section-num">05</span>
        <h2>Projects</h2>
      </div>
      <div class="projects-grid">

        <div class="project-card">
          <div class="project-header">
            <div class="project-icon">🏥</div>
            <div class="project-meta">
              <span class="project-badge">Cisco Packet Tracer</span>
              <span class="project-badge badge-green">Networking</span>
            </div>
          </div>
          <div class="project-title">Hospital Management Network</div>
          <div class="project-desc">
            A fully designed enterprise network simulation for a hospital environment built in Cisco Packet Tracer. The topology covers multi-department segmentation using VLANs, inter-VLAN routing, DHCP, DNS, and access control policies to ensure secure and reliable communication across hospital departments.
          </div>
          <div class="project-tags">
            <span class="tag">VLANs</span>
            <span class="tag">Routing & Switching</span>
            <span class="tag">DHCP</span>
            <span class="tag">DNS</span>
            <span class="tag">ACLs</span>
            <span class="tag">Network Segmentation</span>
          </div>
          <div class="project-footer">
            <a class="project-download" href="Hospital_Management_Network.pkt" download>
              ⬇ Download .pkt File
            </a>
            <span class="project-tool">Opens in Cisco Packet Tracer</span>
          </div>
        </div>

      </div>
    </section>

    <!-- OFFERED SERVICES -->
    <section id="services">
      <div class="section-header">
        <span class="section-num">06</span>
        <h2>Offered Services</h2>
      </div>
      <div class="services-grid">

        <div class="service-card">
          <div class="service-icon">🛡️</div>
          <div class="service-title">SOC Monitoring & Alert Triage</div>
          <div class="service-desc">Continuous monitoring of security events using SIEM platforms. Triaging alerts, filtering false positives, and escalating confirmed incidents with full documentation.</div>
          <div class="service-tags">
            <span class="tag">Splunk</span><span class="tag">SIEM</span><span class="tag">Log Analysis</span>
          </div>
        </div>

        <div class="service-card">
          <div class="service-icon">🔍</div>
          <div class="service-title">Threat Detection & Hunting</div>
          <div class="service-desc">Proactive identification of hidden threats using IOCs, attack patterns, and MITRE ATT&CK framework to detect adversaries before damage occurs.</div>
          <div class="service-tags">
            <span class="tag">MITRE ATT&CK</span><span class="tag">IOCs</span><span class="tag">Threat Intel</span>
          </div>
        </div>

        <div class="service-card">
          <div class="service-icon">⚡</div>
          <div class="service-title">Incident Response & Handling</div>
          <div class="service-desc">End-to-end incident handling covering containment, eradication, and recovery. Detailed post-incident reports with root cause analysis and remediation steps.</div>
          <div class="service-tags">
            <span class="tag">DFIR</span><span class="tag">Playbooks</span><span class="tag">Reporting</span>
          </div>
        </div>

        <div class="service-card">
          <div class="service-icon">🔒</div>
          <div class="service-title">Vulnerability Assessment</div>
          <div class="service-desc">Scanning and evaluating systems for security weaknesses, misconfigurations, and exploitable vulnerabilities with prioritized remediation recommendations.</div>
          <div class="service-tags">
            <span class="tag">Vulnerability Mgmt</span><span class="tag">Risk Assessment</span>
          </div>
        </div>

        <div class="service-card">
          <div class="service-icon">🌐</div>
          <div class="service-title">Network Security Design</div>
          <div class="service-desc">Designing and implementing secure network architectures with firewalls, IDS/IPS, ACLs, VLANs, and VPNs to protect enterprise infrastructure.</div>
          <div class="service-tags">
            <span class="tag">Firewalls</span><span class="tag">IDS/IPS</span><span class="tag">VPN</span><span class="tag">ACLs</span>
          </div>
        </div>

        <div class="service-card">
          <div class="service-icon">📊</div>
          <div class="service-title">Security Reporting & Documentation</div>
          <div class="service-desc">Creating clear technical and executive security reports, incident summaries, and risk assessments tailored to both technical teams and management stakeholders.</div>
          <div class="service-tags">
            <span class="tag">Technical Reports</span><span class="tag">Executive Briefs</span>
          </div>
        </div>

      </div>
    </section>

  </div><!-- /container -->



  <script>
    // Load Cairo font for Arabic
    var cairoLink = document.createElement('link');
    cairoLink.rel = 'stylesheet';
    cairoLink.href = 'https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap';
    document.head.appendChild(cairoLink);

    function setLang(lang) {
      var enEls = document.querySelectorAll('.lang-en');
      var arEls = document.querySelectorAll('.lang-ar');
      var btnEn = document.getElementById('btnEn');
      var btnAr = document.getElementById('btnAr');

      if (lang === 'ar') {
        enEls.forEach(function(el) { el.style.display = 'none'; });
        arEls.forEach(function(el) { el.style.display = ''; });
        btnAr.classList.add('active');
        btnEn.classList.remove('active');
        document.getElementById('usp').setAttribute('dir', 'rtl');
      } else {
        arEls.forEach(function(el) { el.style.display = 'none'; });
        enEls.forEach(function(el) { el.style.display = ''; });
        btnEn.classList.add('active');
        btnAr.classList.remove('active');
        document.getElementById('usp').setAttribute('dir', 'ltr');
      }
    }
  </script>

  <!-- CONTACT -->
  <section class="contact-section" id="contact">
    <div class="container">
      <div class="contact-grid">
        <div class="contact-text">
          <div class="hero-tag">Let's Connect</div>
          <h2>Open to Opportunities</h2>
          <p>Actively seeking entry-level SOC or Network Security roles. Ready to contribute to enterprise IT environments and grow within a motivated team.</p>
          <a href="/cdn-cgi/l/email-protection#98e2e1f9fcf9f4ebe1fca9a1aad8fff5f9f1f4b6fbf7f5" class="btn btn-primary">SEND EMAIL</a>
        </div>
        <div class="contact-items">
          <div class="contact-item">
            <span class="ci-label">EMAIL</span>
            <span><a href="/cdn-cgi/l/email-protection#f48e8d95909598878d90c5cdc6b49399959d98da979b99" style="color:inherit; text-decoration:none;"><span class="__cf_email__" data-cfemail="4f35362e2b2e233c362b7e767d0f28222e2623612c2022">[email&#160;protected]</span></a></span>
          </div>
          <div class="contact-item">
            <span class="ci-label">PHONE</span>
            <span>01001234298</span>
          </div>
          <div class="contact-item">
            <span class="ci-label">LOCATION</span>
            <span>Egypt</span>
          </div>
          <div class="contact-item">
            <span class="ci-label">STATUS</span>
            <span style="color:var(--accent2);">Available · Open to Work</span>
          </div>
          <div class="contact-item">
            <span class="ci-label">LANGS</span>
            <span>Arabic (Native) · English (Very Good)</span>
          </div>
        </div>
          
