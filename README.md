<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project UNIVERSE - The $10 Trillion Global Digital Economy Ecosystem</title>
    <meta name="description" content="Building the world's first comprehensive digital economy ecosystem connecting 8 billion people, 195 governments, and creating the future of human civilization.">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Advanced CSS Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: #ffffff;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            overflow-x: hidden;
            position: relative;
        }

        /* Animated Background Elements */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.05) 0%, transparent 50%);
            z-index: -2;
            animation: gradientShift 20s ease-in-out infinite;
        }

        @keyframes gradientShift {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.8; }
        }

        /* Floating particles animation */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 15s infinite linear;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Header and Navigation */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(0, 0, 0, 0.9);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: #ffffff;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .logo-icon {
            width: 50px;
            height: 50px;
            margin-right: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 8px 32px rgba(102, 126, 234, 0.3);
        }

        .logo-icon::before {
            content: '🌌';
            font-size: 24px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        .nav-menu {
            display: none;
        }

        @media (min-width: 768px) {
            .nav-menu {
                display: flex;
                list-style: none;
                gap: 2rem;
            }

            .nav-menu a {
                color: rgba(255, 255, 255, 0.8);
                text-decoration: none;
                font-weight: 500;
                transition: all 0.3s ease;
                position: relative;
            }

            .nav-menu a:hover {
                color: #667eea;
            }

            .nav-menu a::after {
                content: '';
                position: absolute;
                bottom: -5px;
                left: 0;
                width: 0;
                height: 2px;
                background: linear-gradient(90deg, #667eea, #764ba2);
                transition: width 0.3s ease;
            }

            .nav-menu a:hover::after {
                width: 100%;
            }
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            padding: 8rem 2rem 4rem;
        }

        .hero-content {
            max-width: 1200px;
            z-index: 10;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(102, 126, 234, 0.2);
            color: #667eea;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 2rem;
            border: 1px solid rgba(102, 126, 234, 0.3);
            backdrop-filter: blur(10px);
        }

        .hero h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #ffffff 0%, #667eea 50%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1.1;
            animation: titleGlow 3s ease-in-out infinite alternate;
        }

        @keyframes titleGlow {
            from { text-shadow: 0 0 20px rgba(102, 126, 234, 0.3); }
            to { text-shadow: 0 0 40px rgba(102, 126, 234, 0.6); }
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 3rem;
            color: rgba(255, 255, 255, 0.8);
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .cta-primary, .cta-secondary {
            padding: 1.2rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .cta-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #ffffff;
            box-shadow: 0 8px 32px rgba(102, 126, 234, 0.4);
        }

        .cta-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 48px rgba(102, 126, 234, 0.6);
        }

        .cta-secondary {
            background: transparent;
            color: #ffffff;
            border: 2px solid rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
        }

        .cta-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: #667eea;
            color: #667eea;
        }

        /* Stats Section */
        .stats {
            padding: 6rem 2rem;
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(20px);
        }

        .stats-container {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
        }

        .stat-card {
            text-align: center;
            padding: 2rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }

        .stat-number {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 500;
        }

        /* Features Section */
        .features {
            padding: 8rem 2rem;
        }

        .features-container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 5rem;
        }

        .section-badge {
            display: inline-block;
            background: rgba(102, 126, 234, 0.2);
            color: #667eea;
            padding: 0.6rem 1.2rem;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            border: 1px solid rgba(102, 126, 234, 0.3);
        }

        .section-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 700;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #ffffff 0%, #667eea 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-description {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.7;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
        }

        .feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 24px;
            padding: 3rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 20px 60px rgba(102, 126, 234, 0.2);
        }

        .feature-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 8px 32px rgba(102, 126, 234, 0.3);
        }

        .feature-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #ffffff;
        }

        .feature-description {
            color: rgba(255, 255, 255, 0.7);
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .feature-details {
            list-style: none;
        }

        .feature-details li {
            color: rgba(255, 255, 255, 0.6);
            margin-bottom: 0.8rem;
            position: relative;
            padding-left: 1.5rem;
        }

        .feature-details li::before {
            content: '✦';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
        }

        /* Vision Section */
        .vision {
            padding: 8rem 2rem;
            background: rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(20px);
            position: relative;
        }

        .vision-container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .vision-content {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 30px;
            padding: 4rem 3rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            position: relative;
            overflow: hidden;
        }

        .vision-quote {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            font-weight: 600;
            line-height: 1.4;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, #ffffff 0%, #667eea 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .vision-author {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 600;
        }

        /* Timeline Section */
        .timeline {
            padding: 8rem 2rem;
        }

        .timeline-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .timeline-item {
            display: flex;
            margin-bottom: 4rem;
            position: relative;
        }

        .timeline-item:nth-child(even) {
            flex-direction: row-reverse;
        }

        .timeline-content {
            flex: 1;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2.5rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            position: relative;
        }

        .timeline-year {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 2rem;
            font-weight: 800;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .timeline-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #ffffff;
        }

        .timeline-description {
            color: rgba(255, 255, 255, 0.7);
            line-height: 1.6;
        }

        /* Contact Section */
        .contact {
            padding: 8rem 2rem;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(20px);
        }

        .contact-container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 24px;
            padding: 3rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            margin-top: 3rem;
        }

        .form-group {
            margin-bottom: 2rem;
            text-align: left;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 600;
        }

        .form-input, .form-textarea {
            width: 100%;
            padding: 1rem 1.5rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            color: #ffffff;
            font-size: 1rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: #667eea;
            background: rgba(255, 255, 255, 0.15);
        }

        .form-textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-submit {
            width: 100%;
            padding: 1.2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #ffffff;
            border: none;
            border-radius: 12px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 32px rgba(102, 126, 234, 0.4);
        }

        .form-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 48px rgba(102, 126, 234, 0.6);
        }

        /* Footer */
        .footer {
            padding: 4rem 2rem 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            background: rgba(0, 0, 0, 0.8);
        }

        .footer-container {
            max-width: 1400px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-logo {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .footer-text {
            color: rgba(255, 255, 255, 0.6);
            margin-bottom: 2rem;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #667eea;
        }

        .footer-copyright {
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-container {
                padding: 0 1rem;
            }

            .hero {
                padding: 6rem 1rem 4rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .cta-primary, .cta-secondary {
                width: 100%;
                max-width: 300px;
            }

            .stats-container {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
                gap: 2rem;
            }

            .features-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .feature-card {
                padding: 2rem;
            }

            .timeline-item {
                flex-direction: column !important;
            }

            .timeline-item:nth-child(even) {
                flex-direction: column !important;
            }

            .contact-form {
                padding: 2rem;
            }

            .footer-links {
                flex-direction: column;
                gap: 1rem;
            }
        }

        /* Loading Animation */
        .loading-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
            z-index: 10000;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: opacity 0.5s ease;
        }

        .loading-spinner {
            width: 60px;
            height: 60px;
            border: 3px solid rgba(102, 126, 234, 0.3);
            border-top: 3px solid #667eea;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Loading Overlay -->
    <div class="loading-overlay" id="loadingOverlay">
        <div class="loading-spinner"></div>
    </div>

    <!-- Floating Particles -->
    <div class="particles" id="particles"></div>

    <!-- Header -->
    <header class="header">
        <div class="nav-container">
            <a href="#home" class="logo">
                <div class="logo-icon"></div>
                PROJECT UNIVERSE
            </a>
            <nav class="nav-menu">
                <a href="#features">Features</a>
                <a href="#vision">Vision</a>
                <a href="#timeline">Timeline</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-badge">🚀 The Future of Human Civilization</div>
            <h1>PROJECT UNIVERSE</h1>
            <p>Building the world's first $10 trillion digital economy ecosystem that connects every human, every business, and every government into one unified platform—empowering 8 billion people globally.</p>
            <div class="cta-buttons">
                <a href="#features" class="cta-primary">Explore the Ecosystem</a>
                <a href="#contact" class="cta-secondary">Join the Revolution</a>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="stats-container">
            <div class="stat-card">
                <div class="stat-number">$10T</div>
                <div class="stat-label">Target Annual Revenue</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">8B</div>
                <div class="stat-label">Global Users</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">195</div>
                <div class="stat-label">Countries</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">7</div>
                <div class="stat-label">Ecosystem Layers</div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="features-container">
            <div class="section-header">
                <div class="section-badge">🌟 Seven Revolutionary Layers</div>
                <h2 class="section-title">The Complete Ecosystem</h2>
                <p class="section-description">Seven interconnected layers that will transform how humanity works, lives, and thrives in the digital age.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🆔</div>
                    <h3 class="feature-title">Universal Digital Identity</h3>
                    <p class="feature-description">One identity for everything—blockchain-based, government-approved system serving all 8 billion humans.</p>
                    <ul class="feature-details">
                        <li>Single digital passport for every human</li>
                        <li>Works across all countries and platforms</li>
                        <li>99.99% accuracy with biometric + AI verification</li>
                        <li>$500B annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💰</div>
                    <h3 class="feature-title">Global Digital Currency</h3>
                    <p class="feature-description">Universal money system working in all 195 countries simultaneously with instant, free transactions.</p>
                    <ul class="feature-details">
                        <li>Central bank digital currency infrastructure</li>
                        <li>$20 trillion daily transaction volume target</li>
                        <li>AI-powered fraud detection</li>
                        <li>$2T annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🤖</div>
                    <h3 class="feature-title">AI-Powered Super Platform</h3>
                    <p class="feature-description">The everything app combining social media, e-commerce, banking, work, education, and healthcare.</p>
                    <ul class="feature-details">
                        <li>1000+ services in one super-app</li>
                        <li>AI handles 90% of daily digital tasks</li>
                        <li>Personalized for 8 billion users</li>
                        <li>$3T annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⚛️</div>
                    <h3 class="feature-title">Quantum-AI Cloud Infrastructure</h3>
                    <p class="feature-description">The world's computing brain with 10,000+ quantum data centers powered by renewable energy.</p>
                    <ul class="feature-details">
                        <li>AGI-powered cloud computing</li>
                        <li>80% of global computing demand</li>
                        <li>100% renewable energy powered</li>
                        <li>$1.5T annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚛</div>
                    <h3 class="feature-title">Global Logistics Network</h3>
                    <p class="feature-description">Physical-digital bridge with same-day delivery anywhere on Earth through autonomous systems.</p>
                    <ul class="feature-details">
                        <li>Autonomous delivery in 10,000+ cities</li>
                        <li>Drone + robot + self-driving network</li>
                        <li>50% of global package delivery</li>
                        <li>$800B annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🥽</div>
                    <h3 class="feature-title">Virtual Reality Metaverse</h3>
                    <p class="feature-description">The Second Earth—photorealistic virtual world where humans work, learn, socialize, and live.</p>
                    <ul class="feature-details">
                        <li>8 billion people virtual world</li>
                        <li>Virtual real estate and economies</li>
                        <li>Neural interface for brain connection</li>
                        <li>$1.2T annual revenue potential</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚀</div>
                    <h3 class="feature-title">Space Commerce Platform</h3>
                    <p class="feature-description">Beyond Earth economy with space tourism, mining, colonization, and multi-planetary operations.</p>
                    <ul class="feature-details">
                        <li>First commercial space economy</li>
                        <li>10,000+ space operations target</li>
                        <li>Satellite internet for solar system</li>
                        <li>$1T annual revenue potential</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Vision Section -->
    <section class="vision" id="vision">
        <div class="vision-container">
            <div class="section-header">
                <div class="section-badge">🌍 Global Transformation</div>
                <h2 class="section-title">Our Mission</h2>
            </div>
            <div class="vision-content">
                <p class="vision-quote">"Create the world's first comprehensive digital economy ecosystem that connects every human, every business, every government, and every AI system into one unified platform—generating $10 trillion in annual transaction value while empowering 8 billion people globally."</p>
                <p class="vision-author">— Project UNIVERSE Mission Statement</p>
            </div>
        </div>
    </section>

    <!-- Timeline Section -->
    <section class="timeline" id="timeline">
        <div class="timeline-container">
            <div class="section-header">
                <div class="section-badge">⚡ Speed Execution</div>
                <h2 class="section-title">Road to $10 Trillion</h2>
                <p class="section-description">Fastest path to trillion-dollar valuation in human history</p>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-year">Year 1-2</div>
                    <h3 class="timeline-title">Foundation & Pilot Programs</h3>
                    <p class="timeline-description">Launch Universal Digital Identity and Global Digital Currency pilot programs. Establish government partnerships with 5 countries. Achieve $10B revenue and build core team of 10,000 engineers.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-year">Year 3-4</div>
                    <h3 class="timeline-title">Global Platform Launch</h3>
                    <p class="timeline-description">Deploy AI-Powered Super Platform and early Quantum-AI Cloud Infrastructure. Scale to 50 countries and 2 billion users. Achieve $100B revenue and $500B valuation.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-year">Year 5-6</div>
                    <h3 class="timeline-title">Mass Global Adoption</h3>
                    <p class="timeline-description">Full deployment across all ecosystem layers. 195 countries integrated with 5 billion users. Achieve $1T revenue and $2T valuation. IPO preparation begins.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-year">Year 7-8</div>
                    <h3 class="timeline-title">Global Dominance</h3>
                    <p class="timeline-description">Global Logistics Network and Virtual Reality Metaverse fully operational. 8 billion users connected. Achieve $5T revenue and $5T valuation. Largest company in history.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-year">Year 9-10</div>
                    <h3 class="timeline-title">Space Commerce & Beyond</h3>
                    <p class="timeline-description">Space Commerce Platform operational. Multi-planetary economy established. Achieve $10T revenue and $15T valuation. Post-scarcity civilization begins.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Global Impact Section -->
    <section class="features" style="background: rgba(0, 0, 0, 0.3);">
        <div class="features-container">
            <div class="section-header">
                <div class="section-badge">🌍 Global Impact</div>
                <h2 class="section-title">Transforming Civilization</h2>
                <p class="section-description">Creating solutions for humanity's greatest challenges while building sustainable prosperity.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎯</div>
                    <h3 class="feature-title">Poverty Elimination</h3>
                    <p class="feature-description">End extreme poverty by 2035 through Universal Basic Income powered by 1% of platform revenue.</p>
                    <ul class="feature-details">
                        <li>$100B annually for UBI distribution</li>
                        <li>1 billion people lifted out of poverty</li>
                        <li>AI-optimized resource allocation</li>
                        <li>Sustainable economic empowerment</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🧠</div>
                    <h3 class="feature-title">Education Revolution</h3>
                    <p class="feature-description">World-class education for all 8 billion humans through personalized AI tutors and immersive learning.</p>
                    <ul class="feature-details">
                        <li>Personalized AI tutors for everyone</li>
                        <li>VR/AR immersive learning experiences</li>
                        <li>100x improvement in learning outcomes</li>
                        <li>Universal access to knowledge</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">❤️</div>
                    <h3 class="feature-title">Healthcare Transformation</h3>
                    <p class="feature-description">Prevent 90% of diseases before symptoms through real-time monitoring and AI diagnosis.</p>
                    <ul class="feature-details">
                        <li>Real-time health monitoring for all</li>
                        <li>Personalized medicine for everyone</li>
                        <li>Double human lifespan globally</li>
                        <li>AI-powered early disease detection</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌱</div>
                    <h3 class="feature-title">Climate Solution</h3>
                    <p class="feature-description">Achieve carbon negativity by 2030 through 100% renewable energy infrastructure and AI optimization.</p>
                    <ul class="feature-details">
                        <li>100% renewable energy infrastructure</li>
                        <li>AI-optimized resource management</li>
                        <li>Reverse climate change completely</li>
                        <li>Sustainable planetary stewardship</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌌</div>
                    <h3 class="feature-title">Space Colonization</h3>
                    <p class="feature-description">Multi-planetary human civilization through commercial space infrastructure and lunar/Mars economies.</p>
                    <ul class="feature-details">
                        <li>Commercial space infrastructure</li>
                        <li>Lunar and Mars economic systems</li>
                        <li>Human species survival guarantee</li>
                        <li>Interstellar expansion foundation</li>
                    </ul>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏆</div>
                    <h3 class="feature-title">Economic Democracy</h3>
                    <p class="feature-description">Transform every individual into an entrepreneur with AI-amplified capabilities and unlimited opportunities.</p>
                    <ul class="feature-details">
                        <li>500M new jobs created globally</li>
                        <li>AI amplifies human capabilities 1000x</li>
                        <li>Universal entrepreneurship access</li>
                        <li>Post-scarcity economy achievement</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="contact-container">
            <div class="section-header">
                <div class="section-badge">🤝 Join the Revolution</div>
                <h2 class="section-title">Be Part of History</h2>
                <p class="section-description">Connect with us to explore co-founder opportunities, strategic partnerships, or investment possibilities in building the future of human civilization.</p>
            </div>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label class="form-label" for="name">Full Name</label>
                        <input type="text" id="name" name="name" class="form-input" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="email">Email Address</label>
                        <input type="email" id="email" name="email" class="form-input" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="role">Interest Area</label>
                        <select id="role" name="role" class="form-input" required>
                            <option value="">Select your interest</option>
                            <option value="cofounder">Co-Founder Opportunity</option>
                            <option value="investor">Strategic Investment</option>
                            <option value="government">Government Partnership</option>
                            <option value="technical">Technical Development</option>
                            <option value="business">Business Development</option>
                            <option value="other">Other Collaboration</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="message">Your Vision & Contribution</label>
                        <textarea id="message" name="message" class="form-textarea" placeholder="Tell us about your background, vision, and how you'd like to contribute to building the future of human civilization..." required></textarea>
                    </div>
                    <button type="submit" class="form-submit">Join the Revolution</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-logo">PROJECT UNIVERSE</div>
            <p class="footer-text">Building the future of human civilization, one connection at a time.</p>
            <div class="footer-links">
                <a href="#features">Ecosystem</a>
                <a href="#vision">Vision</a>
                <a href="#timeline">Timeline</a>
                <a href="#contact">Contact</a>
                <a href="mailto:contact@projectuniverse.io">Email</a>
            </div>
            <p class="footer-copyright">© 2025 Project UNIVERSE. Transforming humanity's future. Founded by Md. Ariful Islam (Rasel Munshi).</p>
        </div>
    </footer>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = window.innerWidth > 768 ? 50 : 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Random size between 2px and 6px
                const size = Math.random() * 4 + 2;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                
                // Random horizontal position
                particle.style.left = Math.random() * 100 + '%';
                
                // Random animation delay
                particle.style.animationDelay = Math.random() * 15 + 's';
                
                // Random animation duration
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                
                particlesContainer.appendChild(particle);
            }
        }

        // Smooth scrolling for navigation links
        document.addEventListener('DOMContentLoaded', function() {
            // Remove loading overlay
            setTimeout(() => {
                const loadingOverlay = document.getElementById('loadingOverlay');
                loadingOverlay.style.opacity = '0';
                setTimeout(() => {
                    loadingOverlay.style.display = 'none';
                }, 500);
            }, 1500);

            // Create particles
            createParticles();

            // Smooth scrolling for all anchor links
            const links = document.querySelectorAll('a[href^="#"]');
            links.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        const headerHeight = document.querySelector('.header').offsetHeight;
                        const targetPosition = targetElement.offsetTop - headerHeight;
                        window.scrollTo({
                            top: targetPosition,
                            behavior: 'smooth'
                        });
                    }
                });
            });

            // Header background opacity on scroll
            const header = document.querySelector('.header');
            window.addEventListener('scroll', function() {
                const scrolled = window.pageYOffset;
                const opacity = Math.min(scrolled / 100, 1);
                header.style.background = `rgba(0, 0, 0, ${0.7 + opacity * 0.3})`;
            });

            // Form submission
            const contactForm = document.getElementById('contactForm');
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form data
                const formData = new FormData(this);
                const name = formData.get('name');
                const email = formData.get('email');
                const role = formData.get('role');
                const message = formData.get('message');
                
                // Create mailto link
                const subject = encodeURIComponent('Project UNIVERSE - Revolutionary Partnership Opportunity');
                const body = encodeURIComponent(`Dear Project UNIVERSE Team,

My name is ${name} and I'm reaching out regarding partnership opportunities for your revolutionary $10 trillion ecosystem vision.

Interest Area: ${role}
Email: ${email}

My Vision & Contribution:
${message}

I believe in the transformative potential of Project UNIVERSE and would like to explore how I can contribute to building the future of human civilization.

Looking forward to making history together.

Best regards,
${name}`);
                
                const mailtoLink = `mailto:contact@projectuniverse.io?subject=${subject}&body=${body}`;
                
                // Show success message
                const submitButton = this.querySelector('.form-submit');
                const originalText = submitButton.textContent;
                submitButton.textContent = 'Message Prepared! Opening Email...';
                submitButton.style.background = 'linear-gradient(135deg, #28a745 0%, #20c997 100%)';
                
                // Open email client
                setTimeout(() => {
                    window.location.href = mailtoLink;
                    
                    // Reset button after delay
                    setTimeout(() => {
                        submitButton.textContent = originalText;
                        submitButton.style.background = 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)';
                        this.reset();
                    }, 3000);
                }, 1000);
            });

            // Card hover effects
            const cards = document.querySelectorAll('.feature-card, .stat-card');
            cards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px) scale(1.02)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1)';
                });
            });

            // Parallax effect for hero section
            window.addEventListener('scroll', function() {
                const scrolled = window.pageYOffset;
                const hero = document.querySelector('.hero');
                const parallaxSpeed = 0.5;
                hero.style.transform = `translateY(${scrolled * parallaxSpeed}px)`;
            });

            // Intersection Observer for animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);

            // Observe all cards and sections
            const animatedElements = document.querySelectorAll('.feature-card, .stat-card, .timeline-content, .vision-content');
            animatedElements.forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(30px)';
                el.style.transition = 'all 0.6s ease';
                observer.observe(el);
            });
        });

        // Dynamic particle creation
        setInterval(() => {
            if (document.querySelectorAll('.particle').length < 100) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                const size = Math.random() * 3 + 1;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                document.getElementById('particles').appendChild(particle);
                
                // Remove particle after animation
                setTimeout(() => {
                    particle.remove();
                }, 25000);
            }
        }, 2000);

        // Add floating animation to logo
        const logoIcon = document.querySelector('.logo-icon');
        setInterval(() => {
            logoIcon.style.transform = 'rotate(' + (Math.sin(Date.now() / 1000) * 5) + 'deg)';
        }, 50);

        // Add typing effect to hero title
        function typeWriter() {
            const heroTitle = document.querySelector('.hero h1');
            const text = 'PROJECT UNIVERSE';
            heroTitle.innerHTML = '';
            
            for (let i = 0; i < text.length; i++) {
                setTimeout(() => {
                    heroTitle.innerHTML += text.charAt(i);
                }, i * 100);
            }
        }

        // Start typing effect after loading
        setTimeout(typeWriter, 2000);
    </script>
</body>
</html>