# Soundarya-Yoga-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FaceYogaPro - Transform Your Face Naturally | AI-Powered Face Yoga Platform</title>
    <meta name="description" content="Professional face yoga platform with AI analysis, personalized routines for acne, wrinkles, sagging skin & more">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/responsive.css">
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <div class="logo" onclick="location.href='/'">
                <i class="fas fa-spa"></i>
                <span>FaceYoga<span class="pro">Pro</span></span>
            </div>
            
            <div class="nav-menu" id="navMenu">
                <a href="/" class="nav-link active">Home</a>
                <a href="routines.html" class="nav-link">Routines</a>
                <a href="#" id="analyzerLink" class="nav-link">AI Analyzer</a>
                <a href="community.html" class="nav-link">Community</a>
                <a href="blog.html" class="nav-link">Blog</a>
                <a href="#" id="dashboardLink" class="nav-link" style="display:none;">Dashboard</a>
            </div>
            
            <div class="nav-right">
                <div class="search-bar">
                    <i class="fas fa-search"></i>
                    <input type="text" id="searchInput" placeholder="Search routines, concerns...">
                </div>
                <div class="nav-icons">
                    <i class="far fa-heart" id="wishlistIcon" onclick="viewWishlist()"></i>
                    <i class="far fa-user" id="userIcon" onclick="toggleAuthModal()"></i>
                    <i class="fas fa-bars" id="mobileMenu"></i>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-container">
            <div class="hero-content">
                <div class="badge">✨ AI-Powered Face Yoga Platform</div>
                <h1>Transform Your Face<br><span class="gradient-text">Naturally & Scientifically</span></h1>
                <p>Join 50,000+ happy users getting real results with our AI-guided face yoga routines for acne, wrinkles, sagging skin, and more.</p>
                <div class="hero-buttons">
                    <button class="btn-primary" id="startAnalysisBtn">
                        <i class="fas fa-camera"></i> Start AI Analysis
                    </button>
                    <button class="btn-secondary" id="exploreBtn">
                        Explore Routines <i class="fas fa-arrow-right"></i>
                    </button>
                </div>
                <div class="stats">
                    <div class="stat">
                        <h3>50K+</h3>
                        <p>Active Users</p>
                    </div>
                    <div class="stat">
                        <h3>98%</h3>
                        <p>Satisfaction Rate</p>
                    </div>
                    <div class="stat">
                        <h3>15+</h3>
                        <p>Expert Trainers</p>
                    </div>
                    <div class="stat">
                        <h3>4.9★</h3>
                        <p>Trustpilot Rating</p>
                    </div>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=600" alt="Face Yoga">
                <div class="floating-card card1">
                    <i class="fas fa-smile"></i>
                    <span>7-Day Results</span>
                </div>
                <div class="floating-card card2">
                    <i class="fas fa-leaf"></i>
                    <span>Acne Control</span>
                </div>
                <div class="floating-card card3">
                    <i class="fas fa-chart-line"></i>
                    <span>98% Success</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-header">
                <h2>Why Choose FaceYogaPro?</h2>
                <p>Advanced technology combined with ancient techniques for real results</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-robot"></i></div>
                    <h3>AI Face Analysis</h3>
                    <p>Advanced AI detects wrinkles, acne, and face structure with 95% accuracy</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-user-md"></i></div>
                    <h3>Expert-Designed</h3>
                    <p>Routines created by certified face yoga instructors and dermatologists</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-chart-line"></i></div>
                    <h3>Track Progress</h3>
                    <p>Take weekly photos and see your transformation over time</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-comments"></i></div>
                    <h3>24/7 AI Chatbot</h3>
                    <p>Get instant answers to all your face yoga and skincare questions</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Concern Categories -->
    <section class="categories" id="routines">
        <div class="container">
            <div class="section-header">
                <h2>Choose Your Concern</h2>
                <p>Personalized routines for every face and skin concern</p>
            </div>
            
            <div class="category-filters">
                <button class="filter-btn active" data-category="all">All Concerns</button>
                <button class="filter-btn" data-category="skin">Skin Issues</button>
                <button class="filter-btn" data-category="wrinkles">Wrinkles & Lines</button>
                <button class="filter-btn" data-category="eyes">Eye Area</button>
                <button class="filter-btn" data-category="structure">Face Structure</button>
            </div>
            
            <div class="concerns-grid" id="concernsGrid"></div>
        </div>
    </section>

    <!-- AI Face Analyzer Section -->
    <section class="analyzer" id="analyzer">
        <div class="container">
            <div class="section-header">
                <h2>AI Face & Skin Analyzer</h2>
                <p>Get personalized recommendations based on your unique face</p>
            </div>
            
            <div class="analyzer-container">
                <div class="camera-section">
                    <div class="camera-wrapper">
                        <video id="video" autoplay muted playsinline></video>
                        <canvas id="overlayCanvas"></canvas>
                        <div class="camera-controls">
                            <button id="startCameraBtn" class="cam-btn primary">
                                <i class="fas fa-camera"></i> Start Camera
                            </button>
                            <button id="analyzeFaceBtn" class="cam-btn analyze" style="display:none;">
                                <i class="fas fa-microchip"></i> Analyze My Face
                            </button>
                            <button id="stopCameraBtn" class="cam-btn stop" style="display:none;">
                                <i class="fas fa-stop"></i> Stop
                            </button>
                        </div>
                    </div>
                </div>
                
                <div class="analysis-results" id="analysisResults">
                    <div class="analysis-placeholder">
                        <i class="fas fa-robot"></i>
                        <h3>AI Analysis Ready</h3>
                        <p>Our AI will analyze:</p>
                        <ul>
                            <li>✓ Wrinkle patterns & depth</li>
                            <li>✓ Acne & skin texture issues</li>
                            <li>✓ Face symmetry & structure</li>
                            <li>✓ Sagging & muscle tone</li>
                        </ul>
                        <button class="btn-primary" id="startAnalysisFromPlaceholder" style="margin-top: 20px;">
                            Start Free Analysis
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works -->
    <section class="how-it-works">
        <div class="container">
            <div class="section-header">
                <h2>How It Works</h2>
                <p>Get results in 3 simple steps</p>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <i class="fas fa-camera-retro"></i>
                    <h3>Analyze</h3>
                    <p>Take a photo or use live camera for AI analysis</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <i class="fas fa-clipboard-list"></i>
                    <h3>Get Plan</h3>
                    <p>Receive personalized routine for your concerns</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <i class="fas fa-calendar-check"></i>
                    <h3>Transform</h3>
                    <p>Practice daily and track your progress</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Success Stories -->
    <section class="testimonials">
        <div class="container">
            <div class="section-header">
                <h2>Real Results, Real People</h2>
                <p>Join thousands who transformed their faces naturally</p>
            </div>
            <div class="testimonials-slider">
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p>"After 4 weeks of the acne routine, my skin is clearer than ever! The AI analysis was spot-on."</p>
                    <div class="user">
                        <img src="https://randomuser.me/api/portraits/women/1.jpg" alt="User">
                        <div>
                            <h4>Sarah Johnson</h4>
                            <span>Acne Transformation</span>
                        </div>
                    </div>
                    <div class="before-after">
                        <span>✨ Visible results in 28 days</span>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p>"The forehead wrinkle exercises actually work! My husband noticed the difference in just 2 weeks."</p>
                    <div class="user">
                        <img src="https://randomuser.me/api/portraits/women/2.jpg" alt="User">
                        <div>
                            <h4>Emily Chen</h4>
                            <span>Anti-Wrinkle</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p>"Best investment in my skincare routine. The jawline exercises gave me visible definition!"</p>
                    <div class="user">
                        <img src="https://randomuser.me/api/portraits/men/1.jpg" alt="User">
                        <div>
                            <h4>David Rodriguez</h4>
                            <span>Jawline Transformation</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h2>Get Free Weekly Face Yoga Tips</h2>
                <p>Join 50,000+ subscribers receiving expert advice and exclusive routines</p>
                <form id="newsletterForm">
                    <input type="email" placeholder="Enter your email" required>
                    <button type="submit">Subscribe <i class="fas fa-paper-plane"></i></button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="logo" onclick="location.href='/'">
                        <i class="fas fa-spa"></i>
                        <span>FaceYogaPro</span>
                    </div>
                    <p>Transform your face naturally with AI-powered personalized face yoga routines.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-tiktok"></i></a>
                        <a href="#"><i class="fab fa-pinterest"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <a href="/">Home</a>
                    <a href="routines.html">All Routines</a>
                    <a href="#" id="footerAnalyzer">AI Analyzer</a>
                    <a href="community.html">Community</a>
                    <a href="blog.html">Blog</a>
                </div>
                <div class="footer-col">
                    <h4>Resources</h4>
                    <a href="#">Face Yoga Guide</a>
                    <a href="#">Skincare Tips</a>
                    <a href="#">Success Stories</a>
                    <a href="#">Research & Science</a>
                    <a href="#">FAQ</a>
                </div>
                <div class="footer-col">
                    <h4>Support</h4>
                    <a href="#">Contact Us</a>
                    <a href="#">Help Center</a>
                    <a href="#">Privacy Policy</a>
                    <a href="#">Terms of Service</a>
                    <a href="#">Affiliate Program</a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 FaceYogaPro. All rights reserved. | Made with <i class="fas fa-heart"></i> for natural beauty</p>
            </div>
        </div>
    </footer>

    <!-- Login/Signup Modal -->
    <div class="modal" id="authModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Welcome to FaceYogaPro</h2>
                <i class="fas fa-times" id="closeModal"></i>
            </div>
            <div class="modal-body">
                <div class="auth-tabs">
                    <button class="auth-tab active" data-auth="login">Login</button>
                    <button class="auth-tab" data-auth="signup">Sign Up</button>
                </div>
                
                <!-- Login Form -->
                <form id="loginForm" class="auth-form active">
                    <div class="input-group">
                        <i class="fas fa-envelope"></i>
                        <input type="email" id="loginEmail" placeholder="Email address" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-lock"></i>
                        <input type="password" id="loginPassword" placeholder="Password" required>
                    </div>
                    <div class="form-options">
                        <label>
                            <input type="checkbox"> Remember me
                        </label>
                        <a href="#">Forgot password?</a>
                    </div>
                    <button type="submit" class="btn-primary">Login <i class="fas fa-arrow-right"></i></button>
                    <div class="social-login">
                        <p>Or login with</p>
                        <div class="social-icons">
                            <button class="social-btn google"><i class="fab fa-google"></i></button>
                            <button class="social-btn facebook"><i class="fab fa-facebook-f"></i></button>
                            <button class="social-btn apple"><i class="fab fa-apple"></i></button>
                        </div>
                    </div>
                    <p class="auth-footer">New to FaceYogaPro? <span class="switch-auth">Create account</span></p>
                </form>
                
                <!-- Signup Form -->
                <form id="signupForm" class="auth-form">
                    <div class="input-group">
                        <i class="fas fa-user"></i>
                        <input type="text" id="signupName" placeholder="Full name" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-envelope"></i>
                        <input type="email" id="signupEmail" placeholder="Email address" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-lock"></i>
                        <input type="password" id="signupPassword" placeholder="Create password" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-check-circle"></i>
                        <input type="password" id="signupConfirmPassword" placeholder="Confirm password" required>
                    </div>
                    <button type="submit" class="btn-primary">Create Free Account</button>
                    <p class="auth-footer">Already have an account? <span class="switch-auth">Login</span></p>
                </form>
            </div>
        </div>
    </div>

    <!-- Routine Display Modal -->
    <div class="modal" id="routineModal">
        <div class="modal-content modal-large">
            <div class="modal-header">
                <h2 id="routineModalTitle"></h2>
                <i class="fas fa-times" id="closeRoutineModal"></i>
            </div>
            <div class="modal-body" id="routineModalBody"></div>
        </div>
    </div>

    <!-- AI Chatbot -->
    <div class="chatbot-container" id="chatbotContainer">
        <div class="chatbot-toggle" id="chatbotToggle">
            <i class="fas fa-comment-dots"></i>
            <span class="notification-badge">1</span>
        </div>
        <div class="chatbot-window" id="chatbotWindow">
            <div class="chatbot-header">
                <div class="chatbot-info">
                    <i class="fas fa-robot"></i>
                    <div>
                        <h4>FaceYogAI Assistant</h4>
                        <p>Online • Ask me anything</p>
                    </div>
                </div>
                <i class="fas fa-times" id="closeChatbot"></i>
            </div>
            <div class="chatbot-messages" id="chatbotMessages">
                <div class="message bot">
                    <div class="message-content">
                        👋 Hello! I'm your Face Yoga expert. I can help with:
                        <ul style="margin-top: 8px;">
                            <li>💆‍♀️ Acne & skin concerns</li>
                            <li>📜 Wrinkle reduction techniques</li>
                            <li>👁️ Eye area exercises</li>
                            <li>📋 Personalized routine advice</li>
                        </ul>
                        What would you like to know?
                    </div>
                </div>
            </div>
            <div class="chatbot-input">
                <input type="text" id="chatbotInput" placeholder="Ask me about face yoga, acne, wrinkles...">
                <button id="sendChatbotMsg">
                    <i class="fas fa-paper-plane"></i>
                </button>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/face-api.js@0.22.2/dist/face-api.min.js"></script>
    <script src="js/yoga-data.js"></script>
    <script src="js/face-analysis.js"></script>
    <script src="js/auth.js"></script>
    <script src="js/chatbot.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
