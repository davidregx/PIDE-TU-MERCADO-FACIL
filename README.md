<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Mercado Fácil</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>
    <style>
        /* Estilos existentes (mantenidos) */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
  :root {
            --primary: #4CAF50;
            --primary-light: #81C784;
            --primary-dark: #2E7D32;
            --secondary: #FF9800;
            --light: #f9f9f9;
            --dark: #333;
            --gray: #e0e0e0;
            --gray-light: #f5f5f5;
            --shadow: 0 4px 6px rgba(0,0,0,0.1);
            --danger: #f44336;
            --success: #8BC34A;
            --whatsapp: #25D366;
            --fruit: #FFD54F;
            --veggie: #81C784;
            --dairy: #FFF9C4;
            --meat: #EF9A9A;
            --grain: #D7CCC8;
            --condiment: #F8BBD0;
            --clean: #BBDEFB;
            --drink: #B3E5FC;
            --custom: #BA68C8;
        }
        
  body {
            background: linear-gradient(135deg, #f5f7fa, #e4edf5);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding-bottom: 40px;
        }
        
 .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 15px;
        }
        
 header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 20px 0;
            text-align: center;
            box-shadow: var(--shadow);
            border-radius: 0 0 15px 15px;
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
        }
        
 header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: rgba(255,255,255,0.3);
        }
        
 header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            position: relative;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
  header p {
            font-size: 1rem;
            opacity: 0.9;
            max-width: 700px;
            margin: 0 auto;
            position: relative;
            padding: 0 15px;
        }
        
 .app-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
            margin-bottom: 25px;
        }
        
  .panel {
            background: white;
            border-radius: 15px;
            box-shadow: var(--shadow);
            padding: 20px;
            transition: transform 0.3s ease;
        }
        
 .panel:hover {
            transform: translateY(-5px);
        }
        
  .section-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 2px solid var(--gray);
            color: var(--primary);
            display: flex;
            align-items: center;
        }
        
  .section-title i {
            margin-right: 12px;
            background: rgba(76, 175, 80, 0.15);
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
        }
        
 .categories {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
            overflow-x: auto;
            padding-bottom: 8px;
            -webkit-overflow-scrolling: touch;
        }
        
 .category-btn {
            background: var(--light);
            border: 2px solid var(--gray);
            padding: 8px 16px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 6px;
            min-width: 100px;
            justify-content: center;
            flex-shrink: 0;
        }
        
 .category-btn:hover, .category-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
            box-shadow: 0 4px 8px rgba(76, 175, 80, 0.3);
        }
        
 .category-btn.fruit { background-color: var(--fruit); }
        .category-btn.veggie { background-color: var(--veggie); }
        .category-btn.dairy { background-color: var(--dairy); }
        .category-btn.meat { background-color: var(--meat); }
        .category-btn.grain { background-color: var(--grain); }
        .category-btn.condiment { background-color: var(--condiment); }
        .category-btn.clean { background-color: var(--clean); }
        .category-btn.drink { background-color: var(--drink); }
        .category-btn.custom { background-color: var(--custom); color: white; }
        
 .subcategory-btn {
            background: var(--light);
            border: 2px solid var(--gray);
            padding: 8px 16px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 6px;
            min-width: 120px;
            justify-content: center;
            flex-shrink: 0;
            margin: 5px;
        }
        
 .subcategory-btn:hover, .subcategory-btn.active {
            background: var(--primary-light);
            color: var(--dark);
            border-color: var(--primary);
            box-shadow: 0 4px 8px rgba(76, 175, 80, 0.2);
        }
        
 .subcategories {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
            overflow-x: auto;
            padding-bottom: 8px;
            -webkit-overflow-scrolling: touch;
        }
        
 .products-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
            gap: 12px;
            padding: 8px;
        }
        
 .product-card {
            background: white;
            border-radius: 12px;
            padding: 12px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            border: 1px solid #eee;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 100%;
        }
        
 .product-card:hover {
            transform: translateY(-7px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
 .product-icon {
            font-size: 2rem;
            margin-bottom: 8px;
            color: var(--primary);
        }
        
 .product-name {
            font-size: 1rem;
            margin-bottom: 6px;
            font-weight: 600;
            flex-grow: 1;
        }
        
 .product-options {
            display: flex;
            flex-direction: column;
            gap: 6px;
            margin-top: 8px;
        }
        
 .option-btn {
            background: #f0f7f0;
            border: none;
            border-radius: 20px;
            padding: 6px 10px;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 0.85rem;
        }
        
.option-btn:hover {
            background: var(--primary);
            color: white;
        }
        
 .back-btn {
            background: var(--gray);
            color: var(--dark);
            border: none;
            padding: 8px 15px;
            border-radius: 30px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 15px;
            font-weight: 600;
            transition: all 0.3s;
        }
        
 .back-btn:hover {
            background: var(--primary-light);
        }
        
        /* Botón para expandir productos personalizados */
 .toggle-custom-btn {
            background: var(--custom);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            font-size: 1rem;
            transition: all 0.3s;
            width: 100%;
            margin: 15px 0;
        }
        
 .toggle-custom-btn:hover {
            background: #9c27b0;
            transform: translateY(-3px);
            box-shadow: 0 4px 10px rgba(156, 39, 176, 0.3);
        }
        
 .toggle-custom-btn i {
            transition: transform 0.3s ease;
        }
        
  .toggle-custom-btn.expanded i {
            transform: rotate(45deg);
        }
        
        /* Sección de productos personalizados - inicialmente oculta */
 .custom-product-section {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 15px;
            border: 1px solid #eee;
            display: none;
            animation: slideDown 0.3s ease forwards;
        }
        
 @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
 .custom-product-section.visible {
            display: block;
        }
        
 .custom-product-title {
            font-size: 1.2rem;
            margin-bottom: 12px;
            color: #5C6BC0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
 .custom-form {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            margin-bottom: 10px;
        }
        
 .form-group {
            display: flex;
            flex-direction: column;
        }
        
  .form-group label {
            margin-bottom: 4px;
            font-weight: 600;
            color: #555;
            font-size: 0.85rem;
        }
        
  .form-group input, .form-group select {
            padding: 8px 10px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 0.9rem;
            transition: border 0.3s;
        }
        
  .form-group input:focus, .form-group select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(76, 175, 80, 0.2);
        }
        
 .add-custom-btn {
            background: #5C6BC0;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            font-size: 0.9rem;
            transition: all 0.3s;
            margin-top: 5px;
            width: 100%;
        }
        
 .add-custom-btn:hover {
            background: #3F51B5;
            transform: translateY(-3px);
            box-shadow: 0 4px 10px rgba(92, 107, 192, 0.3);
        }
        
 .search-container {
            position: relative;
            margin-bottom: 15px;
        }
        
 #product-search {
            width: 100%;
            padding: 12px 15px 12px 45px;
            border: 2px solid var(--gray);
            border-radius: 50px;
            font-size: 1rem;
            transition: all 0.3s;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
        }
        
 #product-search:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(76, 175, 80, 0.2);
        }
        
 .search-icon {
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: #777;
            font-size: 1.1rem;
        }
        
  footer {
            text-align: center;
            padding: 15px;
            margin-top: 30px;
            color: #777;
            font-size: 0.9rem;
        }
        
 .notification {
            position: fixed;
            top: 15px;
            right: 15px;
            padding: 12px 20px;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            z-index: 1000;
            transform: translateX(200%);
            transition: transform 0.4s ease;
            font-size: 0.9rem;
            max-width: 90%;
        }
        
 .notification.show {
            transform: translateX(0);
        }
        
 .notification.success {
            background: var(--success);
        }
        
 .notification.error {
            background: var(--danger);
        }
        
        /* Carrito flotante */
 .floating-cart {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 999;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            gap: 15px;
        }
        
 .cart-icon {
            background: var(--primary);
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
            cursor: pointer;
            position: relative;
            transition: all 0.3s;
        }
        
 .cart-icon:hover {
            transform: scale(1.1);
            background: var(--primary-dark);
        }
        
 .cart-count {
            position: absolute;
            top: -5px;
            right: -5px;
            background: var(--danger);
            color: white;
            width: 26px;
            height: 26px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 0.85rem;
        }
        
        /* Modal para boleta - NUEVO DISEÑO */
  .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 10000;
            overflow-y: auto;
            padding: 20px;
        }
        
 .modal-content {
            background: white;
            max-width: 800px;
            margin: 40px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            position: relative;
        }
        
  .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--danger);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            cursor: pointer;
            z-index: 10;
            transition: all 0.3s;
        }
        
 .close-modal:hover {
            transform: rotate(90deg);
            background: #d32f2f;
        }
        
 .modal-header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 25px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
 .modal-header::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: rgba(255,255,255,0.3);
        }
        
 .modal-header h2 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }
        
 .modal-body {
            padding: 25px;
            max-height: 70vh;
            overflow-y: auto;
        }
        
 .receipt-content {
            background: #fff;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 25px;
            position: relative;
            overflow: hidden;
            border: 1px solid var(--gray-light);
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
 .receipt-header {
            text-align: center;
            margin-bottom: 25px;
            position: relative;
        }
        
 .receipt-header h2 {
            color: var(--primary);
            font-size: 1.8rem;
            letter-spacing: 1px;
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
            margin-bottom: 15px;
        }
        
 .receipt-header h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--primary);
            border-radius: 3px;
        }
        
 .receipt-date {
            color: #777;
            font-size: 0.95rem;
            margin-top: 5px;
        }
        
.receipt-items {
            margin: 25px 0;
        }
        
