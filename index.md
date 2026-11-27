
---
layout: default
title: Andre Joe Mhawej | AI & ML Developer
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap');

:root {
  --bg: #080b16;
  --panel: #101629;
  --panel2: #151d35;
  --text: #f4f6ff;
  --muted: #9ba7c5;
  --cyan: #4de4ff;
  --purple: #a78bfa;
  --pink: #ff6eb4;
  --green: #67f5bd;
  --border: rgba(255,255,255,.11);
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Space Grotesk', sans-serif;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  z-index: -2;
  pointer-events: none;
  background:
    radial-gradient(circle at 15% 15%, rgba(77,228,255,.10), transparent 30%),
    radial-gradient(circle at 85% 25%, rgba(167,139,250,.13), transparent 32%),
    radial-gradient(circle at 50% 90%, rgba(255,110,180,.08), transparent 35%);
}

::selection {
  background: var(--cyan);
  color: #080b16;
}

a { color: inherit; }

/* BACKGROUND GRID */

.bg-grid {
  position: fixed;
  inset: 0;
  z-index: -1;
  pointer-events: none;
  opacity: .16;
  background-image:
    linear-gradient(rgba(255,255,255,.035) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,.035) 1px, transparent 1px);
  background-size: 45px 45px;
  mask-image: linear-gradient(to bottom, black, transparent 90%);
}

/* FLOATING PARTICLES */

.particles {
  position: fixed;
  inset: 0;
  z-index: -1;
  overflow: hidden;
  pointer-events: none;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: var(--cyan);
  opacity: .5;
  animation: floatParticle linear infinite;
}

@keyframes floatParticle {
  from { transform: translateY(110vh) scale(.5); }
  to { transform: translateY(-10vh) scale(1.5); }
}

/* PROGRESS BAR */

#progress {
  position: fixed;
  top: 0;
  left: 0;
  width: 0%;
  height: 3px;
  z-index: 1000;
  background: linear-gradient(90deg,var(--cyan),var(--purple),var(--pink));
  box-shadow: 0 0 12px var(--cyan);
}

/* NAVIGATION */

.navbar {
  position: sticky;
  top: 12px;
  z-index: 100;
  max-width: 1150px;
  margin: 15px auto;
  padding: 13px 22px;
  border: 1px solid var(--border);
  border-radius: 18px;
  background: rgba(8,11,22,.78);
  backdrop-filter: blur(18px);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  box-shadow: 0 8px 35px rgba(0,0,0,.2);
}

.logo {
  font-size: 19px;
  font-weight: 700;
  letter-spacing: -1px;
}

.logo span { color: var(--cyan); }

.navlinks {
  display: flex;
  gap: 24px;
  align-items: center;
}

.navlinks a {
  text-decoration: none;
  color: var(--muted);
  font-size: 13px;
  transition: .25s;
}

.navlinks a:hover {
  color: var(--cyan);
}

