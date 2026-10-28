
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#ffffff">
<meta name="description" content="Krish Carpenter — Photographer, visual storyteller and creative collaborator.">
<title>Krish Carpenter — Photography</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #fff;
  --text: #171717;
  --muted: #777;
  --line: #e8e8e8;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--bg);
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
  overflow-x: hidden;
}
a { color: inherit; text-decoration: none; }
img { display: block; width: 100%; }
.wrap { width: 90%; max-width: 1200px; margin: auto; }

::selection { background: #171717; color: #fff; }

header {
  border-bottom: 1px solid var(--line);
  background: rgba(255,255,255,.94);
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(12px);
}
nav {
  min-height: 76px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}
.logo { font-size: 13px; font-weight: 700; letter-spacing: 2px; }
.logo span { font-weight: 400; }
.nav-links { display: flex; gap: 28px; }
.nav-links a {
  font-size: 10px;
  letter-spacing: 1.5px;
  transition: opacity .3s;
}
.nav-links a:hover { opacity: .45; }
.menu-btn {
  display: none;
  border: 1px solid #ddd;
  padding: 9px 12px;
  background: white;
  cursor: pointer;
}

.hero {
  padding: 85px 0 75px;
  display: grid;
  grid-template-columns: 1fr .9fr;
  gap: 65px;
  align-items: center;
}
.eyebrow {
  font-size: 10px;
  letter-spacing: 2.5px;
  color: var(--muted);
  text-transform: uppercase;
}
h1, h2 {
  font-family: 'Playfair Display', serif;
  font-weight: 400;
}
h1 {
  font-size: clamp(48px, 7vw, 85px);
  line-height: 1.08;
  letter-spacing: -2px;
  margin: 22px 0;
}
h1 em, h2 em { font-weight: 400; }
p { color: var(--muted); font-size: 13px; line-height: 1.9; }
.intro p { max-width: 410px; }
.underline-link {
  display: inline-block;
  margin-top: 25px;
  padding-bottom: 6px;
  border-bottom: 1px solid #222;
  font-size: 10px;
  letter-spacing: 1.5px;
  transition: opacity .3s;
}
.underline-link:hover { opacity: .5; }

.hero-image { position: relative; overflow: hidden; }
.hero-image img {
  height: 500px;
  object-fit: cover;
  object-position: center 25%;
  transition: transform .9s cubic-bezier(.2,.7,.2,1);
}
.hero-image:hover img { transform: scale(1.025); }
.image-index {
  position: absolute;
  bottom: 12px;
  right: 12px;
  padding: 8px 10px;
  background: rgba(255,255,255,.9);
  font-size: 9px;
  letter-spacing: 1px;
}

.section {
  padding: 70px 0;
  border-top: 1px solid var(--line);
  scroll-margin-top: 75px;
}
.section-head {
  display: flex;
  align-items: end;
  justify-content: space-between;
  gap: 25px;
  margin-bottom: 32px;
}
h2 { font-size: clamp(35px, 5vw, 53px); line-height: 1.15; margin-top: 12px; }
.section-head p { max-width: 300px; font-size: 12px; }

.gallery {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 42px 24px;
}
.card { min-width: 0; }
.photo {
  overflow: hidden;
  background: #f1f1f1;
}
.photo img {
  width: 100%;
  aspect-ratio: 4 / 5;
  object-fit: cover;
  transition: transform .8s cubic-bezier(.2,.7,.2,1);
}
.card:hover .photo img { transform: scale(1.035); }
.photo img.bw {
  filter: grayscale(100%);
  -webkit-filter: grayscale(100%);
}
.caption {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  padding-top: 14px;
  transition: transform .3s;
}
.card:hover .caption { transform: translateX(4px); }
.caption h3 { font-size: 13px; font-weight: 500; }
.caption p { font-size: 11px; margin-top: 3px; }
.number { font-size: 10px; color: #888; }

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 70px;
}
.about-copy p + p { margin-top: 14px; }
.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 23px;
}
.skills span {
  border: 1px solid #ddd;
  padding: 9px 11px;
  font-size: 10px;
  color: #555;
}

.contact { text-align: center; padding: 90px 0; }
.contact h2 { margin: 17px 0; }
.contact p { max-width: 430px; margin: 0 auto; }
.contact-links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
  margin-top: 27px;
}
.contact-links a {
  font-size: 10px;
  letter-spacing: 1.5px;
  border-bottom: 1px solid #222;
  padding-bottom: 6px;
  transition: opacity .3s;
}
.contact-links a:hover { opacity: .5; }

footer { border-top: 1px solid var(--line); padding: 23px 0; }
.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 15px;
  flex-wrap: wrap;
  font-size: 10px;
  color: #777;
}

/* Scroll reveal animation */
.reveal {
  opacity: 0;
  transform: translateY(22px);
  transition: opacity .7s ease, transform .7s ease;
}
.reveal.visible { opacity: 1; transform: translateY(0); }

@media (max-width: 700px) {
  nav { min-height: 70px; flex-wrap: wrap; padding: 15px 0; }
  .menu-btn { display: block; }
  .nav-links {
    display: none;
    width: 100%;
    padding: 15px 0 8px;
    flex-direction: column;
    gap: 18px;
  }
  .nav-links.open { display: flex; }
  .hero { grid-template-columns: 1fr; gap: 32px; padding: 48px 0; }
  h1 { font-size: 59px; }
  .hero-image img { height: 430px; }
  .section { padding: 48px 0; }
  .section-head { align-items: flex-start; flex-direction: column; }
  .gallery { gap: 28px 15px; }
  .about-grid { grid-template-columns: 1fr; gap: 25px; }
  .contact { padding: 65px 0; }
}
@media (max-width: 430px) {
  .gallery { grid-template-columns: 1fr; }
  .hero-image img { height: 410px; }
  h1 { font-size: 52px; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation: none !important;
    transition: none !important;
    scroll-behavior: auto !important;
  }
  .reveal { opacity: 1; transform: none; }
}
</style>
</head>

