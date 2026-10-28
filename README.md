[28/10, 7:51 pm] Sufia: <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Masala Muse – Food Ordering</title>
<meta name="description" content="Masala Muse: a fast, mobile-ready food ordering website built with HTML, CSS and JavaScript.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700;800&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
</head>
<body>

<!-- Header: brand, navigation, search box, cart button, mobile menu button -->
<header>
  <div class="wrap nav">
    <a class="brand" href="#home" aria-label="Masala Muse home">
      <span class="brand-mark">✦</span><span>masala <em>muse</em></span>
    </a>
    <nav class="navlinks" id="navlinks" aria-label="Main navigation">
      <a href="#home">Home</a><a href="#menu">Explore menu</a>
      <a href="#story">Our story</a><a href="#footer">Contact</a>
    </nav>
    <div class="nav-actions">
      <label class="search-wrap"><span class="search-icon">⌕</span>
        <input id="searchInput" type="search" placeholder="Find your favourite…" aria-label="Search food">
      </label>
      <button class="cart-btn" id="openCart" aria-label="Open shopping cart">
        <span>♧</span><span class="cart-label">Your cart</span>
        <span class="cart-count" id="cartCount">0</span>
      </button>
      <button class="menu-toggle" id="menuToggle" aria-label="Toggle navigation">&#9776;</button>
    </div>
  </div>
</header>

