<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Чудеса — Магазин Электроники</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      background: #f4f4f9;
      color: #333;
    }
    header {
      background: linear-gradient(90deg, #1e3c72, #2a5298);
      color: white;
      text-align: center;
      padding: 20px 0;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    header h1 {
      margin: 0;
      font-size: 2.5rem;
      letter-spacing: 2px;
      animation: fadeIn 1s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px);}
      to { opacity: 1; transform: translateY(0);}
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .product {
      background: white;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .product:hover {
      transform: translateY(-10px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .product img {
      width: 100%;
      height: 150px;
      object-fit: contain;
      transition: transform 0.5s;
    }
    .product:hover img {
      transform: scale(1.05);
    }
    .product h3 {
      text-align: center;
      padding: 10px;
      font-size: 1.1rem;
      color: #1e3c72;
    }
    .modal {
      display: none;
      position: fixed;
      z-index: 10;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.6);
      animation: fadeIn 0.5s;
    }
    .modal-content {
      background: #fff;
      margin: 10% auto;
      padding: 20px;
      border-radius: 15px;
      width: 90%;
      max-width: 400px;
      text-align: center;
      position: relative;
      animation: slideIn 0.5s;
    }
    .close {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 1.5rem;
      cursor: pointer;
      color: #333;
    }
    @keyframes slideIn {
      from { transform: translateY(-50px); opacity: 0;}
      to { transform: translateY(0); opacity: 1;}
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #1e3c72;
      color: white;
    }
    /* Кнопки валюты */
    .currency-switch {
      position: fixed;
      top: 10px;
      right: 10px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
      padding: 10px;
      display: flex;
      gap: 5px;
      z-index: 100;
    }
    .currency-switch button {
      padding: 5px 10px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
      background: #1e3c72;
      color: white;
      font-weight: bold;
      transition: 0.3s;
    }
    .currency-switch button:hover {
      background: #2a5298;
    }
  </style>
</head>
<body>
  <header>
    <h1>AYTO PARKING</h1>
  </header>

  <!-- Переключатель валют -->
  <div class="currency-switch">
    <button onclick="setCurrency('RUB')">₽</button>
    <button onclick="setCurrency('USD')">$</button>
    <button onclick="setCurrency('EUR')">€</button>
  </div>

  <main>
    <section class="products">
      <!-- ВСЕ твои машины сохранены -->
      <div class="product" onclick="showPrice('MERCEDES-BENZ', '3 450 000 ₽')">
  <img src="https://b4051664-be9e-4979-89c4-770444c116cd.selcdn.net/media/common/model_gallery_preview_large/tradeins.space/uploads/photo/12490876/9cd188f49b2401ed1ccbb913aaf3af30.png?v131" alt="MERCEDES-BENZ">
  <h3>MERCEDES-BENZ</h3>
  <p>Немецкий автомобиль премиум-класса с комфортным салоном и надежной инженерией.</p>
</div>

<div class="product" onclick="showPrice('BMW X5', '6 330 000 ₽')">
  <img src="https://apiweb.rolf.ru/storage/thumbnails/large/models/14-bmw/4921-x5_new/f47fe6ea0e935587c7db4f55ba139286.png" alt="BMW X5">
  <h3>BMW X5</h3>
  <p>Мощный внедорожник с динамичной управляемостью, современными технологиями и просторным салоном.</p>
</div>

<div class="product" onclick="showPrice('Toyota Camry', '4 150 000 ₽')">
  <img src="https://www.avtogermes.ru/images/marks/toyota/camry/viii-xv70-restajling/colors/_1/toyota-camry-ix-xv80-china-market-belyj-metallik.67d8792aa249cb7ace5bf3827ecfea09.png" alt="Toyota Camry">
  <h3>Toyota Camry</h3>
  <p>Надежный и экономичный седан с удобным салоном и современными системами безопасности.</p>
</div>

<div class="product" onclick="showPrice('LEXUS LX', '21 150 000 ₽')">
  <img src="https://autopremiumgroup.ru/m/_versions/catalog/autos/2023/lexus_lx_2023_vnedorozhnik_5dv/600_ultra_luxury/lx600_ultra_luxury_2023_atomic_silver_image_series.jpg" alt="LEXUS LX">
  <h3>LEXUS LX</h3>
  <p>Роскошный внедорожник с премиальными материалами, мощным двигателем и высоким уровнем комфорта.</p>
</div>

<div class="product" onclick="showPrice('BMW M5', '20 400 000 ₽')">
  <img src="https://prod.cosy.bmw.cloud/bmwweb/cosySec?COSY-EU-100-7331cqgv2Z7d%25i02uCaY3MuO2kOHUtWPfbYfy91T10tLhu1XzWVo7puMLWFmdkAj5DOP4tFhZ8XgY1nTNIowJ4HO3zkyXq%25sGM8snpq6v6ODubLz2aKqfkoQjmB2fJj5DOP5Eagd%25kcWExHWpbl8FO2k3Hy2o24LEbTQLXg7AF3D%25zhrLGwg6QuiVpRBhSU" alt="BMW M5">
  <h3>BMW M5</h3>
  <p>Высокопроизводительный спортивный седан с точной управляемостью и мощным двигателем.</p>
</div>

<div class="product" onclick="showPrice('Kia Sportage', '4 000 000 ₽')">
  <img src="https://www.avtogermes.ru/images/marks/kia/sportage/v/colors/swp/kia-sportage-v-belyj-perlamutr.714195e1a04160fe58e132b336e8fdb5.png" alt="Kia Sportage">
  <h3>Kia Sportage</h3>
  <p>Компактный кроссовер с современным дизайном, удобным салоном и экономичным двигателем.</p>
</div>

<div class="product" onclick="showPrice('LADA Vesta', '2 000 000 ₽')">
  <img src="https://www.avtogermes.ru/images/generations/preview/lada-vesta-i-restajling.ce01d9961351de4986bf1f4ecf8d9087.png" alt="LADA Vesta">
  <h3>LADA Vesta</h3>
  <p>Доступный и практичный седан с современными функциями и надежной конструкцией.</p>
</div>

<div class="product" onclick="showPrice('Hyundai Palisade', '5 000 000 ₽')">
  <img src="https://avatars.mds.yandex.net/get-autoru-vos/2134599/b5a68334304a3e441f37a4424662efec/456x342" alt="Hyundai Palisade">
  <h3>Hyundai Palisade</h3>
  <p>Просторный внедорожник с современными технологиями и высоким уровнем комфорта для всей семьи.</p>
</div>

<div class="product" onclick="showPrice('Range Rover', '10 000 000 ₽')">
  <img src="https://media.cdn-jaguarlandrover.com/api/v2/images/107596/w/680.jpg" alt="Range Rover">
  <h3>Range Rover</h3>
  <p>Элегантный и мощный внедорожник с премиальными материалами и отличной проходимостью.</p>
</div>

<div class="product" onclick="showPrice('Opel Astra Sports Tourer', '3 000 000 ₽')">
  <img src="https://res.cloudinary.com/finn-auto/image/fetch/q_auto,f_auto,c_auto,dpr_2,w_720/https://dataops-nocodb-s3-bucket-production.s3.eu-central-1.amazonaws.com/nc/uploads/noco/fleet_blue_dragon/car_images/image/D9E4hj.png" alt="Opel Astra Sports Tourer">
  <h3>Opel Astra Sports Tourer</h3>
  <p>Универсальный семейный автомобиль с экономичным двигателем и практичным салоном.</p>
</div>

<div class="product" onclick="showPrice('Audi Q7', '7 500 000 ₽')">
  <img src="https://a3381f52-5e9a-4db6-babe-4d7b4a71b25f.selcdn.net/media/common/model_gallery_preview_large/tradeins.space/uploads/photo/6861241/zie4zc%20(2).jpeg?v239" alt="Audi Q7">
  <h3>Audi Q7</h3>
  <p>Престижный внедорожник с комфортным салоном, передовыми технологиями и динамичной управляемостью.</p>
</div>

<div class="product" onclick="showPrice('Porsche Cayenne', '12 800 000 ₽')">
  <img src="https://d2ivfcfbdvj3sm.cloudfront.net/7fc965ab77efe6e0fa62e4ca1ea7673bb65846530c1e3d8e88cb10/stills_0640_png/MY2023/52727/52727_st0640_116.png" alt="Porsche Cayenne">
  <h3>Porsche Cayenne</h3>
  <p>Спортивный люксовый внедорожник с мощным двигателем и высокой маневренностью.</p>
</div>

<div class="product" onclick="showPrice('Toyota Land Cruiser 300', '9 900 000 ₽')">
  <img src="https://avatars.mds.yandex.net/get-verba/216201/2a0000017a62aab3c61e40933bb9f255cdb3/456x342" alt="Toyota Land Cruiser 300">
  <h3>Toyota Land Cruiser 300</h3>
  <p>Надежный внедорожник с высокой проходимостью и долговечной конструкцией для любых условий.</p>
</div>

<div class="product" onclick="showPrice('Jeep Grand Cherokee', '6 500 000 ₽')">
  <img src="https://w7.pngwing.com/pngs/1005/370/png-transparent-2018-jeep-grand-cherokee-trackhawk-chrysler-sport-utility-vehicle-ram-pickup-grand-sale-car-automatic-transmission-vehicle.png" alt="Jeep Grand Cherokee">
  <h3>Jeep Grand Cherokee</h3>
  <p>Прочный внедорожник с комфортным салоном, отличной проходимостью и современными технологиями.</p>
</div>

<div class="product" onclick="showPrice('Lamborghini Aventador', '45 000 000 ₽')">
  <img src="https://png.pngtree.com/png-vector/20240705/ourmid/pngtree-high-resolution-image-of-a-blue-lamborghini-aventador-clipart-png-image_12960222.png" alt="Lamborghini Aventador">
  <h3>Lamborghini Aventador</h3>
  <p>Эксклюзивный суперкар с невероятной мощностью, аэродинамикой и спортивным дизайном.</p>
</div>

<div class="product" onclick="showPrice('Ferrari 488 GTB', '38 000 000 ₽')">
  <img src="https://png.pngtree.com/png-vector/20250422/ourmid/pngtree-red-ferrari-sports-car-with-racing-stripes-png-image_15976335.png" alt="Ferrari 488 GTB">
  <h3>Ferrari 488 GTB</h3>
  <p>Высокопроизводительный спорткар с итальянским дизайном и выдающейся динамикой на дороге.</p>
</div>

<div class="product" onclick="showPrice('McLaren 720S', '42 000 000 ₽')">
  <img src="https://png.pngtree.com/png-vector/20250429/ourmid/pngtree-sleek-silver-mclaren-720s-supercar-angled-view-showcasing-aerodynamic-design-and-png-image_16098904.png" alt="McLaren 720S">
  <h3>McLaren 720S</h3>
  <p>Современный суперкар с высокой скоростью, аэродинамикой и выдающейся управляемостью.</p>
</div>

<div class="product" onclick="showPrice('Lamborghini Urus', '29 000 000 ₽')">
  <img src="https://png.pngtree.com/png-vector/20250423/ourlarge/pngtree-black-lamborghini-urus-suv-png-image_16072599.png" alt="Lamborghini Urus">
  <h3>Lamborghini Urus</h3>
  <p>Суперкроссовер с мощным двигателем, спортивным дизайном и роскошным интерьером.</p>
</div>

<div class="product" onclick="showPrice('Rolls-Royce Cullinan', '55 000 000 ₽')">
  <img src="https://www.chabe.fr/wp-content/uploads/2021/03/RR2-retourne-600X503.png" alt="Rolls-Royce Cullinan">
  <h3>Rolls-Royce Cullinan</h3>
  <p>Элитный внедорожник с непревзойденным комфортом, роскошными материалами и высокой мощностью.</p>
</div>

<div class="product" onclick="showPrice('Tesla Model X', '11 500 000 ₽')">
  <img src="https://autopremiumgroup.ru/m/_versions/catalog/autos/2015/tesla_model_x_2015_vnedorozhnik_5dv/performance/black_image_series.jpg" alt="Tesla Model X">
  <h3>Tesla Model X</h3>
  <p>Электрический кроссовер с передовыми технологиями, высоким запасом хода и просторным салоном.</p>
</div>

<div class="product" onclick="showPrice('Nissan GT-R', '15 000 000 ₽')">
  <img src="https://img.goodfon.ru/wallpaper/big/4/65/nissan-gt-r-nismo.webp" alt="Nissan GT-R">
  <h3>Nissan GT-R</h3>
  <p>Легендарный спортивный автомобиль с выдающейся динамикой и точной управляемостью.</p>
</div>

<div class="product" onclick="showPrice('Chevrolet Camaro', '7 000 000 ₽')">
  <img src="https://png.pngtree.com/png-vector/20240528/ourmid/pngtree-black-colour-chevrolet-camaro-2ss-png-image_12538610.png" alt="Chevrolet Camaro">
  <h3>Chevrolet Camaro</h3>
  <p>Американский спорткар с мощным двигателем и агрессивным дизайном.</p>
</div>

<div class="product" onclick="showPrice('Audi R8', '18 000 000 ₽')">
  <img src="https://www.shutterstock.com/image-illustration/almaty-kazakhstan-jan-152022-new-600nw-2108483666.jpg" alt="Audi R8">
  <h3>Audi R8</h3>
  <p>Суперкар с немецким качеством, высокой производительностью и элегантным дизайном.</p>
</div>

<div class="product" onclick="showPrice('Ford Mustang', '8 500 000 ₽')">
  <img src="https://autopremiumgroup.ru/m/_versions/ford/mustang_2020/shelby_gt350r/gt350r_mustang_2020_ford_performance_blue_f_image_series_preview.png" alt="Ford Mustang">
  <h3>Ford Mustang</h3>
  <p>Культовый американский мускулкар с мощным двигателем и агрессивным дизайном.</p>
</div>

    </section>
  </main>

  <div id="modal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal()">&times;</span>
      <h2 id="modal-title"></h2>
      <p id="modal-price"></p>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Чудеса. Все права защищены.</p>
  </footer>

  <script>
    const exchangeRates = {
      USD: 100,
      EUR: 110
    };
    let currentCurrency = 'RUB';

    function showPrice(title, price) {
      let numericPrice = parseInt(price.replace(/\s|₽/g, ''));
      let displayPrice = price;
      if(currentCurrency !== 'RUB'){
        let converted = (numericPrice / exchangeRates[currentCurrency]).toFixed(2);
        displayPrice = `${converted} ${currentCurrency}`;
      }
      document.getElementById('modal-title').innerText = title;
      document.getElementById('modal-price').innerText = `Цена: ${displayPrice}`;
      document.getElementById('modal').style.display = 'block';
    }

    function closeModal() {
      document.getElementById('modal').style.display = 'none';
    }

    function setCurrency(currency){
      currentCurrency = currency;
      alert(`Валюта изменена на ${currency}. Откройте товар, чтобы увидеть цену в новой валюте.`);
    }
  </script>
</body>
</html>
