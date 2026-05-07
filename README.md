<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ali Aleddi – GitHub README</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Rajdhani:wght@400;600;700&family=Fira+Code:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#07090f;--bg2:#0a0d18;--bg3:#0d1120;--bg4:#111827;
  --border:#182030;--b2:#1e2d45;
  --cyan:#00e5ff;--green:#00e676;--purple:#d500f9;
  --yellow:#ffd740;--red:#ff1744;
  --vscode:#007acc;--vs:#7b2fe0;
  --nvidia:#76b900;--ms:#00a4ef;
  --text:#9fb0c0;--white:#e8edf3;--muted:#3d5268;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);font-family:'Rajdhani',sans-serif;min-height:100vh;padding:1.5rem;overflow-x:hidden}

/* ── PARTICLES ── */
#pts{position:fixed;inset:0;pointer-events:none;z-index:0;overflow:hidden}
.pt{position:absolute;border-radius:50%;opacity:0;animation:rise linear infinite}
@keyframes rise{0%{opacity:0;transform:translateY(105vh) scale(.5)}8%{opacity:.6}88%{opacity:.2}100%{opacity:0;transform:translateY(-8vh) translateX(25px) scale(1)}}
body::before{content:'';position:fixed;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 2px,rgba(0,229,255,.007) 2px,rgba(0,229,255,.007) 4px);pointer-events:none;z-index:1}

/* ── CARD ── */
.wrap{position:relative;z-index:2;max-width:920px;margin:0 auto}
.card{background:var(--bg2);border:1px solid var(--border);border-radius:16px;overflow:hidden;box-shadow:0 0 100px rgba(0,229,255,.03),0 0 200px rgba(213,0,249,.02)}

/* topbar */
.topbar{background:var(--bg3);border-bottom:1px solid var(--border);padding:11px 20px;display:flex;align-items:center;gap:8px}
.dot{width:12px;height:12px;border-radius:50%}
.dot.r{background:#ff5f57}.dot.y{background:#febc2e}.dot.g{background:#28c840}
.ttl{margin:0 auto;font-family:'Fira Code',monospace;font-size:12px;color:var(--muted)}

.content{padding:2.8rem 3rem 3.2rem}

/* ── SECTIONS ── */
.sec{margin-bottom:2.6rem;animation:up .7s ease both}
@keyframes up{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.sec:nth-child(1){animation-delay:.04s}.sec:nth-child(2){animation-delay:.12s}
.sec:nth-child(3){animation-delay:.2s}.sec:nth-child(4){animation-delay:.28s}
.sec:nth-child(5){animation-delay:.36s}.sec:nth-child(6){animation-delay:.44s}
.sec:nth-child(7){animation-delay:.52s}.sec:nth-child(8){animation-delay:.6s}
.sec:nth-child(9){animation-delay:.68s}

.stitle{font-size:.85rem;font-family:'Share Tech Mono',monospace;color:var(--cyan);letter-spacing:4px;text-transform:uppercase;margin-bottom:1.3rem;display:flex;align-items:center;gap:10px}
.stitle::before{content:'//';color:var(--muted);font-size:.8rem}
.stitle::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,var(--b2),transparent);margin-left:8px}

/* ── HEADER ── */
.hdr{text-align:center;margin-bottom:3rem;position:relative}
.hdr-line{display:block;width:100%;height:1px;margin-top:2.2rem;background:linear-gradient(90deg,transparent,var(--cyan),var(--purple),transparent);opacity:.35}

/* typewriter */
.tw-wrap{font-family:'Fira Code',monospace;font-size:2.7rem;font-weight:500;color:var(--white);letter-spacing:3px;margin-bottom:.7rem;min-height:3.4rem;display:flex;align-items:center;justify-content:center;gap:6px}
.tw-static{color:var(--cyan);text-shadow:0 0 22px var(--cyan)}
.tw-text{color:var(--white)}
.tw-cur{display:inline-block;width:3px;height:1.05em;background:var(--cyan);vertical-align:text-bottom;box-shadow:0 0 10px var(--cyan);flex-shrink:0}
.tw-cur.blink{animation:blink .9s step-end infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}

