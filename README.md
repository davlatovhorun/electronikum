<!DOCTYPE html>
<html lang="ru">
<head> 
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="google-site-verification" content="WlCTcTOwwWr-x6Iy6HqiBJ3XeW-ncZumkvalxS6WhQo" />
  <title>Электроникум — Магазин современной электроники</title>
  <meta name="description" content="Электроникум — ноутбуки, смартфоны, наушники, телевизоры и аксессуары. Быстрая консультация и честные цены." />
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">

  <!-- JSON-LD (SEO) -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "ElectronicsStore",
    "name": "Электроникум",
    "telephone": "+992919222766",
    "address": {
      "@type": "PostalAddress",
      "addressCountry": "TJ"
    },
    "url": "https://example.com/",
    "image": "https://www.iphones.ru/wp-content/uploads/2023/10/IMG_1263.jpeg"
  }
  </script>

  <style>
    :root{
      --bg:#f8fafc; --card:#ffffff; --text:#0f172a; --muted:#475569; --brand:#2563eb; --ring:#93c5fd; --shadow:0 10px 25px rgba(2,6,23,.08);
    }
    *{box-sizing:border-box;}
    html,body{margin:0;padding:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,"Noto Sans",sans-serif;color:var(--text);background:var(--bg);}
    header{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.8);backdrop-filter:blur(8px);border-bottom:1px solid #e2e8f0;}
    .container{max-width:1200px;margin:0 auto;padding:16px;}
    .topbar{display:flex;align-items:center;gap:16px;justify-content:space-between;}
    .brand{display:flex;align-items:center;gap:12px;}
    .brand h1{font-size:20px;margin:0;}
    .brand small{color:var(--muted);}
    nav a{display:inline-block;padding:8px 12px;border-radius:999px;text-decoration:none;color:var(--text);font-weight:600;}
    nav a:hover, nav a:focus{outline:none;background:#e2e8f0;}
    .controls{display:flex;gap:10px;flex-wrap:wrap;margin-top:10px;}
    .input, select{width:100%;max-width:280px;padding:10px 12px;border:1px solid #e2e8f0;border-radius:12px;background:#fff;}
    .btn{appearance:none;border:1px solid #e2e8f0;background:var(--card);padding:10px 14px;border-radius:12px;font-weight:600;cursor:pointer;}
    .btn:hover{box-shadow:var(--shadow);}
    .btn.primary{background:var(--brand);color:white;border-color:var(--brand);}
    .badge{display:inline-block;background:#eef2ff;color:#3730a3;border:1px solid #c7d2fe;padding:2px 8px;border-radius:999px;font-size:12px;}
    .products{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;margin-top:18px;}
    .product{background:var(--card);border:1px solid #e2e8f0;border-radius:18px;box-shadow:var(--shadow);padding:12px;cursor:pointer;display:flex;flex-direction:column;transition:transform .15s ease;}
    .product:focus,.product:hover{transform:translateY(-2px);outline:2px solid var(--ring);}
    .product img{width:100%;height:160px;object-fit:cover;border-radius:12px;background:#f1f5f9;}
    .product h3{margin:10px 0 6px 0;font-size:16px;}
    .product p{font-size:14px;color:#555;margin:0;}
    .price-row{display:flex;align-items:center;justify-content:space-between;margin-top:10px;}
    .price{font-weight:700;}
    .modal{position:fixed;inset:0;background:rgba(2,6,23,.5);display:none;align-items:center;justify-content:center;padding:16px;}
    .modal[aria-hidden="false"]{display:flex;}
    .modal-content{background:var(--card);border-radius:20px;max-width:560px;width:100%;padding:20px;border:1px solid #e2e8f0;box-shadow:var(--shadow);}
    .modal-header{display:flex;justify-content:space-between;align-items:center;gap:8px;}
    .close{border:none;background:transparent;font-size:28px;line-height:1;cursor:pointer;}
    .modal-body{display:grid;grid-template-columns:160px 1fr;gap:16px;margin-top:10px;}
    .modal-body img{width:160px;height:160px;object-fit:cover;border-radius:12px;}
    footer{margin-top:40px;border-top:1px solid #e2e8f0;background:#fff;}
    footer .container{display:grid;gap:6px;}
    .muted{color:var(--muted);}
    .dark{--bg:#0b1220;--card:#0f172a;--text:#e5e7eb;--muted:#94a3b8;--brand:#60a5fa;--ring:#1d4ed8;border-color:#1f2937;}
    .dark header{background:rgba(15,23,42,.6);border-bottom-color:#1f2937;}
    .dark .product{border-color:#1f2937;}
    .dark .input,.dark select{background:#0f172a;border-color:#1f2937;color:var(--text);}
  </style>
</head>
<body>
  <header>
    <div class="container">
      <div class="topbar">
        <div class="brand" aria-label="Электроникум">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M4 7h16M4 12h16M4 17h10" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
          <div><h1>Электроникум</h1><small>Магазин современной электроники</small></div>
        </div>
        <nav aria-label="Основная навигация">
          <a href="#products">Товары</a>
          <a href="#about">О нас</a>
          <a href="#contacts">Контакты</a>
        </nav>
      </div>

      <div class="controls" role="region" aria-label="Панель поиска и фильтров">
        <input id="search" class="input" type="search" placeholder="Поиск по названию…" aria-label="Поиск" />
        <select id="category" aria-label="Категории">
          <option value="">Все категории</option>
          <option value="laptop">Ноутбуки</option>
          <option value="tablet">Планшеты</option>
          <option value="tv">Телевизоры</option>
          <option value="audio">Аудио</option>
          <option value="phone">Смартфоны</option>
          <option value="accessory">Аксессуары</option>
          <option value="console">Игровые приставки</option>
          <option value="home">Техника для дома</option>
          <option value="pc">ПК/Комплектующие</option>
        </select>
        <select id="sort" aria-label="Сортировка">
          <option value="default">Сортировка</option>
          <option value="price-asc">Цена: по возрастанию</option>
          <option value="price-desc">Цена: по убыванию</option>
          <option value="name-asc">Название: А→Я</option>
          <option value="name-desc">Название: Я→А</option>
        </select>
        <button id="currency-toggle" class="btn" type="button" aria-pressed="false" title="Переключить валюту">₽</button>
        <button id="theme-toggle" class="btn" type="button" aria-pressed="false" title="Темная тема">🌓</button>
      </div>
    </div>
  </header>

  <main class="container" id="products">
    <section class="products" id="grid" aria-live="polite"></section>
    <section id="about" style="margin-top:36px">
      <h2>О нас</h2>
      <p class="muted">Мы помогаем подобрать технику для учебы, работы и отдыха. Консультируем, даём гарантию и поддерживаем после покупки.</p>
    </section>
    <section id="contacts" style="margin-top:24px">
      <h2>Контакты</h2>
      <p>Телефон: <a href="tel:+992919222766">+992 919 222 766</a> | <a href="tel:+992555551018">+992 555 551 018</a></p>
      <form id="form" class="controls" onsubmit="event.preventDefault(); alert('Спасибо! Мы свяжемся с вами.'); this.reset();">
        <input class="input" required placeholder="Ваше имя" />
        <input class="input" type="tel" required placeholder="Телефон" />
        <button class="btn primary" type="submit">Отправить</button>
      </form>
    </section>
  </main>

  <div id="modal" class="modal" role="dialog" aria-modal="true" aria-hidden="true" aria-labelledby="modal-title">
    <div class="modal-content">
      <div class="modal-header">
        <h2 id="modal-title"></h2>
        <button class="close" aria-label="Закрыть" onclick="closeModal()">×</button>
      </div>
      <div class="modal-body">
        <img id="modal-image" alt="Изображение товара" />
        <div>
          <p id="modal-desc" class="muted"></p>
          <div class="price-row">
            <span id="modal-price" class="price"></span>
            <button class="btn primary" onclick="alert('Добавлено в корзину')">В корзину</button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <footer>
    <div class="container">
      <p class="muted">© 2025 Электроникум. Все права защищены.</p>
      <p class="muted">Телефон: +992 919 222 766 | +992 555 551 018</p>
    </div>
  </footer>

  <script>
    const products = [
      {title:'MacBook', cat:'laptop', priceRUB:75000_00, desc:'Мощный ноутбук с Retina-дисплеем и процессором Apple M1.', img:'https://www.iphones.ru/wp-content/uploads/2023/10/IMG_1263.jpeg'},
      {title:'Планшет Samsung', cat:'tablet', priceRUB:30000_00, desc:'Универсальный планшет с ярким экраном и поддержкой S Pen.', img:'https://www.cifrus.ru/photos/little/samsung/samsung-galaxy-tab-s10-fe-plus-x628-12-256gb-5g-grey-global-1.jpg'},
      {title:'Телевизор LG', cat:'tv', priceRUB:60000_00, desc:'Смарт-ТВ с 4K разрешением и поддержкой HDR10.', img:'https://s2-techtudo.glbimg.com/ycKlM1DtsKLW8_Yqucso5ogw72o=/0x0:750x480/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_08fbf48bc0524877943fe86e43087e7a/internal_photos/bs/2021/B/a/wpDXATS5ipnuIcyUjO9Q/2012-10-18-large01.jpeg'}
    ];

    const grid = document.getElementById('grid');
    const searchInput = document.getElementById('search');
    const categorySelect = document.getElementById('category');
    const sortSelect = document.getElementById('sort');
    const currencyToggle = document.getElementById('currency-toggle');
    const themeToggle = document.getElementById('theme-toggle');

    let currency = 'RUB';
    const RATE_RUB_TO_TJS = 0.13;

    const formatPrice = (rubCents) => {
      if(currency==='RUB'){
        return new Intl.NumberFormat('ru-RU', {style:'currency', currency:'RUB'}).format(rubCents/100);
      } else {
        const tjs = (rubCents/100) * RATE_RUB_TO_TJS;
        return new Intl.NumberFormat('ru-RU', {style:'currency', currency:'TJS'}).format(tjs);
      }
    }

    function mapCat(c){
      return {laptop:'Ноутбуки', tablet:'Планшеты', tv:'Телевизоры', audio:'Аудио', phone:'Смартфоны', accessory:'Аксессуары', console:'Приставки', home:'Для дома', pc:'ПК'}[c] || 'Другое';
    }

    function productCard(p){
      const el = document.createElement('article');
      el.className = 'product'; el.tabIndex = 0;
      el.setAttribute('data-title', p.title.toLowerCase());
      el.setAttribute('data-cat', p.cat);
      el.setAttribute('data-price', p.priceRUB);
      el.innerHTML = `
        <img loading="lazy" src="${p.img}" alt="${p.title}"/>
        <h3>${p.title}</h3>
        <p class="muted">${p.desc}</p>
        <div class="price-row">
          <span class="price">${formatPrice(p.priceRUB)}</span>
          <span class="badge">${mapCat(p.cat)}</span>
        </div>
      `;
      el.addEventListener('click', ()=> showPrice(p));
      el.addEventListener('keypress', (e)=> { if(e.key==='Enter') showPrice(p); });
      return el;
    }

    function render(list){
      grid.innerHTML = '';
      list.forEach(p=> grid.appendChild(productCard(p)));
      if(list.length===0){
        const empty = document.createElement('p');
        empty.className='muted';
        empty.textContent='Ничего не найдено. Уточните запрос или сбросьте фильтры.';
        grid.appendChild(empty);
      }
    }

    function applyFilters(){
      const q = searchInput.value.trim().toLowerCase();
      const cat = categorySelect.value;
      let list = products.filter(p => (!q || p.title.toLowerCase().includes(q)) && (!cat || p.cat===cat));
      switch(sortSelect.value){
        case 'price-asc': list.sort((a,b)=>a.priceRUB-b.priceRUB); break;
        case 'price-desc': list.sort((a,b)=>b.priceRUB-a.priceRUB); break;
        case 'name-asc': list.sort((a,b)=>a.title.localeCompare(b.title, 'ru')); break;
        case 'name-desc': list.sort((a,b)=>b.title.localeCompare(a.title, 'ru')); break;
      }
      render(list);
    }

    render(products);
    searchInput.addEventListener('input', applyFilters);
    categorySelect.addEventListener('change', applyFilters);
    sortSelect.addEventListener('change', applyFilters);

    currencyToggle.addEventListener('click', ()=>{
      currency = currency==='RUB' ? 'TJS' : 'RUB';
      currencyToggle.textContent = currency==='RUB' ? '₽' : 'SM';
      applyFilters();
    });

    const root = document.documentElement;
    if(localStorage.getItem('theme')==='dark'){ root.classList.add('dark'); themeToggle.setAttribute('aria-pressed','true'); }
    themeToggle.addEventListener('click',()=>{
      const isDark = root.classList.toggle('dark');
      themeToggle.setAttribute('aria-pressed', String(isDark));
      localStorage.setItem('theme', isDark?'dark':'light');
    });

    const modal = document.getElementById('modal');
    const mTitle = document.getElementById('modal-title');
    const mDesc  = document.getElementById('modal-desc');
    const mPrice = document.getElementById('modal-price');
    const mImg   = document.getElementById('modal-image');

    function showPrice(p){
      mTitle.textContent = p.title;
      mDesc.textContent = p.desc;
      mPrice.textContent = formatPrice(p.priceRUB);
      mImg.src = p.img; mImg.alt = p.title;
      modal.setAttribute('aria-hidden','false'); modal.style.display='flex';
      document.body.style.overflow='hidden';
    }

    function closeModal(){
      modal.setAttribute('aria-hidden','true'); modal.style.display='none';
      document.body.style.overflow='auto';
    }

    window.closeModal = closeModal;
    modal.addEventListener