.nav-contact {
  padding: 9px 16px;
  border-radius: 10px;
  color: var(--bg) !important;
  background: linear-gradient(110deg,var(--cyan),#8daaff);
  font-weight: 700;
}

@media(max-width:650px) {
  .navbar { padding: 12px; }
  .navlinks { gap: 12px; }
  .navlinks a { font-size: 11px; }
  .navlinks a:nth-child(2) { display: none; }
  .logo { font-size: 16px; }
}

/* HERO */

.hero {
  max-width: 1150px;
  min-height: 620px;
  margin: auto;
  padding: 100px 25px 85px;
  display: grid;
  grid-template-columns: 1.2fr .8fr;
  align-items: center;
  gap: 45px;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 9px 14px;
  border: 1px solid rgba(77,228,255,.25);
  border-radius: 30px;
  background: rgba(77,228,255,.07);
  color: var(--cyan);
  font: 11px 'Space Mono', monospace;
  letter-spacing: 1px;
}

.online-dot {
  width: 8px;
  height: 8px;
  background: var(--green);
  border-radius: 50%;
  box-shadow: 0 0 12px var(--green);
  animation: blink 1.5s infinite;
}

@keyframes blink {
  50% { opacity: .3; }
}

.hero h1 {
  font-size: clamp(48px,7vw,88px);
  line-height: .98;
  letter-spacing: -5px;
  margin: 28px 0 20px;
  font-weight: 700;
}

.gradient-text {
  background: linear-gradient(100deg,var(--cyan),var(--purple),var(--pink));
  background-size: 200%;
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  animation: gradientMove 5s linear infinite;
}

@keyframes gradientMove {
  to { background-position: 200% center; }
}

.hero-description {
  color: var(--muted);
  font-size: 17px;
  line-height: 1.8;
  max-width: 570px;
}

.typing-line {
  color: var(--cyan);
  font: 13px 'Space Mono',monospace;
  margin-top: 20px;
  min-height: 22px;
}

.hero-buttons {
  display: flex;
  gap: 13px;
  flex-wrap: wrap;
  margin-top: 30px;
}

.btn {
  display: inline-block;
  padding: 13px 20px;
  border-radius: 11px;
  text-decoration: none !important;
  font-weight: 700;
  font-size: 14px;
  transition: transform .25s, box-shadow .25s;
}

.btn:hover {
  transform: translateY(-4px);
}

.btn-primary {
  color: #080b16 !important;
  background: linear-gradient(110deg,var(--cyan),#a2c5ff);
  box-shadow: 0 0 25px rgba(77,228,255,.2);
}

.btn-primary:hover {
  box-shadow: 0 0 35px rgba(77,228,255,.45);
}

.btn-secondary {
  color: var(--text) !important;
  border: 1px solid var(--border);
  background: rgba(255,255,255,.04);
}

.hero-image-wrap {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.orbit {
  position: absolute;
  width: 320px;
  height: 320px;
  border: 1px dashed rgba(77,228,255,.35);
  border-radius: 50%;
  animation: rotate 25s linear infinite;
}

.orbit::before {
  content: "";
  position: absolute;
  top: 35px;
  left: 35px;
  width: 12px;
  height: 12px;
  background: var(--pink);
  border-radius: 50%;
  box-shadow: 0 0 20px var(--pink);
}

.orbit-two {
  width: 390px;
  height: 390px;
  border-color: rgba(167,139,250,.25);
  animation-direction: reverse;
  animation-duration: 35s;
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}

.profile-photo {
  width: 225px;
  height: 225px;
  object-fit: cover;
  border-radius: 50%;
  border: 3px solid var(--cyan);
  padding: 7px;
  background: var(--panel);
  box-shadow: 0 0 35px rgba(77,228,255,.25);
  z-index: 2;
  animation: photoFloat 4s ease-in-out infinite;
}

@keyframes photoFloat {
  50% { transform: translateY(-12px); }
}

.floating-label {
  position: absolute;
  padding: 10px 14px;
  border: 1px solid var(--border);
  border-radius: 10px;
  background: rgba(16,22,41,.9);
  backdrop-filter: blur(10px);
  font: 11px 'Space Mono',monospace;
  color: var(--cyan);
  box-shadow: 0 8px 30px rgba(0,0,0,.25);
  z-index: 3;
  animation: photoFloat 4s ease-in-out infinite;
}

.label-one { top: 12%; right: -4%; }
.label-two { bottom: 12%; left: -5%; animation-delay: 1s; }

@media(max-width:850px) {
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
    padding-top: 75px;
  }
  .hero-description { margin: auto; }
  .hero-buttons { justify-content: center; }
  .hero-image-wrap { margin: 50px 0; min-height: 400px; }
  .hero h1 { letter-spacing: -3px; }
}

@media(max-width:430px) {
  .orbit { width: 260px; height: 260px; }
  .orbit-two { width: 310px; height: 310px; }
  .profile-photo { width: 185px; height: 185px; }
  .label-one { right: 0; }
  .label-two { left: 0; }
}

/* MARQUEE */

.marquee {
  overflow: hidden;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  background: rgba(255,255,255,.025);
  padding: 17px 0;
}

.marquee-track {
  display: flex;
  width: max-content;
  animation: marquee 28s linear infinite;
}

.marquee-track span {
  padding: 0 28px;
  font: 12px 'Space Mono',monospace;
  color: var(--muted);
  letter-spacing: 2px;
}

.marquee-track span::after {
  content: "✦";
  color: var(--cyan);
  margin-left: 50px;
}

@keyframes marquee {
  to { transform: translateX(-50%); }
}

/* SECTION */

.section {
  max-width: 1150px;
  margin: auto;
  padding: 100px 25px;
}

.section-heading {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 20px;
  margin-bottom: 38px;
}

.section-kicker {
  font: 11px 'Space Mono',monospace;
  color: var(--cyan);
  letter-spacing: 2px;
  margin-bottom: 12px;
}

.section-heading h2 {
  font-size: clamp(32px,5vw,48px);
  letter-spacing: -2px;
  margin: 0;
}

.section-heading p {
  color: var(--muted);
  font-size: 13px;
}

/* PROJECT CARDS */

.project-grid {
  display: grid;
  grid-template-columns: repeat(2,1fr);
  gap: 22px;
}

.project-card {
  position: relative;
  overflow: hidden;
  border: 1px solid var(--border);
  border-radius: 20px;
  background: linear-gradient(145deg,var(--panel),#0c1120);
  transition: transform .35s, border-color .35s, box-shadow .35s;
  transform-style: preserve-3d;
}

.project-card:hover {
  transform: translateY(-9px);
  border-color: rgba(77,228,255,.55);
  box-shadow: 0 20px 55px rgba(0,0,0,.35),0 0 30px rgba(77,228,255,.07);
}

.project-card.featured {
  grid-column: 1/-1;
  border-color: rgba(77,228,255,.4);
  background: linear-gradient(135deg,rgba(77,228,255,.09),var(--panel) 40%,rgba(167,139,250,.09));
}

.project-image {
  width: 100%;
  height: 240px;
  object-fit: cover;
  object-position: top;
  border-bottom: 1px solid var(--border);
  transition: transform .6s;
}

.project-card:hover .project-image {
  transform: scale(1.035);
}

.featured .project-image {
  height: 380px;
  object-fit: contain;
  background: #080b16;
}

.project-content {
  padding: 25px;
  position: relative;
}

.project-topline {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  align-items: center;
  margin-bottom: 14px;
}

.project-number {
  font: 11px 'Space Mono',monospace;
  color: var(--cyan);
}

.project-badge {
  font: 10px 'Space Mono',monospace;
  color: var(--green);
  border: 1px solid rgba(103,245,189,.3);
  background: rgba(103,245,189,.07);
  border-radius: 30px;
  padding: 6px 10px;
}

.project-card h3 {
  font-size: clamp(22px,3vw,30px);
  letter-spacing: -.8px;
  margin: 0 0 12px;
}

.project-card p {
  color: var(--muted);
  line-height: 1.75;
  font-size: 14px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin: 20px 0;
}

.project-tags span {
  padding: 6px 10px;
  border-radius: 7px;
  border: 1px solid var(--border);
  color: #c6d1ee;
  font: 10px 'Space Mono',monospace;
}

.project-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 22px;
}

.project-link {
  display: inline-block;
  padding: 10px 15px;
  border-radius: 9px;
  border: 1px solid rgba(77,228,255,.35);
  color: var(--cyan) !important;
  text-decoration: none !important;
  font-size: 12px;
  font-weight: 700;
  transition: .25s;
}

.project-link:hover {
  background: var(--cyan);
  color: var(--bg) !important;
  box-shadow: 0 0 20px rgba(77,228,255,.25);
}

.project-link.primary {
  color: var(--bg) !important;
  background: var(--cyan);
}

.project-link.primary:hover {
  background: white;
  border-color: white;
}

@media(max-width:700px) {
  .project-grid { grid-template-columns: 1fr; }
  .project-card.featured { grid-column: auto; }
  .featured .project-image { height: 230px; }
}

/* SKILLS */

.skills-panel {
  padding: 35px;
  border: 1px solid var(--border);
  border-radius: 20px;
  background: linear-gradient(135deg,rgba(167,139,250,.08),rgba(77,228,255,.04));
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.skill {
  padding: 12px 17px;
  border-radius: 10px;
  background: rgba(255,255,255,.045);
  border: 1px solid var(--border);
  color: #dce5ff;
  font-size: 13px;
  transition: .25s;
}

.skill:hover {
  background: var(--cyan);
  color: var(--bg);
  border-color: var(--cyan);
  transform: translateY(-5px) rotate(-2deg);
  box-shadow: 0 8px 22px rgba(77,228,255,.15);
}

/* ABOUT */

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 22px;
}

.about-card {
  padding: 30px;
  border: 1px solid var(--border);
  border-radius: 18px;
  background: var(--panel);
}

.about-card h3 {
  font-size: 21px;
  margin: 0 0 15px;
}

.about-card p {
  color: var(--muted);
  font-size: 14px;
  line-height: 1.8;
}

.about-icon {
  font-size: 27px;
  margin-bottom: 15px;
}

@media(max-width:700px) {
  .about-grid { grid-template-columns: 1fr; }
}

/* CREDENTIALS */

.credential-list {
  display: grid;
  gap: 13px;
}

.credential {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
  padding: 20px 22px;
  border: 1px solid var(--border);
  border-radius: 13px;
  background: var(--panel);
  text-decoration: none !important;
  transition: .25s;
}

.credential:hover {
  border-color: var(--purple);
  transform: translateX(7px);
  background: var(--panel2);
}

.credential strong { font-size: 15px; }
.credential small { display: block; color: var(--muted); margin-top: 5px; }
.credential .arrow { color: var(--purple); font-size: 22px; }

/* CONTACT */

.contact-section {
  max-width: 1150px;
  margin: 30px auto 80px;
  padding: 65px 35px;
  border: 1px solid rgba(77,228,255,.25);
  border-radius: 25px;
  text-align: center;
  background:
    radial-gradient(circle at 15% 20%,rgba(77,228,255,.13),transparent 35%),
    radial-gradient(circle at 85% 80%,rgba(167,139,250,.16),transparent 35%),
    var(--panel);
}

.contact-section h2 {
  font-size: clamp(32px,6vw,55px);
  letter-spacing: -2px;
  margin: 0 0 15px;
}

.contact-section p {
  color: var(--muted);
  margin-bottom: 27px;
}

.contact-email {
  font-size: clamp(19px,4vw,32px);
  font-weight: 700;
  color: var(--cyan) !important;
  text-decoration: none;
  transition: .25s;
}

.contact-email:hover {
  text-shadow: 0 0 25px var(--cyan);
}

.contact-details {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
  margin-top: 35px;
  color: var(--muted);
  font: 12px 'Space Mono',monospace;
}

/* FOOTER */

.footer {
  text-align: center;
  padding: 25px;
  border-top: 1px solid var(--border);
  color: var(--muted);
  font: 11px 'Space Mono',monospace;
}

/* SCROLL REVEAL */

.reveal {
  opacity: 0;
  transform: translateY(35px);
  transition: opacity .75s ease, transform .75s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* RESPONSIVE */

@media(max-width:600px) {
  .section { padding: 70px 18px; }
  .section-heading { align-items: start; flex-direction: column; }
  .skills-panel { padding: 22px; }
  .project-content { padding: 20px; }
  .contact-section { margin: 20px 15px 60px; padding: 45px 18px; }
}

@media(prefers-reduced-motion:reduce) {
  *,*::before,*::after {
    animation-duration: .01ms !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: .01ms !important;
  }
  .reveal { opacity: 1; transform: none; }
}
</style>

<div id="progress"></div>
<div class="bg-grid"></div>
<div class="particles" id="particles"></div>

<!-- NAVIGATION -->

<nav class="navbar">
  <div class="logo">ANDRE<span>.</span>DEV</div>
  <div class="navlinks">
    <a href="#work">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#credentials">Credentials</a>
    <a href="#contact" class="nav-contact">Let's Talk ↗</a>
  </div>
</nav>

<!-- HERO -->

<section class="hero">

  <div class="hero-text">
    <div class="eyebrow">
      <span class="online-dot"></span>
      AI / ML DEVELOPER
    </div>

    <h1>
      Hello, I'm<br>
      <span class="gradient-text">Andre-Joe.</span>
    </h1>

    <p class="hero-description">
      I turn data into intelligence. I build AI-powered applications,
      computer vision systems, predictive models, and tools that solve
      real-world problems.
    </p>

    <div class="typing-line">
      <span id="typing"></span><span style="animation:blink 1s infinite">▋</span>
    </div>

    <div class="hero-buttons">
      <a href="#work" class="btn btn-primary">Explore My Work ↓</a>
      <a href="#contact" class="btn btn-secondary">Contact Me ↗</a>
    </div>
  </div>

  <div class="hero-image-wrap">
    <div class="orbit"></div>
    <div class="orbit orbit-two"></div>

    <img class="profile-photo"
         src="/assets/me.jpg"
         alt="Andre Joe Mhawej">

    <div class="floating-label label-one">Python / AI</div>
    <div class="floating-label label-two">Computer Vision</div>
  </div>

</section>

<!-- MARQUEE -->

<div class="marquee">
  <div class="marquee-track" id="marquee">
    <span>ARTIFICIAL INTELLIGENCE</span>
    <span>MACHINE LEARNING</span>
    <span>COMPUTER VISION</span>
    <span>DEEP LEARNING</span>
    <span>PYTHON</span>
    <span>DATA SCIENCE</span>
    <span>ARTIFICIAL INTELLIGENCE</span>
    <span>MACHINE LEARNING</span>
    <span>COMPUTER VISION</span>
    <span>DEEP LEARNING</span>
    <span>PYTHON</span>
    <span>DATA SCIENCE</span>
  </div>
</div>

<!-- PROJECTS -->

<section class="section" id="work">

  <div class="section-heading reveal">
    <div>
      <div class="section-kicker">01 / SELECTED WORK</div>
      <h2>Things I've <span class="gradient-text">Built.</span></h2>
    </div>
    <p>From ideas to working systems.</p>
  </div>

  <div class="project-grid">

    <!-- SKY EYE -->

    <article class="project-card featured reveal">
      <img class="project-image"
           src="/assets/skyeye.png"
           alt="SkyEye traffic monitoring system">

      <div class="project-content">
        <div class="project-topline">
          <span class="project-number">PROJECT / 001</span>
          <span class="project-badge">★ FEATURED PROJECT</span>
        </div>

        <h3>SkyEye — AI Traffic Intelligence</h3>

        <p>
          A real-time traffic monitoring system built using dual YOLOv8
          models to detect multiple traffic violations and automatically
          extract supporting evidence.
        </p>

        <p>
          Developed individually, from data collection and annotation
          to preprocessing, model training, testing, and system implementation.
        </p>

        <p>
          Research paper accepted for the 2026 IEEE International Conference
          on Intelligent Computing and Next-Generation Technologies (ICONET).
        </p>

        <div class="project-tags">
          <span>YOLOv8</span>
          <span>COMPUTER VISION</span>
          <span>DEEP LEARNING</span>
          <span>OBJECT DETECTION</span>
          <span>PYTHON</span>
        </div>

        <div class="project-actions">
          <a class="project-link primary"
             href="/assets/SkyEye.html"
             target="_blank" rel="noopener">
            Explore Project ↗
          </a>

          <a class="project-link"
             href="/assets/Andre%20Joe%20Mhawej%20Paper.pdf"
             target="_blank" rel="noopener">
            Research Paper PDF ↗
          </a>
        </div>
      </div>
    </article>

    <!-- CHATBOT -->

    <article class="project-card reveal">
      <img class="project-image"
           src="/assets/chatbot-web.png"
           alt="University Assistant Chatbot">

      <div class="project-content">
        <div class="project-topline">
          <span class="project-number">PROJECT / 002</span>
          <span class="project-badge">AI APPLICATION</span>
        </div>

        <h3>University Assistant Chatbot</h3>

        <p>
          A personal AI assistant built around my AI coursework.
          Using embeddings and Retrieval-Augmented Generation (RAG),
          it retrieves relevant material to answer questions and explain concepts.
        </p>

        <div class="project-tags">
          <span>RAG</span>
          <span>EMBEDDINGS</span>
          <span>NLP</span>
          <span>PYTHON</span>
        </div>

        <div class="project-actions">
          <a class="project-link primary"
             href="https://andre-joe.github.io/University-Preview/"
             target="_blank" rel="noopener">
            Try the Chatbot ↗
          </a>
        </div>
      </div>
    </article>

    <!-- HOUSE PREDICTOR -->

    <article class="project-card reveal">
      <img class="project-image"
           src="/assets/HouseTop.png"
           alt="Lebanon House Price Predictor">

      <div class="project-content">
        <div class="project-topline">
          <span class="project-number">PROJECT / 003</span>
          <span class="project-badge">PREDICTIVE ML</span>
        </div>

        <h3>Lebanon House Price Predictor</h3>

        <p>
          An end-to-end machine learning project using a dataset
          collected in September 2025 to predict property prices
          in the Lebanese real estate market.
        </p>

        <div class="project-tags">
          <span>REGRESSION</span>
          <span>FEATURE ENGINEERING</span>
          <span>PANDAS</span>
          <span>DATA COLLECTION</span>
        </div>

        <div class="project-actions">
          <a class="project-link primary"
             href="https://andre-joe.github.io/House-Preview/"
             target="_blank" rel="noopener">
            Try Predictor ↗
          </a>
        </div>
      </div>
    </article>

  </div>
</section>

<!-- SKILLS -->

<section class="section" id="skills">

  <div class="section-heading reveal">
    <div>
      <div class="section-kicker">02 / TECHNICAL TOOLKIT</div>
      <h2>My <span class="gradient-text">Toolkit.</span></h2>
    </div>
    <p>Technologies and concepts I work with.</p>
  </div>

  <div class="skills-panel reveal">
    <div class="skills">
      <span class="skill">Python</span>
      <span class="skill">PyTorch</span>
      <span class="skill">YOLOv8</span>
      <span class="skill">Computer Vision</span>
      <span class="skill">Scikit-learn</span>
      <span class="skill">Pandas</span>
      <span class="skill">NumPy</span>
      <span class="skill">RAG</span>
      <span class="skill">Embeddings</span>
      <span class="skill">LLMs</span>
      <span class="skill">NLP</span>
      <span class="skill">LSTM</span>
      <span class="skill">Regression</span>
      <span class="skill">Classification</span>
      <span class="skill">Data Visualization</span>
      <span class="skill">Statistics</span>
      <span class="skill">Feature Engineering</span>
      <span class="skill">Google Colab</span>
    </div>
  </div>

</section>

<!-- PROFILE -->

<section class="section">

  <div class="section-heading reveal">
    <div>
      <div class="section-kicker">03 / A LITTLE ABOUT ME</div>
      <h2>Beyond the <span class="gradient-text">Code.</span></h2>
    </div>
  </div>

  <div class="about-grid">

    <div class="about-card reveal">
      <div class="about-icon">🧠</div>
      <h3>How I Think</h3>
      <p>
        I enjoy breaking down complex problems, working with data,
        experimenting with models, and turning technical ideas
        into practical applications.
      </p>
    </div>

    <div class="about-card reveal">
      <div class="about-icon">⚙️</div>
      <h3>How I Work</h3>
      <p>
        I value hands-on learning, independent problem-solving,
        experimentation, and understanding how systems work
        beyond simply using existing tools.
      </p>
    </div>

  </div>
</section>

<!-- CREDENTIALS -->

<section class="section" id="credentials">

  <div class="section-heading reveal">
    <div>
      <div class="section-kicker">04 / EDUCATION & ACHIEVEMENTS</div>
      <h2>Credentials<span class="gradient-text">.</span></h2>
    </div>
    <p>Learning, research, and academic background.</p>
  </div>

  <div class="credential-list reveal">

    <a class="credential"
       href="https://www.coursera.org/user/b2be56243c7bbe7e10eecb1fac05bd18"
       target="_blank" rel="noopener">
      <div>
        <strong>Coursera Certifications</strong>
        <small>Explore my courses and certificates</small>
      </div>
      <span class="arrow">↗</span>
    </a>

    <a class="credential"
       href="/assets/transcript.pdf"
       target="_blank" rel="noopener">
      <div>
        <strong>Academic Transcript</strong>
        <small>University academic record · PDF</small>
      </div>
      <span class="arrow">↗</span>
    </a>

    <a class="credential"
       href="https://github.com/Andre-Joe/Andre-Joe.github.io"
       target="_blank" rel="noopener">
      <div>
        <strong>GitHub Repository</strong>
        <small>Source code and portfolio website</small>
      </div>
      <span class="arrow">↗</span>
    </a>

  </div>
</section>

<!-- CONTACT -->

<section class="contact-section reveal" id="contact">

  <div class="section-kicker">05 / GET IN TOUCH</div>

  <h2>Have a project in <span class="gradient-text">mind?</span></h2>

  <p>
    Interested in AI, machine learning, or computer vision?
    Let's connect.
  </p>

  <a class="contact-email"
     href="mailto:amhawej38@gmail.com">
    amhawej38@gmail.com ↗
  </a>

  <div class="contact-details">
    <span>+961 71 679 208</span>
    <span>BEIRUT, LEBANON</span>
    <span>OPEN TO OPPORTUNITIES</span>
  </div>

</section>

<footer class="footer">
  © <span id="year"></span> ANDRE-JOE MHAWEJ · BUILT WITH HTML, CSS & JS
</footer>

<script>
(function() {
  "use strict";

  const reduceMotion = window.matchMedia(
    "(prefers-reduced-motion: reduce)"
  ).matches;

  // Current year
  document.getElementById("year").textContent =
    new Date().getFullYear();

  // Scroll progress
  function updateProgress() {
    const scrollable =
      document.documentElement.scrollHeight - window.innerHeight;

    const progress = scrollable > 0
      ? (window.scrollY / scrollable) * 100
      : 0;

    document.getElementById("progress").style.width =
      progress + "%";
  }

  window.addEventListener("scroll", updateProgress, {
    passive: true
  });

  updateProgress();

  // Typing animation
  const typingElement = document.getElementById("typing");

  const phrases = [
    "Building intelligent systems...",
    "Exploring computer vision...",
    "Turning data into insights...",
    "Training models, solving problems..."
  ];

  if (!reduceMotion) {
    let phraseIndex = 0;
    let charIndex = 0;
    let deleting = false;

    function typeEffect() {
      const phrase = phrases[phraseIndex];

      typingElement.textContent = phrase.substring(
        0,
        charIndex
      );

      if (!deleting) {
        charIndex++;

        if (charIndex > phrase.length) {
          deleting = true;
          setTimeout(typeEffect, 1200);
          return;
        }
      } else {
        charIndex--;

        if (charIndex < 0) {
          deleting = false;
          phraseIndex = (phraseIndex + 1) % phrases.length;
          charIndex = 0;
        }
      }

      setTimeout(typeEffect, deleting ? 35 : 65);
    }

    typeEffect();
  } else {
    typingElement.textContent = phrases[0];
  }

  // Floating particles
  const particleContainer =
    document.getElementById("particles");

  if (!reduceMotion) {
    for (let i = 0; i < 35; i++) {
      const particle = document.createElement("span");

      particle.className = "particle";
      particle.style.left = Math.random() * 100 + "%";
      particle.style.animationDuration =
        (10 + Math.random() * 20) + "s";
      particle.style.animationDelay =
        (-Math.random() * 25) + "s";
      particle.style.opacity =
        (0.15 + Math.random() * 0.4).toFixed(2);

      const size = 2 + Math.random() * 3;

      particle.style.width = size + "px";
      particle.style.height = size + "px";

      if (i % 3 === 0) {
        particle.style.background = "#a78bfa";
      } else if (i % 3 === 1) {
        particle.style.background = "#ff6eb4";
      }

      particleContainer.appendChild(particle);
    }
  }

  // Scroll reveal
  const revealElements =
    document.querySelectorAll(".reveal");

  if ("IntersectionObserver" in window && !reduceMotion) {
    const observer = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.12 }
    );

    revealElements.forEach(element => {
      observer.observe(element);
    });
  } else {
    revealElements.forEach(element => {
      element.classList.add("visible");
    });
  }

  // Subtle 3D project card tilt on desktop
  const cards = document.querySelectorAll(".project-card");

  if (!reduceMotion && window.matchMedia("(pointer:fine)").matches) {
    cards.forEach(card => {
      card.addEventListener("mousemove", event => {
        const rect = card.getBoundingClientRect();

        const x = (event.clientX - rect.left) / rect.width;
        const y = (event.clientY - rect.top) / rect.height;

        const rotateY = (x - 0.5) * 3;
        const rotateX = (0.5 - y) * 3;

        card.style.transform =
          `translateY(-7px) perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
      });

      card.addEventListener("mouseleave", () => {
        card.style.transform = "";
      });
    });
  }

})();
</script>
