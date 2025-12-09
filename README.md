<!doctype html>
<html lang="vi">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Kim Khánh — Portfolio Aesthetic</title>

<!-- Google font -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;500;700;800&display=swap" rel="stylesheet">

<style>
/* ================= THEME / VARIABLES ================= */
:root{
  --bg:#e7f3ff;
  --card:#ffffffee;
  --text:#13202b;
  --muted:#5c6b7a;
  --accent:#5fa8ff;
  --accent-2:#3f7fe0;
  --glass: rgba(255,255,255,0.55);
  --radius:18px;
  --shadow:0 12px 30px rgba(50,90,160,0.14);
  --soft:0 8px 18px rgba(20,40,80,0.06);
}

/* Dark mode */
body.dark{
  --bg:#07101a;
  --card:rgba(20,30,45,0.85);
  --text:#dbe9ff;
  --muted:#8faad0;
  --accent:#7abbff;
  --accent-2:#3d8aff;
  --glass: rgba(10,18,30,0.6);
}

/* ================= GLOBAL ================= */
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%}
body{
  font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Arial;
  background:linear-gradient(180deg,var(--bg),#d8eefd);
  color:var(--text);
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden;
  transition:background .35s ease,color .35s ease;
  line-height:1.55;
}

/* Floating shapes (aesthetic) */
.shape{
  position:fixed;
  width:260px;height:260px;
  background:radial-gradient(circle at 20% 30%, var(--accent), transparent 60%);
  filter:blur(70px);
  opacity:0.45;
  z-index:0;
  pointer-events:none;
  transform:translate3d(0,0,0);
  animation:float 10s ease-in-out infinite;
}
.shape.b{background:radial-gradient(circle at 80% 60%, var(--accent-2), transparent 60%); animation-delay:2s}
@keyframes float{0%{transform:translateY(0)}50%{transform:translateY(38px)}100%{transform:translateY(0)}}

/* ================= NAV (sticky glass) ================= */
nav{
  position:sticky;
  top:14px;
  z-index:30;
  margin:0 auto;
  max-width:1100px;
  display:flex;
  gap:12px;
  justify-content:center;
  padding:10px;
  background:var(--glass);
  border-radius:999px;
  backdrop-filter:blur(10px) saturate(1.05);
  box-shadow:var(--soft);
  border:1px solid rgba(255,255,255,0.45);
  margin-bottom:18px;
}
body.dark nav{background:rgba(12,20,34,0.55);border:1px solid rgba(255,255,255,0.06)}
nav a{
  color:var(--text);
  text-decoration:none;
  padding:8px 14px;
  border-radius:999px;
  font-weight:700;
  font-size:14px;
  transition:transform .18s, background .18s, color .18s;
}
nav a:hover{transform:translateY(-3px); background:var(--accent); color:white}
nav a.active{background:linear-gradient(90deg,var(--accent),var(--accent-2)); color:white; transform:translateY(-4px)}

/* ================= HEADER (video cover + typing) ================= */
.header{
  position:relative;
  height:340px;
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
  margin-bottom:18px;
  border-bottom-left-radius:18px;
  border-bottom-right-radius:18px;
}
.header video{
  position:absolute;
  width:100%;height:100%;
  object-fit:cover;
  filter:brightness(0.6) saturate(.95);
  z-index:0;
}
.header .overlay{
  position:absolute;inset:0;
  background:linear-gradient(180deg, rgba(4,30,60,0.35), rgba(4,30,60,0.08));
  z-index:1;
}
.header .title-wrap{
  position:relative;z-index:2;text-align:center;color:white;
}
.title-typing{
  font-size:32px;font-weight:800;letter-spacing:-0.4px;
  display:inline-block;
  white-space:nowrap;
  overflow:hidden;
  border-right:3px solid rgba(255,255,255,0.9);
  width:26ch; /* safe width for typing */
  animation:typing 3.2s steps(26, end), blink .8s step-end infinite;
}
@keyframes typing{from{width:0} to{width:26ch}}
@keyframes blink{50%{border-color:transparent}}

/* subtitle */
.subtitle{
  margin-top:10px;color:rgba(255,255,255,0.9);font-weight:500;
  font-size:15px;opacity:0.95;
}

/* ================= CONTAINER & CARDS ================= */
.container{
  max-width:1100px;
  margin: -80px auto 80px; /* overlap hero */
  padding:28px;
  position:relative;
  z-index:5;
}

.card{
  background:var(--card);
  border-radius:16px;
  padding:22px;
  margin-bottom:22px;
  box-shadow:var(--shadow);
  border:1px solid rgba(0,0,0,0.04);
}

/* HERO SECTION (profile) */
.hero{
  display:flex;
  gap:24px;
  align-items:center;
  flex-wrap:wrap;
}
.avatar{
  width:260px;height:260px;border-radius:22px;overflow:hidden;
  border:6px solid rgba(255,255,255,0.64);
  box-shadow:0 18px 40px rgba(30,70,140,0.12);
  flex-shrink:0;
}
.avatar img{width:100%;height:100%;object-fit:cover;display:block}
.hero .intro h1{font-size:26px;margin-bottom:6px}
.lead{color:var(--muted);max-width:640px}

/* CATEGORIES GRID */
.category-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(220px,1fr));
  gap:16px;margin-top:12px;
}
.cat{
  background:linear-gradient(180deg, rgba(255,255,255,0.6), rgba(255,255,255,0.35));
  border-radius:14px;padding:16px;text-align:center;font-weight:700;cursor:pointer;
  transition:transform .20s, box-shadow .20s;
  border:1px solid rgba(0,0,0,0.04);
}
.cat:hover{transform:translateY(-6px);box-shadow:0 16px 40px rgba(30,70,140,0.08)}
body.dark .cat{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border:1px solid rgba(255,255,255,0.04)}

