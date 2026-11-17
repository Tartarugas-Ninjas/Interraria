# Introdução
<!DOCTYPE html>
<html lang="pt-BR" data-bs-theme="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plataforma Cultural Jovem - Arte, Música e Oportunidades</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800;900&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <style>

        :root {
            --pcj-primary: #7928CA;
            --pcj-secondary: #FF0080;
            --pcj-accent: #00F2FE;
            --pcj-accent-green: #10B981;
            --pcj-gradient: linear-gradient(135deg, #7928CA 0%, #FF0080 100%);
            --pcj-gradient-glow: linear-gradient(135deg, rgba(121, 40, 202, 0.4) 0%, rgba(255, 0, 128, 0.4) 100%);
            --pcj-glass: rgba(22, 27, 46, 0.75);
            --pcj-glass-border: rgba(255, 255, 255, 0.12);
            --pcj-bg: #0b0e17;
            --pcj-card-bg: #141824;
            --pcj-text: #f8fafc;
            --pcj-muted: #94a3b8;
            --pcj-radius-lg: 20px;
            --pcj-radius-md: 14px;
            --pcj-radius-sm: 8px;
            --font-heading: 'Outfit', sans-serif;
            --font-body: 'Plus Jakarta Sans', sans-serif;
        }

        [data-bs-theme="light"] {
            --pcj-bg: #f8fafc;
            --pcj-card-bg: #ffffff;
            --pcj-glass: rgba(255, 255, 255, 0.85);
            --pcj-glass-border: rgba(0, 0, 0, 0.08);
            --pcj-text: #0f172a;
            --pcj-muted: #64748b;
        }

        body {
            font-family: var(--font-body);
            background-color: var(--pcj-bg);
            color: var(--pcj-text);
            transition: background-color 0.3s ease, color 0.3s ease;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6, .navbar-brand {
            font-family: var(--font-heading);
        }

        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--pcj-bg);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--pcj-primary);
            border-radius: 4px;
        }
        .glass-nav {
            background: var(--pcj-glass);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--pcj-glass-border);
        }

        .glass-card {
            background: var(--pcj-card-bg);
            border: 1px solid var(--pcj-glass-border);
            border-radius: var(--pcj-radius-lg);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .glass-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 40px rgba(121, 40, 202, 0.25);
            border-color: rgba(255, 0, 128, 0.4);
        }

        .text-gradient {
            background: var(--pcj-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .text-gradient-cyan {
            background: linear-gradient(135deg, #00F2FE 0%, #4FACFE 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .ticker-bar {
            background: var(--pcj-gradient);
            color: #fff;
            font-size: 0.85rem;
            font-weight: 600;
            padding: 6px 0;
        }

        .btn-gradient {
            background: var(--pcj-gradient);
            color: #ffffff !important;
            border: none;
            border-radius: 50px;
            font-weight: 700;
            padding: 10px 24px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 0, 128, 0.3);
        }

        .btn-gradient:hover {
            transform: scale(1.04);
            box-shadow: 0 8px 25px rgba(255, 0, 128, 0.5);
            color: #fff;
        }

        .btn-outline-custom {
            border: 2px solid var(--pcj-primary);
            color: var(--pcj-text);
            border-radius: 50px;
            font-weight: 600;
            padding: 8px 22px;
            transition: all 0.3s ease;
        }

        .btn-outline-custom:hover {
            background: var(--pcj-gradient);
            border-color: transparent;
            color: #fff !important;
        }

        .badge-category {
            background: rgba(121, 40, 202, 0.15);
            color: #d8b4fe;
            border: 1px solid rgba(121, 40, 202, 0.3);
            border-radius: 50px;
            padding: 6px 14px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .hero-section {
            position: relative;
            padding: 100px 0 70px 0;
            background: radial-gradient(circle at 10% 20%, rgba(121, 40, 202, 0.25) 0%, transparent 40%),
                        radial-gradient(circle at 90% 80%, rgba(255, 0, 128, 0.2) 0%, transparent 40%);
        }

        .hero-shape {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            z-index: -1;
            opacity: 0.5;
        }

        .shape-1 {
            width: 300px;
            height: 300px;
            background: var(--pcj-primary);
            top: 10%;
            left: 5%;
        }

        .shape-2 {
            width: 350px;
            height: 350px;
            background: var(--pcj-secondary);
            bottom: 10%;
            right: 5%;
        }

        .filter-pill {
            background: var(--pcj-card-bg);
            border: 1px solid var(--pcj-glass-border);
            color: var(--pcj-text);
            padding: 8px 20px;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.25s ease;
            user-select: none;
            white-space: nowrap;
        }

        .filter-pill.active, .filter-pill:hover {
            background: var(--pcj-gradient);
            color: #ffffff;
            border-color: transparent;
            box-shadow: 0 4px 15px rgba(121, 40, 202, 0.4);
        }

        .card-img-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: var(--pcj-radius-lg) var(--pcj-radius-lg) 0 0;
            height: 220px;
        }

        .card-img-wrapper img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .glass-card:hover .card-img-wrapper img {
            transform: scale(1.08);
        }

        .fav-btn {
            position: absolute;
            top: 12px;
            right: 12px;
            background: rgba(15, 23, 42, 0.7);
            backdrop-filter: blur(8px);
            border: none;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s ease;
            z-index: 2;
        }

        .fav-btn:hover, .fav-btn.active {
            background: #FF0080;
            color: #fff;
            transform: scale(1.1);
        }

        .edital-card {
            border-left: 5px solid var(--pcj-secondary);
        }

        .artist-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--pcj-secondary);
            box-shadow: 0 0 15px rgba(255, 0, 128, 0.4);
        }

        body.high-contrast {
            --pcj-bg: #000000 !important;
            --pcj-card-bg: #111111 !important;
            --pcj-text: #ffff00 !important;
            --pcj-muted: #ffffff !important;
            --pcj-glass-border: #ffff00 !important;
        }
        body.high-contrast .glass-card {
            border: 2px solid #ffff00 !important;
        }
        body.high-contrast .btn-gradient {
            background: #ffff00 !important;
            color: #000000 !important;
        }

        .skeleton {
            background: linear-gradient(90deg, var(--pcj-card-bg) 25%, rgba(255,255,255,0.08) 50%, var(--pcj-card-bg) 75%);
            background-size: 200% 100%;
            animation: loading 1.5s infinite;
            border-radius: var(--pcj-radius-sm);
        }
        @keyframes loading {
            0% { background-position: 200% 0; }
            100% { background-position: -200% 0; }
        }

        .toast-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1100;
        }
    </style>
