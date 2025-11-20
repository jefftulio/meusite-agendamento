[mv-estetica.html.txt](https://github.com/user-attachments/files/23660199/mv-estetica.html.txt)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MV Estética Automotiva - Higienização Premium</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #000000;
            --secondary-color: #ff0000;
            --accent-color: #cc0000;
            --dark-red: #8B0000;
            --light-bg: #0a0a0a;
            --card-bg: #111111;
            --text-light: #f8f9fa;
            --text-muted: #a0a0a0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light-bg);
            color: var(--text-light);
            overflow-x: hidden;
        }
        
        /* Navbar Estilizada */
        .navbar {
            background: linear-gradient(to right, var(--primary-color), var(--dark-red));
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(255, 0, 0, 0.2);
            border-bottom: 1px solid var(--secondary-color);
        }
        
        .navbar-brand {
            font-weight: 700;
            font-size: 1.8rem;
            color: var(--text-light) !important;
            text-shadow: 0 0 10px rgba(255, 0, 0, 0.5);
        }
        
        .navbar-brand i {
            color: var(--secondary-color);
            margin-right: 10px;
        }
        
        .nav-link {
            color: var(--text-light) !important;
            font-weight: 500;
            margin: 0 10px;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .nav-link:hover {
            color: var(--secondary-color) !important;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--secondary-color);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero-section {
            background: linear-gradient(rgba(0,0,0,0.8), rgba(139,0,0,0.7)), url('https://images.unsplash.com/photo-1549399542-7e3f8b79c341?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            padding: 150px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-section:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, transparent 0%, rgba(0,0,0,0.8) 100%);
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .hero-title {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            text-shadow: 0 0 15px rgba(255, 0, 0, 0.5);
        }
        
        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            color: var(--text-muted);
        }
        
        .btn-primary {
            background: linear-gradient(45deg, var(--secondary-color), var(--dark-red));
            border: none;
            padding: 12px 30px;
            font-weight: 600;
            border-radius: 30px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 0, 0, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 0, 0, 0.4);
            background: linear-gradient(45deg, var(--dark-red), var(--secondary-color));
        }
        
        /* Cards de Serviços */
        .service-card {
            background-color: var(--card-bg);
            border: none;
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.4s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
            position: relative;
        }
        
        .service-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--secondary-color), var(--dark-red));
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(255, 0, 0, 0.2);
        }
        
        .service-image {
            height: 200px;
            object-fit: cover;
            width: 100%;
        }
        
        .service-video {
            height: 200px;
            width: 100%;
            object-fit: cover;
            background-color: #000;
        }
        
        .service-content {
            padding: 20px;
        }
        
        .service-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--text-light);
        }
        
        .service-description {
            color: var(--text-muted);
            margin-bottom: 15px;
        }
        
        .price-tag {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary-color);
            text-shadow: 0 0 8px rgba(255, 0, 0, 0.3);
        }
        
        .btn-service {
            background: transparent;
            border: 2px solid var(--secondary-color);
            color: var(--secondary-color);
            padding: 8px 20px;
            border-radius: 30px;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .btn-service:hover {
            background: var(--secondary-color);
            color: var(--text-light);
        }
        
        /* Seção de Extras */
        .extras-section {
            background: linear-gradient(to bottom, var(--light-bg), #1a1a1a);
            padding: 80px 0;
        }
        
        .extra-item {
            background-color: var(--card-bg);
            border-left: 4px solid var(--secondary-color);
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .extra-item:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(255, 0, 0, 0.2);
        }
        
        /* Seção de Agendamento */
        .booking-section {
            padding: 80px 0;
            background: linear-gradient(to bottom, #1a1a1a, var(--light-bg));
        }
        
        .form-control {
            background-color: #222;
            border: 1px solid #333;
            color: var(--text-light);
            border-radius: 5px;
            padding: 12px 15px;
        }
        
        .form-control:focus {
            background-color: #222;
            border-color: var(--secondary-color);
            color: var(--text-light);
            box-shadow: 0 0 0 0.2rem rgba(255, 0, 0, 0.25);
        }
        
        .form-label {
            color: var(--text-light);
            font-weight: 500;
        }
        
        .card {
            background-color: var(--card-bg);
            border: none;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
        }
        
        .card-title {
            color: var(--text-light);
            border-bottom: 1px solid #333;
            padding-bottom: 15px;
            margin-bottom: 20px;
        }
        
        .total-price {
            font-size: 2rem;
            font-weight: 700;
            color: var(--secondary-color);
            text-shadow: 0 0 8px rgba(255, 0, 0, 0.3);
        }
        
        .whatsapp-btn {
            background: linear-gradient(45deg, #25D366, #128C7E);
            border: none;
            color: white;
            font-weight: bold;
            padding: 12px 20px;
            border-radius: 30px;
            transition: all 0.3s ease;
        }
        
        .whatsapp-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.4);
        }
        
        /* Painel Administrativo */
        .admin-panel {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-red));
            color: white;
            padding: 30px;
            border-radius: 10px;
            margin-top: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        /* Modal de Recuperação de Senha */
        .password-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 9999;
            align-items: center;
            justify-content: center;
        }
        
        .password-modal-content {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-red));
            padding: 30px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            box-shadow: 0 10px 30px rgba(255, 0, 0, 0.3);
            position: relative;
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            color: var(--text-light);
            font-size: 1.5rem;
            cursor: pointer;
            transition: color 0.3s ease;
        }
        
        .close-modal:hover {
            color: var(--secondary-color);
        }
        
        /* Títulos de Seção */
        .section-title {
            position: relative;
            margin-bottom: 3rem;
            text-align: center;
            font-weight: 700;
            font-size: 2.5rem;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--secondary-color), var(--dark-red));
            margin: 15px auto;
            border-radius: 2px;
        }
        
        /* Footer */
        footer {
            background: linear-gradient(to right, var(--primary-color), var(--dark-red));
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-links a {
            color: var(--text-muted);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--secondary-color);
        }
        
        /* Animações */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-section {
                padding: 100px 0;
            }
            
            .service-image, .service-video {
                height: 180px;
            }
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fas fa-car"></i> MV Estética Automotiva
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#services">Serviços</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#extras">Extras</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#booking">Agendar</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#admin" id="adminLink">Admin</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="container hero-content">
            <h1 class="hero-title">MV Estética Automotiva</h1>
            <p class="hero-subtitle">Tecnologia e excelência em cuidados automotivos</p>
            <a href="#booking" class="btn btn-primary btn-lg pulse">Agendar Serviço</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-5">
        <div class="container">
            <h2 class="section-title">Nossos Serviços</h2>
            <div class="row">
                <!-- Limpeza Técnica -->
                <div class="col-md-6 col-lg-3">
                    <div class="card service-card h-100">
                        <video class="service-video" controls poster="https://images.unsplash.com/photo-1503376780353-7e6692767b70?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80">
                            <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerJoyrides.mp4" type="video/mp4">
                            Seu navegador não suporta o elemento de vídeo.
                        </video>
                        <div class="service-content">
                            <h5 class="service-title">Limpeza Técnica</h5>
                            <p class="service-description">Processo completo de limpeza interna e externa com produtos de alta qualidade e equipamentos tecnológicos.</p>
                            <div class="price-tag">R$ 80,00</div>
                            <button class="btn btn-service w-100 mt-3 add-service" data-service="Limpeza Técnica" data-price="80">Adicionar</button>
                        </div>
                    </div>
                </div>
                
                <!-- Detalhada -->
                <div class="col-md-6 col-lg-3">
                    <div class="card service-card h-100">
                        <video class="service-video" controls poster="https://images.unsplash.com/photo-1544636331-e26879cd4d9b?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80">
                            <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerJoyrides.mp4" type="video/mp4">
                            Seu navegador não suporta o elemento de vídeo.
                        </video>
                        <div class="service-content">
                            <h5 class="service-title">Limpeza Detalhada</h5>
                            <p class="service-description">Limpeza minuciosa com atenção a cada detalhe, utilizando tecnologia avançada para resultados perfeitos.</p>
                            <div class="price-tag">R$ 150,00</div>
                            <button class="btn btn-service w-100 mt-3 add-service" data-service="Limpeza Detalhada" data-price="150">Adicionar</button>
                        </div>
                    </div>
                </div>
                
                <!-- Guariba -->
                <div class="col-md-6 col-lg-3">
                    <div class="card service-card h-100">
                        <video class="service-video" controls poster="https://images.unsplash.com/photo-1560179707-f14e90ef3623?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80">
                            <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerJoyrides.mp4" type="video/mp4">
                            Seu navegador não suporta o elemento de vídeo.
                        </video>
                        <div class="service-content">
                            <h5 class="service-title">Guariba</h5>
                            <p class="service-description">Limpeza profunda do motor com tecnologia especializada para remover graxa e sujeira sem danificar componentes.</p>
                            <div class="price-tag">R$ 120,00</div>
                            <button class="btn btn-service w-100 mt-3 add-service" data-service="Guariba" data-price="120">Adicionar</button>
                        </div>
                    </div>
                </div>
                
                <!-- Higienização -->
                <div class="col-md-6 col-lg-3">
                    <div class="card service-card h-100">
                        <video class="service-video" controls poster="https://images.unsplash.com/photo-1507136566006-cfc505b114fc?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80">
                            <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerJoyrides.mp4" type="video/mp4">
                            Seu navegador não suporta o elemento de vídeo.
                        </video>
                        <div class="service-content">
                            <h5 class="service-title">Higienização</h5>
                            <p class="service-description">Processo completo de higienização com tecnologia UV e produtos bactericidas para eliminar 99,9% dos germes.</p>
                            <div class="price-tag">R$ 200,00</div>
                            <button class="btn btn-service w-100 mt-3 add-service" data-service="Higienização" data-price="200">Adicionar</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Extras Section -->
    <section id="extras" class="extras-section">
        <div class="container">
            <h2 class="section-title">Serviços Extras</h2>
            <div class="row">
                <div class="col-md-6">
                    <div class="extra-item">
                        <h5>Limpeza de Bancos</h5>
                        <p>Tecnologia de limpeza a vapor para remoção profunda de sujeira e bactérias dos bancos.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 50,00</span>
                            <button class="btn btn-service add-extra" data-service="Limpeza de Bancos" data-price="50">Adicionar</button>
                        </div>
                    </div>
                    
                    <div class="extra-item">
                        <h5>Limpeza de Teto</h5>
                        <p>Limpeza especializada do forro com produtos específicos que não danificam o material.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 40,00</span>
                            <button class="btn btn-service add-extra" data-service="Limpeza de Teto" data-price="40">Adicionar</button>
                        </div>
                    </div>
                    
                    <div class="extra-item">
                        <h5>Limpeza de Carpete</h5>
                        <p>Limpeza profunda com extratoção a vapor para remover sujeira incrustada.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 45,00</span>
                            <button class="btn btn-service add-extra" data-service="Limpeza de Carpete" data-price="45">Adicionar</button>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6">
                    <div class="extra-item">
                        <h5>Polimento Técnico</h5>
                        <p>Polimento com máquinas orbitais de dupla ação para resultado perfeito sem riscos.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 120,00</span>
                            <button class="btn btn-service add-extra" data-service="Polimento Técnico" data-price="120">Adicionar</button>
                        </div>
                    </div>
                    
                    <div class="extra-item">
                        <h5>Polimento de Faróis</h5>
                        <p>Restauração com lixamento progressivo e proteção UV para faróis como novos.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 60,00</span>
                            <button class="btn btn-service add-extra" data-service="Polimento de Faróis" data-price="60">Adicionar</button>
                        </div>
                    </div>
                    
                    <div class="extra-item">
                        <h5>Hidratação de Couro</h5>
                        <p>Hidratação profunda com produtos premium para manter o couro macio e resistente.</p>
                        <div class="d-flex justify-content-between align-items-center">
                            <span class="price-tag">R$ 70,00</span>
                            <button class="btn btn-service add-extra" data-service="Hidratação de Couro" data-price="70">Adicionar</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Section -->
    <section id="booking" class="booking-section">
        <div class="container">
            <h2 class="section-title">Agendar Serviço</h2>
            <div class="row">
                <div class="col-md-8">
                    <div class="card">
                        <div class="card-body">
                            <h5 class="card-title">Seus Serviços Selecionados</h5>
                            <div id="selected-services" class="mb-3">
                                <p class="text-muted">Nenhum serviço selecionado ainda.</p>
                            </div>
                            <div class="total-price text-end mb-4">
                                Total: R$ <span id="total-price">0,00</span>
                            </div>
                            
                            <form id="booking-form">
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="name" class="form-label">Nome Completo</label>
                                            <input type="text" class="form-control" id="name" required>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="phone" class="form-label">Telefone/WhatsApp</label>
                                            <input type="tel" class="form-control" id="phone" required>
                                        </div>
                                    </div>
                                </div>
                                <div class="mb-3">
                                    <label for="vehicle" class="form-label">Veículo (Marca/Modelo/Ano)</label>
                                    <input type="text" class="form-control" id="vehicle" required>
                                </div>
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="date" class="form-label">Data Preferencial</label>
                                            <input type="date" class="form-control" id="date" required>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label for="time" class="form-label">Horário Preferencial</label>
                                            <input type="time" class="form-control" id="time" required>
                                        </div>
                                    </div>
                                </div>
                                <div class="mb-3">
                                    <label for="notes" class="form-label">Observações</label>
                                    <textarea class="form-control" id="notes" rows="3"></textarea>
                                </div>
                                <button type="submit" class="btn btn-primary w-100 py-3">Confirmar Agendamento</button>
                            </form>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-4">
                    <div class="card mb-4">
                        <div class="card-body">
                            <h5 class="card-title">Resumo do Pedido</h5>
                            <div id="order-summary">
                                <p class="text-muted">Nenhum serviço selecionado.</p>
                            </div>
                            <div class="total-price mt-3">
                                Total: R$ <span id="summary-total">0,00</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="card">
                        <div class="card-body text-center">
                            <h5 class="card-title">Fale Conosco</h5>
                            <p class="mb-3">Tire suas dúvidas pelo WhatsApp</p>
                            <a href="https://wa.me/5538998147440?text=Olá, gostaria de informações sobre os serviços da MV Estética Automotiva" class="btn whatsapp-btn w-100" target="_blank">
                                <i class="fab fa-whatsapp"></i> WhatsApp
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Admin Panel -->
    <section id="admin" class="py-5" style="display: none;">
        <div class="container">
            <div class="admin-panel">
                <h2 class="text-center mb-4">Painel Administrativo - MV Estética Automotiva</h2>
                
                <div class="mb-4">
                    <h4><i class="fas fa-cogs me-2"></i>Configurações de Serviços</h4>
                    <div class="row">
                        <div class="col-md-6">
                            <div class="mb-3">
                                <label for="service-name" class="form-label">Nome do Serviço</label>
                                <input type="text" class="form-control" id="service-name">
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="mb-3">
                                <label for="service-price" class="form-label">Preço (R$)</label>
                                <input type="number" class="form-control" id="service-price">
                            </div>
                        </div>
                    </div>
                    <div class="mb-3">
                        <label for="service-description" class="form-label">Descrição</label>
                        <textarea class="form-control" id="service-description" rows="3"></textarea>
                    </div>
                    <button class="btn btn-primary" id="add-service-btn">Adicionar Serviço</button>
                </div>
                
                <div class="mb-4">
                    <h4><i class="fas fa-palette me-2"></i>Configurações de Cores e Temas</h4>
                    <div class="row">
                        <div class="col-md-4">
                            <div class="mb-3">
                                <label for="primary-color" class="form-label">Cor Primária (Preto)</label>
                                <input type="color" class="form-control" id="primary-color" value="#000000">
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="mb-3">
                                <label for="secondary-color" class="form-label">Cor Secundária (Vermelho)</label>
                                <input type="color" class="form-control" id="secondary-color" value="#ff0000">
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="mb-3">
                                <label for="accent-color" class="form-label">Cor de Destaque</label>
                                <input type="color" class="form-control" id="accent-color" value="#cc0000">
                            </div>
                        </div>
                    </div>
                    <button class="btn btn-primary" id="apply-colors">Aplicar Cores</button>
                </div>
                
                <div class="mb-4">
                    <h4><i class="fas fa-tag me-2"></i>Configurações de Promoções</h4>
                    <div class="mb-3">
                        <label for="promotion-text" class="form-label">Texto da Promoção</label>
                        <textarea class="form-control" id="promotion-text" rows="3"></textarea>
                    </div>
                    <button class="btn btn-primary" id="apply-promotion">Aplicar Promoção</button>
                </div>
                
                <div>
                    <h4><i class="fas fa-video me-2"></i>Gerenciar Conteúdo</h4>
                    <div class="mb-3">
                        <label for="video-url" class="form-label">URL do Vídeo</label>
                        <input type="text" class="form-control" id="video-url" placeholder="Cole a URL do vídeo do YouTube">
                    </div>
                    <button class="btn btn-primary" id="update-video">Atualizar Vídeo</button>
                </div>
                
                <div class="mt-5 pt-4 border-top">
                    <h4><i class="fas fa-key me-2"></i>Gerenciar Senha</h4>
                    <p class="text-muted">Caso tenha esquecido sua senha de administrador, você pode recuperá-la.</p>
                    <button class="btn btn-outline-light" id="forgot-password-btn">Esqueci minha senha</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Modal de Recuperação de Senha -->
    <div class="password-modal" id="passwordModal">
        <div class="password-modal-content">
            <span class="close-modal" id="closeModal">&times;</span>
            <h3 class="text-center mb-4">Recuperação de Senha</h3>
            
            <div id="recovery-step-1">
                <p>Para recuperar sua senha, informe seu email cadastrado:</p>
                <div class="mb-3">
                    <label for="recovery-email" class="form-label">Email</label>
                    <input type="email" class="form-control" id="recovery-email" placeholder="seu@email.com">
                </div>
                <button class="btn btn-primary w-100" id="send-recovery-code">Enviar Código de Recuperação</button>
            </div>
            
            <div id="recovery-step-2" style="display: none;">
                <p>Enviamos um código de recuperação para o email informado. Digite o código abaixo:</p>
                <div class="mb-3">
                    <label for="recovery-code" class="form-label">Código de Recuperação</label>
                    <input type="text" class="form-control" id="recovery-code" placeholder="Digite o código de 6 dígitos">
                </div>
                <button class="btn btn-primary w-100" id="verify-recovery-code">Verificar Código</button>
                <p class="text-center mt-3">
                    <a href="#" id="resend-code">Reenviar código</a>
                </p>
            </div>
            
            <div id="recovery-step-3" style="display: none;">
                <p>Agora defina sua nova senha:</p>
                <div class="mb-3">
                    <label for="new-password" class="form-label">Nova Senha</label>
                    <input type="password" class="form-control" id="new-password">
                </div>
                <div class="mb-3">
                    <label for="confirm-password" class="form-label">Confirmar Nova Senha</label>
                    <input type="password" class="form-control" id="confirm-password">
                </div>
                <button class="btn btn-primary w-100" id="reset-password">Redefinir Senha</button>
            </div>
            
            <div id="recovery-success" style="display: none;">
                <div class="text-center">
                    <i class="fas fa-check-circle text-success mb-3" style="font-size: 3rem;"></i>
                    <h4>Senha redefinida com sucesso!</h4>
                    <p>Sua senha foi alterada. Agora você pode acessar o painel administrativo.</p>
                    <button class="btn btn-primary" id="close-success">Fechar</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <h5>MV Estética Automotiva</h5>
                    <p>Tecnologia e excelência em cuidados automotivos.</p>
                </div>
                <div class="col-md-4">
                    <h5>Contato</h5>
                    <p><i class="fas fa-phone me-2"></i> 5538998147440</p>
                    <p><i class="fas fa-envelope me-2"></i> jeffersontulio1999@gmail.com</p>
                </div>
                <div class="col-md-4 footer-links">
                    <h5>Links Rápidos</h5>
                    <p><a href="#services">Serviços</a></p>
                    <p><a href="#extras">Extras</a></p>
                    <p><a href="#booking">Agendamento</a></p>
                </div>
            </div>
            <hr class="my-4">
            <div class="text-center">
                <p>&copy; 2023 MV Estética Automotiva. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    
    <!-- Custom JavaScript -->
    <script>
        // Variáveis para armazenar serviços selecionados
        let selectedServices = [];
        let selectedExtras = [];
        let totalPrice = 0;
        
        // Elementos DOM
        const selectedServicesEl = document.getElementById('selected-services');
        const orderSummaryEl = document.getElementById('order-summary');
        const totalPriceEl = document.getElementById('total-price');
        const summaryTotalEl = document.getElementById('summary-total');
        const bookingForm = document.getElementById('booking-form');
        const adminLink = document.getElementById('adminLink');
        const adminSection = document.getElementById('admin');
        
        // Elementos do modal de recuperação de senha
        const passwordModal = document.getElementById('passwordModal');
        const closeModal = document.getElementById('closeModal');
        const forgotPasswordBtn = document.getElementById('forgot-password-btn');
        const sendRecoveryCodeBtn = document.getElementById('send-recovery-code');
        const verifyRecoveryCodeBtn = document.getElementById('verify-recovery-code');
        const resetPasswordBtn = document.getElementById('reset-password');
        const closeSuccessBtn = document.getElementById('close-success');
        const resendCodeLink = document.getElementById('resend-code');
        
        // Adicionar serviços principais
        document.querySelectorAll('.add-service').forEach(button => {
            button.addEventListener('click', function() {
                const service = this.getAttribute('data-service');
                const price = parseFloat(this.getAttribute('data-price'));
                
                // Verificar se o serviço já foi adicionado
                if (!selectedServices.some(s => s.name === service)) {
                    selectedServices.push({ name: service, price: price });
                    updateOrderSummary();
                }
            });
        });
        
        // Adicionar serviços extras
        document.querySelectorAll('.add-extra').forEach(button => {
            button.addEventListener('click', function() {
                const service = this.getAttribute('data-service');
                const price = parseFloat(this.getAttribute('data-price'));
                
                // Verificar se o extra já foi adicionado
                if (!selectedExtras.some(s => s.name === service)) {
                    selectedExtras.push({ name: service, price: price });
                    updateOrderSummary();
                }
            });
        });
        
        // Atualizar resumo do pedido
        function updateOrderSummary() {
            // Limpar elementos
            selectedServicesEl.innerHTML = '';
            orderSummaryEl.innerHTML = '';
            totalPrice = 0;
            
            // Adicionar serviços principais
            if (selectedServices.length > 0) {
                selectedServices.forEach(service => {
                    const serviceEl = document.createElement('div');
                    serviceEl.className = 'd-flex justify-content-between align-items-center border-bottom pb-2 mb-2';
                    serviceEl.innerHTML = `
                        <span>${service.name}</span>
                        <div>
                            <span class="me-3">R$ ${service.price.toFixed(2)}</span>
                            <button class="btn btn-sm btn-outline-danger remove-service" data-service="${service.name}">Remover</button>
                        </div>
                    `;
                    selectedServicesEl.appendChild(serviceEl);
                    
                    const summaryEl = document.createElement('p');
                    summaryEl.className = 'mb-1';
                    summaryEl.innerHTML = `${service.name} - R$ ${service.price.toFixed(2)}`;
                    orderSummaryEl.appendChild(summaryEl);
                    
                    totalPrice += service.price;
                });
            }
            
            // Adicionar serviços extras
            if (selectedExtras.length > 0) {
                selectedExtras.forEach(extra => {
                    const extraEl = document.createElement('div');
                    extraEl.className = 'd-flex justify-content-between align-items-center border-bottom pb-2 mb-2';
                    extraEl.innerHTML = `
                        <span>${extra.name}</span>
                        <div>
                            <span class="me-3">R$ ${extra.price.toFixed(2)}</span>
                            <button class="btn btn-sm btn-outline-danger remove-extra" data-service="${extra.name}">Remover</button>
                        </div>
                    `;
                    selectedServicesEl.appendChild(extraEl);
                    
                    const summaryEl = document.createElement('p');
                    summaryEl.className = 'mb-1';
                    summaryEl.innerHTML = `${extra.name} - R$ ${extra.price.toFixed(2)}`;
                    orderSummaryEl.appendChild(summaryEl);
                    
                    totalPrice += extra.price;
                });
            }
            
            // Exibir mensagem se não houver serviços
            if (selectedServices.length === 0 && selectedExtras.length === 0) {
                selectedServicesEl.innerHTML = '<p class="text-muted">Nenhum serviço selecionado ainda.</p>';
                orderSummaryEl.innerHTML = '<p class="text-muted">Nenhum serviço selecionado.</p>';
            }
            
            // Atualizar preços totais
            totalPriceEl.textContent = totalPrice.toFixed(2);
            summaryTotalEl.textContent = totalPrice.toFixed(2);
            
            // Adicionar event listeners para botões de remoção
            document.querySelectorAll('.remove-service').forEach(button => {
                button.addEventListener('click', function() {
                    const serviceName = this.getAttribute('data-service');
                    selectedServices = selectedServices.filter(s => s.name !== serviceName);
                    updateOrderSummary();
                });
            });
            
            document.querySelectorAll('.remove-extra').forEach(button => {
                button.addEventListener('click', function() {
                    const serviceName = this.getAttribute('data-service');
                    selectedExtras = selectedExtras.filter(s => s.name !== serviceName);
                    updateOrderSummary();
                });
            });
        }
        
        // Processar formulário de agendamento
        bookingForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            if (selectedServices.length === 0 && selectedExtras.length === 0) {
                alert('Por favor, selecione pelo menos um serviço.');
                return;
            }
            
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const vehicle = document.getElementById('vehicle').value;
            const date = document.getElementById('date').value;
            const time = document.getElementById('time').value;
            const notes = document.getElementById('notes').value;
            
            // Simular envio de mensagem WhatsApp
            let message = `Olá, gostaria de agendar os seguintes serviços na MV Estética Automotiva:\n\n`;
            
            selectedServices.forEach(service => {
                message += `- ${service.name}: R$ ${service.price.toFixed(2)}\n`;
            });
            
            selectedExtras.forEach(extra => {
                message += `- ${extra.name}: R$ ${extra.price.toFixed(2)}\n`;
            });
            
            message += `\nTotal: R$ ${totalPrice.toFixed(2)}\n\n`;
            message += `Dados do agendamento:\n`;
            message += `Nome: ${name}\n`;
            message += `Telefone: ${phone}\n`;
            message += `Veículo: ${vehicle}\n`;
            message += `Data: ${date}\n`;
            message += `Horário: ${time}\n`;
            
            if (notes) {
                message += `Observações: ${notes}\n`;
            }
            
            // Em um ambiente real, isso seria uma integração com a API do WhatsApp
            alert(`Agendamento realizado com sucesso!\n\nUma mensagem será enviada para o WhatsApp com os detalhes:\n\n${message}`);
            
            // Limpar formulário
            bookingForm.reset();
            selectedServices = [];
            selectedExtras = [];
            updateOrderSummary();
        });
        
        // Toggle do painel administrativo
        adminLink.addEventListener('click', function(e) {
            e.preventDefault();
            const password = prompt('Digite a senha de administrador:');
            
            // Em um ambiente real, isso seria uma verificação segura no servidor
            if (password === 'admin123') {
                adminSection.style.display = 'block';
                window.scrollTo(0, document.getElementById('admin').offsetTop);
            } else {
                alert('Senha incorreta!');
            }
        });
        
        // Configurações do painel administrativo
        document.getElementById('apply-colors').addEventListener('click', function() {
            const primaryColor = document.getElementById('primary-color').value;
            const secondaryColor = document.getElementById('secondary-color').value;
            const accentColor = document.getElementById('accent-color').value;
            
            document.documentElement.style.setProperty('--primary-color', primaryColor);
            document.documentElement.style.setProperty('--secondary-color', secondaryColor);
            document.documentElement.style.setProperty('--accent-color', accentColor);
            
            alert('Cores aplicadas com sucesso!');
        });
        
        document.getElementById('apply-promotion').addEventListener('click', function() {
            const promotionText = document.getElementById('promotion-text').value;
            
            if (promotionText) {
                // Em um ambiente real, isso seria salvo no banco de dados
                alert(`Promoção aplicada: "${promotionText}"`);
            } else {
                alert('Por favor, insira o texto da promoção.');
            }
        });
        
        document.getElementById('update-video').addEventListener('click', function() {
            const videoUrl = document.getElementById('video-url').value;
            
            if (videoUrl) {
                // Em um ambiente real, isso seria salvo no banco de dados
                const iframe = document.querySelector('.video-container iframe');
                iframe.src = videoUrl;
                alert('Vídeo atualizado com sucesso!');
            } else {
                alert('Por favor, insira a URL do vídeo.');
            }
        });
        
        document.getElementById('add-service-btn').addEventListener('click', function() {
            const serviceName = document.getElementById('service-name').value;
            const servicePrice = document.getElementById('service-price').value;
            const serviceDescription = document.getElementById('service-description').value;
            
            if (serviceName && servicePrice && serviceDescription) {
                // Em um ambiente real, isso seria salvo no banco de dados
                alert(`Serviço "${serviceName}" adicionado com sucesso!`);
                
                // Limpar campos
                document.getElementById('service-name').value = '';
                document.getElementById('service-price').value = '';
                document.getElementById('service-description').value = '';
            } else {
                alert('Por favor, preencha todos os campos.');
            }
        });
        
        // Sistema de recuperação de senha
        forgotPasswordBtn.addEventListener('click', function() {
            passwordModal.style.display = 'flex';
            resetRecoveryForm();
        });
        
        closeModal.addEventListener('click', function() {
            passwordModal.style.display = 'none';
        });
        
        // Fechar modal ao clicar fora dele
        window.addEventListener('click', function(e) {
            if (e.target === passwordModal) {
                passwordModal.style.display = 'none';
            }
        });
        
        sendRecoveryCodeBtn.addEventListener('click', function() {
            const email = document.getElementById('recovery-email').value;
            
            if (!email) {
                alert('Por favor, informe seu email.');
                return;
            }
            
            // Simular envio de código por email
            alert(`Código de recuperação enviado para: ${email}\n\nEm um sistema real, um código seria enviado por email.`);
            
            // Avançar para a próxima etapa
            document.getElementById('recovery-step-1').style.display = 'none';
            document.getElementById('recovery-step-2').style.display = 'block';
        });
        
        verifyRecoveryCodeBtn.addEventListener('click', function() {
            const code = document.getElementById('recovery-code').value;
            
            if (!code) {
                alert('Por favor, digite o código de recuperação.');
                return;
            }
            
            // Simular verificação do código
            alert('Código verificado com sucesso!');
            
            // Avançar para a próxima etapa
            document.getElementById('recovery-step-2').style.display = 'none';
            document.getElementById('recovery-step-3').style.display = 'block';
        });
        
        resetPasswordBtn.addEventListener('click', function() {
            const newPassword = document.getElementById('new-password').value;
            const confirmPassword = document.getElementById('confirm-password').value;
            
            if (!newPassword || !confirmPassword) {
                alert('Por favor, preencha ambos os campos de senha.');
                return;
            }
            
            if (newPassword !== confirmPassword) {
                alert('As senhas não coincidem. Por favor, digite a mesma senha nos dois campos.');
                return;
            }
            
            // Simular redefinição de senha
            alert(`Senha redefinida com sucesso!\n\nNova senha: ${newPassword}\n\nEm um sistema real, a senha seria criptografada e armazenada com segurança.`);
            
            // Mostrar mensagem de sucesso
            document.getElementById('recovery-step-3').style.display = 'none';
            document.getElementById('recovery-success').style.display = 'block';
        });
        
        closeSuccessBtn.addEventListener('click', function() {
            passwordModal.style.display = 'none';
        });
        
        resendCodeLink.addEventListener('click', function(e) {
            e.preventDefault();
            alert('Código reenviado para seu email.');
        });
        
        function resetRecoveryForm() {
            document.getElementById('recovery-step-1').style.display = 'block';
            document.getElementById('recovery-step-2').style.display = 'none';
            document.getElementById('recovery-step-3').style.display = 'none';
            document.getElementById('recovery-success').style.display = 'none';
            
            document.getElementById('recovery-email').value = '';
            document.getElementById('recovery-code').value = '';
            document.getElementById('new-password').value = '';
            document.getElementById('confirm-password').value = '';
        }
    </script>
</body>
</html>
