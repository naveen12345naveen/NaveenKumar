<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Naveen Kumar B | Portfolio</title>
  <style>
    :root {
      --primary: #4CAF50;
      --dark: #121212;
      --card-bg: #1e1e1e;
      --text: #ffffff;
      --muted: #a0a0a0;
    }
    
    /* 1. ENABLE SMOOTH SCROLLING EFFECT */
    html {
      scroll-behavior: smooth;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { background: var(--dark); color: var(--text); font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; }
    
    /* Navigation Bar with Hover Effects */
    nav { background: #000; padding: 20px; text-align: center; position: sticky; top: 0; z-index: 1000; border-bottom: 1px solid #333; }
    nav a { 
      color: var(--text); 
      text-decoration: none; 
      margin: 0 15px; 
      font-weight: 500; 
      position: relative;
      padding-bottom: 5px;
      transition: color 0.3s ease; 
    }
    nav a:hover { color: var(--primary); }
    
    /* Animated Underline Effect for Nav Links */
    nav a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: var(--primary);
      transition: width 0.3s ease;
    }
    nav a:hover::after {
      width: 100%;
    }

    /* Hero Header Section with Keyframe Entry Animation */
    header { 
      background: linear-gradient(135deg, #1a1a1a 0%, #000000 100%); 
      text-align: center; 
      padding: 120px 20px; 
      border-bottom: 1px solid #222; 
    }
    
    /* 2. FADE-IN & UP ANIMATION RUNNING ON LOAD */
    .animated-entrance {
      animation: fadeInUp 1s ease-out forwards;
      opacity: 0;
    }
    
    header h1 { font-size: 3.5rem; margin-bottom: 10px; letter-spacing: 1px; }
    header p { font-size: 1.3rem; color: var(--primary); margin-bottom: 15px; font-weight: 300; }
    header .sub { font-size: 1rem; color: var(--muted); max-width: 600px; margin: 0 auto; }

    /* Main Container & Sections */
    .container { max-width: 1100px; margin: auto; padding: 20px; }
    section { padding: 60px 0; border-bottom: 1px solid #222; }
    h2 { color: var(--primary); font-size: 2rem; margin-bottom: 30px; text-transform: uppercase; letter-spacing: 1px; }

    /* Grid Layouts & Glowing Interactive Cards */
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
    
    /* 3. HOVER GLOW AND LIFT EFFECT FOR CARDS */
    .card { 
      background: var(--card-bg); 
      padding: 25px; 
      border-radius: 8px; 
      border: 1px solid #333; 
      transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), border-color 0.4s ease, box-shadow 0.4s ease; 
    }
    .card:hover { 
      transform: translateY(-8px); 
      border-color: var(--primary); 
      box-shadow: 0 10px 20px rgba(76, 175, 80, 0.15);
    }
    
    .card h3 { margin-bottom: 10px; color: #fff; }
    .card h4 { color: var(--primary); margin-bottom: 10px; font-weight: 400; }
    .meta { font-size: 0.9rem; color: var(--muted); margin-bottom: 10px; display: block; }

    /* Skills Grid */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; }
    .skills-box ul { list-style: none; }
    .skills-box li { 
      background: #252525; 
      padding: 8px 12px; 
      margin-bottom: 8px; 
      border-radius: 4px; 
      font-size: 0.95rem; 
      border-left: 3px solid var(--primary); 
      transition: transform 0.2s ease;
    }
    .skills-box li:hover {
      transform: translateX(5px);
    }

    /* Contact Form */
    form { max-width: 600px; margin: auto; background: var(--card-bg); padding: 30px; border-radius: 10px; border: 1px solid #333; }
    input, textarea { width: 100%; padding: 12px; margin: 10px 0; background: #2d2d2d; border: 1px solid #444; border-radius: 6px; color: #fff; font-family: inherit; transition: border-color 0.3s ease; }
    input:focus, textarea:focus { border-color: var(--primary); outline: none; }
    button { background: var(--primary); color: #000; font-weight: bold; border: none; padding: 14px 20px; border-radius: 6px; cursor: pointer; width: 100%; font-size: 16px; transition: 0.3s; text-transform: uppercase; }
    button:hover { background: #45a049; transform: scale(1.01); }

    /* Footer Styling */
    footer { background: #111; color: #ddd; padding: 40px 20px; font-family: 'Segoe UI', sans-serif; border-top: 1px solid #222; }
    .footer-content { max-width: 800px; margin: auto; display: flex; flex-direction: column; align-items: center; }
    .footer-content p { margin: 5px 0; text-align: center; }
    .footer-links { margin-top: 15px; }
    .footer-links a { color: var(--primary); text-decoration: none; margin: 0 15px; font-weight: 500; transition: 0.3s; }
    .footer-links a:hover { color: #fff; text-shadow: 0 0 8px var(--primary); }

    /* CSS Keyframes for Entry Animation */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 768px) { header h1 { font-size: 2.5rem; } }
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
    <div class="animated-entrance">
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
