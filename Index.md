HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 9.3 | Flexbox and Grid</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header and Navigation -->
    <header class="header">
        <nav class="navbar container">
            <a href="#" class="logo">Flex<span>Grid</span></a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <a href="#features" class="nav-button">Get Started</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <main>
        <section class="hero container" id="home">
            <div class="hero-content">
                <p class="eyebrow">DESIGN SMARTER</p>
                <h1>Build Beautiful Websites with Flexbox & Grid</h1>
                <p class="hero-description">
                    Create modern, responsive and user-friendly websites
                    with the power of CSS Grid and Flexbox.
                </p>

                <div class="hero-buttons">
                    <a href="#features" class="primary-button">Explore Features</a>
                    <a href="#about" class="secondary-button">Learn More</a>
                </div>
            </div>

            <div class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1000&q=80"
                    alt="Laptop and workspace for web development">
            </div>
        </section>

        <!-- Features Section -->
        <section class="features-section" id="features">
            <div class="container">
                <div class="section-heading">
                    <p class="eyebrow">OUR FEATURES</p>
                    <h2>Everything You Need</h2>
                    <p>
                        Powerful tools and simple layouts for modern websites.
                    </p>
                </div>

                <div class="features-grid">
                    <article class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h3>Responsive Design</h3>
                        <p>
                            Make your website look great on mobiles,
                            tablets and desktops.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">⚡</div>
                        <h3>Fast Performance</h3>
                        <p>
                            Build clean layouts with efficient and
                            lightweight CSS.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">🎨</div>
                        <h3>Modern Design</h3>
                        <p>
                            Create attractive pages with beautiful
                            colors and spacing.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">🧩</div>
                        <h3>CSS Grid</h3>
                        <p>
                            Arrange content into flexible rows and
                            columns with ease.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">📐</div>
                        <h3>Flexbox Layout</h3>
                        <p>
                            Align navigation links and card content
                            with flexible layouts.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">🚀</div>
                        <h3>Easy to Use</h3>
                        <p>
                            Start building organized and accessible
                            websites with simple techniques.
                        </p>
                        <a href="#about">Learn more →</a>
                    </article>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section class="about-section container" id="about">
            <div>
                <p class="eyebrow">WHY FLEXGRID?</p>
                <h2>One Layout, Every Screen</h2>
            </div>
            <p>
                CSS Grid organizes the main page into columns and rows,
                while Flexbox aligns elements inside individual sections.
                Together, they make responsive web design easier.
            </p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer" id="contact">
        <div class="container footer-content">
            <p>© 2026 FlexGrid. Created for Assignment 9.3.</p>
            <a href="#home">Back to top ↑</a>
        </div>
    </footer>

</body>
</html>

CSS
/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    color: #1e293b;
    background-color: #ffffff;
}

a {
    text-decoration: none;
    color: inherit;
}

.container {
    width: min(1120px, 90%);
    margin: 0 auto;
}

/* Header and Navbar - Flexbox */
.header {
    background-color: #ffffff;
    border-bottom: 1px solid #e2e8f0;
}

.navbar {
    min-height: 76px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
}

.logo {
    font-size: 27px;
    font-weight: bold;
    color: #172554;
}

.logo span {
    color: #6366f1;
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 28px;
    list-style: none;
}

.nav-links a {
    color: #475569;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #6366f1;
}

.nav-button,
.primary-button {
    background-color: #6366f1;
    color: white;
    padding: 11px 20px;
    border-radius: 8px;
    display: inline-block;
    font-weight: bold;
    transition: background-color 0.3s ease;
}

.nav-button:hover,
.primary-button:hover {
    background-color: #4f46e5;
}

/* Hero Section - Flexbox */
.hero {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 55px;
    padding-top: 80px;
    padding-bottom: 80px;
}

.hero-content {
    flex: 1;
}

.eyebrow {
    color: #6366f1;
    font-size: 13px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 14px;
}

.hero h1 {
    font-size: clamp(34px, 4vw, 52px);
    line-height: 1.15;
    margin-bottom: 22px;
    color: #172554;
}

.hero-description {
    color: #64748b;
    font-size: 17px;
    margin-bottom: 28px;
    max-width: 500px;
}

.hero-buttons {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    gap: 14px;
}

.secondary-button {
    padding: 10px 20px;
    border: 1px solid #cbd5e1;
    border-radius: 8px;
    font-weight: bold;
}

.secondary-button:hover {
    background-color: #f1f5f9;
}

.hero-image {
    flex: 1;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    height: 360px;
    object-fit: cover;
    border-radius: 18px;
    display: block;
}

/* Features Section - CSS Grid */
.features-section {
    background-color: #f8fafc;
    padding: 75px 0;
}

.section-heading {
    text-align: center;
    margin-bottom: 42px;
}

.section-heading h2,
.about-section h2 {
    font-size: 34px;
    line-height: 1.2;
    color: #172554;
    margin-bottom: 12px;
}

.section-heading > p:last-child {
    color: #64748b;
}

/* Three-column Grid */
.features-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}

/* Card content - Flexbox */
.feature-card {
    background-color: white;
    padding: 28px;
    border: 1px solid #e2e8f0;
    border-radius: 14px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 14px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 28px rgba(15, 23, 42, 0.08);
}

.feature-icon {
    width: 52px;
    height: 52px;
    background-color: #eef2ff;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 25px;
}

.feature-card h3 {
    font-size: 20px;
    color: #172554;
}

.feature-card p {
    color: #64748b;
    font-size: 15px;
    flex-grow: 1;
}

.feature-card a {
    color: #6366f1;
    font-weight: bold;
}

.feature-card a:hover {
    color: #4338ca;
}

/* About Section - Grid */
.about-section {
    padding-top: 75px;
    padding-bottom: 75px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 40px;
}

.about-section > p {
    color: #64748b;
    font-size: 17px;
}

/* Footer */
.footer {
    background-color: #172554;
    color: #e2e8f0;
    padding: 24px 0;
}

.footer-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
}

.footer-content a {
    color: #a5b4fc;
}

/* Tablet Responsive Layout */
@media (max-width: 900px) {
    .navbar {
        flex-wrap: wrap;
        padding-top: 16px;
        padding-bottom: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .hero {
        gap: 30px;
        padding-top: 55px;
        padding-bottom: 55px;
    }

    .hero-image img {
        height: 300px;
    }

    .features-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

/* Mobile Responsive Layout */
@media (max-width: 600px) {
    .navbar {
        justify-content: center;
        gap: 16px;
    }

    .logo {
        width: 100%;
        text-align: center;
    }

    .nav-links {
        justify-content: center;
        flex-wrap: wrap;
        gap: 12px 18px;
    }

    .nav-button {
        padding: 9px 15px;
    }

    .hero {
        flex-direction: column;
        align-items: stretch;
        gap: 30px;
        padding-top: 45px;
        padding-bottom: 45px;
    }

    .hero h1 {
        font-size: 36px;
    }

    .hero-image img {
        height: 250px;
    }

    .features-section {
        padding: 50px 0;
    }

    .section-heading h2,
    .about-section h2 {
        font-size: 28px;
    }

    /* One column on mobile */
    .features-grid {
        grid-template-columns: 1fr;
        gap: 18px;
    }

    .about-section {
        grid-template-columns: 1fr;
        gap: 16px;
        padding-top: 50px;
        padding-bottom: 50px;
    }

    .footer-content {
        flex-direction: column;
        text-align: center;
        gap: 10px;
    }
}
