<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Huỳnh Kim Khánh — Portfolio nghệ thuật</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&family=Playfair+Display:wght@600;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg-1: #e8f7ff;
      --bg-2: #d9f0ff;
      --ocean-1: #0b7285;
      --ocean-2: #0ea5a3;
      --card: rgba(255,255,255,0.9);
      --muted: #4b5563;
      --glass: rgba(255,255,255,0.55);
      --radius: 18px;
      --maxw: 1100px;
    }

    /* Reset */
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,-apple-system,'Segoe UI',Roboto,Arial;color:#042235;-webkit-font-smoothing:antialiased}
    a{color:inherit;text-decoration:none}

    /* Page background */
    body{
      background: radial-gradient(1200px 400px at 10% 10%, rgba(14,165,163,0.06), transparent),
                  linear-gradient(180deg,var(--bg-1),var(--bg-2));
      -webkit-font-smoothing:antialiased;
      font-size:16px;
      line-height:1.6;
    }

    /* Nav */
    nav {
      position:fixed; inset:0 0 auto 0; top:0; left:0; right:0;
      display:flex; align-items:center; justify-content:space-between;
      padding:18px calc((100vw - var(--maxw))/2 + 20px);
      z-index:60;
      backdrop-filter: blur(8px);
    }
    .brand {
      display:flex; gap:12px; align-items:center;
    }
    .logo {
      width:48px; height:48px; border-radius:12px;
      background: linear-gradient(135deg,var(--ocean-1),var(--ocean-2));
      display:grid; place-items:center; color:white; font-weight:800;
      box-shadow: 0 6px 20px rgba(6,78,90,0.12);
    }
    .site-name {font-weight:700; letter-spacing:0.6px}
    .nav-links {display:flex; gap:22px; align-items:center}
    .nav-links a{font-weight:600; color:rgba(4,34,53,0.9); padding:8px 12px; border-radius:10px}
    .nav-links a:hover, .nav-links a.active{background:rgba(255,255,255,0.6); box-shadow:0 8px 18px rgba(6,78,90,0.06)}

    /* Hero */
    .hero {
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding: calc(80px + 20px) 20px 120px;
      position:relative;
      text-align:center;
      overflow:visible;
    }
    .hero .inner {
      max-width:var(--maxw);
      width:100%;
      margin:auto;
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:36px;
      align-items:center;
    }
    .hero-left { text-align:left; padding:40px; }
    .eyebrow {
      display:inline-block; font-weight:700; font-size:14px; color:var(--ocean-1);
      padding:8px 14px; border-radius:999px; background:rgba(14,165,163,0.08);
      margin-bottom:18px;
    }
    h1.display {
      font-family: "Playfair Display", serif;
      font-size:48px;
      line-height:1.02;
      margin:0 0 18px;
      color: #042235;
      letter-spacing:-1px;
    }
    p.lead { color:var(--muted); font-size:18px; margin:0 0 24px; max-width:70% }

    .cta { display:flex; gap:14px; align-items:center; margin-top:8px }
    .btn {
      background: linear-gradient(90deg,var(--ocean-1),var(--ocean-2));
      color:white; padding:12px 18px; border-radius:12px; font-weight:700;
      box-shadow:0 12px 30px rgba(6,78,90,0.12);
    }
    .btn.ghost { background:transparent; color:var(--ocean-1); border:1px solid rgba(6,78,90,0.08) }

    /* Hero right - portrait / art */
    .hero-right {
      display:flex; align-items:center; justify-content:center; gap:18px;
    }
    .card-art {
      width:420px; border-radius:18px; overflow:hidden; background:var(--card);
      padding:18px; box-shadow:0 20px 48px rgba(6,78,90,0.08);
      transform:translateY(0); transition:transform .45s ease;
    }
    .card-art img{ width:100%; height:320px; object-fit:cover; border-radius:10px; display:block; }

    /* floating shapes for artistic effect */
    .shape {
      position:absolute; border-radius:999px; filter:blur(24px); opacity:0.26; pointer-events:none;
      mix-blend-mode:overlay;
    }
    .shape.s1{ width:420px;height:420px; right:6%; top:10%; background:linear-gradient(90deg,#8ee3df,#68c6d2) }
    .shape.s2{ width:260px;height:260px; left:8%; bottom:6%; background:linear-gradient(90deg,#b7e7ff,#9fdcff) }

    /* Sections general */
    main { margin-top:20px; }
    section.block {
      max-width: var(--maxw); margin: 48px auto; padding:40px; border-radius:14px;
      background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.92));
      box-shadow: 0 18px 48px rgba(6,78,90,0.04);
      border: 1px solid rgba(6,78,90,0.03);
    }
    section.block h2 { margin:0 0 14px; font-size:22px; color:var(--ocean-1); font-weight:800 }
    section.block p { color:var(--muted); margin-bottom:10px; }

    /* Projects grid */
    .projects-grid { display:grid; grid-template-columns: repeat(auto-fit,minmax(240px,1fr)); gap:18px; margin-top:18px }
    .project {
      padding:18px; border-radius:12px; background:linear-gradient(180deg, rgba(14,165,163,0.03), rgba(14,165,163,0.01));
      border:1px solid rgba(6,78,90,0.04); transition: transform .28s ease, box-shadow .28s ease;
    }
    .project:hover{ transform:translateY(-6px); box-shadow:0 18px 40px rgba(6,78,90,0.06) }
    .project h3{ margin:0 0 8px; font-size:18px; color:#043a44}
    .project p{ margin:0; color:var(--muted) }

    /* Two-col about */
    .two-col { display:grid; grid-template-columns: 1fr 1fr; gap:26px; align-items:start }
    .about-quote { font-style:italic; color:#0f4b57; font-size:18px; margin-bottom:16px }

    /* Contact form (simple) */
    .contact-grid { display:grid; grid-template-columns: 1fr 360px; gap:20px; align-items:start }
    .contact-card { padding:18px; border-radius:12px; background:linear-gradient(180deg, rgba(14,165,163,0.03), rgba(255,255,255,0.6)); border:1px solid rgba(6,78,90,0.04) }
    .contact-card a{ color:var(--ocean-1); font-weight:700 }

    /* Footer */
    footer { text-align:center; padding:40px 20px; color:var(--muted) }

    /* responsive */
    @media (max-width:1024px){
      .hero .inner { grid-template-columns: 1fr; text-align:center }
      .hero-left { padding:8px; }
      p.lead{ max-width:100% }
      .two-col{ grid-template-columns: 1fr; }
      .contact-grid{ grid-template-columns: 1fr; }
      nav { padding:12px 18px }
    }

    /* subtle reveal animation classes */
    .reveal { opacity:0; transform: translateY(14px); transition: all .6s cubic-bezier(.2,.9,.3,1) }
    .reveal.show { opacity:1; transform: none }

    /* small helpers */
    .muted { color:var(--muted); font-size:15px }
    .kicker { font-size:13px; color:var(--ocean-1); font-weight:700; letter-spacing:0.6px }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="brand">
      <div class="logo">HK</div>
      <div>
        <div class="site-name">Huỳnh Kim Khánh</div>
        <div class="muted" style="font-size:13px">Copywriter • Language Explorer</div>
      </div>
    </div>

    <div class="nav-links" aria-hidden>
      <a href="#home" class="active">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#work">Work</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- HERO -->
  <header class="hero" id="home" role="banner">
    <div class="shape s1" aria-hidden></div>
    <div class="shape s2" aria-hidden></div>

    <div class="inner" role="presentation">
      <div class="hero-left">
        <div class="eyebrow">Hello — I'm Khánh</div>
        <h1 class="display reveal">Viết để kết nối — Tạo nội dung có chiều sâu.</h1>
        <p class="lead reveal">Mình sáng tạo nội dung tập trung vào cảm xúc và hành vi người đọc. Đây là nơi mình lưu trữ ý tưởng, dự án thử nghiệm và những bài viết ngắn — rõ ràng, tinh tế và có nhịp.</p>

        <div class="cta reveal" style="margin-top:20px">
          <a href="#projects" class="btn">Xem dự án</a>
          <a href="#contact" class="btn ghost">Liên hệ</a>
        </div>
      </div>

      <div class="hero-right reveal" style="text-align:center">
        <div class="card-art" id="artCard" aria-hidden>
          <!-- Replace src with your image if you want -->
          <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=1400" alt="Art / mood image" />
          <div style="padding:12px 6px;">
            <div style="font-weight:800; color:var(--ocean-1); font-size:15px">Moodboard • Ocean • Calm</div>
            <div class="muted" style="font-size:14px">Một bức ảnh để gợi mood và tông màu cho portfolio.</div>
          </div>
        </div>
      </div>
    </div>
  </header>

  <main>
    <!-- ABOUT -->
    <section class="block reveal" id="about" aria-labelledby="aboutTitle">
      <h2 id="aboutTitle">Giới thiệu</h2>
      <div class="two-col">
        <div>
          <p class="about-quote">“Tôi tin nội dung tốt là câu chuyện đúng thời điểm — đơn giản nhưng không tầm thường.”</p>
          <p class="muted">Mình là một người thích viết, học ngôn ngữ và thử nghiệm với các định dạng nội dung: email ngắn, microblog, và landing copy. Trong mọi nội dung, mình ưu tiên tính rõ ràng, nhịp điệu và gọi được hành động (soft).</p>
          <p class="muted">Phong cách: chân thành, rõ ràng, có nhạc — phù hợp với thương hiệu tinh tế và thân thiện.</p>
        </div>

        <div>
          <h3 class="kicker">Cái mình làm</h3>
          <ul style="margin-top:8px">
            <li>✍️ Copywriting chuyển đổi (email, landing)</li>
            <li>🎨 Nội dung sáng tạo (microcontent, social snippets)</li>
            <li>🔁 Chuỗi nurturing — viết để giữ kết nối</li>
          </ul>

          <div style="margin-top:18px">
            <div class="kicker">Kỹ năng</div>
            <div style="display:flex; gap:8px; flex-wrap:wrap; margin-top:8px">
              <span style="background:rgba(14,165,163,0.08);padding:8px 12px;border-radius:999px;font-weight:700;color:var(--ocean-1)">Email</span>
              <span style="background:rgba(14,165,163,0.06);padding:8px 12px;border-radius:999px">Landing</span>
              <span style="background:rgba(14,165,163,0.04);padding:8px 12px;border-radius:999px">Canva</span>
              <span style="background:rgba(14,165,163,0.04);padding:8px 12px;border-radius:999px">Translation</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section class="block reveal" id="projects" aria-labelledby="projectsTitle">
      <h2 id="projectsTitle">Dự án & thử nghiệm</h2>
      <p class="muted">Dưới đây là vài ghi chép nhanh về dự án mình từng làm hoặc thử nghiệm — mục đích là minh họa phong cách, không phải case study đầy đủ.</p>

      <div class="projects-grid" style="margin-top:18px">
        <div class="project">
          <h3>Ghi chú học tập — Micro-notes</h3>
          <p>Chuỗi bài viết ngắn tóm tắt kỹ thuật học từ vựng và ghi nhớ bằng hình ảnh.</p>
        </div>

        <div class="project">
          <h3>Landing thử nghiệm — Pet Brand</h3>
          <p>Landing page bán kèm thẻ ưu đãi, tập trung A/B testing tiêu đề và CTA.</p>
        </div>

        <div class="project">
          <h3>Email Nurture Flow</h3>
          <p>Chuỗi 5 email cho subscribers mới, tập trung chuyển đổi nhẹ nhàng và xây dựng trust.</p>
        </div>

        <div class="project">
          <h3>Micro-content cho TikTok</h3>
          <p>Ý tưởng kịch bản ngắn giúp biến insight thành hook 3s đầu.</p>
        </div>
      </div>
    </section>

    <!-- WORK / SERVICES -->
    <section class="block reveal" id="work" aria-labelledby="workTitle">
      <h2 id="workTitle">Dịch vụ / Hợp tác</h2>
      <p class="muted">Mình nhận những công việc nhỏ ↔ trung hạn phù hợp với học sinh/creator: email series, landing copy, microcontent, và proofreading tiếng Anh.</p>

      <div style="display:flex; gap:16px; margin-top:18px; flex-wrap:wrap">
        <div style="flex:1; min-width:220px; padding:18px; border-radius:12px; background:rgba(14,165,163,0.03); border:1px solid rgba(6,78,90,0.03)">
          <strong>Package A</strong>
          <p class="muted" style="margin:8px 0 0">1 landing + 3 email follow-up (basic)</p>
        </div>

        <div style="flex:1; min-width:220px; padding:18px; border-radius:12px; background:rgba(14,165,163,0.02); border:1px solid rgba(6,78,90,0.03)">
          <strong>Package B</strong>
          <p class="muted" style="margin:8px 0 0">Microcontent bundle (10 captions / 5 scripts)</p>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="block reveal" id="contact" aria-labelledby="contactTitle">
      <h2 id="contactTitle">Liên hệ</h2>

      <div class="contact-grid">
        <div>
          <p class="muted">Nếu bạn muốn trao đổi dự án nhỏ, hợp tác nội dung, hay đặt câu hỏi — gửi email hoặc nhắn qua mạng xã hội. Mình trả lời thường xuyên (ngoại trừ lúc bận học).</p>
          <div style="margin-top:14px" class="contact-card">
            <div style="display:flex; gap:14px; align-items:center">
              <div style="width:54px;height:54px;border-radius:12px;background:linear-gradient(135deg,var(--ocean-1),var(--ocean-2));display:grid;place-items:center;color:white;font-weight:800">✉️</div>
              <div>
                <div style="font-weight:700">Email</div>
                <a href="mailto:your-email@example.com">your-email@example.com</a>
              </div>
            </div>

            <div style="margin-top:12px; display:flex; gap:10px; flex-wrap:wrap">
              <a class="btn" href="mailto:your-email@example.com">Gửi email</a>
              <a class="btn ghost" href="#projects">Xem dự án</a>
            </div>
          </div>
        </div>

        <div>
          <!-- small contact form (no backend) -->
          <form id="contactForm" style="display:flex;flex-direction:column;gap:10px">
            <input name="name" placeholder="Tên của bạn" style="padding:12px;border-radius:8px;border:1px solid rgba(6,78,90,0.06)" />
            <input name="email" placeholder="Email" style="padding:12px;border-radius:8px;border:1px solid rgba(6,78,90,0.06)" />
            <textarea name="message" rows="5" placeholder="Nội dung ngắn" style="padding:12px;border-radius:8px;border:1px solid rgba(6,78,90,0.06)"></textarea>
            <button type="submit" class="btn">Gửi liên hệ</button>
            <div id="formNote" class="muted" style="font-size:13px">Ghi chú: Form này gửi email mặc định (mailto) — cần backend để hoạt động tự động.</div>
          </form>
        </div>
      </div>
    </section>

  </main>

  <footer>
    © <span id="year"></span> Huỳnh Kim Khánh — Thiết kế & nội dung: rõ ràng, nghệ thuật.
  </footer>

  <script>
    // Fill year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for nav
    document.querySelectorAll('nav a, .nav-links a').forEach(a=>{
      a.addEventListener('click', function(e){
        const href = this.getAttribute('href');
        if(href && href.startsWith('#')) {
          e.preventDefault();
          document.querySelectorAll('.nav-links a').forEach(n=>n.classList.remove('active'));
          this.classList.add('active');
          const el = document.querySelector(href);
          if(!el) return;
          el.scrollIntoView({behavior:'smooth', block:'start'});
          // small offset for fixed nav
          window.scrollBy(0, -18);
        }
      });
    });

    // Simple Intersection Observer reveal
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(entry=>{
        if(entry.isIntersecting){
          entry.target.classList.add('show');
          io.unobserve(entry.target);
        }
      });
    }, {threshold: 0.12});

    document.querySelectorAll('.reveal').forEach(el=>{
      io.observe(el);
    });

    // Floating slight parallax effect for art card
    const art = document.getElementById('artCard');
    window.addEventListener('mousemove', (e)=>{
      const w = window.innerWidth, h = window.innerHeight;
      const nx = (e.clientX - w/2) / (w/2);
      const ny = (e.clientY - h/2) / (h/2);
      art.style.transform = `translate3d(${nx*6}px, ${ny*6}px, 0)`;
    });

    // Contact form behavior: open mailto if user fills
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      const name = encodeURIComponent(this.name.value.trim() || 'Kết nối');
      const email = encodeURIComponent(this.email.value.trim() || '');
      const msg = encodeURIComponent(this.message.value.trim() || 'Xin chào — muốn liên hệ với bạn.');
      const subject = encodeURIComponent('Liên hệ từ ' + (this.name.value.trim() || 'Người liên hệ'));
      const body = encodeURIComponent(`Tên: ${name}%0AEmail: ${email}%0A%0A${msg}`);
      // mailto fallback
      window.location.href = `mailto:your-email@example.com?subject=${subject}&body=${body}`;
    });

    // small: update active nav on scroll
    const sections = Array.from(document.querySelectorAll('main section, header.hero'));
    window.addEventListener('scroll', ()=>{
      let current = sections.find(s=>{
        const r = s.getBoundingClientRect();
        return r.top <= window.innerHeight * 0.35 && r.bottom > window.innerHeight*0.2;
      });
      if(current) {
        const id = current.id || 'home';
        document.querySelectorAll('.nav-links a').forEach(a=>a.classList.toggle('active', a.getAttribute('href') === '#' + id));
      }
    });

  </script>
</body>
</html>
