<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OLSIL TOUR | Agencia de Viajes Jalisco</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* --- ESTILOS GENERALES --- */
        :root {
            --primary-color: #0B4F35; /* Verde Agave Oscuro */
            --secondary-color: #F4A900; /* Dorado/Amarillo Flyer */
            --text-color: #333;
            --light-bg: #f4f7f6;
            --white: #ffffff;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--light-bg);
        }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }

        /* --- HEADER / BARRA DE NAVEGACIÓN --- */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(5px);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 20px;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--primary-color);
            letter-spacing: 1px;
        }
        
        .logo span { color: var(--secondary-color); }

        .nav-links { display: flex; gap: 25px; }
        .nav-links a { font-weight: 600; transition: color 0.3s; font-size: 0.9rem; text-transform: uppercase;}
        .nav-links a:hover { color: var(--secondary-color); }

        .btn-cta-nav {
            background-color: var(--secondary-color);
            color: var(--white) !important;
            padding: 8px 20px;
            border-radius: 50px;
            transition: transform 0.3s, background-color 0.3s;
        }
        .btn-cta-nav:hover { transform: translateY(-2px); background-color: #e09b00; }

        /* --- HERO SECTION (Imagen Principal) --- */
        .hero {
            height: 85vh;
            /* IMAGEN DE FONDO PRINCIPAL (Campo de Agave) */
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1570530732890-0b67568571bd?q=80&w=1920&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            background-attachment: fixed; /* Efecto Parallax */
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
            margin-top: 60px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            line-height: 1.2;
        }
        
        .hero-content span { color: var(--secondary-color); }

        .hero p { font-size: 1.3rem; margin-bottom: 2.5rem; opacity: 0.9; }

        .btn-hero {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 15px 35px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            transition: all 0.3s;
            border: 2px solid var(--primary-color);
        }
        .btn-hero:hover { background-color: transparent; border-color: var(--white); }

        /* --- SECCIÓN DE TOURS --- */
        .events { max-width: 1200px; margin: 5rem auto; padding: 0 20px; }
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-color);
            font-size: 2.5rem;
            position: relative;
        }
        .section-title::after {
            content: ''; display: block; width: 60px; height: 4px; background: var(--secondary-color); margin: 10px auto 0;
        }

        .card-container {
            display: flex;
            justify-content: center;
            gap: 2.5rem;
            flex-wrap: wrap;
        }

        .tour-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            width: 360px;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid #eee;
        }

        .tour-card:hover { transform: translateY(-10px); box-shadow: 0 15px 40px rgba(0,0,0,0.15); }

        /* Estilo para las imágenes de las tarjetas */
        .card-img {
            height: 250px; /* Aumenté un poco la altura para que el flyer se vea mejor */
            background-color: #ddd;
            background-size: cover;
            /* background-position: center;  <- Cambiado para el flyer */
            background-position: top center; /* Para que se vea la parte de arriba del flyer */
            position: relative;
        }

        .card-content { padding: 25px; }

        .tag {
            background-color: var(--secondary-color);
            color: var(--primary-color);
            padding: 5px 12px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            display: inline-block;
            margin-bottom: 10px;
        }

        .card-title { margin: 10px 0; font-size: 1.5rem; color: var(--text-color); }

        .card-details { list-style: none; margin-bottom: 25px; color: #555; font-size: 0.95rem; }
        .card-details li { margin-bottom: 10px; display: flex; align-items: center; }
        .card-details li::before { content: '✓'; color: var(--secondary-color); margin-right
