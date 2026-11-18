<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>Thiệp Mời Lễ Tốt Nghiệp - Lâm Thị Quy</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-pink: #FFF0F5;
      --card-bg: #FFFDFE;
      --primary-pink: #FF6B9D;
      --dark-pink: #D6336C;
      --soft-pink: #FFD6E5;
      --pastel-yellow: #FFF3BF;
      --text-main: #5C3A47;
      --text-muted: #8E6474;
    }

    /* ================================
       MOBILE FIRST OPTIMIZATION
    ================================ */

    /* Tránh tràn ngang */
    html {
      width: 100%;
      overflow-x: hidden;
      -webkit-text-size-adjust: 100%;
      scroll-behavior: smooth;
    }

    body {
      width: 100%;
      min-width: 320px;
      overflow-x: hidden;
      -webkit-tap-highlight-color: transparent;
      font-family: 'Quicksand', sans-serif;
      background-color: var(--bg-pink);
      background-image: radial-gradient(#FFC2D6 1.5px, transparent 1.5px), radial-gradient(#FFE0EB 1.5px, #FFF0F5 1.5px);
      background-size: 36px 36px;
      background-position: 0 0, 18px 18px;
      color: var(--text-main);
      min-height: 100vh;
      position: relative;
    }

    /* Tối ưu vùng an toàn của điện thoại */
    .container {
      width: 100%;
      max-width: 640px;
      margin: 0 auto;
      padding: 24px 14px calc(40px + env(safe-area-inset-bottom));
      position: relative;
      z-index: 1;
    }

    /* Card co giãn */
    .card {
      background: var(--card-bg);
      border: 2.5px solid #FFC2D6;
      width: 100%;
      padding: clamp(20px, 5vw, 32px) clamp(14px, 4vw, 24px);
      border-radius: 26px;
      margin-bottom: 18px;
      box-shadow: 0 14px 36px rgba(255, 107, 157, 0.16);
      text-align: center;
      position: relative;
    }

    .badge {
      display: inline-block;
      background: var(--soft-pink);
      color: var(--dark-pink);
      font-weight: 700;
      font-size: 0.82rem;
      letter-spacing: 1px;
      text-transform: uppercase;
      padding: 6px 16px;
      border-radius: 999px;
      margin-bottom: 14px;
    }

    /* Tiêu đề tự co giãn */
    .main-heading {
      font-family: 'Dancing Script', cursive;
      font-size: clamp(2.1rem, 9vw, 2.8rem);
      line-height: 1.2;
      color: var(--dark-pink);
      margin-bottom: 6px;
    }

    .graduate-name {
      font-size: clamp(1.35rem, 6vw, 1.85rem);
      font-weight: 700;
      color: #FF4D88;
      margin: 10px 0 18px;
      text-shadow: 0 2px 10px rgba(255, 107, 157, 0.2);
      overflow-wrap: anywhere;
    }

    .envelope-title {
      font-family: 'Dancing Script', cursive;
      font-size: clamp(1.8rem, 8vw, 2.2rem);
      color: var(--dark-pink);
      margin-bottom: 8px;
    }

    /* Thông tin buổi lễ */
    .core-info {
      background: #FFF5F8;
      border: 2px dashed #FF9EBB;
      border-radius: 22px;
      padding: 16px 10px;
      margin: 18px 0;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .info-row {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      font-size: clamp(0.85rem, 3.6vw, 1.05rem);
      font-weight: 600;
      line-height: 1.5;
      color: var(--text-main);
      flex-wrap: wrap;
      text-align: center;
    }

    .info-icon {
      font-size: 1.3rem;
    }

    /* Countdown */
    .countdown-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: clamp(5px, 2vw, 10px);
      margin: 22px 0;
    }

    .time-box {
      background: linear-gradient(180deg, #FFF 0%, #FFE6EF 100%);
      border: 2px solid #FFB3C6;
      min-width: 0;
      padding: 12px 3px;
      border-radius: 14px;
    }

    .time-num {
      font-size: clamp(1.1rem, 5.5vw, 1.55rem);
      font-weight: 700;
      color: var(--dark-pink);
      display: block;
    }

    .time-label {
      font-size: clamp(0.65rem, 2.8vw, 0.78rem);
      font-weight: 600;
      color: var(--text-muted);
    }

    /* Nút bấm thân thiện với cảm ứng */
    button,
    .btn-pink,
    .btn-outline,
    select {
      min-height: 46px;
      touch-action: manipulation;
    }

    .btn-group {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
      margin-top: 14px;
    }

    .btn-pink {
      background: var(--primary-pink);
      color: #fff;
      border: none;
      border-radius: 999px;
      justify-content: center;
      max-width: 100%;
      padding: 12px 17px;
      font-family: 'Quicksand', sans-serif;
      font-weight: 700;
      font-size: 0.88rem;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      box-shadow: 0 6px 14px rgba(255, 107, 157, 0.28);
      transition: transform 0.2s, background 0.2s;
    }

    .btn-pink:hover {
      background: #FF4D88;
      transform: translateY(-2px);
    }

    .btn-outline {
      background: #fff;
      color: var(--dark-pink);
      border: 2px solid #FF9EBB;
      border-radius: 999px;
      justify-content: center;
      max-width: 100%;
      padding: 12px 17px;
      font-family: 'Quicksand', sans-serif;
      font-weight: 700;
      font-size: 0.88rem;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: transform 0.2s, background 0.2s;
    }

    .btn-outline:hover {
      background: #FFF0F5;
      transform: translateY(-2px);
    }

    /* Nút nhạc */
    .music-btn {
      position: fixed;
      top: calc(10px + env(safe-area-inset-top));
      right: 10px;
      z-index: 1001;
      background: #fff;
      border: 2px solid #FFB3C6;
      color: var(--dark-pink);
      border-radius: 999px;
      padding: 9px 13px;
      min-height: 42px;
      font-family: 'Quicksand', sans-serif;
      font-weight: 700;
      font-size: 0.78rem;
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(255, 107, 157, 0.2);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    /* Phong bì */
    #envelope-overlay {
      position: fixed;
      inset: 0;
      background: linear-gradient(135deg, #FFE3EC 0%, #FFC2D6 100%);
      z-index: 1000;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
      transition: opacity 0.7s ease, visibility 0.7s ease;
    }

    #envelope-overlay.hidden {
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
    }

    .envelope-box {
      background: #FFF;
      border: 3px solid #FF9EBB;
      width: 100%;
      max-width: 400px;
      padding: 30px 20px;
      border-radius: 24px;
      text-align: center;
      box-shadow: 0 18px 40px rgba(255, 107, 157, 0.25);
      animation: bounceSlow 2.5s infinite ease-in-out;
    }

    @keyframes bounceSlow {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }

    .grad-icon {
      font-size: 56px;
      margin-bottom: 12px;
      display: inline-block;
    }

    .envelope-sub {
      font-size: 0.95rem;
      color: var(--text-muted);
      margin-bottom: 24px;
    }

    .btn-open {
      background: linear-gradient(135deg, #FF75A0 0%, #FF4D88 100%);
      color: #fff;
      border: none;
      padding: 14px 32px;
      border-radius: 999px;
      font-family: 'Quicksand', sans-serif;
      font-weight: 700;
      font-size: 1.05rem;
      cursor: pointer;
      box-shadow: 0 8px 20px rgba(255, 77, 136, 0.35);
      transition: transform 0.2s, box-shadow 0.2s;
      min-height: 48px;
      max-width: 100%;
      width: 100%;
    }

    .btn-open:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 25px rgba(255, 77, 136, 0.45);
    }

    .mobile-tip {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-top: 16px;
      line-height: 1.4;
    }

    /* Bản đồ */
    .sec-title {
      font-family: 'Dancing Script', cursive;
      font-size: 2rem;
      color: var(--dark-pink);
      margin-bottom: 14px;
    }

    .map-frame {
      height: clamp(190px, 58vw, 260px);
      width: 100%;
      border: 2px solid #FFC2D6;
      border-radius: 20px;
      overflow: hidden;
      margin-bottom: 14px;
    }

    .map-frame iframe {
      display: block;
      width: 100%;
      height: 100%;
      border: 0;
    }

    /* Form */
    .form-group {
      margin-bottom: 12px;
      text-align: left;
    }

    .form-group label {
      display: block;
      font-weight: 700;
      font-size: 0.88rem;
      margin-bottom: 5px;
      color: var(--dark-pink);
    }

    .form-control {
      width: 100%;
      min-height: 46px;
      font-size: 16px; /* Tránh iPhone tự zoom khi nhập */
      border-radius: 13px;
      padding: 12px;
      border: 2px solid #FFD6E5;
      font-family: 'Quicksand', sans-serif;
      color: var(--text-main);
      background: #FFF9FB;
      outline: none;
      transition: border-color 0.2s;
    }

    .form-control:focus {
      border-color: var(--primary-pink);
    }

    textarea.form-control {
      min-height: 100px;
      resize: vertical;
    }

    /* Lời chúc */
    .wish-list {
      margin-top: 18px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-height: 320px;
      overflow-y: auto;
      overscroll-behavior: contain;
      text-align: left;
    }

    .wish-item {
      background: #FFF5F8;
      border: 1.5px solid #FFD6E5;
      border-radius: 16px;
      padding: 12px 14px;
      overflow-wrap: anywhere;
    }

    .wish-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 4px;
    }

    .wish-author {
      font-weight: 700;
      color: var(--dark-pink);
      font-size: 0.92rem;
    }

    .wish-tag {
      font-size: 0.75rem;
      background: #FFE0EB;
      color: var(--dark-pink);
      padding: 2px 8px;
      border-radius: 999px;
      font-weight: 600;
    }

    .wish-text {
      font-size: 0.9rem;
      color: var(--text-main);
      line-height: 1.4;
    }

    canvas#confetti-canvas {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 999;
    }

    .toast {
      position: fixed;
      bottom: 24px;
      left: 50%;
      transform: translateX(-50%) translateY(80px);
      background: var(--dark-pink);
      color: #fff;
      padding: 10px 22px;
      border-radius: 999px;
      font-weight: 600;
      font-size: 0.9rem;
      box-shadow: 0 8px 20px rgba(214, 51, 108, 0.35);
      opacity: 0;
      transition: all 0.35s ease;
      z-index: 2000;
    }

    .toast.show {
      transform: translateX(-50%) translateY(0);
      opacity: 1;
    }

    /* Floating Background */
    .floating-bg {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }

    .floater {
      position: absolute;
      bottom: -40px;
      font-size: 20px;
      opacity: 0.65;
      animation: floatUp linear infinite;
    }

    @keyframes floatUp {
      0% { transform: translateY(0) rotate(0deg); opacity: 0; }
      15% { opacity: 0.7; }
      85% { opacity: 0.7; }
      100% { transform: translateY(-110vh) rotate(360deg); opacity: 0; }
    }

    /* Giảm chuyển động nếu người dùng yêu cầu */
    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        scroll-behavior: auto !important;
        transition-duration: 0.01ms !important;
      }
    }

    /* Điện thoại nhỏ */
    @media (max-width: 380px) {
      .container {
        padding-left: 10px;
        padding-right: 10px;
      }

      .card {
        padding: 20px 13px;
        border-radius: 22px;
      }

      .btn-group {
        flex-direction: column;
      }

      .btn-group > * {
        width: 100%;
      }

      .envelope-box {
        padding: 25px 16px;
      }

      .info-row {
        gap: 5px;
      }
    }

    /* Tablet */
    @media (min-width: 768px) {
      .container {
        padding-top: 40px;
      }

      .card {
        padding: 36px 30px;
      }
    }
  </style>
