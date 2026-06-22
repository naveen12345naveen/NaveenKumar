
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







<meta name="viewport" content="width=1200, initial-scale=1.0">

<audio id="terminal-audio" src="music.mp3" loop preload="auto"></audio>

<div id="desktop-lock-overlay" class="desktop-enforcement-screen" style="display: flex; opacity: 1;">
  
  <div class="ticker-backdrop-matrix">
    <div class="ticker-lane">ANALYTICS_CORE [ONLINE] &nbsp;&nbsp; NIFTY50 +24,000 &nbsp;&nbsp; SENSEX +77,094 &nbsp;&nbsp; NASDAQ +26,000 &nbsp;&nbsp; USD/INR 94.05 &nbsp;&nbsp; DATA_STREAM_A [ENGAGED]</div>
    <div class="ticker-lane reverse">RISK_MATRIX [ACTIVE] &nbsp;&nbsp; BTC/USD +4.82% &nbsp;&nbsp; GOLD/INR -0.15% &nbsp;&nbsp; ALPHA_ENGINE_CONNECTED &nbsp;&nbsp; MARGIN_SAFE</div>
  </div>

  <div class="hud-scanner-grid"></div>
  <div class="hud-corner-bracket tl"></div>
  <div class="hud-corner-bracket tr"></div>
  <div class="hud-corner-bracket bl"></div>
  <div class="hud-corner-bracket br"></div>
  
  <div class="hud-central-matrix-box">
    <div id="gate-ring" class="hud-pulse-ring-vfx">
      <div class="outer-data-ring"></div>
      <div class="middle-data-ring"></div>
      <div class="inner-data-ring"></div>
      
      <div class="radar-wave"></div>
      <div class="radar-wave delay-1"></div>
      
      <div id="gate-icon-container" class="inner-core-node">
        <div class="glow-particle-core"></div>
        <div id="gate-icon" class="vector-symbol">💼</div>
      </div>
    </div>
    
    <div id="gate-prompt" class="interaction-prompt">INITIALIZING TERMINAL</div>
    <div id="gate-subtitle" class="interaction-subtitle">CONNECTING SECURE RISK MATRIX MODULES AND COMPILING ASSET VISUALIZATION TELEMETRY...</div>
    
    <div class="hud-progress-track">
      <div id="gate-progress" class="hud-progress-fill"></div>
    </div>
  </div>
</div>

