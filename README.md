<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kgosi Tech CCTV & Corporate Solutions | Safe, Secure & Compliant</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #0b2545;
            --secondary-color: #134074;
            --accent-color: #00b4d8;
            --light-bg: #eef4f8;
            --dark-text: #1d2d44;
            --white: #ffffff;
            --price-tag: #cc0000;
            --whatsapp-green: #25d366;
            --facebook-blue: #1877f2;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-bg);
            color: var(--dark-text);
            line-height: 1.6;
        }

        /* Header & Navigation */
        header {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 1rem 5%;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-graphics {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            border: 2px solid var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 10px rgba(0,180,216,0.6);
            overflow: hidden;
            background-color: #081b33;
        }

        .logo-graphics img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .logo-text h1 {
            font-size: 1.5rem;
            letter-spacing: 1px;
            font-weight: 800;
        }
        
        .logo-text span {
            color: var(--accent-color);
            font-size: 0.8rem;
            display: block;
            margin-top: -4px;
            font-weight: 600;
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(11, 37, 69, 0.85), rgba(19, 64, 116, 0.9)), url('https://images.unsplash.com/photo-1557597774-9d273605dfa9?auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
            color: var(--white);
            padding: 6rem 5%;
            text-align: center;
        }

        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem auto;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            background-color: var(--accent-color);
            color: var(--white);
            padding: 0.75rem 2rem;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
            display: inline-block;
        }

        .btn:hover {
            background-color: #0096c7;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: transparent;
            border: 2px solid var(--white);
        }

        .btn-secondary:hover {
            background-color: var(--white);
            color: var(--primary-color);
        }

        /* Sections */
        .section {
            padding: 5rem 5%;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 1rem;
            position: relative;
            color: var(--primary-color);
        }

        .section-subtitle {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--secondary-color);
            font-size: 1.1rem;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background-color: var(--accent-color);
            margin: 10px auto 0 auto;
            border-radius: 2px;
        }

        /* Grid Layouts */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .card {
            background-color: var(--white);
            padding: 2.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border-top: 5px solid var(--secondary-color);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            margin-bottom: 1rem;
            color: var(--secondary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card i {
            color: var(--accent-color);
        }

        /* Apparel Section Styles */
        .apparel-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .apparel-card {
            background-color: var(--white);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 6px 18px rgba(0,0,0,0.06);
            display: flex;
            flex-direction: column;
            position: relative;
            transition: transform 0.3s ease;
        }

        .apparel-card:hover {
            transform: translateY(-8px);
        }

        .apparel-img-box {
            width: 100%;
            height: 300px;
            background-color: #f7f9fa;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .apparel-img-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .apparel-card:hover .apparel-img-box img {
            transform: scale(1.05);
        }

        .apparel-info {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            text-align: center;
        }

        .apparel-info h3 {
            font-size: 1.25rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .apparel-price {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        .badge-soon {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: var(--price-tag);
            color: var(--white);
            padding: 0.3rem 0.8rem;
            font-weight: bold;
            font-size: 0.75rem;
            border-radius: 20px;
            text-transform: uppercase;
            z-index: 5;
        }

        /* Founder Section Styling */
        .founder-section {
            background-color: var(--white);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .founder-card {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            width: 100%;
            max-width: 500px;
            background: var(--light-bg);
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.06);
            border-bottom: 5px solid var(--accent-color);
        }

        .founder-img-container {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            overflow: hidden;
            border: 4px solid var(--primary-color);
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
            background-color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .founder-img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Pricing & Services Section */
        .pricing {
            background-color: #e2ebf0;
        }

        .price-card {
            background: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.08);
            text-align: center;
            display: flex;
            flex-direction: column;
            transition: transform 0.3s;
            position: relative;
        }

        .price-card:hover {
            transform: scale(1.03);
        }

        .price-header {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 2rem 1rem;
        }

        .price-header h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }

        .price-tag {
            background-color: var(--price-tag);
            color: var(--white);
            font-size: 1.8rem;
            font-weight: bold;
            padding: 0.5rem;
            display: inline-block;
            width: 100%;
        }

        .price-features {
            list-style: none;
            padding: 2rem 1.5rem;
            flex-grow: 1;
            text-align: left;
        }

        .price-features li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
            font-size: 0.95rem;
        }

        .price-features li::before {
            content: "✓";
            color: green;
            font-weight: bold;
            margin-right: 10px;
        }

        .badge {
            background-color: #2a9d8f;
            color: white;
            padding: 0.2rem 0.6rem;
            font-size: 0.8rem;
            border-radius: 20px;
            position: absolute;
            top: 15px;
            right: 15px;
            z-index: 10;
        }

        /* Booking Form */
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            background: var(--white);
            padding: 2.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05)
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
        }

        /* Social Quick Channels Bar */
        .social-quick-bar {
            background-color: #081b33;
            padding: 1.5rem 5%;
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .social-link-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: var(--white);
            text-decoration: none;
            font-weight: bold;
            padding: 0.6rem 1.5rem;
            border-radius: 30px;
            transition: background 0.3s, transform 0.2s;
        }

        .social-link-btn.wa { background-color: var(--whatsapp-green); }
        .social-link-btn.fb { background-color: var(--facebook-blue); }

        .social-link-btn:hover {
            transform: translateY(-2px);
            filter: brightness(1.1);
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: var(--white);
            text-align: center;
            padding: 2.5rem 5%;
        }

        .footer-info {
            margin-top: 1.5rem;
            font-size: 0.9rem;
            color: #b3c5d7;
            line-height: 1.8;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            nav {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--primary-color);
                box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            }

            nav.active {
                display: block;
            }

            nav ul {
                flex-direction: column;
                padding: 1.5rem 5%;
                gap: 15px;
            }

            .hero h2 { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="nav-container">
            <div class="logo-area">
                <div class="logo-graphics">
                    <!-- Your main company logo -->
                    <img src="https://i.ibb.co/gM87GLTs/IMG-20250212-WA0001.jpg" alt="Kgosi Tech Logo">
                </div>
                <div class="logo-text">
                    <h1>KGOSI TECH</h1>
                    <span>SECURITY & BUSINESS SOLUTIONS</span>
                </div>
            </div>
            <button class="menu-toggle" id="menuToggle" aria-label="Toggle Navigation">
                <i class="fa-solid fa-bars"></i>
            </button>
            <nav id="navMenu">
                <ul>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#services">Core Offerings</a></li>
                    <li><a href="#packages">CCTV Packages</a></li>
                    <li><a href="#apparel">Apparel Gear</a></li>
                    <li><a href="#corporate">Corporate & IT</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <h2>Your "One-Stop-Shop" for Security & Business Growth</h2>
        <p>Bridging the gap between essential physical security and foundational business administration. We secure your property and formalize your business across Barkly West and the broader Northern Cape.</p>
        <div class="hero-buttons">
            <a href="#packages" class="btn">CCTV Packages</a>
            <a href="#apparel" class="btn btn-secondary">Explore Apparel</a>
        </div>
    </section>

    <section id="about" class="section">
        <h2 class="section-title">Who We Are</h2>
        <p class="section-subtitle">Building safer communities and compliant enterprises in Barkly West and Mataleng.</p>
        <div class="grid-3">
            <div class="card">
                <h3><i class="fa-solid fa-crosshairs"></i> Our Mission</h3>
                <p>To provide peace of mind by securing businesses and homes with cutting-edge surveillance technology, ensuring protection for both property and people.</p>
            </div>
            <div class="card">
                <h3><i class="fa-solid fa-eye"></i> Our Vision</h3>
                <p>To create a safer world where technology empowers communities and businesses to operate with confidence and without fear.</p>
            </div>
            <div class="card">
                <h3><i class="fa-solid fa-key"></i> Keys to Success</h3>
                <p><strong>The One-Stop Advantage:</strong> Combining security installations with corporate administrative services makes us a highly convenient partner for new and local business owners.</p>
            </div>
        </div>
    </section>

    <section id="services" class="section" style="background-color: var(--white);">
        <h2 class="section-title">Core Business Divisions</h2>
        <p class="section-subtitle">Comprehensive support structured across three specialized pillars.</p>
        <div class="grid-3">
            <div class="card">
                <h3><i class="fa-solid fa-shield-halved"></i> Security Division</h3>
                <p>CCTV camera supply, installation, maintenance, and remote viewing setup.</p>
            </div>
            <div class="card">
                <h3><i class="fa-solid fa-briefcase"></i> Corporate Services</h3>
                <p>Navigating digital hurdles for local business owners. Direct support for CIPC company registrations, SARS tax compliance, annual return filings, and logo design.</p>
            </div>
            <div class="card">
                <h3><i class="fa-solid fa-laptop-code"></i> IT Support Division</h3>
                <p>Foundational technical architecture including continuous software updates, unique domain registration, secure email hosting, and general tech troubleshooting.</p>
            </div>
        </div>
    </section>

    <section id="founder" class="section founder-section">
        <h2 class="section-title">Leadership</h2>
        <p class="section-subtitle">The driving force behind Kgosi Tech.</p>
        <div class="founder-card">
            <div class="founder-img-container">
                <!-- Corrected Portrait of Bakang Kgosi -->
                <img src="https://i.imgur.com/TshufJO.jpeg" alt="Bakang Kgosi">
            </div>
            <h3>Bakang Kgosi</h3>
            <div class="founder-title">Founder of Kgosi Tech</div>
            <p>Committed to making professional security, modern technology networks, and regulatory compliance services highly accessible, reliable, and affordable for our local community.</p>
        </div>
    </section>

    <section id="packages" class="section pricing">
        <h2 class="section-title">Hikvision 1080P 2MP HD CCTV Packages</h2>
        <p class="section-subtitle">HIGH DEFINITION • RELIABLE • SECURE • 1 YEAR WARRANTY INCLUDED</p>
        
        <div class="grid-3">
            <div class="price-card">
                <div class="price-header">
                    <h3>4 CHANNEL SYSTEM</h3>
                </div>
                <div class="price-tag">R6 500</div>
                <ul class="price-features">
                    <li>4 Channel Hikvision DVR</li>
                    <li>4 x Hikvision 2MP HD Cameras</li>
                    <li>500GB Dedicated Surveillance Hard Drive</li>
                    <li>Cabling, Trunking & Connectors</li>
                    <li>Professional Installation & Remote Viewing Mobile Setup</li>
                </ul>
                <div style="padding: 1.5rem;"><button class="btn" onclick="selectPackage('4 Channel System (R6 500)')">Book Install</button></div>
            </div>

            <div class="price-card">
                <span class="badge">Popular</span>
                <div class="price-header">
                    <h3>8 CHANNEL SYSTEM</h3>
                </div>
                <div class="price-tag">R8 500</div>
                <ul class="price-features">
                    <li>8 Channel Hikvision DVR</li>
                    <li>8 x Hikvision 2MP HD Cameras</li>
                    <li>1TB Dedicated Surveillance Hard Drive</li>
                    <li>Cabling, Trunking & Connectors</li>
                    <li>Professional Installation & Remote Viewing Mobile Setup</li>
                </ul>
                <div style="padding: 1.5rem;"><button class="btn" onclick="selectPackage('8 Channel System (R8 500)')">Book Install</button></div>
            </div>

            <div class="price-card">
                <div class="price-header">
                    <h3>16 CHANNEL SYSTEM</h3>
                </div>
                <div class="price-tag">R14 500</div>
                <ul class="price-features">
                    <li>16 Channel Hikvision DVR</li>
                    <li>16 x Hikvision 2MP HD Cameras</li>
                    <li>2TB Dedicated Surveillance Hard Drive</li>
                    <li>Cabling, Trunking & Connectors</li>
                    <li>Professional Installation & Remote Viewing Mobile Setup</li>
                </ul>
                <div style="padding: 1.5rem;"><button class="btn" onclick="selectPackage('16 Channel System (R14 500)')">Book Install</button></div>
            </div>
        </div>
    </section>

    <section id="apparel" class="section" style="background-color: var(--white);">
        <h2 class="section-title">Official Kgosi Tech Apparel</h2>
        <p class="section-subtitle">Gear up for the season! Secure your premium branded summer drop today.</p>
        
        <div class="apparel-grid">
            <div class="apparel-card">
                <span class="badge-soon">Summer Pre-Order</span>
                <div class="apparel-img-box">
                    <!-- Premium Red Cap with company logo -->
                    <img src="https://i.imgur.com/8J31q1J.jpeg" alt="Kgosi Tech Red Cap with Logo">
                </div>
                <div class="apparel-info">
                    <div>
                        <h3>Premium Snapback - Fire Red</h3>
                        <p style="color: #666; font-size: 0.9rem; margin-bottom: 0.5rem;">Official branded wear with premium cyan front logo embroidery.</p>
                    </div>
                    <div class="apparel-price">R250</div>
                    <button class="btn" onclick="selectPackage('Apparel - Premium Red Cap (R250)')">Pre-Order Cap</button>
                </div>
            </div>

            <div class="apparel-card">
                <span class="badge-soon">Summer Pre-Order</span>
                <div class="apparel-img-box">
                    <!-- Premium Black Cap with company logo -->
                    <img src="https://i.imgur.com/kr2qeyV.jpeg" alt="Kgosi Tech Black Cap with Logo">
                </div>
                <div class="apparel-info">
                    <div>
                        <h3>Premium Snapback - Stealth Black</h3>
                        <p style="color: #666; font-size: 0.9rem; margin-bottom: 0.5rem;">Stealth black aesthetic featuring official circular embroidery logo.</p>
                    </div>
                    <div class="apparel-price">R250</div>
                    <button class="btn" onclick="selectPackage('Apparel - Premium Black Cap (R250)')">Pre-Order Cap</button>
                </div>
            </div>

            <div class="apparel-card">
                <span class="badge-soon">Coming Soon</span>
                <div class="apparel-img-box">
                    <!-- Updated with official Kgosi Tech Golf Shirt picture -->
                    <img src="https://i.imgur.com/lnUAbL3.png" alt="Kgosi Tech Golf Shirt">
                </div>
                <div class="apparel-info">
                    <div>
                        <h3>Kgosi Tech Golf T-Shirt</h3>
                        <p style="color: #666; font-size: 0.9rem; margin-bottom: 0.5rem;">Premium smart-casual branded golf shirt. Drops soon!</p>
                    </div>
                    <div class="apparel-price">R300</div>
                    <button class="btn btn-secondary" style="border-color: var(--accent-color); color: var(--accent-color);" onclick="selectPackage('Apparel - Golf T-Shirt Waitlist')">Join Waitlist</button>
                </div>
            </div>
        </div>
    </section>

    <section id="corporate" class="section pricing">
        <h2 class="section-title">Corporate Services & Specialized Packages</h2>
        <p class="section-subtitle">Formalize your enterprise, unlock government tenders, and establish a digital identity.</p>
        
        <div class="grid-3">
            <div class="card" style="border-top-color: var(--accent-color);">
                <h3><i class="fa-solid fa-certificate"></i> Compliance Rates</h3>
                <p style="margin-bottom: 1rem; font-weight: bold; color: var(--primary-color);">Flat-rate service fees.</p>
                <ul style="list-style: none; padding-left: 0;">
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> CIPC New Registration</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> SARS Tax Compliance Verification</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> Annual Return Submissions</li>
                </ul>
                <div style="margin-top: 1.5rem;"><button class="btn" style="width:100%;" onclick="selectPackage('Corporate Compliance Filing')">Inquire Flat Rates</button></div>
            </div>

            <div class="card" style="border-top-color: #2a9d8f;">
                <span class="badge" style="background-color: #e76f51;">Best Value</span>
                <h3><i class="fa-solid fa-rocket"></i> Business Launch Deal</h3>
                <p style="margin-bottom: 1rem; font-weight: bold; color: var(--primary-color);">Everything needed to formalize your startup.</p>
                <ul style="list-style: none; padding-left: 0;">
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> CIPC Registration & Tax Number</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> Professional Business Logo Design</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> Custom Domain & Business Emails</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee; font-weight: bold; color: var(--accent-color);"><i class="fa-solid fa-gift"></i> CCTV System Discount Voucher</li>
                </ul>
                <div style="margin-top: 1.5rem;"><button class="btn" style="width:100%; background-color: #2a9d8f;" onclick="selectPackage('Business Launch Package')">Order Bundle</button></div>
            </div>

            <div class="card" style="border-top-color: var(--accent-color);">
                <h3><i class="fa-solid fa-network-wired"></i> IT Support Services</h3>
                <p style="margin-bottom: 1rem; font-weight: bold; color: var(--primary-color);">Hourly or fixed-rate fees.</p>
                <ul style="list-style: none; padding-left: 0;">
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> Operating System & Software Updates</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> Domain Hosting & Configuration</li>
                    <li style="padding: 0.4rem 0; border-bottom: 1px solid #eee;"><i class="fa-solid fa-check" style="color: green;"></i> General Technical Troubleshooting</li>
                </ul>
                <div style="margin-top: 1.5rem;"><button class="btn" style="width:100%;" onclick="selectPackage('IT Support Inquiry')">Request IT Support</button></div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <h2 class="section-title">Request a Quote or Pre-Order</h2>
        <p class="section-subtitle">Let us help you build a safe, compliant, and thriving business setup.</p>
        <div class="contact-container">
            <form id="bookingForm" action="https://api.web3forms.com/submit" method="POST">
                <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY_HERE">
                <input type="checkbox" name="botcheck" class="hidden" style="display: none;">

                <div class="form-group">
                    <label for="name">Your Name / Business Name</label>
                    <input type="text" name="name" id="name" required placeholder="Enter name">
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" name="phone" id="phone" required placeholder="e.g. 084 540 2663">
                </div>
                <div class="form-group">
                    <label for="package">Select Service / Package / Apparel</label>
                    <select name="package" id="package">
                        <option value="General Inquiry">General IT / Security Inquiry</option>
                        <option value="4 Channel System (R6 500)">4 Channel CCTV Installation - R6 500</option>
                        <option value="8 Channel System (R8 500)">8 Channel CCTV Installation - R8 500</option>
                        <option value="16 Channel System (R14 500)">16 Channel CCTV Installation - R14 500</option>
                        <option value="Apparel - Premium Red Cap (R250)">Apparel: Premium Red Cap - R250</option>
                        <option value="Apparel - Premium Black Cap (R250)">Apparel: Premium Black Cap - R250</option>
                        <option value="Apparel - Golf T-Shirt Waitlist">Apparel: Golf T-Shirt Waitlist - R300</option>
                        <option value="Corporate Compliance Filing">Corporate Service (CIPC, SARS Compliance, Returns)</option>
                        <option value="Business Launch Package">Business Launch Package Bundle Deal</option>
                        <option value="IT Support Inquiry">IT Technical Support / Email Hosting</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="message">Message Details</label>
                    <textarea name="message" id="message" rows="4" placeholder="Let us know your requirements, delivery location, or physical address..."></textarea>
                </div>
                <button type="submit" class="btn" style="width: 100%;">Submit Request</button>
            </form>
        </div>
    </section>

    <div class="social-quick-bar">
        <a href="https://wa.me/27845402663" target="_blank" class="social-link-btn wa">
            <i class="fa-brands fa-whatsapp" style="font-size: 1.3rem;"></i> WhatsApp Us: 084 540 2663
        </a>
        <a href="https://web.facebook.com/people/KGOSI-TECH-CCTV-SOLUTIONS/100095111956041/" target="_blank" class="social-link-btn fb">
            <i class="fa-brands fa-facebook" style="font-size: 1.3rem;"></i> Facebook: KGOSI TECH CCTV
        </a>
    </div>

    <footer>
        <p>&copy; 2026 Kgosi Tech. All Rights Reserved.</p>
        <p class="footer-info">Barkly West, Northern Cape, South Africa</p>
    </footer>

    <script>
        // Simple Navigation Toggle for Mobile
        const menuToggle = document.getElementById('menuToggle');
        const navMenu = document.getElementById('navMenu');
        
        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });

        // Autofill selected package function
        function selectPackage(packageName) {
            const packageSelect = document.getElementById('package');
            packageSelect.value = packageName;
            document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
        }
    </script>
</body>
</html>
