
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Naveen Kumar B | Portfolio</title>
  <style>
    :root {
      --primary: #4CAF50;
      --primary-glow: rgba(76, 175, 80, 0.4);
      --dark: #0a0a0a;
      --card-bg: #141414;
      --text: #ffffff;
      --muted: #b0b0b0;
    }
    
    /* Smooth Scroll Tracking */
    html {
      scroll-behavior: smooth;
    }

    * { 
      box-sizing: border-box; 
      margin: 0; 
      padding: 0; 
    }
    
    body { 
      background: var(--dark); 
      color: var(--text); 
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
      line-height: 1.6;
      overflow-x: hidden;
    }
    
    /* Sticky Navigation Bar with backdrop filter */
    nav { 
      background: rgba(0, 0, 0, 0.85); 
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      padding: 20px; 
      text-align: center; 
      position: sticky; 
      top: 0; 
      z-index: 1000; 
      border-bottom: 1px solid #222; 
    }
    
    nav a { 
      color: var(--text); 
      text-decoration: none; 
      margin: 0 15px; 
      font-weight: 500; 
      position: relative;
      padding-bottom: 5px;
      transition: color 0.3s ease; 
    }
    
    nav a:hover { 
      color: var(--primary); 
    }
    
    nav a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: var(--primary);
      transition: width 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    nav a:hover::after {
      width: 100%;
    }

    /* HIGH-EFFECT SHIFTING GRADIENT HEADER BLOCK */
    header { 
      background: linear-gradient(-45deg, #0f1f11, #141414, #050b06, #112614);
      background-size: 400% 400%;
      animation: gradientBG 12s ease infinite;
      text-align: center; 
      padding: 150px 20px; 
      border-bottom: 1px solid #1e3a20; 
      position: relative;
      box-shadow: inset 0 -50px 100px rgba(0,0,0,0.8);
    }
    
    .header-reveal {
      animation: fadeInUp 1.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
      opacity: 0;
    }
    
    header h1 { 
      font-size: 4.2rem; 
      margin-bottom: 15px; 
      letter-spacing: 2px;
      text-shadow: 0 0 30px rgba(76, 175, 80, 0.2);
    }
    
    header p { 
      font-size: 1.5rem; 
      color: var(--primary); 
      margin-bottom: 25px; 
      font-weight: 400; 
      letter-spacing: 1px;
      text-shadow: 0 0 12px var(--primary-glow);
    }
    
    header .sub { 
      font-size: 1.1rem; 
      color: var(--muted); 
      max-width: 700px; 
      margin: 0 auto; 
      line-height: 1.8;
    }

    /* Standard Layout Space */
    .container { 
      max-width: 1100px; 
      margin: auto; 
      padding: 20px; 
    }
    
    section { 
      padding: 90px 0; 
      border-bottom: 1px solid #1a1a1a; 
    }
    
    /* ANIMATED GLOWING HEADERS & REVEAL LINES */
    h2 { 
      color: var(--primary); 
      font-size: 2.3rem; 
      margin-bottom: 45px; 
      text-transform: uppercase; 
      letter-spacing: 2px;
      position: relative;
      display: inline-block;
      text-shadow: 0 0 10px rgba(76, 175, 80, 0.2);
    }
    
    h2::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -10px;
      width: 65px;
      height: 3px;
      background: var(--primary);
      box-shadow: 0 0 12px var(--primary), 0 0 20px var(--primary);
      animation: expandLine 2s ease-out infinite alternate;
    }

    /* Responsive Presentation Cards */
    .grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); 
      gap: 35px; 
    }
    
    .card { 
      background: var(--card-bg); 
      padding: 35px; 
      border-radius: 14px; 
      border: 1px solid #222; 
      position: relative;
      overflow: hidden;
      transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), 
                  border-color 0.4s ease, 
                  box-shadow 0.4s ease; 
    }
    
    .card:hover { 
      transform: translateY(-12px); 
      border-color: var(--primary); 
      box-shadow: 0 20px 40px rgba(76, 175, 80, 0.15);
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 4px;
      height: 100%;
      background: var(--primary);
      transform: scaleY(0);
      transition: transform 0.3s ease;
    }

    .card:hover::before {
      transform: scaleY(1);
    }
    
    .card h3 { 
      margin-bottom: 12px; 
      color: #fff; 
      font-size: 1.45rem;
    }
    
    .card h4 { 
      color: var(--primary); 
      margin-bottom: 12px; 
      font-weight: 400; 
    }
    
    .meta { 
      font-size: 0.95rem; 
      color: var(--muted); 
      margin-bottom: 18px; 
      display: block; 
    }

    /* Work Experience Checked Architecture */
    .experience-list {
      list-style: none;
      margin-top: 15px;
    }

    .experience-list li {
      position: relative;
      padding-left: 25px;
      margin-bottom: 12px;
      color: #e0e0e0;
      font-size: 0.98rem;
    }

    .experience-list li::before {
      content: '✓';
      position: absolute;
      left: 0;
      color: var(--primary);
      font-weight: bold;
      text-shadow: 0 0 8px var(--primary);
    }

    /* Responsive Grid layout for Interactive Skills */
    .skills-grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
      gap: 30px; 
    }
    
    .skills-box {
      background: #0f0f0f;
      padding: 30px;
      border-radius: 12px;
      border: 1px solid #1a1a1a;
      transition: border-color 0.3s ease;
    }

    .skills-box:hover {
      border-color: rgba(76, 175, 80, 0.3);
    }
    
    .skills-box h3 {
      font-size: 1.25rem;
      margin-bottom: 20px;
      color: #fff;
      border-bottom: 1px solid #222;
      padding-bottom: 10px;
      position: relative;
    }
    
    .skills-box ul { 
      list-style: none; 
    }
    
    .skills-box li { 
      background: #181818; 
      padding: 12px 18px; 
      margin-bottom: 12px; 
      border-radius: 8px; 
      font-size: 0.95rem; 
      border-left: 4px solid var(--primary); 
      transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), background 0.3s ease;
    }
    
    .skills-box li:hover {
      transform: translateX(10px) scale(1.02);
      background: #1f2d21;
    }

    /* Forms Interactivity elements */
    form { 
      max-width: 650px; 
      margin: auto; 
      background: var(--card-bg); 
      padding: 40px; 
      border-radius: 14px; 
      border: 1px solid #222; 
    }
    
    input, textarea { 
      width: 100%; 
      padding: 15px; 
      margin: 12px 0; 
      background: #181818; 
      border: 1px solid #2a2a2a; 
      border-radius: 8px; 
      color: #fff; 
      font-family: inherit; 
      transition: border-color 0.3s ease, box-shadow 0.3s ease; 
    }
    
    input:focus, textarea:focus { 
      border-color: var(--primary); 
      outline: none; 
      box-shadow: 0 0 15px rgba(76, 175, 80, 0.25);
    }
    
    button { 
      background: var(--primary); 
      color: #000; 
      font-weight: bold; 
      border: none; 
      padding: 16px 20px; 
      border-radius: 8px; 
      cursor: pointer; 
      width: 100%; 
      font-size: 16px; 
      transition: all 0.3s ease; 
      text-transform: uppercase; 
      letter-spacing: 1px;
    }
    
    button:hover { 
      background: #45a049; 
      box-shadow: 0 0 20px var(--primary);
      transform: translateY(-3px);
    }

    /* HIGH-EFFECT FLOATING GLOW FOOTER BLOCK */
    footer { 
      background: #030704; 
      color: #ddd; 
      padding: 60px 20px; 
      font-family: 'Segoe UI', sans-serif; 
      border-top: 1px solid #152b18; 
      position: relative;
    }
    
    footer::before {
      content: '';
      position: absolute;
      top: -1px;
      left: 50%;
      transform: translateX(-50%);
      width: 90%;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--primary), #fff, var(--primary), transparent);
      animation: pulseGlow 5s ease-in-out infinite;
    }
    
    .footer-content { 
      max-width: 800px; 
      margin: auto; 
      display: flex; 
      flex-direction: column; 
      align-items: center; 
    }
    
    .footer-content p { 
      margin: 6px 0; 
      text-align: center; 
    }
    
    .footer-links { 
      margin-top: 30px; 
    }
    
    /* Neon Circular Interactive Bubble Link Modules */
    .footer-links a { 
      color: #fff; 
      text-decoration: none; 
      margin: 0 15px; 
      font-weight: 500; 
      padding: 10px 24px;
      border: 1px solid #333;
      border-radius: 30px;
      display: inline-block;
      box-shadow: inset 0 0 0 rgba(255,255,255,0);
      transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1); 
    }
    
    .footer-links a:hover { 
      color: var(--primary); 
      border-color: var(--primary);
      background: rgba(76, 175, 80, 0.08);
      box-shadow: 0 0 20px var(--primary-glow), inset 0 0 8px rgba(76,175,80,0.1);
      transform: translateY(-5px);
    }

    /* Layout Timelines & Rendering Keyframes */
    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(50px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.4; width: 70%; }
      50% { opacity: 1; width: 95%; }
    }

    @keyframes expandLine {
      from { width: 50px; }
      to { width: 110px; }
    }

    /* Display Architecture Scaling */
    @media (max-width: 768px) { 
      header h1 { font-size: 2.8rem; }
      nav a { margin: 0 6px; font-size: 0.9rem; }
      .footer-links a { margin: 8px; padding: 8px 18px; }
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav>
    <a href="#about">About</a>
    <a href="#education">Education Section</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#my professional work">My Professional Work</a>
    <a href="#contact">Contact</a>
  </nav>

<a id="scroll-left-pop" class="left-popup-box">
  <img src="naveenkumar.jpg.jpeg" alt="Pop-up Image">
</a>

<style>
  .left-popup-box {
    position: fixed;
    bottom: 80px;          
    left: -120px; /* FIXED: Start completely off-screen so the slide-in effect is visible */       
    width: 100px;
    height: 100px;
    border-radius: 50%;
    overflow: hidden;
    border: 2px solid #4CAF50;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5);
    z-index: 99999;        
    display: block; 
    
    /* Smooth cubic-bezier transition for a nice "pop/bounce" effect */
    transition: left 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }

  .left-popup-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  /* When this class is added via JS, it overrides the default 'left' value */
  .left-popup-box.slide-in {
    left: 25px;            
  }
</style>

<script>
  window.addEventListener('scroll', function() {
    const popImage = document.getElementById('scroll-left-pop');
    
    // Checks if user has scrolled down more than 200px
    if (window.scrollY > 200) {
      popImage.classList.add('slide-in');
    } else {
      popImage.classList.remove('slide-in');
    }
  });
</script>

<a id="scroll-right-pop" class="right-popup-box">
  <img src="Indiaflag.jpg" alt="Pop-up Image">
</a>

<style>
  .right-popup-box {
    position: fixed;
    top: 80px;            /* Positioned near the top */
    right: -120px;        /* Hidden off-screen to the right initially */       
    width: 100px;
    height: 100px;
    border-radius: 50%;
    overflow: hidden;
    border: 2px solid #4CAF50;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5);
    z-index: 99999;        
    display: block; 
    
    /* Smooth transition on the 'right' property */
    transition: right 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }

  .right-popup-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  /* When scrolled down, slides in 25px away from the right edge */
  .right-popup-box.slide-in {
    right: 25px;            
  }
</style>

<script>
  window.addEventListener('scroll', function() {
    const popImage = document.getElementById('scroll-right-pop');
    
    if (window.scrollY > 200) {
      popImage.classList.add('slide-in');
    } else {
      popImage.classList.remove('slide-in');
    }
  });
</script>

<a id="scroll-right-pop" class="vfx-box" onclick="popLike(event)">
  <div class="thumb-container">
    <img src="thumbsup.gif" alt="Like" class="thumb-gif">
    <div class="shockwave"></div>
  </div>
  <span id="like-count" class="vfx-counter">0</span>
</a>

<style>
  /* Base Floating Container */
  .vfx-box {
    position: fixed;
    top: 80px;            
    right: -130px; 
    width: 90px;
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
    z-index: 99999;        
    text-decoration: none;
    user-select: none;
    transition: right 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }

  .vfx-box.slide-in {
    right: 25px;            
    animation: gentleFloat 3s ease-in-out infinite alternate;
  }

  /* Futuristic Cyber-Glow Wrapper */
  .thumb-container {
    position: relative;
    width: 76px;
    height: 76px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.9);
    border: 2px solid #00e676;
    box-shadow: 0 0 15px rgba(0, 230, 118, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.2s ease;
  }

  /* GIF Layout Optimization */
  .thumb-gif {
    width: 45px;
    height: 45px;
    object-fit: contain;
    pointer-events: none;
  }

  /* Instant Visual Effect Styles triggered by JS */
  .pop-impact {
    animation: impactWarp 0.4s ease-out;
  }

  @keyframes impactWarp {
    0% { transform: scale(1); filter: brightness(1); }
    30% { transform: scale(1.35) rotate(-10deg); filter: brightness(1.4) drop-shadow(0 0 10px #00e676); }
    100% { transform: scale(1); filter: brightness(1); }
  }

  /* Radial Shockwave Pulse Ring */
  .shockwave {
    position: absolute;
    inset: 0;
    border-radius: 50%;
    border: 3px solid #00e676;
    opacity: 0;
    pointer-events: none;
  }

  .pulse-blast {
    animation: waveBlast 0.5s cubic-bezier(0.1, 0.8, 0.3, 1);
  }

  @keyframes waveBlast {
    0% { transform: scale(0.9); opacity: 1; }
    100% { transform: scale(1.8); opacity: 0; filter: blur(2px); }
  }

  /* Neon Counter Glass Badge */
  .vfx-counter {
    margin-top: 8px;
    background: linear-gradient(135deg, #00e676, #00b0ff);
    color: white;
    font-family: system-ui, sans-serif;
    font-size: 0.85rem;
    font-weight: bold;
    padding: 3px 12px;
    border-radius: 20px;
    box-shadow: 0 4px 10px rgba(0,230,118,0.3);
    min-width: 35px;
    text-align: center;
  }

  .bump { animation: miniBump 0.2s ease-out; }
  @keyframes miniBump { 50% { transform: scale(1.2); } }
  @keyframes gentleFloat { 100% { transform: translateY(-5px); } }
</style>

<script>
  // Slide-in visibility detector
  window.addEventListener('scroll', function() {
    const box = document.getElementById('scroll-right-pop');
    if (window.scrollY > 200) box.classList.add('slide-in');
    else box.classList.remove('slide-in');
  });

  let counts = 0;
  function popLike(e) {
    e.preventDefault();
    
    // Increment Score Metrics
    counts++;
    const label = document.getElementById('like-count');
    label.innerText = counts;

    const container = document.querySelector('.thumb-container');
    const wave = document.querySelector('.shockwave');

    // Trigger Brightness/Warp Visual Pop
    container.classList.remove('pop-impact');
    void container.offsetWidth; 
    container.classList.add('pop-impact');

    // Trigger Ring Blast Wave
    wave.classList.remove('pulse-blast');
    void wave.offsetWidth;
    wave.classList.add('pulse-blast');

    // Trigger Counter Bump
    label.classList.remove('bump');
    void label.offsetWidth;
    label.classList.add('bump');
  }
</script>







<div class="college-badge" style="text-align: center; margin-bottom: 15px;">
  <!-- Profile Image Link -->
  <a href="naveenKumarResume.pdf" target="_blank" title="View Full Resume (PDF)" style="display: inline-block; text-decoration: none; outline: none;">
    <img src="naveenkumar.jpg.jpeg" alt="Naveen Kumar" style="width: 200px; height: 200px; object-fit: cover; border-radius: 50%; border: 2px solid #d4af37; transition: transform 0.3s ease, box-shadow 0.3s ease;" onmouseover="this.style.transform='scale(1.05)'; this.style.boxShadow='0 0 15px rgba(212, 175, 55, 0.6)';" onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='none';">
  </a>

  
  <!-- Integrated PDF Download Action Bar -->
  <div style="margin-top: 12px;">
    <!-- FIXED: Changed inline-inline-flex to inline-flex -->
    <a href="naveenKumarResume.pdf" download="naveenKumarResume.pdf" style="display: inline-flex; align-items: center; justify-content: center; gap: 8px; color: #81C784; text-decoration: none; font-size: 0.9rem; font-weight: 600; padding: 6px 14px; border: 1px solid rgba(129, 199, 132, 0.3); border-radius: 20px; background: rgba(129, 199, 132, 0.05); transition: all 0.3s ease;" onmouseover="this.style.background='rgba(129, 199, 132, 0.15)'; this.style.borderColor='#81C784'; this.style.transform='translateY(-1px)';" onmouseout="this.style.background='rgba(129, 199, 132, 0.05)'; this.style.borderColor='rgba(129, 199, 132, 0.3)'; this.style.transform='translateY(0)';">
      <!-- Inline SVG Graphic representing a PDF file with a clear downward download arrow -->
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" style="display: block;">
        <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
        <polyline points="14 2 14 8 20 8"></polyline>
        <line x1="12" y1="18" x2="12" y2="12"></line>
        <polyline points="9 15 12 18 15 15"></polyline>
      </svg>
      Download Resume
    </a>
  </div>
</div>

  <!-- High Effect Header Section -->
  <header id="about">
    <div class="header-reveal">
      <h1>NaveenKumar B</h1>
      <p>Finance Analyst</p>
      <p class="sub">I am an MBA in Finance and Business Analytics professional blending core financial acumen with a robust data analytics toolkit. Currently driving financial health as a Junior Analyst at ZOLD UDP Foods, I specialize in financial modeling, accounts optimization, and month-end reconciliations. With hands-on mastery over Excel, Power BI, MySQL, and Python, I transform raw corporate data into strategic, actionable business insights. My background spans published research on NBFC capital adequacy alongside practical exposure to manufacturing and supply chain operations. I bridge the gap between finance and technology to eliminate operational inefficiencies and fuel data-backed business growth</p>
    </div>
  </header>

<!-- Tamil Culture & Philosophy Interactive Showcase Module -->
<div class="cultural-motto-card" style="
  margin-top: 45px; 
  padding: 30px; 
  background: linear-gradient(135deg, rgba(253, 251, 247, 0.9) 0%, rgba(245, 240, 230, 0.9) 100%); 
  border-radius: 16px; 
  text-align: center;
  box-shadow: 0 4px 20px rgba(212, 175, 55, 0.08);
  border: 1px solid rgba(212, 175, 55, 0.2);
  position: relative;
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  cursor: default;
" 
onmouseover="this.style.transform='translateY(-6px)'; this.style.boxShadow='0 12px 30px rgba(212, 175, 55, 0.18)'; this.style.borderColor='rgba(212, 175, 55, 0.5)';"
onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 4px 20px rgba(212, 175, 55, 0.08)'; this.style.borderColor='rgba(212, 175, 55, 0.2)';"
>
  <!-- Decorative Background Quote Mark -->
  <div style="position: absolute; top: -20px; right: -10px; font-size: 7rem; color: rgba(212, 175, 55, 0.04); font-family: serif; pointer-events: none; user-select: none;">"</div>
  
  <!-- Icon -->
  <div style="font-size: 2rem; margin-bottom: 12px; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));">✨</div>

  <!-- Tamil Quote -->
  <p style="font-size: 1.6rem; font-weight: 800; color: #2c221e; margin: 0 0 12px 0; font-family: 'Mukta Malar', sans-serif; letter-spacing: 0.5px;">
    "யாதும் ஊரே யாவரும் கேளிர்"
  </p>
  
  <!-- Elegant Divider Line -->
  <div style="width: 50px; height: 2px; background: #d4af37; margin: 0 auto 16px auto; border-radius: 2px;"></div>

  <!-- Meaning -->
  <p style="font-size: 1.1rem; font-style: italic; color: #4a3e39; margin: 0; line-height: 1.7; font-weight: 500;">
    <strong style="color: #d4af37; font-style: normal;">பொருள்:</strong> எல்லா ஊர்களும் நமது ஊர்களே, எல்லா மக்களும் நமது உறவினர்களே.
  </p>
  
  <!-- Poet Credit -->
  <span style="display: block; font-size: 0.85rem; color: #8c766c; margin-top: 15px; font-weight: 600; letter-spacing: 1.5px; text-transform: uppercase;">
    — கணியன் பூங்குன்றனார் (புறநானூறு)
  </span>
</div>

<!-- Education Section -->
<section id="education">
  <h2>Education</h2>
  
  <div class="education-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
    
<!-- Postgraduate Degree -->
    <div class="card" style="display: flex; flex-direction: column; justify-content: space-between;">
      <div>
        <!-- College Visual / Logo Placeholder -->
        <div class="college-badge" style="background: #f4f6f9; padding: 15px; text-align: center; border-radius: 6px; margin-bottom: 15px;">
          <span style="font-size: 2.5rem;">🏛️</span> <!-- Replace this emoji with an <img src="anna-univ-logo.png"> later -->
        </div>
        <h3>Master of Business Administration (MBA)</h3>
        <!-- Added hyperlink to college website -->
        <a href="https://siims.ac.in/" target="_blank" rel="noopener noreferrer" style="text-decoration: none; color: inherit;">
          <h4 style="margin: 0; transition: text-decoration 0.2s;" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'">SIIMS College-Pollachi</h4>
        </a>
        <span class="meta" style="font-size: 0.85rem; color: #777; display: block; margin-bottom: 4px; margin-top: 4px;">Affiliated to Anna University - Chennai </span>
        <span class="meta" style="display: block; margin-bottom: 4px;">2023 - 2025</span>
        <ul class="experience-list" style="margin-top: 12px;">
          <li>Specialization in Financial Management & Data Analytics.</li>
          <li>Deepened expertise in data-driven corporate finance strategy.</li>
        </ul>
      </div>
      <!-- Academic Gift/Highlight Tag -->
      <div class="academic-gift" style="background: #eef9f0; color: #1e7e34; padding: 8px 12px; border-radius: 4px; font-weight: 600; font-size: 0.9rem; margin-top: 15px; display: inline-block; width: max-content;">
        🏆 Academic Merit: 7.8 CGPA
      </div>
    </div> <!-- /card -->
   <!-- Undergraduate Degree -->
    <div class="card" style="display: flex; flex-direction: column; justify-content: space-between;">
      <div>
        <!-- College Visual / Logo Placeholder -->
        <div class="college-badge" style="background: #f4f6f9; padding: 15px; text-align: center; border-radius: 6px; margin-bottom: 15px;">
          <span style="font-size: 2.5rem;">🎓</span> <!-- Replace this emoji with an <img src="ngm-logo.png"> later -->
        </div>
        <h3>Bachelor of Commerce (B.Com)</h3>
        <!-- Added hyperlink to NGM college website -->
        <a href="https://www.ngmc.org/" target="_blank" rel="noopener noreferrer" style="text-decoration: none; color: inherit;">
          <h4 style="margin: 0; transition: text-decoration 0.2s;" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'">NGM College - Pollachi</h4>
        </a>
        <span class="meta" style="font-size: 0.85rem; color: #777; display: block; margin-bottom: 4px; margin-top: 4px;">Affiliated to Bharathiar University - Coimbatore </span>
        <span class="meta" style="display: block; margin-bottom: 4px;">2020 - 2023</span>
        <ul class="experience-list" style="margin-top: 12px;">
          <li>Built a strong foundation in accounting, corporate laws, and business statistics.</li>
          <li>Active participation in commerce and financial literacy forums.</li>
        </ul>
      </div>
      <!-- Academic Gift/Highlight Tag -->
      <div class="academic-gift" style="background: #eef9f0; color: #1e7e34; padding: 8px 12px; border-radius: 4px; font-weight: 600; font-size: 0.9rem; margin-top: 15px; display: inline-block; width: max-content;">
        🏆 Academic Merit: 7.5 CGPA
      </div>
    </div> <!-- /card -->

  </div> <!-- /education-grid -->
</section> <!-- /education -->
    
<!-- Corporate Exposure / Experience Section -->
<section id="experience">
  <h2>Corporate Exposure</h2>
  
  <div class="grid">
    <div class="card">
      <h3 style="display: inline-flex; align-items: center; gap: 12px; font-family: sans-serif; color: #ffffff; margin: 0;">
        Junior Analyst 
        <span style="font-size: 0.75rem; font-weight: 700; color: #d4af37; background: rgba(212, 175, 55, 0.08); padding: 4px 10px; border-radius: 6px; border: 1px solid rgba(212, 175, 55, 0.25); letter-spacing: 0.5px;">
          ✨ ANALYST // 2026
        </span>
      </h3>
      
      <span class="meta" style="display: block; margin-top: 4px;">August 2025 - Present</span>
      <h4 style="margin-top: 8px; margin-bottom: 12px;">ZOLD UDP FOODS PRIVATE LIMITED, Udumalpet</h4>
      
      <ul class="experience-list">
        <li>Assisted in preparing and maintaining accurate financial records and reports.</li>
        <li>Facilitated monthly closing processes, including reconciliations and posting journal entries.</li>
        <li>Managed accounts payable and receivable to ensure timely processing and compliance.</li>
        <li>Collaborated with senior accountants to improve efficiency and reduce reporting errors.</li>
      </ul>
      
      <!-- Clean Text Link Container matching the Projects template design -->
      <div class="article-links-container" style="margin-top: 15px;">
        <a href="https://www.zoldgroup.com/" target="_blank" class="text-link-pdf primary-link">
          Company Website
        </a>
        <span class="link-separator">|</span>
        <a href="https://maps.app.goo.gl/QRWXGr5fm6w1y4nf6" target="_blank" class="text-link-pdf secondary-link">
          Company Location
        </a>
      </div>
      
    </div> <!-- /card -->
  </div> <!-- /grid -->
</section> <!-- /experience -->

  <section id="projects">
  <h2>Research & Projects</h2>
  <div class="grid">
    <div class="card">
      <h3>NBFC Financial Performance Analysis</h3>
      <span class="meta">Postgraduate Project (Published - May 2025)</span>
      
      <p>
        Published a research paper titled "Analysis of Capital Adequacy of Leading 5 Non-Banking Financial Companies in India" 
        in the EPRA International Journal of Economics, Business and Management Studies (EBMS), Vol. 12, Issue 5, May 2025.
      </p>
      
      <div class="article-links-container">
        <a href="NaveenKumar_Published_Article.pdf" target="_blank" class="text-link-pdf primary-link">
          View Published Article (PDF)
        </a>
        <span class="link-separator">|</span>
        <a href="naveenkumar_article_certificate.pdf" target="_blank" class="text-link-pdf secondary-link">
          View Published Article Certificate (PDF)
        </a>
      </div>
    </div> </div> </section>


<!-- Skills & Certifications Section -->
    <section id="skills">
      <h2>Technical Skills & Credentials</h2>
      <div class="skills-grid">
        <div class="skills-box">
          <h3>Analytical & Technical Skills</h3>
          <ul>
            <li>Advanced Excel – Pivot Tables, Macros, Data Visualization</li>
            <li>MySQL – Database queries, joins, stored procedures</li>
            <li>Power BI – Dashboard creation, data modeling</li>
            <li>Python – Data analysis, automation, visualization (Pandas)</li>
            <li>Business Analysis – Financial modeling, process improvement, strategic insights</li>
          </ul>
        </div>
        <div class="skills-box">
          <h3>Accounting & Taxation Skills</h3>
          <ul>
            <li>GST compliance, filing, and reconciliation</li>
            <li>Tally Prime for accounting and financial management</li>
            <li>TDS (Tax Deducted at Source) calculation and reporting</li>
            <li>Income Tax preparation and return filing</li>
            <li>VAT accounting and compliance procedures</li>
          </ul>
        </div>
        <div class="skills-box">
          <h3>Professional Certifications</h3>
          <ul>
            <li>Human Resources Management (Swayam-NPTEL) – Expanded knowledge of management concepts and HR practices</li>
            <li>AI in Marketing (Swayam-NPTEL) – Strengthened understanding of AI’s role in modern marketing strategies</li>
          </ul>
        </div>
      </div>
    </section>

<!-- My Professional Work -->
<section id="my professional work">
    <div class="skills-box">
      <h3>My Professional Work</h3>
      <ul>
        <li>Digital Marketing – Strategic content creation, professional video editing, and impact-driven poster design.</li>
        <li>Financial Analysis – Comprehensive financial statement evaluation and strategic portfolio management.</li>
        <li>Custom Solutions – Dedicated consulting and tailored support to solve your unique business challenges.</li>
        <li>Finance Filling – GST, VAT, TDS, TCS, Income Tax and other Filling and Queries.</li>
      </ul>
    </div>
</section>

  <!-- Vision Statement Showcase Module -->
<div class="vision-container" style="
  margin-top: 45px; 
  padding: 30px; 
  background: linear-gradient(135deg, rgba(253, 251, 247, 0.9) 0%, rgba(245, 240, 230, 0.9) 100%); 
  border-radius: 16px; 
  text-align: center;
  box-shadow: 0 4px 20px rgba(212, 175, 55, 0.08);
  border: 1px solid rgba(212, 175, 55, 0.2);
  position: relative;
  overflow: hidden;
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  cursor: default;
" 
onmouseover="this.style.transform='translateY(-6px)'; this.style.boxShadow='0 12px 30px rgba(212, 175, 55, 0.18)'; this.style.borderColor='rgba(212, 175, 55, 0.5)';"
onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 4px 20px rgba(212, 175, 55, 0.08)'; this.style.borderColor='rgba(212, 175, 55, 0.2)';"
>
  <!-- Decorative Background Quote Mark -->
  <div style="position: absolute; top: -20px; right: -10px; font-size: 7rem; color: rgba(212, 175, 55, 0.04); font-family: serif; pointer-events: none; user-select: none;">"</div>
  
  <!-- Icon -->
  <div style="font-size: 2rem; margin-bottom: 12px; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));">💡</div>

  <!-- Label / Tagline -->
  <span class="vision-label" style="display: block; font-size: 0.85rem; color: #8c766c; margin-bottom: 12px; font-weight: 700; letter-spacing: 1.5px; text-transform: uppercase;">
    Our Vision
  </span>
  
  <!-- Elegant Divider Line -->
  <div style="width: 50px; height: 2px; background: #d4af37; margin: 0 auto 16px auto; border-radius: 2px;"></div>

  <!-- Main Core Quote -->
  <blockquote class="vision-text" style="font-size: 1.45rem; font-style: italic; font-weight: 600; color: #2c221e; margin: 0; padding: 0 10px; line-height: 1.6; font-family: -apple-system, BlinkMacSystemFont, sans-serif;">
    "A flexible, innovative approach to problem-solving that uses limited resources to get things done"
  </blockquote>
</div>

    <!-- Contact Section -->
    <section id="contact">
      <h2>Get In Touch</h2>
      <form action="https://formsubmit.co/naveenbalakrishnan146@gmail.com" method="POST">
        <input type="hidden" name="_captcha" value="false">
        
        <input type="text" name="name" placeholder="Your Name" required>
        <input type="email" name="email" placeholder="Your Email" required>
        <textarea name="message" placeholder="Your Message" required></textarea>
        
        <button type="su  bmit">Send Message</button>
      </form>
    </section>

  <!-- High Effect Footer Section -->
  <footer>
    <div class="footer-content">
      <p>&copy;💙2026 NaveenKumar B💙</p>
      <p>📍Thungavi- Udumalpet - Coimbatore📍</p>
      <p>🌐My personal design🌐</p>
      <p>🎨Portfolio Website🎨</p>
      <div class="footer-links">
        <a href="https://www.linkedin.com/in/naveenkumar-b-3713311ab" target="_blank">LinkedIn</a>
        <a href="https://github.com/naveen12345naveen" target="_blank">GitHub</a>
        <a href="mailto:naveenbalakrishnan146@gmail.com">Email</a>
        <a href="https://www.instagram.com/naveenkumar.b.nkb?igsh=MXNhYjFycG9tN2lnYw==">Instagram</a>
        <a href="tel:+916369311629">Mobile</a>
      </div>
    </div>
  </footer>
  
<!-- Stylish Button Link to Learn with Me Page -->
<div style="text-align: center; margin-top: 30px; margin-bottom: 20px;">
    <a href="page2.html" style="
        display: inline-block;
        padding: 15px 30px;
        font-size: 18px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-weight: bold;
        color: white;
        background: linear-gradient(45deg, #ff416c, #ff4b2b);
        border-radius: 50px;
        text-decoration: none;
        box-shadow: 0 4px 15px rgba(255, 75, 43, 0.4);
        transition: transform 0.2s ease, box-shadow 0.2s ease;
    " onmouseover="this.style.transform='scale(1.05)'; this.style.boxShadow='0 6px 20px rgba(255, 75, 43, 0.6)';" 
      onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='0 4px 15px rgba(255, 75, 43, 0.4)';">
        🎁 Learn with me
    </a>
</div>


