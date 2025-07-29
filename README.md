
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مهندس مهدی رحمانی | توسعه‌دهنده فول استک</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;700&family=Playfair+Display:wght@500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #5D5FEF;
            --primary-light: #E0E1FF;
            --secondary-color: #10B981;
            --secondary-light: #D1FAE5;
            --accent-color: #F59E0B;
            --accent-light: #FEF3C7;
            --dark-color: #1F2937;
            --light-color: #F9FAFB;
            --text-color: #374151;
            --text-light: #F9FAFB;
            --gray-light: #E5E7EB;
            --gray-medium: #9CA3AF;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
            --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 25px rgba(0, 0, 0, 0.1);
            --border-radius: 12px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Vazirmatn', sans-serif;
            background-color: var(--light-color);
            color: var(--text-color);
            line-height: 1.7;
            overflow-x: hidden;
            font-weight: 400;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            line-height: 1.3;
            color: var(--dark-color);
        }
        
        /* نوار ناوبری */
        .navbar {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1.2rem 2rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow-sm);
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: var(--transition);
        }
        
        .navbar.scrolled {
            box-shadow: var(--shadow-md);
            padding: 0.8rem 2rem;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .logo i {
            font-size: 1.4rem;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-right: 1.8rem;
        }
        
        .nav-links a {
            color: var(--dark-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            font-size: 0.95rem;
            padding: 0.5rem 0;
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary-color);
            bottom: 0;
            right: 0;
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
            left: 0;
        }
        
        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--dark-color);
            z-index: 1001;
        }
        
        /* بخش هیرو */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 10%;
            background: linear-gradient(135deg, #f5f7fa 0%, #E0E1FF 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 600px;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            color: var(--dark-color);
        }
        
        .hero h1 span {
            color: var(--primary-color);
            position: relative;
            display: inline-block;
        }
        
        .hero h1 span::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 12px;
            background-color: var(--primary-light);
            bottom: 8px;
            right: 0;
            z-index: -1;
            border-radius: 4px;
        }
        
        .hero p {
            font-size: 1.1rem;
            margin-bottom: 2.5rem;
            color: var(--text-color);
            opacity: 0.9;
            max-width: 90%;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            background-color: var(--primary-color);
            color: var(--text-light);
            padding: 0.9rem 2rem;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
            gap: 0.5rem;
            box-shadow: 0 4px 6px rgba(93, 95, 239, 0.2);
        }
        
        .btn:hover {
            background-color: #4B4DDB;
            transform: translateY(-2px);
            box-shadow: 0 7px 14px rgba(93, 95, 239, 0.25);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 1.5px solid var(--primary-color);
            color: var(--primary-color);
            margin-right: 1rem;
            box-shadow: none;
        }
        
        .btn-outline:hover {
            background-color: var(--primary-light);
            color: var(--primary-color);
            transform: translateY(-2px);
        }
        
        .hero-btns {
            display: flex;
            align-items: center;
        }
        
        .social-icons {
            display: flex;
            margin-top: 3rem;
            gap: 1.2rem;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 42px;
            height: 42px;
            background-color: white;
            color: var(--primary-color);
            border-radius: 50%;
            font-size: 1.2rem;
            transition: var(--transition);
            box-shadow: var(--shadow-sm);
        }
        
        .social-icons a:hover {
            background-color: var(--primary-color);
            color: white;
            transform: translateY(-3px);
            box-shadow: var(--shadow-md);
        }
        
        .hero-shape {
            position: absolute;
            width: 600px;
            height: 600px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(93, 95, 239, 0.1) 0%, rgba(93, 95, 239, 0.05) 100%);
            top: -200px;
            right: -200px;
            z-index: 0;
        }
        
        .hero-shape-2 {
            position: absolute;
            width: 400px;
            height: 400px;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            background: linear-gradient(135deg, rgba(16, 185, 129, 0.1) 0%, rgba(16, 185, 129, 0.05) 100%);
            bottom: -100px;
            left: -100px;
            z-index: 0;
            animation: float 8s ease-in-out infinite;
        }
        
        /* بخش درباره من */
        .about {
            padding: 7rem 10%;
            background-color: white;
            position: relative;
            overflow: hidden;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 4rem;
            color: var(--dark-color);
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 60px;
            height: 4px;
            background-color: var(--primary-color);
            bottom: -12px;
            right: 50%;
            transform: translateX(50%);
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 4rem;
            position: relative;
            z-index: 1;
        }
        
        .about-img {
            flex: 1;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow-lg);
            transition: var(--transition);
        }
        
        .about-img:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s;
        }
        
        .about-img:hover img {
            transform: scale(1.03);
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--dark-color);
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
            color: var(--text-color);
            line-height: 1.8;
        }
        
        .skills {
            margin-top: 2.5rem;
        }
        
        .skill-item {
            margin-bottom: 1.8rem;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.6rem;
            font-size: 0.95rem;
            color: var(--dark-color);
        }
        
        .skill-bar {
            height: 8px;
            background-color: var(--gray-light);
            border-radius: 4px;
            overflow: hidden;
        }
        
        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), #7B7DF2);
            border-radius: 4px;
            transition: width 1s ease-in-out;
            position: relative;
            overflow: hidden;
        }
        
        .skill-progress::after {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: linear-gradient(90deg, 
                            rgba(255,255,255,0.1) 0%, 
                            rgba(255,255,255,0.4) 50%, 
                            rgba(255,255,255,0.1) 100%);
            animation: shine 2s infinite;
        }
        
        /* بخش خدمات */
        .services {
            padding: 7rem 10%;
            background-color: var(--light-color);
            position: relative;
        }
        
        .services-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .service-card {
            background-color: white;
            padding: 2.5rem 2rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.03);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(93, 95, 239, 0.03) 0%, rgba(93, 95, 239, 0.01) 100%);
            z-index: -1;
        }
        
        .service-card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow-lg);
        }
        
        .service-icon {
            width: 70px;
            height: 70px;
            background-color: var(--primary-light);
            color: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin: 0 auto 1.8rem;
            transition: var(--transition);
        }
        
        .service-card:hover .service-icon {
            background-color: var(--primary-color);
            color: white;
            transform: rotateY(180deg);
        }
        
        .service-card h3 {
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
            color: var(--dark-color);
        }
        
        .service-card p {
            color: var(--text-color);
            font-size: 0.95rem;
            line-height: 1.7;
        }
        
        /* بخش نمونه کارها */
        .portfolio {
            padding: 7rem 10%;
            background-color: white;
            position: relative;
        }
        
        .portfolio-filter {
            display: flex;
            justify-content: center;
            margin-bottom: 3.5rem;
            flex-wrap: wrap;
            gap: 0.8rem;
        }
        
        .filter-btn {
            background-color: transparent;
            border: 1px solid var(--gray-light);
            padding: 0.6rem 1.8rem;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: 500;
            color: var(--text-color);
            transition: var(--transition);
            border-radius: 30px;
            font-family: 'Vazirmatn', sans-serif;
        }
        
        .filter-btn.active, .filter-btn:hover {
            background-color: var(--primary-color);
            color: var(--text-light);
            border-color: var(--primary-color);
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 1.8rem;
        }
        
        .portfolio-item {
            position: relative;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            height: 260px;
            transition: var(--transition);
        }
        
        .portfolio-item:hover {
            box-shadow: var(--shadow-lg);
        }
        
        .portfolio-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .portfolio-overlay {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(93, 95, 239, 0.9) 0%, rgba(73, 75, 219, 0.9) 100%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: var(--transition);
            padding: 1.5rem;
            text-align: center;
            color: var(--text-light);
        }
        
        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }
        
        .portfolio-item:hover .portfolio-img {
            transform: scale(1.05);
        }
        
        .portfolio-overlay h3 {
            font-size: 1.5rem;
            margin-bottom: 0.8rem;
        }
        
        .portfolio-overlay p {
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
            opacity: 0.9;
        }
        
        .portfolio-overlay a {
            color: var(--text-light);
            font-size: 1.2rem;
            margin: 0 0.7rem;
            transition: var(--transition);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .portfolio-overlay a:hover {
            background-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
        }
        
        /* بخش تماس */
        .contact {
            padding: 7rem 10%;
            background-color: var(--light-color);
            position: relative;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
        }
        
        .contact-card {
            display: flex;
            align-items: flex-start;
            margin-bottom: 2rem;
            background-color: white;
            padding: 1.8rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            border: 1px solid rgba(0, 0, 0, 0.03);
        }
        
        .contact-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--primary-light);
            color: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            margin-left: 1.5rem;
            flex-shrink: 0;
        }
        
        .contact-text h3 {
            font-size: 1.2rem;
            margin-bottom: 0.6rem;
            color: var(--dark-color);
        }
        
        .contact-text p, .contact-text a {
            color: var(--text-color);
            text-decoration: none;
            font-size: 0.95rem;
            transition: var(--transition);
        }
        
        .contact-text a:hover {
            color: var(--primary-color);
        }
        
        .contact-form {
            background-color: white;
            padding: 2.5rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-sm);
            border: 1px solid rgba(0, 0, 0, 0.03);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-control {
            width: 100%;
            padding: 1rem 1.2rem;
            border: 1px solid var(--gray-light);
            border-radius: 8px;
            font-size: 0.95rem;
            transition: var(--transition);
            font-family: 'Vazirmatn', sans-serif;
        }
        
        .form-control:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(93, 95, 239, 0.1);
        }
        
        textarea.form-control {
            min-height: 160px;
            resize: vertical;
        }
        
        /* فوتر */
        .footer {
            background-color: var(--dark-color);
            color: var(--text-light);
            padding: 4rem 10% 2rem;
            text-align: center;
            position: relative;
        }
        
        .footer::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.02)" d="M0,0 L100,0 L100,100 L0,100 Z"></path></svg>') repeat;
            opacity: 0.1;
            z-index: 0;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.8rem;
            color: var(--text-light);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .footer-logo i {
            font-size: 1.4rem;
            color: var(--primary-color);
        }
        
        .footer-links {
            display: flex;
            list-style: none;
            margin-bottom: 2.5rem;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
        }
        
        .footer-links a {
            color: var(--text-light);
            text-decoration: none;
            transition: var(--transition);
            font-size: 0.95rem;
            opacity: 0.8;
        }
        
        .footer-links a:hover {
            color: var(--primary-light);
            opacity: 1;
        }
        
        .footer-social {
            margin-bottom: 2.5rem;
            display: flex;
            gap: 1.2rem;
        }
        
        .footer-social a {
            color: var(--text-light);
            font-size: 1.2rem;
            transition: var(--transition);
            opacity: 0.7;
        }
        
        .footer-social a:hover {
            color: var(--primary-light);
            opacity: 1;
            transform: translateY(-3px);
        }
        
        .copyright {
            opacity: 0.6;
            font-size: 0.9rem;
            margin-top: 1.5rem;
        }
        
        /* دکمه بازگشت به بالا */
        .back-to-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background-color: var(--primary-color);
            color: var(--text-light);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.2rem;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            z-index: 999;
            box-shadow: var(--shadow-md);
            border: none;
        }
        
        .back-to-top.active {
            opacity: 1;
            visibility: visible;
        }
        
        .back-to-top:hover {
            background-color: var(--dark-color);
            transform: translateY(-5px) scale(1.1);
        }
        
        /* انیمیشن ها */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes float {
            0% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(2deg); }
            100% { transform: translateY(0px) rotate(0deg); }
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .delay-1 { transition-delay: 0.1s; }
        .delay-2 { transition-delay: 0.2s; }
        .delay-3 { transition-delay: 0.3s; }
        .delay-4 { transition-delay: 0.4s; }
        .delay-5 { transition-delay: 0.5s; }
        
        /* رسپانسیو */
        @media (max-width: 1200px) {
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .about-img, .about-text {
                flex: none;
                width: 100%;
            }
            
            .about-img {
                max-width: 500px;
                margin: 0 auto 3rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                max-width: 100%;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: 280px;
                height: 100vh;
                background-color: white;
                flex-direction: column;
                align-items: flex-start;
                padding: 6rem 2rem 2rem;
                transition: right 0.4s ease-in-out;
                box-shadow: var(--shadow-lg);
            }
            
            .nav-links.active {
                right: 0;
            }
            
            .nav-links li {
                margin: 0.8rem 0;
                width: 100%;
            }
            
            .nav-links a {
                padding: 0.8rem 0;
                display: block;
                width: 100%;
                font-size: 1rem;
            }
            
            .hero {
                padding: 0 5%;
                text-align: center;
            }
            
            .hero-content {
                max-width: 100%;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .btn-outline {
                margin-right: 0;
                margin-bottom: 1rem;
            }
            
            .social-icons {
                justify-content: center;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .portfolio-grid {
                grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
                margin-bottom: 3rem;
            }
            
            .portfolio-filter {
                flex-direction: column;
                align-items: center;
            }
            
            .filter-btn {
                width: 100%;
                max-width: 200px;
                margin: 0.3rem 0;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .contact-card {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }
            
            .contact-icon {
                margin-left: 0;
                margin-bottom: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- نوار ناوبری -->
    <nav class="navbar">
        <a href="#" class="logo">
            <i class="fas fa-code"></i>
            <span>مهدی رحمانی</span>
        </a>
        <div class="menu-toggle">
            <i class="fas fa-bars"></i>
        </div>
        <ul class="nav-links">
            <li><a href="#home">خانه</a></li>
            <li><a href="#about">درباره من</a></li>
            <li><a href="#services">خدمات</a></li>
            <li><a href="#portfolio">نمونه کارها</a></li>
            <li><a href="#contact">تماس</a></li>
        </ul>
    </nav>

    <!-- بخش هیرو -->
    <section id="home" class="hero">
        <div class="hero-shape"></div>
        <div class="hero-shape-2"></div>
        <div class="hero-content fade-in">
            <h1>سلام، من <span>مهدی رحمانی</span> هستم</h1>
            <p>توسعه‌دهنده فول استک (Full Stack) با تخصص در طراحی و پیاده‌سازی سیستم‌های نرم‌افزاری پیشرفته و مدرن</p>
            <div class="hero-btns">
                <a href="#portfolio" class="btn btn-outline delay-1">
                    <i class="far fa-eye"></i>
                    نمونه کارها
                </a>
                <a href="#contact" class="btn delay-2">
                    <i class="far fa-paper-plane"></i>
                    تماس با من
                </a>
            </div>
            <div class="social-icons delay-3">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </section>

    <!-- بخش درباره من -->
    <section id="about" class="about">
        <h2 class="section-title fade-in">درباره من</h2>
        <div class="about-content">
            <div class="about-img fade-in">
                <img src="https://images.unsplash.com/photo-1580927752452-89d86da3fa0a?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="مهدی رحمانی">
            </div>
            <div class="about-text fade-in delay-1">
                <h3>مهندس نرم‌افزار و توسعه‌دهنده فول استک (Full Stack)</h3>
                <p>من مهدی رحمانی، مهندس نرم‌افزار با بیش از 4 سال تجربه در توسعه وب و موبایل هستم. تخصص اصلی من در طراحی و پیاده‌سازی سیستم‌های تحت وب پیشرفته با استفاده از آخرین تکنولوژی‌ها است.</p>
                <p>در طول این سال‌ها موفق به تکمیل ده‌ها پروژه موفق برای شرکت‌های داخلی و بین‌المللی شده‌ام و همواره به دنبال یادگیری و استفاده از تکنولوژی‌های جدید هستم.</p>
                
                <div class="skills">
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>HTML & CSS</span>
                            <span>100%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 100%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>JavaScript</span>
                            <span>93%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 93%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>React</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%"></div>
                        </div>
                    </div>
                    
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Node.js</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 80%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- بخش خدمات -->
    <section id="services" class="services">
        <h2 class="section-title fade-in">خدمات من</h2>
        <div class="services-container">
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-code"></i>
                </div>
                <h3>توسعه وب</h3>
                <p>طراحی و توسعه وبسایت‌های حرفه‌ای و واکنش‌گرا با استفاده از آخرین تکنولوژی‌های روز دنیا</p>
            </div>
            
            <div class="service-card fade-in delay-1">
                <div class="service-icon">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <h3>توسعه اپلیکیشن موبایل</h3>
                <p>طراحی و توسعه اپلیکیشن‌های موبایل برای پلتفرم‌های iOS و Android با بهترین کیفیت</p>
            </div>
            
            <div class="service-card fade-in delay-2">
                <div class="service-icon">
                    <i class="fas fa-paint-brush"></i>
                </div>
                <h3>طراحی UI/UX</h3>
                <p>طراحی رابط کاربری حرفه‌ای و تجربه کاربری منحصر به فرد برای محصولات دیجیتال</p>
            </div>
            
            <div class="service-card fade-in delay-3">
                <div class="service-icon">
                    <i class="fas fa-server"></i>
                </div>
                <h3>برنامه‌نویسی بک‌اند</h3>
                <p>پیاده‌سازی سیستم‌های بک‌اند قدرتمند و امن برای وبسایت‌ها و اپلیکیشن‌ها</p>
            </div>
        </div>
    </section>

    <!-- بخش نمونه کارها -->
    <section id="portfolio" class="portfolio">
        <h2 class="section-title fade-in">نمونه کارها</h2>
        <div class="portfolio-filter fade-in">
            <button class="filter-btn active" data-filter="all">همه</button>
            <button class="filter-btn" data-filter="web">وب</button>
            <button class="filter-btn" data-filter="mobile">موبایل</button>
            <button class="filter-btn" data-filter="design">طراحی</button>
        </div>
        <div class="portfolio-grid">
            <div class="portfolio-item fade-in" data-category="web">
                <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 1" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>وبسایت فروشگاهی</h3>
                    <p>یک وبسایت فروشگاهی کامل با سیستم مدیریت محتوا</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="portfolio-item fade-in delay-1" data-category="mobile">
                <img src="https://images.unsplash.com/photo-1555774698-0b77e0d5fac6?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 2" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>اپلیکیشن موبایل</h3>
                    <p>اپلیکیشن مدیریت مالی شخصی برای اندروید و iOS</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="portfolio-item fade-in delay-2" data-category="design">
                <img src="https://images.unsplash.com/photo-1541462608143-67571c6738dd?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 3" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>طراحی رابط کاربری</h3>
                    <p>طراحی UI/UX برای یک اپلیکیشن سلامت</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="portfolio-item fade-in delay-3" data-category="web">
                <img src="https://images.unsplash.com/photo-1481487196290-c152efe083f5?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 4" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>پورتال سازمانی</h3>
                    <p>سیستم مدیریت محتوای سازمانی با امکانات پیشرفته</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="portfolio-item fade-in delay-1" data-category="mobile">
                <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 5" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>اپلیکیشن مسیریابی</h3>
                    <p>اپلیکیشن مسیریابی و نقشه با قابلیت‌های پیشرفته</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="portfolio-item fade-in delay-2" data-category="design">
                <img src="https://images.unsplash.com/photo-1496171367470-9ed9a91ea931?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="پروژه 6" class="portfolio-img">
                <div class="portfolio-overlay">
                    <h3>طراحی برند</h3>
                    <p>طراحی هویت بصری برای یک استارتاپ فناوری</p>
                    <div>
                        <a href="#"><i class="fas fa-link"></i></a>
                        <a href="#"><i class="fas fa-search"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- بخش تماس -->
    <section id="contact" class="contact">
        <h2 class="section-title fade-in">تماس با من</h2>
        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-card fade-in">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div class="contact-text">
                        <h3>آدرس</h3>
                        <p>ایران، تهران</p>
                    </div>
                </div>
                
                <div class="contact-card fade-in delay-1">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div class="contact-text">
                        <h3>تلفن</h3>
                        <a href="tel:+989352250294">00989352250294 / 0093790812955</a>
                    </div>
                </div>
                
                <div class="contact-card fade-in delay-2">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div class="contact-text">
                        <h3>ایمیل</h3>
                        <a href="mailto:mehdi.rahmani@example.com">mahdirahmani77z@gmail.com</a>
                    </div>
                </div>
            </div>
            
            <div class="contact-form fade-in delay-3">
                <form>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="نام شما" required>
                    </div>
                    
                    <div class="form-group">
                        <input type="email" class="form-control" placeholder="ایمیل شما" required>
                    </div>
                    
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="موضوع">
                    </div>
                    
                    <div class="form-group">
                        <textarea class="form-control" placeholder="پیام شما" required></textarea>
                    </div>
                    
                    <button type="submit" class="btn">
                        <i class="far fa-paper-plane"></i>
                        ارسال پیام
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- فوتر -->
    <footer class="footer">
        <div class="footer-content">
            <div class="footer-logo">
                <i class="fas fa-code"></i>
                <span>مهدی رحمانی</span>
            </div>
            <ul class="footer-links">
                <li><a href="#home">خانه</a></li>
                <li><a href="#about">درباره من</a></li>
                <li><a href="#services">خدمات</a></li>
                <li><a href="#portfolio">نمونه کارها</a></li>
                <li><a href="#contact">تماس</a></li>
            </ul>
            <div class="footer-social">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p class="copyright">تمامی حقوق برای مهدی رحمانی محفوظ است © 2023</p>
        </div>
    </footer>

    <!-- دکمه بازگشت به بالا -->
    <div class="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </div>

    <script>
        // منوی موبایل
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            menuToggle.classList.toggle('active');
        });
        
        // اسکرول نرم
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // بستن منو در حالت موبایل
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                    menuToggle.classList.remove('active');
                }
            });
        });
        
        // فیلتر نمونه کارها
        const filterBtns = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');
        
        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // حذف کلاس active از همه دکمه‌ها
                filterBtns.forEach(btn => btn.classList.remove('active'));
                // اضافه کردن کلاس active به دکمه کلیک شده
                btn.classList.add('active');
                
                const filter = btn.getAttribute('data-filter');
                
                portfolioItems.forEach(item => {
                    if (filter === 'all' || item.getAttribute('data-category') === filter) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // انیمیشن مهارت‌ها
        const skillBars = document.querySelectorAll('.skill-progress');
        
        function animateSkills() {
            skillBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width = '0';
                setTimeout(() => {
                    bar.style.width = width;
                }, 100);
            });
        }
        
        // نمایش دکمه بازگشت به بالا
        const backToTopBtn = document.querySelector('.back-to-top');
        const navbar = document.querySelector('.navbar');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopBtn.classList.add('active');
                navbar.classList.add('scrolled');
            } else {
                backToTopBtn.classList.remove('active');
                navbar.classList.remove('scrolled');
            }
        });
        
        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // انیمیشن اسکرول
        const fadeElements = document.querySelectorAll('.fade-in');
        
        function checkScroll() {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementTop < windowHeight - 100) {
                    element.classList.add('visible');
                }
            });
        }
        
        // اجرای انیمیشن مهارت‌ها هنگام نمایش بخش درباره من
        const aboutSection = document.querySelector('.about');
        
        function checkAboutSection() {
            const aboutTop = aboutSection.getBoundingClientRect().top;
            const windowHeight = window.innerHeight;
            
            if (aboutTop < windowHeight - 100) {
                animateSkills();
                window.removeEventListener('scroll', checkAboutSection);
            }
        }
        
        // رویدادهای اسکرول
        window.addEventListener('scroll', checkScroll);
        window.addEventListener('scroll', checkAboutSection);
        
        // اجرای اولیه برای عناصری که در viewport هستند
        checkScroll();
        
        // اجرای انیمیشن برای عناصر در هنگام لود صفحه
        window.addEventListener('load', () => {
            checkScroll();
            checkAboutSection();
        });
    </script>
</body>
</html>
