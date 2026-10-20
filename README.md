<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>امیرمارکت | فروشگاه اینترنتی</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --red: #ef394e;
    --dark: #232933;
    --gray: #f1f2f4;
    --white: #ffffff;
    --text: #333;
}

body {
    font-family: Tahoma, Arial, sans-serif;
    background: #f5f5f5;
    color: var(--text);
}

button, input, select {
    font-family: inherit;
}

button {
    cursor: pointer;
}

.top-banner {
    background: linear-gradient(90deg, #ef394e, #c91d3c);
    color: white;
    text-align: center;
    padding: 12px;
    font-size: 13px;
}

.header {
    background: white;
    padding: 18px 5%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 18px;
    flex-wrap: wrap;
    border-bottom: 1px solid #eee;
}

.logo {
    font-size: 25px;
    font-weight: bold;
    color: var(--red);
    white-space: nowrap;
}

.logo span {
    color: #333;
}

.search-box {
    flex: 1;
    min-width: 180px;
    max-width: 600px;
    display: flex;
    background: #f1f2f4;
    border-radius: 10px;
    overflow: hidden;
}

.search-box input {
    width: 100%;
    border: none;
    outline: none;
    background: transparent;
    padding: 15px;
    font-size: 13px;
}

.search-box button {
    background: transparent;
    border: none;
    padding: 0 15px;
    font-size: 20px;
}

.header-actions {
    display: flex;
    gap: 10px;
}

.header-actions button {
    padding: 11px 14px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background: white;
    font-size: 12px;
}

.header-actions .cart-btn {
    border-color: var(--red);
    color: var(--red);
}

.navbar {
    background: white;
    padding: 15px 5%;
    display: flex;
    gap: 28px;
    overflow-x: auto;
    white-space: nowrap;
    border-bottom: 1px solid #eee;
}

.navbar a {
    color: #555;
    text-decoration: none;
    font-size: 13px;
}

.navbar a:hover {
    color: var(--red);
}

.container {
    width: 92%;
    max-width: 1250px;
    margin: 25px auto;
}

.hero {
    background: linear-gradient(135deg, #252b39, #4b2636);
    color: white;
    border-radius: 18px;
    padding: 42px 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    min-height: 220px;
}

.hero h1 {
    font-size: 27px;
    margin-bottom: 15px;
    line-height: 1.8;
}

.hero p {
    color: #ddd;
    font-size: 14px;
    line-height: 2;
}

.hero .hero-icon {
    font-size: 75px;
}

.hero button {
    margin-top: 20px;
    background: var(--red);
    color: white;
    border: none;
    border-radius: 8px;
    padding: 13px 22px;
}

.section-title {
    font-size: 19px;
    margin: 32px 0 20px;
}

.categories {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 14px;
}

.category {
    background: white;
    border-radius: 12px;
    padding: 22px 10px;
    text-align: center;
    cursor: pointer;
    transition: .2s;
    border: 1px solid #eee;
}

.category:hover {
    transform: translateY(-4px);
    border-color: var(--red);
}

.category .icon {
    font-size: 32px;
    margin-bottom: 12px;
}

.category p {
    font-size: 12px;
}

.products {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 15px;
}

.product {
    background: white;
    border: 1px solid #eee;
    border-radius: 12px;
    padding: 18px;
    transition: .2s;
}

.product:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px #0000000c;
}

.product-icon {
    height: 115px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 60px;
    background: #f8f8f8;
    border-radius: 10px;
    margin-bottom: 15px;
}

.product h3 {
    font-size: 13px;
    line-height: 2;
    height: 52px;
    overflow: hidden;
}

.product .description {
    color: #888;
    font-size: 11px;
    margin: 8px 0 15px;
}

.price {
    font-size: 15px;
    font-weight: bold;
    margin: 12px 0;
}

.price span {
    font-size: 11px;
    font-weight: normal;
}

.add-btn {
    width: 100%;
    border: none;
    background: var(--red);
    color: white;
    border-radius: 8px;
    padding: 12px 5px;
    font-size: 12px;
}

.add-btn:hover {
    background: #d92740;
}

.no-results {
    grid-column: 1 / -1;
    background: white;
    padding: 35px;
    border-radius: 12px;
    text-align: center;
    line-height: 2;
}

footer {
    margin-top: 50px;
    background: #232933;
    color: white;
    padding: 35px 5%;
    text-align: center;
    line-height: 2.5;
}

footer p {
    color: #bbb;
    font-size: 12px;
}

.cart-panel {
    display: none;
    position: fixed;
    inset: 0;
    background: #0008;
    z-index: 100;
    justify-content: center;
    align-items: center;
    padding: 15px;
}

.cart-content {
    background: white;
    width: 100%;
    max-width: 480px;
    max-height: 85vh;
    overflow-y: auto;
    padding: 25px;
    border-radius: 15px;
}

.cart-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.close-btn {
    background: #eee;
    border: none;
    padding: 8px 12px;
    border-radius: 8px;
}

.cart-item {
    padding: 15px 0;
    border-bottom: 1px solid #eee;
    display: flex;
    justify-content: space-between;
    gap: 10px;
    font-size: 12px;
    line-height: 2;
}

.cart-item button {
    border: none;
    background: #ffe8eb;
    color: #d92740;
    padding: 5px 8px;
    border-radius: 5px;
}

.cart-total {
    margin: 20px 0;
    font-weight: bold;
    line-height: 2;
}

.empty-cart {
    text-align: center;
    padding: 30px 0;
    color: #888;
}

@media (max-width: 850px) {
    .products {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .categories {
        grid-template-columns: repeat(3, 1fr);
    }

    .hero h1 {
        font-size: 21px;
    }

    .hero .hero-icon {
        font-size: 50px;
    }
}

@media (max-width: 480px) {
    .header {
        padding: 15px 4%;
    }

    .logo {
        font-size: 21px;
    }

    .header-actions button {
        padding: 9px;
    }

    .categories {
        grid-template-columns: repeat(2, 1fr);
    }

    .hero {
        padding: 25px 18px;
    }

    .hero .hero-icon {
        display: none;
    }

    .product {
        padding: 12px;
    }

    .product-icon {
        height: 90px;
        font-size: 45px;
    }

    .product h3 {
        font-size: 12px;
    }

    .price {
        font-size: 12px;
    }
}
</style>
</head>

<body>

<div class="top-banner">
    🎉 امیرمارکت؛ خریدی آسان، سریع و مطمئن
</div>

<header class="header">

    <div class="logo">امیر<span>مارکت</span> 🛍️</div>

    <div class="search-box">
        <input id="searchInput"
               type="search"
               placeholder="جست‌وجوی محصولات..."
               oninput="renderProducts()">
        <button onclick="renderProducts()">🔍</button>
    </div>

    <div class="header-actions">
        <button onclick="alert('این نسخه نمایشی است و ورود کاربران هنوز فعال نیست.')">
            👤 ورود
        </button>

        <button class="cart-btn" onclick="openCart()">
            🛒 سبد خرید <span id="cartCount">۰</span>
        </button>
    </div>

</header>

<nav class="navbar">
    <a href="#categories">دسته‌بندی کالاها</a>
    <a href="#products">همه محصولات</a>
    <a href="#offers">پیشنهادهای ویژه</a>
    <a href="#about">درباره ما</a>
</nav>

<main class="container">

    <section class="hero">
        <div>
            <h1>به دنیای خرید آنلاین خوش آمدید! ✨</h1>
            <p>
                محصولات متنوع، تجربه خرید ساده و یک فروشگاه مدرن
                برای انتخاب‌های بهتر.
            </p>
            <button onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">
                مشاهده محصولات ←
            </button>
        </div>

        <div class="hero-icon">🛍️</div>
    </section>

    <section id="categories">
        <h2 class="section-title">دسته‌بندی محصولات</h2>

        <div class="categories">
            <div class="category" onclick="filterCategory('موبایل')">
                <div class="icon">📱</div>
                <p>موبایل</p>
            </div>

            <div class="category" onclick="filterCategory('لپ‌تاپ')">
                <div class="icon">💻</div>
                <p>لپ‌تاپ</p>
            </div>

            <div class="category" onclick="filterCategory('هدفون')">
                <div class="icon">🎧</div>
                <p>هدفون</p>
            </div>

            <div class="category" onclick="filterCategory('ساعت')">
                <div class="icon">⌚</div>
                <p>ساعت هوشمند</p>
            </div>

            <div class="category" onclick="filterCategory('لوازم جانبی')">
                <div class="icon">🔌</div>
                <p>لوازم جانبی</p>
            </div>
        </div>
    </section>

    <section id="offers">
        <h2 class="section-title">🔥 پیشنهادهای ویژه</h2>
        <div class="products" id="featuredProducts"></div>
    </section>

    <section id="products">
        <h2 class="section-title">🛒 همه محصولات</h2>
        <div class="products" id="productList"></div>
    </section>

</main>

<footer id="about">
    <h2>امیرمارکت 🛍️</h2>
    <p>فروشگاه اینترنتی مدرن شما</p>
    <p>این نسخه نمایشی است و هنوز به درگاه پرداخت یا سیستم ارسال متصل نیست.</p>
    <p>ساخته شده با ❤️ توسط امیرپژواک</p>
    <p>© تمامی حقوق محفوظ است.</p>
</footer>

<div class="cart-panel" id="cartPanel" onclick="outsideCart(event)">
    <div class="cart-content">

        <div class="cart-header">
            <h3>🛒 سبد خرید شما</h3>
            <button class="close-btn" onclick="closeCart()">بستن ✕</button>
        </div>

        <div id="cartItems"></div>

        <div class="cart-total" id="cartTotal"></div>

        <button class="add-btn" onclick="checkout()">
            ادامه خرید
        </button>

    </div>
</div>

<script>
const products = [
    {
        id: 1,
        name: "گوشی موبایل هوشمند",
        category: "موبایل",
        icon: "📱",
        price: 18500000,
        description: "یک انتخاب جذاب برای استفاده روزمره",
        featured: true
    },
    {
        id: 2,
        name: "لپ‌تاپ حرفه‌ای",
        category: "لپ‌تاپ",
        icon: "💻",
        price: 42500000,
        description: "مناسب کار، درس و سرگرمی",
        featured: true
    },
    {
        id: 3,
        name: "هدفون بی‌سیم",
        category: "هدفون",
        icon: "🎧",
        price: 1850000,
        description: "طراحی مدرن و استفاده آسان",
        featured: true
    },
    {
        id: 4,
        name: "ساعت هوشمند",
        category: "ساعت",
        icon: "⌚",
        price: 2750000,
        description: "همراه هوشمند فعالیت‌های روزانه",
        featured: true
    },
    {
        id: 5,
        name: "شارژر سریع",
        category: "لوازم جانبی",
        icon: "🔌",
        price: 450000,
        description: "وسیله کاربردی برای شارژ دستگاه",
        featured: false
    },
    {
        id: 6,
        name: "تبلت دیجیتال",
        category: "لوازم جانبی",
        icon: "📟",
        price: 12800000,
        description: "مناسب مطالعه و سرگرمی",
        featured: false
    },
    {
        id: 7,
        name: "اسپیکر بلوتوثی",
        category: "لوازم جانبی",
        icon: "🔊",
        price: 1200000,
        description: "موسیقی در هر زمان و مکان",
        featured: false
    },
    {
        id: 8,
        name: "موس بی‌سیم",
        category: "لوازم جانبی",
        icon: "🖱️",
        price: 380000,
        description: "طراحی ساده و کاربردی",
        featured: false
    }
];

let cart = [];
let selectedCategory = "";

const formatPrice = price =>
    new Intl.NumberFormat("fa-IR").format(price) + " تومان";

function createProductCard(product) {
    return `
        <article class="product">
            <div class="product-icon">${product.icon}</div>
            <h3>${product.name}</h3>
            <p class="description">${product.description}</p>
            <div class="price">${formatPrice(product.price)}</div>
            <button class="add-btn" onclick="addToCart(${product.id})">
                افزودن به سبد خرید +
            </button>
        </article>
    `;
}

function renderProducts() {
    const query = document.getElementById("searchInput")
        .value.trim().toLowerCase();

    const filtered = products.filter(product => {
        const matchesSearch =
            product.name.toLowerCase().includes(query) ||
            product.category.toLowerCase().includes(query);

        const matchesCategory =
            !selectedCategory || product.category === selectedCategory;

        return matchesSearch && matchesCategory;
    });

    document.getElementById("productList").innerHTML =
        filtered.length
            ? filtered.map(createProductCard).join("")
            : '<div class="no-results">محصولی پیدا نشد! 🔍<br>عبارت دیگری جست‌وجو کنید.</div>';

    const featured = filtered.filter(product => product.featured);

    document.getElementById("featuredProducts").innerHTML =
        featured.length
            ? featured.map(createProductCard).join("")
            : '<div class="no-results">پیشنهاد ویژه‌ای برای این جست‌وجو وجود ندارد.</div>';
}

function filterCategory(category) {
    selectedCategory = selectedCategory === category ? "" : category;

    document.getElementById("searchInput").value = "";

    renderProducts();

    document.getElementById("products")
        .scrollIntoView({ behavior: "smooth" });
}

function addToCart(id) {
    const product = products.find(item => item.id === id);
    const existing = cart.find(item => item.id === id);

    if (existing) {
        existing.quantity++;
    } else {
        cart.push({ ...product, quantity: 1 });
    }

    updateCart();
    alert("محصول به سبد خرید اضافه شد! 🛒");
}

function updateCart() {
    const count = cart.reduce((sum, item) => sum + item.quantity, 0);

    document.getElementById("cartCount").textContent =
        new Intl.NumberFormat("fa-IR").format(count);

    const cartItems = document.getElementById("cartItems");

    if (cart.length === 0) {
        cartItems.innerHTML =
            '<div class="empty-cart">سبد خرید شما خالی است 🛒</div>';

        document.getElementById("cartTotal").textContent = "";
        return;
    }

    cartItems.innerHTML = cart.map(item => `
        <div class="cart-item">
            <div>
                <strong>${item.icon} ${item.name}</strong><br>
                ${formatPrice(item.price)} ×
                ${new Intl.NumberFormat("fa-IR").format(item.quantity)}
            </div>

            <button onclick="removeFromCart(${item.id})">
                حذف
            </button>
        </div>
    `).join("");

    const total = cart.reduce(
        (sum, item) => sum + item.price * item.quantity, 0
    );

    document.getElementById("cartTotal").textContent =
        "مجموع: " + formatPrice(total);
}

function removeFromCart(id) {
    cart = cart.filter(item => item.id !== id);
    updateCart();
}

function openCart() {
    updateCart();
    document.getElementById("cartPanel").style.display = "flex";
}

function closeCart() {
    document.getElementById("cartPanel").style.display = "none";
}

function outsideCart(event) {
    if (event.target.id === "cartPanel") {
        closeCart();
    }
}

function checkout() {
    if (cart.length === 0) {
        alert("سبد خرید شما خالی است!");
        return;
    }

    alert(
        "این نسخه نمایشی است؛ برای ثبت سفارش واقعی باید سیستم سفارش‌گیری و پرداخت راه‌اندازی شود."
    );
}

renderProducts();
updateCart();
</script>

</body>
</html>
