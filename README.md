<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phambili Services | Integrated Waste & Environmental Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
        }

        :root {
            --green-dark: #3a6b2b;
            --green-light: #7fa84a;
            --orange: #e07c2c;
            --gray-bg: #f5f5f5;
            --text-dark: #1e1e1e;
            --text-light: #ffffff;
            --black: #111;
            --white: #ffffff;
            --shadow: 0 8px 20px rgba(0,0,0,0.08);
        }

        body {
            background-color: #ffffff;
            color: var(--text-dark);
            line-height: 1.5;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* ----- HEADER / NAV ----- */
        header {
            background: white;
            padding: 18px 0;
            border-bottom: 1px solid #e0e0e0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 12px rgba(0,0,0,0.02);
        }

        .nav-wrap {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 16px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-icon {
            background: var(--orange);
            width: 42px;
            height: 42px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            font-weight: 700;
        }

        .logo-text {
            font-weight: 700;
            font-size: 1.4rem;
            line-height: 1.1;
            color: var(--green-dark);
        }

        .logo-text small {
            display: block;
            font-size: 0.65rem;
            font-weight: 400;
            letter-spacing: 1px;
            color: #555;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 28px;
            font-weight: 500;
            font-size: 0.95rem;
            color: #333;
            flex-wrap: wrap;
        }

        .nav-links a {
            text-decoration: none;
            color: inherit;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--orange);
        }

        .nav-links i {
            font-size: 0.75rem;
            margin-left: 4px;
            color: #888;
        }

        .btn-orange {
            background: var(--orange);
            border: none;
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: pointer;
            transition: background 0.2s;
            display: inline-block;
            text-decoration: none;
            text-align: center;
        }

        .btn-orange:hover {
            background: #c96a1e;
        }

        .btn-green {
            background: var(--green-light);
            border: none;
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: pointer;
            transition: background 0.2s;
            display: inline-block;
            text-decoration: none;
            text-align: center;
        }

        .btn-green:hover {
            background: #6b8f3e;
        }

        /* ----- HERO ----- */
        .hero {
            background: #1a1a1a;
            color: white;
            padding: 70px 0;
            position: relative;
            overflow: hidden;
        }

        .hero .container {
            position: relative;
            z-index: 2;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.4rem;
            font-weight: 800;
            line-height: 1.2;
            max-width: 900px;
            margin-bottom: 24px;
        }

        .hero p {
            max-width: 750px;
            font-size: 1.1rem;
            color: #ddd;
            margin-bottom: 36px;
        }

        .hero-buttons {
            display: flex;
            gap: 18px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #1f2a1c 0%, #2b3a26 100%);
            opacity: 0.9;
            z-index: 1;
        }

        /* ----- SECTION GENERIC ----- */
        section {
            padding: 70px 0;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--green-dark);
            margin-bottom: 16px;
        }

        .section-sub {
            color: #555;
            max-width: 700px;
            margin-bottom: 40px;
        }

        /* ----- WHY CHOOSE ----- */
        .why-grid {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 48px;
            align-items: center;
        }

        .why-text h2 {
            font-size: 2.4rem;
            font-weight: 700;
            color: var(--green-dark);
            line-height: 1.2;
            margin-bottom: 24px;
        }

        .why-text p {
            margin-bottom: 16px;
            color: #444;
            font-size: 1.05rem;
        }

        .why-img {
            background: #e0e0e0;
            border-radius: 24px;
            min-height: 340px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .why-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .quote-badge {
            background: var(--green-light);
            color: white;
            padding: 16px 28px;
            border-radius: 50px;
            display: inline-flex;
            align-items: center;
            gap: 14px;
            font-weight: 600;
            margin-top: 16px;
        }

        .quote-badge i {
            font-size: 28px;
            opacity: 0.9;
        }

        /* ----- SERVICE CARDS (3) ----- */
        .cards-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
            margin-top: 20px;
        }

        .service-card {
            background: #fafafa;
            border-radius: 20px;
            padding: 28px 24px;
            box-shadow: 0 4px 14px rgba(0,0,0,0.04);
            border: 1px solid #eee;
            transition: transform 0.2s;
        }

        .service-card:hover {
            transform: translateY(-4px);
        }

        .service-card h3 {
            font-size: 1.3rem;
            color: var(--green-dark);
            margin-bottom: 12px;
            font-weight: 700;
        }

        .service-card p {
            color: #555;
            font-size: 0.95rem;
            margin-bottom: 18px;
        }

        .service-card .read-more {
            color: var(--orange);
            font-weight: 600;
            text-decoration: none;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .service-card .read-more:hover {
            text-decoration: underline;
        }

        /* ----- MISSION / VISION ----- */
        .mission-grid {
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 48px;
            align-items: center;
        }

        .mission-text h2 {
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--green-dark);
            line-height: 1.2;
            margin-bottom: 24px;
        }

        .mission-tabs {
            display: flex;
            gap: 32px;
            border-bottom: 2px solid #ddd;
            padding-bottom: 12px;
            margin-bottom: 24px;
        }

        .mission-tabs span {
            font-weight: 600;
            color: #888;
            cursor: default;
            padding-bottom: 8px;
        }

        .mission-tabs .active {
            color: var(--green-dark);
            border-bottom: 3px solid var(--orange);
        }

        .mission-text p {
            color: #444;
            font-size: 1.05rem;
        }

        .mission-img {
            background: #d4e0c8;
            border-radius: 24px;
            min-height: 280px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .mission-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* ----- CTA / STATS ----- */
        .stats-cta {
            background: #1a1a1a;
            color: white;
            padding: 60px 0;
            border-radius: 0;
        }

        .stats-cta .container {
            display: flex;
            flex-direction: column;
            gap: 48px;
        }

        .stats-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 24px;
        }

        .stats-top h2 {
            font-size: 2.2rem;
            font-weight: 700;
            max-width: 600px;
            line-height: 1.3;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 32px;
            text-align: center;
        }

        .stat-item .number {
            font-size: 2.8rem;
            font-weight: 800;
            color: var(--orange);
            line-height: 1.1;
        }

        .stat-item .label {
            font-size: 1rem;
            font-weight: 500;
            color: #ccc;
            margin-top: 6px;
        }

        /* ----- INDUSTRIES / WE SERVE ----- */
        .industries {
            background: #f0f4ea;
        }

        .industries h2 {
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--green-dark);
            text-align: center;
            margin-bottom: 16px;
        }

        .industry-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 24px;
            margin-top: 40px;
        }

        .industry-card {
            background: white;
            padding: 28px 20px;
            border-radius: 16px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
            border-left: 5px solid var(--green-light);
            transition: 0.2s;
        }

        .industry-card:hover {
            border-left-color: var(--orange);
            box-shadow: 0 8px 20px rgba(0,0,0,0.06);
        }

        .industry-card .num {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--green-light);
            display: block;
            margin-bottom: 10px;
        }

        .industry-card h3 {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--green-dark);
            margin-bottom: 8px;
        }

        .industry-card p {
            font-size: 0.9rem;
            color: #666;
        }

        /* ----- BOTTOM CTA ----- */
        .bottom-cta {
            background: #1e1e1e;
            color: white;
            padding: 70px 0;
            text-align: center;
        }

        .bottom-cta p {
            max-width: 800px;
            margin: 0 auto 32px;
            font-size: 1.25rem;
            color: #ddd;
        }

        /* ----- FOOTER ----- */
        footer {
            background: var(--green-dark);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.2fr 1fr 1fr 1.2fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            font-size: 1.1rem;
            margin-bottom: 20px;
            font-weight: 600;
            color: #f0f0f0;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 10px;
            font-size: 0.9rem;
            color: #cbdbb5;
        }

        .footer-col ul li i {
            margin-right: 10px;
            color: var(--orange);
            width: 18px;
        }

        .footer-logo {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 18px;
        }

        .footer-logo .logo-icon {
            background: var(--orange);
            width: 48px;
            height: 48px;
            border-radius: 12px;
            font-size: 26px;
        }

        .footer-logo span {
            font-weight: 700;
            font-size: 1.4rem;
            line-height: 1.2;
        }

        .footer-logo small {
            display: block;
            font-size: 0.7rem;
            font-weight: 400;
            opacity: 0.8;
        }

        .subscribe-form {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .subscribe-form input {
            padding: 12px 16px;
            border-radius: 8px;
            border: none;
            background: #f0f0f0;
            font-size: 0.9rem;
        }

        .subscribe-form button {
            background: var(--orange);
            border: none;
            padding: 12px;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
        }

        .subscribe-form button:hover {
            background: #c96a1e;
        }

        .copyright {
            border-top: 1px solid rgba(255,255,255,0.15);
            padding-top: 24px;
            text-align: center;
            font-size: 0.85rem;
            color: #b0c99e;
        }

        /* ----- RESPONSIVE ----- */
        @media (max-width: 1024px) {
            .hero h1 { font-size: 2.6rem; }
            .why-grid { grid-template-columns: 1fr; }
            .cards-3 { grid-template-columns: repeat(2, 1fr); }
            .mission-grid { grid-template-columns: 1fr; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); }
            .industry-grid { grid-template-columns: repeat(2, 1fr); }
            .footer-grid { grid-template-columns: 1fr 1fr; }
        }

        @media (max-width: 768px) {
            .nav-wrap { flex-direction: column; align-items: stretch; }
            .nav-links { justify-content: center; gap: 16px; }
            .hero h1 { font-size: 2rem; }
            .cards-3 { grid-template-columns: 1fr; }
            .stats-grid { grid-template-columns: 1fr; }
            .industry-grid { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr; }
            .stats-top { flex-direction: column; text-align: center; }
            .stats-top h2 { font-size: 1.8rem; }
            .btn-orange, .btn-green { width: 100%; }
            .hero-buttons { flex-direction: column; width: 100%; }
            .mission-tabs { gap: 16px; }
        }

        /* ----- UTILITY ----- */
        .text-center { text-align: center; }
        .mt-2 { margin-top: 16px; }
        .mb-2 { margin-bottom: 16px; }
        .flex-center { display: flex; align-items: center; justify-content: center; }
        .gap-2 { gap: 16px; }
    </style>