<style>
  :root {
    --finance-emerald: #00ffaa;
    --finance-gold: #ffc83d;
    --finance-alert: #ff4b2b;
    --dark-void: #090a0f;
    --hud-glow: rgba(0, 255, 170, 0.15);
  }

  /* SUPREME LAYER IMMERSIVE CONTAINER */
  .desktop-enforcement-screen {
    position: fixed;
    inset: 0;
    width: 100vw;
    height: 100vh;
    background: radial-gradient(circle at center, #111420 0%, var(--dark-void) 100%);
    z-index: 9999999;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    user-select: none;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    transition: opacity 0.6s cubic-bezier(0.25, 1, 0.5, 1);
  }

  /* BACKGROUND GRAPHICS / DATA TICKERS */
  .ticker-backdrop-matrix {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 30px;
    opacity: 0.03;
    transform: rotate(-8deg) scale(1.3);
    pointer-events: none;
    font-family: monospace;
    font-size: 2rem;
    font-weight: bold;
    color: var(--finance-emerald);
    white-space: nowrap;
  }

  .ticker-lane { animation: scrollLeft 35s linear infinite; }
  .ticker-lane.reverse { animation: scrollRight 40s linear infinite; color: var(--finance-gold); }

  .hud-scanner-grid {
    position: absolute;
    inset: 0;
    background-image: 
      linear-gradient(rgba(0, 255, 170, 0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0, 255, 170, 0.02) 1px, transparent 1px);
    background-size: 50px 50px;
    background-position: center;
    pointer-events: none;
  }

  /* Minimal Corner Framing Elements */
  .hud-corner-bracket {
    position: absolute;
    width: 24px;
    height: 24px;
    border: 2px solid var(--finance-emerald);
    pointer-events: none;
    opacity: 0.4;
    transition: border-color 0.4s ease;
  }
  .tl { top: 40px; left: 40px; border-right: 0; border-bottom: 0; }
  .tr { top: 40px; right: 40px; border-left: 0; border-bottom: 0; }
  .bl { bottom: 40px; left: 40px; border-right: 0; border-top: 0; }
  .br { bottom: 40px; right: 40px; border-left: 0; border-top: 0; }

  .hud-central-matrix-box {
    text-align: center;
    z-index: 10;
    max-width: 520px;
    padding: 20px;
    box-sizing: border-box;
  }

  /* GEOMETRIC VISUALIZER INTERFACE SYSTEM */
  .hud-pulse-ring-vfx {
    position: relative;
    width: 140px;
    height: 140px;
    margin: 0 auto 35px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .outer-data-ring {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 2px dashed rgba(0, 255, 170, 0.08);
    border-top: 2px solid var(--finance-emerald);
    border-bottom: 2px solid var(--finance-emerald);
    border-radius: 50%;
    animation: rotateClockwise 3s linear infinite;
    transition: border-color 0.4s ease;
  }

  .middle-data-ring {
    position: absolute;
    width: 84%;
    height: 84%;
    border: 1px dotted rgba(255, 200, 61, 0.15);
    border-left: 2px solid var(--finance-gold);
    border-radius: 50%;
    animation: rotateCounterClockwise 1.2s linear infinite;
    transition: border-color 0.4s ease;
  }

  .inner-data-ring {
    position: absolute;
    width: 68%;
    height: 68%;
    border: 2px solid rgba(0, 255, 170, 0.04);
    border-right: 2px dashed var(--finance-emerald);
    border-radius: 50%;
    animation: rotateClockwise 1.8s linear infinite;
    transition: border-color 0.4s ease;
  }

  /* RADAR WAVE PROPAGATION */
  .radar-wave {
    position: absolute;
    width: 50%;
    height: 50%;
    border: 1px solid var(--finance-emerald);
    border-radius: 50%;
    opacity: 0;
    pointer-events: none;
    animation: radarPulse 2s cubic-bezier(0.1, 0.8, 0.3, 1) infinite;
    transition: border-color 0.4s ease;
  }
  .radar-wave.delay-1 { animation-delay: 1s; }

  /* COMPUTING CORE GRAPHIC */
  .inner-core-node {
    position: relative;
    width: 52px;
    height: 52px;
    background: rgba(9, 10, 15, 0.9);
    border: 2px solid var(--finance-emerald);
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
    box-shadow: 0 0 15px rgba(0, 255, 170, 0.2);
    transition: all 0.4s ease;
  }

  .glow-particle-core {
    position: absolute;
    width: 100%;
    height: 100%;
    background: var(--finance-emerald);
    border-radius: 50%;
    filter: blur(8px);
    opacity: 0.15;
    animation: coreBreathe 2s ease-in-out infinite alternate;
    transition: background 0.4s ease;
  }

  .vector-symbol {
    font-size: 20px;
    z-index: 3;
    transition: transform 0.3s ease;
  }

  /* TYPOGRAPHY */
  .interaction-prompt {
    font-size: 1.5rem;
    font-weight: 800;
    color: #ffffff;
    letter-spacing: 4px;
    margin-bottom: 12px;
    text-transform: uppercase;
    text-shadow: 0 0 20px var(--hud-glow);
    transition: text-shadow 0.4s ease;
  }

  .interaction-subtitle {
    font-family: monospace;
    font-size: 0.85rem;
    color: #8fa099;
    letter-spacing: 1.2px;
    line-height: 1.6;
    margin-bottom: 35px;
  }

  /* Precision Data Fill Bar */
  .hud-progress-track {
    width: 200px;
    height: 3px;
    background: rgba(255, 255, 255, 0.04);
    border-radius: 6px;
    margin: 0 auto;
    overflow: hidden;
    position: relative;
    border: 1px solid rgba(0, 255, 170, 0.08);
  }

  .hud-progress-fill {
    position: absolute;
    top: 0; left: 0; bottom: 0;
    width: 0%; 
    background: linear-gradient(90deg, var(--finance-emerald), var(--finance-gold));
    box-shadow: 0 0 12px var(--finance-emerald);
    transition: width 8s linear;
  }

  /* ANIMATION MATRIX */
  @keyframes rotateClockwise { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
  @keyframes rotateCounterClockwise { 0% { transform: rotate(360deg); } 100% { transform: rotate(0deg); } }
  @keyframes scrollLeft { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
  @keyframes scrollRight { 0% { transform: translateX(-50%); } 100% { transform: translateX(0); } }
  @keyframes coreBreathe { 0% { opacity: 0.1; transform: scale(0.9); } 100% { opacity: 0.3; transform: scale(1.1); } }
  @keyframes radarPulse {
    0% { transform: scale(1); opacity: 0.5; }
    100% { transform: scale(2.6); opacity: 0; }
  }
</style>

<script>
  // AUTOMATED MAIN SITE LOADING CONTROLLER ENGINE WITH AUDIO INTERACTION BACKUP
  function initWebsiteGateway() {
    const lockOverlay = document.getElementById('desktop-lock-overlay');
    const gateIcon = document.getElementById('gate-icon');
    const gateIconContainer = document.getElementById('gate-icon-container');
    const glowParticle = document.querySelector('.glow-particle-core');
    const gatePrompt = document.getElementById('gate-prompt');
    const gateSubtitle = document.getElementById('gate-subtitle');
    const gateProgress = document.getElementById('gate-progress');
    const audioEngine = document.getElementById('terminal-audio');
    
    const outerRing = document.querySelector('.outer-data-ring');
    const middleRing = document.querySelector('.middle-data-ring');
    const innerRing = document.querySelector('.inner-data-ring');
    const waves = document.querySelectorAll('.radar-wave');
    const brackets = document.querySelectorAll('.hud-corner-bracket');
    
    // Check hardware layout matrices
    const isMobileDevice = /Mobi|Android|iPhone|iPad|iPod|Windows Phone/i.test(navigator.userAgent);
    const hasDesktopWidth = window.innerWidth >= 1024;

    if (isMobileDevice && !hasDesktopWidth) {
      // 📉 REJECTION HANDLER: Halt execution if on phone without desktop site checked
      gateIcon.textContent = "❌";
      gateIconContainer.style.borderColor = "var(--finance-alert)";
      gateIconContainer.style.boxShadow = "0 0 15px rgba(255, 75, 43, 0.4)";
      glowParticle.style.background = "var(--finance-alert)";
      
      gatePrompt.textContent = "ANALYST DESK REQUIRED";
      gatePrompt.style.textShadow = "0 0 20px rgba(255, 75, 43, 0.4)";
      gateSubtitle.innerHTML = "CRITICAL DESK AUTHENTICATION ERROR.<br><br>COMPILING HIGH-DENSITY QUANTUM DATA ASSETS REQUIRES LARGER ENVIRONMENT SCREENSPACE VARIABLES.<br><br>PLEASE INITIALIZE YOUR MOBILE BROWSER OPTIONS SYSTEM AND VERIFY <strong style='color:var(--finance-gold);'>'REQUEST DESKTOP SITE'</strong>.";
      
      outerRing.style.borderColor = "var(--finance-alert)";
      middleRing.style.borderColor = "transparent";
      innerRing.style.borderColor = "transparent";
      outerRing.style.animationPlayState = 'paused';
      middleRing.style.animationPlayState = 'paused';
      innerRing.style.animationPlayState = 'paused';
      
      waves.forEach(wave => wave.style.borderColor = "var(--finance-alert)");
      brackets.forEach(bracket => bracket.style.borderColor = "var(--finance-alert)");
      
      gateProgress.style.width = "100%";
      gateProgress.style.background = "var(--finance-alert)";
      gateProgress.style.boxShadow = "0 0 12px var(--finance-alert)";
    } else {
      // Try initialization of audio immediately (works if user previously interacted or has sound allowed)
      audioEngine.play().catch(() => {
        // Fallback for strict browser engines: plays on the first user interaction event
        const startAudioOnInteraction = () => {
          audioEngine.play().catch(() => {});
          document.removeEventListener('click', startAudioOnInteraction);
          document.removeEventListener('touchstart', startAudioOnInteraction);
        };
        document.addEventListener('click', startAudioOnInteraction);
        document.addEventListener('touchstart', startAudioOnInteraction);
      });

      // 📊 AUTHORIZED ACCESS SYSTEM: Run the loader and reveal content
      setTimeout(() => { gateProgress.style.width = "100%"; }, 50);

      // 8-SECOND SYSTEM SCANNING RUNTIME PIPELINE
      setTimeout(() => {
        gateIcon.textContent = "📈";
        gatePrompt.textContent = "ACCESS GRANTED";
        gateSubtitle.textContent = "Terminal compiled successfully. Loading environment mainframe modules...";
        
        // Graceful fade transition block
        setTimeout(() => {
          lockOverlay.style.opacity = '0';
          setTimeout(() => {
            lockOverlay.style.display = 'none'; // Unlocks total visual site access to the user
          }, 600);
        }, 800);
      }, 8000); // 8 Seconds hold duration
    }
  }

  // Auto-run the verification pipeline the moment the document object model maps into memory
  window.addEventListener('DOMContentLoaded', initWebsiteGateway);
</script>







<!-- Navigation Bar -->
<nav style="
    display: flex; 
    justify-content: center; 
    align-items: center; 
    flex-wrap: nowrap; /* Forces all elements onto a strict single line */
    overflow-x: auto;  /* Allows scrolling on small mobile screens without breaking layout */
    white-space: nowrap; 
    gap: 5px; /* Set exactly to 5px space between names */
    padding: 12px 10px; 
    background: #121214; 
    position: sticky; 
    top: 0; 
    z-index: 1000;
    
    /* Single Continuous Warm Light VFX Underline */
    border-bottom: 2px solid #ff9f43; 
    box-shadow: 0 4px 25px 0px rgba(255, 140, 0, 0.45), 0 2px 10px 0px rgba(230, 140, 10, 0.25);
">
  <a href="#about" style="
      color: #ff9f43; /* Native warm amber color tint */
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); /* Always glowing text effect */
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">About</a>
  
  <a href="#education" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">Education Section</a>
  
  <a href="#experience" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">Experience</a>
  
  <a href="#projects" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">Projects</a>
  
  <a href="#skills" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">Skills</a>
  
  <a href="#my professional work" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">My Professional Work</a>
  
  <a href="#contact" style="
      color: #ff9f43; 
      text-decoration: none; 
      font-weight: 600; 
      font-size: 0.9rem; 
      padding: 6px 10px; 
      border-radius: 4px; 
      text-shadow: 0 0 8px rgba(255, 159, 67, 0.7); 
      transition: all 0.25s ease-in-out;
  " 
  onmouseover="this.style.color='#ffffff'; this.style.textShadow='0 0 12px #ff9f43, 0 0 20px #ff5a00'; this.style.background='rgba(255, 140, 0, 0.08)';" 
  onmouseout="this.style.color='#ff9f43'; this.style.textShadow='0 0 8px rgba(255, 159, 67, 0.7)'; this.style.background='transparent';">Contact</a>
</nav>

  
<a id="scroll-left-pop" class="left-popup-box">
  <img src="naveenkumar.jpg.jpeg" alt="Pop-up Image">
</a>

<a id="scroll-right-pop" class="right-popup-box">
  <img src="Indiaflag.jpg" alt="Pop-up Image">
</a>

<style>
  /* ==================== LEFT POP-UP LUXURY MATRIX STYLES ==================== */
  .left-popup-box {
    position: fixed;
    bottom: 80px;          
    left: -140px; /* Kept completely off-screen initially for slide-in effect */       
    width: 100px;
    height: 100px;
    border-radius: 50%;
    z-index: 99999;        
    display: block; 
    box-sizing: border-box;
    padding: 3px; /* Creates spacing for internal glow alignment */
    
    /* Obsidian Wood Deep Core Layer & Amber Laser Wireframe Rim */
    background: radial-gradient(circle at center, #221a16 0%, #110c0a 100%);
    border: 2px solid rgba(255, 140, 0, 0.45);
    box-shadow: 
        0 0 20px 2px rgba(255, 90, 0, 0.3), 
        0 10px 30px rgba(0, 0, 0, 0.6),
        inset 0 0 10px rgba(255, 140, 0, 0.2);
    
    /* Premium smooth bounce cubic transition */
    transition: left 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275), transform 0.3s ease;
  }

  .left-popup-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
  }

  /* UNIQUE INTERACTIVE LAYOUT SYMBOL: Orbiting Tech Outer Reticle Wire */
  .left-popup-box::before {
    content: '';
    position: absolute;
    top: -6px; left: -6px; right: -6px; bottom: -6px;
    border-radius: 50%;
    border: 1px dashed rgba(255, 159, 67, 0.4);
    pointer-events: none;
    animation: spinSymbolWire 20s linear infinite;
  }

  .left-popup-box.slide-in { 
    left: 25px; 
  }
  
  .left-popup-box:hover {
    transform: scale(1.08);
    border-color: rgba(255, 159, 67, 0.85);
    box-shadow: 0 0 30px 6px rgba(255, 90, 0, 0.5), 0 12px 35px rgba(0, 0, 0, 0.7);
  }

  /* ==================== RIGHT POP-UP LUXURY MATRIX STYLES ==================== */
  .right-popup-box {
    position: fixed;
    top: 80px;            
    right: -140px; /* Kept completely off-screen initially for slide-in effect */       
    width: 100px;
    height: 100px;
    border-radius: 50%;
    z-index: 99999;        
    display: block; 
    box-sizing: border-box;
    padding: 3px;
    
    /* Obsidian Wood Deep Core Layer & Amber Laser Wireframe Rim */
    background: radial-gradient(circle at center, #221a16 0%, #110c0a 100%);
    border: 2px solid rgba(255, 140, 0, 0.45);
    box-shadow: 
        0 0 20px 2px rgba(255, 90, 0, 0.3), 
        0 10px 30px rgba(0, 0, 0, 0.6),
        inset 0 0 10px rgba(255, 140, 0, 0.2);
        
    transition: right 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275), transform 0.3s ease;
  }

  .right-popup-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 50%;
  }

  /* UNIQUE INTERACTIVE LAYOUT SYMBOL: Top Facing Compass Crosshair Node Anchor */
  .right-popup-box::after {
    content: '✦';
    position: absolute;
    top: -12px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 10px;
    color: #ff9f43;
    text-shadow: 0 0 4px #ff9f43;
  }

  .right-popup-box.slide-in { 
    right: 25px; 
  }
  
  .right-popup-box:hover {
    transform: scale(1.08);
    border-color: rgba(255, 159, 67, 0.85);
    box-shadow: 0 0 30px 6px rgba(255, 90, 0, 0.5), 0 12px 35px rgba(0, 0, 0, 0.7);
  }

  /* Structural Animation Rotation Keyframe Loop */
  @keyframes spinSymbolWire {
    100% { transform: rotate(360deg); }
  }
</style>

<script>
  // Clean, consolidated event handling loop
  window.addEventListener('scroll', function() {
    const leftPop = document.getElementById('scroll-left-pop');
    const rightPop = document.getElementById('scroll-right-pop');
    const scrollActivationLine = 200;
    
    if (window.scrollY > scrollActivationLine) {
      if (leftPop) leftPop.classList.add('slide-in');
      if (rightPop) rightPop.classList.add('slide-in');
    } else {
      if (leftPop) leftPop.classList.remove('slide-in');
      if (rightPop) rightPop.classList.remove('slide-in');
    }
  });
</script>

<div class="college-badge" style="text-align: center; margin-bottom: 25px;">
  <!-- Profile Image Link with Warm Glow -->
  <a href="naveenKumarResume.pdf" target="_blank" title="View Full Resume (PDF)" style="display: inline-block; text-decoration: none; outline: none;">
    <img src="naveenkumar.jpg.jpeg" alt="Naveen Kumar" style="
        width: 200px; 
        height: 200px; 
        object-fit: cover; 
        border-radius: 50%; 
        border: 2px solid rgba(255, 140, 0, 0.4); 
        box-shadow: 
            0 0 20px 2px rgba(255, 90, 0, 0.25),   /* Vibrant amber warmth */
            0 0 40px 5px rgba(230, 140, 10, 0.15);  /* Golden outer spread */
        transition: transform 0.4s ease-in-out, box-shadow 0.4s ease-in-out;
    " 
    onmouseover="this.style.transform='scale(1.05)'; this.style.boxShadow='0 0 30px 5px rgba(255, 90, 0, 0.45), 0 0 55px 12px rgba(230, 140, 10, 0.25)';" 
    onmouseout="this.style.transform='scale(1)'; this.style.boxShadow='0 0 20px 2px rgba(255, 90, 0, 0.25), 0 0 40px 5px rgba(230, 140, 10, 0.15)';" />
  </a>

  <!-- Integrated PDF Download Action Bar with Amber Glow Accent -->
  <div style="margin-top: 18px;">
    <a href="naveenKumarResume.pdf" download="naveenKumarResume.pdf" style="
        display: inline-flex; 
        align-items: center; 
        justify-content: center; 
        gap: 8px; 
        color: #ffb774; /* Matching theme orange/amber text */
        text-decoration: none; 
        font-size: 0.9rem; 
        font-weight: 600; 
        padding: 8px 18px; 
        border: 1px solid rgba(255, 140, 0, 0.3); 
        border-radius: 20px; 
        background: rgba(255, 140, 0, 0.05); 
        box-shadow: 0 0 15px rgba(255, 90, 0, 0.1);
        transition: all 0.3s ease-in-out;
    " 
    onmouseover="this.style.background='rgba(255, 140, 0, 0.15)'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 20px rgba(255, 159, 67, 0.35)'; this.style.transform='translateY(-1px)';" 
    onmouseout="this.style.background='rgba(255, 140, 0, 0.05)'; this.style.borderColor='rgba(255, 140, 0, 0.3)'; this.style.boxShadow='0 0 15px rgba(255, 90, 0, 0.1)'; this.style.transform='translateY(0)';" >
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

<!-- Header Section with text highlights and shimmer base alignment -->
<header id="about" class="vfx-header" style="text-align: center; max-width: 750px; margin: 0 auto; padding: 20px; color: #f3f4f6;">
  <div class="header-reveal">
    <h1 class="vfx-word-shimmer" style="margin-top: 0; margin-bottom: 5px; font-size: 2.8rem; color: #ffffff; letter-spacing: 0.5px; filter: drop-shadow(0 0 10px rgba(255,159,67,0.2));">NaveenKumar B</h1>
    <p class="title-role" style="font-size: 1.3rem; font-weight: 600; color: #ff9f43; margin-top: 0; margin-bottom: 20px; letter-spacing: 1px; text-transform: uppercase;">Finance Analyst</p>
    <p class="sub" style="line-height: 1.7; color: #e0e0e6; font-size: 1.05rem; text-align: justify; margin-bottom: 0;">
      With an MBA blending Finance and Business Analytics, my career is built on a simple premise: financial data is only as good as the actionable insights you can extract from it. Currently, at ZOLD UDP Foods, I engineer the financial models, accounts optimization frameworks, and month-end reconciliations that protect and improve our bottom line. My background isn't just theoretical—it’s anchored in manufacturing operations, supply chain dynamics, and published research on NBFC capital adequacy. Armed with <strong style="color: #ffb774;">Excel, Power BI, MySQL, and Python</strong>, I dismantle operational inefficiencies and build the data infrastructure modern businesses need to scale intelligently.
    </p>
  </div>
</header>
<style>
  /* 1. Ambient 4-Side Edge Glow Container */
  .vfx-header {
    position: relative;
    background: #0f1115; /* Dark premium background so the warm glow breaks perfectly */
    padding: 4rem 2rem;
    border-radius: 16px;
    text-align: center;
    
    /* 4-Side Edge Glow: Combines box shadows to project an even ambient border light on all sides */
    box-shadow: 0 0 25px 2px rgba(212, 175, 55, 0.15),
                0 0 50px 5px rgba(212, 175, 55, 0.08),
                inset 0 0 30px rgba(0, 0, 0, 0.6);
    
    /* Subtle border accent */
    border: 1px solid rgba(212, 175, 55, 0.18);
    transition: box-shadow 0.5s ease, border-color 0.5s ease;
  }

  /* Interactive effect: Header intensifies its 4-side glow when hovered anywhere */
  .vfx-header:hover {
    border-color: rgba(212, 175, 55, 0.35);
    box-shadow: 0 0 35px 5px rgba(212, 175, 55, 0.25),
                0 0 70px 10px rgba(212, 175, 55, 0.12),
                inset 0 0 30px rgba(0, 0, 0, 0.6);
  }

  .header-reveal {
    max-width: 800px;
    margin: 0 auto;
  }

  /* 2. VFX Word Shimmer Effect (Name) */
  .vfx-word-shimmer {
    font-size: 3rem;
    font-weight: 800;
    letter-spacing: 1.5px;
    margin-bottom: 0.5rem;
    
    /* Creates a golden metallic moving gradient shine through the words */
    background: linear-gradient(
      90deg, 
      #ffffff 0%, 
      #ffeaa7 25%, 
      #d4af37 50%, 
      #ffeaa7 75%, 
      #ffffff 100%
    );
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    
    /* Hardware accelerated smooth animation */
    animation: metallicShine 4s linear infinite;
    filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.5));
  }

  @keyframes metallicShine {
    0% { background-position: 0% center; }
    100% { background-position: 200% center; }
  }

  /* 3. VFX Subtitle/Role Glow Animation */
  .title-role {
    font-size: 1.4rem;
    color: #d4af37;
    font-weight: 600;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 2px;
    
    /* Atmospheric text glow */
    text-shadow: 0 0 8px rgba(212, 175, 55, 0.4);
    animation: breathingGlow 3s ease-in-out infinite alternate;
  }

  @keyframes breathingGlow {
    0% { text-shadow: 0 0 6px rgba(212, 175, 55, 0.3); transform: scale(1); }
    100% { text-shadow: 0 0 15px rgba(212, 175, 55, 0.7); transform: scale(1.01); }
  }

  /* Description paragraph settings */
  .sub {
    font-size: 1.05rem;
    color: #b0b5c1;
    line-height: 1.7;
    text-align: justify;
    transition: color 0.3s ease;
  }

  /* Highlights paragraph dynamically when interacting with the dashboard header */
  .vfx-header:hover .sub {
    color: #e2e5ec;
  }
