<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>The Eight &#8212; ESD Competencies: understand, teach, assess, build</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;600;800&family=IBM+Plex+Mono:wght@400;600&family=IBM+Plex+Sans:ital,wght@0,400;0,500;0,600;1,400&display=swap" rel="stylesheet">

<style>
:root{
  --ink:#16211F; --ink-soft:#4A5A56; --paper:#F4F6F4; --card:#FFFFFF; --line:#D6DCD8;
  --moss:#2F5D50; --moss-tint:#E4EDE9; --slate:#3A5A78; --slate-tint:#E5EBF1;
  --amber:#B57D0E; --amber-tint:#F8EFD9; --rose:#9E3B3E; --rose-tint:#F7E4E4; --radius:3px;
}
*{box-sizing:border-box}
html,body{margin:0;padding:0}
body{background:var(--paper);color:var(--ink);font-family:"IBM Plex Sans",system-ui,-apple-system,"Segoe UI",sans-serif;font-size:16px;line-height:1.55;-webkit-font-smoothing:antialiased}
h1,h2,h3,h4{font-family:"Archivo","Arial Narrow",system-ui,sans-serif;margin:0;line-height:1.1;letter-spacing:-0.02em}
h1{font-weight:800;font-size:clamp(27px,4.2vw,44px)}
h2{font-weight:800;font-size:clamp(21px,3vw,29px)}
h3{font-weight:600;font-size:19px;letter-spacing:-0.01em}
h4{font-weight:600;font-size:15.5px}
p{margin:0 0 12px}
a{color:var(--moss)}
button{font:inherit}
.mono{font-family:"IBM Plex Mono",ui-monospace,Menlo,monospace}

