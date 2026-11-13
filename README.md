<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Personal portfolio showcasing programming projects, certificates, and skills.">
    <title>Vince Jin B. Bajar | Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-main: #0f172a;
            --bg-surface: #1e293b;
            --bg-surface-hover: #283548;
            --text-primary: #f8fafc;
            --text-secondary: #94a3b8;
            --accent-primary: #38bdf8;
            --accent-secondary: #818cf8;
            --accent-tertiary: #f472b6;
            --gradient-main: linear-gradient(135deg, #38bdf8 0%, #818cf8 50%, #f472b6 100%);
            --border-color: rgba(255, 255, 255, 0.1);
            --radius: 12px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
            background-color: var(--bg-main);
            color: var(--text-primary);
            line-height: 1.7;
            background-image: 
                radial-gradient(circle at 15% 15%, rgba(56, 189, 248, 0.12) 0%, transparent 40%),
                radial-gradient(circle at 85% 35%, rgba(244, 114, 182, 0.1) 0%, transparent 40%);
        }

        header {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            max-width: 1040px;
            margin: 0 auto;
            padding: 1.1rem 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .site-title {
            font-weight: 800;
            font-size: 1.25rem;
            letter-spacing: 0.5px;
            background: var(--gradient-main);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-secondary);
            font-size: 0.95rem;
            font-weight: 500;
            transition: color 0.25s ease;
        }

        .nav-links a:hover {
            color: var(--accent-primary);
        }

        main {
            max-width: 1040px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        section {
            padding: 5rem 0;
            border-bottom: 1px solid var(--border-color);
        }

        section:last-of-type {
            border-bottom: none;
        }

        h1 {
            font-size: clamp(2.2rem, 5vw, 3.5rem);
            font-weight: 800;
            line-height: 1.15;
            margin-bottom: 1rem;
        }

        .highlight {
            background: var(--gradient-main);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        h2 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.75rem;
            display: inline-block;
            position: relative;
        }

        h2::after {
            content: '';
            display: block;
            width: 50%;
            height: 4px;
            background: var(--gradient-main);
            border-radius: 2px;
            margin-top: 0.4rem;
        }

        h3 {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.6rem;
            color: var(--text-primary);
        }

        .section-subhead {
            color: var(--accent-primary);
            text-transform: uppercase;
            letter-spacing: 1.5px;
            font-size: 0.85rem;
            font-weight: 700;
            margin: 2rem 0 1rem;
        }

        p {
            color: var(--text-secondary);
            margin-bottom: 1.1rem;
        }

        #home {
            padding: 7rem 0;
        }

        .subtitle {
            font-size: 1.2rem;
            max-width: 620px;
            margin-bottom: 2.25rem;
        }

        .button {
            display: inline-block;
            background: var(--gradient-main);
            color: #0f172a;
            padding: 0.8rem 1.75rem;
            text-decoration: none;
            border-radius: 8px;
            font-size: 0.95rem;
            font-weight: 700;
            border: none;
            cursor: pointer;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px -5px rgba(56, 189, 248, 0.4);
        }

        .about-content {
            display: flex;
            gap: 3.5rem;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 2;
            min-width: 280px;
        }

        .about-skills {
            flex: 1;
            min-width: 240px;
        }

        .skills-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 0.65rem;
            margin-top: 0.75rem;
        }

        .skills-list li {
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            color: var(--accent-primary);
            padding: 0.45rem 0.9rem;
            border-radius: 999px;
            font-size: 0.85rem;
            font-weight: 600;
            transition: all 0.2s ease;
        }

        .skills-list li:hover {
            border-color: var(--accent-primary);
            background: rgba(56, 189, 248, 0.1);
            transform: translateY(-2px);
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
            gap: 1.75rem;
            margin-bottom: 2.5rem;
        }

        .card {
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-top: 3px solid var(--accent-primary);
            border-radius: var(--radius);
            padding: 1.75rem;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: transform 0.25s ease, background 0.25s ease, box-shadow 0.25s ease;
        }

        .card:nth-child(2) {
            border-top-color: var(--accent-secondary);
        }

        .card:nth-child(3) {
            border-top-color: var(--accent-tertiary);
        }

        .card:hover {
            transform: translateY(-5px);
            background: var(--bg-surface-hover);
            box-shadow: 0 15px 30px -10px rgba(0, 0, 0, 0.4);
        }

        .card p {
            font-size: 0.95rem;
            margin-bottom: 1.25rem;
        }

        .card a {
            color: var(--accent-primary);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 0.35rem;
        }

        .card a:hover {
            color: var(--accent-tertiary);
        }

        .badge {
            display: inline-block;
            background: rgba(129, 140, 248, 0.15);
            color: var(--accent-secondary);
            padding: 0.25rem 0.65rem;
            border-radius: 6px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
            width: fit-content;
        }

        .contact-layout {
            display: flex;
            gap: 3.5rem;
            flex-wrap: wrap;
        }

        .contact-info {
            flex: 1;
            min-width: 260px;
        }

        .contact-info strong {
            color: var(--text-primary);
        }

        .contact-form {
            flex: 1.2;
            min-width: 280px;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 0.85rem 1rem;
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            color: var(--text-primary);
            font-family: inherit;
            font-size: 0.95rem;
            transition: border-color 0.2s ease, box-shadow 0.2s ease;
        }

        .contact-form input::placeholder,
        .contact-form textarea::placeholder {
            color: var(--text-secondary);
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--accent-primary);
            box-shadow: 0 0 0 3px rgba(56, 189, 248, 0.15);
        }

        .maintenance-note {
            margin-top: 4rem;
            padding: 1.5rem 1.75rem;
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.08), rgba(129, 140, 248, 0.08));
            border: 1px solid rgba(56, 189, 248, 0.25);
            border-radius: var(--radius);
            font-size: 0.95rem;
        }

        .maintenance-note strong {
            color: var(--accent-primary);
            display: block;
            margin-bottom: 0.5rem;
        }

        .maintenance-note ul {
            margin-left: 1.25rem;
            color: var(--text-secondary);
        }

        .maintenance-note li {
            margin-bottom: 0.35rem;
        }

        footer {
            text-align: center;
            padding: 2.5rem 1rem;
            color: var(--text-secondary);
            font-size: 0.9rem;
            border-top: 1px solid var(--border-color);
        }

        @media (max-width: 640px) {
            nav {
                flex-direction: column;
                gap: 0.85rem;
            }
            .nav-links {
                gap: 1.1rem;
                font-size: 0.9rem;
            }
            #home {
                padding: 4.5rem 0;
            }
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <a href="#home" class="site-title">MY PORTFOLIO</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects & Certificates</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home">
            <h1>Hi, I'm <span class="highlight">Vince Jin B. Bajar.</span></h1>
            <p class="subtitle">I'm a Computer Science student passionate about software development, object-oriented programming, and colorful web design.</p>
            <a href="#projects" class="button">See My Work</a>
        </section>

        <section id="about">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I am currently studying programming and software development, focusing on writing clean, readable code and building practical applications. I enjoy breaking down technical problems and learning how different systems work together.</p>
                    <p>Right now, I am sharpening my skills in Java, Python, and front-end web development while building projects to apply what I learn in class.</p>
                </div>
                <div class="about-skills">
                    <h3>Tech Stack & Skills</h3>
                    <ul class="skills-list">
                        <li>Java</li>
                        <li>Python</li>
                        <li>HTML & CSS</li>
                        <li>JavaScript</li>
                        <li>OOP</li>
                        <li>Git & GitHub</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="projects">
            <h2>Projects & Certificates</h2>
            
            <p class="section-subhead">Featured Projects</p>
            <div class="grid">
                <article class="card">
                    <div>
                        <h3>Data Parser Tool</h3>
                        <p>A Python script that reads, validates, and organizes raw text files into clean, structured output.</p>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </article>

                <article class="card">
                    <div>
                        <h3>Simple Banking System</h3>
                        <p>A console-based Java program created to practice object-oriented concepts like encapsulation and inheritance.</p>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </article>

                <article class="card">
                    <div>
                        <h3>Personal Portfolio Website</h3>
                        <p>A responsive single-page website built using semantic HTML, CSS Flexbox, and CSS Grid.</p>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </article>
            </div>

            <p class="section-subhead">Certificates</p>
            <div class="grid">
                <article class="card">
                    <div>
                        <span class="badge">Completed 2026</span>
                        <h3>Java Programming Basics</h3>
                        <p>Covered core syntax, data types, loops, and object-oriented programming fundamentals.</p>
                    </div>
                </article>

                <article class="card">
                    <div>
                        <span class="badge">Completed 2026</span>
                        <h3>Responsive Web Design</h3>
                        <p>Focused on accessible HTML structure, modern CSS layouts, and mobile-friendly design.</p>
                    </div>
                </article>
            </div>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            <div class="contact-layout">
                <div class="contact-info">
                    <p>Feel free to reach out if you have questions about my projects or want to connect.</p>
                    <p><strong>Email:</strong> yourname@email.com</p>
                    <p><strong>GitHub:</strong> github.com/yourusername</p>
                </div>

                <form class="contact-form" action="#" method="POST">
                    <input type="text" name="name" placeholder="Name" required>
                    <input type="email" name="email" placeholder="Email" required>
                    <textarea name="message" rows="4" placeholder="Message" required></textarea>
                    <button type="submit" class="button">Send Message</button>
                </form>
            </div>

            <aside class="maintenance-note">
                <strong>Site Maintenance Plan</strong>
                <ul>
                    <li>Update the projects section each semester with new coursework and personal coding projects.</li>
                    <li>Check all external GitHub links and test mobile responsiveness whenever new content is added.</li>
                    <li>Add new certificates and update my skills list as I learn new programming languages.</li>
                </ul>
            </aside>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Vince Jin B. Bajar &bull; Sana Pasado</p>
    </footer>

</body>
</html>