/* PROJECT LIST */
.proj-list{list-style:none;padding-left:0;margin-top:10px}
.proj-list li{padding:12px 8px;border-radius:10px;margin-bottom:8px;background:rgba(0,0,0,0.02)}

/* CONTACT */
.contact-grid{display:flex;gap:12px;flex-wrap:wrap;margin-top:12px}
.contact-card{background:var(--card);padding:12px;border-radius:12px;display:flex;gap:12px;align-items:center;border:1px solid rgba(0,0,0,0.04);min-width:220px}
.icon{width:44px;height:44px;border-radius:10px;display:grid;place-items:center;background:linear-gradient(135deg,var(--accent),var(--accent-2));color:white;font-weight:800}

/* Fade/slide reveal */
.fade{opacity:0;transform:translateY(18px);transition:all .7s cubic-bezier(.2,.9,.2,1)}
.fade.show{opacity:1;transform:translateY(0)}

/* Footer */
.footer{text-align:center;color:var(--muted);padding:34px 0 80px}

/* Responsive */
@media(max-width:880px){
  .avatar{width:200px;height:200px}
  .title-typing{font-size:22px}
  nav{padding:8px}
  .container{margin-top:-60px;padding:16px}
}
</style>
</head>

<body>

<!-- Floating shapes -->
<div class="shape" style="left:-80px;top:40px"></div>
<div class="shape b" style="right:-80px;bottom:60px"></div>

<!-- NAV -->
<nav id="mainNav">
  <a href="#home" class="active">Trang chủ</a>
  <a href="#about">Về tôi</a>
  <a href="#categories">Danh mục</a>
  <a href="#projects">Projects</a>
  <a href="#contact">Liên hệ</a>
</nav>

<!-- HEADER with video cover and typing title -->
<header class="header">
  <!-- Cover video (demo source) -->
  <video autoplay muted loop playsinline>
    <!-- Nếu muốn, đổi src thành URL video khác -->
    <source src="https://cdn.coverr.co/videos/blue-ocean-waves/download?token=demo" type="video/mp4">
  </video>
  <div class="overlay"></div>

  <div class="title-wrap">
    <div class="title-typing">Kim Khánh — Portfolio 12A • Design • IELTS • Copywriting</div>
    <div class="subtitle">Web nhỏ lưu hành trình học, dự án và những thứ aesthetic mình làm.</div>
  </div>
</header>

<!-- Dark mode toggle (fixed) -->
<button id="darkToggle" aria-label="Toggle dark mode" style="
  position:fixed;right:18px;bottom:18px;z-index:60;padding:10px 14px;border-radius:999px;
  border:0;background:linear-gradient(90deg,var(--accent),var(--accent-2));color:white;font-weight:800;box-shadow:var(--shadow);
">🌙 Dark</button>

