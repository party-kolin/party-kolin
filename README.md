<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Party Kolín | ...s námi to oslavíte</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #8cc63f;
            --text-dark: #1a1a1a;
            --text-gray: #4a4a4a;
            --bg-light: #fdfdfd;
            --border-color: #f0f0f0;
        }

        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            color: var(--text-dark);
            line-height: 1.5;
            background-color: #fff;
            scroll-behavior: smooth;
        }

        /* Navigace */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 3%;
            box-sizing: border-box;
        }

        nav img { height: 40px; }

        .nav-links {
            display: flex;
            gap: 15px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            white-space: nowrap;
            transition: color 0.3s;
        }

        .nav-links a:hover { color: var(--primary-color); }

        /* Hero Sekce - Opravený název fotky */
        .hero {
            height: 65vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.5)), url('Party 1200x628.jpg') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 60px;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: clamp(1.8rem, 7vw, 4rem);
            font-weight: 700;
            margin: 0;
        }

        .hero h1 span { color: var(--primary-color); }

        /* Kontejnery a sekce */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 60px 20px;
        }

        .section-title { text-align: center; margin-bottom: 40px; }
        .section-title h2 { font-size: 1.8rem; margin-bottom: 10px; }
        .section-title .divider { width: 50px; height: 3px; background: var(--primary-color); margin: 0 auto; }

        /* Ceník - Grid */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .card {
            background: #fff;
            padding: 30px;
            border-radius: 8px;
            border: 1px solid var(--border-color);
            text-align: center;
            display: flex;
            flex-direction: column;
        }

        .card h3 { font-size: 1.2rem; margin: 15px 0; }
        .card .price { font-size: 1.6rem; font-weight: 700; margin-bottom: 15px; }
        
        .card-list { list-style: none; padding: 0; margin: 15px 0; text-align: left; font-size: 0.9rem; flex-grow: 1; }
        .card-list li { margin-bottom: 8px; padding-left: 20px; position: relative; }
        .card-list li::before { content: "✓"; color: var(--primary-color); position: absolute; left: 0; font-weight: bold; }

        .btn-main {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 12px 20px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 600;
        }

        /* Footer */
        footer { background: #fafafa; border-top: 1px solid var(--border-color); padding: 40px 20px; text-align: center; }
        .contact-large { font-size: 1.5rem; font-weight: 700; display: block; margin: 10px 0; text-decoration: none; color: var(--text-dark); }

        /* Mobilní optimalizace pro lištu */
        @media (max-width: 900px) {
            .nav-links { gap: 10px; }
            .nav-links a { font-size: 0.6rem; }
        }

        @media (max-width: 600px) {
            nav { flex-direction: column; padding: 10px; }
            .nav-links { flex-wrap: wrap; justify-content: center; margin-top: 10px; }
            .nav-links a { margin: 2px 5px; }
            .hero { height: 50vh; }
        }
    </style>
</head>
<body>

    <nav>
        <img src="logo.png" alt="Party Kolín">
        <div class="nav-links">
            <a href="#sluzby">Naše služby</a>
            <a href="#vybaveni">Vybavení (ceník)</a>
            <a href="#galerie">Fotogalerie</a>
            <a href="#kontakt">Kontakt</a>
            <a href="#podminky">Podmínky</a>
        </div>
    </nav>

    <header class="hero">
        <h1>...s námi to <span>oslavíte</span>.</h1>
    </header>

    <div id="sluzby" class="container">
        <div class="section-title">
            <h2>Naše služby</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; max-width: 800px; margin: 0 auto; color: var(--text-gray);">
            Zajišťujeme kompletní zastřešení pro vaše akce. Od malých rodinných oslav až po velké svatby. 
            Stany dovezeme, postavíme a po akci opět odvezeme, abyste se mohli soustředit jen na zábavu.
        </p>
    </div>

    <div id="vybaveni" style="background: var(--bg-light);">
        <div class="container">
            <div class="section-title">
                <h2>Vybavení (ceník)</h2>
                <div class="divider"></div>
            </div>
            <div class="grid">
                <div class="card">
                    <h3>Párty stan 6x12m</h3>
                    <ul class="card-list">
                        <li>Kapacita 50-80 osob</li>
                        <li>Robustní konstrukce</li>
                    </ul>
                    <div class="price">10 890 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT</a>
                </div>
                <div class="card">
                    <h3>Nůžkový stan 3x6m</h3>
                    <ul class="card-list">
                        <li>Postavení do 5 min</li>
                        <li>Ideální pro 20 osob</li>
                    </ul>
                    <div class="price">1 900 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT</a>
                </div>
                <div class="card">
                    <h3>Pivní set</h3>
                    <ul class="card-list">
                        <li>Stůl + 2 lavice</li>
                        <li>Pro 6-8 osob</li>
                    </ul>
                    <div class="price">330 Kč <span>s DPH</span></div>
                    <a href="#kontakt" class="btn-main">POPTAT</a>
                </div>
            </div>
        </div>
    </div>

    <div id="galerie" class="container">
        <div class="section-title">
            <h2>Fotogalerie</h2>
            <div class="divider"></div>
        </div>
        <p style="text-align: center; color: var(--text-gray);">Zde brzy najdete fotografie z našich realizací.</p>
    </div>

    <div id="podminky" style="background: var(--bg-light);">
        <div class="container">
            <div class="section-title">
                <h2>Obchodní podmínky</h2>
                <div class="divider"></div>
            </div>
            <p style="text-align: center; color: var(--text-gray);">Obsah obchodních podmínek připravujeme.</p>
        </div>
    </div>

    <footer id="kontakt">
        <div class="container" style="padding: 0;">
            <h2>Kontaktujte nás</h2>
            <p>Kolín a široké okolí</p>
            <a href="tel:+420123456789" class="contact-large">+420 123 456 789</a>
            <a href="mailto:info@party-kolin.cz" style="color: var(--primary-color); font-weight: bold; text-decoration: none;">info@party-kolin.cz</a>
            <p style="margin-top: 40px; font-size: 0.7rem; color: #aaa;">&copy; 2026 Party-Kolin.cz</p>
        </div>
    </footer>

</body>
</html>