</style>

<!-- Tamil Culture & Philosophy Interactive Showcase Module -->
<div class="cultural-motto-card" style="
  margin-top: 45px; 
  padding: 35px 30px; 
  background: radial-gradient(circle at center, #221a16 0%, #110c0a 100%); /* Deep luxurious dark wood aesthetic */
  border-radius: 16px; 
  text-align: center;
  position: relative;
  overflow: hidden;
  box-sizing: border-box;
  cursor: default;
  
  /* Precision Structural Border & Warm Light Burst Glow */
  border: 1px solid rgba(255, 140, 0, 0.3);
  box-shadow: 
      0 0 30px 2px rgba(255, 90, 0, 0.2),       
      0 10px 40px -10px rgba(0, 0, 0, 0.7),      
      inset 0 0 20px rgba(255, 100, 0, 0.05);    
      
  transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
" 
onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 0 45px 6px rgba(255, 90, 0, 0.35), 0 15px 50px -5px rgba(0, 0, 0, 0.85), inset 0 0 25px rgba(255, 100, 0, 0.1)'; this.style.borderColor='rgba(255, 159, 67, 0.6)';"
onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 0 30px 2px rgba(255, 90, 0, 0.2), 0 10px 40px -10px rgba(0, 0, 0, 0.7), inset 0 0 20px rgba(255, 100, 0, 0.05)'; this.style.borderColor='rgba(255, 140, 0, 0.3)';" >

  <!-- Decorative Custom Warm Light VFX Corner Accents -->
  <div style="position: absolute; top: 0; left: 0; width: 60px; height: 60px; border-top: 2px solid #ff9f43; border-left: 2px solid #ff9f43; border-top-left-radius: 16px; opacity: 0.4; pointer-events: none;"></div>
  <div style="position: absolute; bottom: 0; right: 0; width: 60px; height: 60px; border-bottom: 2px solid #ff9f43; border-right: 2px solid #ff9f43; border-bottom-right-radius: 16px; opacity: 0.4; pointer-events: none;"></div>

  <!-- Decorative Ambient Wood-Ring Quote Mask Background -->
  <div style="position: absolute; top: -35px; right: -15px; font-size: 10rem; color: rgba(255, 159, 67, 0.04); font-family: serif; pointer-events: none; user-select: none; line-height: 1;">“</div>
  
  <!-- Icon Wrapper containing the original Sparkle emoji flanked by unique glowing layout icons -->
  <div style="margin-bottom: 16px; display: flex; justify-content: center; align-items: center; gap: 15px;">
    <!-- Left Unique Vector Accent -->
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" style="opacity: 0.7; filter: drop-shadow(0 0 5px rgba(255,159,67,0.5));">
      <path d="M12 2L2 12h3v8h14v-8h3L12 2z"/>
    </svg>

    <!-- Original Icon Intact -->
    <div style="font-size: 2rem; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));">✨</div>

    <!-- Right Unique Vector Accent -->
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" style="opacity: 0.7; filter: drop-shadow(0 0 5px rgba(255,159,67,0.5));">
      <circle cx="12" cy="12" r="10"/>
      <path d="M12 6v6l4 2"/>
    </svg>
  </div>

  <!-- Tamil Quote with Active Core Shimmer Text-Glow -->
  <p style="font-size: 1.8rem; font-weight: 800; color: #ffffff; margin: 0 0 16px 0; font-family: 'Mukta Malar', sans-serif; letter-spacing: 0.5px; text-shadow: 0 0 10px rgba(255, 159, 67, 0.6), 0 0 20px rgba(255, 90, 0, 0.3);">
    "யாதும் ஊரே யாவரும் கேளிர்"
  </p>
  
  <!-- Elegant Laser-Line Glowing Divider -->
  <div style="width: 80px; height: 2px; background: linear-gradient(90deg, transparent, #ff9f43, transparent); margin: 0 auto 20px auto; filter: drop-shadow(0 0 4px #ff9f43);"></div>

  <!-- Meaning Wrapper Container with Wood Accent Border -->
  <div style="background: rgba(17, 12, 10, 0.6); padding: 15px 20px; border-radius: 8px; border: 1px solid rgba(255, 140, 0, 0.1); max-width: 620px; margin: 0 auto;">
    <p style="font-size: 1.1rem; color: #e0e0e6; margin: 0; line-height: 1.7; font-weight: 500;">
      <strong style="color: #ff9f43; font-style: normal; text-shadow: 0 0 6px rgba(255,159,67,0.3);">பொருள்:</strong> எல்லா ஊர்களும் நமது ஊர்களே, எல்லா மக்களும் நமது உறவினர்களே.
    </p>
  </div>
  
  <!-- Poet Credit Badge style with micro amber accent tags -->
  <span style="display: inline-block; font-size: 0.8rem; color: #ffb774; margin-top: 22px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; background: rgba(255, 159, 67, 0.08); padding: 4px 14px; border-radius: 12px; border: 1px solid rgba(255, 159, 67, 0.15); display: inline-flex; align-items: center; gap: 8px;">
    <!-- Unique Micro Badge Vector Symbol -->
    <svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor" style="color: #ff9f43;">
      <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
    </svg>
    — கணியன் பூங்குன்றனார் (புறநானூறு)
  </span>
</div>

<!-- Education Section -->
<section id="education" style="padding: 60px 20px; background: #0d0d0e;">
  <h2 style="color: #ff9f43; font-size: 2rem; text-align: center; margin-bottom: 40px; letter-spacing: 0.5px;">Education</h2>
  
  <div class="education-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; max-width: 900px; margin: 0 auto;">
    
    <!-- Postgraduate Degree -->
    <div class="card" style="
        background: #121214; 
        color: #f3f4f6; 
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); 
        
        /* VFX Warm Light Glow on all sides */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   
            0 0 50px 10px rgba(230, 140, 10, 0.15), 
            inset 0 0 15px rgba(255, 100, 0, 0.08); 
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      <div>
        <!-- College Visual / Glowing University SVG Icon -->
        <div class="college-badge" style="background: #1a1a1e; padding: 15px; text-align: center; border-radius: 6px; margin-bottom: 15px; border: 1px solid rgba(255, 140, 0, 0.1); display: flex; justify-content: center; align-items: center;">
          <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="filter: drop-shadow(0 0 8px rgba(255,159,67,0.6));">
            <path d="M22 10v6M2 10l10-5 10 5-10 5z"></path>
            <path d="M6 12v5c0 2 2 3 6 3s6-1 6-3v-5"></path>
          </svg>
        </div>
        <h3 style="margin-top: 0; margin-bottom: 8px; color: #ff9f43; font-size: 1.4rem;">Master of Business Administration (MBA)</h3>
        
        <a href="https://siims.ac.in/" target="_blank" rel="noopener noreferrer" style="text-decoration: none; color: #ffffff;">
          <h4 style="margin: 0; font-weight: 600; transition: color 0.2s;" onmouseover="this.style.color='#ffb774'" onmouseout="this.style.color='#ffffff'">SIIMS College - Pollachi</h4>
        </a>
        <span class="meta" style="font-size: 0.85rem; color: #a0a0aa; display: block; margin-bottom: 4px; margin-top: 6px;">Affiliated to Anna University - Chennai </span>
        <span class="meta" style="font-size: 0.9rem; color: #ffb774; display: block; margin-bottom: 4px; font-weight: 500;">2023 - 2025</span>
        
        <ul class="experience-list" style="margin-top: 12px; margin-bottom: 0; padding-left: 20px; line-height: 1.6; color: #e0e0e6;">
          <li style="margin-bottom: 6px;">Specialization in Financial Management & Data Analytics.</li>
          <li style="margin-bottom: 0;">Deepened expertise in data-driven corporate finance strategy.</li>
        </ul>
      </div>
      
      <!-- Academic Highlight Tag -->
      <div class="academic-gift" style="background: rgba(255, 159, 67, 0.1); color: #ffb774; padding: 8px 12px; border-radius: 6px; font-weight: 600; font-size: 0.9rem; margin-top: 20px; display: inline-block; width: max-content; border: 1px solid rgba(255, 159, 67, 0.25);">
        🏆 Academic Merit: 7.8 CGPA
      </div>
    </div> <!-- /card -->

    <!-- Undergraduate Degree -->
    <div class="card" style="
        background: #121214; 
        color: #f3f4f6; 
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); 
        
        /* VFX Warm Light Glow on all sides */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   
            0 0 50px 10px rgba(230, 140, 10, 0.15), 
            inset 0 0 15px rgba(255, 100, 0, 0.08); 
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      <div>
        <!-- College Visual / Glowing Certificate SVG Icon -->
        <div class="college-badge" style="background: #1a1a1e; padding: 15px; text-align: center; border-radius: 6px; margin-bottom: 15px; border: 1px solid rgba(255, 140, 0, 0.1); display: flex; justify-content: center; align-items: center;">
          <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="filter: drop-shadow(0 0 8px rgba(255,159,67,0.6));">
            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
            <polyline points="14 2 14 8 20 8"></polyline>
            <line x1="16" y1="13" x2="8" y2="13"></line>
            <line x1="16" y1="17" x2="8" y2="17"></line>
            <polyline points="10 9 9 9 8 9"></polyline>
          </svg>
        </div>
        <h3 style="margin-top: 0; margin-bottom: 8px; color: #ff9f43; font-size: 1.4rem;">Bachelor of Commerce (B.Com)</h3>
        
        <a href="https://www.ngmc.org/" target="_blank" rel="noopener noreferrer" style="text-decoration: none; color: #ffffff;">
          <h4 style="margin: 0; font-weight: 600; transition: color 0.2s;" onmouseover="this.style.color='#ffb774'" onmouseout="this.style.color='#ffffff'">NGM College - Pollachi</h4>
        </a>
        <span class="meta" style="font-size: 0.85rem; color: #a0a0aa; display: block; margin-bottom: 4px; margin-top: 6px;">Affiliated to Bharathiar University - Coimbatore </span>
        <span class="meta" style="font-size: 0.9rem; color: #ffb774; display: block; margin-bottom: 4px; font-weight: 500;">2020 - 2023</span>
        
        <ul class="experience-list" style="margin-top: 12px; margin-bottom: 0; padding-left: 20px; line-height: 1.6; color: #e0e0e6;">
          <li style="margin-bottom: 6px;">Built a strong foundation in accounting, corporate laws, and business statistics.</li>
          <li style="margin-bottom: 0;">Active participation in commerce and financial literacy forums.</li>
        </ul>
      </div>
      
      <!-- Academic Highlight Tag -->
      <div class="academic-gift" style="background: rgba(255, 159, 67, 0.1); color: #ffb774; padding: 8px 12px; border-radius: 6px; font-weight: 600; font-size: 0.9rem; margin-top: 20px; display: inline-block; width: max-content; border: 1px solid rgba(255, 159, 67, 0.25);">
        🏆 Academic Merit: 7.5 CGPA
      </div>
    </div> <!-- /card -->

  </div> <!-- /education-grid -->
