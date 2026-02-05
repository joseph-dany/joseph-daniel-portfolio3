  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Joseph Daniel | Data Analyst</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Inter', sans-serif;
      color: #e5e7eb;
      background: radial-gradient(ellipse at bottom, #0f172a 0%, #020617 100%);
      line-height: 1.6;
      overflow-x: hidden;
      cursor: none;
    }
    }
    }
    a { text-decoration: none; color: inherit; }

    /* Layout */
    header, section { padding: 100px 12%; }

    /* Navbar */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(255,255,255,0.9);
      backdrop-filter: blur(8px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 12%;
      z-index: 1000;
      border-bottom: 1px solid #e5e7eb;
    }
    nav .links a {
      margin-right: 24px;
      font-weight: 500;
      color: #374151;
    }
    nav .links a:hover { color: #2563eb; }

    /* Hero */
    header {
      min-height: 100vh;
      display: flex;
      align-items: center;
    }
    .hero {
      max-width: 720px;
    }
    .hero h1 {
      position: relative;
      font-size: 3.8rem;
      font-weight: 800;
      margin-bottom: 16px;
      background: linear-gradient(90deg, #60a5fa, #818cf8, #38bdf8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 0 18px rgba(56,189,248,0.25);
      animation: neonPulse 6s ease-in-out infinite;
      transition: transform 0.4s ease, text-shadow 0.4s ease;
    }

    .hero h1::before {
      content: "";
      position: absolute;
      inset: -40px;
      background: url('https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?auto=format&fit=crop&w=1200&q=80');
      background-size: cover;
      background-position: center;
      filter: blur(25px) saturate(140%);
      opacity: 0.55;
      z-index: -1;
      border-radius: 20px;
    }

    .hero h1:hover {
      transform: scale(1.12);
      text-shadow:
        0 0 40px rgba(56,189,248,0.8),
        0 0 80px rgba(129,140,248,0.9),
        0 0 120px rgba(34,211,238,0.9);
    }
    .hero p {
      font-size: 1.25rem;
      color: #4b5563;
      margin-bottom: 32px;
    }
    .btn {
      display: inline-block;
      padding: 12px 28px;
      border-radius: 8px;
      font-weight: 500;
      background: #2563eb;
      color: #ffffff;
      margin-right: 12px;
    }
    .btn.secondary {
      background: #f3f4f6;
      color: #111827;
    }

    /* Sections */
    h2 {
      font-size: 2.2rem;
      margin-bottom: 32px;
    }
    .card {
      background: rgba(15,23,42,0.7);
      backdrop-filter: blur(14px);
      padding: 32px;
      border-radius: 14px;
      margin-bottom: 24px;
      border: 1px solid rgba(99,102,241,0.15);
      transition: transform 0.4s ease, box-shadow 0.4s ease, border 0.4s ease;
    }
    .card:hover {
      transform: translateY(-6px) scale(1.01);
      box-shadow: 0 0 40px rgba(56,189,248,0.35);
      border: 1px solid rgba(56,189,248,0.6);
    }

    /* Projects */
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 24px;
    }
    .project h3 { margin-bottom: 8px; color: #ffffff; }
    .project p { color: #e5e7eb; }
    .project span { color: #93c5fd; }
    .project span {
      display: inline-block;
      margin-top: 12px;
      color: #2563eb;
      font-weight: 500;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 40px 12%;
      border-top: 1px solid #1f2933;
      color: #9ca3af;
    }

    /* Star background */
    .stars, .stars2, .stars3 {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-repeat: repeat;
      pointer-events: none;
      z-index: -1;
    }

    .stars {
      background-image: radial-gradient(2px 2px at 20px 30px, #fff, transparent),
        radial-gradient(2px 2px at 40px 70px, #fff, transparent),
        radial-gradient(1px 1px at 90px 40px, #fff, transparent);
      background-size: 200px 200px;
      animation: starMove 120s linear infinite;
    }

    .stars2 {
      background-image: radial-gradient(1px 1px at 10px 10px, #c7d2fe, transparent),
        radial-gradient(1px 1px at 50px 80px, #c7d2fe, transparent);
      background-size: 300px 300px;
      animation: starMove 200s linear infinite;
      opacity: 0.6;
    }

    .stars3 {
      background-image: radial-gradient(1px 1px at 60px 20px, #e0e7ff, transparent);
      background-size: 400px 400px;
      animation: starMove 300s linear infinite;
      opacity: 0.4;
    }

    @keyframes neonPulse {
      0% { filter: drop-shadow(0 0 10px rgba(56,189,248,0.4)); }
      50% { filter: drop-shadow(0 0 25px rgba(129,140,248,0.7)); }
      100% { filter: drop-shadow(0 0 10px rgba(56,189,248,0.4)); }
    }

    @keyframes starMove {
      from { transform: translateY(0); }
      to { transform: translateY(-2000px); }
    }

    /* Asteroid animation */
    .asteroid {
      position: fixed;
      top: -100px;
      left: -100px;
      width: 120px;
      height: 2px;
      background: linear-gradient(90deg, rgba(56,189,248,0), rgba(56,189,248,0.9), rgba(56,189,248,0));
      opacity: 0.8;
      transform: rotate(45deg);
      animation: asteroidMove 8s linear infinite;
      pointer-events: none;
      z-index: -1;
    }

    @keyframes asteroidMove {
      0% { transform: translate(-200px, -200px) rotate(45deg); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translate(220vw, 220vh) rotate(45deg); opacity: 0; }
    }

    /* Scroll reveal animation */
    .reveal {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }
    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }
      to { transform: translateY(-2000px); }
    }

    /* Responsive */
    @media (max-width: 768px) {
      header, section { padding: 80px 8%; }
      .hero h1 { font-size: 2.6rem; }
    }
  </style>
</head>
<body>

<!-- Animated star background -->
<div class="stars"></div>
<div class="stars2"></div>
<div class="stars3"></div>
<div class="asteroid"></div>
<div class="asteroid" style="animation-delay:3s;"></div>
<div class="asteroid" style="animation-delay:6s;"></div>

<!-- Animated star background -->
<div class="stars"></div>
<div class="stars2"></div>
<div class="stars3"></div>

<nav>
  <strong>Joseph Daniel</strong>
  <div class="links">
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#experience">Experience</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<header>
  <div class="hero">
    <h1>Hello, I’m Joseph Daniel</h1>
    <p>Data Analyst & Python Developer</p>
    <a href="#contact" class="btn">Hire Me</a>
    <a href="resume.pdf" class="btn secondary" download>Download Resume</a>
  </div>
</header>

<section id="about" class="reveal">
  <h2>About Me</h2>
  <div class="card">
    <p>
      I’m Joseph Daniel, a Data Analyst and Python Developer with a background in civil engineering, bringing strong analytical thinking and problem-solving skills into data-driven work. I specialize in Python, SQL, Excel, and Power BI to clean, analyze, and visualize data, turning complex datasets into clear insights and impactful dashboards. I’m passionate about continuous learning and aim to contribute to data-driven teams by delivering accurate analysis and meaningful business value.
    </p>
  </div>
</section>

<section id="projects" class="reveal">
  <h2>Projects</h2>
  <div class="projects">
    <a class="card project" href="https://github.com/joseph-dany/businfoo.py" target="_blank">
      <h3>Buss Info</h3>
      <p>Python-based project for extracting and analyzing bus-related information.</p>
      <span>View on GitHub →</span>
    </a>
    <a class="card project" href="https://github.com/joseph-dany/blood-donation" target="_blank">
      <h3>Blood Donation</h3>
      <p>Web-based system to manage blood donors and requests.</p>
      <span>View on GitHub →</span>
    </a>
    <a class="card project" href="https://github.com/rakeshreddy03/UID" target="_blank">
      <h3>Online Game Store</h3>
      <p>UI platform for browsing and purchasing digital games.</p>
      <span>View on GitHub →</span>
    </a>
    <div class="card project">
      <h3>Data Analytic Dashboards</h3>
      <p>Power BI and Excel dashboards for business insights.</p>
    </div>
  </div>
</section>

<section id="experience" class="reveal">
  <h2>Experience</h2>
  <div class="card">
    <h3>Data Analyst – Coding Ninjas</h3>
    <p><strong>01/2025 – 03/2025</strong> | Hyderabad, India</p>
    <ul style="margin-top:16px; padding-left:18px;">
      <li>120+ hours of intensive training in Python, SQL, Power BI, and Advanced Excel.</li>
      <li>Executed 2 end-to-end projects translating business needs into insights.</li>
      <li>Built 5+ dashboards using Excel & Power BI.</li>
      <li>Improved data analysis efficiency by 25%.</li>
    </ul>
  </div>
</section>

<section id="contact" class="reveal">
  <h2>Contact</h2>
  <div class="card">
    <form>
      <input type="text" placeholder="Your Name" required style="width:100%;padding:12px;margin-bottom:12px;">
      <input type="email" placeholder="Your Email" required style="width:100%;padding:12px;margin-bottom:12px;">
      <textarea placeholder="Your Message" required style="width:100%;padding:12px;height:120px;"></textarea>
      <button class="btn" type="submit" style="margin-top:16px;">Send Message</button>
    </form>
  </div>
</section>

<footer>
  © 2026 Joseph Daniel
</footer>


<!-- Futuristic Cursor -->
<div class="cursor"></div>
<div class="cursor-ring"></div>

<script>
  const cursor = document.querySelector('.cursor');
  const ring = document.querySelector('.cursor-ring');

  document.addEventListener('mousemove', e => {
    cursor.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
    ring.style.transform = `translate(${e.clientX}px, ${e.clientY}px)`;
  });

  document.querySelectorAll('a, button, .hero h1').forEach(el => {
    el.addEventListener('mouseenter', () => ring.classList.add('active'));
    el.addEventListener('mouseleave', () => ring.classList.remove('active'));
  });

  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  window.addEventListener('scroll', () => {
    reveals.forEach(section => {
      const top = section.getBoundingClientRect().top;
      if (top < window.innerHeight - 100) {
        section.classList.add('active');
      }
    });
  });
</script>

<style>
  .cursor {
    position: fixed;
    width: 6px;
    height: 6px;
    background: #38bdf8;
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
  }
  .cursor-ring {
    position: fixed;
    width: 36px;
    height: 36px;
    border: 2px solid rgba(56,189,248,0.6);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    transition: transform 0.15s ease, opacity 0.2s ease;
  }
  .cursor-ring.active {
    transform: scale(1.8);
    opacity: 0.4;
  }
</style>
</body>
</html>