</head>
<body>

<!-- ===== HEADER ===== -->
<header>
    <div class="container nav-wrap">
        <div class="logo">
            <div class="logo-icon"><i class="fas fa-recycle"></i></div>
            <div class="logo-text">PHAMBILI <small>SERVICES (PTY) LTD</small></div>
        </div>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">About Us</a>
            <a href="#">Industries <i class="fas fa-chevron-down"></i></a>
            <a href="#">Solutions <i class="fas fa-chevron-down"></i></a>
            <a href="#">Projects & Insights <i class="fas fa-chevron-down"></i></a>
            <a href="#">Contact Us</a>
        </div>
        <a href="#" class="btn-orange">Request a Site Assessment</a>
    </div>
</header>

<!-- ===== HERO ===== -->
<section class="hero">
    <div class="hero-bg"></div>
    <div class="container">
        <h1>Integrated Waste, Recovery & Environmental Solutions.</h1>
        <p>Phambili Services helps mining, Industrial, Commercial Property, and Public-Sector Clients manage waste more efficiently, improve compliance, increase recovery, and build practical circular-economy outcomes.</p>
        <div class="hero-buttons">
            <a href="#" class="btn-orange">Request a Site Assessment</a>
            <a href="#" class="btn-green">More About Us</a>
        </div>
    </div>
