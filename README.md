<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Erkan Kolakan - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #fff;
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
        }
        
        .floating-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: linear-gradient(45deg, #00f5ff, #ff00ff);
            border-radius: 50%;
            animation: float 8s infinite ease-in-out;
            opacity: 0.6;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-20px) rotate(120deg); }
            66% { transform: translateY(10px) rotate(240deg); }
        }
        
        .hero-section {
            text-align: center;
            padding: 4rem 0;
            position: relative;
            z-index: 10;
        }
        
        .profile-container {
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }
        
        .profile-glow {
            position: absolute;
            top: -20px;
            left: -20px;
            right: -20px;
            bottom: -20px;
            background: conic-gradient(from 0deg, #ff006e, #8338ec, #3a86ff, #06ffa5, #ffbe0b, #fb5607, #ff006e);
            border-radius: 50%;
            animation: rotate 3s linear infinite;
            z-index: 1;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        .profile-image {
            position: relative;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            font-weight: bold;
            color: #fff;
            z-index: 2;
            margin: 20px;
        }
        
        .name-title {
            margin-bottom: 1rem;
        }
        
        .name {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #00f5ff 0%, #ff00ff 50%, #ffbe0b 100%);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 0.5rem;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from { filter: drop-shadow(0 0 10px rgba(0, 245, 255, 0.3)); }
            to { filter: drop-shadow(0 0 20px rgba(255, 0, 255, 0.5)); }
        }
        
        .subtitle {
            font-size: 1.3rem;
            color: #a0a9c0;
            line-height: 1.6;
            max-width: 600px;
            margin: 0 auto 3rem;
        }
        
        .brand-link {
            color: #00f5ff;
            text-decoration: none;
            font-weight: 600;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .brand-link:hover {
            color: #ff00ff;
            transform: translateY(-2px);
        }
        
        .brand-link::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #00f5ff, #ff00ff);
            transition: width 0.3s ease;
        }
        
        .brand-link:hover::after {
            width: 100%;
        }
        
        .contact-section {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2rem;
            margin: 3rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .contact-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.03), transparent);
            transform: rotate(45deg);
            animation: shimmer 3s linear infinite;
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        .contact-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 2rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .contact-header:hover {
            transform: scale(1.02);
        }
        
        .contact-icon {
            font-size: 1.5rem;
            margin-right: 0.5rem;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .contact-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #fff;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            text-decoration: none;
            color: #fff;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .contact-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }
        
        .contact-item:hover::before {
            left: 100%;
        }
        
        .contact-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 245, 255, 0.3);
            background: rgba(255, 255, 255, 0.12);
        }
        
        .contact-item.linkedin:hover {
            box-shadow: 0 10px 30px rgba(0, 119, 181, 0.4);
        }
        
        .contact-item.gmail:hover {
            box-shadow: 0 10px 30px rgba(234, 67, 53, 0.4);
        }
        
        .contact-item.instagram:hover {
            box-shadow: 0 10px 30px rgba(228, 64, 95, 0.4);
        }
        
        .contact-item img {
            height: 30px;
            margin-right: 0.5rem;
            filter: brightness(1.2);
        }
        
        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 3rem 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #00f5ff, #ff00ff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-label {
            font-size: 1rem;
            color: #a0a9c0;
            margin-top: 0.5rem;
        }
        
        .footer {
            text-align: center;
            padding: 3rem 0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 4rem;
        }
        
        .footer-content {
            color: #a0a9c0;
            font-size: 0.9rem;
        }
        
        .footer-link {
            color: #00f5ff;
            text-decoration: none;
            font-weight: 500;
        }
        
        .footer-link:hover {
            color: #ff00ff;
        }
        
        @media (max-width: 768px) {
            .name {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.1rem;
                padding: 0 1rem;
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-particles" id="particles"></div>
    
    <div class="container">
        <div class="hero-section">
            <div class="profile-container">
                <div class="profile-glow"></div>
                <div class="profile-image">E</div>
            </div>
            
            <div class="name-title">
                <h1 class="name">Hi, I'm Erkan</h1>
                <p class="subtitle">
                    Full Stack Freelancer & Digital Innovator<br>
                    Building exceptional experiences at <a href="https://www.flabex.com/en" target="_blank" class="brand-link">Flabex</a>
                </p>
            </div>
        </div>
        
        <div class="stats-section">
            <div class="stat-card">
                <div class="stat-number">5+</div>
                <div class="stat-label">Years Experience</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">100+</div>
                <div class="stat-label">Projects Completed</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">24/7</div>
                <div class="stat-label">Available</div>
            </div>
        </div>
        
        <div class="contact-section">
            <div class="contact-header" onclick="toggleContact()">
                <span class="contact-icon">📞</span>
                <h2 class="contact-title">Let's Connect</h2>
            </div>
            
            <div class="contact-grid" id="contactGrid">
                <a href="https://www.linkedin.com/in/erkan-kolakan-03138b1a3/" target="_blank" class="contact-item linkedin">
                    <img src="https://img.shields.io/badge/linkedin-%231DA1F2.svg?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
                    <span>LinkedIn</span>
                </a>
                
                <a href="mailto:erkankolakan@gmail.com" target="_blank" class="contact-item gmail">
                    <img src="https://img.shields.io/badge/gmail-EA4335.svg?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" />
                    <span>Email</span>
                </a>
                
                <a href="https://instagram.com/erkankolakans" target="_blank" class="contact-item instagram">
                    <img src="https://img.shields.io/badge/instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white" alt="Instagram" />
                    <span>Instagram</span>
                </a>
            </div>
        </div>
        
        <div class="footer">
            <div class="footer-content">
                Crafted with ❤️ by <a href="https://github.com/erkankolakan" target="_blank" class="footer-link">erkankolakan</a><br>
                Last Updated: December 2024
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const numParticles = 50;
            
            for (let i = 0; i < numParticles; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 8 + 's';
                particle.style.animationDuration = (Math.random() * 6 + 4) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        
        // Initialize particles
        createParticles();
        
        // Smooth scroll and animation on load
        window.addEventListener('load', () => {
            document.body.style.opacity = '0';
            document.body.style.transform = 'translateY(30px)';
            document.body.style.transition = 'all 1s ease-out';
            
            setTimeout(() => {
                document.body.style.opacity = '1';
                document.body.style.transform = 'translateY(0)';
            }, 100);
        });
        
        // Add mouse move effect
        document.addEventListener('mousemove', (e) => {
            const mouseX = e.clientX / window.innerWidth;
            const mouseY = e.clientY / window.innerHeight;
            
            document.querySelectorAll('.particle').forEach((particle, index) => {
                const speed = (index + 1) * 0.1;
                const x = mouseX * speed * 50;
                const y = mouseY * speed * 50;
                particle.style.transform = `translate(${x}px, ${y}px)`;
            });
        });
        
        // Add intersection observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe elements for animation
        document.querySelectorAll('.stat-card, .contact-section').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.8s ease-out';
            observer.observe(el);
        });
        
        // Enhanced contact toggle
        function toggleContact() {
            const grid = document.getElementById('contactGrid');
            const isVisible = grid.style.maxHeight && grid.style.maxHeight !== '0px';
            
            if (isVisible) {
                grid.style.maxHeight = '0px';
                grid.style.opacity = '0';
                grid.style.transform = 'translateY(-20px)';
            } else {
                grid.style.maxHeight = '300px';
                grid.style.opacity = '1';
                grid.style.transform = 'translateY(0)';
            }
        }
        
        // Set initial state
        document.addEventListener('DOMContentLoaded', () => {
            const grid = document.getElementById('contactGrid');
            grid.style.maxHeight = '300px';
            grid.style.transition = 'all 0.5s cubic-bezier(0.4, 0, 0.2, 1)';
        });
    </script>
</body>
</html>
