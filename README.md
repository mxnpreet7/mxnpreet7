<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Manpreet — Developer & Prompt Engineer</title>
<style>
:root{
  --ink:#0E1410;
  --parchment:#F3EFE6;
  --gold:#B9974A;
  --gold-soft:#E8D9AE;
  --forest:#1B2A22;
  --line:rgba(243,239,230,0.14);
  --serif:'Iowan Old Style','Palatino Linotype',Georgia,serif;
  --sans:'Helvetica Neue',Arial,sans-serif;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  background:var(--ink);
  color:var(--parchment);
  font-family:var(--sans);
  overflow-x:hidden;
}
::selection{background:var(--gold);color:var(--ink);}

/* ---- cursor glow ---- */
#glow{
  position:fixed;width:500px;height:500px;border-radius:50%;
  background:radial-gradient(circle, rgba(185,151,74,0.10) 0%, transparent 70%);
  pointer-events:none;z-index:0;transition:transform 0.15s ease-out;
}

/* ---- nav ---- */
nav{
  position:fixed;top:0;left:0;right:0;z-index:50;
  display:flex;justify-content:space-between;align-items:center;
  padding:28px 6vw;
  mix-blend-mode:difference;
}
.logo{font-family:var(--serif);font-size:20px;letter-spacing:2px;}
.navlinks{display:flex;gap:36px;font-size:12px;letter-spacing:2px;text-transform:uppercase;}
.navlinks a{color:var(--parchment);text-decoration:none;opacity:0.7;transition:opacity 0.3s;}
.navlinks a:hover{opacity:1;}

/* ---- hero ---- */
.hero{
  min-height:100vh;position:relative;
  display:flex;flex-direction:column;justify-content:center;
  padding:0 6vw;z-index:1;
}
.eyebrow{
  font-size:12px;letter-spacing:4px;text-transform:uppercase;color:var(--gold);
  opacity:0;animation:rise 1s ease forwards 0.2s;
}
.hero h1{
  font-family:var(--serif);
  font-weight:400;
  font-size:clamp(52px,9vw,128px);
  line-height:0.95;
  margin:18px 0;
  opacity:0;animation:rise 1s ease forwards 0.4s;
}
.hero h1 em{font-style:italic;color:var(--gold-soft);}
.hero p.sub{
  max-width:520px;font-size:17px;line-height:1.6;color:rgba(243,239,230,0.75);
  opacity:0;animation:rise 1s ease forwards 0.6s;
}
.hero-meta{
  margin-top:48px;display:flex;gap:50px;
  opacity:0;animation:rise 1s ease forwards 0.8s;
}
.hero-meta div span{display:block;font-size:11px;letter-spacing:2px;text-transform:uppercase;color:var(--gold);margin-bottom:6px;}
.hero-meta div p{font-family:var(--serif);font-size:15px;}
@keyframes rise{from{opacity:0;transform:translateY(24px);}to{opacity:1;transform:translateY(0);}}

.scroll-cue{
  position:absolute;bottom:40px;left:6vw;font-size:11px;letter-spacing:2px;text-transform:uppercase;
  display:flex;align-items:center;gap:10px;color:var(--gold-soft);opacity:0.6;
}
.scroll-cue .bar{width:1px;height:40px;background:var(--gold);position:relative;overflow:hidden;}
.scroll-cue .bar::after{
  content:'';position:absolute;top:-100%;left:0;width:100%;height:100%;background:var(--parchment);
  animation:drip 1.8s ease-in-out infinite;
}
@keyframes drip{0%{top:-100%;}50%{top:0;}100%{top:100%;}}

/* ---- section shell ---- */
section{position:relative;z-index:1;padding:140px 6vw;border-top:1px solid var(--line);}
.label{
  font-size:12px;letter-spacing:4px;text-transform:uppercase;color:var(--gold);
  display:flex;align-items:center;gap:16px;margin-bottom:56px;
}
.label::after{content:'';flex:1;height:1px;background:var(--line);}

/* reveal on scroll */
.reveal{opacity:0;transform:translateY(30px);transition:opacity 0.9s ease, transform 0.9s ease;}
.reveal.in{opacity:1;transform:translateY(0);}

