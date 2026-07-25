<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>kllipe.web | Criação de Sites e Landing Pages Profissionais</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-dark: #0f172a;
            --bg-card: #1e293b;
            --bg-card-hover: #334155;
            --primary-cyan: #06b6d4;
            --primary-emerald: #10b981;
            --accent-gradient: linear-gradient(135deg, #06b6d4 0%, #10b981 100%);
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --border-color: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Background Animated Glow Blobs */
        .glow-blob {
            position: absolute;
            width: 450px;
            height: 450px;
            background: radial-gradient(circle, rgba(6, 182, 212, 0.25) 0%, rgba(16, 185, 129, 0) 70%);
            border-radius: 50%;
            filter: blur(60px);
            z-index: -1;
            animation: floatGlow 10s ease-in-out infinite alternate;
        }

        .glow-blob-2 {
            position: absolute;
            top: 60%;
            right: 5%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(16, 185, 129, 0.2) 0%, rgba(6, 182, 212, 0) 70%);
            border-radius: 50%;
            filter: blur(70px);
            z-index: -1;
            animation: floatGlow2 12s ease-in-out infinite alternate;
        }

        @keyframes floatGlow {
            0% { transform: translate(-30%, -20%) scale(1); }
            100% { transform: translate(10%, 20%) scale(1.2); }
        }

        @keyframes floatGlow2 {
            0% { transform: translate(10%, -10%) scale(1); }
            100% { transform: translate(-20%, 30%) scale(1.3); }
        }

        /* Header / Navbar */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.1rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            color: #ffffff;
            display: flex;
            align-items: center;
            gap: 8px;
            text-decoration: none;
            transition: transform 0.3s ease;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        .logo span {
            background: var(--accent-gradient);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 4s ease infinite;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease, transform 0.2s ease;
            display: inline-block;
        }

        .nav-links a:hover {
            color: var(--primary-cyan);
            transform: translateY(-2px);
        }

        .btn-header {
            background: var(--accent-gradient);
            background-size: 200% 200%;
            color: #0f172a;
            padding: 0.6rem 1.4rem;
            border-radius: 50px;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            animation: gradientShift 6s ease infinite;
        }

        .btn-header:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 10px 25px -5px rgba(6, 182, 212, 0.5);
        }

        /* Keyframes for Gradient Animations */
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Hero Section Animation */
        .hero {
            padding: 9rem 2rem 5rem;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            animation: fadeInUp 1s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .tag-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(6, 182, 212, 0.1);
            border: 1px solid rgba(6, 182, 212, 0.3);
            color: var(--primary-cyan);
            padding: 0.4rem 1.2rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            animation: pulseBadge 2.5s infinite ease-in-out;
        }

        @keyframes pulseBadge {
            0%, 100% { box-shadow: 0 0 0 0 rgba(6, 182, 212, 0.4); }
            50% { box-shadow: 0 0 0 12px rgba(6, 182, 212, 0); }
        }

        .hero h1 {
            font-size: 3.2rem;
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            letter-spacing: -1px;
        }

        .hero h1 .highlight {
            background: var(--accent-gradient);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 5s ease infinite;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 700px;
            margin: 0 auto 2.5rem;
        }

        .hero-cta {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        /* Pulse / Shimmer CTA Button */
        .btn-primary {
            background: var(--accent-gradient);
            background-size: 200% 200%;
            color: #0f172a;
            padding: 1rem 2.2rem;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            animation: gradientShift 4s ease infinite, btnPulse 3s infinite;
        }

        @keyframes btnPulse {
            0%, 100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(16, 185, 129, 0.4); }
            50% { transform: scale(1.03); box-shadow: 0 0 25px 8px rgba(16, 185, 129, 0.2); }
        }

        .btn-primary:hover {
            transform: translateY(-4px) scale(1.05) !important;
            box-shadow: 0 15px 35px -5px rgba(16, 185, 129, 0.6) !important;
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 1rem 2.2rem;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.12);
            border-color: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .btn-price {
            background: rgba(6, 182, 212, 0.1);
            border: 1px solid var(--primary-cyan);
            color: var(--primary-cyan);
            padding: 1rem 2.2rem;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-price:hover {
            background: rgba(6, 182, 212, 0.2);
            border-color: var(--primary-cyan);
            color: #ffffff;
            transform: translateY(-3px);
            box-shadow: 0 10px 25px -5px rgba(6, 182, 212, 0.3);
        }

        /* Features Section */
        .features {
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .feature-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            padding: 2rem;
            border-radius: 16px;
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .feature-card:hover {
            transform: translateY(-8px);
            border-color: var(--primary-cyan);
            box-shadow: 0 20px 30px -10px rgba(6, 182, 212, 0.2);
        }

        .feature-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            background: rgba(6, 182, 212, 0.1);
            color: var(--primary-cyan);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 1.2rem;
            transition: transform 0.4s ease, background 0.4s ease;
        }

        .feature-card:hover .feature-icon {
            transform: scale(1.15) rotate(5deg);
            background: rgba(6, 182, 212, 0.25);
        }

        .feature-card h3 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
        }

        .feature-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Portfolio Section */
        .portfolio {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3.5rem;
        }

        .section-title h2 {
            font-size: 2.3rem;
            font-weight: 800;
            margin-bottom: 0.8rem;
        }

        .section-title p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .portfolio-card {
            background: var(--bg-card);
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid var(--border-color);
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .portfolio-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-emerald);
            box-shadow: 0 25px 45px -15px rgba(16, 185, 129, 0.25);
        }

        .portfolio-img {
            width: 100%;
            height: 220px;
            background-size: cover;
            background-position: center;
            position: relative;
            transition: transform 0.5s ease;
        }

        .portfolio-card:hover .portfolio-img {
            transform: scale(1.05);
        }

        .portfolio-info {
            padding: 1.5rem;
            position: relative;
            z-index: 2;
            background: var(--bg-card);
        }

        .portfolio-info span {
            color: var(--primary-cyan);
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .portfolio-info h3 {
            font-size: 1.3rem;
            margin: 0.4rem 0 0.8rem;
        }

        .portfolio-info p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 1.2rem;
        }

        .portfolio-link {
            color: var(--primary-cyan);
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: gap 0.3s ease;
        }

        .portfolio-card:hover .portfolio-link {
            gap: 14px;
            color: var(--primary-emerald);
        }

        /* Promo Pricing Section */
        .pricing {
            padding: 6rem 2rem;
            background: linear-gradient(180deg, var(--bg-dark) 0%, #0b1120 100%);
            position: relative;
        }

        .pricing-card {
            max-width: 650px;
            margin: 0 auto;
            background: var(--bg-card);
            border: 2px solid var(--primary-emerald);
            border-radius: 24px;
            padding: 3rem 2.5rem;
            text-align: center;
            position: relative;
            box-shadow: 0 0 50px rgba(16, 185, 129, 0.15);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: cardGlow 4s infinite alternate;
        }

        @keyframes cardGlow {
            0% { box-shadow: 0 0 30px rgba(16, 185, 129, 0.15); }
            100% { box-shadow: 0 0 60px rgba(6, 182, 212, 0.3); }
        }

        .pricing-card:hover {
            transform: translateY(-5px);
        }

        .promo-badge {
            position: absolute;
            top: -18px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--accent-gradient);
            background-size: 200% 200%;
            color: #0f172a;
            font-weight: 800;
            font-size: 0.9rem;
            padding: 0.4rem 1.5rem;
            border-radius: 50px;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 4px 15px rgba(16, 185, 129, 0.3);
            animation: gradientShift 3s ease infinite;
        }

        .discount-tag {
            display: inline-block;
            background: rgba(239, 68, 68, 0.2);
            color: #ef4444;
            border: 1px solid rgba(239, 68, 68, 0.3);
            font-weight: 700;
            font-size: 0.95rem;
            padding: 0.3rem 1rem;
            border-radius: 50px;
            margin-top: 1rem;
            margin-bottom: 1rem;
            animation: flashBadge 2s infinite;
        }

        @keyframes flashBadge {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.6; }
        }

        .price-container {
            margin: 1.5rem 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }

        .old-price {
            font-size: 1.5rem;
            color: var(--text-muted);
            text-decoration: line-through;
        }

        .current-price {
            font-size: 3.5rem;
            font-weight: 800;
            color: #ffffff;
        }

        .current-price span {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--primary-emerald);
        }

        .pricing-features {
            list-style: none;
            text-align: left;
            max-width: 420px;
            margin: 2rem auto;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .pricing-features li {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #e2e8f0;
            font-size: 1rem;
        }

        .pricing-features li i {
            color: var(--primary-emerald);
            font-size: 1.1rem;
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-color);
            padding: 3rem 2rem;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .pricing-card {
                padding: 2.5rem 1.5rem;
            }

            .current-price {
                font-size: 2.8rem;
            }
        }
    </style>
