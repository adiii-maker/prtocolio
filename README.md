# prtocolio
protcolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Welcome to my professional portfolio showcasing my web development skills and projects">
    <meta name="keywords" content="web developer, portfolio, HTML, CSS, JavaScript, React, Node.js">
    <title>My Portfolio - Web Developer</title>
    <link rel="stylesheet" href="style.css">
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Preloader -->
    <div class="preloader" id="preloader">
        <div class="loader"></div>
    </div>

    <!-- Navigation Bar -->
    <nav class="navbar" id="navbar">
        <div class="container">
            <div class="nav-wrapper">
                <div class="logo">
                    <a href="#home">
                        <i class="fas fa-code"></i>
                        <span>My Portfolio</span>
                    </a>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home" class="nav-link">Home</a></li>
                    <li><a href="#about" class="nav-link">About</a></li>
                    <li><a href="#skills" class="nav-link">Skills</a></li>
                    <li><a href="#experience" class="nav-link">Experience</a></li>
                    <li><a href="#projects" class="nav-link">Projects</a></li>
                    <li><a href="#testimonials" class="nav-link">Testimonials</a></li>
                    <li><a href="#contact" class="nav-link">Contact</a></li>
                </ul>
                <div class="hamburger" id="hamburger">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
                <div class="theme-toggle" id="themeToggle">
                    <i class="fas fa-moon"></i>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text" data-aos="fade-up">
                    <h1 class="hero-title">
                        Hi, I'm <span class="highlight">John Doe</span>
                    </h1>
                    <p class="hero-subtitle">Full Stack Web Developer & Designer</p>
                    <p class="hero-description">
                        Crafting beautiful and functional digital experiences. 
                        I transform ideas into interactive web solutions.
                    </p>
                    <div class="hero-stats">
                        <div class="stat">
                            <h3>50+</h3>
                            <p>Projects Completed</p>
                        </div>
                        <div class="stat">
                            <h3>30+</h3>
                            <p>Happy Clients</p>
                        </div>
                        <div class="stat">
                            <h3>3+</h3>
                            <p>Years Experience</p>
                        </div>
                    </div>
                    <div class="hero-buttons">
                        <a href="#projects" class="btn btn-primary">
                            <i class="fas fa-arrow-right"></i> View My Work
                        </a>
                        <a href="#contact" class="btn btn-secondary">
                            <i class="fas fa-envelope"></i> Get In Touch
                        </a>
                    </div>
                    <div class="hero-social">
                        <a href="https://github.com" target="_blank" title="GitHub">
                            <i class="fab fa-github"></i>
                        </a>
                        <a href="https://linkedin.com" target="_blank" title="LinkedIn">
                            <i class="fab fa-linkedin"></i>
                        </a>
                        <a href="https://twitter.com" target="_blank" title="Twitter">
                            <i class="fab fa-twitter"></i>
                        </a>
                    </div>
                </div>
                <div class="hero-image" data-aos="fade-left">
                    <div class="floating-card card-1">
                        <i class="fab fa-html5"></i>
                    </div>
                    <div class="floating-card card-2">
                        <i class="fab fa-css3-alt"></i>
                    </div>
                    <div class="floating-card card-3">
                        <i class="fab fa-js-square"></i>
                    </div>
                    <div class="profile-container">
                        <div class="profile-image">
                            <i class="fas fa-user-circle"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="scroll-indicator">
            <span>Scroll to explore</span>
            <div class="mouse">
                <div class="wheel"></div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">About Me</h2>
                <div class="title-underline"></div>
            </div>

            <div class="about-content">
                <div class="about-text" data-aos="fade-right">
                    <p class="intro-text">
                        I'm a passionate web developer from New York with a strong foundation in 
                        modern web technologies. I love creating digital solutions that solve real-world problems.
                    </p>
                    <p>
                        With 3+ years of professional experience, I've successfully delivered 50+ projects 
                        for startups and established companies. My approach is always user-centric, 
                        focusing on creating intuitive and engaging experiences.
                    </p>
                    <p>
                        I specialize in full-stack development with a particular interest in frontend technologies. 
                        When I'm not coding, you'll find me contributing to open-source projects, 
                        writing technical blogs, or exploring new technologies.
                    </p>

                    <div class="about-info">
                        <div class="info-row">
                            <span class="info-label">📍 Location:</span>
                            <span class="info-value">New York, USA</span>
                        </div>
                        <div class="info-row">
                            <span class="info-label">✉️ Email:</span>
                            <span class="info-value">john@example.com</span>
                        </div>
                        <div class="info-row">
                            <span class="info-label">📱 Phone:</span>
                            <span class="info-value">+1 (555) 123-4567</span>
                        </div>
                        <div class="info-row">
                            <span class="info-label">💼 Profession:</span>
                            <span class="info-value">Full Stack Developer</span>
                        </div>
                    </div>

                    <div class="about-buttons">
                        <a href="#" class="btn btn-primary" download>
                            <i class="fas fa-download"></i> Download CV
                        </a>
                        <a href="#contact" class="btn btn-secondary">
                            <i class="fas fa-comment-dots"></i> Let's Talk
                        </a>
                    </div>
                </div>

                <div class="about-image" data-aos="fade-left">
                    <div class="image-wrapper">
                        <div class="image-bg"></div>
                        <i class="fas fa-user-circle"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">My Skills</h2>
                <div class="title-underline"></div>
            </div>

            <div class="skills-container">
                <!-- Frontend Skills -->
                <div class="skills-category" data-aos="fade-up">
                    <div class="category-header">
                        <i class="fas fa-paint-brush"></i>
                        <h3>Frontend</h3>
                    </div>
                    <div class="skills-list">
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">HTML5</span>
                                <span class="skill-level">95%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 95%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">CSS3</span>
                                <span class="skill-level">92%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 92%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">JavaScript</span>
                                <span class="skill-level">90%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 90%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">React</span>
                                <span class="skill-level">88%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 88%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Responsive Design</span>
                                <span class="skill-level">93%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 93%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Backend Skills -->
                <div class="skills-category" data-aos="fade-up" data-aos-delay="100">
                    <div class="category-header">
                        <i class="fas fa-server"></i>
                        <h3>Backend</h3>
                    </div>
                    <div class="skills-list">
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Node.js</span>
                                <span class="skill-level">85%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Express.js</span>
                                <span class="skill-level">88%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 88%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">MongoDB</span>
                                <span class="skill-level">82%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 82%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Python</span>
                                <span class="skill-level">80%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 80%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">REST APIs</span>
                                <span class="skill-level">89%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 89%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Tools & Others -->
                <div class="skills-category" data-aos="fade-up" data-aos-delay="200">
                    <div class="category-header">
                        <i class="fas fa-tools"></i>
                        <h3>Tools & Others</h3>
                    </div>
                    <div class="skills-list">
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Git & GitHub</span>
                                <span class="skill-level">91%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 91%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Docker</span>
                                <span class="skill-level">75%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 75%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">UI/UX Design</span>
                                <span class="skill-level">84%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 84%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">SEO</span>
                                <span class="skill-level">80%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 80%"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Figma</span>
                                <span class="skill-level">83%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 83%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Tech Stack -->
            <div class="tech-stack" data-aos="fade-up">
                <h3>Tech Stack</h3>
                <div class="tech-grid">
                    <div class="tech-badge">
                        <i class="fab fa-html5"></i>
                        <span>HTML5</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-css3-alt"></i>
                        <span>CSS3</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-js-square"></i>
                        <span>JavaScript</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-react"></i>
                        <span>React</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-node-js"></i>
                        <span>Node.js</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-python"></i>
                        <span>Python</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-git-alt"></i>
                        <span>Git</span>
                    </div>
                    <div class="tech-badge">
                        <i class="fab fa-docker"></i>
                        <span>Docker</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Experience</h2>
                <div class="title-underline"></div>
            </div>

            <div class="experience-timeline">
                <div class="timeline-item" data-aos="fade-up">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="experience-header">
                            <h3>Senior Web Developer</h3>
                            <span class="timeline-date">2022 - Present</span>
                        </div>
                        <p class="company">Tech Solutions Inc.</p>
                        <p class="description">
                            Leading frontend development team. Architected and built multiple large-scale 
                            React applications serving 100k+ users. Improved page load time by 40% through optimization.
                        </p>
                        <div class="experience-tags">
                            <span>React</span>
                            <span>Node.js</span>
                            <span>MongoDB</span>
                            <span>Leadership</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item" data-aos="fade-up" data-aos-delay="100">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="experience-header">
                            <h3>Full Stack Developer</h3>
                            <span class="timeline-date">2021 - 2022</span>
                        </div>
                        <p class="company">Digital Innovations Ltd.</p>
                        <p class="description">
                            Developed end-to-end web solutions for diverse clients. Managed projects 
                            from design to deployment. Implemented responsive designs and RESTful APIs.
                        </p>
                        <div class="experience-tags">
                            <span>React</span>
                            <span>Express.js</span>
                            <span>PostgreSQL</span>
                            <span>AWS</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item" data-aos="fade-up" data-aos-delay="200">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="experience-header">
                            <h3>Junior Web Developer</h3>
                            <span class="timeline-date">2020 - 2021</span>
                        </div>
                        <p class="company">StartUp Hub</p>
                        <p class="description">
                            Built responsive websites and web applications. Collaborated with designers 
                            and backend developers. Gained strong foundation in full-stack development.
                        </p>
                        <div class="experience-tags">
                            <span>HTML/CSS</span>
                            <span>JavaScript</span>
                            <span>React</span>
                            <span>Firebase</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Featured Projects</h2>
                <div class="title-underline"></div>
            </div>

            <div class="project-filters">
                <button class="filter-btn active" data-filter="all">All</button>
                <button class="filter-btn" data-filter="react">React</button>
                <button class="filter-btn" data-filter="fullstack">Full Stack</button>
                <button class="filter-btn" data-filter="web">Web</button>
            </div>

            <div class="project-grid">
                <!-- Project 1 -->
                <div class="project-card" data-category="react" data-aos="fade-up">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>A fully functional e-commerce platform built with React and Node.js featuring product catalog, shopping cart, and secure payment gateway integration.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Stripe</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 2.5k Views</span>
                            <span><i class="fas fa-star"></i> 4.8/5</span>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card" data-category="fullstack" data-aos="fade-up" data-aos-delay="100">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-tasks"></i>
                    </div>
                    <div class="project-content">
                        <h3>Task Management App</h3>
                        <p>A responsive task management application with drag-and-drop functionality, real-time updates, filters, and local storage integration.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">Redux</span>
                            <span class="tech-tag">Tailwind</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 1.8k Views</span>
                            <span><i class="fas fa-star"></i> 4.6/5</span>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card" data-category="web" data-aos="fade-up" data-aos-delay="200">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-camera"></i>
                    </div>
                    <div class="project-content">
                        <h3>Photo Gallery</h3>
                        <p>An interactive photo gallery with advanced filtering, search functionality, and lightbox view. Built with vanilla JavaScript and modern CSS.</p>
                        <div class="project-tech">
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">CSS3</span>
                            <span class="tech-tag">HTML5</span>
                            <span class="tech-tag">Lightbox</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 3.2k Views</span>
                            <span><i class="fas fa-star"></i> 4.9/5</span>
                        </div>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="project-card" data-category="react" data-aos="fade-up" data-aos-delay="300">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-chart-bar"></i>
                    </div>
                    <div class="project-content">
                        <h3>Analytics Dashboard</h3>
                        <p>Real-time analytics dashboard with interactive charts, data visualization, and performance metrics. Displays live data using WebSocket connections.</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Chart.js</span>
                            <span class="tech-tag">WebSocket</span>
                            <span class="tech-tag">Node.js</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 2.1k Views</span>
                            <span><i class="fas fa-star"></i> 4.7/5</span>
                        </div>
                    </div>
                </div>

                <!-- Project 5 -->
                <div class="project-card" data-category="web" data-aos="fade-up" data-aos-delay="400">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-cloud"></i>
                    </div>
                    <div class="project-content">
                        <h3>Weather App</h3>
                        <p>A weather application that fetches real-time weather data using OpenWeather API with beautiful UI, animations, and geolocation support.</p>
                        <div class="project-tech">
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">API</span>
                            <span class="tech-tag">CSS Animations</span>
                            <span class="tech-tag">Geolocation</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 1.5k Views</span>
                            <span><i class="fas fa-star"></i> 4.5/5</span>
                        </div>
                    </div>
                </div>

                <!-- Project 6 -->
                <div class="project-card" data-category="fullstack" data-aos="fade-up" data-aos-delay="500">
                    <div class="project-image">
                        <div class="project-overlay">
                            <div class="project-links">
                                <a href="#" class="project-link" title="Live Demo">
                                    <i class="fas fa-external-link-alt"></i>
                                </a>
                                <a href="#" class="project-link" title="View Code">
                                    <i class="fas fa-code"></i>
                                </a>
                            </div>
                        </div>
                        <i class="fas fa-blog"></i>
                    </div>
                    <div class="project-content">
                        <h3>Personal Blog</h3>
                        <p>A fully functional blog platform with markdown support, categories, search functionality, comments, and content management system.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Next.js</span>
                            <span class="tech-tag">Markdown</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Authentication</span>
                        </div>
                        <div class="project-stats">
                            <span><i class="fas fa-eye"></i> 4.2k Views</span>
                            <span><i class="fas fa-star"></i> 4.8/5</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="view-more">
                <a href="#" class="btn btn-primary">
                    <i class="fas fa-folder-open"></i> View All Projects
                </a>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">What Clients Say</h2>
                <div class="title-underline"></div>
            </div>

            <div class="testimonials-grid">
                <!-- Testimonial 1 -->
                <div class="testimonial-card" data-aos="fade-up">
                    <div class="testimonial-header">
                        <div class="client-image">
                            <i class="fas fa-user-circle"></i>
                        </div>
                        <div class="client-info">
                            <h4>Sarah Anderson</h4>
                            <p>CEO, Tech Startup</p>
                        </div>
                    </div>
                    <div class="stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="testimonial-text">
                        "John delivered an exceptional e-commerce platform that exceeded our expectations. 
                        His attention to detail and technical expertise made the entire process smooth."
                    </p>
                </div>

                <!-- Testimonial 2 -->
                <div class="testimonial-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="testimonial-header">
                        <div class="client-image">
                            <i class="fas fa-user-circle"></i>
                        </div>
                        <div class="client-info">
                            <h4>Michael Chen</h4>
                            <p>Product Manager, Innovation Co.</p>
                        </div>
                    </div>
                    <div class="stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="testimonial-text">
                        "Working with John was amazing. He's not just a developer; he's a problem solver. 
                        Highly recommended for anyone looking for quality web development."
                    </p>
                </div>

                <!-- Testimonial 3 -->
                <div class="testimonial-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="testimonial-header">
                        <div class="client-image">
                            <i class="fas fa-user-circle"></i>
                        </div>
                        <div class="client-info">
                            <h4>Emily Rodriguez</h4>
                            <p>Founder, Creative Agency</p>
                        </div>
                    </div>
                    <div class="stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="testimonial-text">
                        "John's communication and technical skills are outstanding. He transformed our vision 
                        into a beautiful, functional website. Will definitely work together again."
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Get In Touch</h2>
                <div class="title-underline"></div>
                <p class="section-subtitle">
                    Let's discuss your project and create something amazing together!
                </p>
            </div>

            <div class="contact-content">
                <!-- Contact Info -->
                <div class="contact-info" data-aos="fade-right">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Email</h4>
                            <p>
                                <a href="mailto:john@example.com">john@example.com</a><br>
                                <a href="mailto:contact@example.com">contact@example.com</a>
                            </p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Phone</h4>
                            <p>
                                <a href="tel:+15551234567">+1 (555) 123-4567</a><br>
                                <a href="tel:+15559876543">+1 (555) 987-6543</a>
                            </p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Location</h4>
                            <p>
                                New York, NY<br>
                                United States
                            </p>
                        </div>
                    </div>

                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Hours</h4>
                            <p>
                                Mon - Fri: 9:00 AM - 6:00 PM<br>
                                Sat - Sun: Closed
                            </p>
                        </div>
                    </div>

                    <div class="contact-social">
                        <h4>Follow Me</h4>
                        <div class="social-links">
                            <a href="https://github.com" target="_blank" title="GitHub">
                                <i class="fab fa-github"></i>
                            </a>
                            <a href="https://linkedin.com" target="_blank" title="LinkedIn">
                                <i class="fab fa-linkedin"></i>
                            </a>
                            <a href="https://twitter.com" target="_blank" title="Twitter">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="https://facebook.com" target="_blank" title="Facebook">
                                <i class="fab fa-facebook"></i>
                            </a>
                            <a href="https://instagram.com" target="_blank" title="Instagram">
                                <i class="fab fa-instagram"></i>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Contact Form -->
                <form class="contact-form" id="contactForm" data-aos="fade-left">
                    <div class="form-group">
                        <label for="name">Full Name</label>
                        <input 
                            type="text" 
                            id="name" 
                            name="name" 
                            placeholder="Your name" 
                            required
                        >
                        <span class="error-message" id="nameError"></span>
                    </div>

                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input 
                            type="email" 
                            id="email" 
                            name="email" 
                            placeholder="your@email.com" 
                            required
                        >
                        <span class="error-message" id="emailError"></span>
                    </div>

                    <div class="form-group">
                        <label for="phone">Phone Number (Optional)</label>
                        <input 
                            type="tel" 
                            id="phone" 
                            name="phone" 
                            placeholder="Your phone number"
                        >
                    </div>

                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input 
                            type="text" 
                            id="subject" 
                            name="subject" 
                            placeholder="Project subject" 
                            required
                        >
                        <span class="error-message" id="subjectError"></span>
                    </div>

                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea 
                            id="message" 
                            name="message" 
                            placeholder="Tell me about your project..." 
                            rows="5" 
                            required
                        ></textarea>
                        <span class="error-message" id="messageError"></span>
                    </div>

                    <button type="submit" class="btn btn-primary btn-submit">
                        <i class="fas fa-paper-plane"></i> Send Message
                    </button>
                    <span class="success-message" id="successMessage"></span>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About</h3>
                    <p>
                        A passionate full-stack web developer dedicated to creating beautiful, 
                        functional, and user-friendly digital experiences.
                    </p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#">Web Development</a></li>
                        <li><a href="#">UI/UX Design</a></li>
                        <li><a href="#">Consulting</a></li>
                        <li><a href="#">Maintenance</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Follow</h3>
                    <div class="footer-social">
                        <a href="https://github.com" target="_blank">
                            <i class="fab fa-github"></i>
                        </a>
                        <a href="https://linkedin.com" target="_blank">
                            <i class="fab fa-linkedin"></i>
                        </a>
                        <a href="https://twitter.com" target="_blank">
                            <i class="fab fa-twitter"></i>
                        </a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 John Doe. All rights reserved.</p>
                <p>Designed & Developed with <i class="fas fa-heart"></i> by John Doe</p>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button class="back-to-top" id="backToTop">
        <i class="fas fa-arrow-up"></i>
    </button>

    <!-- Scripts -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
    <script src="script.js"></script>
</body>
</html>
