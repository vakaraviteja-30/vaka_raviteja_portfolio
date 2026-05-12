# vaka_raviteja_portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vaka Raviteja — SAP ABAP Developer</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg: #0a0c0f;
  --bg2: #111317;
  --bg3: #171a1f;
  --border: rgba(255,255,255,0.07);
  --border2: rgba(255,255,255,0.12);
  --text: #f0ede8;
  --text2: #9ca3a8;
  --text3: #5c6469;
  --accent: #00e5a0;
  --accent2: #00b87d;
  --accent-glow: rgba(0,229,160,0.15);
  --sap: #0070f3;
  --sap-glow: rgba(0,112,243,0.15);
  --mm: #f59e0b;
  --sd: #0070f3;
  --dd: #a855f7;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
  overflow-x: hidden;
}

/* ── NAV ── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  display: flex; align-items: center; justify-content: space-between;
  padding: 1rem 4rem;
  background: rgba(10,12,15,0.85);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: 'Syne', sans-serif;
  font-weight: 800; font-size: 1.1rem;
  color: var(--text);
  text-decoration: none;
  letter-spacing: -0.02em;
}
.nav-logo span { color: var(--accent); }
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
  text-decoration: none; color: var(--text2);
  font-size: 0.875rem; font-weight: 400;
  transition: color 0.2s;
  letter-spacing: 0.01em;
}
.nav-links a:hover { color: var(--accent); }
.nav-cta {
  background: var(--accent); color: #000;
  padding: 0.5rem 1.25rem; border-radius: 6px;
  text-decoration: none; font-size: 0.85rem; font-weight: 600;
  transition: opacity 0.2s;
}
.nav-cta:hover { opacity: 0.85; }

/* ── HERO ── */
#hero {
  min-height: 100vh;
  display: flex; align-items: center;
  padding: 8rem 4rem 4rem;
  position: relative;
  overflow: hidden;
}
.hero-grid-bg {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
  background-size: 60px 60px;
  mask-image: radial-gradient(ellipse 80% 60% at 50% 50%, black, transparent);
}
.hero-glow {
  position: absolute; top: 20%; left: 10%;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(0,229,160,0.08) 0%, transparent 70%);
  pointer-events: none;
}
.hero-glow2 {
  position: absolute; top: 40%; right: 5%;
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(0,112,243,0.06) 0%, transparent 70%);
  pointer-events: none;
}
.hero-content { position: relative; z-index: 1; max-width: 900px; }
.hero-badge {
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: rgba(0,229,160,0.1); border: 1px solid rgba(0,229,160,0.25);
  color: var(--accent); font-size: 0.8rem; font-weight: 500;
  padding: 0.35rem 0.85rem; border-radius: 100px;
  margin-bottom: 1.5rem; letter-spacing: 0.03em;
}
.hero-badge::before {
  content: ''; display: block;
  width: 6px; height: 6px; border-radius: 50%;
  background: var(--accent);
  animation: pulse 2s ease-in-out infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.7); }
}
.hero-name {
  font-family: 'Syne', sans-serif;
  font-size: clamp(3rem, 7vw, 5.5rem);
  font-weight: 800;
  line-height: 1.0;
  letter-spacing: -0.03em;
  margin-bottom: 0.5rem;
}
.hero-name .line2 { color: var(--accent); }
.hero-title {
  font-family: 'Syne', sans-serif;
  font-size: clamp(1rem, 2.5vw, 1.4rem);
  font-weight: 400;
  color: var(--text2);
  margin-bottom: 1.5rem;
  letter-spacing: 0.02em;
}
.hero-desc {
  font-size: 1.05rem; color: var(--text2);
  max-width: 620px; line-height: 1.75;
  margin-bottom: 2.5rem;
  font-weight: 300;
}
.hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }
.btn-primary {
  background: var(--accent); color: #000;
  padding: 0.8rem 1.75rem; border-radius: 8px;
  text-decoration: none; font-weight: 600; font-size: 0.9rem;
  transition: all 0.2s;
  box-shadow: 0 0 24px rgba(0,229,160,0.3);
}
.btn-primary:hover { transform: translateY(-1px); box-shadow: 0 0 36px rgba(0,229,160,0.4); }
.btn-secondary {
  background: transparent; color: var(--text);
  padding: 0.8rem 1.75rem; border-radius: 8px;
  text-decoration: none; font-weight: 500; font-size: 0.9rem;
  border: 1px solid var(--border2);
  transition: all 0.2s;
}
.btn-secondary:hover { border-color: var(--accent); color: var(--accent); }
.hero-stats {
  display: flex; gap: 3rem; margin-top: 4rem;
  padding-top: 2.5rem;
  border-top: 1px solid var(--border);
}
.stat-item .num {
  font-family: 'Syne', sans-serif;
  font-size: 2rem; font-weight: 800;
  color: var(--accent);
}
.stat-item .label {
  font-size: 0.8rem; color: var(--text3);
  letter-spacing: 0.05em; text-transform: uppercase;
  margin-top: 0.2rem;
}

