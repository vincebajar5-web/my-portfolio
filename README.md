1.75rem;
    box-shadow: 0 8px 20px rgba(33, 150, 243, 0.15);
    transition: box-shadow 0.3s ease;
  }
  .card:hover {
    box-shadow: 0 12px 30px rgba(33, 150, 243, 0.3);
  }
  .card h3 {
    color: #1a237e;
    margin-bottom: 0.7rem;
  }
  .card p {
    font-size: 1rem;
    color: #212121;
    margin-bottom: 0.85rem;
  }
  .card a {
    color: #0d47a1;
    font-weight: 600;
    text-decoration: none;
    font-size: 0.95rem;
  }
  .card a:hover {
    text-decoration: underline;
  }
  .cert-date {
    font-size: 0.85rem;
    color: #555;
    font-style: italic;
    margin-bottom: 0.6rem;
  }
  .contact-layout {
    display: flex;
    gap: 3rem;
    flex-wrap: wrap;
  }
  .contact-info {
    flex: 1;
    min-width: 260px;
    font-size: 1rem;
    color: #333;
  }
  .contact-info strong {
    color: #0d47a1;
  }
  .contact-form {
    flex: 1;
    min-width: 280px;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  .contact-form input,
  .contact-form textarea {
    padding: 0.75rem;
    border-radius: 8px;
    border: 2px solid #90caf9;
    font-size: 1rem;
    font-family: inherit;
    transition: border-color 0.3s ease;
  }
  .contact-form input:focus,
  .contact-form textarea:focus {
    border-color: #1976d2;
    outline: none;
  }
  .maintenance-note {
    margin-top: 3rem;
    background: #e3f2fd;
    padding: 1.5rem;
    border-radius: 12px;
    font-size: 0.95rem;
    color: #31708f;
  }
  .maintenance-note ul {
    margin-left: 1.5rem;
    margin-top: 0.5rem;
    list-style-type: disc;
  }
  footer {
    text-align: center;
    padding: 1.8rem 1rem;
    color: #444;
    font-size: 0.9rem;
    border-top: 1px solid #b3e5fc;
    margin-top: 3rem;
  }
  @media (max-width: 600px) {
    nav {
      flex-direction: column;
      gap: 1rem;
    }
    h1 {
      font-size: 2.2rem;
    }
    main {
      padding: 1.5rem 1.75rem;
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
    <h1>Hi, I'm Vince Jin B. Bajar.</h1>
    <p class="subtitle">I'm a Computer Science student learning software development, object-oriented programming, and web design.</p>
    <a href="#projects" class="button">See My Work</a>
  </section>
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
  <section id="contact">
    <h2>Contact</h2>
    <div class="contact-layout">
      <div class="contact-info">
        <p>Feel free to reach out if you have questions about my projects or want to connect.</p>
        <p><strong>Email:</strong> yourname@email.com</p>
        <p><strong>GitHub:</strong> github.com/yourusername</p>
      </div>
      <form class="contact-form" action="#" method="POST">
        <input type="text" name="name" placeholder="Name" required />
        <input type="email" name="email" placeholder="Email" required />
        <textarea name="message" rows="4" placeholder="Message" required></textarea>
        <button type="submit" class="button">Send</button>
      </form>
    </div>
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
