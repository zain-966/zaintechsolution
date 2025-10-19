<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zain Tech Solution - IT Services & Support</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #3b82f6;
            --accent: #f97316;
            --light: #f3f4f6;
            --dark: #1f2937;
            --text: #4b5563;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f9fafb;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        ul {
            list-style: none;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--accent);
        }
        
        .nav-menu {
            display: flex;
        }
        
        .nav-menu li {
            margin-left: 30px;
        }
        
        .nav-menu a {
            font-weight: 500;
            color: var(--dark);
            transition: color 0.3s;
        }
        
        .nav-menu a:hover {
            color: var(--primary);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(37, 99, 235, 0.9), rgba(37, 99, 235, 0.8)), url('https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            font-weight: 500;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #ea580c;
        }
        
        /* Services Section */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: var(--dark);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--text);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .services {
            padding: 80px 0;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
            text-align: center;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* About Section */
        .about {
            padding: 80px 0;
            background-color: var(--light);
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-text h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Contact Section */
        .contact {
            padding: 80px 0;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-details div {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .contact-details i {
            font-size: 1.2rem;
            color: var(--primary);
            margin-right: 15px;
        }
        
        .map {
            height: 300px;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 30px;
        }
        
        .map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Contact Form */
        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-form h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
        }
        
        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--secondary);
        }
        
        /* Message Confirmation */
        .message-confirmation {
            display: none;
            background-color: #d4edda;
            color: #155724;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            text-align: center;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a:hover {
            color: var(--accent);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .about-image {
                order: -1;
            }
        }
        
        @media (max-width: 768px) {
            .hamburger {
                display: block;
            }
            
            .nav-menu {
                position: fixed;
                top: 70px;
                left: -100%;
                flex-direction: column;
                background-color: white;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
                padding: 20px 0;
            }
            
            .nav-menu.active {
                left: 0;
            }
            
            .nav-menu li {
                margin: 15px 0;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <h1>Zain <span>Tech</span> Solution</h1>
            </div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact Us</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h2>Your Trusted IT Solutions Partner</h2>
            <p>Providing comprehensive technology solutions for businesses and individuals since 2020</p>
            <a href="#contact" class="btn">Get in Touch</a>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>We offer a wide range of IT services to meet all your technology needs</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-desktop"></i>
                    </div>
                    <h3>Desktop & Laptop Support</h3>
                    <p>Expert troubleshooting and repair services for all desktop and laptop computers.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>Annual Maintenance Contract (AMC)</h3>
                    <p>Comprehensive maintenance plans to keep your systems running smoothly all year round.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-server"></i>
                    </div>
                    <h3>Server Installation & Support</h3>
                    <p>Professional server setup, configuration, and ongoing support services.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <h3>Data Backup & Recovery</h3>
                    <p>Secure data backup solutions and expert recovery services for critical data loss situations.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-download"></i>
                    </div>
                    <h3>OS & Software Installation</h3>
                    <p>Professional installation of operating systems and all necessary software applications.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-microchip"></i>
                    </div>
                    <h3>Laptop & PC Upgrade</h3>
                    <p>Hardware upgrades to improve performance and extend the life of your devices.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3>CCTV Installation & Maintenance</h3>
                    <p>Complete CCTV system setup and maintenance for enhanced security.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-network-wired"></i>
                    </div>
                    <h3>Networking Setup & Maintenance</h3>
                    <p>Design, implementation, and maintenance of reliable network infrastructure.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Antivirus Software Installation</h3>
                    <p>Installation and configuration of all major antivirus and security software.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-users-cog"></i>
                    </div>
                    <h3>HR Software Solutions</h3>
                    <p>Implementation of comprehensive HR management software solutions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>About Zain Tech Solution</h2>
                    <p>Founded in 2020, Zain Tech Solution has been providing reliable and professional IT services to businesses and individuals across the region. Our team of certified technicians brings years of experience and expertise to every project.</p>
                    <p>We understand that technology is critical to your success, which is why we're committed to delivering solutions that are tailored to your specific needs and budget.</p>
                    <p>Our mission is to provide exceptional IT services that empower our clients to focus on their core business while we handle their technology needs.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1568992687947-868a62a9f521?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Zain Tech Solution Team">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch with us for all your IT needs</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h2>Get In Touch</h2>
                    <div class="contact-details">
                        <div>
                            <i class="fas fa-phone"></i>
                            <p>9665555970 / 8329720924</p>
                        </div>
                        <div>
                            <i class="fas fa-envelope"></i>
                            <p>zaintechsolutions01@gmail.com</p>
                        </div>
                        <div>
                            <i class="fas fa-map-marker-alt"></i>
                            <p>Nigdi Gaothan, Nigdi, Pimpri-Chinchwad, Maharashtra 411044</p>
                        </div>
                        <div>
                            <i class="fas fa-clock"></i>
                            <p>24/7</p>
                        </div>
                    </div>
                    
                    <div class="map">
                        <!-- Updated Google Maps Embed with your coordinates -->
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3780.685655726773!2d73.772247!3d18.664722!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMTjCsDM5JzUzLjAiTiA3M8KwNDYnMzAuMSJF!5e0!3m2!1sen!2sin!4v1650000000000!5m2!1sen!2sin" allowfullscreen="" loading="lazy"></iframe>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>Send Us a Message</h3>
                    <form id="messageForm">
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" name="phone">
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" name="message" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                    
                    <div class="message-confirmation" id="confirmationMessage">
                        <i class="fas fa-check-circle"></i>
                        <p>Thank you for your message! We'll get back to you soon.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Zain Tech Solution</h3>
                    <p>Your trusted partner for all IT solutions and services. Providing quality support since 2020.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#contact">Contact Us</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#services">Desktop & Laptop Support</a></li>
                        <li><a href="#services">Server Installation</a></li>
                        <li><a href="#services">Data Recovery</a></li>
                        <li><a href="#services">CCTV Installation</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Connect With Us</h3>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Zain Tech Solution. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');
        
        hamburger.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-menu a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Message Form Handling
        const messageForm = document.getElementById('messageForm');
        const confirmationMessage = document.getElementById('confirmationMessage');
        
        messageForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Here you would typically send the form data to a server
            // For this example, we'll just show a confirmation message
            
            // Reset the form
            messageForm.reset();
            
            // Show confirmation message
            confirmationMessage.style.display = 'block';
            
            // Hide confirmation message after 5 seconds
            setTimeout(() => {
                confirmationMessage.style.display = 'none';
            }, 5000);
        });
    </script>
</body>
</html>
