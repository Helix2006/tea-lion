<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tea Lion | Official</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; margin: 0; background: #fffdf5; color: #333; }
        header { background: #5d4037; color: white; padding: 20px; text-align: center; }
        nav { display: flex; justify-content: space-around; background: #3e2723; padding: 10px; position: sticky; top: 0; }
        nav a { color: white; text-decoration: none; font-weight: bold; cursor: pointer; }
        .page { display: none; padding: 20px; animation: fadeIn 0.5s; }
        .active { display: block; }
        .card { background: white; padding: 15px; margin-bottom: 15px; border-radius: 12px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        .menu-img { width: 100%; height: 150px; object-fit: cover; border-radius: 8px; margin-bottom: 10px; }
        .btn { display: block; background: #5d4037; color: white; text-align: center; padding: 10px; border-radius: 5px; text-decoration: none; margin-top: 10px; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<header><h1>TEA LION ☕</h1></header>

<nav>
    <a onclick="showPage('home')">Home</a>
    <a onclick="showPage('menu')">Menu</a>
    <a onclick="showPage('branches')">Branches</a>
    <a onclick="showPage('enquiry')">Contact</a>
</nav>

<div id="home" class="page active">
    <img src="https://images.unsplash.com/photo-1594631252845-29fc4cc8c784?w=800" class="menu-img" alt="Tea">
    <h2>Welcome to Tea Lion</h2>
    <p>Experience the authentic taste of Chennai. Freshly brewed, every time.</p>
</div>

<div id="menu" class="page">
    <h2>Our Menu</h2>
    <div class="card">
        <img src="https://images.unsplash.com/photo-1561336313-0bd4e0b27d88?w=400" class="menu-img">
        <h3>Masala Tea - ₹20</h3>
        <p>A perfect blend of spices and fresh milk.</p>
    </div>
    <div class="card">
        <img src="https://images.unsplash.com/photo-1559056199-641a0ac8b55e?w=400" class="menu-img">
        <h3>Filter Coffee - ₹25</h3>
        <p>South Indian traditional strong coffee.</p>
    </div>
</div>

<div id="branches" class="page">
    <h2>Our Branches</h2>
    <div class="card">
        <h3>Adyar Branch</h3>
        <p>Main Road, Near Bus Stop, Chennai.</p>
        <a href="https://maps.google.com/?q=Adyar+Chennai" class="btn">Navigate on Map</a>
    </div>
    <div class="card">
        <h3>Anna Nagar Branch</h3>
        <p>2nd Avenue, Anna Nagar, Chennai.</p>
        <a href="https://maps.google.com/?q=Anna+Nagar+Chennai" class="btn">Navigate on Map</a>
    </div>
</div>

<div id="enquiry" class="page">
    <h2>Franchise & Contact</h2>
    <div class="card">
        <p><strong>Owner Phone:</strong> +91 98765 43210</p>
        <p><strong>Email:</strong> franchise@tealion.com</p>
    </div>
    <form action="https://formspree.io/f/YOUR_ID_HERE" method="POST">
        <input type="text" name="name" placeholder="Your Name" style="width: 90%; padding: 10px; margin-bottom: 10px;">
        <button type="submit" class="btn">Send Enquiry</button>
    </form>
</div>

<script>
    function showPage(id) {
        document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
        document.getElementById(id).classList.add('active');
    }
</script>

</body>
</html>