/* ── SECTION COMMON ── */
section { padding: 6rem 4rem; }
.section-eyebrow {
  font-size: 0.75rem; font-weight: 600;
  color: var(--accent); letter-spacing: 0.12em;
  text-transform: uppercase; margin-bottom: 0.75rem;
}
.section-title {
  font-family: 'Syne', sans-serif;
  font-size: clamp(1.75rem, 4vw, 2.75rem);
  font-weight: 800; line-height: 1.1;
  letter-spacing: -0.02em;
  margin-bottom: 1.25rem;
}
.section-sub {
  font-size: 1rem; color: var(--text2);
  max-width: 560px; line-height: 1.7;
  font-weight: 300;
}
.section-header { margin-bottom: 3.5rem; }

/* ── ABOUT ── */
#about { background: var(--bg2); }
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1.3fr;
  gap: 5rem;
  align-items: start;
  max-width: 1100px;
}
.about-left .card-info {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 1.75rem;
  margin-top: 2rem;
}
.info-row {
  display: flex; justify-content: space-between; align-items: center;
  padding: 0.65rem 0;
  border-bottom: 1px solid var(--border);
  font-size: 0.875rem;
}
.info-row:last-child { border-bottom: none; }
.info-row .key { color: var(--text3); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.05em; }
.info-row .val { color: var(--text); font-weight: 500; }
.info-row .val.green { color: var(--accent); }

.about-right .para {
  color: var(--text2); font-size: 0.975rem;
  line-height: 1.85; margin-bottom: 1.25rem;
  font-weight: 300;
}
.about-right .para strong { color: var(--text); font-weight: 500; }

/* ── SKILLS ── */
#skills { background: var(--bg); }
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.25rem;
  max-width: 1100px;
}
.skill-card {
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 1.5rem;
  transition: border-color 0.2s, transform 0.2s;
}
.skill-card:hover { border-color: var(--border2); transform: translateY(-2px); }
.skill-card-icon {
  width: 42px; height: 42px; border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.1rem; margin-bottom: 1rem;
}
.skill-card-icon.green { background: rgba(0,229,160,0.1); }
.skill-card-icon.blue { background: rgba(0,112,243,0.12); }
.skill-card-icon.amber { background: rgba(245,158,11,0.1); }
.skill-card-icon.purple { background: rgba(168,85,247,0.1); }
.skill-card-icon.teal { background: rgba(20,184,166,0.1); }
.skill-card-icon.red { background: rgba(239,68,68,0.1); }
.skill-card h4 {
  font-family: 'Syne', sans-serif;
  font-size: 0.95rem; font-weight: 700;
  margin-bottom: 0.9rem; color: var(--text);
}
.tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.tag {
  background: rgba(255,255,255,0.05);
  border: 1px solid var(--border);
  color: var(--text2);
  font-size: 0.75rem; font-family: 'DM Mono', monospace;
  padding: 0.25rem 0.6rem; border-radius: 4px;
}

