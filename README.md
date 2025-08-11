<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mystic Harmony Apothecary</title>
  <link
    href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=Quicksand:wght@400;600&display=swap"
    rel="stylesheet"
  />
  <style>
    :root {
      --lavender-mist: #c8bfe7;
      --sage-green: #a8c3a0;
      --soft-earth: #e7d9c2;
      --amethyst-deep: #6a4e77;
      --charcoal-smoke: #4a4a4a;
      --ivory-white: #faf9f6;
    }

    body {
      margin: 0;
      font-family: "Quicksand", sans-serif;
      background-color: var(--ivory-white);
      color: var(--charcoal-smoke);
    }

    header {
      background-color: var(--sage-green);
      padding: 1rem;
      text-align: center;
    }

    header h1 {
      font-family: "Cormorant Garamond", serif;
      color: var(--amethyst-deep);
      margin: 0;
    }

    nav {
      background-color: var(--lavender-mist);
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      padding: 0.5rem 0;
      flex-wrap: wrap;
    }

    nav a {
      text-decoration: none;
      color: var(--charcoal-smoke);
      font-weight: 600;
      cursor: pointer;
    }

    main {
      padding: 2rem;
      max-width: 1000px;
      margin: 0 auto;
    }

    section {
      margin-bottom: 2rem;
    }

    h2 {
      font-family: "Cormorant Garamond", serif;
      color: var(--amethyst-deep);
    }

    .product-card {
      background-color: var(--soft-earth);
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
      display: inline-block;
      width: 280px;
      margin: 1rem;
      vertical-align: top;
    }

    .product-card img {
      width: 100%;
      border-radius: 8px;
    }

    .product-card button {
      background-color: var(--amethyst-deep);
      color: var(--ivory-white);
      border: none;
      padding: 0.5rem 1rem;
      font-family: "Cormorant Garamond", serif;
      border-radius: 6px;
      cursor: pointer;
    }

    form input,
    form textarea,
    form button {
      display: block;
      width: 100%;
      margin-bottom: 1rem;
      padding: 0.75rem;
      border-radius: 6px;
      border: 1px solid var(--sage-green);
      font-family: "Quicksand", sans-serif;
    }

    form button {
      background-color: var(--amethyst-deep);
      color: var(--ivory-white);
      border: none;
      cursor: pointer;
    }

    footer {
      background-color: var(--charcoal-smoke);
      color: var(--soft-earth);
      text-align: center;
      padding: 1rem;
    }

    /* Cart styles */
    #cart-items ul {
      list-style: none;
      padding-left: 0;
    }

    #cart-items li {
      margin-bottom: 1rem;
    }

    #cart-items input[type="number"] {
      width: 50px;
      padding: 0.25rem;
      border-radius: 4px;
      border: 1px solid var(--sage-green);
      font-family: "Quicksand", sans-serif;
    }

    #cart-items button {
      margin-left: 10px;
      background: var(--amethyst-deep);
      color: var(--ivory-white);
      border: none;
      border-radius: 4px;
      cursor: pointer;
      padding: 0.25rem 0.5rem;
      font-family: "Cormorant Garamond", serif;
    }

    #process-order-btn,
    #clear-cart-btn {
      background-color: var(--amethyst-deep);
      color: var(--ivory-white);
      border: none;
      padding: 0.75rem 1.25rem;
      border-radius: 6px;
      margin-right: 1rem;
      cursor: pointer;
      font-family: "Cormorant Garamond", serif;
      margin-top: 1rem;
    }

    #process-order-btn:disabled,
    #clear-cart-btn:disabled {
      background-color: #a490a9;
      cursor: not-allowed;
    }

    @media (max-width: 600px) {
      nav {
        flex-direction: column;
      }

      .product-card {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Mystic Harmony Apothecary</h1>
  </header>

  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#gallery">Gallery</a>
    <a href="#products">Products</a>
    <a href="#custom">Custom Orders</a>
    <a href="#contact">Contact</a>
    <a href="#cart">Cart</a>
  </nav>

  <main>
    <section id="home">
      <h2>Welcome</h2>
      <p>
        Experience the serenity and beauty of holistic living. Mystic Harmony Apothecary brings nature’s healing elements to your everyday rituals.
      </p>
    </section>

    <section id="about" style="display:none;">
      <h2>About Us</h2>
      <p>
        Mystic Harmony Apothecary was founded on the belief in mindful healing and intentional living. Our mission is to provide spiritual wellness products that are ethically sourced and hand-selected with love.
      </p>
    </section>

    <section id="gallery" style="display:none;">
      <h2>Gallery</h2>
      <p>Take a look at our handcrafted creations and shop ambiance.</p>

      <div class="product-card">
        <img src="https://via.placeholder.com/280x180" alt="White Sage Bundle" />
        <h3>White Sage Bundle</h3>
        <p>$12.00</p>
        <button onclick="addToCart('White Sage Bundle', 12)">Add to Cart</button>
      </div>

      <div class="product-card">
        <img src="https://via.placeholder.com/280x180" alt="Amethyst Crystal" />
        <h3>Amethyst Crystal</h3>
        <p>$18.00</p>
        <button onclick="addToCart('Amethyst Crystal', 18)">Add to Cart</button>
      </div>

      <p>
        Want to see your cart? <a href="#cart" onclick="showCart()">Go to Cart</a>
      </p>
    </section>

    <section id="products" style="display:none;">
      <h2>Featured Products</h2>
      <div class="product-card">
        <img src="https://via.placeholder.com/280x180" alt="White Sage Bundle" />
        <h3>White Sage Bundle</h3>
        <p>$12.00</p>
        <button onclick="addToCart('White Sage Bundle', 12)">Add to Cart</button>
      </div>
      <div class="product-card">
        <img src="https://via.placeholder.com/280x180" alt="Amethyst Crystal" />
        <h3>Amethyst Crystal</h3>
        <p>$18.00</p>
        <button onclick="addToCart('Amethyst Crystal', 18)">Add to Cart</button>
      </div>
    </section>

    <section id="custom" style="display:none;">
      <h2>Custom Orders</h2>
      <p>
        Let us create a personalized ritual kit or spiritual gift for you. Tell us what intention you want to set and we’ll craft something unique.
      </p>
    </section>

    <section id="contact" style="display:none;">
      <h2>Contact Us</h2>
      <form onsubmit="saveContactForm(event)">
        <input type="text" id="name" placeholder="Your Name" required />
        <input type="email" id="email" placeholder="Your Email" required />
        <textarea id="message" placeholder="Your Message" rows="5" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </section>

    <section id="cart" style="display:none;">
      <h2>Your Shopping Cart</h2>
      <div id="cart-items">
        <p>Your cart is empty.</p>
      </div>
      <p id="cart-total"></p>
      <button onclick="processOrder()" id="process-order-btn" disabled>Process Order</button>
      <button onclick="clearCart()" id="clear-cart-btn" disabled>Clear Cart</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Mystic Harmony Apothecary | Designed with intention and care</p>
  </footer>

  <script>
    // Contact form - save to localStorage
    function saveContactForm(event) {
      event.preventDefault();
      const contactData = {
        name: document.getElementById("name").value,
        email: document.getElementById("email").value,
        message: document.getElementById("message").value,
      };
      localStorage.setItem("mysticContactForm", JSON.stringify(contactData));
      alert("Thank you for your message!");
      event.target.reset();
    }

    // CART FUNCTIONS

    // Retrieve cart from localStorage
    function getCart() {
      return JSON.parse(localStorage.getItem("mysticCart")) || [];
    }

    // Save cart to localStorage
    function saveCart(cart) {
      localStorage.setItem("mysticCart", JSON.stringify(cart));
    }

    // Add item to cart
    function addToCart(name, price) {
      let cart = getCart();
      let itemIndex = cart.findIndex((item) => item.name === name);
      if (itemIndex > -1) {
        cart[itemIndex].quantity++;
      } else {
        cart.push({ name, price, quantity: 1 });
      }
      saveCart(cart);
      alert(`${name} added to cart.`);
    }

    // Show cart page and render items
    function showCart() {
      document.querySelector("section#cart").style.display = "block";

      // Hide other sections except cart
      document.querySelectorAll("main > section:not(#cart)").forEach((s) => {
        s.style.display = "none";
      });

      updateCartDisplay();
    }

    // Update the cart display on Cart page
    function updateCartDisplay() {
      const cartDiv = document.getElementById("cart-items");
      const totalDiv = document.getElementById("cart-total");
      const processBtn = document.getElementById("process-order-btn");
      const clearBtn = document.getElementById("clear-cart-btn");

      let cart = getCart();

      if (cart.length === 0) {
        cartDiv.innerHTML = "<p>Your cart is empty.</p>";
        totalDiv.textContent = "";
        processBtn.disabled = true;
        clearBtn.disabled = true;
        return;
      }

      let html = "<ul>";
      let total = 0;

      cart.forEach((item, index) => {
        html += `
          <li>
            <strong>${item.name}</strong> — $${item.price} x 
            <input type="number" min="1" value="${item.quantity}" 
              onchange="changeQuantity(${index}, this.value)">
            = $${(item.price * item.quantity).toFixed(2)}
            <button onclick="removeItem(${index})">Remove</button>
          </li>
        `;
        total += item.price * item.quantity;
      });

      html += "</ul>";
      cartDiv.innerHTML = html;
      totalDiv.textContent = `Total: $${total.toFixed(2)}`;

      processBtn.disabled = false;
      clearBtn.disabled = false;
    }

    // Change quantity of an item
    function changeQuantity(index, newQty) {
      let cart = getCart();
      newQty = parseInt(newQty);
      if (newQty < 1 || isNaN(newQty)) {
        alert("Quantity must be at least 1.");
        updateCartDisplay();
        return;
      }
      cart[index].quantity = newQty;
      saveCart(cart);
      updateCartDisplay();
    }

    // Remove item from cart
    function removeItem(index) {
      let cart = getCart();
      cart.splice(index, 1);
      saveCart(cart);
      updateCartDisplay();
    }

    // Clear entire cart
    function clearCart() {
      if (confirm("Are you sure you want to clear your cart?")) {
        localStorage.removeItem("mysticCart");
        alert("Your cart has been cleared.");
        updateCartDisplay();
      }
    }

    // Process order
    function processOrder() {
      let cart = getCart();
      if (cart.length === 0) {
        alert("Your cart is empty.");
        return;
      }
      alert("Thank you for your order! We will process it shortly.");
      localStorage.removeItem("mysticCart");
      updateCartDisplay();
    }

    // Nav link behavior to show sections properly
    document.querySelectorAll("nav a").forEach((link) => {
      link.addEventListener("click", (e) => {
        e.preventDefault();
        const targetId = link.getAttribute("href").substring(1);
        if (targetId === "cart") {
          showCart();
        } else {
          document.querySelectorAll("main > section").forEach((s) => {
            s.style.display = "none";
          });
          document.getElementById(targetId).style.display = "block";
        }
      });
    });

    // Show Home section on load, hide others
    window.onload = () => {
      document.querySelectorAll("main > section").forEach((s) => (s.style.display = "none"));
      document.getElementById("home").style.display = "block";
