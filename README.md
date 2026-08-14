<div align="center">

<!-- ========================================== -->
<!-- 1. DYNAMIC ANIMATED HERO BANNER (SVG)     -->
<!-- ========================================== -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 440" width="100%" height="auto">
  <defs>
    <!-- Background Gradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#070B08"/>
      <stop offset="40%" stop-color="#0E1410"/>
      <stop offset="80%" stop-color="#141F18"/>
      <stop offset="100%" stop-color="#1B2A22"/>
    </linearGradient>

    <!-- Animated Shimmering Gold Gradient -->
    <linearGradient id="animatedGold" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#8C6E2E"/>
      <stop offset="30%" stop-color="#E2CA83"/>
      <stop offset="50%" stop-color="#FFF4D0"/>
      <stop offset="70%" stop-color="#B9974A"/>
      <stop offset="100%" stop-color="#8C6E2E"/>
      <animate attributeName="x1" values="-100%;100%;-100%" dur="8s" repeatCount="indefinite"/>
      <animate attributeName="x2" values="0%;200%;0%" dur="8s" repeatCount="indefinite"/>
    </linearGradient>

    <!-- Pulsing Radial Ambient Light -->
    <radialGradient id="radialAura" cx="50%" cy="45%" r="55%">
      <stop offset="0%" stop-color="#B9974A" stop-opacity="0.22">
        <animate attributeName="stop-opacity" values="0.08;0.25;0.08" dur="5s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#0E1410" stop-opacity="0"/>
    </radialGradient>

    <!-- Scanning Light Bar Animation -->
    <linearGradient id="scanBeam" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#B9974A" stop-opacity="0"/>
      <stop offset="50%" stop-color="#E2CA83" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#B9974A" stop-opacity="0"/>
      <animate attributeName="x1" values="-100%;100%;-100%" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="x2" values="0%;200%;0%" dur="6s" repeatCount="indefinite"/>
    </linearGradient>

    <style>
      @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@700;900&family=Montserrat:wght@400;600&family=Playfair+Display:ital,wght@1,500&display=swap');

      .title {
        font-family: 'Cinzel', 'Playfair Display', Georgia, serif;
        font-size: 56px;
        fill: url(#animatedGold);
        font-weight: 900;
        letter-spacing: 8px;
        text-shadow: 0 0 20px rgba(185, 151, 74, 0.4);
      }
      .tagline {
        font-family: 'Montserrat', sans-serif;
        font-size: 13px;
        fill: #E2CA83;
        letter-spacing: 9px;
        font-weight: 600;
        text-transform: uppercase;
        opacity: 0.92;
      }
      .metadata {
        font-family: 'Montserrat', sans-serif;
        font-size: 12px;
        fill: #8F9E94;
        letter-spacing: 4px;
      }
      .quote {
        font-family: 'Playfair Display', Georgia, serif;
        font-size: 16px;
        fill: #F3EFE6;
        font-style: italic;
        opacity: 0.85;
        letter-spacing: 1.2px;
      }
      .border-pulse {
        animation: borderPulse 4s ease-in-out infinite alternate;
      }
      @keyframes borderPulse {
        0% { stroke-opacity: 0.25; stroke-width: 1; }
        100% { stroke-opacity: 0.75; stroke-width: 1.5; }
      }
    </style>
  </defs>

  <!-- Background Base -->
  <rect width="1200" height="440" fill="url(#bgGrad)" rx="16"/>
  <rect width="1200" height="440" fill="url(#radialAura)" rx="16"/>

  <!-- Glowing Outer Frame -->
  <rect x="22" y="22" width="1156" height="396" rx="12" fill="none" stroke="#B9974A" class="border-pulse"/>
  <rect x="30" y="30" width="1140" height="380" rx="8" fill="none" stroke="#B9974A" stroke-opacity="0.15" stroke-width="1"/>

  <!-- Scanning Border Accent -->
  <line x1="30" y1="30" x2="1170" y2="30" stroke="url(#scanBeam)" stroke-width="2"/>
  <line x1="30" y1="410" x2="1170" y2="410" stroke="url(#scanBeam)" stroke-width="2"/>

  <!-- Editorial Corner Ornaments -->
  <path d="M 22 55 L 22 22 L 55 22" stroke="#E2CA83" stroke-width="2" fill="none"/>
  <path d="M 1178 55 L 1178 22 L 1145 22" stroke="#E2CA83" stroke-width="2" fill="none"/>
  <path d="M 22 385 L 22 418 L 55 418" stroke="#E2CA83" stroke-width="2" fill="none"/>
  <path d="M 1178 385 L 1178 418 L 1145 418" stroke="#E2CA83" stroke-width="2" fill="none"/>

  <!-- Top Crown Accent -->
  <g transform="translate(600, 76)" text-anchor="middle">
    <line x1="-160" y1="0" x2="-30" y2="0" stroke="#B9974A" stroke-opacity="0.5" stroke-width="1"/>
    <polygon points="0,-5 5,0 0,5 -5,0" fill="#E2CA83"/>
    <line x1="30" y1="0" x2="160" y2="0" stroke="#B9974A" stroke-opacity="0.5" stroke-width="1"/>
    <text y="28" class="tagline">SOFTWARE ENGINEERING &amp; PROMPT ARCHITECTURE</text>
  </g>

  <!-- Hero Name -->
  <text x="600" y="202" text-anchor="middle" class="title">MANPREET SINGH</text>

  <!-- Sub-details -->
  <text x="600" y="246" text-anchor="middle" class="metadata">CHANDIGARH, INDIA &nbsp;•&nbsp; B.TECH CSE (SVIET / PTU)</text>

  <!-- Editorial Divider -->
  <g transform="translate(600, 286)">
    <line x1="-220" y1="0" x2="220" y2="0" stroke="#B9974A" stroke-opacity="0.35" stroke-width="1"/>
    <circle cx="0" cy="0" r="3.5" fill="#E2CA83"/>
    <circle cx="-20" cy="0" r="2" fill="#B9974A" opacity="0.6"/>
    <circle cx="20" cy="0" r="2" fill="#B9974A" opacity="0.6"/>
  </g>

  <!-- Quote -->
  <text x="600" y="342" text-anchor="middle" class="quote">"Synthesizing algorithmic precision with advanced generative intelligence."</text>
</svg>

<br/>

<!-- ========================================== -->
<!-- 2. DYNAMIC LIVE TYPING SVG                 -->
<!-- ========================================== -->
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Cinzel&weight=700&size=20&pause=1800&color=B9974A&center=true&vCenter=true&width=800&lines=ARCHITECTING+ROBUST+SYSTEMS+IN+C%2B%2B+%26+PYTHON;AI+ORCHESTRATION+%7C+PROMPT+ENGINEERING+SPECIALIST;BUILDING+EDITORIAL-GRADE+WEB+INTERFACES;DISCIPLINE+%2B+PRECISION+IN+EVERY+LINE+OF+CODE" alt="Live Typing Reel" />
</a>

<br/><br/>

<!-- ========================================== -->
<!-- 3. INTERACTIVE PROFILE BADGES              -->
<!-- ========================================== -->
<p align="center">
  <a href="https://github.com/mxnpreet7">
    <img src="https://img.shields.io/badge/ACADEMIC-B.Tech_CSE_@_SVIET-0E1410?style=for-the-badge&labelColor=1B2A22&color=B9974A&logoColor=F3EFE6" alt="Academic Affiliation" />
  </a>
  &nbsp;
  <a href="https://github.com/mxnpreet7">
    <img src="https://img.shields.io/badge/FOUNDATION-Class_XII_81.6%25-0E1410?style=for-the-badge&labelColor=1B2A22&color=B9974A" alt="Academic Score" />
  </a>
  &nbsp;
  <a href="https://komarev.com/ghpvc/?username=mxnpreet7">
    <img src="https://komarev.com/ghpvc/?username=mxnpreet7&label=PORTFOLIO+VISITS&color=B9974A&style=for-the-badge&base=100" alt="Live Views" />
  </a>
</p>

</div>

---

### 🏛️ Executive Dossier

> *Operating at the nexus of deterministic computational logic and modern generative AI models.*

<!-- ========================================== -->
<!-- 4. ANIMATED LIVE INTERACTIVE TERMINAL     -->
<!-- ========================================== -->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 850 260" width="100%" height="auto">
  <defs>
    <style>
      .term-body { font-family: 'Fira Code', 'Courier New', monospace; font-size: 13px; fill: #F3EFE6; }
      .gold-tag { fill: #E2CA83; font-weight: bold; }
      .dim-tag { fill: #8F9E94; }
      .comment-tag { fill: #607368; font-style: italic; }
      .cursor-blink {
        animation: cursorBlink 0.9s steps(2, start) infinite;
        fill: #B9974A;
      }
      @keyframes cursorBlink {
        0%, 100% { opacity: 1; }
        50% { opacity: 0; }
      }
    </style>
  </defs>

  <rect width="850" height="260" rx="10" fill="#0E1410" stroke="#1B2A22" stroke-width="2"/>
  
  <!-- Terminal Top Navigation -->
  <rect width="850" height="34" rx="10" fill="#141F18"/>
  <circle cx="22" cy="17" r="5" fill="#8C6E2E"/>
  <circle cx="38" cy="17" r="5" fill="#B9974A"/>
  <circle cx="54" cy="17" r="5" fill="#E2CA83"/>
  <text x="425" y="22" text-anchor="middle" font-family="'Fira Code', monospace" font-size="11" fill="#8F9E94" letter-spacing="2">manpreet@chandigarh-core : active-session</text>

  <!-- Interactive Content Flow -->
  <g transform="translate(26, 64)">
    <text y="0" class="term-body"><tspan class="gold-tag">mxnpreet7@core:~$</tspan> query --profile --verbose</text>
    <text y="26" class="dim-tag">[+] Identity        :</text><text x="180" y="26" class="term-body">Manpreet Singh (Software Developer &amp; AI Prompt Architect)</text>
    <text y="52" class="dim-tag">[+] Education       :</text><text x="180" y="52" class="term-body">B.Tech Computer Science &amp; Engineering (PTU Curriculum)</text>
    <text y="78" class="dim-tag">[+] Core Stack      :</text><text x="180" y="78" class="term-body">C, C++, Python, Modern Web, Prompt Architecture</text>
    <text y="104" class="dim-tag">[+] Freelance Hub   :</text><text x="180" y="104" class="term-body">Custom Prompt Systems, Executive Resumes, Content Architecture</text>
    <text y="130" class="comment-tag">/* Status: 100% operational | Delivering high-yield precision solutions */</text>
    <text y="160" class="gold-tag">mxnpreet7@core:~$ <tspan class="cursor-blink">█</tspan></text>
  </g>
</svg>

---

### ⚡ Technology & Tooling Matrix

<div align="center">

#### `Core Engineering Languages`
<br/>

<a href="#skills">
  <img src="https://img.shields.io/badge/C-0E1410?style=for-the-badge&logo=c&logoColor=B9974A&labelColor=1B2A22" height="38" alt="C" />
</a>
&nbsp;
<a href="#skills">
  <img src="https://img.shields.io/badge/C%2B%2B-0E1410?style=for-the-badge&logo=c%2B%2B&logoColor=B9974A&labelColor=1B2A22" height="38" alt="C++" />
</a>
&nbsp;
<a href="#skills">
  <img src="https://img.shields.io/badge/Python-0E1410?style=for-the-badge&logo=python&logoColor=B9974A&labelColor=1B2A22" height="38" alt="Python" />
</a>
&nbsp;
<a href="#skills">
  <img src="https://img.shields.io/badge/HTML5-0E1410?style=for-the-badge&logo=html5&logoColor=B9974A&labelColor=1B2A22" height="38" alt="HTML5" />
</a>
&nbsp;
<a href="#skills">
  <img src="https://img.shields.io/badge/CSS3-0E1410?style=for-the-badge&logo=css3&logoColor=B9974A&labelColor=1B2A22" height="38" alt="CSS3" />
</a>
&nbsp;
<a href="#skills">
  <img src="https://img.shields.io/badge/JavaScript-0E1410?style=for-the-badge&logo=javascript&logoColor=B9974A&labelColor=1B2A22" height="38" alt="JavaScript" />
</a>

<br/><br/>

#### `Generative AI & Prompt Engineering Orchestration`
*Treating Prompt Engineering as an exact, high-leverage architectural discipline.*
<br/><br/>

<a href="#ai">
  <img src="https://img.shields.io/badge/Claude_3.5_Sonnet-0E1410?style=for-the-badge&logo=anthropic&logoColor=B9974A&labelColor=1B2A22" height="35" alt="Claude" />
</a>
&nbsp;
<a href="#ai">
  <img src="https://img.shields.io/badge/ChatGPT_&_GPT--4o-0E1410?style=for-the-badge&logo=openai&logoColor=B9974A&labelColor=1B2A22" height="35" alt="ChatGPT" />
</a>
&nbsp;
<a href="#ai">
  <img src="https://img.shields.io/badge/DeepSeek_V3_/_R1-0E1410?style=for-the-badge&logo=deepseek&logoColor=B9974A&labelColor=1B2A22" height="35" alt="DeepSeek" />
</a>
&nbsp;
<a href="#ai">
  <img src="https://img.shields.io/badge/Google_Gemini-0E1410?style=for-the-badge&logo=googlegemini&logoColor=B9974A&labelColor=1B2A22" height="35" alt="Gemini" />
</a>
<br/><br/>
<a href="#ai">
  <img src="https://img.shields.io/badge/GitHub_Copilot-0E1410?style=for-the-badge&logo=githubcopilot&logoColor=B9974A&labelColor=1B2A22" height="35" alt="Copilot" />
</a>
&nbsp;
<a href="#ai">
  <img src="https://img.shields.io/badge/Kimi_AI-0E1410?style=for-the-badge&logo=openai&logoColor=B9974A&labelColor=1B2A22" height="35" alt="Kimi AI" />
</a>
&nbsp;
<a href="#ai">
  <img src="https://img.shields.io/badge/Prompt_Architecture-0E1410?style=for-the-badge&logo=databricks&logoColor=B9974A&labelColor=1B2A22" height="35" alt="Prompt Design" />
</a>

</div>

---

### 💼 Specializations & Professional Focus

```yaml
Freelance Practice & AI Orchestration:
  - Specialization: Precision Prompt Engineering & Content Systems
  - Offerings:
      ├── High-Impact Custom LLM Prompt Packages
      ├── Executive & Technical Resume Architectures
      └── Engagement-Engineered Digital Copy & Captions

Software Engineering & Web Craft:
  - Architecture: High-Performance, Accessible Interfaces
  - Philosophy: Minimal overhead, clean syntax, structured algorithms
  - Stack: C, C++, Python, Git Workflow, Modern Frontend
