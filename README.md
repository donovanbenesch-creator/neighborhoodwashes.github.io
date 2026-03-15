# neighborhoodwashes.github.io
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Neighborhood Washes – Pressure Washing Services</title>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

```
:root {
  --navy: #0b1d35;
  --blue: #1560bd;
  --sky: #4fc3f7;
  --white: #000000;
  --gray: #000000;
  --accent: #000000;
}

html { scroll-behavior: smooth; }

body {
  background: var(--navy);
  color: var(--white);
  font-family: 'DM Sans', sans-serif;
  overflow-x: hidden;
}

/* ── HEADER ── */
header {
  position: fixed; top: 0; left: 0; width: 100%; z-index: 100;
  background: rgba(11,29,53,0.92);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(79,195,247,0.15);
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 6vw;
}
.logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.7rem;
  letter-spacing: 2px;
  color: var(--sky);
}
.logo span { color: var(--accent); }
nav a {
  color: #000000;
  text-decoration: none;
  margin-left: 28px;
  font-size: .9rem;
  font-weight: 600;
  transition: color .2s;
}
nav a:hover { color: var(--sky); }

/* ── HERO ── */
.hero {
  min-height: 100vh;
  display: flex; flex-direction: column;
  justify-content: center; align-items: flex-start;
  padding: 120px 8vw 80px;
  position: relative;
  overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse 60% 60% at 80% 40%, rgba(21,96,189,0.35) 0%, transparent 70%),
    radial-gradient(ellipse 40% 40% at 20% 80%, rgba(79,195,247,0.18) 0%, transparent 70%);
  pointer-events: none;
}
.water-drop {
  position: absolute; right: 6vw; top: 50%; transform: translateY(-50%);
  font-size: clamp(140px, 20vw, 280px);
  opacity: .06;
  user-select: none;
  animation: float 6s ease-in-out infinite;
}
@keyframes float {
  0%,100% { transform: translateY(-50%) translateY(0); }
  50%      { transform: translateY(-50%) translateY(-18px); }
}
.hero-tag {
  font-size: .8rem; font-weight: 600; letter-spacing: 3px;
  color: var(--sky); text-transform: uppercase;
  background: rgba(79,195,247,.1);
  border: 1px solid rgba(79,195,247,.3);
  padding: 6px 14px; border-radius: 40px;
  margin-bottom: 24px;
  animation: fadeUp .7s ease both;
}
.hero h1 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(3.5rem, 9vw, 8rem);
  line-height: .95;
  letter-spacing: 2px;
  animation: fadeUp .8s .1s ease both;
}
.hero h1 em {
  color: var(--sky); font-style: normal;
  display: block;
}
.hero p {
  max-width: 520px;
  color: var(--gray);
  font-size: 1.1rem;
  line-height: 1.7;
  margin-top: 24px;
  animation: fadeUp .8s .2s ease both;
}
.hero-cta {
  margin-top: 36px;
  display: flex; gap: 16px; flex-wrap: wrap;
  animation: fadeUp .8s .3s ease both;
}
.btn-primary {
  background: var(--sky);
  color: var(--navy);
  font-weight: 700; font-size: 1rem;
  padding: 14px 32px; border-radius: 8px;
  text-decoration: none;
  transition: transform .15s, box-shadow .15s;
  box-shadow: 0 4px 24px rgba(79,195,247,.35);
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 32px rgba(79,195,247,.5); }
.btn-secondary {
  border: 1px solid rgba(79,195,247,.4);
  color: var(--sky);
  font-weight: 600; font-size: 1rem;
  padding: 14px 32px; border-radius: 8px;
  text-decoration: none;
  transition: background .2s;
}
.btn-secondary:hover { background: rgba(79,195,247,.08); }

@keyframes fadeUp {
  from { opacity:0; transform: translateY(28px); }
  to   { opacity:1; transform: translateY(0); }
}

/* ── SECTION WRAPPER ── */
section { padding: 90px 8vw; }
.section-label {
  font-size: .78rem; font-weight: 600; letter-spacing: 3px;
  text-transform: uppercase; color: var(--sky);
  margin-bottom: 10px;
}
.section-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.2rem, 5vw, 4rem);
  letter-spacing: 1.5px;
  margin-bottom: 16px;
}
.divider {
  width: 48px; height: 3px;
  background: var(--sky);
  margin-bottom: 40px;
  border-radius: 2px;
}

/* ── STATS ── */
.stats {
  background: rgba(21,96,189,.12);
  border-top: 1px solid rgba(79,195,247,.1);
  border-bottom: 1px solid rgba(79,195,247,.1);
  padding: 50px 8vw;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 32px;
  text-align: center;
}
.stat-num {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3.4rem;
  color: var(--sky);
  letter-spacing: 2px;
  line-height: 1;
}
.stat-label { color: var(--gray); font-size: .9rem; margin-top: 6px; }

/* ── SERVICES ── */
.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 24px;
  margin-top: 20px;
}
.service-card {
  background: rgba(255,255,255,.04);
  border: 1px solid rgba(79,195,247,.12);
  border-radius: 16px;
  padding: 36px 28px;
  transition: transform .2s, border-color .2s;
}
.service-card:hover {
  transform: translateY(-4px);
  border-color: rgba(79,195,247,.35);
}
.service-icon { font-size: 2.4rem; margin-bottom: 16px; }
.service-card h3 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.5rem; letter-spacing: 1px;
  color: var(--white); margin-bottom: 10px;
}
.service-card p { color: var(--gray); line-height: 1.65; font-size: .95rem; }

/* ── PRICING ── */
.pricing-box {
  background: linear-gradient(135deg, rgba(21,96,189,.25), rgba(79,195,247,.08));
  border: 1px solid rgba(79,195,247,.25);
  border-radius: 20px;
  padding: 50px;
  max-width: 680px;
}
.price-big {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(4rem, 10vw, 7rem);
  color: var(--accent);
  letter-spacing: 2px;
  line-height: 1;
}
.price-sub { color: var(--sky); font-size: 1.2rem; font-weight: 600; margin-top: 4px; }
.price-note { color: var(--gray); margin-top: 20px; line-height: 1.7; font-size: .95rem; }
.price-note strong { color: var(--white); }

/* ── HOW IT WORKS ── */
.steps {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 32px;
  margin-top: 20px;
}
.step { position: relative; padding-left: 0; }
.step-num {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 4rem; color: rgba(79,195,247,0.45);
  line-height: 1;
}
.step h4 {
  font-size: 1rem; font-weight: 700;
  color: var(--white); margin: 4px 0 8px;
}
.step p { color: #000000; font-size: .95rem; line-height: 1.6; }

/* ── ABOUT ── */
.about-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}
.about-text p { color: var(--gray); line-height: 1.75; font-size: 1rem; margin-bottom: 16px; }
.about-text p strong { color: var(--white); }
.about-badge {
  display: inline-block;
  background: rgba(244,197,66,.12);
  border: 1px solid rgba(244,197,66,.35);
  color: var(--accent);
  font-weight: 600; font-size: .85rem;
  padding: 8px 18px; border-radius: 40px;
  margin-top: 8px;
}
.about-visual {
  background: rgba(21,96,189,.15);
  border: 1px solid rgba(79,195,247,.15);
  border-radius: 20px;
  padding: 40px;
  text-align: center;
}
.about-visual .emoji { font-size: 5rem; display: block; margin-bottom: 20px; }
.about-visual p { color: #000000; font-size: .95rem; line-height: 1.6; }
.about-visual strong { color: var(--sky); }

/* ── CTA / CONTACT ── */
.contact {
  background: linear-gradient(135deg, rgba(21,96,189,.3), rgba(11,29,53,0));
  border-top: 1px solid rgba(79,195,247,.12);
  text-align: center;
}
.contact .section-title { max-width: 600px; margin: 0 auto 8px; }
.contact > p { color: var(--gray); max-width: 520px; margin: 0 auto 40px; line-height: 1.7; }
.phone-display {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(2.5rem, 7vw, 5rem);
  color: var(--sky);
  letter-spacing: 3px;
  display: block;
  margin-bottom: 10px;
  text-decoration: none;
  transition: color .2s;
}
.phone-display:hover { color: var(--accent); }
.availability-badge {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(244,197,66,.1);
  border: 1px solid rgba(244,197,66,.3);
  color: var(--accent);
  font-weight: 600; font-size: .9rem;
  padding: 10px 22px; border-radius: 40px;
  margin-bottom: 40px;
}
.availability-badge::before { content: '📅'; }
.contact-note {
  margin-top: 28px;
  background: rgba(255,255,255,.04);
  border: 1px solid rgba(79,195,247,.1);
  border-radius: 14px;
  padding: 28px 36px;
  max-width: 560px;
  margin: 28px auto 0;
  text-align: left;
}
.contact-note h4 { color: var(--sky); font-size: .85rem; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 14px; }
.contact-note ul { list-style: none; }
.contact-note ul li {
  color: #000000; font-size: .95rem;
  padding: 6px 0; border-bottom: 1px solid rgba(255,255,255,.05);
  display: flex; align-items: center; gap: 10px;
}
.contact-note ul li:last-child { border-bottom: none; }
.contact-note ul li::before { content: '✓'; color: var(--sky); font-weight: 700; }

/* ── FOOTER ── */
footer {
  padding: 30px 8vw;
  border-top: 1px solid rgba(79,195,247,.08);
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 12px;
  color: #000000; font-size: .85rem;
}
footer .logo { font-size: 1.2rem; }

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  nav { display: none; }
  .about-inner { grid-template-columns: 1fr; }
  .pricing-box { padding: 32px 24px; }
  .contact-note { padding: 22px; }
}
```

  </style>
