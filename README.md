<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio — Kim Khánh</title>

  <meta property="og:title" content="Portfolio — Kim Khánh" />
  <meta property="og:locale" content="vi_VN" />
  <meta property="og:site_name" content="Kim Khánh Portfolio" />
  <meta property="og:type" content="website" />
  <meta name="twitter:card" content="summary" />
  <meta property="twitter:title" content="Portfolio — Kim Khánh" />

  <script type="application/ld+json">
  {"@context":"https://schema.org","@type":"WebSite","headline":"Kim Khánh Portfolio","name":"Kim Khánh Portfolio"}
  </script>

  <style>
    :root {
      --card: rgba(255,255,255,0.88);
      --text: #111827;
      --muted: #374151;
    }

    * { box-sizing: border-box; }

    body {
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial;
      margin: 0;
      line-height: 1.6;
      overflow-x: hidden;

      /* Beach background */
      background: url("https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/beach-wallpaper-3840x2160-sandy-shore-sunset-12590.jpg");
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-attachment: fixed;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* Typing text effect */
    .typing {
      font-size: 18px;
      white-space: nowrap;
      overflow: hidden;
      border-right: 3px solid rgba(255,255,255,0.7);
      display: inline-block;
      padding-right: 6px;
      animation: blink 0.7s infinite;
    }
    @keyframes blink {
      50% { border-color: transparent; }
    }

    header {
      text-align: center;
      padding: 60px 20px 30px;
      backdrop-filter: brightness(1.05);
    }

    header h1 {
      font-size: 34px;
      margin: 0 0 12px;
      color: #fff;
      text-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }

    header p {
      margin: 0;
      color: #fff;
      text-shadow: 0 3px 8px rgba(0,0,0,0.25);
      font-size: 16px;
    }

    .container {
      max-width: 960px;
      margin: 40px auto;
      padding: 20px;
      flex: 1;
    }

    .card {
      background: var(--card);
      border-radius: 18px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.15);
      overflow: hidden;
      display: flex;
      flex-wrap: wrap;
      color: var(--text);
      backdrop-filter: blur(6px);
    }

    .left {
      flex: 1 1 260px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 25px;
      background: rgba(255,255,255,0.3);
    }

    .avatar {
      width: 240px;
      height: 240px;
      border-radius: 14px;
      overflow: hidden;
      border: 4px solid rgba(255,255,255,0.6);
      box-shadow: 0 5px 20px rgba(0,0,0,0.2);
    }

    .avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .right {
      flex: 2 1 340px;
      padding: 26px 36px;
    }

    .right h2 {
      font-size: 26px;
      margin: 0 0 6px;
    }

    .meta {
      font-size: 15px;
      margin-bottom: 12px;
      color: var(--muted);
      font-weight: 500;
    }

    .about {
      background: rgba(255,255,255,0.6);
      padding: 16px;
      border-radius: 12px;
      border: 1px solid rgba(255,255,255,0.4);
      font-size: 15px;
      box-shadow: inset 0 2px 6px rgba(0,0,0,0.04);
    }

    footer {
      text-align: center;
      padding: 22px 0;
      font-size: 14px;
      color: #fff;
      text-shadow: 0 3px 10px rgba(0,0,0,0.3);
    }

    /* Typing animation controller */
    @keyframes typeWriter {
      from { width: 0 }
      to { width: 100% }
    }
    .typing.run {
      animation: 
        typeWriter 3.5s steps(36) 1 forwards,
        blink 0.7s infinite;
    }

  </style>
</head>

<body>

<header>
  <h1>Giới thiệu bản thân</h1>
  <p><span id="typeText" class="typing"></span></p>
</header>

<script>
  const text = "Xin chào! Mình là Kim Khánh 🌊 Chào mừng bạn đến với portfolio của mình!";
  const typeText = document.getElementById("typeText");
  typeText.classList.add("run");
  typeText.textContent = text;
</script>

<div class="container">
  <div class="card">
    <div class="left">
      <div class="avatar">
        <img src="https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/golden-retriever-tongue-out.jpg" alt="Ảnh cá nhân Khánh" />
      </div>
    </div>

    <div class="right">
      <h2>Huỳnh Kim Khánh</h2>
      <div class="meta">🎓 Học sinh lớp 12A • ✍️ Direct-response copywriting • 🌅 Yêu biển & khám phá</div>

      <div class="about">
        <p>
          Mình đang trên hành trình học ngôn ngữ và sáng tạo nội dung viết để kết nối cảm xúc với mọi người.  
          Sở thích của mình là <strong>bơi</strong> 🏊, <strong>đi biển</strong> 🌊 và đọc sách phát triển bản thân 📖.  
          Mình tin rằng mỗi con chữ đều có năng lượng — đặc biệt khi nói về những điều mình yêu. 🌱✨
        </p>
      </div>
    </div>
  </div>
</div>

<footer>© 2025 — Designed by Khánh 🌟</footer>

</body>
</html>
