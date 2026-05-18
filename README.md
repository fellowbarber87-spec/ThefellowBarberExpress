# ThefellowBarberExpress
its a barbershop we are here to serve not rush.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Fellow Barber Express | Premium Cuts in Adelaide</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            background-color: #f8f6f2;
            color: #1a1a1a;
            line-height: 1.5;
        }

        /* Header & Navigation */
        header {
            background-color: #0a0a0a;
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo h1 {
            font-size: 1.6rem;
            letter-spacing: 1px;
        }

        .logo p {
            font-size: 0.8rem;
            color: #d4af37;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #d4af37;
        }

        /* Buttons */
        .btn-book, .btn-call, .btn-submit {
            background-color: #d4af37;
            color: #0a0a0a;
            border: none;
            padding: 0.8rem 1.8rem;
            font-weight: bold;
            border-radius: 40px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: transform 0.2s, background 0.3s;
        }

        .btn-book:hover, .btn-call:hover, .btn-submit:hover {
            background-color: #c4a02e;
            transform: scale(1.02);
        }

        .btn-call {
            background-color: #2e7d32;
            color: white;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.65), rgba(0,0,0,0.65)), url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?w=1600&h=600&fit=crop');
            background-size: cover;
            background-position: center 30%;
            color: white;
            text-align: center;
            padding: 5rem 2rem;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* Sections */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 3rem 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 2rem;
            color: #0a0a0a;
            border-bottom: 3px solid #d4af37;
            display: inline-block;
            width: auto;
            padding-bottom: 0.5rem;
        }

        .title-wrapper {
            text-align: center;
            margin-bottom: 2rem;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }

        .service-card {
            background: white;
            padding: 1.8rem;
            border-radius: 16px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.2s;
            text-align: center;
            border: 1px solid #e0d6c5;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-card h3 {
            font-size: 1.6rem;
            margin-bottom: 0.8rem;
        }

        .price {
            font-size: 1.7rem;
            font-weight: bold;
            color: #d4af37;
            margin: 1rem 0;
        }

        .service-desc {
            color: #555;
            font-size: 0.9rem;
        }

        /* About Section */
        .about {
            background-color: #e8e2d4;
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            align-items: center;
        }
        
        .about-text {
            flex: 2;
        }
        
        .about-text p {
            margin-bottom: 1rem;
            font-size: 1.05rem;
        }
        
        .about-highlight {
            background: #0a0a0a;
            color: #d4af37;
            padding: 1rem;
            border-radius: 12px;
            margin-top: 1rem;
            text-align: center;
        }

        /* Hours & Contact */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .info-card {
            background: white;
            padding: 1.5rem;
            border-radius: 16px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            text-align: center;
        }

        .info-card h3 {
            margin-bottom: 1rem;
            font-size: 1.4rem;
        }

        .hours-list p {
            margin: 0.5rem 0;
        }

        .map-placeholder {
            background: #ddd;
            height: 200px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #333;
            font-size: 0.9rem;
            margin-top: 1rem;
        }

        /* Contact Form */
        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1rem;
        }

        .contact-form input, .contact-form textarea {
            padding: 0.8rem;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-family: inherit;
        }

        .contact-form textarea {
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: #0a0a0a;
            color: #aaa;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }

        .social-links a {
            color: #d4af37;
            margin: 0 0.75rem;
            text-decoration: none;
            font-weight: bold;
        }

        /* Mobile */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                text-align: center;
            }
            .hero h2 {
                font-size: 2rem;
            }
            .section-title {
                font-size: 1.8rem;
            }
            .btn-book, .btn-call {
                padding: 0.6rem 1.2rem;
            }
        }
    </style>
</head>
<body>

<header>
    <div class="nav-container">
        <div class="logo">
            <h1>✂️ FELLOW BARBER EXPRESS</h1>
            <p>Adelaide | Premium Cuts & Grooming</p>
        </div>
        <div class="nav-links">
            <a href="#services">Services</a>
            <a href="#about">About</a>
            <a href="#hours">Hours</a>
            <a href="#contact">Contact</a>
        </div>
    </div>
</header>

<section class="hero">
    <h2>Sharp Styles. Express Service.</h2>
    <p>Walk-ins welcome or book ahead — premium barbering in the heart of Adelaide.</p>
    <div class="hero-buttons">
        <a href="#contact" class="btn-book">📅 Book Now</a>
        <a href="tel:+61812345678" class="btn-call">📞 Call (08) 1234 5678</a>
    </div>
</section>

