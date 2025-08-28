<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lazanya - Authentic Italian Restaurant</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #c41e3a;
            --secondary: #f8b500;
            --dark: #252525;
            --light: #f9f9f9;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark);
            background-color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header & Navigation */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            z-index: 1000;
            padding: 1rem 0;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 2rem;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .nav-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 30px;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .nav-btn:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?ixlib=rb-4.0.3&auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .hero-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
            margin: 0 0.5rem;
        }
        
        .hero-btn:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        .hero-btn.outline {
            background-color: transparent;
            border: 2px solid white;
        }
        
        .hero-btn.outline:hover {
            background-color: white;
            color: var(--dark);
        }
        
        /* About Section */
        .about {
            padding: 5rem 0;
            background-color: white;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            max-width: 600px;
            margin: 0 auto;
            color: #777;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: var(--transition);
        }
        
        .about-image img:hover {
            transform: scale(1.05);
        }
        
        /* Menu Section */
        .menu {
            padding: 5rem 0;
            background-color: #f5f5f5;
        }
        
        .menu-filters {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }
        
        .filter-btn {
            background: white;
            border: none;
            padding: 0.7rem 1.5rem;
            margin: 0.5rem;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .filter-btn.active, .filter-btn:hover {
            background-color: var(--primary);
            color: white;
        }
        
        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .menu-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }
        
        .menu-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .menu-item-content {
            padding: 1.5rem;
        }
        
        .menu-item h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .menu-item p {
            color: #777;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
        
        .menu-item-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .price {
            font-weight: 600;
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .add-to-cart {
            background-color: var(--secondary);
            color: var(--dark);
            border: none;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .add-to-cart:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 5rem 0;
            background-color: white;
        }
        
        .testimonials-container {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial {
            text-align: center;
            padding: 2rem;
            display: none;
        }
        
        .testimonial.active {
            display: block;
            animation: fadeIn 1s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .testimonial img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 1rem;
            border: 3px solid var(--primary);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
            font-size: 1.1rem;
        }
        
        .testimonial-author {
            font-weight: 600;
            color: var(--primary);
        }
        
        .testimonial-nav {
            display: flex;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .testimonial-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: #ddd;
            margin: 0 5px;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .testimonial-dot.active {
            background-color: var(--primary);
        }
        
        /* Reservation */
        .reservation {
            padding: 5rem 0;
            background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), url('https://images.unsplash.com/photo-1414235077428-338989a2e8c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }
        
        .reservation h2 {
            margin-bottom: 2rem;
        }
        
        .reservation-form {
            max-width: 600px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }
        
        .form-group {
            text-align: left;
        }
        
        .form-group.full {
            grid-column: 1 / span 2;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: none;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
        }
        
        .reservation-btn {
            grid-column: 1 / span 2;
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 1rem;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .reservation-btn:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-section h3 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }
        
        .footer-section p, .footer-section li {
            margin-bottom: 0.8rem;
            color: #ccc;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section a {
            color: #ccc;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-section a:hover {
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: #333;
            color: white;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid #444;
            color: #999;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h2 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                padding: 1rem 0;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 0.5rem 0;
                text-align: center;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .reservation-form {
                grid-template-columns: 1fr;
            }
            
            .form-group.full {
                grid-column: 1;
            }
        }
        
        @media (max-width: 576px) {
            .hero-buttons {
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }
            
            .hero-btn {
                margin: 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <h1>Laz<span>anya</span></h1>
            </div>
            <nav>
                <ul id="nav-menu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#menu">Menu</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#reservation">Reservation</a></li>
                </ul>
            </nav>
            <button class="nav-btn">Order Online</button>
            <div class="mobile-menu-btn" id="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h2>Authentic Italian Lasagna & Pasta</h2>
            <p>Experience the taste of Italy with our handcrafted dishes made from traditional recipes and the finest ingredients.</p>
            <div class="hero-buttons">
                <button class="hero-btn">View Menu</button>
                <button class="hero-btn outline">Book a Table</button>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>Our Story</h2>
                <p>Discover the passion and tradition behind Lazanya</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Traditional Italian Cuisine Since 1995</h3>
                    <p>Founded by the Rossi family, Lazanya brings the authentic flavors of Italy to your table. Our recipes have been passed down through generations, ensuring an unforgettable dining experience.</p>
                    <p>We source only the freshest ingredients, importing many specialty items directly from Italy to create dishes that truly capture the essence of Italian cuisine.</p>
                    <p>Our chefs are masters of traditional techniques, crafting each dish with care and passion that you can taste in every bite.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1598866594230-a7c12756260f?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Chef preparing pasta">
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section class="menu" id="menu">
        <div class="container">
            <div class="section-title">
                <h2>Our Specialties</h2>
                <p>Delight your palate with our exquisite dishes</p>
            </div>
            <div class="menu-filters">
                <button class="filter-btn active">All</button>
                <button class="filter-btn">Lasagna</button>
                <button class="filter-btn">Pasta</button>
                <button class="filter-btn">Appetizers</button>
                <button class="filter-btn">Desserts</button>
            </div>
            <div class="menu-items">
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1574894709920-11b28e7367e3?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Classic Lasagna">
                    <div class="menu-item-content">
                        <h3>Classic Lasagna</h3>
                        <p>Layers of pasta, beef ragù, béchamel sauce, and Parmigiano-Reggiano</p>
                        <div class="menu-item-price">
                            <span class="price">$16.99</span>
                            <button class="add-to-cart"><i class="fas fa-plus"></i></button>
                        </div>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1621996346565-e3dbc353d2e5?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Truffle Mushroom Lasagna">
                    <div class="menu-item-content">
                        <h3>Truffle Mushroom Lasagna</h3>
                        <p>Wild mushrooms, black truffle, and three cheeses in a creamy sauce</p>
                        <div class="menu-item-price">
                            <span class="price">$18.99</span>
                            <button class="add-to-cart"><i class="fas fa-plus"></i></button>
                        </div>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1611270629569-8b357cb3082c?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Seafood Linguine">
                    <div class="menu-item-content">
                        <h3>Seafood Linguine</h3>
                        <p>Fresh seafood, tomatoes, garlic, and white wine sauce</p>
                        <div class="menu-item-price">
                            <span class="price">$19.99</span>
                            <button class="add-to-cart"><i class="fas fa-plus"></i></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Customers Say</h2>
                <p>Authentic experiences from our beloved customers</p>
            </div>
            <div class="testimonials-container">
                <div class="testimonial active">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Customer">
                    <p class="testimonial-text">"The best Italian food I've had outside of Italy! The lasagna was perfectly cooked and full of flavor. Will definitely be back!"</p>
                    <p class="testimonial-author">- Michael Johnson</p>
                </div>
                <div class="testimonial">
                    <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Customer">
                    <p class="testimonial-text">"Authentic flavors and cozy atmosphere. The pasta was cooked to perfection and the service was exceptional. Highly recommend!"</p>
                    <p class="testimonial-author">- Sarah Williams</p>
                </div>
                <div class="testimonial">
                    <img src="https://images.unsplash.com/photo-1552058544-f2b08422138a?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="Customer">
                    <p class="testimonial-text">"I've been coming to Lazanya for years and the quality never disappoints. Their traditional recipes transport me back to my grandmother's kitchen in Naples."</p>
                    <p class="testimonial-author">- Antonio Rossi</p>
                </div>
                <div class="testimonial-nav">
                    <div class="testimonial-dot active"></div>
                    <div class="testimonial-dot"></div>
                    <div class="testimonial-dot"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reservation -->
    <section class="reservation" id="reservation">
        <div class="container">
            <div class="section-title">
                <h2>Make a Reservation</h2>
                <p>Book your table now and experience the taste of Italy</p>
            </div>
            <form class="reservation-form">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" placeholder="Full Name">
                </div>
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" placeholder="Your Email">
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" placeholder="Your Phone">
                </div>
                <div class="form-group">
                    <label for="guests">Number of Guests</label>
                    <select id="guests">
                        <option value="1">1 Person</option>
                        <option value="2">2 People</option>
                        <option value="3">3 People</option>
                        <option value="4">4 People</option>
                        <option value="5+">5+ People</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="date">Date</label>
                    <input type="date" id="date">
                </div>
                <div class="form-group">
                    <label for="time">Time</label>
                    <select id="time">
                        <option value="17:00">5:00 PM</option>
                        <option value="17:30">5:30 PM</option>
                        <option value="18:00">6:00 PM</option>
                        <option value="18:30">6:30 PM</option>
                        <option value="19:00">7:00 PM</option>
                        <option value="19:30">7:30 PM</option>
                        <option value="20:00">8:00 PM</option>
                        <option value="20:30">8:30 PM</option>
                    </select>
                </div>
                <div class="form-group full">
                    <label for="message">Special Requests</label>
                    <textarea id="message" rows="3" placeholder="Any special requests?"></textarea>
                </div>
                <button type="submit" class="reservation-btn">Book Now</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Lazanya</h3>
                    <p>Authentic Italian restaurant serving traditional lasagna and pasta dishes since 1995.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-tripadvisor"></i></a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>Hours</h3>
                    <p>Monday - Thursday: 11am - 10pm</p>
                    <p>Friday - Saturday: 11am - 11pm</p>
                    <p>Sunday: 12pm - 9pm</p>
                </div>
                <div class="footer-section">
                    <h3>Contact</h3>
                    <p><i class="fas fa-map-marker-alt"></i> 123 Pasta Street, Foodville</p>
                    <p><i class="fas fa-phone"></i> (123) 456-7890</p>
                    <p><i class="fas fa-envelope"></i> info@lazanya.com</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Lazanya Restaurant. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const navMenu = document.getElementById('nav-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            navMenu.classList.toggle('show');
        });
        
        // Testimonial Slider
        const testimonials = document.querySelectorAll('.testimonial');
        const dots = document.querySelectorAll('.testimonial-dot');
        let currentTestimonial = 0;
        
        function showTestimonial(n) {
            testimonials.forEach(testimonial => testimonial.classList.remove('active'));
            dots.forEach(dot => dot.classList.remove('active'));
            
            testimonials[n].classList.add('active');
            dots[n].classList.add('active');
            currentTestimonial = n;
        }
        
        dots.forEach((dot, index) => {
            dot.addEventListener('click', () => {
                showTestimonial(index);
            });
        });
        
        // Auto rotate testimonials
        setInterval(() => {
            currentTestimonial = (currentTestimonial + 1) % testimonials.length;
            showTestimonial(currentTestimonial);
        }, 5000);
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    navMenu.classList.remove('show');
                }
            });
        });
        
        // Form submission
        const reservationForm = document.querySelector('.reservation-form');
        reservationForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your reservation! We will confirm shortly.');
            reservationForm.reset();
        });
    </script>
</body>
</html>
