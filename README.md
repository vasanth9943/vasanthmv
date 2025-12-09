<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vasanth V - Professional Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
            color: #ffffff;
            overflow-x: hidden;
            background: #000000;
            line-height: 1.6;
        }

        /* Animated Background with Gradient Waves */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(45deg, #0a0a0a, #1a1a2e, #16213e, #0f3460);
            background-size: 400% 400%;
            animation: gradientWave 15s ease infinite;
        }

        @keyframes gradientWave {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Tech Grid Pattern */
        .tech-grid {
            position: absolute;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(99, 102, 241, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(99, 102, 241, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridScroll 30s linear infinite;
        }

        @keyframes gridScroll {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        /* Circuit Lines */
        .circuit-lines {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .circuit-line {
            position: absolute;
            background: linear-gradient(90deg, transparent, rgba(99, 102, 241, 0.5), transparent);
            animation: circuitFlow 8s linear infinite;
        }

        .circuit-line:nth-child(1) {
            width: 200px;
            height: 2px;
            top: 20%;
            left: -200px;
            animation-delay: 0s;
        }

        .circuit-line:nth-child(2) {
            width: 150px;
            height: 2px;
            top: 40%;
            left: -150px;
            animation-delay: 2s;
        }

        .circuit-line:nth-child(3) {
            width: 180px;
            height: 2px;
            top: 60%;
            left: -180px;
            animation-delay: 4s;
        }

        .circuit-line:nth-child(4) {
            width: 160px;
            height: 2px;
            top: 80%;
            left: -160px;
            animation-delay: 6s;
        }

        @keyframes circuitFlow {
            0% { left: -200px; opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { left: 100%; opacity: 0; }
        }

        /* Binary Rain Effect */
        .binary-rain {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .binary-col {
            position: absolute;
            top: -100%;
            color: rgba(99, 102, 241, 0.3);
            font-family: 'Courier New', monospace;
            font-size: 14px;
            line-height: 14px;
            white-space: nowrap;
            animation: binaryFall 10s linear infinite;
        }

        .binary-col:nth-child(1) { left: 5%; animation-delay: 0s; }
        .binary-col:nth-child(2) { left: 15%; animation-delay: 2s; }
        .binary-col:nth-child(3) { left: 25%; animation-delay: 4s; }
        .binary-col:nth-child(4) { left: 35%; animation-delay: 1s; }
        .binary-col:nth-child(5) { left: 45%; animation-delay: 3s; }
        .binary-col:nth-child(6) { left: 55%; animation-delay: 5s; }
        .binary-col:nth-child(7) { left: 65%; animation-delay: 2.5s; }
        .binary-col:nth-child(8) { left: 75%; animation-delay: 4.5s; }
        .binary-col:nth-child(9) { left: 85%; animation-delay: 1.5s; }
        .binary-col:nth-child(10) { left: 95%; animation-delay: 3.5s; }

        @keyframes binaryFall {
            0% { top: -100%; opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { top: 100%; opacity: 0; }
        }

        /* Floating Orbs */
        .orb {
            position: absolute;
            border-radius: 50%;
            filter: blur(60px);
            opacity: 0.4;
            animation: float 20s infinite ease-in-out;
        }

        .orb1 {
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, #6366f1, transparent);
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }

        .orb2 {
            width: 350px;
            height: 350px;
            background: radial-gradient(circle, #ec4899, transparent);
            top: 60%;
            right: 10%;
            animation-delay: 3s;
        }

        .orb3 {
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, #14b8a6, transparent);
            bottom: 10%;
            left: 50%;
            animation-delay: 6s;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) scale(1); }
            25% { transform: translate(30px, -30px) scale(1.1); }
            50% { transform: translate(-20px, 20px) scale(0.9); }
            75% { transform: translate(40px, 10px) scale(1.05); }
        }

        /* Particle Effect */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            animation: rise 15s linear infinite;
        }

        .particle:nth-child(1) { left: 5%; animation-delay: 0s; }
        .particle:nth-child(2) { left: 15%; animation-delay: 2s; }
        .particle:nth-child(3) { left: 25%; animation-delay: 4s; }
        .particle:nth-child(4) { left: 35%; animation-delay: 1s; }
        .particle:nth-child(5) { left: 45%; animation-delay: 3s; }
        .particle:nth-child(6) { left: 55%; animation-delay: 5s; }
        .particle:nth-child(7) { left: 65%; animation-delay: 2.5s; }
        .particle:nth-child(8) { left: 75%; animation-delay: 4.5s; }
        .particle:nth-child(9) { left: 85%; animation-delay: 1.5s; }
        .particle:nth-child(10) { left: 95%; animation-delay: 3.5s; }

        @keyframes rise {
            0% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }

        /* Header Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1.5rem 5%;
            z-index: 1000;
            transition: all 0.3s;
        }

        header.scrolled {
            padding: 1rem 5%;
            background: rgba(0, 0, 0, 0.9);
        }

        nav {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(135deg, #6366f1, #ec4899, #14b8a6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -1px;
        }

        .nav-menu {
            display: flex;
            gap: 3rem;
            list-style: none;
            align-items: center;
        }

        .nav-menu a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            font-weight: 500;
            position: relative;
            transition: color 0.3s;
        }

        .nav-menu a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #6366f1, #ec4899);
            transition: width 0.3s;
        }

        .nav-menu a:hover {
            color: #ffffff;
        }

        .nav-menu a:hover::before {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 8rem 5% 5rem;
        }

        .hero-content {
            max-width: 900px;
        }

        .hero-title {
            font-size: clamp(2.5rem, 6vw, 5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #ffffff, #a78bfa, #ec4899);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease;
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.2s backwards;
        }

        .hero-description {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.6);
            margin-bottom: 3rem;
            line-height: 1.8;
            animation: fadeInUp 1s ease 0.4s backwards;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.6s backwards;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            display: inline-block;
        }

        .btn-primary {
            background: linear-gradient(135deg, #6366f1, #ec4899);
            color: #ffffff;
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #ec4899, #6366f1);
            transition: left 0.3s;
            z-index: -1;
        }

        .btn-primary:hover::before {
            left: 0;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 40px rgba(99, 102, 241, 0.5);
        }

        .btn-secondary {
            background: transparent;
            color: #ffffff;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.5);
            transform: translateY(-3px);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Section Styling */
        section {
            padding: 6rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-title {
            font-size: clamp(2rem, 4vw, 3rem);
            text-align: center;
            margin-bottom: 4rem;
            background: linear-gradient(135deg, #6366f1, #ec4899);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 700;
        }

        /* Card Grid */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
        }

        /* Enhanced Cards with Hover Transform */
        .card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(20px);
            border-radius: 24px;
            padding: 2.5rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        /* Card Glow Effect */
        .card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(135deg, #6366f1, #ec4899, #14b8a6);
            border-radius: 24px;
            opacity: 0;
            transition: opacity 0.5s;
            z-index: -1;
        }

        .card::after {
            content: '';
            position: absolute;
            inset: 2px;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            border-radius: 22px;
            z-index: -1;
        }

        .card:hover::before {
            opacity: 1;
            animation: borderGlow 2s linear infinite;
        }

        @keyframes borderGlow {
            0% { filter: hue-rotate(0deg); }
            100% { filter: hue-rotate(360deg); }
        }

        .card:hover {
            transform: translateY(-15px) scale(1.03);
            box-shadow: 0 30px 60px rgba(99, 102, 241, 0.3),
                        0 0 80px rgba(236, 72, 153, 0.2);
            border-color: rgba(255, 255, 255, 0.3);
        }

        /* Card Content Transform on Hover */
        .card:hover .card-icon {
            transform: scale(1.2) rotate(10deg);
        }

        .card:hover .card-title {
            color: #ec4899;
            transform: translateX(10px);
        }

        .card:hover .card-text {
            color: rgba(255, 255, 255, 0.95);
        }

        .card-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #6366f1, #ec4899);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            transition: all 0.4s;
        }

        .card-title {
            font-size: 1.5rem;
            color: #ffffff;
            margin-bottom: 1rem;
            font-weight: 700;
            transition: all 0.4s;
        }

        .card-subtitle {
            color: #ec4899;
            font-weight: 600;
            margin-bottom: 0.5rem;
            font-size: 0.95rem;
        }

        .card-text {
            color: rgba(255, 255, 255, 0.6);
            line-height: 1.8;
            margin-bottom: 0.8rem;
            transition: all 0.4s;
        }

        .card-date {
            color: rgba(255, 255, 255, 0.4);
            font-size: 0.9rem;
            font-style: italic;
            margin-bottom: 1rem;
        }

        /* About Section Special Card */
        .about-card {
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1), rgba(236, 72, 153, 0.1));
            max-width: 900px;
            margin: 0 auto;
        }

        .education-item {
            margin-bottom: 2rem;
            padding-bottom: 2rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .education-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .education-item strong {
            color: #ffffff;
            font-size: 1.1rem;
            display: block;
            margin-bottom: 0.5rem;
        }

        /* Skills Section */
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 3rem;
        }

        .skill-badge {
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.2), rgba(236, 72, 153, 0.2));
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            font-weight: 600;
            transition: all 0.3s;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .skill-badge::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            transform: translate(-50%, -50%);
            transition: width 0.5s, height 0.5s;
        }

        .skill-badge:hover::before {
            width: 300px;
            height: 300px;
        }

        .skill-badge:hover {
            transform: translateY(-5px) scale(1.1);
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.4), rgba(236, 72, 153, 0.4));
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.3);
            border-color: rgba(255, 255, 255, 0.4);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }

        .contact-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #6366f1, #ec4899, #14b8a6, #6366f1);
            border-radius: 20px;
            opacity: 0;
            transition: opacity 0.4s;
            z-index: -1;
            background-size: 300% 300%;
            animation: borderFlow 3s ease infinite;
        }

        .contact-card::after {
            content: '';
            position: absolute;
            inset: 2px;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.95), rgba(22, 33, 62, 0.95));
            border-radius: 18px;
            z-index: -1;
        }

        @keyframes borderFlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .contact-card:hover::before {
            opacity: 1;
        }

        .contact-card:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-10px) scale(1.05);
            border-color: transparent;
            box-shadow: 0 20px 40px rgba(99, 102, 241, 0.3),
                        0 0 60px rgba(236, 72, 153, 0.2);
        }

        .contact-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            transition: all 0.4s;
        }

        .contact-card:hover .contact-icon {
            transform: scale(1.3) rotateY(360deg);
        }

        .contact-label {
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .contact-value {
            color: #ffffff;
            font-weight: 600;
            font-size: 1.1rem;
        }

        .contact-value a {
            color: #ffffff;
            text-decoration: none;
            transition: all 0.3s;
        }

        .contact-value a:hover {
            color: #ec4899;
            text-shadow: 0 0 10px rgba(236, 72, 153, 0.5);
        }

        /* Footer */
        footer {
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(20px);
            text-align: center;
            padding: 3rem 5%;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        footer p {
            color: rgba(255, 255, 255, 0.5);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-menu {
                gap: 1.5rem;
                font-size: 0.9rem;
            }

            .hero {
                padding: 6rem 5% 3rem;
            }

            .card-grid {
                grid-template-columns: 1fr;
            }

            section {
                padding: 4rem 5%;
            }

            .logo {
                font-size: 1.4rem;
            }

            nav {
                flex-wrap: wrap;
                gap: 1rem;
            }

            .nav-menu {
                width: 100%;
                justify-content: center;
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="animated-bg">
        <div class="tech-grid"></div>
        <div class="circuit-lines">
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
            <div class="circuit-line"></div>
        </div>
        <div class="binary-rain">
            <div class="binary-col">01001010<br>10110101<br>01010101<br>11001100<br>10101010<br>01110011</div>
            <div class="binary-col">11010110<br>00101011<br>11001001<br>01010110<br>10011010<br>01100011</div>
            <div class="binary-col">10101100<br>01011010<br>11100110<br>00101101<br>11010101<br>01001110</div>
            <div class="binary-col">01110010<br>10011011<br>01101100<br>11010011<br>00111001<br>10101100</div>
            <div class="binary-col">11001010<br>01010111<br>10110100<br>01101011<br>11010010<br>00101110</div>
            <div class="binary-col">00110101<br>11101001<br>01011100<br>10010110<br>01101010<br>11001101</div>
            <div class="binary-col">10100110<br>01110101<br>11010100<br>00101100<br>10011101<br>01010011</div>
            <div class="binary-col">01101011<br>10010100<br>11000110<br>01011011<br>10101001<br>00110110</div>
            <div class="binary-col">11010101<br>00101110<br>10110011<br>01100101<br>11001010<br>01011100</div>
            <div class="binary-col">01011010<br>10101101<br>11100010<br>00110111<br>10010101<br>01101011</div>
        </div>
        <div class="orb orb1"></div>
        <div class="orb orb2"></div>
        <div class="orb orb3"></div>
    </div>

    <!-- Particles -->
    <div class="particles">
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
    </div>

    <!-- Header -->
    <header>
        <nav>
            <div class="logo">VASANTH V</div>
            <ul class="nav-menu">
                <li><a href="#about">About</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1 class="hero-title">Hi, I'm Vasanth V</h1>
            <p class="hero-subtitle">IT Professional | UI/UX Designer | Machine Learning Enthusiast</p>
            <p class="hero-description">
                Motivated and adaptable individual seeking opportunities in the IT industry to apply problem-solving skills, 
                learn new technologies, and contribute to organizational growth.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">Get In Touch</a>
                <a href="#" class="btn btn-secondary">View Resume</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div class="card about-card">
            <div class="card-icon">🎓</div>
            <h3 class="card-title">Education & Background</h3>
            
            <div class="education-item">
                <strong>B.Tech. Information Technology</strong>
                <p class="card-text">
                    Anjalai Ammal Mahalingam Engineering College, Thiruvarur<br>
                    CGPA: 7.5/10 | Graduation: May 2025
                </p>
            </div>

            <div class="education-item">
                <strong>HSC (State Board)</strong>
                <p class="card-text">
                    Karthi Vidhyalaya
