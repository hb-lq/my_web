<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
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

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background-color: var(--bg-pink);
      background-image: radial-gradient(#FFC2D6 1.5px, transparent 1.5px), radial-gradient(#FFE0EB 1.5px, #FFF0F5 1.5px);
      background-size: 36px 36px;
      background-position: 0 0, 18px 18px;
      color: var(--text-main);
      min-height: 100vh;
      overflow-x: hidden;
      position: relative;
    }

    /* Floating Hearts & Petals */
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

    /* Envelope Cover Overlay */
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
      border-radius: 28px;
      padding: 36px 28px;
      max-width: 400px;
      width: 100%;
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

    .envelope-title {
      font-family: 'Dancing Script', cursive;
      font-size: 2.2rem;
      color: var(--dark-pink);
      margin-bottom: 8px;
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
    }

    .btn-open:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 25px rgba(255, 77, 136, 0.45);
    }

    /* Main Container */
    .container {
      position: relative;
      z-index: 1;
      max-width: 640px;
      margin: 0 auto;
      padding: 28px 16px 60px;
    }

    /* Music Toggle */
    .music-btn {
      position: fixed;
      top: 16px;
      right: 16px;
      z-index: 50;
      background: #fff;
      border: 2px solid #FFB3C6;
      color: var(--dark-pink);
      border-radius: 999px;
      padding: 8px 14px;
      font-family: 'Quicksand', sans-serif;
      font-weight: 700;
      font-size: 0.85rem;
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(255, 107, 157, 0.2);
      display: flex;
      align-items: center;
      gap: 6px;
    }

    /* Main Card */
    .card {
      background: var(--card-bg);
      border: 2.5px solid #FFC2D6;
      border-radius: 32px;
      padding: 32px 24px;
      box-shadow: 0 14px 36px rgba(255, 107, 157, 0.16);
      margin-bottom: 22px;
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

    .main-heading {
      font-family: 'Dancing Script', cursive;
      font-size: 2.8rem;
      color: var(--dark-pink);
      line-height: 1.2;
      margin-bottom: 6px;
    }

    .graduate-name {
      font-size: 1.85rem;
      font-weight: 700;
      color: #FF4D88;
      margin: 10px 0 18px;
      text-shadow: 0 2px 10px rgba(255, 107, 157, 0.2);
    }

    .core-info {
      background: #FFF5F8;
      border: 2px dashed #FF9EBB;
      border-radius: 22px;
      padding: 20px 16px;
      margin:
