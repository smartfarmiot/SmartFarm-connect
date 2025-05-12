<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SmartFarm - Agriculture Intelligente IoT | Solutions Connectées</title>
    <meta name="description" content="Découvrez SmartFarm, la solution IoT révolutionnaire pour une agriculture intelligente, durable et connectée. Capteurs, analyse de données et automatisation.">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Open+Sans:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2E7D32;
            --primary-light: #4CAF50;
            --primary-dark: #1B5E20;
            --accent: #8BC34A;
            --accent-light: #C5E1A5;
            --dark: #263238;
            --light: #F1F8E9;
            --white: #FFFFFF;
            --gray: #ECEFF1;
            --text: #37474F;
            --text-light: #607D8B;
            --danger: #F44336;
            --warning: #FFC107;
            --shadow-sm: 0 2px 8px rgba(0,0,0,0.1);
            --shadow-md: 0 4px 12px rgba(0,0,0,0.15);
            --shadow-lg: 0 8px 24px rgba(0,0,0,0.2);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            color: var(--text);
            line-height: 1.7;
            background-color: var(--white);
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            line-height: 1.3;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 0.9rem;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: var(--white);
            box-shadow: 0 4px 12px rgba(46, 125, 50, 0.3);
        }
        
        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(46, 125, 50, 0.4);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: var(--white);
        }
        
        .section {
            padding: 100px 0;
            position: relative;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }
        
        .section-title p {
            max-width: 700px;
            margin: 0 auto;
            color: var(--text-light);
            font-size: 1.1rem;
        }
        
        /* Header & Navigation */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            transition: var(--transition);
            padding: 20px 0;
        }
        
        .header.scrolled {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: var(--shadow-sm);
            padding: 15px 0;
        }
        
        .header.scrolled .nav-logo {
            color: var(--primary-dark);
        }
        
        .header.scrolled .nav-links a {
            color: var(--dark);
        }
        
        .header.scrolled .nav-links a:hover {
            color: var(--primary);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .nav-logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--white);
            display: flex;
            align-items: center;
        }
        
        .nav-logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            font-weight: 500;
            color: var(--white);
            position: relative;
            transition: var(--transition);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 700px;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), 
                        url('https://images.unsplash.com/photo-1500382017468-9049fed747ef?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100px;
            background: linear-gradient(to top, var(--white), transparent);
            z-index: 1;
        }
        
        .hero-content {
            max-width: 800px;
            color: var(--white);
            position: relative;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .hero-btns {
            display: flex;
            gap: 20px;
        }
        
        /* Technology Section */
        .tech-section {
            background-color: var(--white);
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .tech-card {
            background: var(--white);
            border-radius: 12px;
            padding: 40px 30px;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .tech-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-md);
        }
        
        .tech-icon {
            width: 80px;
            height: 80px;
            background-color: var(--accent-light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            color: var(--primary);
            font-size: 2rem;
            transition: var(--transition);
        }
        
        .tech-card:hover .tech-icon {
            background-color: var(--primary);
            color: var(--white);
            transform: rotateY(180deg);
        }
        
        .tech-card h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* Features Section */
        .features-section {
            background-color: var(--gray);
        }
        
        .feature-tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 50px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .feature-tab {
            padding: 12px 25px;
            background: var(--white);
            border-radius: 50px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
            border: 1px solid var(--gray);
        }
        
        .feature-tab.active {
            background: var(--primary);
            color: var(--white);
            box-shadow: var(--shadow-sm);
        }
        
        .feature-tab:hover:not(.active) {
            background: var(--accent-light);
        }
        
        .feature-content {
            display: none;
            animation: fadeIn 0.5s ease-out;
        }
        
        .feature-content.active {
            display: block;
        }
        
        .feature-box {
            background: var(--white);
            border-radius: 12px;
            padding: 40px;
            box-shadow: var(--shadow-sm);
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .feature-img {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow-md);
        }
        
        .feature-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: var(--transition);
        }
        
        .feature-img:hover img {
            transform: scale(1.05);
        }
        
        .feature-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .feature-text ul {
            list-style: none;
            margin-bottom: 30px;
        }
        
        .feature-text ul li {
            margin-bottom: 15px;
            position: relative;
            padding-left: 30px;
        }
        
        .feature-text ul li::before {
            content: '\f00c';
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            position: absolute;
            left: 0;
            top: 2px;
            color: var(--accent);
        }
        
        /* Systems Section */
        .systems-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .system-card {
            background: var(--white);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            position: relative;
        }
        
        .system-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }
        
        .system-img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .system-card:hover .system-img {
            transform: scale(1.05);
        }
        
        .system-content {
            padding: 25px;
            position: relative;
        }
        
        .system-badge {
            position: absolute;
            top: -20px;
            right: 20px;
            background: var(--primary);
            color: var(--white);
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
            box-shadow: var(--shadow-sm);
        }
        
        .system-content h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .system-stats {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid var(--gray);
        }
        
        .stat-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.9rem;
            color: var(--text-light);
        }
        
        .stat-item i {
            color: var(--accent);
        }
        
        /* Deployment Section */
        .deployment-section {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: var(--white);
        }
        
        .deployment-section .section-title h2,
        .deployment-section .section-title p {
            color: var(--white);
        }
        
        .deployment-steps {
            display: flex;
            justify-content: space-between;
            position: relative;
            margin-top: 50px;
        }
        
        .deployment-steps::before {
            content: '';
            position: absolute;
            top: 40px;
            left: 0;
            width: 100%;
            height: 3px;
            background: rgba(255, 255, 255, 0.2);
            z-index: 1;
        }
        
        .step {
            text-align: center;
            position: relative;
            z-index: 2;
            width: 23%;
        }
        
        .step-number {
            width: 80px;
            height: 80px;
            background: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: var(--primary);
            font-size: 1.8rem;
            font-weight: 700;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
        }
        
        .step:hover .step-number {
            transform: scale(1.1) rotate(10deg);
            background: var(--accent);
            color: var(--white);
        }
        
        .step h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        /* Testimonials */
        .testimonials-section {
            background-color: var(--light);
        }
        
        .testimonials-slider {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial {
            background: var(--white);
            padding: 40px;
            border-radius: 12px;
            box-shadow: var(--shadow-sm);
            text-align: center;
            display: none;
        }
        
        .testimonial.active {
            display: block;
            animation: fadeIn 0.5s ease-out;
        }
        
        .testimonial-text {
            font-size: 1.1rem;
            font-style: italic;
            margin-bottom: 30px;
            position: relative;
        }
        
        .testimonial-text::before,
        .testimonial-text::after {
            content: '"';
            font-size: 3rem;
            color: var(--accent-light);
            opacity: 0.3;
            position: absolute;
        }
        
        .testimonial-text::before {
            top: -20px;
            left: -10px;
        }
        
        .testimonial-text::after {
            bottom: -40px;
            right: -10px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
        }
        
        .author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            margin-bottom: 5px;
        }
        
        .author-info p {
            color: var(--text-light);
            font-size: 0.9rem;
        }
        
        .testimonial-nav {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 30px;
        }
        
        .testimonial-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--gray);
            cursor: pointer;
            transition: var(--transition);
        }
        
        .testimonial-dot.active {
            background: var(--primary);
            transform: scale(1.2);
        }
        
        /* CTA Section */
        .cta-section {
            background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), 
                        url('https://images.unsplash.com/photo-1532187863486-abf9dbad1b69?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
            color: var(--white);
            text-align: center;
        }
        
        .cta-content {
            max-width: 700px;
            margin: 0 auto;
        }
        
        .cta-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--white);
        }
        
        .cta-content p {
            margin-bottom: 30px;
            font-size: 1.1rem;
        }
        
        /* Footer */
        .footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 80px 0 30px;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }
        
        .footer-col h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            position: relative;
            display: inline-block;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--accent);
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .footer-logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        .footer-about p {
            margin-bottom: 20px;
            opacity: 0.8;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            opacity: 0.8;
            transition: var(--transition);
            display: inline-block;
        }
        
        .footer-links a:hover {
            opacity: 1;
            color: var(--accent);
            transform: translateX(5px);
        }
        
        .footer-contact li {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
            gap: 10px;
        }
        
        .footer-contact i {
            color: var(--accent);
            margin-top: 4px;
        }
        
        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .footer-social a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
        
        .footer-social a:hover {
            background: var(--accent);
            transform: translateY(-5px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes fadeInUp {
            from { 
                opacity: 0;
                transform: translateY(30px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .section {
                padding: 80px 0;
            }
            
            .feature-box {
                grid-template-columns: 1fr;
            }
            
            .feature-img {
                order: -1;
            }
            
            .deployment-steps {
                flex-wrap: wrap;
                gap: 40px;
            }
            
            .step {
                width: 45%;
            }
            
            .deployment-steps::before {
                display: none;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero-content h1 {
                font-size: 2.8rem;
            }
            
            .hero-btns {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .section {
                padding: 60px 0;
            }
            
            .hero-content h1 {
                font-size: 2.2rem;
            }
            
            .step {
                width: 100%;
                margin-bottom: 30px;
            }
            
            .step:last-child {
                margin-bottom: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header class="header" id="header">
        <div class="container header-container">
            <a href="#" class="nav-logo">
                <i class="fas fa-leaf"></i>SmartFarm
            </a>
            
            <nav class="nav-links">
                <a href="#technology">Technologie</a>
                <a href="#features">Fonctionnalités</a>
                <a href="#systems">Systèmes</a>
                <a href="#deployment">Déploiement</a>
                <a href="#contact">Contact</a>
            </nav>
            
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Révolutionnez votre agriculture avec SmartFarm</h1>
                <p>Une solution IoT complète pour maximiser vos rendements tout en préservant les ressources naturelles. Surveillance en temps réel, automatisation intelligente et analyses prédictives.</p>
                <div class="hero-btns">
                    <a href="#deployment" class="btn btn-primary">Découvrir nos solutions</a>
                    <a href="#contact" class="btn btn-outline">Contactez-nous</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Technology Section -->
    <section class="section tech-section" id="technology">
        <div class="container">
            <div class="section-title">
                <h2>Notre Technologie Innovante</h2>
                <p>SmartFarm combine les dernières avancées en IoT, intelligence artificielle et science des données pour une agriculture de précision.</p>
            </div>
            
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-microchip"></i>
                    </div>
                    <h3>ESP32 Haute Performance</h3>
                    <p>Microcontrôleur ultra-efficace avec double cœur et connectivité Wi-Fi/Bluetooth pour une communication sans faille.</p>
                </div>
                
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>Capteurs Intelligents</h3>
                    <p>DHT22 (précision 0.5°C), capteurs d'humidité capacitifs, détecteurs de qualité d'air et analyseurs de sol multiparamètres.</p>
                </div>
                
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>IA & Machine Learning</h3>
                    <p>Algorithmes prédictifs pour anticiper les maladies des plantes et optimiser les cycles d'irrigation.</p>
                </div>
                
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <h3>Cloud Sécurisé</h3>
                    <p>Stockage et analyse des données sur serveurs certifiés avec cryptage AES-256 pour une protection maximale.</p>
                </div>
                
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Application Mobile</h3>
                    <p>Tableau de bord complet avec alertes en temps réel et historique des données sur iOS et Android.</p>
                </div>
                
                <div class="tech-card">
                    <div class="tech-icon">
                        <i class="fas fa-chart-network"></i>
                    </div>
                    <h3>Réseau LoRaWAN</h3>
                    <p>Communication longue portée (15km) pour les exploitations étendues avec consommation énergétique minimale.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Features Section -->
    <section class="section features-section" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Fonctionnalités Clés</h2>
                <p>Découvrez comment SmartFarm transforme votre exploitation agricole en un écosystème intelligent et connecté.</p>
            </div>
            
            <div class="feature-tabs">
                <div class="feature-tab active" data-tab="monitoring">Surveillance</div>
                <div class="feature-tab" data-tab="automation">Automatisation</div>
                <div class="feature-tab" data-tab="analytics">Analyses</div>
                <div class="feature-tab" data-tab="security">Sécurité</div>
            </div>
            
            <div class="feature-content active" id="monitoring">
                <div class="feature-box">
                    <div class="feature-text">
                        <h3>Surveillance en Temps Réel 24/7</h3>
                        <p>Accédez à toutes les données de votre exploitation depuis n'importe où dans le monde avec une précision inégalée.</p>
                        <ul>
                            <li>Température et humidité de l'air en continu</li>
                            <li>Humidité du sol à différentes profondeurs</li>
                            <li>Niveaux de nutriments et pH du sol</li>
                            <li>Conditions météorologiques hyperlocales</li>
                            <li>Santé des plantes par imagerie multispectrale</li>
                        </ul>
                        <a href="#" class="btn btn-primary">Voir démonstration</a>
                    </div>
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1586771107445-d3ca888129ce?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Tableau de bord de surveillance SmartFarm">
                    </div>
                </div>
            </div>
            
            <div class="feature-content" id="automation">
                <div class="feature-box">
                    <div class="feature-text">
                        <h3>Automatisation Intelligente</h3>
                        <p>Notre système prend des décisions autonomes pour optimiser vos ressources et maximiser vos rendements.</p>
                        <ul>
                            <li>Irrigation adaptative selon les besoins des plantes</li>
                            <li>Contrôle climatique des serres automatisé</li>
                            <li>Optimisation des apports en engrais</li>
                            <li>Gestion intelligente de l'éclairage</li>
                            <li>Alertes et actions préventives</li>
                        </ul>
                        <a href="#" class="btn btn-primary">Voir démonstration</a>
                    </div>
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1592595896551-49b8c8a698ca?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Serre automatisée SmartFarm">
                    </div>
                </div>
            </div>
            
            <div class="feature-content" id="analytics">
                <div class="feature-box">
                    <div class="feature-text">
                        <h3>Analyses Prédictives Avancées</h3>
                        <p>Notre IA analyse des milliers de points de données pour vous fournir des insights actionnables.</p>
                        <ul>
                            <li>Prévision des rendements avec 95% de précision</li>
                            <li>Détection précoce des maladies des plantes</li>
                            <li>Optimisation des cycles de culture</li>
                            <li>Analyse des tendances historiques</li>
                            <li>Recommandations personnalisées</li>
                        </ul>
                        <a href="#" class="btn btn-primary">Voir démonstration</a>
                    </div>
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Analyses SmartFarm">
                    </div>
                </div>
            </div>
            
            <div class="feature-content" id="security">
                <div class="feature-box">
                    <div class="feature-text">
                        <h3>Sécurité Totale</h3>
                        <p>Protégez votre exploitation contre toutes les menaces physiques et numériques.</p>
                        <ul>
                            <li>Détection d'intrusion et surveillance périmétrique</li>
                            <li>Alarmes incendie et fuites de gaz</li>
                            <li>Protection contre les cyberattaques</li>
                            <li>Sauvegardes automatiques des données</li>
                            <li>Contrôle d'accès biométrique</li>
                        </ul>
                        <a href="#" class="btn btn-primary">Voir démonstration</a>
                    </div>
                    <div class="feature-img">
                        <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Sécurité SmartFarm">
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Systems Section -->
    <section class="section" id="systems">
        <div class="container">
            <div class="section-title">
                <h2>Nos Systèmes Clés en Main</h2>
                <p>Des solutions modulaires adaptées à tous les types d'exploitations agricoles.</p>
            </div>
            
            <div class="systems-grid">
                <div class="system-card">
                    <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Système d'irrigation intelligente" class="system-img">
                    <div class="system-content">
                        <div class="system-badge">Best-seller</div>
                        <h3>SmartIrrigation Pro</h3>
                        <p>Système d'irrigation intelligent qui réduit la consommation d'eau jusqu'à 45% tout en améliorant les rendements grâce à des capteurs d'humidité du sol et des prévisions météo intégrées.</p>
                        <div class="system-stats">
                            <div class="stat-item">
                                <i class="fas fa-tint"></i> Économie d'eau
                            </div>
                            <div class="stat-item">
                                <i class="fas fa-chart-line"></i> +25% rendement
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="system-card">
                    <img src="https://images.unsplash.com/photo-1592595896551-49b8c8a698ca?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Serre connectée" class="system-img">
                    <div class="system-content">
                        <h3>Greenhouse Master</h3>
                        <p>Solution complète pour serres connectées avec contrôle automatique du climat, de l'irrigation, de l'éclairage et de la fertilisation CO2.</p>
                        <div class="system-stats">
                            <div class="stat-item">
                                <i class="fas fa-temperature-low"></i> Climat optimal
                            </div>
                            <div class="stat-item">
                                <i class="fas fa-lightbulb"></i> LED intelligentes
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="system-card">
                    <img src="https://images.unsplash.com/photo-1618941719405-c6a0f5435a0e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Système de sécurité" class="system-img">
                    <div class="system-content">
                        <div class="system-badge">Nouveau</div>
                        <h3>FarmGuard Security</h3>
                        <p>Système de sécurité complet avec détection d'intrusion, caméras intelligentes, détection d'incendie et de gaz, et surveillance à distance 24/7.</p>
                        <div class="system-stats">
                            <div class="stat-item">
                                <i class="fas fa-shield-alt"></i> Protection 360°
                            </div>
                            <div class="stat-item">
                                <i class="fas fa-bell"></i> Alertes instantanées
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Deployment Section -->
    <section class="section deployment-section" id="deployment">
        <div class="container">
            <div class="section-title">
                <h2>Déploiement Sans Souci</h2>
                <p>Nous nous occupons de tout, de l'installation à la formation de votre équipe.</p>
            </div>
            
            <div class="deployment-steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Audit Initial</h3>
                    <p>Analyse approfondie de votre exploitation et définition des besoins spécifiques.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Solution Sur Mesure</h3>
                    <p>Configuration personnalisée des capteurs et des modules pour votre exploitation.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Installation</h3>
                    <p>Déploiement physique par nos techniciens certifiés en moins de 3 jours.</p>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <h3>Formation & Support</h3>
                    <p>Formation complète et support technique illimité pendant 1 an.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials Section -->
    <section class="section testimonials-section">
        <div class="container">
            <div class="section-title">
                <h2>Témoignages</h2>
                <p>Découvrez ce que nos clients disent de SmartFarm.</p>
            </div>
            
            <div class="testimonials-slider">
                <div class="testimonial active">
                    <div class="testimonial-text">
                        Après avoir installé SmartFarm sur mes 50 hectares de vignes, j'ai réduit ma consommation d'eau de 35% tout en augmentant la qualité de mes raisins. Le système de prédiction des maladies m'a permis d'éviter une catastrophe cette année.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Pierre Dubois">
                        </div>
                        <div class="author-info">
                            <h4>Pierre Dubois</h4>
                            <p>Vigneron, Bordeaux</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-text">
                        La serre connectée SmartFarm a transformé notre production de tomates. Nous avons pu passer de 3 à 5 cycles par an avec une qualité constante. L'application mobile est si simple que même mes ouvriers les moins tech-savvy l'utilisent quotidiennement.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sophie Martin">
                        </div>
                        <div class="author-info">
                            <h4>Sophie Martin</h4>
                            <p>Maraîchère, Provence</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial">
                    <div class="testimonial-text">
                        Le système de sécurité FarmGuard a détecté une intrusion à 3h du matin et prévenu la gendarmerie avant que les voleurs ne puissent emporter notre matériel. L'investissement a été amorti en une seule nuit !
                    </div>
                    <div class="testimonial-author">
                        <div class="author-img">
                            <img src="https://randomuser.me/api/portraits/men/68.jpg" alt="Jean Lefèvre">
                        </div>
                        <div class="author-info">
                            <h4>Jean Lefèvre</h4>
                            <p>Céréalier, Normandie</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-nav">
                    <div class="testimonial-dot active" data-slide="0"></div>
                    <div class="testimonial-dot" data-slide="1"></div>
                    <div class="testimonial-dot" data-slide="2"></div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section class="section cta-section">
        <div class="container">
            <div class="cta-content">
                <h2>Prêt à transformer votre exploitation agricole ?</h2>
                <p>Contactez nos experts pour une analyse gratuite de vos besoins et une démonstration personnalisée.</p>
                <a href="#contact" class="btn btn-primary">Demander une démo</a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="footer" id="contact">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="footer-logo">
                        <i class="fas fa-leaf"></i>SmartFarm
                    </div>
                    <div class="footer-about">
                        <p>Leader français des solutions IoT pour l'agriculture intelligente et durable. Nous combinons technologie de pointe et agronomie pour révolutionner les pratiques agricoles.</p>
                        <div class="footer-social">
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="#"><i class="fab fa-linkedin-in"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-youtube"></i></a>
                        </div>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Liens rapides</h3>
                    <ul class="footer-links">
                        <li><a href="#technology">Technologie</a></li>
                        <li><a href="#features">Fonctionnalités</a></li>
                        <li><a href="#systems">Systèmes</a></li>
                        <li><a href="#deployment">Déploiement</a></li>
                        <li><a href="#contact">Contact</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Nos Solutions</h3>
                    <ul class="footer-links">
                        <li><a href="#">SmartIrrigation</a></li>
                        <li><a href="#">Greenhouse Master</a></li>
                        <li><a href="#">FarmGuard Security</a></li>
                        <li><a href="#">Livestock Tracker</a></li>
                        <li><a href="#">Vineyard Pro</a></li>
                        <li><a href="#">Orchard Manager</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Contactez-nous</h3>
                    <ul class="footer-contact">
                        <li>
                            <i class="fas fa-map-marker-alt"></i>
                            <span>12 Rue de l'Innovation, 75015 Paris, France</span>
                        </li>
                        <li>
                            <i class="fas fa-phone-alt"></i>
                            <span>+33 1 23 45 67 89</span>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <span>contact@smartfarm.fr</span>
                        </li>
                        <li>
                            <i class="fas fa-clock"></i>
                            <span>Lun-Ven: 9h-18h</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 SmartFarm. Tous droits réservés. | <a href="#">Politique de confidentialité</a> | <a href="#">Conditions d'utilisation</a></p>
            </div>
        </div>
    </footer>
    
    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active') ? 
                '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });
        
        // Sticky Header
        const header = document.querySelector('.header');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Feature Tabs
        const featureTabs = document.querySelectorAll('.feature-tab');
        
        featureTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                // Remove active class from all tabs and contents
                featureTabs.forEach(t => t.classList.remove('active'));
                document.querySelectorAll('.feature-content').forEach(c => c.classList.remove('active'));
                
                // Add active class to clicked tab and corresponding content
                tab.classList.add('active');
                const tabId = tab.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Testimonial Slider
        const testimonialDots = document.querySelectorAll('.testimonial-dot');
        const testimonials = document.querySelectorAll('.testimonial');
        
        testimonialDots.forEach(dot => {
            dot.addEventListener('click', () => {
                const slideIndex = dot.getAttribute('data-slide');
                
                // Update dots
                testimonialDots.forEach(d => d.classList.remove('active'));
                dot.classList.add('active');
                
                // Update testimonials
                testimonials.forEach(t => t.classList.remove('active'));
                testimonials[slideIndex].classList.add('active');
            });
        });
        
        // Auto-rotate testimonials
        let currentTestimonial = 0;
        setInterval(() => {
            currentTestimonial = (currentTestimonial + 1) % testimonials.length;
            
            testimonialDots.forEach(d => d.classList.remove('active'));
            testimonialDots[currentTestimonial].classList.add('active');
            
            testimonials.forEach(t => t.classList.remove('active'));
            testimonials[currentTestimonial].classList.add('active');
        }, 5000);
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (navLinks.classList.contains('active')) {
                        navLinks.classList.remove('active');
                        mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                }
            });
        });
    </script>
</body>
</html>