</section>
    
<section id="experience" style="padding: 60px 20px; background: #0d0d0e;">
  <h2 style="color: #ff9f43; font-size: 2rem; text-align: center; margin-bottom: 40px; letter-spacing: 0.5px;">Corporate Exposure</h2>
  
  <div class="grid" style="display: flex; flex-wrap: wrap; gap: 25px; justify-content: center; max-width: 1200px; margin: 0 auto;">
    
    <div class="card" style="
        background: #121214; /* Deep premium dark background */
        color: #f3f4f6; /* Light text for readability */
        border-radius: 12px; 
        padding: 30px; 
        position: relative;
        width: 100%;
        max-width: 600px; /* Gives the timeline entry a spacious layout */
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); /* Subtle warm amber border */
        
        /* VFX Warm Light Glow on all sides */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   /* Vibrant inner amber warmth */
            0 0 50px 10px rgba(230, 140, 10, 0.15), /* Soft golden outer spread */
            inset 0 0 15px rgba(255, 100, 0, 0.08); /* Internal edge warmth */
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      
      <div style="display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 10px; margin-bottom: 6px;">
        <h3 style="display: inline-flex; align-items: center; gap: 12px; font-family: sans-serif; color: #ff9f43; margin: 0; font-size: 1.5rem;">
          Junior Analyst 
        </h3>
        <span style="font-size: 0.75rem; font-weight: 700; color: #ffb774; background: rgba(255, 159, 67, 0.1); padding: 4px 10px; border-radius: 6px; border: 1px solid rgba(255, 159, 67, 0.25); letter-spacing: 0.5px;">
          ✨ ANALYST // 2026
        </span>
      </div>
      
      <span class="meta" style="display: block; font-size: 0.9rem; color: #a0a0aa; margin-bottom: 8px;">August 2025 - Present</span>
      <h4 style="margin-top: 0; margin-bottom: 15px; color: #ffffff; font-weight: 600; font-size: 1.1rem;">ZOLD UDP FOODS PRIVATE LIMITED, Udumalpet</h4>
      
      <ul class="experience-list" style="margin-bottom: 20px; padding-left: 20px; line-height: 1.7; color: #e0e0e6;">
        <li style="margin-bottom: 8px;">Assisted in preparing and maintaining accurate financial records and reports.</li>
        <li style="margin-bottom: 8px;">Facilitated monthly closing processes, including reconciliations and posting journal entries.</li>
        <li style="margin-bottom: 8px;">Managed accounts payable and receivable to ensure timely processing and compliance.</li>
        <li style="margin-bottom: 0;">Collaborated with senior accountants to improve efficiency and reduce reporting errors.</li>
      </ul>
      
      <div class="article-links-container" style="margin-top: 15px; font-size: 0.95rem;">
        <a href="https://www.zoldgroup.com/" target="_blank" class="text-link-pdf primary-link" style="color: #ffb774; text-decoration: none; font-weight: 500; transition: color 0.2s;" onmouseover="this.style.color='#ff9f43'" onmouseout="this.style.color='#ffb774'">
          Company Website
        </a>
        <span class="link-separator" style="color: rgba(255, 140, 0, 0.3); margin: 0 10px;">|</span>
        <a href="https://maps.app.goo.gl/QRWXGr5fm6w1y4nf6" target="_blank" class="text-link-pdf secondary-link" style="color: #ffb774; text-decoration: none; font-weight: 500; transition: color 0.2s;" onmouseover="this.style.color='#ff9f43'" onmouseout="this.style.color='#ffb774'">
          Company Location
        </a>
      </div>
      
    </div> </div> </section>

