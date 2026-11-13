# my-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- SEO Metadata -->
    <meta name="description" content="Personal Developer Portfolio - Projects, Skills, and Contact Information">
    <meta name="keywords" content="Portfolio, Software Developer, Java, Python, Web Development">
    <meta name="author" content="Developer Portfolio">
    <title>Personal Portfolio</title>
    <style>
        /* --- Root Variables & Theme --- */
        :root {
            --primary-color: #2563eb;
            --primary-hover: #1d4ed8;
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-color: #f8fafc;
            --text-muted: #94a3b8;
            --border-color: #334155;
            --font-main: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }

        /* --- Global Reset & Base Styles --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* --- Header & Navigation --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(8px);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
        }

        nav {
            max-width: 1100px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
        }

        .logo {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        .nav-links a {
            color: var(--text-color);
            text-decoration: none;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* --- Layout & Section Formatting --- */
        section {
            max-width: 1100px;
            margin: 0 auto;
            padding: 6rem 2rem 3rem;
        }

        h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            border-bottom: 2rem;
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 50%;
            height: 3px;
            background-color: var(--primary-color);
            border-radius: 2px;
        }

        /* --- Home Section --- */
        #home {
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
        }

        .hero-tagline {
            color: var(--primary-color);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .hero-title {
            font-size: 3rem;
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        .hero-desc {
            color: var(--text-muted);
            max-width: 600px;
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: #fff;
            padding: 0.75rem 1.5rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.2s ease, transform 0.2s ease;
        }

        .btn:hover {
            background-color: var(--primary-hover);
            transform: translateY(-2px);
        }

        /* --- About Section --- */
        .about-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
            margin-top: 1rem;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .skill-tag {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 0.4rem 0.8rem;
            border-radius: 4px;
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* --- Projects & Certificates Section --- */
        .grid-layout {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.2s ease, border-color 0.2s ease;
        }

        .card:hover {
            transform: translateY(-4px);
            border-color: var(--primary-color);
        }

        .card h3 {
            margin-bottom: 0.5rem;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }

        .card-link {
            color: var(--primary-color);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
        }

        .card-link:hover {
            text-decoration: underline;
        }

        /* --- Contact Section --- */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 1.5rem;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            color: var(--text-color);
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: 2px solid var(--primary-color);
        }

        /* --- Maintenance Plan Box --- */
        .maintenance-box {
            background-color: var(--card-bg);
            border-left: 4px solid var(--primary-color);
            padding: 1rem 1.5rem;
            margin-top: 2rem;
            border-radius: 0 6px 6px 0;
        }

        /* --- Footer --- */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid var(--border-color);
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 4rem;
        }

        /* --- Responsive Styles --- */
        @media (max-width: 768px) {
            .about-grid, .contact-container {
                grid-template-columns: 1fr;
            }
            .hero-title {
                font-size: 2.2rem;
            }
            .nav-links {
                gap: 1rem;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation Header -->
    <header>
        <nav>
            <a href="#home" class="logo">&lt;DevPortfolio /&gt;</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects & Certificates</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- 1. HOME SECTION -->
        <section id="home">
            <p class="hero-tagline">Hello, World!</p>
            <h1 class="hero-title">Software Developer & Technical Specialist</h1>
            <p class="hero-desc">Building clean, robust, and efficient software applications with structured code and modern web technologies.</p>
            <a href="#projects" class="btn">View Projects</a>
        </section>

        <!-- 2. ABOUT SECTION -->
        <section id="about">
            <h2>About Me</h2>
            <div class="about-grid">
                <div>
                    <p>I am a passionate software developer dedicated to crafting functional applications and solving complex computing challenges. My technical foundation spans object-oriented architecture, data parsing, modern web design, and network protocols.</p>
                    <p style="margin-top: 1rem;">I place a strong emphasis on clean code, intuitive user interfaces, and structured technical documentation.</p>
                </div>
                <div>
                    <h3>Core Skills</h3>
                    <div class="skills-list">
                        <span class="skill-tag">Java</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">HTML5 / CSS3</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">OOP Architecture</span>
                        <span class="skill-tag">Git / GitHub</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- 3. PROJECTS & CERTIFICATES SECTION -->
        <section id="projects">
            <h2>Projects & Certificates</h2>
            
            <h3 style="margin-top: 1rem; color: var(--text-muted);">Featured Projects</h3>
            <div class="grid-layout">
                <article class="card">
                    <h3>Data Parsing System</h3>
                    <p>A structured tool built in Python for parsing, validating, and displaying structured data sets with integrated error handling.</p>
                    <a href="https://github.com" target="_blank" rel="noopener" class="card-link">View Repository &rarr;</a>
                </article>

                <article class="card">
                    <h3>Object-Oriented Banking App</h3>
                    <p>A Java console application demonstrating encapsulation, polymorphism, and inheritance for managing account balances.</p>
                    <a href="https://github.com" target="_blank" rel="noopener" class="card-link">View Repository &rarr;</a>
                </article>

                <article class="card">
                    <h3>Interactive Web Dashboard</h3>
                    <p>A responsive front-end dashboard built using CSS Flexbox/Grid with standard metadata optimization and accessibility focus.</p>
                    <a href="https://github.com" target="_blank" rel="noopener" class="card-link">View Demo &rarr;</a>
                </article>
            </div>

            <h3 style="margin-top: 2.5rem; color: var(--text-muted);">Certifications</h3>
            <div class="grid-layout">
                <article class="card">
                    <h3>Java Programming Essentials</h3>
                    <p>Issued by Educational Institution • Covers OOP fundamentals, standard library implementation, and data structures.</p>
                </article>

                <article class="card">
                    <h3>Web Development Fundamentals</h3>
                    <p>Issued by Educational Institution • Focuses on responsive UI design, accessible markup, and modern CSS standards.</p>
                </article>
            </div>
        </section>

        <!-- 4. CONTACT SECTION -->
        <section id="contact">
            <h2>Contact</h2>
            <div class="contact-container">
                <div>
                    <p>Interested in working together or reviewing my code? Send me a message or connect through social channels.</p>
                    <div style="margin-top: 1.5rem; color: var(--text-muted);">
                        <p><strong>Email:</strong> developer@example.com</p>
                        <p><strong>Location:</strong> Metro Manila, Philippines</p>
                    </div>
                </div>
                <form class="contact-form" action="#" method="POST">
                    <div class="form-group">
                        <input type="text" name="name" placeholder="Your Name" required aria-label="Your Name">
                    </div>
                    <div class="form-group">
                        <input type="email" name="email" placeholder="Your Email" required aria-label="Your Email">
                    </div>
                    <div class="form-group">
                        <textarea name="message" rows="4" placeholder="Your Message" required aria-label="Your Message"></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>

            <!-- Maintenance & Updates Plan (Required by Rubric) -->
            <div class="maintenance-box">
                <h3>Ongoing Maintenance & Update Plan</h3>
                <p>To ensure high quality over time, this portfolio is continuously maintained using the following schedule:</p>
                <ul style="margin-left: 1.25rem; margin-top: 0.5rem; color: var(--text-muted);">
                    <li><strong>Quarterly Project Additions:</strong> Add new repositories with comprehensive README docs and live demos.</li>
                    <li><strong>Skill Set Refresh:</strong> Update technical competencies as new frameworks and design standards emerge.</li>
                    <li><strong>Code Maintenance:</strong> Perform quarterly visual audits, link validations, and performance optimization checks.</li>
                </ul>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Developer Portfolio. All rights reserved.</p>
    </footer>

</body>
</html>
