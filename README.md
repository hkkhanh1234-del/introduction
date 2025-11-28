<!doctype html>
<html lang="vi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Portfolio — Huỳnh Kim Khánh</title>

<meta property="og:title" content="Portfolio — Huỳnh Kim Khánh" />
<meta property="og:locale" content="vi_VN" />
<meta property="og:site_name" content="Huỳnh Kim Khánh Portfolio" />
<meta property="og:type" content="website" />
<meta name="twitter:card" content="summary" />
<meta property="twitter:title" content="Portfolio — Huỳnh Kim Khánh" />
<script type="application/ld+json">
{"@context":"https://schema.org","@type":"WebSite","headline":"Portfolio — Huỳnh Kim Khánh","name":"Huỳnh Kim Khánh Portfolio"}
</script>

<style>
body {
  margin: 0;
  font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial;
  background: url("https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/beach-wallpaper-3840x2160-sandy-shore-sunset-12590.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  overflow-x: hidden;
  color:#111827;
}

header {
  text-align:center;
  padding:90px 20px 40px;
  position:relative;
}
header h1 {
  font-size:54px;
  font-weight:900;
  margin:0;
  color:#fff;
  text-transform:uppercase;
  letter-spacing:2px;
  filter:drop-shadow(0 0 28px rgba(255,255,255,0.8))
         drop-shadow(0 0 48px rgba(37,99,235,0.6));
  animation:titleGlow 2.5s infinite alternate ease-in-out;
}
@keyframes titleGlow {
  from{opacity:0.9;transform:scale(1);}
  to{opacity:1;transform:scale(1.05);}
}

header p {
  font-size:20px;
  font-weight:600;
  color:white;
  text-shadow:0 0 18px rgba(255,255,255,0.6);
}

.container {
  max-width:1000px;
  margin:20px auto 60px;
  padding:20px;
}

.card {
  display:flex;
  flex-wrap:wrap;
  border-radius:22px;
  background:rgba(255,255,255,0.72);
  backdrop-filter:blur(12px);
  box-shadow:0 15px 45px rgba(0,0,0,0.25);
  transition:0.5s;
  transform-style:preserve-3d;
}
.card:hover{
  transform:perspective(900px) rotateX(5deg) rotateY(-5deg) scale(1.02);
  box-shadow:0 22px 58px rgba(37,99,235,0.3), 0 0 30px rgba(255,255,255,0.4);
}

.left {
  flex:1 1 260px;
  display:flex;
  justify-content:center;
  align-items:center;
  padding:35px;
}
.avatar {
  width:240px;
  height:240px;
  border-radius:16px;
  overflow:hidden;
  border:5px solid rgba(255,255,255,0.6);
  box-shadow:0 6px 26px rgba(0,0,0,0.2);
}
.avatar img{
  width:100%;height:100%;object-fit:cover;
}

.right {
  flex:2 1 340px;
  padding:35px 45px;
}
.right h2{
  font-size:38px;font-weight:800;margin:0 0 14px;
  filter:drop-shadow(0 0 8px rgba(37,99,235,0.4));
}

.section {
  margin-top:26px;
  padding:18px 24px;
  border-radius:14px;
  background:rgba(255,255,255,0.64);
  backdrop-filter:blur(6px);
  box-shadow:inset 0 3px 10px rgba(0,0,0,0.03);
  border-left:4px solid rgba(37,99,235,0.4);
}

.section h3 {
  font-size:24px;
  margin:0 0 10px;
  font-weight:700;
}

footer {
  text-align:center;
  padding:30px 0;
  margin-top:auto;
}

.btn-home {
  display:inline-block;
  padding:14px 28px;
  font-size:17px;
  font-weight:700;
  color:#111;
  border-radius:50px;
  background:rgba(255,255,255,0.85);
  backdrop-filter:blur(10px);
  box-shadow:0 6px 20px rgba(255,255,255,0.4);
  transition:0.3s;
  text-decoration:none;
}
.btn-home:hover{
  transform:scale(1.08);
  box-shadow:0 0 26px rgba(255,255,255,0.6);
}

/* BALLOONS */
.balloon {
  position:absolute;
  bottom:-140px;
  border-radius:50%;
  opacity:0.8;
  animation:floatUp linear infinite;
  filter:blur(0.5px);
}
@keyframes floatUp{
  0%{transform:translateY(0);}
  100%{transform:translateY(-120vh);}
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
  <h1>Huỳnh Kim Khánh</h1>
  <p>✍️ Copywriter • 📘 Language Explorer • 🌊 Ocean Lover</p>
</header>

<!-- BALLOON SCRIPT -->
<script>
const balloonCount = 14;
for (let i = 0; i < balloonCount; i++) {
  const b = document.createElement("div");
  b.className = "balloon";
  const size = 52 + Math.random()*38;
  b.style.width = size+"px";
  b.style.height = size*1.26+"px";
  b.style.left = Math.random()*100+"vw";
  b.style.animationDuration = 7 + Math.random()*6 + "s";
  b.style.animationDelay = Math.random()*4 + "s";
  document.body.appendChild(b);
}
</script>

<!-- MAIN CONTENT -->
<div class="container">

  <div class="card">

    <div class="left">
      <div class="avatar">
        <img src="https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/golden-retriever-tongue-out.jpg" alt="Avatar Khánh"/>
      </div>
    </div>

    <div class="right">
      <h2>Kim Khánh</h2>
      <div class="meta">🎓 Học sinh lớp 12A • ✨ Direct-response Copywriting • 🌅 Creativity & Connection</div>

      <div class="section">
        <h3>🧑‍💻 About Me</h3>
        <p>
          Mình là Huỳnh Kim Khánh (thường gọi là Kim Khánh/Khánh), hiện là học sinh lớp 12A.  
          Mình đang xây dựng con đường freelancer trong lĩnh vực sáng tạo nội dung viết và marketing.
          Phong cách của mình thiên về <strong>Direct–Response Copywriting</strong> — tập trung vào cảm xúc, hành vi khách hàng và tạo chuyển đổi thực tế.
        </p>
      </div>

      <div class="section">
        <h3>📘 Language Journey</h3>
        <ul>
          <li>🇬🇧 <strong>English:</strong> Band 7 mục tiêu 8.0 vào tháng 12/2025</li>
          <li>🇪🇸 <strong>Spanish:</strong> Beginner — đang luyện giao tiếp cơ bản</li>
          <li>🇨🇳 <strong>Chinese:</strong> HSK nền tảng — đang học bài 1 “Nǐ hǎo”</li>
        </ul>
      </div>

      <div class="section">
        <h3>✍️ Copywriting & Skills</h3>
        <ul>
          <li>Email Marketing & Lead Nurturing</li>
          <li>Landing Page (Bulldogology, Pet Brand…)</li>
          <li>Canva Design, Translation & Content Creation</li>
          <li>Writing for Psychology-driven campaigns</li>
          <li>Storytelling in sales copy format</li>
        </ul>
      </div>

      <div class="section">
        <h3>🌊 Hobbies</h3>
        <p>
          Khi không viết, mình thường:
        </p>
        <ul>
          <li>🏊 Bơi lội thư giãn & rèn endurance</li>
          <li>🌅 Đi biển — đặc biệt lúc hoàng hôn</li>
          <li>📖 Đọc sách self-growth: <em>The Perfection Trap</em></li>
        </ul>
      </div>

      <div class="section">
        <h3>🎯 Future Goals</h3>
        <ul>
          <li>🔥 Tăng tốc kỹ năng Marketing trên Instagram/TikTok/YouTube</li>
          <li>🚀 Build personal brand về ngôn ngữ & copywriting</li>
          <li>📊 Học finance (stock, fintech, AI in finance)</li>
          <li>💛 Viết nội dung có chiều sâu và kết nối</li>
        </ul>
      </div>

    </div>

  </div>
</div>

<!-- FOOTER WITH HOME BUTTON -->
<footer>
  <a class="btn-home" href="javascript:history.back()">⬅️ Quay lại trang chính</a>
</footer>

</body>
</html>