.tagline{font-family:'Share Tech Mono',monospace;font-size:.9rem;color:var(--green);letter-spacing:4px;text-transform:uppercase;margin-bottom:1.5rem;opacity:.9}

.badges{display:flex;flex-wrap:wrap;justify-content:center;gap:10px;margin-top:1rem}
.badge{display:flex;align-items:center;gap:7px;padding:6px 17px;border-radius:22px;font-size:13px;font-family:'Fira Code',monospace;border:1px solid;transition:all .3s;cursor:default;user-select:none}
.badge:hover{transform:translateY(-4px);box-shadow:0 0 20px currentColor}
.bc{color:var(--cyan);border-color:var(--cyan);background:rgba(0,229,255,.07)}
.bg{color:var(--green);border-color:var(--green);background:rgba(0,230,118,.07)}
.bp{color:var(--purple);border-color:var(--purple);background:rgba(213,0,249,.07)}
.by{color:var(--yellow);border-color:var(--yellow);background:rgba(255,215,64,.07)}
.bv{color:var(--vscode);border-color:var(--vscode);background:rgba(0,122,204,.1)}

/* ── ABOUT ── */
.ag{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.ai{background:var(--bg3);border:1px solid var(--border);border-radius:9px;padding:14px 18px;display:flex;align-items:flex-start;gap:13px;transition:border-color .3s,box-shadow .3s,transform .3s}
.ai:hover{border-color:var(--cyan);box-shadow:0 0 16px rgba(0,229,255,.12);transform:translateY(-2px)}
.aico{font-size:1.5rem;flex-shrink:0;line-height:1}
.albl{font-size:10.5px;color:var(--muted);font-family:'Fira Code',monospace;text-transform:uppercase;letter-spacing:1px;margin-bottom:3px}
.aval{font-size:15px;font-weight:700;color:var(--white)}

/* ── VSCODE WINDOW ── */
.vswin{background:#13141f;border:1px solid var(--vscode);border-radius:12px;overflow:hidden;transition:all .35s}
.vswin:hover{box-shadow:0 0 40px rgba(0,122,204,.3),0 0 80px rgba(0,122,204,.1);transform:translateY(-3px)}
.vstb{background:#1c1e2d;border-bottom:1px solid #252840;padding:8px 14px;display:flex;align-items:center;gap:8px}
.wdots{display:flex;gap:6px}.wdots span{width:11px;height:11px;border-radius:50%}
.wdots .r{background:#ff5f57}.wdots .y{background:#febc2e}.wdots .g{background:#28c840}
.vtab{background:#1a1c2e;border:1px solid #2d3050;border-bottom:none;padding:5px 15px;border-radius:5px 5px 0 0;font-family:'Fira Code',monospace;font-size:12px;color:#7080a0;display:flex;align-items:center;gap:7px;margin-left:10px}
.pydot{width:8px;height:8px;border-radius:50%;background:var(--vscode)}
.vextrow{display:flex;gap:8px;margin-left:auto}
.vext{font-family:'Fira Code',monospace;font-size:11px;color:var(--vscode);background:rgba(0,122,204,.12);border:1px solid rgba(0,122,204,.28);border-radius:4px;padding:2px 8px}
.vbody{display:flex}
.lnums{padding:16px 10px;background:#10111e;border-right:1px solid #1e2038;font-family:'Fira Code',monospace;font-size:13px;color:#2d3f58;line-height:1.95;text-align:right;min-width:36px;user-select:none}
.carea{padding:14px 20px;flex:1;font-family:'Fira Code',monospace;font-size:13.5px;line-height:1.95}
.kw{color:#c792ea}.fn{color:#82aaff}.st{color:#c3e88d}.cm{color:#445568;font-style:italic}
.cl2{color:#ffcb6b}.op{color:#89ddff}.v{color:#aac8d8}
.ln{display:block;min-height:1.95em;border-radius:3px;padding:0 2px}.ln:hover{background:rgba(0,122,204,.08)}
.vsbar{background:#007acc;padding:3px 14px;display:flex;align-items:center;gap:16px}
.sbi{font-family:'Fira Code',monospace;font-size:11px;color:rgba(255,255,255,.85)}

/* ── TECH GRID — 8 cards ── */
.tgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
@media(max-width:700px){.tgrid{grid-template-columns:repeat(2,1fr)}}
.tc{background:var(--bg3);border:1px solid var(--border);border-radius:11px;padding:20px 10px;text-align:center;cursor:default;transition:all .3s;position:relative;overflow:hidden}
.tc:hover{transform:translateY(-6px)}
/* per-card glow */
.tc.py:hover {border-color:#3776ab;box-shadow:0 0 24px rgba(55,118,171,.55)}
.tc.vsc:hover{border-color:#007acc;box-shadow:0 0 30px rgba(0,122,204,.65);background:rgba(0,122,204,.05)}
.tc.vs:hover {border-color:#7b2fe0;box-shadow:0 0 24px rgba(123,47,224,.6)}
.tc.kl:hover {border-color:var(--cyan);box-shadow:0 0 24px rgba(0,229,255,.55)}
.tc.win:hover{border-color:#00adef;box-shadow:0 0 24px rgba(0,173,239,.55)}
.tc.lx:hover {border-color:#e8c200;box-shadow:0 0 24px rgba(232,194,0,.45)}
.tc.git:hover{border-color:#f05032;box-shadow:0 0 24px rgba(240,80,50,.55)}
.tc.gh:hover {border-color:#ccc;box-shadow:0 0 24px rgba(200,200,200,.3)}

.tico{font-size:2.4rem;margin-bottom:10px;display:block;transition:filter .3s,transform .35s}
.tc:hover .tico{transform:scale(1.25);filter:drop-shadow(0 0 10px currentColor)}
.tc.py  .tico{color:#3776ab}.tc.vsc .tico{color:#007acc}
.tc.vs  .tico{color:#7b2fe0}.tc.kl  .tico{color:var(--cyan)}
.tc.win .tico{color:#00adef}.tc.lx  .tico{color:#e8c200}
.tc.git .tico{color:#f05032}.tc.gh  .tico{color:#aaa}

.tname{font-size:13px;font-weight:700;color:var(--white);margin-bottom:2px}
.tdesc{font-size:10.5px;color:var(--muted);font-family:'Fira Code',monospace}
.favchip{display:inline-block;margin-top:6px;background:rgba(0,122,204,.18);border:1px solid rgba(0,122,204,.45);color:var(--vscode);font-size:9px;font-family:'Fira Code',monospace;padding:1px 8px;border-radius:3px;letter-spacing:1px;text-transform:uppercase}

/* os-chip for Kali */
.oschip{display:inline-block;margin-top:6px;background:rgba(0,229,255,.1);border:1px solid rgba(0,229,255,.35);color:var(--cyan);font-size:9px;font-family:'Fira Code',monospace;padding:1px 8px;border-radius:3px;letter-spacing:1px;text-transform:uppercase}
.win-oschip{display:inline-block;margin-top:6px;background:rgba(0,173,239,.1);border:1px solid rgba(0,173,239,.35);color:#00adef;font-size:9px;font-family:'Fira Code',monospace;padding:1px 8px;border-radius:3px;letter-spacing:1px;text-transform:uppercase}

/* ── COMPANIES ── */
.cgrid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.cc{background:var(--bg3);border:1px solid var(--border);border-radius:16px;padding:24px 22px;display:flex;align-items:center;gap:20px;transition:all .35s;cursor:default;position:relative;overflow:hidden}
.cc::before{content:'';position:absolute;inset:0;opacity:0;transition:opacity .35s;border-radius:16px;pointer-events:none}
.cc:hover{transform:translateY(-5px)}

/* NVIDIA */
.cc.nv{border-color:rgba(118,185,0,.2)}
.cc.nv::before{background:radial-gradient(ellipse at 25% 50%,rgba(118,185,0,.12),transparent 65%)}
.cc.nv:hover{border-color:var(--nvidia);box-shadow:0 0 35px rgba(118,185,0,.4),0 0 70px rgba(118,185,0,.12)}
.cc.nv:hover::before{opacity:1}

/* MICROSOFT */
.cc.ms2{border-color:rgba(0,164,239,.2)}
.cc.ms2::before{background:radial-gradient(ellipse at 25% 50%,rgba(0,164,239,.12),transparent 65%)}
.cc.ms2:hover{border-color:var(--ms);box-shadow:0 0 35px rgba(0,164,239,.4),0 0 70px rgba(0,164,239,.12)}
.cc.ms2:hover::before{opacity:1}

.clogo{flex-shrink:0;transition:transform .35s,filter .35s;z-index:1}
.cc:hover .clogo{transform:scale(1.1)}
.cc.nv:hover .clogo{filter:drop-shadow(0 0 14px #76b900)}
.cc.ms2:hover .clogo{filter:drop-shadow(0 0 14px #00a4ef)}

/* Microsoft 4-square */
.msq{display:grid;grid-template-columns:1fr 1fr;gap:6px;width:56px;height:56px}
.msq div{border-radius:3px;transition:filter .3s}
.msq .mr{background:#f25022}.msq .mg{background:#7fba00}
.msq .mb{background:#00a4ef}.msq .my{background:#ffb900}
.cc.ms2:hover .msq div{filter:brightness(1.25)}

.cinfo{flex:1;z-index:1}
.cname{font-size:1.4rem;font-weight:700;font-family:'Rajdhani',sans-serif;letter-spacing:1px;margin-bottom:4px;transition:text-shadow .3s}
.cc.nv .cname{color:#8fd43a}
.cc.ms2 .cname{color:#4ec9f5}
.cc.nv:hover .cname{text-shadow:0 0 16px #76b900}
.cc.ms2:hover .cname{text-shadow:0 0 16px #00a4ef}
.csub{font-size:12px;color:var(--muted);font-family:'Fira Code',monospace;margin-bottom:10px}
.ctags{display:flex;flex-wrap:wrap;gap:6px}
.ctag{font-size:10.5px;font-family:'Fira Code',monospace;padding:3px 10px;border-radius:5px;border:1px solid;transition:all .3s;cursor:default}
.nv .ctag{color:#76b900;border-color:rgba(118,185,0,.35);background:rgba(118,185,0,.07)}
.nv .ctag:hover{background:rgba(118,185,0,.18);box-shadow:0 0 8px rgba(118,185,0,.4)}
.ms2 .ctag{color:#00a4ef;border-color:rgba(0,164,239,.35);background:rgba(0,164,239,.07)}
.ms2 .ctag:hover{background:rgba(0,164,239,.18);box-shadow:0 0 8px rgba(0,164,239,.4)}

/* ── STATS ── */
.srow{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.sbox{background:var(--bg3);border:1px solid var(--border);border-radius:11px;padding:22px 16px;text-align:center;transition:all .3s;cursor:default}
.sbox:hover{border-color:var(--green);box-shadow:0 0 20px rgba(0,230,118,.18);transform:translateY(-3px)}
.snum{font-family:'Share Tech Mono',monospace;font-size:2.2rem;color:var(--green);text-shadow:0 0 18px rgba(0,230,118,.5)}
.slbl{font-size:11px;color:var(--muted);margin-top:5px;font-family:'Fira Code',monospace;text-transform:uppercase;letter-spacing:1px}

/* ── LEARNING ── */
.llist{display:flex;flex-direction:column;gap:10px}
.li{background:var(--bg3);border:1px solid var(--border);border-left:3px solid var(--purple);border-radius:0 9px 9px 0;padding:13px 17px;font-size:14px;color:var(--text);font-family:'Fira Code',monospace;transition:all .3s;display:flex;align-items:center;gap:11px}
.li:hover{border-left-color:var(--cyan);background:rgba(0,229,255,.04);color:var(--white);transform:translateX(4px)}
.arr{color:var(--cyan);flex-shrink:0;transition:transform .3s}
.li:hover .arr{transform:translateX(3px)}
.pb{height:3px;border-radius:2px;background:var(--border);flex:1;overflow:hidden}
.pf{height:100%;border-radius:2px;background:linear-gradient(90deg,var(--cyan),var(--purple))}

/* ── FOOTER ── */
.footer{text-align:center;margin-top:2.5rem;padding-top:2rem;border-top:1px solid var(--border);font-family:'Share Tech Mono',monospace;font-size:12px;color:var(--muted);letter-spacing:2px}
.footer .heart{color:var(--red)}
</style>
</head>
<body>

<div id="pts"></div>

<div class="wrap">
<div class="card">

  <div class="topbar">
    <div class="dot r"></div><div class="dot y"></div><div class="dot g"></div>
    <span class="ttl">ali-aleddi / ali-aleddi / README.md</span>
  </div>

  <div class="content">

    <!-- ══ HEADER ══ -->
    <div class="sec hdr">
      <div class="tw-wrap">
        <span class="tw-static">&lt;</span>
        <span class="tw-text" id="tw"></span>
        <span class="tw-cur blink" id="cur"></span>
        <span class="tw-static">/&gt;</span>
      </div>
      <div class="tagline">Python Developer &amp; Security Enthusiast</div>
      <div class="badges">
        <div class="badge bc">🐍 Python</div>
        <div class="badge bv">⚡ VS Code</div>
        <div class="badge bp" style="color:#7b2fe0;border-color:#7b2fe0;background:rgba(123,47,224,.1)">🛠 Visual Studio</div>
        <div class="badge bg">💀 Kali Linux</div>
        <div class="badge bv" style="color:#00adef;border-color:#00adef;background:rgba(0,173,239,.1)">🪟 Windows</div>
        <div class="badge by">🇸🇾 Syria</div>
      </div>
      <span class="hdr-line"></span>
    </div>

    <!-- ══ ABOUT ══ -->
    <div class="sec">
      <div class="stitle">About Me</div>
      <div class="ag">
        <div class="ai"><div class="aico">🎯</div><div><div class="albl">Focus</div><div class="aval">Python Development</div></div></div>
        <div class="ai"><div class="aico">🔐</div><div><div class="albl">Passion</div><div class="aval">Cybersecurity</div></div></div>
        <div class="ai"><div class="aico">🌍</div><div><div class="albl">Location</div><div class="aval">Syria 🇸🇾</div></div></div>
        <div class="ai"><div class="aico">🚀</div><div><div class="albl">Status</div><div class="aval">Always Learning</div></div></div>
      </div>
    </div>

    <!-- ══ VSCODE WINDOW ══ -->
    <div class="sec">
      <div class="stitle">Primary Editor</div>
      <div class="vswin">
        <div class="vstb">
          <div class="wdots"><span class="r"></span><span class="y"></span><span class="g"></span></div>
          <div class="vtab"><span class="pydot"></span>main.py</div>
          <div class="vextrow">
            <span class="vext">Python 3.x</span>
            <span class="vext">⚡ VS Code</span>
          </div>
        </div>
        <div class="vbody">
          <div class="lnums">1<br>2<br>3<br>4<br>5<br>6<br>7<br>8<br>9<br>10<br>11<br>12<br>13</div>
          <div class="carea">
            <span class="ln"><span class="cm"># Welcome to Ali Aleddi's workspace 🚀</span></span>
            <span class="ln"></span>
            <span class="ln"><span class="kw">class</span> <span class="cl2">Developer</span><span class="op">:</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="v">name</span>       <span class="op">=</span> <span class="st">"Ali Aleddi"</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="v">language</span>   <span class="op">=</span> <span class="st">"Python"</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="v">editor</span>     <span class="op">=</span> <span class="st">"VS Code"</span>  <span class="cm"># ⚡ favourite tool</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="v">os</span>         <span class="op">=</span> <span class="st">"Kali Linux"</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="v">location</span>   <span class="op">=</span> <span class="st">"Syria 🇸🇾"</span></span>
            <span class="ln"></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">greet</span><span class="op">(</span><span class="v">self</span><span class="op">):</span></span>
            <span class="ln">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="fn">print</span><span class="op">(</span><span class="st">f"Hello from </span><span class="op">{</span><span class="v">self</span><span class="op">.</span><span class="v">location</span><span class="op">}</span><span class="st"> 👋"</span><span class="op">)</span></span>
            <span class="ln"></span>
            <span class="ln"><span class="cl2">Developer</span><span class="op">().</span><span class="fn">greet</span><span class="op">()</span>  <span class="cm"># Hello from Syria 🇸🇾 👋</span></span>
          </div>
        </div>
        <div class="vsbar">
          <span class="sbi">⎇ main</span>
          <span class="sbi">🐍 Python 3.12</span>
          <span class="sbi">⚡ VS Code</span>
          <span class="sbi" style="margin-left:auto">Ln 13, Col 1</span>
        </div>
      </div>
    </div>

    <!-- ══ TECH STACK — 8 cards ══ -->
    <div class="sec">
      <div class="stitle">Tech Stack</div>
      <div class="tgrid">

        <div class="tc py">
          <span class="tico">🐍</span>
          <div class="tname">Python</div>
          <div class="tdesc">main language</div>
        </div>

        <div class="tc vsc">
          <span class="tico">
            <!-- VS Code SVG icon -->
            <svg width="38" height="38" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
              <mask id="m1"><rect width="100" height="100" fill="white"/><path d="M70.9 26.1L45.4 49.9 28.6 36.3 23 39.7v20.5l5.6 3.4 16.8-13.6L70.9 73.9 77 70V30l-6.1-3.9z" fill="black"/></mask>
              <path d="M77 30L55.3 50 77 70l6-3V33l-6-3z" fill="#007acc"/>
              <path d="M23 39.7L28.6 36.3 45.4 49.9 28.6 63.7 23 60.2V39.7z" fill="#007acc" opacity=".8"/>
              <path d="M70.9 26.1L45.4 49.9l25.5 23.8L77 70 55.3 50 77 30l-6.1-3.9z" fill="white" opacity=".15"/>
              <path d="M77 30l-6.1-3.9a4 4 0 00-4.1.4L23 61.5v.5l5.6 3.4.8-.5 47.6-31v-.4V30z" fill="#007acc" opacity=".6"/>
              <path d="M70.9 73.9a4 4 0 004.1.4L77 73.1V70l-6.1 3.9z" fill="#007acc" opacity=".8"/>
            </svg>
          </span>
          <div class="tname">VS Code</div>
          <div class="tdesc">code editor</div>
          <div class="favchip">★ fav</div>
        </div>

        <div class="tc vs">
          <span class="tico">
            <!-- Visual Studio SVG icon -->
            <svg width="38" height="38" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
              <defs><linearGradient id="vsg" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#b179f1"/><stop offset="100%" stop-color="#7b2fe0"/></linearGradient></defs>
              <rect width="100" height="100" rx="18" fill="url(#vsg)" opacity=".15"/>
              <!-- Infinity/VS logo approximation -->
              <path d="M15 25 L40 75 L50 55 L60 75 L85 25 L72 25 L50 62 L28 25 Z" fill="url(#vsg)"/>
              <path d="M38 25 L50 48 L62 25 L72 25 L50 68 L28 25 Z" fill="white" opacity=".2"/>
              <circle cx="78" cy="22" r="6" fill="#b179f1" opacity=".8"/>
            </svg>
          </span>
          <div class="tname">Visual Studio</div>
          <div class="tdesc">ide &amp; debugger</div>
        </div>

        <div class="tc kl">
          <span class="tico">
            <!-- Kali dragon-style SVG -->
            <svg width="38" height="38" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
              <circle cx="50" cy="50" r="46" fill="rgba(0,229,255,.08)" stroke="#00e5ff" stroke-width="1.5"/>
              <!-- Kali stylized K -->
              <path d="M30 20 L30 80 L40 80 L40 55 L62 80 L74 80 L48 52 L72 20 L60 20 L40 46 L40 20 Z" fill="#00e5ff"/>
              <!-- Glow top-right -->
              <circle cx="74" cy="22" r="5" fill="#00e5ff" opacity=".6"/>
            </svg>
          </span>
          <div class="tname">Kali Linux</div>
          <div class="tdesc">pentesting os</div>
          <div class="oschip">2nd OS</div>
        </div>

        <div class="tc win">
          <span class="tico">
            <!-- Proper Windows 11 logo SVG -->
            <svg width="38" height="38" viewBox="0 0 88 88" xmlns="http://www.w3.org/2000/svg">
              <rect x="4"  y="4"  width="37" height="37" rx="5" fill="#f25022"/>
              <rect x="47" y="4"  width="37" height="37" rx="5" fill="#7fba00"/>
              <rect x="4"  y="47" width="37" height="37" rx="5" fill="#00a4ef"/>
              <rect x="47" y="47" width="37" height="37" rx="5" fill="#ffb900"/>
            </svg>
          </span>
          <div class="tname">Windows</div>
          <div class="tdesc">main os</div>
          <div class="win-oschip">1st OS</div>
        </div>

        <div class="tc lx">
          <span class="tico">🐧</span>
          <div class="tname">Linux</div>
          <div class="tdesc">terminal &amp; tools</div>
        </div>

        <div class="tc git">
          <span class="tico">
            <!-- Git SVG -->
            <svg width="38" height="38" viewBox="0 0 92 92" xmlns="http://www.w3.org/2000/svg">
              <path fill="#f05032" d="M90.2 41.7L50.3 1.8a6.1 6.1 0 00-8.6 0l-8.6 8.6 10.9 10.9a7.3 7.3 0 019.2 9.3l10.5 10.5a7.3 7.3 0 11-4.4 4.2L49.2 34.7v25.4a7.3 7.3 0 11-6 0V34.1a7.3 7.3 0 01-4-9.6L28.5 13.8 1.8 40.5a6.1 6.1 0 000 8.6l39.9 39.9a6.1 6.1 0 008.6 0l39.9-39.9a6.1 6.1 0 000-8.6"/>
            </svg>
          </span>
          <div class="tname">Git</div>
          <div class="tdesc">version control</div>
        </div>

        <div class="tc gh">
          <span class="tico">
            <!-- GitHub Octocat simplified -->
            <svg width="38" height="38" viewBox="0 0 98 96" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M48.9 0C21.9 0 0 22 0 49.2c0 21.7 14 40.2 33.6 46.7 2.5.5 3.4-1.1 3.4-2.4v-8.4c-13.7 3-16.6-6.6-16.6-6.6-2.2-5.7-5.5-7.2-5.5-7.2-4.5-3 .3-3 .3-3 5 .4 7.6 5.1 7.6 5.1 4.4 7.6 11.6 5.4 14.4 4.1.4-3.2 1.7-5.4 3.1-6.6-11-1.2-22.5-5.5-22.5-24.4 0-5.4 1.9-9.8 5-13.2-.5-1.2-2.2-6.2.5-13 0 0 4.1-1.3 13.4 5a46.8 46.8 0 0124.4 0c9.3-6.3 13.4-5 13.4-5 2.7 6.8 1 11.8.5 13 3.1 3.4 5 7.8 5 13.2 0 18.9-11.5 23.1-22.5 24.3 1.8 1.5 3.3 4.5 3.3 9.1v13.5c0 1.3.9 2.9 3.4 2.4C84 89.4 98 70.9 98 49.2 98 22 76.1 0 48.9 0z" fill="#c0c0c0"/>
            </svg>
          </span>
          <div class="tname">GitHub</div>
          <div class="tdesc">host &amp; collab</div>
        </div>

      </div>
    </div>

    <!-- ══ POWERED BY ══ -->
    <div class="sec">
      <div class="stitle">Favourite Companies</div>
      <div class="cgrid">

        <!-- NVIDIA -->
        <div class="cc nv">
          <div class="clogo">
            <svg width="68" height="68" viewBox="0 0 120 120" xmlns="http://www.w3.org/2000/svg">
              <rect width="120" height="120" rx="16" fill="rgba(118,185,0,.1)" stroke="rgba(118,185,0,.3)" stroke-width="1.5"/>
              <!-- NVIDIA eye logo -->
              <path d="M20 38 C20 38 38 16 65 20 C65 20 65 38 50 42 C50 42 65 38 65 20 C88 26 100 46 100 60 C100 74 85 95 60 95 C35 95 20 75 20 60 C20 50 20 44 20 38Z" fill="none" stroke="#76b900" stroke-width="2" opacity=".4"/>
              <!-- N letter -->
              <path d="M22 42 L22 78 L30 78 L30 58 L46 78 L54 78 L54 42 L46 42 L46 62 L30 42 Z" fill="#76b900"/>
              <!-- VIDIA-style right accent -->
              <path d="M60 50 C72 50 82 55 87 62 C82 69 72 74 60 74 L60 68 C68 68 76 65 80 62 C76 59 68 56 60 56 Z" fill="#76b900" opacity=".8"/>
              <!-- glow dot -->
              <circle cx="93" cy="30" r="6" fill="#76b900" opacity=".4"/>
              <circle cx="93" cy="30" r="3" fill="#a3d45f"/>
            </svg>
          </div>
          <div class="cinfo nv">
            <div class="cname">NVIDIA</div>
            <div class="csub">GPU &amp; AI Computing</div>
            <div class="ctags">
              <span class="ctag">GeForce</span>
              <span class="ctag">CUDA</span>
              <span class="ctag">AI / ML</span>
              <span class="ctag">RTX</span>
            </div>
          </div>
        </div>

        <!-- MICROSOFT -->
        <div class="cc ms2">
          <div class="clogo">
            <div class="msq">
              <div class="mr"></div><div class="mg"></div>
              <div class="mb"></div><div class="my"></div>
            </div>
          </div>
          <div class="cinfo ms2">
            <div class="cname">Microsoft</div>
            <div class="csub">Software &amp; Cloud</div>
            <div class="ctags">
              <span class="ctag">Windows</span>
              <span class="ctag">VS Code</span>
              <span class="ctag">GitHub</span>
              <span class="ctag">Azure</span>
            </div>
          </div>
        </div>

      </div>
    </div>

    <!-- ══ STATS ══ -->
    <div class="sec">
      <div class="stitle">GitHub Stats</div>
      <div class="srow">
        <div class="sbox"><div class="snum">∞</div><div class="slbl">Lines of Code</div></div>
        <div class="sbox"><div class="snum">🔥</div><div class="slbl">Daily Commits</div></div>
        <div class="sbox"><div class="snum">100%</div><div class="slbl">Passion Level</div></div>
      </div>
    </div>

    <!-- ══ LEARNING ══ -->
    <div class="sec">
      <div class="stitle">Currently Exploring</div>
      <div class="llist">
        <div class="li"><span class="arr">▶</span> Python scripting &amp; automation <div class="pb"><div class="pf" style="width:70%"></div></div></div>
        <div class="li"><span class="arr">▶</span> Ethical hacking with Kali Linux <div class="pb"><div class="pf" style="width:55%"></div></div></div>
        <div class="li"><span class="arr">▶</span> Git &amp; open-source collaboration <div class="pb"><div class="pf" style="width:40%"></div></div></div>
        <div class="li"><span class="arr">▶</span> Cybersecurity fundamentals <div class="pb"><div class="pf" style="width:50%"></div></div></div>
      </div>
    </div>

    <!-- ══ FOOTER (unchanged) ══ -->
    <div class="footer">
      MADE WITH <span class="heart">♥</span> BY ALI ALEDDI &nbsp;·&nbsp; SYRIA 🇸🇾 &nbsp;·&nbsp; EST. 2026
    </div>

  </div>
</div>
</div>

<script>
/* ── Particles ── */
const pc=document.getElementById('pts');
const pcols=['#00e5ff','#00e676','#d500f9','#007acc','#76b900','#00a4ef','#ffd740','#7b2fe0'];
for(let i=0;i<50;i++){
  const p=document.createElement('div');p.className='pt';
  p.style.left=Math.random()*100+'%';
  p.style.animationDuration=(9+Math.random()*14)+'s';
  p.style.animationDelay=(Math.random()*16)+'s';
  const c=pcols[Math.floor(Math.random()*pcols.length)];
  const s=(1+Math.random()*2.5)+'px';
  p.style.cssText+=`background:${c};width:${s};height:${s};box-shadow:0 0 5px ${c}`;
  pc.appendChild(p);
}

/* ── Typewriter ── */
const phrases=['Ali Aleddi','Python Dev','Syria 🇸🇾','Security '];
let pi=0,ci=0,del=false;
const tw=document.getElementById('tw');
const cur=document.getElementById('cur');

function tick(){
  const phrase=phrases[pi];
  if(!del){
    ci++;
    tw.textContent=phrase.slice(0,ci);
    cur.classList.remove('blink');
    if(ci===phrase.length){
      del=true;
      setTimeout(tick,1600);
      return;
    }
    setTimeout(tick,90+Math.random()*40);
  } else {
    ci--;
    tw.textContent=phrase.slice(0,ci);
    if(ci===0){
      del=false;
      pi=(pi+1)%phrases.length;
      cur.classList.add('blink');
      setTimeout(tick,400);
      return;
    }
    setTimeout(tick,45);
  }
}
tick();
</script>
</body>
</html>
