<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kyaw Moe Oo · modern profile</title>
    <!-- Font & Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Skill Icons CDN (devicon) for richer backend/frontend visuals -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f6f9fc 0%, #e9f1f8 100%);
            font-family: 'Inter', sans-serif;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            color: #1a2b3e;
            line-height: 1.5;
        }

        .profile-card {
            max-width: 1100px;
            width: 100%;
            background: rgba(255,255,255,0.75);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-radius: 3rem;
            box-shadow: 0 25px 50px -12px rgba(0,20,40,0.25), inset 0 1px 2px rgba(255,255,255,0.8);
            padding: 2.5rem;
            border: 1px solid rgba(255,255,255,0.6);
        }

        /* headings */
        h1 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #0b2b40, #1b4f6e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.25rem;
        }

        .subhead {
            font-size: 1.2rem;
            font-weight: 500;
            color: #2c5779;
            background: rgba(28, 78, 105, 0.08);
            display: inline-block;
            padding: 0.4rem 1.4rem;
            border-radius: 40px;
            backdrop-filter: blur(4px);
            margin-bottom: 1.2rem;
            border: 1px solid rgba(70, 147, 197, 0.2);
        }

        .typing-wrapper {
            margin: 1.5rem 0 1rem;
            filter: drop-shadow(0 4px 6px rgba(0,150,255,0.15));
        }

        /* section styling */
        .section-title {
            font-size: 1.8rem;
            font-weight: 650;
            letter-spacing: -0.01em;
            margin: 2.5rem 0 1.5rem 0;
            position: relative;
            display: inline-block;
        }
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 60%;
            height: 4px;
            background: linear-gradient(90deg, #1b6b8f, #48b5d0, #a0d6f0);
            border-radius: 4px;
        }

        .about-text {
            font-size: 1.1rem;
            background: rgba(255,255,255,0.5);
            padding: 1.5rem 2rem;
            border-radius: 2rem;
            border: 1px solid white;
            box-shadow: 0 5px 15px rgba(0,30,50,0.05);
            backdrop-filter: blur(4px);
            color: #1c3f5a;
            margin-bottom: 0.5rem;
        }

        .about-text i {
            color: #1f6e9f;
            margin-right: 0.5rem;
        }

        /* icon grids */
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem 2.5rem;
            background: rgba(255,255,255,0.3);
            padding: 2rem 2rem;
            border-radius: 2.5rem;
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255,255,255,0.9);
            margin-top: 1rem;
        }

        .tech-category {
            flex: 1 1 180px;
        }

        .tech-category h4 {
            font-size: 1.2rem;
            font-weight: 600;
            color: #154457;
            margin-bottom: 1rem;
            border-left: 5px solid #389ec9;
            padding-left: 0.8rem;
        }

        .icons-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
        }

        .icons-wrap i, .icons-wrap img {
            font-size: 2.5rem;
            filter: drop-shadow(0 6px 8px rgba(0,60,100,0.1));
            transition: transform 0.2s ease, filter 0.2s;
            color: #1f546e; /* fallback for devicon defaults */
        }
        .icons-wrap i:hover, .icons-wrap img:hover {
            transform: translateY(-5px);
            filter: drop-shadow(0 12px 12px rgba(0,150,200,0.25));
        }

        /* devicon colors (optional brand color) */
        .devicon-html5-plain { color: #e34f26; }
        .devicon-css3-plain { color: #1572b6; }
        .devicon-javascript-plain { color: #f7df1e; }
        .devicon-react-original { color: #61dafb; }
        .devicon-tailwindcss-original { color: #38b2ac; }
        .devicon-php-plain { color: #777bb4; }
        .devicon-laravel-original { color: #ff2d20; }
        .devicon-csharp-plain { color: #9b4f96; }
        .devicon-dotnetcore-plain { color: #512bd4; }
        .devicon-nodejs-plain { color: #339933; }
        .devicon-mysql-plain { color: #4479a1; }
        .devicon-mongodb-plain { color: #47a248; }
        .devicon-postgresql-plain { color: #336791; }
        .devicon-git-plain { color: #f05032; }
        .devicon-github-original { color: #181717; }
        .devicon-docker-plain { color: #2496ed; }
        .devicon-vscode-plain { color: #007acc; }
        .devicon-postman-plain { color: #ff6c37; }

        /* stats cards */
        .stats-wrapper {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
            margin: 1.8rem 0;
        }

        .stat-item {
            background: white;
            border-radius: 2rem;
            padding: 1.2rem 1.8rem;
            box-shadow: 0 10px 20px -8px rgba(2,70,110,0.2);
            border: 1px solid rgba(70, 150, 210, 0.2);
            backdrop-filter: blur(4px);
            transition: all 0.2s;
            flex: 1 1 260px;
            display: flex;
            justify-content: center;
        }

        .streak-item {
            background: white;
            border-radius: 2rem;
            padding: 1.2rem 1.8rem;
            box-shadow: 0 10px 25px -8px #023b5a33;
            border: 1px solid #c1e2f5;
            max-width: 550px;
            margin: 0 auto 1.8rem;
        }

        /* project cards */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0 1.2rem;
        }

        .project-card {
            background: white;
            border-radius: 1.8rem;
            padding: 1.5rem 1.2rem;
            border: 1px solid rgba(75, 166, 216, 0.2);
            box-shadow: 0 8px 18px -10px #14455b33;
            transition: 0.15s ease;
            font-weight: 500;
        }

        .project-card:hover {
            background: #f6fdff;
            border-color: #47b3e0;
            box-shadow: 0 16px 24px -12px #166b99;
        }

        .project-card i {
            font-size: 1.6rem;
            background: linear-gradient(145deg, #19678b, #3fa2c9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-right: 10px;
        }

        .focus-panel {
            background: #e1f0f9;
            border-radius: 2rem;
            padding: 1.5rem 2rem;
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin: 2rem 0 1.5rem;
            border: 1px solid white;
        }

        .focus-pill {
            background: white;
            padding: 0.6rem 1.4rem;
            border-radius: 40px;
            font-weight: 500;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
            color: #124e6e;
            border: 1px solid #cbe5f5;
            font-size: 0.95rem;
        }

        .focus-pill i {
            margin-right: 8px;
            color: #2482b1;
        }

        /* connect row */
        .connect-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.8rem;
            padding-top: 1rem;
        }

        .connect-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            background: white;
            padding: 0.8rem 1.8rem;
            border-radius: 60px;
            font-weight: 500;
            color: #1f4b69;
            text-decoration: none;
            border: 1px solid rgba(36, 130, 190, 0.3);
            transition: 0.15s;
            box-shadow: 0 4px 8px rgba(0, 55, 90, 0.05);
            font-size: 1rem;
        }

        .connect-btn:hover {
            background: #d8ecfc;
            border-color: #389ec9;
            transform: scale(1.02);
        }

        .connect-btn i {
            font-size: 1.3rem;
        }

        hr {
            border: none;
            height: 2px;
            background: linear-gradient(90deg, transparent, #a0c9e5, transparent);
            margin: 2rem 0 0.5rem;
        }

        /* align center utility */
        .align-center {
            text-align: center;
        }
        .name-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    </style>
</head>
<body>
<div class="profile-card">
    <!-- HEADER modernized -->
    <div class="name-wrapper">
        <h1>Kyaw Moe Oo</h1>
        <div class="subhead">
            <i class="fas fa-code" style="margin-right: 8px;"></i>Full Stack Web Developer · Backend & Frontend · Microservices
        </div>
    </div>

    <!-- Typing effect (embedded SVG-like with placeholder) -->
    <div class="typing-wrapper align-center">
        <img src="https://readme-typing-svg.herokuapp.com?font=Inter&weight=600&size=26&duration=3200&pause=600&color=1A6B9F&center=true&vCenter=true&width=700&lines=Full+Stack+Developer;Backend+%2B+Frontend+Engineer;Clean+Architecture+Lover;Microservices+Builder" 
             alt="Typing SVG" style="max-width:100%; height:auto; border-radius: 60px; background: rgba(255,255,255,0.3); backdrop-filter: blur(4px); padding: 0.5rem 0;">
    </div>

    <!-- About Me section with modern card -->
    <div class="section-title">👨‍💻 about</div>
    <div class="about-text">
        <i class="fas fa-bolt"></i> Full Stack Web Developer passionate about building scalable applications & clean system architecture.<br>
        <i class="fas fa-cubes" style="margin-left: 1.5rem;"></i> Backend & Frontend · microservices & REST APIs · clean, testable code.<br>
        <i class="fas fa-book-open"></i> Currently mastering .NET, Laravel, and advanced system design.
    </div>

    <!-- Tech Stack with devicon & modern grid -->
    <div class="section-title">🚀 tech stack</div>
    <div class="tech-grid">
        <div class="tech-category">
            <h4><i class="fas fa-paint-brush" style="margin-right: 6px;"></i>Frontend</h4>
            <div class="icons-wrap">
                <i class="devicon-html5-plain"></i>
                <i class="devicon-css3-plain"></i>
                <i class="devicon-javascript-plain"></i>
                <i class="devicon-react-original"></i>
                <i class="devicon-tailwindcss-original"></i>
            </div>
        </div>
        <div class="tech-category">
            <h4><i class="fas fa-server"></i> Backend</h4>
            <div class="icons-wrap">
                <i class="devicon-php-plain"></i>
                <i class="devicon-laravel-original"></i>
                <i class="devicon-csharp-plain"></i>
                <i class="devicon-dotnetcore-plain"></i>
                <i class="devicon-nodejs-plain"></i>
            </div>
        </div>
        <div class="tech-category">
            <h4><i class="fas fa-database"></i> Database</h4>
            <div class="icons-wrap">
                <i class="devicon-mysql-plain"></i>
                <i class="devicon-mongodb-plain"></i>
                <i class="devicon-postgresql-plain"></i>
            </div>
        </div>
        <div class="tech-category">
            <h4><i class="fas fa-tools"></i> Tools</h4>
            <div class="icons-wrap">
                <i class="devicon-git-plain"></i>
                <i class="devicon-github-original"></i>
                <i class="devicon-docker-plain"></i>
                <i class="devicon-vscode-plain"></i>
                <i class="devicon-postman-plain"></i>
            </div>
        </div>
    </div>

    <!-- GitHub Analytics Cards (simulated with placeholders, but styled) -->
    <div class="section-title">📊 GitHub analytics</div>
    <div class="stats-wrapper">
        <div class="stat-item">
            <img src="https://github-readme-stats.vercel.app/api?username=Kyaw-Moe-Oo&show_icons=true&theme=swift&hide_border=true&bg_color=ffffff00&title_color=1b6b8f&icon_color=3d9bc9&text_color=1f4a66" 
                 alt="github stats" style="max-width: 100%;">
        </div>
        <div class="stat-item">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kyaw-Moe-Oo&layout=compact&theme=swift&hide_border=true&bg_color=ffffff00&title_color=1b6b8f&text_color=1f4a66" 
                 alt="top languages" style="max-width: 100%;">
        </div>
    </div>

    <!-- Contribution Streak -->
    <div class="section-title">🔥 contribution streak</div>
    <div class="streak-item align-center">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=Kyaw-Moe-Oo&theme=icegray&hide_border=true&background=ffffff00&ring=1B8BB0&fire=3E9BC8&currStreakNum=145E7E" 
             alt="streak" style="max-width: 100%;">
    </div>

    <!-- Featured Projects with iconography -->
    <div class="section-title">📌 featured projects</div>
    <div class="project-grid">
        <div class="project-card"><i class="fas fa-school"></i> Student Management System – Full Stack PHP, MySQL</div>
        <div class="project-card"><i class="fas fa-cart-shopping"></i> Microservices E-commerce – Laravel + REST + MongoDB</div>
        <div class="project-card"><i class="fas fa-calculator"></i> Interest Calculation Engine – advanced backend logic</div>
        <div class="project-card"><i class="fas fa-ticket-alt"></i> VIP Customer Queue System – priority handling</div>
    </div>

    <!-- Current Focus pills -->
    <div class="section-title">🎯 current focus</div>
    <div class="focus-panel">
        <span class="focus-pill"><i class="fas fa-dot-circle"></i> Advanced .NET & PHP backend</span>
        <span class="focus-pill"><i class="fas fa-cloud"></i> REST API & Microservices</span>
        <span class="focus-pill"><i class="fas fa-mobile-alt"></i> Frontend optimization (React+Tailwind)</span>
        <span class="focus-pill"><i class="fas fa-code-branch"></i> System design & clean code</span>
    </div>

    <!-- Connect section with modern buttons -->
    <div class="section-title">📫 connect</div>
    <div class="connect-links">
        <a href="https://github.com/Kyaw-Moe-Oo" class="connect-btn"><i class="fab fa-github"></i> GitHub</a>
        <a href="https://www.linkedin.com/in/Kyaw-Moe-Oo" class="connect-btn"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="mailto:kyaw.moeoo@example.com" class="connect-btn"><i class="fas fa-envelope"></i> Email</a>
        <!-- optional extra microservice vibe -->
        <span class="connect-btn" style="background:#ebf5fb; cursor: default;"><i class="fas fa-microchip"></i> microservices enthusiast</span>
    </div>

    <!-- subtle separator -->
    <hr>
    <div style="text-align: center; font-size: 0.8rem; color: #5d7f9a; margin-top: 1.2rem;">
        <i class="fas fa-crown" style="opacity: 0.5;"></i> clean architecture · modern stack · 2025
    </div>
</div>
</body>
</html>