/* ── PROJECTS ── */
#projects { background: var(--bg2); }
.projects-list { display: flex; flex-direction: column; gap: 1.5rem; max-width: 1100px; }
.project-card {
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 18px;
  overflow: hidden;
  transition: border-color 0.2s;
}
.project-card:hover { border-color: var(--border2); }
.project-card-header {
  padding: 1.75rem 2rem 1.25rem;
  display: flex; align-items: flex-start; justify-content: space-between; gap: 1rem;
  cursor: pointer;
}
.project-module-badge {
  font-size: 0.7rem; font-weight: 700;
  padding: 0.3rem 0.7rem; border-radius: 100px;
  letter-spacing: 0.06em; text-transform: uppercase; white-space: nowrap;
}
.badge-mm { background: rgba(245,158,11,0.15); color: #f59e0b; border: 1px solid rgba(245,158,11,0.3); }
.badge-sd { background: rgba(0,112,243,0.12); color: #4da3ff; border: 1px solid rgba(0,112,243,0.25); }
.badge-dd { background: rgba(168,85,247,0.12); color: #c084fc; border: 1px solid rgba(168,85,247,0.25); }

.project-title-row { display: flex; align-items: center; gap: 1rem; margin-bottom: 0.5rem; }
.project-title {
  font-family: 'Syne', sans-serif;
  font-size: 1.2rem; font-weight: 700;
  color: var(--text);
}
.project-subtitle { font-size: 0.875rem; color: var(--text3); margin-bottom: 0.9rem; }
.project-tech-row { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.project-tech {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem; color: var(--text3);
  background: rgba(255,255,255,0.04); border: 1px solid var(--border);
  padding: 0.2rem 0.55rem; border-radius: 4px;
}
.toggle-icon {
  color: var(--text3); font-size: 1.2rem;
  transition: transform 0.25s;
  flex-shrink: 0; margin-top: 0.25rem;
}
.project-card.open .toggle-icon { transform: rotate(45deg); }

.project-body {
  display: none; padding: 0 2rem 2rem;
}
.project-card.open .project-body { display: block; }

.csar-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1rem; margin-bottom: 1.5rem; }
@media (max-width: 700px) { .csar-grid { grid-template-columns: 1fr; } }
.csar {
  padding: 1.1rem 1.2rem;
  border-radius: 10px;
  border-left: 3px solid;
}
.csar.challenge { background: rgba(239,68,68,0.07); border-color: rgba(239,68,68,0.4); }
.csar.action { background: rgba(0,112,243,0.07); border-color: rgba(0,112,243,0.35); }
.csar.result { background: rgba(0,229,160,0.07); border-color: rgba(0,229,160,0.35); }
.csar-label {
  font-size: 0.7rem; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.1em;
  margin-bottom: 0.5rem;
}
.challenge .csar-label { color: #f87171; }
.action .csar-label { color: #60a5fa; }
.result .csar-label { color: var(--accent); }
.csar p { font-size: 0.85rem; color: var(--text2); line-height: 1.65; font-weight: 300; }

.bullets { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
.bullets li {
  font-size: 0.875rem; color: var(--text2);
  display: flex; gap: 0.75rem; align-items: flex-start;
  line-height: 1.6; font-weight: 300;
}
.bullets li::before {
  content: '›'; color: var(--accent);
  font-size: 1rem; flex-shrink: 0; margin-top: 0.05rem;
}
.project-divider {
  height: 1px; background: var(--border);
  margin: 1.25rem 0;
}
.bullets-title {
  font-size: 0.75rem; color: var(--text3);
  text-transform: uppercase; letter-spacing: 0.08em;
  font-weight: 600; margin-bottom: 0.75rem;
}

/* ── EDUCATION ── */
#education { background: var(--bg); }
.edu-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 1.25rem; max-width: 1100px; }
.edu-card {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 14px; padding: 1.75rem;
}
.edu-card-top { display: flex; align-items: flex-start; gap: 1rem; margin-bottom: 1.25rem; }
.edu-icon {
  width: 44px; height: 44px; border-radius: 10px;
  background: rgba(0,229,160,0.08); border: 1px solid rgba(0,229,160,0.15);
  display: flex; align-items: center; justify-content: center;
  font-size: 1.2rem; flex-shrink: 0;
}
.edu-card h4 { font-family: 'Syne', sans-serif; font-size: 1rem; font-weight: 700; color: var(--text); margin-bottom: 0.2rem; }
.edu-card .inst { font-size: 0.85rem; color: var(--text2); font-weight: 300; }
.edu-meta { display: flex; gap: 0.75rem; flex-wrap: wrap; margin-top: 1rem; }
.edu-pill {
  font-size: 0.75rem; padding: 0.3rem 0.75rem; border-radius: 100px;
  background: rgba(255,255,255,0.05); border: 1px solid var(--border);
  color: var(--text2);
}
.edu-pill.green { background: rgba(0,229,160,0.1); border-color: rgba(0,229,160,0.25); color: var(--accent); }

/* ── TRAINING ── */
#training { background: var(--bg2); }
.training-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.25rem; max-width: 1100px; }
.training-card {
  background: var(--bg3); border: 1px solid var(--border);
  border-radius: 14px; padding: 1.5rem;
}
.training-card h4 { font-family: 'Syne', sans-serif; font-size: 0.95rem; font-weight: 700; margin-bottom: 0.85rem; }
.training-topics { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.training-topic {
  font-size: 0.75rem; font-family: 'DM Mono', monospace;
  padding: 0.25rem 0.6rem; border-radius: 4px;
  background: rgba(255,255,255,0.04); border: 1px solid var(--border);
  color: var(--text2);
}
.wip-badge {
  display: inline-block; font-size: 0.7rem; font-weight: 600;
  background: rgba(245,158,11,0.12); border: 1px solid rgba(245,158,11,0.3);
  color: #f59e0b; padding: 0.2rem 0.6rem; border-radius: 100px;
  margin-bottom: 0.85rem; letter-spacing: 0.05em;
}

/* ── CONTACT ── */
#contact { background: var(--bg); }
.contact-inner {
  max-width: 1100px;
  display: grid; grid-template-columns: 1.2fr 1fr;
  gap: 5rem; align-items: center;
}
.contact-items { display: flex; flex-direction: column; gap: 1rem; margin-top: 2rem; }
.contact-item {
  display: flex; align-items: center; gap: 1rem;
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 12px; padding: 1.1rem 1.25rem;
  text-decoration: none;
  transition: border-color 0.2s, transform 0.2s;
}
.contact-item:hover { border-color: var(--accent); transform: translateX(4px); }
.contact-icon {
  width: 38px; height: 38px; border-radius: 8px;
  background: rgba(0,229,160,0.08); border: 1px solid rgba(0,229,160,0.15);
  display: flex; align-items: center; justify-content: center;
  font-size: 1rem; flex-shrink: 0;
}
.contact-item-text .label { font-size: 0.72rem; color: var(--text3); text-transform: uppercase; letter-spacing: 0.06em; }
.contact-item-text .val { font-size: 0.9rem; color: var(--text); font-weight: 500; }
.contact-right {
  background: var(--bg2); border: 1px solid var(--border);
  border-radius: 18px; padding: 2rem;
  position: relative; overflow: hidden;
}
.contact-right::before {
  content: '';
  position: absolute; bottom: -60px; right: -60px;
  width: 200px; height: 200px;
  background: radial-gradient(circle, rgba(0,229,160,0.08) 0%, transparent 70%);
}
.contact-right blockquote {
  font-family: 'Syne', sans-serif;
  font-size: 1.3rem; font-weight: 600; line-height: 1.5;
  color: var(--text); margin-bottom: 1.25rem;
}
.contact-right blockquote span { color: var(--accent); }
.contact-right p { font-size: 0.875rem; color: var(--text2); line-height: 1.7; font-weight: 300; }
.open-badge {
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: rgba(0,229,160,0.1); border: 1px solid rgba(0,229,160,0.25);
  color: var(--accent); font-size: 0.78rem; font-weight: 600;
  padding: 0.4rem 1rem; border-radius: 100px;
  margin-top: 1.25rem;
}
.open-badge::before {
  content: ''; display: block;
  width: 6px; height: 6px; border-radius: 50%;
  background: var(--accent);
  animation: pulse 2s ease-in-out infinite;
}

/* ── FOOTER ── */
footer {
  background: var(--bg2);
  border-top: 1px solid var(--border);
  padding: 2rem 4rem;
  display: flex; justify-content: space-between; align-items: center;
  font-size: 0.8rem; color: var(--text3);
}
footer a { color: var(--accent); text-decoration: none; }

/* ── FADE-IN ANIMATION ── */
.fade-in {
  opacity: 0; transform: translateY(20px);
  animation: fadeUp 0.6s ease forwards;
}
@keyframes fadeUp {
  to { opacity: 1; transform: translateY(0); }
}
.delay-1 { animation-delay: 0.1s; }
.delay-2 { animation-delay: 0.2s; }
.delay-3 { animation-delay: 0.3s; }
.delay-4 { animation-delay: 0.4s; }
.delay-5 { animation-delay: 0.55s; }
.delay-6 { animation-delay: 0.7s; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  nav { padding: 1rem 1.5rem; }
  .nav-links { display: none; }
  section { padding: 4rem 1.5rem; }
  #hero { padding: 7rem 1.5rem 3rem; }
  .about-grid { grid-template-columns: 1fr; gap: 2.5rem; }
  .contact-inner { grid-template-columns: 1fr; gap: 2.5rem; }
  .hero-stats { gap: 2rem; }
  footer { flex-direction: column; gap: 0.75rem; text-align: center; }
  .csar-grid { grid-template-columns: 1fr; }
  .project-card-header { flex-wrap: wrap; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#hero">VR<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#training">Training</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a class="nav-cta" href="mailto:vakaraviteja30@gmail.com">Hire Me</a>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid-bg"></div>
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>
  <div class="hero-content">
    <div class="hero-badge fade-in">Available for SAP ABAP roles · Open to relocation</div>
    <h1 class="hero-name fade-in delay-1">
      Vaka<br><span class="line2">Raviteja</span>
    </h1>
    <p class="hero-title fade-in delay-2">SAP ABAP Developer · RICEFW · S/4HANA</p>
    <p class="hero-desc fade-in delay-3">
      I engineer the data pipelines, user experiences, and business rules that make SAP work for real people. From optimised multi-table JOINs to OOP ALV frameworks and BAdI enhancements — I build production-grade ABAP from scratch.
    </p>
    <div class="hero-actions fade-in delay-4">
      <a class="btn-primary" href="#projects">View Projects</a>
      <a class="btn-secondary" href="#contact">Get in Touch</a>
    </div>
    <div class="hero-stats fade-in delay-5">
      <div class="stat-item">
        <div class="num">2</div>
        <div class="label">End-to-End Projects</div>
      </div>
      <div class="stat-item">
        <div class="num">5+</div>
        <div class="label">RICEFW Object Types</div>
      </div>
      <div class="stat-item">
        <div class="num">8.0</div>
        <div class="label">B.Tech CGPA</div>
      </div>
      <div class="stat-item">
        <div class="num">S/4</div>
        <div class="label">HANA Upskilling</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-left">
      <div class="section-eyebrow">Who I Am</div>
      <h2 class="section-title">More than<br>an ABAP coder</h2>
      <div class="card-info">
        <div class="info-row"><span class="key">Name</span><span class="val">Vaka Raviteja</span></div>
        <div class="info-row"><span class="key">Role</span><span class="val">SAP ABAP Developer</span></div>
        <div class="info-row"><span class="key">Location</span><span class="val">Guntur, Andhra Pradesh</span></div>
        <div class="info-row"><span class="key">Relocation</span><span class="val green">✓ Open anywhere in India</span></div>
        <div class="info-row"><span class="key">Phone</span><span class="val">+91-7893266496</span></div>
        <div class="info-row"><span class="key">Email</span><span class="val">vakaraviteja30@gmail.com</span></div>
        <div class="info-row"><span class="key">LinkedIn</span><span class="val">vaka-raviteja</span></div>
        <div class="info-row"><span class="key">Status</span><span class="val green">● Actively seeking roles</span></div>
      </div>
    </div>
    <div class="about-right">
      <div class="section-eyebrow" style="margin-top:2.5rem">My Story</div>
      <p class="para">My journey into SAP didn't start with a job posting — it started with a question: <strong>why do so many enterprise systems feel like they were built for computers, not people?</strong> During my B.Tech in CS&IT at Guntur Engineering College, I became obsessed with the full stack of a business problem — from the database table to the screen the end user touches.</p>
      <p class="para">Since then, I've built two end-to-end, production-grade SAP solutions entirely from scratch. A <strong>Warehouse Inventory Analysis Report</strong> that consolidated four MM tables into a single optimised JOIN, and a <strong>Sales Order–Delivery Status Tracker</strong> that replaced manual cross-transaction lookups with a complete two-tier Interactive ALV with integrated Smart Form output.</p>
      <p class="para">Right now, I'm actively upskilling into the <strong>S/4HANA stack</strong> — CDS Views, AMDP, OData services, and Clean ABAP principles — because the next decade of SAP development is being written today. I'm looking for a team where I can contribute from Day 1 and keep growing.</p>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-header">
    <div class="section-eyebrow">What I Know</div>
    <h2 class="section-title">Technical Skills</h2>
    <p class="section-sub">A full-stack view of my SAP ABAP capabilities — from core development tools to modern S/4HANA technologies.</p>
  </div>
  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-card-icon green">⚙️</div>
      <h4>ABAP Core</h4>
      <div class="tags">
        <span class="tag">Classical Reports</span><span class="tag">Interactive Reports</span>
        <span class="tag">ALV (CL_SALV_TABLE)</span><span class="tag">REUSE_ALV_GRID</span>
        <span class="tag">Dialog Programming</span><span class="tag">ABAP OOP</span>
        <span class="tag">SELECT-OPTIONS</span><span class="tag">Internal Tables</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon blue">🔧</div>
      <h4>Enhancements & Forms</h4>
      <div class="tags">
        <span class="tag">BAdI</span><span class="tag">User Exits</span>
        <span class="tag">Customer Exits</span><span class="tag">Smart Forms</span>
        <span class="tag">Adobe Forms</span><span class="tag">SSF_FUNCTION_MODULE_NAME</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon amber">🗄️</div>
      <h4>Data Dictionary (SE11)</h4>
      <div class="tags">
        <span class="tag">Tables</span><span class="tag">Views</span>
        <span class="tag">Structures</span><span class="tag">Search Helps</span>
        <span class="tag">Lock Objects</span><span class="tag">Table Types</span>
        <span class="tag">SE38</span><span class="tag">SE37</span><span class="tag">SE80</span><span class="tag">SM30</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon teal">🟡</div>
      <h4>MM Module Tables</h4>
      <div class="tags">
        <span class="tag">MARA</span><span class="tag">MAKT</span>
        <span class="tag">MARC</span><span class="tag">MARD</span>
        <span class="tag">MSEG</span><span class="tag">MCHB</span>
        <span class="tag">EKKO</span><span class="tag">EKPO</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon blue">🔵</div>
      <h4>SD Module Tables</h4>
      <div class="tags">
        <span class="tag">VBAK</span><span class="tag">VBAP</span>
        <span class="tag">VBFA</span><span class="tag">LIKP</span>
        <span class="tag">LIPS</span><span class="tag">VBUK</span>
        <span class="tag">VBRK</span><span class="tag">VBRP</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon purple">🚀</div>
      <h4>S/4HANA & Modern Stack</h4>
      <div class="tags">
        <span class="tag">CDS Views</span><span class="tag">AMDP</span>
        <span class="tag">OData Services</span><span class="tag">SAP Fiori Basics</span>
        <span class="tag">Clean ABAP</span><span class="tag">SAP HANA</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon green">📊</div>
      <h4>SQL & Integration</h4>
      <div class="tags">
        <span class="tag">INNER JOIN</span><span class="tag">LEFT OUTER JOIN</span>
        <span class="tag">GROUP BY</span><span class="tag">HAVING</span>
        <span class="tag">ABAP Open SQL</span><span class="tag">FI Awareness</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-card-icon red">📋</div>
      <h4>ATS Keywords</h4>
      <div class="tags">
        <span class="tag">RICEFW</span><span class="tag">S/4HANA</span>
        <span class="tag">CDS</span><span class="tag">OData</span>
        <span class="tag">ALV</span><span class="tag">BAdI</span>
        <span class="tag">SE11</span><span class="tag">SAP ERP</span>
        <span class="tag">ABAP Workbench</span>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-header">
    <div class="section-eyebrow">What I've Built</div>
    <h2 class="section-title">Industry-Scenario Projects</h2>
    <p class="section-sub">End-to-end RICEFW objects built from scratch, mirroring real-world SAP implementation scenarios across MM and SD modules.</p>
  </div>
  <div class="projects-list">

    <!-- PROJECT 1 -->
    <div class="project-card" id="p1">
      <div class="project-card-header" onclick="toggleProject('p1')">
        <div style="flex:1">
          <div class="project-title-row">
            <h3 class="project-title">Warehouse Inventory Analysis Report</h3>
            <span class="project-module-badge badge-mm">MM Module</span>
          </div>
          <p class="project-subtitle">SAP ABAP Training — Production-Grade Inventory Intelligence Tool</p>
          <div class="project-tech-row">
            <span class="project-tech">CL_SALV_TABLE</span>
            <span class="project-tech">BAdI</span>
            <span class="project-tech">INNER JOIN</span>
            <span class="project-tech">SE11</span>
            <span class="project-tech">SELECT-OPTIONS</span>
            <span class="project-tech">MARA · MAKT · MARC · MARD</span>
          </div>
        </div>
        <span class="toggle-icon">+</span>
      </div>
      <div class="project-body">
        <div class="csar-grid">
          <div class="csar challenge">
            <div class="csar-label">Challenge</div>
            <p>Inventory analysts had no unified stock view. Checking reorder thresholds required navigating multiple transactions and running sequential SELECTs — slow, error-prone, and causing critical stockouts to go undetected.</p>
          </div>
          <div class="csar action">
            <div class="csar-label">Action</div>
            <p>Built a high-performance ABAP report using a single INNER JOIN across all four MM tables, eliminating redundant DB round-trips. Added dynamic selection screen, CL_SALV_TABLE with color-coded alerts, and a BAdI on MM01 for data quality enforcement.</p>
          </div>
          <div class="csar result">
            <div class="csar-label">Result</div>
            <p>Single-query report replacing multiple manual lookups. 100% master data compliance on test dataset. Reusable SE11 type structures. Color-coded critical-stock alerts enable instant prioritization with zero extra navigation.</p>
          </div>
        </div>
        <div class="project-divider"></div>
        <div class="bullets-title">Key Technical Highlights</div>
        <ul class="bullets">
          <li>Designed INNER JOIN across MARA (material master), MAKT (descriptions), MARC (plant + reorder level MINBE), and MARD (unrestricted stock LABST) — eliminating redundant DB round-trips vs. sequential SELECTs</li>
          <li>Engineered a fully dynamic Selection Screen with SELECT-OPTIONS for Plant (WERKS), Storage Location (LGORT), Material Type (MTART), and a reorder-threshold checkbox — self-service filtering without ABAP changes</li>
          <li>Delivered output via CL_SALV_TABLE (S/4HANA-preferred OOP ALV) with color-coded exception rows (red = critical stock) and full toolbar (sort, filter, export to Excel)</li>
          <li>Implemented BAdI ZMAT_DESC_VALIDATION on MM01 to enforce naming conventions — blocking non-compliant records at entry and improving master data quality by 100% for test dataset</li>
          <li>Created SE11 Data Dictionary structure ZS_INVENTORY and table type ZT_INVENTORY for type safety and reusability across the program</li>
        </ul>
      </div>
    </div>

    <!-- PROJECT 2 -->
    <div class="project-card" id="p2">
      <div class="project-card-header" onclick="toggleProject('p2')">
        <div style="flex:1">
          <div class="project-title-row">
            <h3 class="project-title">Sales Order–Delivery Status Tracker</h3>
            <span class="project-module-badge badge-sd">SD Module</span>
          </div>
          <p class="project-subtitle">SAP ABAP Training — Complete Order-to-Delivery Audit Engine</p>
          <div class="project-tech-row">
            <span class="project-tech">Interactive ALV</span>
            <span class="project-tech">Smart Forms</span>
            <span class="project-tech">LEFT OUTER JOIN</span>
            <span class="project-tech">AT LINE-SELECTION</span>
            <span class="project-tech">VBAK · VBAP · VBFA · LIKP · LIPS</span>
          </div>
        </div>
        <span class="toggle-icon">+</span>
      </div>
      <div class="project-body">
        <div class="csar-grid">
          <div class="csar challenge">
            <div class="csar-label">Challenge</div>
            <p>Sales teams had no single view of order-to-delivery status. Tracking fulfilled, partial, and pending orders meant manually cross-referencing VA03 and VL03N — a time-consuming workflow causing delays in customer communication.</p>
          </div>
          <div class="csar action">
            <div class="csar-label">Action</div>
            <p>Built a 5-table LEFT OUTER JOIN (VBAK→VBAP→VBFA→LIKP→LIPS) capturing all delivery states in one DB call. Created two-tier Interactive ALV with drill-down and embedded Smart Form print output directly in the ALV toolbar.</p>
          </div>
          <div class="csar result">
            <div class="csar-label">Result</div>
            <p>Replaced manual multi-transaction lookup with a single session. Eliminated a separate print step. Full RICEFW coverage — Report + Interface + Enhancement + Form — in a single, cohesive ABAP object.</p>
          </div>
        </div>
        <div class="project-divider"></div>
        <div class="bullets-title">Key Technical Highlights</div>
        <ul class="bullets">
          <li>Complete Order-to-Delivery audit engine using a 5-table LEFT OUTER JOIN (VBAK→VBAP→VBFA[VBTYP_N='J']→LIKP→LIPS) — capturing fulfilled, partially delivered, and pending orders in one DB call</li>
          <li>Parameterised Selection Screen (Sales Org VKORG, Customer KUNNR, Date range ERDAT, Delivery Status) — allowing analysts to slice data across all dimensions without developer intervention</li>
          <li>Two-tier Interactive ALV: header level shows order summary; AT LINE-SELECTION drills into delivery line-items — full order visibility in a single session, no VA03/VL03N navigation needed</li>
          <li>Triggered Smart Form print output (Delivery Confirmation slip) directly from ALV toolbar using SSF_FUNCTION_MODULE_NAME — combining Report + Form in one RICEFW object, eliminating a manual print step</li>
        </ul>
      </div>
    </div>

    <!-- PROJECT 3 -->
    <div class="project-card" id="p3">
      <div class="project-card-header" onclick="toggleProject('p3')">
        <div style="flex:1">
          <div class="project-title-row">
            <h3 class="project-title">SE11 Type Safety Architecture</h3>
            <span class="project-module-badge badge-dd">Data Dictionary</span>
          </div>
          <p class="project-subtitle">SAP ABAP Training — Reusable Data Dictionary Design for Maintainable Code</p>
          <div class="project-tech-row">
            <span class="project-tech">SE11</span>
            <span class="project-tech">Structures</span>
            <span class="project-tech">Table Types</span>
            <span class="project-tech">ZS_INVENTORY</span>
            <span class="project-tech">ZT_INVENTORY</span>
            <span class="project-tech">Clean ABAP</span>
          </div>
        </div>
        <span class="toggle-icon">+</span>
      </div>
      <div class="project-body">
        <div class="csar-grid">
          <div class="csar challenge">
            <div class="csar-label">Challenge</div>
            <p>ABAP reports without centralised data types are fragile — if an underlying table structure changes, every program using local types breaks independently. New developers also struggle with inconsistent naming and no shared type library.</p>
          </div>
          <div class="csar action">
            <div class="csar-label">Action</div>
            <p>Proactively designed SE11 Data Dictionary structures (ZS_INVENTORY) and table types (ZT_INVENTORY) — decoupling the report from raw database field definitions. Applied this type-safety discipline consistently across both projects.</p>
          </div>
          <div class="csar result">
            <div class="csar-label">Result</div>
            <p>Centralised, reusable types that survive table changes through a single SE11 update. Fully aligned with SAP Clean Core guidelines for upgrade-safe custom code. Demonstrates systems thinking beyond just working reports.</p>
          </div>
        </div>
        <div class="project-divider"></div>
        <div class="bullets-title">Key Technical Highlights</div>
        <ul class="bullets">
          <li>Created ZS_INVENTORY (flat structure) and ZT_INVENTORY (table type) in SE11 — centralised, versioned type definitions used across the entire inventory report program</li>
          <li>Decouples ABAP programs from raw DDIC field definitions — any upstream table change requires a single SE11 update, not hunting through program code</li>
          <li>Follows SAP Clean Core guidelines: no local type definitions in report programs, all types registered in the Data Dictionary for discoverability</li>
          <li>Applied the same approach across the SD tracker, creating a consistent type-safety pattern across both projects — demonstrating architectural consistency, not one-off implementation</li>
        </ul>
      </div>
    </div>

  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-header">
    <div class="section-eyebrow">Background</div>
    <h2 class="section-title">Education</h2>
  </div>
  <div class="edu-grid">
    <div class="edu-card">
      <div class="edu-card-top">
        <div class="edu-icon">🎓</div>
        <div>
          <h4>B.Tech — Computer Science &amp; Information Technology</h4>
          <p class="inst">Guntur Engineering College, Guntur, AP</p>
          <p class="inst" style="margin-top:0.2rem">Affiliated to JNTUK (Jawaharlal Nehru Technological University Kakinada)</p>
        </div>
      </div>
      <div class="edu-meta">
        <span class="edu-pill green">CGPA: 8.0 / 10.0</span>
        <span class="edu-pill">2020 – 2024</span>
        <span class="edu-pill">Computer Science</span>
      </div>
    </div>
  </div>
</section>

<!-- TRAINING -->
<section id="training">
  <div class="section-header">
    <div class="section-eyebrow">Continuous Learning</div>
    <h2 class="section-title">Training &amp; Certifications</h2>
    <p class="section-sub">Structured SAP ABAP training plus active self-learning in S/4HANA and modern SAP technologies.</p>
  </div>
  <div class="training-grid">
    <div class="training-card">
      <h4>SAP ABAP Programming — Comprehensive</h4>
      <div class="training-topics">
        <span class="training-topic">Data Dictionary</span>
        <span class="training-topic">Classical Reports</span>
        <span class="training-topic">Interactive Reports</span>
        <span class="training-topic">ALV Framework</span>
        <span class="training-topic">Dialog Programming</span>
        <span class="training-topic">BAdIs</span>
        <span class="training-topic">Smart Forms</span>
        <span class="training-topic">S/4HANA Basics</span>
        <span class="training-topic">CDS Views</span>
        <span class="training-topic">OData</span>
        <span class="training-topic">Fiori Basics</span>
      </div>
    </div>
    <div class="training-card">
      <div class="wip-badge">⚡ In Progress</div>
      <h4>Self-Learning — S/4HANA &amp; Modern ABAP</h4>
      <div class="training-topics">
        <span class="training-topic">SAP S/4HANA Developer Cert Prep</span>
        <span class="training-topic">Clean ABAP Guidelines</span>
        <span class="training-topic">AMDP</span>
        <span class="training-topic">OData Service Creation</span>
        <span class="training-topic">SAP BTP Basics</span>
        <span class="training-topic">ABAP RESTful App Model</span>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner">
    <div>
      <div class="section-eyebrow">Get in Touch</div>
      <h2 class="section-title">Let's build<br>something together</h2>
      <p class="section-sub">Looking for a SAP ABAP role where I can contribute from Day 1. Open to junior, associate, and project-based positions anywhere in India.</p>
      <div class="contact-items">
        <a class="contact-item" href="mailto:vakaraviteja30@gmail.com">
          <div class="contact-icon">✉️</div>
          <div class="contact-item-text">
            <div class="label">Email</div>
            <div class="val">vakaraviteja30@gmail.com</div>
          </div>
        </a>
        <a class="contact-item" href="tel:+917893266496">
          <div class="contact-icon">📱</div>
          <div class="contact-item-text">
            <div class="label">Phone</div>
            <div class="val">+91-7893266496</div>
          </div>
        </a>
        <a class="contact-item" href="https://linkedin.com/in/vaka-raviteja" target="_blank">
          <div class="contact-icon">💼</div>
          <div class="contact-item-text">
            <div class="label">LinkedIn</div>
            <div class="val">linkedin.com/in/vaka-raviteja</div>
          </div>
        </a>
        <a class="contact-item" href="#">
          <div class="contact-icon">📍</div>
          <div class="contact-item-text">
            <div class="label">Location</div>
            <div class="val">Guntur, Andhra Pradesh · Open to Relocation</div>
          </div>
        </a>
      </div>
    </div>
    <div class="contact-right">
      <blockquote>"I don't just write ABAP — I engineer the solutions that make SAP <span>actually work</span> for the people using it."</blockquote>
      <p>If you're staffing a SAP ABAP role and looking for someone who brings fresh S/4HANA knowledge, solid RICEFW fundamentals, and genuine curiosity about your business processes — let's talk.</p>
      <div class="open-badge">Actively seeking roles · Available immediately</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span>© 2025 Vaka Raviteja · SAP ABAP Developer</span>
  <span>Built with passion · <a href="mailto:vakaraviteja30@gmail.com">vakaraviteja30@gmail.com</a></span>
</footer>

<script>
function toggleProject(id) {
  const card = document.getElementById(id);
  card.classList.toggle('open');
}
</script>
</body>
</html>
