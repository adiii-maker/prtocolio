<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="PortfolioBuilder - Create your professional portfolio website in minutes">
    <meta name="keywords" content="portfolio builder, website builder, portfolio maker, no-code">
    <title>PortfolioBuilder - Create Your Professional Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        /* ==================== Global Styles ==================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #fff;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ==================== Navbar ==================== */

        .navbar {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 700;
            color: #667eea;
            cursor: pointer;
            text-decoration: none;
        }

        .logo i {
            font-size: 1.8rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: #333;
            transition: 0.3s;
        }

        /* ==================== Buttons ==================== */

        .btn {
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }

        .btn-secondary {
            background: #f0f0f0;
            color: #333;
            border: 2px solid #667eea;
        }

        .btn-secondary:hover {
            background: #667eea;
            color: white;
        }

        .btn-small {
            padding: 8px 15px;
            font-size: 0.9rem;
        }

        /* ==================== Hero Section ==================== */

        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 150px 0;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        /* ==================== Features Section ==================== */

        .features {
            padding: 80px 0;
        }

        .features h2,
        .templates h2,
        .pricing h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #333;
        }

        .features-grid,
        .template-grid,
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
        }

        .feature-card i {
            font-size: 2.5rem;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .feature-card p {
            color: #666;
        }

        /* ==================== Templates Section ==================== */

        .templates {
            padding: 80px 0;
            background: #f9f9f9;
        }

        .template-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }

        .template-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
        }

        .template-preview {
            height: 150px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .template-demo {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .template-card h3 {
            padding: 1rem;
            font-size: 1.1rem;
            text-align: center;
        }

        .template-card p {
            text-align: center;
            color: #666;
            padding: 0 1rem 1rem;
            font-size: 0.9rem;
        }

        /* ==================== Pricing Section ==================== */

        .pricing {
            padding: 80px 0;
        }

        .pricing-grid {
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        }

        .pricing-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
        }

        .pricing-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
        }

        .pricing-card.featured {
            border: 2px solid #667eea;
            transform: scale(1.05);
        }

        .pricing-card .badge {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: #667eea;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        .pricing-card h3 {
            font-size: 1.5rem;
            margin: 1rem 0;
        }

        .price {
            display: flex;
            align-items: baseline;
            justify-content: center;
            gap: 5px;
            margin: 1rem 0;
        }

        .price .currency {
            font-size: 1.2rem;
            color: #667eea;
        }

        .price .amount {
            font-size: 3rem;
            font-weight: 700;
            color: #333;
        }

        .price .period {
            color: #666;
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        .features-list {
            list-style: none;
            margin: 2rem 0;
            text-align: left;
        }

        .features-list li {
            padding: 0.8rem 0;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .features-list i {
            width: 20px;
            color: #667eea;
        }

        .features-list i.fa-times {
            color: #ccc;
        }

        .pricing-card .btn {
            width: 100%;
            margin-top: 1rem;
        }

        /* ==================== CTA Section ==================== */

        .cta {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .cta p {
            font-size: 1.1rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        /* ==================== Footer ==================== */

        .footer {
            background: #333;
            color: white;
            padding: 40px 0;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            margin-bottom: 1rem;
            color: #667eea;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: #667eea;
        }

        .footer-section li {
            margin-bottom: 0.5rem;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #555;
            color: #999;
        }

        /* ==================== Modal & Builder ==================== */

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            overflow-y: auto;
        }

        .modal.active {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: white;
            border-radius: 10px;
            width: 95%;
            height: 90vh;
            max-width: 1400px;
            display: flex;
            flex-direction: column;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem;
            border-bottom: 1px solid #eee;
        }

        .modal-header h2 {
            color: #333;
        }

        .close-btn {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: #999;
            transition: color 0.3s ease;
        }

        .close-btn:hover {
            color: #333;
        }

        .modal-body {
            flex: 1;
            overflow: hidden;
        }

        .builder-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            height: 100%;
            gap: 0;
        }

        .editor-panel,
        .preview-panel {
            overflow-y: auto;
            padding: 2rem;
        }

        .editor-panel {
            border-right: 1px solid #eee;
            background: #f9f9f9;
        }

        /* ==================== Tabs ==================== */

        .tabs {
            display: flex;
            gap: 10px;
            margin-bottom: 2rem;
            border-bottom: 2px solid #eee;
            overflow-x: auto;
        }

        .tab-btn {
            padding: 10px 15px;
            background: none;
            border: none;
            cursor: pointer;
            font-weight: 600;
            color: #999;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
            margin-bottom: -2px;
            white-space: nowrap;
        }

        .tab-btn.active {
            color: #667eea;
            border-bottom-color: #667eea;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* ==================== Forms ==================== */

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: #333;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
            font-size: 0.95rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 5px rgba(102, 126, 234, 0.2);
        }

        /* ==================== Color Picker ==================== */

        .color-picker {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .color-picker input[type="color"] {
            width: 50px;
            height: 40px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }

        .color-picker span {
            font-weight: 600;
            color: #667eea;
        }

        .color-schemes {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #ddd;
        }

        .color-schemes label {
            display: block;
            margin-bottom: 1rem;
        }

        .scheme-buttons {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
        }

        .scheme-buttons button {
            width: 100%;
            height: 40px;
            border: 2px solid #ddd;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .scheme-buttons button:hover {
            transform: scale(1.05);
            border-color: #667eea;
        }

        /* ==================== Preview Frame ==================== */

        .preview-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }

        .preview-controls {
            display: flex;
            gap: 10px;
        }

        .preview-controls button {
            background: #667eea;
            color: white;
            border: none;
            padding: 8px 12px;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .preview-controls button:hover {
            background: #764ba2;
        }

        .preview-frame {
            width: 100%;
            height: calc(100% - 80px);
            border: 1px solid #eee;
            border-radius: 5px;
            background: white;
            overflow: auto;
        }

        /* ==================== Toast Notification ==================== */

        .toast {
            position: fixed;
            bottom: -100px;
            left: 50%;
            transform: translateX(-50%);
            background: #333;
            color: white;
            padding: 15px 25px;
            border-radius: 5px;
            z-index: 2000;
            transition: bottom 0.3s ease;
        }

        .toast.show {
            bottom: 20px;
        }

        /* ==================== Responsive Design ==================== */

        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                display: none;
            }

            .nav-links.active {
                display: flex;
                position: absolute;
                top: 60px;
                left: 0;
                right: 0;
                background: white;
                flex-direction: column;
                gap: 0;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
                border-radius: 0;
            }

            .hero-content h1 {
                font-size: 2rem;
            }

            .features-grid,
            .template-grid,
            .pricing-grid {
                grid-template-columns: 1fr;
            }

            .pricing-card.featured {
                transform: scale(1);
            }

            .builder-container {
                grid-template-columns: 1fr;
            }

            .editor-panel {
                border-right: none;
                border-bottom: 1px solid #eee;
            }

            .tabs {
                overflow-x: auto;
            }

            .tab-btn {
                white-space: nowrap;
            }

            .modal-content {
                width: 100%;
                height: 100vh;
                border-radius: 0;
            }

            .modal-body {
                padding: 0;
            }

            .editor-panel,
            .preview-panel {
                padding: 1rem;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 1.5rem;
            }

            .features h2,
            .templates h2,
            .pricing h2,
            .cta h2 {
                font-size: 1.8rem;
            }

            .nav-links {
                gap: 1rem;
            }

            .pricing-card {
                padding: 1rem;
            }

            .form-group input,
            .form-group textarea {
                padding: 8px;
                font-size: 16px;
            }

            .scheme-buttons {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container">
            <div class="nav-wrapper">
                <div class="logo">
                    <i class="fas fa-briefcase"></i>
                    <span>PortfolioBuilder</span>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#features">Features</a></li>
                    <li><a href="#templates">Templates</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#" onclick="startBuilder(); return false;">Start Building</a></li>
                </ul>
                <div class="hamburger" id="hamburger">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Create Your Professional Portfolio</h1>
                <p>Build a stunning portfolio website in minutes. No coding required!</p>
                <button class="btn btn-primary" onclick="startBuilder()">
                    <i class="fas fa-rocket"></i> Start Building Free
                </button>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <h2>Why Choose PortfolioBuilder?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-paint-brush"></i>
                    <h3>Beautiful Templates</h3>
                    <p>Choose from 50+ professionally designed templates</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-code"></i>
                    <h3>No Coding Required</h3>
                    <p>Drag and drop editor - anyone can use it</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>Mobile Responsive</h3>
                    <p>Your portfolio looks perfect on all devices</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-tachometer-alt"></i>
                    <h3>Lightning Fast</h3>
                    <p>Optimized for speed and performance</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-globe"></i>
                    <h3>Custom Domain</h3>
                    <p>Connect your own domain easily</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-shield-alt"></i>
                    <h3>Secure & Safe</h3>
                    <p>Enterprise-grade security for your data</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Templates Section -->
    <section id="templates" class="templates">
        <div class="container">
            <h2>Choose Your Template</h2>
            <div class="template-grid">
                <div class="template-card" onclick="selectTemplate('minimal')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Minimal</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Clean & Simple</p>
                            </div>
                        </div>
                    </div>
                    <h3>Minimal</h3>
                    <p>Clean and minimalist design</p>
                </div>

                <div class="template-card" onclick="selectTemplate('professional')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Professional</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Business Ready</p>
                            </div>
                        </div>
                    </div>
                    <h3>Professional</h3>
                    <p>Perfect for business</p>
                </div>

                <div class="template-card" onclick="selectTemplate('creative')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Creative</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Stand Out</p>
                            </div>
                        </div>
                    </div>
                    <h3>Creative</h3>
                    <p>Bold and eye-catching</p>
                </div>

                <div class="template-card" onclick="selectTemplate('developer')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Developer</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Tech Focused</p>
                            </div>
                        </div>
                    </div>
                    <h3>Developer</h3>
                    <p>For tech professionals</p>
                </div>

                <div class="template-card" onclick="selectTemplate('startup')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Startup</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Modern Vibes</p>
                            </div>
                        </div>
                    </div>
                    <h3>Startup</h3>
                    <p>Perfect for startups</p>
                </div>

                <div class="template-card" onclick="selectTemplate('elegant')">
                    <div class="template-preview" style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);">
                        <div class="template-demo">
                            <div style="padding: 20px; color: white; text-align: center;">
                                <h4 style="margin: 0; font-size: 18px;">Elegant</h4>
                                <p style="margin: 5px 0 0 0; font-size: 12px;">Sophisticated</p>
                            </div>
                        </div>
                    </div>
                    <h3>Elegant</h3>
                    <p>Sophisticated design</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="pricing">
        <div class="container">
            <h2>Simple, Transparent Pricing</h2>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>Free</h3>
                    <div class="price">
                        <span class="currency">$</span>
                        <span class="amount">0</span>
                    </div>
                    <p class="period">Forever free</p>
                    <ul class="features-list">
                        <li><i class="fas fa-check"></i> 1 Portfolio</li>
                        <li><i class="fas fa-check"></i> Basic Templates</li>
                        <li><i class="fas fa-check"></i> Subdomain</li>
                        <li><i class="fas fa-times"></i> Custom Domain</li>
                        <li><i class="fas fa-times"></i> Premium Support</li>
                    </ul>
                    <button class="btn btn-secondary">Get Started</button>
                </div>

                <div class="pricing-card featured">
                    <div class="badge">Popular</div>
                    <h3>Professional</h3>
                    <div class="price">
                        <span class="currency">$</span>
                        <span class="amount">9</span>
                    </div>
                    <p class="period">per month</p>
                    <ul class="features-list">
                        <li><i class="fas fa-check"></i> 5 Portfolios</li>
                        <li><i class="fas fa-check"></i> All Templates</li>
                        <li><i class="fas fa-check"></i> Custom Domain</li>
                        <li><i class="fas fa-check"></i> Priority Support</li>
                        <li><i class="fas fa-times"></i> Analytics</li>
                    </ul>
                    <button class="btn btn-primary">Upgrade Now</button>
                </div>

                <div class="pricing-card">
                    <h3>Enterprise</h3>
                    <div class="price">
                        <span class="currency">$</span>
                        <span class="amount">29</span>
                    </div>
                    <p class="period">per month</p>
                    <ul class="features-list">
                        <li><i class="fas fa-check"></i> Unlimited Portfolios</li>
                        <li><i class="fas fa-check"></i> All Features</li>
                        <li><i class="fas fa-check"></i> Multiple Domains</li>
                        <li><i class="fas fa-check"></i> 24/7 Support</li>
                        <li><i class="fas fa-check"></i> Advanced Analytics</li>
                    </ul>
                    <button class="btn btn-secondary">Contact Sales</button>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
        <div class="container">
            <h2>Ready to Build Your Portfolio?</h2>
            <p>Join thousands of professionals who've already created their portfolios</p>
            <button class="btn btn-primary" onclick="startBuilder()">Start Free Today</button>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>About</h4>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Careers</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Product</h4>
                    <ul>
                        <li><a href="#">Features</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Legal</h4>
                    <ul>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 PortfolioBuilder. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Builder Modal -->
    <div id="builderModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Build Your Portfolio</h2>
                <button class="close-btn" onclick="closeBuilder()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="builder-container">
                    <!-- Left Panel - Editor -->
                    <div class="editor-panel">
                        <div class="tabs">
                            <button class="tab-btn active" onclick="switchTab('basic')">Basic Info</button>
                            <button class="tab-btn" onclick="switchTab('skills')">Skills</button>
                            <button class="tab-btn" onclick="switchTab('projects')">Projects</button>
                            <button class="tab-btn" onclick="switchTab('social')">Social</button>
                            <button class="tab-btn" onclick="switchTab('colors')">Design</button>
                        </div>

                        <!-- Basic Info Tab -->
                        <div id="basic-tab" class="tab-content active">
                            <div class="form-group">
                                <label>Full Name</label>
                                <input type="text" id="fullName" placeholder="Your full name" value="John Doe" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Professional Title</label>
                                <input type="text" id="title" placeholder="e.g., Full Stack Developer" value="Full Stack Developer" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Bio/About</label>
                                <textarea id="bio" placeholder="Tell about yourself..." rows="4" oninput="updatePreview()">Passionate developer creating amazing web experiences with modern technologies.</textarea>
                            </div>
                            <div class="form-group">
                                <label>Email</label>
                                <input type="email" id="email" placeholder="your@email.com" value="john@example.com" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Phone</label>
                                <input type="tel" id="phone" placeholder="+1 (555) 123-4567" value="+1 (555) 123-4567" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Location</label>
                                <input type="text" id="location" placeholder="City, Country" value="New York, USA" oninput="updatePreview()">
                            </div>
                        </div>

                        <!-- Skills Tab -->
                        <div id="skills-tab" class="tab-content">
                            <div class="form-group">
                                <label>Add Skills (comma separated)</label>
                                <textarea id="skills" placeholder="HTML, CSS, JavaScript, React, Node.js..." rows="6" oninput="updatePreview()">HTML5, CSS3, JavaScript, React, Node.js, MongoDB, Express.js, REST APIs, Git, Firebase, UI/UX Design</textarea>
                            </div>
                        </div>

                        <!-- Projects Tab -->
                        <div id="projects-tab" class="tab-content">
                            <div id="projectsList"></div>
                            <button class="btn btn-secondary btn-small" onclick="addProject()">
                                <i class="fas fa-plus"></i> Add Project
                            </button>
                        </div>

                        <!-- Social Tab -->
                        <div id="social-tab" class="tab-content">
                            <div class="form-group">
                                <label>GitHub URL</label>
                                <input type="url" id="githubUrl" placeholder="https://github.com/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>LinkedIn URL</label>
                                <input type="url" id="linkedinUrl" placeholder="https://linkedin.com/in/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Twitter URL</label>
                                <input type="url" id="twitterUrl" placeholder="https://twitter.com/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Portfolio Website</label>
                                <input type="url" id="websiteUrl" placeholder="https://yourwebsite.com" oninput="updatePreview()">
                            </div>
                        </div>

                        <!-- Design Tab -->
                        <div id="colors-tab" class="tab-content">
                            <div class="form-group">
                                <label>Primary Color</label>
                                <div class="color-picker">
                                    <input type="color" id="primaryColor" value="#667eea" oninput="updateColors()">
                                    <span id="primaryColorText">#667eea</span>
                                </div>
                            </div>
                            <div class="form-group">
                                <label>Accent Color</label>
                                <div class="color-picker">
                                    <input type="color" id="accentColor" value="#764ba2" oninput="updateColors()">
                                    <span id="accentColorText">#764ba2</span>
                                </div>
                            </div>
                            <div class="form-group">
                                <label>Font Style</label>
                                <select id="fontStyle" oninput="updatePreview()">
                                    <option value="modern">Modern (Poppins)</option>
                                    <option value="classic">Classic (Georgia)</option>
                                    <option value="minimal">Minimal (Monospace)</option>
                                </select>
                            </div>
                            <div class="color-schemes">
                                <label>Quick Color Schemes:</label>
                                <div class="scheme-buttons">
                                    <button onclick="applyColorScheme(0)" title="Purple Dream" style="background: linear-gradient(135deg, #667eea, #764ba2);"></button>
                                    <button onclick="applyColorScheme(1)" title="Pink Vibes" style="background: linear-gradient(135deg, #f093fb, #f5576c);"></button>
                                    <button onclick="applyColorScheme(2)" title="Blue Ocean" style="background: linear-gradient(135deg, #4facfe, #00f2fe);"></button>
                                    <button onclick="applyColorScheme(3)" title="Green Fresh" style="background: linear-gradient(135deg, #43e97b, #38f9d7);"></button>
                                    <button onclick="applyColorScheme(4)" title="Sunset" style="background: linear-gradient(135deg, #fa709a, #fee140);"></button>
                                    <button onclick="applyColorScheme(5)" title="Night" style="background: linear-gradient(135deg, #30cfd0, #330867);"></button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Right Panel - Preview -->
                    <div class="preview-panel">
                        <div class="preview-header">
                            <h3>Live Preview</h3>
                            <div class="preview-controls">
                                <button onclick="exportPortfolio()" title="Export as HTML">
                                    <i class="fas fa-download"></i>
                                </button>
                                <button onclick="copyLink()" title="Copy Preview Link">
                                    <i class="fas fa-link"></i>
                                </button>
                            </div>
                        </div>
                        <div id="previewFrame" class="preview-frame"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="toast"></div>

    <script>
        /* ==================== Portfolio Builder JavaScript ==================== */

        let portfolioData = {
            fullName: 'John Doe',
            title: 'Full Stack Developer',
            bio: 'Passionate developer creating amazing web experiences with modern technologies.',
            email: 'john@example.com',
            phone: '+1 (555) 123-4567',
            location: 'New York, USA',
            skills: ['HTML5', 'CSS3', 'JavaScript', 'React', 'Node.js', 'MongoDB', 'Express.js', 'REST APIs', 'Git', 'Firebase', 'UI/UX Design'],
            projects: [
                { name: 'E-Commerce Platform', description: 'Full-stack e-commerce solution with React and Node.js' },
                { name: 'Task Manager App', description: 'React-based task management application' }
            ],
            colors: {
                primary: '#667eea',
                accent: '#764ba2'
            },
            fontStyle: 'modern',
            socialLinks: {
                github: '',
                linkedin: '',
                twitter: '',
                website: ''
            }
        };

        let projects = [];

        /* ==================== Modal Functions ==================== */

        function startBuilder() {
            const modal = document.getElementById('builderModal');
            modal.classList.add('active');
            loadPortfolioData();
            setTimeout(updatePreview, 100);
        }

        function closeBuilder() {
            const modal = document.getElementById('builderModal');
            modal.classList.remove('active');
        }

        function switchTab(tabName) {
            // Hide all tabs
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });

            // Remove active class from all buttons
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('active');
            });

            // Show selected tab
            const selectedTab = document.getElementById(tabName + '-tab');
            if (selectedTab) {
                selectedTab.classList.add('active');
            }
            
            // Mark the button as active
            event.target.classList.add('active');
        }

        /* ==================== Data Management ==================== */

        function loadPortfolioData() {
            document.getElementById('fullName').value = portfolioData.fullName;
            document.getElementById('title').value = portfolioData.title;
            document.getElementById('bio').value = portfolioData.bio;
            document.getElementById('email').value = portfolioData.email;
            document.getElementById('phone').value = portfolioData.phone;
            document.getElementById('location').value = portfolioData.location;
            document.getElementById('skills').value = portfolioData.skills.join(', ');
            document.getElementById('primaryColor').value = portfolioData.colors.primary;
            document.getElementById('accentColor').value = portfolioData.colors.accent;
            document.getElementById('fontStyle').value = portfolioData.fontStyle;
            
            // Social links
            document.getElementById('githubUrl').value = portfolioData.socialLinks.github || '';
            document.getElementById('linkedinUrl').value = portfolioData.socialLinks.linkedin || '';
            document.getElementById('twitterUrl').value = portfolioData.socialLinks.twitter || '';
            document.getElementById('websiteUrl').value = portfolioData.socialLinks.website || '';
            
            // Update color text
            document.getElementById('primaryColorText').textContent = portfolioData.colors.primary;
            document.getElementById('accentColorText').textContent = portfolioData.colors.accent;
            
            loadProjects();
        }

        function savePortfolioData() {
            portfolioData.fullName = document.getElementById('fullName').value || 'Your Name';
            portfolioData.title = document.getElementById('title').value || 'Professional Title';
            portfolioData.bio = document.getElementById('bio').value || 'Your bio here';
            portfolioData.email = document.getElementById('email').value || 'email@example.com';
            portfolioData.phone = document.getElementById('phone').value || '+1 (555) 123-4567';
            portfolioData.location = document.getElementById('location').value || 'City, Country';
            portfolioData.skills = document.getElementById('skills').value
                .split(',')
                .map(skill => skill.trim())
                .filter(skill => skill);
            portfolioData.fontStyle = document.getElementById('fontStyle').value;
            
            // Social links
            portfolioData.socialLinks.github = document.getElementById('githubUrl').value;
            portfolioData.socialLinks.linkedin = document.getElementById('linkedinUrl').value;
            portfolioData.socialLinks.twitter = document.getElementById('twitterUrl').value;
            portfolioData.socialLinks.website = document.getElementById('websiteUrl').value;
        }

        /* ==================== Project Management ==================== */

        function addProject() {
            const projectName = prompt('Enter project name:');
            if (projectName) {
                const projectDesc = prompt('Enter project description:');
                projects.push({
                    name: projectName,
                    description: projectDesc || 'No description'
                });
                saveProjects();
                loadProjects();
                updatePreview();
                showToast('Project added successfully!');
            }
        }

        function deleteProject(index) {
            projects.splice(index, 1);
            saveProjects();
            loadProjects();
            updatePreview();
            showToast('Project deleted!');
        }

        function saveProjects() {
            portfolioData.projects = projects;
            localStorage.setItem('portfolioProjects', JSON.stringify(projects));
        }

        function loadProjects() {
            const projectsList = document.getElementById('projectsList');
            projectsList.innerHTML = '';

            if (portfolioData.projects && portfolioData.projects.length > 0) {
                portfolioData.projects.forEach((project, index) => {
                    const projectEl = document.createElement('div');
                    projectEl.style.cssText = `
                        background: white;
                        padding: 12px;
                        border-radius: 5px;
                        margin-bottom: 10px;
                        display: flex;
                        justify-content: space-between;
                        align-items: center;
                        border: 1px solid #ddd;
                    `;
                    projectEl.innerHTML = `
                        <div>
                            <strong>${project.name}</strong>
                            <p style="margin: 5px 0 0 0; font-size: 0.9rem; color: #666;">${project.description}</p>
                        </div>
                        <button onclick="deleteProject(${index})" style="background: #ff6b6b; color: white; border: none; padding: 5px 10px; border-radius: 3px; cursor: pointer;">
                            <i class="fas fa-trash"></i>
                        </button>
                    `;
                    projectsList.appendChild(projectEl);
                });
            } else {
                projectsList.innerHTML = '<p style="color: #999; text-align: center;">No projects added yet</p>';
            }
        }

        /* ==================== Colors ==================== */

        function updateColors() {
            const primaryColor = document.getElementById('primaryColor').value;
            const accentColor = document.getElementById('accentColor').value;

            portfolioData.colors.primary = primaryColor;
            portfolioData.colors.accent = accentColor;

            document.getElementById('primaryColorText').textContent = primaryColor;
            document.getElementById('accentColorText').textContent = accentColor;

            updatePreview();
        }

        /* ==================== Preview ==================== */

        function updatePreview() {
            savePortfolioData();
            const htmlContent = generatePortfolioHTML();
            const previewFrame = document.getElementById('previewFrame');
            previewFrame.innerHTML = htmlContent;
        }

        function generatePortfolioHTML() {
            const { fullName, title, bio, email, phone, location, skills, projects, colors, fontStyle, socialLinks } = portfolioData;

            const skillsHTML = skills.map(skill => 
                `<span class="skill-badge">${skill}</span>`
            ).join('');

            const projectsHTML = projects && projects.length > 0 ? projects.map(project => `
                <div class="project-item">
                    <h4>${project.name}</h4>
                    <p>${project.description}</p>
                </div>
            `).join('') : '';

            const fontFamily = fontStyle === 'classic' ? 'Georgia, serif' : fontStyle === 'minimal' ? 'monospace' : "'Poppins', sans-serif";

            const socialHTML = `
                <div class="social-links">
                    ${socialLinks.github ? `<a href="${socialLinks.github}" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>` : ''}
                    ${socialLinks.linkedin ? `<a href="${socialLinks.linkedin}" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>` : ''}
                    ${socialLinks.twitter ? `<a href="${socialLinks.twitter}" target="_blank" title="Twitter"><i class="fab fa-twitter"></i></a>` : ''}
                    ${socialLinks.website ? `<a href="${socialLinks.website}" target="_blank" title="Website"><i class="fas fa-globe"></i></a>` : ''}
                </div>
            `;

            return `
                <!DOCTYPE html>
                <html>
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>${fullName} - Portfolio</title>
                    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
                    <style>
                        * {
                            margin: 0;
                            padding: 0;
                            box-sizing: border-box;
                        }

                        body {
                            font-family: ${fontFamily};
                            line-height: 1.6;
                            color: #333;
                            background: #f9f9f9;
                        }

                        header {
                            background: linear-gradient(135deg, ${colors.primary} 0%, ${colors.accent} 100%);
                            color: white;
                            padding: 60px 20px;
                            text-align: center;
                        }

                        header h1 {
                            font-size: 2.5rem;
                            margin-bottom: 10px;
                        }

                        header p {
                            font-size: 1.2rem;
                            margin-bottom: 10px;
                            opacity: 0.9;
                        }

                        section {
                            padding: 40px 20px;
                            max-width: 900px;
                            margin: 0 auto;
                            background: white;
                            margin-bottom: 20px;
                            border-radius: 8px;
                        }

                        section h2 {
                            color: ${colors.primary};
                            margin-bottom: 20px;
                            font-size: 1.8rem;
                            border-bottom: 3px solid ${colors.primary};
                            padding-bottom: 10px;
                        }

                        .contact-info {
                            display: grid;
                            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
                            gap: 15px;
                        }

                        .contact-info p {
                            display: flex;
                            align-items: center;
                            gap: 10px;
                        }

                        .contact-info i {
                            color: ${colors.primary};
                            font-size: 1.2rem;
                        }

                        .skills-container {
                            display: flex;
                            flex-wrap: wrap;
                            gap: 10px;
                        }

                        .skill-badge {
                            background: ${colors.primary};
                            color: white;
                            padding: 8px 15px;
                            border-radius: 20px;
                            font-size: 0.9rem;
                            font-weight: 600;
                        }

                        .projects-grid {
                            display: grid;
                            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                            gap: 20px;
                        }

                        .project-item {
                            background: #f9f9f9;
                            padding: 20px;
                            border-radius: 8px;
                            border-left: 4px solid ${colors.primary};
                        }

                        .project-item h4 {
                            color: ${colors.primary};
                            margin-bottom: 10px;
                        }

                        .social-links {
                            display: flex;
                            justify-content: center;
                            gap: 15px;
                            margin-top: 20px;
                        }

                        .social-links a {
                            display: inline-flex;
                            align-items: center;
                            justify-content: center;
                            width: 45px;
                            height: 45px;
                            background: ${colors.primary};
                            color: white;
                            border-radius: 50%;
                            text-decoration: none;
                            transition: all 0.3s ease;
                            font-size: 1.2rem;
                        }

                        .social-links a:hover {
                            background: ${colors.accent};
                            transform: translateY(-3px);
                        }

                        footer {
                            background: #333;
                            color: white;
                            text-align: center;
                            padding: 20px;
                        }

                        @media (max-width: 600px) {
                            header h1 {
                                font-size: 1.8rem;
                            }
                            
                            section {
                                padding: 20px;
                            }
                        }
                    </style>
                </head>
                <body>
                    <header>
                        <h1>${fullName}</h1>
                        <p>${title}</p>
                        <p style="font-size: 0.95rem; margin-top: 15px;">${bio}</p>
                        ${socialLinks.github || socialLinks.linkedin || socialLinks.twitter || socialLinks.website ? socialHTML : ''}
                    </header>

                    <section>
                        <h2><i class="fas fa-envelope"></i> Contact</h2>
                        <div class="contact-info">
                            <p><i class="fas fa-envelope"></i> <a href="mailto:${email}" style="color: inherit; text-decoration: none;">${email}</a></p>
                            <p><i class="fas fa-phone"></i> <a href="tel:${phone}" style="color: inherit; text-decoration: none;">${phone}</a></p>
                            <p><i class="fas fa-map-marker-alt"></i> ${location}</p>
                        </div>
                    </section>

                    <section>
                        <h2><i class="fas fa-star"></i> Skills</h2>
                        <div class="skills-container">
                            ${skillsHTML}
                        </div>
                    </section>

                    ${projects && projects.length > 0 ? `
                        <section>
                            <h2><i class="fas fa-briefcase"></i> Projects</h2>
                            <div class="projects-grid">
                                ${projectsHTML}
                            </div>
                        </section>
                    ` : ''}

                    <footer>
                        <p>&copy; 2025 ${fullName}. All rights reserved.</p>
                        <p>Built with PortfolioBuilder</p>
                    </footer>
                </body>
                </html>
            `;
        }

        /* ==================== Export & Share ==================== */

        function exportPortfolio() {
            savePortfolioData();
            const htmlContent = generatePortfolioHTML();
            const blob = new Blob([htmlContent], { type: 'text/html;charset=utf-8' });
            const link = document.createElement('a');
            const url = URL.createObjectURL(blob);
            link.setAttribute('href', url);
            link.setAttribute('download', `${portfolioData.fullName.replace(/\s+/g, '-').toLowerCase()}-portfolio.html`);
            link.style.visibility = 'hidden';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
            showToast('Portfolio exported successfully!');
        }

        function copyLink() {
            const text = window.location.href;
            navigator.clipboard.writeText(text).then(() => {
                showToast('Link copied to clipboard!');
            }).catch(err => {
                showToast('Failed to copy link');
            });
        }

        /* ==================== Template Selection ==================== */

        function selectTemplate(templateName) {
            const templates = {
                minimal: {
                    primary: '#667eea',
                    accent: '#764ba2',
                    font: 'modern'
                },
                professional: {
                    primary: '#1e3c72',
                    accent: '#2a5298',
                    font: 'classic'
                },
                creative: {
                    primary: '#f5576c',
                    accent: '#f093fb',
                    font: 'modern'
                },
                developer: {
                    primary: '#00f2fe',
                    accent: '#4facfe',
                    font: 'modern'
                },
                startup: {
                    primary: '#fee140',
                    accent: '#fa709a',
                    font: 'modern'
                },
                elegant: {
                    primary: '#fed6e3',
                    accent: '#a8edea',
                    font: 'classic'
                }
            };

            if (templates[templateName]) {
                const template = templates[templateName];
                portfolioData.colors.primary = template.primary;
                portfolioData.colors.accent = template.accent;
                portfolioData.fontStyle = template.font;

                startBuilder();
                loadPortfolioData();
                updatePreview();
                showToast(`${templateName.charAt(0).toUpperCase() + templateName.slice(1)} template selected!`);
            }
        }

        /* ==================== Toast Notifications ==================== */

        function showToast(message) {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.classList.add('show');

            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }

        /* ==================== Color Suggestions ==================== */

        const colorSchemes = [
            { primary: '#667eea', accent: '#764ba2', name: 'Purple Dream' },
            { primary: '#f093fb', accent: '#f5576c', name: 'Pink Vibes' },
            { primary: '#4facfe', accent: '#00f2fe', name: 'Blue Ocean' },
            { primary: '#43e97b', accent: '#38f9d7', name: 'Green Fresh' },
            { primary: '#fa709a', accent: '#fee140', name: 'Warm Sunset' },
            { primary: '#30cfd0', accent: '#330867', name: 'Cool Night' }
        ];

        function applyColorScheme(schemeIndex) {
            const scheme = colorSchemes[schemeIndex];
            portfolioData.colors.primary = scheme.primary;
            portfolioData.colors.accent = scheme.accent;
            
            document.getElementById('primaryColor').value = scheme.primary;
            document.getElementById('accentColor').value = scheme.accent;
            
            document.getElementById('primaryColorText').textContent = scheme.primary;
            document.getElementById('accentColorText').textContent = scheme.accent;
            
            updatePreview();
            showToast(`${scheme.name} color scheme applied!`);
        }

        /* ==================== Event Listeners ==================== */

        document.addEventListener('DOMContentLoaded', function() {
            // Close modal when clicking outside
            const modal = document.getElementById('builderModal');
            window.addEventListener('click', function(event) {
                if (event.target === modal) {
                    closeBuilder();
                }
            });

            // Handle hamburger menu
            const hamburger = document.getElementById('hamburger');
            const navLinks = document.querySelector('.nav-links');
            
            if (hamburger) {
                hamburger.addEventListener('click', function() {
                    navLinks.classList.toggle('active');
                });
            }

            // Load from localStorage
            loadFromLocalStorage();
        });

        /* ==================== Local Storage ==================== */

        function autoSavePortfolio() {
            savePortfolioData();
            localStorage.setItem('portfolioData', JSON.stringify(portfolioData));
        }

        function loadFromLocalStorage() {
            const saved = localStorage.getItem('portfolioData');
            const savedProjects = localStorage.getItem('portfolioProjects');
            
            if (saved) {
                try {
                    portfolioData = JSON.parse(saved);
                } catch (e) {
                    console.error('Error loading portfolio data');
                }
            }
            
            if (savedProjects) {
                try {
                    projects = JSON.parse(savedProjects);
                    portfolioData.projects = projects;
                } catch (e) {
                    console.error('Error loading projects');
                }
            }
        }

        // Set up auto-save on input
        document.addEventListener('input', function(e) {
            if (e.target.matches('#fullName, #title, #bio, #email, #phone, #location, #skills, #fontStyle, #githubUrl, #linkedinUrl, #twitterUrl, #websiteUrl')) {
                autoSavePortfolio();
            }
        });

        // Initialize
        projects = portfolioData.projects || [];
    </script>
</body>
</html>
