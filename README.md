<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="generator" content="">
<title>Rocco Visagie — Full Stack Developer</title>
<style>
  /* Suppress any GitHub Pages injected elements */
  .site-header, .site-footer, header.site-header,
  #header, .header, .gh-header, .pagehead,
  [class*="github"], [id*="github"],
  .markdown-body > p:first-child a[href*="github"],
  body > a:first-child, body > p:first-child {
    display: none !important;
    visibility: hidden !important;
    height: 0 !important;
    overflow: hidden !important;
  }
</style>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700;1,900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0d0d0d;
    --paper: #f5f0e8;
    --rust: #c8401a;
    --gold: #d4a843;
    --slate: #2a2d35;
    --mist: #e8e3d8;
    --accent: #0d0d0d;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  a { color: inherit !important; text-decoration: none !important; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'Inter', sans-serif;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    position: fixed;
    width: 12px; height: 12px;
    background: var(--rust);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%, -50%);
    transition: transform 0.1s ease, width 0.2s, height 0.2s, background 0.2s;
    mix-blend-mode: multiply;
  }
  .cursor-ring {
    position: fixed;
    width: 40px; height: 40px;
    border: 1.5px solid var(--rust);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    transform: translate(-50%, -50%);
    transition: transform 0.25s ease, width 0.3s, height 0.3s;
    opacity: 0.6;
  }
  body:hover .cursor { opacity: 1; }

  /* Noise texture overlay */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 1000;
    opacity: 0.35;
  }

  .greeting-cursor {
    display: inline-block;
    color: var(--rust);
    animation: blink 0.9s step-end infinite;
    font-weight: 300;
  }
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  /* ─── NAV ─── */
  nav {
    position: absolute;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 4rem;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    letter-spacing: 0.1em;
    color: var(--ink);
  }
  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }
  .nav-links a {
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    color: var(--ink);
    position: relative;
    padding-bottom: 2px;
  }
  .nav-links a::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 0; height: 1.5px;
    background: var(--rust);
    transition: width 0.3s ease;
  }
  .nav-links a:hover::after { width: 100%; }

  /* ─── HERO ─── */
  #hero {
    height: 100vh;
    max-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    position: relative;
    overflow: hidden;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 5rem 3rem 3rem 4rem;
    position: relative;
    z-index: 2;
  }

  .hero-eyebrow {
    font-family: 'Inter', sans-serif;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--rust);
    margin-bottom: 1rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.3s forwards;
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5vw, 5rem);
    line-height: 1;
    letter-spacing: -0.01em;
    color: var(--ink);
    opacity: 0;
    animation: fadeUp 0.9s 0.5s forwards;
  }
  .hero-name span {
    display: block;
    color: var(--rust);
    -webkit-text-stroke: 0px;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: clamp(0.9rem, 1.5vw, 1.2rem);
    color: var(--slate);
    margin-top: 0.75rem;
    opacity: 0;
    animation: fadeUp 0.9s 0.7s forwards;
  }

  .hero-tagline {
    margin-top: 0.75rem;
    font-size: 0.8rem;
    line-height: 1.6;
    color: #555;
    max-width: 38ch;
    opacity: 0;
    animation: fadeUp 0.9s 0.9s forwards;
  }

  .hero-cta {
    display: inline-flex;
    align-items: center;
    gap: 0.8rem;
    margin-top: 2.5rem;
    padding: 0.9rem 2rem;
    background: var(--ink);
    color: var(--paper);
    text-decoration: none;
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.9s 1.1s forwards;
    transition: background 0.3s, transform 0.2s;
  }
  .hero-cta:hover { background: var(--rust); transform: translateY(-2px); }
  .hero-cta svg { transition: transform 0.3s; }
  .hero-cta:hover svg { transform: translateX(4px); }

  .hero-right {
    position: relative;
    background: var(--slate);
    overflow: hidden;
    clip-path: polygon(8% 0, 100% 0, 100% 100%, 0% 100%);
  }

  .hero-right-inner {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 6rem 3rem 4rem 5rem;
  }

  .hero-big-letter {
    font-family: 'Playfair Display', serif;
    font-size: 28vw;
    line-height: 0.8;
    color: rgba(255,255,255,0.04);
    position: absolute;
    bottom: -2rem;
    right: -1rem;
    pointer-events: none;
    user-select: none;
  }

  .contact-strip {
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
    opacity: 0;
    animation: fadeUp 0.9s 1.2s forwards;
  }
  .contact-item {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    color: rgba(245,240,232,0.75);
    font-size: 0.78rem;
    letter-spacing: 0.05em;
  }
  .contact-item .icon {
    width: 32px; height: 32px;
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.8rem;
    flex-shrink: 0;
    color: var(--gold);
  }

  .scroll-indicator {
    position: absolute;
    bottom: 2.5rem;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    font-family: 'Inter', sans-serif;
    font-size: 0.6rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--slate);
    opacity: 0;
    animation: fadeIn 1s 1.8s forwards;
  }
  .scroll-line {
    width: 1px;
    height: 50px;
    background: linear-gradient(to bottom, var(--rust), transparent);
    animation: scrollAnim 2s 2s infinite;
  }

  /* ─── SECTIONS ─── */
  section {
    position: relative;
  }

  .section-label {
    font-family: 'Inter', sans-serif;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--rust);
    margin-bottom: 1rem;
  }

  /* ─── ABOUT ─── */
  #about {
    padding: 3rem 4rem;
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 3rem;
    align-items: start;
    background: var(--paper);
    border-top: 1px solid rgba(0,0,0,0.08);
  }

  .about-sidebar {
  }

  .about-number {
    font-family: 'Playfair Display', serif;
    font-size: 5rem;
    color: var(--mist);
    line-height: 1;
    margin-bottom: -1rem;
  }

  .about-heading {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    letter-spacing: 0.02em;
    line-height: 1.1;
    color: var(--ink);
  }

  .about-body p {
    font-size: 0.88rem;
    line-height: 1.75;
    color: #444;
    margin-bottom: 1rem;
    max-width: 60ch;
  }

  .about-body p strong {
    color: var(--ink);
    font-weight: 700;
  }

  .divider {
    width: 60px;
    height: 3px;
    background: var(--rust);
    margin: 1rem 0;
  }

  /* ─── SKILLS ─── */
  #skills {
    padding: 3rem 4rem;
    background: var(--ink);
    color: var(--paper);
    overflow: hidden;
    position: relative;
  }

  #skills .section-label { color: var(--gold); }

  .skills-heading {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    line-height: 1;
    margin-bottom: 2rem;
    color: var(--paper);
  }
  .skills-heading em {
    color: var(--rust);
    font-style: normal;
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5px;
    background: rgba(255,255,255,0.06);
  }

  .skill-card {
    background: var(--slate);
    padding: 1.5rem 1.5rem;
    position: relative;
    overflow: hidden;
    transition: background 0.35s;
  }
  .skill-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 0;
    background: var(--rust);
    transition: height 0.4s ease;
  }
  .skill-card:hover { background: #232730; }
  .skill-card:hover::before { height: 100%; }

  .skill-icon {
    font-size: 1.8rem;
    margin-bottom: 1rem;
  }

  .skill-name {
    font-family: 'Inter', sans-serif;
    font-weight: 800;
    font-size: 0.95rem;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--paper);
    margin-bottom: 0.5rem;
  }

  .skill-desc {
    font-size: 0.78rem;
    color: rgba(245,240,232,0.5);
    line-height: 1.6;
  }

  /* ─── EXPERIENCE ─── */
  #experience {
    padding: 3rem 4rem;
    background: var(--mist);
  }

  .exp-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin-bottom: 2rem;
  }

  .exp-heading {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    line-height: 1;
    color: var(--ink);
  }

  .exp-count {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1rem;
    color: #888;
  }

  .exp-timeline {
    display: flex;
    flex-direction: column;
    gap: 0;
    border-left: 1.5px solid rgba(0,0,0,0.12);
    margin-left: 1rem;
    padding-left: 2.5rem;
  }

  .exp-item {
    position: relative;
    padding: 1.2rem 0;
    border-bottom: 1px solid rgba(0,0,0,0.06);
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 3rem;
    transition: background 0.2s;
  }
  .exp-item::before {
    content: '';
    position: absolute;
    left: -3.15rem;
    top: 2.4rem;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--paper);
    border: 2px solid rgba(0,0,0,0.2);
    transition: background 0.3s, border-color 0.3s;
  }
  .exp-item:hover::before {
    background: var(--rust);
    border-color: var(--rust);
  }

  .exp-meta {
    padding-top: 0.2rem;
  }

  .exp-date {
    font-family: 'Inter', sans-serif;
    font-size: 0.68rem;
    color: var(--rust);
    letter-spacing: 0.1em;
    margin-bottom: 0.5rem;
  }

  .exp-company {
    font-weight: 800;
    font-size: 0.85rem;
    color: #888;
    text-transform: uppercase;
    letter-spacing: 0.1em;
  }

  .exp-role {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--ink);
    margin-bottom: 0.5rem;
    line-height: 1.2;
  }

  .exp-detail {
    font-size: 0.82rem;
    color: #666;
    line-height: 1.7;
  }

  /* ─── EDUCATION ─── */
  #education {
    padding: 3rem 4rem;
    background: var(--paper);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: center;
  }

  .edu-visual {
    position: relative;
    height: 260px;
  }

  .edu-block {
    position: absolute;
    background: var(--slate);
    color: var(--paper);
    padding: 2.5rem;
  }
  .edu-block-1 {
    top: 0; left: 0;
    width: 80%;
    z-index: 2;
  }
  .edu-block-2 {
    bottom: 0; right: 0;
    width: 65%;
    background: var(--rust);
    padding: 2rem;
    z-index: 1;
  }

  .edu-block-label {
    font-family: 'Inter', sans-serif;
    font-size: 0.62rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    opacity: 0.6;
    margin-bottom: 0.75rem;
  }
  .edu-block-school {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    letter-spacing: 0.05em;
    line-height: 1.1;
    margin-bottom: 0.5rem;
  }
  .edu-block-program {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 1rem;
    opacity: 0.85;
  }
  .edu-block-year {
    margin-top: 1rem;
    font-size: 0.75rem;
    opacity: 0.5;
    font-family: 'Inter', sans-serif;
  }

  .edu-content .section-label { color: var(--rust); }

  .edu-heading {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.5rem);
    line-height: 1.1;
    color: var(--ink);
    margin-bottom: 1rem;
  }

  .edu-body {
    font-size: 0.9rem;
    color: #555;
    line-height: 1.8;
  }

  /* ─── REFERENCES ─── */
  #references {
    padding: 3rem 4rem;
    background: var(--slate);
    color: var(--paper);
    text-align: center;
  }

  #references .section-label { color: var(--gold); }

  .ref-heading {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    color: var(--paper);
    margin-bottom: 2rem;
  }

  .ref-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    background: rgba(255,255,255,0.05);
    max-width: 900px;
    margin: 0 auto;
  }

  .ref-card {
    background: #232730;
    padding: 1.5rem 1.5rem;
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
  }
  .ref-card:hover { background: #2a2f3a; }

  .ref-avatar {
    width: 56px; height: 56px;
    border-radius: 50%;
    background: var(--rust);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--paper);
    margin: 0 auto 1.2rem;
  }

  .ref-name {
    font-weight: 800;
    font-size: 0.95rem;
    letter-spacing: 0.05em;
    margin-bottom: 0.5rem;
  }

  .ref-phone {
    font-family: 'Inter', sans-serif;
    font-size: 0.75rem;
    color: var(--gold);
    letter-spacing: 0.08em;
  }

  /* ─── FOOTER ─── */
  footer {
    background: var(--ink);
    color: var(--paper);
    padding: 3rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid rgba(255,255,255,0.05);
  }

  .footer-logo {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    letter-spacing: 0.08em;
  }

  .footer-copy {
    font-size: 0.72rem;
    color: rgba(255,255,255,0.35);
    font-family: 'Inter', sans-serif;
    letter-spacing: 0.1em;
  }

  .footer-email {
    font-size: 0.78rem;
    color: var(--rust);
    text-decoration: none;
    letter-spacing: 0.05em;
    transition: color 0.2s;
  }
  .footer-email:hover { color: var(--gold); }

  /* ─── MARQUEE ─── */
  .marquee-section {
    background: var(--rust);
    padding: 1.2rem 0;
    overflow: hidden;
    position: relative;
  }

  /* ─── CTA MARQUEE ─── */
  .cta-marquee-section {
    display: block;
    background: var(--ink);
    padding: 1.6rem 0;
    overflow: hidden;
    text-decoration: none;
    cursor: none;
    transition: background 0.3s;
  }
  .cta-marquee-section:hover { background: var(--rust); }

  .cta-marquee-track {
    display: flex;
    white-space: nowrap;
    animation: marquee 18s linear infinite;
  }

  .cta-marquee-item {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    letter-spacing: 0.2em;
    color: var(--paper);
    padding: 0 2rem;
    text-transform: uppercase;
  }
  .cta-marquee-item.dim { color: rgba(245,240,232,0.35); }
  .cta-marquee-sep {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--rust);
    padding: 0 0.5rem;
    transition: color 0.3s;
  }
  .cta-marquee-section:hover .cta-marquee-sep { color: var(--gold); }
  .cta-marquee-section:hover .cta-marquee-item { color: var(--paper); }
  .cta-marquee-section:hover .cta-marquee-item.dim { color: rgba(245,240,232,0.5); }
  .marquee-track {
    display: flex;
    white-space: nowrap;
    animation: marquee 20s linear infinite;
  }
  .marquee-item {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    letter-spacing: 0.15em;
    color: rgba(245,240,232,0.6);
    padding: 0 3rem;
  }
  .marquee-item.accent { color: var(--paper); }

  /* ─── ANIMATIONS ─── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }
  @keyframes scrollAnim {
    0% { transform: scaleY(0); transform-origin: top; }
    50% { transform: scaleY(1); transform-origin: top; }
    50.01% { transform: scaleY(1); transform-origin: bottom; }
    100% { transform: scaleY(0); transform-origin: bottom; }
  }
  @keyframes marquee {
    from { transform: translateX(0); }
    to { transform: translateX(-50%); }
  }

  /* ─── REVEAL ─── */
  .reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.8s ease, transform 0.8s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    nav { padding: 1.5rem 2rem; }
    .nav-links { display: none; }
    #hero { grid-template-columns: 1fr; }
    .hero-right { display: none; }
    .hero-left { padding: 7rem 2rem 4rem; }
    #about { grid-template-columns: 1fr; padding: 5rem 2rem; gap: 3rem; }
    #skills { padding: 5rem 2rem; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    #experience { padding: 5rem 2rem; }
    .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
    #education { grid-template-columns: 1fr; padding: 5rem 2rem; }
    .edu-visual { height: 300px; }
    #references { padding: 5rem 2rem; }
    .ref-grid { grid-template-columns: 1fr; max-width: 400px; }
    footer { flex-direction: column; gap: 1rem; text-align: center; padding: 2rem; }
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- NAV -->
<nav>
  <div class="nav-logo">R·G·V</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#references">References</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-left">
    <div class="hero-eyebrow"><span class="greeting-typed" id="greetingText"></span><span class="greeting-cursor">|</span></div>
    <h1 class="hero-name">
      Rocco Given<br>
      <span>Visagie</span>
    </h1>
    <p class="hero-title">Aspiring Full Stack Developer</p>
    <p class="hero-tagline">
      Bridging the gap between design and development. Building experiences that are visually compelling, intuitive, and genuinely enjoyable to use.
    </p>
  </div>
  <div class="hero-right">
    <div class="hero-right-inner">
      <div class="contact-strip">
        <div class="hero-eyebrow" style="color:rgba(245,240,232,0.5); margin-bottom:2rem; opacity:1; animation-delay:1.3s;">— Contact Details</div>
        <div class="contact-item">
          <div class="icon">📍</div>
          <span>26 Kameeldoring St, Rouxville<br>Kuilsriver, Cape Town, 7580</span>
        </div>
        <div class="contact-item">
          <div class="icon">📧</div>
          <span>220343527@mycput.ac.za</span>
        </div>
        <div class="contact-item">
          <div class="icon">📞</div>
          <span>060 920 8354</span>
        </div>
        <div class="contact-item">
          <div class="icon">in</div>
          <a href="https://www.linkedin.com/in/rocco-given-visagie-597717312/?skipRedirect=true" target="_blank" style="color:rgba(245,240,232,0.75); text-decoration:none; letter-spacing:0.05em; font-size:0.78rem; transition:color 0.2s;" onmouseover="this.style.color='#d4a843'" onmouseout="this.style.color='rgba(245,240,232,0.75)'">linkedin.com/in/rocco-given-visagie</a>
        </div>
      </div>
    </div>
    <div class="hero-big-letter">R</div>
  </div>
  <div class="scroll-indicator">
    <div class="scroll-line"></div>
    scroll
  </div>