</head>
<body>

    <!-- Background Glowing Animations -->
    <div class="glow-blob" style="top: 10%; left: 5%;"></div>
    <div class="glow-blob-2"></div>

    <!-- Header -->
    <header>
        <a href="#" class="logo">
            kllipe<span>.web</span>
        </a>
        <ul class="nav-links">
            <li><a href="#vantagens">Vantagens</a></li>
            <li><a href="#exemplos">Exemplos</a></li>
            <li><a href="#preco">Promoção</a></li>
        </ul>
        <a href="https://wa.me/5511921934699?text=Ol%C3%A1%2C%20vi%20o%20seu%20site%20e%20quero%20aproveitar%20a%20promo%C3%A7%C3%A3o%20do%20Primeiro%20Site!" target="_blank" class="btn-header">
            <i class="fa-brands fa-whatsapp"></i> Falar no WhatsApp
        </a>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="tag-badge">
            <i class="fa-solid fa-rocket"></i> Sites & Landing Pages de Alta Conversão
        </div>
        <h1>Transforme seguidores em clientes com um <span class="highlight">Site Profissional</span></h1>
        <p>Desenvolvimento web moderno, rápido e adaptado para celulares. A estrutura que faltava para passar credibilidade e vender mais no seu negócio.</p>
        <div class="hero-cta">
            <a href="https://wa.me/5511921934699?text=Ol%C3%A1%2C%20quero%20aproveitar%20a%20promo%C3%A7%C3%A3o%20de%20R%2449%2C99!" target="_blank" class="btn-primary">
                <i class="fa-brands fa-whatsapp"></i> Garantir Meu Site Agora
            </a>
            <a href="#preco" class="btn-price">
                <i class="fa-solid fa-tag"></i> Ver Preços
            </a>
            <a href="#exemplos" class="btn-secondary">Ver Exemplos</a>
        </div>
    </section>

    <!-- Features -->
    <section class="features" id="vantagens">
        <div class="feature-card">
            <div class="feature-icon"><i class="fa-solid fa-mobile-screen-button"></i></div>
            <h3>100% Responsivo</h3>
            <p>Seu site abrirá perfeito em qualquer dispositivo, seja no celular, tablet ou computador.</p>
        </div>
        <div class="feature-card">
            <div class="feature-icon"><i class="fa-brands fa-whatsapp"></i></div>
            <h3>Foco em Conversão</h3>
            <p>Botões estratégicos direcionando os visitantes diretamente para o seu WhatsApp de vendas.</p>
        </div>
        <div class="feature-card">
            <div class="feature-icon"><i class="fa-solid fa-bolt"></i></div>
            <h3>Carregamento Rápido</h3>
            <p>Código limpo e otimizado para que seu cliente não perca tempo esperando a página carregar.</p>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="exemplos">
        <div class="section-title">
            <h2>Modelos & Exemplos de Sites</h2>
            <p>Conheça alguns formatos prontos para elevar o nível do seu negócio</p>
        </div>
        <div class="portfolio-grid">
            <!-- Project 1 -->
            <div class="portfolio-card">
                <div style="overflow: hidden;">
                    <div class="portfolio-img" style="background: linear-gradient(180deg, rgba(15,23,42,0.2), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?q=80&w=800&auto=format&fit=crop');"></div>
                </div>
                <div class="portfolio-info">
                    <span>Fitness / Saúde</span>
                    <h3>Landing Page para Personal / Academia</h3>
                    <p>Apresentação de planos, depoimentos de alunos e botão direto para agendamento de aulas experimentais.</p>
                    <a href="https://wa.me/5511921934699?text=Gostei%20do%20modelo%20para%20Personal/Academia" target="_blank" class="portfolio-link">Quero um assim <i class="fa-solid fa-arrow-right"></i></a>
                </div>
            </div>
            <!-- Project 2 -->
            <div class="portfolio-card">
                <div style="overflow: hidden;">
                    <div class="portfolio-img" style="background: linear-gradient(180deg, rgba(15,23,42,0.2), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1503951914875-452162b0f3f1?q=80&w=800&auto=format&fit=crop');"></div>
                </div>
                <div class="portfolio-info">
                    <span>Beleza & Estética</span>
                    <h3>Site para Barbearia ou Salão</h3>
                    <p>Cardápio de serviços, fotos dos cortes/trabalhos e integração para agendamento rápido de horários.</p>
                    <a href="https://wa.me/5511921934699?text=Gostei%20do%20modelo%20para%20Barbearia" target="_blank" class="portfolio-link">Quero um assim <i class="fa-solid fa-arrow-right"></i></a>
                </div>
            </div>
            <!-- Project 3 -->
            <div class="portfolio-card">
                <div style="overflow: hidden;">
                    <div class="portfolio-img" style="background: linear-gradient(180deg, rgba(15,23,42,0.2), rgba(15,23,42,0.9)), url('https://images.unsplash.com/photo-1556742049-0a670f4a4591?q=80&w=800&auto=format&fit=crop');"></div>
                </div>
                <div class="portfolio-info">
                    <span>Comércio & Serviços</span>
                    <h3>Página de Vendas / Autônomo</h3>
                    <p>Ideal para prestadores de serviços apresentarem seu trabalho, história e tirarem dúvidas de clientes.</p>
                    <a href="https://wa.me/5511921934699?text=Gostei%20do%20modelo%20para%20Aut%C3%B4nomos" target="_blank" class="portfolio-link">Quero um assim <i class="fa-solid fa-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="pricing" id="preco">
        <div class="section-title">
            <h2>Oportunidade Especial</h2>
            <p>Invista na presença digital do seu negócio por uma condição inédita</p>
        </div>

        <div class="pricing-card">
            <div class="promo-badge">🔥 Oferta do Primeiro Site</div>
            <div class="discount-tag">87,5% DE DESCONTO</div>
            
            <h3>Landing Page Profissional Completa</h3>
            <p style="color: var(--text-muted); font-size: 0.95rem; margin-top: 0.5rem;">Exclusivo para o primeiro projeto fechado do mês!</p>

            <div class="price-container">
                <span class="old-price">R$ 400</span>
                <span class="current-price">R$ 49<span>,99</span></span>
            </div>

            <ul class="pricing-features">
                <li><i class="fa-solid fa-circle-check"></i> Design Exclusivo e Moderno</li>
                <li><i class="fa-solid fa-circle-check"></i> Botão direto para o seu WhatsApp</li>
                <li><i class="fa-solid fa-circle-check"></i> Adaptado para Celular (Responsivo)</li>
                <li><i class="fa-solid fa-circle-check"></i> Seção de Serviços/Produtos</li>
                <li><i class="fa-solid fa-circle-check"></i> Entrega Rápida em poucos dias</li>
            </ul>

            <a href="https://wa.me/5511921934699?text=Quero%20aproveitar%20o%20desconto%20de%2087.5%25%20no%20meu%20primeiro%20site%20por%20R%2449%2C99!" target="_blank" class="btn-primary" style="width: 100%; justify-content: center; margin-top: 1rem;">
                <i class="fa-brands fa-whatsapp"></i> Quero meu site por R$ 49,99
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 <strong>kllipe.web</strong>. Todos os direitos reservados.</p>
        <p style="margin-top: 0.5rem; font-size: 0.8rem;">Desenvolvimento de sites de alta conversão.</p>
    </footer>

</body>
</html>
