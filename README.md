<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>貓窩裏 到府寵物褓姆 🐾</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
:root {
  --pink: #FFB6C1;
  --pink-deep: #FF8FA3;
  --pink-light: #FFF0F3;
  --pink-pale: #FFF5F7;
  --cream: #FFF9F0;
  --yellow: #FFE599;
  --text: #4A3545;
  --text-light: #8B6878;
  --white: #FFFFFF;
  --shadow: rgba(255,143,163,0.2);
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  font-family: 'Noto Sans TC', sans-serif;
  background: var(--pink-pale);
  color: var(--text);
  min-height: 100vh;
}
 
/* HERO */
.hero {
  background: linear-gradient(135deg, #FFD6E0 0%, #FFECF0 40%, #FFF0F8 100%);
  position: relative;
  overflow: hidden;
  border-bottom: 3px dashed var(--pink);
}
.hero-inner {
  max-width: 900px;
  margin: 0 auto;
  padding: 40px 20px 30px;
  text-align: center;
  position: relative;
  z-index: 2;
}
.hero-deco {
  font-size: 2.5rem;
  letter-spacing: 8px;
  margin-bottom: 8px;
  animation: float 3s ease-in-out infinite;
}
@keyframes float {
  0%,100%{transform:translateY(0);}
  50%{transform:translateY(-8px);}
}
.hero h1 {
  font-size: clamp(1.8rem, 5vw, 2.8rem);
  font-weight: 700;
  color: var(--pink-deep);
  text-shadow: 2px 2px 0 #fff, 3px 3px 0 var(--pink);
  margin-bottom: 6px;
  line-height: 1.3;
}
.hero-sub { font-size: 1rem; color: var(--text-light); margin-bottom: 18px; }
.line-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #06C755;
  color: white;
  padding: 10px 22px;
  border-radius: 30px;
  font-weight: 700;
  font-size: 0.95rem;
  text-decoration: none;
  box-shadow: 0 4px 12px rgba(6,199,85,0.3);
  transition: transform .2s;
}
.line-btn:hover { transform: scale(1.05); }
.paw-bg {
  position: absolute;
  top:0;left:0;right:0;bottom:0;
  pointer-events: none;
  overflow: hidden;
}
.paw-bg span {
  position: absolute;
  opacity: 0.12;
  animation: drift 8s linear infinite;
}
@keyframes drift {
  0%{transform:translateY(100%) rotate(0deg);opacity:0;}
  10%{opacity:0.12;}
  90%{opacity:0.12;}
  100%{transform:translateY(-100vh) rotate(360deg);opacity:0;}
}
 
/* NAV */
nav {
  background: var(--white);
  border-bottom: 2px solid var(--pink);
  display: flex;
  justify-content: center;
  gap: 4px;
  padding: 8px 12px;
  flex-wrap: wrap;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 12px var(--shadow);
}
nav a {
  padding: 7px 16px;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--text-light);
  text-decoration: none;
  cursor: pointer;
  transition: all .2s;
}
nav a:hover { background: var(--pink); color: white; }
 
/* SECTION */
.section { max-width: 900px; margin: 30px auto; padding: 0 16px; }
.card {
  background: var(--white);
  border-radius: 20px;
  padding: 28px;
  box-shadow: 0 4px 20px var(--shadow);
  border: 2px solid #FFE0E8;
  margin-bottom: 24px;
  position: relative;
  overflow: hidden;
}
.card::before {
  content: '';
  position: absolute;
  top:-2px;left:-2px;right:-2px;
  height: 6px;
  background: linear-gradient(90deg,var(--pink),var(--pink-deep),var(--pink));
  border-radius: 20px 20px 0 0;
}
.card-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--pink-deep);
  margin-bottom: 18px;
  display: flex;
  align-items: center;
  gap: 8px;
}
 
