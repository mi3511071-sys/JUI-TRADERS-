# JUI-TRADERS-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fresh Vegetables - Online Vegetable Store</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
        }
        
        /* Header */
        header {
            background-color: #2E7D32;
            color: white;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        
        .cart-btn {
            background-color: #FF9800;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }
        
        /* Navigation */
        nav {
            background-color: #388E3C;
            padding: 10px 30px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            margin-right: 20px;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://source.unsplash.com/1600x900/?vegetables');
            background-size: cover;
            color: white;
            text-align: center;
            padding: 100px 20px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero button {
            background-color: #FF9800;
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
        }
        
        /* Products Section */
        .products {
            padding: 50px 30px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .products h2 {
            text-align: center;
            margin-bottom: 40px;
            color: #333;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background: white;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-card img {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 50%;
            margin-bottom: 15px;
        }
        
        .product-card h3 {
            color: #333;
            margin-bottom: 10px;
        }
        
        .price {
            color: #2E7D32;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 15px;
        }
        
        .add-to-cart {
            background-color: #FF9800;
            color: white;
            border: none;
            padding: 10px 25px;
            cursor: pointer;
            border-radius: 5px;
            width: 100%;
        }
        
        /* Features */
        .features {
            display: flex;
            justify-content: space-around;
            padding: 50px 30px;
            background-color: white;
            flex-wrap: wrap;
        }
        
        .feature {
            text-align: center;
            padding: 20px;
        }
        
        .feature-icon {
            font-size: 40px;
            margin-bottom: 10px;
        }
        
        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 50px;
        }
        
        /* Contact Section */
        .contact {
            background-color: white;
            padding: 50px 30px;
            text-align: center;
        }
        
        .contact form {
            max-width: 500px;
            margin: 20px auto;
        }
        
        .contact input, .contact textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .contact button {
            background-color: #2E7D32;
            color: white;
            border: none;
            padding: 12px 40px;
            cursor: pointer;
            border-radius: 5px;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 32px;
            }
        }
    </style>
</head>
<body>
    
    <!-- Header -->
    <header>
        <div class="logo">🥬 Fresh Vegetables</div>
        <div class="cart-btn">🛒 Cart (0)</div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <a href="#home">Home</a>
        <a href="#products">Vegetables</a>
        <a href="#contact">Contact</a>
        <a href="#about">About Us</a>
    </nav>
    
    <!-- Hero Section -->
    <section class="hero" id="home">
        <h1>Fresh Vegetables Delivered to Your Home</h1>
        <p>Best quality Alu, Tomato, Onion, Garlic and more</p>
        <br>
        <button onclick="document.getElementById('products').scrollIntoView()">Shop Now</button>
    </section>
    
    <!-- Products -->
    <section class="products" id="products">
        <h2>Our Fresh Vegetables</h2>
        <div class="product-grid">
            <!-- Potato -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?potato" alt="Potato">
                <h3>Potato (Alu)</h3>
                <p class="price">৳ 30/kg</p>
                <button class="add-to-cart" onclick="addToCart('Potato', 30)">Add to Cart</button>
            </div>
            
            <!-- Tomato -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?tomato" alt="Tomato">
                <h3>Tomato</h3>
                <p class="price">৳ 80/kg</p>
                <button class="add-to-cart" onclick="addToCart('Tomato', 80)">Add to Cart</button>
            </div>
            
            <!-- Onion -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?onion" alt="Onion">
                <h3>Onion</h3>
                <p class="price">৳ 60/kg</p>
                <button class="add-to-cart" onclick="addToCart('Onion', 60)">Add to Cart</button>
            </div>
            
            <!-- Garlic -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?garlic" alt="Garlic">
                <h3>Garlic</h3>
                <p class="price">৳ 200/kg</p>
                <button class="add-to-cart" onclick="addToCart('Garlic', 200)">Add to Cart</button>
            </div>
            
            <!-- Carrot -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?carrot" alt="Carrot">
                <h3>Carrot</h3>
                <p class="price">৳ 70/kg</p>
                <button class="add-to-cart" onclick="addToCart('Carrot', 70)">Add to Cart</button>
            </div>
            
            <!-- Cabbage -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?cabbage" alt="Cabbage">
                <h3>Cabbage</h3>
                <p class="price">৳ 40/piece</p>
                <button class="add-to-cart" onclick="addToCart('Cabbage', 40)">Add to Cart</button>
            </div>
            
            <!-- Cauliflower -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?cauliflower" alt="Cauliflower">
                <h3>Cauliflower</h3>
                <p class="price">৳ 50/piece</p>
                <button class="add-to-cart" onclick="addToCart('Cauliflower', 50)">Add to Cart</button>
            </div>
            
            <!-- Green Chili -->
            <div class="product-card">
                <img src="https://source.unsplash.com/200x200/?chili" alt="Green Chili">
                <h3>Green Chili</h3>
                <p class="price">৳ 120/kg</p>
                <button class="add-to-cart" onclick="addToCart('Green Chili', 120)">Add to Cart</button>
            </div>
        </div>
    </section>
    
    <!-- Features -->
    <section class="features">
        <div class="feature">
            <div class="feature-icon">🚚</div>
            <h3>Fast Delivery</h3>
            <p>Same day delivery</p>
        </div>
        <div class="feature">
            <div class="feature-icon">🌿</div>
            <h3>Fresh Products</h3>
            <p>100% fresh vegetables</p>
        </div>
        <div class="feature">
            <div class="feature-icon">💰</div>
            <h3>Best Price</h3>
            <p>Competitive pricing</p>
        </div>
    </section>
    
    <!-- Contact -->
    <section class="contact" id="contact">
        <h2>Contact Us</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <input type="tel" placeholder="Your Phone Number" required>
            <textarea rows="5" placeholder="Your Message"></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>
    
    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Fresh Vegetables. All rights reserved.</p>
        <p>📞 Hotline: 01234567890 | 📧 Email: info@freshvegetables.com</p>
    </footer>
    
    <script>
        let cartCount = 0;
        
        function addToCart(item, price) {
            cartCount++;
            alert(item + ' added to cart! Price: ৳ ' + price);
            document.querySelector('.cart-btn').textContent = '🛒 Cart (' + cartCount + ')';
        }
    </script>
    
</body>
</html>
