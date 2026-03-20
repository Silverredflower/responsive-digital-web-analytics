<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Responsive Digital — Agencia de Analítica Digital</title>
<meta name="description" content="Agencia boutique especializada en Digital Analytics, GA4, GTM y Google Ads para ecommerce y pymes argentinas.">
<link href="https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap" rel="stylesheet">
<style>
:root {
  --white:#FFFFFF; --teal-light:#D3F5F3; --bg-gray:#F8F8F8;
  --teal-dark:#23656F; --orange:#F15A24; --teal:#2ACDC3;
  --sand:#FBCC7F; --yellow:#FEC72F; --coral:#FF837F; --off-white:#F6F6F6;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Raleway',sans-serif;background:#FFFFFF;color:#23656F;overflow-x:hidden;}

/* NAV */
nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  display:flex;align-items:center;justify-content:space-between;
  padding:16px 48px;background:#FFFFFF;
  border-bottom:1px solid rgba(42,205,195,0.15);
  box-shadow:0 2px 16px rgba(35,101,111,0.07);
}
.nav-logo{display:flex;align-items:center;gap:10px;text-decoration:none;}
.nav-logo img{height:40px;width:auto;mix-blend-mode:multiply;}
.nav-logo-text{font-family:'Raleway',sans-serif;font-weight:700;font-size:18px;color:#F15A24;letter-spacing:-0.3px;}
.nav-links{display:flex;align-items:center;gap:12px;}

/* BUTTONS */
.btn-pill{
  background:#F15A24;color:#F6F6F6;padding:14px 32px;border-radius:100px;
  font-family:'Raleway',sans-serif;font-weight:700;font-size:15px;
  text-decoration:none;border:none;cursor:pointer;
  transition:transform 0.2s,background 0.2s;display:inline-flex;align-items:center;gap:8px;
  box-shadow:0 4px 16px rgba(241,90,36,0.25);
}
.btn-pill:hover{transform:translateY(-2px);background:#d44d1e;}
.btn-pill-lg{
  background:#F15A24;color:#F6F6F6;padding:18px 40px;border-radius:100px;
  font-family:'Raleway',sans-serif;font-weight:700;font-size:16px;
  text-decoration:none;border:2px solid #F15A24;cursor:pointer;
  transition:transform 0.2s,background 0.2s;display:inline-flex;align-items:center;gap:8px;
  box-shadow:0 6px 20px rgba(241,90,36,0.25);
}
.btn-pill-lg:hover{transform:translateY(-2px);background:#d44d1e;border-color:#d44d1e;}

/* HERO */
#hero{
  min-height:100vh;padding:130px 48px 80px;
  background:#D3F5F3;position:relative;overflow:hidden;
  display:flex;flex-direction:column;justify-content:center;
}
.hero-grid{
  position:absolute;inset:0;
  background-image:linear-gradient(rgba(35,101,111,0.05) 1px,transparent 1px),linear-gradient(90deg,rgba(35,101,111,0.05) 1px,transparent 1px);
  background-size:56px 56px;
}
.hero-glow{
  position:absolute;inset:0;
  background:radial-gradient(ellipse 55% 55% at 75% 50%,rgba(42,205,195,0.1) 0%,transparent 65%);
}
.hero-tag{
  display:inline-flex;align-items:center;gap:8px;
  background:rgba(35,101,111,0.1);border:1px solid rgba(35,101,111,0.25);
  border-radius:100px;padding:7px 18px;font-size:13px;color:#23656F;
  font-weight:600;margin-bottom:28px;width:fit-content;position:relative;z-index:1;
}
.hero-dot{width:7px;height:7px;background:#23656F;border-radius:50%;animation:pulse 2s infinite;}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1);}50%{opacity:0.4;transform:scale(0.75);}}
.hero-h1{
  font-size:52px;font-weight:700;line-height:1.1;letter-spacing:-1.5px;
  color:#23656F;max-width:780px;position:relative;z-index:1;margin-bottom:24px;
}
.hero-sub{
  font-size:18px;color:#23656F;max-width:560px;line-height:1.75;
  font-weight:500;position:relative;z-index:1;margin-bottom:40px;
}
.hero-ctas{display:flex;gap:16px;flex-wrap:wrap;position:relative;z-index:1;}
.hero-stats{
  display:flex;gap:40px;margin-top:60px;padding-top:36px;
  border-top:1px solid rgba(35,101,111,0.18);position:relative;z-index:1;
}
.stat-n{font-size:28px;font-weight:700;color:#23656F;line-height:1;margin-bottom:4px;}
.stat-l{font-size:12px;color:rgba(35,101,111,0.6);font-weight:500;}

/* TICKER */
#ticker{
  padding:18px 0;background:#FFFFFF;overflow:hidden;
  border-top:1px solid rgba(42,205,195,0.2);border-bottom:1px solid rgba(42,205,195,0.2);
}
.t-track{display:flex;width:max-content;animation:tick 28s linear infinite;}
@keyframes tick{from{transform:translateX(0);}to{transform:translateX(-50%);}}
.t-item{
  display:inline-flex;align-items:center;gap:10px;padding:0 28px;
  font-size:12px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;
  color:rgba(35,101,111,0.5);
}
.t-dot{width:4px;height:4px;background:#2ACDC3;border-radius:50%;}

/* SECTIONS */
section{padding:100px 48px;position:relative;}
.s-tag{
  display:inline-flex;align-items:center;gap:8px;font-size:12px;font-weight:700;
  letter-spacing:2px;text-transform:uppercase;color:#2ACDC3;margin-bottom:18px;
}
.s-tag::before{content:'';width:24px;height:2px;background:#2ACDC3;}
.s-title{font-size:48px;font-weight:700;line-height:1.1;letter-spacing:-1.5px;margin-bottom:16px;color:#23656F;}
.s-title em{font-style:italic;color:#2ACDC3;}
.s-sub{font-size:17px;color:rgba(35,101,111,0.65);line-height:1.7;max-width:560px;font-weight:500;}

/* S2 PROBLEMA */
#problema{background:#FFFFFF;}
.prob-grid{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;margin-top:56px;}
.prob-cards{display:flex;flex-direction:column;gap:20px;}
.prob-card{
  display:flex;gap:18px;padding:24px;background:#F8F8F8;
  border:1px solid rgba(35,101,111,0.1);border-radius:16px;transition:border-color 0.2s,box-shadow 0.2s;
}
.prob-card:hover{border-color:#2ACDC3;box-shadow:0 4px 20px rgba(42,205,195,0.1);}
.prob-icon{
  width:48px;height:48px;min-width:48px;background:rgba(241,90,36,0.1);
  border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:22px;
}
.prob-card h4{font-size:15px;font-weight:700;color:#23656F;margin-bottom:6px;}
.prob-card p{font-size:14px;color:rgba(35,101,111,0.65);line-height:1.6;}
.funnel-box{background:#F8F8F8;border:1px solid rgba(42,205,195,0.2);border-radius:24px;padding:32px;}
.funnel-lbl{font-size:12px;font-weight:700;color:rgba(35,101,111,0.45);text-transform:uppercase;letter-spacing:1px;margin-bottom:24px;}
.f-steps{display:flex;flex-direction:column;gap:8px;}
.f-row{display:flex;align-items:center;gap:12px;}
.f-bar{height:44px;border-radius:8px;display:flex;align-items:center;padding:0 16px;font-size:14px;font-weight:600;color:#FFFFFF;}
.f-pct{font-size:13px;color:rgba(35,101,111,0.5);font-weight:500;white-space:nowrap;}
.funnel-note{margin-top:20px;font-size:12px;color:rgba(35,101,111,0.4);font-style:italic;line-height:1.5;}

/* S3 VUELOS */
#servicios{background:#F8F8F8;}
.vuelos{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-top:56px;}
.v-card{
  background:#FFFFFF;border:1px solid rgba(35,101,111,0.1);border-radius:24px;
  padding:36px 32px;position:relative;transition:border-color 0.3s,transform 0.3s,box-shadow 0.3s;
  display:flex;flex-direction:column;
}
.v-card:hover{border-color:#2ACDC3;transform:translateY(-4px);box-shadow:0 12px 40px rgba(42,205,195,0.12);}
.v-card.feat{border-color:#23656F;background:linear-gradient(135deg,rgba(42,205,195,0.04),#FFFFFF);}
.feat-badge{
  position:absolute;top:20px;right:20px;background:#23656F;color:#FFFFFF;
  font-size:11px;font-weight:700;padding:5px 14px;border-radius:100px;
}
.v-tag{font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#2ACDC3;margin-bottom:16px;display:block;}
.v-icon{font-size:36px;margin-bottom:16px;display:block;}
.v-name{font-size:22px;font-weight:700;color:#23656F;margin-bottom:6px;}
.v-sub{font-size:13px;color:#23656F;font-weight:500;font-style:italic;margin-bottom:16px;}
.v-desc{font-size:14px;color:#23656F;line-height:1.7;margin-bottom:24px;font-weight:500;}
.v-items{display:flex;flex-direction:column;gap:10px;margin-bottom:32px;flex:1;}
.v-item{display:flex;align-items:center;gap:10px;font-size:14px;color:#23656F;font-weight:500;}
.v-item::before{content:'';width:6px;height:6px;background:#2ACDC3;border-radius:50%;flex-shrink:0;}

/* S4 CASOS */
#casos{background:#23656F;}
.casos-hdr{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:52px;}
.casos-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;}
.c-card{
  background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.15);
  border-radius:20px;padding:32px;transition:border-color 0.2s,transform 0.2s;
}
.c-card:hover{border-color:rgba(42,205,195,0.4);transform:translateY(-3px);}
.c-type{font-size:11px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:#FBCC7F;margin-bottom:16px;}
.c-top{display:flex;align-items:center;gap:12px;margin-bottom:18px;}
.c-emoji{font-size:32px;}
.c-name{font-size:18px;font-weight:700;color:#2ACDC3;}
.c-cat{font-size:12px;color:rgba(255,255,255,0.5);}
.c-prob{
  background:rgba(241,90,36,0.08);border-left:2px solid #F15A24;
  padding:12px 16px;border-radius:0 8px 8px 0;
  font-size:13px;color:rgba(255,255,255,0.8);line-height:1.5;margin-bottom:18px;
}
.c-tags{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:20px;}
.c-tag{
  background:rgba(42,205,195,0.1);border:1px solid rgba(42,205,195,0.2);
  color:#2ACDC3;font-size:11px;font-weight:600;padding:4px 12px;border-radius:100px;
}
.c-disc{font-size:11px;color:rgba(255,255,255,0.25);font-style:italic;border-top:1px solid rgba(255,255,255,0.08);padding-top:14px;}

/* S5 DEMO */
#demo{background:#23656F;}
.demo-g{display:grid;grid-template-columns:1fr 1.1fr;gap:80px;align-items:center;}
.demo-screen{
  background:rgba(255,255,255,0.1);border:1px solid rgba(42,205,195,0.2);
  border-radius:20px;overflow:hidden;
}
.demo-topbar{background:rgba(255,255,255,0.08);border-bottom:1px solid rgba(255,255,255,0.1);padding:14px 20px;display:flex;align-items:center;gap:8px;}
.ddots{display:flex;gap:6px;}
.ddot{width:10px;height:10px;border-radius:50%;}
.durl{background:rgba(255,255,255,0.07);border-radius:6px;padding:4px 12px;font-size:11px;color:rgba(255,255,255,0.35);flex:1;margin-left:6px;}
.demo-cnt{padding:20px;}
.demo-metrics{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:14px;}
.dm{background:rgba(255,255,255,0.08);border-radius:10px;padding:14px;text-align:center;}
.dm-v{font-size:20px;font-weight:700;margin-bottom:4px;}
.dm-l{font-size:10px;color:rgba(255,255,255,0.4);}
.demo-chart{background:rgba(255,255,255,0.08);border-radius:10px;padding:14px;height:100px;display:flex;align-items:flex-end;gap:6px;}
.dc-bar{flex:1;border-radius:3px 3px 0 0;}
.demo-text h3{font-size:32px;font-weight:700;color:#F6F6F6;line-height:1.2;letter-spacing:-0.5px;margin-bottom:16px;}
.demo-text p{font-size:15px;color:rgba(255,255,255,0.7);line-height:1.7;margin-bottom:28px;}
.d-link{
  display:block;width:fit-content;color:#2ACDC3;font-weight:600;font-size:15px;
  text-decoration:none;border-bottom:1px solid rgba(42,205,195,0.35);padding-bottom:2px;
  transition:border-color 0.2s;margin-bottom:12px;
}
.d-link:hover{border-color:#2ACDC3;}

/* S6 SOBRE */
#sobre{background:#F8F8F8;}
.sobre-g{display:grid;grid-template-columns:auto 1fr;gap:80px;align-items:center;margin-top:56px;}
.sobre-photo{
  width:280px;height:340px;background:linear-gradient(135deg,#D3F5F3,#FFFFFF);
  border-radius:24px;border:1px solid rgba(42,205,195,0.3);
  display:flex;align-items:center;justify-content:center;font-size:80px;
  box-shadow:0 8px 32px rgba(35,101,111,0.1);
}
.sobre-name{font-size:44px;font-weight:700;color:#23656F;letter-spacing:-1px;margin-bottom:8px;}
.sobre-role{font-size:16px;font-weight:600;color:#2ACDC3;margin-bottom:24px;}
.sobre-bio{font-size:16px;color:#2ACDC3;line-height:1.8;max-width:560px;margin-bottom:36px;font-weight:500;}

/* S7 FORM */
#auditoria{background:#23656F;overflow:hidden;}
#auditoria::before{
  content:'';position:absolute;top:-30%;right:-10%;width:500px;height:500px;
  background:radial-gradient(circle,rgba(42,205,195,0.12),transparent 60%);pointer-events:none;
}
.audit-g{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;position:relative;z-index:1;}
.audit-title{font-size:40px;font-weight:700;color:#FFFFFF;line-height:1.15;letter-spacing:-1px;margin-bottom:16px;}
.audit-sub{font-size:16px;color:rgba(255,255,255,0.7);line-height:1.7;margin-bottom:32px;}
.audit-pts{display:flex;flex-direction:column;gap:14px;}
.audit-pt{display:flex;align-items:center;gap:12px;font-size:14px;color:rgba(255,255,255,0.85);font-weight:500;}
.audit-pt::before{
  content:'✓';width:26px;height:26px;background:rgba(255,255,255,0.12);border-radius:50%;
  display:flex;align-items:center;justify-content:center;font-size:12px;color:#D3F5F3;flex-shrink:0;
}
.f-card{background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.15);border-radius:24px;padding:40px;}
.f-title{font-size:22px;font-weight:700;color:#FFFFFF;margin-bottom:8px;}
.f-sub{font-size:14px;color:rgba(255,255,255,0.5);margin-bottom:28px;}
.fg{margin-bottom:16px;}
.fg label{display:block;font-size:13px;font-weight:600;color:rgba(255,255,255,0.65);margin-bottom:8px;}
.fg input,.fg select{
  width:100%;background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.12);
  border-radius:10px;padding:14px 16px;font-size:14px;color:#FFFFFF;
  font-family:'Raleway',sans-serif;outline:none;transition:border-color 0.2s;
}
.fg input:focus,.fg select:focus{border-color:#2ACDC3;}
.fg input::placeholder{color:rgba(255,255,255,0.25);}
.fg select option{background:#23656F;}
.f-btn{
  width:100%;background:#F15A24;color:#F6F6F6;border:2px solid #F15A24;
  border-radius:100px;padding:18px;font-family:'Raleway',sans-serif;
  font-size:16px;font-weight:700;cursor:pointer;margin-top:8px;
  transition:background 0.2s,transform 0.2s;box-shadow:0 4px 16px rgba(241,90,36,0.25);
}
.f-btn:hover{background:#d44d1e;border-color:#d44d1e;transform:translateY(-1px);}
.f-disc{text-align:center;font-size:12px;color:rgba(255,255,255,0.3);margin-top:14px;}

/* FOOTER */
footer{background:#23656F;padding:60px 48px 0;}
.ft-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:48px;padding-bottom:48px;}
.ft-title{font-family:'Raleway',sans-serif;font-weight:700;font-size:17px;color:#FFFFFF;margin-bottom:16px;}
.ft-text{font-size:14px;color:rgba(255,255,255,0.75);line-height:1.75;}
.ft-text a{color:#FFFFFF;text-decoration:none;display:block;transition:opacity 0.2s;}
.ft-text a:hover{opacity:0.7;}
.ft-social{display:flex;gap:16px;margin-top:4px;}
.ft-social a{color:#FFFFFF;text-decoration:none;font-size:14px;display:flex;align-items:center;gap:8px;transition:opacity 0.2s;}
.ft-social a:hover{opacity:0.7;}
.ft-hr{border:none;border-top:1px solid rgba(255,255,255,0.18);margin:0;}
.ft-copy{text-align:center;padding:24px 0 32px;font-size:13px;color:rgba(255,255,255,0.55);}

/* MOBILE */
@media(max-width:768px){
  nav{padding:14px 20px;}
  .nav-links{display:none;}
  section{padding:70px 20px;}
  #hero{padding:100px 20px 60px;}
  .hero-h1{font-size:36px;}
  .s-title{font-size:32px;}
  .prob-grid,.demo-g,.sobre-g,.audit-g{grid-template-columns:1fr;gap:40px;}
  .vuelos,.casos-grid{grid-template-columns:1fr;}
  .casos-hdr{flex-direction:column;align-items:flex-start;gap:16px;}
  .hero-stats{gap:24px;flex-wrap:wrap;}
  .ft-grid{grid-template-columns:1fr;gap:32px;}
  footer{padding:48px 20px 0;}
  .sobre-photo{width:100%;height:200px;}
  .audit-title{font-size:32px;}
}
</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <a href="#" class="nav-logo">
    <img src="data:image/png;base64,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" alt="Responsive Digital" style="height:40px;width:auto;mix-blend-mode:multiply;">
    <span class="nav-logo-text">Responsive Digital</span>
  </a>
  <div style="display:flex;align-items:center;gap:12px;">
    <a href="#servicios" class="btn-pill">Ver Servicios</a>
    <a href="#auditoria" class="btn-pill">Auditoría gratuita →</a>
  </div>
</nav>

<!-- S1: HERO -->
<section id="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-tag"><span class="hero-dot"></span>Agencia boutique · Digital Analytics + Google Ads · Ecommerce ARG</div>
  <h1 class="hero-h1">Agencia de Analítica Digital enfocada en resultados claros</h1>
  <p class="hero-sub">Somos Responsive, una agencia boutique que combina analítica digital + IA para transformar tus datos en decisiones medibles y rentables.</p>
  <div class="hero-ctas">
    <a href="#auditoria" class="btn-pill-lg">Hablemos</a>
  </div>
  <div class="hero-stats">
    <div><div class="stat-n">GA4</div><div class="stat-l">Implementación & auditoría</div></div>
    <div><div class="stat-n">GTM</div><div class="stat-l">Arquitectura & DataLayer</div></div>
    <div><div class="stat-n">IA</div><div class="stat-l">Reportes automatizados</div></div>
    <div><div class="stat-n">Looker</div><div class="stat-l">Dashboards a medida</div></div>
  </div>
</section>

<!-- TICKER -->
<div id="ticker">
  <div class="t-track">
    <span class="t-item">SHOPIFY<span class="t-dot"></span></span>
    <span class="t-item">GOOGLE ANALYTICS<span class="t-dot"></span></span>
    <span class="t-item">WORDPRESS<span class="t-dot"></span></span>
    <span class="t-item">REACT<span class="t-dot"></span></span>
    <span class="t-item">SEO<span class="t-dot"></span></span>
    <span class="t-item">A/B TESTING<span class="t-dot"></span></span>
    <span class="t-item">CONVERSION OPTIMIZATION<span class="t-dot"></span></span>
    <span class="t-item">GOOGLE ADS<span class="t-dot"></span></span>
    <span class="t-item">UX DESIGN<span class="t-dot"></span></span>
    <span class="t-item">LOOKER STUDIO<span class="t-dot"></span></span>
    <span class="t-item">VTEX<span class="t-dot"></span></span>
    <span class="t-item">GTM<span class="t-dot"></span></span>
    <span class="t-item">SHOPIFY<span class="t-dot"></span></span>
    <span class="t-item">GOOGLE ANALYTICS<span class="t-dot"></span></span>
    <span class="t-item">WORDPRESS<span class="t-dot"></span></span>
    <span class="t-item">REACT<span class="t-dot"></span></span>
    <span class="t-item">SEO<span class="t-dot"></span></span>
    <span class="t-item">A/B TESTING<span class="t-dot"></span></span>
    <span class="t-item">CONVERSION OPTIMIZATION<span class="t-dot"></span></span>
    <span class="t-item">GOOGLE ADS<span class="t-dot"></span></span>
    <span class="t-item">UX DESIGN<span class="t-dot"></span></span>
    <span class="t-item">LOOKER STUDIO<span class="t-dot"></span></span>
    <span class="t-item">VTEX<span class="t-dot"></span></span>
    <span class="t-item">GTM<span class="t-dot"></span></span>
  </div>
</div>

<!-- S2: PROBLEMA -->
<section id="problema">
  <div class="s-tag">El problema</div>
  <h2 class="s-title" style="max-width:720px;">La mayoría de los negocios tienen el mismo problema: un sitio web que no convierte.</h2>
  <div class="prob-grid">
    <div class="prob-cards">
      <div class="prob-card">
        <div class="prob-icon">📉</div>
        <div>
          <h4>Tráfico alto, conversiones bajas</h4>
          <p>Recibís miles de visitas pero muy pocos se convierten en clientes. El tráfico sin datos confiables es plata tirada.</p>
        </div>
      </div>
      <div class="prob-card">
        <div class="prob-icon">⏱️</div>
        <div>
          <h4>No sabés qué está fallando</h4>
          <p>Sin tracking correcto, no podés identificar en qué paso del funnel se van los usuarios. Todo es suposición.</p>
        </div>
      </div>
      <div class="prob-card">
        <div class="prob-icon">💸</div>
        <div>
          <h4>Perdés dinero en ads sin resultados</h4>
          <p>Invertís en Google Ads pero sin conversiones bien trackeadas, los algoritmos no pueden optimizar y el CPA sube.</p>
        </div>
      </div>
    </div>
    <div class="funnel-box">
      <div class="funnel-lbl">Funnel de conversión — ¿dónde perdés clientes?</div>
      <div class="f-steps">
        <div class="f-row">
          <div class="f-bar" style="background:#2ACDC3;width:100%;">1.000 Visitantes</div>
          <span class="f-pct">100%</span>
        </div>
        <div class="f-row">
          <div class="f-bar" style="background:#FEC72F;width:60%;">150 Exploraron</div>
          <span class="f-pct">15%</span>
        </div>
        <div class="f-row">
          <div class="f-bar" style="background:#FF837F;width:35%;">25 Al checkout</div>
          <span class="f-pct">2.5%</span>
        </div>
        <div class="f-row">
          <div class="f-bar" style="background:#F15A24;width:20%;">5 Compraron</div>
          <span class="f-pct">0.5%</span>
        </div>
      </div>
      <p class="funnel-note">Solo el 0.5% de tus visitantes compra. Con datos confiables y un funnel bien medido, podés saber exactamente dónde y por qué se van los otros 995.</p>
    </div>
  </div>
</section>

<!-- S3: VUELOS -->
<section id="servicios">
  <div class="s-tag">Servicios</div>
  <h2 class="s-title">¿Trabajamos juntos?</h2>
  <p class="s-sub">Elegí el nivel de acompañamiento que mejor se adapte a tus necesidades y presupuesto.</p>
  <div class="vuelos">

    <div class="v-card">
      <span class="v-tag">VUELO 1</span>
      <span class="v-icon">🪜</span>
      <div class="v-name">Technical Foundation</div>
      <div class="v-sub">"Ordenamos la casa"</div>
      <p class="v-desc">Para ecommerce que necesitan ordenar su medición o están empezando con GA4. Proyecto único.</p>
      <div class="v-items">
        <div class="v-item">Auditoría 360° con IA</div>
        <div class="v-item">Plan de Medición + KPIs</div>
        <div class="v-item">Implementación GA4</div>
        <div class="v-item">Arquitectura GTM</div>
        <div class="v-item">Tracking Multicanal</div>
      </div>
      <a href="#auditoria" class="btn-pill-lg" style="width:100%;justify-content:center;">Hablemos</a>
    </div>

    <div class="v-card feat">
      <span class="feat-badge">Más popular</span>
      <span class="v-tag">VUELO 2</span>
      <span class="v-icon">📊</span>
      <div class="v-name">Advanced Measurement</div>
      <div class="v-sub">"Los datos hablan"</div>
      <p class="v-desc">Para quienes ya miden lo básico pero no saben qué hacer con los datos. Proyecto o upgrade.</p>
      <div class="v-items">
        <div class="v-item">Ecommerce Pro (DataLayer)</div>
        <div class="v-item">Dashboard Ejecutivo con IA</div>
        <div class="v-item">Dashboard de Campañas 360°</div>
        <div class="v-item">Consent Mode v2</div>
        <div class="v-item">Documentación Técnica</div>
      </div>
      <a href="#auditoria" class="btn-pill-lg" style="width:100%;justify-content:center;">Hablemos</a>
    </div>

    <div class="v-card">
      <span class="v-tag">VUELO 3</span>
      <span class="v-icon">💎</span>
      <div class="v-name">Growth & Optimization</div>
      <div class="v-sub">"Datos que trabajan solos"</div>
      <p class="v-desc">Retainer mensual para clientes que buscan optimizar su inversión mes a mes con datos confiables.</p>
      <div class="v-items">
        <div class="v-item">Reporte & Estrategia con IA</div>
        <div class="v-item">Gestión Google Ads</div>
        <div class="v-item">Calidad de Datos + Alertas</div>
        <div class="v-item">Atribución Avanzada</div>
        <div class="v-item">Soporte & Consultoría</div>
      </div>
      <a href="#auditoria" class="btn-pill-lg" style="width:100%;justify-content:center;">Hablemos</a>
    </div>

  </div>
</section>

<!-- S4: CASOS -->
<section id="casos">
  <div class="casos-hdr">
    <div>
      <div class="s-tag" style="color:#F6F6F6;--before-bg:#F6F6F6;">Casos de análisis</div>
      <h2 class="s-title" style="color:#F6F6F6;">Nuestra experiencia en <em>acción.</em></h2>
    </div>
    <p style="font-size:13px;color:rgba(246,246,246,0.65);max-width:280px;text-align:right;font-style:italic;">Análisis demostrativos realizados con metodología Responsive Digital sobre ecommerce argentinos reales.</p>
  </div>
  <div class="casos-grid">
    <div class="c-card">
      <div class="c-type">Auditoría Analítica</div>
      <div class="c-top"><div class="c-emoji">🏕️</div><div><div class="c-name">Ecommerce Outdoor</div><div class="c-cat">Marca líder · Tiendanube</div></div></div>
      <div class="c-prob">GA4 bloqueado por ERR_BLOCKED_BY_ORB — las ventas no se atribuían a ninguna fuente. Algoritmos de Google Ads funcionando a ciegas.</div>
      <div class="c-tags"><span class="c-tag">GA4</span><span class="c-tag">GTM</span><span class="c-tag">Diagnóstico crítico</span><span class="c-tag">CPA</span></div>
      <div class="c-disc">Análisis demostrativo · Metodología Responsive Digital</div>
    </div>
    <div class="c-card">
      <div class="c-type">Implementación Técnica</div>
      <div class="c-top"><div class="c-emoji">🐕</div><div><div class="c-name">Ecommerce Mascotas</div><div class="c-cat">Alimento natural · Tiendanube</div></div></div>
      <div class="c-prob">DataLayer incompleto — el funnel de compra era invisible. Imposible saber dónde abandonaban los usuarios ni optimizar Google Ads.</div>
      <div class="c-tags"><span class="c-tag">DataLayer</span><span class="c-tag">GTM</span><span class="c-tag">Ecommerce events</span><span class="c-tag">Google Ads</span></div>
      <div class="c-disc">Análisis demostrativo · Metodología Responsive Digital</div>
    </div>
    <div class="c-card">
      <div class="c-type">CRO + Medición</div>
      <div class="c-top"><div class="c-emoji">🐾</div><div><div class="c-name">Ecommerce Snacks</div><div class="c-cat">Snacks nutritivos · Tiendanube</div></div></div>
      <div class="c-prob">GA4 duplicado (2 IDs) — todos los datos inflados al doble. Decisiones de inversión en ads basadas en información incorrecta.</div>
      <div class="c-tags"><span class="c-tag">GA4 audit</span><span class="c-tag">CRO</span><span class="c-tag">Looker Studio</span><span class="c-tag">First-Party Data</span></div>
      <div class="c-disc">Análisis demostrativo · Metodología Responsive Digital</div>
    </div>
  </div>
</section>

<!-- S5: DEMO -->
<section id="demo">
  <div class="demo-g">
    <div class="demo-screen">
      <div class="demo-topbar">
        <div class="ddots"><div class="ddot" style="background:#FF837F;"></div><div class="ddot" style="background:#FEC72F;"></div><div class="ddot" style="background:#2ACDC3;"></div></div>
        <div class="durl">lookerstudio.google.com/reporting/…</div>
      </div>
      <div class="demo-cnt">
        <div class="demo-metrics">
          <div class="dm"><div class="dm-v" style="color:#2ACDC3;">$2.4M</div><div class="dm-l">Revenue</div></div>
          <div class="dm"><div class="dm-v" style="color:#FEC72F;">3.2%</div><div class="dm-l">Conv. Rate</div></div>
          <div class="dm"><div class="dm-v" style="color:#FF837F;">4.8x</div><div class="dm-l">ROAS</div></div>
        </div>
        <div class="demo-chart">
          <div class="dc-bar" style="height:40%;background:rgba(42,205,195,0.3);"></div>
          <div class="dc-bar" style="height:60%;background:rgba(42,205,195,0.4);"></div>
          <div class="dc-bar" style="height:45%;background:rgba(42,205,195,0.35);"></div>
          <div class="dc-bar" style="height:80%;background:rgba(42,205,195,0.55);"></div>
          <div class="dc-bar" style="height:55%;background:rgba(42,205,195,0.4);"></div>
          <div class="dc-bar" style="height:95%;background:#2ACDC3;"></div>
          <div class="dc-bar" style="height:70%;background:rgba(42,205,195,0.5);"></div>
        </div>
      </div>
    </div>
    <div class="demo-text">
      <h3>Mirá cómo trabajamos antes de contratarnos.</h3>
      <p>Con un Roadmap claro, dashboards en tiempo real y Google Ads optimizado con IA — cada centavo invertido tiene un destino concreto.</p>
      <a href="https://lookerstudio.google.com/reporting/58d493a7-e19d-4264-bacb-9b9a043cd230/page/bvonF" target="_blank" class="d-link">Ver dashboard en vivo →</a>
      <a href="https://lookerstudio.google.com/reporting/fc8aecec-a553-4ead-afe1-8cfd256f0e97/page/o2cqF" target="_blank" class="d-link">Ver segundo ejemplo →</a>
    </div>
  </div>
</section>

<!-- S6: ¿POR QUÉ? -->
<section id="sobre">
  <div class="s-tag">¿Por qué Responsive?</div>
  <h2 class="s-title" style="max-width:800px;">Analítica Digital + I.A. + Google Ads</h2>
  <p style="font-size:18px;color:#2ACDC3;line-height:1.8;max-width:760px;font-weight:500;margin-top:24px;margin-bottom:40px;">
    En Responsive Digital creemos que el crecimiento sostenido no se logra solo con marketing, sino con datos confiables que guían cada decisión. Nos especializamos en analítica digital para que tu inversión siempre tenga dirección. Implementamos GA4, GTM y Google Ads para ecommerce y pymes argentinas. Construimos dashboards con IA que muestran exactamente dónde vale la pena invertir — para que dejes de gastar en lo que no funciona y escales lo que sí.
  </p>
  <a href="#auditoria" class="btn-pill-lg">Trabajemos juntos →</a>
</section>

<!-- S7: AUDITORÍA -->
<section id="auditoria">
  <div class="audit-g">
    <div>
      <div class="s-tag" style="color:rgba(211,245,243,0.8);">Auditoría gratuita</div>
      <h2 class="audit-title">¿Listo para llevar tu ecommerce al siguiente nivel?</h2>
      <p class="audit-sub">Comenzá con una auditoría gratuita. En 48hs te mostramos exactamente dónde están las oportunidades de mejora en tu analítica.</p>
      <div class="audit-pts">
        <div class="audit-pt">Con datos confiables que guían cada decisión</div>
        <div class="audit-pt">Con dashboards a medida en Looker Studio</div>
        <div class="audit-pt">Con GA4 + GTM + IA aplicada a tu negocio</div>
        <div class="audit-pt">Con Google Ads optimizado para tu ecommerce</div>
        <div class="audit-pt">Sin tecnicismos, sin humo. Solo resultados.</div>
      </div>
    </div>
    <div class="f-card">
      <div class="f-title">Quiero mi auditoría gratuita</div>
      <div class="f-sub">Resultados en menos de 48 horas · 100% sin costo</div>
      <div class="fg"><label>URL de tu tienda *</label><input type="url" placeholder="https://mitienda.com.ar"></div>
      <div class="fg"><label>Tu email *</label><input type="email" placeholder="vos@tuempresa.com"></div>
      <div class="fg"><label>Plataforma de tu tienda</label>
        <select><option value="">Seleccioná una opción</option><option>Tiendanube</option><option>Shopify</option><option>VTEX</option><option>WordPress / WooCommerce</option><option>Otra</option></select>
      </div>
      <div class="fg"><label>¿Invertís en Google Ads?</label>
        <select><option value="">Seleccioná una opción</option><option>Sí, actualmente</option><option>No, pero quiero empezar</option><option>No por ahora</option></select>
      </div>
      <button class="f-btn">Quiero mi auditoría gratis →</button>
      <div class="f-disc">Sin spam · Sin compromiso · Respuesta en menos de 48hs</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="ft-grid">
    <div>
      <div class="ft-title">Responsive Digital</div>
      <p class="ft-text">Transformamos datos en decisiones rentables para ecommerce y pymes argentinas.</p>
    </div>
    <div>
      <div class="ft-title">Contacto</div>
      <div class="ft-text">
        <a href="/cdn-cgi/l/email-protection#f79f989b96b7859284879899849e8192939e909e83969bd996909299948e"><span class="__cf_email__" data-cfemail="84ecebe8e5c4f6e1f7f4ebeaf7edf2e1e0ede3edf0e5e8aae5e3e1eae7fd">[email&#160;protected]</span></a>
        <a href="https://wa.me/5491144391487" target="_blank">WhatsApp: +54 11 4439-1487</a>
      </div>
    </div>
    <div>
      <div class="ft-title">Seguinos</div>
      <div class="ft-social">
        <a href="https://www.instagram.com/responsive.digital/" target="_blank">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
          Instagram
        </a>
        <a href="https://ar.linkedin.com/company/responsivedigital-agency/" target="_blank">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
      </div>
    </div>
  </div>
  <hr class="ft-hr">
  <div class="ft-copy">© 2025 Responsive Digital. Todos los derechos reservados.</div>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
// WhatsApp Bridge on form submit
document.querySelector('.f-btn').addEventListener('click', function() {
  const url = document.querySelector('input[type="url"]').value || 'No informado';
  const email = document.querySelector('input[type="email"]').value || 'No informado';
  const selects = document.querySelectorAll('select');
  const platform = selects[0].value || 'No informado';
  const ads = selects[1].value || 'No informado';
  if (!url || !email) { alert('Por favor completá la URL y el email para continuar.'); return; }
  const msg = encodeURIComponent(
    `Hola Sofía! 👋 Completé el formulario de auditoría gratuita.\n\n` 
