<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Personal portfolio showcasing programming projects, certificates, and skills.">
    <title>My Portfolio</title>
    <style>
        /* Basic Reset */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: #fafafa;
            color: #222222;
            line-height: 1.6;
        }

        /* Navigation */
        header {
            background-color: #ffffff;
            border-bottom: 1px solid #e5e5e5;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            max-width: 960px;
            margin: 0 auto;
            padding: 1rem 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .site-title {
            font-weight: 700;
            font-size: 1.1rem;
            color: #111111;
            text-decoration: none;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 1.5rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #555555;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: #0056b3;
        }

        /* Main Container & Sections */
        main {
            max-width: 960px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        section {
            padding: 4rem 0;
            border-bottom: 1px solid #eaeaea;
        }

        section:last-of-type {
            border-bottom: none;
        }

        h1 {
            font-size: 2.5rem;
            color: #111111;
            margin-bottom: 0.75rem;
        }

        h2 {
            font-size: 1.75rem;
            color: #111111;
            margin-bottom: 1.25rem;
        }

        h3 {
            font-size: 1.15rem;
            color: #222222;
            margin-bottom: 0.5rem;
        }

        p {
            color: #444444;
            margin-bottom: 1rem;
        }

        /* Home Section */
        #home {
            padding: 6rem 0;
        }

        .subtitle {
            font-size: 1.15rem;
            color: #555555;
            max-width: 600px;
            margin-bottom: 1.75rem;
        }

        .button {
            display: inline-block;
            background-color: #0056b3;
            color: #ffffff;
            padding: 0.65rem 1.25rem;
            text-decoration: none;
            border-radius: 5px;
            font-size: 0.95rem;
            font-weight: 500;
            border: none;
            cursor: pointer;
        }

        .button:hover {
            background-color: #004494;
        }

        /* About & Skills */
        .about-content {
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 2;
            min-width: 280px;
        }

        .about-skills {
            flex: 1;
            min-width: 220px;
        }

        .skills-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }

        .skills-list li {
            background-color: #efefef;
            color: #333333;
            padding: 0.35rem 0.75rem;
            border-radius: 4px;
            font-size: 0.85rem;
        }

        /* Projects & Certificates Grid */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
            margin-bottom: 2.5rem;
        }

        .card {
            background-color: #ffffff;
            border: 1px solid #e0e0e0;
            border-radius: 6px;
            padding: 1.25rem;
        }

        .card p {
            font-size: 0.92rem;
            margin-bottom: 0.75rem;
        }

        .card a {
            color: #0056b3;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
        }

        .card a:hover {
            text-decoration: underline;
        }

        .cert-date {
            font-size: 0.85rem;
            color: #777777;
        }

        /* Contact & Maintenance */
        .contact-layout {
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .contact-info {
            flex: 1;
            min-width: 250px;
        }

        .contact-form {
            flex: 1;
            min-width: 280px;
            display: flex;
            flex-direction: column;
            gap: 0.85rem;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 0.65rem;
            border: 1px solid #cccccc;
            border-radius: 4px;
            font-family: inherit;
            font-size: 0.95rem;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #0056b3;
        }

        .maintenance-note {
            margin-top: 3rem;
            padding: 1.25rem;
            background-color: #f1f5f9;
            border-radius: 6px;
            font-size: 0.92rem;
        }

        .maintenance-note ul {
            margin-left: 1.25rem;
            margin-top: 0.5rem;
            color: #444444;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem 1rem;
            color: #777777;
            font-size: 0.85rem;
            border-top: 1px solid #eaeaea;
        }

        /* Mobile Adjustments */
        @media (max-width: 600px) {
            nav {
                flex-direction: column;
                gap: 0.75rem;
            }
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <a href="#home" class="site-title"> MY FORTFOLIO</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects & Certificates</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Home Section -->
        <section id="home">
            <h1>Hi, I'm Vince jin b. bajar.</h1>
            <p class="subtitle">I'm an Computer Science student learning software development, object-oriented programming, and web design.</p>
            <a href="#projects" class="button">See My Work</a>
        </section>

        <!-- About Section -->
        <section id="about">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I am currently studying programming and software development, focusing on writing clean, readable code and building practical applications. I enjoy breaking down technical problems and learning how different systems work together.</p>
                    <p>Right now, I am sharpening my skills in Java, Python, and front-end web development while building small projects to apply what I learn in class.</p>
                </div>
                <div class="about-skills">
                    <h3>Skills</h3>
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

        <!-- Projects & Certificates Section -->
        <section id="projects">
            <h2>Projects & Certificates</h2>
            
            <h3>Projects</h3>
            <div class="grid">
                <div class="card">
                    <h3>Data Parser Tool</h3>
                    <p>A Python script that reads, validates, and organizes raw text files into clean, structured output.</p>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </div>

                <div class="card">
                    <h3>Simple Banking System</h3>
                    <p>A console-based Java program created to practice object-oriented concepts like encapsulation and inheritance.</p>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </div>

                <div class="card">
                    <h3>Personal Portfolio Website</h3>
                    <p>A responsive single-page website built using semantic HTML, CSS Flexbox, and CSS Grid.</p>
                    <a href="https://github.com" target="_blank" rel="noopener">View on GitHub &rarr;</a>
                </div>
            </div>

            <h3>Certificates</h3>
            <div class="grid">
                <div class="card">
                    <h3>Java Programming Basics</h3>
                    <p class="cert-date">Completed 2026</p>
                    <p>Covered core syntax, data types, loops, and object-oriented programming fundamentals.</p>
                </div>

                <div class="card">
                    <h3>Responsive Web Design</h3>
                    <p class="cert-date">Completed 2026</p>
                    <p>Focused on accessible HTML structure, CSS layouts, and mobile-friendly design.</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
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
                    <button type="submit" class="button">Send</button>
                </form>
            </div>

            <!-- Maintenance Plan for Grading Rubric -->
            <div class="maintenance-note">
                <strong>Site Maintenance Plan:</strong>
                <ul>
                    <li>Update the projects section each semester with new coursework and personal coding projects.</li>
                    <li>Check all external GitHub links and test mobile responsiveness whenever new content is added.</li>
                    <li>Add new certificates and update my skills list as I learn new programming languages.</li>
                </ul>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 sana pasado</p>
    </footer>

</body>
</html>
