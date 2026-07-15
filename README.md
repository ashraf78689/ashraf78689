<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mohammed Ashraf · AI & Data Science</title>

    <!-- ===== Google Fonts ===== -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet" />

    <!-- ===== Font Awesome 6 (Free) ===== -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

    <style>
        /* ============================================================
                   GLOBAL RESET & BASE
                   ============================================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0D1117;
            font-family: 'Inter', 'Segoe UI', sans-serif;
            color: #e6edf3;
            line-height: 1.6;
            padding: 2rem 1rem;
            display: flex;
            justify-content: center;
        }

        .container {
            max-width: 1100px;
            width: 100%;
            margin: 0 auto;
        }

        /* ============================================================
                   GLASSMORPHISM CARD
                   ============================================================ */
        .glass {
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(0, 245, 255, 0.12);
            border-radius: 28px;
            padding: 2rem 2rem 2.2rem;
            margin-bottom: 2.2rem;
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.7),
                inset 0 1px 0 rgba(255, 255, 255, 0.04);
            transition: border-color 0.3s ease, box-shadow 0.4s ease;
        }

        .glass:hover {
            border-color: rgba(0, 245, 255, 0.30);
            box-shadow: 0 24px 48px -12px rgba(0, 245, 255, 0.08),
                inset 0 1px 0 rgba(255, 255, 255, 0.06);
        }

        /* ============================================================
                   TYPOGRAPHY
                   ============================================================ */
        .font-grotesk {
            font-family: 'Space Grotesk', 'Inter', sans-serif;
        }

        .neon-blue {
            color: #00F5FF;
        }
        .neon-cyan {
            color: #00D9FF;
        }
        .neon-purple {
            color: #8A2BE2;
        }
        .text-white {
            color: #FFFFFF;
        }
        .text-muted {
            color: rgba(255, 255, 255, 0.55);
        }

        .glow-text {
            text-shadow: 0 0 20px rgba(0, 245, 255, 0.25), 0 0 60px rgba(0, 245, 255, 0.08);
        }

        .section-title {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            font-size: 1.9rem;
            letter-spacing: -0.02em;
            display: flex;
            align-items: center;
            gap: 0.6rem;
            margin-bottom: 1.6rem;
        }

        .section-title i {
            color: #00F5FF;
            font-size: 1.7rem;
        }

        .section-sub {
            font-size: 0.95rem;
            color: rgba(255, 255, 255, 0.5);
            margin-top: -0.5rem;
            margin-bottom: 1.8rem;
            letter-spacing: 0.3px;
        }

        /* ============================================================
                   BANNER
                   ============================================================ */
        .banner {
            position: relative;
            overflow: hidden;
            background: radial-gradient(circle at 20% 30%, rgba(138, 43, 226, 0.20) 0%, transparent 60%),
                radial-gradient(circle at 80% 70%, rgba(0, 245, 255, 0.12) 0%, transparent 50%),
                #0D1117;
            border-radius: 28px;
            padding: 3.2rem 2.8rem;
            margin-bottom: 2.2rem;
            border: 1px solid rgba(0, 245, 255, 0.10);
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.8);
        }

        .banner::after {
            content: '';
            position: absolute;
            inset: 0;
            background:
                repeating-linear-gradient(45deg,
                    transparent,
                    transparent 60px,
                    rgba(0, 245, 255, 0.015) 60px,
                    rgba(0, 245, 255, 0.015) 61px);
            pointer-events: none;
        }

        .banner-content {
            position: relative;
            z-index: 2;
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .banner-badge {
            display: inline-block;
            background: rgba(0, 245, 255, 0.08);
            border: 1px solid rgba(0, 245, 255, 0.15);
            border-radius: 100px;
            padding: 0.25rem 1.2rem;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.8px;
            text-transform: uppercase;
            color: #00F5FF;
            width: fit-content;
            backdrop-filter: blur(4px);
        }

        .banner h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 700;
            font-size: clamp(2.6rem, 7vw, 4.8rem);
            line-height: 1.08;
            letter-spacing: -0.03em;
            background: linear-gradient(135deg, #00F5FF 0%, #8A2BE2 70%, #00D9FF 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: none;
            margin: 0.2rem 0 0.2rem;
        }

        .banner .subhead {
            font-size: clamp(1rem, 2vw, 1.4rem);
            color: rgba(255, 255, 255, 0.6);
            font-weight: 400;
            letter-spacing: 0.4px;
        }

        .banner .subhead strong {
            color: #00D9FF;
            font-weight: 500;
        }

        .banner-tagline {
            font-size: clamp(1.1rem, 1.6vw, 1.5rem);
            font-weight: 500;
            color: #FFFFFF;
            margin-top: 0.6rem;
            letter-spacing: -0.01em;
            background: linear-gradient(135deg, #00F5FF, #8A2BE2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .banner-stats {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem 3rem;
            margin-top: 1.2rem;
            padding-top: 1.2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.04);
        }

        .banner-stats .stat-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.5);
        }

        .banner-stats .stat-item i {
            color: #00F5FF;
            font-size: 1rem;
        }

        .banner-stats .stat-item strong {
            color: #FFFFFF;
            font-weight: 600;
        }

        /* ============================================================
                   TYPING ANIMATION (CSS only – no JS)
                   ============================================================ */
        .typing-wrapper {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 0.3rem 0.6rem;
            font-family: 'Space Grotesk', monospace;
            font-size: clamp(1.1rem, 2vw, 1.5rem);
            font-weight: 500;
            color: rgba(255, 255, 255, 0.7);
            margin: 0.2rem 0 0.2rem;
        }

        .typing-wrapper .static-text {
            color: rgba(255, 255, 255, 0.5);
        }

        .typing-wrapper .dynamic-text {
            display: inline-block;
            color: #00F5FF;
            border-right: 3px solid #00F5FF;
            padding-right: 6px;
            animation: blink-caret 0.75s step-end infinite;
            min-width: 120px;
            text-shadow: 0 0 30px rgba(0, 245, 255, 0.15);
        }

        @keyframes blink-caret {
            0%,
            100% {
                border-color: #00F5FF;
            }
            50% {
                border-color: transparent;
            }
        }

        /* ============================================================
                   TECH STACK BADGES
                   ============================================================ */
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1rem;
            margin-top: 0.6rem;
        }

        .tech-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.06);
            border-radius: 100px;
            padding: 0.45rem 1.2rem 0.45rem 1rem;
            font-size: 0.85rem;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.75);
            transition: all 0.25s ease;
            backdrop-filter: blur(4px);
        }

        .tech-badge i {
            font-size: 1.1rem;
            color: #00D9FF;
        }

        .tech-badge:hover {
            background: rgba(0, 245, 255, 0.06);
            border-color: rgba(0, 245, 255, 0.25);
            color: #FFFFFF;
            transform: translateY(-2px);
            box-shadow: 0 8px 20px -8px rgba(0, 245, 255, 0.10);
        }

        /* ============================================================
                   PROJECT CARDS
                   ============================================================ */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.5rem;
            margin-top: 0.6rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 1.5rem 1.4rem;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            background: rgba(255, 255, 255, 0.04);
            border-color: rgba(0, 245, 255, 0.15);
            transform: translateY(-4px);
            box-shadow: 0 16px 32px -12px rgba(0, 0, 0, 0.5);
        }

        .project-card .icon {
            font-size: 1.8rem;
            color: #00F5FF;
            margin-bottom: 0.6rem;
            display: block;
        }

        .project-card h4 {
            font-family: 'Space Grotesk', sans-serif;
            font-weight: 600;
            font-size: 1.1rem;
            color: #FFFFFF;
            margin-bottom: 0.3rem;
        }

        .project-card p {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.5);
            line-height: 1.5;
        }

        .project-card .tag {
            display: inline-block;
            margin-top: 0.7rem;
            font-size: 0.7rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            text-transform: uppercase;
            color: #00D9FF;
            background: rgba(0, 217, 255, 0.06);
            padding: 0.15rem 0.9rem;
            border-radius: 100px;
            border: 1px solid rgba(0, 217, 255, 0.06);
        }

        /* ============================================================
                   GITHUB WIDGETS – inline SVG / markdown‑compatible
                   ============================================================ */
        .gh-widget-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            align-items: center;
            justify-content: center;
            margin: 1.2rem 0 0.2rem;
        }

        .gh-widget-row img {
            max-width: 100%;
            height: auto;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            background: rgba(0, 0, 0, 0.2);
            transition: border-color 0.3s ease;
        }

        .gh-widget-row img:hover {
            border-color: rgba(0, 245, 255, 0.20);
        }

        .gh-widget-row .widget-wrap {
            flex: 1 1 200px;
            min-width: 140px;
            text-align: center;
        }

        .gh-widget-row .widget-wrap img {
            width: 100%;
            max-width: 400px;
        }

        /* ============================================================
                   CONTACT / SOCIAL
                   ============================================================ */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
            margin-top: 0.6rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.5rem 1.4rem;
            border-radius: 100px;
            font-size: 0.9rem;
            font-weight: 500;
            color: rgba(255, 255, 255, 0.6);
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.06);
            text-decoration: none;
            transition: all 0.25s ease;
            backdrop-filter: blur(4px);
        }

        .social-links a i {
            font-size: 1.1rem;
            color: #00D9FF;
        }

        .social-links a:hover {
            background: rgba(0, 245, 255, 0.06);
            border-color: rgba(0, 245, 255, 0.20);
            color: #FFFFFF;
            transform: translateY(-2px);
            box-shadow: 0 8px 20px -8px rgba(0, 245, 255, 0.08);
        }

        /* ============================================================
                   FOOTER WAVES (pure CSS)
                   ============================================================ */
        .footer-wave {
            position: relative;
            margin-top: 2.8rem;
            padding: 2.8rem 0 1.2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.03);
            text-align: center;
            overflow: hidden;
        }

        .footer-wave .wave-container {
            position: absolute;
            top: -2px;
            left: 0;
            width: 100%;
            height: 40px;
            overflow: hidden;
        }

        .footer-wave .wave-container svg {
            display: block;
            width: 100%;
            height: 100%;
        }

        .footer-wave .footer-content {
            position: relative;
            z-index: 2;
        }

        .footer-wave .footer-content p {
            color: rgba(255, 255, 255, 0.25);
            font-size: 0.85rem;
            letter-spacing: 0.3px;
        }

        .footer-wave .footer-content .heart {
            color: #8A2BE2;
        }

        /* ============================================================
                   MISC HELPERS
                   ============================================================ */
        .mt-1 {
            margin-top: 0.8rem;
        }
        .mt-2 {
            margin-top: 1.6rem;
        }
        .mb-1 {
            margin-bottom: 0.8rem;
        }
        .gap-2 {
            gap: 0.8rem;
        }
        .flex-wrap {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
        }
        .flex-center {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .w-full {
            width: 100%;
        }
        .text-center {
            text-align: center;
        }

        .divider {
            width: 100%;
            height: 1px;
            background: linear-gradient(90deg, transparent, rgba(0, 245, 255, 0.10), transparent);
            margin: 0.4rem 0 1.6rem;
        }

        .inline-code {
            font-family: 'Space Grotesk', monospace;
            background: rgba(255, 255, 255, 0.04);
            padding: 0.1rem 0.6rem;
            border-radius: 6px;
            font-size: 0.85rem;
            color: #00D9FF;
            border: 1px solid rgba(255, 255, 255, 0.04);
        }

        /* ============================================================
                   RESPONSIVE
                   ============================================================ */
        @media (max-width: 640px) {
            .glass {
                padding: 1.4rem 1.2rem 1.8rem;
            }
            .banner {
                padding: 2rem 1.4rem;
            }
            .banner h1 {
                font-size: 2.2rem;
            }
            .section-title {
                font-size: 1.5rem;
            }
            .project-grid {
                grid-template-columns: 1fr;
            }
            .typing-wrapper {
                font-size: 1rem;
            }
            .gh-widget-row .widget-wrap {
                flex: 1 1 100%;
            }
            .social-links a {
                padding: 0.4rem 1rem;
                font-size: 0.8rem;
            }
        }

        @media (max-width: 480px) {
            .banner-stats {
                flex-direction: column;
                gap: 0.6rem;
            }
            .banner .subhead {
                font-size: 0.95rem;
            }
            .tech-grid {
                gap: 0.5rem;
            }
            .tech-badge {
                font-size: 0.75rem;
                padding: 0.3rem 0.8rem;
            }
        }
    </style>
</head>

<body>

    <div class="container">

        <!-- ============================================================
        🌌 BANNER
        ============================================================ -->
        <header class="banner">
            <div class="banner-content">

                <span class="banner-badge">
                    <i class="fas fa-robot" style="margin-right:6px;"></i> AI · Data Science
                </span>

                <h1>Mohammed Ashraf</h1>

                <div class="subhead">
                    <i class="fas fa-graduation-cap" style="color:#00D9FF;margin-right:6px;"></i>
                    Fourth Year · <strong>AI &amp; Data Science</strong>
                </div>

                <!-- ⌨️ Typing Animation -->
                <div class="typing-wrapper">
                    <span class="static-text">⚡</span>
                    <span class="dynamic-text" id="typed-text">Transforming Data into Intelligence</span>
                    <span class="static-text" style="color:rgba(255,255,255,0.3);">— one model at a time.</span>
                </div>

                <div class="banner-tagline">
                    <i class="fas fa-brain" style="color:#8A2BE2;margin-right:8px;"></i>
                    Building intelligent solutions that create real‑world impact.
                </div>

                <div class="banner-stats">
                    <span class="stat-item">
                        <i class="fas fa-code"></i>
                        <strong>4+</strong> years coding
                    </span>
                    <span class="stat-item">
                        <i class="fas fa-project-diagram"></i>
                        <strong>12+</strong> projects
                    </span>
                    <span class="stat-item">
                        <i class="fas fa-rocket"></i>
                        <strong>AI</strong> · ML · DL · Flutter
                    </span>
                    <span class="stat-item">
                        <i class="fas fa-cloud"></i>
                        Cloud · DevOps
                    </span>
                </div>

            </div>
        </head

