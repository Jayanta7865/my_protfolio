
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <meta name="description" content="Portfolio of Jayanta Kumar Samanta, Python/web developer.">
    <meta name="keywords" content="Python, Web Developer, Fresher, Portfolio, Jayanta Kumar Samanta">
    <meta name="author" content="Jayanta Kumar Samanta">
    <title>Jayanta Kumar Samanta | Python/Web Developer Portfolio</title>
    <link rel="icon" href="favicon.ico">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --accent: #0077b6;
            --bg: #f8f9fa;
            --text: #222;
            --divider: #e0e0e0;
            --footer-bg: #222;
            --footer-text: #fff;
            --card-bg: #fff;
            --card-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        * { box-sizing: border-box; }
        body {
            margin: 0;
            font-family: 'Inter', Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }
        header {
            background: var(--card-bg);
            box-shadow: var(--card-shadow);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 1100px;
            margin: 0 auto;
            padding: 1rem 2rem;
        }
        .nav-logo {
            font-weight: 600;
            color: var(--accent);
            font-size: 1.2rem;
            letter-spacing: 1px;
        }
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.2s;
        }
        .nav-links a:hover {
            color: var(--accent);
        }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }
        .hamburger span {
            width: 25px;
            height: 3px;
            background: var(--accent);
            border-radius: 2px;
            transition: 0.3s;
        }
        @media (max-width: 800px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 60px;
                right: 2rem;
                background: var(--card-bg);
                box-shadow: var(--card-shadow);
                flex-direction: column;
                gap: 1.5rem;
                padding: 1.5rem 2rem;
                border-radius: 8px;
            }
            .nav-links.active {
                display: flex;
            }
            .hamburger {
                display: flex;
            }
        }
        section {
            max-width: 1100px;
            margin: 0 auto;
            padding: 3rem 2rem;
            border-bottom: 1px solid var(--divider);
        }
        .hero {
            display: flex;
            align-items: center;
            gap: 2.5rem;
            flex-wrap: wrap;
            justify-content: center;
        }
        .hero-img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 4px 16px rgba(0,0,0,0.08);
            border: 4px solid var(--accent);
        }
        .hero-content {
            max-width: 500px;
        }
        .hero-title {
            font-size: 2.1rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        .hero-subtitle {
            font-size: 1.1rem;
            color: var(--accent);
            margin-bottom: 1.2rem;
        }
        .hero-cta {
            display: flex;
            gap: 1rem;
            margin-top: 1.2rem;
        }
        .btn {
            background: var(--accent);
            color: #fff;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 6px;
            font-weight: 500;
            cursor: pointer;
            text-decoration: none;
            transition: background 0.2s;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        .btn:hover {
            background: #023e8a;
        }
        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1.2rem;
            color: var(--accent);
        }
        .about-text {
            font-size: 1.05rem;
            margin-bottom: 2rem;
        }
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
            margin-bottom: 1rem;
        }
        .timeline-card {
            background: var(--card-bg);
            box-shadow: var(--card-shadow);
            border-radius: 8px;
            padding: 1rem 1.2rem;
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }
        .timeline-year {
            font-weight: 600;
            color: var(--accent);
            min-width: 70px;
        }
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        .skill-badge {
            background: var(--accent);
            color: #fff;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.98rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        .projects-list {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
        }
        .project-card {
            background: var(--card-bg);
            box-shadow: var(--card-shadow);
            border-radius: 8px;
            padding: 1.2rem 1.5rem;
            min-width: 260px;
            flex: 1;
        }
        .project-title {
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 0.5rem;
        }
        .project-tech {
            font-size: 0.95rem;
            color: #555;
            margin-bottom: 0.5rem;
        }
        .project-role {
            font-size: 0.98rem;
            margin-bottom: 0.5rem;
        }
        .services-list {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            margin-bottom: 1rem;
        }
        .service-card {
            background: var(--card-bg);
            box-shadow: var(--card-shadow);
            border-radius: 8px;
            padding: 1.2rem 1.5rem;
            min-width: 200px;
            flex: 1;
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        .service-icon {
            font-size: 1.7rem;
            color: var(--accent);
        }
        .contact-form {
            max-width: 400px;
            margin-bottom: 2rem;
        }
        .contact-form label {
            display: block;
            margin-bottom: 0.3rem;
            font-weight: 500;
        }
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 0.7rem;
            margin-bottom: 1rem;
            border: 1px solid var(--divider);
            border-radius: 6px;
            font-size: 1rem;
            font-family: inherit;
            background: #fff;
        }
        .contact-form textarea {
            resize: vertical;
            min-height: 80px;
        }
        .contact-details {
            margin-bottom: 1rem;
            font-size: 1.05rem;
        }
        .contact-details a {
            color: var(--accent);
            text-decoration: none;
            margin-right: 1rem;
            font-weight: 500;
        }
        .contact-details a:hover {
            text-decoration: underline;
        }
        footer {
            background: var(--footer-bg);
            color: var(--footer-text);
            text-align: center;
            padding: 2rem 1rem 1rem 1rem;
            margin-top: 0;
        }
        .footer-social {
            margin: 1rem 0 0.5rem 0;
            display: flex;
            justify-content: center;
            gap: 1.2rem;
        }
        .footer-social a {
            color: var(--footer-text);
            font-size: 1.3rem;
            transition: color 0.2s;
        }
        .footer-social a:hover {
            color: var(--accent);
        }
        .divider {
            height: 1px;
            background: var(--divider);
            margin: 0;
            border: none;
        }
        @media (max-width: 600px) {
            section {
                padding: 2rem 1rem;
            }
            .hero {
                flex-direction: column;
                gap: 1.2rem;
            }
            .services-list, .projects-list {
                flex-direction: column;
                gap: 1.2rem;
            }
        }
        /* Simple fade-in animation */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.7s forwards;
        }
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: none;
            }
        }
        /* Light/Dark mode toggle */
        .mode-toggle {
            background: none;
            border: none;
            font-size: 1.3rem;
            cursor: pointer;
            margin-left: 1rem;
            color: var(--accent);
            transition: color 0.2s;
        }
        .mode-toggle:hover {
            color: #023e8a;
        }
        body.dark {
            --bg: #181a1b;
            --text: #f8f9fa;
            --divider: #333;
            --card-bg: #23272b;
            --footer-bg: #111;
            --footer-text: #f8f9fa;
        }
    </style>
