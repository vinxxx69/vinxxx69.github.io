# vinxxx69.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <title>WebDesignPro – Bring Your Vision Online</title>
  <link href="https://fonts.googleapis.com/css?family=Montserrat:700,400&display=swap" rel="stylesheet">
  <style>
    :root {
      --main-color: #2563eb;
      --accent-color: #38bdf8;
      --bg-gradient: linear-gradient(135deg, #2563eb 40%, #38bdf8 100%);
      --bg-light: #f8fafc;
      --font-main: 'Montserrat', sans-serif;
      --shadow: 0 4px 40px rgba(40,60,100,0.08);
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      padding: 0;
      font-family: var(--font-main);
      background-color: var(--bg-light);
      color: #1e293b;
      min-height: 100vh;
      overflow-x: hidden;
    }

    header {
      background: var(--bg-gradient);
      color: #fff;
      padding: 60px 0 40px 0;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
      text-align: center;
    }
    header::before {
      content: '';
      position: absolute;
      z-index: 0;
      width: 120%;
      height: 170vh;
      top: -110vh;
      left: -10%;
      background: radial-gradient(circle at 70% -10%, #60a5fa 0%, transparent 70%);
      opacity: 0.16;
      pointer-events: none;
    }
    .logo {
      font-weight: 700;
      font-size: 2.2em;
      letter-spacing: 2px;
      display: block;
      text-shadow: 0 4px 16px rgba(0,0,0,0.06);
      margin-bottom: 20px;
      z-index: 1;
    }
    .hero-title {
      font-size: 2.9em;
      font-weight: 700;
      margin: 0 0 16px 0;
      letter-spacing: 0.7px;
      z-index: 1;
      position: relative;
      line-height: 1.15;
      transition: letter-spacing 0.3s;
    }
    .hero-desc {
      font-size: 1.28em;
      margin-bottom: 32px;
      font-weight: 400;
      color: #e0e7ef;
      z-index: 1;
    }
    .cta-btn {
      padding: 14px 38px;
      background: #fff;
      color: var(--main-color);
      border: none;
      border-radius: 28px;
      font-size: 1.2em;
      font-weight: 700;
      box-shadow: 0 2px 16px rgba(30,41,59,0.06);
      transition: background 0.22s, color 0.22s, transform 0.16s;
      cursor: pointer;
      margin-top: 5px;
      letter-spacing: 1px;
      z-index: 1;
      position: relative;
    }
    .cta-btn:hover {
      background: var(--accent-color);
      color: #fff;
      transform: translateY(-2px) scale(1.045);
    }

    main {
      max-width: 1380px;
      margin: 0 auto;
      padding: 48px 25px 24px 25px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
      gap: 36px;
      width: 100%;
      margin: 0 0 28px 0;
    }
    .feature-card {
      background: #fff;
      border-radius: 18px;
      box-shadow: var(--shadow);
      padding: 38px 28px 30px 28px;
      text-align: left;
      transition: transform 0.14s, box-shadow 0.14s;
      position: relative;
      z-index: 1;
    }
    .feature-card:hover {
      transform: translateY(-8px) scale(1.03);
      box-shadow: 0 8px 40px rgba(40,80,160,0.12);
    }
    .feature-icon {
      font-size: 2.3em;
      color: var(--main-color);
      margin-bottom: 14px;
    }
    .feature-title {
      font-size: 1.22em;
      font-weight: 700;
      margin-bottom: 10px;
    }
    .feature-desc {
      color: #475569;
      font-size: 1em;
      line-height: 1.4;
    }
    .portfolio {
      margin: 42px 0 0 0;
      width: 100%;
      max-width: 1060px;
      text-align: center;
    }
    .portfolio-title {
      font-size: 2em;
      font-weight: 700;
      margin-bottom: 14px;
      color: var(--main-color);
    }
    .portfolio-items {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(230px,1fr));
      gap: 24px;
      margin-top: 16px;
    }
    .portfolio-item {
      background: #f3f5f9;
      border-radius: 13px;
      box-shadow: 0 2px 20px rgba(56,143,217,0.06);
      padding: 16px 14px 14px 14px;
      text-align: left;
      transition: box-shadow 0.12s, transform 0.11s;
      border: 1px solid #e5e7ef;
      position: relative;
    }
    .portfolio-item:hover {
      box-shadow: 0 6px 20px rgba(42,108,194,0.09);
      transform: translateY(-4px) scale(1.03);
    }
    .portfolio-thumb {
      width: 100%;
      height: 120px;
      background: #bae6fd;
      border-radius: 8px;
      object-fit: cover;
      margin-bottom: 12px;
      display: block;
    }
    .portfolio-name {
      font-size: 1.09em;
      font-weight: 700;
      margin-bottom: 3px;
    }
    .portfolio-desc {
      font-size: 0.97em;
      color: #64748b;
      margin-bottom: 0;
    }

    footer {
      padding: 20px 0 15px 0;
      color: #475569;
      background: #e9eff7;
      text-align: center;
      font-size: 1em;
      margin-top: 48px;
      box-shadow: 0 -2px 14px rgba(38,80,120,0.03);
    }

    /* Modal styles */
    .modal {
      display: none;
      position: fixed;
      z-index: 10000;
      left: 0;
      top: 0;
      width: 100vw;
      height: 100vh;
      overflow: auto;
      background: rgba(16,28,46,0.17);
      justify-content: center;
      align-items: center;
      transition: opacity 0.18s;
    }
    .modal.open { display: flex; }
    .modal-content {
      background: #fff;
      color: #1e293b;
      padding: 32px 30px 26px 30px;
      border-radius: 18px;
      box-shadow: var(--shadow);
      min-width: 300px;
      max-width: 95vw;
      position: relative;
      animation: modalPop 0.3s;
    }
    @keyframes modalPop {
      0% { transform: scale(0.82) translateY(20px); opacity: 0; }
      100% { transform: scale(1) translateY(0px); opacity: 1; }
    }
    .close-btn {
      position: absolute;
      right: 18px;
      top: 16px;
      border: none;
      background: none;
      font-size: 1.35em;
      color: #64748b;
      cursor: pointer;
      font-weight: 700;
      transition: color 0.15s;
    }
    .close-btn:hover { color: #2563eb; }
    .modal h2 {
      margin: 0 0 16px 0;
      font-size: 1.45em;
      font-weight: 700;
      color: var(--main-color);
    }
    .modal-form label {
      display: block;
      margin-bottom: 6px;
      font-size: 1.03em;
    }
    .modal-form input, .modal-form textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 13px;
      border: 1px solid #cdd6e5;
      border-radius: 7px;
      font-size: 1em;
      font-family: var(--font-main);
      resize: none;
    }
    .modal-form textarea {
      min-height: 68px;
      max-height: 160px;
    }
    .modal-form button[type=submit] {
      background: var(--main-color);
      color: #fff;
      font-weight: bold;
      padding: 10px 24px;
      border: none;
      border-radius: 8px;
      font-size: 1.1em;
      transition: background 0.17s;
      cursor: pointer;
    }
    .modal-form button[type=submit]:hover {
      background: var(--accent-color);
    }

    @media (max-width: 900px) {
      .features { grid-template-columns: 1fr; }
      main { padding: 32px 7vw 10px 7vw;}
    }
    @media (max-width: 550px) {
      header { padding: 30px 0 16px 0;}
      .logo { font-size: 1.5em;}
      .hero-title { font-size: 1.5em;}
      main { padding: 20px 2vw 6px 2vw;}
      .portfolio-title { font-size: 1.15em;}
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">VhaveshDesigns</div>
    <h1 class="hero-title" id="hero-title">Bring Your Vision Online with <span style="color:#38bdf8">Stunning Websites</span></h1>
    <p class="hero-desc">
      We help you <b>design, build, and launch professional websites</b> tailored to your needs.<br>
      Trusted by startups, agencies, and entrepreneurs.
    </p>
    <button class="cta-btn" id="open-modal-btn">Contact Us</button>
  </header>

  <main>
    <section class="features">
      <div class="feature-card">
        <div class="feature-icon">🎨</div>
        <div class="feature-title">Custom Designs</div>
        <div class="feature-desc">
          Unique, modern, and responsive layouts tailored to <b>your brand and audience</b>.
        </div>
      </div>
      <div class="feature-card">
        <div class="feature-icon">⚡</div>
        <div class="feature-title">Lightning Fast</div>
        <div class="feature-desc">
          Optimized sites for performance, speed, and <b>mobile experience</b> across all devices.
        </div>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🚀</div>
        <div class="feature-title">Easy Launch</div>
        <div class="feature-desc">
          We handle everything – design, development, and launch. <b>Focus on your business!</b>
        </div>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🤝</div>
        <div class="feature-title">Personal Support</div>
        <div class="feature-desc">
          Dedicated expert guidance, <b>transparent</b> communication, and after-launch care.
        </div>
      </div>
    </section>

    <section class="portfolio">
      <div class="portfolio-title">Featured Projects</div>
      <div class="portfolio-items">
        <div class="portfolio-item">
          <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80" alt="Business site" class="portfolio-thumb">
          <div class="portfolio-name">Business Corp</div>
          <div class="portfolio-desc">Clean & elegant corporate service website.</div>
        </div>
        <div class="portfolio-item">
          <img src="https://images.unsplash.com/photo-1461749280684-dccba630e2f6?auto=format&fit=crop&w=400&q=80" alt="Portfolio site" class="portfolio-thumb">
          <div class="portfolio-name">Alex Portfolio</div>
          <div class="portfolio-desc">Vibrant personal portfolio for a freelancer.</div>
        </div>
        <div class="portfolio-item">
          <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80" alt="Startup site" class="portfolio-thumb">
          <div class="portfolio-name">StartUp Landing</div>
          <div class="portfolio-desc">Dynamic landing page for a SaaS startup.</div>
        </div>
        <div class="portfolio-item">
          <img src="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80" alt="E-commerce site" class="portfolio-thumb">
          <div class="portfolio-name">ShopEasy</div>
          <div class="portfolio-desc">Modern, clean e-commerce with shopping cart.</div>
        </div>
      </div>
    </section>
  </main>

  <!-- Modal for contact -->
  <div class="modal" id="contact-modal">
    <div class="modal-content">
      <button class="close-btn" id="close-modal-btn">&times;</button>
      <h2>Contact Us</h2>
      <form class="modal-form" id="contact-form">
        <label for="name">Name</label>
        <input required type="text" id="name" name="name" placeholder="Your Name">
        <label for="email">Email</label>
        <input required type="email" id="email" name="email" placeholder="your@email.com">
        <label for="message">Message</label>
        <textarea required id="message" name="message" placeholder="Tell us about your project..."></textarea>
        <button type="submit">Send Message</button>
      </form>
      <div id="success-msg" style="display:none;margin-top:12px;color:var(--main-color);font-weight:600;font-size:1.07em;">
        Thank you! We'll get back to you soon.
      </div>
    </div>
  </div>

  <footer>
    &copy; <span id="year"></span> VhaveshDesigns -- Crafted with passion.
  </footer>

  <script>
    // Modal Script
    const modal = document.getElementById('contact-modal');
    const openBtn = document.getElementById('open-modal-btn');
    const closeBtn = document.getElementById('close-modal-btn');
    openBtn.onclick = () => modal.classList.add('open');
    closeBtn.onclick = () => modal.classList.remove('open');
    window.onclick = (e) => { if (e.target==modal) modal.classList.remove('open'); }

    // Contact form handler (simulate send)
    document.getElementById('contact-form').addEventListener('submit', function(e){
      e.preventDefault();
      this.style.display = 'none';
      document.getElementById('success-msg').style.display = 'block';
      setTimeout(()=>{
        modal.classList.remove('open');
        this.style.display = '';
        document.getElementById('success-msg').style.display = 'none';
        this.reset();
      }, 2100);
    });

    // Animate headline on hover
    const heroTitle = document.getElementById('hero-title');
    heroTitle.addEventListener('mouseenter', () => {
      heroTitle.style.letterSpacing = "2px";
    });
    heroTitle.addEventListener('mouseleave', () => {
      heroTitle.style.letterSpacing = "0.7px";
    });

    // Set current year footer
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
