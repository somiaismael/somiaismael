<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SP-XD GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #c9d1d9;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1100px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 20px 0 30px;
            border-bottom: 1px solid #30363d;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #58a6ff, #1DB954, #f0db4f);
            z-index: 1;
        }
        
        .profile-header {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .avatar-container {
            position: relative;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            overflow: hidden;
            border: 3px solid #58a6ff;
            box-shadow: 0 0 25px rgba(88, 166, 255, 0.4);
        }
        
        .avatar {
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, #1a1f27, #2d3746);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #58a6ff;
            font-size: 60px;
        }
        
        .header-text {
            text-align: left;
            max-width: 500px;
        }
        
        .username {
            font-size: 32px;
            font-weight: 700;
            color: #f0f6fc;
            margin-bottom: 5px;
        }
        
        .title {
            font-size: 20px;
            color: #58a6ff;
            margin-bottom: 15px;
        }
        
        .bio {
            font-size: 16px;
            color: #8b949e;
            margin-bottom: 20px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .badge {
            background: rgba(88, 166, 255, 0.1);
            padding: 6px 15px;
            border-radius: 20px;
            border: 1px solid #30363d;
            display: flex;
            align-items: center;
            font-size: 14px;
            transition: all 0.3s ease;
            cursor: default;
        }
        
        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(88, 166, 255, 0.2);
            background: rgba(88, 166, 255, 0.2);
        }
        
        .badge i {
            margin-right: 8px;
            font-size: 16px;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .stat-card {
            background: rgba(13, 17, 23, 0.7);
            border: 1px solid #30363d;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            min-width: 150px;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            border-color: #58a6ff;
        }
        
        .stat-number {
            font-size: 32px;
            font-weight: 700;
            color: #58a6ff;
            margin-bottom: 5px;
        }
        
        .stat-label {
            font-size: 14px;
            color: #8b949e;
        }
        
        .skills-section {
            margin: 50px 0;
        }
        
        .section-title {
            font-size: 28px;
            font-weight: 700;
            color: #f0f6fc;
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #58a6ff, #1DB954);
            border-radius: 2px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .skill-card {
            background: rgba(22, 27, 34, 0.7);
            border: 1px solid #30363d;
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
            border-color: #58a6ff;
        }
        
        .skill-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: #58a6ff;
        }
        
        .skill-title {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .skill-title i {
            font-size: 28px;
            color: #58a6ff;
            margin-right: 15px;
            width: 50px;
            height: 50px;
            background: rgba(88, 166, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .skill-name {
            font-size: 20px;
            font-weight: 600;
            color: #f0f6fc;
        }
        
        .skill-desc {
            font-size: 15px;
            color: #8b949e;
            line-height: 1.7;
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        .skill-tag {
            background: rgba(88, 166, 255, 0.1);
            color: #58a6ff;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 13px;
        }
        
        .footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid #30363d;
            color: #8b949e;
            font-size: 14px;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(88, 166, 255, 0.1);
            color: #58a6ff;
            font-size: 20px;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-icons a:hover {
            transform: translateY(-5px);
            background: #58a6ff;
            color: #0d1117;
            box-shadow: 0 5px 15px rgba(88, 166, 255, 0.3);
        }
        
        @media (max-width: 768px) {
            .profile-header {
                flex-direction: column;
                text-align: center;
            }
            
            .header-text {
                text-align: center;
            }
            
            .badges {
                justify-content: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animation for cards */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .skill-card {
            animation: fadeIn 0.6s ease forwards;
            opacity: 0;
        }
        
        .skill-card:nth-child(1) { animation-delay: 0.1s; }
        .skill-card:nth-child(2) { animation-delay: 0.2s; }
        .skill-card:nth-child(3) { animation-delay: 0.3s; }
        .skill-card:nth-child(4) { animation-delay: 0.4s; }
        .skill-card:nth-child(5) { animation-delay: 0.5s; }
        .skill-card:nth-child(6) { animation-delay: 0.6s; }
        .skill-card:nth-child(7) { animation-delay: 0.7s; }
        .skill-card:nth-child(8) { animation-delay: 0.8s; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-header">
                <div class="avatar-container">
                    <div class="avatar">
                        <i class="fas fa-code"></i>
                    </div>
                </div>
                <div class="header-text">
                    <h1 class="username">SP-XD</h1>
                    <h2 class="title">Cross-Platform Mobile App Developer</h2>
                    <p class="bio">Passionate Flutter developer creating beautiful, high-performance mobile applications with clean code and modern architecture.</p>
                    
                    <div class="badges">
                        <div class="badge">
                            <i class="fab fa-github"></i> GitHub Pro
                        </div>
                        <div class="badge">
                            <i class="fas fa-code-branch"></i> 50+ Repositories
                        </div>
                        <div class="badge">
                            <i class="fab fa-telegram"></i> @spxd007
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">7+</div>
                    <div class="stat-label">Years Experience</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">25+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">12K+</div>
                    <div class="stat-label">Code Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">98%</div>
                    <div class="stat-label">Success Rate</div>
                </div>
            </div>
        </header>
        
        <section class="skills-section">
            <h2 class="section-title">Technical Skills</h2>
            
            <div class="skills-grid">
                <!-- Skill 1 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-mobile-alt"></i>
                        <h3 class="skill-name">Cross-Platform Development</h3>
                    </div>
                    <p class="skill-desc">Specializing in Flutter for creating high-performance iOS and Android apps with a single codebase.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Flutter</span>
                        <span class="skill-tag">Dart</span>
                        <span class="skill-tag">iOS</span>
                        <span class="skill-tag">Android</span>
                    </div>
                </div>
                
                <!-- Skill 2 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fab fa-dart"></i>
                        <h3 class="skill-name">Dart & OOP</h3>
                    </div>
                    <p class="skill-desc">Expert in Dart programming language and object-oriented design principles for creating scalable applications.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Dart</span>
                        <span class="skill-tag">OOP</span>
                        <span class="skill-tag">Design Patterns</span>
                    </div>
                </div>
                
                <!-- Skill 3 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-fire"></i>
                        <h3 class="skill-name">Firebase Services</h3>
                    </div>
                    <p class="skill-desc">Implementing Firebase Authentication, Firestore, Storage, and other Firebase services for backend functionality.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Firebase Auth</span>
                        <span class="skill-tag">Firestore</span>
                        <span class="skill-tag">Cloud Storage</span>
                    </div>
                </div>
                
                <!-- Skill 4 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-sitemap"></i>
                        <h3 class="skill-name">State Management</h3>
                    </div>
                    <p class="skill-desc">Expert in GetX and BLoC state management solutions for building maintainable and scalable applications.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">GetX</span>
                        <span class="skill-tag">BLoC</span>
                        <span class="skill-tag">Provider</span>
                    </div>
                </div>
                
                <!-- Skill 5 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fab fa-php"></i>
                        <h3 class="skill-name">PHP Development</h3>
                    </div>
                    <p class="skill-desc">Building robust backend solutions and APIs with PHP for mobile and web applications.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">PHP</span>
                        <span class="skill-tag">Laravel</span>
                        <span class="skill-tag">Backend</span>
                    </div>
                </div>
                
                <!-- Skill 6 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-plug"></i>
                        <h3 class="skill-name">API Integration</h3>
                    </div>
                    <p class="skill-desc">Connecting applications to RESTful APIs and working with tools like Thunder Client for API testing.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">REST API</span>
                        <span class="skill-tag">JSON</span>
                        <span class="skill-tag">Thunder Client</span>
                    </div>
                </div>
                
                <!-- Skill 7 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-database"></i>
                        <h3 class="skill-name">Database Management</h3>
                    </div>
                    <p class="skill-desc">Working with various databases including MySQL, Firebase, Firestore, and SQLite for local storage.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">Firestore</span>
                        <span class="skill-tag">SQLite</span>
                    </div>
                </div>
                
                <!-- Skill 8 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-users"></i>
                        <h3 class="skill-name">Social Authentication</h3>
                    </div>
                    <p class="skill-desc">Implementing social media login/sign-up (Facebook, Twitter, Instagram) and Firebase Authentication.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">OAuth</span>
                        <span class="skill-tag">Firebase Auth</span>
                        <span class="skill-tag">Social Login</span>
                    </div>
                </div>
                
                <!-- Skill 9 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-cloud"></i>
                        <h3 class="skill-name">Cloud Services</h3>
                    </div>
                    <p class="skill-desc">Leveraging Google Cloud services for scalable infrastructure and cloud messaging solutions.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Google Cloud</span>
                        <span class="skill-tag">Cloud Messaging</span>
                        <span class="skill-tag">Firebase</span>
                    </div>
                </div>
                
                <!-- Skill 10 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-bell"></i>
                        <h3 class="skill-name">Notifications</h3>
                    </div>
                    <p class="skill-desc">Implementing cloud messaging and local notifications to enhance user engagement.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">FCM</span>
                        <span class="skill-tag">Local Notifications</span>
                    </div>
                </div>
                
                <!-- Skill 11 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-mobile"></i>
                        <h3 class="skill-name">Responsive Design</h3>
                    </div>
                    <p class="skill-desc">Creating adaptive UIs that work seamlessly across various screen sizes and devices.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Responsive UI</span>
                        <span class="skill-tag">Adaptive Layout</span>
                        <span class="skill-tag">Flutter</span>
                    </div>
                </div>
                
                <!-- Skill 12 -->
                <div class="skill-card">
                    <div class="skill-title">
                        <i class="fas fa-save"></i>
                        <h3 class="skill-name">Local Storage</h3>
                    </div>
                    <p class="skill-desc">Using Shared Preferences for local data persistence and caching in mobile applications.</p>
                    <div class="skill-tags">
                        <span class="skill-tag">Shared Preferences</span>
                        <span class="skill-tag">Hive</span>
                        <span class="skill-tag">Local Storage</span>
                    </div>
                </div>
            </div>
        </section>
        
        <div class="footer">
            <p>"Turning complex ideas into elegant mobile solutions"</p>
            <div class="social-icons">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-telegram"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
            </div>
            <p style="margin-top: 20px;">© 2023 SP-XD | Mobile App Developer</p>
        </div>
    </div>
    
    <script>
        // Simple animation on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const skillCards = document.querySelectorAll('.skill-card');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animationPlayState = 'running';
                    }
                });
            }, { threshold: 0.1 });
            
            skillCards.forEach(card => {
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
