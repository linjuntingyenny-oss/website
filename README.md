[index.html](https://github.com/user-attachments/files/28379934/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bridge Housing — Community Events</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --sage:#4a7c59;--sage-light:#e8f0ea;--sage-mid:#c2d9c8;
  --warm:#f5f0e8;--warm-dark:#e8ddd0;--ink:#1a1a18;
  --ink-mid:#4a4a46;--ink-light:#8a8a84;--terracotta:#b85c3a;
  --cream:#faf8f4;--white:#ffffff;
}
html{scroll-behavior:smooth}
body{font-family:'DM Sans',sans-serif;background:var(--cream);color:var(--ink);font-size:16px;line-height:1.7}

/* ── LAYOUT SHELL ─────────────────────────────── */
.page-shell{display:flex;min-height:100vh}

/* ── SIDEBAR ──────────────────────────────────── */
.lang-sidebar{
  width:220px;min-width:220px;background:var(--sage);
  position:fixed;top:0;left:0;height:100vh;
  overflow-y:auto;z-index:200;display:flex;
  flex-direction:column;padding:2rem 1.2rem 1.5rem;
  box-shadow:3px 0 16px rgba(0,0,0,0.12)
}
.sidebar-logo{font-family:'DM Serif Display',serif;font-size:1.25rem;color:#fff;margin-bottom:0.25rem;line-height:1.2}
.sidebar-logo-sub{font-size:0.72rem;color:rgba(255,255,255,0.6);letter-spacing:0.07em;text-transform:uppercase;margin-bottom:2rem}
.lang-sidebar-label{font-size:0.68rem;font-weight:500;color:rgba(255,255,255,0.55);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.75rem}
.lang-btn{
  display:flex;align-items:center;gap:0.75rem;
  background:rgba(255,255,255,0.1);border:1px solid rgba(255,255,255,0.18);
  color:rgba(255,255,255,0.88);font-family:'DM Sans',sans-serif;
  font-size:1rem;padding:10px 14px;border-radius:10px;cursor:pointer;
  transition:background 0.2s;font-weight:400;width:100%;text-align:left;margin-bottom:6px
}
.lang-btn:hover{background:rgba(255,255,255,0.2)}
.lang-btn.active{background:#fff;color:var(--sage);font-weight:500;border-color:#fff}
.lang-flag{font-size:1.3rem;line-height:1;flex-shrink:0}
.lang-name-wrap{display:flex;flex-direction:column}
.lang-name{font-size:1rem;line-height:1.2}
.lang-sub-name{font-size:0.72rem;opacity:0.65}
.lang-btn.active .lang-sub-name{opacity:0.55}
.sidebar-divider{height:1px;background:rgba(255,255,255,0.15);margin:1.2rem 0}
.sidebar-nav-label{font-size:0.68rem;font-weight:500;color:rgba(255,255,255,0.55);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.75rem}
.sidebar-nav a{display:block;font-size:0.9rem;color:rgba(255,255,255,0.78);text-decoration:none;padding:7px 10px;border-radius:8px;margin-bottom:2px;transition:background 0.2s,color 0.2s}
.sidebar-nav a:hover{background:rgba(255,255,255,0.12);color:#fff}
.sidebar-help{margin-top:auto;padding-top:1.5rem}
.help-btn-side{
  display:flex;align-items:center;gap:0.6rem;
  background:rgba(255,255,255,0.12);border:1px solid rgba(255,255,255,0.22);
  border-radius:10px;padding:11px 14px;color:rgba(255,255,255,0.9);
  font-size:0.9rem;cursor:pointer;width:100%;font-family:'DM Sans',sans-serif;transition:background 0.2s
}
.help-btn-side:hover{background:rgba(255,255,255,0.22)}
.help-q{font-size:1.1rem;font-weight:700;background:rgba(255,255,255,0.2);border-radius:50%;width:26px;height:26px;display:flex;align-items:center;justify-content:center;flex-shrink:0}

/* ── MAIN ─────────────────────────────────────── */
.main-content{margin-left:220px;flex:1;min-width:0}
nav{
  position:sticky;top:0;z-index:100;
  background:rgba(250,248,244,0.94);backdrop-filter:blur(12px);
  border-bottom:1px solid var(--warm-dark);padding:0 2rem;
  display:flex;align-items:center;justify-content:flex-end;height:52px
}
.nav-links{display:flex;gap:1.5rem;list-style:none}
.nav-links a{font-size:0.82rem;font-weight:500;color:var(--ink-mid);text-decoration:none;letter-spacing:0.03em;transition:color 0.2s}
.nav-links a:hover{color:var(--sage)}

section{padding:80px 2rem 70px;display:flex;align-items:center}
.container{max-width:980px;margin:0 auto;width:100%}

/* ── HERO ─────────────────────────────────────── */
#home{background:var(--cream);position:relative;overflow:hidden;min-height:100vh}
#home::before{content:'';position:absolute;top:-80px;right:-120px;width:480px;height:480px;border-radius:50%;background:radial-gradient(circle,var(--sage-light) 0%,transparent 70%);pointer-events:none}
.hero-layout{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:center}
.hero-eyebrow{font-size:0.73rem;font-weight:500;letter-spacing:0.12em;text-transform:uppercase;color:var(--sage);margin-bottom:1.1rem}
.hero-title{font-family:'DM Serif Display',serif;font-size:clamp(1.9rem,3.8vw,3.2rem);line-height:1.15;color:var(--ink);margin-bottom:1.4rem}
.hero-title em{font-style:italic;color:var(--sage)}
.hero-body{font-size:0.97rem;color:var(--ink-mid);margin-bottom:1.8rem;line-height:1.85}
.hero-tags{display:flex;flex-wrap:wrap;gap:0.45rem}
.tag{font-size:0.73rem;font-weight:500;padding:4px 11px;border-radius:20px;border:1px solid var(--sage-mid);color:var(--sage);background:var(--sage-light)}
.hero-image-wrap{border-radius:20px;overflow:hidden;height:400px;position:relative}
.hero-image-wrap img{width:100%;height:100%;object-fit:cover}
.hero-image-caption{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(transparent,rgba(0,0,0,0.52));padding:1.5rem 1.2rem 1rem}
.hero-image-caption span{font-size:0.76rem;color:rgba(255,255,255,0.88)}

/* ── SECTION LABELS ───────────────────────────── */
.section-label{font-size:0.7rem;font-weight:500;letter-spacing:0.14em;text-transform:uppercase;color:var(--terracotta);margin-bottom:0.65rem}
.section-title{font-family:'DM Serif Display',serif;font-size:clamp(1.6rem,3vw,2.5rem);line-height:1.2;color:var(--ink);margin-bottom:1.1rem}
.section-body{font-size:0.95rem;color:var(--ink-mid);max-width:580px;margin-bottom:2rem;line-height:1.85}

/* ── PROBLEM ──────────────────────────────────── */
#problem{background:var(--ink);min-height:100vh}
#problem .section-label{color:var(--sage-mid)}
#problem .section-title{color:var(--white)}
#problem .section-body{color:rgba(255,255,255,0.58)}
.problem-layout{display:grid;grid-template-columns:1.1fr 0.9fr;gap:3rem;align-items:start}
.problem-img{border-radius:16px;overflow:hidden;height:360px;margin-top:0.5rem}
.problem-img img{width:100%;height:100%;object-fit:cover;filter:grayscale(15%) brightness(0.82)}
.problem-grid{display:flex;flex-direction:column;gap:1px;background:rgba(255,255,255,0.07);border-radius:12px;overflow:hidden}
.problem-item{padding:1.1rem 1.4rem;background:#222220;transition:background 0.2s;display:flex;gap:1rem;align-items:flex-start}
.problem-item:hover{background:#2c2c2a}
.problem-num{font-family:'DM Serif Display',serif;font-size:1.3rem;color:var(--sage);opacity:0.45;line-height:1;flex-shrink:0;width:26px}
.problem-text{font-size:0.86rem;color:rgba(255,255,255,0.72);line-height:1.65}

/* ── SOLUTION ─────────────────────────────────── */
#solution{background:var(--warm);min-height:100vh}
.solution-cards{display:grid;grid-template-columns:repeat(3,1fr);gap:1.1rem;margin-top:0.5rem}
.solution-card{background:var(--white);border-radius:16px;padding:1.4rem;border:1px solid var(--warm-dark);transition:transform 0.2s,box-shadow 0.2s}
.solution-card:hover{transform:translateY(-4px);box-shadow:0 12px 32px rgba(0,0,0,0.08)}
.card-img{border-radius:10px;overflow:hidden;height:130px;margin-bottom:1rem}
.card-img img{width:100%;height:100%;object-fit:cover}
.card-title{font-family:'DM Serif Display',serif;font-size:1.1rem;color:var(--ink);margin-bottom:0.45rem}
.card-body{font-size:0.83rem;color:var(--ink-mid);line-height:1.7}

/* ── SPACE ────────────────────────────────────── */
#space{background:var(--cream);min-height:100vh}
.space-layout{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:center}
.space-images{display:grid;grid-template-columns:1fr 1fr;gap:9px}
.space-images img{border-radius:12px;width:100%;height:155px;object-fit:cover}
.space-images img:first-child{grid-column:1/-1;height:190px}
.space-list{list-style:none;display:flex;flex-direction:column;gap:0.9rem}
.space-list li{display:flex;align-items:flex-start;gap:0.8rem;font-size:0.91rem;color:var(--ink-mid);line-height:1.65}
.dot{width:7px;height:7px;border-radius:50%;background:var(--sage);flex-shrink:0;margin-top:8px}

/* ── EVENTS HUB ───────────────────────────────── */
#events-hub{background:var(--warm);min-height:100vh}
#events-hub .section-label{color:var(--terracotta)}

/* Level 1 — main categories */
.cat-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;margin-bottom:2rem}
.cat-card{
  background:var(--white);border:1.5px solid var(--warm-dark);border-radius:18px;
  overflow:hidden;cursor:pointer;transition:transform 0.18s,box-shadow 0.18s,border-color 0.18s
}
.cat-card:hover{transform:translateY(-3px);box-shadow:0 10px 28px rgba(74,124,89,0.13);border-color:var(--sage-mid)}
.cat-card.active{border-color:var(--sage);box-shadow:0 10px 28px rgba(74,124,89,0.18)}
.cat-photo{width:100%;height:140px;object-fit:cover;display:block}
.cat-body{padding:1rem 1.1rem}
.cat-title{font-family:'DM Serif Display',serif;font-size:1.05rem;color:var(--ink);margin-bottom:0.2rem}
.cat-eng{font-size:0.72rem;color:var(--ink-light);letter-spacing:0.04em}

/* Level 2 — subcategories */
.subcat-wrap{display:none;margin-top:0.5rem}
.subcat-wrap.visible{display:block}
.level-back{display:inline-flex;align-items:center;gap:0.5rem;font-size:0.85rem;color:var(--sage);font-weight:500;cursor:pointer;border:none;background:none;padding:0;margin-bottom:1.2rem;font-family:'DM Sans',sans-serif}
.level-back:hover{text-decoration:underline}
.subcat-heading{font-family:'DM Serif Display',serif;font-size:1.6rem;color:var(--ink);margin-bottom:1.2rem}
.subcat-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0.9rem}
.subcat-card{
  background:var(--white);border:1.5px solid var(--warm-dark);border-radius:14px;
  overflow:hidden;cursor:pointer;transition:transform 0.18s,box-shadow 0.18s,border-color 0.18s
}
.subcat-card:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(74,124,89,0.1);border-color:var(--sage-mid)}
.subcat-card.active{border-color:var(--sage)}
.subcat-photo{width:100%;height:100px;object-fit:cover;display:block}
.subcat-body{padding:0.75rem 1rem}
.subcat-name{font-size:0.95rem;font-weight:500;color:var(--ink);line-height:1.3}
.subcat-name-zh{font-size:0.75rem;color:var(--ink-light)}

/* Level 3 — event cards */
.events-list-wrap{display:none;margin-top:0.5rem}
.events-list-wrap.visible{display:block}
.events-list-title{font-family:'DM Serif Display',serif;font-size:1.6rem;color:var(--ink);margin-bottom:1.2rem}
.event-card{
  background:var(--white);border:1px solid var(--warm-dark);border-radius:18px;
  padding:1.5rem 1.7rem;margin-bottom:1rem;position:relative;overflow:hidden;transition:box-shadow 0.2s
}
.event-card::before{content:'';position:absolute;left:0;top:0;bottom:0;width:5px;background:var(--sage);border-radius:0}
.event-card.cancelled::before{background:var(--terracotta)}
.event-card:hover{box-shadow:0 8px 24px rgba(0,0,0,0.07)}
.event-header{display:flex;align-items:flex-start;justify-content:space-between;gap:1rem;margin-bottom:0.9rem;flex-wrap:wrap}
.event-name{font-family:'DM Serif Display',serif;font-size:1.2rem;color:var(--ink);line-height:1.25}
.event-badge{font-size:0.72rem;font-weight:500;padding:4px 12px;border-radius:20px;white-space:nowrap;flex-shrink:0}
.badge-regular{background:var(--sage-light);color:var(--sage);border:1px solid var(--sage-mid)}
.badge-cancel{background:#fbeae5;color:var(--terracotta);border:1px solid #e8c0b0}
.event-meta{display:flex;flex-wrap:wrap;gap:1.4rem;margin-bottom:0.85rem}
.event-meta-item{display:flex;align-items:flex-start;gap:0.55rem}
.meta-icon{font-size:1rem;flex-shrink:0;margin-top:2px}
.meta-text{display:flex;flex-direction:column}
.meta-lbl{font-size:0.68rem;font-weight:500;letter-spacing:0.08em;text-transform:uppercase;color:var(--ink-light)}
.meta-val{font-size:0.93rem;color:var(--ink);font-weight:500;line-height:1.4}
.event-desc{font-size:0.9rem;color:var(--ink-mid);line-height:1.75;margin-bottom:1rem}
.event-help-btn{display:inline-flex;align-items:center;gap:0.5rem;font-size:0.82rem;font-weight:500;color:var(--sage);background:var(--sage-light);border:1px solid var(--sage-mid);border-radius:20px;padding:6px 15px;cursor:pointer;font-family:'DM Sans',sans-serif;transition:background 0.2s}
.event-help-btn:hover{background:var(--sage-mid)}

/* ── FOOTER ───────────────────────────────────── */
footer{background:var(--ink);padding:3rem 2rem;text-align:center}
.footer-title{font-family:'DM Serif Display',serif;font-size:1.35rem;color:var(--white);margin-bottom:0.4rem}
.footer-sub{font-size:0.8rem;color:var(--ink-light);margin-bottom:1.4rem}
.footer-refs{display:flex;flex-direction:column;gap:0.35rem;align-items:center}
.footer-ref{font-size:0.73rem;color:var(--ink-light)}

/* ── FADE IN ──────────────────────────────────── */
.fade-in{opacity:0;transform:translateY(20px);transition:opacity 0.6s ease,transform 0.6s ease}
.fade-in.visible{opacity:1;transform:none}
.fade-in:nth-child(2){transition-delay:0.1s}
.fade-in:nth-child(3){transition-delay:0.2s}
.fade-in:nth-child(4){transition-delay:0.3s}

/* ── HELP MODAL ───────────────────────────────── */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(26,26,24,0.55);z-index:500;align-items:center;justify-content:center}
.modal-overlay.open{display:flex}
.modal-box{background:var(--cream);border-radius:22px;padding:2.5rem 2rem;max-width:380px;width:90%;text-align:center;box-shadow:0 24px 60px rgba(0,0,0,0.18)}
.modal-icon{font-size:2.6rem;margin-bottom:0.8rem}
.modal-title{font-family:'DM Serif Display',serif;font-size:1.6rem;color:var(--ink);margin-bottom:0.6rem}
.modal-body{font-size:0.92rem;color:var(--ink-mid);line-height:1.75;margin-bottom:1rem}
.modal-phone{font-family:'DM Serif Display',serif;font-size:1.8rem;color:var(--sage);margin-bottom:1.5rem}
.modal-close{background:var(--sage);color:white;border:none;border-radius:10px;padding:12px 32px;font-size:1rem;font-family:'DM Sans',sans-serif;cursor:pointer;font-weight:500;transition:background 0.2s}
.modal-close:hover{background:#3d6b4a}

@media(max-width:640px){
  .lang-sidebar{display:none}
  .main-content{margin-left:0}
  .hero-layout,.problem-layout,.space-layout{grid-template-columns:1fr;gap:2rem}
  .solution-cards,.cat-grid,.subcat-grid{grid-template-columns:1fr}
  nav .nav-links{display:none}
}
</style>
</head>
<body>
<div class="page-shell">

<!-- ── SIDEBAR ──────────────────────────────────────────────────── -->
<aside class="lang-sidebar">
  <div class="sidebar-logo">Bridge Housing</div>
  <div class="sidebar-logo-sub">CALD Community</div>
  <div class="lang-sidebar-label">🌐 Select language</div>
  <button class="lang-btn active" onclick="setLang('en',this)">
    <span class="lang-flag">🇦🇺</span>
    <span class="lang-name-wrap"><span class="lang-name">English</span><span class="lang-sub-name">English</span></span>
  </button>
  <button class="lang-btn" onclick="setLang('zh',this)">
    <span class="lang-flag">🇨🇳</span>
    <span class="lang-name-wrap"><span class="lang-name">中文</span><span class="lang-sub-name">Chinese</span></span>
  </button>
  <button class="lang-btn" onclick="setLang('ja',this)">
    <span class="lang-flag">🇯🇵</span>
    <span class="lang-name-wrap"><span class="lang-name">日本語</span><span class="lang-sub-name">Japanese</span></span>
  </button>
  <button class="lang-btn" onclick="setLang('ko',this)">
    <span class="lang-flag">🇰🇷</span>
    <span class="lang-name-wrap"><span class="lang-name">한국어</span><span class="lang-sub-name">Korean</span></span>
  </button>
  <button class="lang-btn" onclick="setLang('vi',this)">
    <span class="lang-flag">🇻🇳</span>
    <span class="lang-name-wrap"><span class="lang-name">Tiếng Việt</span><span class="lang-sub-name">Vietnamese</span></span>
  </button>
  <button class="lang-btn" onclick="setLang('ar',this)">
    <span class="lang-flag">🇱🇧</span>
    <span class="lang-name-wrap"><span class="lang-name">العربية</span><span class="lang-sub-name">Arabic</span></span>
  </button>
  <div class="sidebar-divider"></div>
  <div class="sidebar-nav-label">Navigation</div>
  <nav class="sidebar-nav">
    <a href="#home" data-t="nav_home">Home</a>
    <a href="#events-hub" data-t="nav_events">Events</a>
    <a href="#help-section" data-t="nav_help">Help</a>
    <a href="#contact-section" data-t="nav_contact">Contact</a>
  </nav>
  <div class="sidebar-help">
    <button class="help-btn-side" onclick="openHelp()">
      <span class="help-q">?</span>
      <span data-t="help_label">Need help?</span>
    </button>
  </div>
</aside>

<!-- ── MAIN ──────────────────────────────────────────────────────── -->
<div class="main-content">

<nav>
  <ul class="nav-links">
    <li><a href="#home" data-t="nav_home">Home</a></li>
    <li><a href="#events-hub" data-t="nav_events">Events</a></li>
    <li><a href="#help-section" data-t="nav_help">Help</a></li>
    <li><a href="#contact-section" data-t="nav_contact">Contact</a></li>
  </ul>
</nav>

<!-- HOME -->
<section id="home">
  <div class="container">
    <div class="hero-layout">
      <div>
        <div class="hero-eyebrow" data-t="hero_eyebrow">Bridge Housing — CALD Community</div>
        <h1 class="hero-title">
          <span data-t="hero_t1">Welcome to</span> <em data-t="hero_t2">Bridge Housing</em> <span data-t="hero_t3">Community</span>
        </h1>
        <p class="hero-body" data-t="hero_body">Find community events, get help, and connect with your neighbours — in your own language.</p>
        <div style="display:flex;gap:1rem;flex-wrap:wrap;margin-top:1.5rem;">
          <a href="#events-hub" style="background:var(--sage);color:white;padding:14px 28px;border-radius:12px;text-decoration:none;font-size:1.1rem;font-weight:500;" data-t="btn_events">🗓 Events</a>
          <a href="#help-section" style="background:var(--warm-dark);color:var(--ink);padding:14px 28px;border-radius:12px;text-decoration:none;font-size:1.1rem;font-weight:500;" data-t="btn_help">🏠 Housing Information</a>
          <a href="#contact-section" style="background:var(--warm-dark);color:var(--ink);padding:14px 28px;border-radius:12px;text-decoration:none;font-size:1.1rem;font-weight:500;" data-t="btn_contact">📞 Contact / Help</a>
        </div>
      </div>
      <div class="hero-image-wrap fade-in">
        <img src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=800&q=80" alt="Diverse elderly community gathering">
        <div class="hero-image-caption"><span data-t="hero_cap">Diverse residents building connections together</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ── EVENTS HUB ──────────────────────────────────────────────── -->
<section id="events-hub">
  <div class="container">
    <div class="section-label" data-t="events_label">Community Events</div>
    <h2 class="section-title" data-t="events_title">Find an event for you</h2>
    <p class="section-body" data-t="events_sub">Choose a type of activity to discover what's happening near you.</p>

    <!-- LEVEL 1: 6 main categories -->
    <div class="cat-grid" id="cat-grid">
      <div class="cat-card" onclick="showEvents(this,'language')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1516321497487-e288fb19713f?w=600&q=80" alt="Language activities">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_lang">Language Activities</div>
          <div class="cat-eng">语言活动 · Hoạt động ngôn ngữ</div>
        </div>
      </div>
      <div class="cat-card" onclick="showEvents(this,'hobby')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=600&q=80" alt="Hobbies">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_hobby">Hobbies &amp; Arts</div>
          <div class="cat-eng">兴趣爱好 · Sở thích</div>
        </div>
      </div>
      <div class="cat-card" onclick="showEvents(this,'cultural')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1533174072545-7a4b6ad7a6c3?w=600&q=80" alt="Cultural events">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_cultural">Cultural &amp; Religious</div>
          <div class="cat-eng">文化宗教 · Văn hóa tôn giáo</div>
        </div>
      </div>
      <div class="cat-card" onclick="showEvents(this,'community')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=600&q=80" alt="Community events">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_community">Community Events</div>
          <div class="cat-eng">社区活动 · Sự kiện cộng đồng</div>
        </div>
      </div>
      <div class="cat-card" onclick="showEvents(this,'volunteer')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1593113598332-cd288d649433?w=600&q=80" alt="Volunteering">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_volunteer">Volunteering</div>
          <div class="cat-eng">志愿服务 · Tình nguyện</div>
        </div>
      </div>
      <div class="cat-card" onclick="showEvents(this,'education')">
        <img class="cat-photo" src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173?w=600&q=80" alt="Education">
        <div class="cat-body">
          <div class="cat-title" data-t="cat_education">Education &amp; Skills</div>
          <div class="cat-eng">学习技能 · Giáo dục kỹ năng</div>
        </div>
      </div>
    </div>

    <!-- LEVEL 2: Event cards (shown directly after clicking a category) -->
    <div class="events-list-wrap" id="events-list-wrap">
      <button class="level-back" onclick="goBack()">← <span data-t="back_main">Back to all categories</span></button>
      <div class="events-list-title" id="events-list-title"></div>
      <div id="events-cards-container"></div>
    </div>

  </div>
</section>

<!-- HELP SECTION -->
<section id="help-section" style="background:var(--cream);">
  <div class="container">
    <div class="section-label" data-t="help_sec_label">Help</div>
    <h2 class="section-title" data-t="help_sec_title">We are here to help you</h2>
    <p class="section-body" data-t="help_sec_body">If you have any questions or need support, our staff are here for you — in your own language.</p>
    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.2rem;margin-top:1rem;">
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:2rem;margin-bottom:0.75rem;">📞</div>
        <div style="font-family:'DM Serif Display',serif;font-size:1.1rem;color:var(--ink);margin-bottom:0.4rem;" data-t="help_call_title">Call us</div>
        <div style="font-size:0.9rem;color:var(--ink-mid);margin-bottom:0.75rem;" data-t="help_call_body">Mon–Fri, 9:00 AM – 5:00 PM</div>
        <div style="font-size:1.3rem;font-weight:600;color:var(--sage);">(02) 9281 4000</div>
      </div>
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:2rem;margin-bottom:0.75rem;">🌐</div>
        <div style="font-family:'DM Serif Display',serif;font-size:1.1rem;color:var(--ink);margin-bottom:0.4rem;" data-t="help_lang_title">Language support</div>
        <div style="font-size:0.9rem;color:var(--ink-mid);" data-t="help_lang_body">We have staff who speak Mandarin, Cantonese, Vietnamese, Korean and more. Just ask.</div>
      </div>
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:2rem;margin-bottom:0.75rem;">🏠</div>
        <div style="font-family:'DM Serif Display',serif;font-size:1.1rem;color:var(--ink);margin-bottom:0.4rem;" data-t="help_visit_title">Visit us in person</div>
        <div style="font-size:0.9rem;color:var(--ink-mid);" data-t="help_visit_body">Our office is open and welcoming. Come in any time during business hours.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT SECTION -->
<section id="contact-section" style="background:var(--warm);">
  <div class="container">
    <div class="section-label" data-t="contact_label">Contact</div>
    <h2 class="section-title" data-t="contact_title">Get in touch</h2>
    <p class="section-body" data-t="contact_body">Reach out to us any time. We will get back to you as soon as possible.</p>
    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1rem;margin-top:1rem;">
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:1.5rem;margin-bottom:0.5rem;">📧</div>
        <div style="font-size:0.85rem;font-weight:500;color:var(--ink-light);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3rem;" data-t="contact_email_label">Email</div>
        <div style="font-size:0.95rem;color:var(--sage);font-weight:500;">info@bridgehousing.org.au</div>
      </div>
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:1.5rem;margin-bottom:0.5rem;">📞</div>
        <div style="font-size:0.85rem;font-weight:500;color:var(--ink-light);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3rem;" data-t="contact_phone_label">Phone</div>
        <div style="font-size:0.95rem;color:var(--sage);font-weight:500;">(02) 9281 4000</div>
      </div>
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:1.5rem;margin-bottom:0.5rem;">📍</div>
        <div style="font-size:0.85rem;font-weight:500;color:var(--ink-light);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3rem;" data-t="contact_addr_label">Address</div>
        <div style="font-size:0.95rem;color:var(--ink-mid);">Level 1, 2 O'Connell Street, Sydney NSW 2000</div>
      </div>
      <div style="background:white;border-radius:16px;padding:1.5rem;border:1px solid var(--warm-dark);">
        <div style="font-size:1.5rem;margin-bottom:0.5rem;">🕐</div>
        <div style="font-size:0.85rem;font-weight:500;color:var(--ink-light);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.3rem;" data-t="contact_hours_label">Office Hours</div>
        <div style="font-size:0.95rem;color:var(--ink-mid);" data-t="contact_hours_val">Monday – Friday, 9:00 AM – 5:00 PM</div>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="footer-title" data-t="ref_title">Bridge Housing</div>
  <div class="footer-sub" data-t="ref_sub">Community Events & Support</div>
  <div class="footer-refs">
    <div class="footer-ref">© 2025 Bridge Housing. All rights reserved.</div>
    <div class="footer-ref">Level 1, 2 O'Connell Street, Sydney NSW 2000 · (02) 9281 4000</div>
    <div class="footer-ref" style="margin-top:1rem;color:rgba(255,255,255,0.4);font-size:0.68rem;">References</div>
    <div class="footer-ref">Kane, L. (2019). Usability for older adults: Challenges and changes. Nielsen Norman Group. https://www.nngroup.com/articles/usability-for-senior-citizens/</div>
    <div class="footer-ref">Pak, R., Price, M. M., & Thatcher, J. (2009). Age-sensitive design of online health information: Comparative usability study. Journal of Medical Internet Research. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2802567/</div>
  </div>
</footer>

</div><!-- end .main-content -->
</div><!-- end .page-shell -->

<!-- HELP MODAL -->
<div class="modal-overlay" id="help-modal" onclick="if(event.target===this)closeHelp()">
  <div class="modal-box">
    <div class="modal-icon">📞</div>
    <div class="modal-title" data-t="modal_title">Need help?</div>
    <div class="modal-body" data-t="modal_body">Our staff are here for you. Please call us and we will be happy to assist.</div>
    <div class="modal-phone">(02) 9281 4000</div>
    <button class="modal-close" onclick="closeHelp()" data-t="modal_close">Close</button>
  </div>
</div>

<script>
// ── TRANSLATIONS ─────────────────────────────────────────────────────────────
const T = {
  en:{
    nav_home:"Home",nav_events:"Events",nav_help:"Housing Information",nav_contact:"Contact / Help",
    help_label:"Need help?",
    hero_eyebrow:"Bridge Housing — CALD Community",
    hero_t1:"Welcome to",hero_t2:"Bridge Housing",hero_t3:"Community",
    hero_body:"Find community events, get help, and connect with your neighbours — in your own language.",
    hero_cap:"Diverse residents building connections together",
    btn_events:"🗓 Events",btn_help:"🏠 Housing Information",btn_contact:"📞 Contact / Help",
    events_label:"Community Events",events_title:"Find an event for you",
    events_sub:"Choose a type of activity to discover what's happening near you.",
    cat_lang:"Language Activities",cat_hobby:"Hobbies & Arts",
    cat_cultural:"Cultural & Religious",cat_community:"Community Events",
    cat_volunteer:"Volunteering",cat_education:"Education & Skills",
    back_main:"Back to all categories",back_sub:"Back",
    help_sec_label:"Help",help_sec_title:"We are here to help you",
    help_sec_body:"If you have any questions or need support, our staff are here for you — in your own language.",
    help_call_title:"Call us",help_call_body:"Mon–Fri, 9:00 AM – 5:00 PM",
    help_lang_title:"Language support",help_lang_body:"We have staff who speak Mandarin, Cantonese, Vietnamese, Korean and more. Just ask.",
    help_visit_title:"Visit us in person",help_visit_body:"Our office is open and welcoming. Come in any time during business hours.",
    contact_label:"Contact",contact_title:"Get in touch",
    contact_body:"Reach out to us any time. We will get back to you as soon as possible.",
    contact_email_label:"Email",contact_phone_label:"Phone",
    contact_addr_label:"Address",contact_hours_label:"Office Hours",
    contact_hours_val:"Monday – Friday, 9:00 AM – 5:00 PM",
    modal_title:"Need help?",modal_body:"Our staff are here for you. Please call us and we will be happy to assist.",
    modal_close:"Close",
    ref_title:"Bridge Housing",ref_sub:"Community Events & Support"
  },
  zh:{
    nav_home:"首页",nav_events:"活动",nav_help:"帮助",nav_contact:"联系我们",
    help_label:"需要帮助？",
    hero_eyebrow:"Bridge Housing — CALD社区",
    hero_t1:"欢迎来到",hero_t2:"Bridge Housing",hero_t3:"社区",
    hero_body:"用您自己的语言，查找社区活动、获取帮助、与邻居建立联系。",
    hero_cap:"不同背景的居民共同建立联结",
    btn_events:"🗓 活动",btn_help:"❓ 帮助",btn_contact:"📞 联系我们",
    events_label:"社区活动",events_title:"寻找适合您的活动",
    events_sub:"请点击下方类别，查看附近的活动详情。",
    cat_lang:"语言活动",cat_hobby:"兴趣爱好",
    cat_cultural:"文化与宗教",cat_community:"社区活动",
    cat_volunteer:"志愿服务",cat_education:"学习与技能",
    back_main:"返回所有分类",back_sub:"返回",
    help_sec_label:"帮助",help_sec_title:"我们随时为您提供帮助",
    help_sec_body:"如果您有任何问题或需要支持，我们的工作人员随时为您服务——用您自己的语言。",
    help_call_title:"致电我们",help_call_body:"周一至周五，上午9:00 – 下午5:00",
    help_lang_title:"语言支持",help_lang_body:"我们有会说普通话、粤语、越南语、韩语等的工作人员，随时可以询问。",
    help_visit_title:"亲自来访",help_visit_body:"我们的办公室随时欢迎您，请在工作时间内前来。",
    contact_label:"联系我们",contact_title:"与我们取得联系",
    contact_body:"随时联系我们，我们会尽快回复您。",
    contact_email_label:"电子邮件",contact_phone_label:"电话",
    contact_addr_label:"地址",contact_hours_label:"办公时间",
    contact_hours_val:"周一至周五，上午9:00 – 下午5:00",
    modal_title:"需要帮助吗？",modal_body:"我们的工作人员随时为您服务，请致电我们，我们很乐意为您提供帮助。",
    modal_close:"关闭",
    ref_title:"Bridge Housing",ref_sub:"社区活动与支持"
  },
  vi:{
    nav_home:"Trang chủ",nav_events:"Sự kiện",nav_help:"Trợ giúp",nav_contact:"Liên hệ",
    help_label:"Cần giúp đỡ?",
    hero_eyebrow:"Bridge Housing — Cộng đồng CALD",
    hero_t1:"Chào mừng đến",hero_t2:"Bridge Housing",hero_t3:"Cộng đồng",
    hero_body:"Tìm sự kiện cộng đồng, nhận hỗ trợ và kết nối với hàng xóm — bằng ngôn ngữ của bạn.",
    hero_cap:"Cư dân đa dạng cùng nhau xây dựng mối liên kết",
    btn_events:"🗓 Sự kiện",btn_help:"❓ Trợ giúp",btn_contact:"📞 Liên hệ",
    events_label:"Sự kiện cộng đồng",events_title:"Tìm sự kiện cho bạn",
    events_sub:"Chọn loại hoạt động để khám phá những gì đang diễn ra gần bạn.",
    cat_lang:"Hoạt động ngôn ngữ",cat_hobby:"Sở thích & Nghệ thuật",
    cat_cultural:"Văn hóa & Tôn giáo",cat_community:"Sự kiện cộng đồng",
    cat_volunteer:"Tình nguyện",cat_education:"Giáo dục & Kỹ năng",
    back_main:"Quay lại tất cả danh mục",back_sub:"Quay lại",
    help_sec_label:"Trợ giúp",help_sec_title:"Chúng tôi ở đây để giúp bạn",
    help_sec_body:"Nếu bạn có câu hỏi hoặc cần hỗ trợ, nhân viên của chúng tôi luôn sẵn sàng — bằng ngôn ngữ của bạn.",
    help_call_title:"Gọi cho chúng tôi",help_call_body:"Thứ Hai – Thứ Sáu, 9:00 SA – 5:00 CH",
    help_lang_title:"Hỗ trợ ngôn ngữ",help_lang_body:"Chúng tôi có nhân viên nói tiếng Quan Thoại, Quảng Đông, Việt, Hàn và nhiều ngôn ngữ khác.",
    help_visit_title:"Đến thăm chúng tôi",help_visit_body:"Văn phòng của chúng tôi luôn mở cửa chào đón bạn trong giờ làm việc.",
    contact_label:"Liên hệ",contact_title:"Liên lạc với chúng tôi",
    contact_body:"Liên hệ với chúng tôi bất cứ lúc nào. Chúng tôi sẽ phản hồi sớm nhất có thể.",
    contact_email_label:"Email",contact_phone_label:"Điện thoại",
    contact_addr_label:"Địa chỉ",contact_hours_label:"Giờ làm việc",
    contact_hours_val:"Thứ Hai – Thứ Sáu, 9:00 SA – 5:00 CH",
    modal_title:"Cần giúp đỡ?",modal_body:"Nhân viên của chúng tôi luôn sẵn sàng. Vui lòng gọi cho chúng tôi.",
    modal_close:"Đóng",
    ref_title:"Bridge Housing",ref_sub:"Sự kiện cộng đồng & Hỗ trợ"
  },
  ar:{
    nav_home:"الرئيسية",nav_events:"الفعاليات",nav_help:"المساعدة",nav_contact:"اتصل بنا",
    help_label:"تحتاج مساعدة؟",
    hero_eyebrow:"Bridge Housing — مجتمع CALD",
    hero_t1:"مرحباً بك في",hero_t2:"Bridge Housing",hero_t3:"المجتمع",
    hero_body:"ابحث عن الفعاليات المجتمعية واحصل على المساعدة وتواصل مع جيرانك — بلغتك الخاصة.",
    hero_cap:"سكان متنوعون يبنون روابط معاً",
    btn_events:"🗓 الفعاليات",btn_help:"❓ مساعدة",btn_contact:"📞 اتصل بنا",
    events_label:"الفعاليات المجتمعية",events_title:"ابحث عن نشاط لك",
    events_sub:"اختر نوع النشاط لاكتشاف ما يحدث بالقرب منك.",
    cat_lang:"الأنشطة اللغوية",cat_hobby:"الهوايات والفنون",
    cat_cultural:"الثقافة والدين",cat_community:"الفعاليات المجتمعية",
    cat_volunteer:"التطوع",cat_education:"التعليم والمهارات",
    back_main:"العودة إلى جميع الفئات",back_sub:"رجوع",
    help_sec_label:"المساعدة",help_sec_title:"نحن هنا لمساعدتك",
    help_sec_body:"إذا كان لديك أي أسئلة أو تحتاج إلى دعم، فإن موظفينا في خدمتك — بلغتك الخاصة.",
    help_call_title:"اتصل بنا",help_call_body:"الاثنين–الجمعة، 9:00 ص – 5:00 م",
    help_lang_title:"دعم اللغة",help_lang_body:"لدينا موظفون يتحدثون الماندرين والكانتونية والفيتنامية والكورية والمزيد.",
    help_visit_title:"زرنا شخصياً",help_visit_body:"مكتبنا مفتوح ومرحب بك في أي وقت خلال ساعات العمل.",
    contact_label:"اتصل بنا",contact_title:"تواصل معنا",
    contact_body:"تواصل معنا في أي وقت وسنرد عليك في أقرب وقت ممكن.",
    contact_email_label:"البريد الإلكتروني",contact_phone_label:"الهاتف",
    contact_addr_label:"العنوان",contact_hours_label:"ساعات العمل",
    contact_hours_val:"الاثنين – الجمعة، 9:00 ص – 5:00 م",
    modal_title:"هل تحتاج مساعدة؟",modal_body:"موظفونا في خدمتك. يرجى الاتصال بنا.",
    modal_close:"إغلاق",
    ref_title:"Bridge Housing",ref_sub:"الفعاليات المجتمعية والدعم"
  },
  ko:{
    nav_home:"홈",nav_events:"행사",nav_help:"도움",nav_contact:"연락처",
    help_label:"도움이 필요하세요?",
    hero_eyebrow:"Bridge Housing — CALD 커뮤니티",
    hero_t1:"Bridge Housing",hero_t2:"커뮤니티에",hero_t3:"오신 것을 환영합니다",
    hero_body:"여러분의 언어로 커뮤니티 행사를 찾고, 도움을 받고, 이웃과 연결하세요.",
    hero_cap:"다양한 배경의 주민들이 함께 유대를 형성합니다",
    btn_events:"🗓 행사",btn_help:"❓ 도움",btn_contact:"📞 연락처",
    events_label:"커뮤니티 행사",events_title:"나에게 맞는 행사 찾기",
    events_sub:"활동 유형을 선택하여 근처에서 무슨 일이 있는지 알아보세요.",
    cat_lang:"언어 활동",cat_hobby:"취미 & 예술",
    cat_cultural:"문화 & 종교",cat_community:"커뮤니티 행사",
    cat_volunteer:"자원봉사",cat_education:"교육 & 기술",
    back_main:"모든 카테고리로 돌아가기",back_sub:"뒤로",
    help_sec_label:"도움",help_sec_title:"저희가 도와드리겠습니다",
    help_sec_body:"질문이 있거나 지원이 필요하시면, 저희 직원이 여러분의 언어로 도와드립니다.",
    help_call_title:"전화하기",help_call_body:"월–금, 오전 9:00 – 오후 5:00",
    help_lang_title:"언어 지원",help_lang_body:"저희는 만다린, 광둥어, 베트남어, 한국어 등을 구사하는 직원이 있습니다.",
    help_visit_title:"직접 방문",help_visit_body:"저희 사무실은 업무 시간 내 언제든지 방문 환영합니다.",
    contact_label:"연락처",contact_title:"문의하기",
    contact_body:"언제든지 연락해 주세요. 최대한 빨리 답변드리겠습니다.",
    contact_email_label:"이메일",contact_phone_label:"전화",
    contact_addr_label:"주소",contact_hours_label:"운영 시간",
    contact_hours_val:"월요일 – 금요일, 오전 9:00 – 오후 5:00",
    modal_title:"도움이 필요하세요?",modal_body:"직원이 언제든지 도와드립니다. 전화해 주세요.",
    modal_close:"닫기",
    ref_title:"Bridge Housing",ref_sub:"커뮤니티 행사 & 지원"
  },
  ja:{
    nav_home:"ホーム",nav_events:"イベント",nav_help:"ヘルプ",nav_contact:"お問い合わせ",
    help_label:"お困りですか？",
    hero_eyebrow:"Bridge Housing — CALDコミュニティ",
    hero_t1:"Bridge Housingへ",hero_t2:"ようこそ",hero_t3:"コミュニティ",
    hero_body:"あなたの言語で、コミュニティイベントを見つけ、サポートを受け、ご近所さんとつながりましょう。",
    hero_cap:"多様な住民が共につながりを築いています",
    btn_events:"🗓 イベント",btn_help:"❓ ヘルプ",btn_contact:"📞 お問い合わせ",
    events_label:"コミュニティイベント",events_title:"あなたに合ったイベントを探す",
    events_sub:"活動の種類を選んで、近くで開催されているイベントを見つけましょう。",
    cat_lang:"言語活動",cat_hobby:"趣味＆アート",
    cat_cultural:"文化＆宗教",cat_community:"コミュニティイベント",
    cat_volunteer:"ボランティア",cat_education:"教育＆スキル",
    back_main:"すべてのカテゴリに戻る",back_sub:"戻る",
    help_sec_label:"ヘルプ",help_sec_title:"いつでもお手伝いします",
    help_sec_body:"ご質問やサポートが必要な場合は、あなたの言語でお手伝いできるスタッフがいます。",
    help_call_title:"お電話",help_call_body:"月〜金、9:00〜17:00",
    help_lang_title:"言語サポート",help_lang_body:"中国語（普通話・広東語）、ベトナム語、韓国語などを話すスタッフがいます。",
    help_visit_title:"直接ご来訪",help_visit_body:"営業時間内はいつでもお気軽にお越しください。",
    contact_label:"お問い合わせ",contact_title:"ご連絡ください",
    contact_body:"いつでもご連絡ください。できる限り早くお返事いたします。",
    contact_email_label:"メール",contact_phone_label:"電話",
    contact_addr_label:"住所",contact_hours_label:"営業時間",
    contact_hours_val:"月曜日〜金曜日、9:00〜17:00",
    modal_title:"お困りですか？",modal_body:"スタッフがいつでもお手伝いします。お電話ください。",
    modal_close:"閉じる",
    ref_title:"Bridge Housing",ref_sub:"コミュニティイベント＆サポート"
  }
};

function setLang(lang, btn) {
  const t = T[lang];
  if (!t) return;
  currentLang = lang;
  document.querySelectorAll('[data-t]').forEach(el => {
    const k = el.getAttribute('data-t');
    if (t[k] !== undefined) el.textContent = t[k];
  });
  document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.documentElement.lang = lang;
  if (currentCat && document.getElementById('events-list-wrap').classList.contains('visible')) {
    renderCards();
  }
}

// ── EVENT DATA (2-level) ─────────────────────────────────────────────────────
const EVENTS = {
  language: [
    {icon:'🗣️',photo:'https://images.unsplash.com/photo-1516321497487-e288fb19713f?w=600&q=80',s:'regular',
     en:{n:'Mandarin Conversation Group',b:'Weekly · Wed 10:00 AM',l:'Surry Hills Community Centre',d:'Friendly chat in Mandarin with neighbours. All levels welcome. Tea provided.'},
     zh:{n:'普通话会话小组',b:'每周 · 周三上午10:00',l:'Surry Hills社区中心',d:'与邻居用普通话轻松聊天，欢迎各水平，提供茶水。'},
     vi:{n:'Nhóm hội thoại tiếng Phổ thông',b:'Hàng tuần · T4 10:00 SA',l:'TT Cộng đồng Surry Hills',d:'Trò chuyện thân thiện bằng tiếng Phổ thông. Mọi trình độ đều được chào đón.'},
     ko:{n:'만다린 회화 그룹',b:'매주 · 수요일 오전 10:00',l:'Surry Hills 커뮤니티 센터',d:'이웃과 만다린으로 편안하게 대화합니다. 모든 수준 환영.'},
     ar:{n:'مجموعة محادثة ماندرين',b:'أسبوعي · الأربعاء 10:00 ص',l:'مركز مجتمع Surry Hills',d:'محادثة ودية بالصينية مع الجيران. جميع المستويات مرحب بها.'},
     ja:{n:'中国語会話グループ',b:'毎週 · 水曜 10:00',l:'サリーヒルズ・コミュニティセンター',d:'ご近所の方と中国語でリラックスした会話を楽しみましょう。'}},
    {icon:'🇻🇳',photo:'https://images.unsplash.com/photo-1524069290683-0457abfe42c3?w=600&q=80',s:'regular',
     en:{n:'Vietnamese Conversation Circle',b:'Weekly · Mon 10:00 AM',l:'Cabramatta Community Hall',d:'Chat in Vietnamese with your community. Warm and welcoming for all ages.'},
     zh:{n:'越南语会话圈',b:'每周 · 周一上午10:00',l:'Cabramatta社区厅',d:'与社区邻居用越南语聊天，温馨友好，欢迎所有年龄段。'},
     vi:{n:'Vòng tròn hội thoại tiếng Việt',b:'Hàng tuần · T2 10:00 SA',l:'Hội trường Cộng đồng Cabramatta',d:'Trò chuyện bằng tiếng Việt với cộng đồng của bạn. Ấm áp và thân thiện.'},
     ko:{n:'베트남어 대화 모임',b:'매주 · 월요일 오전 10:00',l:'Cabramatta 커뮤니티 홀',d:'커뮤니티 사람들과 베트남어로 대화합니다.'},
     ar:{n:'مجموعة محادثة الفيتنامية',b:'أسبوعي · الاثنين 10:00 ص',l:'قاعة مجتمع Cabramatta',d:'تحدث بالفيتنامية مع مجتمعك. دافئ ومرحب لجميع الأعمار.'},
     ja:{n:'ベトナム語会話サークル',b:'毎週 · 月曜 10:00',l:'カブラマッタ・コミュニティホール',d:'コミュニティの方々とベトナム語で会話しましょう。'}},
    {icon:'🇦🇺',photo:'https://images.unsplash.com/photo-1434030216411-0b793f4b4173?w=600&q=80',s:'regular',
     en:{n:'English for Daily Life',b:'Weekly · Tue 10:00 AM',l:'Bridge Housing Office',d:'Learn useful English for shopping, doctors and everyday tasks. Patient, friendly support.'},
     zh:{n:'日常生活英语',b:'每周 · 周二上午10:00',l:'Bridge Housing办公室',d:'学习购物、看医生和日常事务中的实用英语，耐心友好的辅导。'},
     vi:{n:'Tiếng Anh cho cuộc sống hàng ngày',b:'Hàng tuần · T3 10:00 SA',l:'Văn phòng Bridge Housing',d:'Học tiếng Anh thực dụng cho mua sắm, đi khám bác sĩ và sinh hoạt hàng ngày.'},
     ko:{n:'일상생활 영어',b:'매주 · 화요일 오전 10:00',l:'Bridge Housing 사무실',d:'쇼핑, 병원, 일상 업무에 필요한 영어를 배웁니다.'},
     ar:{n:'الإنجليزية للحياة اليومية',b:'أسبوعي · الثلاثاء 10:00 ص',l:'مكتب Bridge Housing',d:'تعلم الإنجليزية المفيدة للتسوق والأطباء والمهام اليومية.'},
     ja:{n:'日常生活の英語',b:'毎週 · 火曜 10:00',l:'Bridge Housingオフィス',d:'買い物や病院など日常生活で使える英語を学びましょう。'}},
    {icon:'🇰🇷',photo:'https://images.unsplash.com/photo-1543269865-cbf427effbad?w=600&q=80',s:'regular',
     en:{n:'Korean Conversation Group',b:'Weekly · Thu 10:00 AM',l:'Strathfield Community Hall',d:'Chat in Korean with neighbours. Welcoming to all levels and ages.'},
     zh:{n:'韩语会话小组',b:'每周 · 周四上午10:00',l:'Strathfield社区厅',d:'与邻居用韩语聊天，欢迎所有水平和年龄段。'},
     vi:{n:'Nhóm hội thoại tiếng Hàn',b:'Hàng tuần · T5 10:00 SA',l:'Hội trường Cộng đồng Strathfield',d:'Trò chuyện bằng tiếng Hàn với hàng xóm.'},
     ko:{n:'한국어 회화 그룹',b:'매주 · 목요일 오전 10:00',l:'Strathfield 커뮤니티 홀',d:'이웃과 한국어로 대화합니다. 모든 수준과 연령 환영.'},
     ar:{n:'مجموعة محادثة الكورية',b:'أسبوعي · الخميس 10:00 ص',l:'قاعة مجتمع Strathfield',d:'تحدث بالكورية مع الجيران. مرحب بجميع المستويات.'},
     ja:{n:'韓国語会話グループ',b:'毎週 · 木曜 10:00',l:'ストラスフィールド・コミュニティホール',d:'ご近所の方と韓国語で会話しましょう。'}},
    {icon:'📖',photo:'https://images.unsplash.com/photo-1481627834876-b7833e8f5570?w=600&q=80',s:'regular',
     en:{n:'Multilingual Morning Tea',b:'Weekly · Fri 10:00 AM',l:'Surry Hills Community Centre',d:'Gather with neighbours who speak many languages. Chat, laugh and connect over tea.'},
     zh:{n:'多语言早茶',b:'每周 · 周五上午10:00',l:'Surry Hills社区中心',d:'与说各种语言的邻居聚在一起，喝茶聊天，轻松愉快。'},
     vi:{n:'Trà sáng đa ngôn ngữ',b:'Hàng tuần · T6 10:00 SA',l:'TT Cộng đồng Surry Hills',d:'Gặp gỡ hàng xóm nói nhiều ngôn ngữ. Trò chuyện và kết nối bên tách trà.'},
     ko:{n:'다국어 모닝 티',b:'매주 · 금요일 오전 10:00',l:'Surry Hills 커뮤니티 센터',d:'다양한 언어를 사용하는 이웃들과 차를 마시며 대화합니다.'},
     ar:{n:'شاي الصباح متعدد اللغات',b:'أسبوعي · الجمعة 10:00 ص',l:'مركز مجتمع Surry Hills',d:'التقِ بالجيران الناطقين بلغات متعددة وتواصل على الشاي.'},
     ja:{n:'多言語モーニングティー',b:'毎週 · 金曜 10:00',l:'サリーヒルズ・コミュニティセンター',d:'様々な言語を話すご近所さんとお茶を楽しみながら交流しましょう。'}},
    {icon:'✍️',photo:'https://images.unsplash.com/photo-1513364776144-60967b0f800f?w=600&q=80',s:'cancelled',
     en:{n:'Chinese Calligraphy Class',b:'Monthly · 1st Tue 10:30 AM',l:'Redfern Community Hall',d:'Learn the beautiful art of Chinese calligraphy in a relaxed and welcoming setting.'},
     zh:{n:'中国书法课',b:'每月 · 第一个周二上午10:30',l:'Redfern社区厅',d:'在轻松愉快的环境中学习美丽的中国书法艺术。'},
     vi:{n:'Lớp thư pháp Trung Hoa',b:'Hàng tháng · T3 đầu tháng 10:30 SA',l:'Hội trường Cộng đồng Redfern',d:'Học nghệ thuật thư pháp Trung Hoa trong môi trường thoải mái và thân thiện.'},
     ko:{n:'중국 서예 수업',b:'매월 · 첫째 화요일 오전 10:30',l:'Redfern 커뮤니티 홀',d:'편안하고 환영하는 분위기에서 중국 서예 예술을 배웁니다.'},
     ar:{n:'درس الخط الصيني',b:'شهري · أول ثلاثاء 10:30 ص',l:'قاعة مجتمع Redfern',d:'تعلم فن الخط الصيني الجميل في بيئة مريحة ومرحبة.'},
     ja:{n:'中国書法教室',b:'毎月 · 第1火曜 10:30',l:'レッドファーン・コミュニティホール',d:'リラックスした雰囲気で中国書法の美しい芸術を学びましょう。'}}
  ],
  hobby: [
    {icon:'💃',photo:'https://images.unsplash.com/photo-1524594152303-9fd13543fe6e?w=600&q=80',s:'regular',
     en:{n:'Gentle Line Dancing',b:'Weekly · Mon 10:30 AM',l:'Waterloo Community Centre',d:'Easy line dancing for all fitness levels. Fun, social and great gentle exercise!'},
     zh:{n:'轻柔排舞',b:'每周 · 周一上午10:30',l:'Waterloo社区中心',d:'适合所有体能水平的简单排舞，有趣、社交性强，是很好的轻度运动！'},
     vi:{n:'Khiêu vũ dây nhẹ nhàng',b:'Hàng tuần · T2 10:30 SA',l:'TT Cộng đồng Waterloo',d:'Khiêu vũ dây dễ dàng cho mọi thể lực. Vui vẻ, giao lưu và tập thể dục nhẹ nhàng!'},
     ko:{n:'부드러운 라인 댄스',b:'매주 · 월요일 오전 10:30',l:'Waterloo 커뮤니티 센터',d:'모든 체력 수준에 맞는 쉬운 라인 댄스. 즐겁고 사교적인 운동!'},
     ar:{n:'الرقص الخطي اللطيف',b:'أسبوعي · الاثنين 10:30 ص',l:'مركز مجتمع Waterloo',d:'رقص خطي سهل لجميع مستويات اللياقة. ممتع ورياضة خفيفة رائعة!'},
     ja:{n:'ゆったりラインダンス',b:'毎週 · 月曜 10:30',l:'ウォータールー・コミュニティセンター',d:'どんな体力レベルでも楽しめる簡単なラインダンス。楽しくて社交的！'}},
    {icon:'🪴',photo:'https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=600&q=80',s:'regular',
     en:{n:'Community Garden Morning',b:'Weekly · Sat 9:00 AM',l:'Surry Hills Community Garden',d:'Plant, weed and water together. Take home produce you have grown yourself!'},
     zh:{n:'社区花园早晨',b:'每周 · 周六上午9:00',l:'Surry Hills社区花园',d:'一起种植、除草和浇水，带回自己种的农产品！'},
     vi:{n:'Buổi sáng vườn cộng đồng',b:'Hàng tuần · T7 9:00 SA',l:'Vườn Cộng đồng Surry Hills',d:'Cùng nhau trồng, nhổ cỏ và tưới nước. Mang về sản phẩm bạn tự trồng!'},
     ko:{n:'커뮤니티 정원 아침',b:'매주 · 토요일 오전 9:00',l:'Surry Hills 커뮤니티 정원',d:'함께 심고, 잡초를 뽑고, 물을 줍니다. 직접 키운 채소를 집에 가져가세요!'},
     ar:{n:'صباح الحديقة المجتمعية',b:'أسبوعي · السبت 9:00 ص',l:'حديقة مجتمع Surry Hills',d:'ازرع واحصد معاً. خذ إلى المنزل منتجات زرعتها بنفسك!'},
     ja:{n:'コミュニティガーデンの朝',b:'毎週 · 土曜 9:00',l:'サリーヒルズ・コミュニティガーデン',d:'一緒に植えて、草取りして、水やりしましょう。自分で育てた野菜を持ち帰れます！'}},
    {icon:'🎨',photo:'https://images.unsplash.com/photo-1513364776144-60967b0f800f?w=600&q=80',s:'regular',
     en:{n:'Watercolour Painting Group',b:'Weekly · Tue 10:00 AM',l:'Surry Hills Community Centre',d:'Paint in a friendly group. All supplies provided — no experience needed at all.'},
     zh:{n:'水彩画小组',b:'每周 · 周二上午10:00',l:'Surry Hills社区中心',d:'在友好小组中画水彩画，提供所有材料，完全不需要经验。'},
     vi:{n:'Nhóm vẽ màu nước',b:'Hàng tuần · T3 10:00 SA',l:'TT Cộng đồng Surry Hills',d:'Vẽ trong nhóm thân thiện. Cung cấp đầy đủ dụng cụ — không cần kinh nghiệm.'},
     ko:{n:'수채화 그룹',b:'매주 · 화요일 오전 10:00',l:'Surry Hills 커뮤니티 센터',d:'친근한 그룹에서 그림을 그립니다. 모든 용품 제공 — 경험 불필요.'},
     ar:{n:'مجموعة رسم الألوان المائية',b:'أسبوعي · الثلاثاء 10:00 ص',l:'مركز مجتمع Surry Hills',d:'ارسم في مجموعة ودية. جميع الأدوات مُقدَّمة — لا خبرة مطلوبة.'},
     ja:{n:'水彩画グループ',b:'毎週 · 火曜 10:00',l:'サリーヒルズ・コミュニティセンター',d:'和やかなグループで水彩画を楽しみましょう。材料はすべて提供 — 経験不要。'}},
    {icon:'✂️',photo:'https://images.unsplash.com/photo-1452860606245-08befc0ff44b?w=600&q=80',s:'regular',
     en:{n:'Knitting & Craft Circle',b:'Weekly · Wed 10:00 AM',l:'Surry Hills Community Centre',d:'Knit, crochet or do crafts together. Bring your own project or learn something new.'},
     zh:{n:'编织与手工圈',b:'每周 · 周三上午10:00',l:'Surry Hills社区中心',d:'一起编织、钩针或做手工，可带自己的项目，也可以学新东西。'},
     vi:{n:'Vòng tròn đan len & thủ công',b:'Hàng tuần · T4 10:00 SA',l:'TT Cộng đồng Surry Hills',d:'Cùng đan, móc hoặc làm thủ công. Mang dự án của bạn hoặc học điều mới.'},
     ko:{n:'뜨개질 & 공예 모임',b:'매주 · 수요일 오전 10:00',l:'Surry Hills 커뮤니티 센터',d:'함께 뜨개질, 코바늘 또는 공예를 합니다.'},
     ar:{n:'دائرة الحياكة والحرف اليدوية',b:'أسبوعي · الأربعاء 10:00 ص',l:'مركز مجتمع Surry Hills',d:'انسج أو اعمل حرفاً يدوية معاً. احضر مشروعك أو تعلم شيئاً جديداً.'},
     ja:{n:'編み物と手芸サークル',b:'毎週 · 水曜 10:00',l:'サリーヒルズ・コミュニティセンター',d:'一緒に編み物やクロッシェ、手芸を楽しみましょう。'}},
    {icon:'🎵',photo:'https://images.unsplash.com/photo-1507838153414-b4b713384a76?w=600&q=80',s:'regular',
     en:{n:'Community Singing Group',b:'Weekly · Thu 11:00 AM',l:'Waterloo Community Centre',d:'Sing songs from many cultures together. No experience needed — just enthusiasm!'},
     zh:{n:'社区歌唱小组',b:'每周 · 周四上午11:00',l:'Waterloo社区中心',d:'一起唱来自各种文化的歌曲，不需要任何经验，只需要热情！'},
     vi:{n:'Nhóm hát cộng đồng',b:'Hàng tuần · T5 11:00 SA',l:'TT Cộng đồng Waterloo',d:'Cùng hát những bài từ nhiều nền văn hóa. Không cần kinh nghiệm — chỉ cần nhiệt tình!'},
     ko:{n:'커뮤니티 노래 그룹',b:'매주 · 목요일 오전 11:00',l:'Waterloo 커뮤니티 센터',d:'다양한 문화의 노래를 함께 부릅니다. 경험 불필요 — 열정만 있으면 됩니다!'},
     ar:{n:'مجموعة الغناء المجتمعية',b:'أسبوعي · الخميس 11:00 ص',l:'مركز مجتمع Waterloo',d:'غنِّ أغاني من ثقافات متعددة معاً. لا خبرة مطلوبة — فقط الحماس!'},
     ja:{n:'コミュニティ合唱グループ',b:'毎週 · 木曜 11:00',l:'ウォータールー・コミュニティセンター',d:'様々な文化の歌を一緒に歌いましょう。経験不要！'}},
    {icon:'🍳',photo:'https://images.unsplash.com/photo-1476224203421-9ac39bcb3327?w=600&q=80',s:'cancelled',
     en:{n:'Multicultural Cook-Together',b:'Monthly · 2nd Sat 11:00 AM',l:'Zetland Kitchen Space',d:'Everyone brings and teaches a dish from their home country. Eat together after!'},
     zh:{n:'多元文化共同烹饪',b:'每月 · 第二个周六上午11:00',l:'Zetland厨房空间',d:'每人带来并教做一道家乡菜，然后一起共进午餐！'},
     vi:{n:'Cùng nấu ăn đa văn hóa',b:'Hàng tháng · T7 tuần 2, 11:00 SA',l:'Không gian bếp Zetland',d:'Mỗi người mang và dạy một món ăn từ quê hương. Cùng ăn sau đó!'},
     ko:{n:'다문화 요리 모임',b:'매월 · 둘째 토요일 오전 11:00',l:'Zetland 주방 공간',d:'각자 고향 음식을 가져와서 가르쳐 줍니다. 함께 식사합니다!'},
     ar:{n:'الطبخ المشترك متعدد الثقافات',b:'شهري · السبت الثاني 11:00 ص',l:'مطبخ Zetland',d:'يُحضر الجميع طبقاً من بلدهم ويعلمونه للآخرين. نأكل معاً بعد ذلك!'},
     ja:{n:'多文化料理シェアリング',b:'毎月 · 第2土曜 11:00',l:'ゼットランド・キッチンスペース',d:'それぞれが故郷の料理を持ち寄って教え合います。一緒に食べましょう！'}}
  ],
  cultural: [
    {icon:'🏮',photo:'https://images.unsplash.com/photo-1533174072545-7a4b6ad7a6c3?w=600&q=80',s:'regular',
     en:{n:'Lunar New Year Celebration',b:'Annual · Late Jan / Feb',l:'Chinatown Cultural Centre',d:'Celebrate the Lunar New Year with food, lion dancing and community. Everyone welcome!'},
     zh:{n:'农历新年庆典',b:'每年 · 1月底/2月',l:'唐人街文化中心',d:'与大家一起欢庆农历新年，有美食、舞狮和社区活动，欢迎所有人！'},
     vi:{n:'Lễ Tết Nguyên Đán',b:'Hàng năm · Cuối tháng 1 / 2',l:'Trung tâm Văn hóa Phố Tàu',d:'Cùng đón Tết Nguyên Đán với ẩm thực, múa lân và cộng đồng.'},
     ko:{n:'설날 축하 행사',b:'매년 · 1월 말 / 2월',l:'차이나타운 문화 센터',d:'음식, 사자춤과 함께 설날을 축하합니다. 모든 분 환영!'},
     ar:{n:'احتفال رأس السنة القمرية',b:'سنوي · أواخر يناير / فبراير',l:'المركز الثقافي للحي الصيني',d:'احتفل برأس السنة القمرية بالطعام والرقصات والمجتمع. الجميع مرحب به!'},
     ja:{n:'旧正月のお祝い',b:'毎年 · 1月末〜2月',l:'チャイナタウン文化センター',d:'料理や獅子舞と共に旧正月をお祝いしましょう。どなたでも歓迎！'}},
    {icon:'🕌',photo:'https://images.unsplash.com/photo-1545378406-c84d9f5e5d47?w=600&q=80',s:'regular',
     en:{n:'Eid Community Feast',b:'Annual · Date varies',l:'Lakemba Community Hall',d:'Celebrate Eid with neighbours. Halal food, warm atmosphere, all are welcome.'},
     zh:{n:'开斋节社区聚餐',b:'每年 · 日期待定',l:'Lakemba社区厅',d:'与邻居一起庆祝开斋节，有清真食品，气氛温馨，欢迎所有人。'},
     vi:{n:'Lễ Eid cộng đồng',b:'Hàng năm · Ngày sẽ thông báo',l:'Hội trường Cộng đồng Lakemba',d:'Cùng hàng xóm kỷ niệm Eid. Thức ăn Halal, không khí ấm áp.'},
     ko:{n:'이드 커뮤니티 축제',b:'매년 · 날짜 변동',l:'Lakemba 커뮤니티 홀',d:'이웃과 함께 이드를 축하합니다. 할랄 음식, 따뜻한 분위기, 모든 분 환영.'},
     ar:{n:'مأدبة العيد المجتمعية',b:'سنوي · تاريخ يتغير',l:'قاعة مجتمع Lakemba',d:'احتفل بالعيد مع الجيران. طعام حلال، أجواء دافئة، الجميع مرحب به.'},
     ja:{n:'イード・コミュニティ・フィースト',b:'毎年 · 日程は変動',l:'レイクンバ・コミュニティホール',d:'ご近所さんと一緒にイードをお祝いしましょう。ハラール料理あり。'}},
    {icon:'🎎',photo:'https://images.unsplash.com/photo-1528360983277-13d401cdc186?w=600&q=80',s:'regular',
     en:{n:'Japanese Culture Day',b:'Monthly · 2nd Sun 2:00 PM',l:'Glebe Community Centre',d:'Origami, tea ceremony and Japanese cultural sharing. A calm and beautiful afternoon.'},
     zh:{n:'日本文化日',b:'每月 · 第二个周日下午2:00',l:'Glebe社区中心',d:'折纸、茶道和日本文化分享，宁静而美好的下午。'},
     vi:{n:'Ngày văn hóa Nhật Bản',b:'Hàng tháng · CN tuần 2, 2:00 CH',l:'TT Cộng đồng Glebe',d:'Origami, trà đạo và chia sẻ văn hóa Nhật Bản. Một buổi chiều bình yên và đẹp đẽ.'},
     ko:{n:'일본 문화의 날',b:'매월 · 둘째 일요일 오후 2:00',l:'Glebe 커뮤니티 센터',d:'종이접기, 다도, 일본 문화 나눔. 조용하고 아름다운 오후.'},
     ar:{n:'يوم الثقافة اليابانية',b:'شهري · الأحد الثاني 2:00 م',l:'مركز مجتمع Glebe',d:'الأوريغامي وحفلة الشاي ومشاركة الثقافة اليابانية. بعد ظهر هادئ وجميل.'},
     ja:{n:'日本文化の日',b:'毎月 · 第2日曜 14:00',l:'グリーブ・コミュニティセンター',d:'折り紙、茶道、日本文化の紹介。穏やかで美しい午後を過ごしましょう。'}},
    {icon:'🪔',photo:'https://images.unsplash.com/photo-1574169208507-84376144848b?w=600&q=80',s:'regular',
     en:{n:'Diwali Festival of Lights',b:'Annual · Oct / Nov',l:'Parramatta Community Hall',d:'Celebrate Diwali with lamps, sweets, rangoli art and the Indian community.'},
     zh:{n:'排灯节',b:'每年 · 10月/11月',l:'Parramatta社区厅',d:'用油灯、甜品、彩绘艺术与印度社区一起庆祝排灯节。'},
     vi:{n:'Lễ hội ánh sáng Diwali',b:'Hàng năm · Tháng 10 / 11',l:'Hội trường Cộng đồng Parramatta',d:'Cùng cộng đồng Ấn Độ kỷ niệm Diwali với đèn, bánh ngọt và nghệ thuật rangoli.'},
     ko:{n:'디왈리 빛의 축제',b:'매년 · 10월 / 11월',l:'Parramatta 커뮤니티 홀',d:'등불, 과자, 란골리 예술로 인도 커뮤니티와 함께 디왈리를 축하합니다.'},
     ar:{n:'مهرجان الأنوار ديوالي',b:'سنوي · أكتوبر / نوفمبر',l:'قاعة مجتمع Parramatta',d:'احتفل بديوالي مع المصابيح والحلويات وفن الرانغولي والمجتمع الهندي.'},
     ja:{n:'ディワリ 光の祭典',b:'毎年 · 10月〜11月',l:'パラマタ・コミュニティホール',d:'ランプ、お菓子、ランゴリーアートとともにディワリをお祝いしましょう。'}},
    {icon:'🌍',photo:'https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=600&q=80',s:'regular',
     en:{n:'World Food Sharing Day',b:'Monthly · Last Sun 12:00 PM',l:'Bridge Housing Common Room',d:'Everyone brings a dish from their home country. A feast of flavours and friendship!'},
     zh:{n:'世界美食分享日',b:'每月 · 最后一个周日中午12:00',l:'Bridge Housing公共室',d:'每人带一道家乡菜来分享，美食与友谊的盛宴！'},
     vi:{n:'Ngày chia sẻ ẩm thực thế giới',b:'Hàng tháng · CN cuối tháng 12:00 CH',l:'Phòng chung Bridge Housing',d:'Mỗi người mang một món ăn từ quê hương. Một bữa tiệc hương vị và tình bạn!'},
     ko:{n:'세계 음식 나눔의 날',b:'매월 · 마지막 일요일 정오',l:'Bridge Housing 공용 공간',d:'각자 고향 음식을 가져옵니다. 다양한 맛과 우정의 잔치!'},
     ar:{n:'يوم مشاركة طعام العالم',b:'شهري · آخر أحد 12:00 م',l:'غرفة مشتركة Bridge Housing',d:'يُحضر الجميع طبقاً من بلدهم. وليمة من النكهات والصداقة!'},
     ja:{n:'世界の料理シェアリングデー',b:'毎月 · 最終日曜 12:00',l:'Bridge Housing共用ルーム',d:'みんなが故郷の料理を持ち寄ります。味と友情の饗宴！'}},
    {icon:'⛪',photo:'https://images.unsplash.com/photo-1542884748-2b87b36c6b90?w=600&q=80',s:'cancelled',
     en:{n:'Christmas Community Lunch',b:'Annual · December',l:'Bridge Housing Common Room',d:'A free Christmas lunch for all residents. Carols, gifts and warm community spirit.'},
     zh:{n:'圣诞社区午餐',b:'每年 · 12月',l:'Bridge Housing公共室',d:'为所有居民提供的免费圣诞午餐，有圣诞颂歌、礼物和温暖的社区氛围。'},
     vi:{n:'Bữa trưa Giáng sinh cộng đồng',b:'Hàng năm · Tháng 12',l:'Phòng chung Bridge Housing',d:'Bữa trưa Giáng sinh miễn phí cho tất cả cư dân. Thánh ca, quà và không khí ấm áp.'},
     ko:{n:'크리스마스 커뮤니티 점심',b:'매년 · 12월',l:'Bridge Housing 공용 공간',d:'모든 주민을 위한 무료 크리스마스 점심. 캐럴, 선물, 따뜻한 커뮤니티 정신.'},
     ar:{n:'غداء عيد الميلاد المجتمعي',b:'سنوي · ديسمبر',l:'غرفة مشتركة Bridge Housing',d:'غداء مجاني لعيد الميلاد لجميع السكان. ترانيم وهدايا وروح مجتمعية دافئة.'},
     ja:{n:'クリスマス・コミュニティランチ',b:'毎年 · 12月',l:'Bridge Housing共用ルーム',d:'全住民無料のクリスマスランチ。キャロル、プレゼント、温かなコミュニティの雰囲気。'}}
  ],
  community: [
    {icon:'☕',photo:'https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=600&q=80',s:'regular',
     en:{n:'Friday Morning Tea',b:'Weekly · Fri 10:00 AM',l:'Bridge Housing Common Room',d:'Relax over tea and biscuits with neighbours. No agenda — just warmth and friendship.'},
     zh:{n:'周五早茶',b:'每周 · 周五上午10:00',l:'Bridge Housing公共室',d:'与邻居一起喝茶吃饼干，无需任何安排，只有温馨和友谊。'},
     vi:{n:'Trà sáng thứ Sáu',b:'Hàng tuần · T6 10:00 SA',l:'Phòng chung Bridge Housing',d:'Thư giãn bên tách trà và bánh với hàng xóm. Không có lịch trình — chỉ là sự ấm áp.'},
     ko:{n:'금요일 모닝 티',b:'매주 · 금요일 오전 10:00',l:'Bridge Housing 공용 공간',d:'이웃과 차와 비스킷을 즐기며 쉽니다. 특별한 일정 없이 — 그냥 따뜻한 우정.'},
     ar:{n:'شاي صباح الجمعة',b:'أسبوعي · الجمعة 10:00 ص',l:'غرفة مشتركة Bridge Housing',d:'استرخِ مع الشاي والبسكويت مع الجيران. لا جدول أعمال — فقط الدفء والصداقة.'},
     ja:{n:'金曜モーニングティー',b:'毎週 · 金曜 10:00',l:'Bridge Housing共用ルーム',d:'ご近所さんとお茶とビスケットでリラックス。議題なし — ただ温もりと友情を。'}},
    {icon:'🚶',photo:'https://images.unsplash.com/photo-1504051771394-dd2e66b2b975?w=600&q=80',s:'regular',
     en:{n:'Gentle Morning Walk',b:'Weekly · Tue 8:30 AM',l:'Centennial Park Gate 1',d:'A gentle 30-minute walk together. Slow pace, beautiful scenery, great company.'},
     zh:{n:'轻柔晨走',b:'每周 · 周二上午8:30',l:'Centennial公园1号门',d:'一起轻柔散步30分钟，节奏缓慢，风景优美，同伴友好。'},
     vi:{n:'Đi bộ buổi sáng nhẹ nhàng',b:'Hàng tuần · T3 8:30 SA',l:'Cổng 1 Công viên Centennial',d:'Đi bộ nhẹ nhàng 30 phút cùng nhau. Tốc độ chậm, cảnh đẹp, bạn đồng hành tốt.'},
     ko:{n:'부드러운 아침 산책',b:'매주 · 화요일 오전 8:30',l:'Centennial Park 1번 입구',d:'함께 30분 부드럽게 걷습니다. 느린 속도, 아름다운 풍경, 좋은 친구들.'},
     ar:{n:'مشي الصباح اللطيف',b:'أسبوعي · الثلاثاء 8:30 ص',l:'بوابة 1 حديقة Centennial',d:'مشية لطيفة مدة 30 دقيقة معاً. وتيرة بطيئة، مناظر جميلة، رفقة رائعة.'},
     ja:{n:'ゆったり朝のお散歩',b:'毎週 · 火曜 8:30',l:'センテニアルパーク 第1ゲート',d:'一緒にゆっくり30分散歩。ゆっくりペースで美しい景色と良い仲間と。'}},
    {icon:'🎲',photo:'https://images.unsplash.com/photo-1528819622765-d6bcf132f793?w=600&q=80',s:'regular',
     en:{n:'Mahjong & Card Games',b:'Weekly · Tue & Fri 2:00 PM',l:'Surry Hills Community Centre',d:'Play mahjong or card games with friendly neighbours. Beginners always welcome!'},
     zh:{n:'麻将与纸牌游戏',b:'每周 · 周二和周五下午2:00',l:'Surry Hills社区中心',d:'与友好的邻居一起打麻将或玩纸牌，欢迎初学者！'},
     vi:{n:'Mạt chược & trò chơi bài',b:'Hàng tuần · T3 & T6 2:00 CH',l:'TT Cộng đồng Surry Hills',d:'Chơi mạt chược hoặc bài với hàng xóm thân thiện. Người mới bắt đầu luôn được chào đón!'},
     ko:{n:'마작 & 카드 게임',b:'매주 · 화·금요일 오후 2:00',l:'Surry Hills 커뮤니티 센터',d:'친근한 이웃과 마작이나 카드 게임을 즐깁니다. 초보자 항상 환영!'},
     ar:{n:'الماجونغ وألعاب الورق',b:'أسبوعي · الثلاثاء والجمعة 2:00 م',l:'مركز مجتمع Surry Hills',d:'العب الماجونغ أو ألعاب الورق مع الجيران الودودين. المبتدئون مرحب بهم دائماً!'},
     ja:{n:'麻雀とカードゲーム',b:'毎週 · 火・金曜 14:00',l:'サリーヒルズ・コミュニティセンター',d:'ご近所さんと麻雀やカードゲームを楽しみましょう。初心者大歓迎！'}},
    {icon:'🎬',photo:'https://images.unsplash.com/photo-1489599849927-2ee91cede3ba?w=600&q=80',s:'regular',
     en:{n:'Movie Afternoon',b:'Weekly · Fri 2:00 PM',l:'Bridge Housing Common Room',d:'Watch a movie together with subtitles. Tea and popcorn provided. All languages and genres.'},
     zh:{n:'电影下午',b:'每周 · 周五下午2:00',l:'Bridge Housing公共室',d:'一起看有字幕的电影，提供茶水和爆米花，涵盖各种语言和类型。'},
     vi:{n:'Chiều xem phim',b:'Hàng tuần · T6 2:00 CH',l:'Phòng chung Bridge Housing',d:'Cùng xem phim có phụ đề. Có trà và bắp rang. Mọi ngôn ngữ và thể loại.'},
     ko:{n:'영화 오후',b:'매주 · 금요일 오후 2:00',l:'Bridge Housing 공용 공간',d:'자막이 있는 영화를 함께 봅니다. 차와 팝콘 제공. 모든 언어와 장르.'},
     ar:{n:'بعد ظهر السينما',b:'أسبوعي · الجمعة 2:00 م',l:'غرفة مشتركة Bridge Housing',d:'شاهد فيلماً معاً بترجمة. يُقدَّم الشاي والفشار. جميع اللغات والأنواع.'},
     ja:{n:'映画の午後',b:'毎週 · 金曜 14:00',l:'Bridge Housing共用ルーム',d:'字幕付きで一緒に映画を観ましょう。お茶とポップコーンあり。'}},
    {icon:'📖',photo:'https://images.unsplash.com/photo-1481627834876-b7833e8f5570?w=600&q=80',s:'regular',
     en:{n:'Book & Story Sharing',b:'Fortnightly · Mon 2:00 PM',l:'Glebe Library',d:'Share a favourite book or short story from your culture. All languages welcome.'},
     zh:{n:'书籍与故事分享',b:'每两周 · 周一下午2:00',l:'Glebe图书馆',d:'分享你文化中最喜欢的书或短篇故事，欢迎所有语言。'},
     vi:{n:'Chia sẻ sách & câu chuyện',b:'2 tuần/lần · T2 2:00 CH',l:'Thư viện Glebe',d:'Chia sẻ cuốn sách yêu thích hoặc câu chuyện ngắn từ văn hóa của bạn. Mọi ngôn ngữ đều được chào đón.'},
     ko:{n:'책 & 이야기 나눔',b:'격주 · 월요일 오후 2:00',l:'Glebe 도서관',d:'내 문화에서 좋아하는 책이나 단편 이야기를 나눕니다. 모든 언어 환영.'},
     ar:{n:'مشاركة الكتب والقصص',b:'كل أسبوعين · الاثنين 2:00 م',l:'مكتبة Glebe',d:'شارك كتابك المفضل أو قصة قصيرة من ثقافتك. جميع اللغات مرحب بها.'},
     ja:{n:'本と物語のシェアリング',b:'隔週 · 月曜 14:00',l:'グリーブ図書館',d:'あなたの文化のお気に入りの本や短編を紹介しましょう。全言語歓迎。'}},
    {icon:'🌿',photo:'https://images.unsplash.com/photo-1523712999610-f77fbcfc3843?w=600&q=80',s:'cancelled',
     en:{n:'Botanic Garden Stroll',b:'Monthly · 2nd Wed 10:00 AM',l:'Royal Botanic Garden main gate',d:'Walk through the gardens and enjoy seasonal flowers. Free entry, gentle pace.'},
     zh:{n:'植物园漫步',b:'每月 · 第二个周三上午10:00',l:'皇家植物园正门',d:'在植物园中漫步，欣赏应季花朵，免费入园，节奏悠闲。'},
     vi:{n:'Tản bộ trong vườn thực vật',b:'Hàng tháng · T4 tuần 2, 10:00 SA',l:'Cổng chính Vườn Thực vật Hoàng gia',d:'Đi dạo trong vườn và thưởng thức hoa theo mùa. Vào cửa miễn phí, tốc độ nhẹ nhàng.'},
     ko:{n:'식물원 산책',b:'매월 · 둘째 수요일 오전 10:00',l:'왕립 식물원 정문',d:'정원을 걸으며 계절 꽃을 즐깁니다. 무료 입장, 느긋한 속도.'},
     ar:{n:'التجول في الحديقة النباتية',b:'شهري · الأربعاء الثاني 10:00 ص',l:'البوابة الرئيسية للحديقة النباتية الملكية',d:'تجوّل في الحدائق واستمتع بزهور الموسم. دخول مجاني، وتيرة هادئة.'},
     ja:{n:'植物園の散歩',b:'毎月 · 第2水曜 10:00',l:'王立植物園・正門',d:'庭園を散歩して季節の花を楽しみましょう。無料入園、ゆっくりペース。'}}
  ],
  volunteer: [
    {icon:'🛒',photo:'https://images.unsplash.com/photo-1607082348824-0a96f2a4b9da?w=600&q=80',s:'regular',
     en:{n:'Shopping Companion',b:'Weekly · Tue 10:00 AM',l:'Meet at Bridge Housing entrance',d:'A volunteer walks with you to the local supermarket and shops. Builds confidence.'},
     zh:{n:'购物陪伴',b:'每周 · 周二上午10:00',l:'Bridge Housing门口集合',d:'志愿者陪同您去当地超市购物，帮助建立自信。'},
     vi:{n:'Bạn đồng hành mua sắm',b:'Hàng tuần · T3 10:00 SA',l:'Gặp tại cửa Bridge Housing',d:'Một tình nguyện viên đi cùng bạn đến siêu thị và cửa hàng địa phương.'},
     ko:{n:'쇼핑 동반자',b:'매주 · 화요일 오전 10:00',l:'Bridge Housing 입구에서 만남',d:'자원봉사자가 현지 슈퍼마켓까지 함께 걸어갑니다. 자신감을 키웁니다.'},
     ar:{n:'رفيق التسوق',b:'أسبوعي · الثلاثاء 10:00 ص',l:'الالتقاء عند مدخل Bridge Housing',d:'يرافقك متطوع إلى المتجر المحلي للتسوق. يبني الثقة بالنفس.'},
     ja:{n:'買い物サポート',b:'毎週 · 火曜 10:00',l:'Bridge Housing入口で待ち合わせ',d:'ボランティアが近くのスーパーまで一緒に歩いてくれます。'}},
    {icon:'📞',photo:'https://images.unsplash.com/photo-1516387938699-a93567ec168e?w=600&q=80',s:'regular',
     en:{n:'Weekly Phone Friend',b:'Weekly · Flexible time',l:'From your home',d:'A friendly volunteer calls you once a week for a chat. Available in your language.'},
     zh:{n:'每周电话朋友',b:'每周 · 时间灵活',l:'在您家中（电话）',d:'一位友善的志愿者每周给您打一次电话聊天，可用您的语言交流。'},
     vi:{n:'Bạn điện thoại hàng tuần',b:'Hàng tuần · Giờ linh hoạt',l:'Từ nhà bạn',d:'Một tình nguyện viên thân thiện gọi cho bạn mỗi tuần để trò chuyện. Có thể bằng ngôn ngữ của bạn.'},
     ko:{n:'주간 전화 친구',b:'매주 · 시간 유동적',l:'자택에서',d:'친근한 자원봉사자가 매주 한 번 전화해 이야기를 나눕니다. 귀하의 언어로 가능.'},
     ar:{n:'صديق الهاتف الأسبوعي',b:'أسبوعي · وقت مرن',l:'من منزلك',d:'يتصل بك متطوع ودي مرة في الأسبوع للدردشة. متاح بلغتك.'},
     ja:{n:'週1回の電話お友達',b:'毎週 · 時間は柔軟',l:'ご自宅から',d:'週1回、ボランティアが話し相手として電話してくれます。あなたの言語で対応可。'}},
    {icon:'🌻',photo:'https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=600&q=80',s:'regular',
     en:{n:'Garden Volunteer Morning',b:'Weekly · Sat 9:00 AM',l:'Surry Hills Community Garden',d:'Help plant, weed and water the shared garden. Meet your neighbours while volunteering.'},
     zh:{n:'花园志愿者早晨',b:'每周 · 周六上午9:00',l:'Surry Hills社区花园',d:'帮助在共用花园中种植、除草和浇水，边做志愿服务边认识邻居。'},
     vi:{n:'Buổi sáng tình nguyện vườn',b:'Hàng tuần · T7 9:00 SA',l:'Vườn Cộng đồng Surry Hills',d:'Giúp trồng, nhổ cỏ và tưới vườn chung. Gặp gỡ hàng xóm khi tình nguyện.'},
     ko:{n:'정원 자원봉사 아침',b:'매주 · 토요일 오전 9:00',l:'Surry Hills 커뮤니티 정원',d:'공유 정원의 심기, 잡초 뽑기, 물주기를 도웁니다. 봉사하며 이웃을 만납니다.'},
     ar:{n:'صباح المتطوعين في الحديقة',b:'أسبوعي · السبت 9:00 ص',l:'حديقة مجتمع Surry Hills',d:'ساعد في زراعة الحديقة المشتركة وإزالة الأعشاب وريّها.'},
     ja:{n:'ガーデンボランティアの朝',b:'毎週 · 土曜 9:00',l:'サリーヒルズ・コミュニティガーデン',d:'共用ガーデンの植え付け、草取り、水やりをお手伝い。'}},
    {icon:'🍱',photo:'https://images.unsplash.com/photo-1476224203421-9ac39bcb3327?w=600&q=80',s:'regular',
     en:{n:'Community Kitchen Volunteer',b:'Weekly · Mon & Thu 10:00 AM',l:'Redfern Community Kitchen',d:'Help cook hot meals for residents in need. Very rewarding and friendly team.'},
     zh:{n:'社区厨房志愿者',b:'每周 · 周一和周四上午10:00',l:'Redfern社区厨房',d:'帮助为有需要的居民烹制热饭菜，非常有意义，团队友好。'},
     vi:{n:'Tình nguyện bếp cộng đồng',b:'Hàng tuần · T2 & T5 10:00 SA',l:'Bếp Cộng đồng Redfern',d:'Giúp nấu bữa ăn nóng cho cư dân có nhu cầu. Rất có ý nghĩa và đội ngũ thân thiện.'},
     ko:{n:'커뮤니티 주방 자원봉사',b:'매주 · 월·목요일 오전 10:00',l:'Redfern 커뮤니티 주방',d:'도움이 필요한 주민을 위해 따뜻한 식사를 만드는 것을 돕습니다.'},
     ar:{n:'متطوع المطبخ المجتمعي',b:'أسبوعي · الاثنين والخميس 10:00 ص',l:'مطبخ مجتمع Redfern',d:'ساعد في طهي وجبات ساخنة للسكان المحتاجين. مجزٍ جداً وفريق ودي.'},
     ja:{n:'コミュニティキッチンボランティア',b:'毎週 · 月・木曜 10:00',l:'レッドファーン・コミュニティキッチン',d:'支援が必要な住民のために温かい食事を作るお手伝い。'}},
    {icon:'📱',photo:'https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?w=600&q=80',s:'regular',
     en:{n:'Tech Support Volunteer',b:'Weekly · Wed 10:00 AM',l:'Bridge Housing Office',d:'Help neighbours with smartphones, tablets and computers. Training provided.'},
     zh:{n:'科技支持志愿者',b:'每周 · 周三上午10:00',l:'Bridge Housing办公室',d:'帮助邻居使用智能手机、平板电脑和电脑，提供培训。'},
     vi:{n:'Tình nguyện hỗ trợ công nghệ',b:'Hàng tuần · T4 10:00 SA',l:'Văn phòng Bridge Housing',d:'Giúp hàng xóm với điện thoại thông minh, máy tính bảng và máy tính.'},
     ko:{n:'기술 지원 자원봉사',b:'매주 · 수요일 오전 10:00',l:'Bridge Housing 사무실',d:'이웃의 스마트폰, 태블릿, 컴퓨터 사용을 돕습니다. 교육 제공.'},
     ar:{n:'متطوع الدعم التقني',b:'أسبوعي · الأربعاء 10:00 ص',l:'مكتب Bridge Housing',d:'ساعد الجيران في استخدام الهواتف الذكية والأجهزة اللوحية والحواسيب.'},
     ja:{n:'テクノロジーサポートボランティア',b:'毎週 · 水曜 10:00',l:'Bridge Housingオフィス',d:'ご近所さんのスマートフォン、タブレット、パソコンのお手伝い。研修あり。'}},
    {icon:'👧',photo:'https://images.unsplash.com/photo-1481627834876-b7833e8f5570?w=600&q=80',s:'cancelled',
     en:{n:'Story Time Grandparent',b:'Weekly · Wed 10:30 AM',l:'Surry Hills Library',d:'Read to young children as a volunteer "story grandparent". Joyful and very rewarding.'},
     zh:{n:'"故事爷爷奶奶"读书',b:'每周 · 周三上午10:30',l:'Surry Hills图书馆',d:'作为志愿者"故事祖父母"给小朋友朗读故事，充满欢乐且非常有意义。'},
     vi:{n:'Ông bà kể chuyện tình nguyện',b:'Hàng tuần · T4 10:30 SA',l:'Thư viện Surry Hills',d:'Đọc sách cho trẻ nhỏ với tư cách "ông bà kể chuyện" tình nguyện.'},
     ko:{n:'이야기 시간 할머니·할아버지',b:'매주 · 수요일 오전 10:30',l:'Surry Hills 도서관',d:'자원봉사 "이야기 조부모"로 어린 아이들에게 책을 읽어줍니다.'},
     ar:{n:'متطوع وقت القصة للأطفال',b:'أسبوعي · الأربعاء 10:30 ص',l:'مكتبة Surry Hills',d:'اقرأ للأطفال الصغار كـ"جد أو جدة القصص" المتطوع. ممتع ومجزٍ جداً.'},
     ja:{n:'読み聞かせボランティア',b:'毎週 · 水曜 10:30',l:'サリーヒルズ図書館',d:'ボランティアの"おじいちゃん・おばあちゃん"として子どもたちに絵本を読んであげましょう。'}}
  ],
  education: [
    {icon:'📱',photo:'https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?w=600&q=80',s:'regular',
     en:{n:'Smartphone Basics',b:'Weekly · Mon 10:00 AM',l:'Bridge Housing Office',d:'Learn to make calls, send texts and use apps step by step. Patient one-on-one help.'},
     zh:{n:'手机基础课',b:'每周 · 周一上午10:00',l:'Bridge Housing办公室',d:'逐步学习打电话、发短信和使用应用程序，提供耐心的一对一辅助。'},
     vi:{n:'Cơ bản về điện thoại thông minh',b:'Hàng tuần · T2 10:00 SA',l:'Văn phòng Bridge Housing',d:'Học cách gọi điện, nhắn tin và dùng ứng dụng từng bước. Hỗ trợ 1-1 kiên nhẫn.'},
     ko:{n:'스마트폰 기초',b:'매주 · 월요일 오전 10:00',l:'Bridge Housing 사무실',d:'통화, 문자, 앱 사용을 단계별로 배웁니다. 인내심 있는 1:1 도움.'},
     ar:{n:'أساسيات الهاتف الذكي',b:'أسبوعي · الاثنين 10:00 ص',l:'مكتب Bridge Housing',d:'تعلم إجراء المكالمات وإرسال الرسائل واستخدام التطبيقات خطوة بخطوة.'},
     ja:{n:'スマートフォン入門',b:'毎週 · 月曜 10:00',l:'Bridge Housingオフィス',d:'電話、メッセージ、アプリの使い方をステップごとに学びます。丁寧な個別サポートあり。'}},
    {icon:'💻',photo:'https://images.unsplash.com/photo-1518770660439-4636190af475?w=600&q=80',s:'regular',
     en:{n:'Computer Basics',b:'Weekly · Tue 10:00 AM',l:'Glebe Library',d:'Learn to use a computer from scratch. Typing, browsing and email at your own pace.'},
     zh:{n:'电脑基础课',b:'每周 · 周二上午10:00',l:'Glebe图书馆',d:'从零开始学习使用电脑，按自己的节奏学习打字、浏览网页和发邮件。'},
     vi:{n:'Cơ bản về máy tính',b:'Hàng tuần · T3 10:00 SA',l:'Thư viện Glebe',d:'Học cách dùng máy tính từ đầu. Gõ phím, duyệt web và email theo tốc độ của bạn.'},
     ko:{n:'컴퓨터 기초',b:'매주 · 화요일 오전 10:00',l:'Glebe 도서관',d:'컴퓨터 사용을 처음부터 배웁니다. 타이핑, 인터넷, 이메일을 자신의 속도로.'},
     ar:{n:'أساسيات الحاسوب',b:'أسبوعي · الثلاثاء 10:00 ص',l:'مكتبة Glebe',d:'تعلم استخدام الحاسوب من الصفر. الكتابة والتصفح والبريد الإلكتروني بوتيرتك.'},
     ja:{n:'パソコン入門',b:'毎週 · 火曜 10:00',l:'グリーブ図書館',d:'ゼロからパソコンの使い方を学びます。タイピング、検索、メールを自分のペースで。'}},
    {icon:'💬',photo:'https://images.unsplash.com/photo-1434030216411-0b793f4b4173?w=600&q=80',s:'regular',
     en:{n:'English Conversation Class',b:'Weekly · Wed 9:30 AM',l:'Surry Hills Community Centre',d:'Practise everyday English in a warm, non-judgmental group. All levels very welcome.'},
     zh:{n:'英语会话课',b:'每周 · 周三上午9:30',l:'Surry Hills社区中心',d:'在温暖友好、无评判的小组中练习日常英语，欢迎所有水平。'},
     vi:{n:'Lớp hội thoại tiếng Anh',b:'Hàng tuần · T4 9:30 SA',l:'TT Cộng đồng Surry Hills',d:'Thực hành tiếng Anh hàng ngày trong nhóm ấm áp, không phán xét. Mọi trình độ đều được chào đón.'},
     ko:{n:'영어 회화 수업',b:'매주 · 수요일 오전 9:30',l:'Surry Hills 커뮤니티 센터',d:'따뜻하고 판단 없는 그룹에서 일상 영어를 연습합니다. 모든 수준 환영.'},
     ar:{n:'درس محادثة الإنجليزية',b:'أسبوعي · الأربعاء 9:30 ص',l:'مركز مجتمع Surry Hills',d:'تدرّب على الإنجليزية اليومية في مجموعة دافئة وغير حكمية. جميع المستويات مرحب بها.'},
     ja:{n:'英会話クラス',b:'毎週 · 水曜 9:30',l:'サリーヒルズ・コミュニティセンター',d:'温かく評価しないグループで日常英語を練習しましょう。全レベル大歓迎。'}},
    {icon:'💰',photo:'https://images.unsplash.com/photo-1554224155-8d04cb21cd6c?w=600&q=80',s:'regular',
     en:{n:'Understanding Your Bills',b:'Monthly · 1st Wed 10:00 AM',l:'Bridge Housing Office',d:'Learn to read electricity, water and phone bills. Know exactly what you are paying for.'},
     zh:{n:'读懂您的账单',b:'每月 · 第一个周三上午10:00',l:'Bridge Housing办公室',d:'学习如何阅读电费、水费和电话账单，清楚了解您每项费用的内容。'},
     vi:{n:'Hiểu hóa đơn của bạn',b:'Hàng tháng · T4 đầu tháng 10:00 SA',l:'Văn phòng Bridge Housing',d:'Học cách đọc hóa đơn điện, nước và điện thoại. Biết chính xác bạn đang trả tiền cho gì.'},
     ko:{n:'청구서 이해하기',b:'매월 · 첫째 수요일 오전 10:00',l:'Bridge Housing 사무실',d:'전기, 수도, 전화 요금 청구서 읽는 법을 배웁니다.'},
     ar:{n:'فهم فواتيرك',b:'شهري · أول أربعاء 10:00 ص',l:'مكتب Bridge Housing',d:'تعلم قراءة فواتير الكهرباء والماء والهاتف. اعرف بالضبط ما تدفعه.'},
     ja:{n:'請求書の読み方',b:'毎月 · 第1水曜 10:00',l:'Bridge Housingオフィス',d:'電気・水道・電話の請求書の読み方を学びます。'}},
    {icon:'🏥',photo:'https://images.unsplash.com/photo-1576091160550-2173dba999ef?w=600&q=80',s:'regular',
     en:{n:'Know Your Medicare',b:'Monthly · 1st Mon 10:00 AM',l:'Bridge Housing Office',d:'Understand your Medicare card and how to use it. Access free or low-cost health care.'},
     zh:{n:'了解您的医疗保险',b:'每月 · 第一个周一上午10:00',l:'Bridge Housing办公室',d:'了解您的医疗保险卡及其使用方法，获得免费或低价的医疗服务。'},
     vi:{n:'Hiểu thẻ Medicare của bạn',b:'Hàng tháng · T2 đầu tháng 10:00 SA',l:'Văn phòng Bridge Housing',d:'Hiểu thẻ Medicare của bạn và cách sử dụng. Tiếp cận chăm sóc sức khỏe miễn phí hoặc chi phí thấp.'},
     ko:{n:'메디케어 이해하기',b:'매월 · 첫째 월요일 오전 10:00',l:'Bridge Housing 사무실',d:'메디케어 카드와 사용법을 이해합니다. 무료 또는 저비용 의료 서비스 이용.'},
     ar:{n:'اعرف تأمينك الصحي',b:'شهري · أول اثنين 10:00 ص',l:'مكتب Bridge Housing',d:'افهم بطاقة ميديكير الخاصة بك وكيفية استخدامها.'},
     ja:{n:'メディケアを理解しよう',b:'毎月 · 第1月曜 10:00',l:'Bridge Housingオフィス',d:'メディケアカードの使い方を学びましょう。無料または低コストの医療を受けられます。'}},
    {icon:'🗺️',photo:'https://images.unsplash.com/photo-1509099381441-ea3c0cf98b94?w=600&q=80',s:'cancelled',
     en:{n:'Public Transport Help',b:'Monthly · 2nd Fri 10:00 AM',l:'Bridge Housing entrance',d:'Learn to use Opal cards, buses, trains and ferries with a volunteer guide by your side.'},
     zh:{n:'公共交通使用指导',b:'每月 · 第二个周五上午10:00',l:'Bridge Housing门口',d:'学习如何使用Opal卡、公共汽车、火车和渡轮，有志愿者在旁指导。'},
     vi:{n:'Hướng dẫn phương tiện công cộng',b:'Hàng tháng · T6 tuần 2, 10:00 SA',l:'Cửa Bridge Housing',d:'Học cách dùng thẻ Opal, xe buýt, tàu hỏa và phà với hướng dẫn viên tình nguyện bên cạnh.'},
     ko:{n:'대중교통 이용 도움',b:'매월 · 둘째 금요일 오전 10:00',l:'Bridge Housing 입구',d:'자원봉사 가이드와 함께 오팔 카드, 버스, 기차, 페리 이용법을 배웁니다.'},
     ar:{n:'مساعدة في المواصلات العامة',b:'شهري · الجمعة الثانية 10:00 ص',l:'مدخل Bridge Housing',d:'تعلم استخدام بطاقة Opal والحافلات والقطارات والعبّارات مع مرشد متطوع.'},
     ja:{n:'公共交通機関サポート',b:'毎月 · 第2金曜 10:00',l:'Bridge Housing入口',d:'ボランティアガイドと一緒にオパールカード、バス、電車、フェリーの使い方を学びます。'}}
  ]
};

// ── UI STRINGS ────────────────────────────────────────────────────────────────
const UI = {
  en: {lbl_time:'Day & Time', lbl_loc:'Location', help:'? Need help?', cancelled:'⚠ Cancelled this week', back:'← Back to categories'},
  zh: {lbl_time:'时间',         lbl_loc:'地点',      help:'? 需要帮助？',  cancelled:'⚠ 本周取消',            back:'← 返回分类'},
  vi: {lbl_time:'Thời gian',   lbl_loc:'Địa điểm', help:'? Cần giúp?',  cancelled:'⚠ Tuần này bị hủy',     back:'← Quay lại'},
  ko: {lbl_time:'날짜 및 시간', lbl_loc:'장소',      help:'? 도움 필요?', cancelled:'⚠ 이번 주 취소',         back:'← 뒤로'},
  ar: {lbl_time:'الوقت',       lbl_loc:'المكان',    help:'? مساعدة؟',    cancelled:'⚠ ملغى هذا الأسبوع',    back:'← رجوع'},
  ja: {lbl_time:'日時',         lbl_loc:'場所',      help:'? お困りですか？',cancelled:'⚠ 今週は中止',        back:'← 戻る'}
};

// ── STATE & FUNCTIONS ────────────────────────────────────────────────────────
let currentCat = null;
let currentLang = 'en';

function showEvents(card, cat) {
  document.querySelectorAll('.cat-card').forEach(c => c.classList.remove('active'));
  card.classList.add('active');
  currentCat = cat;
  renderCards();
  const wrap = document.getElementById('events-list-wrap');
  wrap.classList.add('visible');
  setTimeout(() => wrap.scrollIntoView({behavior:'smooth', block:'start'}), 60);
}

function renderCards() {
  const ui = UI[currentLang] || UI.en;
  const events = EVENTS[currentCat] || [];
  const container = document.getElementById('events-cards-container');
  container.innerHTML = '';
  events.forEach(ev => {
    const tr = ev[currentLang] || ev.en;
    const cancelled = ev.s === 'cancelled';
    const div = document.createElement('div');
    div.className = 'event-card' + (cancelled ? ' cancelled' : '');
    div.innerHTML = `
      <div style="display:flex;align-items:flex-start;justify-content:space-between;gap:1rem;margin-bottom:0.9rem;flex-wrap:wrap">
        <div class="event-name">${ev.icon} ${tr.n}</div>
        <span class="event-badge ${cancelled ? 'badge-cancel' : 'badge-regular'}">${cancelled ? ui.cancelled : tr.b}</span>
      </div>
      <div class="event-meta">
        <div class="event-meta-item"><span class="meta-icon">📅</span><span class="meta-text"><span class="meta-lbl">${ui.lbl_time}</span><span class="meta-val">${tr.b}</span></span></div>
        <div class="event-meta-item"><span class="meta-icon">📍</span><span class="meta-text"><span class="meta-lbl">${ui.lbl_loc}</span><span class="meta-val">${tr.l}</span></span></div>
      </div>
      <p class="event-desc">${tr.d}</p>
      <button class="event-help-btn" onclick="openHelp()">${ui.help}</button>`;
    container.appendChild(div);
  });
  const backBtn = document.querySelector('#events-list-wrap .level-back');
  if (backBtn) backBtn.textContent = ui.back;
}

function goBack() {
  document.getElementById('events-list-wrap').classList.remove('visible');
  document.querySelectorAll('.cat-card').forEach(c => c.classList.remove('active'));
  document.getElementById('cat-grid').scrollIntoView({behavior:'smooth', block:'start'});
  currentCat = null;
}

function openHelp() { document.getElementById('help-modal').classList.add('open'); }
function closeHelp() { document.getElementById('help-modal').classList.remove('open'); }

// Fade-in observer
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, {threshold:0.1});
document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));
</script>
</body>
</html>
