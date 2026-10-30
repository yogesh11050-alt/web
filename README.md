```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Yogesh | Sports Car Portfolio</title>

<style>
/* GENERAL */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: Arial, sans-serif;
    background: #050914;
    color: white;
    overflow-x: hidden;
}

:root {
    --cyan: #00eaff;
    --purple: #b04dff;
    --dark: #050914;
    --card: #101a2b;
}

a {
    text-decoration: none;
    color: inherit;
}

/* NAVIGATION */
header {
    background: rgba(5, 9, 20, 0.97);
    border-bottom: 1px solid var(--cyan);
    position: sticky;
    top: 0;
    z-index: 100;
}

nav {
    max-width: 1200px;
    min-height: 75px;
    margin: auto;
    padding: 15px 25px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
}

.logo {
    font-size: 30px;
    font-weight: bold;
    letter-spacing: 3px;
}

.logo span {
    color: var(--cyan);
}

nav ul {
    display: flex;
    gap: 25px;
    list-style: none;
    flex-wrap: wrap;
}

nav ul a {
    color: #d9e4f7;
    transition: 0.3s;
}

nav ul a:hover {
    color: var(--cyan);
    text-shadow: 0 0 12px var(--cyan);
}

/* HOME */
.hero {
    min-height: 620px;
    padding: 70px 7%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 45px;
    background:
        radial-gradient(ellipse at 80% 50%,
        #102b53 0%, transparent 50%),
        var(--dark);
}

.hero-text {
    flex: 1 1 350px;
    animation: slideIn 1s ease;
}

.tag {
    color: var(--cyan);
    letter-spacing: 4px;
    font-size: 13px;
    margin-bottom: 20px;
}

.hero h1 {
    font-size: clamp(42px, 6vw, 70px);
    line-height: 1.15;
    margin-bottom: 15px;
}

.cyan {
    color: var(--cyan);
}

.purple {
    color: var(--purple);
}

.hero h2 {
    font-size: 24px;
    color: var(--purple);
    margin-bottom: 20px;
}

.hero p {
    color: #bdc9dc;
    line-height: 1.8;
    max-width: 520px;
}

.buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    margin-top: 30px;
}

.btn {
    display: inline-block;
    padding: 13px 22px;
    border: 1px solid var(--cyan);
    border-radius: 30px;
    transition: 0.3s;
}

.btn.primary {
    background: var(--cyan);
    color: #06101b;
    font-weight: bold;
}

.btn:hover {
    transform: translateY(-4px);
    box-shadow: 0 0 22px #00eaff77;
}

.btn.secondary {
    border-color: var(--purple);
}

/* HERO SPORTS CAR IMAGE */
.hero-car {
    flex: 1 1 380px;
    min-width: 0;
    text-align: center;
}

.hero-car img {
    display: block;
    width: 100%;
    max-width: 600px;
    height: auto;
    margin: auto;
    border-radius: 15px;
    filter: drop-shadow(0 0 20px #008cff66);
    animation: floatCar 4s ease-in-out infinite;
}

/* GENERAL SECTIONS */
section.content-section {
    padding: 80px 7%;
}

.section-heading {
    text-align: center;
    font-size: 38px;
    margin-bottom: 15px;
}

.section-subtitle {
    text-align: center;
    color: var(--cyan);
    letter-spacing: 4px;
    font-size: 12px;
    margin-bottom: 40px;
}

/* ABOUT */
.about-box {
    max-width: 850px;
    margin: auto;
    padding: 35px;
    border: 1px solid #183e59;
    background: var(--card);
    border-radius: 15px;
    transition: 0.3s;
}

.about-box:hover {
    border-color: var(--cyan);
    box-shadow: 0 0 20px #00eaff22;
}

.about-box p {
    color: #c4cee0;
    line-height: 1.9;
    margin-bottom: 12px;
}

.education {
    margin-top: 20px;
    color: var(--cyan);
}

/* SKILLS */
.skills {
    background: #080f1d;
}

.grid {
    max-width: 1100px;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 22px;
}

.card {
    background: var(--card);
    border: 1px solid #203047;
    border-radius: 14px;
    padding: 30px 22px;
    text-align: center;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: var(--cyan);
    box-shadow: 0 0 22px #00eaff22;
}

.card .icon {
    font-size: 42px;
    margin-bottom: 15px;
}

.card h3 {
    color: var(--cyan);
    margin-bottom: 12px;
}

.card p {
    color: #bdc9dc;
    line-height: 1.7;
    font-size: 14px;
}

/* SPORTS CAR SECTION */
.sports-section {
    background:
        radial-gradient(ellipse at 50% 60%,
        #10274b 0%, transparent 65%);
}

.car-showcase {
    max-width: 1100px;
    margin: auto;
    padding: 30px;
    border: 1px solid #19465e;
    border-radius: 20px;
    background: linear-gradient(135deg, #0d1627, #050914);
    overflow: hidden;
}

.car-showcase img {
    display: block;
    width: 100%;
    max-width: 950px;
    height: auto;
    margin: auto;
    border-radius: 12px;
    filter: drop-shadow(0 0 20px #008cff66);
    transition: transform 0.4s;
}

.car-showcase img:hover {
    transform: scale(1.03);
}

.car-name {
    text-align: center;
    margin-top: 25px;
    font-size: 27px;
    letter-spacing: 3px;
    color: var(--cyan);
}

.car-description {
    max-width: 700px;
    margin: 15px auto;
    text-align: center;
    color: #bdc9dc;
    line-height: 1.8;
}

.car-features {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 25px;
}

.feature {
    border: 1px solid #263a55;
    padding: 12px 20px;
    border-radius: 10px;
    text-align: center;
    color: #dce7f7;
}

.feature strong {
    display: block;
    color: var(--purple);
    margin-bottom: 5px;
}

/* CONTACT */
.contact-box {
    max-width: 650px;
    margin: auto;
    text-align: center;
    padding: 40px 25px;
    background: var(--card);
    border: 1px solid #174358;
    border-radius: 15px;
}

.contact-box p {
    color: #bdc9dc;
    line-height: 1.8;
    margin-bottom: 20px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 25px 15px;
    border-top: 1px solid #16354b;
    color: #aab9cf;
    font-size: 13px;
}

footer span {
    color: var(--cyan);
}

/* ANIMATIONS */
@keyframes floatCar {
    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateX(-30px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

/* MOBILE RESPONSIVE */
@media (max-width: 750px) {
    nav {
        flex-direction: column;
    }

    nav ul {
        justify-content: center;
        gap: 12px 18px;
    }

    nav ul a {
        font-size: 13px;
    }

    .hero {
        padding: 55px 6%;
        text-align: center;
    }

    .hero p {
        margin-left: auto;
        margin-right: auto;
    }

    .buttons {
        justify-content: center;
    }

    .hero-car {
        flex-basis: 100%;
    }

    section.content-section {
        padding: 60px 6%;
    }

    .grid {
        grid-template-columns: 1fr;
    }

    .section-heading {
        font-size: 30px;
    }

    .car-showcase {
        padding: 15px;
    }

    .car-name {
        font-size: 21px;
    }
}

@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation: none !important;
        scroll-behavior: auto !important;
        transition: none !important;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->
<header>
    <nav>
        <a href="#home" class="logo">YOGESH<span>.</span></a>

        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#sports-car">Sports Car</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<!-- HOME -->
<section class="hero" id="home">

    <div class="hero-text">
        <div class="tag">WELCOME TO MY PORTFOLIO</div>

        <h1>
            Hi, I'm <span class="cyan">Yogesh</span>
        </h1>

        <h2>Mechanical Engineering Student</h2>

        <p>
            I am a first-year Mechanical Engineering student at
            Mount Zion College of Engineering. I love cars, gaming,
            technology, and learning new things.
        </p>

        <div class="buttons">
            <a href="#about" class="btn primary">Explore My World</a>
            <a href="#contact" class="btn secondary">Contact Me</a>
        </div>
    </div>

    <div class="hero-car">
        <img
            src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1000&q=85"
            alt="Sports car"
        >
    </div>

</section>

<!-- ABOUT -->
<section class="content-section" id="about">

    <h2 class="section-heading">
        About <span class="cyan">Me</span>
    </h2>

    <p class="section-subtitle">GET TO KNOW ME</p>

    <div class="about-box">
        <h3 class="cyan">🚗 I LOVE CARS</h3>

        <p>
            Hello! My name is Yogesh. I am studying Mechanical
            Engineering at Mount Zion College of Engineering.
            I enjoy learning about cars, automobile technology,
            gaming, and engineering.
        </p>

        <p>
            My ambition is to improve my technical skills, create
            interesting projects, and become a successful engineer.
        </p>

        <div class="education">
            <p><strong>Department:</strong> Mechanical Engineering</p>
            <p><strong>Year:</strong> First Year</p>
            <p><strong>College:</strong> Mount Zion College of Engineering</p>
        </div>
    </div>

</section>

<!-- SKILLS -->
<section class="content-section skills" id="skills">

    <h2 class="section-heading">
        My <span class="cyan">Skills</span>
    </h2>

    <p class="section-subtitle">WHAT I ENJOY</p>

    <div class="grid">

        <div class="card">
            <div class="icon">🎮</div>
            <h3>Gaming</h3>
            <p>I enjoy playing games and exploring gaming worlds.</p>
        </div>

        <div class="card">
            <div class="icon">🏎️</div>
            <h3>Cars</h3>
            <p>I love sports cars, vehicle design, and automobile technology.</p>
        </div>

        <div class="card">
            <div class="icon">⚙️</div>
            <h3>Engineering</h3>
            <p>I am learning about mechanical systems and engineering.</p>
        </div>

    </div>

</section>

<!-- SPORTS CAR -->
<section class="content-section sports-section" id="sports-car">

    <h2 class="section-heading">
        My Dream <span class="cyan">Sports Car</span>
    </h2>

    <p class="section-subtitle">SPEED • POWER • PERFORMANCE</p>

    <div class="car-showcase">

        <img
            src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1400&q=90"
            alt="Luxury Porsche sports car"
            loading="lazy"
        >

        <h3 class="car-name">PORSCHE 911</h3>

        <p class="car-description">
            A sports car represents my passion for speed, engineering,
            performance, and beautiful automobile design. This Porsche
            911 image showcases the style that inspires me.
        </p>

        <div class="car-features">

            <div class="feature">
                <strong>DESIGN</strong>
                Sporty
            </div>

            <div class="feature">
                <strong>STYLE</strong>
                Premium
            </div>

            <div class="feature">
                <strong>PASSION</strong>
                Automobiles
            </div>

        </div>

    </div>

</section>

<!-- PROJECTS -->
<section class="content-section" id="projects">

    <h2 class="section-heading">
        My <span class="cyan">Projects</span>
    </h2>

    <p class="section-subtitle">MY LEARNING JOURNEY</p>

    <div class="grid">

        <div class="card">
            <div class="icon">💻</div>
            <h3>Portfolio Website</h3>
            <p>A personal website designed using HTML and CSS.</p>
        </div>

        <div class="card">
            <div class="icon">🚘</div>
            <h3>Automobile Learning</h3>
            <p>Exploring car components and mechanical engineering concepts.</p>
        </div>

        <div class="card">
            <div class="icon">💡</div>
            <h3>Future Projects</h3>
            <p>A place to showcase new projects as I develop my skills.</p>
        </div>

    </div>

</section>

<!-- CONTACT -->
<section class="content-section" id="contact">

    <h2 class="section-heading">
        Contact <span class="cyan">Me</span>
    </h2>

    <p class="section-subtitle">LET'S CONNECT</p>

    <div class="contact-box">
        <h3>Thanks for visiting my portfolio!</h3>

        <p>
            Feel free to contact me about cars, gaming,
            mechanical engineering, and projects.
        </p>

        <!-- Replace with your own email address -->
        <a href="mailto:yourname@example.com" class="btn primary">
            Send Me an Email
        </a>
    </div>

</section>

<!-- FOOTER -->
<footer>
    <p>Designed by <span>Yogesh</span> | © 2026 All Rights Reserved</p>
</footer>

</body>
</html>
```