<main>
  <!-- Hero section -->
  <section class="hero" id="home">
    <div class="wrap hero-grid">
      <div>
        <span class="pill">FRESHLY MADE, JOYFULLY DELIVERED</span>
        <h1>A little spice.<br>A lot of <em>happiness.</em></h1>
        <p class="lead">From comfort-food classics to your new favourite bites, discover thoughtfully made food that turns an ordinary day into something delicious.</p>
        <div class="hero-actions">
          <button class="primary" data-scroll="#menu">Explore the menu ↗</button>
          <button class="secondary" data-scroll="#story">Our kitchen story</button>
        </div>
        <div class="hero-stats">
          <div class="avatars" aria-hidden="true"><i></i><i></i><i></i></div>
          <div><strong>4.9/5 <span class="stars">★★★★★</span></strong>Loved by food people</div>
          <div><strong>25–35 min</strong>Average delivery</div>
        </div>
      </div>
      <div class="hero-visual">
        <div class="hero-plate"><img src="images/hero.jpg" alt="Chicken biryani served in a clay bowl"></div>
        <div class="float-chip chip-a"><span class="ico">🥗</span><div><b>Fresh ingredients</b>Picked with care, daily</div></div>
        <div class="float-chip chip-b"><span class="ico">♡</span><div><b>Made with love</b>Every bite counts</div></div>
      </div>
    </div>
  </section>

  <!-- Trust strip -->
  <div class="trust"><div class="wrap">
    <span>✦ Fresh, quality ingredients</span><span>♧ Carefully packed</span>
    <span>↗ Quick doorstep delivery</span><span>♡ Flavour in every bite</span>
  </div></div>

  <!-- Menu section -->
  <section class="section" id="menu">
    <div class="wrap">
      <div class="section-head">
        <div>
          <div class="eyebrow">THE GOOD STUFF</div>
          <h2>Made to make you hungry.</h2>
          <p>Fresh favourites, big flavours, and a little something for everyone.</p>
        </div>
        <span class="result-count" id="resultCount">12 delicious picks</span>
      </div>

      <!-- Category filter buttons -->
      <div class="filters" id="filters" aria-label="Filter food categories">
        <button class="filter active" data-category="All">All dishes</button>
        <button class="filter" data-category="Indian">Indian favourites</button>
        <button class="filter" data-category="Pizza">Pizza</button>
        <button class="filter" data-category="Burgers">Burgers</button>
        <button class="filter" data-category="Healthy">Fresh &amp; healthy</button>
        <button class="filter" data-category="Desserts">Desserts</button>
        <button class="filter" data-category="Drinks">Drinks</button>
      </div>

      <!-- Food cards (data-* attributes feed the cart) -->
      <div class="menu-grid" id="menuGrid">
    <article class="food-card" data-name="Paneer tikka bowl" data-category="Indian" data-price="249" data-id="paneer">
      <div class="food-image-wrap">
        <img class="food-image" alt="Paneer tikka served with chutney" loading="lazy" src="images/paneer.jpg">
        <span class="tag">BESTSELLER</span>
        <button class="heart" aria-label="Add Paneer Tikka Bowl to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Paneer Tikka Bowl</h3><span class="price">₹249</span></div>
        <p class="food-desc">Smoky paneer, fragrant rice and creamy masala.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.9 · 20 min</span>
          <button class="add-btn" aria-label="Add Paneer Tikka Bowl to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Margherita pizza" data-category="Pizza" data-price="299" data-id="margherita">
      <div class="food-image-wrap">
        <img class="food-image" alt="Margherita pizza" loading="lazy" src="images/margherita.jpg">
        <span class="tag">VEG FAVOURITE</span>
        <button class="heart" aria-label="Add Margherita Pizza to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Margherita Pizza</h3><span class="price">₹299</span></div>
        <p class="food-desc">Golden crust, melty mozzarella and fresh basil.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.8 · 25 min</span>
          <button class="add-btn" aria-label="Add Margherita Pizza to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Classic smash burger" data-category="Burgers" data-price="219" data-id="smash">
      <div class="food-image-wrap">
        <img class="food-image" alt="Smash burger with lettuce" loading="lazy" src="images/smash.jpg">
        <span class="tag">CROWD PLEASER</span>
        <button class="heart" aria-label="Add Classic Smash Burger to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Classic Smash Burger</h3><span class="price">₹219</span></div>
        <p class="food-desc">Juicy patty, crisp lettuce and house sauce.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.7 · 20 min</span>
          <button class="add-btn" aria-label="Add Classic Smash Burger to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Garden fresh salad" data-category="Healthy" data-price="189" data-id="salad">
      <div class="food-image-wrap">
        <img class="food-image" alt="Fresh garden salad bowl" loading="lazy" src="images/salad.jpg">
        <button class="heart" aria-label="Add Garden Fresh Salad to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Garden Fresh Salad</h3><span class="price">₹189</span></div>
        <p class="food-desc">Crunchy greens, seasonal veggies and tangy dressing.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.6 · 15 min</span>
          <button class="add-btn" aria-label="Add Garden Fresh Salad to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Butter chicken bowl" data-category="Indian" data-price="289" data-id="butter">
      <div class="food-image-wrap">
        <img class="food-image" alt="Butter chicken curry" loading="lazy" src="images/butter.jpg">
        <span class="tag">CHEF'S PICK</span>
        <button class="heart" aria-label="Add Butter Chicken Bowl to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Butter Chicken Bowl</h3><span class="price">₹289</span></div>
        <p class="food-desc">Silky tomato gravy, tender chicken and warm spices.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.9 · 25 min</span>
          <button class="add-btn" aria-label="Add Butter Chicken Bowl to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Farmhouse pizza" data-category="Pizza" data-price="349" data-id="farmhouse">
      <div class="food-image-wrap">
        <img class="food-image" alt="Farmhouse pizza" loading="lazy" src="images/farmhouse.jpg">
        <button class="heart" aria-label="Add Farmhouse Pizza to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Farmhouse Pizza</h3><span class="price">₹349</span></div>
        <p class="food-desc">Peppers, mushrooms, onion and extra cheese.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.7 · 30 min</span>
          <button class="add-btn" aria-label="Add Farmhouse Pizza to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Crispy chicken burger" data-category="Burgers" data-price="259" data-id="crispy">
      <div class="food-image-wrap">
        <img class="food-image" alt="Crispy chicken burger" loading="lazy" src="images/crispy.jpg">
        <button class="heart" aria-label="Add Crispy Chicken Burger to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Crispy Chicken Burger</h3><span class="price">₹259</span></div>
        <p class="food-desc">Crunchy chicken, pickles and creamy pepper mayo.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.8 · 22 min</span>
          <button class="add-btn" aria-label="Add Crispy Chicken Burger to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Avocado toast" data-category="Healthy" data-price="199" data-id="avocado">
      <div class="food-image-wrap">
        <img class="food-image" alt="Avocado toast" loading="lazy" src="images/avocado.jpg">
        <button class="heart" aria-label="Add Avocado Toast to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Avocado Toast</h3><span class="price">₹199</span></div>
        <p class="food-desc">Sourdough toast, creamy avocado and chilli flakes.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.5 · 15 min</span>
          <button class="add-btn" aria-label="Add Avocado Toast to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Chocolate lava cake" data-category="Desserts" data-price="149" data-id="lava">
      <div class="food-image-wrap">
        <img class="food-image" alt="Chocolate lava cake" loading="lazy" src="images/lava.jpg">
        <button class="heart" aria-label="Add Chocolate Lava Cake to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Chocolate Lava Cake</h3><span class="price">₹149</span></div>
        <p class="food-desc">Warm chocolate cake with a molten centre.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.9 · 12 min</span>
          <button class="add-btn" aria-label="Add Chocolate Lava Cake to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Classic cheesecake" data-category="Desserts" data-price="179" data-id="cheesecake">
      <div class="food-image-wrap">
        <img class="food-image" alt="Cheesecake slice" loading="lazy" src="images/cheesecake.jpg">
        <button class="heart" aria-label="Add Classic Cheesecake to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Classic Cheesecake</h3><span class="price">₹179</span></div>
        <p class="food-desc">Creamy baked cheesecake with berry topping.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.7 · 12 min</span>
          <button class="add-btn" aria-label="Add Classic Cheesecake to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Mango smoothie" data-category="Drinks" data-price="129" data-id="mango">
      <div class="food-image-wrap">
        <img class="food-image" alt="Mango smoothie" loading="lazy" src="images/mango.jpg">
        <button class="heart" aria-label="Add Mango Smoothie to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Mango Smoothie</h3><span class="price">₹129</span></div>
        <p class="food-desc">Thick, chilled mango blended smooth.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.8 · 10 min</span>
          <button class="add-btn" aria-label="Add Mango Smoothie to cart">+</button>
        </div>
      </div>
    </article>

    <article class="food-card" data-name="Iced coffee" data-category="Drinks" data-price="139" data-id="coffee">
      <div class="food-image-wrap">
        <img class="food-image" alt="Iced coffee" loading="lazy" src="images/coffee.jpg">
        <button class="heart" aria-label="Add Iced Coffee to favourites">♡</button>
      </div>
      <div class="food-info">
        <div class="food-title-row"><h3>Iced Coffee</h3><span class="price">₹139</span></div>
        <p class="food-desc">Cold coffee over ice with a splash of milk.</p>
        <div class="food-bottom">
          <span class="food-rating"><span>★</span> 4.6 · 10 min</span>
          <button class="add-btn" aria-label="Add Iced Coffee to cart">+</button>
        </div>
      </div>
    </article>

        <div class="empty-state" id="emptyState">No dishes found. Try another search or category.</div>
      </div>
    </div>
  </section>

  <!-- Promo banner -->
  <div class="wrap">
    <div class="promo">
      <div>
        <div class="eyebrow">A LITTLE TREAT FROM US</div>
        <h2>Your first order deserves a little extra.</h2>
        <p>Enjoy a special welcome offer on your first delicious order.</p>
        <span class="code">MUSE10</span>
      </div>
      <button class="primary" data-scroll="#menu">Find your favourite ↗</button>
    </div>
  </div>

  <!-- Our story -->
  <section class="story" id="story">
    <div class="wrap story-grid">
      <img src="images/story.jpg" alt="Colourful Indian spices and herbs" loading="lazy">
      <div>
        <div class="eyebrow">OUR STORY</div>
        <h2>The Masala Muse Journey</h2>
        <p>At Masala Muse, we believe food is more than just a meal — it's an experience. Our journey started with a simple idea: to bring authentic flavours, fresh ingredients and a touch of love to your plate. From traditional favourites to modern twists, we serve dishes that make you feel at home.</p>
      </div>
    </div>
  </section>
