<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shivam Jha | AIML Student & React Developer</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <nav id="navbar" class="nav">
    <div class="logo" tabindex="0">Shivam Jha</div>
    <ul class="nav-links">
      <li><a href="#about" class="nav-link active">About</a></li>
      <li><a href="#experience" class="nav-link">Experience</a></li>
      <li><a href="#projects" class="nav-link">Projects</a></li>
      <li><a href="#competitions" class="nav-link">Competitions</a></li>
      <li><a href="#contact" class="nav-link">Contact</a></li>
    </ul>
    <button id="theme-toggle" aria-label="Toggle dark/light mode" title="Toggle dark/light mode">
      🌙
    </button>
  </nav>

  <section class="hero section" id="hero" tabindex="0" aria-label="Introduction">
    <div class="container">
      <h1>Hi, I'm Shivam Jha</h1>
      <p>2nd year AIML student at Lamrin Tech Skills University, Punjab.<br />
        Passionate about coding and aspiring to become a React developer.</p>
      <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">
        Let's Connect
      </button>
    </div>
  </section>

  <section id="about" class="section container" tabindex="0" aria-labelledby="aboutHeading">
    <h2 id="aboutHeading">About Me</h2>
    <p>
      I am a 2nd-year student specializing in Artificial Intelligence and Machine Learning at Lamrin Tech Skills University, Punjab. I am passionate about coding and dedicated to becoming a skilled React developer in the future.
    </p>
    <p>
      I have hands-on experience building various machine learning models, including NLP and CNN models, and have developed full-stack web applications.
    </p>
  </section>

  <section id="experience" class="section container" tabindex="0" aria-labelledby="experienceHeading">
    <h2 id="experienceHeading">Experience</h2>
    <ul>
      <li><strong>Full Stack Web Development Intern</strong> at Pantech.ai Solutions</li>
      <li><strong>Data Analytics Intern</strong> at Accenture Forage</li>
    </ul>
  </section>

  <section id="projects" class="section container" tabindex="0" aria-labelledby="projectsHeading">
    <h2 id="projectsHeading">Projects</h2>
    <div class="projects-grid" id="projectsGrid"></div>
  </section>

  <section id="competitions" class="section container" tabindex="0" aria-labelledby="competitionsHeading">
    <h2 id="competitionsHeading">Competitions & Hackathons</h2>
    <ul>
      <li>International Robotics Competition – 2nd Position at State Level</li>
      <li>Participated in Hackathons and Ideathons at Amity University, Chitkara University, CT University, IIT Delhi, GNA University, and more</li>
    </ul>
  </section>

  <section id="contact" class="section container" tabindex="0" aria-labelledby="contactHeading">
    <h2 id="contactHeading">Contact Me</h2>
    <form id="contactForm" novalidate>
      <input type="text" id="name" placeholder="Your Name" required aria-required="true" />
      <input type="email" id="email" placeholder="Your Email" required aria-required="true" />
      <textarea id="message" rows="5" placeholder="Your Message" required aria-required="true"></textarea>
      <button type="submit" class="btn-primary">Send</button>
    </form>
  </section>

  <script src="script.js"></script>
</body>
</html>
/* Import Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');

/* CSS Variables for light and dark mode */
:root {
  --color-bg: #f9fafc;
  --color-text: #1e293b;
  --color-primary: #2563eb;
  --color-primary-hover: #1e40af;
  --color-bg-section: #ffffff;
  --color-shadow: rgba(0, 0, 0, 0.07);
  --color-btn-text: #f1f5f9;
  --transition-speed: 0.3s;
}

[data-theme="dark"] {
  --color-bg: #121827;
  --color-text: #e0e7ff;
  --color-primary: #3b82f6;
  --color-primary-hover: #60a5fa;
  --color-bg-section: #1e293b;
  --color-shadow: rgba(0, 0, 0, 0.5);
  --color-btn-text: #f1f5f9;
}

/* Base styles */
*,
*::before,
*::after {
  box-sizing: border-box;
}
body {
  margin: 0;
  font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: var(--color-bg);
  color: var(--color-text);
  line-height: 1.6;
  scroll-behavior: smooth;
  transition: background-color var(--transition-speed), color var(--transition-speed);
}
a {
  color: var(--color-primary);
  text-decoration: none;
  transition: color var(--transition-speed);
}
a:hover,
a:focus {
  color: var(--color-primary-hover);
  outline: none;
}

/* Container */
.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 0 1rem;
}