</section>

<!-- ===== WHY CHOOSE ===== -->
<section>
    <div class="container why-grid">
        <div class="why-text">
            <h2>Why Leading Operators Choose Phambili</h2>
            <p>We combine operational reliability and safety-first delivery, with a deep understanding of your needs and the changing environment.</p>
            <p>Our approach is built for clean, auditable reporting – the kind that's a compliance asset, not a liability.</p>
            <p>Safety is central to how we operate. From hazardous waste transport to general operations, we meet the highest standards because the wellbeing of our teams and the communities we work in matters.</p>
            <p>We also take our environmental responsibilities seriously. Beyond compliance, we drive local initiatives and sustainable practices where we operate.</p>
            <p>Phambili Services is a South African services company focused on delivering waste and recovery solutions built for the realities of our customers – cost pressures, compliance, continuity, and the growing need for circularity.</p>
            <div class="quote-badge">
                <i class="fas fa-quote-left"></i> Cleaning the environment, creating value.
            </div>
        </div>
        <div class="why-img">
            <img src="https://images.unsplash.com/photo-1532996122724-e3c354a0b15b?w=800&h=600&fit=crop&crop=center" alt="Waste management truck">
        </div>
    </div>
</section>

<!-- ===== SERVICE CARDS (3) ===== -->
<section style="padding-top: 0;">
    <div class="container cards-3">
        <div class="service-card">
            <h3>Integrated Waste Management</h3>
            <p>We manage the full operational cycle: collection, transport, site handling, skip and bin solutions, and downstream management.</p>
            <a href="#" class="read-more">Read More <i class="fas fa-arrow-right"></i></a>
        </div>
        <div class="service-card">
            <h3>Recycling & Recovery</h3>
            <p>From source separation to clean and dirty recycling systems, we help you recover more and send less to landfill.</p>
            <a href="#" class="read-more">Read More <i class="fas fa-arrow-right"></i></a>
        </div>
        <div class="service-card">
            <h3>Compliance, Advisory & Training</h3>
            <p>Regulatory pressure doesn't ease up, and neither do we. We provide waste planning support, reporting inputs, and audit-readiness.</p>
            <a href="#" class="read-more">Read More <i class="fas fa-arrow-right"></i></a>
        </div>
    </div>
