<html lang="en">
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
      --neon-blue: #00e5ff;
    }
    
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
    
    /* Navigation Bar */
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

    /* Ticker & Audio Bar */
    .market-ticker-container {
      background: #050505;
      border-bottom: 1px dashed rgba(76, 175, 80, 0.4);
      padding: 12px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-family: 'Courier New', Courier, monospace;
      font-size: 0.85rem;
      position: relative;
      z-index: 999;
    }

    .ticker-left {
      display: flex;
      gap: 20px;
      color: var(--neon-blue);
      font-weight: bold;
      text-shadow: 0 0 5px rgba(0, 229, 255, 0.3);
    }

    .ticker-item {
      background: #111;
      padding: 4px 10px;
      border-radius: 4px;
      border: 1px solid #222;
    }

    .ticker-item span {
      color: #fff;
      margin-left: 5px;
    }

    .up-trend { color: #00ff88 !important; }

    .audio-control-btn {
      background: linear-gradient(90deg, #1e3a20, #4CAF50);
      color: #000;
      border: none;
      padding: 6px 16px;
      border-radius: 20px;
      cursor: pointer;
      font-size: 0.8rem;
      font-family: inherit;
      font-weight: bold;
      text-transform: uppercase;
      transition: all 0.3s ease;
      box-shadow: 0 0 15px var(--primary-glow);
      animation: pulseGlowBtn 1.5s infinite;
    }

    .audio-control-btn.active {
      background: #222;
      color: var(--primary);
      border: 1px solid #333;
      animation: none;
      box-shadow: none;
    }

    /* Shifting Gradient Header */
    header { 
      background: linear-gradient(-45deg, #0f1f11, #141414, #050b06, #112614);
      background-size: 400% 400%;
      animation: gradientBG 12s ease infinite;
      text-align: center; 
      padding: 130px 20px; 
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

    .container { 
      max-width: 1100px; 
      margin: auto; 
      padding: 20px; 
    }
    
    section { 
      padding: 90px 0; 
      border-bottom: 1px solid #1a1a1a; 
    }
    
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
    
    .card h3 { margin-bottom: 12px; color: #fff; font-size: 1.45rem; }
    .card h4 { color: var(--primary); margin-bottom: 12px; font-weight: 400; }
    .meta { font-size: 0.95rem; color: var(--muted); margin-bottom: 18px; display: block; }

    .experience-list { list-style: none; margin-top: 15px; }
    .experience-list li { position: relative; padding-left: 25px; margin-bottom: 12px; color: #e0e0e0; font-size: 0.98rem; }
    .experience-list li::before { content: '✓'; position: absolute; left: 0; color: var(--primary); font-weight: bold; text-shadow: 0 0 8px var(--primary); }

    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
    .skills-box { background: #0f0f0f; padding: 30px; border-radius: 12px; border: 1px solid #1a1a1a; transition: border-color 0.3s ease; }
    .skills-box:hover { border-color: rgba(76, 175, 80, 0.3); }
    .skills-box h3 { font-size: 1.25rem; margin-bottom: 20px; color: #fff; border-bottom: 1px solid #222; padding-bottom: 10px; }
    .skills-box ul { list-style: none; }
    .skills-box li { background: #181818; padding: 12px 18px; margin-bottom: 12px; border-radius: 8px; font-size: 0.95rem; border-left: 4px solid var(--primary); transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), background 0.3s ease; }
    .skills-box li:hover { transform: translateX(10px) scale(1.02); background: #1f2d21; }

    /* Dynamic Contact Form & Upload Mechanics */
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

    /* UNIQUE VISUAL COMPONENT: PHOTO UPLOAD CONTAINER */
    .file-upload-wrapper {
      margin: 20px 0;
      position: relative;
    }

    .file-upload-label {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 25px;
      background: #0f0f0f;
      border: 2px dashed #333;
      border-radius: 8px;
      cursor: pointer;
      text-align: center;
      transition: all 0.3s ease;
    }

    .file-upload-label:hover {
      border-color: var(--primary);
      background: rgba(76, 175, 80, 0.03);
      box-shadow: 0 0 15px rgba(76, 175, 80, 0.1);
    }

    .file-upload-label span {
      font-size: 0.9rem;
      color: var(--muted);
      margin-top: 5px;
    }

    .file-upload-label .icon {
      font-size: 1.8rem;
      color: var(--primary);
      text-shadow: 0 0 8px var(--primary-glow);
    }

    /* Hidden Native File Input Wrapper */
    .file-upload-input {
      display: none;
    }

    /* Dynamic Preview Block Component */
    .image-preview-box {
      margin-top: 15px;
      display: none;
      text-align: center;
      border: 1px solid #222;
      padding: 10px;
      border-radius: 8px;
      background: #090909;
    }

    .image-preview-box img {
      max-width: 100%;
      max-height: 200px;
      border-radius: 6px;
      border: 1px solid #333;
    }

    .remove-preview-btn {
      display: inline-block;
      margin-top: 8px;
      font-size: 0.8rem;
      color: #ff5252;
      cursor: pointer;
      text-decoration: underline;
    }

    button[type="submit"] { 
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
    
    button[type="submit"]:hover { 
      background: #45a049; 
      box-shadow: 0 0 20px var(--primary);
      transform: translateY(-3px);
    }

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
    
    .footer-content p { margin: 6px 0; text-align: center; }
    .footer-links { margin-top: 30px; }
    
    .footer-links a { 
      color: #fff; 
      text-decoration: none; 
      margin: 0 15px; 
      font-weight: 500; 
      padding: 10px 24px;
      border: 1px solid #333;
      border-radius: 30px;
      display: inline-block;
      transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1); 
    }
    
    .footer-links a:hover { 
      color: var(--primary); 
      border-color: var(--primary);
      background: rgba(76, 175, 80, 0.08);
      box-shadow: 0 0 20px var(--primary-glow), inset 0 0 8px rgba(76,175,80,0.1);
      transform: translateY(-5px);
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(50px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.4; width: 70%; }
      50% { opacity: 1; width: 95%; }
    }

    @keyframes expandLine {
      from { width: 50px; }
      to { width: 110px; }
    }

    @keyframes pulseGlowBtn {
      0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(76, 175, 80, 0.7); }
      70% { transform: scale(1.03); box-shadow: 0 0 0 12px rgba(76, 175, 80, 0); }
      100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(76, 175, 80, 0); }
    }

    @media (max-width: 768px) { 
      header h1 { font-size: 2.8rem; }
      nav a { margin: 0 6px; font-size: 0.9rem; }
      .market-ticker-container { flex-direction: column; gap: 10px; text-align: center; }
      .ticker-left { flex-wrap: wrap; justify-content: center; }
    }
  </style>
</head>
<body>

  <nav>
    <a href="#about">About</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
  </nav>

  <div class="market-ticker-container">
    <div class="ticker-left">
      <div class="ticker-item">NSE NIFTY50: <span id="nse-val" class="up-trend">24,041.75</span></div>
      <div class="ticker-item">BSE SENSEX: <span id="bse-val" class="up-trend">78,920.40</span></div>
      <div class="ticker-item">USD/INR: <span id="usd-val">83.54</span></div>
    </div>
    <div>
      <button id="audio-toggle" class="audio-control-btn" onclick="toggleMusicEngine()">Unmute Background Music</button>
    </div>
  </div>

  <header id="about">
    <div class="header-reveal">
      <h1>Naveen Kumar B</h1>
      <p>MBA in Finance & Business Analyst</p>
      <p class="sub">Specializing in financial modeling, data analysis, and transforming complex data into strategic business insights using Power BI, MySQL, and Python.</p>
    </div>
  </header>

  <div class="container">
    
    <section id="experience">
      <h2>Corporate Exposure</h2>
      <div class="card">
        <h3>Junior Analyst [cite: 12]</h3>
        <h4>ZOLD UDP FOODS PRIVATE LIMITED, Udumalpet [cite: 12]</h4>
        <span class="meta">August 2025 - Present [cite: 12]</span>
        <ul class="experience-list">
          <li>Assisted in preparing and maintaining accurate financial records and reports. [cite: 12]</li>
          <li>Facilitated monthly closing processes, including reconciliations and posting journal entries. [cite: 13]</li>
          <li>Managed accounts payable and receivable to ensure timely processing and compliance. [cite: 14]</li>
          <li>Collaborated with senior accountants to improve efficiency and reduce reporting errors. [cite: 15]</li>
        </ul>
      </div>
    </section>

    <section id="projects">
      <h2>Research & Projects</h2>
      <div class="grid">
        <div class="card">
          <h3>NBFC Financial Performance Analysis [cite: 26]</h3>
          <span class="meta">Postgraduate Project (Published - May 2025) [cite: 25, 49, 50]</span>
          <p>Published a research paper titled "Analysis of Capital Adequacy of Leading 5 Non-Banking Financial Companies in India" in the EPRA International Journal of Economics, Business and Management Studies (EBMS), Vol. 12, Issue 5, May 2025. [cite: 49, 50]</p>
        </div>
        <div class="card">
          <h3>Handloom Weaving Landscape Study [cite: 23]</h3>
          <span class="meta">Research Project (Pollachi Taluk) [cite: 21, 23]</span>
          <p>Conducted qualitative data gathering from local weavers to analyze critical bottlenecks in demand, credit access, and marketing infrastructure, proposing sustainable growth strategies. [cite: 23, 24]</p>
        </div>
      </div>
    </section>

    <section id="skills">
      <h2>Technical Skills & Credentials</h2>
      <div class="skills-grid">
        <div class="skills-box">
          <h3>Analytical & Technical Skills [cite: 28]</h3>
          <ul>
            <li>Advanced Excel – Pivot Tables, Macros, Data Visualization [cite: 29]</li>
            <li>MySQL – Database queries, joins, stored procedures [cite: 30]</li>
            <li>Power BI – Dashboard creation, data modeling [cite: 31]</li>
            <li>Python – Data analysis, automation, visualization (Pandas) [cite: 32]</li>
            <li>Business Analysis – Financial modeling, process improvement, strategic insights [cite: 33]</li>
          </ul>
        </div>
        <div class="skills-box">
          <h3>Accounting & Taxation Skills [cite: 34]</h3>
          <ul>
            <li>GST compliance, filing, and reconciliation [cite: 35]</li>
            <li>Tally Prime for accounting and financial management [cite: 36]</li>
            <li>TDS (Tax Deducted at Source) calculation and reporting [cite: 37]</li>
            <li>Income Tax preparation and return filing [cite: 37]</li>
            <li>VAT accounting and compliance procedures [cite: 38]</li>
          </ul>
        </div>
        <div class="skills-box">
          <h3>Professional Certifications [cite: 39]</h3>
          <ul>
            <li>Human Resources Management (Swayam-NPTEL) – Expanded knowledge of management concepts and HR practices [cite: 42]</li>
            <li>AI in Marketing (Swayam-NPTEL) – Strengthened understanding of AI’s role in modern marketing strategies [cite: 43]</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="contact">
      <h2>Get In Touch</h2>
      
      <form action="https://formsubmit.co/naveenbalakrishnan146@gmail.com" method="POST" enctype="multipart/form-data">
        <input type="hidden" name="_captcha" value="false">
        
        <input type="text" name="name" placeholder="Your Name" required>
        <input type="email" name="email" placeholder="Your Email" required>
        <textarea name="message" placeholder="Your Message" required></textarea>
        
        <div class="file-upload-wrapper">
          <label for="photo-attachment" class="file-upload-label">
            <div class="icon">dagger;</div>
            <p style="font-weight: bold; margin-top: 5px; color: #fff;">Upload Image / Attachment</p>
            <span>Click to browse files (Images, PDF, PNG, JPG)</span>
          </label>
          <input type="file" id="photo-attachment" name="attachment" accept="image/*,application/pdf" class="file-upload-input" onchange="previewImage(event)">
        </div>

        <div id="preview-container" class="image-preview-box">
          <img id="output-image" src="#" alt="Upload Preview">
          <div><span class="remove-preview-btn" onclick="clearPreviewFile()">Remove Attachment</span></div>
        </div>
        
        <button type="submit">Send Message</button>
      </form>
    </section>

  </div>

  <footer>
    <div class="footer-content">
      <p>&copy; 2026 Naveen Kumar B</p>
      <p>Finance & Business Analyst | Portfolio Website</p>
      <div class="footer-links">
        <a href="https://www.linkedin.com/in/naveenkumar-b-3713311ab" target="_blank">LinkedIn</a>
        <a href="https://github.com/naveen12345naveen" target="_blank">GitHub</a>
        <a href="mailto:naveenbalakrishnan146@gmail.com">Email</a>
      </div>
    </div>
  </footer>

  <script>
    let audioCtx = null;
    let musicPlaying = false;
    let sequenceInterval = null;
    let currentStep = 0;

    const chords = [
      [164.81, 196.00, 246.94, 293.66], 
      [130.81, 164.81, 196.00, 261.63], 
      [146.83, 196.00, 246.94, 293.66], 
      [146.83, 220.00, 293.66, 369.99]  
    ];

    function toggleMusicEngine() {
      const btn = document.getElementById('audio-toggle');
      if (!musicPlaying) {
        audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        musicPlaying = true;
        btn.textContent = "Music Loop Active";
        btn.classList.add('active');
        playAmbientChord();
        sequenceInterval = setInterval(playAmbientChord, 4000);
      } else {
        musicPlaying = false;
        btn.textContent = "Unmute Background Music";
        btn.classList.remove('active');
        clearInterval(sequenceInterval);
      }
    }

    function playAmbientChord() {
      if (!musicPlaying || !audioCtx) return;
      const chord = chords[currentStep];
      const now = audioCtx.currentTime;
      chord.forEach((freq) => {
        let osc = audioCtx.createOscillator();
        let gain = audioCtx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(freq, now);
        gain.gain.setValueAtTime(0, now);
        gain.gain.linearRampToValueAtTime(0.015, now + 1.5);
        gain.gain.exponentialRampToValueAtTime(0.0001, now + 4.0);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start(now);
        osc.stop(now + 4.0);
      });
      currentStep = (currentStep + 1) % chords.length;
    }

    /* NEW JAVASCRIPT: MEDIA FILE READERS & PREVIEW CONTROL ENGINE */
    function previewImage(event) {
      const reader = new FileReader();
      const imageField = document.getElementById('output-image');
      const previewContainer = document.getElementById('preview-container');

      reader.onload = function() {
        if (reader.readyState === 2) {
          // If the uploaded file is a PDF, use a standard icon placeholder, otherwise show the image
          if (event.target.files[0].type === "application/pdf") {
            imageField.src = "https://cdn-icons-png.flaticon.com/512/337/337946.png"; 
          } else {
            imageField.src = reader.result;
          }
          previewContainer.style.display = "block";
        }
      }
      if (event.target.files[0]) {
        reader.readAsDataURL(event.target.files[0]);
      }
    }

    function clearPreviewFile() {
      const fileInput = document.getElementById('photo-attachment');
      const previewContainer = document.getElementById('preview-container');
      const imageField = document.getElementById('output-image');
      
      fileInput.value = ""; // Erases the stored attachment file data
      imageField.src = "#";
      previewContainer.style.display = "none";
    }

    function initTickerEngine() {
      setInterval(() => {
        const nseDelta = (Math.random() * 4 - 2);
        const bseDelta = (Math.random() * 12 - 6);
        const currentNse = parseFloat(document.getElementById('nse-val').textContent.replace(/,/g, ''));
        const currentBse = parseFloat(document.getElementById('bse-val').textContent.replace(/,/g, ''));
        document.getElementById('nse-val').textContent = (currentNse + nseDelta).toLocaleString('en-IN', {maximumFractionDigits: 2});
        document.getElementById('bse-val').textContent = (currentBse + bseDelta).toLocaleString('en-IN', {maximumFractionDigits: 2});
      }, 4000);
    }

    document.addEventListener("DOMContentLoaded", initTickerEngine);
  </script>

</body>
</html>