</head>
<body>

<!-- HEADER -->

<header>
  <div class="logo">Neighborhood<span>Washes</span></div>
  <nav>
    <a href="#services">Services</a>
    <a href="#pricing">Pricing</a>
    <a href="#how">How It Works</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- HERO -->

<section class="hero">
  <div class="water-drop">💧</div>
  <div class="hero-tag">Local &bull; Reliable &bull; Affordable</div>
  <h1>Your Driveway,<em>Spotless.</em></h1>
  <p>Professional pressure washing by your neighbors — making driveways shine across the community at an unbeatable price.</p>
  <div class="hero-cta">
    <a href="tel:7133920786" class="btn-primary">📞 Call Now</a>
    <a href="#how" class="btn-secondary">How It Works →</a>
  </div>
</section>

<!-- STATS -->

<div class="stats">
  <div>
    <div class="stat-num">$0.40</div>
    <div class="stat-label">Per Square Foot — Flat Rate</div>
  </div>
  <div>
    <div class="stat-num">~1HR</div>
    <div class="stat-label">Average Driveway Time</div>
  </div>
  <div>
    <div class="stat-num">2</div>
    <div class="stat-label">Dedicated Local Owners</div>
  </div>
  <div>
    <div class="stat-num">100%</div>
    <div class="stat-label">Neighborhood Pride</div>
  </div>