</section>

<!-- GET IN TOUCH MARQUEE -->
<a href="mailto:220343527@mycput.ac.za" class="cta-marquee-section">
  <div class="cta-marquee-track">
    <span class="cta-marquee-item">Get In Touch</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item dim">220343527@mycput.ac.za</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item">Get In Touch</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item dim">220343527@mycput.ac.za</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item">Get In Touch</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item dim">220343527@mycput.ac.za</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item">Get In Touch</span>
    <span class="cta-marquee-sep">→</span>
    <span class="cta-marquee-item dim">220343527@mycput.ac.za</span>
    <span class="cta-marquee-sep">→</span>
  </div>
</a>

<!-- MARQUEE -->
<div class="marquee-section">
  <div class="marquee-track">
    <span class="marquee-item accent">Java</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">JavaScript</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">UX/UI Design</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Full Stack</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Cape Town</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">CPUT</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Java</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">JavaScript</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">UX/UI Design</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Full Stack</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Cape Town</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">CPUT</span>
    <span class="marquee-item">·</span>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-sidebar reveal">
    <div class="section-label">Career Objective</div>
    <h2 class="about-heading">About<br>Me</h2>
  </div>
  <div class="about-body reveal">
    <p>
      I'm a <strong>final-year ICT Applications Development student</strong> at Cape Peninsula University of Technology, with a deep passion for crafting digital experiences that feel just right — visually compelling, intuitive, and enjoyable to use.
    </p>
    <div class="divider"></div>
    <p>
      I bridge the gap between design and development by leveraging strong <strong>Java and JavaScript skills</strong> to create clean, scalable solutions. My goal is to deliver seamless end-to-end applications that balance aesthetic detail with technical excellence.
    </p>
    <p>
      With diverse experience across customer service, retail, and events industries, I bring a unique human-centred perspective to every line of code I write.
    </p>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div style="margin-bottom: 1rem;" class="reveal">
    <div class="section-label">What I Bring</div>
    <h2 class="skills-heading">Technical<br><em>Skills</em></h2>
  </div>
  <div class="skills-grid">
    <div class="skill-card reveal">
      <div class="skill-icon">☕</div>
      <div class="skill-name">Java Programming</div>
      <div class="skill-desc">Building clean, scalable back-end solutions with strong OOP principles and Java fundamentals.</div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">⚡</div>
      <div class="skill-name">JavaScript</div>
      <div class="skill-desc">Dynamic front-end interactions, DOM manipulation, and modern ES6+ patterns for responsive interfaces.</div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🎨</div>
      <div class="skill-name">UX/UI Design</div>
      <div class="skill-desc">Designing interfaces that feel as good as they look — user-centred, accessible, and polished.</div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">📋</div>
      <div class="skill-name">Project Management</div>
      <div class="skill-desc">Coordinating deliverables, timelines, and team communication to keep projects on track.</div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🔍</div>
      <div class="skill-name">Debugging</div>
      <div class="skill-desc">Systematic problem-solving to identify, trace, and resolve bugs efficiently across the stack.</div>
    </div>
    <div class="skill-card reveal">
      <div class="skill-icon">🧪</div>
      <div class="skill-name">Usability Testing</div>
      <div class="skill-desc">Evaluating user flows and interactions to ensure applications meet real-world usability standards.</div>
    </div>
  </div>
