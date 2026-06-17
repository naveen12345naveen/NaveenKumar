<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NaveenKumar B - Personal Portfolio</title>
    <style>
        / Base Reset & Variables /
        {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }

        :root {
            --primary-color: #4CAF50;
            --bg-color: #121212;
            --card-bg: #1e1e1e;
            --text-color: #e0e0e0;
            --text-muted: #a0a0a0;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        / Navbar /
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem 5%;
            background-color: rgba(30, 30, 30, 0.9);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary-color);
        }

        / Hero Section /
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 70vh;
            text-align: center;
            padding: 0 1rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
        }

        .hero h1 span {
            color: var(--primary-color);
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .cta-btn {
            background-color: var(--primary-color);
            color: #fff;
            padding: 0.8rem 2rem;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: transform 0.3s, background-color 0.3s;
        }

        .cta-btn:hover {
            background-color: #45a049;
            transform: translateY(-3px);
        }

        / Sections /
        section {
            padding: 5rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        h2.section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
        }

        h2.section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background-color: var(--primary-color);
            margin: 10px auto 0;
            border-radius: 2px;
        }

        / About Section /
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-content p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        / Projects Section /
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            padding: 1.5rem;
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-card h3 {
            margin-bottom: 0.5rem;
        }

        .project-card p {
            color: var(--text-muted);
            margin-bottom: 1rem;
        }

        .project-card a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: bold;
        }

        / Contact Section /
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
        }

        .contact-form input, .contact-form textarea {
            background-color: var(--card-bg);
            border: 1px solid #333;
            color: var(--text-color);
            padding: 1rem;
            margin-bottom: 1.5rem;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-form textarea {
            resize: vertical;
            height: 150px;
        }

        .contact-form button {
            background-color: var(--primary-color);
            color: #fff;
            border: none;
            padding: 1rem;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .contact-form button:hover {
            background-color: #45a049;
        }

        / Footer /
        footer {
            text-align: center;
            padding: 2rem;
            background-color: var(--card-bg);
            color: var(--text-muted);
        }

        / Responsive Design /
        @media (max-width: 768px) {
            nav ul {
                display: none; / Consider adding a mobile menu here /
            }
            .about-content {
                grid-template-columns: 1fr;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="logo">Portfolio.</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <p>Hello, I'm</p>
        <h1>[Naveenkumar B]</h1>
        <p>A passionate Developer & Designer building digital experiences.</p>
        <a href="#contact" class="cta-btn">Get In Touch</a>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div>
                <p>I am a dedicated professional with a strong foundation in designing and developing scalable, responsive, and user-centric websites. My goal is to turn complex problems into beautiful, simple, and intuitive interfaces.</p>
            </div>
            <div>
                <p><strong>Skills:</strong> HTML5/CSS3, JavaScript, React, UI/UX Design, Problem Solving, and Version Control (Git).</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2 class="section-title">My Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Project One</h3>
                <p>A brief description of your first project. Highlight the technologies used and the problem it solved.</p>
                <a href="#">View Code &rarr;</a>
            </div>
            <div class="project-card">
                <h3>Project Two</h3>
                <p>A brief description of your second project. Mention features like responsive design or API integrations.</p>
                <a href="#">View Code &rarr;</a>
            </div>
            <div class="project-card">
                <h3>Project Three</h3>
                <p>A brief description of your third project. Focus on your specific contribution and design choices.</p>
                <a href="#">View Code &rarr;</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Contact Me</h2>
        <form class="contact-form" action="https://formsubmit.co" method="POST">
            <input type="text" name="name" placeholder="NaveenKumar B" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 [NaveenKumar B]. Built with HTML & CSS.</p>
    </footer>

</body>
</html>
