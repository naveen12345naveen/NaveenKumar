<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Naveen Kumar B | Portfolio</title>
  <style>
    :root {
      --primary: #4CAF50;
      --primary-glow: rgba(76, 175, 80, 0.3);
      --dark: #0a0a0a;
      --card-bg: #141414;
      --text: #ffffff;
      --muted: #b0b0b0;
    }
    
    /* Global Smooth Scrolling */
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
    
    /* Modern Navigation Bar with Glassmorphism */
    nav { 
      background: rgba(0, 0, 0, 0.8); 
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
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

    /* HIGH-EFFECT HEADER SECTION (Moving Gradient Backdrop) */
    header { 
      background: linear-gradient(-45deg, #111, #1a3a1e, #000, #141414);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      text-align: center; 
      padding: 140px 20px; 
      border-bottom: 1px solid #222; 
      position: relative;
    }
    
    /* Fade and Rise Entry Presentation */
    .header-reveal {
      animation: fadeInUp 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;
      opacity: 0;
    }
    
    header h1 { 
      font-size: 4rem; 
      margin-bottom: 15px; 
      letter-spacing: 2px;
      text-shadow: 0 0 20px rgba(255,255,255,0.1);
    }
    
    header p { 
      font-size: 1.4rem; 
      color: var(--primary); 
      margin-bottom: 20px; 
      font-weight: 400; 
      letter-spacing: 1px;
      text-shadow: 0 0 10px var(--primary-glow);
    }
    
    header .sub { 
      font-size: 1.05rem; 
      color: var(--muted); 
      max-width: 650px; 
      margin: 0 auto; 
      line-height: 1.8;
    }

    /* Layout Containers */
    .container { 
      max-width: 1100px; 
      margin: auto; 
      padding: 20px; 
    }
    
    section { 
      padding: 80px 0; 
      border-bottom: 1px solid #1a1a1a; 
    }
    
    h2 { 
      color: var(--primary); 
      font-size: 2.2rem; 
      margin-bottom: 40px; 
      text-transform: uppercase; 
      letter-spacing: 1.5px;
      position: relative;
      display: inline-block;
    }
    
    h2::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -8px;
      width: 50px;
      height: 3px;
      background: var(--primary);
      box-shadow: 0 0 8px var(--primary);
    }

    /* Interactive Adaptive Card Grids */
    .grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
      gap: 30px; 
    }
    
    .card { 
      background: var(--card-bg); 
      padding: 30px; 
      border-radius: 12px; 
      border: 1px solid #222; 
      transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), 
                  border-color 0.4s ease, 
                  box-shadow 0.4s ease; 
    }
    
    .card:hover { 
      transform: translateY(-10px); 
      border-color: var(--primary); 
      box-shadow: 0 15px 30px rgba(76, 175, 80, 0.12);
    }
    
    .card h3 { 
      margin-bottom: 12px; 
      color: #fff; 
      font-size: 1.4rem;
    }
    
    .card h4 { 
      color: var(--primary); 
      margin-bottom: 12px; 
      font-weight: 400; 
    }
    
    .meta { 
      font-size: 0.9rem; 
      color: var(--muted); 
      margin-bottom: 15px; 
      display: block; 
    }

    /* Interactive Skills Architecture */
    .skills-grid { 
      display: grid; 
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); 
      gap: 30px; 
    }
    
    .skills-box {
      background: #0f0f0f;
      padding: 25px;
      border-radius: 10px;
      border: 1px solid #1a1a1a;
    }
    
    .skills-box h3 {
      font-size: 1.2rem;
      margin-bottom: 15px;
      color: #fff;
      border-bottom: 1px solid #222;
      padding-bottom: 8px;
    }
    
    .skills-box ul { 
      list-style: none; 
    }
    
    .skills-box li { 
      background: #181818; 
      padding: 10px 15px; 
      margin-bottom: 10px; 
      border-radius: 6px; 
      font-size: 0.95rem; 
      border-left: 3px solid var(--primary); 
      transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275), background 0.3s ease;
    }
    
    .skills-box li:hover {
      transform: translateX(8px) scale(1.02);
      background: #202020;
    }

    /* Form Fields Styling & Focus Effects */
    form { 
      max-width: 600px; 
      margin: auto; 
      background: var(--card-bg); 
      padding: 40px; 
      border-radius: 12px; 
      border: 1px solid #222; 
    }
    
    input, textarea { 
      width: 100%; 
      padding: 14px; 
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
      box-shadow: 0 0 10px rgba(76, 175, 80, 0.2);
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
      box-shadow: 0 0 15px var(--primary);
      transform: translateY(-2px);
    }

    /* HIGH-EFFECT FOOTER SECTION */
    footer { 
      background: #050505; 
      color: #ddd; 
      padding: 50px 20px; 
      font-family: 'Segoe UI', sans-serif; 
      border-top: 1px solid #1a1a1a; 
      position: relative;
    }
    
    /* Pulsing Top Footer Ambient Light */
    footer::before {
      content: '';
      position: absolute;
      top: -1px;
      left: 50%;
      transform: translateX(-50%);
      width: 80%;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--primary), transparent);
      animation: pulseGlow 4s ease-in-out infinite;
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
      margin-top: 25px; 
    }
    
    /* Glowing Bubble Footer Links */
    .footer-links a { 
      color: #fff; 
      text-decoration: none; 
      margin: 0 12px; 
      font-weight: 500; 
      padding: 8px 18px;
      border: 1px solid #222;
      border-radius: 30px;
      display: inline-block;
      transition: all 0.3s cubic-bezier(0.165, 0.84, 0.44, 1); 
    }
    
    .footer-links a:hover { 
      color: var(--primary); 
      border-color: var(--primary);
      background: rgba(76, 175, 80, 0.05);
      box-shadow: 0 0 15px var(--primary-glow);
      transform: translateY(-3px);
    }

    /* Core Animation Timelines (Keyframes) */
    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.3; width: 60%; }
      50% { opacity: 1; width: 90%; }
    }

    /* Responsive Tweaks */
    @media (max-width: 768px) { 
      header h1 { font-size: 2.8rem; }
      nav a { margin: 0 8px; font-size: 0.95rem; }
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

  <header id="about">
    <div class="header-reveal">
      <h1>Naveen Kumar B</h1>
      <p>MBA in Finance & Business Analyst</p>
      <p class="sub">Specializing in financial modeling, data analysis, and transforming complex data into strategic business insights using Power BI, MySQL, and Python.</p>
    </div>
  </header>

  <div class="container">
    
    <section id="experience">
      <h2>Work Experience</h2>
      <div class="card">
        <h3>Junior Analyst</h3>
        <h4>ZOLD UDP FOODS PRIVATE LIMITED, Udumalpet</h4>
        <span class="meta">August 2025 - Present</span>
        <p>Assisted in preparing financial records, facilitated monthly closing processes and reconciliations, and managed accounts payable/receivable. Collaborated closely with senior accountants to streamline reporting efficiency.</p>
      </div>
    </section>

    <section id="projects">
      <h2>Research & Projects</h2>
      <div class="grid">
        <div class="card">
          <h3>NBFC Financial Performance Analysis</h3>
          <span class="meta">Postgraduate Project (Published - EPRA EBMS Journal, May 2025)</span>
          <p>Analyzed the capital adequacy, profitability, and trend evaluation of the top five NBFCs in India over a decade. Formulated strategic recommendations for long-term financial sustainability.</p>
        </div>
        <div class="card">
          <h3>Handloom Weaving Landscape Study</h3>
          <span class="meta">Research Project (Pollachi Taluk)</span>
          <p>Conducted qualitative data gathering from local weavers to analyze critical bottlenecks in demand, credit access, and marketing infrastructure, proposing sustainable growth strategies.</p>
        </div>
      </div>
    </section>

    <section id="skills">
      <h2>Technical & Core Skills</h2>
      <div class="skills-grid">
        <div class="skills-box">
          <h3>Analytics & Tech</h3>
          <ul>
            <li>Advanced Excel (Pivots, Macros)</li>
            <li>MySQL (Queries, Joins, SPs)</li>
            <li>Power BI Dashboarding</li>
            <li>Python Data Analysis (Pandas)</li>
          </ul>
        </div>
        <div class="skills-box">
          <h3>Accounting & Tax</h3>
          <ul>
            <li>Tally Prime Management</li>
            <li>GST Compliance & Filing</li>
            <li>TDS Calculation</li>
            <li>Income Tax Preparation</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="contact">
      <h2>Get In Touch</h2>
      <form action="https://formsubmit.co/naveenbalakrishnan146@gmail.com" method="POST">
        <input type="hidden" name="_captcha" value="false">
        
        <input type="text" name="name" placeholder="Your Name" required>
        <input type="email" name="email" placeholder="Your Email" required>
        <textarea name="message" placeholder="Your Message" required></textarea>
        
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

</body>
</html>