.shell{display:grid;grid-template-columns:252px minmax(0,1fr);min-height:100vh}
.rail{background:#FFFFFF;color:var(--ink);padding:24px 16px 40px;position:sticky;top:0;height:100vh;overflow:auto;border-right:1px solid var(--line)}
.brandmark{font-family:"IBM Plex Mono",monospace;font-size:10.5px;letter-spacing:.2em;text-transform:uppercase;color:var(--moss)}
.brandtitle{font-family:"Archivo",sans-serif;font-weight:800;font-size:30px;line-height:.95;margin:8px 0 4px;color:var(--ink);letter-spacing:-0.03em}
.brandsub{font-size:12px;color:var(--ink-soft);line-height:1.4;margin-bottom:20px}
.navbtn{display:flex;gap:11px;align-items:baseline;width:100%;text-align:left;background:none;border:0;border-left:3px solid transparent;color:var(--ink-soft);padding:11px 10px;margin:1px 0;border-radius:0 6px 6px 0;cursor:pointer;transition:background .14s,color .14s,border-color .14s}

.navbtn:hover{background:#EEF3F0;color:var(--ink)}
.navbtn[aria-current="true"]{background:var(--moss-tint);color:var(--moss);border-left-color:var(--moss)}
.navbtn[aria-current="true"] .lbl{color:var(--moss)}
.navbtn[aria-current="true"] .sub{color:#5E7D72}
.navbtn .num{font-family:"IBM Plex Mono",monospace;font-size:11px;color:#9DB1AA;min-width:16px}
.navbtn[aria-current="true"] .num{color:var(--moss)}
.navbtn .lbl{font-family:"Archivo",sans-serif;font-weight:600;font-size:15.5px;letter-spacing:-0.01em}
.navbtn .sub{display:block;font-size:11.5px;color:#8A9A94;font-weight:400;font-family:"IBM Plex Sans",sans-serif;letter-spacing:0}
.navbtn .tick{margin-left:auto;font-size:12px;color:var(--moss);font-weight:700}
.railfoot{margin-top:22px;padding-top:16px;border-top:1px solid var(--line);font-size:11.5px;color:var(--ink-soft);line-height:1.55}
.railfoot code{color:var(--moss);font-weight:600}

.main{padding:36px clamp(18px,4vw,54px) 90px;max-width:1080px}
.eyebrow{font-family:"IBM Plex Mono",monospace;font-size:11px;letter-spacing:.2em;text-transform:uppercase;color:var(--moss);margin-bottom:10px}
.lede{font-size:17px;color:var(--ink-soft);max-width:64ch;margin:12px 0 28px}
.hidden{display:none !important}

.ledger{border-top:2px solid var(--ink);margin-top:6px}
.lrow{display:grid;grid-template-columns:46px minmax(0,1fr) minmax(0,1.2fr) 92px;gap:16px;align-items:center;border-bottom:1px solid var(--line);padding:14px 6px;cursor:pointer;background:none;border-left:0;border-right:0;border-top:0;width:100%;text-align:left;transition:background .14s}
.lrow:hover{background:var(--moss-tint)}
.lrow .idx{font-family:"IBM Plex Mono",monospace;font-size:20px;color:var(--moss);font-weight:600}
.lrow .nm{font-family:"Archivo",sans-serif;font-weight:600;font-size:18px;letter-spacing:-0.01em}
.lrow .one{font-size:14px;color:var(--ink-soft)}
.lrow .go{font-family:"IBM Plex Mono",monospace;font-size:11px;color:var(--ink-soft);text-align:right;letter-spacing:.08em}
.lrow.capstone .idx{color:var(--amber)}

.card{background:var(--card);border:1px solid var(--line);border-radius:var(--radius);padding:22px 24px;margin-bottom:18px}
.card.tight{padding:16px 18px}
.grid2{display:grid;grid-template-columns:repeat(auto-fit,minmax(285px,1fr));gap:16px}
.grid3{display:grid;grid-template-columns:repeat(auto-fit,minmax(215px,1fr));gap:14px}
.tag{display:inline-block;font-family:"IBM Plex Mono",monospace;font-size:10.5px;letter-spacing:.14em;text-transform:uppercase;padding:3px 8px;border-radius:2px;background:var(--moss-tint);color:var(--moss)}
.tag.amber{background:var(--amber-tint);color:var(--amber)}
.tag.slate{background:var(--slate-tint);color:var(--slate)}
.tag.rose{background:var(--rose-tint);color:var(--rose)}
.shift{border-left:3px solid var(--moss);padding:8px 0 8px 14px;font-style:italic;color:var(--moss);margin:14px 0}
.obslist{list-style:none;margin:0;padding:0;counter-reset:o}
.obslist li{counter-increment:o;position:relative;padding:11px 0 11px 40px;border-bottom:1px dotted var(--line);font-size:15.2px}
.obslist li:last-child{border-bottom:0}
.obslist li::before{content:counter(o);position:absolute;left:0;top:10px;font-family:"IBM Plex Mono",monospace;font-size:11px;color:#fff;background:var(--moss);width:20px;height:20px;border-radius:50%;display:grid;place-items:center}

.btn{background:var(--ink);color:#fff;border:1px solid var(--ink);padding:10px 18px;border-radius:var(--radius);cursor:pointer;font-weight:500;font-size:15px;transition:opacity .15s}
.btn.action{background:var(--amber);border-color:var(--amber);color:#fff;font-weight:600;box-shadow:0 1px 0 rgba(181,125,14,.35)}
.btn.action:hover{opacity:.9}
input:not([type="button"]):focus,select:focus,textarea:focus{outline:2px solid var(--amber);outline-offset:1px;border-color:var(--amber)}
.btn:hover{opacity:.86}
.btn.ghost{background:transparent;color:var(--ink)}
.btn.moss{background:var(--moss);border-color:var(--moss)}
.btn.small{padding:6px 12px;font-size:13.5px}
select,input[type=text]{font:inherit;width:100%;padding:9px 11px;border:1px solid var(--line);border-radius:var(--radius);background:#fff;color:var(--ink)}
label.fl{display:block;font-size:12.5px;font-weight:600;letter-spacing:.02em;margin:14px 0 5px;color:var(--ink-soft)}
label.fl .hint{font-weight:400;color:#8A9793}
:focus-visible{outline:2px solid var(--amber);outline-offset:2px}

.opt{display:block;width:100%;text-align:left;background:#fff;border:1px solid var(--line);border-radius:var(--radius);padding:12px 14px;margin-bottom:9px;cursor:pointer;font-size:15.2px;transition:border-color .12s,background .12s}
.opt:hover{border-color:var(--moss)}
.opt.correct{border-color:var(--moss);background:var(--moss-tint)}
.opt.wrong{border-color:var(--rose);background:var(--rose-tint)}
.opt.dim{opacity:.55}
.opt[disabled]{cursor:default}
.feedback{border-left:3px solid var(--amber);background:var(--amber-tint);padding:12px 14px;margin:6px 0 4px;font-size:14.6px}
.progressbar{height:5px;background:var(--line);border-radius:3px;overflow:hidden;margin:4px 0 20px}
.progressbar i{display:block;height:100%;background:var(--moss);transition:width .3s}

.meter{display:grid;grid-template-columns:190px 1fr 54px;gap:12px;align-items:center;padding:7px 0;border-bottom:1px dotted var(--line);font-size:14.4px}
.meter .bar{background:var(--line);height:9px;border-radius:5px;overflow:hidden}
.meter .bar i{display:block;height:100%;background:var(--moss)}
.meter .bar i.low{background:var(--rose)}
.meter .bar i.mid{background:var(--amber)}
.meter .val{text-align:right;font-family:"IBM Plex Mono",monospace;font-size:12.5px;color:var(--ink-soft)}

.tbl{width:100%;border-collapse:collapse;font-size:14px;margin-top:10px}
.tbl th{background:var(--ink);color:#fff;font-family:"Archivo",sans-serif;font-weight:600;font-size:11.5px;letter-spacing:.06em;text-transform:uppercase;padding:9px 10px;text-align:left}
.tbl td{border:1px solid var(--line);padding:9px 10px;vertical-align:top;background:#fff}
.tbl td.k{background:var(--moss-tint);font-weight:500;width:26%}
.prov{display:block;margin-top:4px;font-family:"IBM Plex Mono",monospace;font-size:10px;letter-spacing:.02em;text-transform:none;font-weight:400;color:var(--ink-soft);opacity:.85}
.pedlist{display:flex;flex-direction:column;gap:10px}
.pedrow{border-left:3px solid var(--moss-tint);padding:8px 0 8px 14px}
.pedname{font-weight:600;font-size:15px}
.pedfam{display:inline-block;margin-left:8px;font-family:"IBM Plex Mono",monospace;font-size:9.5px;letter-spacing:.1em;text-transform:uppercase;color:var(--moss);vertical-align:middle}
.peddoes{font-size:14px;margin-top:3px}
.pedassess{font-size:13.4px;color:var(--ink-soft);margin-top:3px}
.vidfeature{position:relative;padding-top:56.25%;height:0;border-radius:6px;overflow:hidden;background:#000}
.vidfeature iframe{position:absolute;inset:0;width:100%;height:100%;border:0}
.vidgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:14px;margin-top:16px}
.vidshort .frame{position:relative;padding-top:177.78%;height:0;border-radius:6px;overflow:hidden;background:#000}
.vidshort .frame iframe{position:absolute;inset:0;width:100%;height:100%;border:0}
.vidcap{font-size:12.5px;color:var(--ink-soft);margin-top:7px;text-align:center;line-height:1.3}
.toggle2{display:inline-flex;border:1px solid var(--line);border-radius:22px;overflow:hidden;margin:8px 0 4px}
.pilltog{background:var(--card);border:0;padding:9px 18px;font-size:14px;font-weight:600;color:var(--ink-soft);cursor:pointer;transition:background .14s,color .14s}
.pilltog:hover{background:#EEF3F0}
.pilltog.on{background:var(--moss-tint);color:var(--moss)}
.aicfg{border:1px solid var(--line);border-radius:6px;padding:10px 14px;background:var(--paper)}
.aicfg summary{cursor:pointer;font-weight:600;font-size:14px;color:var(--moss)}
.aicfgbody{margin-top:10px}
.aicfg input,.aicfg select{width:100%;box-sizing:border-box}
.aiopt{border:1px solid var(--line);border-radius:8px;padding:14px 16px;margin-bottom:14px;background:var(--card)}
.aiopt-h{font-weight:700;font-size:14px;color:var(--moss);margin-bottom:6px}
.aiopt-tag{display:inline-block;margin-left:8px;font-family:"IBM Plex Mono",monospace;font-size:9.5px;letter-spacing:.08em;text-transform:uppercase;font-weight:600;color:var(--amber);background:var(--amber-tint);padding:2px 7px;border-radius:10px;vertical-align:middle}
.locard{background:var(--paper);border:1px solid var(--line);border-radius:8px;padding:16px}
.locard .lonum{display:inline-flex;align-items:center;justify-content:center;width:34px;height:34px;border-radius:50%;color:#fff;font-weight:700;font-family:"IBM Plex Mono",monospace;font-size:16px}
.locard h4{margin:12px 0 6px;font-size:16px}
.locard p{font-size:14px;color:var(--ink-soft);margin:0}
.devgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:14px;margin-top:8px}
.dev{border-left:3px solid var(--moss-tint);padding:2px 0 2px 14px}
.devname{font-weight:600;font-size:15px}
.devaff{font-size:13px;color:var(--ink-soft);margin-top:3px}
.tbl tr td:first-child{width:26%}

.callout{background:var(--ink);color:#E4EDE9;padding:18px 20px;border-radius:var(--radius);margin:18px 0}
.callout strong{color:#fff}
.split{display:grid;grid-template-columns:1fr 1fr;gap:0;border:1px solid var(--line);border-radius:var(--radius);overflow:hidden;margin-top:14px}
.split>div{padding:18px 20px;background:#fff}
.split>div:first-child{background:var(--rose-tint);border-right:1px solid var(--line)}
.split>div:last-child{background:var(--moss-tint)}
.split .hd{font-family:"IBM Plex Mono",monospace;font-size:11px;letter-spacing:.14em;text-transform:uppercase;margin-bottom:8px}
.quote{font-family:"Archivo",sans-serif;font-weight:500;font-size:17px;line-height:1.3;margin-bottom:10px}

.gradient{display:grid;grid-template-columns:repeat(4,1fr);gap:0;border:1px solid var(--line);margin-top:12px;border-radius:var(--radius);overflow:hidden}
.gradient>div{padding:14px;background:#fff;border-right:1px solid var(--line);font-size:13.6px}
.gradient>div:last-child{border-right:0;background:var(--moss-tint)}
.gradient .lv{font-family:"IBM Plex Mono",monospace;font-size:10.5px;letter-spacing:.12em;color:var(--ink-soft);display:block;margin-bottom:7px}

.status{font-size:13px;color:var(--ink-soft);margin-top:10px;min-height:20px}
.err{color:var(--rose)}
details{border-top:1px solid var(--line);padding-top:10px;margin-top:10px}
summary{cursor:pointer;font-size:14.4px;color:var(--moss);font-weight:500}
.chip{display:inline-block;font-size:12.5px;background:var(--slate-tint);color:var(--slate);padding:3px 9px;border-radius:20px;margin:0 5px 5px 0}
.chip.m{background:var(--moss-tint);color:var(--moss)}

@media(max-width:860px){
  .shell{grid-template-columns:1fr}
  .rail{position:static;height:auto;padding:18px 16px 20px;border-right:0;border-bottom:1px solid var(--line)}
  .navrow{display:grid;grid-template-columns:repeat(2,1fr);gap:0 14px}
  .lrow{grid-template-columns:34px 1fr;gap:6px 12px}
  .lrow .one{grid-column:2}
  .lrow .go{display:none}
  .meter{grid-template-columns:1fr;gap:4px}
  .meter .val{text-align:left}
  .split,.gradient{grid-template-columns:1fr}
  .split>div:first-child{border-right:0;border-bottom:1px solid var(--line)}
  .gradient>div{border-right:0;border-bottom:1px solid var(--line)}
}
@media print{.rail,.noprint{display:none !important}body{background:#fff}.shell{display:block}.card{break-inside:avoid}}
/* ---- Build tab ---- */
.wf-steps{display:flex;flex-wrap:wrap;gap:6px;margin:6px 0 26px}
.wf-steps .wf{flex:1 1 90px;min-width:84px;border:1px solid var(--line);border-radius:6px;background:#fff;padding:9px 10px;font-size:11.5px;color:var(--ink-soft);position:relative}
.wf-steps .wf .wn{font-family:"IBM Plex Mono",monospace;font-size:10px;letter-spacing:.1em;color:#9DB1AA;display:block}
.wf-steps .wf .wl{font-family:"Archivo",sans-serif;font-weight:600;font-size:13px;color:var(--ink);margin-top:2px;display:block;line-height:1.15}
.wf-steps .wf.done{border-color:var(--moss);background:var(--moss-tint)}
.wf-steps .wf.done .wl{color:var(--moss)}
.wf-steps .wf.done .wn{color:var(--moss)}
.stepcard{background:#fff;border:1px solid var(--line);border-radius:8px;padding:20px 22px;margin-bottom:16px;border-left:4px solid var(--line)}
.stepcard.ok{border-left-color:var(--moss)}
.stepcard.warn{border-left-color:var(--amber)}
.stepnum{display:inline-flex;align-items:center;justify-content:center;width:26px;height:26px;border-radius:50%;background:var(--ink);color:#fff;font-family:"IBM Plex Mono",monospace;font-size:13px;font-weight:600;margin-right:10px}
.stepcard.ok .stepnum{background:var(--moss)}
.stephead{display:flex;align-items:center;margin-bottom:6px}
.stephead h3{font-size:18px}
.stepsub{font-size:13.5px;color:var(--ink-soft);margin:0 0 14px 36px}
.pickgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:8px;margin-left:36px}
.pick{border:1px solid var(--line);border-radius:6px;background:#fff;padding:10px 12px;cursor:pointer;text-align:left;font-size:13.5px;transition:border-color .12s,background .12s;color:var(--ink)}
.pick:hover{border-color:var(--moss)}
.pick[aria-pressed="true"]{border-color:var(--moss);background:var(--moss-tint);color:var(--moss);font-weight:600}
.pick .pk{font-family:"IBM Plex Mono",monospace;font-size:10px;color:#9DB1AA;display:block}
.pick[aria-pressed="true"] .pk{color:var(--moss)}
.sdgpick{border:1px solid var(--line);border-radius:6px;background:#fff;padding:8px 10px;cursor:pointer;text-align:left;font-size:12.5px;display:flex;gap:8px;align-items:center;transition:border-color .12s,background .12s;color:var(--ink)}
.sdgpick:hover{border-color:var(--slate)}
.sdgpick[aria-pressed="true"]{border-color:var(--slate);background:var(--slate-tint);color:var(--slate);font-weight:600}
.sdgpick .sn{font-family:"IBM Plex Mono",monospace;font-weight:700;min-width:20px}
.blk{margin-left:36px;margin-bottom:16px;padding:16px;border:1px solid var(--line);border-radius:6px;background:#FAFBFA}
.blk h4{font-size:14.5px;margin-bottom:2px}
.blk .bsub{font-size:12.5px;color:var(--ink-soft);margin-bottom:10px}
.rubedit{width:100%;border-collapse:collapse;margin-top:8px;font-size:12.5px}
.rubedit th{background:var(--ink);color:#fff;font-family:"Archivo",sans-serif;font-size:10.5px;letter-spacing:.05em;text-transform:uppercase;padding:6px 7px;text-align:left}
.rubedit td{border:1px solid var(--line);padding:0;vertical-align:top}
.rubedit td.rc{background:var(--moss-tint);font-weight:500;padding:8px;width:22%;font-size:12px}
.rubedit textarea{width:100%;border:0;background:transparent;padding:7px 8px;font:inherit;font-size:12px;line-height:1.4;resize:vertical;min-height:60px;color:var(--ink)}
.rubedit td:nth-child(2){background:#FBEDED}
.rubedit td:nth-child(3){background:#FBF3E2}
.rubedit td:nth-child(4){background:#EDF3F0}
.rubedit td:nth-child(5){background:#E4EDE9}
textarea.cloin{width:100%;font:inherit;font-size:14px;padding:9px 11px;border:1px solid var(--line);border-radius:6px;min-height:56px;resize:vertical;line-height:1.45;color:var(--ink)}
.verbhint{font-size:12px;color:var(--ink-soft);margin-top:6px}
.verbhint b{color:var(--moss);font-family:"IBM Plex Mono",monospace;font-weight:600}
.alignprev{background:#fff;border:1px solid var(--line);border-radius:8px;padding:20px 22px;margin-top:8px}
.wchip{display:inline-block;font-size:12px;background:var(--amber-tint);color:var(--amber);border:1px solid #E9D9AE;padding:4px 10px;border-radius:20px;margin-left:36px;margin-bottom:8px}
@media(max-width:860px){.pickgrid{grid-template-columns:1fr 1fr}.stepsub,.pickgrid,.blk,.wchip{margin-left:0}.rubedit td.rc{width:30%}}
@media(prefers-reduced-motion:reduce){*{transition:none !important}}
</style>

<div class="shell">
  <nav class="rail">
    <div class="brandmark">UNESCO 2030 framework</div>
    <div class="brandtitle">The<br>Eight</div>
    <div class="brandsub">Understand the competencies, see them in your field, teach them, and assess them with a rubric you can defend.</div>
    <div class="navrow">
      <button class="navbtn" data-view="understand"><span class="num">01</span><span><span class="lbl">Understand</span><span class="sub">The eight in general</span></span><span class="tick" data-tick="understand"></span></button>
      <button class="navbtn" data-view="lens"><span class="num">02</span><span><span class="lbl">Your field</span><span class="sub">The eight, from your discipline</span></span><span class="tick" data-tick="lens"></span></button>
      <button class="navbtn" data-view="quiz1"><span class="num">03</span><span><span class="lbl">Quiz 1</span><span class="sub">Meaning and field</span></span><span class="tick" data-tick="quiz1"></span></button>
      <button class="navbtn" data-view="pedagogy"><span class="num">04</span><span><span class="lbl">Pedagogy</span><span class="sub">How to teach each one</span></span><span class="tick" data-tick="pedagogy"></span></button>
      <button class="navbtn" data-view="assess"><span class="num">05</span><span><span class="lbl">Assess</span><span class="sub">Tasks and rubrics, all eight</span></span><span class="tick" data-tick="assess"></span></button>
      <button class="navbtn" data-view="quiz2"><span class="num">06</span><span><span class="lbl">Quiz 2</span><span class="sub">Assessment and rubrics</span></span><span class="tick" data-tick="quiz2"></span></button>
      <button class="navbtn" data-view="quiz3"><span class="num">07</span><span><span class="lbl">Quiz 3</span><span class="sub">Diagnose real assignments</span></span><span class="tick" data-tick="quiz3"></span></button>
      <button class="navbtn" data-view="build"><span class="num">08</span><span><span class="lbl">Build a module</span><span class="sub">The full workflow, end to end</span></span><span class="tick" data-tick="build"></span></button>
    </div>
    <div class="railfoot">
      Field: <code id="railDisc" class="mono">not set</code><br>
      <span id="railSaved">Progress saves on this device.</span>
      <div style="margin-top:14px;padding-top:12px;border-top:1px solid var(--line)">
        <div class="mono" style="font-size:9.5px;letter-spacing:.14em;text-transform:uppercase;color:var(--moss);margin-bottom:6px">References</div>
        UNESCO (2020). <i>ESD: A Roadmap (ESD for 2030)</i>.<br>
        MQA. <i>Malaysian Qualifications Framework (MQF)</i>, Second Edition 2024.<br>
        UPM Policy on ESD &#183; assessed under PLO12.
      </div>
    </div>
  </nav>

  <main class="main">

  <!-- ================= 01 UNDERSTAND ================= -->
  <section id="view-understand">
    <div class="eyebrow">Stage 01 &#183; Understand</div>
    <h1>Seven capacities, plus one that integrates them.</h1>
    <p class="lede">Start here, before your discipline and before assessment. Open each row for what the competency actually claims, the shift it demands of student work, and the three observable behaviours &#8212; these seed criteria 1&#8211;3 of every rubric later, with a fourth criterion added for what the student does with the analysis.</p>

    <div class="card">
      <span class="tag">Learning outcomes</span>
      <h3 style="margin:12px 0 2px">Three objectives to achieve by the end of this workshop</h3>
      <div class="grid3" style="margin-top:14px">
        <div class="locard"><span class="lonum" style="background:var(--moss)">1</span><h4>Understand &amp; internalise</h4><p>Deeply comprehend and internalise the core Education for Sustainable Development (ESD) competencies.</p></div>
        <div class="locard"><span class="lonum" style="background:var(--amber)">2</span><h4>Design course content</h4><p>Structure curriculum and content capable of delivering ESD competencies through active and suitable pedagogy.</p></div>
        <div class="locard"><span class="lonum" style="background:var(--slate)">3</span><h4>Assess ESD competencies</h4><p>Evaluate and measure student attainment of ESD competencies using an appropriate, defensible rubric.</p></div>
      </div>
    </div>

    <div class="ledger" id="ledger"></div>

    <div class="card noprint" style="margin-top:26px">
      <span class="tag">Watch</span>
      <h3 style="margin:12px 0 6px">Short explainers to go with the eight</h3>
      <p style="color:var(--ink-soft);font-size:15px">Start with the overview, then one short per competency.</p>
      <div class="vidfeature" style="margin-top:14px"><iframe src="https://www.youtube.com/embed/N0eB2n5L-xE" title="Education for Sustainable Development \u2014 overview" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div>
      <div class="vidgrid">
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/VVtdcICaVu0" title="Systems Thinking" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">01 &#183; Systems Thinking</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/Bk4Nu1mfh_o" title="Anticipatory Competency" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">02 &#183; Anticipatory Competency</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/BNA0UdvqlhY" title="Normative Competency" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">03 &#183; Normative Competency</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/S5HETTBNJx0" title="Strategic Competency" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">04 &#183; Strategic Competency</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/Fdkph29HjpA" title="Collaboration Competency" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">05 &#183; Collaboration Competency</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/dfpuvpwsJNA" title="Critical Thinking" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">06 &#183; Critical Thinking</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/aMvpJKFqatk" title="Self-awareness" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">07 &#183; Self-awareness</div></div>
        <div class="vidshort"><div class="frame"><iframe src="https://www.youtube.com/embed/ePkq6rWdt8c" title="Integrated Problem-solving" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></div><div class="vidcap">08 &#183; Integrated Problem-solving</div></div>
      </div>
    </div>

    <div class="card" style="margin-top:26px">
      <span class="tag">Checkpoint</span>
      <h3 style="margin:12px 0 8px">Four distinctions worth getting right</h3>
      <p style="color:var(--ink-soft);font-size:15px">These confusions are the ones that show up in course outlines.</p>
      <div class="grid2" id="distinctions"></div>
    </div>

    <div class="callout">
      <strong>The line to carry into every later stage.</strong> If a student could score full marks without using the competency, you have not assessed it &#8212; whatever your outline claims.
    </div>

    <div class="card" style="margin-top:26px">
      <span class="tag slate">Content developers</span>
      <h3 style="margin:12px 0 8px">Developed by</h3>
      <div class="devgrid">
        <div class="dev"><div class="devname">Prof. Dr Zurina Zainal Abidin</div><div class="devaff">Department of Chemical and Environmental Engineering, Faculty of Engineering, Universiti Putra Malaysia</div></div>
        <div class="dev"><div class="devname">Assoc. Prof. Dr Suriati Paiman</div><div class="devaff">Department of Physics, Faculty of Science, Universiti Putra Malaysia</div></div>
        <div class="dev"><div class="devname">Dr Rafidah Hod</div><div class="devaff">Department of Medical Education, Faculty of Medicine and Life Sciences, Universiti Putra Malaysia</div></div>
        <div class="dev"><div class="devname">Dr Siti Mastura Md Ishak</div><div class="devaff">Department of Industrial Design, Faculty of Design and Architecture, Universiti Putra Malaysia</div></div>
      </div>
    </div>
    <p class="noprint"><button class="btn moss" data-goto="lens">Next: see them in your field &#8594;</button></p>
  </section>

  <!-- ================= COMPETENCY DETAIL ================= -->
  <section id="view-detail" class="hidden">
    <button class="btn ghost small noprint" id="backBtn">&#8592; Back</button>
    <div id="detailBody" style="margin-top:20px"></div>
  </section>

  <!-- ================= 02 DISCIPLINE LENS ================= -->
  <section id="view-lens" class="hidden">
    <div class="eyebrow">Stage 02 &#183; Your field</div>
    <h1>Same demand. Your vocabulary.</h1>
    <p class="lede">Choose your discipline and the eight are restated as things a student in your field would actually be asked to do. Adapt the wording; keep the demand. If your field is not listed, pick the nearest and write your own equivalent &#8212; that improvisation is itself the exercise.</p>

    <div class="card noprint">
      <label class="fl" for="disc">My discipline</label>
      <select id="disc"></select>
      <p style="margin:12px 0 0;font-size:13.6px;color:var(--ink-soft)">Quiz 1 uses your field, so set this before you start it.</p>
    </div>

    <div id="lensOut"></div>
    <p class="noprint"><button class="btn moss" data-goto="quiz1">Next: quiz on stages 01 and 02 &#8594;</button></p>
  </section>

  <!-- ================= 03 QUIZ 1 ================= -->
  <section id="view-quiz1" class="hidden">
    <div class="eyebrow">Stage 03 &#183; Quiz 1</div>
    <h1>Can you name it, and tell it apart?</h1>
    <div id="q1intro">
      <p class="lede">Fifteen questions on meaning and on your field. Identify the competency from a student behaviour, from a plain-language description, and from a task in your discipline &#8212; then separate the four pairs people confuse. Every answer comes with the reason, not just a tick.</p>
      <div class="grid3">
        <div class="card"><span class="tag">Identify</span><p style="margin-top:10px;font-size:14.6px">A student does this &#8212; which of the eight is it evidence of?</p></div>
        <div class="card"><span class="tag slate">In your field</span><p style="margin-top:10px;font-size:14.6px">A task from your discipline &#8212; which competency does it carry?</p></div>
        <div class="card"><span class="tag amber">Distinguish</span><p style="margin-top:10px;font-size:14.6px">The four pairs that get mis-selected in outlines.</p></div>
      </div>
      <p style="margin-top:22px"><button class="btn action" data-start="q1">Start quiz 1</button></p>
    </div>
    <div class="qrun hidden" data-run="q1"></div>
    <div class="qdone hidden" data-done="q1"></div>
  </section>

  <!-- ================= 04 PEDAGOGY ================= -->
  <section id="view-pedagogy" class="hidden">
    <div class="eyebrow">Stage 04 &#183; Pedagogy</div>
    <h1>Coverage means students practise it.</h1>
    <p class="lede">Explaining a competency is not covering it. This stage shows what each competency looks like under a real teaching approach &#8212; and why changing how you teach means nothing unless the assessment changes with it.</p>

    <div class="card">
      <span class="tag">The framing that prevents the commonest error</span>
      <div class="grid3" style="margin-top:14px">
        <div><h4>The pedagogy</h4><p style="font-size:14.6px;margin-top:6px">Delivers the experience where students practise the competency.</p></div>
        <div><h4>The competency</h4><p style="font-size:14.6px;margin-top:6px">Stays the same regardless of the method you choose.</p></div>
        <div><h4>The assessment</h4><p style="font-size:14.6px;margin-top:6px">Must change to capture what that method actually produces.</p></div>
      </div>
      <div class="callout" style="margin-bottom:0">A gamified course that still marks a written exam has changed nothing that matters.</div>
    </div>

    <h2 style="margin:30px 0 6px">Methods that develop each competency</h2>
    <p style="color:var(--ink-soft);margin-bottom:16px">Drawn from UNESCO's four method families (guidebook Part 3.3). Pick one you can run in week 5 and repeat in week 9 &#8212; one activity produces an anecdote, two spaced with feedback produce a capability. Gamification is left out on purpose: it develops motivation only and evidences no competency on its own.</p>
    <div id="pedCards"></div>

    <div class="card">
      <h3>Classroom methods, competency by competency</h3>
      <p style="font-size:14.6px;color:var(--ink-soft)">Pick one you could run in week 5 and repeat in week 9. Repetition matters &#8212; one activity produces an anecdote, not a capability.</p>
      <table class="tbl"><thead><tr><th>Competency</th><th>Methods</th><th>Strongest pedagogy</th></tr></thead><tbody id="methodRows"></tbody></table>
    </div>

    <div class="card">
      <span class="tag">Worked example</span>
      <h3 style="margin:12px 0 4px">One session, redesigned</h3>
      <p style="color:var(--ink-soft);font-size:15px">Same topic. Same hours. Different question.</p>
      <div class="split">
        <div>
          <div class="hd" style="color:var(--rose)">Before</div>
          <p style="margin:0 0 6px">Lecture on treatment stages.</p>
          <p style="margin:0 0 6px">Tutorial: calculate loading rates.</p>
          <p style="margin:0 0 10px">Exam question on process selection.</p>
          <p style="margin:0;font-size:13.6px;color:var(--ink-soft)">Competency evidenced: none. One right answer, nobody affected.</p>
        </div>
        <div>
          <div class="hd" style="color:var(--moss)">After &#183; systems + normative</div>
          <p style="margin:0 0 6px">Same lecture, unchanged.</p>
          <p style="margin:0 0 6px">Same calculation, then map who uses the water downstream.</p>
          <p style="margin:0 0 6px">Decide the discharge standard to design to, and justify it.</p>
          <p style="margin:0 0 10px">Same report, plus a two-page justification memo.</p>
          <p style="margin:0;font-size:13.6px;color:var(--ink-soft)">Added cost: one tutorial redesign, two pages per student to mark.</p>
        </div>
      </div>
      <p style="margin-top:14px;font-size:14.6px">The calculation does not change. What changes is that the answer must then be defended against a question with no single right answer.</p>
    </div>

    <div class="card">
      <span class="tag amber">Three things must always be true</span>
      <p style="margin:12px 0 0;color:var(--ink-soft);font-size:15px">Whatever teaching method you choose.</p>
      <div class="grid3" style="margin-top:12px">
        <div><h4>1 &#183; Individual evidence exists</h4><p style="font-size:14.4px;margin-top:6px">Something each student personally produced can be judged.</p></div>
        <div><h4>2 &#183; The task requires the competency</h4><p style="font-size:14.4px;margin-top:6px">It cannot be completed well without using it.</p></div>
        <div><h4>3 &#183; The rubric was published first</h4><p style="font-size:14.4px;margin-top:6px">Students saw the criteria before they began the work.</p></div>
      </div>
    </div>
    <p class="noprint"><button class="btn moss" data-goto="assess">Next: assessment and rubrics &#8594;</button></p>
  </section>

  <!-- ================= 05 ASSESS ================= -->
  <section id="view-assess" class="hidden">
    <div class="eyebrow">Stage 05 &#183; Assess</div>
    <h1>The mark has to survive being questioned.</h1>
    <p class="lede">A knowledge question cannot assess a competency. This stage covers the task that can, the output each of the eight produces, the anatomy of a usable rubric and the four faults that break one &#8212; then gives you rubric anchors for all eight competencies.</p>

    <div class="card">
      <span class="tag">Task design</span>
      <h3 style="margin:12px 0 4px">Two questions, same topic</h3>
      <p style="color:var(--ink-soft);font-size:15px">Only one assesses a competency.</p>
      <div class="split">
        <div>
          <div class="hd" style="color:var(--rose)">Assesses knowledge</div>
          <p class="quote">&#8220;Define systems thinking and explain its importance.&#8221;</p>
          <p style="margin:0;font-size:14.2px">A student who memorised the lecture scores full marks. There is nothing here to build four rubric levels from except length and polish.</p>
        </div>
        <div>
          <div class="hd" style="color:var(--moss)">Assesses the competency</div>
          <p class="quote">&#8220;Define the system boundary and justify what you excluded. Identify one feedback loop. State one consequence appearing elsewhere.&#8221;</p>
          <p style="margin:0;font-size:14.2px">The student must perform the competency to answer at all &#8212; and each clause becomes a rubric criterion.</p>
        </div>
      </div>
    </div>

    <div class="card">
      <h3>What evidence does each competency produce?</h3>
      <p style="font-size:14.6px;color:var(--ink-soft)">Choose the output first. The rubric follows.</p>
      <table class="tbl"><thead><tr><th>Competency</th><th>Output that carries the evidence</th></tr></thead><tbody id="evidenceRows"></tbody></table>
      <p style="margin-top:12px;font-size:14.4px">The collaboration row matters most: a group report is evidence of a group, not of an individual. Every group task needs an individual output attached, or the rubric cannot be applied to a person.</p>
    </div>

    <div class="card">
      <span class="tag rose">Three traps when marking</span>
      <p style="margin:12px 0 0;color:var(--ink-soft);font-size:15px">Each one produces a mark you cannot defend.</p>
      <div class="grid3" style="margin-top:12px">
        <div><h4>Marking the group</h4><p style="font-size:14.4px;margin:6px 0">A group report used as evidence that an individual holds the competency.</p><p style="font-size:14.4px;color:var(--moss);margin:0">Attach a short individual output.</p></div>
        <div><h4>Marking sincerity</h4><p style="font-size:14.4px;margin:6px 0">Reflective work graded on how heartfelt it sounds.</p><p style="font-size:14.4px;color:var(--moss);margin:0">Mark specificity and reasoning, never sentiment.</p></div>
        <div><h4>Marking the position</h4><p style="font-size:14.4px;margin:6px 0">Rewarding students whose values match your own.</p><p style="font-size:14.4px;color:var(--moss);margin:0">Mark whether the principle was applied consistently.</p></div>
      </div>
    </div>

    <div class="grid2">
      <div class="card">
        <span class="tag">Anatomy of a usable rubric</span>
        <table class="tbl"><tbody>
          <tr><td class="k">Criteria</td><td>Taken from the observable behaviours. Three per competency.</td></tr>
          <tr><td class="k">Levels</td><td>Four: Limited, Developing, Proficient, Exemplary.</td></tr>
          <tr><td class="k">Descriptors</td><td>What the work looks like &#8212; differentiated by quality, not quantity.</td></tr>
          <tr><td class="k">Weighting</td><td>The share of the course mark these criteria carry.</td></tr>
        </tbody></table>
      </div>
      <div class="card">
        <span class="tag rose">The four faults</span>
        <table class="tbl"><tbody>
          <tr><td class="k">Adjectives, not descriptors</td><td>&#8220;Excellent / Good / Fair / Poor&#8221; is a grading scale. It tells the student nothing.</td></tr>
          <tr><td class="k">Levels separated by counting</td><td>&#8220;Three factors&#8221; versus &#8220;one factor&#8221; measures volume, not competence.</td></tr>
          <tr><td class="k">Criteria that restate the brief</td><td>&#8220;Report is well structured&#8221; assesses report writing, not the competency.</td></tr>
          <tr><td class="k">Written after the task</td><td>A rubric students never saw is a marking aid, not an assessment design.</td></tr>
        </tbody></table>
      </div>
    </div>

    <div class="card">
      <span class="tag amber">The technique</span>
      <h3 style="margin:12px 0 4px">Write level 1 and level 4 first, then split the gap</h3>
      <p style="font-size:15px;color:var(--ink-soft)">Writing levels in order produces a flat, undifferentiated middle. The gradient below transfers to any of the eight: <strong style="color:var(--ink)">lists &#8594; connects &#8594; justifies &#8594; sees its own choice as a choice.</strong></p>
      <p style="font-size:14.4px;margin-bottom:4px"><strong>Systems Thinking &#183; criterion: boundary and elements</strong></p>
      <div class="gradient">
        <div><span class="lv">1 &#183; LIMITED</span>Lists factors affecting the catchment. No boundary drawn.</div>
        <div><span class="lv">2 &#183; DEVELOPING</span>Identifies main elements. Boundary implied but not stated.</div>
        <div><span class="lv">3 &#183; PROFICIENT</span>States the boundary and justifies what was excluded.</div>
        <div><span class="lv">4 &#183; EXEMPLARY</span>Justifies it, and shows how a different boundary changes the conclusion.</div>
      </div>
      <p style="font-size:14.4px;margin:18px 0 4px"><strong>Normative Competency &#183; criterion: justification of position</strong></p>
      <div class="gradient">
        <div><span class="lv">1 &#183; LIMITED</span>States a preference with no supporting reason.</div>
        <div><span class="lv">2 &#183; DEVELOPING</span>Gives reasons, but the criteria shift between options.</div>
        <div><span class="lv">3 &#183; PROFICIENT</span>Applies an explicit principle consistently throughout.</div>
        <div><span class="lv">4 &#183; EXEMPLARY</span>Applies it, states the strongest counter-argument, and responds with reason.</div>
      </div>
      <p style="margin-top:14px;font-size:14.6px">Same shape in both: assert, reason, apply a principle, withstand challenge. That is what makes the technique transferable to the other six.</p>
    </div>

    <div class="card">
      <h3>Rubric anchors for all eight</h3>
      <p style="font-size:14.6px;color:var(--ink-soft)">Four criteria per competency: three taken from its observable behaviours and a fourth for the &#8220;so what&#8221;. Each names the UNESCO (2017) clause it operationalises, or is declared institutional. The two anchor levels are written; fill the middle using the gradient above.</p>
      <label class="fl" for="rubPick">Show rubric anchors for</label>
      <select id="rubPick"></select>
      <div id="rubOut" style="margin-top:14px"></div>
    </div>

    <div class="card">
      <span class="tag slate">Alignment</span>
      <h3 style="margin:12px 0 4px">One worked alignment table</h3>
      <p style="color:var(--ink-soft);font-size:15px">Urban Water Resources Management &#183; Year 3. Only the CLO is directly assessed &#8212; every other layer is a claim that must be traceable through it.</p>
      <table class="tbl"><thead><tr><th>CLO</th><th>PLO</th><th>SDG</th><th>ESDC</th><th>Assessed by</th></tr></thead><tbody>
        <tr><td>Evaluate competing water allocation options for an urban catchment.</td><td>PLO2 &#183; Problem analysis</td><td>SDG 6</td><td>Systems Thinking</td><td>Case report, criteria 1&#8211;3</td></tr>
        <tr><td>Justify the trade-offs between affected groups using an explicit principle.</td><td>PLO8 &#183; Ethics and responsibility</td><td>SDG 6 and 11</td><td>Normative Competency</td><td>Justification memo, criteria 4&#8211;6</td></tr>
      </tbody></table>
      <p style="margin-top:12px;font-size:14.4px">The criteria numbering is what makes it auditable &#8212; an external reviewer can follow a competency to a specific criterion on a specific rubric.</p>
      <details><summary>Five ways alignment fails an audit</summary>
        <table class="tbl" style="margin-top:10px"><tbody>
          <tr><td class="k">SDG as decoration</td><td>A goal logo on the outline with nothing in the content connecting to it.</td></tr>
          <tr><td class="k">Competency with no CLO</td><td>Named in the course outline, but no outcome actually requires it.</td></tr>
          <tr><td class="k">One CLO, five SDGs</td><td>Broad mapping that dilutes everything. Choose one primary goal.</td></tr>
          <tr><td class="k">Reverse-engineered PLO mapping</td><td>CLOs written first, mapping fitted afterwards to satisfy the form.</td></tr>
          <tr><td class="k">Task misses the competency</td><td>The assessment evidences the content of the CLO but not its competency.</td></tr>
        </tbody></table>
        <p style="margin-top:10px;font-size:14.4px">An auditor reads the alignment table, then asks to see the marked scripts.</p>
      </details>
    </div>

    <div class="grid2">
      <div class="card">
        <span class="tag">Student learning resources</span>
        <table class="tbl"><tbody>
          <tr><td class="k">Case file or data set</td><td>Real and messy. A tidy case cannot evidence systems or values reasoning.</td></tr>
          <tr><td class="k">Stakeholder briefs</td><td>Needed for any negotiation, role-play or SULAM activity.</td></tr>
          <tr><td class="k">The rubric itself</td><td>Released with the brief. It is a learning resource, not only a marking tool.</td></tr>
          <tr><td class="k">Reflection prompts</td><td>Unprompted reflection produces sentiment, not assessable evidence.</td></tr>
          <tr><td class="k">Two or three readings</td><td>Chosen to be argued with, not summarised.</td></tr>
          <tr><td class="k">One worked example</td><td>Show a Proficient answer, not an Exemplary one, so students aim above it.</td></tr>
        </tbody></table>
      </div>
      <div class="card">
        <span class="tag">Implementation, next semester</span>
        <table class="tbl"><tbody>
          <tr><td class="k">Before semester</td><td>Finalise the CLO and publish the rubric inside the course outline.</td></tr>
          <tr><td class="k">Week 1</td><td>Tell students the two competencies in plain language.</td></tr>
          <tr><td class="k">Week 4</td><td>Release the task brief together with the rubric.</td></tr>
          <tr><td class="k">Week 5</td><td>First practice activity.</td></tr>
          <tr><td class="k">Week 9</td><td>Second practice activity, same competency.</td></tr>
          <tr><td class="k">Week 11</td><td>Submission, including the individual evidence.</td></tr>
          <tr><td class="k">Week 12&#8211;13</td><td>Mark, then moderate a sample with a colleague.</td></tr>
          <tr><td class="k">After results</td><td>Revise weak descriptors and report coverage to the programme.</td></tr>
        </tbody></table>
      </div>
    </div>
    <p class="noprint"><button class="btn moss" data-goto="quiz2">Next: quiz on assessment and rubrics &#8594;</button></p>
  </section>

  <!-- ================= 06 QUIZ 2 ================= -->
  <section id="view-quiz2" class="hidden">
    <div class="eyebrow">Stage 06 &#183; Quiz 2</div>
    <h1>Would this mark survive being questioned?</h1>
    <div id="q2intro">
      <p class="lede">Fifteen questions on stages 04 and 05. Diagnose the fault in a rubric descriptor, pick the output that carries the evidence, judge whether a task assesses the competency it names, and match a pedagogy to what it actually develops.</p>
      <div class="grid3">
        <div class="card"><span class="tag rose">Diagnose</span><p style="margin-top:10px;font-size:14.6px">What is wrong with this descriptor, task or alignment?</p></div>
        <div class="card"><span class="tag">Evidence</span><p style="margin-top:10px;font-size:14.6px">Which output carries evidence for this competency?</p></div>
        <div class="card"><span class="tag slate">Pedagogy</span><p style="margin-top:10px;font-size:14.6px">Which approach develops it, and what do you actually mark?</p></div>
      </div>
      <p style="margin-top:22px"><button class="btn action" data-start="q2">Start quiz 2</button></p>
    </div>
    <div class="qrun hidden" data-run="q2"></div>
    <div class="qdone hidden" data-done="q2"></div>
  </section>

  <!-- ================= 07 BUILD ================= -->
  <section id="view-build" class="hidden">
    <div class="eyebrow">Stage 08 &#183; Build your module</div>
    <h1>One course, turned into an ESD module.</h1>
    <p class="lede">Work the guidebook workflow end to end: pick the SDG, choose one or two competencies, write the CLO, design the activities and output, describe the assignment topic, then let an AI build a complete rubric tied to it. Everything you enter saves on this device; the AI step uses your chosen provider (Claude by default) and you can set it in step 8.</p>
    <div class="wf-steps" id="wfSteps"></div>
    <div id="buildBody"></div>
  </section>

  <!-- ================= 08 QUIZ 3 ================= -->
  <section id="view-quiz3" class="hidden">
    <div class="eyebrow">Stage 07 &#183; Quiz 3</div>
    <h1>Given a real task, which competency does it assess?</h1>
    <div id="q3intro">
      <p class="lede">Ten real assignment tasks, drawn from the discipline examples in the guidebook. For some, name the competency the task primarily assesses. For others, judge whether the task is suitable to assess a named competency at all &#8212; the one rule decides it: if a student could score full marks without using the competency, it does not assess it.</p>
      <div class="grid3">
        <div class="card"><span class="tag">Name it</span><p style="margin-top:10px;font-size:14.6px">A real task &#8212; which of the eight does it primarily assess?</p></div>
        <div class="card"><span class="tag slate">Judge it</span><p style="margin-top:10px;font-size:14.6px">Is this task suitable to assess the named competency? Yes or no.</p></div>
        <div class="card"><span class="tag amber">The one rule</span><p style="margin-top:10px;font-size:14.6px">Could a student score without using it? Then it is not assessed.</p></div>
      </div>
      <p style="margin-top:22px"><button class="btn action" data-start="q3">Start quiz 3</button></p>
    </div>
    <div class="qrun hidden" data-run="q3"></div>
    <div class="qdone hidden" data-done="q3"></div>
  </section>



  </main>
</div>

<script>
/* ============================================================
   DATA
   ============================================================ */
const DISCIPLINES=["Health, Medical and Life Sciences","Sciences","Engineering","Computer Science and Information Technology","Mathematics and Statistics","Education","Economics, Accounting, Business, Finance and Management","Language, Literature and Communications","Sociology, Psychology and Human Development","Architecture and Design","Agriculture, Forestry, Environmental Science and Food Science"];

const C=[
{n:1,key:"systems",name:"Systems Thinking",one:"See the whole",
 def:"Seeing a problem as connected parts whose interactions produce the outcome.",
 meaning:"Students decide what is inside the system and what is outside it. They trace how a change in one part travels through the rest, recognising feedback, delay, and effects that appear far from the cause.",
 shift:"The shift is from listing factors to mapping relationships.",
 obs:["Maps relationships instead of listing factors","Traces a feedback loop, not just cause and effect","Names a consequence appearing in another domain or at another scale"],
 note:"Listing factors is not systems thinking \u2014 most student work stops at a list, and the competency begins at the relationship. The third behaviour discriminates strong from average work more reliably than the map itself.",
 methods:"Causal loop diagrams \u00b7 life-cycle mapping \u00b7 boundary exercises",
 ped:"Problem-based \u00b7 simulation \u00b7 field work",
 evidence:"Annotated system map with written interpretation",
 rubric:[
  {crit:"Boundary and elements",prov:"UNESCO: analyse complex systems",l1:"Lists factors. No boundary drawn.",l4:"States the boundary, justifies what was excluded, and shows how a different boundary would change the conclusion."},
  {crit:"Interconnections",prov:"UNESCO: recognise and understand relationships",l1:"Describes elements in isolation, or notes cause and effect only.",l4:"Traces a feedback loop and explains a delay or non-linear effect within it."},
  {crit:"Consequences across domains and scales",prov:"UNESCO: systems embedded within different domains and scales",l1:"Treats the system as having no side effects.",l4:"Traces consequences across domain, scale or time, and states what the map cannot settle."},
  {crit:"Interpretation",prov:"UNESCO: deal with uncertainty",l1:"Presents the map with no reading of it.",l4:"Draws the conclusion, identifies the leverage point it reveals, and states what the remaining uncertainty means for acting."}],
 fromDeck:true,
 ex:{"Health, Medical and Life Sciences":"Map how lifestyle, access and policy interact to drive an outbreak.","Sciences":"Trace fertiliser runoff from soil to river to fish stocks.","Engineering":"Map how a procurement saving creates rework and emissions elsewhere.","Computer Science and Information Technology":"Trace how a data-centre efficiency gain shifts load and emissions elsewhere.","Mathematics and Statistics":"Model a loop where the output re-enters as input.","Education":"Map how one assessment policy reshapes teaching, behaviour and attainment.","Economics, Accounting, Business, Finance and Management":"Show how a packaging cost cut raises returns and complaints.","Language, Literature and Communications":"Analyse how one media frame spreads and shapes policy.","Sociology, Psychology and Human Development":"Map how school zoning shifts housing prices, then enrolment.","Architecture and Design":"Trace a building material from source to demolition, naming one off-site impact.","Agriculture, Forestry, Environmental Science and Food Science":"Trace how a crop switch affects soil, water and food security."}},

{n:2,key:"anticipatory",name:"Anticipatory Competency",one:"Work with futures",
 def:"Working with several possible futures at once, not assuming tomorrow extends today.",
 meaning:"Students separate the probable future from the possible and the desirable. They build scenarios that differ in substance rather than in optimism, test a decision against each, and apply caution where an outcome cannot be undone.",
 shift:"The shift is from one forecast to a range.",
 obs:["Builds scenarios that differ structurally, and names one future they want","Tests a decision against each and reports where it fails","Applies caution where a consequence is irreversible or the evidence is unsettled"],
 note:"Watch for best case / worst case / most likely \u2014 that is one scenario at three volumes. Structural difference is the criterion. Irreversibility is the most teachable idea here: it turns an abstract futures discussion into a decision filter.",
 methods:"Scenario building \u00b7 backcasting from a 2040 target \u00b7 futures wheel",
 ped:"Simulation and gamification \u00b7 scenario cases",
 evidence:"Scenario set, and a decision tested against each",
 rubric:[
  {crit:"Scenario construction",prov:"UNESCO: multiple futures; create one\u2019s own visions",l1:"One future, or three volumes of the same future.",l4:"Scenarios differ structurally, the driver separating each is named, and the desired future is argued for."},
  {crit:"Testing the decision",prov:"UNESCO: assess the consequences of actions",l1:"States a preferred option without testing it.",l4:"Tests the decision against each scenario and reports where and why it fails."},
  {crit:"Precaution and irreversibility",prov:"UNESCO: apply the precautionary principle",l1:"Treats every consequence as recoverable.",l4:"Separates reversible from irreversible and lets irreversibility shape the recommendation, including where the evidence is unsettled."},
  {crit:"Robust recommendation",prov:"UNESCO: deal with risks and changes",l1:"No recommendation, or one tied to a single future.",l4:"Recommends a robust option and names the signal that would trigger a change of course."}],
 ex:{"Health, Medical and Life Sciences":"Build three ageing-population futures; test one service model against each.","Sciences":"Test which lab findings hold under three structurally different climate futures.","Engineering":"Design drainage for three 2070 rainfall futures, not 1990 records.","Computer Science and Information Technology":"Build three AI-adoption futures; test one system design against each.","Mathematics and Statistics":"Compare model outputs under three structurally different assumption sets.","Education":"Build three graduate-labour-market futures; test one curriculum decision.","Economics, Accounting, Business, Finance and Management":"Stress-test a five-year strategy against three carbon-pricing futures.","Language, Literature and Communications":"Write one message that must hold across three different public moods.","Sociology, Psychology and Human Development":"Forecast three community futures; name the irreversible social outcomes.","Architecture and Design":"Design for three climate futures; name the irreversible commitments.","Agriculture, Forestry, Environmental Science and Food Science":"Build three resource-scarcity scenarios; state where the plan fails."}},

{n:3,key:"normative",name:"Normative Competency",one:"Negotiate values",
 def:"Recognising that sustainability decisions rest on values, and negotiating them openly.",
 meaning:"Every sustainability choice contains a judgement about what matters, who counts, and over what timeframe. Students surface those judgements including their own, separate a technical disagreement from a values conflict, and argue from a stated principle rather than a preference.",
 shift:"The shift is from 'what is correct' to 'on what basis are we deciding'.",
 obs:["Names the values in conflict, including their own","States who bears the cost and who gains","Justifies using an explicit, consistent principle"],
 note:"Most often written into a course outline and least often assessed, because technical lecturers are uncomfortable marking value reasoning. You are not marking which position the student takes \u2014 you mark whether values were surfaced, distribution analysed, and a principle applied consistently.",
 methods:"Value ranking \u00b7 ethical dilemma cases \u00b7 deliberative debate",
 ped:"Role-play and case-based \u00b7 SULAM",
 evidence:"Justification memo naming the principle applied",
 rubric:[
  {crit:"Surfacing values",prov:"UNESCO: reflect on the norms and values underlying one\u2019s own actions",l1:"Presents the decision as purely technical.",l4:"Names the values in conflict and shows how their own values shaped the choice they made."},
  {crit:"Distribution of cost and benefit",prov:"UNESCO: conflicting interests and trade-offs",l1:"Does not say who gains or who loses.",l4:"Analyses how cost and benefit fall across groups and over time."},
  {crit:"Principled justification",prov:"UNESCO: negotiate principles under uncertain knowledge and contradictions",l1:"States a preference with no reason.",l4:"Applies an explicit principle and shows it still holds where evidence is uncertain or two of their own principles conflict."},
  {crit:"Engaging the counter-position",prov:"UNESCO: negotiate, under contradiction",l1:"Ignores any opposing view.",l4:"States the strongest counter-argument and negotiates to a workable position, conceding what it earns without dropping the principle."}],
 fromDeck:true,
 ex:{"Health, Medical and Life Sciences":"Justify a rule for allocating scarce treatment; say who loses.","Sciences":"Decide whether to publish a finding that could be misused.","Engineering":"Choose between the legal discharge limit and the ecological one.","Computer Science and Information Technology":"Adjudicate a data-privacy trade-off; name who bears the cost.","Mathematics and Statistics":"Choose the fairness definition inside an allocation algorithm.","Education":"Weigh raising standards against widening access; state the principle.","Economics, Accounting, Business, Finance and Management":"Argue what a mine's rehabilitation provision should cover.","Language, Literature and Communications":"Examine whose story a translation keeps and whose it erases.","Sociology, Psychology and Human Development":"Decide whose voice counts in a community consultation.","Architecture and Design":"Weigh heritage conservation against housing need on one site.","Agriculture, Forestry, Environmental Science and Food Science":"Adjudicate between farm productivity and biodiversity on one landholding."}},

{n:4,key:"strategic",name:"Strategic Competency",one:"Build the pathway",
 def:"Turning an intention into a sequenced, resourced plan that somebody owns.",
 meaning:"Students find where a small intervention produces a large effect, then build the pathway: who acts, in what order, with what resources, against which obstacle, by when.",
 shift:"The shift is from proposing a goal to designing the route to it.",
 obs:["Identifies a leverage point and justifies why, against a non-standard option","Sequences actions with dependencies, owners and resources","Names the likely obstacle and a proportionate response"],
 note:"Students reach for awareness campaigns; leverage analysis usually points to defaults, procurement rules and pricing. Easiest of the eight to assess, because a plan is a concrete output.",
 methods:"Theory of change \u00b7 leverage analysis \u00b7 90-day action plan",
 ped:"Project-based learning",
 evidence:"Implementation plan with owners and sequence",
 rubric:[
  {crit:"Leverage point",prov:"UNESCO: innovative actions",l1:"Proposes an awareness campaign or a general goal.",l4:"Justifies why the leverage point moves the system more than the alternatives, having considered a non-standard option."},
  {crit:"Sequence and dependencies",prov:"UNESCO: implement; local level and further afield",l1:"Lists actions with no order.",l4:"Sequences with dependencies, shows why the order cannot be reversed, and what must hold beyond this site."},
  {crit:"Owners and resources",prov:"UNESCO: collectively develop",l1:"Names no owner and no resource.",l4:"Assigns owners and resources, tests them against what is available, and shows how those who must act were brought into the plan."},
  {crit:"Obstacles and response",prov:"UNESCO: implement",l1:"Assumes the plan proceeds unopposed.",l4:"Names the obstacle, who raises it, and a proportionate response; where carried out, reports what actually obstructed it."}],
 ex:{"Health, Medical and Life Sciences":"Plan medical-waste reduction with owners, sequence and the likely obstacle.","Sciences":"Plan how a lab cuts solvent use without halting research.","Engineering":"Sequence a retrofit, with owners and costs, so the building stays occupied.","Computer Science and Information Technology":"Plan to cut a software service's carbon cost; name the leverage point.","Mathematics and Statistics":"Identify which variable moves the system most, then sequence around it.","Education":"Design a 90-day plan to embed one sustainability practice.","Economics, Accounting, Business, Finance and Management":"Build a 90-day plan to shift one supplier, with costs.","Language, Literature and Communications":"Design a campaign that changes behaviour, not just awareness.","Sociology, Psychology and Human Development":"Plan an intervention starting with the most persuadable group.","Architecture and Design":"Sequence a low-carbon design pathway with dependencies and owners.","Agriculture, Forestry, Environmental Science and Food Science":"Plan watershed or farm management; state what must happen first."}},

{n:5,key:"collaboration",name:"Collaboration Competency",one:"Work across difference",
 def:"Working productively across difference of discipline, interest and power.",
 meaning:"Students find who holds relevant knowledge and who is affected, listen closely enough to represent another position accurately, handle disagreement without suppressing it or winning at all costs, and involve people while the design can still change.",
 shift:"The shift is from dividing work to integrating difference.",
 obs:["Represents accurately a position they disagree with","Identifies affected groups absent from the process","Helps resolve disagreement, and makes room for the party least able to insist"],
 note:"A group report is evidence of a group, not of an individual. Always pair it with an individual output \u2014 a revision log, a reflective account, a justified peer assessment.",
 methods:"Role-played negotiation \u00b7 cross-disciplinary teams \u00b7 peer critique",
 ped:"SULAM \u00b7 project-based \u00b7 role-play",
 evidence:"Individual revision log and justified peer assessment",
 rubric:[
  {crit:"Representing other positions",prov:"UNESCO: understand and respect the perspectives of others (empathy)",l1:"Describes only their own position.",l4:"States a disagreed-with position accurately enough that its holder would accept the account."},
  {crit:"Who is absent",prov:"UNESCO: facilitate collaborative and participatory problem solving",l1:"Considers only the people in the room.",l4:"Identifies absent groups and what their absence changed, or what changed once they were brought in."},
  {crit:"Handling disagreement",prov:"UNESCO: deal with conflicts in a group; empathic leadership",l1:"Avoids or suppresses the disagreement.",l4:"Works it through, makes room for the party least able to insist, and shows how it changed the outcome."},
  {crit:"Individual contribution",prov:"Institutional: moderation control; partly serves learn-from-others",l1:"No individual evidence; only the group product.",l4:"Documents what they changed or conceded, at whose prompting, and what they now understand differently."}],
 ex:{"Health, Medical and Life Sciences":"Reach one care plan with a multidisciplinary team that first disagreed.","Sciences":"Reach one conclusion with a team that read the data differently.","Engineering":"Resolve a clash between structural, mechanical and cost needs.","Computer Science and Information Technology":"Reconcile security, cost and usability across a cross-functional build.","Mathematics and Statistics":"Agree modelling assumptions with those who use the results.","Education":"Co-design a teaching intervention with a partner school.","Economics, Accounting, Business, Finance and Management":"Negotiate a supplier contract both sides can sustain.","Language, Literature and Communications":"Interpret between two sides without flattening either.","Sociology, Psychology and Human Development":"Co-design research with the community being researched.","Architecture and Design":"Reconcile client, planner and community needs in one scheme.","Agriculture, Forestry, Environmental Science and Food Science":"Co-develop practices with farmers whose priorities differ from yours."}},

{n:6,key:"critical",name:"Critical Thinking",one:"Question the claim",
 def:"Questioning claims, evidence, assumptions and framings \u2014 including your own.",
 meaning:"Students separate evidence from assertion, examine who made a claim and how it was measured, and question the framing of the problem itself: what the question makes visible and what it hides. They take a considered position rather than accepting or rejecting wholesale.",
 shift:"The shift is from evaluating the answer to interrogating the question.",
 obs:["Evaluates the source, method and limits of evidence","Identifies an assumption in the framing, or a standard practice accepted without justification","States the weakest point of their own position"],
 note:"Distinguish it from scepticism: critical thinking turns on the student's own position too, cynicism never does. The third behaviour is the highest-value rubric criterion in the whole set.",
 methods:"Claim audits \u00b7 greenwashing analysis \u00b7 method critique",
 ped:"Problem-based \u00b7 case-based",
 evidence:"Claim audit or source critique",
 rubric:[
  {crit:"Evidence",prov:"UNESCO: question opinions",l1:"Repeats claims as given.",l4:"Evaluates source, method and limits, and states what the evidence cannot show."},
  {crit:"Framing, norms and assumptions",prov:"UNESCO: question norms, practices and opinions",l1:"Accepts the question as posed.",l4:"Identifies the assumption or accepted practice, and whose interest it serves."},
  {crit:"Own position",prov:"UNESCO: reflect on one\u2019s own values, perceptions and actions",l1:"Asserts a position, or rejects everything.",l4:"States the weakest point, names what in their perception produced it, and responds."},
  {crit:"Warranted judgement",prov:"UNESCO: take a position in the sustainability discourse",l1:"Reaches a conclusion the evidence does not support.",l4:"Takes a position with the confidence the evidence warrants, and the evidence that would change it."}],
 ex:{"Health, Medical and Life Sciences":"Appraise evidence for an intervention, including funding and sample.","Sciences":"Audit a study's method, sample and limits before citing it.","Engineering":"Question whether the design brief solves the real problem.","Computer Science and Information Technology":"Evaluate a benchmark behind an AI-performance claim.","Mathematics and Statistics":"Expose the assumption that makes a statistic convincing.","Education":"Critique the evidence base for a popular teaching method.","Economics, Accounting, Business, Finance and Management":"Test three 'eco-friendly' claims against the evidence.","Language, Literature and Communications":"Analyse how word choice frames who gets blamed.","Sociology, Psychology and Human Development":"Ask what a survey question makes impossible to say.","Architecture and Design":"Interrogate a 'green building' rating against its own data.","Agriculture, Forestry, Environmental Science and Food Science":"Audit two competing green-material or yield claims."}},

{n:7,key:"selfaware",name:"Self-awareness",one:"Examine your role",
 def:"Examining your own role, values and impact inside the system you study.",
 meaning:"Students locate themselves in the problem \u2014 as beneficiary, contributor, bystander or agent \u2014 recognise how their background and discipline shaped how they framed it, and handle the emotional weight of these topics without dismissal or paralysis.",
 shift:"The shift is from studying the problem to being situated within it.",
 obs:["Locates their own role specifically, not in general","Says how their background shaped the framing","Names a change they control, its cost, and what they would have to stop wanting"],
 note:"The assessment risk is rewarding performed confession. Mark the specificity and the reasoning, never the sentiment. Reflection must be prompted \u2014 unprompted reflection produces sentiment, not assessable evidence.",
 methods:"Reflective journals with prompts \u00b7 footprint comparison",
 ped:"SULAM \u00b7 field and work-based learning",
 evidence:"Reflective account written against set prompts",
 rubric:[
  {crit:"Locating yourself",prov:"UNESCO: reflect on one\u2019s role in the community and wider society",l1:"Writes in general terms only.",l4:"Locates their role specifically in the immediate setting and the wider system, with evidence."},
  {crit:"Background and framing",prov:"Institutional: positionality construct",l1:"Presents their own view as neutral.",l4:"Shows how background and discipline shaped the framing, and names what that framing hid."},
  {crit:"Change and its cost",prov:"UNESCO: continually evaluate one\u2019s actions; deal with one\u2019s feelings and desires",l1:"States an intention with no cost attached.",l4:"Names the change and its cost, reasons about what makes it hard, and how they would know in six months whether it held."},
  {crit:"Specificity of evidence",prov:"Institutional: evidential control against rewarding fluency",l1:"General sentiment, no concrete instance.",l4:"Analyses one specific incident in depth and reasons from it."}],
 ex:{"Health, Medical and Life Sciences":"Reflect on how your background shapes whose account you trust.","Sciences":"State how your discipline shaped the question you asked.","Engineering":"Identify whose convenience your design prioritised, and its cost.","Computer Science and Information Technology":"Notice whose needs your default choices served, and who they excluded.","Mathematics and Statistics":"Notice which assumptions you chose because they were easier.","Education":"Notice how your own schooling shapes what you call good teaching.","Economics, Accounting, Business, Finance and Management":"Compare your own consumption with the advice you wrote.","Language, Literature and Communications":"Notice which register you default to, and who it excludes.","Sociology, Psychology and Human Development":"Write a positionality statement before entering the field.","Architecture and Design":"Ask whose comfort your design centres, and what a change would cost.","Agriculture, Forestry, Environmental Science and Food Science":"Notice which land use you treat as natural, and what that hides."}},

{n:8,key:"integrated",name:"Integrated Problem-solving",one:"Combine all seven",capstone:true,
 def:"Combining the other seven on a real problem to produce a workable option.",
 meaning:"Students choose which lens the problem needs first, sequence the others behind it, and produce a defensible option rather than a perfect answer. Integration is judgement about which competency this problem requires \u2014 not applying all seven at once.",
 shift:"The shift is from analysis to a decision somebody could act on.",
 obs:["Applies three or more lenses and shows what each revealed","Produces a viable option, and states who it includes and who it leaves out","States what it trades off, and who bears that"],
 note:"Placement: capstone, final-year project, industrial training and clinical practice. Where it is met mid-programme, assess it as emerging: mark all four levels as normal, set the attainment threshold at Developing, and declare that in the course outline. Do not cap the rubric.",
 methods:"Real-client projects \u00b7 design charrettes \u00b7 capstone defence",
 ped:"Capstone project \u00b7 work-based learning",
 evidence:"Capstone report with an oral defence",
 rubric:[
  {crit:"Choice and sequence of lenses",prov:"UNESCO: apply different frameworks; integrate the other competencies",l1:"Applies one lens, or names several without using any.",l4:"Applies three or more, shows what each revealed, and justifies the sequence."},
  {crit:"The option",prov:"UNESCO: viable, inclusive and equitable solution options",l1:"Describes the problem; recommends nothing actionable.",l4:"Produces an option that holds under real constraints and is defensible on equity grounds."},
  {crit:"Trade-offs",prov:"UNESCO: inclusive and equitable",l1:"Presents the option as costless.",l4:"States the trade-offs, who bears them, and what would change the recommendation."},
  {crit:"Defence under challenge",prov:"Institutional: assessment device for defensibility",l1:"Cannot answer questions on the choice.",l4:"Concedes a fair challenge and adjusts the option without collapsing it."}],
 ex:{"Health, Medical and Life Sciences":"Healthcare innovation project with a real partner, defended orally.","Sciences":"Final-year project on a real environmental problem with a client.","Engineering":"Capstone design with a live site, budget and community.","Computer Science and Information Technology":"Capstone system for a real client, with trade-offs stated.","Mathematics and Statistics":"Build a decision model for an organisation's real dilemma.","Education":"Design, deliver and evaluate a real teaching intervention.","Economics, Accounting, Business, Finance and Management":"Consultancy project delivering a defensible recommendation.","Language, Literature and Communications":"Design and deliver a real communication strategy for a partner.","Sociology, Psychology and Human Development":"Community-based research producing an actionable proposal.","Architecture and Design":"Capstone design for a real occupant, site and budget.","Agriculture, Forestry, Environmental Science and Food Science":"Integrated land or food-system project, defended before a panel."}}
];
const byKey=k=>C.find(c=>c.key===k);

const DISTINCT=[
 {a:"Systems",b:"Integrated",text:"Systems analyses how the parts interact. Integrated decides what to do."},
 {a:"Critical",b:"Normative",text:"Critical asks if a claim is true. Normative asks if it is right, and for whom."},
 {a:"Anticipatory",b:"Strategic",text:"Anticipatory imagines possible futures. Strategic builds the route."},
 {a:"Collaboration",b:"group work",text:"Group work divides labour. Collaboration integrates people who disagree."}
];

/* Method families from UNESCO (2017) Section 2.4 / guidebook Part 3.3, expanded for university use.
   develops[] follows the guidebook's DEVELOPS columns and the pedagogy-competency matrix (Part 3.4). */
const PEDAGOGIES=[
 {name:"Problem-Based Learning",fam:"Inquiry and problem-centred",does:"Work an ill-structured problem with no single right answer, define what they need to know, then learn it.",develops:["systems","critical","collaboration"],assess:"The problem definition and reasoning trail, plus an individual reasoning log.",watch:"Marking only the solution rewards the group that guessed well; the competency is in how the problem was framed."},
 {name:"Case-Based Learning",fam:"Inquiry and problem-centred",does:"Analyse a real case with incomplete information and defend a recommendation.",develops:["critical","normative","systems"],assess:"The analysis and the justification of the recommendation."},
 {name:"Guided Inquiry",fam:"Inquiry and problem-centred",does:"Generate the questions before being given the method.",develops:["critical","systems"],assess:"The quality and framing of the questions asked."},
 {name:"Jigsaw",fam:"Inquiry and problem-centred",does:"Master one component, then teach it to a group that needs it.",develops:["collaboration","systems"],assess:"An individual mastery check plus the group product."},
 {name:"Socratic Seminar",fam:"Inquiry and problem-centred",does:"Rule-governed discussion of a difficult text or case.",develops:["critical","normative"],assess:"A position paper written after and revised in light of the seminar."},
 {name:"Project-Based Learning",fam:"Project and production",does:"Work over weeks toward an output for a defined client, with milestones.",develops:["strategic","integrated","collaboration"],assess:"Milestone reviews, the output, and an individual contribution record.",watch:"A polished output can hide a weak process; assess at milestones, not only at submission."},
 {name:"Design Thinking",fam:"Project and production",does:"Empathise, define, ideate, prototype and test with real users.",develops:["collaboration","selfaware","strategic"],assess:"The problem reframing after user contact."},
 {name:"Design Charrette",fam:"Project and production",does:"Time-boxed collaborative design against real constraints.",develops:["integrated","collaboration"],assess:"The trade-off log and the defence of the final option."},
 {name:"Studio Critique",fam:"Project and production",does:"Work presented and critiqued publicly at intervals.",develops:["critical","selfaware"],assess:"The revision made in response, not the final piece."},
 {name:"Challenge-Based Learning",fam:"Project and production",does:"An organisation poses a genuine challenge to solve.",develops:["integrated","strategic"],assess:"The client deliverable plus an individual justification."},
 {name:"SULAM / Service Learning",fam:"Experiential and work-based",does:"Apply content to a genuine community need, with the partner as collaborator.",develops:["collaboration","selfaware","normative"],assess:"A prompted reflective journal, partner feedback, and the delivered output.",watch:"Hours served is not evidence, and neither is gratitude; mark the specificity of the reflection."},
 {name:"Field and Work-Based Learning",fam:"Experiential and work-based",does:"Work in a site, lab or workplace under real, non-idealised conditions.",develops:["systems","selfaware","integrated"],assess:"Supervised observation against criteria, plus an interpretive account.",watch:"Attendance is not competence; observation needs published criteria or it becomes an impression."},
 {name:"Living Lab",fam:"Experiential and work-based",does:"Use the campus or neighbourhood as the site of a real intervention.",develops:["strategic","integrated","collaboration"],assess:"The intervention, its monitoring plan, and what failed."},
 {name:"Role-Play",fam:"Simulation and role",does:"Take a stakeholder role and decide under constraints.",develops:["normative","collaboration"],assess:"The written justification afterwards, and the revision after challenge.",watch:"Performance skill is not competence; a confident speaker with weak reasoning should not score highly."},
 {name:"Negotiation / Mock Hearing",fam:"Simulation and role",does:"Reach agreement across conflicting interests.",develops:["collaboration","normative"],assess:"The agreement, the concession log, and each party's account of the other."},
 {name:"Systems Simulation",fam:"Simulation and role",does:"Operate a model with delayed, non-obvious consequences.",develops:["systems","anticipatory"],assess:"The debrief: strategy used, system inferred, what they would change."},
 {name:"Futures Workshop",fam:"Simulation and role",does:"Critique the present, build a desired future, then plan toward it.",develops:["anticipatory","strategic"],assess:"The scenario set, the desired future argued for, and a decision tested against it.",watch:"The utopia stage is where UNESCO's create-one's-own-visions clause is actually practised; do not skip it."},
 {name:"Structured Academic Controversy",fam:"Dialogic and deliberative",does:"Argue a position, then its opposite, then seek a joint position.",develops:["normative","collaboration","critical"],assess:"The joint statement plus each student's account of what changed their mind."},
 {name:"Deliberative Forum",fam:"Dialogic and deliberative",does:"Weigh options as a mini-public with briefing materials.",develops:["normative","collaboration"],assess:"A reasoned recommendation and a minority report."},
 {name:"Prompted Reflective Journal",fam:"Reflective and narrative",does:"Write to specific prompts at set intervals.",develops:["selfaware"],assess:"Reasoning about what they want and resist, never the warmth of the sentiment.",watch:"Highest risk of rewarding fluency; anchor every criterion in specificity."},
 {name:"Critical Incident Analysis",fam:"Reflective and narrative",does:"Analyse one moment where assumptions were challenged.",develops:["selfaware","critical"],assess:"Depth on one incident, not breadth."},
 {name:"Backcasting",fam:"Analytical tools",does:"Work backward from a desired future to milestones and dependencies.",develops:["anticipatory","strategic"],assess:"The backward pathway with milestones and the assumptions it rests on."},
 {name:"Causal Loop Diagram",fam:"Analytical tools",does:"Map elements and the loops that connect them.",develops:["systems"],assess:"The annotated map with loop polarity, interpretation, and what it cannot settle."},
 {name:"Leverage Point Analysis",fam:"Analytical tools",does:"Rank where a small intervention moves the system most.",develops:["strategic"],assess:"Ranked intervention points with justification."},
 {name:"Claim and Practice Audit",fam:"Analytical tools",does:"Interrogate a claim and the accepted practice behind it.",develops:["critical"],assess:"Source, method, limits, the norm the practice rests on, and what the evidence cannot show."},
 {name:"Trade-off Matrix",fam:"Analytical tools",does:"Weigh options against criteria and name who bears each cost.",develops:["integrated"],assess:"The matrix plus who bears each cost."}
];
/* Gamification develops motivation only; the guidebook is explicit that it evidences no competency on its own. */

/* ---- quiz 1 hand-written items ---- */
const DISTINGUISH=[
 {stem:"A student maps how a fertiliser subsidy changes farm practice, river quality and fishery income \u2014 and stops there, recommending nothing.",opts:["systems","integrated"],ans:"systems",why:"Analysis of how the parts interact is Systems Thinking. It becomes Integrated Problem-solving only when the student must choose a defensible option and own its trade-offs."},
 {stem:"A student is given a real client, a real budget and three competing pressures, and must deliver one recommendation they can defend.",opts:["systems","integrated"],ans:"integrated",why:"A decision somebody could act on, with trade-offs named, is Integrated Problem-solving. Place it in capstone or final-year work only."},
 {stem:"A student examines who funded a study, how the sample was drawn, and what the method could not detect.",opts:["critical","normative"],ans:"critical",why:"Interrogating evidence, method and framing is Critical Thinking. Normative would ask whether acting on the finding is right, and for whom."},
 {stem:"A student argues the discharge limit should protect downstream fishers even though the legal limit is looser, and states the principle they are applying.",opts:["critical","normative"],ans:"normative",why:"Values in conflict, distribution of cost and benefit, and an explicit principle \u2014 that is Normative Competency. You mark the reasoning, not the position."},
 {stem:"A student builds three futures for the campus water supply that differ in structure, then reports which decision fails in each.",opts:["anticipatory","strategic"],ans:"anticipatory",why:"Several possible futures, tested against a decision, is Anticipatory. Strategic begins when they sequence who acts, with what resources, against which obstacle."},
 {stem:"A student names the leverage point, orders the actions, assigns owners and costs, and names the obstacle most likely to stop it.",opts:["anticipatory","strategic"],ans:"strategic",why:"Sequenced, resourced, owned \u2014 Strategic Competency. It is the easiest of the eight to assess because the plan is a concrete output."},
 {stem:"Four students split a report into four sections, write them separately, and staple them together the night before.",opts:["collaboration","neither"],ans:"neither",why:"That is divisible group work \u2014 evidence of a group, not of collaboration. A divisible task cannot evidence this competency, and most existing group assignments are divisible."},
 {stem:"A student must represent, accurately and in writing, the position of a stakeholder they disagree with before the team's design is finalised.",opts:["collaboration","neither"],ans:"collaboration",why:"Representing a position you disagree with, and involving affected people while the design can still change, is the observable core of Collaboration."}
];

/* ---- quiz 2 hand-written items ---- */
const FAULTS=[
 {stem:"\u201cLevel 4: Excellent analysis. Level 3: Good analysis. Level 2: Fair analysis. Level 1: Poor analysis.\u201d",ans:"adjectives",why:"Adjectives, not descriptors. That is a grading scale \u2014 the student cannot use it to improve and you cannot defend it when the mark is disputed."},
 {stem:"\u201cLevel 4: identifies four or more feedback loops. Level 2: identifies one feedback loop.\u201d",ans:"counting",why:"Levels separated by counting. It measures volume, not competence \u2014 counting feels objective, which is exactly why the fault spreads. Quality gradients are the real work."},
 {stem:"\u201cLevel 4: the report is well structured, referenced correctly and free of grammatical errors.\u201d",ans:"restates",why:"A criterion that restates the brief. It assesses report writing, not the competency, and would score the same for a student who never reasoned about the system."},
 {stem:"The rubric is finalised while marking, after students have submitted, so it fits the range of work received.",ans:"after",why:"Written after the task. A rubric students never saw is a marking aid, not an assessment design \u2014 and it fails the requirement that criteria are published before they start."},
 {stem:"\u201cLevel 4: states the boundary, justifies what was excluded, and shows how a different boundary changes the conclusion.\u201d",ans:"none",why:"No fault. It describes what the work looks like, differentiates by quality rather than quantity, and comes straight from an observable behaviour."},
 {stem:"\u201cLevel 3: demonstrates a satisfactory level of critical engagement with the material.\u201d",ans:"adjectives",why:"Adjectives again, wearing academic clothing. Satisfactory engagement is not observable \u2014 replace it with what the student's work actually shows."}
];
const ALIGNFAIL=[
 {stem:"A course outline shows the SDG 12 logo. Nothing in the content, tasks or readings connects to responsible consumption.",ans:"decoration",why:"SDG as decoration. Every claim in an alignment table has to survive someone reading the actual marked work."},
 {stem:"The outline names Collaboration Competency. No course learning outcome requires students to work across difference, and no task produces evidence of it.",ans:"nocld",why:"Competency with no CLO. Named in the outline but carried by no outcome \u2014 this is the finding an auditor reaches fastest."},
 {stem:"One CLO is mapped to SDGs 4, 6, 11, 12 and 13.",ans:"fivesdg",why:"One CLO, five SDGs. Broad mapping dilutes everything \u2014 choose one primary goal, at most two."},
 {stem:"The CLOs were written first. The PLO column was filled in afterwards so the template would be complete.",ans:"reverse",why:"Reverse-engineered PLO mapping. Build in order: content, SDG, competency, CLO, then the upward mapping."},
 {stem:"The CLO names Normative Competency. The exam question asks students to calculate the compliant discharge rate.",ans:"taskmiss",why:"Task misses the competency. It evidences the content of the CLO but not its competency \u2014 the most widespread failure, and the least admitted."}
];
const TRAPQ=[
 {stem:"Six students submit one group report on a community project. The lecturer gives all six the same Collaboration mark.",ans:"group",why:"Marking the group. A group report is evidence of a group, not of an individual \u2014 attach a short individual output such as a revision log or a justified peer assessment."},
 {stem:"A reflective journal is graded on how deeply the student appears to care about climate change.",ans:"sincerity",why:"Marking sincerity. Mark specificity and reasoning, never sentiment \u2014 otherwise you reward performed confession."},
 {stem:"Two students argue opposite positions on a discharge standard, each naming values, analysing who bears the cost, and applying a principle consistently. The lecturer marks down the one whose position they disagree with.",ans:"position",why:"Marking the position. Both students can reach level 4 \u2014 the rubric applies to the quality of reasoning, not to which side the student took."}
];

/* ============================================================
   STORAGE
   ============================================================ */
const hasS=typeof window!=="undefined"&&window.storage&&typeof window.storage.get==="function";
const FB="esd8:";
const S={
 async set(k,v,shared=false){
  if(hasS){try{return await window.storage.set(k,JSON.stringify(v),shared);}catch(e){}}
  try{localStorage.setItem(FB+(shared?"pub:":"")+k,JSON.stringify(v));return true;}catch(e){return null;}
 },
 async get(k,shared=false){
  if(hasS){try{const r=await window.storage.get(k,shared);return r?JSON.parse(r.value):null;}catch(e){}}
  try{const r=localStorage.getItem(FB+(shared?"pub:":"")+k);return r?JSON.parse(r):null;}catch(e){return null;}
 },
 async list(prefix,shared=false){
  if(hasS){try{const r=await window.storage.list(prefix,shared);return (r&&r.keys)||[];}catch(e){}}
  const p=FB+(shared?"pub:":"")+prefix,out=[];
  try{for(let i=0;i<localStorage.length;i++){const k=localStorage.key(i);if(k.indexOf(p)===0)out.push(k.slice((FB+(shared?"pub:":"")).length));}}catch(e){}
  return out;
 }
};

/* ============================================================
   STATE
   ============================================================ */
const state={pid:null,code:"",disc:"",seen:{},q1:null,q2:null,q3:null,build:{course:"",cluster:"",sdg:"",comps:[],clo:{},cloMode:"two",cloOne:"",activity:{},output:{},rubric:{},assignment:""}};
function uid(){return "p"+Math.random().toString(36).slice(2,9)+Date.now().toString(36).slice(-4);}
async function loadLocal(){
  let pid=await S.get("esd8v2:pid");
  if(!pid){pid=uid();await S.set("esd8v2:pid",pid);}
  state.pid=pid;
  const saved=await S.get("esd8v2:progress");
  if(saved)Object.assign(state,saved,{pid});
  if(!state.build)state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},cloMode:"two",cloOne:"",activity:{},output:{},rubric:{},assignment:""};
  if(typeof state.build.assignment!=="string")state.build.assignment="";
  if(state.build.cloMode!=="one"&&state.build.cloMode!=="two")state.build.cloMode="two";
  if(typeof state.build.cloOne!=="string")state.build.cloOne="";
}
let saveTimer=null;
function saveLocal(){
  clearTimeout(saveTimer);
  saveTimer=setTimeout(()=>{
    S.set("esd8v2:progress",{code:state.code,disc:state.disc,seen:state.seen,q1:state.q1,q2:state.q2,q3:state.q3,build:state.build});
    const el=document.getElementById("railSaved");if(el)el.textContent="Saved on this device.";
  },400);
}
function markSeen(v){ if(["understand","lens","pedagogy","assess"].includes(v)){state.seen[v]=true;saveLocal();paintTicks();} }
function paintTicks(){
  document.querySelectorAll("[data-tick]").forEach(t=>{
    const k=t.dataset.tick;
    if(k==="quiz1")t.textContent=state.q1?"\u2713":"";
    else if(k==="quiz2")t.textContent=state.q2?"\u2713":"";
    else if(k==="quiz3")t.textContent=state.q3?"\u2713":"";
    else t.textContent=state.seen[k]?"\u2713":"";
  });
}

/* ============================================================
   NAV
   ============================================================ */
const VIEWS=["understand","lens","quiz1","pedagogy","assess","quiz2","build","quiz3","detail"];
function show(v){
  VIEWS.forEach(x=>{const el=document.getElementById("view-"+x);if(el)el.classList.toggle("hidden",x!==v);});
  document.querySelectorAll(".navbtn").forEach(b=>b.setAttribute("aria-current",String(b.dataset.view===v)));
  markSeen(v);
  window.scrollTo({top:0,behavior:"instant"});
}
document.querySelectorAll(".navbtn").forEach(b=>b.addEventListener("click",()=>{
  const v=b.dataset.view;show(v);
  if(v==="lens")renderLens();
  if(v==="build")renderBuild();
}));
document.querySelectorAll("[data-goto]").forEach(b=>b.addEventListener("click",()=>{
  const v=b.dataset.goto;show(v);if(v==="lens")renderLens();if(v==="build")renderBuild();
}));

/* ============================================================
   01 UNDERSTAND
   ============================================================ */
function renderLedger(){
  const L=document.getElementById("ledger");L.innerHTML="";
  C.forEach(c=>{
    const b=document.createElement("button");
    b.className="lrow"+(c.capstone?" capstone":"");
    b.innerHTML=`<span class="idx">${String(c.n).padStart(2,"0")}</span>
      <span class="nm">${c.name}${c.capstone?' <span class="tag amber" style="margin-left:6px">capstone</span>':''}</span>
      <span class="one">${c.def}</span><span class="go">${c.one} \u2192</span>`;
    b.addEventListener("click",()=>openDetail(c.key,"understand"));
    L.appendChild(b);
  });
  const D=document.getElementById("distinctions");D.innerHTML="";
  DISTINCT.forEach(d=>{
    const el=document.createElement("div");
    el.innerHTML=`<div class="mono" style="font-size:12.5px;color:var(--ink-soft);letter-spacing:.06em">${d.a.toUpperCase()} &nbsp;vs&nbsp; ${d.b.toUpperCase()}</div><p style="margin-top:6px;font-size:15px">${d.text}</p>`;
    D.appendChild(el);
  });
}
let detailReturn="understand";
function openDetail(key,from){
  detailReturn=from||"understand";
  const c=byKey(key);
  const d=state.disc;
  document.getElementById("detailBody").innerHTML=`
    <div class="eyebrow">Competency ${String(c.n).padStart(2,"0")} of 08</div>
    <h1>${c.name}</h1>
    <p class="lede">${c.def}</p>
    <div class="grid2">
      <div class="card"><span class="tag">What it means</span><p style="margin-top:12px">${c.meaning}</p><div class="shift">${c.shift}</div></div>
      <div class="card"><span class="tag amber">Observable when a student\u2026</span>
        <p style="margin:10px 0 4px;font-size:13.4px;color:var(--ink-soft)">These three become the rubric criteria in stage 05.</p>
        <ul class="obslist">${c.obs.map(o=>`<li>${o}</li>`).join("")}</ul></div>
    </div>
    <div class="callout"><strong>Facilitator note.</strong> ${c.note}</div>
    ${d?`<div class="card"><span class="tag slate">In ${d}</span><h3 style="margin:12px 0 6px">${c.ex[d]}</h3>
      <p style="font-size:13.6px;color:var(--ink-soft)">Adapt the wording; keep the demand.</p></div>`:
      `<div class="card"><p style="margin:0;color:var(--ink-soft)">Set your discipline in stage 02 to see this competency in your own field.</p></div>`}
    <p class="noprint"><button class="btn ghost small" id="prevC">\u2190 ${C[(c.n+6)%8].name}</button>
    <button class="btn ghost small" id="nextC">${C[c.n%8].name} \u2192</button></p>`;
  show("detail");
  document.getElementById("prevC").addEventListener("click",()=>openDetail(C[(c.n+6)%8].key,detailReturn));
  document.getElementById("nextC").addEventListener("click",()=>openDetail(C[c.n%8].key,detailReturn));
}
document.getElementById("backBtn").addEventListener("click",()=>{show(detailReturn);if(detailReturn==="lens")renderLens();});
/* ============================================================
   02 DISCIPLINE LENS
   ============================================================ */
function fillDisc(){
  const s=document.getElementById("disc");s.innerHTML="";
  const b=document.createElement("option");b.value="";b.textContent="\u2014 choose your discipline \u2014";s.appendChild(b);
  DISCIPLINES.forEach(d=>{const o=document.createElement("option");o.value=d;o.textContent=d;s.appendChild(o);});
  s.value=state.disc||"";
  s.addEventListener("change",e=>{state.disc=e.target.value;document.getElementById("railDisc").textContent=state.disc||"not set";saveLocal();renderLens();});
}
function renderLens(){
  const out=document.getElementById("lensOut");
  if(!state.disc){out.innerHTML=`<div class="card"><p style="margin:0;color:var(--ink-soft)">Choose a discipline above and the eight competencies reappear as tasks a student in your field would be given.</p></div>`;return;}
  out.innerHTML=`<div class="ledger">${C.map(c=>`
    <div class="lrow" style="cursor:default" data-nohover>
      <span class="idx">${String(c.n).padStart(2,"0")}</span>
      <span class="nm">${c.name}</span>
      <span class="one" style="color:var(--ink);font-size:15px">${c.ex[state.disc]}</span>
      <span class="go">${c.one}</span>
    </div>`).join("")}</div>
    <div class="card" style="margin-top:24px"><span class="tag slate">Compare</span>
      <h3 style="margin:12px 0 8px">The same competency, elsewhere</h3>
      <p style="font-size:14.6px;color:var(--ink-soft)">Useful when you teach a shared or service course, or when a colleague's version helps you see your own.</p>
      <label class="fl" for="cmpPick">Show all eight as they appear in</label>
      <select id="cmpPick">${DISCIPLINES.filter(d=>d!==state.disc).map(d=>`<option>${d}</option>`).join("")}</select>
      <div id="cmpOut" style="margin-top:14px"></div>
    </div>`;
  const pick=document.getElementById("cmpPick");
  const paint=()=>{
    document.getElementById("cmpOut").innerHTML=`<table class="tbl"><tbody>${C.map(c=>`<tr><td class="k">${c.name}</td><td>${c.ex[pick.value]}</td></tr>`).join("")}</tbody></table>`;
  };
  pick.addEventListener("change",paint);paint();
}

/* ============================================================
   QUIZ ENGINE
   ============================================================ */
function shuffle(a){a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]];}return a;}

function buildQ1(){
  const items=[];
  const pool=[];
  C.forEach(c=>{
    const ob=c.obs[Math.floor(Math.random()*c.obs.length)];
    pool.push({type:"identify",comp:c.key,stem:`A student ${ob.charAt(0).toLowerCase()+ob.slice(1)}. Which competency is this evidence of?`,why:c.shift});
    pool.push({type:"identify",comp:c.key,stem:`\u201c${c.def}\u201d Which competency is being described?`,why:c.meaning.split(".")[0]+"."});
  });
  shuffle(pool).slice(0,6).forEach(x=>items.push(x));
  const d=state.disc||"Engineering";
  shuffle(C).slice(0,4).forEach(c=>items.push({type:"field",comp:c.key,stem:`A task set in ${d}: \u201c${c.ex[d]}\u201d Which competency does it primarily carry?`,why:c.def}));
  shuffle(DISTINGUISH).slice(0,5).forEach(x=>items.push(Object.assign({type:"distinguish"},x)));
  return shuffle(items);
}

function buildQ2(){
  const items=[];
  shuffle(FAULTS).slice(0,3).forEach(f=>items.push({type:"fault",stem:f.stem,q:"Which rubric fault is this?",ans:f.ans,why:f.why,
    opts:[{v:"adjectives",t:"Adjectives, not descriptors"},{v:"counting",t:"Levels separated by counting"},{v:"restates",t:"Criterion restates the brief"},{v:"after",t:"Written after the task"},{v:"none",t:"No fault \u2014 this one works"}]}));
  shuffle(ALIGNFAIL).slice(0,3).forEach(f=>items.push({type:"align",stem:f.stem,q:"Which alignment failure is this?",ans:f.ans,why:f.why,
    opts:[{v:"decoration",t:"SDG as decoration"},{v:"nocld",t:"Competency with no CLO"},{v:"fivesdg",t:"One CLO, five SDGs"},{v:"reverse",t:"Reverse-engineered PLO mapping"},{v:"taskmiss",t:"Task misses the competency"}]}));
  shuffle(TRAPQ).slice(0,3).forEach(f=>items.push({type:"trap",stem:f.stem,q:"Which marking trap is this?",ans:f.ans,why:f.why,
    opts:[{v:"group",t:"Marking the group"},{v:"sincerity",t:"Marking sincerity"},{v:"position",t:"Marking the position"}]}));
  shuffle(C).slice(0,2).forEach(c=>items.push({type:"evidence",comp:c.key,stem:`Your course assesses ${c.name}. Which output carries the evidence?`,ans:c.key,why:`${c.evidence}. Choose the output first \u2014 the rubric follows from it.`,
    opts:shuffle(shuffle(C.filter(x=>x.key!==c.key)).slice(0,3).map(x=>({v:x.key,t:x.evidence})).concat([{v:c.key,t:c.evidence}]))}));
  shuffle(PEDAGOGIES).slice(0,2).forEach(p=>{
    const right=p.develops[0];
    items.push({type:"pedagogy",comp:right,stem:`${p.name}: ${p.does} Which competency does it develop most naturally?`,ans:right,why:`${p.name} develops ${p.develops.map(k=>byKey(k).name).join(", ")}. Assess it by: ${p.assess}`,
      opts:shuffle(shuffle(C.filter(x=>!p.develops.includes(x.key))).slice(0,3).map(x=>({v:x.key,t:x.name})).concat([{v:right,t:byKey(right).name}]))});
  });
  items.push({type:"task",stem:"\u201cDefine systems thinking and explain its importance.\u201d",q:"Does this assess the competency?",ans:"no",comp:"systems",
    opts:[{v:"yes",t:"Yes"},{v:"no",t:"No"}],
    why:"A student who memorised the lecture scores full marks. There is nothing here to build four rubric levels from except length and polish."});
  items.push({type:"task",stem:"\u201cDefine the system boundary and justify what you excluded. Identify one feedback loop. State one consequence appearing elsewhere.\u201d",q:"Does this assess the competency?",ans:"yes",comp:"systems",
    opts:[{v:"yes",t:"Yes"},{v:"no",t:"No"}],
    why:"The student must perform the competency to answer at all, and each clause becomes one rubric criterion."});
  return shuffle(items);
}

function buildQ3(){
  // Real tasks from the guidebook's discipline examples (Appendix A).
  const opt=key=>shuffle(shuffle(C.filter(x=>x.key!==key)).slice(0,3).map(x=>({v:x.key,t:x.name})).concat([{v:key,t:byKey(key).name}]));
  const which=[
   {comp:"systems",cl:"Sciences",task:"Trace how fertiliser runoff moves from soil to river to fish stocks. State the boundary, name one effect appearing in the economic or social domain, and state the remaining uncertainty.",
    why:"Mapping how the parts interact across domains, and stating what the map cannot settle, is Systems Thinking. It becomes Integrated only when a defensible option is chosen and owned."},
   {comp:"normative",cl:"Engineering",task:"Write a two-page memo on whether to design to the legal discharge limit or the ecological one. Name the values in conflict including your own, state who bears the cost, apply one principle consistently, and answer the strongest objection.",
    why:"Values in conflict, distribution of cost and benefit, and a principle applied consistently is Normative. Critical would ask whether a claim is true, not whether acting on it is right."},
   {comp:"strategic",cl:"Economics, Accounting, Business, Finance and Management",task:"Build a 90-day plan to shift one supplier to sustainable sourcing, with costs, owners, the agreements it depends on, and the obstacle most likely to derail it.",
    why:"A sequenced, resourced, owned plan against an obstacle is Strategic. Anticipatory imagines futures; Strategic builds the route to one."},
   {comp:"critical",cl:"Economics, Accounting, Business, Finance and Management",task:"Test three sustainable product claims against the evidence. Identify what each claim's framing hides and which industry practice makes the framing normal. State which claim, if any, you would stand behind.",
    why:"Interrogating evidence and framing, then taking a position, is Critical Thinking. The stated position is criterion 4, the highest-value move in the set."},
   {comp:"integrated",cl:"Engineering",task:"Capstone design for a real site and budget. Show what three competencies each revealed and which framework each brought, produce one option that is viable, inclusive and equitable, state its trade-offs, and defend it orally.",
    why:"Combining several lenses into one defensible, equitable option with an oral defence is Integrated Problem-solving. Place it in capstone or final-year work."}
  ];
  const suit=[
   {comp:"collaboration",suitable:"no",task:"Define collaboration and explain why it matters in teamwork.",
    why:"No. A student who memorised a definition scores full marks without ever working across difference. It assesses recall, not the competency."},
   {comp:"collaboration",suitable:"no",task:"Four students split a report into four sections, write them separately, and staple them together the night before.",
    why:"No. That is divisible group work \u2014 evidence of a group, not of collaboration. Make the task non-divisible and attach an individual output such as a revision log."},
   {comp:"selfaware",suitable:"yes",task:"Reflective account against set prompts: name a change in your own practice, its cost to you, and how you would know in six months whether it held.",
    why:"Yes. It is prompted, anchored in a specific change and its cost, and asks for follow-up evidence \u2014 exactly the Self-awareness behaviours. Mark the reasoning, never the sentiment."},
   {comp:"systems",suitable:"no",task:"Given a real client, a real budget and three competing pressures, deliver one recommendation you can defend, with the trade-offs named.",
    why:"No. Producing and defending a single option with trade-offs is Integrated Problem-solving. Systems Thinking analyses how the parts interact; it does not decide the option."},
   {comp:"anticipatory",suitable:"yes",task:"Construct three futures for AI adoption that differ in mechanism, plus a preferred future you argue for, and test one system design against each.",
    why:"Yes. Structurally different scenarios, a desired future argued for, and a decision tested against each are the Anticipatory behaviours, including UNESCO's create-one's-own-visions clause."}
  ];
  const items=[];
  which.forEach(w=>items.push({type:"whichcomp",comp:w.comp,ans:w.comp,
    stem:`A real assignment set in ${w.cl}: \u201c${w.task}\u201d`,q:"Which competency does it primarily assess?",why:w.why,opts:opt(w.comp)}));
  suit.forEach(su=>items.push({type:"suit",comp:su.comp,ans:su.suitable,
    stem:`\u201c${su.task}\u201d`,q:`Is this task suitable to assess ${byKey(su.comp).name}?`,why:su.why,
    opts:[{v:"yes",t:"Yes \u2014 it assesses the competency"},{v:"no",t:"No \u2014 it does not"}]}));
  return shuffle(items);
}
function optionsFor(item){
  if(item.opts && typeof item.opts[0]==="object") return item.opts;
  if(item.type==="identify"||item.type==="field"){
    const wrong=shuffle(C.filter(c=>c.key!==item.comp)).slice(0,3).map(c=>({v:c.key,t:c.name}));
    return shuffle(wrong.concat([{v:item.comp,t:byKey(item.comp).name}]));
  }
  if(item.type==="distinguish"){
    return item.opts.map(v=>({v,t:v==="neither"?"Neither \u2014 this is divisible group work":byKey(v).name}));
  }
  return [{v:"yes",t:"Yes"},{v:"no",t:"No"}];
}
function answerOf(i){return (i.type==="identify"||i.type==="field")?i.comp:i.ans;}
function labelOf(item,v){
  const o=optionsFor(item).find(x=>x.v===v);return o?o.t:v;
}

const RUN={};
function startQuiz(id){
  const items = id==="q1"?buildQ1():id==="q2"?buildQ2():buildQ3();
  RUN[id]={items,i:0,score:0,total:0,perComp:{},perType:{}};
  document.getElementById(id+"intro").classList.add("hidden");
  document.querySelector(`[data-done="${id}"]`).classList.add("hidden");
  const run=document.querySelector(`[data-run="${id}"]`);
  run.classList.remove("hidden");
  renderQ(id);
}
document.querySelectorAll("[data-start]").forEach(b=>b.addEventListener("click",()=>startQuiz(b.dataset.start)));

function renderQ(id){
  const r=RUN[id],item=r.items[r.i],run=document.querySelector(`[data-run="${id}"]`);
  run.innerHTML=`
    <div class="progressbar"><i style="width:${r.i/r.items.length*100}%"></i></div>
    <div class="mono" style="display:flex;justify-content:space-between;font-size:12.5px;color:var(--ink-soft)">
      <span>Question ${r.i+1} of ${r.items.length}</span><span>${item.type.toUpperCase()}</span></div>
    <div class="card" style="margin-top:10px">
      <h3 style="line-height:1.35;margin-bottom:16px">${item.stem}${item.q?`<br><span style="font-weight:500;color:var(--ink-soft);font-size:16px">${item.q}</span>`:""}</h3>
      <div class="opts"></div><div class="fb"></div>
      <div style="margin-top:14px"><button class="btn small action next hidden"></button></div>
    </div>`;
  const box=run.querySelector(".opts");
  optionsFor(item).forEach(o=>{
    const b=document.createElement("button");b.className="opt";b.textContent=o.t;
    b.addEventListener("click",()=>grade(id,o.v,b));
    box.appendChild(b);
  });
  run.querySelector(".next").addEventListener("click",()=>{
    if(r.i===r.items.length-1){finishQuiz(id);}else{r.i++;renderQ(id);}
  });
}
function grade(id,chosen,btn){
  const r=RUN[id],item=r.items[r.i],correct=answerOf(item),ok=chosen===correct;
  const run=document.querySelector(`[data-run="${id}"]`);
  [...run.querySelectorAll(".opt")].forEach(b=>{b.disabled=true;b.classList.add("dim");});
  btn.classList.remove("dim");btn.classList.add(ok?"correct":"wrong");
  r.total++;if(ok)r.score++;
  const ck=item.comp&&byKey(item.comp)?item.comp:null;
  if(ck){const p=r.perComp[ck]||{c:0,n:0};p.n++;if(ok)p.c++;r.perComp[ck]=p;}
  const t=r.perType[item.type]||{c:0,n:0};t.n++;if(ok)t.c++;r.perType[item.type]=t;
  run.querySelector(".fb").innerHTML=`<div class="feedback"><strong>${ok?"Correct.":"Not quite \u2014 the answer is \u201c"+labelOf(item,correct)+"\u201d."}</strong> ${item.why}</div>`;
  const nb=run.querySelector(".next");nb.classList.remove("hidden");
  nb.textContent=(r.i===r.items.length-1)?"See your results":"Next question";
}
function finishQuiz(id){
  const r=RUN[id];
  document.querySelector(`[data-run="${id}"]`).classList.add("hidden");
  const res={score:r.score,total:r.total,perComp:r.perComp,perType:r.perType,at:new Date().toISOString()};
  state[id]=res;saveLocal();paintTicks();
  const pct=Math.round(r.score/r.total*100);
  const weak=Object.entries(r.perComp).filter(([k,v])=>v.c/v.n<0.6).map(([k])=>byKey(k).name);
  const typeNames={identify:"Identifying from behaviour",field:"Recognising it in your field",distinguish:"Telling the confused pairs apart",fault:"Diagnosing rubric faults",align:"Spotting alignment failures",trap:"Spotting marking traps",evidence:"Choosing the evidence output",pedagogy:"Matching pedagogy to competency",task:"Judging whether a task assesses it",whichcomp:"Naming the competency a task assesses",suit:"Judging whether a task suits a competency"};
  const el=document.querySelector(`[data-done="${id}"]`);el.classList.remove("hidden");
  el.innerHTML=`<div class="card">
    <span class="tag">Result</span>
    <h2 style="margin:12px 0 4px">${r.score} of ${r.total} \u2014 ${pct}%</h2>
    <p style="color:var(--ink-soft)">${pct>=85?"Strong. You could run this section for your own department.":pct>=65?"Solid working grasp. The gaps below are worth a second pass.":"Worth revisiting the stage before this one."}</p>
    <h3 style="margin:20px 0 8px">By question type</h3>
    ${Object.entries(r.perType).map(([k,v])=>{const p=Math.round(v.c/v.n*100),cls=p<50?"low":p<75?"mid":"";
      return `<div class="meter"><span>${typeNames[k]||k}</span><span class="bar"><i class="${cls}" style="width:${p}%"></i></span><span class="val">${v.c}/${v.n}</span></div>`;}).join("")}
    ${Object.keys(r.perComp).length?`<h3 style="margin:20px 0 8px">By competency</h3>
      ${Object.entries(r.perComp).sort((a,b)=>byKey(a[0]).n-byKey(b[0]).n).map(([k,v])=>{const p=Math.round(v.c/v.n*100),cls=p<50?"low":p<75?"mid":"";
      return `<div class="meter"><span>${byKey(k).name}</span><span class="bar"><i class="${cls}" style="width:${p}%"></i></span><span class="val">${v.c}/${v.n}</span></div>`;}).join("")}`:""}
    ${weak.length?`<div class="callout" style="margin-top:20px"><strong>Revisit before you move on:</strong> ${weak.join(", ")}.</div>`:""}
    <p class="noprint" style="margin-top:16px;display:flex;gap:10px;flex-wrap:wrap">
      <button class="btn action" data-retake="${id}">Take it again</button>
      ${id==="q1"?'<button class="btn ghost" data-goto="pedagogy">Continue to pedagogy \u2192</button>':id==="q2"?'<button class="btn ghost" data-goto="quiz3">Continue to quiz 3 \u2192</button>':'<button class="btn ghost" data-goto="build">Continue to build a module \u2192</button>'}
    </p></div>`;
  el.querySelector(`[data-retake="${id}"]`).addEventListener("click",()=>{
    document.getElementById(id+"intro").classList.remove("hidden");el.classList.add("hidden");
  });
  el.querySelectorAll("[data-goto]").forEach(b=>b.addEventListener("click",()=>{const v=b.dataset.goto;show(v);}));
}

/* ============================================================
   04 PEDAGOGY + 05 ASSESS rendering
   ============================================================ */
function renderPedagogy(){
  const w=document.getElementById("pedCards");w.innerHTML="";
  C.forEach(c=>{
    const meth=PEDAGOGIES.filter(p=>p.develops.includes(c.key));
    const el=document.createElement("div");el.className="card";
    el.innerHTML=`<h3>${String(c.n).padStart(2,"0")} \u00b7 ${c.name}</h3>
      <p style="color:var(--ink-soft);font-size:14px;margin:2px 0 12px">${c.evidence} carries the PLO12 mark. ${meth.length} methods develop this competency:</p>
      <div class="pedlist">${meth.map(p=>`
        <div class="pedrow">
          <div class="pedname">${p.name}<span class="pedfam">${p.fam}</span></div>
          <div class="peddoes">${p.does}</div>
          <div class="pedassess"><b>Assess:</b> ${p.assess}</div>
        </div>`).join("")}</div>`;
    w.appendChild(el);
  });
  document.getElementById("methodRows").innerHTML=C.map(c=>
    `<tr><td class="k">${String(c.n).padStart(2,"0")} \u00b7 ${c.name}</td><td>${c.methods}</td><td>${c.ped}</td></tr>`).join("");
  document.getElementById("evidenceRows").innerHTML=C.map(c=>
    `<tr><td class="k">${String(c.n).padStart(2,"0")} \u00b7 ${c.name}</td><td>${c.evidence}</td></tr>`).join("");
}
function renderRubricPicker(){
  const s=document.getElementById("rubPick");s.innerHTML="";
  C.forEach(c=>{const o=document.createElement("option");o.value=c.key;o.textContent=`${String(c.n).padStart(2,"0")} \u00b7 ${c.name}`;s.appendChild(o);});
  const paint=()=>{
    const c=byKey(s.value);
    document.getElementById("rubOut").innerHTML=`
      ${c.fromDeck?'<span class="tag">Worked example from the workshop</span>':'<span class="tag slate">Built on the same gradient</span>'}
      <table class="tbl" style="margin-top:12px"><thead><tr><th>Criterion</th><th>Level 1 \u00b7 Limited</th><th>Level 4 \u00b7 Exemplary</th></tr></thead>
      <tbody>${c.rubric.map(r=>`<tr><td class="k">${r.crit}<span class="prov">${r.prov||""}</span></td><td>${r.l1}</td><td>${r.l4}</td></tr>`).join("")}</tbody></table>
      <p style="margin-top:12px;font-size:14.4px;color:var(--ink-soft)">Four criteria per competency: criteria 1&#8211;3 come from the observable behaviours; criterion 4 is the &#8220;so what&#8221;. Each states the UNESCO (2017) Box 1.1 clause it operationalises, or is declared institutional (Appendix C). Fill levels 2 and 3 by splitting the gap \u2014 connects, then justifies.</p>`;
  };
  s.addEventListener("change",paint);paint();
}

/* ============================================================
   BOOT
   ============================================================ */

/* ============================================================
   07 BUILD  \u2014 interactive guidebook workflow
   ============================================================ */
const SDGS=[
 [1,"No Poverty"],[2,"Zero Hunger"],[3,"Good Health & Well-being"],[4,"Quality Education"],
 [5,"Gender Equality"],[6,"Clean Water & Sanitation"],[7,"Affordable & Clean Energy"],
 [8,"Decent Work & Economic Growth"],[9,"Industry, Innovation & Infrastructure"],
 [10,"Reduced Inequalities"],[11,"Sustainable Cities & Communities"],
 [12,"Responsible Consumption & Production"],[13,"Climate Action"],[14,"Life Below Water"],
 [15,"Life on Land"],[16,"Peace, Justice & Strong Institutions"],[17,"Partnerships for the Goals"]
];
const VERBS={
 systems:["map","trace","model","delineate the boundary of"],
 anticipatory:["construct scenarios for","test against","identify irreversibility in"],
 normative:["justify","weigh","adjudicate between","apply a principle to"],
 strategic:["sequence","resource","prioritise","plan the implementation of"],
 collaboration:["negotiate","represent","integrate","reconcile"],
 critical:["evaluate","interrogate","audit","expose the assumption in"],
 selfaware:["locate","situate","examine one's own","account for"],
 integrated:["recommend","defend","decide between","produce a defensible"]
};
function pedForComp(key){
  const strong=PEDAGOGIES.filter(pd=>pd.develops.includes(key));
  return (strong.length?strong:PEDAGOGIES);
}
function B(){return state.build;}

function renderWfSteps(){
  const b=B();
  const have=b.comps.length>=1;
  const done=[
    !!b.cluster, !!b.sdg, have,
    have && cloReady(b),
    have && b.comps.every(k=>b.activity[k]),
    have && b.comps.every(k=>(b.output[k]||"").trim()),
    have && (b.assignment||"").trim().length>0,
    have && b.comps.every(k=>rubricFilled(k))
  ];
  const labels=["Content","SDG","Competency","CLO","Activity","Output","Topic","Rubric"];
  document.getElementById("wfSteps").innerHTML=labels.map((l,i)=>
    `<div class="wf${done[i]?' done':''}"><span class="wn">STEP ${i+1}</span><span class="wl">${l}</span></div>`).join("");
  const allDone=done.every(Boolean);
  state.build._done=allDone;
  const t=document.querySelector('[data-tick="build"]'); if(t)t.textContent=allDone?"\u2713":"";
}
function rubricFilled(key){
  const r=B().rubric[key]; if(!r)return false;
  return r.every(row=>row.l1&&row.l2&&row.l3&&row.l4);
}
function isOneClo(b){return b.comps.length===2 && b.cloMode==="one";}
function cloReady(b){
  if(b.comps.length===0)return false;
  if(isOneClo(b))return (b.cloOne||"").trim().length>0;
  return b.comps.every(k=>(b.clo[k]||"").trim());
}
function ensureRubric(key){
  const c=byKey(key); const b=B();
  // Rebuild if missing, or if a stale rubric (e.g. the old 3-criteria shape) was loaded.
  if(!b.rubric[key] || b.rubric[key].length!==c.rubric.length){
    b.rubric[key]=c.rubric.map(r=>({crit:r.crit,prov:r.prov,l1:r.l1,l2:"",l3:"",l4:r.l4}));
  }
}

function renderBuild(){
  const b=B(); const body=document.getElementById("buildBody");
  const clustersOpts=DISCIPLINES.map(d=>`<option value="${d}"${b.cluster===d?' selected':''}>${d}</option>`).join("");
  let h="";

  // STEP 1 \u2014 content + cluster
  h+=`<div class="stepcard${b.cluster?' ok':''}">
    <div class="stephead"><span class="stepnum">1</span><h3>Content &amp; cluster</h3></div>
    <div class="stepsub">Start from a course you already teach. Pick the discipline cluster it belongs to.</div>
    <div style="margin-left:36px">
      <label class="fl">Course name <span class="hint">&#8212; code and title</span></label>
      <input type="text" id="bCourse" placeholder="e.g. Urban Water Resources Management" value="${(b.course||'').replace(/"/g,'&quot;')}">
      <label class="fl" style="margin-top:12px">Discipline cluster</label>
      <select id="bCluster"><option value="">&#8212; choose your cluster &#8212;</option>${clustersOpts}</select>
    </div></div>`;

  // STEP 2 \u2014 SDG
  h+=`<div class="stepcard${b.sdg?' ok':''}">
    <div class="stephead"><span class="stepnum">2</span><h3>Sustainability challenge &amp; SDG</h3></div>
    <div class="stepsub">Choose one primary SDG your content genuinely touches. One, at most two &#8212; broad mapping fails audit.</div>
    <div class="pickgrid" id="bSdgGrid" style="grid-template-columns:repeat(auto-fill,minmax(210px,1fr))">
      ${SDGS.map(([n,t])=>`<button class="sdgpick" data-sdg="${n}" aria-pressed="${b.sdg==(''+n)}"><span class="sn">${n}</span><span>${t}</span></button>`).join("")}
    </div></div>`;

  // STEP 3 \u2014 competencies (one or two)
  const nsel=b.comps.length;
  h+=`<div class="stepcard${nsel>=1?' ok':''}">
    <div class="stephead"><span class="stepnum">3</span><h3>Select one or two competencies</h3></div>
    <div class="stepsub">Both are assessed under PLO12. Pick one or two your content can genuinely produce evidence for &#8212; two per course is UPM's default.</div>
    ${nsel===0?`<div class="wchip">Pick one or two to continue</div>`:''}
    ${b.comps.includes('integrated')?`<div class="wchip">Integrated Problem-solving is capstone / final-year work. Met mid-programme, assess it as emerging: mark all four levels, set the attainment threshold at Developing, and declare that in the course outline.</div>`:''}
    <div class="pickgrid" id="bCompGrid">
      ${C.map(c=>`<button class="pick" data-comp="${c.key}" aria-pressed="${b.comps.includes(c.key)}"><span class="pk">${String(c.n).padStart(2,'0')}</span>${c.name}</button>`).join("")}
    </div></div>`;

  // STEPS 4-8 per competency (once one or two chosen)
  if(b.comps.length>=1){
    b.comps.forEach(ensureRubric);
    const oneClo=isOneClo(b);

    // STEP 4 CLO \u2014 with a two-CLOs / one-CLO toggle when two competencies are selected
    h+=`<div class="stepcard${cloReady(b)?' ok':''}">
      <div class="stephead"><span class="stepnum">4</span><h3>Write the CLO, mapped to PLO12</h3></div>
      <div class="stepsub">Use an observable verb. The test: can you write four rubric levels for it?</div>`;
    if(b.comps.length===2){
      h+=`<div class="toggle2 noprint">
        <button class="pilltog${!oneClo?' on':''}" data-clomode="two">Two CLOs &#8212; one per competency</button>
        <button class="pilltog${oneClo?' on':''}" data-clomode="one">One CLO &#8212; carrying both</button>
      </div>
      <div class="stepsub" style="margin:2px 0 0">Choose one CLO only when the task cannot be done without both competencies together &#8212; typically capstone or design work. Both blocks of rubric criteria (1&#8211;4 and 5&#8211;8) then hang off this one CLO; state which criteria evidence which competency.</div>`;
    }
    if(oneClo){
      const A=byKey(b.comps[0]),Bc=byKey(b.comps[1]);
      const verbs=[...new Set([...VERBS[b.comps[0]],...VERBS[b.comps[1]]])];
      h+=`<div class="blk"><h4>${A.name} + ${Bc.name}</h4><div class="bsub">One CLO carrying both competencies</div>
        <textarea class="cloin" id="bCloOne" placeholder="e.g. Produce and defend an integrated option, tracing the system effects and justifying the trade-offs...">${(b.cloOne||'').replace(/</g,'&lt;')}</textarea>
        <div class="verbhint">Verbs that work: ${verbs.map(v=>`<b>${v}</b>`).join(" &middot; ")}</div></div>`;
    }else{
      b.comps.forEach(k=>{
        const c=byKey(k);
        h+=`<div class="blk"><h4>${c.name}</h4><div class="bsub">${c.shift}</div>
          <textarea class="cloin" data-clo="${k}" placeholder="e.g. Evaluate competing options and justify the trade-offs...">${(b.clo[k]||'').replace(/</g,'&lt;')}</textarea>
          <div class="verbhint">Verbs that work: ${VERBS[k].map(v=>`<b>${v}</b>`).join(" &middot; ")}</div></div>`;
      });
    }
    h+=`</div>`;

    // STEP 5 activity
    h+=`<div class="stepcard${b.comps.every(k=>b.activity[k])?' ok':''}">
      <div class="stephead"><span class="stepnum">5</span><h3>Design the learning activity</h3></div>
      <div class="stepsub">Choose a pedagogy that makes students practise the competency &#8212; twice, with feedback.</div>`;
    b.comps.forEach(k=>{
      const c=byKey(k); const peds=pedForComp(k);
      h+=`<div class="blk"><h4>${c.name}</h4>
        <label class="fl">Suggested pedagogy <span class="hint">&#8212; strong fits for this competency</span></label>
        <select data-act="${k}"><option value="">&#8212; choose a method &#8212;</option>
        ${peds.map(pd=>`<option value="${pd.name}"${b.activity[k]===pd.name?' selected':''}>${pd.name}</option>`).join("")}</select>`;
      const chosen=peds.find(pd=>pd.name===b.activity[k]);
      if(chosen)h+=`<div class="bsub" style="margin-top:8px"><b>Assess by:</b> ${chosen.assess}</div>`;
      h+=`</div>`;
    });
    h+=`</div>`;

    // STEP 6 output
    h+=`<div class="stepcard${b.comps.every(k=>(b.output[k]||'').trim())?' ok':''}">
      <div class="stephead"><span class="stepnum">6</span><h3>Choose the output that carries the evidence</h3></div>
      <div class="stepsub">Pick the individual output first; the rubric follows from it.</div>`;
    b.comps.forEach(k=>{
      const c=byKey(k);
      if(!b.output[k])b.output[k]=c.evidence;
      h+=`<div class="blk"><h4>${c.name}</h4>
        <textarea class="cloin" data-out="${k}" style="min-height:44px">${(b.output[k]||'').replace(/</g,'&lt;')}</textarea>
        ${k==='collaboration'?'<div class="verbhint">Collaboration needs an individual output attached &#8212; a group report evidences a group, not a person.</div>':''}
        </div>`;
    });
    h+=`</div>`;

    // STEP 7 describe the assignment topic
    h+=`<div class="stepcard${(b.assignment||'').trim()?' ok':''}">
      <div class="stephead"><span class="stepnum">7</span><h3>Describe the assignment topic</h3></div>
      <div class="stepsub">Describe the task students will do to demonstrate ${b.comps.map(k=>byKey(k).name).join(" and ")}. Give the situation, what each student produces, and any group element &#8212; enough for a rubric to be tied to it.</div>
      <div style="margin-left:36px">
        <label class="fl">Assignment topic and task <span class="hint">&#8212; the situation and the individual output</span></label>
        <textarea class="cloin" id="bAssignText" style="min-height:110px" placeholder="e.g. Students receive a real catchment dataset and a drought scenario. Individually, they produce an annotated allocation map (Part A) and a two-page justification memo (Part B) defending who gets water and why.">${(b.assignment||'').replace(/</g,'&lt;')}</textarea>
        <div class="verbhint">Make students USE both competencies to succeed, not describe them. Attach individual evidence where any part is group work, so the mark is attributable.</div>
      </div></div>`;

    // STEP 8 suggest the complete rubric
    h+=`<div class="stepcard${b.comps.every(k=>rubricFilled(k))?' ok':''}">
      <div class="stephead"><span class="stepnum">8</span><h3>Build the rubric</h3></div>
      <div class="stepsub">From the course name, topic, CLO and competencies, an AI drafts the complete rubric for this content. Use it two ways: copy the prompt into any AI you already have, or connect a provider to do it in one click. Criteria 1&#8211;3 come from the observable behaviours; criterion 4 is the &#8220;so what&#8221;. Review and edit every cell &#8212; the mark must be one you could defend at an exam board.</div>
      <div style="margin-left:36px;margin-bottom:14px" class="noprint">
        <div class="aiopt">
          <div class="aiopt-h">Option A &#183; Use any AI, by copy and paste <span class="aiopt-tag">works with anything, no key</span></div>
          <p class="hint" style="margin:0 0 10px">Copy the prompt, paste it into any AI you already have &#8212; ChatGPT, Gemini, Claude, Copilot, DeepSeek, a local model &#8212; then paste its reply back here. No account or API key needed.</p>
          <button class="btn action small" id="bCopyPrompt">Copy the rubric prompt</button>
          <label class="fl" style="margin-top:12px">Paste the AI's reply here</label>
          <textarea id="aiPasteIn" class="cloin" style="min-height:96px" placeholder="Paste the AI's full reply. It should contain a JSON block like { &quot;A&quot;: [ ... ], &quot;B&quot;: [ ... ] }."></textarea>
          <div style="margin-top:10px"><button class="btn small" id="bFillPaste">Fill rubric from reply</button></div>
          <div class="status" id="aiPasteStatus" style="margin-top:8px"></div>
        </div>
        <div class="aiopt">
          <div class="aiopt-h">Option B &#183; Connect an AI provider (one click)</div>
          <p class="hint" style="margin:0 0 10px">Do it automatically instead of copy and paste. Default is Claude (inside Claude, no key); or plug in any OpenAI-compatible endpoint, the Anthropic API, or Google Gemini with your own key.</p>
          ${aiSettingsHTML()}
          <button class="btn action small" id="bSuggestRub" style="margin-top:12px">Build the rubric with the connected AI</button>
          <div id="aiRubOut" style="margin-top:12px"></div>
        </div>
      </div>`;
    b.comps.forEach((k,ci)=>{
      const c=byKey(k); const rr=b.rubric[k];
      h+=`<div class="blk"><h4>${c.name} &#8212; criteria ${ci*4+1}&#8211;${ci*4+4}</h4>
        <table class="rubedit"><thead><tr><th>Criterion</th><th>1 Limited</th><th>2 Developing</th><th>3 Proficient</th><th>4 Exemplary</th></tr></thead><tbody>
        ${rr.map((row,ri)=>`<tr><td class="rc">${row.crit}<span class="prov">${row.prov||''}</span></td>
          <td><textarea data-rub="${k}|${ri}|l1">${(row.l1||'').replace(/</g,'&lt;')}</textarea></td>
          <td><textarea data-rub="${k}|${ri}|l2" placeholder="connects...">${(row.l2||'').replace(/</g,'&lt;')}</textarea></td>
          <td><textarea data-rub="${k}|${ri}|l3" placeholder="justifies...">${(row.l3||'').replace(/</g,'&lt;')}</textarea></td>
          <td><textarea data-rub="${k}|${ri}|l4">${(row.l4||'').replace(/</g,'&lt;')}</textarea></td></tr>`).join("")}
        </tbody></table></div>`;
    });
    h+=`</div>`;
  }

  // ALIGNMENT PREVIEW
  h+=renderAlignPreview();

  body.innerHTML=h;
  wireBuild();
  renderWfSteps();
}

function renderAlignPreview(){
  const b=B();
  const n=b.comps.length;
  const oneClo=isOneClo(b);
  const sdgCell=b.sdg?('SDG '+b.sdg):'&#8212;';
  let rows="";
  if(n>=1){
    if(oneClo){
      const A=byKey(b.comps[0]),Bc=byKey(b.comps[1]);
      rows=`<tr><td>${(b.cloOne||'<span style="color:#9DB1AA">CLO not written</span>')}</td>
        <td class="k" style="width:auto;background:var(--slate-tint);color:var(--slate);font-weight:600">PLO12</td>
        <td>${sdgCell}</td>
        <td>${A.name} + ${Bc.name}</td>
        <td>${A.evidence} / ${Bc.evidence}, criteria 1&#8211;8</td></tr>`;
    }else{
      b.comps.forEach((k,ci)=>{
        const c=byKey(k);
        rows+=`<tr><td>${(b.clo[k]||'<span style="color:#9DB1AA">CLO not written</span>')}</td>
          <td class="k" style="width:auto;background:var(--slate-tint);color:var(--slate);font-weight:600">PLO12</td>
          <td>${sdgCell}</td>
          <td>${c.name}</td>
          <td>${b.output[k]||c.evidence}, criteria ${ci*4+1}&#8211;${ci*4+4}</td></tr>`;
      });
    }
  }
  return `<div class="alignprev">
    <span class="tag slate">Live alignment table</span>
    <h3 style="margin:12px 0 4px">${b.course||'Your course'}${b.cluster?' &#183; '+b.cluster:''}</h3>
    <p style="font-size:13.5px;color:var(--ink-soft)">Only the CLO is directly assessed; every other column is a claim traceable through it.</p>
    ${(b.assignment||'').trim()?`<div style="margin:14px 0"><div class="mono" style="font-size:10.5px;letter-spacing:.14em;text-transform:uppercase;color:var(--moss)">Assignment topic</div><p style="font-size:14px;margin-top:4px;white-space:pre-wrap">${(b.assignment||'').replace(/</g,'&lt;')}</p></div>`:''}
    ${n>=1?`<table class="tbl"><thead><tr><th>CLO</th><th>PLO</th><th>SDG</th><th>ESDC</th><th>Assessed by</th></tr></thead><tbody>${rows}</tbody></table>`:'<p style="color:#9DB1AA;font-size:14px">Select one or two competencies to assemble the table.</p>'}
    <div style="margin-top:16px;display:flex;gap:10px;flex-wrap:wrap" class="noprint">
      <button class="btn moss small" id="bPrint">Print / save as PDF</button>
      <button class="btn ghost small" id="bCopy">Copy as text</button>
      <button class="btn ghost small" id="bReset">Start over</button>
    </div>
    <div class="status" id="bStatus"></div>
  </div>`;
}

function wireBuild(){
  const b=B();
  const cn=document.getElementById("bCourse");
  if(cn)cn.addEventListener("input",e=>{b.course=e.target.value;saveLocal();updateAlign();});
  const cl=document.getElementById("bCluster");
  if(cl)cl.addEventListener("change",e=>{b.cluster=e.target.value;saveLocal();renderBuild();});
  document.querySelectorAll("[data-sdg]").forEach(btn=>btn.addEventListener("click",()=>{
    b.sdg=(b.sdg===btn.dataset.sdg)?"":btn.dataset.sdg;saveLocal();renderBuild();
  }));
  document.querySelectorAll("[data-comp]").forEach(btn=>btn.addEventListener("click",()=>{
    const k=btn.dataset.comp; const i=b.comps.indexOf(k);
    if(i>=0)b.comps.splice(i,1);
    else{ if(b.comps.length>=2)b.comps.shift(); b.comps.push(k); }
    saveLocal();renderBuild();
  }));
  document.querySelectorAll("[data-clo]").forEach(t=>t.addEventListener("input",e=>{
    b.clo[e.target.dataset.clo]=e.target.value;saveLocal();updateAlign();markBuildTick();
  }));
  document.querySelectorAll("[data-clomode]").forEach(btn=>btn.addEventListener("click",()=>{
    b.cloMode=btn.dataset.clomode;saveLocal();renderBuild();
  }));
  const co=document.getElementById("bCloOne");
  if(co)co.addEventListener("input",e=>{b.cloOne=e.target.value;saveLocal();updateAlign();markBuildTick();});
  document.querySelectorAll("[data-act]").forEach(sel=>sel.addEventListener("change",e=>{
    b.activity[e.target.dataset.act]=e.target.value;saveLocal();renderBuild();
  }));
  document.querySelectorAll("[data-out]").forEach(t=>t.addEventListener("input",e=>{
    b.output[e.target.dataset.out]=e.target.value;saveLocal();updateAlign();
  }));
  document.querySelectorAll("[data-rub]").forEach(t=>t.addEventListener("input",e=>{
    const [k,ri,lv]=e.target.dataset.rub.split("|");
    b.rubric[k][+ri][lv]=e.target.value;saveLocal();markBuildTick();
  }));
  const at=document.getElementById("bAssignText");
  if(at)at.addEventListener("input",e=>{b.assignment=e.target.value;saveLocal();updateAlign();markBuildTick();});
  const sg=document.getElementById("bSuggestRub"); if(sg)sg.addEventListener("click",suggestRubric);
  const cpp=document.getElementById("bCopyPrompt"); if(cpp)cpp.addEventListener("click",copyRubricPrompt);
  const flp=document.getElementById("bFillPaste"); if(flp)flp.addEventListener("click",fillRubricFromPaste);
  const aip=document.getElementById("aiProvider");
  if(aip)aip.addEventListener("change",e=>{
    const p=e.target.value, fields=document.getElementById("aiFields");
    if(fields)fields.style.display=(p==="claude")?"none":"";
    const bu=document.getElementById("aiBaseUrl"), md=document.getElementById("aiModel");
    const defs={openai:["https://api.openai.com/v1","gpt-4o-mini"],anthropic:["https://api.anthropic.com","claude-3-5-sonnet-latest"],gemini:["https://generativelanguage.googleapis.com","gemini-1.5-flash"]};
    if(defs[p]){ if(bu&&!bu.value.trim())bu.value=defs[p][0]; if(md&&!md.value.trim())md.value=defs[p][1]; }
  });
  const aisv=document.getElementById("aiSave");
  if(aisv)aisv.addEventListener("click",()=>{
    const g=id=>{const el=document.getElementById(id);return el?el.value:"";};
    const cfg={provider:g("aiProvider"),baseUrl:g("aiBaseUrl").trim(),apiKey:g("aiKey").trim(),model:g("aiModel").trim()};
    const okc=setAICfg(cfg); const st=document.getElementById("aiCfgStatus");
    if(st)st.textContent=okc?("Saved \u2014 the rubric will use "+cfg.provider+"."):"Could not save settings in this browser.";
  });
  const aicl=document.getElementById("aiClear");
  if(aicl)aicl.addEventListener("click",()=>{
    clearAICfg();
    const aip2=document.getElementById("aiProvider"); if(aip2)aip2.value="claude";
    const fields=document.getElementById("aiFields"); if(fields)fields.style.display="none";
    ["aiBaseUrl","aiKey","aiModel"].forEach(id=>{const el=document.getElementById(id);if(el)el.value="";});
    const st=document.getElementById("aiCfgStatus"); if(st)st.textContent="Cleared \u2014 back to the default (Claude).";
  });
  const pr=document.getElementById("bPrint"); if(pr)pr.addEventListener("click",()=>window.print());
  const cp=document.getElementById("bCopy"); if(cp)cp.addEventListener("click",copyModule);
  const rs=document.getElementById("bReset"); if(rs)rs.addEventListener("click",()=>{
    if(confirm("Clear this module and start over?")){
      state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},cloMode:"two",cloOne:"",activity:{},output:{},rubric:{},assignment:""};
      saveLocal();renderBuild();
    }
  });
}
function updateAlign(){
  const host=document.querySelector("#buildBody .alignprev");
  if(host){ host.outerHTML=renderAlignPreview();
    const pr=document.getElementById("bPrint"); if(pr)pr.addEventListener("click",()=>window.print());
    const cp=document.getElementById("bCopy"); if(cp)cp.addEventListener("click",copyModule);
    const rs=document.getElementById("bReset"); if(rs)rs.addEventListener("click",()=>{
      if(confirm("Clear this module and start over?")){state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},cloMode:"two",cloOne:"",activity:{},output:{},rubric:{},assignment:""};saveLocal();renderBuild();}});
  }
}
function markBuildTick(){ renderWfSteps(); }

function copyModule(){
  const b=B(); const L=[]; const oneClo=isOneClo(b);
  L.push("ESD MODULE \u2014 "+(b.course||"Course"));
  L.push("Cluster: "+(b.cluster||"\u2014"));
  L.push("Primary SDG: "+(b.sdg?("SDG "+b.sdg):"\u2014"));
  L.push("Assessed under: PLO12");
  L.push("");
  L.push("ASSIGNMENT TOPIC:");
  L.push(b.assignment||"\u2014");
  L.push("");
  if(oneClo){
    L.push("CLO (\u2192PLO12, carries both competencies): "+(b.cloOne||"\u2014"));
    L.push("");
  }
  b.comps.forEach((k,ci)=>{
    const c=byKey(k);
    L.push("\u2014 "+c.name.toUpperCase()+" \u2014");
    if(!oneClo)L.push("CLO (\u2192PLO12): "+(b.clo[k]||"\u2014"));
    L.push("Activity: "+(b.activity[k]||"\u2014"));
    L.push("Output: "+(b.output[k]||c.evidence));
    L.push("Rubric (criteria "+(ci*4+1)+"\u2013"+(ci*4+4)+"):");
    (b.rubric[k]||[]).forEach(r=>{
      L.push("  "+r.crit+(r.prov?"  ["+r.prov+"]":""));
      L.push("   1 Limited: "+(r.l1||""));
      L.push("   2 Developing: "+(r.l2||""));
      L.push("   3 Proficient: "+(r.l3||""));
      L.push("   4 Exemplary: "+(r.l4||""));
    });
    L.push("");
  });
  const txt=L.join("\n");
  const done=()=>{const st=document.getElementById("bStatus");if(st)st.textContent="Module copied to clipboard.";};
  if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(txt).then(done).catch(()=>fallbackCopy(txt,done));}
  else fallbackCopy(txt,done);
}
function fallbackCopy(txt,done){
  const ta=document.createElement("textarea");ta.value=txt;document.body.appendChild(ta);ta.select();
  try{document.execCommand("copy");done();}catch(e){const st=document.getElementById("bStatus");if(st)st.innerHTML='<span class="err">Copy failed \u2014 use Print instead.</span>';}
  ta.remove();
}

/* ============================================================
   08 BUILD \u2014 AI-assisted rubric (provider-agnostic)
   The default path uses Claude and only connects inside Claude;
   any other provider uses the user's own endpoint, key and model.
   Everything else in the app works with no AI at all.
   ============================================================ */
const AIBOX={brief:null,rub:null};
function esc(s){return (s==null?"":String(s)).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;");}
function aiErr(msg){return '<div class="status"><span class="err">'+msg+'</span></div>';}

async function callClaude(prompt){
  const res=await fetch("https://api.anthropic.com/v1/messages",{
    method:"POST",
    headers:{"Content-Type":"application/json"},
    body:JSON.stringify({model:"claude-sonnet-4-6",max_tokens:1000,messages:[{role:"user",content:prompt}]})
  });
  if(!res.ok)throw new Error("service returned "+res.status);
  const data=await res.json();
  return (data.content||[]).filter(x=>x&&x.type==="text").map(x=>x.text).join("\n");
}
function extractJSON(text){
  let t=(text||"").trim();
  t=t.replace(/^```json/i,"").replace(/^```/,"").replace(/```$/,"").trim();
  const a=t.indexOf("{"),z=t.lastIndexOf("}");
  if(a>=0&&z>a)t=t.slice(a,z+1);
  return JSON.parse(t);
}

/* ---- provider-agnostic AI adapter ----
   Default "claude" uses the in-app path (no key, works only inside Claude).
   Any other provider uses the user's own endpoint, key and model, stored in this browser. */
function getAICfg(){ try{const r=localStorage.getItem("esd8:aicfg");return r?JSON.parse(r):null;}catch(e){return null;} }
function setAICfg(c){ try{localStorage.setItem("esd8:aicfg",JSON.stringify(c));return true;}catch(e){return false;} }
function clearAICfg(){ try{localStorage.removeItem("esd8:aicfg");}catch(e){} }
function aiMsg(d,status){ const e=d&&d.error; return (e&&(e.message||(typeof e==="string"?e:null)))||("service returned "+status); }

async function callModel(prompt){
  const cfg=getAICfg()||{};
  const provider=cfg.provider||"claude";
  if(provider==="claude"){ return callClaude(prompt); }
  const key=(cfg.apiKey||"").trim();
  if(provider==="anthropic"){
    const base=(cfg.baseUrl||"https://api.anthropic.com").replace(/\/+$/,"");
    const res=await fetch(base+"/v1/messages",{method:"POST",
      headers:{"Content-Type":"application/json","x-api-key":key,"anthropic-version":"2023-06-01","anthropic-dangerous-direct-browser-access":"true"},
      body:JSON.stringify({model:cfg.model||"claude-3-5-sonnet-latest",max_tokens:2048,messages:[{role:"user",content:prompt}]})});
    const d=await res.json(); if(!res.ok)throw new Error(aiMsg(d,res.status));
    return (d.content||[]).filter(x=>x&&x.type==="text").map(x=>x.text).join("\n");
  }
  if(provider==="gemini"){
    const base=(cfg.baseUrl||"https://generativelanguage.googleapis.com").replace(/\/+$/,"");
    const model=cfg.model||"gemini-1.5-flash";
    const res=await fetch(base+"/v1beta/models/"+encodeURIComponent(model)+":generateContent?key="+encodeURIComponent(key),
      {method:"POST",headers:{"Content-Type":"application/json"},body:JSON.stringify({contents:[{parts:[{text:prompt}]}]})});
    const d=await res.json(); if(!res.ok)throw new Error(aiMsg(d,res.status));
    return ((((d.candidates||[])[0]||{}).content||{}).parts||[]).map(p=>p.text||"").join("");
  }
  // openai-compatible chat completions (OpenAI, OpenRouter, Groq, Together, local Ollama / LM Studio, ...)
  const base=(cfg.baseUrl||"https://api.openai.com/v1").replace(/\/+$/,"");
  const res=await fetch(base+"/chat/completions",{method:"POST",
    headers:{"Content-Type":"application/json","Authorization":"Bearer "+key},
    body:JSON.stringify({model:cfg.model||"gpt-4o-mini",messages:[{role:"user",content:prompt}],temperature:0.3,max_tokens:2048})});
  const d=await res.json(); if(!res.ok)throw new Error(aiMsg(d,res.status));
  return (((d.choices||[])[0]||{}).message||{}).content||"";
}

function escA(s){return esc(s).replace(/"/g,"&quot;");}
function aiSettingsHTML(){
  const cfg=getAICfg()||{provider:"claude",baseUrl:"",apiKey:"",model:""};
  const p=cfg.provider||"claude";
  const sel=v=>p===v?" selected":"";
  return `<details class="aicfg"${p!=="claude"?" open":""}>
    <summary>AI provider settings${p!=="claude"?" \u2014 using "+p:" \u2014 default: Claude"}</summary>
    <div class="aicfgbody">
      <p class="hint" style="margin:0 0 10px">Choose who generates the rubric. The default uses Claude and needs no key, but only works when this page is opened inside Claude. To use any other AI, pick a provider and paste your own key. Settings are stored only in this browser, on this device.</p>
      <label class="fl">Provider</label>
      <select id="aiProvider">
        <option value="claude"${sel("claude")}>Claude (inside Claude \u2014 no key needed)</option>
        <option value="openai"${sel("openai")}>OpenAI-compatible (OpenAI, OpenRouter, Groq, Together, local Ollama / LM Studio)</option>
        <option value="anthropic"${sel("anthropic")}>Anthropic API (your own key)</option>
        <option value="gemini"${sel("gemini")}>Google Gemini</option>
      </select>
      <div id="aiFields"${p==="claude"?' style="display:none"':""}>
        <label class="fl" style="margin-top:10px">API base URL</label>
        <input type="text" id="aiBaseUrl" value="${escA(cfg.baseUrl||"")}" placeholder="e.g. https://api.openai.com/v1  (or http://localhost:11434/v1 for Ollama)">
        <label class="fl" style="margin-top:10px">API key</label>
        <input type="password" id="aiKey" value="${escA(cfg.apiKey||"")}" placeholder="paste your key" autocomplete="off">
        <label class="fl" style="margin-top:10px">Model</label>
        <input type="text" id="aiModel" value="${escA(cfg.model||"")}" placeholder="e.g. gpt-4o-mini">
      </div>
      <div style="margin-top:12px;display:flex;gap:10px;align-items:center;flex-wrap:wrap">
        <button class="btn small" id="aiSave">Save settings</button>
        <button class="btn ghost small" id="aiClear">Clear</button>
        <span class="hint" id="aiCfgStatus"></span>
      </div>
      <p class="hint" style="margin-top:8px">Note: some hosted providers block direct calls from a web page (CORS). Local models (Ollama, LM Studio) and OpenRouter generally work from the browser; for others you may need their browser-access option, or run the page through a small proxy.</p>
    </div>
  </details>`;
}

function rubricPrompt(b){
  const oneClo=isOneClo(b);
  const lineOf=r=>r.crit+" ("+(r.prov||"institutional")+")";
  const topic=(b.assignment||"").trim();
  const letters=["A","B"];
  const L=[
"You are helping a Malaysian university lecturer build a complete, defensible PLO12 marking rubric for the assignment below. It follows UNESCO (2017) ESD competencies and the UPM guidebook (four criteria per competency, four levels each).",
"",
"CONTEXT",
"Course: "+(b.course||"(unnamed)"),
"Discipline cluster: "+(b.cluster||"(none)"),
"Primary SDG: "+(b.sdg?("SDG "+b.sdg):"(none)"),
""];
  if(oneClo){ L.push("One CLO carrying both competencies: "+(b.cloOne||"(not written)")); L.push(""); }
  L.push("ASSIGNMENT TOPIC AND TASK", (topic||"(not described)"), "");
  b.comps.forEach((k,ci)=>{
    const c=byKey(k), rr=(b.rubric[k]||c.rubric);
    L.push("COMPETENCY "+letters[ci]+": "+c.name+" - "+c.def);
    if(!oneClo) L.push("CLO "+letters[ci]+": "+(b.clo[k]||"(not written)"));
    L.push("Output "+letters[ci]+": "+(b.output[k]||c.evidence));
    L.push("Four criteria, keep these exact names in this order (UNESCO clause in brackets):");
    L.push(rr.map(lineOf).join(" | "));
    L.push("");
  });
  L.push(
"For EACH criterion write all four level descriptors (1 Limited, 2 Developing, 3 Proficient, 4 Exemplary) that:",
"- describe what the student's actual work ON THIS ASSIGNMENT looks like at each level",
"- differentiate by QUALITY, never by counting (do not use 'three factors' vs 'one factor')",
"- avoid bare adjectives (no 'excellent / good / fair / poor')",
"- follow the gradient: lists, then connects, then justifies, then treats its own choice as a choice (for the values competencies: asserts, reasons, applies a principle, withstands challenge)",
"- operationalise the named UNESCO clause for that criterion, and refer to concrete features of THIS assignment so the mark is defensible to a student",
"Each descriptor: one sentence, under 22 words, plain punctuation, no em dashes.",
"");
  const four='[{"l1":"","l2":"","l3":"","l4":""},{"l1":"","l2":"","l3":"","l4":""},{"l1":"","l2":"","l3":"","l4":""},{"l1":"","l2":"","l3":"","l4":""}]';
  if(b.comps.length===2){
    L.push('Return ONLY valid JSON, no preamble and no markdown fences. Exactly FOUR rows per competency, in the given order:');
    L.push('{"A":'+four+',"B":'+four+'}');
  }else{
    L.push('Return ONLY valid JSON, no preamble and no markdown fences. Exactly FOUR rows, in the given order:');
    L.push('{"A":'+four+'}');
  }
  return L.join("\n");
}

function rubricPreviewHTML(b){
  let h='<div class="alignprev" style="margin-top:0"><span class="tag">Suggested complete rubric \u2014 review before inserting</span>';
  b.comps.forEach(k=>{
    const c=byKey(k),rows=(AIBOX.rub&&AIBOX.rub[k])||[],base=b.rubric[k]||[];
    h+='<h4 style="margin:14px 0 6px">'+c.name+'</h4>';
    h+='<table class="tbl"><thead><tr><th>Criterion</th><th>1 Limited</th><th>2 Developing</th><th>3 Proficient</th><th>4 Exemplary</th></tr></thead><tbody>';
    base.forEach((row,ri)=>{const s=rows[ri]||{};
      h+='<tr><td class="k">'+esc(row.crit)+'<span class="prov">'+esc(row.prov||"")+'</span></td><td>'+esc(s.l1)+'</td><td>'+esc(s.l2)+'</td><td>'+esc(s.l3)+'</td><td>'+esc(s.l4)+'</td></tr>';});
    h+='</tbody></table>';
  });
  h+='<div style="margin-top:12px" class="noprint"><button class="btn action small" id="bInsertRub">Insert into the rubric editor above</button></div></div>';
  return h;
}

async function suggestRubric(){
  const b=B();
  const out=document.getElementById("aiRubOut");
  const btn=document.getElementById("bSuggestRub");
  if(!out)return;
  if(b.comps.length<1){out.innerHTML=aiErr("Select one or two competencies first (step 3).");return;}
  if(!(b.assignment||"").trim()){out.innerHTML=aiErr("Describe the assignment topic in step 7 first, so the rubric can be specific to it.");return;}
  b.comps.forEach(ensureRubric);
  const old=btn.textContent;btn.disabled=true;btn.textContent="Working\u2026";
  out.innerHTML='<p class="bsub" style="margin:0">The AI is drafting the complete rubric for this content\u2026</p>';
  try{
    const txt=await callModel(rubricPrompt(b));
    const j=extractJSON(txt);
    AIBOX.rub={};
    AIBOX.rub[b.comps[0]]=j.A||[];
    if(b.comps[1])AIBOX.rub[b.comps[1]]=j.B||[];
    out.innerHTML=rubricPreviewHTML(b);
    const ins=document.getElementById("bInsertRub");
    if(ins)ins.addEventListener("click",()=>{
      const n=fillRubricInPlace(AIBOX.rub);
      const o=document.getElementById("aiRubOut");
      if(o)o.innerHTML='<div class="status">Rubric inserted ('+n+' cells). Review and edit every cell below.</div>';
    });
  }catch(e){
    out.innerHTML=aiErr("Could not reach the AI ("+e.message+"). Check the AI provider settings above \u2014 the default only works inside Claude; to use another AI, choose a provider and paste your key. Some hosted providers also block direct browser calls (CORS). You can instead use the copy-and-paste option above, which works with any AI. The rubric editor below still works by hand.");
  }finally{btn.disabled=false;btn.textContent=old;}
}

/* Fill the editable rubric in place (no full re-render) so the paste box and status survive. */
function fillRubricInPlace(byComp){
  const b=B(); let filled=0;
  b.comps.forEach(k=>{
    const rows=(byComp&&byComp[k])||[];
    (b.rubric[k]||[]).forEach((row,ri)=>{
      const s=rows[ri]; if(!s)return;
      ["l1","l2","l3","l4"].forEach(lv=>{
        if(s[lv]){ row[lv]=s[lv];
          const el=document.querySelector('[data-rub="'+k+"|"+ri+"|"+lv+'"]');
          if(el)el.value=s[lv];
          filled++;
        }
      });
    });
  });
  saveLocal(); if(typeof markBuildTick==="function")markBuildTick();
  return filled;
}
function copyTextTo(txt,statusEl,okMsg){
  const ok=()=>{if(statusEl)statusEl.textContent=okMsg;};
  const fb=()=>{const ta=document.createElement("textarea");ta.value=txt;document.body.appendChild(ta);ta.select();
    try{document.execCommand("copy");ok();}catch(e){if(statusEl)statusEl.innerHTML='<span class="err">Copy failed \u2014 select the text and copy it manually.</span>';}ta.remove();};
  if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(txt).then(ok).catch(fb);}
  else fb();
}
/* Copy-and-paste path: works with ANY AI (ChatGPT, Gemini, Claude, Copilot, local models, ...). No key, no API, no CORS. */
function copyRubricPrompt(){
  const b=B(); const st=document.getElementById("aiPasteStatus");
  const set=(m,err)=>{if(st)st.innerHTML=err?'<span class="err">'+m+'</span>':m;};
  if(b.comps.length<1){set("Select one or two competencies first (step 3).",true);return;}
  if(!(b.assignment||"").trim()){set("Describe the assignment topic in step 7 first, so the rubric can be specific to it.",true);return;}
  b.comps.forEach(ensureRubric);
  copyTextTo(rubricPrompt(b),st,"Prompt copied. Paste it into any AI, let it answer, then paste the whole reply in the box below and press Fill.");
}
function fillRubricFromPaste(){
  const b=B(); const st=document.getElementById("aiPasteStatus");
  const set=(m,err)=>{if(st)st.innerHTML=err?'<span class="err">'+m+'</span>':m;};
  if(b.comps.length<1){set("Select one or two competencies first (step 3).",true);return;}
  b.comps.forEach(ensureRubric);
  const ta=document.getElementById("aiPasteIn"); const raw=ta?ta.value:"";
  if(!raw.trim()){set("Paste the AI's reply in the box first.",true);return;}
  let j;
  try{ j=extractJSON(raw); }catch(e){ set("Could not find JSON in that text. Paste the AI's full reply \u2014 it should contain a { ... } block with an \"A\" (and, for two competencies, a \"B\") array.",true); return; }
  const byComp={}; byComp[b.comps[0]]=j.A||[]; if(b.comps[1])byComp[b.comps[1]]=j.B||[];
  if(!Object.values(byComp).some(r=>Array.isArray(r)&&r.length)){ set("That JSON did not contain the expected \"A\" (and \"B\") arrays of level descriptors. Re-copy the prompt and try again.",true); return; }
  const n=fillRubricInPlace(byComp);
  set(n?("Rubric filled ("+n+" cells) from the pasted reply. Review and edit every cell below."):"No matching descriptors were found in that reply.",!n);
}


(async function(){
  await loadLocal();
  renderLedger();fillDisc();renderPedagogy();renderRubricPicker();renderBuild();
  document.getElementById("railDisc").textContent=state.disc||"not set";
  paintTicks();
  show("understand");
  if(!hasS)document.getElementById("railSaved").textContent="Progress saves in this browser.";
})();
</script>
