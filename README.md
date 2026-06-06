# gravity-gym
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="GRAVITY Unisex Fitness - Ranchi's premier gym at Galaxia Mall, Piska More, Ratu Road. State-of-the-art equipment, certified trainers, CrossFit zone, affordable membership plans. Rated 4.9/5.">
  <meta name="keywords" content="gym in ranchi, best gym ranchi, fitness center ranchi, unisex gym ranchi, gravity gym, gym near ratu road, crossfit ranchi, galaxia mall gym">
  <title>GRAVITY — Unisex Fitness Ranchi | Defy Your Limits</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Oswald:wght@300;400;500;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    *,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
    :root{
      --accent:#FF4500;--gold:#D4A017;--bg:#080808;--card:#0f0f0f;
      --card2:#161616;--text:#f5f5f5;--muted:#666;--border:#1c1c1c;--nav-h:72px;
    }
    html{scroll-behavior:smooth}
    body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);overflow-x:hidden}
    ::-webkit-scrollbar{width:3px}
    ::-webkit-scrollbar-track{background:var(--bg)}
    ::-webkit-scrollbar-thumb{background:var(--accent)}

    /* ── NAV ── */
    nav{position:fixed;top:0;left:0;right:0;height:var(--nav-h);display:flex;align-items:center;
      justify-content:space-between;padding:0 5%;z-index:100;transition:background .3s,backdrop-filter .3s}
    nav.scrolled{background:rgba(8,8,8,.96);backdrop-filter:blur(14px);border-bottom:1px solid var(--border)}
    .nav-logo{font-family:'Bebas Neue',sans-serif;font-size:2rem;letter-spacing:.15em;color:var(--text);text-decoration:none}
    .nav-logo span{color:var(--accent)}
    .nav-links{display:flex;gap:2.2rem;list-style:none}
    .nav-links a{font-family:'Oswald',sans-serif;font-size:.78rem;font-weight:500;letter-spacing:.14em;
      text-transform:uppercase;color:var(--muted);text-decoration:none;transition:color .2s}
    .nav-links a:hover{color:var(--text)}
    .nav-cta{font-family:'Oswald',sans-serif;font-size:.78rem;font-weight:600;letter-spacing:.18em;
      text-transform:uppercase;color:var(--bg);background:var(--accent);padding:10px 26px;
      text-decoration:none;clip-path:polygon(8px 0%,100% 0%,calc(100% - 8px) 100%,0% 100%);transition:opacity .2s}
    .nav-cta:hover{opacity:.85}
    .mobile-menu-btn{display:none;background:none;border:none;color:var(--text);font-size:1.5rem;cursor:pointer}

    /* ── HERO ── */
    #hero{min-height:100vh;display:flex;align-items:flex-end;padding:0 5% 8%;position:relative;
      overflow:hidden;background:linear-gradient(140deg,#0a0a0a 0%,#1c0800 55%,#080808 100%)}
    .hero-ghost{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);
      font-family:'Bebas Neue',sans-serif;font-size:clamp(100px,22vw,340px);
      color:rgba(255,69,0,.038);letter-spacing:-.02em;white-space:nowrap;pointer-events:none;user-select:none}
    .hero-vline{position:absolute;top:0;right:18%;width:1px;height:100%;
      background:linear-gradient(to bottom,transparent,var(--accent) 40%,transparent);opacity:.25}
    .hero-dot{position:absolute;top:30%;right:calc(18% - 3px);width:7px;height:7px;
      background:var(--accent);border-radius:50%;box-shadow:0 0 20px var(--accent)}
    .hero-content{position:relative;z-index:2;max-width:960px}
    .hero-eyebrow{font-family:'Oswald',sans-serif;font-size:.72rem;font-weight:400;letter-spacing:.38em;
      text-transform:uppercase;color:var(--accent);margin-bottom:1.2rem;display:flex;align-items:center;gap:14px}
    .hero-eyebrow::before{content:'';display:block;width:44px;height:1px;background:var(--accent)}
    .hero-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(80px,15vw,210px);
      line-height:.87;letter-spacing:.025em;color:var(--text);margin-bottom:1.6rem}
    .hero-title .ac{color:var(--accent)}
    .hero-title .ol{-webkit-text-stroke:1.5px rgba(255,255,255,.12);color:transparent}
    .hero-sub{font-size:1rem;font-weight:300;color:var(--muted);max-width:500px;line-height:1.7;margin-bottom:2.8rem}
    .hero-sub strong{color:var(--text);font-weight:500}
    .hero-actions{display:flex;gap:1.2rem;align-items:center;flex-wrap:wrap}
    .btn-primary{font-family:'Oswald',sans-serif;font-size:.82rem;font-weight:600;letter-spacing:.22em;
      text-transform:uppercase;color:var(--bg);background:var(--accent);padding:15px 38px;
      text-decoration:none;clip-path:polygon(10px 0%,100% 0%,calc(100% - 10px) 100%,0% 100%);
      transition:transform .2s,opacity .2s;display:inline-block}
    .btn-primary:hover{transform:translateY(-2px);opacity:.9}
    .btn-ghost{font-family:'Oswald',sans-serif;font-size:.82rem;font-weight:500;letter-spacing:.2em;
      text-transform:uppercase;color:var(--text);text-decoration:none;
      border-bottom:1px solid var(--accent);padding-bottom:3px;transition:color .2s}
    .btn-ghost:hover{color:var(--accent)}

    /* ── MARQUEE ── */
    .marquee-strip{background:var(--accent);padding:13px 0;overflow:hidden}
    .marquee-inner{display:flex;gap:0;animation:marquee 22s linear infinite;white-space:nowrap}
    .marquee-inner span{font-family:'Bebas Neue',sans-serif;font-size:1rem;letter-spacing:.22em;
      color:var(--bg);padding:0 2.2rem}
    .marquee-inner span.dot{color:rgba(0,0,0,.35);padding:0;font-size:.7rem}
    @keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

    /* ── SECTION COMMONS ── */
    section{padding:100px 5%}
    .sl{font-family:'Oswald',sans-serif;font-size:.68rem;font-weight:500;letter-spacing:.42em;
      text-transform:uppercase;color:var(--accent);margin-bottom:1rem;display:flex;align-items:center;gap:12px}
    .sl::after{content:'';display:block;width:32px;height:1px;background:var(--accent)}
    .st{font-family:'Bebas Neue',sans-serif;font-size:clamp(52px,7.5vw,100px);
      line-height:.9;letter-spacing:.03em;color:var(--text);margin-bottom:1.5rem}
    .st .ac{color:var(--accent)}

    /* ── STATS ── */
    #stats{padding:60px 5%;background:var(--card);border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
    .stats-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--border)}
    .stat-item{background:var(--card);padding:44px 28px;text-align:center}
    .stat-num{font-family:'Bebas Neue',sans-serif;font-size:clamp(56px,6.5vw,84px);
      line-height:1;color:var(--accent);margin-bottom:.3rem}
    .stat-lbl{font-family:'Oswald',sans-serif;font-size:.7rem;font-weight:400;letter-spacing:.28em;
      text-transform:uppercase;color:var(--muted)}

    /* ── ABOUT ── */
    #about{background:var(--bg)}
    .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center}
    .about-img-wrap{position:relative}
    .about-img{width:100%;aspect-ratio:4/5;background:var(--card);border:1px solid var(--border);
      display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
    .about-img img{width:100%;height:100%;object-fit:cover;opacity:.85}
    .about-img::before{content:'';position:absolute;inset:0;
      background:linear-gradient(135deg,rgba(255,69,0,.06) 0%,transparent 60%);z-index:1}
    .about-badge{position:absolute;bottom:-18px;right:-18px;width:110px;height:110px;
      background:var(--accent);display:flex;align-items:center;justify-content:center;flex-direction:column;z-index:2}
    .about-badge .bn{font-family:'Bebas Neue',sans-serif;font-size:2.2rem;line-height:1;color:var(--bg)}
    .about-badge .bt{font-family:'Oswald',sans-serif;font-size:.58rem;letter-spacing:.15em;
      text-transform:uppercase;color:rgba(0,0,0,.55)}
    .about-desc{font-size:.92rem;font-weight:300;color:var(--muted);line-height:1.85;margin-bottom:2rem}
    .about-desc strong{color:var(--text);font-weight:500}
    .perks{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    .perk{display:flex;align-items:center;gap:10px;font-family:'Oswald',sans-serif;
      font-size:.75rem;font-weight:400;letter-spacing:.1em;text-transform:uppercase;color:var(--muted)}
    .perk::before{content:'▸';color:var(--accent);font-size:.65rem}

    /* ── SERVICES ── */
    #services{background:var(--card)}
    .svc-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--border);margin-top:60px}
    .svc-card{background:var(--card);padding:40px 30px;transition:background .3s;position:relative;overflow:hidden}
    .svc-card::after{content:'';position:absolute;bottom:0;left:0;width:0;height:2px;
      background:var(--accent);transition:width .35s}
    .svc-card:hover{background:var(--card2)}
    .svc-card:hover::after{width:100%}
    .svc-icon{font-size:2rem;margin-bottom:1.2rem;display:block}
    .svc-name{font-family:'Bebas Neue',sans-serif;font-size:1.55rem;letter-spacing:.05em;
      color:var(--text);margin-bottom:.8rem}
    .svc-desc{font-size:.83rem;font-weight:300;color:var(--muted);line-height:1.75}

    /* ── PLANS ── */
    #plans{background:var(--bg)}
    .plans-head{display:flex;justify-content:space-between;align-items:flex-end;
      margin-bottom:60px;flex-wrap:wrap;gap:20px}
    .plans-note{font-size:.85rem;font-weight:300;color:var(--muted);max-width:280px;line-height:1.7}
    .plans-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--border)}
    .plan-card{background:var(--card);padding:40px 30px;position:relative;
      display:flex;flex-direction:column;transition:transform .3s}
    .plan-card.feat{background:var(--accent)}
    .plan-card:hover{transform:translateY(-5px)}
    .plan-badge{position:absolute;top:-1px;right:18px;background:var(--gold);color:var(--bg);
      font-family:'Oswald',sans-serif;font-size:.62rem;font-weight:700;letter-spacing:.15em;
      text-transform:uppercase;padding:5px 13px}
    .plan-nm{font-family:'Oswald',sans-serif;font-size:.72rem;font-weight:500;letter-spacing:.32em;
      text-transform:uppercase;color:var(--muted);margin-bottom:1rem}
    .plan-card.feat .plan-nm{color:rgba(0,0,0,.55)}
    .plan-price{font-family:'Bebas Neue',sans-serif;font-size:4.2rem;line-height:1;
      color:var(--text);margin-bottom:.3rem}
    .plan-card.feat .plan-price{color:var(--bg)}
    .plan-price sup{font-family:'DM Sans',sans-serif;font-size:1.3rem;font-weight:400;vertical-align:super}
    .plan-per{font-family:'Oswald',sans-serif;font-size:.68rem;letter-spacing:.22em;
      text-transform:uppercase;color:var(--muted);margin-bottom:2rem}
    .plan-card.feat .plan-per{color:rgba(0,0,0,.45)}
    .plan-div{height:1px;background:var(--border);margin-bottom:1.6rem}
    .plan-card.feat .plan-div{background:rgba(0,0,0,.15)}
    .plan-feats{list-style:none;flex:1;margin-bottom:2rem}
    .plan-feats li{font-size:.83rem;font-weight:300;color:var(--muted);padding:8px 0;
      display:flex;align-items:center;gap:10px;border-bottom:1px solid var(--border)}
    .plan-card.feat .plan-feats li{color:rgba(0,0,0,.65);border-color:rgba(0,0,0,.12)}
    .plan-feats li::before{content:'✓';color:var(--accent);font-size:.72rem;flex-shrink:0}
    .plan-card.feat .plan-feats li::before{color:var(--bg)}
    .plan-btn{font-family:'Oswald',sans-serif;font-size:.78rem;font-weight:600;letter-spacing:.2em;
      text-transform:uppercase;text-align:center;padding:14px;text-decoration:none;
      border:1px solid var(--accent);color:var(--accent);display:block;
      transition:background .2s,color .2s;
      clip-path:polygon(8px 0%,100% 0%,calc(100% - 8px) 100%,0% 100%)}
    .plan-btn:hover{background:var(--accent);color:var(--bg)}
    .plan-card.feat .plan-btn{background:var(--bg);color:var(--text);border-color:var(--bg)}
    .plan-card.feat .plan-btn:hover{background:var(--card2)}

    /* ── TRAINERS ── */
    #trainers{background:var(--card)}
    .tr-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--border);margin-top:60px}
    .tr-card{background:var(--card);overflow:hidden}
    .tr-img{width:100%;aspect-ratio:3/4;position:relative;overflow:hidden}
    .tr-img img{width:100%;height:100%;object-fit:cover;transition:transform .4s}
    .tr-card:hover .tr-img img{transform:scale(1.05)}
    .tr-img::after{content:'';position:absolute;bottom:0;left:0;right:0;height:55%;
      background:linear-gradient(to top,var(--card),transparent)}
    .tr-info{padding:24px 26px 30px}
    .tr-name{font-family:'Bebas Neue',sans-serif;font-size:1.9rem;letter-spacing:.04em;
      color:var(--text);margin-bottom:.3rem}
    .tr-role{font-family:'Oswald',sans-serif;font-size:.68rem;font-weight:400;letter-spacing:.2em;
      text-transform:uppercase;color:var(--accent);margin-bottom:1rem}
    .tr-desc{font-size:.82rem;font-weight:300;color:var(--muted);line-height:1.65}

    /* ── TESTIMONIALS ── */
    #testimonials{background:var(--bg)}
    .test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-top:60px}
    .test-card{background:var(--card);border:1px solid var(--border);padding:32px;position:relative}
    .test-card::before{content:'"';font-family:'Bebas Neue',sans-serif;font-size:5.5rem;
      color:var(--accent);opacity:.12;position:absolute;top:8px;left:18px;line-height:1;pointer-events:none}
    .test-stars{color:var(--gold);font-size:.82rem;margin-bottom:1rem;letter-spacing:2px}
    .test-text{font-size:.86rem;font-weight:300;color:var(--muted);line-height:1.75;
      margin-bottom:1.5rem;position:relative}
    .test-author{font-family:'Oswald',sans-serif;font-size:.72rem;font-weight:500;
      letter-spacing:.15em;text-transform:uppercase;color:var(--text)}
    .test-since{font-size:.68rem;color:var(--muted);margin-top:3px}

    /* ── CONTACT ── */
    #contact{background:var(--card)}
    .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:80px;margin-top:60px}
    .cf{display:flex;flex-direction:column;gap:16px}
    .fg{display:flex;flex-direction:column;gap:6px}
    .fl{font-family:'Oswald',sans-serif;font-size:.62rem;font-weight:500;letter-spacing:.26em;
      text-transform:uppercase;color:var(--muted)}
    .fi,.ft{background:var(--bg);border:1px solid var(--border);color:var(--text);
      font-family:'DM Sans',sans-serif;font-size:.88rem;padding:12px 16px;
      outline:none;transition:border-color .2s;width:100%}
    .fi:focus,.ft:focus{border-color:var(--accent)}
    .ft{resize:vertical;min-height:120px}
    .fsub{font-family:'Oswald',sans-serif;font-size:.82rem;font-weight:600;letter-spacing:.2em;
      text-transform:uppercase;color:var(--bg);background:var(--accent);border:none;
      padding:16px;cursor:pointer;clip-path:polygon(10px 0%,100% 0%,calc(100% - 10px) 100%,0% 100%);
      transition:opacity .2s;margin-top:8px}
    .fsub:hover{opacity:.85}
    .ci{display:flex;flex-direction:column;gap:28px}
    .ci-lbl{font-family:'Oswald',sans-serif;font-size:.62rem;font-weight:500;letter-spacing:.3em;
      text-transform:uppercase;color:var(--accent);margin-bottom:.5rem}
    .ci-val{font-size:.92rem;font-weight:300;color:var(--text);line-height:1.7}
    .ci-val a{color:var(--accent);text-decoration:none}
    .hours-g{display:flex;flex-direction:column;gap:6px}
    .hr{font-size:.8rem;font-weight:300;color:var(--muted);display:flex;justify-content:space-between;gap:24px}
    .hr strong{color:var(--text);font-weight:400}
    .map-wrap{width:100%;height:220px;border:1px solid var(--border);margin-top:10px;overflow:hidden}
    .map-wrap iframe{width:100%;height:100%;border:none;filter:grayscale(100%) invert(92%) contrast(83%)}

    /* ── FOOTER ── */
    footer{background:#040404;border-top:1px solid var(--border);padding:64px 5% 32px}
    .footer-top{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:60px;margin-bottom:48px}
    .f-logo{font-family:'Bebas Neue',sans-serif;font-size:2.6rem;letter-spacing:.15em;
      color:var(--text);display:block;margin-bottom:1rem}
    .f-logo span{color:var(--accent)}
    .f-tag{font-size:.8rem;font-weight:300;color:var(--muted);line-height:1.75;max-width:260px;margin-bottom:1.5rem}
    .f-social{display:flex;gap:10px}
    .soc{width:36px;height:36px;border:1px solid var(--border);display:flex;align-items:center;
      justify-content:center;text-decoration:none;font-family:'Oswald',sans-serif;font-size:.7rem;
      font-weight:500;color:var(--muted);transition:border-color .2s,color .2s}
    .soc:hover{border-color:var(--accent);color:var(--accent)}
    .f-col-title{font-family:'Oswald',sans-serif;font-size:.68rem;font-weight:600;letter-spacing:.3em;
      text-transform:uppercase;color:var(--text);margin-bottom:1.2rem}
    .f-links{list-style:none;display:flex;flex-direction:column;gap:10px}
    .f-links a{font-size:.8rem;font-weight:300;color:var(--muted);text-decoration:none;transition:color .2s}
    .f-links a:hover{color:var(--accent)}
    .f-bottom{display:flex;justify-content:space-between;align-items:center;
      padding-top:24px;border-top:1px solid var(--border);flex-wrap:wrap;gap:10px}
    .f-copy{font-family:'Oswald',sans-serif;font-size:.62rem;font-weight:400;letter-spacing:.15em;
      text-transform:uppercase;color:var(--muted)}
    .f-copy span{color:var(--accent)}
    .f-made{font-size:.72rem;color:var(--muted)}

    /* ── FADE ANIMATIONS ── */
    @keyframes fadeUp{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}
    .fu{opacity:0;animation:fadeUp .75s ease forwards}
    .d1{animation-delay:.1s}.d2{animation-delay:.28s}.d3{animation-delay:.46s}.d4{animation-delay:.62s}

    /* ── SCROLL REVEAL ── */
    .reveal{opacity:0;transform:translateY(40px);transition:opacity .8s ease,transform .8s ease}
    .reveal.active{opacity:1;transform:translateY(0)}

    /* ── RESPONSIVE ── */
    @media(max-width:1024px){
      .about-grid,.contact-grid{grid-template-columns:1fr;gap:50px}
      .footer-top{grid-template-columns:1fr 1fr;gap:40px}
      .svc-grid,.plans-grid,.tr-grid,.test-grid{grid-template-columns:1fr 1fr}
      .stats-grid{grid-template-columns:1fr 1fr}
    }
    @media(max-width:768px){
      .nav-links{display:none}
      .mobile-menu-btn{display:block}
      .svc-grid,.plans-grid,.tr-grid,.test-grid,.stats-grid{grid-template-columns:1fr}
      .footer-top{grid-template-columns:1fr}
      .hero-title{font-size:clamp(50px,14vw,120px)}
      section{padding:70px 5%}
      .plans-head{flex-direction:column;align-items:flex-start}
    }

    /* ── EDITOR PANEL ── */
    #edit-toggle{position:fixed;bottom:28px;right:28px;z-index:999;background:var(--accent);
      color:var(--bg);border:none;font-family:'Oswald',sans-serif;font-size:.72rem;font-weight:700;
      letter-spacing:.2em;text-transform:uppercase;padding:12px 22px;cursor:pointer;
      clip-path:polygon(8px 0%,100% 0%,calc(100% - 8px) 100%,0% 100%);
      box-shadow:0 4px 28px rgba(255,69,0,.45);transition:opacity .2s}
    #edit-toggle:hover{opacity:.85}
    #editor-panel{position:fixed;top:0;right:-420px;width:400px;height:100vh;
      background:#0c0c0c;border-left:1px solid var(--border);z-index:998;
      overflow-y:auto;transition:right .38s cubic-bezier(.4,0,.2,1);display:flex;flex-direction:column}
    #editor-panel.open{right:0}
    .ep-hd{padding:20px 24px;border-bottom:1px solid var(--border);display:flex;
      align-items:center;justify-content:space-between;position:sticky;top:0;background:#0c0c0c;z-index:2}
    .ep-title{font-family:'Bebas Neue',sans-serif;font-size:1.4rem;letter-spacing:.1em;color:var(--text)}
    .ep-close{background:none;border:1px solid var(--border);color:var(--muted);
      font-size:1rem;width:32px;height:32px;cursor:pointer;transition:color .2s,border-color .2s}
    .ep-close:hover{color:var(--accent);border-color:var(--accent)}
    .ep-tabs{display:flex;border-bottom:1px solid var(--border);position:sticky;top:61px;background:#0c0c0c;z-index:2}
    .ep-tab{flex:1;padding:12px 6px;background:none;border:none;border-bottom:2px solid transparent;
      color:var(--muted);font-family:'Oswald',sans-serif;font-size:.6rem;font-weight:500;
      letter-spacing:.12em;text-transform:uppercase;cursor:pointer;transition:color .2s,border-color .2s}
    .ep-tab.active{color:var(--accent);border-bottom-color:var(--accent)}
    .ep-body{padding:24px;flex:1}
    .ep-sec{display:none}
    .ep-sec.active{display:block}
    .ep-grp{margin-bottom:26px}
    .ep-gt{font-family:'Oswald',sans-serif;font-size:.58rem;font-weight:600;letter-spacing:.32em;
      text-transform:uppercase;color:var(--accent);margin-bottom:12px;padding-bottom:6px;
      border-bottom:1px solid var(--border)}
    .ep-fld{margin-bottom:14px}
    .ep-lbl{font-family:'Oswald',sans-serif;font-size:.58rem;font-weight:400;letter-spacing:.2em;
      text-transform:uppercase;color:var(--muted);display:block;margin-bottom:6px}
    .ep-in{width:100%;background:#141414;border:1px solid var(--border);color:var(--text);
      font-family:'DM Sans',sans-serif;font-size:.85rem;padding:9px 12px;
      outline:none;transition:border-color .2s}
    .ep-in:focus{border-color:var(--accent)}
    .ep-in[type="color"]{height:40px;padding:4px;cursor:pointer}
    .ep-btn{background:var(--accent);color:var(--bg);border:none;padding:10px 18px;
      font-family:'Oswald',sans-serif;font-size:.7rem;font-weight:600;letter-spacing:.15em;
      text-transform:uppercase;cursor:pointer;clip-path:polygon(6px 0%,100% 0%,calc(100% - 6px) 100%,0% 100%);
      transition:opacity .2s;margin-top:4px}
    .ep-btn:hover{opacity:.85}
    .ep-preview{font-size:.72rem;color:var(--muted);margin-top:6px;font-style:italic}

    /* Toast notification */
    .toast{position:fixed;bottom:90px;right:28px;background:var(--card2);border:1px solid var(--border);
      color:var(--text);padding:14px 22px;font-size:.82rem;z-index:1000;transform:translateY(100px);
      opacity:0;transition:all .4s ease;font-family:'Oswald',sans-serif;letter-spacing:.1em}
    .toast.show{transform:translateY(0);opacity:1}
  </style>
</head>
<body>

  <!-- ═══ NAV ═══ -->
  <nav id="navbar">
    <a href="#" class="nav-logo">GRAVI<span>T</span>Y</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#plans">Plans</a></li>
      <li><a href="#trainers">Trainers</a></li>
      <li><a href="#testimonials">Reviews</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <a href="#contact" class="nav-cta">Join Now</a>
    <button class="mobile-menu-btn" onclick="alert('Mobile menu coming soon')">☰</button>
  </nav>

  <!-- ═══ HERO ═══ -->
  <section id="hero">
    <div class="hero-ghost">GRAVITY</div>
    <div class="hero-vline"></div>
    <div class="hero-dot"></div>
    <div class="hero-content">
      <div class="hero-eyebrow fu d1">Unisex Fitness — Ranchi</div>
      <h1 class="hero-title fu d2">DEFY<br>YOUR <span class="ac">LIMITS</span></h1>
      <p class="hero-sub fu d3">
        <strong>Ranchi's most trusted fitness destination.</strong> Located at Galaxia Mall, Piska More, Ratu Road. 
        State-of-the-art equipment, certified trainers, and a community that pushes you further every single day.
      </p>
      <div class="hero-actions fu d4">
        <a href="#plans" class="btn-primary">View Memberships</a>
        <a href="#contact" class="btn-ghost">Free Trial →</a>
      </div>
    </div>
  </section>

  <!-- ═══ MARQUEE ═══ -->
  <div class="marquee-strip">
    <div class="marquee-inner">
      <span>STRENGTH</span><span class="dot">●</span>
      <span>CARDIO</span><span class="dot">●</span>
      <span>CROSSFIT</span><span class="dot">●</span>
      <span>ZUMBA</span><span class="dot">●</span>
      <span>YOGA</span><span class="dot">●</span>
      <span>PERSONAL TRAINING</span><span class="dot">●</span>
      <span>NUTRITION</span><span class="dot">●</span>
      <span>STRENGTH</span><span class="dot">●</span>
      <span>CARDIO</span><span class="dot">●</span>
      <span>CROSSFIT</span><span class="dot">●</span>
      <span>ZUMBA</span><span class="dot">●</span>
      <span>YOGA</span><span class="dot">●</span>
      <span>PERSONAL TRAINING</span><span class="dot">●</span>
      <span>NUTRITION</span><span class="dot">●</span>
    </div>
  </div>

  <!-- ═══ STATS ═══ -->
  <section id="stats">
    <div class="stats-grid">
      <div class="stat-item reveal">
        <div class="stat-num" data-target="1200">0</div>
        <div class="stat-lbl">Active Members</div>
      </div>
      <div class="stat-item reveal">
        <div class="stat-num" data-target="15">0</div>
        <div class="stat-lbl">Expert Trainers</div>
      </div>
      <div class="stat-item reveal">
        <div class="stat-num" data-target="4.9">0</div>
        <div class="stat-lbl">Google Rating</div>
      </div>
      <div class="stat-item reveal">
        <div class="stat-num" data-target="6">0</div>
        <div class="stat-lbl">Years Strong</div>
      </div>
    </div>
  </section>

  <!-- ═══ ABOUT ═══ -->
  <section id="about">
    <div class="about-grid">
      <div class="about-img-wrap reveal">
        <div class="about-img">
          <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=800&q=80" alt="GRAVITY Gym Interior">
        </div>
        <div class="about-badge">
          <span class="bn">6+</span>
          <span class="bt">Years</span>
        </div>
      </div>
      <div class="reveal">
        <div class="sl">About Us</div>
        <h2 class="st">WHERE <span class="ac">GRAVITY</span><br>MEETS GRIT</h2>
        <p class="about-desc">
          Located on the <strong>Lower Ground Floor of Galaxia Mall, Piska More, Ratu Road, Ranchi-834001</strong>, 
          GRAVITY Unisex Fitness has been transforming lives since 2019. We are not just a gym — we are a movement.
        </p>
        <p class="about-desc">
          Our <strong>8,000 sq. ft.</strong> facility features imported equipment from Life Fitness & Hammer Strength, 
          a dedicated CrossFit zone, functional training area, steam room, and separate locker rooms for men and women. 
          Rated <strong>4.9/5</strong> by our members, we pride ourselves on results, not promises.
        </p>
        <div class="perks">
          <div class="perk">Unisex Environment</div>
          <div class="perk">AC Training Floor</div>
          <div class="perk">Steam & Shower</div>
          <div class="perk">Diet Counseling</div>
          <div class="perk">Free Parking</div>
          <div class="perk">EMI Available</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ SERVICES ═══ -->
  <section id="services">
    <div class="reveal">
      <div class="sl">What We Offer</div>
      <h2 class="st">OUR <span class="ac">SERVICES</span></h2>
    </div>
    <div class="svc-grid">
      <div class="svc-card reveal">
        <span class="svc-icon">🏋️</span>
        <h3 class="svc-name">STRENGTH TRAINING</h3>
        <p class="svc-desc">Full range of free weights, plate-loaded machines, and cable stations. Progressive overload programs designed by our NSCA-certified coaches.</p>
      </div>
      <div class="svc-card reveal">
        <span class="svc-icon">🔥</span>
        <h3 class="svc-name">CROSSFIT ZONE</h3>
        <p class="svc-desc">Dedicated 1,200 sq. ft. CrossFit area with rigs, battle ropes, sleds, and kettlebells. High-intensity WODs every morning and evening.</p>
      </div>
      <div class="svc-card reveal">
        <span class="svc-icon">💃</span>
        <h3 class="svc-name">ZUMBA & AEROBICS</h3>
        <p class="svc-desc">Energizing group classes with certified Zumba instructors. Burn up to 800 calories per session while having fun.</p>
      </div>
      <div class="svc-card reveal">
        <span class="svc-icon">🧘</span>
        <h3 class="svc-name">YOGA & STRETCHING</h3>
        <p class="svc-desc">Morning yoga sessions for flexibility and mindfulness. Power yoga, Hatha, and restorative stretching classes available.</p>
      </div>
      <div class="svc-card reveal">
        <span class="svc-icon">🥗</span>
        <h3 class="svc-name">NUTRITION PLANS</h3>
        <p class="svc-desc">Customized diet charts by our in-house nutritionist. Vegetarian and non-vegetarian meal plans tailored to your fitness goals.</p>
      </div>
      <div class="svc-card reveal">
        <span class="svc-icon">🎯</span>
        <h3 class="svc-name">PERSONAL TRAINING</h3>
        <p class="svc-desc">One-on-one sessions with dedicated trainers. Body composition analysis, goal tracking, and weekly progress reports included.</p>
      </div>
    </div>
  </section>

  <!-- ═══ PLANS ═══ -->
  <section id="plans">
    <div class="plans-head reveal">
      <div>
        <div class="sl">Pricing</div>
        <h2 class="st">MEMBERSHIP <span class="ac">PLANS</span></h2>
      </div>
      <p class="plans-note">All plans include full gym access, locker, and steam. No hidden charges. EMI options available on 6-month and annual plans.</p>
    </div>
    <div class="plans-grid">
      <div class="plan-card reveal">
        <div class="plan-nm">Monthly</div>
        <div class="plan-price"><sup>₹</sup>1,499</div>
        <div class="plan-per">per month</div>
        <div class="plan-div"></div>
        <ul class="plan-feats">
          <li>Full Gym Access</li>
          <li>Basic Cardio & Weights</li>
          <li>Locker & Shower</li>
          <li>Group Classes (2/week)</li>
          <li>Steam Room Access</li>
        </ul>
        <a href="#contact" class="plan-btn">Get Started</a>
      </div>
      <div class="plan-card feat reveal">
        <div class="plan-badge">Best Value</div>
        <div class="plan-nm">6 Months</div>
        <div class="plan-price"><sup>₹</sup>7,499</div>
        <div class="plan-per">₹1,249/month</div>
        <div class="plan-div"></div>
        <ul class="plan-feats">
          <li>Everything in Monthly</li>
          <li>Unlimited Group Classes</li>
          <li>1 PT Session / Month</li>
          <li>Diet Consultation</li>
          <li>Body Composition Scan</li>
          <li>Freeze Option (15 days)</li>
        </ul>
        <a href="#contact" class="plan-btn">Join Now</a>
      </div>
      <div class="plan-card reveal">
        <div class="plan-nm">Annual</div>
        <div class="plan-price"><sup>₹</sup>12,999</div>
        <div class="plan-per">₹1,083/month</div>
        <div class="plan-div"></div>
        <ul class="plan-feats">
          <li>Everything in 6 Months</li>
          <li>2 PT Sessions / Month</li>
          <li>Quarterly Progress Report</li>
          <li>Supplement Discounts</li>
          <li>Guest Passes (4/year)</li>
          <li>Priority Booking</li>
        </ul>
        <a href="#contact" class="plan-btn">Go Annual</a>
      </div>
    </div>
  </section>

  <!-- ═══ TRAINERS ═══ -->
  <section id="trainers">
    <div class="reveal">
      <div class="sl">The Team</div>
      <h2 class="st">MEET YOUR <span class="ac">TRAINERS</span></h2>
    </div>
    <div class="tr-grid">
      <div class="tr-card reveal">
        <div class="tr-img">
          <img src="https://images.unsplash.com/photo-1567013127542-490d757e51fc?w=600&q=80" alt="Trainer">
        </div>
        <div class="tr-info">
          <h3 class="tr-name">RAJESH KUMAR</h3>
          <p class="tr-role">Head Coach — Strength</p>
          <p class="tr-desc">ACE Certified with 10+ years experience. Specializes in powerlifting and body recomposition. Trained 500+ clients.</p>
        </div>
      </div>
      <div class="tr-card reveal">
        <div class="tr-img">
          <img src="https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=600&q=80" alt="Trainer">
        </div>
        <div class="tr-info">
          <h3 class="tr-name">PRIYA SHARMA</h3>
          <p class="tr-role">CrossFit & Functional</p>
          <p class="tr-desc">CrossFit L1 Trainer and former national athlete. Known for high-energy WODs that push limits safely.</p>
        </div>
      </div>
      <div class="tr-card reveal">
        <div class="tr-img">
          <img src="https://images.unsplash.com/photo-1594381898411-846e7d193883?w=600&q=80" alt="Trainer">
        </div>
        <div class="tr-info">
          <h3 class="tr-name">AMIT SINGH</h3>
          <p class="tr-role">Nutritionist & Yoga</p>
          <p class="tr-desc">Certified nutritionist and 500hr RYT yoga instructor. Holistic approach to fitness and mindful eating.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ TESTIMONIALS ═══ -->
  <section id="testimonials">
    <div class="reveal">
      <div class="sl">Testimonials</div>
      <h2 class="st">MEMBER <span class="ac">STORIES</span></h2>
    </div>
    <div class="test-grid">
      <div class="test-card reveal">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">Best gym in Ranchi hands down. The equipment is world-class and trainers actually care about your progress. Lost 18kg in 4 months with Rajesh sir's guidance.</p>
        <div class="test-author">Ankit Mishra</div>
        <div class="test-since">Member since 2023</div>
      </div>
      <div class="test-card reveal">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">As a woman, I feel completely safe and comfortable here. The unisex environment is respectful and the Zumba classes are the highlight of my day!</p>
        <div class="test-author">Sneha Gupta</div>
        <div class="test-since">Member since 2024</div>
      </div>
      <div class="test-card reveal">
        <div class="test-stars">★★★★★</div>
        <p class="test-text">The CrossFit zone is incredible. I've been to gyms in Delhi and Mumbai — GRAVITY matches that quality at half the price. Location at Galaxia Mall is super convenient too.</p>
        <div class="test-author">Vikram Rathore</div>
        <div class="test-since">Member since 2022</div>
      </div>
    </div>
  </section>

  <!-- ═══ CONTACT ═══ -->
  <section id="contact">
    <div class="reveal">
      <div class="sl">Get In Touch</div>
      <h2 class="st">START YOUR <span class="ac">JOURNEY</span></h2>
    </div>
    <div class="contact-grid">
      <form class="cf reveal" id="contactForm" onsubmit="handleSubmit(event)">
        <div class="fg">
          <label class="fl">Full Name</label>
          <input type="text" class="fi" placeholder="Your name" required>
        </div>
        <div class="fg">
          <label class="fl">Phone Number</label>
          <input type="tel" class="fi" placeholder="+91 98765 43210" required>
        </div>
        <div class="fg">
          <label class="fl">Email</label>
          <input type="email" class="fi" placeholder="you@email.com">
        </div>
        <div class="fg">
          <label class="fl">Interested In</label>
          <select class="fi" style="cursor:pointer">
            <option>General Membership</option>
            <option>Personal Training</option>
            <option>CrossFit</option>
            <option>Zumba / Yoga</option>
            <option>Corporate Package</option>
          </select>
        </div>
        <div class="fg">
          <label class="fl">Message</label>
          <textarea class="ft" placeholder="Tell us about your fitness goals..."></textarea>
        </div>
        <button type="submit" class="fsub">Send Enquiry</button>
      </form>
      <div class="ci reveal">
        <div>
          <div class="ci-lbl">Location</div>
          <div class="ci-val">
            Lower Ground Floor, Galaxia Mall<br>
            Piska More, Vikash Nagar<br>
            Ratu Road, Ranchi — 834001<br>
            Jharkhand, India
          </div>
          <div class="map-wrap">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3662.857!2d85.2876!3d23.3692!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39f4e1a2a2a2a2a2%3A0x2a2a2a2a2a2a2a2a!2sGalaxia%20Mall%2C%20Ratu%20Road%2C%20Ranchi!5e0!3m2!1sen!2sin!4v1700000000000!5m2!1sen!2sin" allowfullscreen loading="lazy"></iframe>
          </div>
        </div>
        <div>
          <div class="ci-lbl">Contact</div>
          <div class="ci-val">
            <a href="tel:+919876543210">+91 98765 43210</a><br>
            <a href="mailto:info@gravityfitness.ranchi">info@gravityfitness.ranchi</a>
          </div>
        </div>
        <div>
          <div class="ci-lbl">Timings</div>
          <div class="hours-g">
            <div class="hr"><span>Monday — Saturday</span><strong>5:00 AM — 10:00 PM</strong></div>
            <div class="hr"><span>Sunday</span><strong>6:00 AM — 2:00 PM</strong></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ FOOTER ═══ -->
  <footer>
    <div class="footer-top">
      <div>
        <span class="f-logo">GRAVI<span>T</span>Y</span>
        <p class="f-tag">Ranchi's premier unisex fitness destination. Defy your limits at Galaxia Mall, Ratu Road. Results guaranteed.</p>
        <div class="f-social">
          <a href="#" class="soc" title="Instagram">IG</a>
          <a href="#" class="soc" title="Facebook">FB</a>
          <a href="#" class="soc" title="WhatsApp">WA</a>
          <a href="#" class="soc" title="YouTube">YT</a>
        </div>
      </div>
      <div>
        <h4 class="f-col-title">Quick Links</h4>
        <ul class="f-links">
          <li><a href="#about">About Us</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#plans">Memberships</a></li>
          <li><a href="#trainers">Trainers</a></li>
        </ul>
      </div>
      <div>
        <h4 class="f-col-title">Services</h4>
        <ul class="f-links">
          <li><a href="#">Strength Training</a></li>
          <li><a href="#">CrossFit</a></li>
          <li><a href="#">Zumba</a></li>
          <li><a href="#">Personal Training</a></li>
        </ul>
      </div>
      <div>
        <h4 class="f-col-title">Support</h4>
        <ul class="f-links">
          <li><a href="#contact">Contact</a></li>
          <li><a href="#">FAQ</a></li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Terms of Service</a></li>
        </ul>
      </div>
    </div>
    <div class="f-bottom">
      <p class="f-copy">© 2026 <span>GRAVITY</span> UNISEX FITNESS. ALL RIGHTS RESERVED.</p>
      <p class="f-made">Made with grit in Ranchi, Jharkhand</p>
    </div>
  </footer>

  <!-- ═══ EDITOR PANEL ═══ -->
  <button id="edit-toggle" onclick="toggleEditor()">Edit Site</button>
  <div id="editor-panel">
    <div class="ep-hd">
      <span class="ep-title">Site Editor</span>
      <button class="ep-close" onclick="toggleEditor()">×</button>
    </div>
    <div class="ep-tabs">
      <button class="ep-tab active" onclick="switchTab(0)">Content</button>
      <button class="ep-tab" onclick="switchTab(1)">Colors</button>
      <button class="ep-tab" onclick="switchTab(2)">About</button>
    </div>
    <div class="ep-body">
      <!-- TAB: Content -->
      <div class="ep-sec active">
        <div class="ep-grp">
          <div class="ep-gt">Hero Section</div>
          <div class="ep-fld">
            <label class="ep-lbl">Headline Line 1</label>
            <input class="ep-in" type="text" id="heroL1" value="DEFY" oninput="updateHero()">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Headline Line 2</label>
            <input class="ep-in" type="text" id="heroL2" value="YOUR LIMITS" oninput="updateHero()">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Subtitle</label>
            <textarea class="ep-in" id="heroSub" rows="3" oninput="updateHero()">Ranchi's most trusted fitness destination. Located at Galaxia Mall, Piska More, Ratu Road. State-of-the-art equipment, certified trainers, and a community that pushes you further every single day.</textarea>
          </div>
        </div>
        <div class="ep-grp">
          <div class="ep-gt">Contact Info</div>
          <div class="ep-fld">
            <label class="ep-lbl">Phone</label>
            <input class="ep-in" type="text" id="epPhone" value="+91 98765 43210">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Email</label>
            <input class="ep-in" type="text" id="epEmail" value="info@gravityfitness.ranchi">
          </div>
          <button class="ep-btn" onclick="updateContact()">Update Contact</button>
        </div>
      </div>
      <!-- TAB: Colors -->
      <div class="ep-sec">
        <div class="ep-grp">
          <div class="ep-gt">Brand Colors</div>
          <div class="ep-fld">
            <label class="ep-lbl">Accent Color (Orange)</label>
            <input class="ep-in" type="color" id="accentColor" value="#FF4500" oninput="updateColors()">
            <p class="ep-preview" id="accentPreview">Current: #FF4500</p>
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Gold Color</label>
            <input class="ep-in" type="color" id="goldColor" value="#D4A017" oninput="updateColors()">
            <p class="ep-preview" id="goldPreview">Current: #D4A017</p>
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Background</label>
            <input class="ep-in" type="color" id="bgColor" value="#080808" oninput="updateColors()">
          </div>
          <button class="ep-btn" onclick="resetColors()">Reset to Default</button>
        </div>
      </div>
      <!-- TAB: About -->
      <div class="ep-sec">
        <div class="ep-grp">
          <div class="ep-gt">Business Details</div>
          <div class="ep-fld">
            <label class="ep-lbl">Gym Name</label>
            <input class="ep-in" type="text" id="gymName" value="GRAVITY Unisex Fitness">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Established Year</label>
            <input class="ep-in" type="number" id="estYear" value="2019">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Square Feet</label>
            <input class="ep-in" type="text" id="sqft" value="8,000">
          </div>
          <div class="ep-fld">
            <label class="ep-lbl">Google Rating</label>
            <input class="ep-in" type="text" id="gRating" value="4.9">
          </div>
          <button class="ep-btn" onclick="updateAbout()">Update Details</button>
        </div>
      </div>
    </div>
  </div>

  <!-- Toast -->
  <div class="toast" id="toast">Message sent successfully!</div>

  <script>
    // ── NAV SCROLL EFFECT ──
    const nav = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
      if(window.scrollY > 50) nav.classList.add('scrolled');
      else nav.classList.remove('scrolled');
    });

    // ── SCROLL REVEAL ──
    const reveals = document.querySelectorAll('.reveal');
    const revealObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.classList.add('active');
          // Trigger counter animation if stat
          const statNum = entry.target.querySelector('.stat-num');
          if(statNum && !statNum.classList.contains('counted')) {
            statNum.classList.add('counted');
            animateCounter(statNum);
          }
        }
      });
    }, {threshold: 0.15});
    reveals.forEach(el => revealObserver.observe(el));

    // ── COUNTER ANIMATION ──
    function animateCounter(el) {
      const target = parseFloat(el.dataset.target);
      const isDecimal = target % 1 !== 0;
      const duration = 2000;
      const start = performance.now();
      function update(now) {
        const progress = Math.min((now - start) / duration, 1);
        const ease = 1 - Math.pow(1 - progress, 3);
        const current = target * ease;
        el.textContent = isDecimal ? current.toFixed(1) : Math.floor(current);
        if(progress < 1) requestAnimationFrame(update);
      }
      requestAnimationFrame(update);
    }

    // ── EDITOR PANEL ──
    function toggleEditor() {
      document.getElementById('editor-panel').classList.toggle('open');
    }
    function switchTab(n) {
      document.querySelectorAll('.ep-tab').forEach((t,i) => t.classList.toggle('active', i===n));
      document.querySelectorAll('.ep-sec').forEach((s,i) => s.classList.toggle('active', i===n));
    }

    // ── LIVE EDITS ──
    function updateHero() {
      const l1 = document.getElementById('heroL1').value;
      const l2 = document.getElementById('heroL2').value;
      const sub = document.getElementById('heroSub').value;
      document.querySelector('.hero-title').innerHTML = l1 + '<br>' + l2.split(' ').map((w,i) => i===1 ? '<span class="ac">' + w + '</span>' : w).join(' ');
      document.querySelector('.hero-sub').innerHTML = sub.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>');
    }
    function updateColors() {
      const accent = document.getElementById('accentColor').value;
      const gold = document.getElementById('goldColor').value;
      const bg = document.getElementById('bgColor').value;
      document.documentElement.style.setProperty('--accent', accent);
      document.documentElement.style.setProperty('--gold', gold);
      document.documentElement.style.setProperty('--bg', bg);
      document.getElementById('accentPreview').textContent = 'Current: ' + accent;
      document.getElementById('goldPreview').textContent = 'Current: ' + gold;
    }
    function resetColors() {
      document.getElementById('accentColor').value = '#FF4500';
      document.getElementById('goldColor').value = '#D4A017';
      document.getElementById('bgColor').value = '#080808';
      updateColors();
    }
    function updateContact() {
      const phone = document.getElementById('epPhone').value;
      const email = document.getElementById('epEmail').value;
      document.querySelector('.ci-val a[href^="tel"]').href = 'tel:' + phone.replace(/\s/g,'');
      document.querySelector('.ci-val a[href^="tel"]').textContent = phone;
      document.querySelector('.ci-val a[href^="mailto"]').href = 'mailto:' + email;
      document.querySelector('.ci-val a[href^="mailto"]').textContent = email;
      showToast('Contact info updated!');
    }
    function updateAbout() {
      showToast('Business details updated!');
    }

    // ── FORM HANDLER ──
    function handleSubmit(e) {
      e.preventDefault();
      showToast('Enquiry sent! We will call you within 24 hours.');
      e.target.reset();
    }
    function showToast(msg) {
      const t = document.getElementById('toast');
      t.textContent = msg;
      t.classList.add('show');
      setTimeout(() => t.classList.remove('show'), 3000);
    }

    // ── SMOOTH SCROLL FOR ANCHORS ──
    document.querySelectorAll('a[href^="#"]').forEach(a => {
      a.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if(target) target.scrollIntoView({behavior:'smooth',block:'start'});
      });
    });
  </script>
</body>
</html>
