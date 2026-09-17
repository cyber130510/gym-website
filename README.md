<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fitness War Gym Lalbagh | Forge Your Legacy</title>
    <!-- Google Fonts for Roman/Epic Vibe -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;800&family=Plus+Jakarta+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-deep: #0a0505;
            --bg-card: #140a0a;
            --primary-red: #cc0000;
            --accent-red: #ff1a1a;
            --text-light: #f4f4f4;
            --text-muted: #a0a0a0;
            --border-glow: rgba(204, 0, 0, 0.4);
            --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-deep);
            color: var(--text-light);
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
        }

        h1, h2, h3, .roman-font {
            font-family: 'Cinzel', serif;
            letter-spacing: 1px;
        }

        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: var(--bg-deep);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--primary-red);
            border-radius: 4px;
        }

        /* Liquid Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            background: rgba(10, 5, 5, 0.85);
            backdrop-filter: blur(12px);
            z-index: 1000;
            border-bottom: 1px solid rgba(204, 0, 0, 0.2);
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--text-light);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--primary-red);
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 35px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-muted);
            font-weight: 600;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--accent-red);
            text-shadow: 0 0 10px var(--primary-red);
        }

        .cta-btn {
            background: linear-gradient(135deg, var(--primary-red), #880000);
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            box-shadow: 0 4px 15px rgba(204, 0, 0, 0.4);
            transition: var(--transition);
            border: 1px solid rgba(255, 26, 26, 0.4);
            cursor: pointer;
            display: inline-block;
        }

        .cta-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 26, 26, 0.7);
            background: linear-gradient(135deg, var(--accent-red), var(--primary-red));
        }

        .secondary-btn {
            background: transparent;
            color: var(--text-light);
            border: 1px solid var(--primary-red);
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .secondary-btn:hover {
            background: rgba(204, 0, 0, 0.2);
            box-shadow: 0 0 15px rgba(204, 0, 0, 0.4);
        }

        /* Hero Section */
        header.hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: radial-gradient(circle at center, #200808 0%, var(--bg-deep) 70%);
            text-align: center;
            padding: 0 20px;
        }

        .hero-content {
            max-width: 800px;
            z-index: 2;
        }

        .hero h1 {
            font-size: clamp(2.3rem, 5vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .hero h1 span {
            color: var(--primary-red);
            text-shadow: 0 0 25px rgba(204, 0, 0, 0.6);
        }

        .hero p {
            color: var(--text-muted);
            font-size: 1.1rem;
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .glow-orb {
            position: absolute;
            width: 400px;
            height: 400px;
            background: rgba(204, 0, 0, 0.15);
            filter: blur(120px);
            border-radius: 50%;
            z-index: 1;
            animation: floatOrb 8s infinite alternate ease-in-out;
        }

        @keyframes floatOrb {
            0% { transform: translate(-50px, -50px) scale(1); }
            100% { transform: translate(50px, 50px) scale(1.2); }
        }

        /* Sections */
        section {
            padding: 100px 8%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--text-light);
        }

        .section-title h2 span {
            color: var(--primary-red);
        }

        .section-title p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .admin-controls-header {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid rgba(204, 0, 0, 0.2);
            padding: 40px 30px;
            border-radius: 12px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .card i {
            font-size: 2.5rem;
            color: var(--primary-red);
            margin-bottom: 20px;
        }

        .card h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            line-height: 1.6;
        }

        /* Admin Panels */
        .admin-panel {
            background: linear-gradient(135deg, #140a0a, #0f0707);
            border: 1px solid rgba(204, 0, 0, 0.3);
            border-radius: 16px;
            padding: 40px;
            max-width: 700px;
            margin: 0 auto;
            backdrop-filter: blur(10px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.6);
            display: none;
        }

        .admin-panel.active {
            display: block;
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--text-light);
            font-weight: 600;
            font-size: 0.9rem;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            background: rgba(20, 10, 10, 0.8);
            border: 1px solid rgba(204, 0, 0, 0.3);
            border-radius: 8px;
            color: var(--text-light);
            font-family: 'Plus Jakarta Sans', sans-serif;
            outline: none;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--accent-red);
            box-shadow: 0 0 10px rgba(204, 0, 0, 0.4);
        }

        /* Products Display Grid */
        .products-display-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .product-item-card {
            background: var(--bg-card);
            border: 1px solid rgba(204, 0, 0, 0.3);
            border-radius: 10px;
            overflow: hidden;
            text-align: left;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .product-item-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-red);
            box-shadow: 0 10px 25px rgba(204,0,0,0.3);
        }

        .product-item-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .product-info {
            padding: 15px;
        }

        .product-info h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .product-info p {
            color: var(--primary-red);
            font-weight: 700;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .order-now-btn {
            display: block;
            width: calc(100% - 30px);
            margin: 0 15px 15px 15px;
            background: #25d366;
            color: white;
            text-align: center;
            padding: 10px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }

        .order-now-btn:hover {
            background: #1ebe5d;
            box-shadow: 0 0 10px rgba(37, 211, 102, 0.5);
        }

        /* Modal Overlay for Checkout Form & Orders */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.85);
            backdrop-filter: blur(8px);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            padding: 20px;
        }

        .modal-box {
            background: var(--bg-card);
            border: 1px solid var(--primary-red);
            border-radius: 12px;
            padding: 30px;
            max-width: 500px;
            width: 100%;
            text-align: left;
            position: relative;
            box-shadow: 0 10px 30px rgba(204,0,0,0.5);
            max-height: 90vh;
            overflow-y: auto;
        }

        .modal-box h3 {
            color: var(--text-light);
            margin-bottom: 15px;
            font-size: 1.4rem;
            text-align: center;
        }

        .modal-box p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 15px;
            line-height: 1.5;
        }

        .bkash-box {
            background: rgba(204, 0, 0, 0.1);
            border: 1px dashed var(--primary-red);
            padding: 12px;
            border-radius: 8px;
            font-weight: 700;
            color: #ff4d4d;
            font-size: 1rem;
            margin-bottom: 15px;
            text-align: center;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.3rem;
            cursor: pointer;
        }

        .close-modal:hover {
            color: var(--text-light);
        }

        /* Order Table for Admin View */
        .order-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            font-size: 0.85rem;
        }

        .order-table th, .order-table td {
            border: 1px solid rgba(204,0,0,0.2);
            padding: 10px;
            text-align: left;
        }

        .order-table th {
            background: rgba(204,0,0,0.2);
            color: var(--text-light);
        }

        .order-table td {
            color: var(--text-muted);
        }

        /* Footer */
        footer {
            background: #050202;
            padding: 30px 8%;
            text-align: center;
            border-top: 1px solid rgba(204, 0, 0, 0.2);
            color: var(--text-muted);
            font-size: 0.9rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        footer span {
            color: var(--primary-red);
        }

        .developer-credit {
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        .developer-credit span {
            color: var(--text-light);
            font-weight: 600;
        }

        @media(max-width: 768px) {
            .nav-links {
                display: none;
            }
            footer {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation Bar -->
    <nav>
        <a href="#" class="logo">
            <i class="fa-solid fa-fire-flame-curved" style="color: var(--primary-red);"></i> FITNESS WAR <span>LALBAGH</span>
        </a>
        <ul class="nav-links">
            <li><a href="#hero">Home</a></li>
            <li><a href="#programs">Programs</a></li>
            <li><a href="#shop">Store</a></li>
        </ul>
        <a href="#shop" class="cta-btn">Admin Portal</a>
    </nav>

    <!-- Hero Section -->
    <header class="hero" id="hero">
        <div class="glow-orb" style="top: 20%; left: 30%;"></div>
        <div class="hero-content">
            <h5 style="color: var(--primary-red); letter-spacing: 3px; margin-bottom: 15px; font-weight: 600;">FORGE YOUR BODY • CONQUER THE ARENA</h5>
            <h1>Fitness War Gym <span>Lalbagh</span></h1>
            <p>Step into the ultimate battleground of strength. Liquid Roman architecture and heavy training equipment built for true titans in Lalbagh.</p>
            <div style="display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
                <a href="#shop" class="cta-btn">Browse Store</a>
            </div>
        </div>
    </header>

    <!-- Programs Section -->
    <section id="programs">
        <div class="section-title">
            <h2>Elite <span>Battle Programs</span></h2>
            <p>Choose your protocol and conquer your physical limits</p>
        </div>
        <div class="grid-3">
            <div class="card">
                <i class="fa-solid fa-dumbbell"></i>
                <h3>Gladiator Hypertrophy</h3>
                <p>Intense muscle-building protocols designed using classic heavy compound movements mixed with modern science.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-fire"></i>
                <h3>Infernal Shred</h3>
                <p>High-intensity interval training tailored to strip body fat while preserving hard-earned muscle tissue.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-shield-halved"></i>
                <h3>Titanium Strength</h3>
                <p>Powerlifting and raw strength conditioning to turn your physique into an impenetrable fortress.</p>
            </div>
        </div>
    </section>

    <!-- Product Store & Admin Panels Section -->
    <section id="shop">
        <div class="section-title">
            <h2>Gym Store & <span>Admin Dashboard</span></h2>
            <p>Manage products or check customer orders securely</p>
        </div>

        <!-- Admin Buttons Toggle -->
        <div class="admin-controls-header">
            <button class="secondary-btn" onclick="toggleAdminPanel('upload')"><i class="fa-solid fa-plus-circle"></i> Add New Product</button>
            <button class="secondary-btn" onclick="toggleAdminPanel('orders')"><i class="fa-solid fa-clipboard-list"></i> View Customer Orders</button>
        </div>

        <!-- Admin Product Upload Panel -->
        <div class="admin-panel" id="uploadPanel">
            <h3 style="margin-bottom: 25px; font-size: 1.3rem; color: var(--text-light); text-align: center;"><i class="fa-solid fa-lock"></i> Admin Product Uploader</h3>
            
            <div class="form-group">
                <label for="pName">Product Name</label>
                <input type="text" id="pName" class="form-control" placeholder="e.g. Whey Protein / Gym Belt">
            </div>

            <div class="form-group">
                <label for="pPrice">Price (BDT)</label>
                <input type="number" id="pPrice" class="form-control" placeholder="e.g. 3500">
            </div>

            <div class="form-group">
                <label for="pImage">Upload Product Picture</label>
                <input type="file" id="pImage" class="form-control" accept="image/*">
            </div>

            <div style="text-align: center; margin-top: 30px;">
                <button type="button" class="cta-btn" id="doneBtn" style="padding: 12px 40px; font-size: 1rem;">Done / Publish Product</button>
            </div>
        </div>

        <!-- Admin Customer Orders View Panel -->
        <div class="admin-panel" id="ordersPanel">
            <h3 style="margin-bottom: 20px; font-size: 1.3rem; color: var(--text-light); text-align: center;"><i class="fa-solid fa-users"></i> Customer Orders List</h3>
            <div id="adminOrdersContainer">
                <!-- Orders table will load here -->
            </div>
        </div>

        <!-- Live Products Grid Container -->
        <div class="products-display-grid" id="productContainer">
            <!-- Products will be loaded here dynamically -->
        </div>
    </section>

    <!-- Checkout Modal Form (Name, Phone, Address, Advance bKash) -->
    <div class="modal-overlay" id="orderModal">
        <div class="modal-box">
            <button class="close-modal" id="closeModal">&times;</button>
            <h3>Complete Your Order</h3>
            <p id="modalProductText">Product Info</p>
            
            <div class="bkash-box">
                <i class="fa-solid fa-wallet"></i> Cash on Delivery Policy:<br>
                Age <strong>200 Taka</strong> advance pathate hobe bKash-e: <br>
                <span style="font-size: 1.2rem; color: #fff;">01765336997</span> (Personal/Send Money)
            </div>

            <form id="customerOrderForm">
                <div class="form-group">
                    <label for="custName">Your Full Name</label>
                    <input type="text" id="custName" class="form-control" placeholder="e.g. Rahim Ahmed" required>
                </div>
                <div class="form-group">
                    <label for="custPhone">Phone Number</label>
                    <input type="text" id="custPhone" class="form-control" placeholder="e.g. 017XXXXXXXX" required>
                </div>
                <div class="form-group">
                    <label for="custAddress">Delivery Address</label>
                    <textarea id="custAddress" class="form-control" rows="2" placeholder="House, Road, Area, Lalbagh, Dhaka" required></textarea>
                </div>
                <div class="form-group">
                    <label for="custTrx">bKash TrxID (After sending 200tk advance)</label>
                    <input type="text" id="custTrx" class="form-control" placeholder="e.g. 9N8G7F65E4" required>
                </div>
                <button type="submit" class="cta-btn" style="width: 100%; text-align: center; border-radius: 8px; padding: 12px; background: #25d366; border-color: #25d366;">
                    <i class="fa-brands fa-whatsapp"></i> Submit Order & Chat on WhatsApp
                </button>
            </form>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 <span>Fitness War Gym Lalbagh</span>. All Rights Reserved.</p>
        <div class="developer-credit">
            Developed by <span>Mir Abdullah</span>
        </div>
    </footer>

    <!-- JavaScript Handling All Features -->
    <script>
        const ADMIN_PASSWORD = "3351774017";
        const ADMIN_WHATSAPP = "8801765336997";
        let selectedProductForOrder = null;

        // Load data on startup
        document.addEventListener('DOMContentLoaded', () => {
            loadProducts();
        });

        // Toggle Admin Panels with Password
        function toggleAdminPanel(type) {
            const enteredPass = prompt("Enter Admin Password to access:");
            if (enteredPass !== ADMIN_PASSWORD) {
                alert("Incorrect Password! Access Denied.");
                return;
            }

            const uploadPanel = document.getElementById('uploadPanel');
            const ordersPanel = document.getElementById('ordersPanel');

            if(type === 'upload') {
                uploadPanel.classList.toggle('active');
                ordersPanel.classList.remove('active');
            } else if(type === 'orders') {
                ordersPanel.classList.toggle('active');
                uploadPanel.classList.remove('active');
                renderAdminOrders();
            }
        }

        // Add Product Logic
        document.getElementById('doneBtn').addEventListener('click', function() {
            const name = document.getElementById('pName').value.trim();
            const price = document.getElementById('pPrice').value.trim();
            const imageInput = document.getElementById('pImage');
            
            if(!name || !price || imageInput.files.length === 0) {
                alert('Please fill out all fields and upload a product picture!');
                return;
            }

            const reader = new FileReader();
            reader.onload = function(e) {
                const newProduct = {
                    id: Date.now(),
                    name: name,
                    price: price,
                    image: e.target.result
                };

                let products = JSON.parse(localStorage.getItem('gymProducts')) || [];
                products.push(newProduct);
                localStorage.setItem('gymProducts', JSON.stringify(products));

                loadProducts();
                
                document.getElementById('pName').value = '';
                document.getElementById('pPrice').value = '';
                document.getElementById('pImage').value = '';
                
                alert('Product Published Successfully!');
                document.getElementById('uploadPanel').classList.remove('active');
            }
            reader.readAsDataURL(imageInput.files[0]);
        });

        // Load Products to Store Grid
        function loadProducts() {
            const container = document.getElementById('productContainer');
            container.innerHTML = '';
            
            let products = JSON.parse(localStorage.getItem('gymProducts')) || [];
            
            if(products.length === 0) {
                container.innerHTML = '<p style="color: var(--text-muted); grid-column: 1/-1; text-align: center; padding: 20px;">No products listed yet.</p>';
                return;
            }

            products.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-item-card';
                productCard.innerHTML = `
                    <img src="${product.image}" alt="${product.name}">
                    <div class="product-info">
                        <h4>${product.name}</h4>
                        <p>৳ ${product.price}</p>
                    </div>
                    <button class="order-now-btn" onclick="openOrderModal('${product.name}', '${product.price}')">
                        <i class="fa-solid fa-cart-shopping"></i> Order Now
                    </button>
                `;
                container.appendChild(productCard);
            });
        }

        // Open Checkout Modal
        const modal = document.getElementById('orderModal');
        const closeModalBtn = document.getElementById('closeModal');

        function openOrderModal(productName, productPrice) {
            selectedProductForOrder = { name: productName, price: productPrice };
            document.getElementById('modalProductText').innerHTML = `Ordering: <strong style="color:var(--text-light);">${productName}</strong> (৳ ${productPrice})`;
            modal.style.display = 'flex';
        }

        closeModalBtn.addEventListener('click', () => { modal.style.display = 'none'; });
        window.addEventListener('click', (e) => { if(e.target === modal) modal.style.display = 'none'; });

        // Handle Customer Order Form Submit
        document.getElementById('customerOrderForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('custName').value.trim();
            const phone = document.getElementById('custPhone').value.trim();
            const address = document.getElementById('custAddress').value.trim();
            const trx = document.getElementById('custTrx').value.trim();

            const orderData = {
                id: Date.now(),
                productName: selectedProductForOrder.name,
                productPrice: selectedProductForOrder.price,
                customerName: name,
                customerPhone: phone,
                customerAddress: address,
                bkashTrx: trx,
                date: new Date().toLocaleString()
            };

            // Save to localStorage so admin can view it
            let orders = JSON.parse(localStorage.getItem('gymCustomerOrders')) || [];
            orders.push(orderData);
            localStorage.setItem('gymCustomerOrders', JSON.stringify(orders));

            // Construct WhatsApp Redirect Message
            const waMessage = encodeURIComponent(`*New Order Placed - Fitness War Gym*
----------------------------------
*Product:* ${orderData.productName} (৳ ${orderData.productPrice})
*Customer Name:* ${name}
*Phone:* ${phone}
*Address:* ${address}
*bKash TrxID:* ${trx}
----------------------------------
Please confirm my order!`);

            modal.style.display = 'none';
            document.getElementById('customerOrderForm').reset();

            // Open WhatsApp
            window.open(`https://wa.me/${ADMIN_WHATSAPP}?text=${waMessage}`, '_blank');
            alert('Order Submitted Successfully! Redirecting to WhatsApp to confirm...');
        });

        // Render Admin Orders in Table
        function renderAdminOrders() {
            const container = document.getElementById('adminOrdersContainer');
            let orders = JSON.parse(localStorage.getItem('gymCustomerOrders')) || [];

            if(orders.length === 0) {
                container.innerHTML = '<p style="color: var(--text-muted); text-align: center; padding: 15px;">No customer orders received yet.</p>';
                return;
            }

            let tableHTML = `
                <div style="overflow-x: auto;">
                    <table class="order-table">
                        <tr>
                            <th>Date</th>
                            <th>Product</th>
                            <th>Customer Info</th>
                            <th>Address</th>
                            <th>bKash TrxID</th>
                        </tr>
            `;

            orders.reverse().forEach(ord => {
                tableHTML += `
                    <tr>
                        <td>${ord.date}</td>
                        <td><strong>${ord.productName}</strong><br>৳ ${ord.productPrice}</td>
                        <td>${ord.customerName}<br>📞 ${ord.customerPhone}</td>
                        <td>${ord.customerAddress}</td>
                        <td style="color: #ff4d4d; font-weight:700;">${ord.bkashTrx}</td>
                    </tr>
                `;
            });

            tableHTML += `</table></div>`;
            container.innerHTML = tableHTML;
        }
    </script>
</body>
</html>