<!-- CONTENT -->
<div class="container">

  <!-- HOME -->
  <section id="home" class="card fade">
    <div class="hero">
      <div class="avatar" aria-hidden="true">
        <img alt="Avatar art-style" src="https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/golden-retriever-tongue-out.jpg">
      </div>

      <div class="intro">
        <h1>Xin chào! Mình là Kim Khánh 👋</h1>
        <p class="lead">
          Học sinh lớp 12A — thích làm web aesthetic, học tiếng Anh và sáng tạo nội dung.
          Mình xây web này để lưu hành trình IELTS, chia sẻ dự án copywriting, và trưng những bài tập thiết kế.
        </p>

        <p style="color:var(--muted);margin-top:10px">
          Sở thích: đọc sách (The Perfection Trap), học tiếng Anh/Spanish/Chinese, làm web, và nghiên cứu tâm lý khách hàng trong ngành pet.
        </p>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="card fade">
    <h2>Về mình</h2>
    <p>
      Mình là <strong>Kim Khánh</strong>, học sinh lớp 12A. Mình thích kết hợp ngôn ngữ, thẩm mỹ và tư duy marketing để tạo nội dung có cảm xúc.
      Mục tiêu hiện tại: <strong>IELTS </strong> và cải thiện portfolio freelance trong copywriting.
    </p>

    <ul style="margin-top:12px; color:var(--muted);">
      <li>🏫 Trường: (điền tên trường nếu muốn)</li>
      <li>🎯 Mục tiêu: IELTS 8.0, ĐGNL 1000+</li>
      <li>💼 Kỹ năng: HTML/CSS, copywriting, email marketing basics, UX basics</li>
      <li>📚 Đang học: Tài chính cơ bản, Spanish căn bản</li>
    </ul>
  </section>

  <!-- CATEGORIES -->
  <section id="categories" class="card fade">
    <h2>Danh mục</h2>
    <div class="category-grid">
      <div class="cat" data-key="ielts">
        <h3>IELTS</h3>
        <p style="font-weight:500;color:var(--muted);margin-top:6px">Tips, bài luyện, bài mẫu Speaking & Writing, roadmap </p>
      </div>

      <div class="cat" data-key="copy">
        <h3>Copywriting</h3>
        <p style="font-weight:500;color:var(--muted);margin-top:6px">Ví dụ email flows, landing page, A/B test copy, voice & tone</p>
      </div>

      <div class="cat" data-key="pet">
        <h3>Pet Brand</h3>
        <p style="font-weight:500;color:var(--muted);margin-top:6px">Nghiên cứu khách hàng, content & memes cho ngành thú cưng</p>
      </div>

      <div class="cat" data-key="beach">
        <h3>Beach Boutique</h3>
        <p style="font-weight:500;color:var(--muted);margin-top:6px">Dự án thương hiệu biển: email, landing & visual storytelling</p>
      </div>

      <div class="cat" data-key="projects">
        <h3>Projects</h3>
        <p style="font-weight:500;color:var(--muted);margin-top:6px">Web, animations, mini tools & study notes</p>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects" class="card fade">
    <h2>Dự án nổi bật</h2>
    <ul class="proj-list">
      <li><strong>🌊 Beach Boutique — Welcome Flow:</strong> 3-email storytelling + 10% discount VIP onboarding (subject line tests)</li>
      <li><strong>🐶 Bulldogology — Landing Rewrite:</strong> Direct-response copy, value-driven bullets, reduced bounce rate (mock)</li>
      <li><strong>📘 IELTS Notes Hub:</strong> Tổng hợp chiến lược Part 1–3, mẫu trả lời Part 2, error log</li>
      <li><strong>💻 Mini Web Aesthetic:</strong> Bộ template HTML/CSS (animations, dark mode, hero video)</li>
      <li><strong>🧪 Pet Brand Psychology Report:</strong> Tại sao meme & emoji tăng engagement</li>
    </ul>

    <p style="margin-top:10px;color:var(--muted)">Muốn thêm project cụ thể vào đây? Gửi tên + mô tả ngắn, mình thêm ngay.</p>
  </section>
<section id="favorite-music" class="card fade">
  <h2>Bài hát yêu thích</h2>
  <div class="music-list">
    <!-- Bài 1 -->
    <div class="music-item">
      <iframe width="100%" height="260"
        src="https://www.youtube.com/embed/_E-7A81Ac8U?rel=0"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
      <p class="music-title">Bài 1</p>
    </div>

    <!-- Bài 2 -->
    <div class="music-item">
      <iframe width="100%" height="260"
        src="https://www.youtube.com/embed/stvWuowo1dU?rel=0"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
      <p class="music-title">Bài 2</p>
    </div>

    <!-- Bài 3 -->
    <div class="music-item">
      <iframe width="100%" height="260"
        src="https://www.youtube.com/embed/Rzm_kltwHbg?rel=0"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
      <p class="music-title">Bài 3</p>
    </div>