</div>

<!-- SERVICES -->

<section id="services">
  <div class="section-label">What We Do</div>
  <div class="section-title">Our Services</div>
  <div class="divider"></div>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-icon">🚗</div>
      <h3>Driveway Cleaning</h3>
      <p>Our specialty. We blast away dirt, oil stains, grime, and buildup to leave your driveway looking brand new. Most driveways take around an hour — sometimes more, sometimes less depending on size and condition.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🌿</div>
      <h3>Backyard Surfaces</h3>
      <p>We may be able to tackle your backyard depending on the surface type and layout. Give us a call and describe what you've got — we'll let you know if it's something we can handle.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">✨</div>
      <h3>Custom Quotes</h3>
      <p>Not sure about pricing or whether your job fits? Call us on the weekend and we'll talk through your address, square footage, and any special details to get you an accurate picture before we show up.</p>
    </div>
  </div>
</section>

<!-- PRICING -->

<section id="pricing" style="padding-top:0;">
  <div class="section-label">Transparent Pricing</div>
  <div class="section-title">Simple, Fair Rates</div>
  <div class="divider"></div>
  <div class="pricing-box">
    <div class="price-big">$0.40</div>
    <div class="price-sub">per square foot</div>
    <p class="price-note">
      <strong>No hidden fees. No surprises.</strong> The price is based purely on the square footage of the area we clean.<br><br>
      For example, a typical two-car driveway (~400 sq ft) would come out to around <strong>$160</strong>. We'll confirm exact pricing when you call — just have your address ready so we can give you a good estimate.
    </p>
  </div>
