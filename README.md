<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">  <!-- ← CSS connected here -->
    <title>Portfolio | Jesse</title>
</head>
<body>

    <header class="header">
        <a href="#home" class="logo">Jesse</a>

        <nav class="navbar">
            <a href="#home" class="active">Home</a>
            <a href="#services">Services</a>
            <a href="#skills">Skills</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section id="home" class="home">
        <div class="home-img">
            <img src="images/main.jpg" alt="Shadowed man walking down a street">
        </div>

        <div class="home-content">
            <h1>Hello, I'm <span>Jesse</span></h1>
            <h3 class="typing-text">I'm an <span>artist and IT student.</span></h3>
            <p>
                Welcome to my portfolio website! I'm passionate about creating art and exploring the world of 
                information technology. Here, you will find a showcase of my work and skills.
                Feel free to browse through my projects and get in touch if you'd like to collaborate or learn more about me.
            </p>

            <div class="btn-group">
                <a href="#projects" class="btn primary-btn">View Projects</a>
                <a href="#contact" class="btn outline-btn">Contact Me</a>
            </div>

            <div class="social-icons">
              <img
                src="images/facebook-icon.png"
                class="contact-icon"
                alt=""
                aria-hidden="true"
              />
            </div>
            <div class="social-icons">
              <img
                src="images/instagram-icon.png"
                class="contact-icon"
                alt=""
                aria-hidden="true"
              />
            </div>
            <div class="social-icons">
              <img
                src="images/x-twitter-icon.png"
                class="contact-icon"
                alt=""
                aria-hidden="true"
              />
            </div>
            <div class="social-icons">
              <img
                src="images/github-icon.png"
                class="contact-icon"
                alt=""
                aria-hidden="true"
              />
            </div>
        </div>
    </section>

:root {
    --bg-main: #020203;
    --bg-panel: #0d0d0f;
    --bg-panel-soft: #141416;

    --ink-main: #f5f5f5;
    --ink-muted: #a0a0a0;
    --ink-soft: #c6c6c6;

    --accent: #e0ded2;
    --accent-muted: #8e8b7d;

    --border-subtle: #26262a;
    --shadow-soft: 0 18px 40px rgba(0, 0, 0, 0.9);
    --shadow-strong: 0 30px 80px rgba(0, 0, 0, 0.98);

    --font-heading: "Georgia", "Times New Roman", serif;
    --font-body: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;

    scroll-behavior: smooth;
}

*,
*::before,
*::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    font-size: 16px;
}

body {
    position: relative;
    font-family: var(--font-body);
    color: var(--ink-main);
    background-color: var(--bg-main);
    background-image:
        radial-gradient(circle at top, #28282c 0, #050508 45%, #000 100%);
    line-height: 1.6;
    padding-top: 4.4rem;
    overflow-x: hidden;
}

body::before {
    content: "";
    pointer-events: none;
    position: fixed;
    inset: -20px;
    opacity: 0.12;
    mix-blend-mode: soft-light;
    background-image:
        repeating-linear-gradient(
            0deg,
            rgba(255, 255, 255, 0.06) 0px,
            rgba(255, 255, 255, 0.06) 1px,
            transparent 1px,
            transparent 3px
        ),
        repeating-linear-gradient(
            90deg,
            rgba(0, 0, 0, 0.4) 0px,
            rgba(0, 0, 0, 0.4) 2px,
            transparent 2px,
            transparent 4px
        );
    z-index: -1;
}

section {
    padding: 5.5rem 7vw;
}

.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 1rem 7vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(3, 3, 5, 0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    box-shadow: 0 16px 45px rgba(0, 0, 0, 0.95);
    z-index: 50;
}

.logo {
    font-family: var(--font-heading);
    font-size: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.18em;
    color: var(--ink-main);
    text-decoration: none;
}

.navbar {
    display: flex;
    gap: 1.6rem;
}

.navbar a {
    position: relative;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 0.78rem;
    letter-spacing: 0.22em;
    color: var(--ink-muted);
    padding-bottom: 0.1rem;
    transition: color 0.25s ease;
}

.navbar a::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -0.35rem;
    width: 0;
    height: 2px;
    background: var(--accent);
    transition: width 0.25s ease;
}

