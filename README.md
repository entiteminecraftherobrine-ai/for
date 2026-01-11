[open.html](https://github.com/user-attachments/files/24553415/open.html)
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Liam Engine Titan - Officiel</title>
    <style>
        :root {
            --primary: #007bff;
            --primary-hover: #0056b3;
            --bg-dark: #0a0a0a;
            --card-bg: #1a1a1a;
            --text-light: #e0e0e0;
        }

        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* Navbar style Unity */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            background: rgba(0, 0, 0, 0.95);
            position: fixed;
            width: 90%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid #333;
        }

        .logo { font-weight: bold; font-size: 1.5rem; letter-spacing: 1px; }
        .logo span { color: var(--primary); }

        .menu a {
            color: #999;
            text-decoration: none;
            margin-left: 25px;
            font-size: 0.9rem;
            transition: 0.3s;
            position: relative;
        }

        .menu a:hover { color: white; }

        /* Animation de la ligne sous les liens */
        .menu a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: var(--primary);
            transition: width 0.3s;
        }
        .menu a:hover::after { width: 100%; }

        /* Section Hero */
        .hero {
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: radial-gradient(circle at center, #1a1a1a 0%, #000 100%);
            padding: 0 20px;
        }

        .hero h1 { font-size: 4rem; margin: 0; color: white; }
        .hero p { font-size: 1.2rem; color: #888; max-width: 600px; }

        /* BOUTON TÉLÉCHARGER AVEC ANIMATION REBOND */
        .btn-download {
            background: var(--primary);
            color: white;
            padding: 20px 50px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            margin-top: 30px;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 10px 20px rgba(0, 123, 255, 0.2);
            display: inline-block;
        }

        .btn-download:hover {
            transform: scale(1.05) translateY(-5px);
            background: var(--primary-hover);
            box-shadow: 0 15px 30px rgba(0, 123, 255, 0.4);
        }

        .btn-download:active { transform: scale(0.98); }

        /* ASSET STORE GRID */
        .asset-store { padding: 100px 5%; background: #050505; }
        .asset-store h2 { font-size: 2.5rem; text-align: center; margin-bottom: 50px; }

        .asset-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .asset-card {
            background: var(--card-bg);
            border-radius: 10px;
            padding: 0;
            border: 1px solid #222;
            transition: 0.4s;
            overflow: hidden;
        }

        .asset-card:hover {
            transform: translateY(-15px);
            border-color: var(--primary);
            box-shadow: 0 10px 40px rgba(0, 123, 255, 0.1);
        }

        .asset-img {
            width: 100%;
            height: 180px;
            background: #222;
            transition: 0.4s;
        }

        .asset-card:hover .asset-img { filter: brightness(1.2); }

        .asset-content { padding: 25px; }

        /* BOUTONS ASSETS ANIMÉS */
        .btn-asset {
            display: block;
            width: 100%;
            padding: 12px 0;
            text-align: center;
            background: transparent;
            border: 1px solid #444;
            color: white;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 500;
            transition: 0.3s;
        }

        .btn-asset:hover {
            background: var(--primary);
            border-color: var(--primary);
            transform: scale(1.02);
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">LIAM <span>ENGINE</span></div>
        <div class="menu">
            <a href="#">Jeux</a>
            <a href="#">Industrie</a>
            <a href="#assets">Asset Store</a>
            <a href="#">Ressources</a>
            <a href="#">Apprentissage</a>
        </div>
    </nav>

    <header class="hero">
        <h1>Liam Engine Titan</h1>
        <p>Téléchargez la plateforme de développement la plus puissante pour vos projets .m3d</p>
        
        <a href="LiamEngineInstaller.exe" class="btn-download">Téléchargement pour Windows</a>
        <p style="font-size: 0.8rem; margin-top: 15px;">Version 1.0.0 Stable</p>
    </header>

    <section class="asset-store" id="assets">
        <h2>Asset Store</h2>
        <div class="asset-grid">
            
            <div class="asset-card">
                <div class="asset-img" style="background: linear-gradient(45deg, #111, #333);"></div>
                <div class="asset-content">
                    <h3>Character Controller</h3>
                    <p>Scripts ZQSD et Saut pro.</p>
                    <a href="#" class="btn-asset">Télécharger l'Asset</a>
                </div>
            </div>

            <div class="asset-card">
                <div class="asset-img" style="background: linear-gradient(45deg, #001, #004);"></div>
                <div class="asset-content">
                    <h3>Skybox Titan</h3>
                    <p>Pack de ciels réalistes 4K.</p>
                    <a href="#" class="btn-asset">Télécharger l'Asset</a>
                </div>
            </div>

            <div class="asset-card">
                <div class="asset-img" style="background: linear-gradient(45deg, #220, #440);"></div>
                <div class="asset-content">
                    <h3>Pack 3D Models</h3>
                    <p>150 objets pour votre monde.</p>
                    <a href="#" class="btn-asset">Télécharger l'Asset</a>
                </div>
            </div>

        </div>
    </section>

</body>
</html>