</section>

<!-- HOW IT WORKS -->

<section id="how" style="padding-top:0;">
  <div class="section-label">The Process</div>
  <div class="section-title">How It Works</div>
  <div class="divider"></div>
  <div class="steps">
    <div class="step">
      <div class="step-num">01</div>
      <h4>Call Us on the Weekend</h4>
      <p>Reach out Saturday or Sunday. We're available to chat about your job, pricing, and scheduling.</p>
    </div>
    <div class="step">
      <div class="step-num">02</div>
      <h4>Discuss the Details</h4>
      <p>Share your address, describe the area, and we'll talk through timing, square footage, and total cost.</p>
    </div>
    <div class="step">
      <div class="step-num">03</div>
      <h4>We Show Up & Get to Work</h4>
      <p>We arrive at the agreed time with everything needed. Most driveways are done in about an hour.</p>
    </div>
    <div class="step">
      <div class="step-num">04</div>
      <h4>Enjoy the Results</h4>
      <p>Step back and admire a clean, fresh driveway — without lifting a finger.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->

<section id="about">
  <div class="section-label">Who We Are</div>
  <div class="section-title">Meet the Owners</div>
  <div class="divider"></div>
  <div class="about-inner">
    <div class="about-text">
      <p>
        Neighborhood Washes was started by two 12-year-old entrepreneurs from right here in the community — <strong>Jacob Bucko</strong> and his business partner — who saw a need and decided to do something about it.
      </p>
      <p>
        We're not a big corporation. We're your actual neighbors, putting in real work to earn your trust and deliver results you can see. Every driveway we clean is a reflection of our reputation — and we take that seriously.
      </p>
      <p>
        We keep things simple: show up on time, do great work, charge a fair price. That's the Neighborhood Washes promise.
      </p>
      <span class="about-badge">🏡 Locally Owned &amp; Operated</span>
    </div>
    <div class="about-visual">
      <span class="emoji">🤝</span>
      <p>
        <strong>Two friends. One mission.</strong><br><br>
        We started this business because we believe hard work pays off — and we want to prove it one clean driveway at a time.
      </p>
    </div>
  </div>
</section>

<!-- CONTACT -->

<section id="contact" class="contact">
  <div class="section-label">Get In Touch</div>
  <div class="section-title">Ready to Book?</div>
  <div class="divider" style="margin:0 auto 20px;"></div>
  <p>Give us a call on the weekend and we'll get everything sorted — time, price, address, and any questions you have.</p>

  <div class="availability-badge">Calls accepted Saturdays &amp; Sundays only</div>

<a href="tel:7133920786" class="phone-display">713-392-0786</a>

  <div class="contact-note">
    <h4>What to have ready when you call</h4>
    <ul>
      <li>Your home address</li>
      <li>Description of the area to be cleaned (driveway, backyard, etc.)</li>
      <li>Preferred day and time</li>
      <li>Any questions about pricing or the process</li>
    </ul>
  </div>
</section>

<!-- FOOTER -->

<footer>
  <div class="logo">Neighborhood<span>Washes</span></div>
  <div>© 2025 Neighborhood Washes. All rights reserved.</div>
  <div>📞 <a href="tel:7133920786" style="color:var(--sky);text-decoration:none;">713-392-0786</a> &nbsp;|&nbsp; Weekends Only</div>
</footer>

</body>
</html>