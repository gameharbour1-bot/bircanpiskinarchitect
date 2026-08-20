<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Bircan Pişkin — Architecture</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #f7f7f5;
            color: #111;
            font-family: "Inter", Arial, sans-serif;
            font-weight: 300;
        }

        /* HEADER */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 28px 42px;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            z-index: 100;
            mix-blend-mode: difference;
            color: white;
        }

        .logo {
            font-size: 13px;
            line-height: 1.25;
            letter-spacing: .04em;
            text-transform: uppercase;
        }

        nav {
            display: flex;
            gap: 34px;
        }

        nav a {
            color: inherit;
            text-decoration: none;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: .08em;
        }

        nav a:hover {
            opacity: .5;
        }

        /* HERO */

        .hero {
            height: 100vh;
            min-height: 700px;
            position: relative;
            display: flex;
            align-items: flex-end;
            padding: 42px;
            overflow: hidden;
        }

        .hero-image {
            position: absolute;
            inset: 0;
            background:
                linear-gradient(
                    rgba(0,0,0,.08),
                    rgba(0,0,0,.18)
                ),
                url("https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?auto=format&fit=crop&w=2400&q=90")
                center center / cover no-repeat;
            transform: scale(1.01);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            color: white;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
        }

        .hero-title {
            font-size: clamp(42px, 6vw, 100px);
            line-height: .9;
            letter-spacing: -.055em;
            text-transform: uppercase;
        }

        .hero-info {
            text-align: right;
            font-size: 11px;
            line-height: 1.7;
            text-transform: uppercase;
            letter-spacing: .08em;
        }

        /* INTRO */

        .intro {
            padding: 160px 42px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
        }

        .intro-label {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: .1em;
        }

        .intro-text {
            font-size: clamp(25px, 3vw, 48px);
            line-height: 1.05;
            letter-spacing: -.035em;
            max-width: 750px;
        }

        /* PROJECTS */

        .projects {
            padding: 0 42px 160px;
        }

        .section-title {
            border-top: 1px solid #111;
            padding-top: 16px;
            margin-bottom: 55px;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: .1em;
        }

        .project {
            margin-bottom: 120px;
        }

        .project-image {
            width: 100%;
            height: 75vh;
            min-height: 500px;
            object-fit: cover;
            display: block;
            transition: transform .8s cubic-bezier(.2,.6,.2,1);
        }

        .project-link {
            overflow: hidden;
            display: block;
        }

        .project-link:hover .project-image {
            transform: scale(1.025);
        }

        .project-info {
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding-top: 18px;
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: .08em;
        }

        .project-meta {
            text-align: right;
        }

        /* FOOTER */

        footer {
            background: #111;
            color: #fff;
            padding: 120px 42px 40px;
        }

        .footer-title {
            font-size: clamp(45px, 8vw, 130px);
            line-height: .85;
            letter-spacing: -.06em;
            text-transform: uppercase;
            margin-bottom: 120px;
        }

        .footer-bottom {
            border-top: 1px solid #555;
            padding-top: 18px;
            display: flex;
            justify-content: space-between;
            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: .08em;
        }

        footer a {
            color: white;
            text-decoration: none;
        }

        /* MOBILE */

        @media (max-width: 700px) {

            header {
                padding: 22px;
            }

            nav {
                gap: 14px;
            }

            .hero {
                padding: 22px;
            }

            .hero-content {
                display: block;
            }

            .hero-title {
                margin-bottom: 25px;
            }

            .hero-info {
                text-align: left;
            }

            .intro {
                padding: 100px 22px;
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .projects {
                padding: 0 22px 100px;
            }

            .project-image {
                height: 55vh;
                min-height: 400px;
            }

            .project-info {
                grid-template-columns: 1fr;
                gap: 10px;
            }

            .project-meta {
                text-align: left;
            }

            footer {
                padding: 90px 22px 30px;
            }

            .footer-bottom {
                flex-direction: column;
                gap: 10px;
            }
        }

    </style>
</head>

<body>

<header>

    <div class="logo">
        Bircan Pişkin<br>
        Architecture
    </div>

    <nav>
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>

</header>


<main>

    <!-- HERO -->

    <section class="hero">

        <div class="hero-image"></div>

        <div class="hero-content">

            <h1 class="hero-title">
                Architecture<br>
                & Design
            </h1>

            <div class="hero-info">
                Bircan Pişkin<br>
                Architect<br>
                Istanbul / Türkiye
            </div>

        </div>

    </section>


    <!-- INTRO -->

    <section class="intro" id="about">

        <div class="intro-label">
            01 — About
        </div>

        <div class="intro-text">
            Bircan Pişkin Architecture is an independent architectural
            practice focusing on architecture, interior design and
            contemporary spatial experiences.
        </div>

    </section>


    <!-- PROJECTS -->

    <section class="projects" id="projects">

        <div class="section-title">
            02 — Selected Projects
        </div>


        <article class="project">

            <a href="#" class="project-link">

                <img
                    class="project-image"
                    src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=2400&q=90"
                    alt="Life Bakırköy"
                >

            </a>

            <div class="project-info">

                <div>
                    Life Bakırköy
                </div>

                <div class="project-meta">
                    Residential<br>
                    Istanbul / 2024
                </div>

            </div>

        </article>


        <article class="project">

            <a href="#" class="project-link">

                <img
                    class="project-image"
                    src="https://images.unsplash.com/photo-1600566753086-00f18fb6b3ea?auto=format&fit=crop&w=2400&q=90"
                    alt="Villa Project"
                >

            </a>

            <div class="project-info">

                <div>
                    Bodrum Villa
                </div>

                <div class="project-meta">
                    Residential<br>
                    Bodrum / Türkiye
                </div>

            </div>

        </article>


        <article class="project">

            <a href="#" class="project-link">

                <img
                    class="project-image"
                    src="https://images.unsplash.com/photo-1600607688969-a5bfcd646154?auto=format&fit=crop&w=2400&q=90"
                    alt="Interior Project"
                >

            </a>

            <div class="project-info">

                <div>
                    Interior Studies
                </div>

                <div class="project-meta">
                    Interior<br>
                    Istanbul / Türkiye
                </div>

            </div>

        </article>

    </section>

</main>


<footer id="contact">

    <div class="footer-title">
        Let's<br>
        Talk.
    </div>

    <div class="footer-bottom">

        <div>
            © 2026 Bircan Pişkin Architecture
        </div>

        <div>
            <a href="mailto:info@bircanpiskin.com">
                info@bircanpiskin.com
            </a>
        </div>

        <div>
            Istanbul / Türkiye
        </div>

    </div>

</footer>

</body>
</html>