<section id="projects" style="padding: 60px 20px; background: #0d0d0e; border-top: 1px solid rgba(255, 140, 0, 0.05);">
  <h2 style="color: #ff9f43; font-size: 2rem; text-align: center; margin-bottom: 40px; letter-spacing: 0.5px;">Research & Projects</h2>
  
  <div class="grid" style="display: flex; flex-wrap: wrap; gap: 25px; justify-content: center; max-width: 1200px; margin: 0 auto;">
    
    <div class="card" style="
        background: #121214; 
        color: #f3f4f6; 
        border-radius: 12px; 
        padding: 30px; 
        position: relative;
        width: 100%;
        max-width: 600px; 
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); 
        
        /* VFX Warm Light Glow on all sides */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   
            0 0 50px 10px rgba(230, 140, 10, 0.15), 
            inset 0 0 15px rgba(255, 100, 0, 0.08); 
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      
      <h3 style="margin-top: 0; margin-bottom: 6px; color: #ff9f43; font-size: 1.5rem; letter-spacing: 0.5px;">NBFC Financial Performance Analysis</h3>
      <span class="meta" style="display: block; font-size: 0.9rem; color: #a0a0aa; margin-bottom: 15px;">Postgraduate Project (Published - May 2025)</span>
      
      <p style="line-height: 1.7; color: #e0e0e6; margin-bottom: 20px; font-size: 1rem;">
        Published a research paper titled <strong style="color: #ffffff;">"Analysis of Capital Adequacy of Leading 5 Non-Banking Financial Companies in India"</strong> 
        in the EPRA International Journal of Economics, Business and Management Studies (EBMS), Vol. 12, Issue 5, May 2025.
      </p>
      
      <div class="article-links-container" style="margin-top: 15px; font-size: 0.95rem;">
        <a href="NaveenKumar_Published_Article.pdf" target="_blank" class="text-link-pdf primary-link" style="color: #ffb774; text-decoration: none; font-weight: 500; transition: color 0.2s;" onmouseover="this.style.color='#ff9f43'" onmouseout="this.style.color='#ffb774'">
          View Published Article (PDF)
        </a>
        <span class="link-separator" style="color: rgba(255, 140, 0, 0.3); margin: 0 10px;">|</span>
        <a href="naveenkumar_article_certificate.pdf" target="_blank" class="text-link-pdf secondary-link" style="color: #ffb774; text-decoration: none; font-weight: 500; transition: color 0.2s;" onmouseover="this.style.color='#ff9f43'" onmouseout="this.style.color='#ffb774'">
          View Published Article Certificate (PDF)
        </a>
      </div>
      
    </div> </div> </section>


<section id="skills" style="padding: 60px 20px; background: #0d0d0e;">
  <h2 style="color: #ff9f43; font-size: 2rem; text-align: center; margin-bottom: 40px; letter-spacing: 0.5px;">Technical Skills & Credentials</h2>
  
  <div class="skills-grid" style="display: flex; flex-wrap: wrap; gap: 25px; justify-content: center; max-width: 1200px; margin: 0 auto;">
    
    <div class="skills-box" style="
        background: #121214; /* Deep premium dark background */
        color: #f3f4f6; /* Light text for readability */
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        flex: 1 1 300px; /* Responsive sizing */
        max-width: 360px;
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); /* Subtle warm amber border */
        
        /* VFX Warm Light Glow on all sides */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   /* Vibrant inner amber warmth */
            0 0 50px 10px rgba(230, 140, 10, 0.15), /* Soft golden outer spread */
            inset 0 0 15px rgba(255, 100, 0, 0.08); /* Internal edge warmth */
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      <h3 style="margin-top: 0; margin-bottom: 15px; color: #ff9f43; font-size: 1.4rem; letter-spacing: 0.5px;">Analytical & Technical Skills</h3>
      <ul style="margin-bottom: 0; padding-left: 20px; line-height: 1.6; color: #e0e0e6;">
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Advanced Excel</strong> – Pivot Tables, Macros, Data Visualization</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">MySQL</strong> – Database queries, joins, stored procedures</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Power BI</strong> – Dashboard creation, data modeling</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Python</strong> – Data analysis, automation, visualization (Pandas)</li>
        <li style="margin-bottom: 0;"><strong style="color: #ffb774;">Business Analysis</strong> – Financial modeling, process improvement, strategic insights</li>
      </ul>
    </div>

    <div class="skills-box" style="
        background: #121214; 
        color: #f3f4f6; 
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        flex: 1 1 300px;
        max-width: 360px;
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); 
        
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   
            0 0 50px 10px rgba(230, 140, 10, 0.15), 
            inset 0 0 15px rgba(255, 100, 0, 0.08); 
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      <h3 style="margin-top: 0; margin-bottom: 15px; color: #ff9f43; font-size: 1.4rem; letter-spacing: 0.5px;">Accounting & Taxation Skills</h3>
      <ul style="margin-bottom: 0; padding-left: 20px; line-height: 1.6; color: #e0e0e6;">
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">GST</strong> compliance, filing, and reconciliation</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Tally Prime</strong> for accounting and financial management</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">TDS</strong> (Tax Deducted at Source) calculation and reporting</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Income Tax</strong> preparation and return filing</li>
        <li style="margin-bottom: 0;"><strong style="color: #ffb774;">VAT</strong> accounting and compliance procedures</li>
      </ul>
    </div>

    <div class="skills-box" style="
        background: #121214; 
        color: #f3f4f6; 
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        flex: 1 1 300px;
        max-width: 360px;
        box-sizing: border-box;
        border: 1px solid rgba(255, 140, 0, 0.25); 
        
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   
            0 0 50px 10px rgba(230, 140, 10, 0.15), 
            inset 0 0 15px rgba(255, 100, 0, 0.08); 
        
    transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';" >
      <h3 style="margin-top: 0; margin-bottom: 15px; color: #ff9f43; font-size: 1.4rem; letter-spacing: 0.5px;">Professional Certifications</h3>
      <ul style="margin-bottom: 0; padding-left: 20px; line-height: 1.6; color: #e0e0e6;">
        <li style="margin-bottom: 12px;"><strong style="color: #ffb774;">Human Resources Management</strong> (Swayam-NPTEL) – Expanded knowledge of management concepts and HR practices</li>
        <li style="margin-bottom: 0;"><strong style="color: #ffb774;">AI in Marketing</strong> (Swayam-NPTEL) – Strengthened understanding of AI’s role in modern marketing strategies</li>
        <a href="NPTL AI in Marketing.pdf" target="_blank" style="color: #ff9f43; text-decoration: underline; font-weight: bold; transition: color 0.3s ease;" onmouseover="this.style.color='#ff9f43'" onmouseout="this.style.color='#ffb774'">Certifications</a>
      </ul>
    </div>

  </div>
