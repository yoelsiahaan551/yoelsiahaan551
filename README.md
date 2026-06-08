<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Yoel Siahaan - Profile</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css">
<style>
  * { box-sizing:border-box; margin:0; padding:0; }
  body { background:#f8f9fa; min-height:100vh; display:flex; align-items:center; justify-content:center; font-family:'Segoe UI',sans-serif; }

  @keyframes fadeInDown { from { opacity:0; transform:translateY(-20px); } to { opacity:1; transform:translateY(0); } }
  @keyframes fadeInUp { from { opacity:0; transform:translateY(20px); } to { opacity:1; transform:translateY(0); } }
  @keyframes pulse { 0%,100% { transform:scale(1); } 50% { transform:scale(1.08); } }
  @keyframes float { 0%,100% { transform:translateY(0px); } 50% { transform:translateY(-8px); } }
  @keyframes slideIn { from { opacity:0; transform:translateX(-30px); } to { opacity:1; transform:translateX(0); } }
  @keyframes shimmer { 0% { background-position:-200% center; } 100% { background-position:200% center; } }
  @keyframes blink { 0%,100% { opacity:1; } 50% { opacity:0; } }
  @keyframes badgeIn { from { opacity:0; transform:scale(0.5); } to { opacity:1; transform:scale(1); } }
  @keyframes ripple { 0% { box-shadow:0 0 0 0 rgba(99,102,241,0.3); } 100% { box-shadow:0 0 0 16px rgba(99,102,241,0); } }
  @keyframes typewriter { from { width:0; } to { width:100%; } }
  @keyframes starFloat { 0%,100% { transform:translateY(0) rotate(0deg); opacity:0.7; } 50% { transform:translateY(-12px) rotate(180deg); opacity:1; } }

  .container {
    background:#fff;
    border-radius:16px;
    box-shadow:0 4px 32px rgba(0,0,0,0.08);
    max-width:660px;
    width:100%;
    margin:2rem auto;
    padding:2rem 1.5rem;
    color:#1a1a1a;
  }

  .hero { text-align:center; margin-bottom:2rem; animation: fadeInDown 0.8s ease both; }

  .avatar-ring {
    display:inline-block;
    width:100px; height:100px;
    border-radius:50%;
    background:linear-gradient(135deg,#6366f1,#8b5cf6,#06b6d4);
    padding:3px;
    margin-bottom:1rem;
    animation: float 3s ease-in-out infinite, ripple 2s ease-out infinite;
  }

  .avatar-inner {
    width:100%; height:100%;
    border-radius:50%;
    background:#fff;
    display:flex; align-items:center; justify-content:center;
    font-size:36px; font-weight:600;
    color:#6366f1;
  }

  .name {
    font-size:28px; font-weight:600;
    margin-bottom:0.4rem;
    background: linear-gradient(90deg, #6366f1, #06b6d4, #8b5cf6, #6366f1);
    background-size:200% auto;
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
    background-clip:text;
    animation: shimmer 3s linear infinite;
  }

  .tagline {
    font-size:14px; color:#6b7280;
    margin-bottom:1rem;
    overflow:hidden; white-space:nowrap;
    display:inline-block;
    animation: typewriter 2s steps(50) 0.5s both;
    border-right:2px solid #6366f1;
  }

  .badges { display:flex; gap:8px; justify-content:center; flex-wrap:wrap; margin-bottom:1rem; }

  .badge {
    padding:5px 14px;
    border-radius:20px;
    font-size:12px; font-weight:500;
    border:0.5px solid;
    cursor:pointer;
    transition: transform 0.2s, box-shadow 0.2s;
    animation: badgeIn 0.5s ease both;
    text-decoration:none;
    display:inline-flex; align-items:center; gap:5px;
  }

  .badge:nth-child(1) { animation-delay:1s; background:#EEF2FF; color:#4F46E5; border-color:#C7D2FE; }
  .badge:nth-child(2) { animation-delay:1.2s; background:#FDF2F8; color:#BE185D; border-color:#FBCFE8; }
  .badge:hover { transform:scale(1.1); box-shadow:0 4px 12px rgba(99,102,241,0.2); }

  .divider { height:0.5px; background:#e5e7eb; margin:1.5rem 0; }

  .section-title {
    font-size:16px; font-weight:600;
    margin-bottom:1rem;
    display:flex; align-items:center; gap:8px;
    animation: slideIn 0.6s ease both;
  }

  .section-icon {
    width:28px; height:28px;
    border-radius:8px;
    display:flex; align-items:center; justify-content:center;
    font-size:14px;
  }

  .subsection { margin-bottom:1.5rem; }

  .sub-label {
    font-size:11px; color:#9ca3af;
    margin-bottom:0.6rem;
    letter-spacing:0.08em; font-weight:600;
  }

  .tech-grid { display:flex; flex-wrap:wrap; gap:6px; }

  .tech-badge {
    display:inline-flex; align-items:center; gap:5px;
    padding:5px 10px;
    border-radius:6px;
    font-size:12px; font-weight:500;
    border:0.5px solid;
    cursor:default;
    transition: transform 0.15s, box-shadow 0.15s;
    animation: badgeIn 0.4s ease both;
  }

  .tech-badge:hover {
    transform: translateY(-3px) scale(1.04);
    box-shadow: 0 6px 16px rgba(0,0,0,0.1);
  }

  .dot { width:7px; height:7px; border-radius:50%; display:inline-block; flex-shrink:0; }

  .t-html  { background:#FFF1EE; color:#C2410C; border-color:#FED7AA; }
  .t-css   { background:#EFF6FF; color:#1D4ED8; border-color:#BFDBFE; }
  .t-js    { background:#FEFCE8; color:#854D0E; border-color:#FEF08A; }
  .t-ts    { background:#EFF6FF; color:#1D4ED8; border-color:#93C5FD; }
  .t-react { background:#F0FDFA; color:#0F766E; border-color:#99F6E4; }
  .t-rn    { background:#F0FDFA; color:#0F766E; border-color:#6EE7B7; }
  .t-tw    { background:#F0FDFA; color:#0369A1; border-color:#BAE6FD; }
  .t-mysql { background:#EFF6FF; color:#1E40AF; border-color:#BFDBFE; }
  .t-supa  { background:#ECFDF5; color:#065F46; border-color:#6EE7B7; }
  .t-git   { background:#FFF1EE; color:#9A3412; border-color:#FED7AA; }
  .t-gh    { background:#F9FAFB; color:#111827; border-color:#D1D5DB; }
  .t-vs    { background:#EFF6FF; color:#1D4ED8; border-color:#BFDBFE; }
  .t-post  { background:#FFF7ED; color:#C2410C; border-color:#FED7AA; }
  .t-figma { background:#FDF2F8; color:#9D174D; border-color:#FBCFE8; }

  .about-card {
    background:#f9fafb;
    border:0.5px solid #e5e7eb;
    border-radius:12px;
    padding:1rem 1.25rem;
    font-size:14px; color:#6b7280;
    line-height:1.7;
    animation: fadeInUp 0.6s ease both;
    position:relative; overflow:hidden;
  }

  .about-card::before {
    content:'';
    position:absolute; left:0; top:0; bottom:0;
    width:3px;
    background:linear-gradient(to bottom,#6366f1,#06b6d4);
  }

  .status-row {
    display:flex; align-items:center; gap:6px;
    font-size:12px; color:#9ca3af;
    margin-top:1rem;
    animation: fadeInUp 0.6s ease 1.5s both;
    opacity:0; animation-fill-mode:both;
  }

  .status-dot {
    width:7px; height:7px;
    border-radius:50%; background:#10b981;
    animation: pulse 2s ease-in-out infinite;
    flex-shrink:0;
  }
</style>
</head>
<body>

<div class="container">

  <div class="hero">
    <div class="avatar-ring">
      <div class="avatar-inner">YS</div>
    </div>
    <div class="name">Yoel Siahaan</div>
    <div class="tagline">Fullstack Developer | Mobile Developer | UI/UX Enthusiast</div>
    <div class="badges" style="margin-top:1rem;">
      <a class="badge" href="https://github.com/yoelsiahaan551" target="_blank">
        <i class="ti ti-brand-github"></i> GitHub
      </a>
      <a class="badge" href="https://www.instagram.com/shn_yoel" target="_blank">
        <i class="ti ti-brand-instagram"></i> Instagram
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <div style="animation:fadeInUp 0.6s ease 0.4s both; opacity:0; animation-fill-mode:both;">
    <div class="section-title">
      <div class="section-icon" style="background:#EEF2FF; color:#6366f1;">
        <i class="ti ti-code"></i>
      </div>
      Tech Stack
    </div>

    <div class="subsection">
      <div class="sub-label">FRONTEND</div>
      <div class="tech-grid">
        <span class="tech-badge t-html" style="animation-delay:0.5s"><span class="dot" style="background:#E34F26;"></span>HTML5</span>
        <span class="tech-badge t-css" style="animation-delay:0.6s"><span class="dot" style="background:#1572B6;"></span>CSS3</span>
        <span class="tech-badge t-js" style="animation-delay:0.7s"><span class="dot" style="background:#F7DF1E;"></span>JavaScript</span>
        <span class="tech-badge t-ts" style="animation-delay:0.8s"><span class="dot" style="background:#007ACC;"></span>TypeScript</span>
        <span class="tech-badge t-react" style="animation-delay:0.9s"><span class="dot" style="background:#61DAFB;"></span>React</span>
        <span class="tech-badge t-rn" style="animation-delay:1.0s"><span class="dot" style="background:#61DAFB;"></span>React Native</span>
        <span class="tech-badge t-tw" style="animation-delay:1.1s"><span class="dot" style="background:#38B2AC;"></span>Tailwind CSS</span>
      </div>
    </div>

    <div class="subsection">
      <div class="sub-label">BACKEND & DATABASE</div>
      <div class="tech-grid">
        <span class="tech-badge t-mysql" style="animation-delay:1.2s"><span class="dot" style="background:#4479A1;"></span>MySQL</span>
        <span class="tech-badge t-supa" style="animation-delay:1.3s"><span class="dot" style="background:#3ECF8E;"></span>Supabase</span>
      </div>
    </div>

    <div class="subsection">
      <div class="sub-label">TOOLS & PLATFORM</div>
      <div class="tech-grid">
        <span class="tech-badge t-git" style="animation-delay:1.4s"><span class="dot" style="background:#F05032;"></span>Git</span>
        <span class="tech-badge t-gh" style="animation-delay:1.5s"><span class="dot" style="background:#181717;"></span>GitHub</span>
        <span class="tech-badge t-vs" style="animation-delay:1.6s"><span class="dot" style="background:#007ACC;"></span>VS Code</span>
        <span class="tech-badge t-post" style="animation-delay:1.7s"><span class="dot" style="background:#FF6C37;"></span>Postman</span>
        <span class="tech-badge t-figma" style="animation-delay:1.8s"><span class="dot" style="background:#F24E1E;"></span>Figma</span>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div style="animation:fadeInUp 0.6s ease 1s both; opacity:0; animation-fill-mode:both;">
    <div class="section-title">
      <div class="section-icon" style="background:#FDF2F8; color:#BE185D;">
        <i class="ti ti-sparkles"></i>
      </div>
      Tentang Saya
    </div>
    <div class="about-card">
      Hai! Aku Yoel — developer yang suka membangun aplikasi web dan mobile yang fungsional sekaligus indah.
      Senang menjelajahi teknologi baru dan menciptakan pengalaman pengguna yang menyenangkan. ✨
    </div>
  </div>

  <div class="status-row">
    <span class="status-dot"></span>
    <span>Available for collaboration</span>
    <span style="margin-left:auto; opacity:0.5; font-size:11px;">yoelsiahaan551</span>
  </div>

</div>

</body>
</html>