.navbar a:hover,
.navbar a.active {
    color: var(--accent);
}

.navbar a:hover::after,
.navbar a.active::after {
    width: 100%;
}

.home {
    min-height: calc(100vh - 4.4rem);
    display: grid;
    grid-template-columns: minmax(0, 1.1fr) minmax(0, 1.3fr);
    gap: 3.2rem;
    align-items: center;
}

.home-content {
    position: relative;
}

.home-content::before {
    content: "";
    position: absolute;
    inset: -40px;
    background: radial-gradient(circle at left, rgba(255, 255, 255, 0.12), transparent 60%);
    opacity: 0.6;
    mix-blend-mode: soft-light;
    z-index: -1;
}

.home-img {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

.home-img img {
    max-width: 320px;
    width: 100%;
    border-radius: 1rem;
    border: 1px solid var(--border-subtle);
    box-shadow: var(--shadow-soft);
    filter: grayscale(100%) contrast(1.35) brightness(0.9);
    transform: translateY(0);
    transition:
        transform 0.5s ease,
        filter 0.5s ease,
        box-shadow 0.5s ease;
}

.home-img::before {
    content: "";
    position: absolute;
    inset: 5%;
    background-image: repeating-linear-gradient(
        to bottom,
        rgba(0, 0, 0, 0.75) 0,
        rgba(0, 0, 0, 0.75) 4px,
        transparent 4px,
        transparent 10px
    );
    mix-blend-mode: multiply;
    opacity: 0.6;
    pointer-events: none;
    transition: opacity 0.5s ease;
}

.home-img:hover img {
    transform: translateY(-8px) scale(1.03);
    filter: grayscale(30%) contrast(1.1) brightness(1);
    box-shadow: var(--shadow-strong);
}

.home-img:hover::before {
    opacity: 0.2;
}

.home-content h1 {
    font-family: var(--font-heading);
    font-size: 2.5rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.6rem;
}

.home-content h1 span {
    color: var(--accent);
}

.typing-text {
    font-size: 0.9rem;
    text-transform: uppercase;
    letter-spacing: 0.32em;
    color: var(--ink-muted);
    margin-bottom: 1.4rem;
}

.typing-text span {
    color: var(--accent-muted);
}

.home-content p {
    max-width: 620px;
    font-size: 0.97rem;
    color: var(--ink-soft);
}


.btn-group {
    display: flex;
    flex-wrap: wrap;
    gap: 0.9rem;
    margin: 2rem 0 1.4rem;
}

.btn {
    display: inline-block;
    padding: 0.8rem 1.8rem;
    border-radius: 999px;
    text-transform: uppercase;
    font-size: 0.74rem;
    letter-spacing: 0.24em;
    border: 1px solid var(--border-subtle);
    text-decoration: none;
    cursor: pointer;
    transition:
        background-color 0.25s ease,
        color 0.25s ease,
        transform 0.2s ease,
        border-color 0.25s ease,
        box-shadow 0.25s ease;
}

.primary-btn {
    background-color: var(--accent-muted);
    color: #111111;
    border-color: var(--accent-muted);
}

.primary-btn:hover {
    background-color: var(--accent);
    color: #050505;
    transform: translateY(-3px);
    box-shadow: 0 16px 40px rgba(0, 0, 0, 0.95);
}

.outline-btn {
    background-color: transparent;
    color: var(--ink-main);
}

.outline-btn:hover {
    background-color: #151515;
    color: var(--accent);
    border-color: var(--accent);
    transform: translateY(-3px);
}


.social-icons {
    display: flex;
    gap: 0.8rem;
}

.social-icons a {
    width: 2.3rem;
    height: 2.3rem;
    border-radius: 50%;
    border: 1px solid var(--border-subtle);
    display: inline-flex;
    align-items: center;
    justify-content: center;
    color: var(--ink-muted);
    text-decoration: none;
    font-size: 0.9rem;
    background-color: #0c0c0e;
    transition:
        transform 0.22s ease,
        background-color 0.22s ease,
        color 0.22s ease,
        border-color 0.22s ease,
        box-shadow 0.22s ease;
}

.social-icons a:hover {
    transform: translateY(-3px) rotate(-5deg);
    background-color: var(--accent);
    color: #111111;
    border-color: var(--accent);
    box-shadow: 0 14px 36px rgba(0, 0, 0, 0.95);
}


.section,
.projects,
.contact-section {
    background-color: var(--bg-panel);
    border-top: 1px solid rgba(255, 255, 255, 0.02);
    border-bottom: 1px solid rgba(255, 255, 255, 0.02);
    transition:
        background-color 0.4s ease,
        border-color 0.4s ease,
        box-shadow 0.4s ease;
}

.section:hover,
.projects:hover,
.contact-section:hover {
    background-color: var(--bg-panel-soft);
    border-color: rgba(255, 255, 255, 0.06);
    box-shadow: 0 0 60px rgba(0, 0, 0, 0.9);
}

.section-title {
    font-family: var(--font-heading);
    font-size: 1.6rem;
    text-transform: uppercase;
    letter-spacing: 0.28em;
    margin-bottom: 1.1rem;
}

.section-text {
    max-width: 520px;
    color: var(--ink-soft);
    font-size: 0.95rem;
}


.projects {
    padding-top: 4.8rem;
    padding-bottom: 4.8rem;
}

.projects-grid {
    margin-top: 2.3rem;
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.8rem;
}

.project-card {
    background: #101013;
    border-radius: 0.9rem;
    padding: 1.6rem 1.5rem 1.4rem;
    border: 1px solid var(--border-subtle);
    box-shadow: var(--shadow-soft);
    transition:
        transform 0.3s ease,
        box-shadow 0.3s ease,
        border-color 0.3s ease,
        background-color 0.3s ease;
}

.project-card h3 {
    font-size: 1rem;
    text-transform: uppercase;
    letter-spacing: 0.18em;
    margin-bottom: 0.7rem;
}

.project-card p {
    font-size: 0.9rem;
    color: var(--ink-muted);
    margin-bottom: 1rem;
}

.project-card .tag {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.35rem 1.1rem;
    border-radius: 999px;
    border: 1px solid var(--accent-muted);
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.2em;
    color: var(--accent);
}

.project-card:hover {
    transform: translateY(-9px);
    border-color: var(--accent);
    background-color: #15151a;
    box-shadow: var(--shadow-strong);
}

.contact-section .section-text {
    max-width: none;
}

.contact-link {
    color: var(--accent);
    text-decoration: none;
    border-bottom: 1px dotted rgba(224, 222, 210, 0.7);
    transition:
        color 0.25s ease,
        border-color 0.25s ease;
}

.contact-link:hover {
    color: #ffffff;
    border-color: #ffffff;
}

.footer {
    padding: 1.3rem 7vw 1.6rem;
    text-align: center;
    font-size: 0.84rem;
    color: var(--ink-muted);
    background-color: #050507;
    border-top: 1px solid rgba(255, 255, 255, 0.08);
}

@media (max-width: 900px) {
    .home {
        grid-template-columns: 1fr;
        gap: 2.6rem;
    }

    .home-img {
        order: -1;
    }

    .home-content h1 {
        font-size: 2.2rem;
    }

    .projects-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

@media (max-width: 640px) {
    .header {
        padding-inline: 6vw;
    }

    .navbar {
        gap: 1rem;
    }

    .navbar a {
        font-size: 0.7rem;
        letter-spacing: 0.2em;
    }

    section {
        padding: 4.3rem 7vw;
    }

    .projects-grid {
        grid-template-columns: 1fr;
    }
}

.contact-icon {
  width: 1.2rem;      
  height: 1.2rem;     
  object-fit: contain;
  vertical-align: middle; 
}
