<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>KemMY – Cari Campsite Malaysia</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@400;500;600;700&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg:        #0c1e0e;
    --bg2:       #142916;
    --green:     #7bc67a;
    --green-dim: #4a7c46;
    --green-dk:  #2d6a4f;
    --text:      #e2ddd4;
    --text-dim:  #8aab88;
    --text-muted:#4e6e4e;
    --card:      rgba(255,255,255,0.04);
    --border:    rgba(74,124,70,0.22);
    --border-hi: rgba(123,198,122,0.5);
    --wa:        #25d366;
    --orange:    #f4a261;
    --blue:      #457b9d;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }
  body::before {
    content: '';
    position: fixed; inset: 0; pointer-events: none; z-index: 0;
    background:
      radial-gradient(ellipse at 15% 20%, rgba(74,124,70,.1) 0%, transparent 55%),
      radial-gradient(ellipse at 85% 80%, rgba(30,80,40,.12) 0%, transparent 55%);
  }

  ::-webkit-scrollbar { width: 5px; height: 5px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: rgba(74,124,70,.35); border-radius: 10px; }

  header {
    position: sticky; top: 0; z-index: 200;
    background: rgba(10,22,12,.9);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid var(--border);
    padding: 13px 24px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .logo { display:flex; align-items:center; gap:10px; cursor:pointer; text-decoration:none; }
  .logo-icon { font-size: 28px; }
  .logo-name { font-family:'Playfair Display',serif; font-size:20px; color:var(--green); line-height:1; }
  .logo-tagline { font-size:9px; color:var(--text-muted); letter-spacing:.2em; text-transform:uppercase; margin-top:2px; }
  nav { display:flex; gap:8px; }
  .nav-btn {
    background: transparent;
    border: 1px solid rgba(74,124,70,.2);
    color: var(--text-dim); padding: 6px 16px;
    border-radius: 20px; font-size: 13px; cursor: pointer;
    font-family: inherit; transition: all .2s;
  }
  .nav-btn.active, .nav-btn:hover {
    background: rgba(74,124,70,.35);
    border-color: var(--green); color: var(--green);
  }

  .view { display: none; position: relative; z-index: 1; }
  .view.active { display: block; }

  .hero {
    padding: 52px 24px 32px;
    text-align: center;
    background: linear-gradient(180deg, rgba(74,124,70,.1) 0%, transparent 100%);
  }
  .hero-eyebrow { font-size:12px; letter-spacing:.25em; color:var(--green); margin-bottom:10px; text-transform:uppercase; }
  .hero-title {
    font-family:'Playfair Display',serif;
    font-size: clamp(28px,7vw,52px);
    line-height: 1.1; margin-bottom: 14px;
    background: linear-gradient(135deg,#b8e0b5 0%,#7bc67a 50%,#4a7c46 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .hero-sub { color:var(--text-dim); font-size:15px; max-width:400px; margin:0 auto 28px; line-height:1.6; }
  .search-wrap {
    max-width:480px; margin:0 auto;
    background: rgba(255,255,255,.06);
    border-radius: 50px; border: 1px solid rgba(74,124,70,.4);
    display: flex; align-items: center; gap: 8px;
    padding: 10px 20px; backdrop-filter: blur(8px);
  }
  .search-wrap input {
    flex:1; background:transparent; border:none; outline:none;
    color:var(--text); font-size:14px; font-family:inherit;
  }
  .search-wrap input::placeholder { color: var(--text-muted); }

  .filters {
    padding: 16px 16px 20px;
    display:flex; gap:8px; flex-wrap:wrap; justify-content:center;
  }
  .filter-btn {
    padding: 5px 14px; border-radius:20px; border:1px solid rgba(74,124,70,.25);
    background: rgba(255,255,255,.03); color:var(--text-dim);
    font-size:12px; cursor:pointer; font-family:inherit;
    white-space:nowrap; transition:all .2s;
  }
  .filter-btn.active { font-weight:700; }

  .result-count { text-align:center; color:var(--text-muted); font-size:12px; padding:0 16px 14px; }
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px,1fr));
    gap: 20px; padding: 0 20px 48px;
    max-width: 1100px; margin: 0 auto;
  }
  .card {
    background: var(--card); border-radius:20px;
    border: 1px solid var(--border); overflow:hidden;
    cursor:pointer; transition:transform .25s, border-color .25s, box-shadow .25s;
    animation: fadeUp .4s both;
  }
  .card:hover {
    transform: translateY(-5px);
    border-color: var(--border-hi);
    box-shadow: 0 18px 52px rgba(0,0,0,.45);
  }
  .card-img-wrap { position:relative; height:200px; overflow:hidden; }
  .card-img-wrap img { width:100%; height:100%; object-fit:cover; transition:transform .4s; display:block; }
  .card:hover .card-img-wrap img { transform:scale(1.06); }
  .card-img-overlay {
    position:absolute; inset:0;
    background:linear-gradient(to top,rgba(10,22,12,.72) 0%,transparent 60%);
  }
  .card-rating {
    position:absolute; top:12px; right:12px;
    background:rgba(0,0,0,.6); border-radius:20px;
    padding:3px 10px; font-size:12px;
    display:flex; align-items:center; gap:4px;
    backdrop-filter:blur(8px);
  }
  .star-icon { color:var(--orange); }
  .card-types {
    position:absolute; bottom:12px; left:12px;
    display:flex; gap:6px; flex-wrap:wrap;
  }
  .type-badge {
    font-size:10px; padding:3px 8px; border-radius:10px;
    color:#fff; font-weight:600; backdrop-filter:blur(4px);
  }
  .card-body { padding:16px; }
  .card-name { font-weight:800; font-size:16px; margin-bottom:4px; color:#d4eed0; }
  .card-loc { color:#7a9a78; font-size:13px; margin-bottom:6px; }
  .card-meta-row { display:flex; gap:12px; margin-bottom:8px; flex-wrap:wrap; }
  .card-meta-item { font-size:11px; color:var(--text-muted); display:flex; align-items:center; gap:3px; }
  .card-desc { color:#a0b8a0; font-size:12px; line-height:1.55; margin-bottom:12px; }
  .pill-row { display:flex; gap:6px; flex-wrap:wrap; margin-bottom:12px; }
  .pill {
    background:rgba(74,124,70,.15); border:1px solid rgba(74,124,70,.3);
    color:var(--text-dim); font-size:10px; padding:2px 8px; border-radius:8px;
  }
  .card-footer { display:flex; align-items:center; justify-content:space-between; }
  .price-main { color:var(--green); font-weight:800; font-size:18px; }
  .price-sub { color:var(--text-muted); font-size:11px; }
  .btn-primary {
    background:linear-gradient(135deg,var(--green-dim),var(--green-dk));
    border:none; border-radius:20px; color:#d4eed0;
    font-size:12px; padding:7px 16px; cursor:pointer;
    font-family:inherit; font-weight:600; transition:opacity .2s;
  }
  .btn-primary:hover { opacity:.85; }

  /* DETAIL */
  #view-detail { padding:20px 16px 60px; max-width:760px; margin:0 auto; }
  .back-btn {
    background:transparent; border:none; color:var(--green);
    cursor:pointer; font-size:14px; font-family:inherit;
    display:flex; align-items:center; gap:6px; margin-bottom:20px; padding:0;
  }
  .gallery-main { border-radius:20px; overflow:hidden; margin-bottom:12px; position:relative; }
  .gallery-main img { width:100%; height:320px; object-fit:cover; display:block; }
  .gallery-dots {
    position:absolute; bottom:12px; left:50%; transform:translateX(-50%);
    display:flex; gap:8px;
  }
  .dot {
    height:8px; border-radius:10px; border:none; cursor:pointer;
    background:rgba(255,255,255,.4); transition:all .3s; padding:0;
  }
  .dot.active { background:var(--green); width:28px; }
  .dot:not(.active) { width:8px; }
  .gallery-label {
    position:absolute; top:12px; right:12px;
    background:rgba(0,0,0,.6); border-radius:20px;
    padding:4px 12px; font-size:12px; backdrop-filter:blur(8px);
  }
  .thumbs { display:flex; gap:8px; margin-bottom:20px; flex-wrap:wrap; }
  .thumb {
    width:80px; height:56px; object-fit:cover; border-radius:10px;
    cursor:pointer; border:2px solid transparent;
    transition:border-color .2s, opacity .2s; opacity:.55;
  }
  .thumb.active { border-color:var(--green); opacity:1; }
  .info-card {
    background:var(--card); border-radius:20px;
    border:1px solid var(--border); padding:22px; margin-bottom:16px;
  }
  .info-top { display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap; gap:12px; margin-bottom:12px; }
  .info-name { font-family:'Playfair Display',serif; font-size:22px; color:#d4eed0; margin-bottom:6px; }
  .info-loc { color:#7a9a78; font-size:14px; margin-bottom:4px; }
  .info-state-badge {
    display:inline-block; font-size:10px; padding:2px 10px; border-radius:20px;
    background:rgba(74,124,70,.2); border:1px solid rgba(74,124,70,.3);
    color:var(--green); margin-top:4px;
  }
  .info-price-big { color:var(--green); font-weight:800; font-size:24px; }
  .info-price-unit { color:var(--text-muted); font-size:12px; }
  .stars-row { display:flex; align-items:center; gap:8px; margin-bottom:14px; }
  .stars-display { color:var(--orange); font-size:18px; letter-spacing:2px; }
  .rating-val { color:var(--orange); font-weight:800; font-size:16px; }
  .rating-count { color:var(--text-muted); font-size:13px; }
  .info-desc { color:#a0b8a0; line-height:1.7; margin-bottom:16px; font-size:14px; }
  .section-label { color:var(--green); font-size:11px; letter-spacing:.12em; font-weight:700; margin-bottom:8px; text-transform:uppercase; }

  /* Detail stats grid */
  .stats-grid {
    display:grid; grid-template-columns:repeat(3,1fr); gap:10px; margin-bottom:16px;
  }
  .stat-box {
    background:rgba(74,124,70,.08); border:1px solid rgba(74,124,70,.2);
    border-radius:12px; padding:12px; text-align:center;
  }
  .stat-val { color:var(--green); font-weight:800; font-size:16px; margin-bottom:2px; }
  .stat-label { color:var(--text-muted); font-size:10px; }

  /* Best for tags */
  .best-for-row { display:flex; gap:8px; flex-wrap:wrap; margin-bottom:16px; }
  .best-for-tag {
    font-size:11px; padding:4px 12px; border-radius:20px;
    background:rgba(244,162,97,.1); border:1px solid rgba(244,162,97,.3);
    color:var(--orange);
  }

  /* Rules */
  .rules-list { list-style:none; }
  .rules-list li {
    padding:6px 0; border-bottom:1px solid rgba(74,124,70,.1);
    font-size:13px; color:#9ab898; display:flex; gap:8px; align-items:flex-start;
  }
  .rules-list li:last-child { border-bottom:none; }

  .action-grid { display:grid; grid-template-columns:1fr 1fr; gap:12px; margin-bottom:16px; }
  .btn-map {
    background:linear-gradient(135deg,#1d6fa4,var(--blue));
    border:none; border-radius:14px; color:#fff;
    padding:14px; font-size:14px; cursor:pointer;
    font-family:inherit; font-weight:700;
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .btn-contact {
    background:linear-gradient(135deg,var(--wa),#128c7e);
    border:none; border-radius:14px; color:#fff;
    padding:14px; font-size:14px; cursor:pointer;
    font-family:inherit; font-weight:700;
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .contact-box {
    background:rgba(37,211,102,.06); border-radius:16px;
    border:1px solid rgba(37,211,102,.22);
    padding:18px; margin-bottom:16px;
    display:none; animation:fadeUp .3s ease;
  }
  .contact-box.open { display:block; }
  .contact-owner { color:var(--wa); font-weight:700; margin-bottom:12px; font-size:14px; }
  .contact-links { display:flex; gap:10px; flex-wrap:wrap; }
  .contact-links a {
    display:flex; align-items:center; gap:6px;
    border-radius:10px; padding:8px 16px;
    font-size:13px; font-weight:600; text-decoration:none;
    transition:opacity .2s;
  }
  .contact-links a:hover { opacity:.85; }
  .link-call { background:rgba(37,211,102,.12); border:1px solid rgba(37,211,102,.35); color:var(--wa); }
  .link-wa { background:linear-gradient(135deg,var(--wa),#128c7e); color:#fff; }

  .review-item { display:flex; gap:12px; padding:16px 0; border-bottom:1px solid rgba(74,124,70,.12); }
  .review-item:last-child { border-bottom:none; }
  .avatar {
    width:36px; height:36px; border-radius:50%;
    background:linear-gradient(135deg,var(--green-dim),var(--green-dk));
    display:flex; align-items:center; justify-content:center;
    color:#d4eed0; font-weight:800; font-size:14px; flex-shrink:0;
  }
  .rv-meta { display:flex; justify-content:space-between; align-items:center; margin-bottom:4px; }
  .rv-user { font-weight:700; color:#c8dcc8; font-size:14px; }
  .rv-date { color:var(--text-muted); font-size:11px; }
  .rv-stars { color:var(--orange); font-size:13px; letter-spacing:1px; }
  .rv-comment { color:#9ab898; font-size:13px; line-height:1.6; margin-top:5px; }

  .write-stars { display:flex; gap:4px; margin-bottom:12px; }
  .w-star {
    font-size:28px; cursor:pointer; color:#3a4a3a;
    transition:color .15s; background:none; border:none; line-height:1;
  }
  .w-star.lit { color:var(--orange); }
  textarea.review-input {
    width:100%; background:rgba(74,124,70,.08);
    border:1px solid rgba(74,124,70,.25); border-radius:12px;
    color:var(--text); font-size:13px; padding:12px;
    font-family:inherit; resize:vertical; outline:none; line-height:1.6;
    transition:border-color .2s;
  }
  textarea.review-input:focus { border-color:rgba(123,198,122,.5); }
  textarea.review-input::placeholder { color:var(--text-muted); }
  .btn-submit {
    margin-top:12px; border:none; border-radius:12px;
    color:#d4eed0; padding:11px 22px; font-size:14px;
    cursor:pointer; font-family:inherit; font-weight:700; transition:all .2s;
  }
  .btn-submit.ready { background:linear-gradient(135deg,var(--green-dim),var(--green-dk)); }
  .btn-submit.disabled { background:rgba(74,124,70,.15); color:#3a5a3a; cursor:default; }
  .submitted-msg { text-align:center; padding:20px; color:var(--green); font-size:15px; }

  /* MAP VIEW */
  #view-map { padding:24px 16px 60px; max-width:760px; margin:0 auto; }
  .map-card {
    background:var(--card); border-radius:16px;
    border:1px solid var(--border); padding:16px;
    display:flex; justify-content:space-between; align-items:center;
    gap:12px; flex-wrap:wrap; margin-bottom:12px;
    transition:border-color .2s;
  }
  .map-card:hover { border-color:var(--border-hi); }
  .map-thumb { width:64px; height:64px; border-radius:10px; object-fit:cover; flex-shrink:0; }
  .map-info-name { color:#d4eed0; font-weight:700; font-size:15px; margin-bottom:3px; }
  .map-info-loc { color:#7a9a78; font-size:12px; margin-bottom:2px; }
  .map-info-coord { color:var(--text-muted); font-size:11px; }
  .map-btns { display:flex; gap:8px; }
  .btn-detail {
    background:rgba(74,124,70,.15); border:1px solid rgba(74,124,70,.3);
    color:var(--green); border-radius:10px; padding:7px 14px;
    font-size:12px; cursor:pointer; font-family:inherit;
  }
  .btn-gmaps {
    background:linear-gradient(135deg,#1d6fa4,var(--blue));
    border:none; color:#fff; border-radius:10px; padding:7px 14px;
    font-size:12px; cursor:pointer; font-family:inherit; font-weight:600;
  }

  @keyframes fadeUp {
    from { opacity:0; transform:translateY(18px); }
    to   { opacity:1; transform:translateY(0); }
  }

  @media (max-width:520px) {
    .action-grid { grid-template-columns:1fr; }
    .stats-grid { grid-template-columns:repeat(2,1fr); }
    .grid { padding:0 12px 40px; }
    header { padding:12px 16px; }
    .hero { padding:36px 16px 24px; }
  }
</style>
</head>
<body>

<header>
  <a class="logo" onclick="showView('home')">
    <span class="logo-icon">⛺</span>
    <div>
      <div class="logo-name">KemMY</div>
      <div class="logo-tagline">Cari · Camp · Connect</div>
    </div>
  </a>
  <nav>
    <button class="nav-btn active" id="nav-home" onclick="showView('home')">🏠 Explore</button>
    <button class="nav-btn" id="nav-map" onclick="showView('map')">🗺️ Peta</button>
  </nav>
</header>

<!-- HOME -->
<div id="view-home" class="view active">
  <div class="hero">
    <div class="hero-eyebrow">🌿 Aplikasi Camping Malaysia</div>
    <h1 class="hero-title">Jelajah Alam,<br>Temui Ketenangan</h1>
    <p class="hero-sub">Cari campsite terbaik, hubungi owner terus &amp; baca ulasan komuniti camper Malaysia.</p>
    <div class="search-wrap">
      <span>🔍</span>
      <input type="text" id="search-input" placeholder="Cari nama atau lokasi campsite..." oninput="renderCards()" />
    </div>
  </div>
  <div class="filters" id="filters"></div>
  <div class="result-count" id="result-count"></div>
  <div class="grid" id="cards-grid"></div>
</div>

<!-- DETAIL -->
<div id="view-detail" class="view">
  <button class="back-btn" onclick="showView('home')">← Kembali ke senarai</button>

  <div class="gallery-main">
    <img id="det-photo" src="" alt="campsite" />
    <div class="gallery-dots" id="det-dots"></div>
    <div class="gallery-label" id="det-photo-label"></div>
  </div>
  <div class="thumbs" id="det-thumbs"></div>

  <div class="info-card">
    <div class="info-top">
      <div>
        <div class="info-name" id="det-name"></div>
        <div class="info-loc" id="det-loc"></div>
        <div class="info-state-badge" id="det-state"></div>
      </div>
      <div style="text-align:right">
        <div class="info-price-big" id="det-price"></div>
        <div class="info-price-unit">per malam / orang</div>
      </div>
    </div>
    <div class="stars-row">
      <div class="stars-display" id="det-stars"></div>
      <span class="rating-val" id="det-rating-val"></span>
      <span class="rating-count" id="det-rating-count"></span>
    </div>
    <p class="info-desc" id="det-desc"></p>

    <div class="section-label">📊 Maklumat Ringkas</div>
    <div class="stats-grid" id="det-stats"></div>

    <div class="section-label" style="margin-top:4px">👥 Sesuai Untuk</div>
    <div class="best-for-row" id="det-best-for"></div>

    <div class="section-label">🏕️ Kemudahan</div>
    <div class="pill-row" id="det-facilities"></div>

    <div class="section-label" style="margin-top:4px">🏷️ Jenis Kem</div>
    <div class="pill-row" id="det-types"></div>
  </div>

  <div class="info-card">
    <div class="section-label">📋 Peraturan Kem</div>
    <ul class="rules-list" id="det-rules"></ul>
  </div>

  <div class="action-grid">
    <button class="btn-map" id="btn-open-map">🗺️ Buka Google Maps</button>
    <button class="btn-contact" onclick="toggleContact()">📱 Hubungi Owner</button>
  </div>

  <div class="contact-box" id="contact-box">
    <div class="contact-owner" id="contact-owner-name"></div>
    <div class="contact-links" id="contact-links"></div>
  </div>

  <div class="info-card">
    <div class="section-label" id="review-section-label"></div>
    <div id="reviews-list"></div>
  </div>

  <div class="info-card">
    <div class="section-label">✍️ Tulis Ulasan Anda</div>
    <div id="write-review-area">
      <div style="color:var(--text-dim);font-size:12px;margin-bottom:6px;">Rating anda:</div>
      <div class="write-stars" id="write-stars"></div>
      <textarea class="review-input" id="review-text" rows="4" placeholder="Kongsi pengalaman camping anda di sini..."></textarea>
      <button class="btn-submit disabled" id="btn-submit-review" onclick="submitReview()">Hantar Ulasan 🌿</button>
    </div>
    <div class="submitted-msg" id="submitted-msg" style="display:none">✅ Terima kasih! Ulasan anda telah dihantar.</div>
  </div>
</div>

<!-- MAP -->
<div id="view-map" class="view">
  <h2 style="color:var(--green);font-family:'Playfair Display',serif;margin-bottom:6px;font-size:22px;">🗺️ Peta Campsite</h2>
  <p style="color:var(--text-dim);font-size:13px;margin-bottom:20px;">Pilih campsite untuk buka Google Maps dengan arah perjalanan.</p>
  <div id="map-list"></div>
</div>

<script>
const typeColors = {
  Jungle:"#2d6a4f", River:"#1d6fa4", Waterfall:"#48cae4",
  Family:"#e07a5f", Highland:"#6d6875", Trekking:"#b5838d",
  Lake:"#457b9d", Fishing:"#f4a261", Beach:"#0096c7",
  Glamping:"#9b5de5", Cave:"#6b4226", Waterpark:"#00b4d8"
};

const campsites = [
  {
    id: 1,
    name: "Hutan Lipur Lentang",
    location: "Bentong, Pahang",
    state: "Pahang",
    lat: 3.5234, lng: 101.9108,
    type: ["Jungle","River"],
    price: 15,
    capacity: "200 orang",
    area: "5 ekar",
    openHours: "8am – 10pm",
    rating: 4.7, totalReviews: 84,
    bestFor: ["Keluarga","Kumpulan Besar","Pengakap"],
    owner: { name: "Pak Azmi", phone: "0123456789", whatsapp: "60123456789" },
    facilities: ["Tandas","Shower","BBQ Pit","Sungai","Parking","Khemah Sewa","Lampu Kawasan"],
    rules: ["Dilarang bising selepas 11pm","Sampah mesti dibuang di tempat yang ditetapkan","Dilarang membawa alkohol","Api unggun hanya di kawasan yang ditetapkan","Kanak-kanak mesti diawasi di tepi sungai"],
    description: "Hutan Lipur Lentang adalah destinasi alam semulajadi yang tenang di kaki Gunung Benom. Dengan sungai yang jernih dan denai hiking yang menakjubkan, campsite ini sesuai untuk keluarga dan kumpulan besar yang ingin menikmati keindahan alam Pahang. Pokok-pokok berusia ratusan tahun mengelilingi kawasan perkhemahan, memberikan teduhan semula jadi sepanjang hari.",
    photos: [
      "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=800&q=80",
      "https://images.unsplash.com/photo-1510312305653-8ed496efae75?w=800&q=80",
      "https://images.unsplash.com/photo-1563299796-b729d4e43ad9?w=800&q=80"
    ],
    reviews: [
      { user:"Hafizuddin R.", avatar:"H", rating:5, comment:"Tempat yang sangat cantik! Sungai jernih dan udara segar. Kami akan datang lagi!", date:"2 hari lalu" },
      { user:"Siti Aisyah M.", avatar:"S", rating:4, comment:"Bagus tapi toilet perlu dinaik taraf sikit. Overall best!", date:"1 minggu lalu" },
      { user:"Razif K.", avatar:"R", rating:5, comment:"Perfect untuk escape dari bandar. Owner friendly dan helpful.", date:"2 minggu lalu" }
    ]
  },
  {
    id: 2,
    name: "Kem Sungai Gabai",
    location: "Hulu Langat, Selangor",
    state: "Selangor",
    lat: 3.0789, lng: 101.8756,
    type: ["Waterfall","Family"],
    price: 20,
    capacity: "300 orang",
    area: "8 ekar",
    openHours: "7am – 11pm",
    rating: 4.5, totalReviews: 122,
    bestFor: ["Keluarga","Team Building","Pelancong"],
    owner: { name: "Cik Rohani", phone: "0198887766", whatsapp: "60198887766" },
    facilities: ["Chalet","Kafeteria","Air Terjun","Wifi","Parking","Gelanggang Sukan","Musolla"],
    rules: ["Waktu senyap 12 tengah malam","Tiada api unggun berhampiran pokok","Pakaian sopan diperlukan","Dilarang berburu binatang liar","Booking diperlukan untuk kumpulan >50 orang"],
    description: "Terletak berhampiran dengan Air Terjun Gabai yang terkenal, campsite ini menawarkan pengalaman alam semulajadi yang lengkap dengan kemudahan moden. Airnya sejuk dan segar, sesuai untuk berendam dan bersantai. Kafeteria menyediakan makanan tempatan yang lazat, menjadikan ia pilihan sempurna untuk aktiviti keluarga dan team building korporat.",
    photos: [
      "https://images.unsplash.com/photo-1537225228614-56cc3556d7ed?w=800&q=80",
      "https://images.unsplash.com/photo-1496080174650-637e3f22fa03?w=800&q=80",
      "https://images.unsplash.com/photo-1533240332313-0db49b459ad6?w=800&q=80"
    ],
    reviews: [
      { user:"Amirul F.", avatar:"A", rating:5, comment:"Air terjun memang power! Sangat sesuai untuk bawa anak-anak.", date:"3 hari lalu" },
      { user:"Nurul H.", avatar:"N", rating:4, comment:"Kawasan bersih dan owner cepat respond. Recommended!", date:"5 hari lalu" },
      { user:"Benny T.", avatar:"B", rating:4, comment:"Makanan di kafeteria sedap. Nasi lemak pagi memang terbaik!", date:"2 minggu lalu" }
    ]
  },
  {
    id: 3,
    name: "Kem Rimba Janda Baik",
    location: "Bentong, Pahang",
    state: "Pahang",
    lat: 3.6012, lng: 101.8234,
    type: ["Highland","Trekking","Glamping"],
    price: 45,
    capacity: "80 orang",
    area: "3 ekar",
    openHours: "24 jam",
    rating: 4.9, totalReviews: 56,
    bestFor: ["Pasangan","Fotografi","Pencinta Alam"],
    owner: { name: "Encik Farid", phone: "0177654321", whatsapp: "60177654321" },
    facilities: ["Glamping Tent","Bonfire","Jungle Trek","Photography Spot","Breakfast Included","Hot Shower","Hammock"],
    rules: ["No plastic bags","Dilarang merokok dalam tent","Generator dibenarkan hingga 10pm","Haiwan peliharaan tidak dibenarkan","Minimum 2 malam pada hujung minggu"],
    description: "Pengalaman glamping premium di kawasan highland Janda Baik dengan pemandangan gunung yang memukau. Setiap tent dilengkapi dengan katil, lampu suluh, dan sarapan pagi percuma. Pada waktu malam, langit dipenuhi bintang yang tiada tandingannya. Sesuai untuk pasangan yang mencari pengalaman romantik atau fotografer yang mahukan shot alam semulajadi terbaik.",
    photos: [
      "https://images.unsplash.com/photo-1478131143081-80f7f84ca84d?w=800&q=80",
      "https://images.unsplash.com/photo-1445308394109-4ec2920981b1?w=800&q=80",
      "https://images.unsplash.com/photo-1520962922320-2038eebab146?w=800&q=80"
    ],
    reviews: [
      { user:"Darwisyah Z.", avatar:"D", rating:5, comment:"View dia luar biasa! Malam nampak bintang penuh. Terbaik!", date:"1 hari lalu" },
      { user:"Khairul A.", avatar:"K", rating:5, comment:"Glamping experience yang sangat worth it. Akan datang lagi!", date:"4 hari lalu" },
      { user:"Melissa C.", avatar:"M", rating:5, comment:"Sarapan pagi sedap, tent selesa. Perfect honeymoon spot!", date:"1 minggu lalu" }
    ]
  },
  {
    id: 4,
    name: "Kem Tasik Banding",
    location: "Gerik, Perak",
    state: "Perak",
    lat: 5.0234, lng: 101.1234,
    type: ["Lake","Fishing"],
    price: 18,
    capacity: "150 orang",
    area: "10 ekar",
    openHours: "6am – 10pm",
    rating: 4.3, totalReviews: 38,
    bestFor: ["Pemancing","Pencinta Alam","Kumpulan Lelaki"],
    owner: { name: "Tok Wan Yusof", phone: "0165559988", whatsapp: "60165559988" },
    facilities: ["Bot Sewa","Pancing","Dapur Awam","Hammock","Parking","Tempat Letak Perahu","Kedai Runcit"],
    rules: ["Lesen memancing diperlukan","Dilarang menggunakan jaring","Ikan yang ditangkap mestilah dilepaskan semula (catch & release)","Waktu memancing: 6am – 6pm","Dilarang buang sampah ke dalam tasik"],
    description: "Kem Tasik Banding terletak di tepi Tasik Royal Belum, salah satu hutan hujan tertua di dunia. Tempat ini ideal untuk pemancing yang ingin menikmati ketenangan alam sambil memancing pelbagai jenis ikan air tawar. Bot sewa tersedia untuk menjelajahi tasik yang luas. Pemandangan matahari terbenam di atas tasik adalah antara yang paling indah di Malaysia.",
    photos: [
      "https://images.unsplash.com/photo-1501854140801-50d01698950b?w=800&q=80",
      "https://images.unsplash.com/photo-1508193638397-1c4234db14d8?w=800&q=80",
      "https://images.unsplash.com/photo-1571863533956-01c88e79957e?w=800&q=80"
    ],
    reviews: [
      { user:"Johari M.", avatar:"J", rating:4, comment:"Tasik cantik, ikan pun banyak! Tok Wan sangat friendly.", date:"1 minggu lalu" },
      { user:"Ramli S.", avatar:"R", rating:4, comment:"Tangkap ikan Toman besar! Pengalaman yang tak terlupakan.", date:"3 minggu lalu" }
    ]
  },
  {
    id: 5,
    name: "Kem Pantai Cherating",
    location: "Cherating, Pahang",
    state: "Pahang",
    lat: 4.0789, lng: 103.3876,
    type: ["Beach","Family"],
    price: 25,
    capacity: "250 orang",
    area: "6 ekar",
    openHours: "24 jam",
    rating: 4.6, totalReviews: 93,
    bestFor: ["Keluarga","Sukan Air","Pasangan"],
    owner: { name: "Abang Zaki", phone: "0134445566", whatsapp: "60134445566" },
    facilities: ["Tepi Pantai","Bilik Mandi","BBQ Pit","Kayak Sewa","Parking","Wifi","Cafeteria","Surau"],
    rules: ["Dilarang berenang selepas 7pm","Jaga kebersihan pantai","Dilarang bawa kenderaan ke atas pasir","Kayak hanya boleh disewa pada waktu siang","Dilarang bawa haiwan peliharaan ke pantai"],
    description: "Kem Pantai Cherating menawarkan pengalaman camping terus di tepi pantai yang indah dengan ombak yang tenang. Sesuai untuk aktiviti sukan air seperti kayak, snorkeling, dan berjemur. Pada musim tertentu, boleh melihat penyu bertelur di pantai berhampiran. Matahari terbenam di Cherating adalah antara yang paling cantik di Pantai Timur Malaysia.",
    photos: [
      "https://images.unsplash.com/photo-1507525428034-b723cf961d3e?w=800&q=80",
      "https://images.unsplash.com/photo-1519046904884-53103b34b206?w=800&q=80",
      "https://images.unsplash.com/photo-1473116763249-2faaef81ccda?w=800&q=80"
    ],
    reviews: [
      { user:"Fatimah Z.", avatar:"F", rating:5, comment:"Pantai yang cantik! Ombak tenang, sesuai untuk anak-anak.", date:"2 hari lalu" },
      { user:"David L.", avatar:"D", rating:5, comment:"Best camping experience! Kayak di waktu pagi sangat best.", date:"1 minggu lalu" },
      { user:"Zuraida M.", avatar:"Z", rating:4, comment:"Matahari terbenam sangat cantik. Owner baik dan helpful.", date:"2 minggu lalu" }
    ]
  },
  {
    id: 6,
    name: "Kem Gunung Ledang",
    location: "Tangkak, Johor",
    state: "Johor",
    lat: 2.3678, lng: 102.6123,
    type: ["Highland","Trekking","Jungle"],
    price: 30,
    capacity: "100 orang",
    area: "4 ekar",
    openHours: "7am – 9pm",
    rating: 4.8, totalReviews: 71,
    bestFor: ["Pendaki","Pencinta Alam","Kumpulan Aktif"],
    owner: { name: "Pak Rashid", phone: "0167778899", whatsapp: "60167778899" },
    facilities: ["Basecamp","Shower Sejuk","Kedai Peralatan","Guide Tersedia","Dapur","Parking","Klinik Kecemasan"],
    rules: ["Mesti daftar masuk sebelum 3pm","Mendaki hanya bersama pemandu berlesen","Bawa keluar semua sampah anda","Dilarang memetik tumbuhan","Lapor kepada pihak berkuasa jika rasa tidak sihat"],
    description: "Kem Gunung Ledang adalah titik permulaan bagi pendaki yang ingin menakluki Gunung Ledang, gunung bersejarah yang dikaitkan dengan legenda Puteri Gunung Ledang. Kemudahan basecamp yang lengkap termasuk panduan berpengalaman dan klinik kecemasan untuk keselamatan pendaki. Pemandangan dari puncak pada ketinggian 1,276m adalah ganjaran terbaik bagi pendaki yang berjaya.",
    photos: [
      "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800&q=80",
      "https://images.unsplash.com/photo-1551632811-561732d1e306?w=800&q=80",
      "https://images.unsplash.com/photo-1483728642387-6c3bdd6c93e5?w=800&q=80"
    ],
    reviews: [
      { user:"Hafifi A.", avatar:"H", rating:5, comment:"Pengalaman mendaki yang luar biasa! Guide sangat membantu.", date:"3 hari lalu" },
      { user:"Anis R.", avatar:"A", rating:5, comment:"Basecamp bersih dan selesa. Pemandangan dari puncak memang tak terlupa!", date:"1 minggu lalu" },
      { user:"Syahril M.", avatar:"S", rating:4, comment:"Laluan mendaki mencabar tapi berbaloi. Akan datang lagi!", date:"3 minggu lalu" }
    ]
  },
  {
    id: 7,
    name: "Kem Sungai Sedim",
    location: "Kulim, Kedah",
    state: "Kedah",
    lat: 5.5123, lng: 100.7234,
    type: ["River","Jungle","Trekking"],
    price: 12,
    capacity: "180 orang",
    area: "7 ekar",
    openHours: "8am – 10pm",
    rating: 4.4, totalReviews: 47,
    bestFor: ["Keluarga","Pelajar","Kumpulan Besar"],
    owner: { name: "Encik Hasrul", phone: "0114443322", whatsapp: "60114443322" },
    facilities: ["River Tubing","Canopy Walk","Tandas","Shower","BBQ","Parking","Khemah Sewa","Kedai Makanan"],
    rules: ["Pelampung wajib semasa river tubing","Dilarang lari di atas jambatan canopy","Waktu senyap 11pm","Dilarang membuang sampah ke dalam sungai","Kanak-kanak bawah 12 tahun mesti disertai dewasa"],
    description: "Kem Sungai Sedim terkenal dengan aktiviti river tubing yang mendebarkan dan canopy walk yang menakjubkan. Sungai Sedim yang jernih mengalir melalui hutan dara, menjadikannya tempat yang sempurna untuk menikmati keindahan alam semulajadi Kedah. Tarikan utama adalah canopy walk sepanjang 1.3km yang menghubungkan pokok-pokok gergasi di ketinggian 30 meter.",
    photos: [
      "https://images.unsplash.com/photo-1519681393784-d120267933ba?w=800&q=80",
      "https://images.unsplash.com/photo-1472396961693-142e6e269027?w=800&q=80",
      "https://images.unsplash.com/photo-1448375240586-882707db888b?w=800&q=80"
    ],
    reviews: [
      { user:"Kamariah B.", avatar:"K", rating:4, comment:"River tubing sangat best! Anak-anak suka sangat.", date:"4 hari lalu" },
      { user:"Izzatul H.", avatar:"I", rating:5, comment:"Canopy walk memang mengujakan! Pemandangan dari atas sangat cantik.", date:"2 minggu lalu" }
    ]
  },
  {
    id: 8,
    name: "Kem Cameron Highlands",
    location: "Brinchang, Pahang",
    state: "Pahang",
    lat: 4.5234, lng: 101.3876,
    type: ["Highland","Trekking","Glamping"],
    price: 55,
    capacity: "60 orang",
    area: "2 ekar",
    openHours: "24 jam",
    rating: 4.7, totalReviews: 108,
    bestFor: ["Pasangan","Keluarga","Pelancong Antarabangsa"],
    owner: { name: "Kak Suraya", phone: "0189996677", whatsapp: "60189996677" },
    facilities: ["Glamping Dome","Heater","Strawberry Farm","Tea Plantation Tour","Hot Shower","Breakfast","Wifi","Parking"],
    rules: ["Suhu malam boleh turun ke 14°C, bawa pakaian tebal","Check-in: 3pm, Check-out: 12pm","Dilarang memetik strawberi tanpa bayaran","Jaga kebersihan kawasan","Haiwan peliharaan tidak dibenarkan"],
    description: "Kem Cameron Highlands menawarkan pengalaman glamping yang unik di kawasan ladang teh yang ikonik. Menginap dalam dome transparent yang membolehkan anda melihat bintang dari dalam bilik tidur. Suhu sejuk Cameron Highlands (14-25°C) menjadikannya pelarian sempurna dari panas bandar. Lawatan ke ladang strawberi dan ladang teh termasuk dalam pakej.",
    photos: [
      "https://images.unsplash.com/photo-1508739773434-c26b3d09e071?w=800&q=80",
      "https://images.unsplash.com/photo-1444492417251-9c84a5fa18e0?w=800&q=80",
      "https://images.unsplash.com/photo-1501854140801-50d01698950b?w=800&q=80"
    ],
    reviews: [
      { user:"Priya S.", avatar:"P", rating:5, comment:"Most beautiful camping experience! The dome under stars is magical.", date:"1 hari lalu" },
      { user:"Rohana A.", avatar:"R", rating:5, comment:"Sejuk sangat tapi best! Strawberry fresh dari ladang sedap.", date:"5 hari lalu" },
      { user:"James T.", avatar:"J", rating:4, comment:"Pemandangan ladang teh memang cantik. Breakfast sedap!", date:"2 minggu lalu" }
    ]
  },
  {
    id: 9,
    name: "Kem Air Terjun Sungai Chiling",
    location: "Kuala Kubu Bharu, Selangor",
    state: "Selangor",
    lat: 3.5678, lng: 101.6543,
    type: ["Waterfall","River","Jungle"],
    price: 10,
    capacity: "120 orang",
    area: "3 ekar",
    openHours: "7am – 6pm",
    rating: 4.5, totalReviews: 64,
    bestFor: ["Pencinta Alam","Backpacker","Kumpulan Muda"],
    owner: { name: "Pak Long Idris", phone: "0122221133", whatsapp: "60122221133" },
    facilities: ["Air Terjun","Sungai Jernih","Tandas Asas","Parking","Jambatan Gantung","Kolam Semulajadi"],
    rules: ["Tiada kemudahan elektrik","Bawa makanan sendiri","Dilarang bising (kawasan konservasi)","Perlu menyeberangi sungai 7 kali untuk sampai","Dilarang membuat api"],
    description: "Sungai Chiling adalah permata tersembunyi Selangor yang memerlukan 7 kali penyeberangan sungai untuk sampai ke air terjun utama. Perjalanan ke sana adalah sebahagian daripada pengalaman — meredah sungai, hutan primer, dan alam liar. Air terjun yang tinggi mencurah ke kolam semulajadi yang jernih dan sejuk. Tempat yang paling authentic untuk camper sejati.",
    photos: [
      "https://images.unsplash.com/photo-1432405972618-c60b0225b8f9?w=800&q=80",
      "https://images.unsplash.com/photo-1455218873509-8097305ee378?w=800&q=80",
      "https://images.unsplash.com/photo-1547970810-dc1eac37d174?w=800&q=80"
    ],
    reviews: [
      { user:"Asyraf M.", avatar:"A", rating:5, comment:"Perjalanan mencabar tapi berbaloi 100%! Air terjun gergasi!", date:"2 hari lalu" },
      { user:"Linda K.", avatar:"L", rating:4, comment:"Authentic jungle experience. Bawa kasut yang sesuai untuk sungai!", date:"1 minggu lalu" }
    ]
  },
  {
    id: 10,
    name: "Kem Gua Tempurung",
    location: "Gopeng, Perak",
    state: "Perak",
    lat: 4.3789, lng: 101.1456,
    type: ["Cave","Jungle","Trekking"],
    price: 22,
    capacity: "90 orang",
    area: "4 ekar",
    openHours: "8am – 8pm",
    rating: 4.4, totalReviews: 52,
    bestFor: ["Pencinta Cabaran","Kumpulan Aktif","Pelajar"],
    owner: { name: "Encik Zainudin", phone: "0155667788", whatsapp: "60155667788" },
    facilities: ["Gua Tour","Helmet & Torch","Shower","Parking","Dapur","Camping Ground","Khemah Sewa"],
    rules: ["Wajib memakai helmet dalam gua","Dilarang masuk gua tanpa pemandu","Jangan sentuh stalaktit/stalagmit","Bawa cahaya tambahan","Tidak sesuai untuk claustrophobic"],
    description: "Kem Gua Tempurung terletak bersebelahan dengan Gua Tempurung, salah satu gua terbesar di Semenanjung Malaysia. Pengalaman menjelajahi gua sepanjang 3km dengan stalaktit dan stalagmit yang menakjubkan adalah tidak ternilai. Terdapat 5 peringkat lawatan gua dari mudah hingga ekstrem. Selepas menjelajah gua, relaks di kawasan perkhemahan yang tenang di pinggir hutan.",
    photos: [
      "https://images.unsplash.com/photo-1520206183501-b80df61043c2?w=800&q=80",
      "https://images.unsplash.com/photo-1578662996442-48f60103fc96?w=800&q=80",
      "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?w=800&q=80"
    ],
    reviews: [
      { user:"Fadzillah N.", avatar:"F", rating:5, comment:"Gua yang menakjubkan! Guide sangat profesional dan selamat.", date:"6 hari lalu" },
      { user:"Victor T.", avatar:"V", rating:4, comment:"Unique experience! Cave exploration memang mendebarkan.", date:"3 minggu lalu" }
    ]
  }
];

let currentFilter = "All";
let currentSite   = null;
let currentPhoto  = 0;
let writeRating   = 0;
let contactOpen   = false;

function showView(name) {
  document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('view-' + name).classList.add('active');
  const navBtn = document.getElementById('nav-' + name);
  if (navBtn) navBtn.classList.add('active');
  if (name === 'home') renderCards();
  if (name === 'map')  renderMapList();
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function buildFilters() {
  const allTypes = ["All","Jungle","River","Waterfall","Family","Highland","Trekking","Lake","Fishing","Beach","Glamping","Cave"];
  const wrap = document.getElementById('filters');
  wrap.innerHTML = allTypes.map(t => {
    const isActive = t === currentFilter;
    const color = typeColors[t] || 'var(--green)';
    let style = '';
    if (t === 'All') {
      style = isActive ? 'border-color:var(--green);color:var(--green);background:rgba(74,124,70,.2);' : '';
    } else {
      style = `border-color:${color}44;${isActive ? `background:${color}22;color:${color};` : ''}`;
    }
    return `<button class="filter-btn ${isActive ? 'active' : ''}" style="${style}" onclick="setFilter('${t}')">
      ${t === 'All' ? '🌍 Semua' : t}
    </button>`;
  }).join('');
}

function setFilter(type) {
  currentFilter = type;
  buildFilters();
  renderCards();
}

function renderCards() {
  buildFilters();
  const q = (document.getElementById('search-input').value || '').toLowerCase();
  const filtered = campsites.filter(c => {
    const matchQ = c.name.toLowerCase().includes(q) || c.location.toLowerCase().includes(q) || c.state.toLowerCase().includes(q);
    const matchT = currentFilter === 'All' || c.type.includes(currentFilter);
    return matchQ && matchT;
  });
  document.getElementById('result-count').textContent = `${filtered.length} campsite dijumpai`;
  document.getElementById('cards-grid').innerHTML = filtered.map((s, i) => `
    <div class="card" style="animation-delay:${i*0.05}s" onclick="openDetail(${s.id})">
      <div class="card-img-wrap">
        <img src="${s.photos[0]}" alt="${s.name}" loading="lazy" />
        <div class="card-img-overlay"></div>
        <div class="card-rating">
          <span class="star-icon">★</span>
          <span style="color:var(--text);font-weight:700">${s.rating}</span>
          <span style="color:#8a8a8a">(${s.totalReviews})</span>
        </div>
        <div class="card-types">
          ${s.type.map(t=>`<span class="type-badge" style="background:${typeColors[t]||'#4a7c46'}cc">${t}</span>`).join('')}
        </div>
      </div>
      <div class="card-body">
        <div class="card-name">${s.name}</div>
        <div class="card-loc">📍 ${s.location}</div>
        <div class="card-meta-row">
          <span class="card-meta-item">👥 ${s.capacity}</span>
          <span class="card-meta-item">⏰ ${s.openHours}</span>
          <span class="card-meta-item">📐 ${s.area}</span>
        </div>
        <div class="card-desc">${s.description.substring(0,90)}...</div>
        <div class="pill-row">
          ${s.facilities.slice(0,3).map(f=>`<span class="pill">${f}</span>`).join('')}
          ${s.facilities.length>3?`<span style="color:var(--text-muted);font-size:10px">+${s.facilities.length-3} lagi</span>`:''}
        </div>
        <div class="card-footer">
          <div><span class="price-main">RM${s.price}</span><span class="price-sub">/malam</span></div>
          <button class="btn-primary" onclick="event.stopPropagation();openDetail(${s.id})">Lihat Lebih →</button>
        </div>
      </div>
    </div>`).join('');
}

function openDetail(id) {
  currentSite  = campsites.find(c => c.id === id);
  currentPhoto = 0;
  contactOpen  = false;
  writeRating  = 0;
  document.getElementById('contact-box').classList.remove('open');
  document.getElementById('submitted-msg').style.display = 'none';
  document.getElementById('write-review-area').style.display = 'block';
  document.getElementById('review-text').value = '';

  const s = currentSite;
  document.getElementById('det-name').textContent   = s.name;
  document.getElementById('det-loc').textContent    = '📍 ' + s.location;
  document.getElementById('det-state').textContent  = '🏳️ ' + s.state;
  document.getElementById('det-price').textContent  = 'RM' + s.price;
  document.getElementById('det-desc').textContent   = s.description;
  document.getElementById('det-stars').textContent  = '★'.repeat(Math.round(s.rating)) + '☆'.repeat(5-Math.round(s.rating));
  document.getElementById('det-rating-val').textContent   = s.rating;
  document.getElementById('det-rating-count').textContent = `(${s.totalReviews} ulasan)`;
  document.getElementById('review-section-label').textContent = `⭐ Ulasan Campers (${s.reviews.length})`;

  document.getElementById('det-stats').innerHTML = `
    <div class="stat-box"><div class="stat-val">${s.capacity}</div><div class="stat-label">Kapasiti</div></div>
    <div class="stat-box"><div class="stat-val">${s.area}</div><div class="stat-label">Keluasan</div></div>
    <div class="stat-box"><div class="stat-val">${s.openHours}</div><div class="stat-label">Waktu Operasi</div></div>
  `;

  document.getElementById('det-best-for').innerHTML =
    s.bestFor.map(b=>`<span class="best-for-tag">${b}</span>`).join('');

  document.getElementById('det-types').innerHTML =
    s.type.map(t=>`<span class="pill" style="background:${typeColors[t]||'#4a7c46'}22;border-color:${typeColors[t]||'#4a7c46'}66;color:${typeColors[t]||'var(--green)'};">${t}</span>`).join('');

  document.getElementById('det-facilities').innerHTML =
    s.facilities.map(f=>`<span class="pill">${f}</span>`).join('');

  document.getElementById('det-rules').innerHTML =
    s.rules.map(r=>`<li><span>⚠️</span><span>${r}</span></li>`).join('');

  document.getElementById('contact-owner-name').textContent = '👤 ' + s.owner.name;
  document.getElementById('contact-links').innerHTML = `
    <a class="link-call" href="tel:${s.owner.phone}">📞 ${s.owner.phone}</a>
    <a class="link-wa" href="https://wa.me/${s.owner.whatsapp}?text=Salam%2C%20saya%20berminat%20dengan%20campsite%20${encodeURIComponent(s.name)}" target="_blank" rel="noreferrer">💬 WhatsApp Terus</a>`;

  document.getElementById('btn-open-map').onclick = () =>
    window.open(`https://www.google.com/maps/search/?api=1&query=${s.lat},${s.lng}`, '_blank');

  renderGallery();
  renderReviews();
  renderWriteStars();
  document.getElementById('review-text').addEventListener('input', updateSubmitBtn);

  showView('detail');
}

function renderGallery() {
  const s = currentSite;
  document.getElementById('det-photo').src = s.photos[currentPhoto];
  document.getElementById('det-photo-label').textContent = `📸 ${currentPhoto+1} / ${s.photos.length}`;
  document.getElementById('det-dots').innerHTML = s.photos.map((_,i)=>
    `<button class="dot ${i===currentPhoto?'active':''}" onclick="setPhoto(${i})"></button>`).join('');
  document.getElementById('det-thumbs').innerHTML = s.photos.map((p,i)=>
    `<img class="thumb ${i===currentPhoto?'active':''}" src="${p}" alt="" onclick="setPhoto(${i})" />`).join('');
}

function setPhoto(i) { currentPhoto = i; renderGallery(); }

function renderReviews() {
  document.getElementById('reviews-list').innerHTML =
    currentSite.reviews.map(r=>`
      <div class="review-item">
        <div class="avatar">${r.avatar}</div>
        <div style="flex:1">
          <div class="rv-meta">
            <span class="rv-user">${r.user}</span>
            <span class="rv-date">${r.date}</span>
          </div>
          <div class="rv-stars">${'★'.repeat(r.rating)}${'☆'.repeat(5-r.rating)}</div>
          <div class="rv-comment">${r.comment}</div>
        </div>
      </div>`).join('');
}

function renderWriteStars() {
  document.getElementById('write-stars').innerHTML = [1,2,3,4,5].map(n=>
    `<button class="w-star ${writeRating>=n?'lit':''}" onclick="setWriteRating(${n})">★</button>`).join('');
}

function setWriteRating(n) { writeRating = n; renderWriteStars(); updateSubmitBtn(); }

function updateSubmitBtn() {
  const btn = document.getElementById('btn-submit-review');
  const hasComment = document.getElementById('review-text').value.trim().length > 0;
  btn.className = (writeRating && hasComment) ? 'btn-submit ready' : 'btn-submit disabled';
}

function submitReview() {
  const comment = document.getElementById('review-text').value.trim();
  if (!writeRating || !comment) return;
  document.getElementById('write-review-area').style.display = 'none';
  document.getElementById('submitted-msg').style.display = 'block';
}

function toggleContact() {
  contactOpen = !contactOpen;
  const box = document.getElementById('contact-box');
  contactOpen ? box.classList.add('open') : box.classList.remove('open');
}

function renderMapList() {
  document.getElementById('map-list').innerHTML = campsites.map(s=>`
    <div class="map-card">
      <img class="map-thumb" src="${s.photos[0]}" alt="${s.name}" loading="lazy" />
      <div style="flex:1">
        <div class="map-info-name">${s.name}</div>
        <div class="map-info-loc">📍 ${s.location}</div>
        <div class="map-info-coord">🧭 ${s.lat.toFixed(4)}°N, ${s.lng.toFixed(4)}°E</div>
      </div>
      <div class="map-btns">
        <button class="btn-detail" onclick="openDetail(${s.id})">Detail</button>
        <button class="btn-gmaps" onclick="window.open('https://www.google.com/maps/search/?api=1&query=${s.lat},${s.lng}','_blank')">🗺️ Maps</button>
      </div>
    </div>`).join('');
}

renderCards();
</script>
</body>
</html>
