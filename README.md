<!doctype html>
<html lang="vi">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Kim Khánh — Personal Portfolio</title>

<style>
/* ================= THEME ================= */
:root{
  --blue-1:#d9ecff;
  --blue-2:#bedbff;
  --glass:#ffffffdd;
  --card:#ffffffee;
  --text:#1c2b3a;
  --muted:#5c6b7a;
  --accent:#65a8ff;
  --accent-2:#3f7fe0;
  --radius:18px;
  --shadow:0 12px 32px rgba(40,80,140,0.12);
  --shadow-soft:0 10px 24px rgba(40,80,140,0.08);
}

*{box-sizing:border-box}
body{
  margin:0;
  font-family:"Inter",system-ui;
  background:linear-gradient(180deg,var(--blue-1),var(--blue-2));
  color:var(--text);
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
  line-height:1.55;
}

/* ================= HEADER ================= */
.header{
  position:relative;
  padding:40px 20px 70px;
  overflow:hidden;
}

.header::before{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(180deg,rgba(0,60,150,0.45),rgba(0,60,150,0.25)),
             url("https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1200&q=80");
  background-size:cover;
  background-position:center;
  filter:brightness(0.7);
}

.header-inner{
  position:relative;
  z-index:2;
  max-width:1080px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.brand{
  display:flex;
  align-items:center;
  gap:16px;
}

.logo{
  width:74px;height:74px;
  border-radius:20px;
  background:linear-gradient(135deg,var(--accent),var(--accent-2));
  display:grid;place-items:center;
  color:white;
  font-size:24px;font-weight:800;
  box-shadow:var(--shadow);
}

.titles .name{
  color:white;
  font-size:20px;
  font-weight:800;
}
.titles .role{
  color:#eef6ff;
  font-size:13px;
}

/* NAV */
nav{
  display:flex;
  gap:12px;
}
nav a{
  color:white;
  padding:8px 16px;
  border-radius:999px;
  text-decoration:none;
  font-weight:600;
  font-size:14px;
  background:rgba(255,255,255,0.08);
  border:1px solid rgba(255,255,255,0.07);
  transition:.18s;
}
nav a:hover{
  transform:translateY(-3px);
  box-shadow:var(--shadow);
}
nav a.active{
  background:rgba(255,255,255,0.18);
  transform:translateY(-4px);
}

/* ================= CARDS ================= */
.container{
  max-width:1080px;
  margin:-40px auto 60px;
  padding:20px;
  position:relative;
  z-index:3;
}

.card{
  background:var(--card);
  padding:24px;
  border-radius:var(--radius);
  margin-bottom:26px;
  box-shadow:var(--shadow-soft);
  border:1px solid rgba(0,0,0,0.04);
}

/* HOME */
.home{
  display:flex;
  gap:24px;
  flex-wrap:wrap;
  align-items:center;
}

.hero-photo{
  width:260px;height:260px;
  border-radius:22px;
  overflow:hidden;
  box-shadow:var(--shadow);
  border:6px solid rgba(255,255,255,0.6);
}

.hero-photo img{
  width:100%;height:100%;object-fit:cover;
}

.intro h1{
  margin:0 0 10px;
  font-size:28px;
  font-weight:800;
}

.lead{
  color:var(--muted);
  max-width:420px;
}

/* ABOUT */
.two-col{
  display:grid;
  grid-template-columns:300px 1fr;
  gap:20px;
}

.photo{
  border-radius:20px;
  overflow:hidden;
  border:6px solid rgba(255,255,255,0.6);
  box-shadow:var(--shadow);
}

.photo img{
  width:100%;height:100%;object-fit:cover;
}

ul.clean{color:var(--muted);margin-left:20px}

/* FOOTER */
.footer{
  text-align:center;
  color:var(--muted);
  padding:20px 0 50px;
}
</style>
</head>

<body>

<header class="header">
  <div class="header-inner">

    <div class="brand">
      <div class="logo">KK</div>
      <div class="titles">
        <div class="name">Kim Khánh</div>
        <div class="role">Lớp 12A — Portfolio cá nhân</div>
      </div>
    </div>

    <nav>
      <a href="#home" class="active">Trang chủ</a>
      <a href="#about">Về tôi</a>
      <a href="#study">Học tập</a>
      <a href="#hobbies">Sở thích</a>
      <a href="#contact">Liên hệ</a>
    </nav>

  </div>
</header>

<main class="container">

<section id="home" class="card">
  <div class="home">
    <div class="hero-photo">
      <!-- Avatar art-style bạn dùng ảnh gì thì thay -->
      <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=800&q=80">
    </div>

    <div class="intro">
      <h1>Xin chào! Mình là Khánh 👋</h1>
      <p class="lead">
        Học sinh lớp 12A, thích ngôn ngữ, sáng tạo và xây dựng những không gian đẹp — như chính website này.
      </p>
    </div>
  </div>
</section>

<section id="about" class="card">
  <h2>Về mình</h2>

  <div class="two-col">
    <div class="photo">
      <img src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&w=900&q=80">
    </div>

    <div>
      <p>
        Mình là <b>Kim Khánh</b> — người thích học, thích làm, thích thử mọi thứ mới.
        Cuộc sống của mình xoay quanh việc khám phá, sáng tạo và biến những điều nhỏ thành đẹp.
      </p>

      <ul class="clean">
        <li>Phong cách: minimal – aesthetic – creative</li>
        <li>Sở thích: English, copywriting, thiết kế web</li>
        <li>Màu yêu thích: xanh biển</li>
        <li>Goal hiện tại: IELTS 8.0 và ĐGNL 1000+</li>
      </ul>
    </div>
  </div>
</section>

<section id="study" class="card">
  <h2>Học tập</h2>

  <ul class="clean">
    <li>Học tiếng Anh mỗi ngày</li>
    <li>Luyện IELTS: Reading, Writing, Speaking</li>
    <li>Tự học lập trình web (HTML/CSS/JS)</li>
    <li>Copywriting cho dự án freelance</li>
  </ul>
</section>

<section id="hobbies" class="card">
  <h2>Sở thích</h2>

  <ul class="clean">
    <li>Đọc sách (self-help, kinh tế, ngôn ngữ)</li>
    <li>Làm web aesthetic</li>
    <li>Viết lách, làm content, email marketing</li>
    <li>Học tiếng mới: English, Spanish, Chinese</li>
  </ul>
</section>

<section id="contact" class="card">
  <h2>Liên hệ</h2>
  <p>Nếu bạn muốn kết nối, hợp tác hoặc học chung, hãy nhắn nhé!</p>
  <ul class="clean">
    <li>Email: yourmail@example.com (bạn sửa)</li>
    <li>Instagram: @yourhandle</li>
  </ul>
</section>

<div class="footer">Made with 💙 by Khánh</div>

</main>
</body>
</html>