/* Navbar */
nav.nav {
  position: fixed;
  top: 0;
  width: 100%;
  background-color: var(--color-bg-section);
  box-shadow: 0 2px 8px var(--color-shadow);
  z-index: 9999;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  transition: background-color var(--transition-speed), box-shadow var(--transition-speed);
}
nav.nav.scrolled {
  box-shadow: 0 4px 20px var(--color-shadow);
}
nav .logo {
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--color-primary);
  letter-spacing: 2px;
  user-select: none;
}
nav ul.nav-links {
  list-style: none;
  display: flex;
  gap: 2rem;
  margin: 0;
}
nav ul.nav-links li {
  font-weight: 600;
}
nav ul.nav-links li a.nav-link {
  font-size: 1rem;
  padding: 0.3rem 0.5rem;
  border-radius: 4px;
  transition: background-color var(--transition-speed), color var(--transition-speed);
  color: var(--color-text);
}
nav ul.nav-links li a.nav-link.active,
nav ul.nav-links li a.nav-link:hover,
nav ul.nav-links li a.nav-link:focus {
  background-color: var(--color-primary);
  color: var(--color-btn-text);
  outline: none;
}

/* Theme toggle button */
#theme-toggle {
  background: transparent;
  border: none;
  font-size: 1.4rem;
  cursor: pointer;
  color: var(--color-primary);
  transition: color var(--transition-speed);
  user-select: none;
}
#theme-toggle:hover,
#theme-toggle:focus {
  color: var(--color-primary-hover);
  outline: none;
}