</head>
<body>

    <div class="ticker-bar text-center">
        <div class="container d-flex justify-content-between align-items-center">
            <span class="d-none d-md-inline"><i class="fa-solid fa-bullhorn me-2"></i><strong>EDITAIS 2026:</strong> R$ 500 mil em bolsas de incentivo para jovens artistas! Inscrições abertas.</span>
            <span class="d-md-none"><i class="fa-solid fa-star me-1"></i> Editais 2026 Abertos!</span>
            <a href="#editais" class="text-white text-decoration-underline ms-2 fw-bold">Saiba mais</a>
        </div>
    </div>

    <nav class="navbar navbar-expand-lg sticky-top glass-nav py-3">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center me-4" href="#">
                <div class="bg-gradient p-2 rounded-circle me-2 d-flex align-items-center justify-content-center" style="width: 42px; height: 42px; background: var(--pcj-gradient);">
                    <i class="fa-solid fa-bolt text-white fs-5"></i>
                </div>
                <span class="fw-bold fs-4 tracking-tight">CAMA<span class="text-gradient">FLOW</span>
            </a>

            <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarMain">
                <i class="fa-solid fa-bars fs-3 text-white"></i>
            </button>

            <div class="collapse navbar-collapse" id="navbarMain">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0 fw-semibold">
                    <li class="nav-item"><a class="nav-link px-3 active" href="#inicio">Início</a></li>
                    <li class="nav-item"><a class="nav-link px-3" href="#eventos">Eventos</a></li>
                    <li class="nav-item"><a class="nav-link px-3" href="#oficinas">Oficinas</a></li>
                    <li class="nav-item"><a class="nav-link px-3" href="#editais">Editais</a></li>
                    <li class="nav-item"><a class="nav-link px-3" href="#artistas">Artistas</a></li>
                    <li class="nav-item"><a class="nav-link px-3" href="#contato">Contato</a></li>
                </ul>

                <div class="d-flex align-items-center gap-2 mt-3 mt-lg-0">
                    <div class="input-group d-none d-xl-flex" style="width: 220px;">
                        <span class="input-group-text bg-transparent border-end-0 border-secondary text-muted"><i class="fa-solid fa-magnifying-glass"></i></span>
                        <input type="text" id="navSearchInput" class="form-bg-input form-control bg-transparent border-start-0 border-secondary text-white" placeholder="Buscar arte..." style="font-size: 0.88rem;">
                    </div>

                    <button class="btn btn-outline-secondary position-relative rounded-circle" id="favDrawerBtn" title="Seus Favoritos" style="width:42px; height:42px; padding:0;">
                        <i class="fa-solid fa-heart text-danger"></i>
                        <span id="favBadge" class="position-absolute top-0 start-100 translate-middle badge rounded-pill bg-danger" style="display:none;">0</span>
                    </button>

                    <button class="btn btn-outline-secondary rounded-circle" id="themeToggleBtn" title="Alternar Tema (Escuro/Claro)" style="width:42px; height:42px; padding:0;">
                        <i class="fa-solid fa-moon text-warning" id="themeIcon"></i>
                    </button>

                    <button class="btn btn-outline-secondary rounded-circle" id="accessibilityBtn" title="Opções de Acessibilidade" style="width:42px; height:42px; padding:0;">
                        <i class="fa-solid fa-universal-access text-info"></i>
                    </button>

                    <button class="btn btn-gradient ms-2" data-bs-toggle="modal" data-bs-target="#modalSubmeterEdital">
                        <i class="fa-solid fa-plus me-1"></i> Publicar
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <section id="inicio" class="hero-section">
        <div class="hero-shape shape-1"></div>
        <div class="hero-shape shape-2"></div>
        
        <div class="container position-relative z-1">
            <div class="row align-items-center">
                <div class="col-lg-7 text-center text-lg-start mb-5 mb-lg-0">
                    <span class="badge bg-secondary-subtle text-gradient px-3 py-2 rounded-pill fw-bold mb-3 d-inline-block">
                        <i class="fa-solid fa-sparkles me-1"></i> O Hub da Nova Geração Artística
                    </span>
                    <h1 class="display-3 fw-extrabold mb-4 lh-sm">
                        Conectando a Juventude à <span class="text-gradient">Arte, Música</span> e Oportunidades
                    </h1>
                    <p class="lead text-muted mb-4 pe-lg-5 fs-5">
                        Descubra eventos periféricos, workshops gratuitos, editais de financiamento e conecte-se com talentos emergentes de todo o país. O palco da sua expressão é aqui.
                    </p>

                    <div class="d-flex flex-wrap justify-content-center justify-content-lg-start gap-3 mb-4">
                        <a href="#eventos" class="btn btn-gradient btn-lg px-4 py-3">
                            <i class="fa-solid fa-compass me-2"></i> Explorar Eventos
                        </a>
                        <button class="btn btn-outline-custom btn-lg px-4 py-3" data-bs-toggle="modal" data-bs-target="#modalSubmeterEdital">
                            <i class="fa-solid fa-lightbulb me-2"></i> Inscrever Projeto
                        </button>
                    </div>

                    <div class="row pt-4 border-top border-secondary-subtle text-center text-lg-start">
                        <div class="col-4">
                            <h3 class="fw-bold mb-0 text-gradient-cyan">+18k</h3>
                            <small class="text-muted">Jovens Impactados</small>
                        </div>
                        <div class="col-4">
                            <h3 class="fw-bold mb-0 text-gradient">+350</h3>
                            <small class="text-muted">Oficinas Gratuitas</small>
                        </div>
                        <div class="col-4">
                            <h3 class="fw-bold mb-0 text-warning">R$ 1.2M</h3>
                            <small class="text-muted">Distribuídos em Bolsas</small>
                        </div>
                    </div>
                </div>

                <div class="col-lg-5">
                    <div class="glass-card p-3 position-relative overflow-hidden shadow-lg transform-hover">
                        <img src="https://images.unsplash.com/photo-1514525253161-7a46d19cd819?auto=format&fit=crop&w=800&q=80" alt="Festival Cultural Jovem" class="img-fluid rounded-4 w-100 shadow">
                        <div class="position-absolute bottom-0 start-0 end-0 p-4 m-3 rounded-4 glass-nav">
                            <div class="d-flex align-items-center gap-3">
                                <div class="bg-gradient p-3 rounded-circle text-white" style="background: var(--pcj-gradient)">
                                    <i class="fa-solid fa-compact-disc fa-spin fs-4"></i>
                                </div>
                                <div>
                                    <h6 class="mb-0 fw-bold">Festival Conexão Urbano 2026</h6>
                                    <small class="text-muted"><i class="fa-solid fa-location-dot me-1 text-danger"></i> Centro Cultural Juventude - Entrada Franca</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <main class="container py-5">
        
        <section id="eventos" class="mb-5">
            <div class="d-flex flex-column flex-md-row justify-content-between align-items-md-center mb-4 gap-3">
                <div>
                    <h2 class="fw-bold mb-1">Agenda Cultural & Oficinas</h2>
                    <p class="text-muted mb-0">Filtre por linguagem artística, local ou busca por palavras-chave</p>
                </div>

                <div class="d-flex align-items-center gap-2">
                    <span id="apiStatusBadge" class="badge bg-success-subtle text-success border border-success-subtle px-3 py-2 rounded-pill">
                        <i class="fa-solid fa-wifi me-1"></i> API Conectada
                    </span>
                    <button id="refreshEventsBtn" class="btn btn-sm btn-outline-secondary rounded-circle" title="Recarregar Dados">
                        <i class="fa-solid fa-rotate-right"></i>
                    </button>
                </div>
            </div>

            <div class="glass-card p-4 mb-4">
                <div class="row g-3">
                    <div class="col-md-5">
                        <label for="searchInput" class="form-label small text-muted fw-semibold">O QUE VOCÊ PROCURA?</label>
                        <div class="input-group">
                            <span class="input-group-text bg-transparent border-secondary text-muted"><i class="fa-solid fa-magnifying-glass"></i></span>
                            <input type="text" id="searchInput" class="form-control bg-transparent border-secondary text-white" placeholder="Ex: Batalha de Rima, Fotografia, Teatro...">
                        </div>
                    </div>

                    <div class="col-md-4">
                        <label for="locationFilter" class="form-label small text-muted fw-semibold">CIDADE / REGIÃO</label>
                        <select id="locationFilter" class="form-select bg-transparent border-secondary text-white">
                            <option value="" class="bg-dark text-white">Todas as Regiões</option>
                            <option value="São Paulo - SP" class="bg-dark text-white">São Paulo - SP</option>
                            <option value="Rio de Janeiro - RJ" class="bg-dark text-white">Rio de Janeiro - RJ</option>
                            <option value="Salvador - BA" class="bg-dark text-white">Salvador - BA</option>
                            <option value="Belo Horizonte - MG" class="bg-dark text-white">Belo Horizonte - MG</option>
                            <option value="Online / Remoto" class="bg-dark text-white">Online / Remoto</option>
                        </select>
                    </div>

                    <div class="col-md-3">
                        <label for="dateFilter" class="form-label small text-muted fw-semibold">QUANDO?</label>
                        <select id="dateFilter" class="form-select bg-transparent border-secondary text-white">
                            <option value="all" class="bg-dark text-white">Qualquer Data</option>
                            <option value="today" class="bg-dark text-white">Hoje / Esta semana</option>
                            <option value="month" class="bg-dark text-white">Este Mês</option>
                        </select>
                    </div>
                </div>

                <div class="d-flex align-items-center gap-2 overflow-x-auto pt-4 mt-2 border-top border-secondary-subtle" id="categoryPills">
                    <span class="filter-pill active" data-category="all"><i class="fa-solid fa-shapes me-1"></i> Todos</span>
                    <span class="filter-pill" data-category="Música"><i class="fa-solid fa-music me-1"></i> Música</span>
                    <span class="filter-pill" data-category="Teatro"><i class="fa-solid fa-masks-theater me-1"></i> Teatro</span>
                    <span class="filter-pill" data-category="Dança"><i class="fa-solid fa-person-dancing me-1"></i> Dança</span>
                    <span class="filter-pill" data-category="Artes Visuais"><i class="fa-solid fa-palette me-1"></i> Artes Visuais</span>
                    <span class="filter-pill" data-category="Literatura"><i class="fa-solid fa-book-open me-1"></i> Literatura</span>
                    <span class="filter-pill" data-category="Cinema"><i class="fa-solid fa-film me-1"></i> Cinema & Vídeo</span>
                    <span class="filter-pill" data-category="Games & Digital"><i class="fa-solid fa-gamepad me-1"></i> Games & Digital</span>
                </div>
            </div>

            <div class="row g-4" id="eventsGrid">
                <div class="col-md-6 col-lg-4 skeleton-card">
                    <div class="glass-card p-3">
                        <div class="skeleton mb-3" style="height: 180px;"></div>
                        <div class="skeleton mb-2" style="height: 20px; width: 40%;"></div>
                        <div class="skeleton mb-2" style="height: 28px; width: 80%;"></div>
                        <div class="skeleton" style="height: 15px; width: 60%;"></div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 skeleton-card">
                    <div class="glass-card p-3">
                        <div class="skeleton mb-3" style="height: 180px;"></div>
                        <div class="skeleton mb-2" style="height: 20px; width: 40%;"></div>
                        <div class="skeleton mb-2" style="height: 28px; width: 80%;"></div>
                        <div class="skeleton" style="height: 15px; width: 60%;"></div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-4 skeleton-card d-none d-lg-block">
                    <div class="glass-card p-3">
                        <div class="skeleton mb-3" style="height: 180px;"></div>
                        <div class="skeleton mb-2" style="height: 20px; width: 40%;"></div>
                        <div class="skeleton mb-2" style="height: 28px; width: 80%;"></div>
                        <div class="skeleton" style="height: 15px; width: 60%;"></div>
                    </div>
                </div>
            </div>

            <div id="noResultsMsg" class="text-center py-5 d-none">
                <i class="fa-regular fa-face-frown fs-1 text-muted mb-3"></i>
                <h4 class="fw-bold">Nenhum evento encontrado</h4>
                <p class="text-muted">Tente alterar os termos da busca ou selecionar outra categoria.</p>
                <button class="btn btn-outline-custom mt-2" onclick="resetFilters()">Limpar Filtros</button>
            </div>
        </section>
        <section id="oficinas" class="my-5 py-4">
            <div class="p-4 p-md-5 rounded-4 position-relative overflow-hidden glass-card border-0" style="background: linear-gradient(135deg, rgba(121, 40, 202, 0.9) 0%, rgba(255, 0, 128, 0.8) 100%); color: #fff;">
                <div class="row align-items-center position-relative z-1">
                    <div class="col-lg-8 mb-4 mb-lg-0">
                        <span class="badge bg-white text-dark fw-bold mb-3 px-3 py-2 rounded-pill"><i class="fa-solid fa-graduation-cap me-1"></i> Formação Gratuita</span>
                        <h2 class="display-6 fw-bold mb-3">Laboratórios & Oficinas de Capacitação Cultural</h2>
                        <p class="fs-5 opacity-90 mb-0">Aprenda produção musical, iluminação cênica, gestão de carreira artística e mídias sociais com profissionais renomados do mercado.</p>
                    </div>
                    <div class="col-lg-4 text-lg-end">
                        <button class="btn btn-light text-dark btn-lg rounded-pill fw-bold px-4 shadow" data-bs-toggle="modal" data-bs-target="#modalOficinas">
                            Ver Programação Completa
                        </button>
                    </div>
                </div>
            </div>
        </section>
        <section id="editais" class="my-5">
            <div class="d-flex justify-content-between align-items-end mb-4">
                <div>
                    <span class="text-gradient fw-bold text-uppercase tracking-wider">Oportunidades & Financiamento</span>
                    <h2 class="fw-bold mb-0">Editais Abertos para a Juventude</h2>
                </div>
                <button class="btn btn-outline-custom btn-sm" data-bs-toggle="modal" data-bs-target="#modalSubmeterEdital">
                    <i class="fa-solid fa-paper-plane me-1"></i> Submeter Projeto
                </button>
            </div>

            <div class="row g-4" id="editaisGrid">
            </div>
        </section>

        <section id="artistas" class="my-5 py-4">
            <div class="text-center mb-5">
                <span class="text-gradient fw-bold text-uppercase tracking-wider">Talentos Emergentes</span>
                <h2 class="fw-bold display-5">Vitrine de Artistas Independentes</h2>
                <p class="text-muted mx-auto" style="max-width: 600px;">Conheça e apoie a nova safra de músicos, dançarinos, ilustradores e poetas da periferia e dos centros urbanos.</p>
            </div>

            <div class="row g-4" id="artistsGrid">
            </div>
        </section>

        <section id="contato" class="my-5">
            <div class="glass-card p-4 p-md-5 position-relative overflow-hidden">
                <div class="row align-items-center">
                    <div class="col-lg-6 mb-4 mb-lg-0">
                        <h2 class="fw-bold mb-3">Fique por dentro das <span class="text-gradient">Bolsas e Shows</span></h2>
                        <p class="text-muted mb-4">Receba semanalmente em primeira mão no seu e-mail ou WhatsApp as melhores oportunidades da cena cultural jovem.</p>
                        <div class="d-flex align-items-center gap-3">
                            <div class="d-flex align-items-center text-success">
                                <i class="fa-solid fa-circle-check me-2"></i> Sem Spam
                            </div>
                            <div class="d-flex align-items-center text-info">
                                <i class="fa-solid fa-circle-check me-2"></i> 100% Gratuito
                            </div>
                        </div>
                    </div>
                    
                    <div class="col-lg-6">
                        <form id="newsletterForm" class="needs-validation" novalidate>
                            <div class="mb-3">
                                <label for="userName" class="form-label small fw-semibold">SEU NOME COMPLETO</label>
                                <input type="text" class="form-control bg-transparent border-secondary text-white p-3" id="userName" placeholder="Ex: MC Carol de Souza" required>
                                <div class="invalid-feedback">Por favor, informe seu nome.</div>
                            </div>
                            <div class="mb-3">
                                <label for="userEmail" class="form-label small fw-semibold">SEU MELHOR E-MAIL OU WHATSAPP</label>
                                <input type="email" class="form-control bg-transparent border-secondary text-white p-3" id="userEmail" placeholder="seunome@exemplo.com" required>
                                <div class="invalid-feedback">Insira um e-mail válido.</div>
                            </div>
                            <div class="mb-3">
                                <label for="userCategory" class="form-label small fw-semibold">ÁREA DE INTERESSE PRINCIPAL</label>
                                <select class="form-select bg-transparent border-secondary text-white p-3" id="userCategory" required>
                                    <option value="" class="bg-dark">Selecione uma área...</option>
                                    <option value="musica" class="bg-dark">Música & Produção Sound</option>
                                    <option value="artes" class="bg-dark">Artes Visuais & Grafite</option>
                                    <option value="teatro" class="bg-dark">Teatro & Dança</option>
                                    <option value="editais" class="bg-dark">Editais & Bolsas de Apoio</option>
                                </select>
                            </div>
                            <button type="submit" class="btn btn-gradient w-100 p-3 fs-5">
                                <i class="fa-solid fa-paper-plane me-2"></i> Cadastrar Gratuitamente
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="glass-nav pt-5 pb-4 mt-5 border-top border-secondary-subtle">
        <div class="container">
            <div class="row g-4 mb-4">
                <div class="col-lg-4 mb-3">
                    <a class="navbar-brand d-flex align-items-center mb-3" href="#">
                        <div class="bg-gradient p-2 rounded-circle me-2 d-flex align-items-center justify-content-center" style="width: 36px; height: 36px; background: var(--pcj-gradient);">
                            <i class="fa-solid fa-bolt text-white fs-6"></i>
                        </div>
                        <span class="fw-bold fs-5">Plataforma<span class="text-gradient">Cultural</span>Jovem</span>
                    </a>
                    <p class="text-muted small mb-3">
                        Iniciativa independente focada na democratização do acesso à cultura, formação artística e fomento de novas linguagens periféricas da juventude.
                    </p>
                    <div class="d-flex gap-2">
                        <a href="#" class="btn btn-outline-secondary rounded-circle" style="width:38px; height:38px; padding:6px;"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#" class="btn btn-outline-secondary rounded-circle" style="width:38px; height:38px; padding:6px;"><i class="fa-brands fa-tiktok"></i></a>
                        <a href="#" class="btn btn-outline-secondary rounded-circle" style="width:38px; height:38px; padding:6px;"><i class="fa-brands fa-youtube"></i></a>
                        <a href="#" class="btn btn-outline-secondary rounded-circle" style="width:38px; height:38px; padding:6px;"><i class="fa-brands fa-spotify"></i></a>
                    </div>
                </div>

                <div class="col-6 col-lg-2">
                    <h6 class="fw-bold text-uppercase mb-3 small text-gradient">Navegação</h6>
                    <ul class="list-unstyled text-muted small lh-lg">
                        <li><a href="#inicio" class="text-reset text-decoration-none">Início</a></li>
                        <li><a href="#eventos" class="text-reset text-decoration-none">Agenda Cultural</a></li>
                        <li><a href="#oficinas" class="text-reset text-decoration-none">Workshops</a></li>
                        <li><a href="#editais" class="text-reset text-decoration-none">Editais Abertos</a></li>
                        <li><a href="#artistas" class="text-reset text-decoration-none">Vitrine de Artistas</a></li>
                    </ul>
                </div>

                <div class="col-6 col-lg-2">
                    <h6 class="fw-bold text-uppercase mb-3 small text-gradient">Linguagens</h6>
                    <ul class="list-unstyled text-muted small lh-lg">
                        <li><a href="#" class="text-reset text-decoration-none">Música Urbana</a></li>
                        <li><a href="#" class="text-reset text-decoration-none">Slam & Poesia</a></li>
                        <li><a href="#" class="text-reset text-decoration-none">Grafite & Muralismo</a></li>
                        <li><a href="#" class="text-reset text-decoration-none">Dança de Rua</a></li>
                        <li><a href="#" class="text-reset text-decoration-none">Cinema Periférico</a></li>
                    </ul>
                </div>

                <div class="col-lg-4">
                    <h6 class="fw-bold text-uppercase mb-3 small text-gradient">Acessibilidade e Idioma</h6>
                    <div class="d-flex flex-column gap-2">
                        <button class="btn btn-sm btn-outline-secondary text-start" onclick="toggleContrast()">
                            <i class="fa-solid fa-circle-half-stroke me-2"></i> Alternar Alto Contraste
                        </button>
                        <button class="btn btn-sm btn-outline-secondary text-start" onclick="adjustFontSize(1)">
                            <i class="fa-solid fa-font me-2"></i> Aumentar Tamanho da Fonte
                        </button>
                        <button class="btn btn-sm btn-outline-secondary text-start" onclick="adjustFontSize(-1)">
                            <i class="fa-solid fa-font me-2 text-xs"></i> Diminuir Tamanho da Fonte
                        </button>
                    </div>
                </div>
            </div>

            <div class="row border-top border-secondary-subtle pt-4 text-center text-md-start align-items-center">
                <div class="col-md-6 text-muted small">
                    © 2026 Plataforma Cultural Jovem. Licenciado via Creative Commons BY-NC 4.0.
                </div>
                <div class="col-md-6 text-md-end text-muted small mt-2 mt-md-0">
                    Feito com <i class="fa-solid fa-heart text-danger"></i> para a juventude criativa.
                </div>
            </div>
        </div>
    </footer>

    <div class="modal fade" id="modalEventDetails" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered modal-lg">
            <div class="modal-content glass-card border-secondary text-white">
                <div class="modal-header border-secondary">
                    <h5 class="modal-title fw-bold" id="eventModalTitle">Detalhes do Evento</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <img id="eventModalImg" src="" alt="Imagem do Evento" class="img-fluid rounded-4 w-100 mb-4" style="height: 280px; object-fit: cover;">
                    <div class="d-flex flex-wrap gap-2 mb-3">
                        <span id="eventModalCategory" class="badge-category">Categoria</span>
                        <span id="eventModalPrice" class="badge bg-success">Gratuito</span>
                    </div>
                    <p id="eventModalDesc" class="lead text-muted fs-6 mb-4"></p>
                    
                    <div class="row g-3 p-3 rounded-3 bg-dark bg-opacity-50 border border-secondary mb-4">
                        <div class="col-md-6"><i class="fa-solid fa-calendar text-danger me-2"></i><strong id="eventModalDate">Data:</strong></div>
                        <div class="col-md-6"><i class="fa-solid fa-clock text-warning me-2"></i><strong id="eventModalTime">Horário:</strong></div>
                        <div class="col-md-6"><i class="fa-solid fa-location-dot text-info me-2"></i><strong id="eventModalLocation">Local:</strong></div>
                        <div class="col-md-6"><i class="fa-solid fa-users text-primary me-2"></i><strong id="eventModalOrganizer">Organizador:</strong></div>
                    </div>
                </div>
                <div class="modal-footer border-secondary">
                    <button type="button" class="btn btn-outline-secondary rounded-pill" data-bs-dismiss="modal">Fechar</button>
                    <button type="button" class="btn btn-gradient" onclick="reserveTicket()">
                        <i class="fa-solid fa-ticket me-1"></i> Garantir Ingressos / Inscrição
                    </button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="modalSubmeterEdital" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered modal-lg">
            <div class="modal-content glass-card border-secondary text-white">
                <div class="modal-header border-secondary">
                    <h5 class="modal-title fw-bold"><i class="fa-solid fa-lightbulb text-warning me-2"></i>Inscrever Projeto Cultural</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <form id="projectSubmissionForm" onsubmit="handleProjectSubmit(event)">
                    <div class="modal-body">
                        <p class="text-muted small mb-4">Envie sua proposta para avaliação nos editais ativos ou para divulgação em nosso catálogo.</p>
                        
                        <div class="row g-3">
                            <div class="col-md-6">
                                <label class="form-label small fw-semibold">TÍTULO DO PROJETO</label>
                                <input type="text" class="form-control bg-transparent border-secondary text-white" placeholder="Ex: Mostra Periférica de Curta Metragem" required>
                            </div>
                            <div class="col-md-6">
                                <label class="form-label small fw-semibold">RESPONSÁVEL / PROPONENTE</label>
                                <input type="text" class="form-control bg-transparent border-secondary text-white" placeholder="Seu nome ou Coletivo" required>
                            </div>
                            <div class="col-md-6">
                                <label class="form-label small fw-semibold">CATEGORIA ARTÍSTICA</label>
                                <select class="form-select bg-transparent border-secondary text-white" required>
                                    <option value="" class="bg-dark">Selecione...</option>
                                    <option value="musica" class="bg-dark">Música</option>
                                    <option value="teatro" class="bg-dark">Teatro / Dança</option>
                                    <option value="artes" class="bg-dark">Artes Visuais</option>
                                    <option value="cinema" class="bg-dark">Cinema</option>
                                    <option value="literatura" class="bg-dark">Literatura</option>
                                </select>
                            </div>
                            <div class="col-md-6">
                                <label class="form-label small fw-semibold">CIDADE / ESTADO</label>
                                <input type="text" class="form-control bg-transparent border-secondary text-white" placeholder="Ex: Salvador - BA" required>
                            </div>
                            <div class="col-12">
                                <label class="form-label small fw-semibold">RESUMO DA PROPOSTA (MAX 500 CARACTERES)</label>
                                <textarea class="form-control bg-transparent border-secondary text-white" rows="4" placeholder="Descreva os objetivos, público-alvo e justificativa do projeto..." required></textarea>
                            </div>
                            <div class="col-12">
                                <label class="form-label small fw-semibold">LINK DO PORTFÓLIO / PORTAL (OPCIONAL)</label>
                                <input type="url" class="form-control bg-transparent border-secondary text-white" placeholder="https://instagram.com/seuprojetocultural">
                            </div>
                        </div>
                    </div>
                    <div class="modal-footer border-secondary">
                        <button type="button" class="btn btn-outline-secondary rounded-pill" data-bs-dismiss="modal">Cancelar</button>
                        <button type="submit" class="btn btn-gradient">Submeter para Avaliação</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
    <div class="modal fade" id="modalOficinas" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered modal-lg">
            <div class="modal-content glass-card border-secondary text-white">
                <div class="modal-header border-secondary">
                    <h5 class="modal-title fw-bold"><i class="fa-solid fa-graduation-cap text-info me-2"></i>Grade de Oficinas Gratuitas 2026</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="list-group list-group-flush bg-transparent">
                        <div class="list-group-item bg-transparent text-white border-secondary py-3">
                            <div class="d-flex justify-content-between align-items-center">
                                <div>
                                    <h6 class="fw-bold mb-1">Produção de Beats & Mixagem Hip-Hop</h6>
                                    <small class="text-muted"><i class="fa-solid fa-clock me-1"></i> Terças e Quintas | 19h às 21h (Online)</small>
                                </div>
                                <button class="btn btn-sm btn-gradient" onclick="triggerRegistration('Produção de Beats')">Garantir Vaga</button>
                            </div>
                        </div>
                        <div class="list-group-item bg-transparent text-white border-secondary py-3">
                            <div class="d-flex justify-content-between align-items-center">
                                <div>
                                    <h6 class="fw-bold mb-1">Fotografia Urbana e Edição Mobile</h6>
                                    <small class="text-muted"><i class="fa-solid fa-clock me-1"></i> Sábados | 14h às 17h (Presencial SP)</small>
                                </div>
                                <button class="btn btn-sm btn-gradient" onclick="triggerRegistration('Fotografia Urbana')">Garantir Vaga</button>
                            </div>
                        </div>
                        <div class="list-group-item bg-transparent text-white border-secondary py-3">
                            <div class="d-flex justify-content-between align-items-center">
                                <div>
                                    <h6 class="fw-bold mb-1">Elaboração de Projetos para Editais Públicos</h6>
                                    <small class="text-muted"><i class="fa-solid fa-clock me-1"></i> Quartas-feiras | 18h30 às 20h30 (Online)</small>
                                </div>
                                <button class="btn btn-sm btn-gradient" onclick="triggerRegistration('Elaboração de Projetos')">Garantir Vaga</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="modalFavs" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content glass-card border-secondary text-white">
                <div class="modal-header border-secondary">
                    <h5 class="modal-title fw-bold"><i class="fa-solid fa-heart text-danger me-2"></i>Seus Eventos Salvos</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body" id="favsModalList">
                    <p class="text-muted text-center py-3">Você ainda não marcou nenhum evento como favorito.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="toast-container">
        <div id="appToast" class="toast align-items-center text-white bg-dark border-secondary shadow-lg" role="alert" aria-live="assertive" aria-atomic="true">
            <div class="d-flex">
                <div class="toast-body d-flex align-items-center gap-2">
                    <i id="toastIcon" class="fa-solid fa-circle-check text-success fs-5"></i>
                    <span id="toastMsg">Ação realizada com sucesso!</span>
                </div>
                <button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast" aria-label="Close"></button>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

    <script>
      
        const MOCK_EVENTS = [
            {
                id: 1,
                title: "Festival de Hip-Hop & Batalha de Rima Slam",
                category: "Música",
                date: "2026-11-20",
                dateFormatted: "20 de Novembro, 2026",
                time: "16:00 - 22:00",
                location: "São Paulo - SP",
                venue: "Praça das Artes - Centro",
                price: "Gratuito",
                organizer: "Coletivo Rima Livre",
                image: "https://images.unsplash.com/photo-1514525253161-7a46d19cd819?auto=format&fit=crop&w=600&q=80",
                description: "Edição especial de celebração da cultura Hip-Hop com batalhas de MCs, DJs, workshops de grafite ao vivo e pocket shows independentes."
            },
            {
                id: 2,
                title: "Mostra de Cinema Jovem Periférico",
                category: "Cinema",
                date: "2026-11-25",
                dateFormatted: "25 de Novembro, 2026",
                time: "18:30 - 21:30",
                location: "Rio de Janeiro - RJ",
                venue: "Cine Periferia Lapa",
                price: "Gratuito",
                organizer: "Cineclube Juventude Viva",
                image: "https://images.unsplash.com/photo-1489599849927-2ee91cede3ba?auto=format&fit=crop&w=600&q=80",
                description: "Exibição de 8 curtas-metragens produzidos por diretores entre 16 e 29 anos de favelas e periferias. Sessão seguida de debate com diretores."
            },
            {
                id: 3,
                title: "Oficina Imersiva de Fotografia Urbana",
                category: "Artes Visuais",
                date: "2026-12-02",
                dateFormatted: "02 de Dezembro, 2026",
                time: "14:00 - 18:00",
                location: "Salvador - BA",
                venue: "Pelourinho Hub Cultural",
                price: "Gratuito",
                organizer: "Laboratório Olhar Jovem",
                image: "https://images.unsplash.com/photo-1542038784456-1ea8e935640e?auto=format&fit=crop&w=600&q=80",
                description: "Aprenda técnicas de composição, iluminação natural e edição mobile para registrar as narrativas e estética da sua cidade."
            },
            {
                id: 4,
                title: "Espetáculo de Dança Contemporânea: Margens",
                category: "Dança",
                date: "2026-12-05",
                dateFormatted: "05 de Dezembro, 2026",
                time: "20:00",
                location: "Belo Horizonte - MG",
                venue: "Teatro Espanca!",
                price: "R$ 10,00 (Meia)",
                organizer: "Corpo em Movimento",
                image: "https://images.unsplash.com/photo-1508700115892-45ecd05ae2ad?auto=format&fit=crop&w=600&q=80",
                description: "Performance vibrante que expressa os desafios, sonhos e memórias da juventude urbana através de coreografias dinâmicas."
            },
            {
                id: 5,
                title: "Encontro Poético & Feira de Zines Independentes",
                category: "Literatura",
                date: "2026-12-10",
                dateFormatted: "10 de Dezembro, 2026",
                time: "15:00 - 20:00",
                location: "Online / Remoto",
                venue: "Transmissão ao vivo YouTube",
                price: "Gratuito",
                organizer: "Editora Periférica",
                image: "https://images.unsplash.com/photo-1457369804613-52c61a468e7d?auto=format&fit=crop&w=600&q=80",
                description: "Lançamento de publicações artesanais, microfone aberto para declamação e mesa sobre literatura marginal com convidados."
            },
            {
                id: 6,
                title: "Hackathon de Game Design & Pixel Art",
                category: "Games & Digital",
                date: "2026-12-15",
                dateFormatted: "15 de Dezembro, 2026",
                time: "09:00 - 19:00",
                location: "Online / Remoto",
                venue: "Discord / Twitch",
                price: "Gratuito",
                organizer: "Indie Game Devs BR",
                image: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=600&q=80",
                description: "Desafio 24h para criar protótipos de jogos inspirados no folclore e na cultura urbana brasileira. Prêmios para os melhores projetos."
            }
        ];

        const MOCK_EDITAIS = [
            {
                id: 103,
                title: "Fundo de Apoio para equipamentos, eventos e patrocínio de artistas",
                reward: "R$ 10.500,00 por coletivo",
                deadline: "30/12/2026",
                status: "Em Breve",
                category: "Apoio a causa",
                badgeClass: "bg-info text-dark"
            }
        ];

        const MOCK_ARTISTS = [
            {
                id: 201,
                name: "MC Aisha Luna",
                discipline: "Hip-Hop & Trap",
                bio: "Compondo rimas marcantes sobre a vivência jovem no extremo sul de SP. Mais de 100k streams.",
                image: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=300&q=80",
                likes: 420
            },
            {
                id: 202,
                name: "Lucas Graf",
                discipline: "Muralismo & Grafite",
                bio: "Transformando muros cinzas em galerias a céu aberto nas ruas de Salvador.",
                image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=300&q=80",
                likes: 315
            },
            {
                id: 203,
                name: "Yara Poetisa",
                discipline: "Slam & Literatura",
                bio: "Campeã do Slam Juventude 2025. Autora do livro independente 'Vozes da Leste'.",
                image: "https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=300&q=80",
                likes: 512
            }
        ];

        let eventsData = [];
        let favorites = JSON.parse(localStorage.getItem('pcj_favorites')) || [];
        let activeCategory = 'all';

        document.addEventListener('DOMContentLoaded', () => {
            initTheme();
            fetchEventsData();
            renderEditais();
            renderArtists();
            setupEventListeners();
            updateFavBadge();
        });

        async function fetchEventsData() {
            const grid = document.getElementById('eventsGrid');
            const statusBadge = document.getElementById('apiStatusBadge');

            try {
                const simulatedApiPromise = new Promise((resolve) => {
                    setTimeout(() => resolve(MOCK_EVENTS), 600);
                });

                eventsData = await simulatedApiPromise;
                renderEvents(eventsData);
                
                statusBadge.innerHTML = `<i class="fa-solid fa-wifi me-1"></i> API Conectada`;
                statusBadge.className = 'badge bg-success-subtle text-success border border-success-subtle px-3 py-2 rounded-pill';
            } catch (error) {
                console.warn("API request failed, falling back to local dataset:", error);
                eventsData = MOCK_EVENTS;
                renderEvents(eventsData);

                statusBadge.innerHTML = `<i class="fa-solid fa-triangle-exclamation me-1"></i> Modo Offline`;
                statusBadge.className = 'badge bg-warning-subtle text-warning border border-warning-subtle px-3 py-2 rounded-pill';
            }
        }
        function renderEvents(items) {
            const grid = document.getElementById('eventsGrid');
            const noResults = document.getElementById('noResultsMsg');
            
            grid.innerHTML = '';

            if (!items || items.length === 0) {
                noResults.classList.remove('d-none');
                return;
            }
            noResults.classList.add('d-none');

            items.forEach(event => {
                const isFav = favorites.includes(event.id);
                const col = document.createElement('div');
                col.className = 'col-md-6 col-lg-4';
                
                col.innerHTML = `
                    <div class="glass-card h-100 d-flex flex-column">
                        <div class="card-img-wrapper">
                            <img src="${event.image}" alt="${event.title}" loading="lazy">
                            <button class="fav-btn ${isFav ? 'active' : ''}" onclick="toggleFavorite(${event.id}, this)" title="Salvar Favorito">
                                <i class="fa-${isFav ? 'solid' : 'regular'} fa-heart"></i>
                            </button>
                            <span class="position-absolute bottom-0 start-0 m-3 badge bg-dark bg-opacity-75 text-white backdrop-blur">
                                <i class="fa-solid fa-tag me-1"></i> ${event.price}
                            </span>
                        </div>
                        <div class="p-4 d-flex flex-column flex-grow-1">
                            <div class="d-flex justify-content-between align-items-center mb-2">
                                <span class="badge-category">${event.category}</span>
                                <small class="text-muted"><i class="fa-solid fa-calendar me-1"></i> ${event.dateFormatted}</small>
                            </div>
                            <h5 class="fw-bold mb-2 text-white">${event.title}</h5>
                            <p class="text-muted small mb-4 flex-grow-1">${event.description.substring(0, 90)}...</p>
                            
                            <div class="pt-3 border-top border-secondary-subtle d-flex justify-content-between align-items-center mt-auto">
                                <small class="text-muted"><i class="fa-solid fa-location-dot me-1 text-danger"></i> ${event.location}</small>
                                <button class="btn btn-sm btn-outline-custom" onclick="openEventModal(${event.id})">
                                    Ver Detalhes
                                </button>
                            </div>
                        </div>
                    </div>
                `;
                grid.appendChild(col);
            });
        }

        function renderEditais() {
            const container = document.getElementById('editaisGrid');
            container.innerHTML = '';

            MOCK_EDITAIS.forEach(edital => {
                const col = document.createElement('div');
                col.className = 'col-md-4';
                col.innerHTML = `
                    <div class="glass-card edital-card p-4 h-100 d-flex flex-column justify-content-between">
                        <div>
                            <div class="d-flex justify-content-between align-items-center mb-3">
                                <span class="badge ${edital.badgeClass}">${edital.status}</span>
                                <small class="text-muted"><i class="fa-regular fa-clock me-1"></i> Até ${edital.deadline}</small>
                            </div>
                            <span class="text-gradient small fw-bold text-uppercase d-block mb-1">${edital.category}</span>
                            <h5 class="fw-bold mb-3">${edital.title}</h5>
                            <h4 class="text-warning fw-extrabold mb-3">${edital.reward}</h4>
                        </div>
                        <button class="btn btn-outline-custom w-100 mt-3" data-bs-toggle="modal" data-bs-target="#modalSubmeterEdital">
                            Inscrever-se Agora
                        </button>
                    </div>
                `;
                container.appendChild(col);
            });
        }

        function renderArtists() {
            const container = document.getElementById('artistsGrid');
            container.innerHTML = '';

            MOCK_ARTISTS.forEach(artist => {
                const col = document.createElement('div');
                col.className = 'col-md-4';
                col.innerHTML = `
                    <div class="glass-card p-4 text-center h-100 d-flex flex-column align-items-center justify-content-between">
                        <div>
                            <img src="${artist.image}" alt="${artist.name}" class="artist-avatar mb-3">
                            <h5 class="fw-bold mb-1">${artist.name}</h5>
                            <span class="badge bg-secondary-subtle text-gradient px-3 py-1 rounded-pill small mb-3 d-inline-block">${artist.discipline}</span>
                            <p class="text-muted small mb-4">${artist.bio}</p>
                        </div>
                        <div class="d-flex align-items-center gap-2 w-100">
                            <button class="btn btn-sm btn-outline-danger flex-grow-1" onclick="likeArtist(${artist.id}, this)">
                                <i class="fa-solid fa-heart me-1"></i> Aplaudir (<span class="like-count">${artist.likes}</span>)
                            </button>
                            <a href="#" class="btn btn-sm btn-outline-secondary rounded-circle" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
                        </div>
                    </div>
                `;
                container.appendChild(col);
            });
        }

        function filterEvents() {
            const searchVal = document.getElementById('searchInput').value.toLowerCase();
            const locationVal = document.getElementById('locationFilter').value;

            const filtered = eventsData.filter(item => {
                const matchesSearch = item.title.toLowerCase().includes(searchVal) ||
                                      item.description.toLowerCase().includes(searchVal) ||
                                      item.category.toLowerCase().includes(searchVal);
                
                const matchesLocation = locationVal === "" || item.location === locationVal;
                const matchesCategory = activeCategory === 'all' || item.category === activeCategory;

                return matchesSearch && matchesLocation && matchesCategory;
            });

            renderEvents(filtered);
        }

        function resetFilters() {
            document.getElementById('searchInput').value = '';
            document.getElementById('locationFilter').value = '';
            document.getElementById('dateFilter').value = 'all';
            activeCategory = 'all';
            
            document.querySelectorAll('.filter-pill').forEach(p => p.classList.remove('active'));
            document.querySelector('.filter-pill[data-category="all"]').classList.add('active');
            
            renderEvents(eventsData);
        }

        function openEventModal(eventId) {
            const event = eventsData.find(e => e.id === eventId);
            if (!event) return;

            document.getElementById('eventModalTitle').textContent = event.title;
            document.getElementById('eventModalImg').src = event.image;
            document.getElementById('eventModalCategory').textContent = event.category;
            document.getElementById('eventModalPrice').textContent = event.price;
            document.getElementById('eventModalDesc').textContent = event.description;
            document.getElementById('eventModalDate').innerHTML = `<strong>Data:</strong> ${event.dateFormatted}`;
            document.getElementById('eventModalTime').innerHTML = `<strong>Horário:</strong> ${event.time}`;
            document.getElementById('eventModalLocation').innerHTML = `<strong>Local:</strong> ${event.venue} (${event.location})`;
            document.getElementById('eventModalOrganizer').innerHTML = `<strong>Organizador:</strong> ${event.organizer}`;

            const modal = new bootstrap.Modal(document.getElementById('modalEventDetails'));
            modal.show();
        }

        function reserveTicket() {
            const modalEl = document.getElementById('modalEventDetails');
            const modal = bootstrap.Modal.getInstance(modalEl);
            modal.hide();

            showToast("Inscrição Confirmada!", "Você recebeu os ingressos no seu e-mail cadastrado.", "fa-ticket");
        }

        function toggleFavorite(eventId, btnElement) {
            const index = favorites.indexOf(eventId);
            if (index > -1) {
                favorites.splice(index, 1);
                showToast("Removido!", "Evento removido dos seus favoritos.", "fa-trash");
            } else {
                favorites.push(eventId);
                showToast("Favoritado!", "Evento salvo na sua lista de favoritos.", "fa-heart text-danger");
            }

            localStorage.setItem('pcj_favorites', JSON.stringify(favorites));
            updateFavBadge();
            filterEvents();
        }

        function updateFavBadge() {
            const badge = document.getElementById('favBadge');
            if (favorites.length > 0) {
                badge.textContent = favorites.length;
                badge.style.display = 'block';
            } else {
                badge.style.display = 'none';
            }
        }

        function openFavsDrawer() {
            const container = document.getElementById('favsModalList');
            const favEvents = eventsData.filter(e => favorites.includes(e.id));

            if (favEvents.length === 0) {
                container.innerHTML = `<p class="text-muted text-center py-4">Sua lista de favoritos está vazia.</p>`;
            } else {
                container.innerHTML = favEvents.map(e => `
                    <div class="d-flex align-items-center justify-content-between p-2 mb-2 border-bottom border-secondary">
                        <div class="d-flex align-items-center gap-3">
                            <img src="${e.image}" style="width: 50px; height: 50px; object-fit: cover;" class="rounded-3">
                            <div>
                                <h6 class="mb-0 fw-bold">${e.title}</h6>
                                <small class="text-muted">${e.dateFormatted} - ${e.location}</small>
                            </div>
                        </div>
                        <button class="btn btn-sm btn-outline-danger" onclick="toggleFavorite(${e.id}); openFavsDrawer();">
                            <i class="fa-solid fa-xmark"></i>
                        </button>
                    </div>
                `).join('');
            }

            const modal = new bootstrap.Modal(document.getElementById('modalFavs'));
            modal.show();
        }

        function likeArtist(artistId, btn) {
            const artist = MOCK_ARTISTS.find(a => a.id === artistId);
            if (artist) {
                artist.likes += 1;
                btn.querySelector('.like-count').textContent = artist.likes;
                btn.classList.replace('btn-outline-danger', 'btn-danger');
                showToast("Você aplaudiu!", `Você enviou incentivo para ${artist.name}.`, "fa-thumbs-up");
            }
        }

        function setupEventListeners() {
            document.querySelectorAll('.filter-pill').forEach(pill => {
                pill.addEventListener('click', (e) => {
                    document.querySelectorAll('.filter-pill').forEach(p => p.classList.remove('active'));
                    pill.classList.add('active');
                    activeCategory = pill.getAttribute('data-category');
                    filterEvents();
                });
            });

            document.getElementById('searchInput').addEventListener('input', filterEvents);
            document.getElementById('navSearchInput').addEventListener('input', (e) => {
                document.getElementById('searchInput').value = e.target.value;
                filterEvents();
            });
            document.getElementById('locationFilter').addEventListener('change', filterEvents);
            document.getElementById('dateFilter').addEventListener('change', filterEvents);
            document.getElementById('refreshEventsBtn').addEventListener('click', fetchEventsData);
            document.getElementById('favDrawerBtn').addEventListener('click', openFavsDrawer);
            document.getElementById('themeToggleBtn').addEventListener('click', toggleTheme);
            document.getElementById('accessibilityBtn').addEventListener('click', toggleContrast);

            const newsForm = document.getElementById('newsletterForm');
            newsForm.addEventListener('submit', (e) => {
                e.preventDefault();
                if (!newsForm.checkValidity()) {
                    e.stopPropagation();
                    newsForm.classList.add('was-validated');
                    return;
                }

                const name = document.getElementById('userName').value;
                showToast("Cadastro Realizado!", `Bem-vindo(a) à comunidade, ${name}!`, "fa-circle-check");
                newsForm.reset();
                newsForm.classList.remove('was-validated');
            });
        }

        function handleProjectSubmit(e) {
            e.preventDefault();
            const modalEl = document.getElementById('modalSubmeterEdital');
            const modal = bootstrap.Modal.getInstance(modalEl);
            modal.hide();

            showToast("Projeto Submetido!", "Sua proposta foi enviada para análise da comissão cultural.", "fa-paper-plane");
            document.getElementById('projectSubmissionForm').reset();
        }

        function triggerRegistration(workshopName) {
            showToast("Inscrição Efetuada!", `Sua vaga para '${workshopName}' foi pré-reservada.`, "fa-graduation-cap");
        }

        function initTheme() {
            const savedTheme = localStorage.getItem('pcj_theme') || 'dark';
            document.documentElement.setAttribute('data-bs-theme', savedTheme);
            updateThemeIcon(savedTheme);
        }

        function toggleTheme() {
            const currentTheme = document.documentElement.getAttribute('data-bs-theme');
            const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
            document.documentElement.setAttribute('data-bs-theme', newTheme);
            localStorage.setItem('pcj_theme', newTheme);
            updateThemeIcon(newTheme);
        }

        function updateThemeIcon(theme) {
            const icon = document.getElementById('themeIcon');
            if (theme === 'light') {
                icon.className = 'fa-solid fa-sun text-warning';
            } else {
                icon.className = 'fa-solid fa-moon text-warning';
            }
        }

        function toggleContrast() {
            document.body.classList.toggle('high-contrast');
            const isHigh = document.body.classList.contains('high-contrast');
            showToast("Acessibilidade", isHigh ? "Alto Contraste Ativado" : "Modo Normal Restaurado", "fa-universal-access");
        }

        let currentFontDelta = 0;
        function adjustFontSize(delta) {
            currentFontDelta += delta;
            if (currentFontDelta > 3) currentFontDelta = 3;
            if (currentFontDelta < -1) currentFontDelta = -1;

            const baseSize = 16 + currentFontDelta * 2;
            document.documentElement.style.fontSize = `${baseSize}px`;
        }

        function showToast(title, message, iconClass = "fa-circle-check") {
            const toastEl = document.getElementById('appToast');
            document.getElementById('toastMsg').textContent = `${title} ${message}`;
            document.getElementById('toastIcon').className = `fa-solid ${iconClass} me-2 fs-5`;

            const toast = new bootstrap.Toast(toastEl, { delay: 3500 });
            toast.show();
        }
    </script>
</body>
</html>
