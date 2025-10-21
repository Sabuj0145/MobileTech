<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MobileTech - Premium Pre-owned Phones</title>
    <style>
        /* CSS Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --text-color: #333;
            --text-light: #7f8c8d;
        }

        body {
            background-color: #f9f9f9;
            color: var(--text-color);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 12px 24px;
            border-radius: 4px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .btn-primary {
            background-color: var(--accent-color);
        }

        .btn-primary:hover {
            background-color: #c0392b;
        }

        /* Header Styles */
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
            font-size: 24px;
            font-weight: 700;
            color: var(--primary-color);
        }

        .logo span {
            color: var(--secondary-color);
        }

        nav ul {
            display: flex;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--secondary-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), url('https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }

        /* Categories Section */
        .categories {
            padding: 80px 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 32px;
            color: var(--primary-color);
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .category-card {
            background-color: var(--light-color);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .category-card:hover {
            transform: translateY(-10px);
        }

        .category-img {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }

        .category-content {
            padding: 20px;
            text-align: center;
        }

        .category-content h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }

        .category-content p {
            margin-bottom: 20px;
            color: var(--text-light);
        }

        /* Products Section */
        .products {
            padding: 80px 0;
            background-color: #f5f7fa;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-img {
            height: 200px;
            width: 100%;
            object-fit: contain;
            padding: 15px;
            background-color: #f9f9f9;
        }

        .product-content {
            padding: 20px;
        }

        .product-content h3 {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .product-price {
            font-size: 20px;
            font-weight: 700;
            color: var(--accent-color);
            margin-bottom: 15px;
        }

        .product-features {
            margin-bottom: 20px;
            color: var(--text-light);
            font-size: 14px;
        }

        /* Footer Styles */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--secondary-color);
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            transition: color 0.3s ease;
        }

        .footer-column ul li a:hover {
            color: var(--secondary-color);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 14px;
            color: rgba(255, 255, 255, 0.7);
        }

        .address {
            font-style: normal;
            line-height: 1.8;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }

            nav ul {
                margin-top: 15px;
            }

            nav ul li {
                margin: 0 10px;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container header-container">
            <div class="logo">Mobile<span>Tech</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#categories">Categories</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Premium Pre-owned Phones</h1>
            <p>Discover high-quality second-hand iPhones and Samsung devices at unbeatable prices. All devices are thoroughly tested and certified.</p>
            <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn btn-primary">Order Now</a>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="categories" id="categories">
        <div class="container">
            <h2 class="section-title">Phone Categories</h2>
            <div class="category-grid">
                <div class="category-card">
                    <img src="6.png" alt="iPhone Category" class="category-img">
                    <div class="category-content">
                        <h3>iPhone</h3>
                        <p>Latest and previous generation iPhones in excellent condition</p>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Browse iPhones</a>
                    </div>
                </div>
                <div class="category-card">
                    <img src="9.png" alt="Samsung Category" class="category-img">
                    <div class="category-content">
                        <h3>Samsung</h3>
                        <p>Galaxy series and other Samsung models with warranty</p>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Browse Samsung</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title">Featured Products</h2>
            <div class="product-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <img src="1.png" alt="iPhone 12 Pro" class="product-img">
                    <div class="product-content">
                        <h3>iPhone 12 Pro</h3>
                        <div class="product-price">$119</div>
                        <div class="product-features">
                            <p>128GB • Pacific Blue • Excellent Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 2 -->
                <div class="product-card">
                    <img src="2.jpg" alt="Samsung Galaxy S21" class="product-img">
                    <div class="product-content">
                        <h3>Samsung Galaxy S21</h3>
                        <div class="product-price">$109</div>
                        <div class="product-features">
                            <p>256GB • Phantom Black • Like New</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 3 -->
                <div class="product-card">
                    <img src="3.jpg" alt="iPhone 11" class="product-img">
                    <div class="product-content">
                        <h3>iPhone 11</h3>
                        <div class="product-price">$89</div>
                        <div class="product-features">
                            <p>64GB • Purple • Good Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 4 -->
                <div class="product-card">
                    <img src="4.png" alt="Samsung Galaxy Note 20" class="product-img">
                    <div class="product-content">
                        <h3>Samsung Galaxy Note 20</h3>
                        <div class="product-price">$129</div>
                        <div class="product-features">
                            <p>256GB • Mystic Bronze • Excellent Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 5 -->
                <div class="product-card">
                    <img src="5.jpg" alt="iPhone SE" class="product-img">
                    <div class="product-content">
                        <h3>iPhone SE (2020)</h3>
                        <div class="product-price">$59</div>
                        <div class="product-features">
                            <p>128GB • White • Very Good Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 6 -->
                <div class="product-card">
                    <img src="6.png" alt="Samsung Galaxy A52" class="product-img">
                    <div class="product-content">
                        <h3>Samsung Galaxy A52</h3>
                        <div class="product-price">$69</div>
                        <div class="product-features">
                            <p>128GB • Awesome Black • Good Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 7 -->
                <div class="product-card">
                    <img src="7.jpg" alt="iPhone XR" class="product-img">
                    <div class="product-content">
                        <h3>iPhone XR</h3>
                        <div class="product-price">$69</div>
                        <div class="product-features">
                            <p>64GB • Coral • Fair Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 8 -->
                <div class="product-card">
                    <img src="8.jpg" alt="Samsung Galaxy Z Flip" class="product-img">
                    <div class="product-content">
                        <h3>Samsung Galaxy Z Flip</h3>
                        <div class="product-price">$159</div>
                        <div class="product-features">
                            <p>256GB • Mirror Purple • Like New</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
                <!-- Product 9 -->
                <div class="product-card">
                    <img src="9.png" alt="iPhone 13 Mini" class="product-img">
                    <div class="product-content">
                        <h3>iPhone 13 Mini</h3>
                        <div class="product-price">$139</div>
                        <div class="product-features">
                            <p>128GB • Pink • Excellent Condition</p>
                        </div>
                        <a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff" class="btn">Order Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>MobileTech</h3>
                    <p>Your trusted source for premium pre-owned smartphones. Quality devices at affordable prices.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#categories">Categories</a></li>
                        <li><a href="#products">Products</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Categories</h3>
                    <ul>
                        <li><a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff">iPhone</a></li>
                        <li><a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff">Samsung</a></li>
                        <li><a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff">Accessories</a></li>
                        <li><a href="https://www.effectivegatecpm.com/r05ak5c2?key=a31c933f03969285c79e5c51026686ff">Tablets</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <div class="address">
                        <p><strong>New York Store:</strong><br>
                        123 Tech Avenue, Suite 101<br>
                        New York, NY 10001<br>
                        Phone: (212) 555-1234</p>
                        
                        <p><strong>Los Angeles Store:</strong><br>
                        456 Innovation Blvd<br>
                        Los Angeles, CA 90001<br>
                        Phone: (310) 555-5678</p>
                        
                        <p><strong>Chicago Store:</strong><br>
                        789 Mobile Street<br>
                        Chicago, IL 60601<br>
                        Phone: (312) 555-9012</p>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 MobileTech. All rights reserved. | Premium Pre-owned Phones</p>
            </div>
        </div>
    </footer>

    <script>
        // JavaScript for smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Add active class to navigation links on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('nav ul li a');
            
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if(pageYOffset >= (sectionTop - 100)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if(link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });

        // Simple form validation for newsletter signup (if added later)
        function validateForm() {
            const email = document.getElementById('email').value;
            if(!email) {
                alert('Please enter your email address');
                return false;
            }
            return true;
        }
    </script>
</body>
</html>