</section>



<!-- Quote Inspiration Showcase Module -->
<div class="inspiration-container" style="
  margin-top: 45px; 
  padding: 35px 30px; 
  background: #111113; /* Premium dark background to let the warm VFX light pop */
  border-radius: 16px; 
  text-align: center;
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(255, 140, 0, 0.2);
  
  /* VFX Warm Light Glow distributed evenly on all sides */
  box-shadow: 
    0 0 25px 2px rgba(255, 100, 0, 0.2),    /* Warm volcanic core glow */
    0 0 50px 10px rgba(212, 175, 55, 0.12), /* Ambient golden background spread */
    inset 0 0 20px rgba(255, 255, 255, 0.02); /* Delicate internal edge light */
    
  transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
  cursor: default;
" 
onmouseover="
  this.style.transform='translateY(-6px)'; 
  this.style.boxShadow='0 0 40px 6px rgba(255, 100, 0, 0.35), 0 0 70px 18px rgba(212, 175, 55, 0.22), inset 0 0 25px rgba(255, 255, 255, 0.05)'; 
  this.style.borderColor='rgba(255, 165, 0, 0.5)';
"
onmouseout="
  this.style.transform='translateY(0)'; 
  this.style.boxShadow='0 0 25px 2px rgba(255, 100, 0, 0.2), 0 0 50px 10px rgba(212, 175, 55, 0.12), inset 0 0 20px rgba(255, 255, 255, 0.02)'; 
  this.style.borderColor='rgba(255, 140, 0, 0.2)';
"
>
  <!-- Decorative Backdrop Layer Graphic -->
  <div style="position: absolute; bottom: -30px; left: 50%; transform: translateX(-50%); font-size: 11rem; color: rgba(255, 140, 0, 0.02); font-weight: 900; pointer-events: none; user-select: none; font-family: sans-serif;">🏔️</div>
  
  <!-- Icon / Animated VFX Anchor -->
  <div style="font-size: 2.5rem; margin-bottom: 8px; filter: drop-shadow(0 0 12px rgba(255, 165, 0, 0.6));">🏔️</div>

  <!-- Label / Tagline -->
  <span class="inspiration-label" style="display: block; font-size: 0.8rem; color: #ff9f43; margin-bottom: 12px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase;">
    Core Mindset
  </span>
  
  <!-- Elegant Warm Divider Line -->
  <div style="width: 60px; height: 2px; background: linear-gradient(90deg, transparent, #ff8c00, transparent); margin: 0 auto 20px auto; border-radius: 2px;"></div>

  <!-- Tamil Quote Text Effect -->
  <p class="quote-tamil" style="font-size: 1.5rem; font-weight: 700; color: #ffffff; margin: 0 0 12px 0; padding: 0 10px; line-height: 1.5; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; letter-spacing: 0.5px;">
    "விடாமுயற்சியும், தன்னம்பிக்கையும் இருந்தால், எந்த மலையையும் வெல்லலாம்."
  </p>

  <!-- English Quote Text Effect with Styled Key words -->
  <blockquote class="quote-english" style="font-size: 1.1rem; font-style: italic; font-weight: 400; color: #b3b3ba; margin: 0 auto 24px auto; padding: 0 15px; line-height: 1.6; max-width: 600px;">
    If you have <span style="color: #ff9f43; font-weight: 600; text-shadow: 0 0 8px rgba(255, 159, 67, 0.3);">perseverance</span> and <span style="color: #ff9f43; font-weight: 600; text-shadow: 0 0 8px rgba(255, 159, 67, 0.3);">self-confidence</span>, you can conquer any mountain.
  </blockquote>

  <!-- Academic Gift / Highlight Tag -->
  <div class="achievement-badge" style="
    background: linear-gradient(135deg, rgba(255,140,0,0.15) 0%, rgba(212,175,55,0.15) 100%); 
    color: #ffd700; 
    padding: 6px 14px; 
    border-radius: 20px; 
    font-weight: 600; 
    font-size: 0.8rem; 
    letter-spacing: 0.5px;
    display: inline-flex; 
    align-items: center; 
    gap: 6px;
    border: 1px solid rgba(212, 175, 55, 0.3);
    box-shadow: 0 2px 10px rgba(0,0,0,0.3);
  ">
    🏆 Peak Achiever Mindset
  </div>
</div>

<section id="my professional work">
    <div class="skills-box" style="
        background: #121214; /* Deep premium dark background to make the glow stand out */
        color: #f3f4f6; /* Light text for readability */
        border-radius: 12px; 
        padding: 25px; 
        position: relative;
        border: 1px solid rgba(255, 140, 0, 0.25); /* Subtle warm amber border */
        
        /* VFX Warm Light Glow on all sides (0 offset ensures it doesn't leak out of corners sharply) */
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25),   /* Vibrant inner amber warmth */
            0 0 50px 10px rgba(230, 140, 10, 0.15), /* Soft golden outer spread */
            inset 0 0 15px rgba(255, 100, 0, 0.08); /* Internal edge warmth */
        
        transition: all 0.4s ease-in-out;
    "
    onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)';"
    onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)';">
      
      <h3 style="margin-top: 0; color: #ff9f43; font-size: 1.6rem; letter-spacing: 0.5px;">My Professional Work</h3>
      <ul class="skills-list" style="margin-bottom: 0; padding-left: 20px; line-height: 1.7; color: #e0e0e6;">
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Digital Marketing</strong> – Strategic content creation, professional video editing, and impact-driven poster design.</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Financial Analysis</strong> – Comprehensive financial statement evaluation and strategic portfolio management.</li>
        <li style="margin-bottom: 8px;"><strong style="color: #ffb774;">Custom Solutions</strong> – Dedicated consulting and tailored support to solve your unique business challenges.</li>
        <li style="margin-bottom: 0;"><strong style="color: #ffb774;">Finance Filing</strong> – GST, VAT, TDS, TCS, Income Tax and other Filing and Queries.</li>
      </ul>
    </div>