/* ---- about ---- */
.about-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:80px;align-items:start;}
.about-grid h2{font-family:var(--serif);font-size:clamp(28px,3vw,42px);font-weight:400;line-height:1.35;}
.about-grid h2 em{color:var(--gold-soft);font-style:italic;}
.about-list{display:flex;flex-direction:column;gap:22px;}
.about-list .row{
  display:flex;justify-content:space-between;border-bottom:1px solid var(--line);padding-bottom:18px;
  font-size:14px;
}
.about-list .row .k{color:rgba(243,239,230,0.55);letter-spacing:1px;text-transform:uppercase;font-size:11px;}
.about-list .row .v{font-family:var(--serif);font-size:16px;text-align:right;}

/* ---- skills marquee ---- */
.marquee-wrap{overflow:hidden;border-top:1px solid var(--line);border-bottom:1px solid var(--line);padding:34px 0;margin:0;}
.marquee{display:flex;gap:60px;white-space:nowrap;animation:scroll 26s linear infinite;width:max-content;}
.marquee span{font-family:var(--serif);font-size:34px;color:rgba(243,239,230,0.25);}
.marquee span.on{color:var(--gold-soft);}
@keyframes scroll{from{transform:translateX(0);}to{transform:translateX(-50%);}}

/* ---- capability cards ---- */
.cap-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--line);border:1px solid var(--line);}
.cap-card{background:var(--ink);padding:42px 34px;transition:background 0.4s ease;}
.cap-card:hover{background:var(--forest);}
.cap-num{font-size:11px;color:var(--gold);letter-spacing:2px;margin-bottom:24px;display:block;}
.cap-card h3{font-family:var(--serif);font-size:22px;font-weight:400;margin-bottom:14px;}
.cap-card p{font-size:13.5px;line-height:1.7;color:rgba(243,239,230,0.6);}

/* ---- soft skills : compass ---- */
.compass{display:grid;grid-template-columns:repeat(4,1fr);gap:40px;}
.compass-item{text-align:left;border-left:1px solid var(--line);padding-left:22px;position:relative;}
.compass-item::before{
  content:'';position:absolute;left:-1px;top:0;width:1px;height:0;background:var(--gold);
  transition:height 1.1s ease;
}
.compass-item.in::before{height:100%;}
.compass-item h4{font-family:var(--serif);font-size:19px;font-weight:400;margin-bottom:10px;color:var(--gold-soft);}
.compass-item p{font-size:13px;color:rgba(243,239,230,0.55);line-height:1.6;}

/* ---- contact ---- */
.contact{text-align:left;}
.contact h2{
  font-family:var(--serif);font-weight:400;
  font-size:clamp(38px,6vw,84px);line-height:1.05;max-width:900px;
}
.contact h2 a{color:var(--gold-soft);text-decoration:none;border-bottom:1px solid var(--gold);transition:opacity 0.3s;}
.contact h2 a:hover{opacity:0.7;}
.contact-links{display:flex;gap:50px;margin-top:60px;flex-wrap:wrap;}
.contact-links a{
  color:var(--parchment);text-decoration:none;font-size:13px;letter-spacing:1px;
  display:flex;align-items:center;gap:10px;border-bottom:1px solid transparent;padding-bottom:4px;
  transition:border-color 0.3s,color 0.3s;
}
.contact-links a:hover{border-color:var(--gold);color:var(--gold-soft);}
.contact-links a .arrow{transition:transform 0.3s;}
.contact-links a:hover .arrow{transform:translate(3px,-3px);}

footer{
  padding:30px 6vw;font-size:11px;letter-spacing:1px;color:rgba(243,239,230,0.35);
  display:flex;justify-content:space-between;border-top:1px solid var(--line);position:relative;z-index:1;
}

@media(max-width:820px){
  .about-grid{grid-template-columns:1fr;gap:50px;}
  .cap-grid{grid-template-columns:1fr;}
  .compass{grid-template-columns:1fr 1fr;}
  .navlinks{display:none;}
}
@media (prefers-reduced-motion: reduce){
  *{animation:none !important;transition:none !important;}
}
</style>
</head>
<body>

<div id="glow"></div>

<nav>
  <div class="logo">MANPREET</div>
  <div class="navlinks">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#soft">Approach</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<section class="hero">
  <div class="eyebrow">B.Tech CSE · PTU · Chandigarh</div>
  <h1>Manpreet<br><em>Singh</em></h1>
  <p class="sub">I build with code and with AI in the same breath — treating prompt engineering as a craft, not a shortcut. Currently exploring web development and AI-assisted freelance work.</p>
  <div class="hero-meta">
    <div><span>Focus</span><p>AI Tools & Development</p></div>
    <div><span>Based In</span><p>Chandigarh, India</p></div>
    <div><span>Status</span><p>Open to work</p></div>
  </div>
  <div class="scroll-cue"><div class="bar"></div>Scroll</div>
