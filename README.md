# -X
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Medium Inspired Landing Page</title>
    <style>
        :root {
            --background-color: #F7F4EF;
            --primary-color: #000000;
            --button-color: #000000;
            --button-text-color: #FFFFFF;
            --hover-button-color: #333333;
            --font-serif: 'Playfair Display', serif;
            --font-sans: 'Arial', sans-serif;
            --transition-speed: 0.3s;
        }

        body {
            margin: 0;
            font-family: var(--font-sans);
            background-color: var(--background-color);
            color: var(--primary-color);
            overflow-x: hidden;
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.8);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav {
            display: flex;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--primary-color);
        }

        .cta-button {
            background-color: var(--button-color);
            color: var(--button-text-color);
            padding: 0.5rem 1rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: background-color var(--transition-speed);
        }

        .cta-button:hover {
            background-color: var(--hover-button-color);
        }

        .hero {
            display: flex;
            align-items: center;
            height: 100vh;
            padding: 0 2rem;
            overflow: hidden;
        }

        .hero-text {
            flex: 1;
            max-width: 600px;
        }

        h1 {
            font-family: var(--font-serif);
            font-size: 70px;
            margin: 0;
            animation: fadeIn 1s ease-in;
        }

        h2 {
            font-size: 24px;
            margin: 1rem 0;
        }

        .hero-illustration {
            flex: 1;
            position: relative;
            overflow: hidden;
        }

        .floating-svg {
            position: absolute;
            animation: float 3s infinite;
        }

        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }

        footer {
            padding: 2rem 0;
            text-align: center;
            background-color: var(--background-color);
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 50px;
            }

            .hero {
                flex-direction: column;
                text-align: center;
            }

            .hero-text {
                max-width: 100%;
            }

            nav {
                display: none;
            }

            .hamburger {
                display: block;
                cursor: pointer;
            }

            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                background-color: #fff;
                top: 60px;
                right: 0;
                border: 1px solid #ccc;
                width: 100%;
                z-index: 1000;
            }

            .nav-links.active {
                display: flex;
            }
        }

        .hamburger {
            display: none;
        }

    </style>
</head>
<body>

<header>
    <div class="logo">Medium</div>
    <nav class="nav-links" id="navLinks">
        <a href="#">Our Story</a>
        <a href="#">Membership</a>
        <a href="#">Write</a>
        <a href="#">Sign In</a>
        <button class="cta-button">Get Started</button>
    </nav>
    <div class="hamburger" id="hamburger">&#9776;</div>
</header>

<section class="hero">
    <div class="hero-text">
        <h1>Human stories & ideas</h1>
        <h2>A place to read, write, and deepen your understanding.</h2>
        <button class="cta-button">Start Reading</button>
    </div>
    <div class="hero-illustration">
        <svg class="floating-svg" width="100" height="100" style="top: 20%; left: 70%;">
            <circle cx="50" cy="50" r="50" fill="green" />
        </svg>
        <svg class="floating-svg" width="100" height="100" style="top: 40%; left: 10%;">
            <rect width="100" height="100" fill="lightblue" />
        </svg>
    </div>
</section>

<footer>
    <a href="#">Help</a>
    <a href="#">Status</a>
    <a href="#">About</a>
    <a href="#">Careers</a>
    <a href="#">Press</a>
    <a href="#">Blog</a>
    <a href="#">Store</a>
    <a href="#">Privacy</a>
    <a href="#">Rules</a>
    <a href="#">Terms</a>
    <a href="#">Text to Speech</a>
</footer>

<script>
    const hamburger = document.getElementById('hamburger');
    const navLinks = document.getElementById('navLinks');

    hamburger.addEventListener('click', () => {
        navLinks.classList.toggle('active');
    });
</script>

</body>
</html>
