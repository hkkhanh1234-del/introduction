<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Khánh — Cuốn sổ học tập & sáng tạo</title>

  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@600;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --dark-bg: #0b1e28;
      --light-bg: #f0f9ff;
      --accent: #0e7490;
      --text-dark: #042635;
      --text-light: #e4faff;
      --card-bg: rgba(255,255,255,0.9);
    }
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: Inter, sans-serif; line-height:1.6; background: var(--light-bg); color: var(--text-dark); transition: background 0.4s, color 0.4s; }
    a { color: inherit; text-decoration: none; }

    /* Dark mode */
    .dark-mode { background: var(--dark-bg); color: var(--text-light); }

    /* Navbar fixed + minimal */
    nav {
      position: fixed; top:0; left:0; right:0; z-index:100;
      display: flex; justify-content: space-between; align-items: center;
      padding:16px 8%; background: rgba(255,255,255,0.72); backdrop-filter: blur(10px);
    }
    .dark-mode nav { background: rgba(11,30,40,0.8); }
    nav .site-name { font-weight:700; font-size:20px; }
    nav .toggle-dark { cursor:pointer; font-size:18px; }

    /* Hero / Cover */
    header.hero {
      min-height:100vh; display:flex; align-items:center; justify-content:center;
      text-align:center; padding:0 20px;
      background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=1400') center/cover no-repeat;
      color: white;
      position: relative;
    }
    header.hero::before {
      content:''; position:absolute; inset:0;
      background: rgba(0,0,0,0.4);
    }
    header.hero .inner { position: relative; z-index:2; }
    .hero .title { font-family: 'Playfair Display', serif; font-size:48px; font-weight:800; margin-bottom:18px; }
    .hero .subtitle { font-size:20px; opacity:0.9; }

    main { padding-top:80px; }

    section { max-width:850px; margin:80px auto; padding:0 20px; }
    h2 { font-size:24px; color: var(--accent); margin-bottom:14px; }

    .card {
      background: var(--card-bg);
      border-radius:12px;
      padding:24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.08);
      margin-bottom:28px;
    }

    /* Projects / Notes list */
    .notes-list { list-style: none; }
    .notes-list li { margin-bottom:14px; }

    /* Avatar / image art style */
    .avatar {
      width:180px; height:180px; border-radius:50%; overflow:hidden;
      margin:30px auto; box-shadow: 0 10px 26px rgba(0,0,0,0.2);
    }
    .avatar img { width:100%; height:100%; object-fit:cover; }

    footer { text-align:center; padding:40px 20px; font-size:14px; opacity:0.75; }
  </style>
</head>

<body>

<nav>
  <div class="site-name">Khánh’s Space</div>
  <div class="toggle-dark">🌙</div>
</nav>

<header class="hero">
  <div class="inner">
    <h1 class="title">Một cuốn sổ nhỏ — học, sống & sáng tạo</h1>
    <p class="subtitle">Ghi chép hành trình học tập, sở thích, và những ý tưởng vụn vặt tuổi 17.</p>
  </div>
</header>

<main>
  <!-- About -->
  <section>
    <h2>Về mình</h2>
    <div class="card">
      <p>Mình là học sinh cấp 3, yêu thích tiếng Anh, viết lách, đọc sách và học thuật. Trang web này là góc nhỏ để mình ghi lại suy nghĩ, trải nghiệm, và những gì mình học được mỗi ngày.</p>
    </div>
  </section>

  <!-- Học tập & Ghi chú -->
  <section>
    <h2>Học tập & ghi chú</h2>
    <ul class="notes-list">
      <li>📘 Ôn từ vựng tiếng Anh mỗi ngày</li>
      <li>🧠 Rèn tư duy logic bằng bài toán</li>
      <li>🎯 Luyện kỹ năng viết & dịch — tiếng Anh / tiếng Trung</li>
      <li>💻 Học HTML & CSS — tự làm web cá nhân</li>
    </ul>
  </section>

  <!-- Sở thích & Cuộc sống -->
  <section>
    <h2>Sở thích & cuộc sống</h2>
    <div class="card">
      <p>Mỗi khi rảnh: mình đọc sách, nghe nhạc, viết nhật ký, đi biển hoặc hóng hoàng hôn — để thư giãn và lấy cảm hứng.</p>
    </div>
  </section>

  <!-- Ví dụ ghi chép / note nhỏ -->
  <section>
    <h2>Ghi chép & thử nghiệm</h2>
    <div class="card">
      <p>✅ Ghi chú IELTS, mind-map học từ vựng</p>
      <p>✨ Layout báo cáo nhỏ bằng HTML/CSS</p>
      <p>📝 Ghi lại cảm xúc, nhật ký học & cuộc sống</p>
    </div>
  </section>
</main>

<footer>
  © <span id="year"></span> — Một góc nhỏ của Khánh  
</footer>

<script>
  // dark mode toggle
  const btn = document.querySelector('.toggle-dark');
  btn.onclick = () => {
    document.body.classList.toggle('dark-mode');
  };
  // auto year
  document.getElementById('year').textContent = new Date().getFullYear();
</script>

</body>
</html>
