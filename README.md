<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio — Kim Khánh</title>

  <!-- SEO / Social sharing tags (giữ cấu trúc giống trang mẫu) -->
  <meta property="og:title" content="Portfolio — Kim Khánh" />
  <meta property="og:locale" content="vi_VN" />
  <meta property="og:site_name" content="Kim Khánh Portfolio" />
  <meta property="og:type" content="website" />
  <meta name="twitter:card" content="summary" />
  <meta property="twitter:title" content="Portfolio — Kim Khánh" />

  <script type="application/ld+json">
  {"@context":"https://schema.org","@type":"WebSite","headline":"Portfolio — Kim Khánh","name":"Kim Khánh Portfolio"}
  </script>

  <style>
    :root {
      --bg: #f3f4f6;
      --card: #ffffff;
      --primary: #2563eb;
      --secondary: #1e40af;
      --text: #111827;
      --muted: #6b7280;
    }
    * { box-sizing: border-box; }
    body {
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial;
      margin: 0;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    header {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: #fff;
      padding: 48px 20px;
      text-align: center;
    }
    header h1 { font-size: 36px; margin: 0 0 10px; }
    header p { font-size: 16px; margin: 0; opacity: 0.9; }

    .container {
      max-width: 960px;
      margin: 40px auto;
      padding: 20px;
    }

    .card {
      background: var(--card);
      border-radius: 16px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.08);
      overflow: hidden;
      display: flex;
      flex-wrap: wrap;
    }

    .left {
      flex: 1 1 280px;
      background: #eef2ff;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 30px;
    }

    .avatar {
      width: 260px;
      height: 260px;
      border-radius: 14px;
      overflow: hidden;
      border: 5px solid rgba(255,255,255,0.6);
      box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    }
    .avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .right {
      flex: 2 1 320px;
      padding: 30px 40px;
    }
    .right h2 {
      margin: 0 0 8px;
      font-size: 26px;
    }
    .right .meta {
      color: var(--muted);
      margin-bottom: 16px;
    }

    .about {
      background: #f9fafb;
      padding: 16px;
      border-radius: 12px;
      border: 1px solid #e5e7eb;
      min-height: 120px;
    }

    footer {
      text-align: center;
      padding: 20px 0;
      color: var(--muted);
      font-size: 14px;
    }

    @media(max-width: 720px){
      .right { padding: 20px; }
      header h1 { font-size: 28px; }
    }
  </style>
</head>

<body>
  <header>
    <h1>Giới thiệu bản thân </h1>
    <p>✍️ Copywriter • 📘 Ngôn ngữ • 🌊 Người yêu biển</p>
  </header>

  <div class="container">
    <div class="card">
      <div class="left">
        <div class="avatar">
          <img src="(https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/golden-retriever-tongue-out.jpg)" alt="Ảnh cá nhân Khánh" />
        </div>
      </div>

      <div class="right">
        <h2>Huỳnh Kim Khánh</h2>
        <div class="meta">🎓 Học sinh lớp 12A</div>

        <div class="about">
          <p>
            Xin chào! Mình là <strong>Kim Khánh</strong>.  
            Mình đam mê học ngôn ngữ và copywriting theo hướng direct-response.  
            Khi rảnh mình thích <strong>bơi</strong>, <strong>đi biển</strong> và đọc <em>The Perfection Trap</em>.  
            Đây là góc chia sẻ nhỏ để mọi người hiểu hơn về mình và hành trình mình đang xây dựng 🌱
          </p>
        </div>
      </div>
    </div>
  </div>

  <footer>© 2025 — Designed by Khánh 🌟</footer>
</body>
</html>
