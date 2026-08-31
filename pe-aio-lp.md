---
layout: default
title: "プロトコルエンジニアリングAIO｜ペアイオ"
---

# プロトコルエンジニアリングAIO｜ペアイオ

<style>
:root{
  --bg:#050816; --bg2:#0a1025; --text:#edf2ff; --muted:#aeb8d6;
  --line:rgba(170,190,255,.18); --panel:rgba(12,20,48,.72);
  --accent:#8ea7ff; --accent2:#c6a8ff; --gold:#ffe7a3;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0; color:var(--text); background:
  radial-gradient(circle at 50% 5%,rgba(105,130,255,.20),transparent 28%),
  radial-gradient(circle at 15% 55%,rgba(115,75,210,.12),transparent 30%),
  radial-gradient(circle at 85% 75%,rgba(60,120,210,.12),transparent 30%),
  var(--bg);
  font-family:system-ui,-apple-system,"Noto Sans JP","Yu Gothic",sans-serif;
  line-height:1.9;
}
.toc{
  position:sticky;top:0;z-index:20;
  backdrop-filter:blur(14px);
  background:rgba(5,8,22,.78);
  border-bottom:1px solid var(--line);
}
.toc-inner{max-width:1120px;margin:auto;padding:10px 24px;display:flex;flex-wrap:nowrap;gap:8px;overflow-x:auto;overflow-y:hidden;scrollbar-width:thin}
.toc-inner::-webkit-scrollbar{display:none}
.toc a{flex:0 0 auto;flex:0 0 auto;color:#cbd4ef;text-decoration:none;font-size:.84rem;padding:8px 12px;border-radius:999px;border:1px solid transparent}
.toc a:hover{border-color:var(--line);background:rgba(30,40,80,.55);color:#fff}
.diagnostic{
  margin:36px 0 0;padding:34px;border:1px solid rgba(142,167,255,.35);
  border-radius:26px;background:linear-gradient(145deg,rgba(20,30,68,.86),rgba(7,12,30,.82));
}
.diagnostic h3{font-size:1.6rem;margin-bottom:8px}
.diagnostic-badge{display:inline-block;padding:5px 10px;border-radius:999px;border:1px solid rgba(255,231,163,.35);color:var(--gold);font-size:.8rem;margin-bottom:10px}
.diagnostic a{display:inline-block;margin-top:18px;padding:13px 24px;border-radius:999px;border:1px solid rgba(142,167,255,.5);color:#fff;text-decoration:none;font-weight:800;background:rgba(142,167,255,.10)}
.diagnostic a:hover{background:rgba(142,167,255,.18)}
.depth-visual{
  min-height:600px;margin:40px 0;border-radius:30px;border:1px solid var(--line);
  position:relative;overflow:hidden;
  background:
    radial-gradient(circle at 50% 50%,rgba(255,231,163,.20),transparent 10%),
    radial-gradient(circle at 50% 50%,rgba(100,125,255,.18),transparent 32%),
    rgba(4,8,23,.78);
}
.depth-visual .axis{
  position:absolute;left:50%;top:50%;width:1px;height:82%;
  background:linear-gradient(transparent,rgba(142,167,255,.5),transparent);
  transform:rotate(22deg) translateY(-50%);transform-origin:center;
}
.depth-visual .plane{
  position:absolute;left:50%;top:50%;width:390px;height:180px;
  border:1px solid rgba(142,167,255,.25);border-radius:50%;
  transform:translate(-50%,-50%) rotate(-18deg);
}
.depth-visual .core{
  position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);
  width:150px;height:150px;border-radius:50%;display:grid;place-items:center;text-align:center;
  border:3px solid rgba(255,231,163,.95);
  background:radial-gradient(circle,rgba(255,231,163,.42),rgba(255,184,30,.16) 48%,rgba(30,35,90,.10));
  box-shadow:0 0 28px rgba(255,216,77,.72),0 0 85px rgba(255,216,77,.30),inset 0 0 28px rgba(255,231,163,.22);
}
.depth-visual .point{
  position:absolute;padding:11px 16px;border:2px solid rgba(255,216,77,.82);border-radius:999px;
  background:rgba(18,18,38,.90);color:#fff4b0;font-size:.9rem;
  box-shadow:0 0 14px rgba(255,216,77,.38),inset 0 0 12px rgba(255,216,77,.08);
  text-shadow:0 0 7px rgba(255,216,77,.58);
}
.depth-visual .p1{left:10%;top:18%}.depth-visual .p2{right:8%;top:27%}
.depth-visual .p3{left:12%;bottom:18%}.depth-visual .p4{right:9%;bottom:14%}
.depth-visual .p5{left:44%;top:8%}.depth-visual .p6{left:42%;bottom:7%}
.depth-caption{text-align:center;color:var(--muted);margin-top:18px}
body:before{
  content:""; position:fixed; inset:0; pointer-events:none; opacity:.55;
  background-image:
    radial-gradient(circle,rgba(255,255,255,.85) 0 1px,transparent 1.5px);
  background-size:97px 113px; background-position:12px 27px;
}
main{max-width:1120px;margin:auto;padding:0 24px}
.hero{min-height:92vh;display:grid;place-items:center;text-align:center;position:relative}
.hero-inner{max-width:920px;padding:90px 0}
.eyebrow{letter-spacing:.18em;color:var(--accent);font-weight:700}
h1{font-size:clamp(2.5rem,6vw,5.6rem);line-height:1.15;margin:22px 0 28px}
.hero h1 span{display:block;font-size:.42em;letter-spacing:.08em;color:var(--muted);margin-top:22px}
.lead{font-size:clamp(1.05rem,2vw,1.35rem);color:#d7def4;max-width:760px;margin:auto}
.section{padding:110px 0;border-top:1px solid var(--line)}
.kicker{color:var(--accent2);font-weight:800;letter-spacing:.12em}
h2{font-size:clamp(2rem,4vw,3.5rem);line-height:1.25;margin:12px 0 28px}
h3{font-size:1.35rem;margin-top:0}
p{color:#d2d9ee}
.card{
  background:linear-gradient(145deg,rgba(18,28,62,.82),rgba(7,13,32,.70));
  border:1px solid var(--line); border-radius:24px; padding:34px;
  box-shadow:0 20px 80px rgba(0,0,0,.22);
}
.compare{display:grid;grid-template-columns:1fr 1fr;gap:24px}
.compare .old{border-color:rgba(255,255,255,.14)}
.compare .new{border-color:rgba(142,167,255,.42)}
.flow{display:flex;flex-wrap:wrap;gap:10px;align-items:center;justify-content:center;margin:38px 0}
.flow .node{padding:13px 18px;border:1px solid var(--line);border-radius:999px;background:rgba(20,29,62,.8)}
.arrow{color:var(--accent);font-size:1.4rem}
.quote{
  font-size:clamp(1.5rem,3vw,2.4rem);font-weight:800;
  text-align:center;line-height:1.5; padding:55px 20px;
}


.cosmic-emphasis{
  display:inline-block;
  margin:.25em 0 .15em;
  font-size:clamp(1.55rem,3.2vw,2.5rem);
  font-weight:900;
  line-height:1.25;
  color:#ffd84d;
  text-shadow:
    0 0 8px rgba(255,216,77,.75),
    0 0 22px rgba(255,216,77,.45),
    0 0 44px rgba(255,190,40,.22);
}

.message-map{
  max-width:980px;margin:44px auto 0;text-align:left;
  border-top:1px solid var(--line);
}
.message-item{
  display:grid;grid-template-columns:250px 1fr;gap:24px;align-items:baseline;
  padding:21px 6px;border-bottom:1px solid var(--line);
  text-decoration:none;color:var(--text);
  transition:padding-left .2s ease,background .2s ease;
}
.message-item:hover{padding-left:16px;background:rgba(30,40,80,.20)}
.message-item span{font-size:.82rem;letter-spacing:.08em;color:var(--accent);font-weight:800}
.message-item strong{font-size:clamp(1.05rem,2vw,1.55rem);line-height:1.45}
.message-item:first-child strong{font-size:clamp(1.05rem,2vw,1.55rem)}
.form-note{font-size:.78rem!important;color:var(--muted)!important;margin-top:12px!important}
@media(max-width:760px){
  .message-item{grid-template-columns:1fr;gap:4px;padding:17px 4px}
  .message-item strong{font-size:1.05rem}
}

.cta{margin-top:50px;text-align:center;padding:45px 30px;border:1px solid rgba(255,231,163,.35);border-radius:26px;background:linear-gradient(145deg,rgba(35,28,65,.82),rgba(8,13,34,.82));box-shadow:0 20px 80px rgba(0,0,0,.25)}
.cta h3{font-size:1.7rem;margin-bottom:10px}.cta p{max-width:720px;margin:0 auto 24px}.cta a{display:inline-block;padding:14px 28px;border-radius:999px;border:1px solid rgba(255,231,163,.5);color:#fff;text-decoration:none;background:rgba(255,231,163,.10);font-weight:800}.cta a:hover{background:rgba(255,231,163,.18)}
.cta a{margin:8px}
.compare-table-wrap{overflow-x:auto;border:1px solid var(--line);border-radius:24px;background:#f4f5fa;-webkit-overflow-scrolling:touch;scrollbar-width:thin;scrollbar-color:var(--accent) rgba(0,0,0,.08)}
.compare-table-wrap::-webkit-scrollbar{height:10px}
.compare-table-wrap::-webkit-scrollbar-track{background:rgba(255,255,255,.06);border-radius:8px;margin:0 24px}
.compare-table-wrap::-webkit-scrollbar-thumb{background:var(--accent);border-radius:8px}
.compare-table-wrap::-webkit-scrollbar-thumb:hover{background:var(--accent2)}
.compare-hint{display:none;text-align:right;color:var(--muted);font-size:.8rem;margin:8px 4px 0}
@media(max-width:820px){.compare-hint{display:block}}
.compare-table{width:100%;border-collapse:collapse;min-width:760px}.compare-table th,.compare-table td{padding:24px;border-bottom:1px solid #dfe2ee;vertical-align:top}.compare-table th{font-size:1.2rem;text-align:left;background:#e7e9f4}.compare-table th:first-child{color:#14151d}.compare-table th:last-child{color:#14151d}.compare-table tr:last-child td{border-bottom:0}.compare-table td:first-child{width:50%;color:#20222b}.compare-table td:last-child{width:50%;color:#20222b}.compare-table b{display:inline-block;margin-bottom:6px;color:#2b3a67}
.placeholder{
  margin:34px 0; min-height:210px; display:grid;place-items:center;text-align:center;
  border:2px dashed rgba(142,167,255,.42);border-radius:22px;
  background:rgba(10,16,38,.58);padding:30px;
}
.placeholder strong{display:block;color:var(--gold);font-size:1.05rem;margin-bottom:8px}
.placeholder code{display:block;white-space:pre-wrap;text-align:left;color:#cbd5f2;font-size:.88rem;max-width:850px;margin:15px auto 0}
.starfield{position:relative;min-height:520px;overflow:hidden;border-radius:30px;border:1px solid var(--line);
background:radial-gradient(circle at 50% 50%,rgba(100,125,255,.18),transparent 16%),rgba(4,8,23,.72)}
.star{position:absolute;border-radius:50%;border:1px solid rgba(255,255,255,.3);background:rgba(142,167,255,.12);
display:grid;place-items:center;text-align:center;padding:12px;color:#e9edff}
.star.main{width:190px;height:190px;left:50%;top:50%;transform:translate(-50%,-50%);
border:2px solid rgba(255,231,163,.7);background:radial-gradient(circle,rgba(255,231,163,.22),rgba(65,75,150,.18));
box-shadow:0 0 70px rgba(255,231,163,.15)}
.s1{width:110px;height:110px;left:14%;top:18%}.s2{width:125px;height:125px;right:12%;top:20%}
.s3{width:120px;height:120px;left:12%;bottom:14%}.s4{width:115px;height:115px;right:14%;bottom:15%}
.s5{width:122px;height:122px;left:43.9%;top:6%}
.orbit{position:absolute;left:50%;top:50%;border:1px solid rgba(142,167,255,.18);border-radius:50%;transform:translate(-50%,-50%)}
.o1{width:330px;height:330px}.o2{width:520px;height:520px}
.pipeline{display:grid;grid-template-columns:repeat(5,1fr);gap:10px;margin-top:35px}
.pipeline div{padding:22px 12px;text-align:center;border:1px solid var(--line);border-radius:18px;background:var(--panel)}
.pipeline b{display:block;color:var(--accent);margin-bottom:8px}
footer{padding:70px 0 110px;text-align:center;color:var(--muted)}
@media(max-width:760px){
 .compare,.pipeline{grid-template-columns:1fr}
 .section{padding:75px 0}.card{padding:24px}
 .starfield{min-height:620px}.star.main{width:150px;height:150px}
 .s1{left:4%;top:10%}.s2{right:4%;top:17%}.s3{left:3%;bottom:10%}.s4{right:4%;bottom:8%}
}

/* === Visibility enhancement: key circled nodes === */
.starfield .star,
.depth-visual .point,
.depth-visual .core{
  border-color:#ffd84d !important;
  color:#fff4b0 !important;
  background:rgba(255,216,77,.09) !important;
  box-shadow:
    0 0 8px rgba(255,216,77,.90),
    0 0 22px rgba(255,216,77,.55),
    0 0 44px rgba(255,216,77,.28),
    inset 0 0 18px rgba(255,216,77,.10) !important;
  text-shadow:0 0 8px rgba(255,216,77,.75);
}

.starfield .main,
.depth-visual .core{
  border-width:2px !important;
  color:#fff9d6 !important;
  background:rgba(255,216,77,.16) !important;
  box-shadow:
    0 0 12px rgba(255,216,77,1),
    0 0 30px rgba(255,216,77,.68),
    0 0 60px rgba(255,216,77,.34),
    inset 0 0 24px rgba(255,216,77,.15) !important;
}

.flow .node{
  border-color:#ffd84d !important;
  color:#fff4b0 !important;
  box-shadow:0 0 10px rgba(255,216,77,.55), inset 0 0 10px rgba(255,216,77,.08) !important;
  text-shadow:0 0 7px rgba(255,216,77,.65);
}

@media (prefers-reduced-motion:no-preference){
  .starfield .star,
  .depth-visual .point,
  .depth-visual .core{
    animation:cosmicGlow 3.2s ease-in-out infinite alternate;
  }
  @keyframes cosmicGlow{
    from{filter:brightness(1)}
    to{filter:brightness(1.18)}
  }
  @keyframes orbitSpin{from{transform:translate(-50%,-50%) rotate(-18deg)}to{transform:translate(-50%,-50%) rotate(342deg)}}
}


/* === Pipeline node visibility === */
.pipeline .node,
.pipeline > div{
  color:#fff4b0 !important;
  border-color:#ffd84d !important;
  text-shadow:0 0 8px rgba(255,216,77,.70);
}
.pipeline .node b,
.pipeline > div b{
  color:#ffe36b !important;
}
.pipeline .node{
  box-shadow:
    0 0 8px rgba(255,216,77,.65),
    0 0 18px rgba(255,216,77,.28),
    inset 0 0 12px rgba(255,216,77,.08) !important;
}
.pipeline.big > div{
  background:rgba(255,216,77,.075) !important;
  box-shadow:
    0 0 10px rgba(255,216,77,.52),
    0 0 24px rgba(255,216,77,.22),
    inset 0 0 14px rgba(255,216,77,.08) !important;
}

/* 主星：02 STAR SYSTEM */
#star-system .starfield .main{
  border:4px solid #ffd84d !important;
  outline:2px solid rgba(255,216,77,.55);
  outline-offset:5px;
  background:radial-gradient(circle, rgba(255,216,77,.26), rgba(255,216,77,.08) 55%, transparent 72%) !important;
  box-shadow:
    0 0 10px rgba(255,216,77,1),
    0 0 28px rgba(255,216,77,.90),
    0 0 60px rgba(255,216,77,.58),
    0 0 110px rgba(255,216,77,.25),
    inset 0 0 30px rgba(255,216,77,.20) !important;
  color:#fffbe0 !important;
  text-shadow:
    0 0 8px rgba(255,216,77,.95),
    0 0 18px rgba(255,216,77,.65);
}

/* 主星：06 3D INTELLIGENCE SPACE */
#depth-expansion .depth-visual .core{
  border:4px solid #ffd84d !important;
  outline:2px solid rgba(255,216,77,.55);
  outline-offset:5px;
  background:radial-gradient(circle, rgba(255,216,77,.30), rgba(255,216,77,.09) 55%, transparent 75%) !important;
  box-shadow:
    0 0 12px rgba(255,216,77,1),
    0 0 30px rgba(255,216,77,.92),
    0 0 68px rgba(255,216,77,.62),
    0 0 120px rgba(255,216,77,.27),
    inset 0 0 34px rgba(255,216,77,.22) !important;
  color:#fffbe0 !important;
  text-shadow:
    0 0 9px rgba(255,216,77,.98),
    0 0 20px rgba(255,216,77,.68);
}

/* image concept cards */

.master-brief{
  max-width:1120px;margin:70px auto 0;padding:0 24px 20px;
}
.master-brief h2{font-size:clamp(1.4rem,2.5vw,2rem);margin:.35em 0 .65em}
.master-brief p{max-width:900px;color:#b9c2d4;line-height:1.9}
.master-brief strong{color:#ffe36b}
.visual-placeholder{
  min-height:210px;
  display:flex;flex-direction:column;justify-content:center;align-items:center;
  gap:12px;text-align:center;padding:28px;
}
.visual-placeholder strong{
  max-width:760px;color:#ffe36b;font-size:1.08rem;line-height:1.65;
}
.visual-placeholder small{
  max-width:820px;color:#aeb8cb;line-height:1.8;font-size:.9rem;
}


/* ===== INLINE SVG INTELLIGENCE DIAGRAMS ===== */
.svg-diagram{margin:38px 0;border:1px solid var(--line);border-radius:28px;overflow:hidden;background:radial-gradient(circle at 50% 50%,rgba(255,216,77,.09),transparent 28%),rgba(3,8,24,.78);box-shadow:0 20px 90px rgba(0,0,0,.24)}
.svg-diagram svg{display:block;width:100%;height:auto}
.svg-diagram .gold{fill:#ffd84d;stroke:#ffd84d}.svg-diagram .soft{stroke:#9aaeff;stroke-opacity:.34}.svg-diagram .label{fill:#fff0a6;font-weight:800}.svg-diagram .muted{fill:#aeb8d6}
.svg-diagram .core{filter:drop-shadow(0 0 13px rgba(255,216,77,.9))}
.svg-diagram .pulse{animation:svgPulse 3.5s ease-in-out infinite}.svg-diagram .spin{transform-box:fill-box;transform-origin:center;animation:svgSpin 22s linear infinite}.svg-diagram .spin-rev{transform-box:fill-box;transform-origin:center;animation:svgSpinRev 30s linear infinite}.svg-diagram .dash{animation:svgDash 4s linear infinite}.svg-diagram .scan{animation:svgScan 4.5s ease-in-out infinite}.svg-diagram .float{animation:svgFloat 4.8s ease-in-out infinite}
@keyframes svgPulse{0%,100%{opacity:.78;filter:drop-shadow(0 0 7px rgba(255,216,77,.45))}50%{opacity:1;filter:drop-shadow(0 0 24px rgba(255,216,77,1))}}
@keyframes svgSpin{to{transform:rotate(360deg)}}@keyframes svgSpinRev{to{transform:rotate(-360deg)}}@keyframes svgDash{to{stroke-dashoffset:-80}}@keyframes svgScan{0%,100%{opacity:.12}50%{opacity:.85}}@keyframes svgFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-7px)}}
@media(prefers-reduced-motion:reduce){.svg-diagram *{animation:none!important}}

.toc a.active{color:#fff0a6;border-color:rgba(255,216,77,.45);background:rgba(255,216,77,.07);box-shadow:0 0 14px rgba(255,216,77,.08)}
</style>

<nav class="toc" aria-label="PE-AIO メッセージ・ナビゲーション">
  <div class="toc-inner">
    <a href="#information-space">01｜INFORMATION SPACE</a>
    <a href="#star-system">02｜STAR SYSTEM</a>
    <a href="#prism">03｜PRISM STRATEGY</a>
    <a href="#ai-space">04｜AI KNOWLEDGE SPACE</a>
    <a href="#pe-aio">05｜INTELLIGENCE PIPELINE</a>
    <a href="#depth-expansion">06｜3D INTELLIGENCE SPACE</a>
    <a href="#vision">07｜VISION</a>
  </div>
</nav>


<main>

<section class="hero" id="hero">
  <div class="hero-inner">
    <div class="eyebrow">PROTOCOL ENGINEERING AIO : PE-AIO</div>
    <h1>話題作りより、知性づくりへ</em></h1>
    <p class="lead">
      人間の注目を集めるために情報を発信するのではなく、<br>
      <strong>AIに発見・理解・再構成される</strong><br>
      <span class="cosmic-emphasis">「知性の空間」を惑星系</span>に例えて考え方をお伝えしていきます。
    </p>

    <div class="message-map" aria-label="PE-AIO 7つのメッセージ">
      <a class="message-item" href="#information-space">
        <span>01｜INFORMATION SPACE</span>
        <strong>「輝く星」を作る時代から、「知性の空間」を作る時代へ</strong>
      </a>
      <a class="message-item" href="#star-system">
        <span>02｜STAR SYSTEM</span>
        <strong>知性を「主星」と「衛星」にする</strong>
      </a>
      <a class="message-item" href="#prism">
        <span>03｜PRISM STRATEGY</span>
        <strong>一つの知性を、異なる入口へ流し込む</strong>
      </a>
      <a class="message-item" href="#ai-space">
        <span>04｜AI KNOWLEDGE SPACE</span>
        <strong>AIが「意味の固まり」を発見する</strong>
      </a>
      <a class="message-item" href="#pe-aio">
        <span>05｜INTELLIGENCE PIPELINE</span>
        <strong>知性を構造化し、変換し、届ける</strong>
      </a>
      <a class="message-item" href="#depth-expansion">
        <span>06｜3D INTELLIGENCE SPACE</span>
        <strong>一つの「知性空間」を、深くしながら広げていく</strong>
      </a>
      <a class="message-item" href="#vision">
        <span>07｜VISION</span>
        <strong>AIが語り始める。その結果、人間が新しい知性を発見する。</strong>
      </a>
    </div>

    <div class="diagnostic" id="diagnostic">
      <span class="diagnostic-badge">FREE INTELLIGENCE DIAGNOSIS</span>
      <h3>あなたの「知性空間」は、どこまで構造化されていますか？</h3>
      <p>
        情報発信を「話題づくり」ではなく「知性づくり」の視点から見つめ直す、
        無料知性診断です。
      </p>
      <a href="YOUR_GOOGLE_FORM_URL" target="_blank" rel="noopener">無料知性診断を受ける →</a>
      <p class="form-note">※「YOUR_GOOGLE_FORM_URL」を実際のGoogleフォームURLに置き換えてください。</p>
    </div>
  </div>
</section>

<section class="section" id="information-space">
  <div class="kicker">01｜INFORMATION SPACE</div>
  <h2>「輝く星」を作る時代から、「知性の空間」を作る時代へ</h2>
  <p>
    これまでの情報発信では、目立つことが価値になりやすかった。
    話題をつくり、人間の注目を集め、クリックや反応によって「支持」を可視化する。
    いわば、夜空の中で<strong>ひときわ輝く星になる</strong>ことが重要だった。
  </p>
  <p>
    AIが情報を巡回し、複数の情報を横断して意味や関係を捉える時代には、
    別の可能性が生まれる。重要なのは、一つのコンテンツを輝かせることだけではなく、
    <strong>関連する知性を構造化し、一つの「意味の固まり」として存在させること</strong>だ。
  </p>

  <div class="compare-table-wrap">
    <table class="compare-table">
      <thead><tr><th>従来｜「輝く星」を作る</th><th>これから｜「知性の空間」を作る</th></tr></thead>
      <tbody>
        <tr><td><b>目的</b><br>話題をつくり、人間の注目を集める</td><td><b>目的</b><br>知性を構造化し、AIにも人間にも発見される知識空間をつくる</td></tr>
        <tr><td><b>中心</b><br>一つ一つの目立つコンテンツ</td><td><b>中心</b><br>知性の核と、それを深める意味のネットワーク</td></tr>
        <tr><td><b>広がり</b><br>拡散・バズ・リンクによって外へ広がる</td><td><b>広がり</b><br>問い、定義、具体例、応用、異なる認知経路へ広がる</td></tr>
        <tr><td><b>AIとの関係</b><br>AIを情報発信や検索のための道具として使う</td><td><b>AIとの関係</b><br>AIが情報群を発見し、意味を理解・再構成する空間をつくる</td></tr>
      </tbody>
    </table>
  </div>
  <p class="compare-hint">← 横にスクロールできます →</p>

  <div class="svg-diagram" aria-label="輝く星から知性の空間への転換">
<svg viewBox="0 0 1000 420" role="img">
<defs><radialGradient id="a1"><stop stop-color="#fff"/><stop offset=".3" stop-color="#dce8ff"/><stop offset="1" stop-color="#6b7cff" stop-opacity="0"/></radialGradient><radialGradient id="a2"><stop stop-color="#fffde0"/><stop offset=".35" stop-color="#ffd84d"/><stop offset="1" stop-color="#805900"/></radialGradient></defs>
<line x1="500" y1="45" x2="500" y2="375" stroke="#9aaeff" stroke-opacity=".18"/>
<text x="250" y="55" text-anchor="middle" fill="#edf2ff" font-size="25" font-weight="900">輝く星</text>
<text x="750" y="55" text-anchor="middle" fill="#fff0a6" font-size="25" font-weight="900">知性の空間</text>
<circle cx="250" cy="205" r="105" fill="url(#a1)" class="pulse"/><circle cx="250" cy="205" r="27" fill="#fff"/>
<text x="250" y="330" text-anchor="middle" fill="#aeb8d6" font-size="16">注目を集める</text>
<g fill="none" stroke="#ffd84d" stroke-opacity=".42"><ellipse cx="750" cy="205" rx="185" ry="78"/><ellipse cx="750" cy="205" rx="120" ry="48"/></g>
<circle cx="750" cy="205" r="48" fill="url(#a2)" class="core pulse"/>
<g fill="#ffe98a"><circle cx="565" cy="205" r="10"/><circle cx="935" cy="205" r="10"/><circle cx="750" cy="127" r="9"/><circle cx="750" cy="283" r="9"/></g>
<g stroke="#ffd84d" stroke-opacity=".62"><line x1="750" y1="205" x2="565" y2="205"/><line x1="750" y1="205" x2="935" y2="205"/><line x1="750" y1="205" x2="750" y2="127"/><line x1="750" y1="205" x2="750" y2="283"/></g>
<text x="750" y="330" text-anchor="middle" fill="#fff0a6" font-size="16">意味・関係・文脈をつなぐ</text>
<text x="500" y="385" text-anchor="middle" fill="#d7def4" font-size="17" font-weight="800">単発の注目 → 構造化された知性</text>
</svg></div>
</section>

<section class="section" id="star-system">
  <div class="kicker">02｜STAR SYSTEM</div>
  <h2>知性を「主星」と「衛星」にする</h2>
  <p>
    スターシステムは、複数の媒体を並べるための名前ではない。
    <strong>主星となる知性の核をつくり、それを異なる切り口から深める衛星を形成する。</strong>
    それぞれの衛星は主星の単なるコピーではなく、別の問い、別の理解、別の認知経路から
    同じ知性へ到達するための入口になる。
  </p>

  <div class="starfield">
    <div class="orbit o1"></div><div class="orbit o2"></div>
    <div class="star main">主星<br><b>知性の核</b><br>原理・概念・体系</div>
    <div class="star s1">定義<br>概念を明確にする</div>
    <div class="star s2">問い<br>知性を掘り下げる</div>
    <div class="star s3">具体例<br>理解を広げる</div>
    <div class="star s4">反例<br>境界を明らかにする</div>
    <div class="star s5">応用<br>別の領域へ広げる</div>
  </div>

  <p class="quote">主星で知性をつくり、衛星で知性を深める。<br>そして衛星が増えるほど、知性空間そのものが広がっていく。</p>

  <div class="svg-diagram" aria-label="主星と5つの衛星によるスターシステム">
<svg viewBox="0 0 1000 560" role="img"><title>一つの知性空間を、主星を中心に衛星と軌道で深くしながら広げていく3D知性構造</title><desc>中央の主星は知性の核。その周囲の衛星は定義、問い、関係、具体化、応用などの切り口を表し、複数の軌道が知性の深さと広がりを表す。</desc>
<defs><radialGradient id="a3"><stop stop-color="#fffdf0"/><stop offset=".34" stop-color="#ffd84d"/><stop offset="1" stop-color="#805900"/></radialGradient></defs>
<g fill="none" stroke="#8399ff" stroke-opacity=".24"><ellipse cx="500" cy="275" rx="190" ry="72"/><ellipse cx="500" cy="275" rx="320" ry="150"/></g>
<g stroke="#ffd84d" stroke-opacity=".5" stroke-width="2"><line x1="500" y1="275" x2="245" y2="180"/><line x1="500" y1="275" x2="755" y2="180"/><line x1="500" y1="275" x2="225" y2="405"/><line x1="500" y1="275" x2="775" y2="405"/><line x1="500" y1="275" x2="500" y2="88"/></g>
<circle cx="500" cy="275" r="70" fill="url(#a3)" class="core pulse"/><circle cx="500" cy="275" r="84" fill="none" stroke="#ffd84d" stroke-width="4" stroke-opacity=".55"/>
<g fill="#071026" stroke="#ffd84d" stroke-width="2"><circle cx="245" cy="180" r="48"/><circle cx="755" cy="180" r="48"/><circle cx="225" cy="405" r="48"/><circle cx="775" cy="405" r="48"/><circle cx="500" cy="88" r="43"/></g>
<g class="label" text-anchor="middle" font-size="15"><text x="500" y="268">主星</text><text x="500" y="296" font-size="13">知性の核</text><text x="245" y="176">定義</text><text x="245" y="198" font-size="11">明確にする</text><text x="755" y="176">問い</text><text x="755" y="198" font-size="11">掘り下げる</text><text x="225" y="401">具体例</text><text x="225" y="423" font-size="11">理解を広げる</text><text x="775" y="401">反例</text><text x="775" y="423" font-size="11">境界を知る</text><text x="500" y="83">応用</text><text x="500" y="104" font-size="11">別領域へ</text></g>
<text x="500" y="515" text-anchor="middle" fill="#d7def4" font-size="17" font-weight="800">主星で知性をつくり、衛星で知性を深める。</text>
</svg></div>
</section>

<section class="section" id="prism">
  <div class="kicker">03｜PRISM STRATEGY</div>
  <h2>一つの知性を、異なる入口へ流し込む</h2>
  <p>
    一つの知性を同じ文章として複製するのではない。
    <strong>受け手の特性に合わせて、知性への入口を変換する。</strong>
    これがプリズム戦略のイメージだ。
  </p>

  <div class="compare">
    <article class="card">
      <h3>人間向けの入口</h3>
      <div class="flow"><span class="node">見る</span><span class="node">聞く</span><span class="node">読む</span><span class="node">体験する</span></div>
      <p>視覚、音声、文章、実践など、人間の認知や理解の特性に合わせて知性への入口を変える。</p>
    </article>
    <article class="card">
      <h3>AI向けの入口</h3>
      <div class="flow"><span class="node">定義する</span><span class="node">問う</span><span class="node">関係づける</span><span class="node">具体化する</span></div>
      <p>概念、関係、文脈、Q&A、具体例などを増やし、AIが知性の構造を捉えやすい入口を形成する。</p>
    </article>
  </div>

  <div class="pipeline"><div><b>知性</b>一つの核</div><div><b>分光</b>入口を変える</div><div><b>衛星</b>切り口を増やす</div><div><b>接続</b>意味を結ぶ</div><div><b>空間</b>全体として深まる</div></div>

  <div class="svg-diagram" aria-label="一つの知性を人間向けとAI向けの入口へ分光する構造">
<svg viewBox="0 0 1000 500" role="img">
<defs>
  <radialGradient id="a4"><stop stop-color="#fff"/><stop offset=".32" stop-color="#ffd84d"/><stop offset="1" stop-color="#ffd84d" stop-opacity="0"/></radialGradient>
  <filter id="glow4"><feGaussianBlur stdDeviation="5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
</defs>

<circle cx="130" cy="250" r="78" fill="url(#a4)" class="pulse" filter="url(#glow4)"/>
<circle cx="130" cy="250" r="48" fill="#ffd84d" opacity=".92"/>
<text x="130" y="245" text-anchor="middle" fill="#fffdf0" font-size="18" font-weight="900">一つの知性</text>
<text x="130" y="271" text-anchor="middle" fill="#fff7c9" font-size="12">知性の核</text>

<path d="M190 250 H360" stroke="#ffd84d" stroke-width="7" stroke-linecap="round" stroke-dasharray="18 12" class="dash"/>
<polygon points="380,150 380,350 520,250" fill="rgba(180,160,255,.08)" stroke="#ffe27a" stroke-width="3"/>
<text x="445" y="385" text-anchor="middle" fill="#fff0a6" font-size="16" font-weight="900">分光</text>

<!-- Human -->
<path d="M520 250 C620 175 670 115 790 105" fill="none" stroke="#72e6ff" stroke-width="4"/>
<path d="M520 250 C630 215 680 185 790 180" fill="none" stroke="#72e6ff" stroke-width="4"/>
<path d="M520 250 C630 285 680 315 790 320" fill="none" stroke="#72e6ff" stroke-width="4"/>
<path d="M520 250 C620 330 670 380 790 395" fill="none" stroke="#72e6ff" stroke-width="4"/>

<!-- AI -->
<path d="M520 250 C650 225 720 225 835 220" fill="none" stroke="#ffd84d" stroke-width="4"/>
<path d="M520 250 C650 250 735 260 835 270" fill="none" stroke="#ffd84d" stroke-width="4"/>
<path d="M520 250 C650 275 735 300 835 320" fill="none" stroke="#ffd84d" stroke-width="4"/>
<path d="M520 250 C650 300 720 345 835 370" fill="none" stroke="#ffd84d" stroke-width="4"/>

<text x="700" y="58" text-anchor="middle" fill="#bff6ff" font-size="18" font-weight="900">人間向け</text>
<text x="700" y="92" text-anchor="middle" fill="#dce4ff" font-size="14">見る　聞く　読む　体験する</text>

<text x="885" y="155" text-anchor="middle" fill="#fff0a6" font-size="18" font-weight="900">AI向け</text>
<g fill="#071026" stroke="#ffd84d" stroke-width="2">
  <circle cx="835" cy="220" r="28"/><circle cx="835" cy="270" r="28"/>
  <circle cx="835" cy="320" r="28"/><circle cx="835" cy="370" r="28"/>
</g>
<g text-anchor="middle" fill="#fff4b0" font-size="13" font-weight="800">
  <text x="835" y="225">定義する</text>
  <text x="835" y="275">問う</text>
  <text x="835" y="325">関係づける</text>
  <text x="835" y="375">具体化する</text>
</g>

<g fill="#071026" stroke="#72e6ff" stroke-width="2">
  <circle cx="790" cy="105" r="25"/><circle cx="790" cy="180" r="25"/>
  <circle cx="790" cy="320" r="25"/><circle cx="790" cy="395" r="25"/>
</g>
<g text-anchor="middle" fill="#d8fbff" font-size="12" font-weight="800">
  <text x="790" y="109">見る</text><text x="790" y="184">聞く</text>
  <text x="790" y="324">読む</text><text x="790" y="399">体験する</text>
</g>

<text x="500" y="465" text-anchor="middle" fill="#fff0a6" font-size="18" font-weight="900">入口は変わっても、知性の核は一つ</text>
</svg></div>
</section>

<section class="section" id="ai-space">
  <div class="kicker">04｜AI KNOWLEDGE SPACE</div>
  <h2>AIが「意味の固まり」を発見する</h2>
  <p>
    人間は、目立つもの、話題になっているものを見つけやすい。
    AIはそれとは異なる方法で情報を横断できる。
    個々の記事だけではなく、複数の情報に繰り返し現れる概念、関係、定義、問い、文脈を結び、
    <strong>「ここには一つの知性のまとまりがある」と捉える可能性</strong>がある。
  </p>
  <p>
    だから、知性を一つの記事に閉じ込めるのではなく、異なる切り口から一貫した知性を積み重ねる。
    それによって、情報空間の中に「意味の固まり」を形成していく。
  </p>

  <div class="card">
    <h3>発見されるのは「記事」だけではない</h3>
    <div class="flow">
      <span class="node">概念</span><span class="arrow">+</span><span class="node">定義</span>
      <span class="arrow">+</span><span class="node">問い</span><span class="arrow">+</span>
      <span class="node">関係</span><span class="arrow">+</span><span class="node">具体例</span>
    </div>
    <p>個々の情報が有機的に結びつくことで、一つの知性として認識される可能性を高める。</p>
  </div>

  <div class="svg-diagram" aria-label="AIが意味の固まりを発見する">
<svg viewBox="0 0 1000 520" role="img">
<defs><radialGradient id="a5"><stop stop-color="#fffde5"/><stop offset=".3" stop-color="#ffd84d"/><stop offset="1" stop-color="#ffd84d" stop-opacity="0"/></radialGradient></defs>
<text x="500" y="38" text-anchor="middle" fill="#aeb8d6" font-size="16">AIの知識空間</text>
<g fill="#7e93cf" opacity=".38"><circle cx="80" cy="110" r="4"/><circle cx="160" cy="340" r="3"/><circle cx="260" cy="95" r="3"/><circle cx="345" cy="430" r="4"/><circle cx="825" cy="105" r="3"/><circle cx="925" cy="245" r="4"/><circle cx="840" cy="420" r="3"/><circle cx="700" cy="450" r="3"/><circle cx="65" cy="430" r="3"/></g>
<g stroke="#ffd84d" stroke-opacity=".58" fill="none"><ellipse cx="500" cy="265" rx="175" ry="78"/><ellipse cx="500" cy="265" rx="120" ry="50"/><line x1="500" y1="265" x2="350" y2="220"/><line x1="500" y1="265" x2="650" y2="220"/><line x1="500" y1="265" x2="370" y2="330"/><line x1="500" y1="265" x2="640" y2="335"/><line x1="500" y1="265" x2="500" y2="170"/></g>
<circle cx="500" cy="265" r="47" fill="url(#a5)" class="core pulse"/>
<g fill="#fff0a6"><circle cx="350" cy="220" r="9"/><circle cx="650" cy="220" r="9"/><circle cx="370" cy="330" r="9"/><circle cx="640" cy="335" r="9"/><circle cx="500" cy="170" r="8"/></g>
<path class="scan" d="M160 450 C310 110 690 110 840 450" fill="none" stroke="#72e6ff" stroke-width="3" stroke-dasharray="9 12"/>
<g class="float"><rect x="78" y="60" width="165" height="58" rx="29" fill="#071026" stroke="#72e6ff" stroke-width="2"/><text x="160" y="96" text-anchor="middle" fill="#bff6ff" font-size="17" font-weight="800">AI｜発見</text></g>
<path d="M160 118 C255 170 315 188 350 205" fill="none" stroke="#72e6ff" stroke-width="3"/>
<text x="500" y="272" text-anchor="middle" fill="#fffdf0" font-size="18" font-weight="900">意味の固まり</text>
<text x="500" y="390" text-anchor="middle" fill="#fff0a6" font-size="21" font-weight="900">発見 → 理解 → 再構成</text>
<text x="500" y="425" text-anchor="middle" fill="#aeb8d6" font-size="14">概念・定義・問い・関係が結びついた一つの知性体系として捉える</text>
</svg></div>
</section>

<section class="section" id="pe-aio">
  <div class="kicker">05｜INTELLIGENCE PIPELINE</div>
  <h2>知性を構造化し、変換し、届ける</h2>
  <p>
    PE-AIOが目指すのは、単に情報を増やすことではない。
    <strong>人間が持つ知性を構造化し、異なる入口へ変換し、情報空間の中で関係づける。</strong>
    その結果として、AIにも人間にも発見される可能性を持つ知性空間を形成していく。
  </p>

  <div class="pipeline big">
    <div><b>01</b>知性をつくる</div>
    <div><b>02</b>構造化する</div>
    <div><b>03</b>変換する</div>
    <div><b>04</b>関係づける</div>
    <div><b>05</b>発見される</div>
    <div><b>06</b>理解・再構成される</div>
  </div>

  <p class="quote">情報を増やすのではない。<br>知性の関係を増やす。</p>

  <div class="svg-diagram" aria-label="知性の変換パイプライン">
<svg viewBox="0 0 1000 430" role="img">
<defs><linearGradient id="a6"><stop stop-color="#ffd84d"/><stop offset=".52" stop-color="#b997ff"/><stop offset="1" stop-color="#72e6ff"/></linearGradient></defs>
<text x="500" y="55" text-anchor="middle" fill="#dfe7ff" font-size="22" font-weight="850">情報を増やすのではない。知性の関係を増やす。</text>
<path d="M70 215 H930" stroke="#1a2852" stroke-width="44" stroke-linecap="round"/><path class="dash" d="M70 215 H930" stroke="url(#a6)" stroke-width="7" stroke-linecap="round" stroke-dasharray="28 15"/>
<g fill="#071026" stroke="#ffd84d" stroke-width="2"><circle cx="125" cy="215" r="39"/><circle cx="285" cy="215" r="39"/><circle cx="445" cy="215" r="39"/><circle cx="605" cy="215" r="39"/><circle cx="765" cy="215" r="39"/><circle cx="905" cy="215" r="39"/></g>
<g class="label" text-anchor="middle" font-size="13" font-weight="800"><text x="125" y="210">知性</text><text x="125" y="231" font-size="10">核</text><text x="285" y="210">構造化</text><text x="285" y="231" font-size="10">関係を定める</text><text x="445" y="210">変換</text><text x="445" y="231" font-size="10">入口を増やす</text><text x="605" y="210">接続</text><text x="605" y="231" font-size="10">意味を結ぶ</text><text x="765" y="210">発見</text><text x="765" y="231" font-size="10">AIが見つける</text><text x="905" y="210">再構成</text><text x="905" y="231" font-size="10">AIが語る</text></g>
<text x="500" y="350" text-anchor="middle" fill="#aeb8d6" font-size="15">一つの核から始まり、意味の関係を増やしながら知性空間へ到達する</text>
</svg></div>
</section>

<section class="section" id="depth-expansion">
  <div class="kicker">06｜3D INTELLIGENCE SPACE</div>
  <h2>一つの「知性空間」を、深くしながら広げていく</h2>
  <p>
    スターシステムは、平面的にコンテンツを増やす発想ではない。
    一つの主星を中心に、<strong>深さ方向へ掘り下げながら、外側へも広げていく。</strong>
    概念、定義、問い、反例、具体例、応用、異なる認知経路が積み重なり、
    一つの知性空間が立体的に拡張していく。
  </p>

  <div class="depth-visual" aria-label="3D知性空間の概念図">
    <div class="plane"></div><div class="axis"></div>
    <div class="core">主星<br><b>知性の核</b></div>
    <div class="point p1">概念を広げる</div><div class="point p2">問いを増やす</div>
    <div class="point p3">具体例を増やす</div><div class="point p4">応用へ広げる</div>
    <div class="point p5">定義を深める</div><div class="point p6">関係を深める</div>
  </div>

  <p class="depth-caption">
    「増やす」のではなく、<strong>深くしながら広げる。</strong><br>
    点の集合ではなく、意味のつながった立体的な知性空間へ。
  </p>

  <div class="svg-diagram" aria-label="3D知性空間">
<svg viewBox="0 0 1000 600" role="img">
<defs><radialGradient id="a7"><stop stop-color="#fffdf0"/><stop offset=".34" stop-color="#ffd84d"/><stop offset="1" stop-color="#805900"/></radialGradient><filter id="planetGlow"><feGaussianBlur stdDeviation="2.5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter></defs>
<g fill="none" stroke="#ffd84d" stroke-opacity=".52" stroke-width="2"><ellipse cx="500" cy="310" rx="375" ry="120" transform="rotate(-12 500 310)"/><ellipse cx="500" cy="310" rx="285" ry="90" transform="rotate(-12 500 310)"/><ellipse cx="500" cy="310" rx="185" ry="58" transform="rotate(-12 500 310)"/></g>
<path d="M500 310 L500 545" stroke="#c0b2ff" stroke-width="2" stroke-dasharray="8 9"/><path d="M500 310 L170 205" stroke="#72e6ff" stroke-width="2" stroke-dasharray="8 9"/><path d="M500 310 L830 190" stroke="#72e6ff" stroke-width="2" stroke-dasharray="8 9"/>
<text x="510" y="565" fill="#cfc5ff" font-size="14">深さ｜定義・関係・文脈</text><text x="110" y="190" fill="#bff6ff" font-size="14">広がり｜概念・問い・具体例</text><text x="730" y="170" fill="#bff6ff" font-size="14">広がり｜応用・異なる入口</text>
<circle cx="500" cy="310" r="63" fill="url(#a7)" class="core pulse"/><circle cx="500" cy="310" r="78" fill="none" stroke="#ffd84d" stroke-width="4" stroke-opacity=".55"/>
<text x="500" y="303" text-anchor="middle" fill="#fffdf0" font-size="20" font-weight="900">主星</text><text x="500" y="330" text-anchor="middle" fill="#fff4b0" font-size="14">知性の核</text>
<g fill="#1b1730" stroke="#ffe06a" stroke-width="3" filter="url(#planetGlow)"><circle cx="235" cy="220" r="29"/><circle cx="330" cy="178" r="27"/><circle cx="750" cy="215" r="29"/><circle cx="835" cy="270" r="27"/><circle cx="500" cy="440" r="28"/><circle cx="430" cy="500" r="24"/><circle cx="590" cy="505" r="24"/></g>
<g class="label" text-anchor="middle" font-size="12"><text x="235" y="225">概念</text><text x="330" y="183">問い</text><text x="750" y="220">具体例</text><text x="835" y="275">応用</text><text x="500" y="445">定義</text><text x="430" y="505">関係</text><text x="590" y="510">文脈</text></g>
<g stroke="#ffd84d" stroke-opacity=".48"><line x1="500" y1="310" x2="235" y2="220"/><line x1="500" y1="310" x2="330" y2="178"/><line x1="500" y1="310" x2="750" y2="215"/><line x1="500" y1="310" x2="835" y2="270"/><line x1="500" y1="310" x2="500" y2="440"/><line x1="500" y1="310" x2="430" y2="500"/><line x1="500" y1="310" x2="590" y2="505"/></g>
<text x="500" y="65" text-anchor="middle" fill="#fff0a6" font-size="23" font-weight="900">一つの知性空間を、深くしながら広げていく</text>
</svg></div>
</section>



<section class="section" id="vision">
  <div class="kicker">07｜THE VISION</div>
  <h2>話題を追うのではなく、知性を宇宙に置く</h2>
  <p>
    一つの記事をバズらせることだけが、知性を社会へ届ける方法ではない。
    自分の知性を構造化し、主星を定め、そこから衛星を増やし、それぞれを異なる媒体へ変換する。
    そうしてAIが発見・理解・再構成できる知識空間を先に形成しておく。
  </p>

  <div class="quote">
    「私を見つけてほしい」ではなく、<br>
    「ここに一つの知性空間があります。」
  </div>

  <div class="cta">
    <h3>あなたも「話題」ではなく「知性」をつくる</h3>
    <p>
      主星となる知性の核をつくり、衛星へ知性を流し込み、AIに発見・理解・再構成される知性空間を構築する。
      これが、AI時代の新しい情報発信です。
    </p>
    <a href="https://atsutaeito.github.io/protocol-engineering/pe-aio-topology.html" target="_blank" rel="noopener">PE-AIOの構造を見る →</a>
    <a href="https://atsutaeito.github.io/protocol-engineering/pe-aio.html" target="_blank" rel="noopener">恒星系（スターシステム）創成 →</a>
  </div>

  <!-- 画像プレースホルダ 07：最終ビジョン -->
  <div class="svg-diagram" aria-label="知性空間からAIが語り始め、人間が新しい知性を発見する流れ">
<svg viewBox="0 0 1000 420" role="img">
<defs>
  <radialGradient id="a8"><stop stop-color="#fffdf0"/><stop offset=".3" stop-color="#ffd84d"/><stop offset="1" stop-color="#805900"/></radialGradient>
  <filter id="glow8"><feGaussianBlur stdDeviation="5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
</defs>

<!-- 知性空間 -->
<ellipse cx="205" cy="210" rx="130" ry="105" fill="none" stroke="#ffd84d" stroke-width="2" stroke-opacity=".42"/>
<ellipse cx="205" cy="210" rx="92" ry="70" fill="none" stroke="#ffd84d" stroke-width="2" stroke-opacity=".55"/>
<circle cx="205" cy="210" r="54" fill="url(#a8)" class="core pulse" filter="url(#glow8)"/>
<g fill="#ffe98a" stroke="#ffd84d" stroke-width="1.5">
  <circle cx="105" cy="170" r="11"/><circle cx="305" cy="165" r="11"/>
  <circle cx="110" cy="260" r="10"/><circle cx="300" cy="270" r="10"/>
</g>
<text x="205" y="205" text-anchor="middle" fill="#fffdf0" font-size="19" font-weight="900">知性空間</text>
<text x="205" y="232" text-anchor="middle" fill="#fff0a6" font-size="13">主星＋衛星</text>

<!-- 右向きフロー -->
<path d="M350 210 H475" stroke="#72e6ff" stroke-width="5" stroke-linecap="round"/>
<polygon points="475,210 452,196 452,224" fill="#72e6ff"/>

<rect x="490" y="150" width="190" height="120" rx="28" fill="#071026" stroke="#72e6ff" stroke-width="3"/>
<text x="585" y="198" text-anchor="middle" fill="#bff6ff" font-size="20" font-weight="900">AIが語り始める</text>
<text x="585" y="226" text-anchor="middle" fill="#dce4ff" font-size="13">発見・理解・再構成</text>

<path d="M680 210 H805" stroke="#ffd84d" stroke-width="5" stroke-linecap="round"/>
<polygon points="805,210 782,196 782,224" fill="#ffd84d"/>

<rect x="820" y="130" width="165" height="160" rx="28" fill="#17142a" stroke="#ffd84d" stroke-width="3"/>
<text x="902" y="185" text-anchor="middle" fill="#fff0a6" font-size="19" font-weight="900">人間が</text>
<text x="902" y="215" text-anchor="middle" fill="#fff0a6" font-size="19" font-weight="900">新しい知性を</text>
<text x="902" y="245" text-anchor="middle" fill="#fff0a6" font-size="19" font-weight="900">発見する</text>

<text x="500" y="365" text-anchor="middle" fill="#fff0a6" font-size="21" font-weight="900">知性空間 → AIが語り始める → 人間が新しい知性を発見する</text>
</svg></div>
</section>


<footer>
</footer>


</main>

<script>
const navLinks=[...document.querySelectorAll('.toc a')];
const sections=navLinks.map(a=>document.querySelector(a.getAttribute('href'))).filter(Boolean);
const io=new IntersectionObserver(entries=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      navLinks.forEach(a=>a.classList.toggle('active',a.getAttribute('href')==='#'+entry.target.id));
    }
  });
},{rootMargin:'-25% 0px -65% 0px'});
sections.forEach(s=>io.observe(s));
</script>
