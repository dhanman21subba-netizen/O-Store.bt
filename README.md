Here's your ready-to-use mobile-friendly store webpage code. It works like a Facebook Shop and POS system, and you can link it to both your Facebook Page and WhatsApp.

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>O-Store</title>
<style>
  body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f9f9f9; }
  header { background: #4CAF50; color: white; padding: 1rem; text-align: center; }
  .container { padding: 1rem; }
  .product { background: white; border-radius: 8px; padding: 1rem; margin-bottom: 1rem; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
  .product img { max-width: 100%; border-radius: 8px; }
  .product h3 { margin: 0.5rem 0; }
  .product button { background: #4CAF50; color: white; border: none; padding: 0.5rem 1rem; border-radius: 4px; cursor: pointer; }
  .product button:hover { background: #45a049; }
  footer { background: #333; color: white; text-align: center; padding: 1rem; }
</style>
</head>
<body>
<header>
  <h1>O-Store</h1>
  <p>Thimphu, Bhutan | <a href="https://www.facebook.com/share/1D526pbknX/" style="color:white;">Facebook</a></p>
</header>
<div class="container" id="product-list"></div>
<footer>
  <p>Contact us on <a href="https://wa.me/97517823940" style="color:#4CAF50;">WhatsApp</a></p>
</footer>
<script>
const products = [
  {
    name: "Continental Xtra — Instant South Blend",
    price: 395,
    stock: 20,
    image: "continental_xtra.jpg",
    description: "Instant coffee — South Blend.",
  },
  {
    name: "Continental Spéciale — 100% Pure Instant Coffee",
    price: 320,
    stock: 15,
    image: "continental_speciale.jpg",
    description: "Instant coffee — Speciale.",
  }
];
const container = document.getElementById('product-list');
products.forEach(p => {
  const div = document.createElement('div');
  div.className = 'product';
  div.innerHTML = `
    <img src="${p.image}" alt="${p.name}">
    <h3>${p.name}</h3>
    <p>${p.description}</p>
    <p><strong>Nu. ${p.price}</strong> | Stock: ${p.stock}</p>
    <a href="https://wa.me/97517823940?text=I want to buy ${encodeURIComponent(p.name)}" target="_blank">
      <button>Order on WhatsApp</button>
    </a>
  `;
  container.appendChild(div);
});
</script>
</body>
</html>

You can:

Replace continental_xtra.jpg and continental_speciale.jpg with your real image links.

Host this free on Netlify or GitHub Pages.

Share the link directly on Facebook and WhatsApp.