<body>
<header>
  <nav class="wrap">
    <a class="logo" href="#home">KRISH CARPENTER<span>.</span></a>
    <button class="menu-btn" id="menuBtn" aria-expanded="false"
      aria-controls="navLinks">MENU</button>
    <div class="nav-links" id="navLinks">
      <a href="#home">HOME</a>
      <a href="#work">WORK</a>
      <a href="#about">ABOUT</a>
      <a href="#contact">CONTACT</a>
    </div>
  </nav>
</header>

<main class="wrap">
  <section class="hero" id="home">
    <div class="intro reveal">
      <span class="eyebrow">Photographer · Visual Storyteller</span>
      <h1>Stories<br>in every <em>frame.</em></h1>
      <p>
        I'm Krish Carpenter, a photographer passionate about people,
        weddings and genuine moments. Building my craft through
        thoughtful images and visual storytelling.
      </p>
      <a class="underline-link" href="#work">VIEW SELECTED WORK ↗</a>
    </div>
    <div class="hero-image reveal">
      <img src="images/krish-portrait.webp"
        alt="Portrait from Krish Carpenter's portfolio">
      <span class="image-index">01 — PORTRAIT</span>
    </div>
  </section>

  <section class="section" id="work">
    <div class="section-head reveal">
      <div>
        <span class="eyebrow">A selection of photographs</span>
        <h2>Selected Work</h2>
      </div>
      <p>Real moments. Honest expressions. Timeless frames.</p>
    </div>

    <div class="gallery">
      <article class="card reveal">
        <div class="photo">
          <img src="images/wedding-couple.webp"
            alt="Wedding photography in colour" loading="lazy">
        </div>
        <div class="caption">
          <div><h3>Wedding Stories</h3><p>Wedding Photography · Colour</p></div>
          <span class="number">01</span>
        </div>
      </article>

      <article class="card reveal">
        <div class="photo">
          <img class="bw" src="images/wedding-couple.webp"
            alt="Black and white wedding photograph" loading="lazy">
        </div>
        <div class="caption">
          <div><h3>Quiet Moments</h3><p>Wedding Photography · Monochrome</p></div>
          <span class="number">02</span>
        </div>
      </article>

      <article class="card reveal">
        <div class="photo">
          <img src="images/krish-portrait.webp"
            alt="Portrait photograph in colour" loading="lazy">
        </div>
        <div class="caption">
          <div><h3>Portraits</h3><p>People & Expressions · Colour</p></div>
          <span class="number">03</span>
        </div>
      </article>

      <article class="card reveal">
        <div class="photo">
          <img class="bw" src="images/krish-portrait.webp"
            alt="Black and white portrait photograph" loading="lazy">
        </div>
        <div class="caption">
          <div><h3>Monochrome</h3><p>Light & Contrast · Black & White</p></div>
          <span class="number">04</span>
        </div>
      </article>
    </div>
  </section>

  <section class="section" id="about">
    <div class="about-grid">
      <div class="reveal">
        <span class="eyebrow">A little about me</span>
        <h2>Behind the<br><em>camera.</em></h2>
      </div>
      <div class="about-copy reveal">
        <p>
          I'm developing my craft in photography, wedding coverage and
          visual storytelling. I value thoughtful compositions, natural
          expressions and the details that make each frame meaningful.
        </p>
        <p>
          I'm open to photography assisting, second-shooter assignments
          and creative collaborations with experienced photographers
          and teams in Mumbai and beyond.
        </p>
        <div class="skills">
          <span>Wedding Photography</span>
          <span>Portraits</span>
          <span>Video Editing</span>
          <span>Colour Grading</span>
          <span>Visual Storytelling</span>
        </div>
      </div>
    </div>
  </section>

  <section class="contact section" id="contact">
    <div class="reveal">
      <span class="eyebrow">Work & collaborations</span>
      <h2>Let's create something<br><em>worth remembering.</em></h2>
      <p>
        For photography assignments, assisting opportunities
        and creative collaborations.
      </p>
      <div class="contact-links">
        <a href="mailto:YOUR_EMAIL@example.com">EMAIL ↗</a>
        <a href="https://instagram.com/YOUR_INSTAGRAM"
           target="_blank" rel="noopener noreferrer">INSTAGRAM ↗</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap footer-inner">
    <span>KRISH CARPENTER</span>
    <span>PHOTOGRAPHY · VISUAL STORIES</span>
    <span>© <span id="year"></span></span>
  </div>
</footer>

<script>
const menuBtn = document.getElementById('menuBtn');
const navLinks = document.getElementById('navLinks');

menuBtn.addEventListener('click', () => {
  const isOpen = navLinks.classList.toggle('open');
  menuBtn.setAttribute('aria-expanded', String(isOpen));
});

navLinks.querySelectorAll('a').forEach(link => {
  link.addEventListener('click', () => {
    navLinks.classList.remove('open');
    menuBtn.setAttribute('aria-expanded', 'false');
  });
});

document.getElementById('year').textContent =
  new Date().getFullYear();

if ('IntersectionObserver' in window) {
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll('.reveal').forEach(item => {
    observer.observe(item);
  });
} else {
  document.querySelectorAll('.reveal').forEach(item => {
    item.classList.add('visible');
  });
}
</script>
</body>
</html>