</main>

<footer id="footer">
  <div class="wrap">
    <strong>masala muse</strong>
    <nav><a href="#home">Home</a> &nbsp;·&nbsp; <a href="#menu">Menu</a> &nbsp;·&nbsp; <a href="#story">About</a></nav>
    <a href="mailto:masalamuse@gmail.com">✉ masalamuse@gmail.com</a>
    <div class="copy">© 2026 Masala Muse. All rights reserved. Demo project – no real orders are taken.</div>
  </div>
</footer>

<!-- Dark overlay behind the cart drawer -->
<div class="overlay" id="overlay"></div>

<!-- Cart drawer with bill summary -->
<aside class="cart-drawer" id="cartDrawer" aria-label="Shopping cart" aria-modal="true" role="dialog">
  <div class="cart-head">
    <h2>Your basket <span style="color:var(--orange)" id="basketItemsLabel">(0)</span></h2>
    <button class="close-cart" id="closeCart" aria-label="Close cart">×</button>
  </div>
  <div class="cart-items" id="cartItems"><!-- filled by JavaScript --></div>
  <div class="cart-foot">
    <div class="bill-line"><span>Subtotal</span><strong id="subtotal">₹0</strong></div>
    <div class="bill-line"><span>Delivery</span><strong id="delivery">₹0</strong></div>
    <div class="bill-line total"><span>Total</span><span id="total">₹0</span></div>
    <button class="primary checkout" id="checkoutBtn" disabled>Continue to checkout →</button>
  </div>