</section>

<!-- MARQUEE 2 -->
<div class="marquee-section" style="background: var(--slate);">
  <div class="marquee-track" style="animation-direction: reverse;">
    <span class="marquee-item accent">Customer Experience</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Problem Solving</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Team Work</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Attention to Detail</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Adaptability</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Customer Experience</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Problem Solving</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Team Work</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item">Attention to Detail</span>
    <span class="marquee-item">·</span>
    <span class="marquee-item accent">Adaptability</span>
    <span class="marquee-item">·</span>
  </div>
</div>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="exp-header reveal">
    <h2 class="exp-heading">Work<br>Experience</h2>
    <span class="exp-count">Six roles & counting</span>
  </div>

  <div class="exp-timeline">
    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">Jun 2022 — Jan 2024</div>
        <div class="exp-company">Capita Call Centre</div>
      </div>
      <div>
        <div class="exp-role">Customer Experience Advisor</div>
        <div class="exp-detail">Marks & Spencer Campaign — Delivered high-quality customer support, handling complex queries with professionalism and empathy in a fast-paced call centre environment.</div>
      </div>
    </div>

    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">2022</div>
        <div class="exp-company">Deli Den Urban Farmhouse</div>
      </div>
      <div>
        <div class="exp-role">Cashier / Merchandiser / Sales</div>
        <div class="exp-detail">Managed point-of-sale operations, product merchandising, and customer-facing sales in a boutique urban farmhouse retail environment.</div>
      </div>
    </div>

    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">2021</div>
        <div class="exp-company">Footgear — Access Park</div>
      </div>
      <div>
        <div class="exp-role">Sales Associate</div>
        <div class="exp-detail">Assisted customers with product selection, maintained stock, and contributed to a positive in-store experience at a high-traffic retail outlet.</div>
      </div>
    </div>

    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">2019</div>
        <div class="exp-company">Dis-Chem</div>
      </div>
      <div>
        <div class="exp-role">Cashier / Merchandiser</div>
        <div class="exp-detail">Handled cash transactions and product placement in one of South Africa's leading pharmacy chains, building strong retail fundamentals.</div>
      </div>
    </div>

    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">2016</div>
        <div class="exp-company">Ignite Events Company</div>
      </div>
      <div>
        <div class="exp-role">Bartender / Waiter</div>
        <div class="exp-detail">Served guests at high-energy events, developing strong interpersonal skills, composure under pressure, and team coordination.</div>
      </div>
    </div>

    <div class="exp-item reveal">
      <div class="exp-meta">
        <div class="exp-date">2015</div>
        <div class="exp-company">Spur Steak Ranches</div>
      </div>
      <div>
        <div class="exp-role">Waiter</div>
        <div class="exp-detail">Delivered attentive table service in a family restaurant chain, honing communication skills and building a customer-first mindset from an early age.</div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="edu-visual reveal">
    <div class="edu-block edu-block-1">
      <div class="edu-block-label">Current Studies</div>
      <div class="edu-block-school">Cape Peninsula University<br>of Technology</div>
      <div class="edu-block-program">Diploma in ICT: Applications Development</div>
      <div class="edu-block-year">District Six Campus · Final Year</div>
    </div>
    <div class="edu-block edu-block-2">
      <div class="edu-block-label">Matriculated</div>
      <div class="edu-block-school">De Kuilen<br>High School</div>
      <div class="edu-block-program">NSC — Bachelor's Pass</div>
      <div class="edu-block-year">Completed 2015</div>
    </div>
  </div>
  <div class="edu-content reveal">
    <div class="section-label">Education</div>
    <h2 class="edu-heading">Building<br>The<br>Foundation</h2>
    <p class="edu-body">
      Currently completing my final year at CPUT's District Six Campus, where I've developed a strong grounding in software development, systems design, and application architecture.<br><br>
      From achieving a Bachelor's Pass at De Kuilen High School, to tackling the complexities of full-stack development — every step has been intentional.
    </p>
  </div>