</section>

<style>
.music-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
}
.music-item {
  background: var(--card);
  border-radius: var(--radius);
  padding: 12px;
  box-shadow: var(--shadow);
}
.music-title {
  margin-top: 8px;
  font-weight: 600;
  color: var(--text);
  text-align: center;
}
</style>

  <!-- CONTACT -->
  <section id="contact" class="card fade">
    <h2>Liên hệ</h2>
    <p>Nếu bạn muốn hợp tác, xem thêm tài liệu, hoặc trao đổi luyện IELTS — liên hệ mình nhé.</p>

    <div class="contact-grid">
      <div class="contact-card">
        <div class="icon">✉️</div>
        <div>
          <div style="font-weight:700">Email</div>
          <div style="color:var(--muted)">yourmail@example.com</div>
        </div>
      </div>

      <div class="contact-card">
        <div class="icon">📸</div>
        <div>
          <div style="font-weight:700">Instagram</div>
          <div style="color:var(--muted)">@yourhandle</div>
        </div>
      </div>

      <div class="contact-card">
        <div class="icon">🔗</div>
        <div>
          <div style="font-weight:700">More</div>
          <div style="color:var(--muted)">Notion / Linktree (nếu có)</div>
        </div>
      </div>
    </div>
  </section>

  <div class="footer">Made with 💙 by Khánh — design & code</div>
   <a class="back-btn" href="https://daisubinta.github.io/Nhom4tin12anh.github.io/">
    ← Quay lại trang chính
  </a>
</div>

<!-- ================= SCRIPTS: typing, dark, fade, smooth nav, categories ================= -->
<script>
/* Typing animation: (already CSS-driven). If you want to change text dynamically, uncomment below. */
/* Example dynamic typing replacement:
const typingEl = document.querySelector('.title-typing');
const messages = ['Kim Khánh — Portfolio 12A • Design • IELTS • Copywriting', 'Web aesthetic • Projects • Study Notes'];
let idx = 0;
setInterval(()=>{ typingEl.textContent = messages[idx%messages.length]; idx++; }, 4200);
*/

/* Dark mode toggle */
const darkBtn = document.getElementById('darkToggle');
darkBtn.addEventListener('click', () => {
  document.body.classList.toggle('dark');
  if(document.body.classList.contains('dark')) darkBtn.textContent = '☀️ Light';
  else darkBtn.textContent = '🌙 Dark';
});

/* Fade reveal on scroll */
const faders = document.querySelectorAll('.fade');
const appearOptions = {threshold: 0.15, rootMargin: "0px 0px -60px 0px"};
const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll){
  entries.forEach(entry=>{
    if(!entry.isIntersecting) return;
    entry.target.classList.add('show');
    appearOnScroll.unobserve(entry.target);
  });
}, appearOptions);
faders.forEach(f => appearOnScroll.observe(f));

/* Smooth scrolling + active nav */
const navLinks = document.querySelectorAll('nav a');
navLinks.forEach(a => {
  a.addEventListener('click', (e)=>{
    e.preventDefault();
    navLinks.forEach(n=>n.classList.remove('active'));
    a.classList.add('active');
    const id = a.getAttribute('href').replace('#','');
    const el = document.getElementById(id);
    if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
  });
});

/* Category click: quick scroll to Projects and filter (simple demo) */
document.querySelectorAll('.cat').forEach(c => {
  c.addEventListener('click', ()=>{
    const key = c.dataset.key;
    // Basic interaction: highlight and scroll to projects
    document.querySelectorAll('.cat').forEach(x=>x.style.outline='none');
    c.style.outline = '3px solid rgba(95,168,255,0.18)';
    // Scroll to projects
    const proj = document.getElementById('projects');
    if(proj) proj.scrollIntoView({behavior:'smooth'});
    // (Optional) You could implement filtering of projects here
  });
});

/* optional: parallax movement for shapes on mouse move */
document.addEventListener('mousemove', (e)=>{
  const w = window.innerWidth/2;
  const h = window.innerHeight/2;
  const x = (e.clientX - w)/w;
  const y = (e.clientY - h)/h;
  document.querySelectorAll('.shape').forEach((s,i)=>{
    const mult = (i+1)*6;
    s.style.transform = `translate3d(${x*mult}px, ${y*mult}px, 0)`;
  });
});
</script>

</body>
</html>
