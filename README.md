<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>لالیگا اسپانیا | LaLiga EA Sports</title>
    <meta name="description" content="وب‌سایت رسمی لالیگا اسپانیا - اطلاعات کامل تیم‌ها، جدول رده‌بندی، آمار و تاریخچه">
    
    <!-- Fonts & Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #DC143C;
            --secondary: #FFD700;
            --dark: #0A0A0A;
            --light: #F8F9FA;
            --gradient: linear-gradient(135deg, #DC143C 0%, #8B0000 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Tajawal', sans-serif;
            background: var(--light);
            color: var(--dark);
            overflow-x: hidden;
        }
        
        /* Header */
        header {
            background: var(--gradient);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }
        
        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 900;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-menu a {
            color: white;
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }
        
        .nav-menu a:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }
        
        /* Mobile Menu */
        .mobile-menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Main Content */
        main {
            margin-top: 80px;
        }
        
        /* Hero Section */
        .hero {
            background: var(--gradient);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="rgba(255,255,255,0.1)"/></svg>') repeat;
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% { transform: translate(0,0) rotate(0deg); }
            100% { transform: translate(-50px, -50px) rotate(360deg); }
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background: var(--secondary);
            color: var(--dark);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(255,215,0,0.4);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255,215,0,0.6);
        }
        
        /* Section Styles */
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }
        
        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }
        
        .stat-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 900;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: #666;
            font-weight: 700;
        }
        
        /* Teams Grid */
        .teams-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .team-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .team-card:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        
        .team-header {
            background: var(--gradient);
            color: white;
            padding: 1.5rem;
            text-align: center;
        }
        
        .team-logo {
            width: 80px;
            height: 80px;
            background: white;
            border-radius: 50%;
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: 900;
            color: var(--primary);
        }
        
        .team-info {
            padding: 1.5rem;
        }
        
        .team-stats {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            text-align: center;
        }
        
        .team-stat {
            flex: 1;
        }
        
        .team-stat-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .team-stat-label {
            font-size: 0.9rem;
            color: #666;
        }
        
        /* Table Styles */
        .league-table {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            margin-bottom: 3rem;
        }
        
        .table-header {
            background: var(--gradient);
            color: white;
            padding: 1.5rem;
            text-align: center;
            font-size: 1.3rem;
            font-weight: 700;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        th {
            background: #f8f9fa;
            padding: 1rem;
            text-align: center;
            font-weight: 700;
            color: var(--primary);
            border-bottom: 2px solid #e0e0e0;
        }
        
        td {
            padding: 1rem;
            text-align: center;
            border-bottom: 1px solid #eee;
        }
        
        tr:hover {
            background: #f8f9fa;
        }
        
        .team-name {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-weight: 600;
        }
        
        .position {
            font-weight: 900;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .position.gold { background: gold; color: #000; }
        .position.silver { background: silver; color: #000; }
        .position.bronze { background: #cd7f32; color: #fff; }
        .position.top4 { background: #3f51b5; color: #fff; }
        .position.top6 { background: #009688; color: #fff; }
        .position.relegation { background: #f44336; color: #fff; }
        
        /* Champions Section */
        .champions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .champion-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }
        
        .champion-card:hover {
            transform: translateY(-5px);
        }
        
        .champion-logo {
            width: 100px;
            height: 100px;
            background: var(--gradient);
            border-radius: 50%;
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2.5rem;
            font-weight: 900;
        }
        
        .champion-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .champion-count {
            font-size: 3rem;
            font-weight: 900;
            color: var(--secondary);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .social-links {
            margin: 2rem 0;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--secondary);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background: var(--gradient);
                width: 100%;
                text-align: center;
                transition: 0.3s;
                padding: 2rem 0;
            }
            
            .nav-menu.active {
                left: 0;
            }
            
            .mobile-menu-toggle {
                display: block;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .stat-number {
                font-size: 2rem;
            }
        }
        
        /* Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 0.8s ease forwards;
        }
        
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <a href="#" class="logo">
                <i class="fas fa-futbol"></i>
                <span>لالیگا</span>
            </a>
            <ul class="nav-menu">
                <li><a href="#home"><i class="fas fa-home"></i> خانه</a></li>
                <li><a href="#teams"><i class="fas fa-shield-alt"></i> تیم‌ها</a></li>
                <li><a href="#table"><i class="fas fa-table"></i> جدول</a></li>
                <li><a href="#stats"><i class="fas fa-chart-bar"></i> آمار</a></li>
                <li><a href="#history"><i class="fas fa-history"></i> تاریخچه</a></li>
            </ul>
            <button class="mobile-menu-toggle" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </nav>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="home" class="hero">
            <div class="hero-content fade-in">
                <h1>لالیگا EA اسپورتس 2025-26</h1>
                <p>معتبرترین لیگ فوتبال اسپانیا و یکی از برترین لیگ‌های جهان</p>
                <a href="#teams" class="cta-button">مشاهده تیم‌ها</a>
            </div>
        </section>

        <!-- Stats Section -->
        <section id="stats">
            <h2 class="section-title fade-in">آمار کلیدی لالیگا</h2>
            <div class="stats-grid fade-in">
                <div class="stat-card">
                    <div class="stat-number">95</div>
                    <div class="stat-label">فصل برگزار شده</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">20</div>
                    <div class="stat-label">تیم حاضر در لیگ</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">36</div>
                    <div class="stat-label">قهرمانی رئال مادرید</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">28</div>
                    <div class="stat-label">قهرمانی بارسلونا</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">474</div>
                    <div class="stat-label">گل مسی (رکورددار)</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">622</div>
                    <div class="stat-label">بازی ژاکین (رکورددار)</div>
                </div>
            </div>
        </section>

        <!-- Teams Section -->
        <section id="teams">
            <h2 class="section-title fade-in">تیم‌های حاضر در فصل 2025-26</h2>
            <div class="teams-grid">
                <!-- Real Madrid -->
                <div class="team-card fade-in">
                    <div class="team-header">
                        <div class="team-logo">RM</div>
                        <h3>رئال مادرید</h3>
                        <p>Real Madrid CF</p>
                    </div>
                    <div class="team-info">
                        <div class="team-stats">
                            <div class="team-stat">
                                <div class="team-stat-value">36</div>
                                <div class="team-stat-label">قهرمانی</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">95</div>
                                <div class="team-stat-label">فصل حضور</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">84,000</div>
                                <div class="team-stat-label">ظرفیت ورزشگاه</div>
                            </div>
                        </div>
                        <p style="margin-top: 1rem; color: #666;">
                            <i class="fas fa-map-marker-alt"></i> مادرید - سانتیاگو برنابئو
                        </p>
                    </div>
                </div>

                <!-- Barcelona -->
                <div class="team-card fade-in">
                    <div class="team-header">
                        <div class="team-logo">FCB</div>
                        <h3>بارسلونا</h3>
                        <p>FC Barcelona</p>
                    </div>
                    <div class="team-info">
                        <div class="team-stats">
                            <div class="team-stat">
                                <div class="team-stat-value">28</div>
                                <div class="team-stat-label">قهرمانی</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">95</div>
                                <div class="team-stat-label">فصل حضور</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">105,367</div>
                                <div class="team-stat-label">ظرفیت ورزشگاه</div>
                            </div>
                        </div>
                        <p style="margin-top: 1rem; color: #666;">
                            <i class="fas fa-map-marker-alt"></i> بارسلونا - کامپ نوو
                        </p>
                    </div>
                </div>

                <!-- Atletico Madrid -->
                <div class="team-card fade-in">
                    <div class="team-header">
                        <div class="team-logo">ATM</div>
                        <h3>اتلتیکو مادرید</h3>
                        <p>Atlético de Madrid</p>
                    </div>
                    <div class="team-info">
                        <div class="team-stats">
                            <div class="team-stat">
                                <div class="team-stat-value">11</div>
                                <div class="team-stat-label">قهرمانی</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">89</div>
                                <div class="team-stat-label">فصل حضور</div>
                            </div>
                            <div class="team-stat">
                                <div class="team-stat-value">70,460</div>
                                <div class="team-stat-label">ظرفیت ورزشگاه</div>
                            </div>
                        </div>
                        <p style="margin-top: 1rem; color: #666;">
                            <i class="fas fa-map-marker-alt"></i> مادرید - متروپولیتانو
                        </p>
                    </div>
                </d
