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
:root {
  --primary: #2563eb;
  --secondary: #1e40af;
}

/* BACKGROUND */
body {
  margin: 0;
  font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, Arial;
  background: url("https://raw.githubusercontent.com/daisubinta/Nhom4tin12anh.github.io/refs/heads/main/beach-wallpaper-3840x2160-sandy-shore-sunset-12590.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  overflow-x: hidden;
}

/* HEADER TEXT */
header {
  text-align:center;
  padding:110px 20px 50px;
  position:relative;
  overflow:hidden;
}

.hero-title {
  font-size:68px;
  font-weight:900;
  margin:0;
  text-transform:uppercase;

  /* Stroke viền chữ */
  -webkit-text-stroke: 2px #93c5fd;

  /* Shadow 3 lớp */
  text-shadow:
    0 0 14px rgba(255,255,255,0.7),
    0 6px 28px rgba(37,99,235,0.6),
    0 12px 45px rgba(0,0,0,0.55);

  /* Gradient chữ */
  background: linear-gradient(to right, #ffffff, #bfdbfe, #60a5fa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  /* Chuyển động */
  animation: glowScale 2.5s infinite alternate ease-in-out;
  position:relative;
  display:inline-block;
}

/* Ánh nắng shimmer chạy qua chữ */
.hero-title::after {
  content:"";
  position:absolute;
  top:0;left:-120%;
  width:120%;height:100%;
  background:linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
  transform:skewX(-22deg);
  animation: shine 3.5s ease-in-out infinite;
}

@keyframes shine {
  0% { left:-130%; }
  100% { left:130%; }
}

@keyframes glowScale {
  0% { opacity:0.95; transform:scale(1); }
  100% { opacity:1; transform:scale(1.06); }
}

.hero-tagline {
  font-size:22px;
  font-weight:600;
  color:#f0f9ff;
  margin-top:18px;
  background:rgba(0,0,0,0.32);
  display:inline-block;
  padding:10px 26px;
  border-radius:40px;
  backdrop-filter:blur(8px);
  box-shadow:0 4px 30px rgba(255,255,255,0.2);
  text-shadow:0 0 8px rgba(255,255,255,0.5);
}

/* CONTAINER */
.container {
  max-width:1000px;
  margin:10px auto 80px;
  padding:20px;
}

.card {
  display:flex;
  flex-wrap:wrap;
  border-radius:24px;
  background:rgba(255,255,255,0.78);
  backdrop-filter:blur(15px);
  box-shadow:0 15px 45px rgba(0,0,0,0.25);
  transition:0.5s;
}
.c