.receipt-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px solid #f0f0f0;
            transition: background 0.2s;
        }
        
 .receipt-item:hover {
            background: rgba(76, 175, 80, 0.05);
        }
        
 .receipt-item:last-child {
            border-bottom: none;
        }
        
 .receipt-item-info {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
 .receipt-item-icon {
            width: 30px;
            height: 30px;
            background: rgba(76, 175, 80, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 0.9rem;
        }
        
 .receipt-item-details {
            display: flex;
            flex-direction: column;
        }
        
.receipt-item-name {
            font-weight: 600;
            margin-bottom: 3px;
        }
        
.receipt-item-unit {
            font-size: 0.85rem;
            color: #777;
        }
        
 .receipt-item-price {
            font-weight: 600;
            color: var(--primary);
        }
        
 .receipt-total {
            display: flex;
            justify-content: space-between;
            padding: 18px 0;
            margin-top: 15px;
            border-top: 2px solid var(--primary);
            font-weight: bold;
            font-size: 1.3rem;
            background: rgba(76, 175, 80, 0.05);
            padding: 15px 20px;
            border-radius: 8px;
            color: var(--primary-dark);
        }
        
 .action-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
 .action-btn {
            padding: 14px 30px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 12px;
            transition: all 0.3s;
            font-size: 1.05rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
 .capture-btn {
            background: var(--primary);
            color: white;
        }
        
 .whatsapp-btn {
            background: var(--whatsapp);
            color: white;
        }
        
 .clear-btn {
            background: var(--danger);
            color: white;
        }
        
 .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.15);
        }
        
.action-btn i {
            font-size: 1.3rem;
        }
        
        /* Mejoras para dispositivos móviles */
 @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
 header {
                padding: 15px 0;
                border-radius: 0 0 10px 10px;
                margin-bottom: 15px;
            }
            
 header h1 {
                font-size: 1.8rem;
            }
            
 header p {
                font-size: 0.9rem;
            }
            
 .app-container {
                gap: 15px;
                margin-bottom: 20px;
            }
            
 .panel {
                padding: 15px;
                border-radius: 12px;
            }
            
 .section-title {
                font-size: 1.3rem;
                margin-bottom: 15px;
                padding-bottom: 10px;
            }
            
 .section-title i {
                width: 32px;
                height: 32px;
                font-size: 0.9rem;
            }
            
 .categories {
                gap: 8px;
                margin-bottom: 15px;
                padding-bottom: 5px;
            }
            
 .category-btn {
                padding: 6px 12px;
                font-size: 0.85rem;
                min-width: 85px;
            }
            
 .subcategory-btn {
                padding: 6px 12px;
                font-size: 0.8rem;
                min-width: 100px;
            }
            
 .products-container {
                grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
                gap: 10px;
            }
            
 .product-card {
                padding: 10px;
            }
            
 .product-icon {
                font-size: 1.8rem;
            }
            
 .product-name {
                font-size: 0.9rem;
            }
            
 .option-btn {
                padding: 5px 8px;
                font-size: 0.8rem;
            }
            
 .toggle-custom-btn {
                padding: 10px 15px;
                font-size: 0.95rem;
            }
            
 .custom-product-section {
                padding: 12px;
                margin-top: 10px;
            }
            
 .custom-product-title {
                font-size: 1.1rem;
                margin-bottom: 10px;
            }
            
 .custom-form {
                grid-template-columns: 1fr;
                gap: 8px;
            }
            
 .form-group label {
                font-size: 0.85rem;
            }
            
 .form-group input, .form-group select {
                padding: 8px 10px;
                font-size: 0.9rem;
            }
            
 .add-custom-btn {
                padding: 10px 15px;
                font-size: 0.95rem;
            }
            
            /* Carrito flotante */
 .floating-cart {
                bottom: 20px;
                right: 20px;
            }
            
 .cart-icon {
                width: 60px;
                height: 60px;
                font-size: 1.6rem;
            }
            
 .cart-count {
                width: 24px;
                height: 24px;
                font-size: 0.8rem;
            }
            
            /* Modal */
 .modal-content {
                margin: 20px auto;
            }
            
.modal-header {
                padding: 20px 15px;
            }
            
 .modal-header h2 {
                font-size: 1.5rem;
            }
            
 .modal-body {
                padding: 15px;
            }
            
 .receipt-content {
                padding: 20px;
            }
            
  .receipt-header h2 {
                font-size: 1.6rem;
            }
            
 .action-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
 .action-btn {
                width: 100%;
                justify-content: center;
            }
        }
        
 @media (max-width: 480px) {
            .products-container {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
            
 .category-btn {
                min-width: 75px;
                font-size: 0.8rem;
                padding: 5px 10px;
            }
            
 .subcategory-btn {
                min-width: 90px;
                font-size: 0.75rem;
                padding: 5px 8px;
            }
            
 .product-name {
                font-size: 0.85rem;
            }
            
 .option-btn {
                font-size: 0.75rem;
            }
            
 .floating-cart {
                bottom: 15px;
                right: 15px;
            }
            
 .cart-icon {
                width: 55px;
                height: 55px;
                font-size: 1.5rem;
            }
            
 .custom-form {
                grid-template-columns: 1fr;
            }
        }
 </style>
</head>
<body>
    <header>
        <div class="container">
            <h1><i class="fas fa-shopping-basket"></i> Lista de Mercado Fácil</h1>
            <p>Haz tu lista de mercado de forma rápida y sencilla</p>
        </div>
    </header>
    
 <div class="container">
        <div class="app-container">
            <div class="panel">
                <h2 class="section-title"><i class="fas fa-list"></i> Productos</h2>
                
 <div class="search-container">
                    <i class="fas fa-search search-icon"></i>
                    <input type="text" id="product-search" placeholder="Buscar productos...">
                </div>
                
                <!-- Botón para expandir productos personalizados -->
<button id="toggle-custom-btn" class="toggle-custom-btn">
                    <i class="fas fa-plus-circle"></i> Agregar Producto Personalizado
                </button>
                
                <!-- Sección de productos personalizados (inicialmente oculta) -->
 <div id="custom-product-section" class="custom-product-section">
                    <h3 class="custom-product-title"><i class="fas fa-edit"></i> Nuevo Producto</h3>
                    
 <div class="custom-form">
                        <div class="form-group">
                            <label for="custom-name">Nombre</label>
                            <input type="text" id="custom-name" placeholder="Ej: Aceite de Oliva">
                        </div>
                        
 <div class="form-group">
                            <label for="custom-unit">Unidad</label>
                            <select id="custom-unit">
                                <option value="unidad">Unidad</option>
                                <option value="kg">Kilogramo</option>
                                <option value="gr">Gramo</option>
                                <option value="litro">Litro</option>
                                <option value="ml">Mililitro</option>
                                <option value="paquete">Paquete</option>
                                <option value="caja">Caja</option>
                                <option value="docena">Docena</option>
                            </select>
                        </div>
                        
 <div class="form-group">
                            <label for="custom-quantity">Cantidad</label>
                            <input type="number" id="custom-quantity" min="1" value="1">
                        </div>
                        
 <div class="form-group">
                            <label for="custom-price">Precio (opc)</label>
                            <input type="number" id="custom-price" min="0" step="0.01" placeholder="Opcional">
                        </div>
                    </div>
                    
  <button class="add-custom-btn" id="add-custom-btn">
                        <i class="fas fa-plus"></i> Agregar Producto
                    </button>
                </div>
                
 <div class="categories" id="categories">
                    <button class="category-btn fruit active" data-category="all">
                        <i class="fas fa-star"></i> Todos
                    </button>
                    <button class="category-btn fruit" data-category="frutas">
                        <i class="fas fa-apple-alt"></i> Frutas
                    </button>
                    <button class="category-btn veggie" data-category="verduras">
                        <i class="fas fa-leaf"></i> Verduras
                    </button>
                    <button class="category-btn dairy" data-category="lacteos">
                        <i class="fas fa-cheese"></i> Lácteos
                    </button>
                    <button class="category-btn meat" data-category="carnes">
                        <i class="fas fa-drumstick-bite"></i> Carnes
                    </button>
                    <button class="category-btn grain" data-category="granos">
                        <i class="fas fa-bread-slice"></i> Granos
                    </button>
                    <button class="category-btn condiment" data-category="condimentos">
                        <i class="fas fa-mortar-pestle"></i> Condimentos
                    </button>
                    <button class="category-btn clean" data-category="limpieza">
                        <i class="fas fa-pump-soap"></i> Limpieza
                    </button>
                    <button class="category-btn drink" data-category="bebidas">
                        <i class="fas fa-wine-bottle"></i> Bebidas
                    </button>
                    <button class="category-btn custom" data-category="personalizado">
                        <i class="fas fa-plus-circle"></i> Personalizados
                    </button>
                </div>
                
                <!-- Contenedor para subcategorías -->
 <div class="subcategories" id="subcategories" style="display: none;"></div>
                
                <!-- Botón para volver a categorías -->
<button id="back-to-categories" class="back-btn" style="display: none;">
                    <i class="fas fa-arrow-left"></i> Volver a Categorías
                </button>
                
<div class="products-container" id="products-container">
                    <!-- Los productos se cargarán aquí con JavaScript -->
                </div>
            </div>
        </div>
    </div>
    
    <!-- Carrito flotante -->
 <div class="floating-cart">
        <div class="cart-icon" id="cart-icon">
            <i class="fas fa-shopping-basket"></i>
            <span class="cart-count" id="cart-count">0</span>
        </div>
    </div>
    
    <!-- Modal para la boleta - NUEVO DISEÑO -->
<div class="modal" id="receipt-modal">
        <div class="modal-content">
            <div class="close-modal" id="close-modal">
                <i class="fas fa-times"></i>
            </div>
            <div class="modal-header">
                <h2>Boleta de Compra</h2>
                <div class="receipt-date" id="current-date"></div>
            </div>
            <div class="modal-body">
                <div class="receipt-content" id="receipt-content">
                    <div class="receipt-header">
                        <h2><i class="fas fa-shopping-basket"></i> LISTA DE MERCADO</h2>
                    </div>
                    
 <div class="receipt-items" id="receipt-items">
                        <div class="empty-receipt">Selecciona productos para generar tu boleta</div>
                    </div>
                    
<div class="receipt-total">
                        <div>TOTAL:</div>
                        <div id="receipt-total">S/ 0.00</div>
                    </div>
                </div>
                
 <div class="action-buttons">
                    <button class="action-btn capture-btn" id="capture-btn">
                        <i class="fas fa-camera"></i> Capturar Boleta
                    </button>
                    <button class="action-btn whatsapp-btn" id="whatsapp-btn">
                        <i class="fab fa-whatsapp"></i> Enviar Pedido
                    </button>
                    <button class="action-btn clear-btn" id="clear-btn">
                        <i class="fas fa-trash"></i> Limpiar Todo
                    </button>
                </div>
            </div>
        </div>
    </div>
    
 <div id="notification" class="notification"></div>
    
<footer>
        <div class="container">
            <p>Lista de Mercado Fácil &copy; 2023 - Envía tus pedidos al WhatsApp: 975842622</p>
        </div>
    </footer>
    
 <script>
        // Datos de productos con todas las opciones
        const products = [
            // Frutas
            { id: 1, name: "Plátano de seda", category: "frutas", subcategory: "frutas-frescas", icon: "banana", options: [
                { size: "1 kg", price: 2.00 },
                { size: "5 kg", price: 9.50 }
            ]},
            { id: 2, name: "Plátano isla", category: "frutas", subcategory: "frutas-frescas", icon: "banana", options: [
                { size: "1 kg", price: 2.50 },
                { size: "5 kg", price: 12.00 }
            ]},
            { id: 3, name: "Plátano bellaco", category: "frutas", subcategory: "frutas-frescas", icon: "banana", options: [
                { size: "1 kg", price: 2.20 },
                { size: "5 kg", price: 10.50 }
            ]},
            { id: 4, name: "Naranja de jugo", category: "frutas", subcategory: "frutas-frescas", icon: "orange", options: [
                { size: "1 kg", price: 1.50 },
                { size: "5 kg", price: 7.00 }
            ]},
            { id: 5, name: "Naranja de mesa", category: "frutas", subcategory: "frutas-frescas", icon: "orange", options: [
                { size: "1 kg", price: 2.00 },
                { size: "5 kg", price: 9.50 }
            ]},
            { id: 6, name: "Piña golden", category: "frutas", subcategory: "frutas-tropicales", icon: "pineapple", options: [
                { size: "1 unidad (1.5-2 kg)", price: 3.50 },
                { size: "Trozos 500 g", price: 2.00 }
            ]},
            { id: 7, name: "Piña hawaiana", category: "frutas", subcategory: "frutas-tropicales", icon: "pineapple", options: [
                { size: "1 unidad (1.5-2 kg)", price: 3.80 },
                { size: "Trozos 500 g", price: 2.20 }
            ]},
            { id: 8, name: "Manzana Fuji", category: "frutas", subcategory: "frutas-frescas", icon: "apple-alt", options: [
                { size: "1 kg", price: 4.50 },
                { size: "3 kg", price: 13.00 }
            ]},
            { id: 9, name: "Manzana Gala", category: "frutas", subcategory: "frutas-frescas", icon: "apple-alt", options: [
                { size: "1 kg", price: 4.80 },
                { size: "3 kg", price: 14.00 }
            ]},
            { id: 10, name: "Manzana nacional", category: "frutas", subcategory: "frutas-frescas", icon: "apple-alt", options: [
                { size: "1 kg", price: 3.00 },
                { size: "3 kg", price: 8.50 }
            ]},
            { id: 11, name: "Arándanos", category: "frutas", subcategory: "frutas-tropicales", icon: "berries", options: [
                { size: "Bandeja 125 g", price: 10.00 },
                { size: "Bandeja 250 g", price: 18.00 }
            ]},
            { id: 12, name: "Mango Kent", category: "frutas", subcategory: "frutas-tropicales", icon: "mango", options: [
                { size: "1 kg", price: 3.00 },
                { size: "5 kg", price: 14.00 }
            ]},
            { id: 13, name: "Mango Edward", category: "frutas", subcategory: "frutas-tropicales", icon: "mango", options: [
                { size: "1 kg", price: 3.50 },
                { size: "5 kg", price: 16.50 }
            ]},
            { id: 14, name: "Sandía", category: "frutas", subcategory: "frutas-frescas", icon: "watermelon", options: [
                { size: "1 kg", price: 1.20 },
                { size: "1 unidad (5-8 kg)", price: 8.00 },
                { size: "Trozos 1 kg", price: 1.50 }
            ]},
            { id: 15, name: "Melón coquito", category: "frutas", subcategory: "frutas-frescas", icon: "melon", options: [
                { size: "1 unidad (2-3 kg)", price: 4.00 },
                { size: "Trozos 1 kg", price: 1.80 }
            ]},
            { id: 16, name: "Melón verde", category: "frutas", subcategory: "frutas-frescas", icon: "melon", options: [
                { size: "1 unidad (2-3 kg)", price: 4.50 },
                { size: "Trozos 1 kg", price: 2.00 }
            ]},
            { id: 17, name: "Tangelo", category: "frutas", subcategory: "frutas-frescas", icon: "citrus", options: [
                { size: "1 kg", price: 2.50 },
                { size: "5 kg", price: 12.00 }
            ]},
            { id: 18, name: "Mandarina", category: "frutas", subcategory: "frutas-frescas", icon: "tangerine", options: [
                { size: "1 kg", price: 2.30 },
                { size: "5 kg", price: 11.00 }
            ]},
            { id: 19, name: "Uva red globe", category: "frutas", subcategory: "frutas-frescas", icon: "grapes", options: [
                { size: "1 kg", price: 5.00 },
                { size: "3 kg", price: 14.50 }
            ]},
            { id: 20, name: "Fresa", category: "frutas", subcategory: "frutas-frescas", icon: "strawberry", options: [
                { size: "Bandeja 250 g", price: 3.50 },
                { size: "Bandeja 500 g", price: 6.00 }
            ]},
            { id: 21, name: "Palta Hass", category: "frutas", subcategory: "frutas-frescas", icon: "avocado", options: [
                { size: "1 kg", price: 8.00 },
                { size: "1 unidad (200-250 g)", price: 2.00 }
            ]},
            { id: 22, name: "Palta fuerte", category: "frutas", subcategory: "frutas-frescas", icon: "avocado", options: [
                { size: "1 kg", price: 7.50 },
                { size: "1 unidad (200-250 g)", price: 1.80 }
            ]},
            { id: 23, name: "Limón", category: "frutas", subcategory: "frutas-frescas", icon: "lemon", options: [
                { size: "1 kg", price: 2.00 },
                { size: "5 kg", price: 9.50 }
            ]},
            { id: 24, name: "Granadilla", category: "frutas", subcategory: "frutas-tropicales", icon: "passion-fruit", options: [
                { size: "1 kg", price: 4.50 },
                { size: "5 kg", price: 21.00 }
            ]},
            { id: 25, name: "Chirimoya", category: "frutas", subcategory: "frutas-tropicales", icon: "custard-apple", options: [
                { size: "1 kg", price: 5.00 },
                { size: "1 unidad (500-700 g)", price: 3.50 }
            ]},
            
            // Verduras
            { id: 26, name: "Papa yungay", category: "verduras", subcategory: "tuberculos", icon: "potato", options: [
                { size: "1 kg", price: 1.00 },
                { size: "5 kg", price: 4.80 }
            ]},
            { id: 27, name: "Papa huayro", category: "verduras", subcategory: "tuberculos", icon: "potato", options: [
                { size: "1 kg", price: 1.20 },
                { size: "5 kg", price: 5.80 }
            ]},
            { id: 28, name: "Papa peruanita", category: "verduras", subcategory: "tuberculos", icon: "potato", options: [
                { size: "1 kg", price: 1.30 },
                { size: "5 kg", price: 6.20 }
            ]},
            { id: 29, name: "Papa canchan", category: "verduras", subcategory: "tuberculos", icon: "potato", options: [
                { size: "1 kg", price: 1.15 },
                { size: "5 kg", price: 5.50 }
            ]},
            { id: 30, name: "Cebolla cabeza roja", category: "verduras", subcategory: "verduras-frescas", icon: "onion", options: [
                { size: "1 kg", price: 1.30 },
                { size: "5 kg", price: 6.20 }
            ]},
            { id: 31, name: "Cebolla blanca", category: "verduras", subcategory: "verduras-frescas", icon: "onion", options: [
                { size: "1 kg", price: 1.50 },
                { size: "5 kg", price: 7.20 }
            ]},
            { id: 32, name: "Tomate katia", category: "verduras", subcategory: "verduras-frescas", icon: "tomato", options: [
                { size: "1 kg", price: 1.80 },
                { size: "5 kg", price: 8.50 }
            ]},
            { id: 33, name: "Tomate italiano", category: "verduras", subcategory: "verduras-frescas", icon: "tomato", options: [
                { size: "1 kg", price: 2.00 },
                { size: "5 kg", price: 9.50 }
            ]},
            { id: 34, name: "Zapallo macre", category: "verduras", subcategory: "verduras-frescas", icon: "pumpkin", options: [
                { size: "1 kg", price: 1.00 },
                { size: "5 kg", price: 4.80 }
            ]},
            { id: 35, name: "Zapallo loche", category: "verduras", subcategory: "verduras-frescas", icon: "pumpkin", options: [
                { size: "1 kg", price: 1.50 },
                { size: "5 kg", price: 7.20 }
            ]},
            { id: 36, name: "Camote morado", category: "verduras", subcategory: "tuberculos", icon: "sweet-potato", options: [
                { size: "1 kg", price: 1.10 },
                { size: "5 kg", price: 5.20 }
            ]},
            { id: 37, name: "Camote amarillo", category: "verduras", subcategory: "tuberculos", icon: "sweet-potato", options: [
                { size: "1 kg", price: 1.00 },
                { size: "5 kg", price: 4.80 }
            ]},
            { id: 38, name: "Haba verde", category: "verduras", subcategory: "legumbres", icon: "beans", options: [
                { size: "1 kg", price: 1.20 },
                { size: "5 kg", price: 5.80 }
            ]},
            { id: 39, name: "Brócoli", category: "verduras", subcategory: "verduras-frescas", icon: "broccoli", options: [
                { size: "1 kg", price: 3.50 },
                { size: "1 unidad (500-700 g)", price: 2.00 }
            ]},
            { id: 40, name: "Espárrago verde", category: "verduras", subcategory: "verduras-frescas", icon: "asparagus", options: [
                { size: "Atado 250 g", price: 2.50 },
                { size: "Atado 500 g", price: 4.00 }
            ]},
            { id: 41, name: "Zanahoria", category: "verduras", subcategory: "verduras-frescas", icon: "carrot", options: [
                { size: "1 kg", price: 1.50 },
                { size: "5 kg", price: 7.20 }
            ]},
            { id: 42, name: "Lechuga hidropónica", category: "verduras", subcategory: "verduras-frescas", icon: "lettuce", options: [
                { size: "1 unidad", price: 2.00 },
                { size: "3 unidades", price: 5.50 }
            ]},
            { id: 43, name: "Lechuga criolla", category: "verduras", subcategory: "verduras-frescas", icon: "lettuce", options: [
                { size: "1 unidad", price: 1.50 },
                { size: "3 unidades", price: 4.00 }
            ]},
            { id: 44, name: "Coliflor", category: "verduras", subcategory: "verduras-frescas", icon: "cauliflower", options: [
                { size: "1 unidad (1-1.5 kg)", price: 3.50 },
                { size: "1 kg", price: 2.50 }
            ]},
            { id: 45, name: "Apio", category: "verduras", subcategory: "verduras-frescas", icon: "celery", options: [
                { size: "Atado 250 g", price: 1.50 },
                { size: "Atado 500 g", price: 2.00 }
            ]},
            { id: 46, name: "Ají amarillo", category: "verduras", subcategory: "condimentos", icon: "pepper", options: [
                { size: "1 kg", price: 4.00 },
                { size: "500 g", price: 2.20 }
            ]},
            { id: 47, name: "Ají panca", category: "verduras", subcategory: "condimentos", icon: "pepper", options: [
                { size: "1 kg", price: 3.50 },
                { size: "500 g", price: 2.00 }
            ]},
            { id: 48, name: "Ajo", category: "verduras", subcategory: "condimentos", icon: "garlic", options: [
                { size: "1 kg", price: 10.00 },
                { size: "100 g", price: 1.20 }
            ]},
            { id: 49, name: "Beterraga", category: "verduras", subcategory: "verduras-frescas", icon: "beet", options: [
                { size: "1 kg", price: 1.80 },
                { size: "5 kg", price: 8.50 }
            ]},
            { id: 50, name: "Espinaca", category: "verduras", subcategory: "verduras-frescas", icon: "spinach", options: [
                { size: "Atado 250 g", price: 1.50 },
                { size: "Atado 500 g", price: 2.00 }
            ]},
            
            // Lácteos
            { id: 51, name: "Leche evaporada Gloria", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Bolsa 400 ml", price: 2.50 },
                { size: "Lata 400 g", price: 3.00 },
                { size: "Lata 170 g", price: 1.50 }
            ]},
            { id: 52, name: "Leche entera Gloria", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 3.00 },
                { size: "Tetra Pak 1 litro", price: 5.00 },
                { size: "Bolsa 900 ml", price: 3.50 }
            ]},
            { id: 53, name: "Leche entera Laive", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 2.80 },
                { size: "Tetra Pak 1 litro", price: 4.80 }
            ]},
            { id: 54, name: "Leche entera Ideal", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Bolsa 450 ml", price: 2.00 },
                { size: "Bolsa 900 ml", price: 3.50 }
            ]},
            { id: 55, name: "Leche entera Bonlé", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 2.50 },
                { size: "Tetra Pak 1 litro", price: 4.50 }
            ]},
            { id: 56, name: "Leche descremada Gloria", category: "lacteos", subcategory: "leches", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 3.20 },
                { size: "Tetra Pak 1 litro", price: 5.20 }
            ]},
            { id: 57, name: "Yogur natural Gloria", category: "lacteos", subcategory: "yogures", icon: "yogurt", options: [
                { size: "Botella 500 ml", price: 4.00 },
                { size: "Botella 1 litro", price: 7.00 }
            ]},
            { id: 58, name: "Yogur natural Laive", category: "lacteos", subcategory: "yogures", icon: "yogurt", options: [
                { size: "Botella 500 ml", price: 3.80 },
                { size: "Botella 1 litro", price: 6.50 }
            ]},
            { id: 59, name: "Yogur Yogoso (sabor)", category: "lacteos", subcategory: "yogures", icon: "yogurt", options: [
                { size: "Envase 120 g", price: 1.20 },
                { size: "Envase 1 kg", price: 8.00 }
            ]},
            { id: 60, name: "Yogur griego Gloria", category: "lacteos", subcategory: "yogures", icon: "yogurt", options: [
                { size: "Envase 150 g", price: 2.50 },
                { size: "Envase 900 g", price: 12.00 }
            ]},
            { id: 61, name: "Queso fresco Gloria", category: "lacteos", subcategory: "quesos", icon: "cheese", options: [
                { size: "500 g", price: 9.50 },
                { size: "1 kg", price: 18.00 }
            ]},
            { id: 62, name: "Queso andino artesanal", category: "lacteos", subcategory: "quesos", icon: "cheese", options: [
                { size: "500 g", price: 8.00 },
                { size: "1 kg", price: 15.00 }
            ]},
            { id: 63, name: "Queso paria", category: "lacteos", subcategory: "quesos", icon: "cheese", options: [
                { size: "500 g", price: 8.50 },
                { size: "1 kg", price: 16.00 }
            ]},
            { id: 64, name: "Queso edam Laive", category: "lacteos", subcategory: "quesos", icon: "cheese", options: [
                { size: "500 g", price: 10.50 },
                { size: "1 kg", price: 20.00 }
            ]},
            { id: 65, name: "Mantequilla Gloria", category: "lacteos", subcategory: "mantequillas", icon: "butter", options: [
                { size: "Barra 100 g", price: 3.50 },
                { size: "Barra 200 g", price: 6.00 }
            ]},
            { id: 66, name: "Mantequilla Manty", category: "lacteos", subcategory: "mantequillas", icon: "butter", options: [
                { size: "Barra 100 g", price: 3.00 },
                { size: "Barra 200 g", price: 5.50 }
            ]},
            { id: 67, name: "Leche de almendra Silk", category: "lacteos", subcategory: "leches-vegetales", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 7.00 },
                { size: "Tetra Pak 1 litro", price: 12.00 }
            ]},
            { id: 68, name: "Leche de soya Natura", category: "lacteos", subcategory: "leches-vegetales", icon: "milk", options: [
                { size: "Tetra Pak 500 ml", price: 6.00 },
                { size: "Tetra Pak 1 litro", price: 10.00 }
            ]},
            { id: 69, name: "Crema de leche Gloria", category: "lacteos", subcategory: "cremas", icon: "cream", options: [
                { size: "Lata 100 g", price: 2.50 },
                { size: "Lata 200 g", price: 4.00 }
            ]},
            { id: 70, name: "Manjar blanco Gloria", category: "lacteos", subcategory: "dulces", icon: "cream", options: [
                { size: "Pote 200 g", price: 3.50 },
                { size: "Pote 400 g", price: 6.50 }
            ]},
            
            // Carnes
            { id: 71, name: "Pollo entero fresco", category: "carnes", subcategory: "pollo", icon: "chicken", options: [
                { size: "1 kg", price: 9.00 },
                { size: "2 kg", price: 17.50 }
            ]},
            { id: 72, name: "Pechuga de pollo San Fernando", category: "carnes", subcategory: "pollo", icon: "chicken", options: [
                { size: "500 g", price: 6.50 },
                { size: "1 kg", price: 12.00 }
            ]},
            { id: 73, name: "Muslos de pollo Redondos", category: "carnes", subcategory: "pollo", icon: "chicken", options: [
                { size: "500 g", price: 5.50 },
                { size: "1 kg", price: 10.00 }
            ]},
            { id: 74, name: "Alas de pollo fresco", category: "carnes", subcategory: "pollo", icon: "chicken", options: [
                { size: "500 g", price: 4.50 },
                { size: "1 kg", price: 8.50 }
            ]},
            { id: 75, name: "Carne de res (bistec)", category: "carnes", subcategory: "res", icon: "beef", options: [
                { size: "500 g", price: 13.00 },
                { size: "1 kg", price: 25.00 }
            ]},
            { id: 76, name: "Lomo fino de res", category: "carnes", subcategory: "res", icon: "beef", options: [
                { size: "500 g", price: 18.00 },
                { size: "1 kg", price: 35.00 }
            ]},
            { id: 77, name: "Carne molida de res", category: "carnes", subcategory: "res", icon: "beef", options: [
                { size: "500 g", price: 10.50 },
                { size: "1 kg", price: 20.00 }
            ]},
            { id: 78, name: "Hígado de res", category: "carnes", subcategory: "res", icon: "liver", options: [
                { size: "500 g", price: 8.00 },
                { size: "1 kg", price: 15.00 }
            ]},
            { id: 79, name: "Chuleta de cerdo", category: "carnes", subcategory: "cerdo", icon: "pork", options: [
                { size: "500 g", price: 9.50 },
                { size: "1 kg", price: 18.00 }
            ]},
            { id: 80, name: "Costilla de cerdo", category: "carnes", subcategory: "cerdo", icon: "pork", options: [
                { size: "500 g", price: 8.50 },
                { size: "1 kg", price: 16.00 }
            ]},
            { id: 81, name: "Pernil de cerdo", category: "carnes", subcategory: "cerdo", icon: "pork", options: [
                { size: "500 g", price: 10.50 },
                { size: "1 kg", price: 20.00 }
            ]},
            { id: 82, name: "Pescado chita fresco", category: "carnes", subcategory: "pescados", icon: "fish", options: [
                { size: "500 g", price: 8.00 },
                { size: "1 kg", price: 15.00 }
            ]},
            { id: 83, name: "Pescado corvina fresco", category: "carnes", subcategory: "pescados", icon: "fish", options: [
                { size: "500 g", price: 10.50 },
                { size: "1 kg", price: 20.00 }
            ]},
            { id: 84, name: "Pescado lenguado fresco", category: "carnes", subcategory: "pescados", icon: "fish", options: [
                { size: "500 g", price: 9.50 },
                { size: "1 kg", price: 18.00 }
            ]},
            { id: 85, name: "Salmón (importado)", category: "carnes", subcategory: "pescados", icon: "fish", options: [
                { size: "500 g", price: 26.00 },
                { size: "1 kg", price: 50.00 }
            ]},
            { id: 86, name: "Camarones frescos", category: "carnes", subcategory: "mariscos", icon: "shrimp", options: [
                { size: "500 g", price: 13.00 },
                { size: "1 kg", price: 25.00 }
            ]},
            { id: 87, name: "Calamar fresco", category: "carnes", subcategory: "mariscos", icon: "squid", options: [
                { size: "500 g", price: 8.00 },
                { size: "1 kg", price: 15.00 }
            ]},
            { id: 88, name: "Jamón inglés San Fernando", category: "carnes", subcategory: "embutidos", icon: "ham", options: [
                { size: "Paquete 100 g", price: 3.50 },
                { size: "Paquete 200 g", price: 6.00 }
            ]},
            { id: 89, name: "Salchicha Braedt", category: "carnes", subcategory: "embutidos", icon: "sausage", options: [
                { size: "Paquete 250 g", price: 5.50 },
                { size: "Paquete 500 g", price: 10.00 }
            ]},
            { id: 90, name: "Chorizo artesanal", category: "carnes", subcategory: "embutidos", icon: "sausage", options: [
                { size: "500 g", price: 10.50 },
                { size: "1 kg", price: 20.00 }
            ]},
            { id: 91, name: "Mortadela Laive", category: "carnes", subcategory: "embutidos", icon: "sausage", options: [
                { size: "Paquete 250 g", price: 4.50 },
                { size: "Paquete 500 g", price: 8.00 }
            ]},
            
            // Granos
            { id: 92, name: "Arroz Valle Norte", category: "granos", subcategory: "arroz", icon: "rice", options: [
                { size: "Bolsa 750 g", price: 3.00 },
                { size: "Bolsa 1 kg", price: 4.00 },
                { size: "Bolsa 5 kg", price: 18.00 }
            ]},
            { id: 93, name: "Arroz Costeño", category: "granos", subcategory: "arroz", icon: "rice", options: [
                { size: "Bolsa 750 g", price: 3.20 },
                { size: "Bolsa 1 kg", price: 4.20 },
                { size: "Bolsa 5 kg", price: 18.00 }
            ]},
            { id: 94, name: "Arroz integral Costeño", category: "granos", subcategory: "arroz", icon: "rice", options: [
                { size: "Bolsa 500 g", price: 3.00 },
                { size: "Bolsa 1 kg", price: 5.00 }
            ]},
            { id: 95, name: "Quinua blanca", category: "granos", subcategory: "granos-andinos", icon: "quinoa", options: [
                { size: "Bolsa 250 g", price: 3.50 },
                { size: "Bolsa 500 g", price: 6.00 },
                { size: "Bolsa 1 kg", price: 11.00 }
            ]},
            { id: 96, name: "Quinua roja", category: "granos", subcategory: "granos-andinos", icon: "quinoa", options: [
                { size: "Bolsa 250 g", price: 4.00 },
                { size: "Bolsa 500 g", price: 7.00 }
            ]},
            { id: 97, name: "Quinua negra", category: "granos", subcategory: "granos-andinos", icon: "quinoa", options: [
                { size: "Bolsa 250 g", price: 4.20 },
                { size: "Bolsa 500 g", price: 7.50 }
            ]},
            { id: 98, name: "Frijol canario", category: "granos", subcategory: "legumbres", icon: "beans", options: [
                { size: "Bolsa 500 g", price: 2.80 },
                { size: "Bolsa 1 kg", price: 5.00 }
            ]},
            { id: 99, name: "Frijol negro", category: "granos", subcategory: "legumbres", icon: "beans", options: [
                { size: "Bolsa 500 g", price: 2.50 },
                { size: "Bolsa 1 kg", price: 4.50 }
            ]},
            { id: 100, name: "Frijol castilla", category: "granos", subcategory: "legumbres", icon: "beans", options: [
                { size: "Bolsa 500 g", price: 3.00 },
                { size: "Bolsa 1 kg", price: 5.50 }
            ]},
            { id: 101, name: "Lentejas", category: "granos", subcategory: "legumbres", icon: "lentils", options: [
                { size: "Bolsa 250 g", price: 2.00 },
                { size: "Bolsa 500 g", price: 3.50 }
            ]},
            { id: 102, name: "Lentejas rojas", category: "granos", subcategory: "legumbres", icon: "lentils", options: [
                { size: "Bolsa 250 g", price: 2.20 },
                { size: "Bolsa 500 g", price: 4.00 }
            ]},
            { id: 103, name: "Maíz chullpi", category: "granos", subcategory: "maiz", icon: "corn", options: [
                { size: "Bolsa 500 g", price: 2.50 },
                { size: "Bolsa 1 kg", price: 4.00 }
            ]},
            { id: 104, name: "Maíz morado", category: "granos", subcategory: "maiz", icon: "corn", options: [
                { size: "Bolsa 500 g", price: 3.00 },
                { size: "Bolsa 1 kg", price: 5.50 }
            ]},
            { id: 105, name: "Maíz cancha", category: "granos", subcategory: "maiz", icon: "corn", options: [
                { size: "Bolsa 500 g", price: 2.50 },
                { size: "Bolsa 1 kg", price: 4.50 }
            ]},
            { id: 106, name: "Garbanzo", category: "granos", subcategory: "legumbres", icon: "chickpea", options: [
                { size: "Bolsa 500 g", price: 2.80 },
                { size: "Bolsa 1 kg", price: 5.00 }
            ]},
            { id: 107, name: "Trigo mote", category: "granos", subcategory: "granos-andinos", icon: "wheat", options: [
                { size: "Bolsa 500 g", price: 2.00 },
                { size: "Bolsa 1 kg", price: 3.50 }
            ]},
            
            // Condimentos
            { id: 108, name: "Comino molido Huarango", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 25 g", price: 1.50 },
                { size: "Bolsa 50 g", price: 2.50 },
                { size: "Bolsa 100 g", price: 4.00 }
            ]},
            { id: 109, name: "Comino entero artesanal", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 50 g", price: 2.00 },
                { size: "Bolsa 100 g", price: 3.00 }
            ]},
            { id: 110, name: "Pimienta molida Huarango", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 25 g", price: 1.80 },
                { size: "Bolsa 50 g", price: 3.00 }
            ]},
            { id: 111, name: "Pimienta entera artesanal", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 25 g", price: 2.00 },
                { size: "Bolsa 50 g", price: 3.50 }
            ]},
            { id: 112, name: "Orégano molido Huarango", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 25 g", price: 1.20 },
                { size: "Bolsa 50 g", price: 2.00 }
            ]},
            { id: 113, name: "Ají panca molido Huarango", category: "condimentos", subcategory: "ajies", icon: "spice", options: [
                { size: "Bolsa 50 g", price: 2.00 },
                { size: "Bolsa 100 g", price: 3.50 }
            ]},
            { id: 114, name: "Ají amarillo molido artesanal", category: "condimentos", subcategory: "ajies", icon: "spice", options: [
                { size: "Bolsa 50 g", price: 2.20 },
                { size: "Bolsa 100 g", price: 4.00 }
            ]},
            { id: 115, name: "Ajo molido McCormick", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Frasco 25 g", price: 3.00 },
                { size: "Frasco 50 g", price: 5.00 }
            ]},
            { id: 116, name: "Cúrcuma molida Huarango", category: "condimentos", subcategory: "especias", icon: "spice", options: [
                { size: "Bolsa 25 g", price: 1.50 },
                { size: "Bolsa 50 g", price: 2.50 }
            ]},
            { id: 117, name: "Pasta de ají amarillo Doña Gusta", category: "condimentos", subcategory: "ajies", icon: "spice", options: [
                { size: "Frasco 100 g", price: 3.50 },
                { size: "Frasco 200 g", price: 6.00 }
            ]},
            { id: 118, name: "Pasta de ají panca Doña Gusta", category: "condimentos", subcategory: "ajies", icon: "spice", options: [
                { size: "Frasco 100 g", price: 3.20 },
                { size: "Frasco 200 g", price: 5.50 }
            ]},
            { id: 119, name: "Laurel artesanal", category: "condimentos", subcategory: "hierbas", icon: "spice", options: [
                { size: "Bolsa 10 g", price: 1.00 },
                { size: "Bolsa 20 g", price: 1.50 }
            ]},
            { id: 120, name: "Sazonador Maggi", category: "condimentos", subcategory: "sazonadores", icon: "spice", options: [
                { size: "Sobre 50 g", price: 1.80 },
                { size: "Sobre 100 g", price: 3.00 }
            ]},
            { id: 121, name: "Caldo en cubos Maggi (pollo)", category: "condimentos", subcategory: "caldos", icon: "spice", options: [
                { size: "Paquete 4 cubos", price: 1.50 },
                { size: "Paquete 8 cubos", price: 2.50 }
            ]},
            { id: 122, name: "Caldo en cubos Knorr (carne)", category: "condimentos", subcategory: "caldos", icon: "spice", options: [
                { size: "Paquete 4 cubos", price: 1.50 },
                { size: "Paquete 8 cubos", price: 2.50 }
            ]},
            { id: 123, name: "Vinagre blanco Lider", category: "condimentos", subcategory: "vinagres", icon: "vinegar", options: [
                { size: "Botella 250 ml", price: 2.00 },
                { size: "Botella 500 ml", price: 3.00 }
            ]},
            { id: 124, name: "Vinagre de manzana Capri", category: "condimentos", subcategory: "vinagres", icon: "vinegar", options: [
                { size: "Botella 250 ml", price: 3.00 },
                { size: "Botella 500 ml", price: 5.00 }
            ]},
            
            // Limpieza
            { id: 125, name: "Detergente Sapolio", category: "limpieza", subcategory: "detergentes", icon: "soap", options: [
                { size: "Bolsa 500 g", price: 3.50 },
                { size: "Bolsa 1 kg", price: 6.00 },
                { size: "Bolsa 3 kg", price: 16.00 }
            ]},
            { id: 126, name: "Detergente Bolívar", category: "limpieza", subcategory: "detergentes", icon: "soap", options: [
                { size: "Bolsa 500 g", price: 3.20 },
                { size: "Bolsa 1 kg", price: 5.50 },
                { size: "Bolsa 3 kg", price: 15.00 }
            ]},
            { id: 127, name: "Detergente líquido Bolívar", category: "limpieza", subcategory: "detergentes", icon: "soap", options: [
                { size: "Botella 1 litro", price: 7.00 },
                { size: "Botella 3 litros", price: 18.00 }
            ]},
            { id: 128, name: "Detergente líquido Ariel", category: "limpieza", subcategory: "detergentes", icon: "soap", options: [
                { size: "Botella 1 litro", price: 8.00 },
                { size: "Botella 3 litros", price: 20.00 }
            ]},
            { id: 129, name: "Jabón líquido lavavajillas Sapolio", category: "limpieza", subcategory: "lavavajillas", icon: "soap", options: [
                { size: "Botella 500 ml", price: 4.50 },
                { size: "Botella 900 ml", price: 7.00 }
            ]},
            { id: 130, name: "Jabón líquido lavavajillas Ayudín", category: "limpieza", subcategory: "lavavajillas", icon: "soap", options: [
                { size: "Botella 500 ml", price: 5.00 },
                { size: "Botella 900 ml", price: 8.00 }
            ]},
            { id: 131, name: "Jabón líquido lavavajillas Patito", category: "limpieza", subcategory: "lavavajillas", icon: "soap", options: [
                { size: "Botella 500 ml", price: 4.20 },
                { size: "Botella 900 ml", price: 6.50 }
            ]},
            { id: 132, name: "Lejía Clorox", category: "limpieza", subcategory: "lejias", icon: "bleach", options: [
                { size: "Botella 500 ml", price: 2.50 },
                { size: "Botella 1 litro", price: 4.00 },
                { size: "Bidón 2 litros", price: 7.00 }
            ]},
            { id: 133, name: "Lejía Sapolio", category: "limpieza", subcategory: "lejias", icon: "bleach", options: [
                { size: "Botella 500 ml", price: 2.20 },
                { size: "Botella 1 litro", price: 3.50 },
                { size: "Bidón 2 litros", price: 6.00 }
            ]},
            { id: 134, name: "Lejía Clorinda", category: "limpieza", subcategory: "lejias", icon: "bleach", options: [
                { size: "Botella 1 litro", price: 3.80 },
                { size: "Bidón 2 litros", price: 6.00 }
            ]},
            { id: 135, name: "Limpiador multiusos Mr. Músculo", category: "limpieza", subcategory: "multiusos", icon: "cleaner", options: [
                { size: "Botella 500 ml", price: 6.00 },
                { size: "Botella 900 ml", price: 8.50 }
            ]},
            { id: 136, name: "Limpiador multiusos Sapolio", category: "limpieza", subcategory: "multiusos", icon: "cleaner", options: [
                { size: "Botella 500 ml", price: 5.50 },
                { size: "Botella 1 litro", price: 8.00 }
            ]},
            { id: 137, name: "Desinfectante Poett", category: "limpieza", subcategory: "desinfectantes", icon: "cleaner", options: [
                { size: "Botella 500 ml", price: 5.00 },
                { size: "Botella 900 ml", price: 7.50 }
            ]},
            { id: 138, name: "Jabón en barra Sapolio", category: "limpieza", subcategory: "jabones", icon: "soap", options: [
                { size: "Unidad 100 g", price: 1.50 },
                { size: "Unidad 200 g", price: 2.50 }
            ]},
            { id: 139, name: "Esponjas Scotch-Brite", category: "limpieza", subcategory: "utensilios", icon: "sponge", options: [
                { size: "Paquete 1 unidad", price: 2.50 },
                { size: "Paquete 2 unidades", price: 4.00 }
            ]},
            { id: 140, name: "Bolsas de basura Lider", category: "limpieza", subcategory: "bolsas", icon: "trash-bag", options: [
                { size: "Paquete 10 unidades (30 litros)", price: 4.00 },
                { size: "Paquete 10 unidades (50 litros)", price: 5.00 }
            ]},
            
            // Bebidas
            { id: 141, name: "Agua Cielo", category: "bebidas", subcategory: "aguas", icon: "water", options: [
                { size: "Botella 500 ml", price: 1.50 },
                { size: "Botella 1 litro", price: 2.50 },
                { size: "Botella 2.5 litros", price: 4.50 },
                { size: "Bidón 7 litros", price: 10.00 }
            ]},
            { id: 142, name: "Agua San Luis", category: "bebidas", subcategory: "aguas", icon: "water", options: [
                { size: "Botella 500 ml", price: 1.80 },
                { size: "Botella 1 litro", price: 2.80 },
                { size: "Botella 2.5 litros", price: 5.00 },
                { size: "Bidón 7 litros", price: 11.00 }
            ]},
            { id: 143, name: "Agua San Mateo", category: "bebidas", subcategory: "aguas", icon: "water", options: [
                { size: "Botella 500 ml", price: 1.70 },
                { size: "Botella 1 litro", price: 2.70 },
                { size: "Botella 2.5 litros", price: 4.80 },
                { size: "Bidón 7 litros", price: 10.00 }
            ]},
            { id: 144, name: "Inca Kola", category: "bebidas", subcategory: "gaseosas", icon: "soda", options: [
                { size: "Botella 500 ml", price: 2.50 },
                { size: "Botella 1 litro", price: 4.00 },
                { size: "Botella 1.5 litros", price: 6.00 },
                { size: "Botella 3 litros", price: 10.00 }
            ]},
            { id: 145, name: "Coca-Cola", category: "bebidas", subcategory: "gaseosas", icon: "soda", options: [
                { size: "Botella 500 ml", price: 2.50 },
                { size: "Botella 1 litro", price: 4.00 },
                { size: "Botella 1.5 litros", price: 6.00 },
                { size: "Botella 3 litros", price: 10.00 }
            ]},
            { id: 146, name: "Sprite", category: "bebidas", subcategory: "gaseosas", icon: "soda", options: [
                { size: "Botella 500 ml", price: 2.30 },
                { size: "Botella 1.5 litros", price: 5.50 },
                { size: "Botella 3 litros", price: 9.50 }
            ]},
            { id: 147, name: "Fanta", category: "bebidas", subcategory: "gaseosas", icon: "soda", options: [
                { size: "Botella 500 ml", price: 2.30 },
                { size: "Botella 1.5 litros", price: 5.50 },
                { size: "Botella 3 litros", price: 9.50 }
            ]},
            { id: 148, name: "Cerveza Pilsen", category: "bebidas", subcategory: "cervezas", icon: "beer", options: [
                { size: "Botella 330 ml", price: 3.50 },
                { size: "Botella 620 ml", price: 5.50 },
                { size: "Lata 355 ml", price: 4.00 }
            ]},
            { id: 149, name: "Cerveza Cristal", category: "bebidas", subcategory: "cervezas", icon: "beer", options: [
                { size: "Botella 330 ml", price: 3.80 },
                { size: "Botella 620 ml", price: 5.80 },
                { size: "Lata 355 ml", price: 4.00 }
            ]},
            { id: 150, name: "Cerveza Cusqueña (dorada)", category: "bebidas", subcategory: "cervezas", icon: "beer", options: [
                { size: "Botella 330 ml", price: 4.50 },
                { size: "Botella 620 ml", price: 6.50 },
                { size: "Lata 355 ml", price: 4.80 }
            ]},
            { id: 151, name: "Cerveza Cusqueña (negra)", category: "bebidas", subcategory: "cervezas", icon: "beer", options: [
                { size: "Botella 330 ml", price: 5.00 },
                { size: "Botella 620 ml", price: 7.00 }
            ]},
            { id: 152, name: "Café instantáneo Nescafé", category: "bebidas", subcategory: "cafes", icon: "coffee", options: [
                { size: "Frasco 50 g", price: 4.50 },
                { size: "Frasco 100 g", price: 7.50 },
                { size: "Frasco 200 g", price: 12.00 }
            ]},
            { id: 153, name: "Café molido Altomayo", category: "bebidas", subcategory: "cafes", icon: "coffee", options: [
                { size: "Bolsa 125 g", price: 5.50 },
                { size: "Bolsa 250 g", price: 10.00 },
                { size: "Bolsa 500 g", price: 18.00 }
            ]},
            { id: 154, name: "Café molido Tostado", category: "bebidas", subcategory: "cafes", icon: "coffee", options: [
                { size: "Bolsa 125 g", price: 4.50 },
                { size: "Bolsa 250 g", price: 8.00 }
            ]},
            { id: 155, name: "Jugo Frugos (naranja)", category: "bebidas", subcategory: "jugos", icon: "juice", options: [
                { size: "Botella 500 ml", price: 3.00 },
                { size: "Botella 1 litro", price: 5.00 },
                { size: "Botella 2 litros", price: 8.50 }
            ]},
            { id: 156, name: "Jugo Pulp (mango)", category: "bebidas", subcategory: "jugos", icon: "juice", options: [
                { size: "Botella 500 ml", price: 2.80 },
                { size: "Botella 1 litro", price: 4.50 },
                { size: "Botella 2 litros", price: 8.00 }
            ]},
            { id: 157, name: "Vino Tabernero (tinto)", category: "bebidas", subcategory: "vinos", icon: "wine", options: [
                { size: "Botella 375 ml", price: 12.00 },
                { size: "Botella 750 ml", price: 20.00 }
            ]},
            { id: 158, name: "Vino Santiago Queirolo (blanco)", category: "bebidas", subcategory: "vinos", icon: "wine", options: [
                { size: "Botella 375 ml", price: 13.00 },
                { size: "Botella 750 ml", price: 22.00 }
            ]},
            { id: 159, name: "Pisco Queirolo", category: "bebidas", subcategory: "licores", icon: "wine", options: [
                { size: "Botella 375 ml", price: 15.00 },
                { size: "Botella 750 ml", price: 25.00 }
            ]},
            { id: 160, name: "Red Bull", category: "bebidas", subcategory: "energizantes", icon: "energy", options: [
                { size: "Lata 250 ml", price: 6.00 },
                { size: "Lata 473 ml", price: 8.50 }
            ]},
            { id: 161, name: "Monster Energy", category: "bebidas", subcategory: "energizantes", icon: "energy", options: [
                { size: "Lata 250 ml", price: 5.50 },
                { size: "Lata 473 ml", price: 7.00 }
            ]},
            { id: 162, name: "Volt", category: "bebidas", subcategory: "energizantes", icon: "energy", options: [
                { size: "Lata 250 ml", price: 5.50 },
                { size: "Lata 473 ml", price: 7.50 }
            ]},
            { id: 163, name: "Chicha morada artesanal", category: "bebidas", subcategory: "refrescos", icon: "juice", options: [
                { size: "Botella 500 ml", price: 3.00 },
                { size: "Botella 1 litro", price: 5.00 },
                { size: "Botella 2 litros", price: 8.50 }
            ]},
            { id: 164, name: "Té Lipton (limón)", category: "bebidas", subcategory: "tes", icon: "tea", options: [
                { size: "Botella 500 ml", price: 2.50 },
                { size: "Botella 1.5 litros", price: 5.50 }
            ]}
        ];

        // Mapeo de iconos para FontAwesome
        const customIcons = {
            "banana": "banana",
            "orange": "orange",
            "pineapple": "pineapple",
            "apple-alt": "apple-alt",
            "berries": "strawberry",
            "mango": "mango",
            "watermelon": "watermelon",
            "melon": "lemon",
            "citrus": "lemon",
            "tangerine": "lemon",
            "grapes": "grapes",
            "strawberry": "strawberry",
            "avocado": "avocado",
            "lemon": "lemon",
            "passion-fruit": "lemon",
            "custard-apple": "apple-alt",
            "potato": "carrot",
            "onion": "onion",
            "tomato": "tomato",
            "pumpkin": "carrot",
            "sweet-potato": "carrot",
            "beans": "seedling",
            "broccoli": "carrot",
            "asparagus": "carrot",
            "carrot": "carrot",
            "lettuce": "leaf",
            "cauliflower": "carrot",
            "celery": "carrot",
            "pepper": "pepper-hot",
            "garlic": "garlic",
            "beet": "carrot",
            "spinach": "leaf",
            "milk": "wine-bottle",
            "cheese": "cheese",
            "egg": "egg",
            "drumstick": "drumstick",
            "bacon": "bacon",
            "fish": "fish",
            "rice": "bread-slice",
            "seedling": "seedling",
            "mortar-pestle": "mortar-pestle",
            "pump-soap": "pump-soap",
            "wine-bottle": "wine-bottle",
            "yogurt": "cupcake",
            "butter": "cheese",
            "cream": "ice-cream",
            "chicken": "drumstick",
            "beef": "drumstick",
            "liver": "drumstick",
            "pork": "drumstick",
            "shrimp": "fish",
            "squid": "fish",
            "ham": "drumstick",
            "sausage": "hotdog",
            "quinoa": "seedling",
            "lentils": "seedling",
            "corn": "corn",
            "chickpea": "seedling",
            "wheat": "seedling",
            "spice": "mortar-pestle",
            "vinegar": "wine-bottle",
            "soap": "soap",
            "bleach": "soap",
            "cleaner": "soap",
            "sponge": "soap",
            "trash-bag": "trash",
            "water": "water",
            "soda": "wine-bottle",
            "beer": "beer",
            "coffee": "coffee",
            "juice": "wine-bottle",
            "wine": "wine-glass",
            "energy": "bolt",
            "tea": "mug-hot"
        };

        // Variables globales
        let cart = [];
        let currentCategory = 'all';
        let currentSubcategory = null;
        const whatsappNumber = "975842622";

        // Inicializar la aplicación
        document.addEventListener('DOMContentLoaded', () => {
            // Mostrar fecha actual en la boleta
            const now = new Date();
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('current-date').textContent = now.toLocaleDateString('es-ES', options);
            
            // Inicializar productos
            renderProducts(currentCategory, currentSubcategory);
            
            // Configurar eventos
            setupEventListeners();
            
            // Actualizar contador del carrito
            updateCartCount();
        });

        // Configurar los event listeners
        function setupEventListeners() {
            // Eventos para botones de categorías
            document.querySelectorAll('.category-btn').forEach(button => {
                button.addEventListener('click', () => {
                    // Remover clase activa de todos los botones
                    document.querySelectorAll('.category-btn').forEach(btn => {
                        btn.classList.remove('active');
                    });
                    
                    // Añadir clase activa al botón seleccionado
                    button.classList.add('active');
                    
                    // Actualizar categoría y subcategoría
                    currentCategory = button.getAttribute('data-category');
                    currentSubcategory = null;
                    
                    // Mostrar subcategorías si no es 'all'
                    if (currentCategory !== 'all') {
                        renderSubcategories(currentCategory);
                        document.getElementById('subcategories').style.display = 'flex';
                        document.getElementById('back-to-categories').style.display = 'none';
                    } else {
                        document.getElementById('subcategories').style.display = 'none';
                        document.getElementById('back-to-categories').style.display = 'none';
                        renderProducts(currentCategory, currentSubcategory);
                    }
                    
                    // Limpiar búsqueda
                    document.getElementById('product-search').value = '';
                });
            });
            
            // Botón de volver a categorías
            document.getElementById('back-to-categories').addEventListener('click', () => {
                currentSubcategory = null;
                document.getElementById('subcategories').style.display = 'flex';
                document.getElementById('back-to-categories').style.display = 'none';
                renderProducts(currentCategory, currentSubcategory);
            });
            
            // Botón de captura de boleta
            document.getElementById('capture-btn').addEventListener('click', captureReceipt);
            
            // Botón de enviar por WhatsApp
            document.getElementById('whatsapp-btn').addEventListener('click', sendToWhatsApp);
            
            // Botón de limpiar todo
            document.getElementById('clear-btn').addEventListener('click', clearAll);
            
            // Evento para el buscador
            document.getElementById('product-search').addEventListener('input', searchProducts);
            
            // Botón para agregar producto personalizado
            document.getElementById('add-custom-btn').addEventListener('click', addCustomProduct);
            
            // Botón para abrir modal del carrito
            document.getElementById('cart-icon').addEventListener('click', () => {
                document.getElementById('receipt-modal').style.display = 'block';
                renderReceipt();
            });
            
            // Botón para cerrar modal
            document.getElementById('close-modal').addEventListener('click', () => {
                document.getElementById('receipt-modal').style.display = 'none';
            });
            
            // Botón para expandir/colapsar productos personalizados
            document.getElementById('toggle-custom-btn').addEventListener('click', () => {
                const customSection = document.getElementById('custom-product-section');
                const toggleBtn = document.getElementById('toggle-custom-btn');
                
                customSection.classList.toggle('visible');
                toggleBtn.classList.toggle('expanded');
                
                // Cambiar el texto del botón según el estado
                if (customSection.classList.contains('visible')) {
                    toggleBtn.innerHTML = '<i class="fas fa-times"></i> Cancelar';
                } else {
                    toggleBtn.innerHTML = '<i class="fas fa-plus-circle"></i> Agregar Producto Personalizado';
                }
            });
        }

        // Función para renderizar subcategorías
        function renderSubcategories(category) {
            const subcategoriesContainer = document.getElementById('subcategories');
            subcategoriesContainer.innerHTML = '';
            
            // Obtener subcategorías únicas para esta categoría
            const subcategories = [...new Set(products
                .filter(p => p.category === category)
                .map(p => p.subcategory)
            )];
            
            // Crear botones para cada subcategoría
            subcategories.forEach(subcategory => {
                const button = document.createElement('button');
                button.className = 'subcategory-btn';
                button.textContent = subcategory;
                button.addEventListener('click', () => {
                    currentSubcategory = subcategory;
                    renderProducts(currentCategory, currentSubcategory);
                    document.getElementById('subcategories').style.display = 'none';
                    document.getElementById('back-to-categories').style.display = 'block';
                });
                subcategoriesContainer.appendChild(button);
            });
        }

        // Función para agregar producto personalizado
        function addCustomProduct() {
            const nameInput = document.getElementById('custom-name');
            const unitInput = document.getElementById('custom-unit');
            const quantityInput = document.getElementById('custom-quantity');
            const priceInput = document.getElementById('custom-price');
            
            const name = nameInput.value.trim();
            const unit = unitInput.value;
            const quantity = parseInt(quantityInput.value) || 1;
            const price = parseFloat(priceInput.value) || 0.00;
            
            if (!name) {
                showNotification('Ingresa un nombre para el producto', 'error');
                return;
            }
            
            // Crear nuevo producto personalizado
            const newProduct = {
                id: Date.now(), // ID único basado en timestamp
                name: name,
                category: "personalizado",
                subcategory: "personalizados",
                icon: "shopping-basket", // Icono genérico
                options: [
                    { size: unit, price: price }
                ]
            };
            
            // Agregar al array de productos
            products.push(newProduct);
            
            // Actualizar vista de productos
            renderProducts(currentCategory, currentSubcategory);
            
            // Limpiar campos
            nameInput.value = '';
            quantityInput.value = '1';
            priceInput.value = '';
            
            // Mostrar notificación
            showNotification(`Producto personalizado "${name}" añadido`, 'success');
            
            // Cambiar a la categoría de personalizados
            document.querySelectorAll('.category-btn').forEach(btn => {
                btn.classList.remove('active');
                if (btn.getAttribute('data-category') === 'personalizado') {
                    btn.classList.add('active');
                }
            });
            currentCategory = 'personalizado';
            currentSubcategory = null;
            document.getElementById('subcategories').style.display = 'none';
            document.getElementById('back-to-categories').style.display = 'none';
            renderProducts('personalizado', null);
            
            // Colapsar la sección de productos personalizados
            document.getElementById('custom-product-section').classList.remove('visible');
            document.getElementById('toggle-custom-btn').classList.remove('expanded');
            document.getElementById('toggle-custom-btn').innerHTML = '<i class="fas fa-plus-circle"></i> Agregar Producto Personalizado';
        }

        // Función de búsqueda de productos
        function searchProducts() {
            const searchTerm = document.getElementById('product-search').value.toLowerCase();
            
            if (!searchTerm) {
                if (currentCategory === 'all') {
                    renderProducts('all', null);
                } else if (currentSubcategory) {
                    renderProducts(currentCategory, currentSubcategory);
                } else {
                    renderSubcategories(currentCategory);
                    document.getElementById('subcategories').style.display = 'flex';
                    document.getElementById('back-to-categories').style.display = 'none';
                }
                return;
            }
            
            // Filtrar productos que coincidan con el término de búsqueda
            const filteredProducts = products.filter(product => 
                product.name.toLowerCase().includes(searchTerm)
            );
            
            renderProducts(filteredProducts);
        }

        // Renderizar productos según categoría y subcategoría
        function renderProducts(categoryOrProducts, subcategory = null) {
            const productsContainer = document.getElementById('products-container');
            productsContainer.innerHTML = '';
            
            let productsToShow;
            
            if (Array.isArray(categoryOrProducts)) {
                // Si es un array (búsqueda)
                productsToShow = categoryOrProducts;
            } else if (categoryOrProducts === 'all') {
                productsToShow = products;
            } else if (subcategory) {
                productsToShow = products.filter(p => p.category === categoryOrProducts && p.subcategory === subcategory);
            } else {
                productsToShow = products.filter(p => p.category === categoryOrProducts);
            }
            
            if (productsToShow.length === 0) {
                productsContainer.innerHTML = '<p class="empty-receipt">No se encontraron productos</p>';
                return;
            }
            
            productsToShow.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                // Añadir clase especial para productos personalizados
                if (product.category === 'personalizado') {
                    productCard.classList.add('custom-product-card');
                }
                
                // Obtener el icono correcto
                const iconClass = customIcons[product.icon] || 'shopping-basket';
                
                productCard.innerHTML = `
                    <div class="product-icon">
                        <i class="fas fa-${iconClass}"></i>
                    </div>
                    <div class="product-name">${product.name}</div>
                    <div class="product-options">
                        ${product.options.map((option, index) => `
                            <button class="option-btn" data-id="${product.id}" data-option="${index}">
                                ${option.size} - S/ ${option.price.toFixed(2)}
                            </button>
                        `).join('')}
                    </div>
                `;
                productsContainer.appendChild(productCard);
                
                // Eventos para botones de opciones
                productCard.querySelectorAll('.option-btn').forEach(button => {
                    button.addEventListener('click', (e) => {
                        e.stopPropagation();
                        const productId = parseInt(button.getAttribute('data-id'));
                        const optionIndex = parseInt(button.getAttribute('data-option'));
                        addToCart(productId, optionIndex);
                    });
                });
            });
        }

        // Añadir producto al carrito
        function addToCart(productId, optionIndex) {
            const product = products.find(p => p.id === productId);
            
            if (!product) return;
            
            const option = product.options[optionIndex];
            
            // Buscar si el producto con esta opción ya está en el carrito
            const existingItem = cart.find(item => 
                item.id === productId && item.optionIndex === optionIndex
            );
            
            if (existingItem) {
                // Incrementar cantidad si ya existe
                existingItem.quantity++;
            } else {
                // Añadir nuevo producto al carrito
                cart.push({
                    id: productId,
                    name: product.name,
                    optionIndex: optionIndex,
                    size: option.size,
                    price: option.price,
                    quantity: 1,
                    icon: product.icon
                });
            }
            
            // Mostrar notificación
            showNotification(`"${product.name} (${option.size})" añadido al carrito`, 'success');
            
            // Actualizar contador del carrito
            updateCartCount();
            
            // Actualizar boleta si el modal está abierto
            if (document.getElementById('receipt-modal').style.display === 'block') {
                renderReceipt();
            }
        }

        // Actualizar contador del carrito flotante
        function updateCartCount() {
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            document.getElementById('cart-count').textContent = totalItems;
        }

        // Renderizar la boleta en el modal
        function renderReceipt() {
            const receiptItems = document.getElementById('receipt-items');
            const receiptTotal = document.getElementById('receipt-total');
            
            if (cart.length === 0) {
                receiptItems.innerHTML = '<div class="empty-receipt">Selecciona productos para generar tu boleta</div>';
                receiptTotal.textContent = 'S/ 0.00';
                return;
            }
            
            // Generar HTML para los productos de la boleta
            let receiptHTML = '';
            let totalPrice = 0;
            
            cart.forEach(item => {
                const subtotal = item.price * item.quantity;
                totalPrice += subtotal;
                
                // Obtener el icono correcto
                const iconClass = customIcons[item.icon] || 'shopping-basket';
                
                receiptHTML += `
                    <div class="receipt-item">
                        <div class="receipt-item-info">
                            <div class="receipt-item-icon">
                                <i class="fas fa-${iconClass}"></i>
                            </div>
                            <div class="receipt-item-details">
                                <div class="receipt-item-name">${item.name}</div>
                                <div class="receipt-item-unit">${item.quantity} x ${item.size}</div>
                            </div>
                        </div>
                        <div class="receipt-item-price">S/ ${subtotal.toFixed(2)}</div>
                    </div>
                `;
            });
            
            receiptItems.innerHTML = receiptHTML;
            receiptTotal.textContent = `S/ ${totalPrice.toFixed(2)}`;
        }

        // Capturar la boleta como imagen (MEJORADO)
        function captureReceipt() {
            if (cart.length === 0) {
                showNotification('Tu carrito está vacío. Añade productos para generar una boleta.', 'error');
                return;
            }
            
            const receiptContent = document.getElementById('receipt-content');
            
            // Configuración para capturar todo el contenido, incluso fuera de la vista
            const options = {
                scale: 2, // Mejor calidad
                useCORS: true,
                allowTaint: true,
                scrollX: 0,
                scrollY: 0,
                windowWidth: receiptContent.scrollWidth,
                windowHeight: receiptContent.scrollHeight
            };
            
            html2canvas(receiptContent, options).then(canvas => {
                // Crear un enlace de descarga
                const link = document.createElement('a');
                link.download = `lista-mercado-${new Date().toISOString().slice(0, 10)}.png`;
                link.href = canvas.toDataURL('image/png');
                link.click();
                
                showNotification('Boleta capturada con éxito', 'success');
            });
        }

        // Enviar la lista por WhatsApp
        function sendToWhatsApp() {
            if (cart.length === 0) {
                showNotification('Tu carrito está vacío. Añade productos para enviar por WhatsApp.', 'error');
                return;
            }
            
            // Crear texto del mensaje
            let message = `*¡Hola! Tengo un pedido de mercado:*\n\n`;
            
            cart.forEach(item => {
                message += `- *${item.name}*: ${item.quantity} x ${item.size} (S/ ${item.price.toFixed(2)} c/u)\n`;
            });
            
            const totalPrice = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            message += `\n*Total: S/ ${totalPrice.toFixed(2)}*\n\n`;
            message += `*Por favor, envíame la captura de la boleta para hacer el presupuesto.*\n`;
            message += `*Número de contacto:* ${whatsappNumber}`;
            
            // Codificar el mensaje para URL
            const encodedMessage = encodeURIComponent(message);
            
            // Abrir WhatsApp con el mensaje
            window.open(`https://wa.me/${whatsappNumber}?text=${encodedMessage}`, '_blank');
            
            showNotification('Pedido enviado por WhatsApp', 'success');
        }

        // Limpiar todo el carrito
        function clearAll() {
            if (cart.length === 0) {
                showNotification('El carrito ya está vacío', 'error');
                return;
            }
            
            cart = [];
            updateCartCount();
            renderReceipt();
            showNotification('Carrito limpiado con éxito', 'success');
        }

        // Mostrar notificación
        function showNotification(message, type) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.className = `notification ${type} show`;
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }
    </script>
</body>
</html>