/* INPUTS */
.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
@media(max-width:520px){ .contact-grid{ grid-template-columns:1fr; } }
.input-field { display: flex; flex-direction: column; gap: 5px; }
.input-field.full { grid-column: 1 / -1; }
.input-field label { font-size: 0.82rem; color: var(--text-light); font-weight: 500; }
.input-field input, .input-field textarea {
  padding: 10px 14px;
  border: 2px solid #FFD6E0;
  border-radius: 12px;
  font-size: 0.9rem;
  font-family: inherit;
  color: var(--text);
  background: white;
  outline: none;
  transition: border .2s;
  resize: vertical;
}
.input-field input:focus, .input-field textarea:focus { border-color: var(--pink-deep); }
 
/* DATE */
.date-row { display: flex; gap: 14px; flex-wrap: wrap; }
.date-field { flex:1; min-width:140px; }
.date-field label { display:block; font-size:0.82rem; color:var(--text-light); margin-bottom:5px; font-weight:500; }
.date-field input {
  width:100%; padding:10px 14px;
  border:2px solid #FFD6E0; border-radius:12px;
  font-size:0.9rem; font-family:inherit; color:var(--text);
  background:white; outline:none; transition:border .2s;
}
.date-field input:focus { border-color: var(--pink-deep); }
.date-info { margin-top:10px; font-size:0.88rem; color:var(--pink-deep); font-weight:600; }
 
/* NUMBER */
.number-field { display:flex; flex-direction:column; gap:5px; }
.number-field label { font-size:0.82rem; color:var(--text-light); font-weight:500; }
.num-ctrl { display:flex; align-items:center; gap:8px; }
.num-btn {
  width:32px; height:32px;
  border:2px solid var(--pink); border-radius:50%;
  background:white; font-size:1.1rem; color:var(--pink-deep);
  cursor:pointer; display:flex; align-items:center; justify-content:center;
  font-weight:700; transition:all .15s;
}
.num-btn:hover { background:var(--pink); color:white; }
.num-val { font-size:1.1rem; font-weight:700; min-width:24px; text-align:center; }
 
