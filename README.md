<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Marcus Tan Zse Fong — Life Sciences Consultant</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Syne:wght@400;500;600;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #F7F5F0;
    --bg-dark: #EEEBE3;
    --ink: #1A1814;
    --ink-muted: #6B6760;
    --ink-faint: #B0ADA6;
    --accent: #1B6B54;
    --accent-light: #E8F2EE;
    --accent-mid: #2E9E75;
    --rule: #D8D4CB;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--ink);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 4vw;
    height: 60px;
    background: rgba(247,245,240,0.9);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--rule);
    transition: transform 0.3s ease;
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 500;
    letter-spacing: 0.02em;
    color: var(--ink);
    text-decoration: none;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-muted);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: 55% 45%;
    padding-top: 60px;
  }
  .hero-left {
    background: var(--ink);
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding: 3rem 5vw 3rem 6vw;
    position: relative;
    overflow: hidden;
  }
  .hero-left::before {
    content: '';
    position: absolute;
    top: -100px; right: -60px;
    width: 500px; height: 500px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(46,158,117,0.12) 0%, transparent 65%);
    pointer-events: none;
  }
  .hero-left::after {
    content: '';
    position: absolute;
    bottom: -80px; left: -60px;
    width: 320px; height: 320px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(46,158,117,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-photo {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    object-fit: cover;
    object-position: center top;
    border: 2px solid rgba(46,158,117,0.5);
    margin-bottom: 1.8rem;
    display: block;
  }
  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 1.8rem;
  }
  .hero-badge-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent-mid);
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.6; transform: scale(0.85); }
  }
  .hero-badge-text {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent-mid);
  }
  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(48px, 5.5vw, 80px);
    font-weight: 300;
    line-height: 1.05;
    color: #F7F5F0;
    letter-spacing: -0.01em;
    margin-bottom: 1.8rem;
  }
  .hero-name em { font-style: italic; color: var(--accent-mid); }
  .hero-summary {
    font-size: 14px;
    color: rgba(247,245,240,0.5);
    max-width: 380px;
    line-height: 1.85;
    margin-bottom: 2.5rem;
    font-weight: 300;
  }
  .hero-cta { display: flex; gap: 12px; flex-wrap: wrap; }
  .btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 11px 22px;
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 2px;
    transition: all 0.2s;
    cursor: pointer;
  }
  .btn-primary { background: var(--accent); color: white; border: 1px solid var(--accent); }
  .btn-primary:hover { background: var(--accent-mid); border-color: var(--accent-mid); }
  .btn-outline { background: transparent; color: rgba(247,245,240,0.65); border: 1px solid rgba(247,245,240,0.2); }
  .btn-outline:hover { border-color: rgba(247,245,240,0.55); color: #F7F5F0; }

  .hero-right {
    background: var(--bg);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 6vw 5vw 6vw 4vw;
    gap: 1.5rem;
  }
  .hero-stat-row { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .stat-card {
    background: var(--white);
    border: 1px solid var(--rule);
    border-radius: 4px;
    padding: 18px 20px;
    position: relative;
    overflow: hidden;
    transition: box-shadow 0.2s;
  }
  .stat-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }
  .stat-card:hover { box-shadow: 0 4px 20px rgba(0,0,0,0.06); }
  .stat-card:hover::after { transform: scaleX(1); }
  .stat-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 36px;
    font-weight: 500;
    line-height: 1;
    color: var(--ink);
    margin-bottom: 4px;
  }
  .stat-label { font-size: 11px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase; color: var(--ink-muted); }

  .contact-strip {
    background: var(--accent-light);
    border: 1px solid #C2DDD5;
    border-radius: 4px;
    padding: 16px 20px;
  }
  .contact-strip-title {
    font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 10px;
  }
  .contact-items { display: flex; flex-direction: column; gap: 6px; }
  .contact-item {
    display: flex; align-items: center; gap: 10px;
    font-size: 13px; color: var(--ink); text-decoration: none;
  }
  .contact-item:hover { color: var(--accent); }
  .contact-icon { width: 14px; height: 14px; flex-shrink: 0; color: var(--accent); }

  /* ── ABOUT ── */
  #about { background: var(--ink); padding: 72px 6vw; }
  .about-inner {
    max-width: 900px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 56px;
    align-items: start;
  }
  .about-label {
    font-family: 'Syne', sans-serif;
    font-size: 11px; font-weight: 600;
    letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--accent-mid);
    writing-mode: vertical-rl;
    transform: rotate(180deg);
    padding-top: 4px;
  }
  .about-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(18px, 2vw, 24px);
    font-weight: 300;
    line-height: 1.7;
    color: rgba(247,245,240,0.85);
  }
  .about-text em { font-style: italic; color: var(--accent-mid); }

  /* ── SECTIONS ── */
  section { padding: 80px 6vw; }
  .section-header { display: flex; align-items: center; gap: 20px; margin-bottom: 52px; }
  .section-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px; font-weight: 400;
    color: var(--accent-mid); letter-spacing: 0.05em;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(30px, 3.2vw, 44px);
    font-weight: 400; line-height: 1.1; color: var(--ink);
  }
  .section-rule { flex: 1; height: 1px; background: var(--rule); }

  /* ── TIMELINE ── */
  #experience { background: var(--bg); }
  .timeline { position: relative; padding-left: 28px; }
  .timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 8px; bottom: 0;
    width: 1px; background: var(--rule);
  }
  .timeline-item {
    position: relative;
    margin-bottom: 52px;
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .timeline-item.visible { opacity: 1; transform: translateY(0); }
  .timeline-item::before {
    content: '';
    position: absolute;
    left: -34px; top: 8px;
    width: 12px; height: 12px;
    border-radius: 50%;
    background: var(--white);
    border: 2px solid var(--accent-mid);
    transition: background 0.2s;
  }
  .timeline-item:hover::before { background: var(--accent-mid); }
  .timeline-meta { display: flex; align-items: flex-start; justify-content: space-between; gap: 16px; margin-bottom: 2px; }
  .timeline-company {
    font-family: 'Syne', sans-serif;
    font-size: 13px; font-weight: 600;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--accent);
  }
  .timeline-period { font-size: 14px; color: var(--ink-muted); white-space: nowrap; font-style: italic; padding-top: 2px; font-weight: 500; }
  .timeline-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 500;
    color: var(--ink); margin-bottom: 14px; line-height: 1.25;
  }
  .timeline-bullets { list-style: none; display: flex; flex-direction: column; gap: 7px; margin-bottom: 14px; }
  .timeline-bullets li {
    font-size: 13.5px; color: var(--ink-muted);
    padding-left: 16px; position: relative; line-height: 1.65;
  }
  .timeline-bullets li::before {
    content: '—';
    position: absolute; left: 0;
    color: var(--accent-mid); font-size: 11px; top: 2px;
  }

  .rotation-block {
    background: var(--white);
    border: 1px solid var(--rule);
    border-left: 3px solid var(--accent);
    border-radius: 0 4px 4px 0;
    padding: 18px 22px;
    margin-top: 16px;
  }
  .rotation-label {
    font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 3px;
  }
  .rotation-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 17px; font-weight: 500;
    color: var(--ink); margin-bottom: 4px;
  }
  .rotation-period { font-size: 13px; color: var(--ink-muted); margin-bottom: 10px; font-style: italic; font-weight: 500; }

  /* ── ACHIEVEMENTS ── */
  #achievements { background: var(--bg-dark); }
  .achievement-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 18px; }
  .achievement-card {
    background: var(--white);
    border: 1px solid var(--rule);
    border-radius: 4px;
    padding: 26px;
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.5s ease, transform 0.5s ease, box-shadow 0.2s;
  }
  .achievement-card.visible { opacity: 1; transform: translateY(0); }
  .achievement-card:hover { box-shadow: 0 8px 40px rgba(0,0,0,0.07); }
  .achievement-icon {
    width: 38px; height: 38px;
    background: var(--accent-light);
    border-radius: 7px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 14px;
  }
  .achievement-icon svg { width: 18px; height: 18px; color: var(--accent); }
  .achievement-title { font-family: 'Cormorant Garamond', serif; font-size: 19px; font-weight: 500; color: var(--ink); margin-bottom: 7px; line-height: 1.3; }
  .achievement-desc { font-size: 13px; color: var(--ink-muted); line-height: 1.7; }
  .achievement-tag {
    display: inline-block; margin-top: 12px;
    padding: 3px 9px;
    background: var(--accent-light); color: var(--accent);
    font-size: 11px; font-weight: 500; letter-spacing: 0.05em;
    border-radius: 2px;
  }

  /* ── SKILLS ── */
  #skills { background: var(--bg); }
  .skills-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; }
  .skill-category-title {
    font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 18px;
    padding-bottom: 10px; border-bottom: 1px solid var(--rule);
  }
  .skill-items { display: flex; flex-direction: column; gap: 11px; }
  .skill-item { display: flex; align-items: center; justify-content: space-between; gap: 12px; }
  .skill-name { font-size: 13.5px; color: var(--ink); min-width: 190px; }
  .skill-bar-bg { flex: 1; height: 2px; background: var(--rule); border-radius: 1px; overflow: hidden; }
  .skill-bar {
    height: 100%; border-radius: 1px;
    background: var(--accent-mid);
    transform-origin: left; transform: scaleX(0);
    transition: transform 0.9s cubic-bezier(0.16, 1, 0.3, 1), background 0.9s ease;
  }
  .skill-pct {
    font-size: 11px;
    font-weight: 500;
    color: var(--ink-faint);
    min-width: 32px;
    text-align: right;
    transition: color 0.9s ease;
  }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 7px; margin-top: 4px; }
  .skill-tag {
    padding: 5px 12px;
    background: var(--white); border: 1px solid var(--rule);
    border-radius: 2px; font-size: 12px; color: var(--ink-muted);
    transition: all 0.2s;
  }
  .skill-tag:hover { border-color: var(--accent-mid); color: var(--accent); background: var(--accent-light); }

  /* ── PROJECTS ── */
  #projects { background: var(--bg); }
  .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
  .project-card {
    background: var(--white);
    border: 1px solid var(--rule);
    border-radius: 4px;
    padding: 28px;
    display: flex; flex-direction: column;
    opacity: 0; transform: translateY(16px);
    transition: opacity 0.5s ease, transform 0.5s ease, box-shadow 0.2s;
  }
  .project-card.visible { opacity: 1; transform: translateY(0); }
  .project-card:hover { box-shadow: 0 8px 40px rgba(0,0,0,0.07); }
  .project-card-header { display: flex; align-items: flex-start; justify-content: space-between; gap: 12px; margin-bottom: 10px; }
  .project-title { font-family: 'Cormorant Garamond', serif; font-size: 20px; font-weight: 500; color: var(--ink); line-height: 1.25; }
  .project-gh-link {
    flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
    width: 32px; height: 32px;
    border: 1px solid var(--rule); border-radius: 4px;
    color: var(--ink-muted); text-decoration: none;
    transition: all 0.2s;
  }
  .project-gh-link:hover { border-color: var(--accent-mid); color: var(--accent); background: var(--accent-light); }
  .project-gh-link svg { width: 15px; height: 15px; }
  .project-type {
    font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 10px;
  }
  .project-desc { font-size: 13px; color: var(--ink-muted); line-height: 1.7; flex: 1; }
  .project-stack { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 16px; }
  .project-tag {
    padding: 3px 9px;
    background: var(--bg-dark); border: 1px solid var(--rule);
    border-radius: 2px; font-size: 11px;
    font-family: 'DM Sans', monospace; color: var(--ink-muted);
  }

  /* ── CERTIFICATIONS ── */
  #certifications { background: var(--bg-dark); }
  .cert-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; }
  .cert-card {
    background: var(--white);
    border: 1px solid var(--rule);
    border-radius: 4px;
    padding: 22px 24px;
    display: flex; align-items: flex-start; gap: 14px;
    opacity: 0; transform: translateY(12px);
    transition: opacity 0.5s ease, transform 0.5s ease, box-shadow 0.2s;
  }
  .cert-card.visible { opacity: 1; transform: translateY(0); }
  .cert-card:hover { box-shadow: 0 4px 20px rgba(0,0,0,0.06); }
  .cert-icon-wrap {
    width: 36px; height: 36px; flex-shrink: 0;
    background: var(--accent-light); border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
  }
  .cert-icon-wrap svg { width: 16px; height: 16px; color: var(--accent); }
  .cert-name { font-size: 14px; font-weight: 500; color: var(--ink); line-height: 1.3; margin-bottom: 3px; }
  .cert-issuer { font-size: 12px; color: var(--ink-faint); }

  /* ── EDUCATION ── */
  #education { background: var(--ink); }
  #education .section-title { color: #F7F5F0; }
  #education .section-number { color: var(--accent-mid); }
  #education .section-rule { background: rgba(247,245,240,0.12); }
  .edu-grid { display: flex; flex-direction: column; gap: 16px; }
  .edu-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 4px;
    padding: 28px 32px;
    display: grid; grid-template-columns: 1fr auto;
    gap: 24px; align-items: center;
    opacity: 0; transform: translateY(14px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }
  .edu-card.visible { opacity: 1; transform: translateY(0); }
  .edu-card.primary { padding: 32px 36px; }
  .edu-institution {
    font-family: 'Syne', sans-serif;
    font-size: 10px; font-weight: 600;
    letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--accent-mid); margin-bottom: 6px;
  }
  .edu-degree {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 400;
    color: #F7F5F0; line-height: 1.25; margin-bottom: 6px;
  }
  .edu-card.primary .edu-degree { font-size: 28px; }
  .edu-details { font-size: 13px; color: rgba(247,245,240,0.45); }
  .edu-badge {
    background: rgba(46,158,117,0.12);
    border: 1px solid rgba(46,158,117,0.25);
    border-radius: 4px; padding: 14px 18px;
    text-align: center; white-space: nowrap;
  }
  .edu-badge-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px; font-weight: 500;
    color: var(--accent-mid); display: block;
    line-height: 1; margin-bottom: 3px;
  }
  .edu-badge-label { font-size: 10px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase; color: rgba(247,245,240,0.35); }

  /* ── CONTACT ── */
  #contact { background: var(--bg-dark); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; align-items: start; }
  .contact-intro {
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px; font-weight: 400;
    line-height: 1.45; color: var(--ink); margin-bottom: 20px;
  }
  .contact-intro em { font-style: italic; color: var(--accent-mid); }
  .contact-cards { display: flex; flex-direction: column; gap: 10px; }
  .contact-card {
    background: var(--white); border: 1px solid var(--rule);
    border-radius: 4px; padding: 14px 18px;
    display: flex; align-items: center; gap: 12px;
    text-decoration: none; transition: all 0.2s;
  }
  .contact-card:hover { border-color: var(--accent-mid); box-shadow: 0 4px 20px rgba(0,0,0,0.05); }
  .contact-card-icon {
    width: 34px; height: 34px;
    background: var(--accent-light); border-radius: 6px;
    display: flex; align-items: center; justify-content: center; flex-shrink: 0;
  }
  .contact-card-icon svg { width: 14px; height: 14px; color: var(--accent); }
  .contact-card-label { font-size: 10px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 1px; }
  .contact-card-value { font-size: 13.5px; color: var(--ink); }

  /* ── FOOTER ── */
  footer {
    background: var(--ink); padding: 26px 6vw;
    display: flex; align-items: center; justify-content: space-between;
  }
  .footer-name { font-family: 'Cormorant Garamond', serif; font-size: 16px; color: rgba(247,245,240,0.4); }
  .footer-copy { font-size: 11px; color: rgba(247,245,240,0.25); }

  /* ── FADE ── */
  .fade-up { opacity: 0; transform: translateY(20px); transition: opacity 0.7s ease, transform 0.7s ease; }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 820px) {
    .hero { grid-template-columns: 1fr; }
    .hero-left { min-height: 60vh; padding: 8vw; }
    .hero-right { padding: 7vw; }
    .about-inner { grid-template-columns: 1fr; gap: 16px; }
    .about-label { writing-mode: horizontal-tb; transform: none; }
    .skills-layout, .contact-grid { grid-template-columns: 1fr; }
    .edu-card { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    section { padding: 56px 5vw; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav id="main-nav">
  <a href="#top" class="nav-logo">Marcus Tan</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#achievements">Achievements</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#certifications">Certifications</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="top">
  <div class="hero-left">
    <img src="data:image/jpeg;base64,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+CSjGxFkgDEGv1OoyBxCBQS5o6lxjEd1k94K6eYCpxgrAQwUzfeVipqX4EapyxylCzxeneGe0M/uYZaZb5eBkuUSty1jFGP11WZTguniPMGe0aZl5mJHhLrmOVjFSRXOIypijuMYYZJTRu+senFILTSu6fP1jq5naGlY7yw9mLNw2y+8XFzrzAdNEs9hP4qZYUfAZrwVdRPUmWd0Szo1L9RyXEzBITAOqfcfiKy25ZpiaXfwuK2/CsNdPA51HMwfArI7mgI90e0T2IHXUFa4le+bLg+/+plYlkNp3QyxhxN8TjrF9JqIUCE4j7xX+UNQURYZSUYl3gEw95VaCPMcMMNz/9oADAMBAAIAAwAAABDzzzzzybLVLz3/AMIMz9D8cwc8c888884RJ6FE6OwPGL3nx888w888888s5hIsq0RqGYJY+48M8ws888884KRDsS4M1Tss/F3888888888841+EndI3L0/Ze0s888M4888888jKYokvJ6o6CKZJ888ws888888boCRRwNazXA6EZ888w88888884vQsVrJkKelZ2v8888o888888pMBANHVlZR0jlX888M8888888opUSlb/YHLM1b0888w8888888syViZQuwT5FDL8888ws88888883S6VBsHAEdd88888888888888s2gU/W+Suyc08888M688888888+70VskGdmY0a888ws88888888819wPwL/jMzVb8l88888888888mumomadbBXOsac88888888884A2VeHMS5BPDNlB80888888vSYej50mdvaxq2tXWYG8888n9rM7LZLdH5Qg6P/T0tyb88rPiGwx9EixOlp1veZcKHOVg86FqweGYHsN874HLEw35Y3SLE4UcyeC7XwEONJH1/BOOVpns6at4YqRjsmcoevEoWslDKcFbcVHmWa6oSsTCIrub8cDj1kvbzOyHTYEakUY54t0p9h5jygj/AJoq5lP/xAAjEQEBAQACAgICAgMAAAAAAAABABEhMRBBMFFhcSBAgZGh/9oACAEDAQE/EP5nkMLFetk57xHo3CJ+UmD7tWW3cs6jEBAl7SYbPD8hBrcbA3JbKCLcCI8Qi2Ecl2+QsKcdgMliB6gSAgpJys2lwjifla6bni6ah5DN7sSbgX4bo8LiAePfhflcIdmGxWfW7NE6cQnCA4fYk5iF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" class="hero-photo" alt="Marcus Tan">
    <div class="hero-badge">
      <div class="hero-badge-dot"></div>
      <span class="hero-badge-text">Available · Life Sciences Consultant</span>
    </div>
    <h1 class="hero-name">Marcus<br><em>Tan Zse Fong</em></h1>
    <p class="hero-summary">Professional in life science manufacturing with expertise spanning operations, engineering, MES digitization, project management, and GxP compliance — across biologics and API manufacturing environments.</p>
    <div class="hero-cta">
      <a href="#experience" class="btn btn-primary">View Experience</a>
      <a href="#contact" class="btn btn-outline">Get in Touch</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-stat-row">
      <div class="stat-card">
        <div class="stat-number">6+</div>
        <div class="stat-label">Years in Pharma</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">2</div>
        <div class="stat-label">Successful NPIs</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">4</div>
        <div class="stat-label">Major Projects</div>
      </div>
    </div>
    <div class="contact-strip">
      <div class="contact-strip-title">Contact</div>
      <div class="contact-items">
        <a href="mailto:mmarcustan95@gmail.com" class="contact-item">
          <svg class="contact-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75"/></svg>
          mmarcustan95@gmail.com
        </a>
        <a href="tel:+6582827315" class="contact-item">
          <svg class="contact-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z"/></svg>
          +65 8282 7315
        </a>
        <a href="https://linkedin.com/in/marcustan1995" target="_blank" class="contact-item">
          <svg class="contact-icon" fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          linkedin.com/in/marcustan1995
        </a>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-inner">
    <div class="about-label">About</div>
    <p class="about-text fade-up">
      Professional in the <em>life science manufacturing</em> industry with experience spanning manufacturing operations, validation, engineering, and project management for brownfield facilities — across both <em>biologics and API manufacturing</em>. Proficient in project management, engineering equipment design, manufacturing process design, GxP compliance, EBR recipe design, MES and ERP system support, and the <em>Microsoft Power Platform</em>.
    </p>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-header">
    <span class="section-number">01</span>
    <h2 class="section-title">Work Experience</h2>
    <div class="section-rule"></div>
  </div>

  <div class="timeline">

    <!-- ORKA -->
    <div class="timeline-item">
      <div class="timeline-meta">
        <span class="timeline-company">ORKA Consulting Partners</span>
        <span class="timeline-period">Apr 2026 — Present</span>
      </div>
      <h3 class="timeline-role">Consultant</h3>
      <ul class="timeline-bullets">
        <li>Providing consulting services within the life sciences manufacturing sector, leveraging expertise in MES, digitization, and manufacturing operations.</li>
      </ul>
    </div>

    <!-- NNIT -->
    <div class="timeline-item">
      <div class="timeline-meta">
        <span class="timeline-company">NNIT · GSK Vaccines Tuas</span>
        <span class="timeline-period">Jan 2024 — Apr 2026</span>
      </div>
      <h3 class="timeline-role">Digitalization Consultant</h3>
      <ul class="timeline-bullets">
        <li>Qualified Siemens OpsCenter Recipe Designer, supporting a multi-product, multi-facility MES deployment project and ongoing routine management at GSK Vaccines Singapore.</li>
        <li>Workstream lead for an end-to-end digitization project converting paper batch records to electronic batch records (eBR), greatly improving workflow efficiency and data integrity.</li>
        <li>Collaborated with manufacturing stakeholders to draft User Requirement Specifications (URS) for MES recipe design and identify pain points and digitization opportunities.</li>
        <li>Designed and qualified MES recipes for both Upstream and Purification processes with SAP and OSIsoft PI (OSIPI) integration.</li>
        <li>Provided end-to-end technical support for Performance Qualification (PQ) of MES recipes including incident management, resulting in a successful right-first-time go-live.</li>
      </ul>
    </div>

    <!-- AbbVie -->
    <div class="timeline-item">
      <div class="timeline-meta">
        <span class="timeline-company">AbbVie Biologics Singapore</span>
        <span class="timeline-period">Aug 2020 — Jan 2024</span>
      </div>
      <h3 class="timeline-role">Operations Development Program → Project &amp; Process Engineer II</h3>
      <p style="font-size:13px; color:var(--ink-muted); margin-bottom:18px; font-style:italic; line-height:1.6;">A selective global leadership development program — three 12-month rotations across Operations, followed by a permanent role as Project &amp; Process Engineer II.</p>

      <div class="rotation-block">
        <div class="rotation-label">Final Role</div>
        <div class="rotation-role">Project &amp; Process Engineer II</div>
        <div class="rotation-period">Aug 2023 — Dec 2023</div>
        <ul class="timeline-bullets">
          <li>Continued leading engineering and project management responsibilities in the local site following completion of the ODP program.</li>
        </ul>
      </div>

      <div class="rotation-block">
        <div class="rotation-label">Rotation 3 · ODP</div>
        <div class="rotation-role">TPM Account Manager (Global) &amp; Project Engineering (Local)</div>
        <div class="rotation-period">Aug 2022 — Aug 2023</div>
        <ul class="timeline-bullets">
          <li>Led a tech transfer project to introduce a new drug product manufacturing process to a Third Party Manufacturer (TPM) site in Italy; managed internal and external stakeholders to hit all milestone deliverables.</li>
          <li>Co-led a ~SGD 10 million CAPEX NPI project at the Singapore site, including end-to-end design, procurement, and construction of an Ultrafiltration skid in the Purification Suite.</li>
          <li>Managed and negotiated with 50+ external vendors across 60+ components; maintained financial oversight in collaboration with Finance.</li>
          <li>Collaborated with Finance routinely to maintain budget and call out financial risks; supported transition of a product from clinical to commercial manufacturing at the TPM.</li>
        </ul>
      </div>

      <div class="rotation-block">
        <div class="rotation-label">Rotation 2 · ODP</div>
        <div class="rotation-role">API Technical Operations (MSAT)</div>
        <div class="rotation-period">Aug 2021 — Aug 2022</div>
        <ul class="timeline-bullets">
          <li>Supported technology transfer, qualification, and validation activities for the New Product Introduction (NPI) project in API manufacturing.</li>
          <li>Provided technical support for process and equipment troubleshooting and investigations; supported operational efficiency goals for yield and product quality.</li>
          <li>Authored technical reports, batch records, SOPs, investigation reports, and process FMEAs as key project deliverables.</li>
        </ul>
      </div>

      <div class="rotation-block">
        <div class="rotation-label">Rotation 1 · ODP</div>
        <div class="rotation-role">Biologics Manufacturing Specialist</div>
        <div class="rotation-period">Aug 2020 — Aug 2021</div>
        <ul class="timeline-bullets">
          <li>Initiated multiple digital dashboarding projects to improve communication, workflow automation, and reduction of human error within manufacturing teams.</li>
          <li>Led multiple change plan projects to improve existing work processes as part of the site's throughput expansion initiative.</li>
          <li>Commissioned small standalone Upstream equipment and led a feasibility study to restructure shift teams to minimize night-shift headcount for biotechnologists.</li>
        </ul>
      </div>
    </div>

    <!-- GSK Internship -->
    <div class="timeline-item">
      <div class="timeline-meta">
        <span class="timeline-company">GSK Singapore</span>
        <span class="timeline-period">Jul 2019 — Jan 2020</span>
      </div>
      <h3 class="timeline-role">Process Improvement Intern</h3>
      <ul class="timeline-bullets">
        <li>Worked closely with Production Engineers, Superintendents, and Operations Technicians to drive improvement initiatives in Value Stream 1 (VS1) towards zero accidents, defects, and wastes.</li>
        <li>Built industry knowledge in cGMP; developed skills in root cause analysis, lean manufacturing tools, data analysis, and stakeholder presentations.</li>
        <li>Awarded a Recommendation Letter upon completion of the 6-month internship.</li>
      </ul>
    </div>

  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <div class="section-header fade-up">
    <span class="section-number">02</span>
    <h2 class="section-title">Key Achievements</h2>
    <div class="section-rule"></div>
  </div>
  <div class="achievement-grid">

    <div class="achievement-card">
      <div class="achievement-icon">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v5.714a2.25 2.25 0 01-.659 1.591L5 14.5M9.75 3.104c-.251.023-.501.05-.75.082m.75-.082a24.301 24.301 0 014.5 0m0 0v5.714c0 .597.237 1.17.659 1.591L19.8 15.3M14.25 3.104c.251.023.501.05.75.082M19.8 15.3l-1.57.393A9.065 9.065 0 0112 15a9.065 9.065 0 00-6.23-.693L5 14.5m14.8.8l1.402 1.402c1.232 1.232.65 3.318-1.067 3.611A48.309 48.309 0 0112 21c-2.773 0-5.491-.235-8.135-.687-1.718-.293-2.3-2.379-1.067-3.61L5 14.5"/></svg>
      </div>
      <div class="achievement-title">Atogepant New Product Introduction</div>
      <p class="achievement-desc">As part of the MSAT team, successfully introduced a new blockbuster API drug substance projected at USD 766 million to the Singapore site, ensuring global supply assurance — delivered within an aggressive timeline alongside routine plant operations.</p>
      <span class="achievement-tag">AbbVie Singapore</span>
    </div>

    <div class="achievement-card">
      <div class="achievement-icon">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 21h19.5m-18-18v18m10.5-18v18m6-13.5V21M6.75 6.75h.75m-.75 3h.75m-.75 3h.75m3-6h.75m-.75 3h.75m-.75 3h.75M6.75 21v-3.375c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21M3 3h12m-.75 4.5H21m-3.75 3.75h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008zm0 3h.008v.008h-.008v-.008z"/></svg>
      </div>
      <div class="achievement-title">Skyrizi NPI — Singapore Site</div>
      <p class="achievement-desc">Co-led an approximately SGD 10 million capital project to introduce Skyrizi to the Singapore biologics plant, managing an equipment work package on an extremely tight timeline with zero disruption to existing operations — while concurrently managing a global TPM role.</p>
      <span class="achievement-tag">AbbVie Singapore</span>
    </div>

    <div class="achievement-card">
      <div class="achievement-icon">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M12 21a9.004 9.004 0 008.716-6.747M12 21a9.004 9.004 0 01-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 017.843 4.582M12 3a8.997 8.997 0 00-7.843 4.582m15.686 0A11.953 11.953 0 0112 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0121 12c0 .778-.099 1.533-.284 2.253M3 12a8.959 8.959 0 00.284 2.253"/></svg>
      </div>
      <div class="achievement-title">Skyrizi BDP Tech Transfer — Patheon Italy</div>
      <p class="achievement-desc">Successfully coordinated with global counterparts and an external TPM in Italy to achieve the technical transfer of the Skyrizi biologics drug product filling process to a new external manufacturer, meeting all project deadlines and key deliverables.</p>
      <span class="achievement-tag">AbbVie Global</span>
    </div>

    <div class="achievement-card">
      <div class="achievement-icon">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M9 17.25v1.007a3 3 0 01-.879 2.122L7.5 21h9l-.621-.621A3 3 0 0115 18.257V17.25m6-12V15a2.25 2.25 0 01-2.25 2.25H5.25A2.25 2.25 0 013 15V5.25m18 0A2.25 2.25 0 0018.75 3H5.25A2.25 2.25 0 003 5.25m18 0H3"/></svg>
      </div>
      <div class="achievement-title">GSK Vaccines MES Full Go-Live</div>
      <p class="achievement-desc">Rapidly mastered a new MES platform to meet an aggressive client timeline. Designed and implemented eBR recipes for existing GSK products, successfully delivering the full technical go-live of the system on the original project deadline.</p>
      <span class="achievement-tag">NNIT / GSK</span>
    </div>

  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-header fade-up">
    <span class="section-number">03</span>
    <h2 class="section-title">Personal Projects</h2>
    <div class="section-rule"></div>
  </div>
  <div class="project-grid">

    <div class="project-card">
      <div class="project-type">Reinforcement Learning</div>
      <div class="project-card-header">
        <div class="project-title">The Ministry of Silly Walks</div>
        <a href="https://github.com/mmarcustan95/Project_MOSW" target="_blank" class="project-gh-link" title="View on GitHub">
          <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
        </a>
      </div>
      <p class="project-desc">A reinforcement learning experiment that subverts the standard BipedalWalker-v3 objective — instead of optimal locomotion, custom reward shaping is used to encourage chaotic and non-traditional movement patterns in a simulated bipedal robot.</p>
      <div class="project-stack">
        <span class="project-tag">Python</span>
        <span class="project-tag">Gymnasium</span>
        <span class="project-tag">Stable-Baselines3</span>
        <span class="project-tag">Pandas</span>
        <span class="project-tag">Matplotlib</span>
        <span class="project-tag">Box2D</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-type">Deep Learning · NLP</div>
      <div class="project-card-header">
        <div class="project-title">Neural Network Chatbot from Scratch</div>
        <a href="https://github.com/mmarcustan95/ChatBot" target="_blank" class="project-gh-link" title="View on GitHub">
          <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
        </a>
      </div>
      <p class="project-desc">A 12-class intent classification chatbot built entirely from scratch using only NumPy — no PyTorch or TensorFlow. Implements hand-coded forward pass, backpropagation, He initialization, ReLU activations, softmax output, and cross-entropy loss. Trained on ~11,500 samples from HuggingFace with a 500→64→12 architecture.</p>
      <div class="project-stack">
        <span class="project-tag">Python</span>
        <span class="project-tag">NumPy</span>
        <span class="project-tag">scikit-learn</span>
        <span class="project-tag">HuggingFace</span>
        <span class="project-tag">Bag-of-Words</span>
        <span class="project-tag">SGD</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-type">Full-Stack · Industry Tool</div>
      <div class="project-card-header">
        <div class="project-title">Equipment Validation Knowledge Library</div>
        <a href="https://github.com/mmarcustan95/ORKA_equipment_library-" target="_blank" class="project-gh-link" title="View on GitHub">
          <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
        </a>
      </div>
      <p class="project-desc">A searchable API backend built for ORKA Consulting to centralize institutional knowledge from past equipment validation projects. Features smart filtering by validation phase (URS, IQ, OQ, PQ), SharePoint integration, and a responsive dashboard. Phase 2 targets Microsoft Graph API and Azure hosting with Entra ID authentication.</p>
      <div class="project-stack">
        <span class="project-tag">Python</span>
        <span class="project-tag">FastAPI</span>
        <span class="project-tag">SQLite</span>
        <span class="project-tag">JavaScript</span>
        <span class="project-tag">Supabase</span>
        <span class="project-tag">MS Graph API</span>
      </div>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-header fade-up">
    <span class="section-number">04</span>
    <h2 class="section-title">Skills &amp; Expertise</h2>
    <div class="section-rule"></div>
  </div>
  <div class="skills-layout">
    <div>
      <div class="skill-category-title">Technical Proficiency</div>
      <div class="skill-items">
        <div class="skill-item"><span class="skill-name">MES Design &amp; Implementation</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.95"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">EBR / GxP Compliance</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.92"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Process Qualification (PQ/IQ/OQ)</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.90"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Siemens OpsCenter (PH)</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.90"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Microsoft Power Platform</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.82"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">SAP &amp; OSIsoft PI Integration</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.80"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Equipment Commissioning</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.85"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Emerson Delta V DCS</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.82"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">MATLAB / Simulink / Aspen HYSYS</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.81"></div></div><span class="skill-pct">0%</span></div>
        <div class="skill-item"><span class="skill-name">Data Science &amp; Supervised Learning</span><div class="skill-bar-bg"><div class="skill-bar" data-width="0.80"></div></div><span class="skill-pct">0%</span></div>
      </div>
    </div>
    <div>
      <div class="skill-category-title">Domain Expertise</div>
      <div class="skill-tags">
        <span class="skill-tag">Biologics Manufacturing</span>
        <span class="skill-tag">API Manufacturing</span>
        <span class="skill-tag">Electronic Batch Records</span>
        <span class="skill-tag">New Product Introduction</span>
        <span class="skill-tag">Tech Transfer</span>
        <span class="skill-tag">Process Digitization</span>
        <span class="skill-tag">Third Party Manufacturing</span>
        <span class="skill-tag">CAPEX Management</span>
        <span class="skill-tag">Vendor Negotiation</span>
        <span class="skill-tag">Process FMEA</span>
        <span class="skill-tag">Upstream &amp; Purification</span>
        <span class="skill-tag">SOP &amp; Technical Authoring</span>
        <span class="skill-tag">Lean Manufacturing</span>
        <span class="skill-tag">Root Cause Analysis</span>
      </div>
      <div style="margin-top: 28px;">
        <div class="skill-category-title">Leadership &amp; Management</div>
        <div class="skill-tags">
          <span class="skill-tag">Stakeholder Engagement</span>
          <span class="skill-tag">Cross-functional Leadership</span>
          <span class="skill-tag">Project Management</span>
          <span class="skill-tag">Risk Management</span>
          <span class="skill-tag">Global Collaboration</span>
          <span class="skill-tag">Budget Management</span>
          <span class="skill-tag">Procurement</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="section-header fade-up">
    <span class="section-number">05</span>
    <h2 class="section-title">Certifications</h2>
    <div class="section-rule"></div>
  </div>
  <div class="cert-grid">
    <div class="cert-card">
      <div class="cert-icon-wrap">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5"/></svg>
      </div>
      <div>
        <div class="cert-name">WSQ Data Science Bootcamp</div>
        <div class="cert-issuer">SkillsFuture Singapore</div>
      </div>
    </div>
    <div class="cert-card">
      <div class="cert-icon-wrap">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M12 18v-5.25m0 0a6.01 6.01 0 001.5-.189m-1.5.189a6.01 6.01 0 01-1.5-.189m3.75 7.478a12.06 12.06 0 01-4.5 0m3.75 2.383a14.406 14.406 0 01-3 0M14.25 18v-.192c0-.983.658-1.823 1.508-2.316a7.5 7.5 0 10-7.517 0c.85.493 1.509 1.333 1.509 2.316V18"/></svg>
      </div>
      <div>
        <div class="cert-name">Building Business Acumen</div>
        <div class="cert-issuer">Professional Development</div>
      </div>
    </div>
    <div class="cert-card">
      <div class="cert-icon-wrap">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75L11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 01-1.043 3.296 3.745 3.745 0 01-3.296 1.043A3.745 3.745 0 0112 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 01-3.296-1.043 3.745 3.745 0 01-1.043-3.296A3.745 3.745 0 013 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 011.043-3.296 3.746 3.746 0 013.296-1.043A3.746 3.746 0 0112 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 013.296 1.043 3.746 3.746 0 011.043 3.296A3.745 3.745 0 0121 12z"/></svg>
      </div>
      <div>
        <div class="cert-name">Pathway Certificate</div>
        <div class="cert-issuer">Professional Certification</div>
      </div>
    </div>
    <div class="cert-card">
      <div class="cert-icon-wrap">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M11.42 15.17L17.25 21A2.652 2.652 0 0021 17.25l-5.877-5.877M11.42 15.17l2.496-3.03c.317-.384.74-.626 1.208-.766M11.42 15.17l-4.655 5.653a2.548 2.548 0 11-3.586-3.586l6.837-5.63m5.108-.233c.55-.164 1.163-.188 1.743-.14a4.5 4.5 0 004.486-6.336l-3.276 3.277a3.004 3.004 0 01-2.25-2.25l3.276-3.276a4.5 4.5 0 00-6.336 4.486c.091 1.076-.071 2.264-.904 2.95l-.102.085m-1.745 1.437L5.909 7.5H4.5L2.25 3.75l1.5-1.5L7.5 4.5v1.409l4.26 4.26m-1.745 1.437l1.745-1.437m6.615 8.206L15.75 15.75M4.867 19.125h.008v.008h-.008v-.008z"/></svg>
      </div>
      <div>
        <div class="cert-name">Siemens OpsCenter Recipe Designer</div>
        <div class="cert-issuer">Qualified · Siemens</div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-header fade-up">
    <span class="section-number">06</span>
    <h2 class="section-title">Education</h2>
    <div class="section-rule"></div>
  </div>
  <div class="edu-grid">

    <div class="edu-card primary">
      <div>
        <div class="edu-institution">National University of Singapore (NUS)</div>
        <div class="edu-degree">Bachelor of Engineering<br>Chemical Engineering (Honours)</div>
        <div class="edu-details" style="margin-top:8px;">Aug 2016 — Jul 2020 &nbsp;·&nbsp; Singapore</div>
      </div>
      <div class="edu-badge">
        <span class="edu-badge-number">3.4</span>
        <span class="edu-badge-label">CAP / 5.0</span>
      </div>
    </div>

    <div class="edu-card">
      <div>
        <div class="edu-institution">University of Delaware</div>
        <div class="edu-degree">Exchange Programme · Chemical Engineering</div>
        <div class="edu-details" style="margin-top:6px;">2019 &nbsp;·&nbsp; Newark, Delaware, USA</div>
      </div>
      <div style="color: rgba(247,245,240,0.2); font-family:'Cormorant Garamond',serif; font-size:32px; font-weight:300; align-self:center;">✦</div>
    </div>

    <div class="edu-card">
      <div>
        <div class="edu-institution">Victoria Junior College</div>
        <div class="edu-degree">GCE 'A' Levels · Science</div>
        <div class="edu-details" style="margin-top:6px;">2012 — 2013 &nbsp;·&nbsp; Singapore</div>
      </div>
      <div style="color: rgba(247,245,240,0.2); font-family:'Cormorant Garamond',serif; font-size:32px; font-weight:300; align-self:center;">✦</div>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-header fade-up">
    <span class="section-number">07</span>
    <h2 class="section-title">Get in Touch</h2>
    <div class="section-rule"></div>
  </div>
  <div class="contact-grid">
    <div class="fade-up">
      <p class="contact-intro">Open to <em>new opportunities</em> in life sciences consulting, MES digitization, and biotech manufacturing.</p>
      <p style="font-size:14px; color:var(--ink-muted); max-width:360px; line-height:1.85; margin-top:4px;">Whether you're looking to discuss a project, explore a collaboration, or just connect — feel free to reach out through any of the channels below.</p>
    </div>
    <div class="contact-cards fade-up">
      <a href="mailto:mmarcustan95@gmail.com" class="contact-card">
        <div class="contact-card-icon">
          <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75"/></svg>
        </div>
        <div><div class="contact-card-label">Email</div><div class="contact-card-value">mmarcustan95@gmail.com</div></div>
      </a>
      <a href="tel:+6582827315" class="contact-card">
        <div class="contact-card-icon">
          <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z"/></svg>
        </div>
        <div><div class="contact-card-label">Phone</div><div class="contact-card-value">+65 8282 7315</div></div>
      </a>
      <a href="https://linkedin.com/in/marcustan1995" target="_blank" class="contact-card">
        <div class="contact-card-icon">
          <svg fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        </div>
        <div><div class="contact-card-label">LinkedIn</div><div class="contact-card-value">linkedin.com/in/marcustan1995</div></div>
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span class="footer-name">Marcus Tan Zse Fong</span>
  <span class="footer-copy">Singapore · Life Sciences &amp; Manufacturing Consultant</span>
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.timeline-item, .achievement-card, .cert-card, .edu-card, .project-card, .fade-up').forEach(el => observer.observe(el));

  document.querySelectorAll('.skill-bar').forEach(bar => {
    const o = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const val = parseFloat(bar.dataset.width);
          const pct = Math.round(val * 100);
          const color = val >= 0.90 ? '#16a34a' : val >= 0.85 ? '#22c55e' : '#4ade80';
          setTimeout(() => {
            bar.style.transform = `scaleX(${val})`;
            bar.style.background = color;
            const pctEl = bar.closest('.skill-item').querySelector('.skill-pct');
            if (pctEl) {
              let current = 0;
              const step = Math.ceil(pct / 40);
              const timer = setInterval(() => {
                current = Math.min(current + step, pct);
                pctEl.textContent = current + '%';
                pctEl.style.color = color;
                if (current >= pct) clearInterval(timer);
              }, 20);
            }
          }, 150);
          o.unobserve(bar);
        }
      });
    }, { threshold: 0.5 });
    o.observe(bar);
  });

  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const t = document.querySelector(a.getAttribute('href'));
      if (t) t.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });

  let last = 0;
  const nav = document.getElementById('main-nav');
  window.addEventListener('scroll', () => {
    const y = window.scrollY;
    nav.style.transform = y > last && y > 80 ? 'translateY(-100%)' : 'translateY(0)';
    last = y;
  });
</script>
</body>
</html>