</aside>

<!-- Checkout modal form -->
<div class="modal-backdrop" id="checkoutBackdrop">
  <form class="checkout-modal" id="checkoutForm">
    <div class="modal-top"><h2>Almost delicious.</h2>
      <button type="button" class="close-cart" id="closeModal" aria-label="Close checkout">×</button></div>
    <p>Where should we bring your order?</p>
    <label for="customerName">Your name</label>
    <input id="customerName" name="name" required placeholder="Enter your name">
    <label for="customerPhone">Phone number</label>
    <input id="customerPhone" name="phone" type="tel" required pattern="[0-9+\-\s]{10,15}"
           placeholder="10-digit phone number">
    <label for="customerAddress">Delivery address</label>
    <textarea id="customerAddress" name="address" required placeholder="House / street / area"></textarea>
    <label for="paymentMethod">Payment method</label>
    <select id="paymentMethod">
      <option>Cash on delivery</option><option>UPI (demo)</option><option>Card (demo)</option>
    </select>
    <div id="orderSummary" class="fineprint"></div>
    <button type="submit" class="primary">Place demo order · <span id="modalTotal">₹0</span></button>
    <p class="fineprint">Demo experience only — this page does not process real payments
       or send orders to a restaurant.</p>
  </form>
</div>

<!-- Toast notification -->
<div class="toast" id="toast" role="status" aria-live="polite"></div>