</section>

 <div class="vision-container" style="
  margin-top: 45px; 
  padding: 35px 30px; 
  background: radial-gradient(circle at center, #221a16 0%, #110c0a 100%); /* Deep luxurious dark wood aesthetic */
  border-radius: 16px; 
  text-align: center;
  position: relative;
  overflow: hidden;
  box-sizing: border-box;
  cursor: default;
  
  /* Precision Structural Border & Warm Light Burst Glow */
  border: 1px solid rgba(255, 140, 0, 0.3);
  box-shadow: 
      0 0 30px 2px rgba(255, 90, 0, 0.2),       /* Inner warm core */
      0 10px 40px -10px rgba(0, 0, 0, 0.7),      /* Deep ground shadow drop */
      inset 0 0 20px rgba(255, 100, 0, 0.05);    /* Ambient interior heat glow */
      
  transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
" 
onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 0 45px 6px rgba(255, 90, 0, 0.35), 0 15px 50px -5px rgba(0, 0, 0, 0.85), inset 0 0 25px rgba(255, 100, 0, 0.1)'; this.style.borderColor='rgba(255, 159, 67, 0.6)';"
onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 0 30px 2px rgba(255, 90, 0, 0.2), 0 10px 40px -10px rgba(0, 0, 0, 0.7), inset 0 0 20px rgba(255, 100, 0, 0.05)'; this.style.borderColor='rgba(255, 140, 0, 0.3)';" >

  <div style="position: absolute; left: 10px; top: 50%; transform: translateY(-50%); opacity: 0.25; pointer-events: none;">
    <svg width="14" height="40" viewBox="0 0 14 40" fill="none" stroke="#ff9f43" stroke-width="1.5">
      <line x1="7" y1="0" x2="7" y2="40" stroke-dasharray="2 4"/>
      <circle cx="7" cy="20" r="3" fill="#ff9f43"/>
    </svg>
  </div>
  <div style="position: absolute; right: 10px; top: 50%; transform: translateY(-50%); opacity: 0.25; pointer-events: none;">
    <svg width="14" height="40" viewBox="0 0 14 40" fill="none" stroke="#ff9f43" stroke-width="1.5">
      <line x1="7" y1="0" x2="7" y2="40" stroke-dasharray="2 4"/>
      <circle cx="7" cy="20" r="3" fill="#ff9f43"/>
    </svg>
  </div>

  <div style="position: absolute; top: 0; left: 0; width: 60px; height: 60px; border-top: 2px solid #ff9f43; border-left: 2px solid #ff9f43; border-top-left-radius: 16px; opacity: 0.4; pointer-events: none;"></div>
  <div style="position: absolute; bottom: 0; right: 0; width: 60px; height: 60px; border-bottom: 2px solid #ff9f43; border-right: 2px solid #ff9f43; border-bottom-right-radius: 16px; opacity: 0.4; pointer-events: none;"></div>

  <div style="position: absolute; top: -35px; right: -15px; font-size: 10rem; color: rgba(255, 159, 67, 0.04); font-family: serif; pointer-events: none; user-select: none; line-height: 1;">“</div>
  
  <div style="margin-bottom: 16px; display: flex; justify-content: center; align-items: center; gap: 15px;">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="opacity: 0.7; filter: drop-shadow(0 0 5px rgba(255,159,67,0.5));">
      <circle cx="12" cy="12" r="10"></circle>
      <circle cx="12" cy="12" r="6"></circle>
      <circle cx="12" cy="12" r="2"></circle>
    </svg>

    <div style="font-size: 2rem; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));">💡</div>

    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="opacity: 0.7; filter: drop-shadow(0 0 5px rgba(255,159,67,0.5));">
      <path d="M2 12s3-7 10-7 10 7 10 7-3 7-10 7-10-7-10-7z"></path>
      <circle cx="12" cy="12" r="3"></circle>
    </svg>
  </div>

  <span class="vision-label" style="display: inline-block; font-size: 0.8rem; color: #ffb774; margin-bottom: 16px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; background: rgba(255, 159, 67, 0.08); padding: 4px 14px; border-radius: 12px; border: 1px solid rgba(255, 159, 67, 0.15); display: inline-flex; align-items: center; gap: 8px;">
    <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3">
      <path d="M20 6L9 17l-5-5"></path>
    </svg>
    Our Vision
  </span>
  
  <div style="width: 80px; height: 2px; background: linear-gradient(90deg, transparent, #ff9f43, transparent); margin: 0 auto 20px auto; filter: drop-shadow(0 0 4px #ff9f43);"></div>

  <div style="background: rgba(17, 12, 10, 0.6); padding: 20px; border-radius: 8px; border: 1px solid rgba(255, 140, 0, 0.1); max-width: 650px; margin: 0 auto; position: relative;">
    
    <div style="position: absolute; top: 4px; left: 4px; width: 4px; height: 4px; background: #ff9f43; opacity: 0.4; border-radius: 50%;"></div>
    <div style="position: absolute; top: 4px; right: 4px; width: 4px; height: 4px; background: #ff9f43; opacity: 0.4; border-radius: 50%;"></div>
    <div style="position: absolute; bottom: 4px; left: 4px; width: 4px; height: 4px; background: #ff9f43; opacity: 0.4; border-radius: 50%;"></div>
    <div style="position: absolute; bottom: 4px; right: 4px; width: 4px; height: 4px; background: #ff9f43; opacity: 0.4; border-radius: 50%;"></div>

    <blockquote class="vision-text" style="font-size: 1.5rem; font-style: italic; font-weight: 600; color: #ffffff; margin: 0; padding: 0 5px; line-height: 1.6; font-family: -apple-system, BlinkMacSystemFont, sans-serif; text-shadow: 0 0 10px rgba(255, 159, 67, 0.5), 0 0 20px rgba(255, 90, 0, 0.25);">
      "A flexible, innovative approach to problem-solving that uses limited resources to get things done"
    </blockquote>
  </div>
</div>

  <section id="contact" style="padding: 50px 20px; display: flex; justify-content: center; background: #0d0d0e;">
  
  <div class="contact-box" style="
      background: #121214; /* Deep premium dark background */
      color: #f3f4f6; /* Light text for readability */
      border-radius: 12px; 
      padding: 30px; 
      position: relative;
      width: 100%;
      max-width: 500px; /* Keeps the form looking neat on desktop */
      box-sizing: border-box;
      border: 1px solid rgba(255, 140, 0, 0.25); /* Subtle warm amber border */
      
      /* VFX Warm Light Glow on all sides */
      box-shadow: 
          0 0 25px 2px rgba(255, 90, 0, 0.25),   /* Vibrant inner amber warmth */
          0 0 50px 10px rgba(230, 140, 10, 0.15), /* Soft golden outer spread */
          inset 0 0 15px rgba(255, 100, 0, 0.08); /* Internal edge warmth */
      
      transition: all 0.4s ease-in-out;
  "
  onmouseover="this.style.boxShadow='0 0 35px 5px rgba(255, 90, 0, 0.35), 0 0 65px 15px rgba(230, 140, 10, 0.22), inset 0 0 20px rgba(255, 100, 0, 0.12)'; this.style.transform='translateY(-2px)';"
  onmouseout="this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 0 50px 10px rgba(230, 140, 10, 0.15), inset 0 0 15px rgba(255, 100, 0, 0.08)'; this.style.transform='translateY(0)';">
    
    <h2 style="margin-top: 0; margin-bottom: 25px; color: #ff9f43; font-size: 1.8rem; letter-spacing: 0.5px; text-align: center;">Get In Touch</h2>
    
    <form action="https://formsubmit.co/naveenbalakrishnan146@gmail.com" method="POST" style="display: flex; flex-direction: column; gap: 15px;">
      <input type="hidden" name="_captcha" value="false">
      
      <input type="text" name="name" placeholder="Your Name" required style="
          width: 100%; padding: 12px; background: #1a1a1e; border: 1px solid rgba(255, 140, 0, 0.2); 
          border-radius: 6px; color: #f3f4f6; font-size: 1rem; box-sizing: border-box;
      ">
      
      <input type="email" name="email" placeholder="Your Email" required style="
          width: 100%; padding: 12px; background: #1a1a1e; border: 1px solid rgba(255, 140, 0, 0.2); 
          border-radius: 6px; color: #f3f4f6; font-size: 1rem; box-sizing: border-box;
      ">
      
      <textarea name="message" placeholder="Your Message" required style="
          width: 100%; height: 120px; padding: 12px; background: #1a1a1e; border: 1px solid rgba(255, 140, 0, 0.2); 
          border-radius: 6px; color: #f3f4f6; font-size: 1rem; box-sizing: border-box; resize: vertical;
      "></textarea>
      
      <button type="submit" style="
          width: 100%; padding: 14px; background: linear-gradient(135deg, #ff9f43,#55a142); 
          border: none; border-radius: 6px; color: #fff; font-size: 1rem; font-weight: bold; 
          cursor: pointer; transition: opacity 0.2s ease; margin-top: 5px;
      "
      onmouseover="this.style.opacity='0.9'"
      onmouseout="this.style.opacity='1'">Send Message</button>
    </form>
    
  </div>
</section>
    
<!-- High Effect Footer Section -->
<footer style="
    margin-top: 60px;
    padding: 40px 20px;
    background: radial-gradient(circle at top, #221a16 0%, #110c0a 100%); /* Deep dark wood aesthetic */
    position: relative;
    overflow: hidden;
    text-align: center;
    box-sizing: border-box;
    
    /* Top Border Warm Light VFX Laser Glow Line */
    border-top: 2px solid #ff9f43;
    box-shadow: 0 -4px 30px 0px rgba(255, 140, 0, 0.35), 0 -2px 10px 0px rgba(230, 140, 10, 0.15);
">

  <!-- UNIQUE EXTRA DESIGN SYMBOLS: Structural Corner Grid Marks -->
  <div style="position: absolute; top: 8px; right: 12px; opacity: 0.25; pointer-events: none;">
    <svg width="40" height="12" viewBox="0 0 40 12" fill="none" stroke="#ff9f43" stroke-width="1.5">
      <circle cx="6" cy="6" r="3" fill="#ff9f43"/>
      <line x1="14" y1="6" x2="40" y2="6" stroke-dasharray="2 3"/>
    </svg>
  </div>

  <div class="footer-content" style="max-width: 800px; margin: 0 auto; display: flex; flex-direction: column; gap: 10px;">
    
    <!-- Row 1: Copyright Shimmer Text -->
    <p style="margin: 0; font-size: 1.1rem; font-weight: 700; color: #ffffff; letter-spacing: 0.5px; text-shadow: 0 0 8px rgba(255, 159, 67, 0.45);">
      &copy;💙2026 NaveenKumar B💙
    </p>
    
    <!-- Row 2: Location Block with Ambient Container Frame -->
    <p style="margin: 4px 0; font-size: 0.95rem; color: #e0e0e6; font-weight: 500; letter-spacing: 0.5px;">
      📍Thungavi- Udumalpet - Coimbatore📍
    </p>
    
    <!-- Rows 3 & 4: Design & Portfolio Marks -->
    <p style="margin: 2px 0; font-size: 0.9rem; color: #ffb774; font-weight: 600; opacity: 0.9;">
      🌐My personal design🌐
    </p>
    <p style="margin: 2px 0 20px 0; font-size: 0.9rem; color: #ffb774; font-weight: 600; opacity: 0.9;">
      🎨Portfolio Website🎨
    </p>

    <!-- Mid-way Glowing Accent Divider Vector -->
    <div style="width: 120px; height: 1px; background: linear-gradient(90deg, transparent, #ff9f43, transparent); margin: 5px auto 20px auto; filter: drop-shadow(0 0 3px #ff9f43);"></div>

    <!-- Interactive Navigation Links Container -->
    <div class="footer-links" style="display: flex; justify-content: center; align-items: center; flex-wrap: wrap; gap: 12px 18px;">
      
      <!-- LinkedIn Link Component -->
      <a href="https://www.linkedin.com/in/naveenkumar-b-3713311ab" target="_blank" style="
          color: #ff9f43; text-decoration: none; font-weight: 700; font-size: 0.9rem; letter-spacing: 1px; text-transform: uppercase;
          padding: 6px 14px; border: 1px solid rgba(255,159,67,0.25); border-radius: 20px; background: rgba(17,12,10,0.5);
          text-shadow: 0 0 6px rgba(255,159,67,0.4); display: inline-flex; align-items: center; gap: 6px; transition: all 0.3s ease;
      "
      onmouseover="this.style.color='#ffffff'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 14px rgba(255,159,67,0.45)'; this.style.background='rgba(255,159,67,0.1)';"
      onmouseout="this.style.color='#ff9f43'; this.style.borderColor='rgba(255,159,67,0.25)'; this.style.boxShadow='none'; this.style.background='rgba(17,12,10,0.5)';"
      ><svg width="10" height="10" viewBox="0 0 24 24" fill="currentColor" style="opacity:0.8;"><circle cx="12" cy="12" r="10"/></svg>LinkedIn</a>
      
      <!-- GitHub Link Component -->
      <a href="https://github.com/naveen12345naveen" target="_blank" style="
          color: #ff9f43; text-decoration: none; font-weight: 700; font-size: 0.9rem; letter-spacing: 1px; text-transform: uppercase;
          padding: 6px 14px; border: 1px solid rgba(255,159,67,0.25); border-radius: 20px; background: rgba(17,12,10,0.5);
          text-shadow: 0 0 6px rgba(255,159,67,0.4); display: inline-flex; align-items: center; gap: 6px; transition: all 0.3s ease;
      "
      onmouseover="this.style.color='#ffffff'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 14px rgba(255,159,67,0.45)'; this.style.background='rgba(255,159,67,0.1)';"
      onmouseout="this.style.color='#ff9f43'; this.style.borderColor='rgba(255,159,67,0.25)'; this.style.boxShadow='none'; this.style.background='rgba(17,12,10,0.5)';"
      ><svg width="10" height="10" viewBox="0 0 24 24" fill="currentColor" style="opacity:0.8;"><circle cx="12" cy="12" r="10"/></svg>GitHub</a>
      
      <!-- Email Link Component -->
      <a href="mailto:naveenbalakrishnan146@gmail.com" style="
          color: #ff9f43; text-decoration: none; font-weight: 700; font-size: 0.9rem; letter-spacing: 1px; text-transform: uppercase;
          padding: 6px 14px; border: 1px solid rgba(255,159,67,0.25); border-radius: 20px; background: rgba(17,12,10,0.5);
          text-shadow: 0 0 6px rgba(255,159,67,0.4); display: inline-flex; align-items: center; gap: 6px; transition: all 0.3s ease;
      "
      onmouseover="this.style.color='#ffffff'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 14px rgba(255,159,67,0.45)'; this.style.background='rgba(255,159,67,0.1)';"
      onmouseout="this.style.color='#ff9f43'; this.style.borderColor='rgba(255,159,67,0.25)'; this.style.boxShadow='none'; this.style.background='rgba(17,12,10,0.5)';"
      ><svg width="10" height="10" viewBox="0 0 24 24" fill="currentColor" style="opacity:0.8;"><circle cx="12" cy="12" r="10"/></svg>Email</a>
      
      <!-- Instagram Link Component -->
      <a href="https://www.instagram.com/naveenkumar.b.nkb?igsh=MXNhYjFycG9tN2lnYw==" target="_blank" style="
          color: #ff9f43; text-decoration: none; font-weight: 700; font-size: 0.9rem; letter-spacing: 1px; text-transform: uppercase;
          padding: 6px 14px; border: 1px solid rgba(255,159,67,0.25); border-radius: 20px; background: rgba(17,12,10,0.5);
          text-shadow: 0 0 6px rgba(255,159,67,0.4); display: inline-flex; align-items: center; gap: 6px; transition: all 0.3s ease;
      "
      onmouseover="this.style.color='#ffffff'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 14px rgba(255,159,67,0.45)'; this.style.background='rgba(255,159,67,0.1)';"
      onmouseout="this.style.color='#ff9f43'; this.style.borderColor='rgba(255,159,67,0.25)'; this.style.boxShadow='none'; this.style.background='rgba(17,12,10,0.5)';"
      ><svg width="10" height="10" viewBox="0 0 24 24" fill="currentColor" style="opacity:0.8;"><circle cx="12" cy="12" r="10"/></svg>Instagram</a>
      
      <!-- Mobile Link Component -->
      <a href="tel:+916369311629" style="
          color: #ff9f43; text-decoration: none; font-weight: 700; font-size: 0.9rem; letter-spacing: 1px; text-transform: uppercase;
          padding: 6px 14px; border: 1px solid rgba(255,159,67,0.25); border-radius: 20px; background: rgba(17,12,10,0.5);
          text-shadow: 0 0 6px rgba(255,159,67,0.4); display: inline-flex; align-items: center; gap: 6px; transition: all 0.3s ease;
      "
      onmouseover="this.style.color='#ffffff'; this.style.borderColor='#ff9f43'; this.style.boxShadow='0 0 14px rgba(255,159,67,0.45)'; this.style.background='rgba(255,159,67,0.1)';"
      onmouseout="this.style.color='#ff9f43'; this.style.borderColor='rgba(255,159,67,0.25)'; this.style.boxShadow='none'; this.style.background='rgba(17,12,10,0.5)';"
      ><svg width="10" height="10" viewBox="0 0 24 24" fill="currentColor" style="opacity:0.8;"><circle cx="12" cy="12" r="10"/></svg>Mobile</a>

    </div>
  </div>
</footer>

<!-- Stylish Button Link to Learn with Me Page -->
<div style="text-align: center; margin-top: 30px; margin-bottom: 20px;">
    <a href="page2.html" style="
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 12px;
        padding: 16px 36px;
        font-size: 18px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-weight: bold;
        color: #ffffff;
        
        /* Premium Obsidian Wood Gradient Core */
        background: linear-gradient(135deg, #2c201a 0%, #16100e 100%);
        border-radius: 50px;
        text-decoration: none;
        position: relative;
        overflow: hidden;
        box-sizing: border-box;
        
        /* Precision Warm Light VFX Laser Border & Ambient Core Glow */
        border: 2px solid rgba(255, 140, 0, 0.4);
        box-shadow: 
            0 0 25px 2px rgba(255, 90, 0, 0.25), 
            0 8px 25px -8px rgba(0, 0, 0, 0.6),
            inset 0 0 12px rgba(255, 140, 0, 0.1);
            
        transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
    " 
    onmouseover="this.style.transform='translateY(-3px) scale(1.03)'; this.style.boxShadow='0 0 35px 6px rgba(255, 90, 0, 0.45), 0 12px 30px -5px rgba(0, 0, 0, 0.75), inset 0 0 15px rgba(255, 140, 0, 0.2)'; this.style.borderColor='rgba(255, 159, 67, 0.85)';" 
    onmouseout="this.style.transform='translateY(0) scale(1)'; this.style.boxShadow='0 0 25px 2px rgba(255, 90, 0, 0.25), 0 8px 25px -8px rgba(0, 0, 0, 0.6), inset 0 0 12px rgba(255, 140, 0, 0.1)'; this.style.borderColor='rgba(255, 140, 0, 0.4)';" >
        
        <!-- UNIQUE DESIGN SYMBOL: Left Micro Bracket Node -->
        <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="3" style="opacity: 0.8; filter: drop-shadow(0 0 3px #ff9f43);">
            <path d="M15 18l-6-6 6-6"/>
        </svg>

        <!-- Original Icon Intact -->
        <span>🎁 Learn with me</span>

        <!-- UNIQUE DESIGN SYMBOL: Right Micro Bracket Node -->
        <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="#ff9f43" stroke-width="3" style="opacity: 0.8; filter: drop-shadow(0 0 3px #ff9f43);">
            <path d="M9 18l6-6-6-6"/>
        </svg>
    </a>
</div>