<!-- Services Section -->
<section id="services">
    <div class="container">
        <div class="title-wrapper">
            <h2 class="section-title">Our Services</h2>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <h3>✂️ Classic Haircut</h3>
                <div class="price">$35</div>
                <p class="service-desc">Precision scissor & clipper cut. Finished with hot towel.</p>
            </div>
            <div class="service-card">
                <h3>🧔 Beard Trim</h3>
                <div class="price">$20</div>
                <p class="service-desc">Shape, line-up, and oil finish. Beard wash included.</p>
            </div>
            <div class="service-card">
                <h3>💈 Cut + Beard Combo</h3>
                <div class="price">$50</div>
                <p class="service-desc">Haircut & full beard service — best value.</p>
            </div>
            <div class="service-card">
                <h3>✨ Hot Towel Shave</h3>
                <div class="price">$40</div>
                <p class="service-desc">Traditional straight razor shave with steamed towels.</p>
            </div>
            <div class="service-card">
                <h3>🧴 Kids Cut (under 12)</h3>
                <div class="price">$25</div>
                <p class="service-desc">Quick, friendly cut for little gents.</p>
            </div>
            <div class="service-card">
                <h3>🎓 Student/Senior</h3>
                <div class="price">$30</div>
                <p class="service-desc">Valid ID required. Same quality cut.</p>
            </div>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about" class="about">
    <div class="container">
        <div class="title-wrapper">
            <h2 class="section-title">About Fellow Barber Express</h2>
        </div>
        <div class="about-content">
            <div class="about-text">
                <p>Fellow Barber Express brings fast, high-quality barbering to Adelaide. No fuss, no wait — just sharp cuts and even sharper service. Our experienced barbers specialize in modern and classic styles, from fades to scissor cuts, beard sculpting, and straight razor shaves.</p>
                <p>We keep it efficient so you get a great look without wasting your day. Walk into our welcoming shop and leave feeling refreshed and confident.</p>
                <div class="about-highlight">
                    ⚡ Express service • 🧼 Hot towels • 🍺 Complimentary drink • 📍 Central Adelaide
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Hours & Location -->
<section id="hours">
    <div class="container">
        <div class="title-wrapper">
            <h2 class="section-title">Hours & Location</h2>
        </div>
        <div class="info-grid">
            <div class="info-card">
                <h3>🕒 Opening Hours</h3>
                <div class="hours-list">
                    <p><strong>Tuesday - Friday:</strong> 9:00 AM – 7:00 PM</p>
                    <p><strong>Saturday:</strong> 9:00 AM – 5:00 PM</p>
                    <p><strong>Sunday:</strong> 10:00 AM – 4:00 PM</p>
                    <p><strong>Monday:</strong> Closed</p>
                </div>
            </div>
            <div class="info-card">
                <h3>📍 Find Us</h3>
                <p><strong>Fellow Barber Express</strong><br>
                123 Rundle Street, Adelaide SA 5000</p>
                <div class="map-placeholder">
                    📍 Google Map — (easily add your exact pin later)
                </div>
                <p style="margin-top: 0.8rem;">📞 <a href="tel:+61812345678" style="color:#d4af37;">(08) 1234 5678</a></p>
            </div>
        </div>
    </div>
</section>

<!-- Contact & Booking -->
<section id="contact">
    <div class="container">
        <div class="title-wrapper">
            <h2 class="section-title">Book or Ask a Question</h2>
        </div>
        <div class="info-grid">
            <div class="info-card">
                <h3>📧 Send a Message</h3>
                <form class="contact-form" id="contactForm">
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Email Address" required>
                    <input type="tel" placeholder="Phone Number">
                    <textarea rows="3" placeholder="Preferred date/time or question..."></textarea>
                    <button type="submit" class="btn-submit">✉️ Send Request</button>
                </form>
                <p style="font-size: 0.8rem; margin-top: 0.8rem;">We’ll reply within a few hours.</p>
            </div>
            <div class="info-card">
                <h3>⚡ Walk-ins Welcome</h3>
                <p>Prefer to just show up? We always keep chairs open for express cuts.</p>
                <p><strong>Call ahead to check wait times:</strong><br>
                <a href="tel:+61812345678" class="btn-call" style="display: inline-block; margin-top: 0.5rem;">📞 Call Shop</a></p>
                <hr style="margin: 1rem 0;">
                <h3>📱 Follow Us</h3>
                <div class="social-links">
                    <a href="#">Instagram</a> | 
                    <a href="#">Facebook</a> | 
                    <a href="#">TikTok</a>
                </div>
            </div>
        </div>
    </div>
</section>

<footer>
    <p>© 2026 Fellow Barber Express — Adelaide’s go-to for sharp, fast barbering.</p>
    <p style="margin-top: 0.5rem;">✂️ Walk-ins | Book online | Gift cards coming soon</p>
</footer>

<script>
    // Simple form alert
    document.getElementById('contactForm').addEventListener('submit', function(e) {
        e.preventDefault();
        alert('Thanks for reaching out! We’ll get back to you shortly. ✂️\n(To actually receive messages, connect a free form backend later.)');
        this.reset();
    });
</script>

</body>
</html>
