# sakthi---portfolio
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Sakthi Krishnan – AI &amp; Data Science student</title>
<style>
  :root {
    --paper: #FFFFFF;
    --wash: #F3F7EA;
    --ink: #24351A;
    --muted: #66775A;
    --line: #DCE5CC;
    --matcha: #5E8A2B;
    --forest: #2F4A1C;
    --jade: #3F7A5A;
    --olive: #7A7F1E;
    --accent: var(--matcha);
    --black: #0A0A0A;
    --body: system-ui, -apple-system, "Segoe UI", "Helvetica Neue", Arial, sans-serif;
    --pad: clamp(1.25rem, 4vw, 3rem);
    color-scheme: light;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --paper: #17210F;
      --wash: #1E2B14;
      --ink: #F2F7E8;
      --muted: #A8B898;
      --line: #2F4020;
      --matcha: #A8CF6B;
      --forest: #E4EFCB;
      --jade: #7FD1A0;
      --olive: #D2D66B;
      --black: #F2F7E8;
      color-scheme: dark;
    }
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--paper);
    color: var(--ink);
    font-family: var(--body);
    line-height: 1.5;
    overflow-x: clip;
    -webkit-font-smoothing: antialiased;
  }
  ::selection { background: var(--matcha); color: var(--paper); }
  a { color: inherit; }
  a:focus-visible { outline: 2px solid var(--matcha); outline-offset: 4px; }

  .sr {
    position: absolute; width: 1px; height: 1px; overflow: hidden;
    clip: rect(0 0 0 0); white-space: nowrap;
  }

  .wrap { padding-inline: var(--pad); max-width: 1280px; margin-inline: auto; }

  /* Progress */
  .progress {
    position: fixed; inset: 0 0 auto 0; height: 3px; z-index: 20;
    background: var(--matcha);
    transform: scaleX(0); transform-origin: left;
  }

  /* Nav */
  .nav {
    position: fixed; inset: 0 0 auto 0; z-index: 10;
    background: color-mix(in srgb, var(--paper) 88%, transparent);
    backdrop-filter: blur(8px);
    -webkit-backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }
  .nav .wrap {
    display: flex; justify-content: space-between; align-items: center;
    height: 3.5rem; font-size: 0.9rem;
  }
  .nav nav { display: flex; gap: 1.25rem; }
  .nav a { text-decoration: none; }
  .nav nav a:hover { color: var(--matcha); text-decoration: underline; text-underline-offset: 4px; }

  /* Hero */
  .hero {
    min-height: 100svh;
    display: flex; flex-direction: column; justify-content: flex-end;
    padding-block: 6rem 3rem;
    overflow: hidden;
  }
  .hero h1 {
    font-size: clamp(2.8rem, 14.5vw, 12rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    line-height: 1;
  }
  .hero h1 > span { display: block; will-change: transform; }
  .hero h1 .l1 { color: var(--matcha); }
  .hero h1 .l2 { padding-left: 0.2em; color: var(--forest); }
  .hero .role {
    margin-top: 2.5rem;
    max-width: 34ch;
    font-size: clamp(1rem, 2vw, 1.25rem);
    font-weight: 700;
  }

  /* Section heading */
  .section-title {
    font-size: 1.05rem; font-weight: 700; color: var(--muted);
    padding-block: 5rem 1.5rem;
  }

  /* Projects */
  .project { border-top: 1px solid var(--line); padding-block: 1.5rem 3rem; }
  .project-head {
    display: flex; flex-wrap: wrap; justify-content: space-between;
    align-items: baseline; gap: 0.5rem 2rem; margin-bottom: 1.5rem;
  }
  .project h3 {
    font-size: clamp(1.8rem, 5.5vw, 3.5rem);
    font-weight: 800; letter-spacing: -0.02em; line-height: 1.1;
    color: var(--c);
  }
  .project p { color: var(--black); max-width: 40ch; font-weight: 700; }
  .thumb {
    position: relative; aspect-ratio: 16 / 9; overflow: hidden;
    clip-path: inset(0 100% 0 0);
    transition: clip-path 1.1s cubic-bezier(.7, 0, .2, 1);
  }
  .thumb.in { clip-path: inset(0 0 0 0); }
  .thumb i { position: absolute; display: block; }

  .t1 { background: #A8C26B; }
  .t1 i:nth-child(1) { width: 38%; aspect-ratio: 1; border-radius: 50%; background: #FFFFFF; right: 12%; top: 18%; }
  .t1 i:nth-child(2) { width: 100%; height: 22%; left: 0; bottom: 0; background: #2F4A1C; }

  .t2 { background: #2F4A1C; }
  .t2 i:nth-child(1) { width: 46%; height: 62%; left: 10%; top: 19%; background: #FFFFFF; }
  .t2 i:nth-child(2) { width: 22%; height: 62%; right: 12%; top: 19%; background: #C9DC9A; }

  .t3 { background: #E4EFCB; }
  .t3 i:nth-child(1) { width: 56%; height: 14%; left: 8%; top: 24%; background: #2F4A1C; }
  .t3 i:nth-child(2) { width: 36%; height: 14%; left: 8%; top: 46%; background: #5E8A2B; }
  .t3 i:nth-child(3) { width: 14%; aspect-ratio: 1; border-radius: 50%; right: 10%; bottom: 16%; background: #FFFFFF; }

  .t4 { background: #7FA24A; }
  .t4 i:nth-child(1) { width: 30%; aspect-ratio: 1; border-radius: 50%; left: 14%; top: 30%; background: #FFFFFF; }
  .t4 i:nth-child(2) { width: 30%; aspect-ratio: 1; left: 50%; top: 30%; background: #24351A; }

  /* About */
  .about { padding-block: 6rem 4rem; border-top: 1px solid var(--line); background: var(--wash); }
  .about-text {
    position: relative;
    font-size: clamp(1.4rem, 3.8vw, 2.6rem);
    line-height: 1.3; letter-spacing: -0.01em; font-weight: 800;
    max-width: 24em;
  }
  .about-text .w { opacity: 0.22; transition: opacity 0.25s linear; }
  .about-text .w.on { opacity: 1; }

  /* Contact */
  .contact { padding-block: 6rem 4rem; border-top: 1px solid var(--line); }
  .contact p { color: var(--muted); margin-bottom: 1rem; font-weight: 700; }
  .contact a.mail {
    color: var(--matcha);
    font-size: clamp(1.6rem, 6.2vw, 4.5rem);
    font-weight: 800; letter-spacing: -0.02em; text-decoration: none;
    background: linear-gradient(var(--forest), var(--forest)) 0 100% / 0% 3px no-repeat;
    transition: background-size 0.4s ease;
    overflow-wrap: anywhere;
  }
  .contact a.mail:hover, .contact a.mail:focus-visible { background-size: 100% 3px; }
  footer { padding-block: 2rem 3rem; color: var(--muted); font-size: 0.9rem; font-weight: 700; }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    .thumb { clip-path: none; transition: none; }
    .about-text .w { opacity: 1; transition: none; }
  }
</style>
</head>
<body>
  <div class="progress" aria-hidden="true"></div>

  <div class="nav">
    <div class="wrap">
      <a href="#top">Sakthi Krishnan</a>
      <nav aria-label="Primary">
        <a href="#work">Work</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </div>

  <main id="top">
    <header class="hero wrap">
      <h1 aria-label="Sakthi Krishnan">
        <span class="l1" aria-hidden="true">Sakthi</span>
        <span class="l2" aria-hidden="true">Krishnan</span>
      </h1>
      <p class="role">First-year AI &amp; Data Science student. I'm learning to build things with Python, data and machine learning.</p>
    </header>

    <section id="work" class="wrap">
      <h2 class="section-title">Selected work</h2>

      <article class="project" style="--c: var(--matcha)">
        <div class="project-head">
          <h3>Iris Classifier</h3>
          <p>My first machine learning model in Python, 2026</p>
        </div>
        <div class="thumb t1" role="img" aria-label="Iris Classifier project preview"><i></i><i></i></div>
      </article>

      <article class="project" style="--c: var(--forest)">
        <div class="project-head">
          <h3>Data Dashboard</h3>
          <p>Charts and insights from a public dataset, 2026</p>
        </div>
        <div class="thumb t2" role="img" aria-label="Data Dashboard project preview"><i></i><i></i></div>
      </article>

      <article class="project" style="--c: var(--jade)">
        <div class="project-head">
          <h3>Study Planner</h3>
          <p>A small app that plans my weekly study time, 2026</p>
        </div>
        <div class="thumb t3" role="img" aria-label="Study Planner project preview"><i></i><i></i><i></i></div>
      </article>

      <article class="project" style="--c: var(--olive)">
        <div class="project-head">
          <h3>Mini Game</h3>
          <p>A simple 2D game with two levels, 2026</p>
        </div>
        <div class="thumb t4" role="img" aria-label="Mini Game project preview"><i></i><i></i></div>
      </article>
    </section>

    <section id="about" class="about">
      <div class="wrap">
        <h2 class="section-title" style="padding-top:0">About</h2>
        <p class="about-text">I'm Sakthi, a first-year student in Artificial Intelligence and Data Science. I'm learning Python, statistics and machine learning, and I build small projects to practice what I learn. I'm looking for internships, teammates and projects where I can learn from people who know more than I do.</p>
      </div>
    </section>

    <section id="contact" class="contact">
      <div class="wrap">
        <p>Want to work together or say hi? Email me.</p>
        <a class="mail" href="mailto:sakthi@example.com">sakthi@example.com</a>
      </div>
    </section>
  </main>

  <footer class="wrap">© 2026 Sakthi Krishnan</footer>

<script>
(() => {
  const reduce = matchMedia('(prefers-reduced-motion: reduce)').matches;

  // Convert letters and digits to Unicode Mathematical Sans-Serif Bold
  const bold = str => Array.from(str).map(ch => {
    const k = ch.codePointAt(0);
    if (k >= 65 && k <= 90)  return String.fromCodePoint(0x1D5D4 + k - 65);
    if (k >= 97 && k <= 122) return String.fromCodePoint(0x1D5EE + k - 97);
    if (k >= 48 && k <= 57)  return String.fromCodePoint(0x1D7EC + k - 48);
    return ch;
  }).join('');

  const bar = document.querySelector('.progress');
  const hero = document.querySelector('.hero');
  const l1 = hero.querySelector('.l1');
  const l2 = hero.querySelector('.l2');
  const role = hero.querySelector('.role');
  const about = document.querySelector('.about-text');

  // About: split into words (bold-converted), keep the real text for screen readers
  const original = about.textContent.trim();
  about.textContent = '';
  const sr = document.createElement('span');
  sr.className = 'sr';
  sr.textContent = original;
  about.append(sr);
  const spans = original.split(/\s+/).map(w => {
    const s = document.createElement('span');
    s.className = 'w';
    s.setAttribute('aria-hidden', 'true');
    s.textContent = bold(w);
    about.append(s, ' ');
    return s;
  });

  // Everything else: swap each text node for a bold version + hidden real text
  const walker = document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT, {
    acceptNode: n => {
      if (!n.nodeValue.trim()) return NodeFilter.FILTER_REJECT;
      const p = n.parentElement;
      if (p.closest('script, style, .about-text')) return NodeFilter.FILTER_REJECT;
      return NodeFilter.FILTER_ACCEPT;
    }
  });
  const nodes = [];
  while (walker.nextNode()) nodes.push(walker.currentNode);
  nodes.forEach(n => {
    const visual = document.createElement('span');
    visual.setAttribute('aria-hidden', 'true');
    visual.textContent = bold(n.nodeValue);
    const real = document.createElement('span');
    real.className = 'sr';
    real.textContent = n.nodeValue;
    n.replaceWith(visual, real);
  });

  // Wipe-in for project previews
  const thumbs = document.querySelectorAll('.thumb');
  if (reduce || !('IntersectionObserver' in window)) {
    thumbs.forEach(t => t.classList.add('in'));
  } else {
    const io = new IntersectionObserver(entries => {
      entries.forEach(e => {
        if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); }
      });
    }, { threshold: 0.25 });
    thumbs.forEach(t => io.observe(t));
  }

  const clamp = (n, a, b) => Math.min(b, Math.max(a, n));
  let ticking = false;

  function update() {
    ticking = false;
    const y = window.scrollY;
    const vh = window.innerHeight;
    const max = document.documentElement.scrollHeight - vh;
    bar.style.transform = `scaleX(${max > 0 ? clamp(y / max, 0, 1) : 0})`;

    if (reduce) return;

    // Hero: the two name lines slide apart and fade
    const p = clamp(y / (hero.offsetHeight * 0.8), 0, 1);
    l1.style.transform = `translate3d(${-p * 30}vw,0,0)`;
    l2.style.transform = `translate3d(${p * 30}vw,0,0)`;
    l1.style.opacity = l2.style.opacity = 1 - p;
    role.style.opacity = 1 - p * 1.6;

    // About: words light up as the paragraph scrolls through
    const r = about.getBoundingClientRect();
    const prog = clamp((vh * 0.8 - r.top) / (r.height + vh * 0.3), 0, 1);
    const lit = Math.round(prog * spans.length);
    spans.forEach((s, i) => s.classList.toggle('on', i < lit));
  }

  function onScroll() {
    if (!ticking) { ticking = true; requestAnimationFrame(update); }
  }
  addEventListener('scroll', onScroll, { passive: true });
  addEventListener('resize', onScroll);
  update();
})();
</script>
</body>
</html>

