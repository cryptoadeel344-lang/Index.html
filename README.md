<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Shop</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #ffffff;
            color: #000000;
        }
        header {
            background-color: #000000;
            color: #ffffff;
            text-align: center;
            padding: 20px;
            font-size: 2em;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        .product {
            border: 1px solid #cccccc;
            padding: 20px;
            text-align: center;
            background-color: #f9f9f9;
        }
        .product img {
            max-width: 100%;
            height: auto;
        }
        .product h3 {
            margin: 10px 0;
        }
        .product p {
            margin: 10px 0;
        }
        .btn {
            background-color: #000000;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            margin-top: 10px;
        }
        .btn:hover {
            background-color: #333333;
        }
        @media (max-width: 768px) {
            header {
                font-size: 1.5em;
                padding: 15px;
            }
            .container {
                padding: 10px;
            }
            .products {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>My Shop</h1>
    </header>
    <div class="container">
        <section class="products">
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=Product+1" alt="Product 1">
                <h3>Product 1</h3>
                <p>Price: $10.00</p>
                <p>Description: This is a great product for everyday use.</p>
                <button class="btn" onclick="orderOnWhatsApp('Product 1')">Order on WhatsApp</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=Product+2" alt="Product 2">
                <h3>Product 2</h3>
                <p>Price: $15.00</p>
                <p>Description: High-quality item with excellent features.</p>
                <button class="btn" onclick="orderOnWhatsApp('Product 2')">Order on WhatsApp</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=Product+3" alt="Product 3">
                <h3>Product 3</h3>
                <p>Price: $20.00</p>
                <p>Description: Premium product for special occasions.</p>
                <button class="btn" onclick="orderOnWhatsApp('Product 3')">Order on WhatsApp</button>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/300x200?text=Product+4" alt="Product 4">
                <h3>Product 4</h3>
                <p>Price: $25.00</p>
                <p>Description: Durable and reliable for long-term use.</p>
                <button class="btn" onclick="orderOnWhatsApp('Product 4')">Order on WhatsApp</button>
            </div>
        </section>
    </div>
    <script>
        function orderOnWhatsApp(productName) {
            const phoneNumber = "+923274695193";
            const message = encodeURIComponent(`Hi, I'd like to order ${productName}.`);
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }
    </script>
</body>
</html>