</section>

<!-- ===== MISSION / VISION ===== -->
<section style="background: #f9f9f9;">
    <div class="container mission-grid">
        <div class="mission-text">
            <h2>We handle Complexities, So You Can Drive Growth.</h2>
            <div class="mission-tabs">
                <span class="active">Our Mission</span>
                <span>Vision</span>
            </div>
            <p>To deliver integrated, compliant, and sustainable waste management solutions that protect people, planet, and productivity. We aim to be the partner of choice for businesses and municipalities that value reliability, transparency, and environmental stewardship.</p>
        </div>
        <div class="mission-img">
            <img src="https://images.unsplash.com/photo-1542601906990-b4d3fb778b09?w=800&h=500&fit=crop&crop=center" alt="Community clean up">
        </div>
    </div>
</section>

<!-- ===== STATS / CTA ===== -->
<section class="stats-cta">
    <div class="container">
        <div class="stats-top">
            <h2>Our Solutions are customised to satisfy client needs.</h2>
            <a href="#" class="btn-orange">Contact us</a>
        </div>
        <div class="stats-grid">
            <div class="stat-item">
                <div class="number">1999</div>
                <div class="label">Year Established</div>
            </div>
            <div class="stat-item">
                <div class="number">2001</div>
                <div class="label">Service Pillars</div>
            </div>
            <div class="stat-item">
                <div class="number">2001</div>
                <div class="label">Compliance Status</div>
            </div>
            <div class="stat-item">
                <div class="number">2001</div>
                <div class="label">Projects</div>
            </div>
        </div>
    </div>
</section>

<!-- ===== INDUSTRIES ===== -->
<section class="industries">
    <div class="container">
        <h2>Industries We Serve</h2>
        <div class="industry-grid">
            <div class="industry-card">
                <span class="num">01.</span>
                <h3>Mining</h3>
                <p>Powering Operations, Protecting the Land</p>
            </div>
            <div class="industry-card">
                <span class="num">02.</span>
                <h3>Industrial & Manufacturing</h3>
                <p>Keeping Production Moving, Responsibly</p>
            </div>
            <div class="industry-card">
                <span class="num">03.</span>
                <h3>Commercial Property & Retail</h3>
                <p>Clean Spaces. Quiet Service.</p>
            </div>
            <div class="industry-card">
                <span class="num">04.</span>
                <h3>Municipal & Community Projects</h3>
                <p>Cleaner Communities, Together.</p>
            </div>
        </div>
    </div>
</section>

<!-- ===== BOTTOM CTA ===== -->
<section class="bottom-cta">
    <div class="container">
        <p>Whether you need day-to-day waste services, improved recycling, compliance support, or design and build of larger recovery infrastructure, Phambili is ready to engage.</p>
        <a href="#" class="btn-orange">Contact us</a>
    </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
    <div class="container">
        <div class="footer-grid">
            <div class="footer-col">
                <div class="footer-logo">
                    <div class="logo-icon"><i class="fas fa-recycle"></i></div>
                    <span>PHAMBILI <small>SERVICES (PTY) LTD</small></span>
                </div>
                <p style="font-size: 0.9rem; color: #cbdbb5; margin-top: 12px;">Integrated waste, recovery & environmental solutions for South Africa.</p>
            </div>
            <div class="footer-col">
                <h4>Solutions</h4>
                <ul>
                    <li><i class="fas fa-chevron-right"></i> Integrated Waste Management</li>
                    <li><i class="fas fa-chevron-right"></i> Recycling & Recovery</li>
                    <li><i class="fas fa-chevron-right"></i> Compliance, Advisory & Training</li>
                    <li><i class="fas fa-chevron-right"></i> Infrastructure & Projects</li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Contacts</h4>
                <ul>
                    <li><i class="fas fa-map-marker-alt"></i> 42 Baksteen Road, Clayville, JHB</li>
                    <li><i class="fas fa-envelope"></i> info@phambiliservices.co.za</li>
                    <li><i class="fas fa-phone-alt"></i> 010 448 1488</li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Subscribe</h4>
                <p style="font-size: 0.9rem; color: #cbdbb5; margin-bottom: 12px;">Get updates to news & events</p>
                <div class="subscribe-form">
                    <input type="email" placeholder="Your Email Address">
                    <button type="submit">Subscribe</button>
                </div>
            </div>
        </div>
        <div class="copyright">
            ©Copy Right 2026. All Rights Reserved
        </div>
    </div>
</footer>

</body>
</html>