/* SERVICE */
.service-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(180px,1fr)); gap:12px; margin-bottom:12px; }
.service-card {
  border:2px solid #FFD6E0; border-radius:16px; padding:16px 12px;
  cursor:pointer; text-align:center; transition:all .2s;
  background:var(--pink-pale); position:relative;
}
.service-card:hover { border-color:var(--pink-deep); transform:translateY(-2px); }
.service-card.selected {
  border-color:var(--pink-deep);
  background:linear-gradient(135deg,#FFD6E0,#FFF0F3);
  box-shadow:0 4px 12px var(--shadow);
}
.service-card.selected::after { content:'✓'; position:absolute; top:6px; right:10px; color:var(--pink-deep); font-weight:700; }
.service-icon { font-size:1.8rem; margin-bottom:6px; }
.service-name { font-size:0.82rem; font-weight:600; color:var(--text); }
.service-price { font-size:0.78rem; color:var(--pink-deep); font-weight:700; margin-top:2px; }
 
/* ADDON */
.addon-list { display:flex; flex-wrap:wrap; gap:10px; }
.addon-item {
  display:flex; align-items:center; gap:8px;
  border:2px solid #FFD6E0; border-radius:30px; padding:8px 14px;
  cursor:pointer; font-size:0.82rem; transition:all .2s;
  background:white; user-select:none;
}
.addon-item input { display:none; }
.addon-item:has(input:checked) {
  background:var(--pink-light); border-color:var(--pink-deep);
  color:var(--pink-deep); font-weight:600;
}
 
/* DISTANCE */
.dist-input {
  width:90px; padding:10px 12px;
  border:2px solid #FFD6E0; border-radius:12px;
  font-size:0.95rem; font-family:inherit; text-align:center;
  outline:none; transition:border .2s;
}
.dist-input:focus { border-color:var(--pink-deep); }
.map-link {
  display:inline-flex; align-items:center; gap:6px;
  background:var(--cream); border:2px solid #FFE599; border-radius:20px;
  padding:8px 14px; font-size:0.82rem; color:#A07800;
  font-weight:600; text-decoration:none; transition:all .2s;
}
.map-link:hover { background:var(--yellow); }
 
/* SUMMARY */
.summary-box {
  background:linear-gradient(135deg,#FFF0F3,#FFF9F0);
  border:2px dashed var(--pink); border-radius:16px; padding:20px; margin-top:6px;
}
.summary-row { display:flex; justify-content:space-between; font-size:0.88rem; padding:4px 0; color:var(--text-light); }
.summary-row.total {
  border-top:2px dashed var(--pink); margin-top:10px; padding-top:10px;
  font-size:1.1rem; font-weight:700; color:var(--pink-deep);
}
.submit-btn {
  width:100%; padding:16px;
  background:linear-gradient(135deg,var(--pink-deep),#FF6B8A);
  color:white; border:none; border-radius:16px;
  font-size:1.1rem; font-weight:700; font-family:inherit;
  cursor:pointer; box-shadow:0 6px 20px rgba(255,107,138,0.35);
  transition:all .2s; letter-spacing:2px; margin-top:20px;
}
.submit-btn:hover { transform:translateY(-2px); box-shadow:0 8px 24px rgba(255,107,138,0.45); }
 
/* TEAM */
.team-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:16px; }
.team-card {
  background:linear-gradient(135deg,var(--pink-pale),white);
  border:2px solid #FFD6E0; border-radius:18px; padding:20px 16px; text-align:center;
}
.team-avatar { font-size:2.5rem; margin-bottom:8px; }
.team-name { font-weight:700; color:var(--pink-deep); font-size:1rem; margin-bottom:4px; }
.team-badge {
  display:inline-block; background:var(--pink); color:white;
  border-radius:20px; font-size:0.7rem; padding:2px 10px; font-weight:600; margin-bottom:8px;
}
.team-desc { font-size:0.8rem; color:var(--text-light); line-height:1.6; }
 
/* MODAL */
.modal-overlay {
  display:none; position:fixed; inset:0;
  background:rgba(0,0,0,0.38); z-index:999;
  align-items:center; justify-content:center;
  backdrop-filter:blur(4px);
}
.modal-overlay.show { display:flex; }
.modal {
  background:white; border-radius:24px; padding:32px 28px;
  text-align:center; max-width:400px; width:92%;
  box-shadow:0 20px 60px rgba(255,107,138,0.25);
  animation:popIn .3s ease;
}
@keyframes popIn {
  from{transform:scale(.85);opacity:0;}
  to{transform:scale(1);opacity:1;}
}
.modal-icon { font-size:3.2rem; margin-bottom:10px; }
.modal-title { font-size:1.25rem; font-weight:700; color:var(--pink-deep); margin-bottom:10px; }
.modal-msg { font-size:0.9rem; color:var(--text-light); line-height:1.8; margin-bottom:16px; }
.modal-line-box {
  background:#F0FFF5; border:2px solid #06C755; border-radius:14px;
  padding:14px 16px; margin-bottom:18px;
}
.modal-line-label { font-size:0.8rem; color:#047A36; margin-bottom:10px; font-weight:600; line-height:1.5; }
.modal-line-btn {
  display:inline-flex; align-items:center; gap:8px;
  background:#06C755; color:white; padding:10px 22px;
  border-radius:30px; font-weight:700; font-size:0.9rem;
  text-decoration:none; transition:opacity .2s;
}
.modal-line-btn:hover { opacity:.88; }
.modal-close {
  background:var(--pink-deep); color:white; border:none;
  border-radius:30px; padding:11px 0; font-size:0.9rem;
  font-family:inherit; font-weight:700; cursor:pointer;
  display:block; width:100%; transition:all .2s;
}
.modal-close:hover { background:#FF6B8A; }
 
/* FOOTER */
footer {
  background:linear-gradient(135deg,#FFD6E0,#FFECF0);
  text-align:center; padding:30px 20px; margin-top:40px;
  border-top:3px dashed var(--pink); font-size:0.85rem; color:var(--text-light);
}
footer .footer-title { font-weight:700; font-size:1rem; color:var(--pink-deep); margin-bottom:8px; }
</style>
</head>
<body>
 
<!-- HERO -->
<div class="hero">
  <div class="paw-bg" id="pawBg"></div>
  <div class="hero-inner">
    <div class="hero-deco">🐱 🐾 🐶</div>
    <h1>貓窩裏<br>到府寵物褓姆</h1>
    <p class="hero-sub">專業到府照顧・讓毛孩在家也能被愛包圍 🌸</p>
    <a class="line-btn" href="https://line.me/R/ti/p/@099nuhen" target="_blank">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="white"><path d="M12 2C6.48 2 2 6.02 2 11c0 4.18 2.76 7.73 6.76 9.29L8 22l2.09-1.28C10.7 20.88 11.35 21 12 21c5.52 0 10-4.02 10-9s-4.48-9-10-9z"/></svg>
      加入 LINE @099nuhen
    </a>
  </div>
</div>
 
<!-- NAV -->
<nav>
  <a onclick="goTo('booking')">📋 立即預約</a>
  <a onclick="goTo('services')">🛁 服務項目</a>
  <a onclick="goTo('team')">👩‍⚕️ 認識保母</a>
  <a href="admin.html">🔐 後臺管理</a>
</nav>
 
<!-- BOOKING -->
<div class="section" id="booking">
 
  <!-- 1. 飼主資料 -->
  <div class="card">
    <div class="card-title">📝 飼主資料</div>
    <div class="contact-grid">
      <div class="input-field">
        <label>飼主姓名 *</label>
        <input type="text" id="ownerName" placeholder="您的稱呼">
      </div>
      <div class="input-field">
        <label>聯絡電話 *</label>
        <input type="tel" id="ownerPhone" placeholder="0912-345-678">
      </div>
      <div class="input-field">
        <label>LINE ID</label>
        <input type="text" id="ownerLine" placeholder="您的 LINE ID">
      </div>
      <div class="input-field">
        <label>服務地址 *</label>
        <input type="text" id="ownerAddr" placeholder="台北市...（請填詳細地址）">
      </div>
      <div class="input-field">
        <label>寵物名字 *</label>
        <input type="text" id="petName" placeholder="例：橘寶、小黑...">
      </div>
      <div class="input-field">
        <label>品種 / 年齡</label>
        <input type="text" id="petBreed" placeholder="例：橘貓 3歲">
      </div>
      <div class="input-field full">
        <label>特殊需求 / 健康狀況</label>
        <textarea id="petInfo" rows="2" placeholder="例：需每日餵慢性病藥、個性友善..."></textarea>
      </div>
    </div>
  </div>
 
  <!-- 2. 預約日期 -->
  <div class="card">
    <div class="card-title">📅 預約日期與次數</div>
    <div class="date-row">
      <div class="date-field">
        <label>開始日期</label>
        <input type="date" id="startDate" onchange="calcTotal()">
      </div>
      <div class="date-field">
        <label>結束日期</label>
        <input type="date" id="endDate" onchange="calcTotal()">
      </div>
    </div>
    <div class="date-info" id="dateInfo">請選擇服務日期</div>
    <div style="margin-top:18px;">
      <div class="number-field">
        <label>每天服務次數（次/天）</label>
        <div class="num-ctrl" style="margin-top:4px;">
          <button class="num-btn" onclick="changeNum('timesPerDay',-1)">−</button>
          <span class="num-val" id="timesPerDay">1</span>
          <button class="num-btn" onclick="changeNum('timesPerDay',1)">＋</button>
        </div>
      </div>
    </div>
  </div>
 
  <!-- 3. 主要服務 -->
  <div class="card">
    <div class="card-title">🐾 選擇主要服務</div>
    <div class="service-grid">
      <div class="service-card selected" data-service="companion" data-base="300" onclick="toggleService(this)">
        <div class="service-icon">🏠</div>
        <div class="service-name">到府陪伴</div>
        <div class="service-price">$300 / 0.5H</div>
      </div>
      <div class="service-card" data-service="walk" data-base="200" onclick="toggleService(this)">
        <div class="service-icon">🦮</div>
        <div class="service-name">散步服務</div>
        <div class="service-price">$200 / 0.5H</div>
      </div>
    </div>
    <div style="font-size:0.8rem;color:var(--text-light);">※ 可同時選擇多項主要服務</div>
  </div>
 
  <!-- 4. 加購 -->
  <div class="card">
    <div class="card-title">✨ 加購服務（每次、每天計費）</div>
    <div class="addon-list" id="addonList">
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="50" data-name="餵藥"><span>💊</span> 餵藥 <strong>+$50</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="50" data-name="點藥"><span>💧</span> 點藥 <strong>+$50</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="100" data-name="寵物舒緩按摩"><span>💆</span> 舒緩按摩 <strong>+$100</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="80" data-name="剪指甲"><span>✂️</span> 剪指甲 <strong>+$80</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="80" data-name="協助排便導尿"><span>🚿</span> 協助排便導尿 <strong>+$80</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="30" data-name="收信"><span>📮</span> 收信 <strong>+$30</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="30" data-name="澆花"><span>🌿</span> 澆花 <strong>+$30</strong></label>
      <label class="addon-item" onclick="calcTotal()"><input type="checkbox" value="50" data-name="倒垃圾"><span>🗑️</span> 倒垃圾 <strong>+$50</strong></label>
    </div>
    <div style="margin-top:18px;">
      <label style="font-size:0.82rem;color:var(--text-light);font-weight:500;display:block;margin-bottom:10px;">🐾 第三隻起加收（貓 +$30 / 狗 +$30 / 次）</label>
      <div style="display:flex;gap:20px;flex-wrap:wrap;">
        <div class="number-field">
          <label>貓咪數量</label>
          <div class="num-ctrl"><button class="num-btn" onclick="changeNum('catCount',-1)">−</button><span class="num-val" id="catCount">1</span><button class="num-btn" onclick="changeNum('catCount',1)">＋</button></div>
        </div>
        <div class="number-field">
          <label>狗狗數量</label>
          <div class="num-ctrl"><button class="num-btn" onclick="changeNum('dogCount',-1)">−</button><span class="num-val" id="dogCount">0</span><button class="num-btn" onclick="changeNum('dogCount',1)">＋</button></div>
        </div>
      </div>
    </div>
  </div>
 
  <!-- 5. 車馬費 -->
  <div class="card">
    <div class="card-title">🚗 車馬費計算</div>
    <div style="margin-bottom:12px;">
      <a class="map-link" href="https://maps.google.com" target="_blank">🗺️ 開啟 Google Maps 查詢距離</a>
    </div>
    <div style="display:flex;align-items:center;gap:12px;flex-wrap:wrap;">
      <span style="font-size:0.88rem;color:var(--text-light);">單程距離</span>
      <input type="number" class="dist-input" id="distance" placeholder="0" min="0" step="0.1" oninput="calcTotal()">
      <span style="font-size:0.88rem;color:var(--text-light);">公里</span>
      <span id="distCost" style="font-size:0.85rem;color:var(--pink-deep);font-weight:700;"></span>
    </div>
    <div style="margin-top:10px;font-size:0.78rem;color:var(--text-light);">
      🐾 5km 以內免收車馬費 ｜ 超過 5km，每多 1km 加收 $50
    </div>
  </div>
 
  <!-- 6. 備注 -->
  <div class="card">
    <div class="card-title">💬 其他備注</div>
    <div class="input-field">
      <label>其他服務需求或備注（選填）</label>
      <textarea id="notes" rows="3" placeholder="其他特殊服務需求可於此詳述，我們將盡快與您確認..."></textarea>
    </div>
  </div>
 
  <!-- SUMMARY + SUBMIT -->
  <div class="card">
    <div class="card-title">🧾 費用試算</div>
    <div class="summary-box" id="summaryBox">
      <div class="summary-row"><span>填寫資料後自動計算</span><span></span></div>
    </div>
    <button class="submit-btn" onclick="submitBooking()">🐾 送出預約申請 🐾</button>
  </div>
 
</div>
 
<!-- SERVICES -->
<div class="section" id="services">
  <div class="card">
    <div class="card-title">🛁 服務項目說明</div>
    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px;">
      <div style="background:var(--pink-pale);border-radius:14px;padding:16px;">
        <div style="font-weight:700;color:var(--pink-deep);margin-bottom:8px;">🏠 到府陪伴 $300/0.5H</div>
        <div style="font-size:0.82rem;line-height:1.8;color:var(--text-light);">✦ 餵食<br>✦ 環境清潔<br>✦ 陪玩互動<br>✦ 身體狀況觀察</div>
      </div>
      <div style="background:var(--pink-pale);border-radius:14px;padding:16px;">
        <div style="font-weight:700;color:var(--pink-deep);margin-bottom:8px;">🦮 散步服務 $200/0.5H</div>
        <div style="font-size:0.82rem;line-height:1.8;color:var(--text-light);">✦ 安全外出散步<br>✦ 適度運動<br>✦ 社交互動</div>
      </div>
      <div style="background:#FFF0F3;border-radius:14px;padding:16px;">
        <div style="font-weight:700;color:var(--pink-deep);margin-bottom:8px;">✨ 加購服務</div>
        <div style="font-size:0.82rem;line-height:1.8;color:var(--text-light);">
          💊 餵藥 +$50｜💧 點藥 +$50<br>💆 舒緩按摩 +$100<br>✂️ 剪指甲 +$80<br>🚿 協助排便導尿 +$80<br>📮 收信 +$30｜🌿 澆花 +$30<br>🗑️ 倒垃圾 +$50<br>🐾 第三隻起 貓/狗 +$30/次
        </div>
      </div>
    </div>
    <div style="margin-top:16px;background:var(--cream);border-radius:12px;padding:14px;font-size:0.82rem;color:var(--text-light);line-height:1.8;">
      💬 其他特殊服務需求歡迎透過 LINE 詳談：<strong style="color:#06C755;">@099nuhen</strong>
    </div>
  </div>
</div>
 
<!-- TEAM -->
<div class="section" id="team">
  <div class="card">
    <div class="card-title">👩‍⚕️ 認識我們的保母團隊</div>
    <div class="team-grid">
      <div class="team-card"><div class="team-avatar">👩‍⚕️</div><div class="team-name">May</div><div class="team-badge">首席顧問</div><div class="team-desc">護理師背景，數十年養貓資歷，專業醫療判斷力，是團隊最強力的後盾。</div></div>
      <div class="team-card"><div class="team-avatar">🐱</div><div class="team-name">Ying</div><div class="team-badge">資深貓咪照護</div><div class="team-desc">長期照顧貓咪逾10年，老年照護經驗豐富，可協助飼主學習皮下點滴技巧。</div></div>
      <div class="team-card"><div class="team-avatar">🌟</div><div class="team-name">小汶</div><div class="team-badge">老年寵物照護</div><div class="team-desc">前安養機構寵物助理，對老齡毛孩的日常照顧與情緒陪伴有豐富實務經驗。</div></div>
      <div class="team-card"><div class="team-avatar">🍎</div><div class="team-name">菓菓</div><div class="team-badge">中途志工</div><div class="team-desc">家有四隻貓，在中途培養了餵藥、清潔等多項照護技能，衛生習慣嚴謹。</div></div>
      <div class="team-card"><div class="team-avatar">🐕</div><div class="team-name">小茹</div><div class="team-badge">中途志工</div><div class="team-desc">家有一犬，熱愛陪伴動物，貓狗照護均有豐富實戰經驗的愛心保母。</div></div>
      <div class="team-card"><div class="team-avatar">🌺</div><div class="team-name">阿瑛</div><div class="team-badge">中途志工</div><div class="team-desc">長期投入中途志工服務，具備基礎貓狗照護能力，細心溫柔是她的特色。</div></div>
    </div>
  </div>
</div>
 
<footer>
  <div class="footer-title">🐾 貓窩裏 到府寵物褓姆</div>
  <div>LINE 官方帳號：<strong>@099nuhen</strong></div>
  <div style="margin-top:6px;font-size:0.78rem;">© 2025 貓窩裏 · 讓每隻毛孩都被好好愛著 💕</div>
</footer>
 
<!-- MODAL -->
<div class="modal-overlay" id="modalOverlay">
  <div class="modal">
    <div class="modal-icon">🐾</div>
    <div class="modal-title">預約申請已送出！</div>
    <div class="modal-msg">
      感謝您填寫預約資料 💕<br>
      <strong>褓姆將盡速與您聯繫</strong>，請保持電話暢通。
    </div>
    <div class="modal-line-box">
      <div class="modal-line-label">📢 請先加入我們的 LINE 官方帳號<br>以便保母即時與您確認訂單細節！</div>
      <a class="modal-line-btn" href="https://line.me/R/ti/p/@099nuhen" target="_blank">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="white"><path d="M12 2C6.48 2 2 6.02 2 11c0 4.18 2.76 7.73 6.76 9.29L8 22l2.09-1.28C10.7 20.88 11.35 21 12 21c5.52 0 10-4.02 10-9s-4.48-9-10-9z"/></svg>
        加入 LINE @099nuhen
      </a>
    </div>
    <button class="modal-close" onclick="closeModal()">好的，我知道了 🌸</button>
  </div>
</div>
 
<script>
// Smooth scroll with nav offset
function goTo(id){
  const el = document.getElementById(id);
  if(!el) return;
  const navH = document.querySelector('nav').offsetHeight;
  window.scrollTo({ top: el.getBoundingClientRect().top + window.pageYOffset - navH - 12, behavior:'smooth' });
}
 
// Paw BG
const pawBg = document.getElementById('pawBg');
['🐾','🐱','🐶','🌸','💕','⭐'].forEach(p=>{
  for(let i=0;i<2;i++){
    const s=document.createElement('span');
    s.textContent=p;
    s.style.cssText=`left:${Math.random()*100}%;animation-delay:${Math.random()*8}s;animation-duration:${6+Math.random()*6}s;font-size:${1.5+Math.random()*1.5}rem`;
    pawBg.appendChild(s);
  }
});
 
// Service toggle
function toggleService(el){
  const all=document.querySelectorAll('.service-card.selected');
  if(el.classList.contains('selected')&&all.length===1) return;
  el.classList.toggle('selected');
  calcTotal();
}
 
// Number controls
const N={catCount:1,dogCount:0,timesPerDay:1};
function changeNum(id,delta){
  N[id]=Math.max(id==='timesPerDay'?1:0, N[id]+delta);
  document.getElementById(id).textContent=N[id];
  calcTotal();
}
 
// Days
function calcDays(){
  const s=document.getElementById('startDate').value;
  const e=document.getElementById('endDate').value;
  if(!s||!e) return 0;
  const d=Math.floor((new Date(e)-new Date(s))/(864e5))+1;
  return d<0?0:d;
}
 
// Distance cost: 5km以內免費，超過5km每多1km加$50
function distCost(km){
  km=parseFloat(km)||0;
  if(km<=5) return 0;
  return Math.ceil((km-5))*50;
}
 
// Calc
function calcTotal(){
  const days=calcDays();
  const times=N.timesPerDay;
  const cats=N.catCount, dogs=N.dogCount;
  const km=parseFloat(document.getElementById('distance').value)||0;
 
  document.getElementById('dateInfo').textContent=days>0?`📅 共 ${days} 天`:'請選擇服務日期';
 
  const dc=distCost(km);
  const de=document.getElementById('distCost');
  if(!km) de.textContent='';
  else if(dc===0) de.textContent='🎉 5km 內免收車馬費';
  else de.textContent=`車馬費 $${dc}（超出 ${(km-5).toFixed(1)} km × $50）`;
 
  let base=0;
  const cards=document.querySelectorAll('.service-card.selected');
  cards.forEach(c=>base+=parseInt(c.dataset.base));
 
  let addon=0; const addonNames=[];
  document.querySelectorAll('#addonList input:checked').forEach(cb=>{
    addon+=parseInt(cb.value); addonNames.push(cb.dataset.name);
  });
 
  let extra=0;
  if(cats>2) extra+=(cats-2)*30;
  if(dogs>2) extra+=(dogs-2)*30;
 
  const perSession=base+addon+extra;
  const daily=perSession*times;
  const sub=daily*(days||0);
  const total=sub+dc;
 
  const svcNames=[];
  cards.forEach(c=>svcNames.push({companion:'到府陪伴',walk:'散步服務'}[c.dataset.service]||c.dataset.service));
 
  let html='';
  html+=row(`主要服務（${svcNames.join('+')}）/次`,`$${base}`);
  if(addon>0) html+=row(`加購（${addonNames.join('、')}）/次`,`$${addon}`);
  if(extra>0) html+=row(`多寵物加收（貓${cats}/狗${dogs}隻）/次`,`$${extra}`);
  html+=row('每次費用',`$${perSession}`,'font-weight:600;color:var(--text)');
  html+=row(`× 每天 ${times} 次`,`每日 $${daily}`,'color:var(--text-light)');
  if(days>0) html+=row(`× ${days} 天`,`小計 $${sub}`,'color:var(--text-light)');
  if(dc>0) html+=row('車馬費',`$${dc}`);
  html+=`<div class="summary-row total"><span>💕 預估總費用</span><span>${days>0?'$'+total:'-'}</span></div>`;
  document.getElementById('summaryBox').innerHTML=html;
}
 
function row(l,v,s=''){
  return `<div class="summary-row" style="${s}"><span>${l}</span><span>${v}</span></div>`;
}
 
// Submit
function submitBooking(){
  const name=document.getElementById('ownerName').value.trim();
  const phone=document.getElementById('ownerPhone').value.trim();
  const addr=document.getElementById('ownerAddr').value.trim();
  const petName=document.getElementById('petName').value.trim();
  if(!name||!phone||!addr){ alert('請填寫飼主姓名、聯絡電話與服務地址 🐾'); return; }
  if(!petName){ alert('請填寫寵物名字 🐱'); return; }
  if(!calcDays()){ alert('請選擇預約日期 📅'); return; }
 
  const km=parseFloat(document.getElementById('distance').value)||0;
  const dc=distCost(km);
  const cards=document.querySelectorAll('.service-card.selected');
  let base=0; cards.forEach(c=>base+=parseInt(c.dataset.base));
  let addon=0; const addons=[];
  document.querySelectorAll('#addonList input:checked').forEach(cb=>{ addon+=parseInt(cb.value); addons.push(cb.dataset.name); });
  const cats=N.catCount, dogs=N.dogCount;
  let extra=0;
  if(cats>2) extra+=(cats-2)*30;
  if(dogs>2) extra+=(dogs-2)*30;
  const days=calcDays();
  const sub=(base+addon+extra)*N.timesPerDay*days;
  const total=sub+dc;
 
  const b={
    id:Date.now(), timestamp:new Date().toISOString(),
    ownerName:name, ownerPhone:phone,
    ownerLine:document.getElementById('ownerLine').value,
    ownerAddr:addr, petName,
    petBreed:document.getElementById('petBreed').value,
    petInfo:document.getElementById('petInfo').value,
    notes:document.getElementById('notes').value,
    startDate:document.getElementById('startDate').value,
    endDate:document.getElementById('endDate').value,
    days, timesPerDay:N.timesPerDay,
    services:Array.from(cards).map(c=>c.dataset.service),
    addons, catCount:cats, dogCount:dogs,
    distance:km, transport:dc, total,
    status:'待確認', assignedTo:''
  };
 
  const list=JSON.parse(localStorage.getItem('petBookings')||'[]');
  list.push(b);
  localStorage.setItem('petBookings',JSON.stringify(list));
  document.getElementById('modalOverlay').classList.add('show');
}
 
function closeModal(){
  document.getElementById('modalOverlay').classList.remove('show');
}
 
calcTotal();
</script>
</body>
</html>