</head>
<body>
    <header>
        <nav class="nav">
            <div class="nav-logo">Jayanta Kumar Samanta</div>
            <div class="nav-links" id="navLinks">
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#skills">Skills</a>
                <a href="#projects">Projects</a>
                <a href="#services">Services</a>
                <a href="#contact">Contact</a>
            </div>
            <button class="mode-toggle" id="modeToggle" title="Toggle light/dark mode">&#9788;</button>
            <div class="hamburger" id="hamburger" aria-label="Menu" tabindex="0">
                <span></span><span></span><span></span>
            </div>
        </nav>
    </header>

    <section id="home" class="hero fade-in">
        <!-- <img src="m1.jpg" alt="Jayanta Kumar Samanta" class="hero-img"> -->
        <div class="hero-content">
            <div class="hero-title">Hi, I'm Jayanta Kumar Samanta.</div>
            <div class="hero-subtitle">A Python Developer | Fresher | Web Enthusiast</div>
            <div class="hero-cta">
                <a href="Jayanta_Kumar_Samanta_Resume.pdf" class="btn" download>📄 Download Resume</a>
                <a href="#contact" class="btn">📫 Contact Me</a>
            </div>
        </div>
    </section>

    <section id="about" class="fade-in">
        <div class="section-title">🙋 About Me</div>
        <div class="about-text">
            I'm a fresher passionate about backend development and automation using Python. I enjoy learning new technologies and applying them to solve real-world problems. I'm currently pursuing my MCA after completing my BCA and looking for opportunities to grow.
        </div>
        <div class="section-title" style="font-size:1.15rem;color:#555;margin-bottom:0.7rem;">Education</div>
        <div class="timeline">
            <div class="timeline-card">
                <div class="timeline-year">2022</div>
                <div>12th – Dasagram S.S Sikhshasadan</div>
            </div>
            <div class="timeline-card">
                <div class="timeline-year">2022–25</div>
                <div>BCA – Panskura Banamali College</div>
            </div>
            <div class="timeline-card">
                <div class="timeline-year">2025–ongoing</div>
                <div>MCA – Haldia Institute of Technology</div>
            </div>
        </div>
    </section>

    <section id="skills" class="fade-in">
        <div class="section-title">🛠 Skills</div>
        <div class="skills-list">
            <span class="skill-badge">🐍 Python</span>
            <span class="skill-badge">🌐 Django</span>
            <span class="skill-badge">🗄️ MySQL</span>
            <span class="skill-badge">📝 HTML</span>
            <span class="skill-badge">🎨 CSS</span>
            <span class="skill-badge">💻 C</span>
            <span class="skill-badge">📚 DSA</span>
        </div>
    </section>

    <section id="projects" class="fade-in">
        <div class="section-title">📂 Projects</div>
        <div class="projects-list">
            <div class="project-card">
                <div class="project-title">Online Quiz System</div>
                <div class="project-tech">Tech: HTML, CSS, JS, PHP, MySQL</div>
                <div class="project-role">Role: Designed and managed database</div>
                <div>A web app for quizzes</div>
            </div>
        </div>
    </section>

    <section id="services" class="fade-in">
        <div class="section-title">🧰 Services / Focus Areas</div>
        <div class="services-list">
            <div class="service-card">
                <span class="service-icon">🌐</span>
                <span>Web Development</span>
            </div>
            <div class="service-card">
                <span class="service-icon">⚙️</span>
                <span>Backend with Django</span>
            </div>
            <div class="service-card">
                <span class="service-icon">🗄️</span>
                <span>MySQL Database Design</span>
            </div>
        </div>
    </section>

    <section id="contact" class="fade-in">
        <div class="section-title">📞 Contact</div>
        <form class="contact-form" name="contact" method="POST" data-netlify="true">
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required>
            <label for="email">Email</label>
            <input type="email" id="email" name="email" required>
            <label for="message">Message</label>
            <textarea id="message" name="message" required></textarea>
            <button type="submit" class="btn">Send Message</button>
        </form>
        <div class="contact-details">
            <div>📧 Email: <a href="mailto:jsamanta2003@gmail.com">jsamanta2003@gmail.com</a></div>
            <div>📞 Phone: <a href="tel:+917865042543">+91 7865042543</a></div>
            <div>💻 GitHub: <a href="https://github.com/jayanta7865" target="_blank">github.com/jayanta7865</a></div>
            <div>🔗 LinkedIn: <a href="https://www.linkedin.com/in/jayanta-samanta-22a662330" target="_blank">jayanta-samanta</a></div>
        </div>
    </section>

    <footer>
        <div>© 2025 Jayanta Kumar Samanta</div>
        <div class="footer-social">
            <a href="mailto:jsamanta2003@gmail.com" title="Email"><span aria-label="Email">📧</span></a>
            <a href="https://github.com/jayanta7865" target="_blank" title="GitHub"><span aria-label="GitHub">💻</span></a>
            <!-- LinkedIn icon placeholder -->
            <a href="#" title="LinkedIn"><span aria-label="LinkedIn">🔗</span></a>
        </div>
    </footer>

    <script>
        // Hamburger menu
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        hamburger.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') navLinks.classList.toggle('active');
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    e.preventDefault();
                    target.scrollIntoView({ behavior: 'smooth' });
                    navLinks.classList.remove('active');
                }
            });
        });

        // Simple fade-in animation on scroll
        function fadeInOnScroll() {
            document.querySelectorAll('.fade-in').forEach(el => {
                const rect = el.getBoundingClientRect();
                if (rect.top < window.innerHeight - 50) {
                    el.style.animationPlayState = 'running';
                }
            });
        }
        window.addEventListener('scroll', fadeInOnScroll);
        window.addEventListener('load', fadeInOnScroll);

        // Light/Dark mode toggle
        const modeToggle = document.getElementById('modeToggle');
        modeToggle.addEventListener('click', () => {
            document.body.classList.toggle('dark');
            modeToggle.innerHTML = document.body.classList.contains('dark') ? '&#9790;' : '&#9788;';
        });

        // SEO: Add canonical link
        const link = document.createElement('link');
        link.rel = 'canonical';
        link.href = window.location.href;
        document.head.appendChild(link);
    </script>
</body>
</html>
</div>