<script src="script.js"></script>
</body>
</html>
[28/10, 7:51 pm] Sufia: /* ---- Remaining styles (buttons, hero, sections, cart rows, forms, footer) ---- */
a{color:inherit; text-decoration:none}
button{font-family:inherit; cursor:pointer}
em{font-family:'Playfair Display',serif}
header .brand{display:flex; align-items:center; gap:9px; font-weight:800; font-size:20px; letter-spacing:-.5px}
.brand{white-space:nowrap}
.brand em{color:var(--orange); font-style:normal}
.brand-mark{display:grid; place-items:center; width:34px; height:34px; border-radius:10px; background:var(--orange); color:#fff; font-size:16px}
.navlinks{display:flex; gap:28px; font-size:13px; font-weight:700}
.navlinks a:hover{color:var(--orange)}
.nav-actions{display:flex; align-items:center; gap:10px}
.search-wrap{display:flex; align-items:center; gap:6px; background:#fff; border:1px solid var(--line); border-radius:14px; padding:0 12px; height:40px}
.search-wrap input{border:0; outline:0; background:transparent; font:inherit; font-size:13px; width:170px}
.search-wrap:focus-within{border-color:var(--orange)}
.search-icon{color:var(--muted); font-size:13px}
.cart-btn{display:flex; align-items:center; gap:8px; background:var(--ink); color:#fff; border:0; border-radius:13px; height:40px; padding:0 14px; font-weight:800; font-size:13px}
.cart-count{background:var(--orange); border-radius:999px; min-width:19px; height:19px; display:grid; place-items:center; font-size:11px}
.menu-toggle{display:none; background:#fff; border:1px solid var(--line); border-radius:12px; width:40px; height:40px; font-size:18px}

.hero{padding:52px 0 40px}
.pill{display:inline-flex; align-items:center; gap:8px; background:#e5f1ea; color:var(--green); border-radius:999px; padding:7px 13px; font-size:11px; font-weight:800; letter-spacing:.6px}
.pill:before{content:""; width:6px; height:6px; border-radius:50%; background:var(--green)}
.hero h1{font-family:'Playfair Display',serif; font-size:clamp(44px,6vw,72px); line-height:.98; letter-spacing:-2.5px; margin:22px 0 18px}
.hero h1 em{color:var(--orange)}
.hero p.lead{color:var(--muted); font-size:15px; line-height:1.7; max-width:430px}
.hero-actions{display:flex; gap:12px; margin:26px 0}
.primary,.secondary{border:1px solid transparent; border-radius:13px; padding:13px 20px; font-weight:800; font-size:14px; transition:.2s}
.secondary{background:#fff; border-color:var(--line); color:var(--ink)}
.secondary:hover{border-color:var(--ink)}
.hero-stats{display:flex; align-items:center; gap:18px; font-size:12px; color:var(--muted)}
.hero-stats strong{display:block; color:var(--ink); font-size:13px}
.stars{color:#f5a623; letter-spacing:1px}
.avatars{display:flex}
.avatars i{width:30px; height:30px; border-radius:50%; background:#f3d9c2; border:2px solid var(--cream); margin-left:-8px}
.avatars i:first-child{margin-left:0}
.hero-visual{position:relative; width:min(460px,100%); aspect-ratio:1; justify-self:center}
.hero-visual:before{content:""; position:absolute; inset:2% -3% -3% 4%; background:var(--peach); border-radius:48% 52% 45% 55%}
.hero-plate{position:absolute; inset:7%; border-radius:50%; overflow:hidden; border:10px solid #fff; box-shadow:var(--shadow)}
.hero-plate img{width:100%; height:100%; object-fit:cover}
.float-chip{position:absolute; display:flex; align-items:center; gap:10px; background:#fff; border-radius:14px; padding:10px 13px; box-shadow:0 14px 40px #6b402018; font-size:11px; color:var(--muted)}
.float-chip b{display:block; color:var(--ink); font-size:12px}
.float-chip .ico{display:grid; place-items:center; width:30px; height:30px; background:var(--peach); border-radius:9px}
.chip-a{top:9%; left:-6%} .chip-b{bottom:12%; right:-4%}

.trust{border-top:1px solid var(--line); border-bottom:1px solid var(--line); background:#fffdf9}
.trust .wrap{display:grid; grid-template-columns:repeat(4,1fr); gap:10px; padding:18px 0; font-size:12px; font-weight:700; color:#5d574f; text-align:center}

.section{padding:64px 0 36px}
.eyebrow{color:var(--orange); font-size:10px; font-weight:800; letter-spacing:1.6px}
.section h2{font-family:'Playfair Display',serif; font-size:clamp(30px,4vw,40px); margin:8px 0 6px; letter-spacing:-1px}
.section-head{display:flex; justify-content:space-between; align-items:flex-end; gap:14px; flex-wrap:wrap}
.section-head p{margin:0; color:var(--muted); font-size:13px}
.result-count{color:var(--muted); font-size:12px}
.filters{display:flex; gap:8px; flex-wrap:wrap; margin:22px 0}
.filter{background:#fff; border:1px solid var(--line); border-radius:999px; padding:9px 15px; font-size:12px; font-weight:800; transition:.2s}
.food-image-wrap{position:relative; aspect-ratio:1.5/1; overflow:hidden; background:#f3d9c2}
.tag{position:absolute; top:10px; left:10px; background:#fff; color:var(--green); font-size:9px; font-weight:800; letter-spacing:.5px; padding:5px 8px; border-radius:8px}
.heart{position:absolute; top:10px; right:10px; width:30px; height:30px; border-radius:50%; border:0; background:#fff; color:#b9aea2; font-size:15px}
.heart.liked{color:#e0383e}
.food-info{padding:14px 15px 15px}
.food-title-row{display:flex; justify-content:space-between; gap:8px; align-items:baseline}
.food-title-row h3{margin:0; font-size:14px}
.price{font-weight:800; font-size:14px}
.food-desc{color:var(--muted); font-size:11.5px; line-height:1.5; min-height:34px; margin:6px 0 12px}
.food-bottom{display:flex; justify-content:space-between; align-items:center}
.food-rating{font-size:11px; font-weight:800; color:#5d574f}
.food-rating span{color:#f5a623}
.add-btn{width:34px; height:34px; border-radius:11px; border:1px solid #f9dccc; background:var(--peach); color:var(--orange-dark); font-size:18px; font-weight:700; transition:.2s}
.empty-state{display:none; grid-column:1/-1; text-align:center; color:var(--muted); padding:40px 10px}

.promo{margin:44px auto; background:#27251f; color:#fff; border-radius:26px; padding:38px; display:flex; justify-content:space-between; align-items:center; gap:20px; flex-wrap:wrap; overflow:hidden; position:relative}
.promo .eyebrow{color:#ffb48f}
.promo h2{font-family:'Playfair Display',serif; font-size:clamp(26px,3.4vw,36px); margin:8px 0}
.promo p{margin:0 0 14px; color:#cfc8bd; font-size:13px}
.code{display:inline-block; border:1px dashed #9a9387; border-radius:9px; padding:8px 14px; font-weight:800; letter-spacing:1.5px; font-size:13px}

.story{padding:30px 0 70px}
.story-grid{display:grid; grid-template-columns:1fr 1fr; gap:34px; align-items:center}
.story-grid img{width:100%; border-radius:22px; aspect-ratio:1.6/1; object-fit:cover}
.story p{color:var(--muted); line-height:1.75; font-size:14px}

footer{background:#27251f; color:#d8d1c6; padding:34px 0; font-size:13px}
footer .wrap{display:flex; justify-content:space-between; gap:16px; flex-wrap:wrap; align-items:center}
footer a:hover{color:#fff}
.copy{width:100%; text-align:center; color:#8f887c; font-size:12px; margin-top:12px}

.cart-head,.modal-top{display:flex; justify-content:space-between; align-items:center}
.cart-head{padding:22px 22px 16px; border-bottom:1px solid var(--line)}
.cart-head h2,.modal-top h2{margin:0; font-family:'Playfair Display',serif; font-size:24px}
.close-cart{width:36px; height:36px; border-radius:11px; border:1px solid var(--line); background:#fff; font-size:20px}
.cart-items{flex:1; overflow:auto; padding:8px 22px}
.cart-empty{color:var(--muted); text-align:center; margin-top:60px; font-size:14px}
.cart-row{display:grid; grid-template-columns:56px 1fr auto; gap:12px; align-items:center; padding:14px 0; border-bottom:1px solid var(--line)}
.cart-row img{width:56px; height:56px; border-radius:12px; object-fit:cover}
.cart-row h4{margin:0 0 3px; font-size:12px}
.cart-row .unit{font-size:11px; font-weight:800}
.qty{display:flex; align-items:center; gap:7px; margin-top:6px; font-size:12px; font-weight:800}
.qty button{width:22px; height:22px; border:1px solid var(--line); background:#fff; border-radius:7px; line-height:1}
.cart-foot{padding:18px 22px 22px; border-top:1px solid var(--line)}
.bill-line{display:flex; justify-content:space-between; font-size:12px; color:var(--muted); margin-bottom:9px}
.bill-line.total{border-top:1px solid var(--line); padding-top:12px; margin-top:6px; color:var(--ink); font-weight:800; font-size:15px}
.checkout{width:100%; margin-top:10px}
.primary:disabled{opacity:.45; cursor:not-allowed; transform:none}
.checkout-modal{width:min(430px,100%); background:var(--cream); border-radius:24px; padding:24px; max-height:94dvh; overflow:auto}
.checkout-modal p{color:var(--muted); font-size:12px}
.checkout-modal label{display:block; font-size:11px; font-weight:800; margin:14px 0 6px}
.checkout-modal input,.checkout-modal textarea,.checkout-modal select{width:100%; border:1px solid var(--line); border-radius:11px; padding:11px 12px; font:inherit; font-size:13px; background:#fff}
.checkout-modal input:focus,.checkout-modal textarea:focus,.checkout-modal select:focus{outline:0; border-color:var(--orange)}
.checkout-modal textarea{min-height:76px; resize:vertical}
.checkout-modal .primary{width:100%; margin-top:14px}
.fineprint{font-size:10.5px!important; color:var(--muted); margin:12px 0 0}
@media(max-width:980px){.trust .wrap{grid-template-columns:repeat(2,1fr)} .story-grid{grid-template-columns:1fr}}
@media(max-width:760px){
  .hero{padding-top:30px}
  .hero-actions{flex-direction:column; align-items:flex-start}
  .cart-label{display:none}
  .promo{padding:26px}
  header{position:sticky}
  .navlinks{background:var(--cream); padding:14px 20px; gap:14px; border-bottom:1px solid var(--line)}
}
@media(max-width:390px){ .wrap{width:calc(100% - 28px)} .hero h1{letter-spacing:-1.5px} .food-desc{min-height:0} }

/* Colour palette and base styles */
:root{
  --ink:#24221f; --muted:#817b73; --cream:#fffaf4; --paper:#fff;
  --orange:#ed6a35; --orange-dark:#cf4f20; --peach:#fff0e5; --green:#39765b;
  --line:#eee5db; --shadow:0 14px 45px #6b40200d;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0; background:var(--cream); color:var(--ink); font-family:'DM Sans',sans-serif}
.wrap{width:min(1160px,calc(100% - 40px)); margin:auto}

/* Sticky header */
header{position:sticky; top:0; z-index:20; background:#fffaf4eF; backdrop-filter:blur(16px);
       border-bottom:1px solid #eee5dbb8}
.nav{height:78px; display:flex; align-items:center; justify-content:space-between; gap:22px}

/* Hero layout and buttons */
.hero-grid{display:grid; grid-template-columns:1.02fr .98fr; align-items:center; gap:28px}
.primary{background:var(--orange); color:white; box-shadow:0 10px 20px #ed6a352b}
.primary:hover{background:var(--orange-dark); transform:translateY(-2px)}

/* Menu grid and food card */
.menu-grid{display:grid; grid-template-columns:repeat(4,minmax(0,1fr)); gap:20px}
.food-card{background:#fff; border:1px solid #f0e7dd; border-radius:21px; overflow:hidden;
           transition:transform .25s,box-shadow .25s; position:relative}
.food-card:hover{transform:translateY(-5px); box-shadow:var(--shadow)}
.food-image{width:100%; height:100%; object-fit:cover; transition:transform .4s}
.food-card:hover .food-image{transform:scale(1.06)}
.filter:hover,.filter.active{background:var(--ink); color:white; border-color:var(--ink)}
.add-btn:hover{background:var(--orange); color:white}

/* Sliding cart drawer and dark overlay */
.cart-drawer{position:fixed; right:0; top:0; height:100dvh; width:min(430px,100%);
             background:var(--cream); z-index:51; transform:translateX(105%);
             transition:transform .3s ease; display:flex; flex-direction:column}
.cart-drawer.open{transform:translateX(0)}
.overlay{position:fixed; inset:0; background:#1d1b18a8; z-index:50; opacity:0;
         pointer-events:none; transition:opacity .25s}
.overlay.open{opacity:1; pointer-events:auto}

/* Checkout modal and toast message */
.modal-backdrop{position:fixed; inset:0; background:#1d1b18a8; z-index:70; display:none;
                place-items:center; padding:18px}
.modal-backdrop.open{display:grid}
.toast{position:fixed; bottom:24px; left:50%; transform:translate(-50%,20px); background:#272821;
       color:#fff; padding:13px 18px; border-radius:13px; z-index:60; opacity:0;
       pointer-events:none; transition:.25s}
.toast.show{opacity:1; transform:translate(-50%,0)}

/* Responsive breakpoints */
@media(max-width:980px){ .menu-grid{grid-template-columns:repeat(3,minmax(0,1fr))} }
@media(max-width:760px){
  .navlinks{display:none; position:absolute; top:68px; left:0; right:0; flex-direction:column}
  .navlinks.open{display:flex}
  .menu-toggle{display:block}
  .search-wrap{display:none}
  .hero-grid{grid-template-columns:1fr}
  .menu-grid{grid-template-columns:repeat(2,minmax(0,1fr)); gap:13px}
}
@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{scroll-behavior:auto!important; transition:none!important; animation:none!important}
}
[28/10, 7:51 pm] Sufia: // ---- State and helpers ----
const toastEl = document.getElementById('toast');
let toastTimer;
const overlay = document.getElementById('overlay');
const drawer = document.getElementById('cartDrawer');
const backdrop = document.getElementById('checkoutBackdrop');
const cart = new Map();
let activeCategory = 'All';
const grid = document.getElementById('menuGrid');
const cards = [...document.querySelectorAll('.food-card')];
const money = n => '₹' + n.toLocaleString('en-IN');

function toast(message){
  toastEl.textContent = message;
  toastEl.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => toastEl.classList.remove('show'), 2300);
}

// ---- Open / close panels ----
function openCart(){ drawer.classList.add('open'); overlay.classList.add('open'); }
function closeCart(){ drawer.classList.remove('open'); overlay.classList.remove('open'); }
function openCheckout(){
  const t = totals();
  document.getElementById('orderSummary').textContent =
    `${t.count} items · ${t.delivery ? money(t.delivery) + ' delivery' : 'Free delivery'} · Total ${money(t.total)}`;
  document.getElementById('modalTotal').textContent = money(t.total);
  backdrop.classList.add('open');
}
function closeCheckout(){ backdrop.classList.remove('open'); }

// ---- Cart logic ----
function getItem(id){
  const card = cards.find(c => c.dataset.id === id);
  return {id, name: card.dataset.name, price: Number(card.dataset.price),
          img: card.querySelector('.food-image').src};
}
function addToCart(id){
  const item = getItem(id);
  const existing = cart.get(id);
  cart.set(id, {...item, qty: (existing?.qty || 0) + 1});
  renderCart();
  toast(`${item.name} added to your basket`);
}
function changeQty(id, delta){
  const item = cart.get(id);
  if(!item) return;
  item.qty += delta;
  if(item.qty <= 0) cart.delete(id); else cart.set(id, item);
  renderCart();
}
function totals(){
  let subtotal = 0, count = 0;
  cart.forEach(i => { subtotal += i.price * i.qty; count += i.qty });
  return {subtotal, count,
          delivery: count ? (subtotal >= 499 ? 0 : 29) : 0,
          total: subtotal + (count ? (subtotal >= 499 ? 0 : 29) : 0)};
}
function renderCart(){
  const t = totals();
  document.getElementById('cartCount').textContent = t.count;
  document.getElementById('basketItemsLabel').textContent = `(${t.count})`;
  document.getElementById('subtotal').textContent = money(t.subtotal);
  document.getElementById('delivery').textContent =
    t.count ? (t.delivery ? money(t.delivery) : 'FREE') : money(0);
  document.getElementById('total').textContent = money(t.total);
  document.getElementById('checkoutBtn').disabled = !t.count;
  const holder = document.getElementById('cartItems');
  if(!cart.size){ holder.innerHTML = '<div class="cart-empty">Your basket is empty.<br>Add something delicious!</div>'; return }
  holder.innerHTML = [...cart.values()].map(i => `<div class="cart-row">
    <img src="${i.img}" alt="${i.name}">
    <div><h4>${i.name}</h4><div class="unit">${money(i.price)}</div>
      <div class="qty"><button data-id="${i.id}" data-qty="-1" aria-label="Decrease quantity">−</button>
      <span>${i.qty}</span><button data-id="${i.id}" data-qty="1" aria-label="Increase quantity">+</button></div></div>
    <strong>${money(i.price * i.qty)}</strong></div>`).join('');
}

// ---- Search and category filter ----
function filterCards(){
  const query = document.getElementById('searchInput').value.trim().toLowerCase();
  let visible = 0;
  cards.forEach(c => {
    const matchCategory = activeCategory === 'All' || c.dataset.category === activeCategory;
    const matchSearch = c.dataset.name.toLowerCase().includes(query)
      || c.querySelector('.food-desc').textContent.toLowerCase().includes(query);
    c.style.display = matchCategory && matchSearch ? '' : 'none';
    if(matchCategory && matchSearch) visible++;
  });
  document.getElementById('emptyState').style.display = visible ? 'none' : 'block';
  document.getElementById('resultCount').textContent =
    `${visible} delicious ${visible === 1 ? 'pick' : 'picks'}`;
}

// ---- Event listeners ----
grid.addEventListener('click', e => {
  const add = e.target.closest('.add-btn');
  if(add){ addToCart(add.closest('.food-card').dataset.id); return }
  const heart = e.target.closest('.heart');
  if(heart){
    heart.classList.toggle('liked');
    heart.textContent = heart.classList.contains('liked') ? '♥' : '♡';
    toast(heart.classList.contains('liked') ? 'Added to your favourites' : 'Removed from your favourites');
  }
});
document.getElementById('cartItems').addEventListener('click', e => {
  const b = e.target.closest('[data-qty]');
  if(b) changeQty(b.dataset.id, Number(b.dataset.qty));
});
document.getElementById('filters').addEventListener('click', e => {
  const b = e.target.closest('.filter');
  if(!b) return;
  document.querySelectorAll('.filter').forEach(x => x.classList.toggle('active', x === b));
  activeCategory = b.dataset.category;
  filterCards();
});
document.getElementById('searchInput').addEventListener('input', filterCards);
document.getElementById('openCart').addEventListener('click', openCart);
document.getElementById('closeCart').addEventListener('click', closeCart);
overlay.addEventListener('click', closeCart);
document.getElementById('checkoutBtn').addEventListener('click', openCheckout);
document.getElementById('closeModal').addEventListener('click', closeCheckout);
backdrop.addEventListener('click', e => { if(e.target === backdrop) closeCheckout(); });
document.getElementById('menuToggle').addEventListener('click', () =>
  document.getElementById('navlinks').classList.toggle('open'));
document.getElementById('navlinks').addEventListener('click', e => {
  if(e.target.closest('a')) document.getElementById('navlinks').classList.remove('open');
});
document.querySelectorAll('[data-scroll]').forEach(b => b.addEventListener('click', () =>
  document.querySelector(b.dataset.scroll).scrollIntoView({behavior:'smooth'})));
document.addEventListener('keydown', e => {
  if(e.key === 'Escape'){
    closeCart(); closeCheckout();
    document.getElementById('navlinks').classList.remove('open');
  }
});

// ---- Checkout: place the demo order ----
document.getElementById('checkoutForm').addEventListener('submit', e => {
  e.preventDefault();
  const name = document.getElementById('customerName').value.trim();
  if(!name) return;
  const orderNo = 'MM' + Math.floor(10000 + Math.random() * 90000);
  cart.clear(); renderCart(); closeCheckout(); closeCart(); e.target.reset();
  toast(`Thanks, ${name}! Demo order ${orderNo} placed`);
});
renderCart();
filterCards();
