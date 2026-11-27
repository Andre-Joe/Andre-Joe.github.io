
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Andre Joe Mhawej — Engineer specializing in Artificial Intelligence and Computer Vision.">
  <meta name="theme-color" content="#08090d">

  <title>Andre Joe Mhawej | AI & Computer Vision</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #08090d;
      --surface: #101218;
      --text: #f0f0f2;
      --muted: #9295a2;
      --accent: #a5ffcb;
      --accent-2: #8ca8ff;
      --border: rgba(255,255,255,0.10);
      --mono: "DM Mono", monospace;
      --font: "Space Grotesk", sans-serif;
      --max-width: 1160px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font);
      overflow-x: hidden;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    ::selection {
      background: var(--accent);
      color: #08090d;
    }

    /* BACKGROUND */

    .background-glow {
      position: fixed;
      inset: 0;
      z-index: -2;
      pointer-events: none;
      background:
        radial-gradient(ellipse at 15% 15%, rgba(140,168,255,0.10), transparent 35%),
        radial-gradient(ellipse at 85% 45%, rgba(165,255,203,0.07), transparent 35%),
        var(--bg);
    }

    .grid-background {
      position: fixed;
      inset: 0;
      z-index: -1;
      pointer-events: none;
      opacity: 0.13;
      background-image:
        linear-gradient(rgba(255,255,255,0.045) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.045) 1px, transparent 1px);
      background-size: 55px 55px;
      mask-image: linear-gradient(to bottom, black, transparent 85%);
    }

    #particles {
      position: fixed;
      inset: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      pointer-events: none;
    }

    /* GENERAL */

    .container {
      width: min(var(--max-width), calc(100% - 48px));
      margin: 0 auto;
    }

    .section {
      padding: 115px 0;
    }

    .section-heading {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 45px;
    }

    .section-number {
      font-family: var(--mono);
      font-size: 13px;
      color: var(--accent);
    }

    .section-heading h2 {
      font-size: clamp(28px, 4vw, 42px);
      letter-spacing: -1.5px;
    }

    .section-heading::after {
      content: "";
      height: 1px;
      flex: 1;
      background: var(--border);
      margin-left: 15px;
    }

    /* NAVIGATION */

    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 100;
      border-bottom: 1px solid transparent;
      transition: 0.3s ease;
    }

    .navbar.scrolled {
      background: rgba(8,9,13,0.88);
      backdrop-filter: blur(18px);
      border-bottom-color: var(--border);
    }

    .nav-inner {
      width: min(var(--max-width), calc(100% - 48px));
      height: 78px;
      margin: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 19px;
      font-weight: 700;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--accent);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 32px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 13px;
      transition: 0.25s;
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    .nav-contact {
      padding: 10px 17px;
      border: 1px solid var(--accent);
      border-radius: 4px;
      color: var(--accent) !important;
    }

    .nav-contact:hover {
      background: var(--accent);
      color: var(--bg) !important;
    }

    .menu-toggle {
      display: none;
      background: none;
      border: none;
      color: var(--text);
      font-size: 26px;
      cursor: pointer;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 140px 0 90px;
      position: relative;
    }

    .hero-content {
      display: grid;
      grid-template-columns: 1.35fr 0.65fr;
      align-items: center;
      gap: 60px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-family: var(--mono);
      font-size: 12px;
      color: var(--accent);
      letter-spacing: 1.5px;
      margin-bottom: 27px;
    }

    .online-dot {
      width: 8px;
      height: 8px;
      background: var(--accent);
      border-radius: 50%;
      box-shadow: 0 0 12px var(--accent);
      animation: pulse 1.8s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.35; }
    }

    .hero h1 {
      font-size: clamp(48px, 7vw, 88px);
      line-height: 1.04;
      letter-spacing: -5px;
      font-weight: 700;
      margin-bottom: 25px;
    }

    .gradient-text {
      background: linear-gradient(100deg, var(--accent), var(--accent-2));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-description {
      color: var(--muted);
      font-size: 17px;
      max-width: 590px;
      line-height: 1.9;
      margin-bottom: 34px;
    }

    .typing-line {
      color: var(--accent);
      font-family: var(--mono);
      font-size: 14px;
      min-height: 24px;
      margin-bottom: 35px;
    }

    .cursor {
      display: inline-block;
      width: 7px;
      height: 16px;
      background: var(--accent);
      vertical-align: middle;
      margin-left: 4px;
      animation: blink 0.8s infinite;
    }

    @keyframes blink {
      50% { opacity: 0; }
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 13px 22px;
      border-radius: 4px;
      font-size: 13px;
      font-weight: 600;
      transition: 0.25s ease;
    }

    .btn-primary {
      color: #08090d;
      background: var(--accent);
      border: 1px solid var(--accent);
    }

    .btn-primary:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 30px rgba(165,255,203,0.2);
    }

    .btn-outline {
      border: 1px solid var(--border);
      color: var(--text);
    }

    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-4px);
    }

    /* PROFILE IMAGE */

    .profile-area {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .profile-orbit {
      width: min(330px, 75vw);
      aspect-ratio: 1;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .orbit-ring {
      position: absolute;
      inset: 0;
      border: 1px solid rgba(165,255,203,0.28);
      border-radius: 50%;
      animation: rotate 18s linear infinite;
    }

    .orbit-ring::before {
      content: "";
      position: absolute;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: var(--accent);
      top: 35px;
      left: 30px;
      box-shadow: 0 0 18px var(--accent);
    }

    .orbit-ring-two {
      inset: 17px;
      border-color: rgba(140,168,255,0.25);
      animation-direction: reverse;
      animation-duration: 25s;
    }

    @keyframes rotate {
      to { transform: rotate(360deg); }
    }

    .profile-image {
      width: 76%;
      height: 76%;
      object-fit: cover;
      border-radius: 50%;
      border: 3px solid rgba(165,255,203,0.6);
      box-shadow: 0 0 50px rgba(165,255,203,0.12);
      animation: float 5s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-12px); }
    }

    /* MARQUEE */

    .marquee-wrapper {
      overflow: hidden;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      padding: 22px 0;
      background: rgba(255,255,255,0.015);
    }

    .marquee {
      display: flex;
      width: max-content;
      animation: marquee 28s linear infinite;
    }

    .marquee span {
      font-family: var(--mono);
      font-size: 13px;
      letter-spacing: 2px;
      color: var(--muted);
      padding: 0 35px;
      white-space: nowrap;
    }

    .marquee span::after {
      content: "✳";
      color: var(--accent);
      margin-left: 65px;
    }

    @keyframes marquee {
      to { transform: translateX(-50%); }
    }

    /* PROJECTS */

    .projects-intro {
      color: var(--muted);
      max-width: 620px;
      margin-top: -25px;
      margin-bottom: 42px;
    }

    .projects-grid {
      display: flex;
      flex-direction: column;
      gap: 25px;
    }

    .project-card {
      display: grid;
      grid-template-columns: 42% 58%;
      align-items: stretch;
      overflow: hidden;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 8px;
      transition: transform 0.35s ease, border-color 0.35s ease;
    }

    .project-card:hover {
      border-color: rgba(165,255,203,0.55);
      transform: translateY(-5px);
    }

    .project-image {
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 260px;
      padding: 15px;
      overflow: hidden;
      background: #171a23;
    }

    .project-image img {
      display: block;
      width: 100%;
      height: 100%;
      min-height: 0;
      max-height: 360px;
      object-fit: contain;
      transition: transform 0.5s ease;
    }

    .project-card:hover .project-image img {
      transform: scale(1.025);
    }

    .project-content {
      padding: 30px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .project-label {
      font-family: var(--mono);
      color: var(--accent);
      font-size: 11px;
      letter-spacing: 1.5px;
      margin-bottom: 15px;
    }

    .project-content h3 {
      font-size: 25px;
      letter-spacing: -0.8px;
      margin-bottom: 14px;
    }

    .project-content p {
      color: var(--muted);
      font-size: 14px;
      line-height: 1.85;
      margin-bottom: 22px;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 25px;
    }

    .tag {
      font-family: var(--mono);
      font-size: 10px;
      padding: 6px 9px;
      color: var(--accent);
      border: 1px solid rgba(165,255,203,0.2);
      border-radius: 3px;
      background: rgba(165,255,203,0.04);
    }

    .project-links {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: auto;
    }

    .project-links a {
      font-size: 12px;
      color: var(--text);
      border-bottom: 1px solid var(--accent);
      padding-bottom: 4px;
      transition: 0.2s;
    }

    .project-links a:hover {
      color: var(--accent);
    }

    /* SKILLS */

    .skills-intro {
      color: var(--muted);
      max-width: 620px;
      margin-top: -25px;
      margin-bottom: 40px;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .skill-card {
      padding: 28px;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 7px;
      transition: 0.3s ease;
    }

    .skill-card:hover {
      border-color: rgba(165,255,203,0.5);
      transform: translateY(-5px);
    }

    .skill-icon {
      font-size: 25px;
      color: var(--accent);
      margin-bottom: 18px;
    }

    .skill-card h3 {
      font-size: 17px;
      margin-bottom: 14px;
    }

    .skill-card p {
      font-size: 13px;
      color: var(--muted);
      line-height: 1.9;
    }

    /* CREDENTIALS */

    .credentials-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .credential-card {
      padding: 30px;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 7px;
      transition: 0.3s;
    }

    .credential-card:hover {
      border-color: rgba(165,255,203,0.45);
      transform: translateY(-5px);
    }

    .credential-type {
      color: var(--accent);
      font-family: var(--mono);
      font-size: 11px;
      letter-spacing: 1.5px;
      margin-bottom: 15px;
    }

    .credential-card h3 {
      font-size: 19px;
      margin-bottom: 10px;
    }

    .credential-card p {
      color: var(--muted);
      font-size: 13px;
      line-height: 1.8;
      margin-bottom: 20px;
    }

    .credential-card a {
      font-size: 12px;
      color: var(--accent);
      border-bottom: 1px solid rgba(165,255,203,0.5);
      padding-bottom: 4px;
    }

    /* CONTACT */

    .contact-section {
      padding-bottom: 100px;
    }

    .contact-panel {
      position: relative;
      overflow: hidden;
      padding: 65px;
      border: 1px solid rgba(165,255,203,0.25);
      border-radius: 9px;
      background:
        radial-gradient(circle at 90% 10%, rgba(165,255,203,0.10), transparent 35%),
        var(--surface);
    }

    .contact-panel h2 {
      font-size: clamp(32px, 5vw, 55px);
      letter-spacing: -2px;
      margin-bottom: 15px;
    }

    .contact-panel > p {
      color: var(--muted);
      max-width: 550px;
      margin-bottom: 32px;
    }

    .contact-links {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .contact-links a {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      padding: 12px 17px;
      border: 1px solid var(--border);
      border-radius: 4px;
      font-size: 12px;
      transition: 0.25s;
    }

    .contact-links a:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-3px);
    }

    /* FOOTER */

    .footer {
      border-top: 1px solid var(--border);
      padding: 28px 0;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      color: var(--muted);
      font-family: var(--mono);
      font-size: 11px;
    }

    .back-to-top {
      color: var(--accent);
    }

    /* SCROLL ANIMATIONS */

    .reveal {
      opacity: 0;
      transform: translateY(35px);
      transition: opacity 0.8s ease, transform 0.8s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .progress-bar {
      position: fixed;
      top: 0;
      left: 0;
      height: 2px;
      width: 0;
      background: var(--accent);
      z-index: 200;
      box-shadow: 0 0 10px var(--accent);
    }

    /* TABLET */

    @media (max-width: 850px) {
      .hero-content {
        grid-template-columns: 1fr;
        gap: 55px;
      }

      .hero-text {
        order: 2;
      }

      .profile-area {
        order: 1;
      }

      .profile-orbit {
        width: 230px;
      }

      .hero {
        padding-top: 125px;
      }

      .hero h1 {
        letter-spacing: -3px;
      }

      .project-card {
        grid-template-columns: 1fr;
      }

      .project-image {
        min-height: 220px;
      }

      .project-image img {
        max-height: 320px;
      }

      .skills-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    /* MOBILE */

    @media (max-width: 650px) {
      .container,
      .nav-inner {
        width: min(100% - 32px, var(--max-width));
      }

      .nav-inner {
        height: 68px;
      }

      .menu-toggle {
        display: block;
      }

      .nav-links {
        position: absolute;
        top: 68px;
        left: 0;
        width: 100%;
        display: none;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 10px 24px 20px;
        background: rgba(8,9,13,0.97);
        border-bottom: 1px solid var(--border);
      }

      .nav-links.open {
        display: flex;
      }

      .nav-links li a {
        display: block;
        padding: 13px 0;
      }

      .nav-contact {
        display: inline-block !important;
        width: fit-content;
        margin-top: 8px;
      }

      .section {
        padding: 80px 0;
      }

      .hero {
        min-height: auto;
        padding: 120px 0 80px;
      }

      .hero h1 {
        font-size: clamp(44px, 13vw, 65px);
      }

      .hero-description {
        font-size: 15px;
      }

      .skills-grid,
      .credentials-grid {
        grid-template-columns: 1fr;
      }

      .project-content {
        padding: 24px;
      }

      .project-image {
        min-height: 180px;
        padding: 12px;
      }

      .project-image img {
        max-height: 260px;
      }

      .contact-panel {
        padding: 35px 25px;
      }

      .footer-inner {
        flex-direction: column;
        align-items: flex-start;
      }

      .section-heading h2 {
        font-size: 30px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        scroll-behavior: auto !important;
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
      }

      .reveal {
        opacity: 1;
        transform: none;
      }
    }
  </style>
</head>

<body>

  <div class="background-glow"></div>
  <div class="grid-background"></div>
  <canvas id="particles"></canvas>
  <div class="progress-bar" id="progressBar"></div>

  <!-- NAVIGATION -->

  <header class="navbar" id="navbar">
    <nav class="nav-inner">
      <a href="#home" class="logo">ANDRE<span>-JOE</span></a>

      <button class="menu-toggle" id="menuToggle" aria-label="Toggle navigation">
        ☰
      </button>

      <ul class="nav-links" id="navLinks">
        <li><a href="#home">Home</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#credentials">Credentials</a></li>
        <li><a href="#contact" class="nav-contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>

    <!-- HERO -->

    <section class="hero" id="home">
      <div class="container hero-content">

        <div class="hero-text">
          <div class="eyebrow">
            <span class="online-dot"></span>
            AI & COMPUTER VISION DEVELOPER
          </div>

          <h1>
            Hello, I'm<br>
            <span class="gradient-text">Andre-Joe.</span>
          </h1>

          <p class="hero-description">
            I build intelligent systems using Artificial Intelligence and
            Computer Vision, from real-time object detection to practical
            applications that solve real-world problems.
          </p>

          <div class="typing-line">
            <span id="typingText"></span><span class="cursor"></span>
          </div>

          <div class="hero-buttons">
            <a href="#projects" class="btn btn-primary">
              Explore My Work <span>↗</span>
            </a>

            <a href="#contact" class="btn btn-outline">
              Get In Touch
            </a>
          </div>
        </div>

        <div class="profile-area">
          <div class="profile-orbit">
            <div class="orbit-ring"></div>
            <div class="orbit-ring orbit-ring-two"></div>
            <img
              src="/assets/me.jpg"
              alt="Andre Joe Mhawej"
              class="profile-image"
            >
          </div>
        </div>

      </div>
    </section>

    <!-- TECHNOLOGY MARQUEE -->

    <div class="marquee-wrapper">
      <div class="marquee">
        <span>ARTIFICIAL INTELLIGENCE</span>
        <span>COMPUTER VISION</span>
        <span>DEEP LEARNING</span>
        <span>OBJECT DETECTION</span>
        <span>YOLOv8</span>
        <span>PYTHON</span>

        <span>ARTIFICIAL INTELLIGENCE</span>
        <span>COMPUTER VISION</span>
        <span>DEEP LEARNING</span>
        <span>OBJECT DETECTION</span>
        <span>YOLOv8</span>
        <span>PYTHON</span>
      </div>
    </div>

    <!-- PROJECTS -->

    <section class="section" id="projects">
      <div class="container">

        <div class="section-heading reveal">
          <span class="section-number">01 /</span>
          <h2>Selected Projects</h2>
        </div>

        <p class="projects-intro reveal">
          A selection of projects where I apply engineering, programming,
          and intelligent technologies to solve practical problems.
        </p>

        <div class="projects-grid">

          <!-- SKY EYE -->

          <article class="project-card reveal">
            <div class="project-image">
              <img
                src="/assets/skyeye.png"
                alt="SkyEye traffic monitoring system"
                loading="lazy"
              >
            </div>

            <div class="project-content">
              <div class="project-label">FEATURED PROJECT / COMPUTER VISION</div>

              <h3>SkyEye</h3>

              <p>
                A real-time traffic monitoring system designed to detect
                multiple traffic violations using two YOLOv8 models.
                The system processes road-camera footage and automatically
                extracts evidence, reducing the need for continuous manual
                monitoring.
              </p>

              <div class="tags">
                <span class="tag">Python</span>
                <span class="tag">YOLOv8</span>
                <span class="tag">Computer Vision</span>
                <span class="tag">Deep Learning</span>
                <span class="tag">Object Detection</span>
              </div>

              <div class="project-links">
                <a href="/assets/SkyEye.html" target="_blank" rel="noopener">
                  Explore the System ↗
                </a>

                <a href="/assets/Andre%20Joe%20Mhawej%20Paper.pdf" target="_blank" rel="noopener">
                  Read Research Paper ↗
                </a>
              </div>
            </div>
          </article>

          <!-- CHATBOT -->

          <article class="project-card reveal">
            <div class="project-image">
              <img
                src="/assets/chatbot-web.png"
                alt="AI chatbot web application"
                loading="lazy"
              >
            </div>

            <div class="project-content">
              <div class="project-label">AI APPLICATION</div>

              <h3>AI Chatbot</h3>

              <p>
                A web-based chatbot application that provides an interactive
                conversational experience through an AI-powered interface.
              </p>

              <div class="tags">
                <span class="tag">Artificial Intelligence</span>
                <span class="tag">Python</span>
                <span class="tag">Web Development</span>
              </div>

              <div class="project-links">
                <a href="https://andre-joe.github.io/University-Preview/" target="_blank" rel="noopener">
                  Chat with the Bot ↗
                </a>
              </div>
            </div>
          </article>

          <!-- HOUSE PRICE PREDICTOR -->

          <article class="project-card reveal">
            <div class="project-image">
              <img
                src="/assets/HouseTop.png"
                alt="House price prediction application"
                loading="lazy"
              >
            </div>

            <div class="project-content">
              <div class="project-label">MACHINE LEARNING APPLICATION</div>

              <h3>House Price Predictor</h3>

              <p>
                A predictive application that estimates house prices based
                on property-related information, demonstrating the use of
                data and machine learning for practical prediction tasks.
              </p>

              <div class="tags">
                <span class="tag">Machine Learning</span>
                <span class="tag">Python</span>
                <span class="tag">Prediction</span>
              </div>

              <div class="project-links">
                <a href="https://andre-joe.github.io/House-Preview/" target="_blank" rel="noopener">
                  Predict a House Price ↗
                </a>
              </div>
            </div>
          </article>

        </div>
      </div>
    </section>

    <!-- SKILLS -->

    <section class="section" id="skills">
      <div class="container">

        <div class="section-heading reveal">
          <span class="section-number">02 /</span>
          <h2>Technical Skills</h2>
        </div>

        <p class="skills-intro reveal">
          Technologies and areas I work with across Artificial Intelligence,
          Computer Vision, and software development.
        </p>

        <div class="skills-grid">

          <div class="skill-card reveal">
            <div class="skill-icon">⌘</div>
            <h3>Programming</h3>
            <p>
              Python, object-oriented programming, problem solving,
              and software development fundamentals.
            </p>
          </div>

          <div class="skill-card reveal">
            <div class="skill-icon">◉</div>
            <h3>Computer Vision</h3>
            <p>
              Object detection, image processing, video analysis,
              bounding boxes, and real-time vision applications.
            </p>
          </div>

          <div class="skill-card reveal">
            <div class="skill-icon">✳</div>
            <h3>Deep Learning</h3>
            <p>
              Neural networks, YOLOv8, model training, evaluation,
              dataset preparation, and performance optimization.
            </p>
          </div>

          <div class="skill-card reveal">
            <div class="skill-icon">⌬</div>
            <h3>Artificial Intelligence</h3>
            <p>
              Machine learning concepts, predictive systems,
              supervised learning, and practical AI applications.
            </p>
          </div>

          <div class="skill-card reveal">
            <div class="skill-icon">▤</div>
            <h3>Data Preparation</h3>
            <p>
              Data collection, annotation, preprocessing,
              augmentation, and dataset organization.
            </p>
          </div>

          <div class="skill-card reveal">
            <div class="skill-icon">⌘</div>
            <h3>Development Tools</h3>
            <p>
              Git, GitHub, Roboflow, development environments,
              and technical documentation.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- CREDENTIALS -->

    <section class="section" id="credentials">
      <div class="container">

        <div class="section-heading reveal">
          <span class="section-number">03 /</span>
          <h2>Credentials</h2>
        </div>

        <div class="credentials-grid">

          <div class="credential-card reveal">
            <div class="credential-type">RESEARCH PUBLICATION</div>

            <h3>IEEE Conference Paper</h3>

            <p>
              SkyEye: A Real-Time Multi-Violation Traffic Monitoring System
              Using Dual YOLOv8 Models with Automated Evidence Extraction.
              Published in the 2026 IEEE International Conference on
              Intelligent Computing and Next-Generation Technologies.
            </p>

            <a
              href="/assets/Andre%20Joe%20Mhawej%20Paper.pdf"
              target="_blank"
              rel="noopener"
            >
              View Research Paper ↗
            </a>
          </div>

          <div class="credential-card reveal">
            <div class="credential-type">ACADEMIC BACKGROUND</div>

            <h3>Academic Transcript</h3>

            <p>
              Academic record documenting my engineering studies
              and university coursework.
            </p>

            <a href="/assets/transcript.pdf" target="_blank" rel="noopener">
              View Transcript ↗
            </a>
          </div>

          <div class="credential-card reveal">
            <div class="credential-type">ONLINE LEARNING</div>

            <h3>Coursera</h3>

            <p>
              Online learning profile and completed coursework.
            </p>

            <a
              href="https://www.coursera.org/user/b2be56243c7bbe7e10eecb1fac05bd18"
              target="_blank"
              rel="noopener"
            >
              View Profile ↗
            </a>
          </div>

        </div>
      </div>
    </section>

    <!-- CONTACT -->

    <section class="section contact-section" id="contact">
      <div class="container">

        <div class="contact-panel reveal">
          <div class="eyebrow">
            <span class="online-dot"></span>
            CONTACT
          </div>

          <h2>
            Let's build something<br>
            <span class="gradient-text">intelligent.</span>
          </h2>

          <p>
            Interested in Artificial Intelligence, Computer Vision,
            and engineering opportunities. Feel free to reach out.
          </p>

          <div class="contact-links">

            <a href="mailto:amhawej38@gmail.com">
              Email ↗
            </a>

            <a
              href="https://www.linkedin.com/in/andre-joe-mhawej-55a081279"
              target="_blank"
              rel="noopener"
            >
              LinkedIn ↗
            </a>

            <a href="tel:+96171679208">
              +961 71 679 208
            </a>

          </div>
        </div>

      </div>
    </section>

  </main>

  <!-- FOOTER -->

  <footer class="footer">
    <div class="container footer-inner">
      <span>© <span id="year"></span> ANDRE-JOE MHAWEJ</span>
      <a href="#home" class="back-to-top">BACK TO TOP ↑</a>
    </div>
  </footer>

  <script>
    // CURRENT YEAR

    document.getElementById("year").textContent =
      new Date().getFullYear();


    // NAVIGATION SCROLL EFFECT

    const navbar = document.getElementById("navbar");

    window.addEventListener("scroll", () => {
      navbar.classList.toggle("scrolled", window.scrollY > 30);
    });


    // MOBILE MENU

    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {
      navLinks.classList.toggle("open");

      menuToggle.textContent =
        navLinks.classList.contains("open") ? "×" : "☰";
    });

    document.querySelectorAll(".nav-links a").forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        menuToggle.textContent = "☰";
      });
    });


    // TYPING ANIMATION

    const typingText = document.getElementById("typingText");

    const phrases = [
      "Building intelligent systems.",
      "Turning data into insights.",
      "Developing computer vision solutions.",
      "Solving real-world problems with AI."
    ];

    let phraseIndex = 0;
    let characterIndex = 0;
    let deleting = false;

    function typeEffect() {
      const currentPhrase = phrases[phraseIndex];

      if (deleting) {
        characterIndex--;
      } else {
        characterIndex++;
      }

      typingText.textContent =
        currentPhrase.substring(0, characterIndex);

      let delay = deleting ? 35 : 65;

      if (!deleting && characterIndex === currentPhrase.length) {
        deleting = true;
        delay = 1500;
      } else if (deleting && characterIndex === 0) {
        deleting = false;
        phraseIndex = (phraseIndex + 1) % phrases.length;
        delay = 400;
      }

      setTimeout(typeEffect, delay);
    }

    typeEffect();


    // SCROLL REVEAL

    const revealObserver = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            revealObserver.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.12 }
    );

    document.querySelectorAll(".reveal").forEach(element => {
      revealObserver.observe(element);
    });


    // SCROLL PROGRESS BAR

    const progressBar = document.getElementById("progressBar");

    window.addEventListener("scroll", () => {
      const scrollable =
        document.documentElement.scrollHeight - window.innerHeight;

      const progress = scrollable > 0
        ? (window.scrollY / scrollable) * 100
        : 0;

      progressBar.style.width = progress + "%";
    });


    // BACKGROUND PARTICLES

    const canvas = document.getElementById("particles");
    const ctx = canvas.getContext("2d");

    let particles = [];
    let canvasWidth = 0;
    let canvasHeight = 0;

    function resizeCanvas() {
      canvasWidth = canvas.width = window.innerWidth;
      canvasHeight = canvas.height = window.innerHeight;

      createParticles();
    }

    function createParticles() {
      particles = [];

      const count = Math.min(
        Math.floor((canvasWidth * canvasHeight) / 15000),
        90
      );

      for (let i = 0; i < count; i++) {
        particles.push({
          x: Math.random() * canvasWidth,
          y: Math.random() * canvasHeight,
          radius: Math.random() * 1.5 + 0.4,
          speedX: (Math.random() - 0.5) * 0.35,
          speedY: (Math.random() - 0.5) * 0.35,
          opacity: Math.random() * 0.5 + 0.15
        });
      }
    }

    function animateParticles() {
      ctx.clearRect(0, 0, canvasWidth, canvasHeight);

      particles.forEach(particle => {
        particle.x += particle.speedX;
        particle.y += particle.speedY;

        if (particle.x < 0 || particle.x > canvasWidth) {
          particle.speedX *= -1;
        }

        if (particle.y < 0 || particle.y > canvasHeight) {
          particle.speedY *= -1;
        }

        ctx.beginPath();

        ctx.arc(
          particle.x,
          particle.y,
          particle.radius,
          0,
          Math.PI * 2
        );

        ctx.fillStyle =
          `rgba(165,255,203,${particle.opacity})`;

        ctx.fill();
      });

      requestAnimationFrame(animateParticles);
    }

    resizeCanvas();
    animateParticles();

    window.addEventListener("resize", resizeCanvas);
  </script>

</body>
</html>
