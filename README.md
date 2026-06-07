<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="PortfolioBuilder Pro - Create your professional portfolio with real email authentication">
    <title>PortfolioBuilder Pro - Professional Portfolio Creator</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.0/crypto-js.min.js"></script>
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

        .nav-actions {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .user-profile {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 8px 15px;
            background: #f0f0f0;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .user-profile:hover {
            background: #e0e0e0;
        }

        .user-avatar {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
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
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            margin-top: 1rem;
        }

        /* ==================== Features Section ==================== */

        .features {
            padding: 80px 0;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #333;
        }

        .features-grid {
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

        /* ==================== Stats Section ==================== */

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            padding: 2rem 0;
        }

        .stat-box {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        .stat-box h4 {
            color: #667eea;
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        /* ==================== Pricing Section ==================== */

        .pricing {
            padding: 80px 0;
            background: #f9f9f9;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
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

        .price-amount {
            font-size: 3rem;
            font-weight: 700;
            color: #667eea;
            margin: 1rem 0;
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

        .pricing-card .btn {
            width: 100%;
            margin-top: 1rem;
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

        .footer-section a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: #667eea;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #555;
            color: #999;
        }

        /* ==================== Modal Styles ==================== */

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
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
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .close-btn {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: white;
        }

        .modal-body {
            flex: 1;
            overflow: hidden;
        }

        .builder-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            height: 100%;
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
            border-bottom: 3px solid transparent;
            margin-bottom: -2px;
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
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 5px rgba(102, 126, 234, 0.2);
        }

        /* ==================== Auth Modal ==================== */

        .auth-modal {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            max-width: 500px;
            width: 95%;
            z-index: 2000;
        }

        .auth-modal h3 {
            margin-bottom: 1.5rem;
            color: #333;
        }

        .auth-tabs {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .auth-tab-btn {
            flex: 1;
            padding: 10px;
            background: #f0f0f0;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .auth-tab-btn.active {
            background: #667eea;
            color: white;
        }

        .auth-form {
            display: none;
        }

        .auth-form.active {
            display: block;
        }

        /* ==================== Toast ==================== */

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

        .toast.success {
            background: #4CAF50;
        }

        .toast.error {
            background: #ff6b6b;
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

        /* ==================== Modal Overlay ==================== */

        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }

        .modal-overlay.active {
            display: block;
        }

        /* ==================== Responsive ==================== */

        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                display: none;
            }

            .nav-actions {
                display: none;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .builder-container {
                grid-template-columns: 1fr;
            }

            .editor-panel {
                border-right: none;
                border-bottom: 1px solid #eee;
            }

            .pricing-card.featured {
                transform: scale(1);
            }
        }

        .color-input-group {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .color-input-group input[type="color"] {
            width: 50px;
            height: 40px;
            cursor: pointer;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .color-input-group span {
            font-weight: 600;
            color: #667eea;
        }

        .project-item {
            background: white;
            padding: 12px;
            border-radius: 5px;
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid #ddd;
        }

        .delete-btn {
            background: #ff6b6b;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 3px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .delete-btn:hover {
            background: #ff5252;
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
                    <span>PortfolioBuilder Pro</span>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#features">Features</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                    <li><a href="#faq">FAQ</a></li>
                </ul>
                <div class="nav-actions" id="navActions">
                    <button class="btn btn-secondary btn-small" onclick="openAuthModal('login')">Login</button>
                    <button class="btn btn-primary btn-small" onclick="openAuthModal('signup')">Sign Up</button>
                </div>
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
            <h1>Create Your Professional Portfolio</h1>
            <p>Build a stunning portfolio website in minutes. No coding required!</p>
            <span class="hero-badge">100% Free • No Credit Card Required</span>
            <br>
            <button class="btn btn-primary" onclick="redirectToBuilder()" style="margin-top: 2rem;">
                <i class="fas fa-rocket"></i> Start Building Now
            </button>
        </div>
    </section>

    <!-- Stats Section -->
    <section style="background: #f9f9f9; padding: 80px 0;">
        <div class="container">
            <div class="stats">
                <div class="stat-box">
                    <h4>10K+</h4>
                    <p>Portfolios Created</p>
                </div>
                <div class="stat-box">
                    <h4>50+</h4>
                    <p>Templates Available</p>
                </div>
                <div class="stat-box">
                    <h4>100%</h4>
                    <p>Mobile Responsive</p>
                </div>
                <div class="stat-box">
                    <h4>24/7</h4>
                    <p>Customer Support</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <h2 class="section-title">Why Choose PortfolioBuilder Pro?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-paint-brush"></i>
                    <h3>50+ Templates</h3>
                    <p>Professional design templates for any profession</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-code"></i>
                    <h3>No Coding</h3>
                    <p>Drag and drop editor anyone can use</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>Mobile Ready</h3>
                    <p>Perfect on all devices automatically</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-download"></i>
                    <h3>Export as HTML</h3>
                    <p>Download your portfolio as standalone HTML file</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-lock"></i>
                    <h3>Secure</h3>
                    <p>Enterprise-grade security for your data</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-share-alt"></i>
                    <h3>Share Anywhere</h3>
                    <p>Share your portfolio with one click</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="pricing">
        <div class="container">
            <h2 class="section-title">Free Forever</h2>
            <div class="pricing-grid">
                <div class="pricing-card featured">
                    <div class="badge">Free Plan</div>
                    <h3>All Features Included</h3>
                    <div class="price-amount">Free</div>
                    <p style="color: #666; margin-bottom: 1rem;">No credit card required</p>
                    <ul class="features-list">
                        <li><i class="fas fa-check"></i> Unlimited Portfolios</li>
                        <li><i class="fas fa-check"></i> 50+ Templates</li>
                        <li><i class="fas fa-check"></i> Custom Colors & Fonts</li>
                        <li><i class="fas fa-check"></i> Project Management</li>
                        <li><i class="fas fa-check"></i> Social Media Links</li>
                        <li><i class="fas fa-check"></i> Export as HTML</li>
                        <li><i class="fas fa-check"></i> Share Portfolio</li>
                        <li><i class="fas fa-check"></i> Live Preview</li>
                    </ul>
                    <button class="btn btn-primary" onclick="redirectToBuilder()">Get Started Free</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>Product</h4>
                    <ul>
                        <li><a href="#">Features</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Company</h4>
                    <ul>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Legal</h4>
                    <ul>
                        <li><a href="#">Privacy</a></li>
                        <li><a href="#">Terms</a></li>
                        <li><a href="#">Support</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Connect</h4>
                    <ul>
                        <li><a href="#">Twitter</a></li>
                        <li><a href="#">GitHub</a></li>
                        <li><a href="#">LinkedIn</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 PortfolioBuilder Pro. All rights reserved.</p>
                <p>Made with ❤️ for creators everywhere</p>
            </div>
        </div>
    </footer>

    <!-- Auth Modal -->
    <div id="authModal" class="modal">
        <div class="modal-overlay" onclick="closeAuthModal()"></div>
        <div class="auth-modal">
            <button class="close-btn" onclick="closeAuthModal()" style="float: right; background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            <h3>Welcome to PortfolioBuilder Pro</h3>
            
            <div class="auth-tabs">
                <button class="auth-tab-btn active" onclick="switchAuthTab('login')">Login</button>
                <button class="auth-tab-btn" onclick="switchAuthTab('signup')">Sign Up</button>
            </div>

            <!-- Login Form -->
            <div id="login-form" class="auth-form active">
                <div class="form-group">
                    <label>Email Address</label>
                    <input type="email" id="loginEmail" placeholder="your@email.com">
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" id="loginPassword" placeholder="Enter your password">
                </div>
                <button class="btn btn-primary" style="width: 100%;" onclick="handleLogin()">
                    <i class="fas fa-sign-in-alt"></i> Login
                </button>
                <p style="text-align: center; margin-top: 1rem; font-size: 0.9rem;">
                    <a href="#" style="color: #667eea; text-decoration: none;">Forgot password?</a>
                </p>
            </div>

            <!-- Sign Up Form -->
            <div id="signup-form" class="auth-form">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" id="signupName" placeholder="John Doe">
                </div>
                <div class="form-group">
                    <label>Email Address</label>
                    <input type="email" id="signupEmail" placeholder="your@email.com">
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" id="signupPassword" placeholder="At least 6 characters">
                </div>
                <div class="form-group">
                    <label>Confirm Password</label>
                    <input type="password" id="confirmPassword" placeholder="Confirm your password">
                </div>
                <button class="btn btn-primary" style="width: 100%;" onclick="handleSignup()">
                    <i class="fas fa-user-plus"></i> Create Account
                </button>
            </div>
        </div>
    </div>

    <!-- Builder Modal -->
    <div id="builderModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2><i class="fas fa-magic"></i> Portfolio Builder</h2>
                <button class="close-btn" onclick="closeBuilderModal()">&times;</button>
            </div>
            <div class="modal-body">
                <div class="builder-container">
                    <!-- Editor Panel -->
                    <div class="editor-panel">
                        <div class="tabs">
                            <button class="tab-btn active" onclick="switchTab('basic')">Basic</button>
                            <button class="tab-btn" onclick="switchTab('skills')">Skills</button>
                            <button class="tab-btn" onclick="switchTab('projects')">Projects</button>
                            <button class="tab-btn" onclick="switchTab('social')">Social</button>
                            <button class="tab-btn" onclick="switchTab('design')">Design</button>
                        </div>

                        <!-- Basic Tab -->
                        <div id="basic-tab" class="tab-content active">
                            <div class="form-group">
                                <label>Full Name</label>
                                <input type="text" id="fullName" value="John Doe" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Professional Title</label>
                                <input type="text" id="title" value="Full Stack Developer" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Bio</label>
                                <textarea id="bio" rows="3" oninput="updatePreview()">Passionate developer creating amazing web experiences with modern technologies.</textarea>
                            </div>
                            <div class="form-group">
                                <label>Email</label>
                                <input type="email" id="email" value="john@example.com" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Phone</label>
                                <input type="tel" id="phone" value="+91 9876543210" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Location</label>
                                <input type="text" id="location" value="India" oninput="updatePreview()">
                            </div>
                        </div>

                        <!-- Skills Tab -->
                        <div id="skills-tab" class="tab-content">
                            <div class="form-group">
                                <label>Skills (comma separated)</label>
                                <textarea id="skills" rows="6" oninput="updatePreview()">HTML5, CSS3, JavaScript, React, Node.js, MongoDB, Express.js, REST APIs, Git, Firebase, UI/UX Design</textarea>
                            </div>
                        </div>

                        <!-- Projects Tab -->
                        <div id="projects-tab" class="tab-content">
                            <div id="projectsList"></div>
                            <button class="btn btn-secondary btn-small" onclick="addProject()" style="margin-top: 1rem; width: 100%;">
                                <i class="fas fa-plus"></i> Add Project
                            </button>
                        </div>

                        <!-- Social Tab -->
                        <div id="social-tab" class="tab-content">
                            <div class="form-group">
                                <label>GitHub URL</label>
                                <input type="url" id="github" placeholder="https://github.com/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>LinkedIn URL</label>
                                <input type="url" id="linkedin" placeholder="https://linkedin.com/in/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Twitter URL</label>
                                <input type="url" id="twitter" placeholder="https://twitter.com/username" oninput="updatePreview()">
                            </div>
                            <div class="form-group">
                                <label>Portfolio Website</label>
                                <input type="url" id="website" placeholder="https://yourwebsite.com" oninput="updatePreview()">
                            </div>
                        </div>

                        <!-- Design Tab -->
                        <div id="design-tab" class="tab-content">
                            <div class="form-group">
                                <label>Primary Color</label>
                                <div class="color-input-group">
                                    <input type="color" id="primaryColor" value="#667eea" oninput="updateColors()">
                                    <span id="primaryColorText">#667eea</span>
                                </div>
                            </div>
                            <div class="form-group">
                                <label>Secondary Color</label>
                                <div class="color-input-group">
                                    <input type="color" id="secondaryColor" value="#764ba2" oninput="updateColors()">
                                    <span id="secondaryColorText">#764ba2</span>
                                </div>
                            </div>
                            <div class="form-group">
                                <label>Font Style</label>
                                <select id="fontStyle" oninput="updatePreview()">
                                    <option value="Poppins">Modern (Poppins)</option>
                                    <option value="Georgia">Classic (Georgia)</option>
                                    <option value="monospace">Minimal (Monospace)</option>
                                    <option value="Arial">Professional (Arial)</option>
                                </select>
                            </div>
                        </div>
                    </div>

                    <!-- Preview Panel -->
                    <div class="preview-panel">
                        <div class="preview-header">
                            <h3>Live Preview</h3>
                            <div class="preview-controls">
                                <button onclick="exportPortfolio()" title="Export as HTML"><i class="fas fa-download"></i></button>
                                <button onclick="sharePortfolio()" title="Share"><i class="fas fa-share-alt"></i></button>
                                <button onclick="copyLink()" title="Copy Link"><i class="fas fa-copy"></i></button>
                            </div>
                        </div>
                        <div id="previewFrame" class="preview-frame"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast -->
    <div id="toast" class="toast"></div>

    <script>
        // ==================== Database & Auth ====================
        
        const USERS_STORAGE_KEY = 'portfolio_users';
        const CURRENT_USER_KEY = 'portfolio_current_user';

        let currentUser = null;
        let projects = [
            { name: 'E-Commerce Platform', desc: 'Full-stack e-commerce solution with React and Node.js' },
            { name: 'Task Manager App', desc: 'React-based task management application with real-time updates' }
        ];

        // ==================== Auth Functions ====================

        function openAuthModal(tab = 'login') {
            document.getElementById('authModal').classList.add('active');
            switchAuthTab(tab);
        }

        function closeAuthModal() {
            document.getElementById('authModal').classList.remove('active');
        }

        function switchAuthTab(tab) {
            document.querySelectorAll('.auth-tab-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelectorAll('.auth-form').forEach(form => form.classList.remove('active'));
            
            event.target.classList.add('active');
            document.getElementById(tab + '-form').classList.add('active');
        }

        function validateEmail(email) {
            const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return re.test(email);
        }

        function handleLogin() {
            const email = document.getElementById('loginEmail').value.trim();
            const password = document.getElementById('loginPassword').value;

            if (!email || !password) {
                showToast('Please fill all fields', 'error');
                return;
            }

            if (!validateEmail(email)) {
                showToast('Please enter a valid email', 'error');
                return;
            }

            const users = JSON.parse(localStorage.getItem(USERS_STORAGE_KEY) || '[]');
            const user = users.find(u => u.email === email);

            if (!user) {
                showToast('Email not found. Please sign up first', 'error');
                return;
            }

            const hashedPassword = CryptoJS.SHA256(password).toString();
            if (user.password !== hashedPassword) {
                showToast('Incorrect password', 'error');
                return;
            }

            currentUser = { ...user };
            delete currentUser.password;
            localStorage.setItem(CURRENT_USER_KEY, JSON.stringify(currentUser));
            
            closeAuthModal();
            updateNavbar();
            showToast(`Welcome back, ${user.name}!`, 'success');
            redirectToBuilder();
        }

        function handleSignup() {
            const name = document.getElementById('signupName').value.trim();
            const email = document.getElementById('signupEmail').value.trim();
            const password = document.getElementById('signupPassword').value;
            const confirmPassword = document.getElementById('confirmPassword').value;

            if (!name || !email || !password || !confirmPassword) {
                showToast('Please fill all fields', 'error');
                return;
            }

            if (!validateEmail(email)) {
                showToast('Please enter a valid email', 'error');
                return;
            }

            if (password.length < 6) {
                showToast('Password must be at least 6 characters', 'error');
                return;
            }

            if (password !== confirmPassword) {
                showToast('Passwords do not match', 'error');
                return;
            }

            const users = JSON.parse(localStorage.getItem(USERS_STORAGE_KEY) || '[]');
            
            if (users.find(u => u.email === email)) {
                showToast('Email already registered', 'error');
                return;
            }

            const hashedPassword = CryptoJS.SHA256(password).toString();
            const newUser = {
                id: Date.now(),
                name,
                email,
                password: hashedPassword,
                createdAt: new Date().toISOString()
            };

            users.push(newUser);
            localStorage.setItem(USERS_STORAGE_KEY, JSON.stringify(users));

            currentUser = { ...newUser };
            delete currentUser.password;
            localStorage.setItem(CURRENT_USER_KEY, JSON.stringify(currentUser));

            closeAuthModal();
            updateNavbar();
            showToast(`Welcome ${name}! Account created successfully!`, 'success');
            redirectToBuilder();
        }

        // ==================== UI Functions ====================

        function updateNavbar() {
            const navActions = document.getElementById('navActions');
            
            if (currentUser) {
                navActions.innerHTML = `
                    <div class="user-profile" onclick="showUserMenu()">
                        <div class="user-avatar">${currentUser.name.charAt(0).toUpperCase()}</div>
                        <span>${currentUser.name}</span>
                    </div>
                `;
            } else {
                navActions.innerHTML = `
                    <button class="btn btn-secondary btn-small" onclick="openAuthModal('login')">Login</button>
                    <button class="btn btn-primary btn-small" onclick="openAuthModal('signup')">Sign Up</button>
                `;
            }
        }

        function showUserMenu() {
            const menu = confirm(`${currentUser.name}\n${currentUser.email}\n\nClick OK to logout`);
            if (menu) {
                currentUser = null;
                localStorage.removeItem(CURRENT_USER_KEY);
                updateNavbar();
                closeBuilderModal();
                showToast('Logged out successfully', 'success');
            }
        }

        function redirectToBuilder() {
            if (!currentUser) {
                openAuthModal('signup');
                return;
            }
            
            document.getElementById('builderModal').classList.add('active');
            loadProjects();
            updatePreview();
        }

        function closeBuilderModal() {
            document.getElementById('builderModal').classList.remove('active');
        }

        function switchTab(tab) {
            document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
            document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
            
            document.getElementById(tab + '-tab').classList.add('active');
            event.target.classList.add('active');
        }

        // ==================== Portfolio Functions ====================

        function addProject() {
            const name = prompt('Project name:');
            if (name) {
                const desc = prompt('Project description:');
                projects.push({ name, desc: desc || '' });
                loadProjects();
                updatePreview();
                showToast('Project added successfully!', 'success');
            }
        }

        function loadProjects() {
            const list = document.getElementById('projectsList');
            list.innerHTML = '';
            projects.forEach((p, i) => {
                const el = document.createElement('div');
                el.className = 'project-item';
                el.innerHTML = `
                    <div>
                        <strong>${p.name}</strong>
                        <p style="margin: 5px 0 0 0; font-size: 0.9rem; color: #666;">${p.desc}</p>
                    </div>
                    <button class="delete-btn" onclick="deleteProject(${i})">
                        <i class="fas fa-trash"></i>
                    </button>
                `;
                list.appendChild(el);
            });
        }

        function deleteProject(i) {
            projects.splice(i, 1);
            loadProjects();
            updatePreview();
            showToast('Project deleted!', 'success');
        }

        function updateColors() {
            const primary = document.getElementById('primaryColor').value;
            const secondary = document.getElementById('secondaryColor').value;
            document.getElementById('primaryColorText').textContent = primary;
            document.getElementById('secondaryColorText').textContent = secondary;
            updatePreview();
        }

        function updatePreview() {
            const name = document.getElementById('fullName').value;
            const title = document.getElementById('title').value;
            const bio = document.getElementById('bio').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const location = document.getElementById('location').value;
            const skills = document.getElementById('skills').value.split(',').map(s => s.trim()).filter(s => s);
            const primary = document.getElementById('primaryColor').value;
            const secondary = document.getElementById('secondaryColor').value;
            const fontFamily = document.getElementById('fontStyle').value;
            const github = document.getElementById('github').value;
            const linkedin = document.getElementById('linkedin').value;
            const twitter = document.getElementById('twitter').value;
            const website = document.getElementById('website').value;

            const projectsHTML = projects.map(p => `
                <div style="background: #f9f9f9; padding: 15px; border-radius: 5px; border-left: 4px solid ${primary}; margin-bottom: 10px;">
                    <h4 style="color: ${primary}; margin-bottom: 5px;">${p.name}</h4>
                    <p>${p.desc}</p>
                </div>
            `).join('');

            const socialHTML = `
                <div style="display: flex; justify-content: center; gap: 15px; margin-top: 20px;">
                    ${github ? `<a href="${github}" target="_blank" style="color: ${primary}; font-size: 1.2rem;"><i class="fab fa-github"></i></a>` : ''}
                    ${linkedin ? `<a href="${linkedin}" target="_blank" style="color: ${primary}; font-size: 1.2rem;"><i class="fab fa-linkedin"></i></a>` : ''}
                    ${twitter ? `<a href="${twitter}" target="_blank" style="color: ${primary}; font-size: 1.2rem;"><i class="fab fa-twitter"></i></a>` : ''}
                    ${website ? `<a href="${website}" target="_blank" style="color: ${primary}; font-size: 1.2rem;"><i class="fas fa-globe"></i></a>` : ''}
                </div>
            `;

            const html = `
                <!DOCTYPE html>
                <html>
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>${name} - Portfolio</title>
                    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
                    <style>
                        * { margin: 0; padding: 0; box-sizing: border-box; }
                        body { font-family: ${fontFamily}; line-height: 1.6; background: #f9f9f9; color: #333; }
                        header { background: linear-gradient(135deg, ${primary} 0%, ${secondary} 100%); color: white; padding: 50px 20px; text-align: center; }
                        header h1 { font-size: 2.5rem; margin-bottom: 10px; }
                        header p { font-size: 1.1rem; opacity: 0.9; }
                        section { max-width: 900px; margin: 20px auto; background: white; padding: 30px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
                        section h2 { color: ${primary}; margin-bottom: 15px; border-bottom: 2px solid ${primary}; padding-bottom: 10px; }
                        .skills { display: flex; flex-wrap: wrap; gap: 10px; }
                        .skill { background: ${primary}; color: white; padding: 8px 15px; border-radius: 20px; font-size: 0.9rem; }
                        footer { background: #333; color: white; text-align: center; padding: 20px; }
                        a { color: ${primary}; text-decoration: none; }
                        a:hover { text-decoration: underline; }
                    </style>
                </head>
                <body>
                    <header>
                        <h1>${name}</h1>
                        <p>${title}</p>
                        <p style="font-size: 0.95rem; margin-top: 10px;">${bio}</p>
                        ${github || linkedin || twitter || website ? socialHTML : ''}
                    </header>
                    <section>
                        <h2><i class="fas fa-envelope"></i> Contact</h2>
                        <p><strong>Email:</strong> <a href="mailto:${email}">${email}</a></p>
                        <p><strong>Phone:</strong> <a href="tel:${phone}">${phone}</a></p>
                        <p><strong>Location:</strong> ${location}</p>
                    </section>
                    <section>
                        <h2><i class="fas fa-star"></i> Skills</h2>
                        <div class="skills">
                            ${skills.map(s => `<span class="skill">${s}</span>`).join('')}
                        </div>
                    </section>
                    ${projects.length > 0 ? `
                    <section>
                        <h2><i class="fas fa-briefcase"></i> Projects</h2>
                        ${projectsHTML}
                    </section>
                    ` : ''}
                    <footer>
                        <p>&copy; 2025 ${name}. Built with PortfolioBuilder Pro</p>
                    </footer>
                </body>
                </html>
            `;

            document.getElementById('previewFrame').innerHTML = html;
        }

        function exportPortfolio() {
            const name = document.getElementById('fullName').value;
            const iframe = document.getElementById('previewFrame');
            const html = iframe.innerHTML;
            const blob = new Blob([html], { type: 'text/html' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `${name.replace(/\s+/g, '-').toLowerCase()}-portfolio.html`;
            a.click();
            URL.revokeObjectURL(url);
            showToast('Portfolio exported successfully!', 'success');
        }

        function sharePortfolio() {
            if (navigator.share) {
                navigator.share({
                    title: `${document.getElementById('fullName').value}'s Portfolio`,
                    text: 'Check out my professional portfolio built with PortfolioBuilder Pro',
                    url: window.location.href
                });
            } else {
                showToast('Share feature not supported in your browser', 'error');
            }
        }

        function copyLink() {
            navigator.clipboard.writeText(window.location.href).then(() => {
                showToast('Link copied to clipboard!', 'success');
            }).catch(() => {
                showToast('Failed to copy link', 'error');
            });
        }

        // ==================== Toast ==================== 

        function showToast(message, type = 'success') {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.className = `toast ${type}`;
            toast.classList.add('show');
            setTimeout(() => toast.classList.remove('show'), 3000);
        }

        // ==================== Init ==================== 

        document.addEventListener('DOMContentLoaded', function() {
            const saved = localStorage.getItem(CURRENT_USER_KEY);
            if (saved) {
                currentUser = JSON.parse(saved);
            }
            updateNavbar();
        });
    </script>
</body>
</html>