</section>

<!-- REFERENCES -->
<section id="references">
  <div class="section-label reveal">References</div>
  <h2 class="ref-heading reveal">People Who<br>Know My Work</h2>
  <div class="ref-grid">
    <div class="ref-card reveal">
      <div class="ref-avatar">SP</div>
      <div class="ref-name">Stephen Pedro</div>
      <div class="ref-phone">076 072 5156</div>
    </div>
    <div class="ref-card reveal">
      <div class="ref-avatar">PH</div>
      <div class="ref-name">Phillip Human</div>
      <div class="ref-phone">083 395 8662</div>
    </div>
    <div class="ref-card reveal">
      <div class="ref-avatar">JH</div>
      <div class="ref-name">Justin Hector</div>
      <div class="ref-phone">082 948 7547</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Rocco Given Visagie</div>
  <a href="mailto:220343527@mycput.ac.za" class="footer-email">220343527@mycput.ac.za</a>
  <a href="https://www.linkedin.com/in/rocco-given-visagie-597717312/?skipRedirect=true" target="_blank" class="footer-email">LinkedIn ↗</a>
  <span class="footer-copy">© 2025 — Cape Town, ZA</span>
</footer>

<script>
  // Custom cursor
  const cursor = document.getElementById('cursor');
  const ring = document.getElementById('cursorRing');
  let mx = 0, my = 0, rx = 0, ry = 0;

  document.addEventListener('mousemove', e => {
    mx = e.clientX; my = e.clientY;
    cursor.style.left = mx + 'px';
    cursor.style.top = my + 'px';
  });

  function animateRing() {
    rx += (mx - rx) * 0.12;
    ry += (my - ry) * 0.12;
    ring.style.left = rx + 'px';
    ring.style.top = ry + 'px';
    requestAnimationFrame(animateRing);
  }
  animateRing();

  document.querySelectorAll('a, button').forEach(el => {
    el.addEventListener('mouseenter', () => {
      cursor.style.width = '20px';
      cursor.style.height = '20px';
      ring.style.width = '60px';
      ring.style.height = '60px';
    });
    el.addEventListener('mouseleave', () => {
      cursor.style.width = '12px';
      cursor.style.height = '12px';
      ring.style.width = '40px';
      ring.style.height = '40px';
    });
  });


  // Scroll reveal
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  // Typing greeting
  const greetings = [
    "Welcome. Based in Cape Town, ZA.",
    "Full Stack Developer in the making.",
    "Turning ideas into digital experiences.",
    "Design meets development. That's Rocco."
  ];
  const el = document.getElementById('greetingText');
  let gi = 0, ci = 0, deleting = false;
  function typeGreeting() {
    const current = greetings[gi];
    if (!deleting) {
      el.textContent = current.slice(0, ++ci);
      if (ci === current.length) { deleting = true; setTimeout(typeGreeting, 2200); return; }
    } else {
      el.textContent = current.slice(0, --ci);
      if (ci === 0) { deleting = false; gi = (gi + 1) % greetings.length; }
    }
    setTimeout(typeGreeting, deleting ? 35 : 70);
  }
  setTimeout(typeGreeting, 800);
</script>
</body>
</html>
