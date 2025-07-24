<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Qi Myotherapy | Myotherapy on the Road</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f8f8f8;
      color: #333;
    }
    header {
      background-color: #004d40;
      color: white;
      padding: 2rem;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
    }
    header p {
      margin: 0.5rem 0 0;
      font-size: 1rem;
    }
    main {
      max-width: 800px;
      margin: 2rem auto;
      padding: 0 1rem;
    }
    section {
      margin-bottom: 2rem;
    }
    h2 {
      color: #00695c;
      border-bottom: 2px solid #e0e0e0;
      padding-bottom: 0.5rem;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    ul li {
      padding: 0.3rem 0;
    }
    .contact p {
      margin: 0.3rem 0;
    }
    footer {
      background: #004d40;
      color: white;
      text-align: center;
      padding: 1rem;
      font-size: 0.9rem;
    }
    .lang-switcher {
      text-align: center;
      margin-top: 1rem;
    }
    .lang-switcher button, .booking-button {
      margin: 0.5rem;
      padding: 0.5rem 1rem;
      border: none;
      background: #00796b;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
    .booking-button {
      display: inline-block;
      font-size: 1rem;
    }
    .distance-input {
      margin-top: 1rem;
    }
    .distance-input input {
      padding: 0.4rem;
      margin-right: 0.5rem;
      width: 60%;
    }
  </style>
</head>
<body>
  <header>
    <h1>Qi Myotherapy</h1>
    <p>Myotherapy on the Road</p>
  </header>

  <div class="lang-switcher">
    <button onclick="switchLang('en')">English</button>
    <button onclick="switchLang('zh')">中文</button>
  </div>

  <main>
    <div id="content-en">
      <section>
        <h2>About</h2>
        <p>We offer professional mobile myotherapy services with over 5 years of clinical experience. Specializing in soft tissue therapy, we treat muscle overuse, acute and chronic injuries, postural correction, and provide sports taping — all in the comfort of your home.</p>
      </section>
      <section>
        <h2>Pricing</h2>
        <ul>
          <li>Standard (60 min): $130 <strong>(First visit: $99)</strong></li>
          <li>Extended (90 min): $180</li>
        </ul>
        <p><strong>Travel Fee:</strong></p>
        <ul>
          <li>Within 10km: $10</li>
          <li>10–20km: $20</li>
          <li>20km+: $30</li>
        </ul>
        <div class="distance-input">
          <label for="address">Enter your address:</label>
          <input type="text" id="address" placeholder="e.g. 123 Example St, Clayton">
          <button onclick="checkDistance()">Check Travel Fee</button>
          <p id="distance-result"></p>
        </div>
        <a href="mailto:qimyotherapy@gmail.com" class="booking-button">Book Now</a>
      </section>
      <section>
        <h2>Services</h2>
        <ul>
          <li>Dry Needling</li>
          <li>Cupping</li>
          <li>Deep Tissue Massage</li>
          <li>Postural Correction & Muscle Overuse</li>
          <li>Sports Taping</li>
        </ul>
      </section>
      <section class="contact">
        <h2>Contact</h2>
        <p>Phone: 0406 379 771</p>
        <p>Email: <a href="mailto:qimyotherapy@gmail.com">qimyotherapy@gmail.com</a></p>
        <p>WeChat: qichen9611</p>
        <p>Xiaohongshu: 墨尔本启源理疗</p>
      </section>
    </div>

    <div id="content-zh" style="display: none;">
      <section>
        <h2>关于我们</h2>
        <p>专业的肌肉筋膜理疗服务，拥有超过五年的临床经验。擅长软组织治疗、肌肉劳损、急慢性损伤、体态调整和运动贴扎服务，让您在家即可享受诊所级别的治疗。</p>
      </section>
      <section>
        <h2>价格</h2>
        <ul>
          <li>常规 60 分钟：$130 <strong>（首次优惠价：$99）</strong></li>
          <li>加长 90 分钟：$180</li>
        </ul>
        <p><strong>上门费：</strong></p>
        <ul>
          <li>10公里以内：$10</li>
          <li>10–20公里：$20</li>
          <li>20公里以上：$30</li>
        </ul>
        <div class="distance-input">
          <label for="address-zh">请输入您的地址：</label>
          <input type="text" id="address-zh" placeholder="例如：123 某街, Clayton">
          <button onclick="checkDistance('zh')">计算上门费</button>
          <p id="distance-result-zh"></p>
        </div>
        <a href="mailto:qimyotherapy@gmail.com" class="booking-button">预约咨询</a>
      </section>
      <section>
        <h2>服务项目</h2>
        <ul>
          <li>干针疗法</li>
          <li>拔罐</li>
          <li>深层组织按摩</li>
          <li>姿势调整与肌肉劳损</li>
          <li>运动贴扎</li>
        </ul>
      </section>
      <section class="contact">
        <h2>联系方式</h2>
        <p>电话：0406 379 771</p>
        <p>邮箱：<a href="mailto:qimyotherapy@gmail.com">qimyotherapy@gmail.com</a></p>
        <p>微信：qichen9611</p>
        <p>小红书：墨尔本启源理疗</p>
      </section>
    </div>
  </main>

  <footer>
    &copy; 2025 Qi Myotherapy. All rights reserved.
  </footer>

  <script>
    function switchLang(lang) {
      document.getElementById('content-en').style.display = lang === 'en' ? 'block' : 'none';
      document.getElementById('content-zh').style.display = lang === 'zh' ? 'block' : 'none';
    }

    function checkDistance(lang = 'en') {
      const address = lang === 'zh' ? document.getElementById('address-zh').value : document.getElementById('address').value;
      const resultEl = lang === 'zh' ? document.getElementById('distance-result-zh') : document.getElementById('distance-result');
      if (!address.trim()) {
        resultEl.textContent = lang === 'zh' ? '请输入有效地址。' : 'Please enter a valid address.';
        return;
      }
      resultEl.textContent = lang === 'zh' ? '请参考地图软件估算距离（起点：Ash Court, Wheelers Hill）以确认上门费用。' : 'Please estimate distance using a map app (Start: Ash Court, Wheelers Hill) to determine travel fee.';
    }
  </script>
</body>
</html>