</head>
<body>

  <canvas id="confetti-canvas"></canvas>
  <div class="floating-bg" id="floating-bg"></div>

  <!-- Envelope Cover -->
  <div id="envelope-overlay">
    <div class="envelope-box">
      <div class="grad-icon">🎓🌸</div>
      <div class="envelope-title">Thiệp Mời Tốt Nghiệp</div>
      <p class="envelope-sub">Gửi bạn một chiếc thiệp nhỏ xinh từ<br><strong>Lâm Thị Quy</strong> ✨</p>
      <button class="btn-open" onclick="openInvitation()">💌 Mở Thiệp Ngay</button>
      <div class="mobile-tip">
        💡 <i>Mẹo: Nếu xem bằng Zalo/Messenger, hãy bấm dấu <b>3 chấm (...)</b> góc phải chọn <b>Mở bằng trình duyệt</b> để có trải nghiệm tốt nhất nhé!</i>
      </div>
    </div>
  </div>

  <!-- Music Button -->
  <button class="music-btn" id="music-toggle" onclick="toggleMusic()">🎵 Nhạc: Tắt</button>

  <div class="container">
    <!-- Hero Card -->
    <div class="card">
      <span class="badge">🎀 Graduation Ceremony 🎀</span>
      <h1 class="main-heading">Lễ Tốt Nghiệp</h1>
      <div class="graduate-name">✨ Lâm Thị Quy ✨</div>

      <div class="core-info">
        <div class="info-row">
          <span class="info-icon">🕒</span>
          <span>14:00 • Thứ Sáu, ngày 20/11/2026</span>
        </div>
        <div class="info-row">
          <span class="info-icon">🏫</span>
          <span>Trường Đại học Khoa học – Đại học Thái Nguyên</span>
        </div>
      </div>

      <!-- Countdown -->
      <div class="countdown-grid">
        <div class="time-box">
          <span class="time-num" id="days">00</span>
          <span class="time-label">Ngày</span>
        </div>
        <div class="time-box">
          <span class="time-num" id="hours">00</span>
          <span class="time-label">Giờ</span>
        </div>
        <div class="time-box">
          <span class="time-num" id="minutes">00</span>
          <span class="time-label">Phút</span>
        </div>
        <div class="time-box">
          <span class="time-num" id="seconds">00</span>
          <span class="time-label">Giây</span>
        </div>
      </div>

      <div class="btn-group">
        <button class="btn-pink" onclick="downloadICS()">📅 Lưu Vào Lịch</button>
        <button class="btn-outline" onclick="fireConfetti()">🎉 Bắn Pháo Giấy</button>
      </div>
    </div>

    <!-- Map Card -->
    <div class="card">
      <h2 class="sec-title">📍 Địa Điểm Tổ Chức</h2>
      <p style="font-size: 0.95rem; font-weight: 600; margin-bottom: 12px;">
        Trường Đại học Khoa học – ĐH Thái Nguyên<br>
        <span style="font-weight: 400; font-size: 0.85rem; color: var(--text-muted);">Phường Tân Thịnh, TP. Thái Nguyên, Thái Nguyên</span>
      </p>
      <div class="map-frame">
        <iframe
          src="https://maps.google.com/maps?q=Tr%C6%B0%E1%BB%9Dng%20%C4%90%E1%BA%A1i%20h%E1%BB%8Dc%20Khoa%20h%E1%BB%8Dc%20-%20%C4%90%E1%BA%A1i%20h%E1%BB%8Dc%20Th%C3%A1i%20Nguy%C3%AAn&t=&z=15&ie=UTF8&iwloc=&output=embed"
          allowfullscreen>
        </iframe>
      </div>
      <div class="btn-group">
        <a class="btn-pink" href="https://www.google.com/maps/search/?api=1&query=Tr%C6%B0%E1%BB%9Dng+%C4%90%E1%BA%A1i+h%E1%BB%8Dc+Khoa+h%E1%BB%8Dc+-+%C4%90%E1%BA%A1i+h%E1%BB%8Dc+Th%C3%A1i+Nguy%C3%AAn" target="_blank" rel="noopener">
          🗺️ Mở Google Maps
        </a>
        <button class="btn-outline" onclick="copyAddress()">📋 Sao Chép Địa Chỉ</button>
      </div>
    </div>

    <!-- RSVP & Wishes Card -->
    <div class="card">
      <h2 class="sec-title">💖 Xác Nhận & Gửi Lời Chúc</h2>
      <form id="rsvp-form" onsubmit="submitWish(event)">
        <div class="form-group">
          <label>Tên của bạn 🌸</label>
          <input type="text" id="guest-name" class="form-control" placeholder="Nhập tên của bạn..." required />
        </div>
        <div class="form-group">
          <label>Bạn sẽ tham dự chứ? 🎀</label>
          <select id="guest-status" class="form-control">
            <option value="Chắc chắn tham dự 💖">Chắc chắn tham dự 💖</option>
            <option value="Đi cùng bạn bè ✨">Đi cùng bạn bè ✨</option>
            <option value="Gửi lời chúc từ xa 🌸">Gửi lời chúc từ xa 🌸</option>
          </select>
        </div>
        <div class="form-group">
          <label>Lời chúc gửi đến Lâm Thị Quy 💌</label>
          <textarea id="guest-wish" class="form-control" placeholder="Chúc mừng tân cử nhân xinh đẹp..." required></textarea>
        </div>
        <button type="submit" class="btn-pink" style="width: 100%; justify-content: center;">
          ✨ Gửi Xác Nhận & Lời Chúc
        </button>
      </form>

      <div class="wish-list" id="wish-list">
        <div class="wish-item">
          <div class="wish-header">
            <span class="wish-author">Hội Bạn Thân 💕</span>
            <span class="wish-tag">Chắc chắn tham dự 💖</span>
          </div>
          <div class="wish-text">Chúc mừng tân cử nhân Lâm Thị Quy! Chúc cậu luôn rạng rỡ, xinh đẹp và thành công trên chặng đường mới nhé! 🎓🌸</div>
        </div>
      </div>
    </div>
  </div>

  <div class="toast" id="toast"></div>

  <script>
    // Floating Cute Icons
    const floatingIcons = ['🌸', '💖', '✨', '🎀', '🌷', '🎓'];
    const bgContainer = document.getElementById('floating-bg');
    for (let i = 0; i < 18; i++) {
      const el = document.createElement('div');
      el.className = 'floater';
      el.textContent = floatingIcons[i % floatingIcons.length];
      el.style.left = Math.random() * 100 + 'vw';
      el.style.animationDuration = (8 + Math.random() * 10) + 's';
      el.style.animationDelay = (Math.random() * 8) + 's';
      el.style.fontSize = (16 + Math.random() * 14) + 'px';
      bgContainer.appendChild(el);
    }

    // Toast helper
    function showToast(msg) {
      const t = document.getElementById('toast');
      t.textContent = msg;
      t.classList.add('show');
      setTimeout(() => t.classList.remove('show'), 2800);
    }

    // Open Envelope
    function openInvitation() {
      document.getElementById('envelope-overlay').classList.add('hidden');
      fireConfetti();
      startMusic();
    }

    // Countdown Timer to 2026-11-20 14:00:00
    const targetDate = new Date('2026-11-20T14:00:00+07:00').getTime();
    function updateCountdown() {
      const now = Date.now();
      const diff = Math.max(0, targetDate - now);
      const d = Math.floor(diff / (1000 * 60 * 60 * 24));
      const h = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const m = Math.floor((diff / 1000 / 60) % 60);
      const s = Math.floor((diff / 1000) % 60);
      document.getElementById('days').textContent = String(d).padStart(2, '0');
      document.getElementById('hours').textContent = String(h).padStart(2, '0');
      document.getElementById('minutes').textContent = String(m).padStart(2, '0');
      document.getElementById('seconds').textContent = String(s).padStart(2, '0');
    }
    setInterval(updateCountdown, 1000);
    updateCountdown();

    // Download .ics Calendar Event
    function downloadICS() {
      const icsContent = [
        'BEGIN:VCALENDAR',
        'VERSION:2.0',
        'PRODID:-//ThiepMoiTotNghiep//LamThiQuy//VI',
        'BEGIN:VEVENT',
        'UID:graduation-lamthiquy-20261120@invite',
        'DTSTAMP:20261117T120000Z',
        'DTSTART:20261120T070000Z',
        'DTEND:20261120T100000Z',
        'SUMMARY:Lễ Tốt Nghiệp - Lâm Thị Quy 🎓',
        'LOCATION:Trường Đại học Khoa học - Đại học Thái Nguyên, Phường Tân Thịnh, TP. Thái Nguyên',
        'DESCRIPTION:Trân trọng kính mời bạn đến tham dự Lễ Tốt Nghiệp của Lâm Thị Quy!',
        'END:VEVENT',
        'END:VCALENDAR'
      ].join('\r\n');

      const blob = new Blob([icsContent], { type: 'text/calendar;charset=utf-8' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'Le-Tot-Nghiep-Lam-Thi-Quy.ics';
      a.click();
      URL.revokeObjectURL(url);
      showToast('📅 Đã tải file lịch (.ics)!');
    }

    // Copy Address
    function copyAddress() {
      const addr = 'Trường Đại học Khoa học – Đại học Thái Nguyên, Phường Tân Thịnh, TP. Thái Nguyên';
      navigator.clipboard.writeText(addr).then(() => {
        showToast('📋 Đã sao chép địa chỉ!');
      });
    }

    // RSVP & Wish Wall
    function submitWish(e) {
      e.preventDefault();
      const name = document.getElementById('guest-name').value.trim();
      const status = document.getElementById('guest-status').value;
      const wish = document.getElementById('guest-wish').value.trim();
      if (!name || !wish) return;

      const list = document.getElementById('wish-list');
      const item = document.createElement('div');
      item.className = 'wish-item';
      item.innerHTML = `
        <div class="wish-header">
          <span class="wish-author">${escapeHTML(name)} 🌸</span>
          <span class="wish-tag">${escapeHTML(status)}</span>
        </div>
        <div class="wish-text">${escapeHTML(wish)}</div>
      `;
      list.prepend(item);
      document.getElementById('rsvp-form').reset();
      fireConfetti();
      showToast('💖 Cảm ơn bạn đã gửi lời chúc!');
    }

    function escapeHTML(str) {
      return str.replace(/[&<>"']/g, m => ({
        '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;'
      }[m]));
    }

    // Optimized Confetti for Mobile
    const canvas = document.getElementById('confetti-canvas');
    const ctx = canvas.getContext('2d');
    let particles = [];
    const colors = ['#FF6B9D', '#FF9EBB', '#FFD6E5', '#FFE066', '#FFA8C5', '#D6336C'];

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    function fireConfetti() {
      for (let i = 0; i < 45; i++) {
        particles.push({
          x: canvas.width / 2 + (Math.random() - 0.5) * 140,
          y: canvas.height / 2,
          vx: (Math.random() - 0.5) * 12,
          vy: (Math.random() - 1.2) * 12,
          size: 6 + Math.random() * 5,
          color: colors[Math.floor(Math.random() * colors.length)],
          rot: Math.random() * 360,
          vRot: (Math.random() - 0.5) * 10
        });
      }
    }

    function animateConfetti() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      particles.forEach((p, idx) => {
        p.x += p.vx;
        p.y += p.vy;
        p.vy += 0.35;
        p.rot += p.vRot;
        ctx.save();
        ctx.translate(p.x, p.y);
        ctx.rotate((p.rot * Math.PI) / 180);
        ctx.fillStyle = p.color;
        ctx.fillRect(-p.size / 2, -p.size / 2, p.size, p.size * 0.65);
        ctx.restore();
        if (p.y > canvas.height + 20) particles.splice(idx, 1);
      });
      requestAnimationFrame(animateConfetti);
    }
    animateConfetti();

    // Gentle Web Audio Melody
    let audioCtx = null;
    let isPlaying = false;
    let melodyTimer = null;
    const notes = [523.25, 659.25, 783.99, 1046.50, 783.99, 659.25, 587.33, 698.46, 880.00, 783.99];
    let noteIdx = 0;

    function playNote() {
      if (!isPlaying || !audioCtx) return;
      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();
      osc.type = 'sine';
      osc.frequency.value = notes[noteIdx % notes.length];
      noteIdx++;
      gain.gain.setValueAtTime(0.04, audioCtx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 0.65);
      osc.connect(gain);
      gain.connect(audioCtx.destination);
      osc.start();
      osc.stop(audioCtx.currentTime + 0.65);
      melodyTimer = setTimeout(playNote, 700);
    }

    function startMusic() {
      if (isPlaying) return;
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === 'suspended') audioCtx.resume();
      isPlaying = true;
      document.getElementById('music-toggle').textContent = '🎵 Nhạc: Bật';
      playNote();
    }

    function stopMusic() {
      isPlaying = false;
      clearTimeout(melodyTimer);
      document.getElementById('music-toggle').textContent = '🎵 Nhạc: Tắt';
    }

    function toggleMusic() {
      if (isPlaying) stopMusic();
      else startMusic();
    }
  </script>
</body>
</html>
