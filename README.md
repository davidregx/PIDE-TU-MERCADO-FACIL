<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Mercado - Perú</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

 body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 10px;
            color: #333;
        }

 .container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            animation: slideIn 0.6s ease-out;
            position: relative;
            padding-bottom: 80px;
        }

 @keyframes slideIn {
            from { transform: translateY(30px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

 h1 {
            text-align: center;
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.8rem;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

 .input-section {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 20px;
        }

 .input-group {
            width: 100%;
        }

  input, select {
            width: 100%;
            padding: 14px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s ease;
            background: white;
        }

  input:focus, select:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

 .btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 14px 20px;
            border-radius: 12px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            width: 100%;
            margin-top: 5px;
        }

 .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

.btn:active {
            transform: translateY(0);
        }

 .btn-whatsapp {
            background: linear-gradient(45deg, #25d366, #128c7e);
        }

 .btn-whatsapp:hover {
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.3);
        }

 .btn-capture {
            background: linear-gradient(45deg, #ff6b6b, #ee5a52);
        }

 .btn-capture:hover {
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.3);
        }

 .btn-back {
            background: linear-gradient(45deg, #6c757d, #5a6268);
            margin-bottom: 15px;
        }

 .lista-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px;
            margin: 8px 0;
            background: linear-gradient(135deg, #f8f9ff, #e8f2ff);
            border-radius: 12px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
            animation: itemSlideIn 0.4s ease-out;
        }

  @keyframes itemSlideIn {
            from { transform: translateX(-20px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

 .lista-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 3px 10px rgba(102, 126, 234, 0.2);
        }

 .item-info {
            flex: 1;
        }

  .item-nombre {
            font-weight: 600;
            color: #333;
            font-size: 1rem;
        }

 .item-detalles {
            color: #666;
            font-size: 0.85rem;
            margin-top: 3px;
        }

.item-precio {
            font-weight: bold;
            color: #667eea;
            font-size: 1.1rem;
            margin-right: 10px;
        }

 .btn-eliminar {
            background: linear-gradient(45deg, #ff4757, #ff3838);
            color: white;
            border: none;
            padding: 8px 12px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 12px;
            transition: all 0.3s ease;
        }

 .btn-eliminar:hover {
            transform: scale(1.05);
            box-shadow: 0 3px 8px rgba(255, 71, 87, 0.3);
        }

  .total {
            text-align: center;
            font-size: 1.3rem;
            font-weight: bold;
            color: #667eea;
            padding: 15px;
            background: linear-gradient(135deg, #f8f9ff, #e8f2ff);
            border-radius: 12px;
            border: 2px solid #667eea;
            margin: 15px 0;
        }

 .empty-state {
            text-align: center;
            padding: 30px;
            color: #999;
            font-size: 1rem;
        }

 .empty-state::before {
            content: "🛒";
            font-size: 2.5rem;
            display: block;
            margin-bottom: 10px;
        }

 .categorias-container {
            margin-bottom: 25px;
            position: relative;
            z-index: 10;
        }

 .categorias-container h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.2rem;
            text-align: center;
        }

  .categorias-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
            margin-bottom: 15px;
        }

 .categoria-item {
            position: relative;
            background: linear-gradient(135deg, #f8f9ff, #e8f2ff);
            border: 2px solid #667eea;
            border-radius: 12px;
            padding: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            font-weight: 600;
            color: #667eea;
            font-size: 0.95rem;
        }

 .categoria-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

 .categoria-item::before {
            content: attr(data-emoji);
            font-size: 1.3rem;
            display: block;
            margin-bottom: 5px;
        }

 .categoria-item.active {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

 .subcategorias-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
            margin: 15px 0;
            display: none;
        }

 .subcategoria-item {
            background: linear-gradient(135deg, #fff9c4, #ffecb3);
            border: 2px solid #ffd54f;
            border-radius: 12px;
            padding: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            font-weight: 600;
            color: #333;
            font-size: 0.95rem;
        }

 .subcategoria-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 3px 10px rgba(255, 213, 79, 0.3);
            background: linear-gradient(135deg, #ffecb3, #ffe082);
        }

 .subcategoria-item::before {
            content: attr(data-emoji);
            font-size: 1.3rem;
            display: block;
            margin-bottom: 5px;
        }

  .subcategoria-item.active {
            background: linear-gradient(135deg, #ffd54f, #ffb300);
            color: #333;
            border-color: #ffa000;
        }

 .productos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 12px;
            margin: 15px 0;
            display: none;
        }

 .producto-item {
            background: linear-gradient(135deg, #e8f5e9, #c8e6c9);
            border: 2px solid #81c784;
            border-radius: 12px;
            padding: 12px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

 .producto-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 3px 10px rgba(76, 175, 80, 0.3);
            border-color: #4caf50;
            background: linear-gradient(135deg, #c8e6c9, #a5d6a7);
        }

 .producto-nombre {
            font-weight: 600;
            color: #333;
            margin-bottom: 5px;
            font-size: 0.95rem;
        }

 .producto-precio {
            font-weight: bold;
            color: #25d366;
            font-size: 1rem;
        }

 .producto-unidad {
            color: #666;
            font-size: 0.85rem;
        }

 .btn-agregar {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            text-align: center;
            padding: 8px;
            font-size: 13px;
            border-radius: 0 0 10px 10px;
            transform: translateY(100%);
            transition: all 0.3s ease;
            opacity: 0;
            cursor: pointer;
        }

 .producto-item:hover .btn-agregar {
            transform: translateY(0);
            opacity: 1;
        }

 .producto-section-title {
            text-align: center;
            margin: 15px 0 8px;
            color: #667eea;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            font-size: 1.1rem;
        }

  .producto-section-title::before, 
        .producto-section-title::after {
            content: "";
            flex: 1;
            height: 2px;
            background: linear-gradient(to right, transparent, #667eea, transparent);
        }
        
        /* Notificaciones */
  .notification {
            position: fixed;
            top: 15px;
            right: 15px;
            left: 15px;
            background: #4CAF50;
            color: white;
            padding: 12px 15px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.2);
            z-index: 2000;
            animation: slideInRight 0.5s ease-out;
            text-align: center;
        }

  @keyframes slideInRight {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        /* ÍCONO FLOTANTE DEL CARRITO */
  .cart-icon {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            cursor: pointer;
            transition: all 0.3s ease;
        }

 .cart-icon:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
        }

 .cart-icon i {
            font-size: 24px;
            color: white;
        }

 .cart-count {
            position: absolute;
            top: -5px;
            right: -5px;
            background: #ff6b6b;
            color: white;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 13px;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
        }

        /* CARRO FLOTANTE */
 .floating-cart {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: white;
            z-index: 2000;
            overflow: hidden;
            transition: all 0.4s ease;
            transform: translateY(100%);
            opacity: 0;
            visibility: hidden;
            display: flex;
            flex-direction: column;
            border-radius: 20px 20px 0 0;
        }

 .floating-cart.open {
            transform: translateY(0);
            opacity: 1;
            visibility: visible;
        }

 .cart-header {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

 .cart-title {
            font-size: 1.2rem;
            font-weight: 600;
        }

 .close-cart {
            background: none;
            border: none;
            color: white;
            font-size: 1.3rem;
            cursor: pointer;
            transition: all 0.3s;
            padding: 5px 10px;
        }

 .close-cart:hover {
            transform: rotate(90deg);
        }

  .cart-content {
            flex: 1;
            overflow-y: auto;
            padding: 15px;
            background: #f9f9ff;
        }

 .cart-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px solid #eee;
        }

 .cart-item:last-child {
            border-bottom: none;
        }

 .cart-item-name {
            font-weight: 500;
            flex: 2;
            font-size: 0.95rem;
        }

 .cart-item-details {
            color: #666;
            font-size: 0.85rem;
            flex: 1;
            text-align: right;
        }

 .cart-total {
            background: linear-gradient(135deg, #f8f9ff, #e8f2ff);
            padding: 15px;
            text-align: center;
            font-weight: bold;
            font-size: 1.2rem;
            color: #667eea;
            border-top: 2px solid #667eea;
        }

 .cart-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            padding: 15px;
            background: #f5f7ff;
        }

  .cart-actions .btn {
            flex: 1;
            min-width: 120px;
            padding: 14px;
            font-size: 14px;
        }

 .cart-actions .btn i {
            margin-right: 5px;
        }
        
        /* Mejoras para móviles */
  @media (min-width: 768px) {
            .container {
                padding: 25px;
            }
            
  .input-section {
                flex-direction: row;
                flex-wrap: wrap;
            }
            
  .input-group {
                flex: 1;
                min-width: 120px;
            }
            
  .btn {
                width: auto;
                margin-top: 0;
            }
            
  .floating-cart {
                top: auto;
                left: auto;
                right: 30px;
                bottom: 120px;
                width: 350px;
                height: auto;
                max-height: 500px;
                border-radius: 20px;
            }
            
 .notification {
                left: auto;
                width: auto;
                max-width: 350px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🛒 Lista de Mercado - Perú</h1>
        
        <!-- Categorías de productos -->
 <div class="categorias-container">
            <h3>📋 Categorías de Productos</h3>
            <div class="categorias-grid" id="categoriasGrid">
                <!-- Las categorías se generarán dinámicamente -->
            </div>
            
 <div class="subcategorias-grid" id="subcategoriasGrid">
                <!-- Subcategorías se generarán dinámicamente -->
            </div>
            
 <div class="productos-grid" id="productosGrid">
                <!-- Productos se generarán dinámicamente -->
            </div>
            
 <button class="btn btn-back" id="btnBack" style="display: none;" onclick="volverACategorias()">← Volver a Categorías</button>
        </div>

 <div class="input-section">
            <div class="input-group">
                <input type="text" id="producto" placeholder="Nombre del producto" />
            </div>
            <div class="input-group">
                <input type="number" id="cantidad" placeholder="Cantidad" min="1" value="1" />
            </div>
            <div class="input-group">
                <select id="unidad">
                    <option value="unidad">Unidad</option>
                    <option value="kg">Kilogramo</option>
                    <option value="lb">Libra</option>
                    <option value="g">Gramo</option>
                    <option value="L">Litro</option>
                    <option value="ml">Mililitro</option>
                    <option value="paquete">Paquete</option>
                    <option value="caja">Caja</option>
                </select>
            </div>
            <div class="input-group">
                <input type="number" id="precio" placeholder="Precio (opcional)" min="0" step="0.01" />
            </div>
            <button class="btn" onclick="agregarProducto()">Agregar</button>
        </div>

        <!-- Mensaje cuando la lista está vacía -->
 <div class="empty-state" id="emptyState">
            Tu lista está vacía. ¡Agrega algunos productos!
        </div>
    </div>

    <!-- Ícono flotante del carrito -->
 <div class="cart-icon" id="cartIcon">
        <i class="fas fa-shopping-cart"></i>
        <div class="cart-count" id="cartCount">0</div>
    </div>

    <!-- Carrito flotante -->
 <div class="floating-cart" id="floatingCart">
        <div class="cart-header">
            <div class="cart-title">Tu Carrito de Compras</div>
            <button class="close-cart" onclick="toggleCart()">
                <i class="fas fa-times"></i>
            </button>
        </div>
        <div class="cart-content" id="cartContent">
            <!-- Los productos se mostrarán aquí -->
        </div>
        <div class="cart-total" id="cartTotal">
            Total estimado: S/0.00
        </div>
        <div class="cart-actions">
            <button class="btn btn-capture" onclick="capturarLista()"><i class="fas fa-camera"></i> Capturar</button>
            <button class="btn btn-whatsapp" onclick="enviarWhatsApp()"><i class="fab fa-whatsapp"></i> WhatsApp</button>
            <button class="btn" onclick="limpiarLista()"><i class="fas fa-trash"></i> Limpiar</button>
        </div>
    </div>

 <script>
        let listaProductos = [];
        let totalMonto = 0;
        let categoriaActual = null;
        let subcategoriaActual = null;
        let cartOpen = false;

        // Base de datos de productos por categorías (precios en Soles Peruanos)
        const productosDB = {
            frutas: {
                emoji: '🍎',
                nombre: 'Frutas',
                subcategorias: {
                    manzanas: {
                        emoji: '🍏',
                        nombre: 'Manzanas',
                        productos: [
                            { nombre: 'Manzana Roja', precio: 5.50, unidad: 'kg' },
                            { nombre: 'Manzana Verde', precio: 6.00, unidad: 'kg' },
                            { nombre: 'Manzana Amarilla', precio: 5.80, unidad: 'kg' },
                            { nombre: 'Manzana Gala', precio: 6.50, unidad: 'kg' },
                            { nombre: 'Manzana Fuji', precio: 7.00, unidad: 'kg' }
                        ]
                    },
                    platanos: {
                        emoji: '🍌',
                        nombre: 'Plátanos',
                        productos: [
                            { nombre: 'Plátano Común', precio: 3.00, unidad: 'kg' },
                            { nombre: 'Plátano Maduro', precio: 2.80, unidad: 'kg' },
                            { nombre: 'Plátano Verde', precio: 3.20, unidad: 'kg' },
                            { nombre: 'Plátano Dominico', precio: 4.00, unidad: 'kg' }
                        ]
                    },
                    naranjas: {
                        emoji: '🍊',
                        nombre: 'Naranjas',
                        productos: [
                            { nombre: 'Naranja Común', precio: 3.50, unidad: 'kg' },
                            { nombre: 'Naranja Valencia', precio: 4.20, unidad: 'kg' },
                            { nombre: 'Naranja Navel', precio: 5.00, unidad: 'kg' },
                            { nombre: 'Mandarina', precio: 4.80, unidad: 'kg' }
                        ]
                    },
                    citricos: {
                        emoji: '🍋',
                        nombre: 'Otros Cítricos',
                        productos: [
                            { nombre: 'Limón', precio: 7.00, unidad: 'kg' },
                            { nombre: 'Lima', precio: 8.00, unidad: 'kg' },
                            { nombre: 'Toronja', precio: 4.20, unidad: 'kg' },
                            { nombre: 'Pomelo', precio: 6.00, unidad: 'kg' }
                        ]
                    }
                }
            },
            verduras: {
                emoji: '🥕',
                nombre: 'Verduras',
                subcategorias: {
                    hojas: {
                        emoji: '🥬',
                        nombre: 'Hojas Verdes',
                        productos: [
                            { nombre: 'Lechuga', precio: 3.00, unidad: 'unidad' },
                            { nombre: 'Espinaca', precio: 5.00, unidad: 'kg' },
                            { nombre: 'Acelga', precio: 4.20, unidad: 'kg' },
                            { nombre: 'Rúcula', precio: 6.50, unidad: 'kg' },
                            { nombre: 'Apio', precio: 5.80, unidad: 'kg' }
                        ]
                    },
                    tuberculos: {
                        emoji: '🥔',
                        nombre: 'Tubérculos',
                        productos: [
                            { nombre: 'Papa Común', precio: 3.50, unidad: 'kg' },
                            { nombre: 'Papa Amarilla', precio: 4.20, unidad: 'kg' },
                            { nombre: 'Camote', precio: 5.00, unidad: 'kg' },
                            { nombre: 'Yuca', precio: 4.00, unidad: 'kg' },
                            { nombre: 'Zanahoria', precio: 4.80, unidad: 'kg' }
                        ]
                    },
                    tomates: {
                        emoji: '🍅',
                        nombre: 'Tomates',
                        productos: [
                            { nombre: 'Tomate Común', precio: 6.00, unidad: 'kg' },
                            { nombre: 'Tomate Cherry', precio: 10.00, unidad: 'kg' },
                            { nombre: 'Tomate de Árbol', precio: 8.50, unidad: 'kg' },
                            { nombre: 'Tomate Riñón', precio: 7.50, unidad: 'kg' }
                        ]
                    },
                    cebollas: {
                        emoji: '🧅',
                        nombre: 'Cebollas',
                        productos: [
                            { nombre: 'Cebolla Blanca', precio: 4.00, unidad: 'kg' },
                            { nombre: 'Cebolla Morada', precio: 5.00, unidad: 'kg' },
                            { nombre: 'Cebolla Larga', precio: 5.80, unidad: 'kg' },
                            { nombre: 'Cebollín', precio: 2.00, unidad: 'paquete' }
                        ]
                    }
                }
            },
            carnes: {
                emoji: '🥩',
                nombre: 'Carnes',
                subcategorias: {
                    res: {
                        emoji: '🐄',
                        nombre: 'Carne de Res',
                        productos: [
                            { nombre: 'Lomo Fino', precio: 28.50, unidad: 'kg' },
                            { nombre: 'Chuleta', precio: 24.00, unidad: 'kg' },
                            { nombre: 'Bistec', precio: 23.00, unidad: 'kg' },
                            { nombre: 'Carne Molida', precio: 20.00, unidad: 'kg' },
                            { nombre: 'Costilla', precio: 18.00, unidad: 'kg' }
                        ]
                    },
                    pollo: {
                        emoji: '🐔',
                        nombre: 'Pollo',
                        productos: [
                            { nombre: 'Pollo Entero', precio: 12.50, unidad: 'kg' },
                            { nombre: 'Pechuga', precio: 16.00, unidad: 'kg' },
                            { nombre: 'Muslo', precio: 11.00, unidad: 'kg' },
                            { nombre: 'Alas', precio: 10.00, unidad: 'kg' },
                            { nombre: 'Pollo Desmenuzado', precio: 18.00, unidad: 'kg' }
                        ]
                    },
                    cerdo: {
                        emoji: '🐖',
                        nombre: 'Carne de Cerdo',
                        productos: [
                            { nombre: 'Lomo de Cerdo', precio: 20.00, unidad: 'kg' },
                            { nombre: 'Chuleta de Cerdo', precio: 19.00, unidad: 'kg' },
                            { nombre: 'Tocino', precio: 16.00, unidad: 'kg' },
                            { nombre: 'Jamón', precio: 25.00, unidad: 'kg' }
                        ]
                    },
                    pescado: {
                        emoji: '🐟',
                        nombre: 'Pescados',
                        productos: [
                            { nombre: 'Tilapia', precio: 15.00, unidad: 'kg' },
                            { nombre: 'Trucha', precio: 22.00, unidad: 'kg' },
                            { nombre: 'Atún', precio: 26.00, unidad: 'kg' },
                            { nombre: 'Salmón', precio: 40.00, unidad: 'kg' }
                        ]
                    }
                }
            },
            lacteos: {
                emoji: '🥛',
                nombre: 'Lácteos',
                subcategorias: {
                    leche: {
                        emoji: '🥛',
                        nombre: 'Leche',
                        productos: [
                            { nombre: 'Leche Entera', precio: 4.20, unidad: 'L' },
                            { nombre: 'Leche Descremada', precio: 4.50, unidad: 'L' },
                            { nombre: 'Leche Deslactosada', precio: 5.00, unidad: 'L' },
                            { nombre: 'Leche de Almendra', precio: 9.00, unidad: 'L' }
                        ]
                    },
                    quesos: {
                        emoji: '🧀',
                        nombre: 'Quesos',
                        productos: [
                            { nombre: 'Queso Fresco', precio: 12.00, unidad: 'kg' },
                            { nombre: 'Queso Mozzarella', precio: 15.00, unidad: 'kg' },
                            { nombre: 'Queso Cheddar', precio: 16.50, unidad: 'kg' },
                            { nombre: 'Queso Manchego', precio: 22.00, unidad: 'kg' }
                        ]
                    },
                    yogurt: {
                        emoji: '🍶',
                        nombre: 'Yogurt',
                        productos: [
                            { nombre: 'Yogurt Natural', precio: 8.00, unidad: 'kg' },
                            { nombre: 'Yogurt con Frutas', precio: 9.50, unidad: 'kg' },
                            { nombre: 'Yogurt Griego', precio: 12.50, unidad: 'kg' },
                            { nombre: 'Yogurt Descremado', precio: 8.80, unidad: 'kg' }
                        ]
                    }
                }
            },
            granos: {
                emoji: '🌾',
                nombre: 'Granos y Cereales',
                subcategorias: {
                    arroz: {
                        emoji: '🍚',
                        nombre: 'Arroz',
                        productos: [
                            { nombre: 'Arroz Blanco', precio: 4.00, unidad: 'kg' },
                            { nombre: 'Arroz Integral', precio: 5.80, unidad: 'kg' },
                            { nombre: 'Arroz Basmati', precio: 8.00, unidad: 'kg' },
                            { nombre: 'Arroz de Coco', precio: 6.50, unidad: 'kg' }
                        ]
                    },
                    frijoles: {
                        emoji: '🫘',
                        nombre: 'Frijoles',
                        productos: [
                            { nombre: 'Frijol Negro', precio: 5.00, unidad: 'kg' },
                            { nombre: 'Frijol Rojo', precio: 5.20, unidad: 'kg' },
                            { nombre: 'Frijol Blanco', precio: 5.50, unidad: 'kg' },
                            { nombre: 'Lenteja', precio: 6.50, unidad: 'kg' }
                        ]
                    },
                    pasta: {
                        emoji: '🍝',
                        nombre: 'Pasta',
                        productos: [
                            { nombre: 'Espaguetti', precio: 5.00, unidad: 'paquete' },
                            { nombre: 'Macarrones', precio: 5.20, unidad: 'paquete' },
                            { nombre: 'Penne', precio: 5.80, unidad: 'paquete' },
                            { nombre: 'Lasaña', precio: 7.20, unidad: 'paquete' }
                        ]
                    }
                }
            },
            bebidas: {
                emoji: '🥤',
                nombre: 'Bebidas',
                subcategorias: {
                    gaseosas: {
                        emoji: '🥤',
                        nombre: 'Gaseosas',
                        productos: [
                            { nombre: 'Coca Cola', precio: 8.00, unidad: 'L' },
                            { nombre: 'Pepsi', precio: 7.50, unidad: 'L' },
                            { nombre: 'Sprite', precio: 7.80, unidad: 'L' },
                            { nombre: 'Fanta', precio: 7.80, unidad: 'L' }
                        ]
                    },
                    jugos: {
                        emoji: '🧃',
                        nombre: 'Jugos',
                        productos: [
                            { nombre: 'Jugo de Naranja', precio: 10.00, unidad: 'L' },
                            { nombre: 'Jugo de Manzana', precio: 10.50, unidad: 'L' },
                            { nombre: 'Jugo de Uva', precio: 11.50, unidad: 'L' },
                            { nombre: 'Jugo Multivitamínico', precio: 13.00, unidad: 'L' }
                        ]
                    },
                    agua: {
                        emoji: '💧',
                        nombre: 'Agua',
                        productos: [
                            { nombre: 'Agua Mineral', precio: 3.50, unidad: 'L' },
                            { nombre: 'Agua con Gas', precio: 5.00, unidad: 'L' },
                            { nombre: 'Agua Saborizada', precio: 6.00, unidad: 'L' }
                        ]
                    }
                }
            }
        };

        // Inicializar la aplicación
        document.addEventListener('DOMContentLoaded', function() {
            generarCategorias();
            document.getElementById('producto').focus();
        });

        function generarCategorias() {
            const container = document.getElementById('categoriasGrid');
            let html = '';

            Object.keys(productosDB).forEach(categoriaKey => {
                const categoria = productosDB[categoriaKey];
                html += `
                    <div class="categoria-item" data-emoji="${categoria.emoji}" 
                         data-categoria="${categoriaKey}" onclick="mostrarSubcategorias('${categoriaKey}')">
                        ${categoria.nombre}
                    </div>
                `;
            });

            container.innerHTML = html;
        }

        function mostrarSubcategorias(categoriaKey) {
            // Ocultar todas las categorías
            document.querySelectorAll('.categoria-item').forEach(el => {
                el.classList.remove('active');
            });
            
            // Marcar la categoría actual como activa
            document.querySelector(`.categoria-item[data-categoria="${categoriaKey}"]`).classList.add('active');
            
            // Ocultar productos si están visibles
            document.getElementById('productosGrid').style.display = 'none';
            
            // Mostrar subcategorías
            const categoria = productosDB[categoriaKey];
            const subcategoriasGrid = document.getElementById('subcategoriasGrid');
            let html = '';
            
            Object.keys(categoria.subcategorias).forEach(subcategoriaKey => {
                const subcategoria = categoria.subcategorias[subcategoriaKey];
                html += `
                    <div class="subcategoria-item" data-emoji="${subcategoria.emoji}" 
                         data-subcategoria="${subcategoriaKey}" 
                         onclick="mostrarProductos('${categoriaKey}', '${subcategoriaKey}')">
                        ${subcategoria.nombre}
                    </div>
                `;
            });
            
            subcategoriasGrid.innerHTML = html;
            subcategoriasGrid.style.display = 'grid';
            
            // Mostrar botón de volver
            document.getElementById('btnBack').style.display = 'block';
            
            // Guardar categoría actual
            categoriaActual = categoriaKey;
            subcategoriaActual = null;
        }

        function mostrarProductos(categoriaKey, subcategoriaKey) {
            // Ocultar todas las subcategorías
            document.querySelectorAll('.subcategoria-item').forEach(el => {
                el.classList.remove('active');
            });
            
            // Marcar la subcategoría actual como activa
            document.querySelector(`.subcategoria-item[data-subcategoria="${subcategoriaKey}"]`).classList.add('active');
            
            // Mostrar productos
            const subcategoria = productosDB[categoriaKey].subcategorias[subcategoriaKey];
            const productosGrid = document.getElementById('productosGrid');
            let html = '';
            
            subcategoria.productos.forEach(producto => {
                html += `
                    <div class="producto-item">
                        <div class="producto-nombre">${producto.nombre}</div>
                        <div class="producto-precio">S/${producto.precio.toFixed(2)}</div>
                        <div class="producto-unidad">por ${producto.unidad}</div>
                        <div class="btn-agregar" onclick="agregarProductoDirectamente('${producto.nombre}', ${producto.precio}, '${producto.unidad}')">Agregar a lista</div>
                    </div>
                `;
            });
            
            productosGrid.innerHTML = html;
            productosGrid.style.display = 'grid';
            
            // Guardar subcategoría actual
            subcategoriaActual = subcategoriaKey;
        }

        function volverACategorias() {
            // Ocultar subcategorías y productos
            document.getElementById('subcategoriasGrid').style.display = 'none';
            document.getElementById('productosGrid').style.display = 'none';
            
            // Ocultar botón de volver
            document.getElementById('btnBack').style.display = 'none';
            
            // Desmarcar categorías activas
            document.querySelectorAll('.categoria-item').forEach(el => {
                el.classList.remove('active');
            });
            
            document.querySelectorAll('.subcategoria-item').forEach(el => {
                el.classList.remove('active');
            });
            
            categoriaActual = null;
            subcategoriaActual = null;
        }

        // Función para agregar productos directamente desde la base de datos
        function agregarProductoDirectamente(nombre, precio, unidad) {
            const nuevoProducto = {
                id: Date.now(),
                nombre: nombre,
                cantidad: 1,
                unidad: unidad,
                precio: precio
            };

            listaProductos.push(nuevoProducto);
            actualizarLista();
            mostrarNotificacion(`${nombre} agregado a la lista`);
        }

        function agregarProducto() {
            const producto = document.getElementById('producto').value.trim();
            const cantidad = parseInt(document.getElementById('cantidad').value);
            const unidad = document.getElementById('unidad').value;
            const precio = parseFloat(document.getElementById('precio').value) || 0;

            if (!producto) {
                mostrarNotificacion('Por favor, ingresa el nombre del producto');
                return;
            }

            const nuevoProducto = {
                id: Date.now(),
                nombre: producto,
                cantidad: cantidad,
                unidad: unidad,
                precio: precio
            };

            listaProductos.push(nuevoProducto);
            actualizarLista();
            limpiarFormulario();
            mostrarNotificacion('Producto agregado correctamente');
        }

        function eliminarProducto(id) {
            listaProductos = listaProductos.filter(p => p.id !== id);
            actualizarLista();
            mostrarNotificacion('Producto eliminado');
        }

        function actualizarLista() {
            const emptyState = document.getElementById('emptyState');
            const cartContent = document.getElementById('cartContent');
            const cartTotal = document.getElementById('cartTotal');
            const cartCount = document.getElementById('cartCount');

            if (listaProductos.length === 0) {
                emptyState.style.display = 'block';
                cartContent.innerHTML = '<div class="empty-state">Tu lista está vacía. ¡Agrega algunos productos!</div>';
                cartTotal.textContent = 'Total estimado: S/0.00';
                cartCount.textContent = '0';
                return;
            }

            emptyState.style.display = 'none';
            
            let total = 0;
            let html = '';

            listaProductos.forEach(producto => {
                const subtotal = producto.precio * producto.cantidad;
                total += subtotal;

                html += `
                    <div class="cart-item">
                        <div class="cart-item-name">${producto.nombre}</div>
                        <div class="cart-item-details">
                            ${producto.cantidad} ${producto.unidad}${producto.cantidad > 1 && producto.unidad === 'unidad' ? 'es' : ''}
                            <br>
                            ${producto.precio > 0 ? `S/${subtotal.toFixed(2)}` : ''}
                        </div>
                    </div>
                `;
            });

            cartContent.innerHTML = html;
            cartTotal.textContent = `Total estimado: S/${total.toFixed(2)}`;
            cartCount.textContent = listaProductos.length;
        }

        function limpiarFormulario() {
            document.getElementById('producto').value = '';
            document.getElementById('cantidad').value = '1';
            document.getElementById('unidad').value = 'unidad';
            document.getElementById('precio').value = '';
            document.getElementById('producto').focus();
        }

        function limpiarLista() {
            if (listaProductos.length > 0 && confirm('¿Estás seguro de que quieres limpiar toda la lista?')) {
                listaProductos = [];
                actualizarLista();
                mostrarNotificacion('Lista limpiada');
            }
        }

        function generarTextoLista() {
            if (listaProductos.length === 0) {
                return 'Lista vacía';
            }

            let texto = '🛒 *LISTA DE MERCADO*\n\n';
            let total = 0;

            listaProductos.forEach((producto, index) => {
                const subtotal = producto.precio * producto.cantidad;
                total += subtotal;
                
                texto += `${index + 1}. *${producto.nombre}*\n`;
                texto += `   Cantidad: ${producto.cantidad} ${producto.unidad}${producto.cantidad > 1 && producto.unidad === 'unidad' ? 'es' : ''}\n`;
                
                if (producto.precio > 0) {
                    texto += `   Precio: S/${subtotal.toFixed(2)}\n`;
                }
                texto += '\n';
            });

            if (total > 0) {
                texto += `💰 *TOTAL ESTIMADO: S/${total.toFixed(2)}*\n\n`;
            }

            texto += '📱 Lista generada desde Lista de Mercado App';
            return texto;
        }

        function enviarWhatsApp() {
            if (listaProductos.length === 0) {
                mostrarNotificacion('Tu lista está vacía. Agrega algunos productos antes de enviar.');
                return;
            }

            const numeroWhatsApp = '975842622';
            const mensaje = generarTextoLista();
            const url = `https://wa.me/${numeroWhatsApp}?text=${encodeURIComponent(mensaje)}`;
            
            window.open(url, '_blank');
        }

        function capturarLista() {
            if (listaProductos.length === 0) {
                mostrarNotificacion('Tu lista está vacía. Agrega algunos productos antes de capturar.');
                return;
            }

            // Crear un canvas para capturar la lista
            const canvas = document.createElement('canvas');
            const ctx = canvas.getContext('2d');
            
            // Configurar el canvas
            canvas.width = 600;
            canvas.height = Math.max(400, listaProductos.length * 80 + 150);
            
            // Fondo blanco
            ctx.fillStyle = '#ffffff';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Título
            ctx.fillStyle = '#667eea';
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('🛒 LISTA DE MERCADO - PERÚ', canvas.width / 2, 40);
            
            // Línea separadora
            ctx.strokeStyle = '#667eea';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(50, 60);
            ctx.lineTo(canvas.width - 50, 60);
            ctx.stroke();
            
            // Productos
            let y = 100;
            let total = 0;
            
            listaProductos.forEach((producto, index) => {
                const subtotal = producto.precio * producto.cantidad;
                total += subtotal;
                
                // Número del producto
                ctx.fillStyle = '#333';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'left';
                ctx.fillText(`${index + 1}.`, 50, y);
                
                // Nombre del producto
                ctx.fillStyle = '#333';
                ctx.font = 'bold 18px Arial';
                ctx.fillText(producto.nombre, 80, y);
                
                // Cantidad y unidad
                ctx.fillStyle = '#666';
                ctx.font = '14px Arial';
                ctx.fillText(`${producto.cantidad} ${producto.unidad}${producto.cantidad > 1 && producto.unidad === 'unidad' ? 'es' : ''}`, 80, y + 20);
                
                // Precio
                if (producto.precio > 0) {
                    ctx.fillStyle = '#667eea';
                    ctx.font = 'bold 16px Arial';
                    ctx.textAlign = 'right';
                    ctx.fillText(`S/${subtotal.toFixed(2)}`, canvas.width - 50, y);
                }
                
                y += 50;
            });
            
            // Total
            if (total > 0) {
                y += 20;
                ctx.strokeStyle = '#667eea';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(50, y);
                ctx.lineTo(canvas.width - 50, y);
                ctx.stroke();
                
                ctx.fillStyle = '#667eea';
                ctx.font = 'bold 20px Arial';
                ctx.textAlign = 'right';
                ctx.fillText(`TOTAL: S/${total.toFixed(2)}`, canvas.width - 50, y + 30);
            }
            
            // Descargar la imagen
            canvas.toBlob(function(blob) {
                const url = URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = 'lista_mercado.png';
                a.click();
                URL.revokeObjectURL(url);
                mostrarNotificacion('Lista capturada y descargada');
            });
        }

        function mostrarNotificacion(mensaje) {
            const notification = document.createElement('div');
            notification.className = 'notification';
            notification.textContent = mensaje;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }

        function toggleCart() {
            const cart = document.getElementById('floatingCart');
            cartOpen = !cartOpen;
            
            if (cartOpen) {
                cart.classList.add('open');
            } else {
                cart.classList.remove('open');
            }
        }

        // Permitir agregar productos con Enter
        document.getElementById('producto').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                agregarProducto();
            }
        });

        document.getElementById('cantidad').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                agregarProducto();
            }
        });

        document.getElementById('precio').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                agregarProducto();
            }
        });

        // Asignar evento al ícono del carrito
        document.getElementById('cartIcon').addEventListener('click', toggleCart);

        // Enfocar el campo de producto al cargar
        document.getElementById('producto').focus();
    </script>
</body>
</html>
