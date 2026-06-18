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
    <a href="#education section">Education Section</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#my professional work">My Professional Work</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- High Effect Header Section -->
  <header id="about">
    <div class="header-reveal">
      <h1>Naveen Kumar B</h1>
      <p>MBA in Finance & Business Analyst</p>
      <p class="sub">I am an MBA in Finance and Business Analytics professional blending core financial acumen with a robust data analytics toolkit. Currently driving financial health as a Junior Analyst at ZOLD UDP Foods, I specialize in financial modeling, accounts optimization, and month-end reconciliations. With hands-on mastery over Excel, Power BI, MySQL, and Python, I transform raw corporate data into strategic, actionable business insights. My background spans published research on NBFC capital adequacy alongside practical exposure to manufacturing and supply chain operations. I bridge the gap between finance and technology to eliminate operational inefficiencies and fuel data-backed business growth</p>
    </div>
  </header>

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
            <h4>Anna University (Regional Campus, Coimbatore)</h4>
            <span class="meta">2023 - 2025</span>
            <ul class="experience-list" style="margin-top: 12px;">
              <li>Specialization in Financial Management & Data Analytics.</li>
              <li>Deepened expertise in data-driven corporate finance strategy.</li>
            </ul>
          </div>
          <!-- Academic Gift/Highlight Tag -->
          <div class="academic-gift" style="background: #eef9f0; color: #1e7e34; padding: 8px 12px; border-radius: 4px; font-weight: 600; font-size: 0.9rem; margin-top: 15px; display: inline-block; width: max-content;">
            🏆 Academic Merit: 7.8 CGPA
          </div>
        </div>

        <!-- Undergraduate Degree -->
        <div class="card" style="display: flex; flex-direction: column; justify-content: space-between;">
          <div>
            <!-- College Visual / Logo Placeholder -->
            <div class="college-badge" style="background: #f4f6f9; padding: 15px; text-align: center; border-radius: 6px; margin-bottom: 15px;">
              <span style="font-size: 2.5rem;">🎓</span> <!-- Replace this emoji with an <img src="ngm-logo.png"> later -->
            </div>
            <h3>Bachelor of Commerce (B.Com)</h3>
            <h4>NGM College, Pollachi</h4>
            <span class="meta" style="font-size: 0.85rem; color: #777;">Affiliated to Bharathiar University</span><br>
            <span class="meta">2020 - 2023</span>
            <ul class="experience-list" style="margin-top: 12px;">
              <li>Built a strong foundation in accounting, corporate laws, and business statistics.</li>
              <li>Active participation in commerce and financial literacy forums.</li>
            </ul>
          </div>
          <!-- Academic Gift/Highlight Tag -->
          <div class="academic-gift" style="background: #eef9f0; color: #1e7e34; padding: 8px 12px; border-radius: 4px; font-weight: 600; font-size: 0.9rem; margin-top: 15px; display: inline-block; width: max-content;">
            🏆 Academic Merit: 7.5 CGPA
          </div>
        </div>

      </div>
    </section>

  <div class="container">
    
    <!-- Corporate Exposure / Experience Section -->
    <section id="experience">
      <h2>Corporate Exposure</h2>
      <div class="card">
        <h3>Junior Analyst</h3>
        <h4>ZOLD UDP FOODS PRIVATE LIMITED, Udumalpet</h4>
        <span class="meta">August 2025 - Present</span>
        <ul class="experience-list">
          <li>Assisted in preparing and maintaining accurate financial records and reports.</li>
          <li>Facilitated monthly closing processes, including reconciliations and posting journal entries.</li>
          <li>Managed accounts payable and receivable to ensure timely processing and compliance.</li>
          <li>Collaborated with senior accountants to improve efficiency and reduce reporting errors.</li>
        </ul>
      </div>
    </section>

    <!-- Projects & Publications Section -->
    <section id="projects">
      <h2>Research & Projects</h2>
     <div class="grid">
  <div class="card">
    <h3>NBFC Financial Performance Analysis</h3>
    <span class="meta">Postgraduate Project (Published - May 2025)</span>
    <p>Published a research paper titled "Analysis of Capital Adequacy of Leading 5 Non-Banking Financial Companies in India" in the EPRA International Journal of Economics, Business and Management Studies (EBMS), Vol. 12, Issue 5, May 2025.</p>
    <a href="NaveenKumar_Published_Article.pdf" target="_blank" class="btn-pdf">View Published Article (PDF)</a>
  </div>

        <div class="card">
          <h3>Handloom Weaving Landscape Study</h3>
          <span class="meta">Research Project (Pollachi Taluk)</span>
          <p>Conducted qualitative data gathering from local weavers to analyze critical bottlenecks in demand, credit access, and marketing infrastructure, proposing sustainable growth strategies.</p>
        </div>
      </div>
    </section>

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
    <div class="skills-box">
      <h3>My Professional Work</h3>
      <ul>
        <li>Digital Marketing – Strategic content creation, professional video editing, and impact-driven poster design.</li>
        <li>Financial Analysis – Comprehensive financial statement evaluation and strategic portfolio management.</li>
        <li>Custom Solutions – Dedicated consulting and tailored support to solve your unique business challenges.</li>
        <li>Finance Filling – GST, VAT, TDS, TCS, Income Tax and other Filling and Queries.</li>
      </ul>
    </div>
    
  <!-- Vision Theme -->
  <div class="vision-statement" style="text-align: center; margin-top: 40px; padding: 15px; border-top: 1px dashed #ddd;">
    <p style="font-size: 1.25rem; font-style: italic; font-weight: 600; color: #2c3e50; margin: 0;">
      "Innovating to shape a brand new world."
    </p>
  </div>
 
    <!-- Contact Section -->
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


  <!-- High Effect Footer Section -->
  <footer>
    <div class="footer-content">
      <p>&copy; 2026 Naveen Kumar B</p>
      <p>Finance & Business Analyst | Portfolio Website</p>
      <div class="footer-links">
        <a href="https://www.linkedin.com/in/naveenkumar-b-3713311ab" target="_blank">LinkedIn</a>
        <a href="https://github.com/naveen12345naveen" target="_blank">GitHub</a>
        <a href="mailto:naveenbalakrishnan146@gmail.com">Email</a>
          <a href="https://www.instagram.com/naveenkumar.b.nkb?igsh=MXNhYjFycG9tN2lnYw==">Instagram</a>
      </div>
    </div>
  </footer>
