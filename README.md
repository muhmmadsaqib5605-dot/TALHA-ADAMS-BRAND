<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TALHA ADAMS</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">

<style>
body{
  margin:0;
  font-family:Poppins;
  background:#fff;
}

/* HEADER */
header{
  display:flex;
  justify-content:space-between;
  padding:15px;
  border-bottom:1px solid #eee;
}

header h2{
  font-weight:bold;
}

/* PRODUCTS */
.products{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:10px;
  padding:10px;
}

.card{
  background:#fff;
  border-radius:10px;
  overflow:hidden;
  box-shadow:0 0 10px #eee;
}

.card img{
  width:100%;
}

.card p{
  padding:5px;
}

.price{
  font-weight:bold;
}

.btn{
  margin:5px;
  padding:10px;
  width:90%;
  background:black;
  color:white;
  border:none;
  border-radius:5px;
  cursor:pointer;
}

/* CONTACT */
.contact{
  text-align:center;
  padding:20px;
}

.contact a{
  display:inline-block;
  margin-top:10px;
  padding:12px 25px;
  background:#25D366;
  color:white;
  border-radius:30px;
  text-decoration:none;
}

/* FLOAT BUTTON */
.whatsapp{
  position:fixed;
  bottom:20px;
  right:20px;
  background:#25D366;
  padding:15px;
  border-radius:50%;
  color:white;
  font-size:22px;
  text-decoration:none;
}
</style>
</head>

<body>

<header>
  <h2>TALHA ADAMS</h2>
</header>

<div class="products">

  <div class="card">
    <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab">
    <p>T-Shirt</p>
    <p class="price">Rs 1999</p>
    <button class="btn" onclick="orderNow('T-Shirt')">Order Now</button>
  </div>

  <div class="card">
    <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f">
    <p>Pants</p>
    <p class="price">Rs 2499</p>
    <button class="btn" onclick="orderNow('Pants')">Order Now</button>
  </div>

</div>

<div class="contact">
  <h3>Contact Us</h3>
  <p>📞 0324 2994136</p>

  <!-- DIRECT WHATSAPP BUTTON -->
  <a href="https://wa.me/923242994136?text=Hello%20Talha%20Adams%20I%20want%20to%20order" target="_blank">
    Chat on WhatsApp
  </a>
</div>

<a class="whatsapp" href="https://wa.me/923242994136?text=Hello%20Talha%20Adams" target="_blank">💬</a>

<script>
function orderNow(product){
  let msg = "Hello Talha Adams, I want to order " + product;
  
  // IMPORTANT FIX
  let url = "https://wa.me/923242994136?text=" + encodeURIComponent(msg);

  window.open(url, "_blank");
}
</script>

</body>
</html>