</section>

<section id="about">
  <div class="label">About</div>
  <div class="about-grid reveal">
    <h2>I sit at the intersection of <em>traditional engineering discipline</em> and <em>modern AI fluency</em> — using tools like Claude, GPT and Gemini not as crutches, but as instruments I've learned to play well.</h2>
    <div class="about-list">
      <div class="row"><span class="k">Education</span><span class="v">B.Tech CSE, SVIET (PTU)</span></div>
      <div class="row"><span class="k">Class XII</span><span class="v">81.6%</span></div>
      <div class="row"><span class="k">Core Language</span><span class="v">C, C++, Python</span></div>
      <div class="row"><span class="k">Specialty</span><span class="v">Prompt Engineering</span></div>
      <div class="row"><span class="k">Interest</span><span class="v">AI-Assisted Freelancing</span></div>
    </div>
  </div>
</section>

<div class="marquee-wrap">
  <div class="marquee">
    <span class="on">C++</span><span>PYTHON</span><span class="on">C</span><span>PROMPT ENGINEERING</span><span class="on">CLAUDE</span><span>GIT</span><span class="on">GITHUB</span><span>WEB DEV</span>
    <span class="on">C++</span><span>PYTHON</span><span class="on">C</span><span>PROMPT ENGINEERING</span><span class="on">CLAUDE</span><span>GIT</span><span class="on">GITHUB</span><span>WEB DEV</span>
  </div>
</div>

<section id="skills">
  <div class="label">Capabilities</div>
  <div class="cap-grid">
    <div class="cap-card reveal">
      <span class="cap-num">01</span>
      <h3>Core Programming</h3>
      <p>Solid foundation in C, growing fluency in C++ and Python — building the logic layer beneath every AI-assisted workflow.</p>
    </div>
    <div class="cap-card reveal">
      <span class="cap-num">02</span>
      <h3>Prompt Engineering</h3>
      <p>Fluent across Claude, ChatGPT, Gemini, DeepSeek, Copilot and Kimi — engineering prompts as a repeatable, professional skill.</p>
    </div>
    <div class="cap-card reveal">
      <span class="cap-num">03</span>
      <h3>Applied AI Work</h3>
      <p>Turning AI fluency into real output: resumes, study guides, freelance service concepts, and early web builds.</p>
    </div>
  </div>
</section>

<section id="soft">
  <div class="label">How I Work</div>
  <div class="compass">
    <div class="compass-item reveal"><h4>Leadership</h4><p>Comfortable taking initiative and owning outcomes, not just tasks.</p></div>
    <div class="compass-item reveal"><h4>Decision Making</h4><p>Weigh options quickly, commit, and adjust course without hesitation.</p></div>
    <div class="compass-item reveal"><h4>Communication</h4><p>Explain technical ideas plainly — to teammates, recruiters, or clients.</p></div>
    <div class="compass-item reveal"><h4>Teamwork & Creativity</h4><p>Bring collaborative energy and original thinking to every build.</p></div>
  </div>
</section>

<section id="contact" class="contact">
  <div class="label">Contact</div>
  <h2 class="reveal">Let's build<br>something with <a href="mailto:iammanpreet640@gmail.com">intent</a>.</h2>
  <div class="contact-links reveal">
    <a href="mailto:iammanpreet640@gmail.com">Email <span class="arrow">↗</span></a>
    <a href="https://www.linkedin.com/in/manpreet-singh-7063703b2" target="_blank">LinkedIn <span class="arrow">↗</span></a>
    <a href="https://github.com/mxnpreet7" target="_blank">GitHub <span class="arrow">↗</span></a>
  </div>
</section>

<footer>
  <span>© 2026 Manpreet Singh</span>
  <span>Designed & built with intent</span>
</footer>

<script>
// cursor glow
const glow = document.getElementById('glow');
document.addEventListener('mousemove', e=>{
  glow.style.transform = `translate(${e.clientX-250}px, ${e.clientY-250}px)`;
});

// scroll reveal
const io = new IntersectionObserver((entries)=>{
  entries.forEach(en=>{ if(en.isIntersecting) en.target.classList.add('in'); });
},{threshold:0.15});
document.querySelectorAll('.reveal, .compass-item').forEach(el=>io.observe(el));
</script>

</body>
</html>