/* Hero Section */
.hero.section {
  height: 100vh;
  background: linear-gradient(135deg, var(--color-primary) 0%, #3b82f6 100%);
  color: var(--color-btn-text);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 0 1rem;
  user-select: none;
  transition: background-color var(--transition-speed);
}
.hero h1 {
  font-size: 3.5rem;
  font-weight: 800;
  margin-bottom: 1rem;
  letter-spacing: 3px;
  line-height: 1.1;
  text-shadow: 0 2px 8px rgba(0,0,0,0.25);
}
.hero p {
  font-size: 1.3rem;
  max-width: 600px;
  margin-bottom: 2.5rem;
  font-weight: 500;
  text-shadow: 0 1px 4px rgba(0,0,0,0.2);
}

/* Buttons */
.btn-primary {
  background-color: var(--color-btn-text);
  color: var(--color-primary);
  padding: 0.9rem 2.5rem;
  font-size: 1.2rem;
  font-weight: 700;
  border: none;
  border-radius: 40px;
  cursor: pointer;
  box-shadow: 0 6px 15px rgba(255,255,255,0.8);
  transition: background-color var(--transition-speed), color var(--transition-speed), box-shadow var(--transition-speed);
  text-transform: uppercase;
  letter-spacing: 2px;
  user-select: none;
}
.btn-primary:hover,
.btn-primary:focus {
  background-color: var(--color-primary-hover);
  color: var(--color-btn-text);
  box-shadow: 0 8px 25px rgba(30,64,175,0.8);
  outline: none;
}

/* Sections */
.section {
  background-color: var(--color-bg-section);
  border-radius: 12px;
  padding: 3rem 2rem;
  margin: 6rem auto 4rem;
  box-shadow: 0 6px 20px var(--color-shadow);
  max-width: 900px;
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}
.section.visible {
  opacity: 1;
  transform: translateY(0);
}
.section h2 {
  color: var(--color-primary);
  font-weight: 700;
  font-size: 2.25rem;
  margin-bottom: 1.5rem;
  border-bottom: 3px solid var(--color-primary);
  padding-bottom: 0.3rem;
  user-select: none;
}
.section p {
  font-size: 1.1rem;
  color: var(--color-text);
  margin-bottom: 1.3rem;
  font-weight: 500;
}
.section ul {
  list-style: disc inside;
  margin-bottom: 1.5rem;
  color: var(--color-text);
  font-weight: 600;
}
.section ul li {
  margin-bottom: 0.8rem;
}

/* Projects Grid */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
  gap: 2rem;
}
.project-card {
  background-color: #f1f5f9;
  border-radius: 12px;
  padding: 1.8rem 1.5rem;
  box-shadow: 0 4px 12px rgba(0,0,0,0.07);
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  user-select: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.project-card:hover,
.project-card:focus-within {
  transform: translateY(-10px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  outline: none;
}
.project-card h3 {
  color: #1e40af;
  font-weight: 700;
  margin-bottom: 1rem;
  font-size: 1.25rem;
}
.project-card p {
  color: #475569;
  font-weight: 500;
  line-height: 1.4;
  flex-grow: 1;
}

/* Contact Form */
form {
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}
form input,
form textarea {
  padding: 1rem 1.2rem;
  border-radius: 10px;
  border: 2px solid #cbd5e1;
  font-size: 1rem;
  font-weight: 500;
  color: #334155;
  transition: border-color var(--transition-speed), box-shadow var(--transition-speed);
  resize: vertical;
  font-family: inherit;
  background-color: var(--color-bg-section);
  transition: background-color var(--transition-speed), border-color var(--transition-speed);
}
form input:focus,
form textarea:focus {
  border-color: var(--color-primary);
  box-shadow: 0 0 8px rgba(37, 99, 235, 0.4);
  outline: none;
}
form button {
  width: 160px;
  background-color: var(--color-primary);
  color: var(--color-btn-text);
  font-weight: 700;
  font-size: 1.1rem;
  padding: 0.9rem 2rem;
  border: none;
  border-radius: 40px;
  cursor: pointer;
  align-self: flex-start;
  transition: background-color var(--transition-speed), box-shadow var(--transition-speed);
  user-select: none;
}
form button:hover,
form button:focus {
  background-color: var(--color-primary-hover);
  box-shadow: 0 8px 25px rgba(30,64,175,0.7);
  outline: none;
}

/* Responsive */
@media (max-width: 600px) {
  nav ul.nav-links {
    gap: 1rem;
  }
  .hero h1 {
    font-size: 2.5rem;
  }
  .section {
    margin: 4rem 1rem 3rem;
    padding: 2rem 1.5rem;
  }
  .projects-grid {
    grid-template-columns: 1fr;
  }
  form button {
    width: 100%;
  }
}
// Projects data
const projects = [
    {
      title: "NLP Model",
      description: "Developed an NLP model for text analysis as part of AIML specialization."
    },
    {
      title: "CNN for Signature Verification",
      description: "Built a CNN model to verify signatures for banking fraud prevention."
    },
    {
      title: "Website Clones",
      description: "Created clones of popular websites like Netflix, Uber, Amazon, and more."
    },
    {
      title: "LLM-based Deep Learning",
      description: "Worked on projects training deep learning models with large language models."
    }
  ];
  
  // Render projects dynamically
  const projectsGrid = document.getElementById('projectsGrid');
  projects.forEach(proj => {
    const card = document.createElement('div');
    card.className = 'project-card';
    card.tabIndex = 0;
    card.innerHTML = `
      <h3>${proj.title}</h3>
      <p>${proj.description}</p>
    `;
    projectsGrid.appendChild(card);
  });
  
  // Highlight active nav link on scroll
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('nav ul.nav-links li a');
  
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
      const sectionTop = section.offsetTop - 90;
      if (pageYOffset >= sectionTop) {
        current = section.getAttribute('id');
      }
    });
    navLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href').substring(1) === current) {
        link.classList.add('active');
      }
    });
  
    // Navbar shadow on scroll
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 10) {
      navbar.classList.add('scrolled');
    } else {
      navbar.classList.remove('scrolled');
    }
  });
  
  // Animate sections on scroll
  const observerOptions = {
    threshold: 0.15
  };
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, observerOptions);
  
  document.querySelectorAll('.section').forEach(section => {
    observer.observe(section);
  });
  
  // Theme toggle
  const themeToggleBtn = document.getElementById('theme-toggle');
  const prefersDark = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches;
  
  function setTheme(theme) {
    if (theme === 'dark') {
      document.documentElement.setAttribute('data-theme', 'dark');
      themeToggleBtn.textContent = '☀️';
    } else {
      document.documentElement.removeAttribute('data-theme');
      themeToggleBtn.textContent = '🌙';
    }
    localStorage.setItem('theme', theme);
  }
  
  // Initialize theme
  const savedTheme = localStorage.getItem('theme');
  if (savedTheme) {
    setTheme(savedTheme);
  } else if (prefersDark) {
    setTheme('dark');
  } else {
    setTheme('light');
  }
  
  themeToggleBtn.addEventListener('click', () => {
    const currentTheme = document.documentElement.getAttribute('data-theme');
    if (currentTheme === 'dark') {
      setTheme('light');
    } else {
      setTheme('dark');
    }
  });
  
  // Contact form validation and submission
  document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();
  
    const name = this.name.value.trim();
    const email = this.email.value.trim();
    const message = this.message.value.trim();
  
    if (!name || !email || !message) {
      alert('Please fill in all fields.');
      return;
    }
  
    // Basic email regex validation
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (!emailRegex.test(email)) {
      alert('Please enter a valid email address.');
      return;
    }
  
    alert(`Thank you, ${name}! Your message has been received.`);
    this.reset();
  });
  
