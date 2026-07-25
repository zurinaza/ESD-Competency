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
      <button class="navbtn" data-view="build"><span class="num">07</span><span><span class="lbl">Build a module</span><span class="sub">The full workflow, end to end</span></span><span class="tick" data-tick="build"></span></button>
      <button class="navbtn" data-view="facil"><span class="num">08</span><span><span class="lbl">Facilitator</span><span class="sub">Room results by code</span></span></button>
    </div>
    <div class="railfoot">
      Workshop code: <code id="railCode" class="mono">not set</code><br>
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
    <p class="lede">Start here, before your discipline and before assessment. Open each row for what the competency actually claims, the shift it demands of student work, and the three observable behaviours &#8212; those three are the raw material for every rubric later in this app.</p>

    <div class="card noprint" style="display:flex;gap:16px;flex-wrap:wrap;align-items:flex-end">
      <div style="flex:1 1 240px">
        <label class="fl" for="codeIn">Workshop code <span class="hint">&#8212; from your facilitator</span></label>
        <input type="text" id="codeIn" class="mono" placeholder="e.g. UPM-ESD-01" autocomplete="off">
      </div>
      <div><button class="btn ghost small" id="saveCode">Set code</button></div>
    </div>

    <div class="ledger" id="ledger"></div>

    <div class="card" style="margin-top:26px">
      <span class="tag">Checkpoint</span>
      <h3 style="margin:12px 0 8px">Four distinctions worth getting right</h3>
      <p style="color:var(--ink-soft);font-size:15px">These confusions are the ones that show up in course outlines.</p>
      <div class="grid2" id="distinctions"></div>
    </div>

    <div class="callout">
      <strong>The line to carry into every later stage.</strong> If a student could score full marks without using the competency, you have not assessed it &#8212; whatever your outline claims.
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
      <p class="lede">Eighteen questions on meaning and on your field. Identify the competency from a student behaviour, from a plain-language description, and from a task in your discipline &#8212; then separate the four pairs people confuse. Every answer comes with the reason, not just a tick.</p>
      <div class="grid3">
        <div class="card"><span class="tag">Identify</span><p style="margin-top:10px;font-size:14.6px">A student does this &#8212; which of the eight is it evidence of?</p></div>
        <div class="card"><span class="tag slate">In your field</span><p style="margin-top:10px;font-size:14.6px">A task from your discipline &#8212; which competency does it carry?</p></div>
        <div class="card"><span class="tag amber">Distinguish</span><p style="margin-top:10px;font-size:14.6px">The four pairs that get mis-selected in outlines.</p></div>
      </div>
      <p style="margin-top:22px"><button class="btn moss" data-start="q1">Start quiz 1</button></p>
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

    <h2 style="margin:30px 0 6px">Six approaches, and what each one really assesses</h2>
    <p style="color:var(--ink-soft);margin-bottom:16px">The <em>watch out</em> line is where most implementations fail.</p>
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
      <p style="font-size:14.6px;color:var(--ink-soft)">Three criteria per competency, taken straight from its observable behaviours, with the two anchor levels written. Fill the middle yourself using the gradient above.</p>
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
      <p class="lede">Sixteen questions on stages 04 and 05. Diagnose the fault in a rubric descriptor, pick the output that carries the evidence, judge whether a task assesses the competency it names, and match a pedagogy to what it actually develops.</p>
      <div class="grid3">
        <div class="card"><span class="tag rose">Diagnose</span><p style="margin-top:10px;font-size:14.6px">What is wrong with this descriptor, task or alignment?</p></div>
        <div class="card"><span class="tag">Evidence</span><p style="margin-top:10px;font-size:14.6px">Which output carries evidence for this competency?</p></div>
        <div class="card"><span class="tag slate">Pedagogy</span><p style="margin-top:10px;font-size:14.6px">Which approach develops it, and what do you actually mark?</p></div>
      </div>
      <p style="margin-top:22px"><button class="btn moss" data-start="q2">Start quiz 2</button></p>
    </div>
    <div class="qrun hidden" data-run="q2"></div>
    <div class="qdone hidden" data-done="q2"></div>
  </section>

  <!-- ================= 07 BUILD ================= -->
  <section id="view-build" class="hidden">
    <div class="eyebrow">Stage 07 &#183; Build your module</div>
    <h1>One course, turned into an ESD module.</h1>
    <p class="lede">Work the guidebook workflow end to end: pick the SDG, choose two competencies, design the activities, choose the output and generate a rubric and PLO12 alignment table you can export. Everything you enter saves on this device.</p>
    <div class="wf-steps" id="wfSteps"></div>
    <div id="buildBody"></div>
  </section>

  <!-- ================= 08 FACILITATOR ================= -->
  <section id="view-facil" class="hidden">
    <div class="eyebrow">Stage 07 &#183; Facilitator</div>
    <h1>What the room actually understood.</h1>
    <p class="lede">Participants submit at the end of each quiz. Enter your workshop code to see both quizzes side by side, which competencies the room got wrong, and which disciplines are represented.</p>
    <div class="card">
      <div class="grid2" style="align-items:end">
        <div><label class="fl" for="fCode">Workshop code</label><input type="text" id="fCode" class="mono" placeholder="UPM-ESD-01"></div>
        <div><button class="btn moss" id="loadBtn">Load results</button></div>
      </div>
      <div class="status" id="facStatus"></div>
    </div>
    <div id="facOut"></div>
  </section>

  </main>
</div>

<script>
/* ============================================================
   DATA
   ============================================================ */
const DISCIPLINES=["Health, Medical & Life Sciences","Sciences","Engineering","Computer Science & IT","Mathematics & Statistics","Education","Business & Economics","Languages & Communication","Sociology, Psychology & Human Development","Architecture & Design","Agriculture, Forestry & Environmental Science"];

const C=[
{n:1,key:"systems",name:"Systems Thinking",one:"See the whole",
 def:"Seeing a problem as connected parts whose interactions produce the outcome.",
 meaning:"Students decide what is inside the system and what is outside it. They trace how a change in one part travels through the rest, recognising feedback, delay, and effects that appear far from the cause.",
 shift:"The shift is from listing factors to mapping relationships.",
 obs:["Maps relationships instead of listing factors","Traces a feedback loop, not just cause and effect","Names a side effect that appears elsewhere"],
 note:"Listing factors is not systems thinking \u2014 most student work stops at a list, and the competency begins at the relationship. The third behaviour discriminates strong from average work more reliably than the map itself.",
 methods:"Causal loop diagrams \u00b7 life-cycle mapping \u00b7 boundary exercises",
 ped:"Problem-based \u00b7 simulation \u00b7 field work",
 evidence:"Annotated system map with written interpretation",
 rubric:[
  {crit:"Boundary and elements",l1:"Lists factors. No boundary drawn.",l4:"Justifies the boundary and shows how a different one changes the conclusion."},
  {crit:"Interconnections",l1:"Describes linear cause and effect only.",l4:"Explains interacting loops, including a delay or non-linear effect."},
  {crit:"Consequences",l1:"Treats the solution as having no side effects.",l4:"Traces consequences across scales and states the remaining uncertainty."}],
 fromDeck:true,
 ex:{"Health, Medical & Life Sciences":"Map how lifestyle, access and policy interact to drive an outbreak.","Sciences":"Trace fertiliser runoff from soil to river to fish stocks.","Engineering":"Map how a procurement saving creates rework and emissions elsewhere.","Computer Science & IT":"Trace how a data-centre efficiency gain shifts load and emissions elsewhere.","Mathematics & Statistics":"Model a loop where the output re-enters as input.","Education":"Map how one assessment policy reshapes teaching, behaviour and attainment.","Business & Economics":"Show how a packaging cost cut raises returns and complaints.","Languages & Communication":"Analyse how one media frame spreads and shapes policy.","Sociology, Psychology & Human Development":"Map how school zoning shifts housing prices, then enrolment.","Architecture & Design":"Trace a building material from source to demolition, naming one off-site impact.","Agriculture, Forestry & Environmental Science":"Trace how a crop switch affects soil, water and food security."}},

{n:2,key:"anticipatory",name:"Anticipatory Competency",one:"Work with futures",
 def:"Working with several possible futures at once, not assuming tomorrow extends today.",
 meaning:"Students separate the probable future from the possible and the desirable. They build scenarios that differ in substance rather than in optimism, test a decision against each, and apply caution where an outcome cannot be undone.",
 shift:"The shift is from one forecast to a range.",
 obs:["Builds scenarios that differ structurally, not in degree","Tests a decision against each and reports where it fails","Identifies which consequences are irreversible"],
 note:"Watch for best case / worst case / most likely \u2014 that is one scenario at three volumes. Structural difference is the criterion. Irreversibility is the most teachable idea here: it turns an abstract futures discussion into a decision filter.",
 methods:"Scenario building \u00b7 backcasting from a 2040 target \u00b7 futures wheel",
 ped:"Simulation and gamification \u00b7 scenario cases",
 evidence:"Scenario set, and a decision tested against each",
 rubric:[
  {crit:"Scenario construction",l1:"Describes one future, or three volumes of the same future.",l4:"Builds scenarios that differ structurally and names the driver that separates them."},
  {crit:"Testing the decision",l1:"States a preferred option without testing it against any future.",l4:"Tests the decision against each scenario and reports where and why it fails."},
  {crit:"Irreversibility",l1:"Treats every consequence as recoverable.",l4:"Separates reversible from irreversible outcomes and lets that shape the recommendation."}],
 ex:{"Health, Medical & Life Sciences":"Build three ageing-population futures; test one service model against each.","Sciences":"Test which lab findings hold under three structurally different climate futures.","Engineering":"Design drainage for three 2070 rainfall futures, not 1990 records.","Computer Science & IT":"Build three AI-adoption futures; test one system design against each.","Mathematics & Statistics":"Compare model outputs under three structurally different assumption sets.","Education":"Build three graduate-labour-market futures; test one curriculum decision.","Business & Economics":"Stress-test a five-year strategy against three carbon-pricing futures.","Languages & Communication":"Write one message that must hold across three different public moods.","Sociology, Psychology & Human Development":"Forecast three community futures; name the irreversible social outcomes.","Architecture & Design":"Design for three climate futures; name the irreversible commitments.","Agriculture, Forestry & Environmental Science":"Build three resource-scarcity scenarios; state where the plan fails."}},

{n:3,key:"normative",name:"Normative Competency",one:"Negotiate values",
 def:"Recognising that sustainability decisions rest on values, and negotiating them openly.",
 meaning:"Every sustainability choice contains a judgement about what matters, who counts, and over what timeframe. Students surface those judgements including their own, separate a technical disagreement from a values conflict, and argue from a stated principle rather than a preference.",
 shift:"The shift is from 'what is correct' to 'on what basis are we deciding'.",
 obs:["Names the values in conflict, not just the options","States who bears the cost and who gains","Justifies using an explicit, consistent principle"],
 note:"Most often written into a course outline and least often assessed, because technical lecturers are uncomfortable marking value reasoning. You are not marking which position the student takes \u2014 you mark whether values were surfaced, distribution analysed, and a principle applied consistently.",
 methods:"Value ranking \u00b7 ethical dilemma cases \u00b7 deliberative debate",
 ped:"Role-play and case-based \u00b7 SULAM",
 evidence:"Justification memo naming the principle applied",
 rubric:[
  {crit:"Surfacing values",l1:"Presents the decision as purely technical.",l4:"Names the values in conflict including their own, and its influence."},
  {crit:"Who bears the cost",l1:"Does not consider who is affected.",l4:"Analyses distribution across groups and over time."},
  {crit:"Justification",l1:"States a preference with no reason.",l4:"Applies a principle, states the strongest counter-argument, holds or revises with reason."}],
 fromDeck:true,
 ex:{"Health, Medical & Life Sciences":"Justify a rule for allocating scarce treatment; say who loses.","Sciences":"Decide whether to publish a finding that could be misused.","Engineering":"Choose between the legal discharge limit and the ecological one.","Computer Science & IT":"Adjudicate a data-privacy trade-off; name who bears the cost.","Mathematics & Statistics":"Choose the fairness definition inside an allocation algorithm.","Education":"Weigh raising standards against widening access; state the principle.","Business & Economics":"Argue what a mine's rehabilitation provision should cover.","Languages & Communication":"Examine whose story a translation keeps and whose it erases.","Sociology, Psychology & Human Development":"Decide whose voice counts in a community consultation.","Architecture & Design":"Weigh heritage conservation against housing need on one site.","Agriculture, Forestry & Environmental Science":"Adjudicate between farm productivity and biodiversity on one landholding."}},

{n:4,key:"strategic",name:"Strategic Competency",one:"Build the pathway",
 def:"Turning an intention into a sequenced, resourced plan that somebody owns.",
 meaning:"Students find where a small intervention produces a large effect, then build the pathway: who acts, in what order, with what resources, against which obstacle, by when.",
 shift:"The shift is from proposing a goal to designing the route to it.",
 obs:["Identifies a leverage point and justifies why","Sequences actions with owners and resources","Names the likely obstacle and a response"],
 note:"Students reach for awareness campaigns; leverage analysis usually points to defaults, procurement rules and pricing. Easiest of the eight to assess, because a plan is a concrete output.",
 methods:"Theory of change \u00b7 leverage analysis \u00b7 90-day action plan",
 ped:"Project-based learning",
 evidence:"Implementation plan with owners and sequence",
 rubric:[
  {crit:"Leverage point",l1:"Proposes an awareness campaign or a general goal.",l4:"Identifies a leverage point and justifies why it moves the system more than the alternatives."},
  {crit:"Sequence and resources",l1:"Lists actions with no order, owner or cost.",l4:"Sequences actions with owners, resources and dependencies, and states what must happen first."},
  {crit:"Obstacles",l1:"Assumes the plan proceeds unopposed.",l4:"Names the most likely obstacle, who raises it, and a proportionate response."}],
 ex:{"Health, Medical & Life Sciences":"Plan medical-waste reduction with owners, sequence and the likely obstacle.","Sciences":"Plan how a lab cuts solvent use without halting research.","Engineering":"Sequence a retrofit, with owners and costs, so the building stays occupied.","Computer Science & IT":"Plan to cut a software service's carbon cost; name the leverage point.","Mathematics & Statistics":"Identify which variable moves the system most, then sequence around it.","Education":"Design a 90-day plan to embed one sustainability practice.","Business & Economics":"Build a 90-day plan to shift one supplier, with costs.","Languages & Communication":"Design a campaign that changes behaviour, not just awareness.","Sociology, Psychology & Human Development":"Plan an intervention starting with the most persuadable group.","Architecture & Design":"Sequence a low-carbon design pathway with dependencies and owners.","Agriculture, Forestry & Environmental Science":"Plan watershed or farm management; state what must happen first."}},

{n:5,key:"collaboration",name:"Collaboration Competency",one:"Work across difference",
 def:"Working productively across difference of discipline, interest and power.",
 meaning:"Students find who holds relevant knowledge and who is affected, listen closely enough to represent another position accurately, handle disagreement without suppressing it or winning at all costs, and involve people while the design can still change.",
 shift:"The shift is from dividing work to integrating difference.",
 obs:["Represents accurately a position they disagree with","Identifies affected groups absent from the process","Helps resolve disagreement rather than avoid it"],
 note:"A group report is evidence of a group, not of an individual. Always pair it with an individual output \u2014 a revision log, a reflective account, a justified peer assessment.",
 methods:"Role-played negotiation \u00b7 cross-disciplinary teams \u00b7 peer critique",
 ped:"SULAM \u00b7 project-based \u00b7 role-play",
 evidence:"Individual revision log and justified peer assessment",
 rubric:[
  {crit:"Representing other positions",l1:"Describes only their own position.",l4:"States a position they disagree with accurately enough that its holder would accept the account."},
  {crit:"Who is absent",l1:"Considers only the people in the room.",l4:"Identifies affected groups absent from the process and what their absence changed."},
  {crit:"Handling disagreement",l1:"Avoids or suppresses the disagreement.",l4:"Surfaces it, works it through, and shows how it changed the outcome."}],
 ex:{"Health, Medical & Life Sciences":"Reach one care plan with a multidisciplinary team that first disagreed.","Sciences":"Reach one conclusion with a team that read the data differently.","Engineering":"Resolve a clash between structural, mechanical and cost needs.","Computer Science & IT":"Reconcile security, cost and usability across a cross-functional build.","Mathematics & Statistics":"Agree modelling assumptions with those who use the results.","Education":"Co-design a teaching intervention with a partner school.","Business & Economics":"Negotiate a supplier contract both sides can sustain.","Languages & Communication":"Interpret between two sides without flattening either.","Sociology, Psychology & Human Development":"Co-design research with the community being researched.","Architecture & Design":"Reconcile client, planner and community needs in one scheme.","Agriculture, Forestry & Environmental Science":"Co-develop practices with farmers whose priorities differ from yours."}},

{n:6,key:"critical",name:"Critical Thinking",one:"Question the claim",
 def:"Questioning claims, evidence, assumptions and framings \u2014 including your own.",
 meaning:"Students separate evidence from assertion, examine who made a claim and how it was measured, and question the framing of the problem itself: what the question makes visible and what it hides. They take a considered position rather than accepting or rejecting wholesale.",
 shift:"The shift is from evaluating the answer to interrogating the question.",
 obs:["Evaluates the source, method and limits of evidence","Identifies an assumption inside the framing","States the weakest point of their own position"],
 note:"Distinguish it from scepticism: critical thinking turns on the student's own position too, cynicism never does. The third behaviour is the highest-value rubric criterion in the whole set.",
 methods:"Claim audits \u00b7 greenwashing analysis \u00b7 method critique",
 ped:"Problem-based \u00b7 case-based",
 evidence:"Claim audit or source critique",
 rubric:[
  {crit:"Evidence",l1:"Repeats claims as given.",l4:"Evaluates source, method and limits, and states what the evidence cannot show."},
  {crit:"Framing",l1:"Accepts the question exactly as posed.",l4:"Identifies an assumption inside the framing and what that framing makes invisible."},
  {crit:"Own position",l1:"Asserts a position, or rejects everything wholesale.",l4:"States the weakest point of their own position and responds to it."}],
 ex:{"Health, Medical & Life Sciences":"Appraise evidence for an intervention, including funding and sample.","Sciences":"Audit a study's method, sample and limits before citing it.","Engineering":"Question whether the design brief solves the real problem.","Computer Science & IT":"Evaluate a benchmark behind an AI-performance claim.","Mathematics & Statistics":"Expose the assumption that makes a statistic convincing.","Education":"Critique the evidence base for a popular teaching method.","Business & Economics":"Test three 'eco-friendly' claims against the evidence.","Languages & Communication":"Analyse how word choice frames who gets blamed.","Sociology, Psychology & Human Development":"Ask what a survey question makes impossible to say.","Architecture & Design":"Interrogate a 'green building' rating against its own data.","Agriculture, Forestry & Environmental Science":"Audit two competing green-material or yield claims."}},

{n:7,key:"selfaware",name:"Self-awareness",one:"Examine your role",
 def:"Examining your own role, values and impact inside the system you study.",
 meaning:"Students locate themselves in the problem \u2014 as beneficiary, contributor, bystander or agent \u2014 recognise how their background and discipline shaped how they framed it, and handle the emotional weight of these topics without dismissal or paralysis.",
 shift:"The shift is from studying the problem to being situated within it.",
 obs:["Locates their own role specifically, not in general","Says how their background shaped the framing","Names a change they control, and its cost"],
 note:"The assessment risk is rewarding performed confession. Mark the specificity and the reasoning, never the sentiment. Reflection must be prompted \u2014 unprompted reflection produces sentiment, not assessable evidence.",
 methods:"Reflective journals with prompts \u00b7 footprint comparison",
 ped:"SULAM \u00b7 field and work-based learning",
 evidence:"Reflective account written against set prompts",
 rubric:[
  {crit:"Locating yourself",l1:"Writes about the problem in general terms only.",l4:"Locates their specific role \u2014 beneficiary, contributor, bystander or agent \u2014 with evidence."},
  {crit:"Background and framing",l1:"Presents their own view as neutral.",l4:"Shows how background and discipline shaped the framing, and what that hid from view."},
  {crit:"Change and its cost",l1:"States a good intention with no cost attached.",l4:"Names a change within their control and what it would cost them to make it."}],
 ex:{"Health, Medical & Life Sciences":"Reflect on how your background shapes whose account you trust.","Sciences":"State how your discipline shaped the question you asked.","Engineering":"Identify whose convenience your design prioritised, and its cost.","Computer Science & IT":"Notice whose needs your default choices served, and who they excluded.","Mathematics & Statistics":"Notice which assumptions you chose because they were easier.","Education":"Notice how your own schooling shapes what you call good teaching.","Business & Economics":"Compare your own consumption with the advice you wrote.","Languages & Communication":"Notice which register you default to, and who it excludes.","Sociology, Psychology & Human Development":"Write a positionality statement before entering the field.","Architecture & Design":"Ask whose comfort your design centres, and what a change would cost.","Agriculture, Forestry & Environmental Science":"Notice which land use you treat as natural, and what that hides."}},

{n:8,key:"integrated",name:"Integrated Problem-solving",one:"Combine all seven",capstone:true,
 def:"Combining the other seven on a real problem to produce a workable option.",
 meaning:"Students choose which lens the problem needs first, sequence the others behind it, and produce a defensible option rather than a perfect answer. Integration is judgement about which competency this problem requires \u2014 not applying all seven at once.",
 shift:"The shift is from analysis to a decision somebody could act on.",
 obs:["Applies three or more lenses and shows what each revealed","Produces an option that is viable and defensible","States what it trades off, and who bears that"],
 note:"Placement: capstone, final-year project, industrial training and clinical practice only. If a mid-programme course selects it, assess it as an emerging capability with the rubric capped at level 3, and declare that in the course outline.",
 methods:"Real-client projects \u00b7 design charrettes \u00b7 capstone defence",
 ped:"Capstone project \u00b7 work-based learning",
 evidence:"Capstone report with an oral defence",
 rubric:[
  {crit:"Choice of lenses",l1:"Applies one lens, or names several without using any.",l4:"Applies three or more, shows what each revealed, and justifies the sequence."},
  {crit:"The option",l1:"Describes the problem and recommends nothing actionable.",l4:"Produces a viable option that holds up under challenge and real constraints."},
  {crit:"Trade-offs",l1:"Presents the option as costless.",l4:"States what it trades off, who bears that, and what would change the recommendation."}],
 ex:{"Health, Medical & Life Sciences":"Healthcare innovation project with a real partner, defended orally.","Sciences":"Final-year project on a real environmental problem with a client.","Engineering":"Capstone design with a live site, budget and community.","Computer Science & IT":"Capstone system for a real client, with trade-offs stated.","Mathematics & Statistics":"Build a decision model for an organisation's real dilemma.","Education":"Design, deliver and evaluate a real teaching intervention.","Business & Economics":"Consultancy project delivering a defensible recommendation.","Languages & Communication":"Design and deliver a real communication strategy for a partner.","Sociology, Psychology & Human Development":"Community-based research producing an actionable proposal.","Architecture & Design":"Capstone design for a real occupant, site and budget.","Agriculture, Forestry & Environmental Science":"Integrated land or food-system project, defended before a panel."}}
];
const byKey=k=>C.find(c=>c.key===k);

const DISTINCT=[
 {a:"Systems",b:"Integrated",text:"Systems analyses how the parts interact. Integrated decides what to do."},
 {a:"Critical",b:"Normative",text:"Critical asks if a claim is true. Normative asks if it is right, and for whom."},
 {a:"Anticipatory",b:"Strategic",text:"Anticipatory imagines possible futures. Strategic builds the route."},
 {a:"Collaboration",b:"group work",text:"Group work divides labour. Collaboration integrates people who disagree."}
];

const PEDAGOGIES=[
 {name:"Problem-Based Learning",sub:"Students meet the problem before the content.",
  does:"Work in tutorial groups on an ill-structured problem with no single right answer. They define what they need to know, then go and learn it.",
  develops:["systems","critical","collaboration"],
  assess:"The problem definition and the reasoning trail \u2014 not only the final solution. Add an individual reasoning log to the group output.",
  watch:"Marking only the solution rewards the group that guessed well. The competency is visible in how the problem was framed."},
 {name:"Project-Based Learning",sub:"Students produce a real deliverable for a real audience.",
  does:"Work over several weeks toward an output \u2014 a design, a plan, a campaign, a prototype \u2014 with milestones and a defined client or audience.",
  develops:["strategic","integrated","collaboration"],
  assess:"The plan and its sequencing at milestone reviews, plus the output and an individual contribution record.",
  watch:"A polished final output can hide a weak process. Assess at milestones, not only at submission."},
 {name:"Gamification and Simulation",sub:"Students decide under rules, roles and consequences.",
  does:"Play a simulation, negotiation game or resource dilemma where choices have consequences and feedback arrives quickly.",
  develops:["anticipatory","normative","systems"],
  assess:"The debrief, never the score. Ask what strategy they used, what values drove it, and what they would change next round.",
  watch:"Points measure play, not competence. A student can win by exploiting the rules and learn nothing."},
 {name:"SULAM \u00b7 Service Learning",sub:"Students apply course content to a genuine community need.",
  does:"Work with a community partner on a real need, with the partner as a genuine collaborator rather than a recipient.",
  develops:["collaboration","selfaware","normative"],
  assess:"A structured reflective journal against set prompts, partner feedback, and the output delivered to the community.",
  watch:"Hours served is not evidence. Neither is gratitude. Mark the specificity of the reflection and the quality of the partnership."},
 {name:"Case-Based Learning and Role-Play",sub:"Students take a position and defend it under challenge.",
  does:"Take a role in a realistic scenario, decide under constraints and incomplete information, then defend the decision to people who disagree.",
  develops:["normative","collaboration","anticipatory"],
  assess:"The written justification produced after the role-play, and the revision made after being challenged.",
  watch:"Performance skill is not competence. A confident speaker with weak reasoning should not score highly."},
 {name:"Field, Laboratory and Work-Based Learning",sub:"Students meet the real constraints of a real setting.",
  does:"Work in a site, laboratory or workplace where decisions have consequences and conditions are not idealised.",
  develops:["systems","selfaware","integrated"],
  assess:"Supervised observation against published criteria, plus a reflective account linking what was observed to what was decided.",
  watch:"Attendance and completion are not competence. Observation needs criteria, or it becomes an impression."}
];

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
const state={pid:null,code:"",disc:"",seen:{},q1:null,q2:null,build:{course:"",cluster:"",sdg:"",comps:[],clo:{},activity:{},output:{},rubric:{}}};
function uid(){return "p"+Math.random().toString(36).slice(2,9)+Date.now().toString(36).slice(-4);}
async function loadLocal(){
  let pid=await S.get("esd8v2:pid");
  if(!pid){pid=uid();await S.set("esd8v2:pid",pid);}
  state.pid=pid;
  const saved=await S.get("esd8v2:progress");
  if(saved)Object.assign(state,saved,{pid});
  if(!state.build)state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},activity:{},output:{},rubric:{}};
}
let saveTimer=null;
function saveLocal(){
  clearTimeout(saveTimer);
  saveTimer=setTimeout(()=>{
    S.set("esd8v2:progress",{code:state.code,disc:state.disc,seen:state.seen,q1:state.q1,q2:state.q2,build:state.build});
    const el=document.getElementById("railSaved");if(el)el.textContent="Saved on this device.";
  },400);
}
function markSeen(v){ if(["understand","lens","pedagogy","assess"].includes(v)){state.seen[v]=true;saveLocal();paintTicks();} }
function paintTicks(){
  document.querySelectorAll("[data-tick]").forEach(t=>{
    const k=t.dataset.tick;
    if(k==="quiz1")t.textContent=state.q1?"\u2713":"";
    else if(k==="quiz2")t.textContent=state.q2?"\u2713":"";
    else t.textContent=state.seen[k]?"\u2713":"";
  });
}

/* ============================================================
   NAV
   ============================================================ */
const VIEWS=["understand","lens","quiz1","pedagogy","assess","quiz2","build","facil","detail"];
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
document.getElementById("saveCode").addEventListener("click",()=>{
  const v=document.getElementById("codeIn").value.trim().toUpperCase();
  state.code=v;document.getElementById("railCode").textContent=v||"not set";
  document.getElementById("fCode").value=v;saveLocal();
});

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
  shuffle(DISTINGUISH).slice(0,8).forEach(x=>items.push(Object.assign({type:"distinguish"},x)));
  return shuffle(items);
}

function buildQ2(){
  const items=[];
  shuffle(FAULTS).slice(0,4).forEach(f=>items.push({type:"fault",stem:f.stem,q:"Which rubric fault is this?",ans:f.ans,why:f.why,
    opts:[{v:"adjectives",t:"Adjectives, not descriptors"},{v:"counting",t:"Levels separated by counting"},{v:"restates",t:"Criterion restates the brief"},{v:"after",t:"Written after the task"},{v:"none",t:"No fault \u2014 this one works"}]}));
  shuffle(ALIGNFAIL).slice(0,3).forEach(f=>items.push({type:"align",stem:f.stem,q:"Which alignment failure is this?",ans:f.ans,why:f.why,
    opts:[{v:"decoration",t:"SDG as decoration"},{v:"nocld",t:"Competency with no CLO"},{v:"fivesdg",t:"One CLO, five SDGs"},{v:"reverse",t:"Reverse-engineered PLO mapping"},{v:"taskmiss",t:"Task misses the competency"}]}));
  shuffle(TRAPQ).slice(0,3).forEach(f=>items.push({type:"trap",stem:f.stem,q:"Which marking trap is this?",ans:f.ans,why:f.why,
    opts:[{v:"group",t:"Marking the group"},{v:"sincerity",t:"Marking sincerity"},{v:"position",t:"Marking the position"}]}));
  shuffle(C).slice(0,3).forEach(c=>items.push({type:"evidence",comp:c.key,stem:`Your course assesses ${c.name}. Which output carries the evidence?`,ans:c.key,why:`${c.evidence}. Choose the output first \u2014 the rubric follows from it.`,
    opts:shuffle(shuffle(C.filter(x=>x.key!==c.key)).slice(0,3).map(x=>({v:x.key,t:x.evidence})).concat([{v:c.key,t:c.evidence}]))}));
  shuffle(PEDAGOGIES).slice(0,3).forEach(p=>{
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
  const items = id==="q1"?buildQ1():buildQ2();
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
      <div style="margin-top:14px"><button class="btn small next hidden"></button></div>
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
  const typeNames={identify:"Identifying from behaviour",field:"Recognising it in your field",distinguish:"Telling the confused pairs apart",fault:"Diagnosing rubric faults",align:"Spotting alignment failures",trap:"Spotting marking traps",evidence:"Choosing the evidence output",pedagogy:"Matching pedagogy to competency",task:"Judging whether a task assesses it"};
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
    <div class="grid2" style="margin-top:18px">
      <div><label class="fl" for="${id}Name">Name <span class="hint">\u2014 optional</span></label><input type="text" id="${id}Name" placeholder="Leave blank to stay anonymous"></div>
      <div><label class="fl" for="${id}Dept">Department <span class="hint">\u2014 optional</span></label><input type="text" id="${id}Dept" placeholder="e.g. Chemical & Environmental Engineering"></div>
    </div>
    <p class="noprint" style="margin-top:16px;display:flex;gap:10px;flex-wrap:wrap">
      <button class="btn moss" data-submit="${id}">Submit to workshop</button>
      <button class="btn ghost" data-retake="${id}">Take it again</button>
      ${id==="q1"?'<button class="btn ghost" data-goto="pedagogy">Continue to pedagogy \u2192</button>':'<button class="btn ghost" data-goto="assess">Back to assessment \u2192</button>'}
    </p>
    <div class="status" data-st="${id}"></div></div>`;
  el.querySelector(`[data-retake="${id}"]`).addEventListener("click",()=>{
    document.getElementById(id+"intro").classList.remove("hidden");el.classList.add("hidden");
  });
  el.querySelector(`[data-submit="${id}"]`).addEventListener("click",()=>submit(id));
  el.querySelectorAll("[data-goto]").forEach(b=>b.addEventListener("click",()=>{const v=b.dataset.goto;show(v);}));
}

async function submit(id){
  const st=document.querySelector(`[data-st="${id}"]`);
  if(!state.code){st.innerHTML='<span class="err">Set a workshop code first \u2014 the field is at the top of stage 01.</span>';return;}
  const payload={pid:state.pid,at:new Date().toISOString(),
    name:(document.getElementById(id+"Name").value||"").trim(),
    dept:(document.getElementById(id+"Dept").value||"").trim(),
    disc:state.disc||"",q1:state.q1||null,q2:state.q2||null};
  const r=await S.set(`esd8v2:room:${state.code}:${state.pid}`,payload,true);
  st.textContent=r===null?"":`Submitted to ${state.code}. Submitting again replaces your previous entry, so both quizzes stay together.`;
  if(r===null)st.innerHTML='<span class="err">Could not reach shared storage. Screenshot this result and send it to your facilitator.</span>';
}

/* ============================================================
   04 PEDAGOGY + 05 ASSESS rendering
   ============================================================ */
function renderPedagogy(){
  const w=document.getElementById("pedCards");w.innerHTML="";
  PEDAGOGIES.forEach(p=>{
    const el=document.createElement("div");el.className="card";
    el.innerHTML=`<h3>${p.name}</h3>
      <p style="color:var(--ink-soft);font-size:15px;margin:4px 0 12px">${p.sub}</p>
      <div class="grid2">
        <div><div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--ink-soft)">WHAT STUDENTS DO</div>
          <p style="margin-top:6px;font-size:14.8px">${p.does}</p>
          <div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--ink-soft);margin-top:12px">DEVELOPS BEST</div>
          <p style="margin-top:8px">${p.develops.map(k=>`<span class="chip m">${byKey(k).name}</span>`).join("")}</p></div>
        <div><div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--moss)">ASSESS IT BY</div>
          <p style="margin-top:6px;font-size:14.8px">${p.assess}</p>
          <div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--rose);margin-top:12px">WATCH OUT</div>
          <p style="margin-top:6px;font-size:14.8px">${p.watch}</p></div>
      </div>`;
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
      <tbody>${c.rubric.map(r=>`<tr><td class="k">${r.crit}</td><td>${r.l1}</td><td>${r.l4}</td></tr>`).join("")}</tbody></table>
      <p style="margin-top:12px;font-size:14.4px;color:var(--ink-soft)">Each criterion comes from one observable behaviour: ${c.obs.map(o=>`<em>${o.toLowerCase()}</em>`).join("; ")}. Fill levels 2 and 3 by splitting the gap \u2014 connects, then justifies.</p>`;
  };
  s.addEventListener("change",paint);paint();
}

/* ============================================================
   07 FACILITATOR
   ============================================================ */
document.getElementById("loadBtn").addEventListener("click",async()=>{
  const code=document.getElementById("fCode").value.trim().toUpperCase();
  const st=document.getElementById("facStatus"),out=document.getElementById("facOut");
  if(!code){st.innerHTML='<span class="err">Enter the workshop code you gave participants.</span>';return;}
  st.textContent="Loading\u2026";out.innerHTML="";
  const keys=await S.list(`esd8v2:room:${code}:`,true);
  if(!keys.length){st.textContent=`No submissions yet under ${code}. Participants submit at the end of each quiz.`;return;}
  const rows=[];for(const k of keys){const v=await S.get(k,true);if(v)rows.push(v);}
  st.textContent=`${rows.length} participant${rows.length===1?"":"s"} under ${code}.`;

  const meanOf=q=>{const s=rows.filter(r=>r[q]&&r[q].total);return s.length?Math.round(s.reduce((a,r)=>a+r[q].score/r[q].total,0)/s.length*100):null;};
  const doneOf=q=>rows.filter(r=>r[q]&&r[q].total).length;
  const agg=(q,field)=>{const o={};rows.forEach(r=>{if(r[q]&&r[q][field])Object.entries(r[q][field]).forEach(([k,v])=>{const p=o[k]||{c:0,n:0};p.c+=v.c;p.n+=v.n;o[k]=p;});});return o;};
  const comp1=agg("q1","perComp"),comp2=agg("q2","perComp");
  const compAll={};[comp1,comp2].forEach(src=>Object.entries(src).forEach(([k,v])=>{const p=compAll[k]||{c:0,n:0};p.c+=v.c;p.n+=v.n;compAll[k]=p;}));
  const type1=agg("q1","perType"),type2=agg("q2","perType");
  const discCount={};rows.forEach(r=>{if(r.disc)discCount[r.disc]=(discCount[r.disc]||0)+1;});
  const typeNames={identify:"Identifying from behaviour",field:"Recognising it in their field",distinguish:"Telling the confused pairs apart",fault:"Diagnosing rubric faults",align:"Spotting alignment failures",trap:"Spotting marking traps",evidence:"Choosing the evidence output",pedagogy:"Matching pedagogy to competency",task:"Judging whether a task assesses it"};
  const meters=o=>Object.entries(o).sort((a,b)=>(a[1].c/a[1].n)-(b[1].c/b[1].n)).map(([k,v])=>{
    const p=Math.round(v.c/v.n*100),cls=p<50?"low":p<75?"mid":"";
    const nm=byKey(k)?byKey(k).name:(typeNames[k]||k);
    return `<div class="meter"><span>${nm}</span><span class="bar"><i class="${cls}" style="width:${p}%"></i></span><span class="val">${p}%</span></div>`;}).join("")||"<p>No data yet.</p>";

  out.innerHTML=`
  <div class="grid3">
    <div class="card"><div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--ink-soft)">PARTICIPANTS</div><h2 style="margin-top:6px">${rows.length}</h2></div>
    <div class="card"><div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--ink-soft)">QUIZ 1 MEAN</div><h2 style="margin-top:6px">${meanOf("q1")===null?"\u2014":meanOf("q1")+"%"}</h2><p style="margin:0;font-size:13px;color:var(--ink-soft)">${doneOf("q1")} of ${rows.length} completed</p></div>
    <div class="card"><div class="mono" style="font-size:11px;letter-spacing:.14em;color:var(--ink-soft)">QUIZ 2 MEAN</div><h2 style="margin-top:6px">${meanOf("q2")===null?"\u2014":meanOf("q2")+"%"}</h2><p style="margin:0;font-size:13px;color:var(--ink-soft)">${doneOf("q2")} of ${rows.length} completed</p></div>
  </div>
  <div class="card"><h3>Weakest competencies across both quizzes</h3>
    <p style="font-size:14px;color:var(--ink-soft)">Under 60% is worth re-teaching before people draft anything.</p>${meters(compAll)}</div>
  <div class="grid2">
    <div class="card"><h3>Quiz 1 \u00b7 by question type</h3>${meters(type1)}</div>
    <div class="card"><h3>Quiz 2 \u00b7 by question type</h3>${meters(type2)}</div>
  </div>
  <div class="card"><h3>Disciplines in the room</h3>
    ${Object.entries(discCount).sort((a,b)=>b[1]-a[1]).map(([k,v])=>`<div class="meter"><span>${k}</span><span class="bar"><i style="width:${v/rows.length*100}%"></i></span><span class="val">${v}</span></div>`).join("")||"<p>No disciplines set yet.</p>"}</div>
  <div class="card"><h3>Submissions</h3>
    <div style="overflow:auto"><table class="tbl"><thead><tr><th>Participant</th><th>Discipline</th><th>Quiz 1</th><th>Quiz 2</th></tr></thead>
    <tbody>${rows.sort((a,b)=>(b.at||"").localeCompare(a.at||"")).map(r=>`<tr>
      <td class="k">${r.name||"Anonymous"}${r.dept?`<br><span style="font-weight:400;color:var(--ink-soft);font-size:12.5px">${r.dept}</span>`:""}</td>
      <td>${r.disc||"\u2014"}</td>
      <td class="mono">${r.q1&&r.q1.total?Math.round(r.q1.score/r.q1.total*100)+"%":"\u2014"}</td>
      <td class="mono">${r.q2&&r.q2.total?Math.round(r.q2.score/r.q2.total*100)+"%":"\u2014"}</td></tr>`).join("")}</tbody></table></div></div>`;
});

/* ============================================================
   BOOT
   ============================================================ */

/* ============================================================
   07 BUILD  — interactive guidebook workflow
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
  const done=[
    !!b.cluster, !!b.sdg, b.comps.length===2,
    b.comps.length===2 && b.comps.every(k=>(b.clo[k]||"").trim()),
    b.comps.length===2 && b.comps.every(k=>b.activity[k]),
    b.comps.length===2 && b.comps.every(k=>(b.output[k]||"").trim()),
    b.comps.length===2 && b.comps.every(k=>rubricFilled(k))
  ];
  const labels=["Content","SDG","Competency","CLO","Activity","Output","Rubric"];
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
function ensureRubric(key){
  const c=byKey(key); const b=B();
  if(!b.rubric[key]){
    b.rubric[key]=c.rubric.map(r=>({crit:r.crit,l1:r.l1,l2:"",l3:"",l4:r.l4}));
  }
}

function renderBuild(){
  const b=B(); const body=document.getElementById("buildBody");
  const clustersOpts=DISCIPLINES.map(d=>`<option value="${d}"${b.cluster===d?' selected':''}>${d}</option>`).join("");
  let h="";

  // STEP 1 — content + cluster
  h+=`<div class="stepcard${b.cluster?' ok':''}">
    <div class="stephead"><span class="stepnum">1</span><h3>Content &amp; cluster</h3></div>
    <div class="stepsub">Start from a course you already teach. Pick the discipline cluster it belongs to.</div>
    <div style="margin-left:36px">
      <label class="fl">Course name <span class="hint">&#8212; code and title</span></label>
      <input type="text" id="bCourse" placeholder="e.g. Urban Water Resources Management" value="${(b.course||'').replace(/"/g,'&quot;')}">
      <label class="fl" style="margin-top:12px">Discipline cluster</label>
      <select id="bCluster"><option value="">&#8212; choose your cluster &#8212;</option>${clustersOpts}</select>
    </div></div>`;

  // STEP 2 — SDG
  h+=`<div class="stepcard${b.sdg?' ok':''}">
    <div class="stephead"><span class="stepnum">2</span><h3>Sustainability challenge &amp; SDG</h3></div>
    <div class="stepsub">Choose one primary SDG your content genuinely touches. One, at most two &#8212; broad mapping fails audit.</div>
    <div class="pickgrid" id="bSdgGrid" style="grid-template-columns:repeat(auto-fill,minmax(210px,1fr))">
      ${SDGS.map(([n,t])=>`<button class="sdgpick" data-sdg="${n}" aria-pressed="${b.sdg==(''+n)}"><span class="sn">${n}</span><span>${t}</span></button>`).join("")}
    </div></div>`;

  // STEP 3 — competencies (exactly 2)
  const nsel=b.comps.length;
  const warn3 = nsel!==2;
  h+=`<div class="stepcard${!warn3?' ok':(nsel>0?' warn':'')}">
    <div class="stephead"><span class="stepnum">3</span><h3>Select exactly two competencies</h3></div>
    <div class="stepsub">Both are assessed under PLO12. Choose two your content can genuinely produce evidence for.</div>
    ${nsel!==2?`<div class="wchip">${nsel} of 2 selected</div>`:''}
    ${b.comps.includes('integrated')?`<div class="wchip">Integrated Problem-solving is capstone / final-year only &#8212; cap the rubric at level 3 mid-programme.</div>`:''}
    <div class="pickgrid" id="bCompGrid">
      ${C.map(c=>`<button class="pick" data-comp="${c.key}" aria-pressed="${b.comps.includes(c.key)}"><span class="pk">${String(c.n).padStart(2,'0')}</span>${c.name}</button>`).join("")}
    </div></div>`;

  // STEPS 4-7 per competency (only if 2 chosen)
  if(b.comps.length===2){
    b.comps.forEach(ensureRubric);

    // STEP 4 CLO
    h+=`<div class="stepcard${b.comps.every(k=>(b.clo[k]||'').trim())?' ok':''}">
      <div class="stephead"><span class="stepnum">4</span><h3>Write a CLO for each, mapped to PLO12</h3></div>
      <div class="stepsub">Use an observable verb. The test: can you write four rubric levels for it?</div>`;
    b.comps.forEach(k=>{
      const c=byKey(k);
      h+=`<div class="blk"><h4>${c.name}</h4><div class="bsub">${c.shift}</div>
        <textarea class="cloin" data-clo="${k}" placeholder="e.g. Evaluate competing options and justify the trade-offs...">${(b.clo[k]||'').replace(/</g,'&lt;')}</textarea>
        <div class="verbhint">Verbs that work: ${VERBS[k].map(v=>`<b>${v}</b>`).join(" &middot; ")}</div></div>`;
    });
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

    // STEP 7 rubric
    h+=`<div class="stepcard${b.comps.every(k=>rubricFilled(k))?' ok':''}">
      <div class="stephead"><span class="stepnum">7</span><h3>Build the rubric</h3></div>
      <div class="stepsub">Three criteria from the observable behaviours. Levels 1 and 4 are drafted &#8212; write 2 and 3 by splitting the gap.</div>`;
    b.comps.forEach((k,ci)=>{
      const c=byKey(k); const rr=b.rubric[k];
      h+=`<div class="blk"><h4>${c.name} &#8212; criteria ${ci*3+1}&#8211;${ci*3+3}</h4>
        <table class="rubedit"><thead><tr><th>Criterion</th><th>1 Limited</th><th>2 Developing</th><th>3 Proficient</th><th>4 Exemplary</th></tr></thead><tbody>
        ${rr.map((row,ri)=>`<tr><td class="rc">${row.crit}</td>
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
  const ready=b.comps.length===2 && b.cluster && b.sdg;
  let rows="";
  if(b.comps.length===2){
    b.comps.forEach((k,ci)=>{
      const c=byKey(k);
      rows+=`<tr><td>${(b.clo[k]||'<span style="color:#9DB1AA">CLO not written</span>')}</td>
        <td class="k" style="width:auto;background:var(--slate-tint);color:var(--slate);font-weight:600">PLO12</td>
        <td>${b.sdg?('SDG '+b.sdg):'&#8212;'}</td>
        <td>${c.name}</td>
        <td>${b.output[k]||c.evidence}, criteria ${ci*3+1}&#8211;${ci*3+3}</td></tr>`;
    });
  }
  return `<div class="alignprev">
    <span class="tag slate">Live alignment table</span>
    <h3 style="margin:12px 0 4px">${b.course||'Your course'}${b.cluster?' &#183; '+b.cluster:''}</h3>
    <p style="font-size:13.5px;color:var(--ink-soft)">Only the CLO is directly assessed; every other column is a claim traceable through it.</p>
    ${b.comps.length===2?`<table class="tbl"><thead><tr><th>CLO</th><th>PLO</th><th>SDG</th><th>ESDC</th><th>Assessed by</th></tr></thead><tbody>${rows}</tbody></table>`:'<p style="color:#9DB1AA;font-size:14px">Select two competencies to assemble the table.</p>'}
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
  const pr=document.getElementById("bPrint"); if(pr)pr.addEventListener("click",()=>window.print());
  const cp=document.getElementById("bCopy"); if(cp)cp.addEventListener("click",copyModule);
  const rs=document.getElementById("bReset"); if(rs)rs.addEventListener("click",()=>{
    if(confirm("Clear this module and start over?")){
      state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},activity:{},output:{},rubric:{}};
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
      if(confirm("Clear this module and start over?")){state.build={course:"",cluster:"",sdg:"",comps:[],clo:{},activity:{},output:{},rubric:{}};saveLocal();renderBuild();}});
  }
}
function markBuildTick(){ renderWfSteps(); }

function copyModule(){
  const b=B(); const L=[];
  L.push("ESD MODULE \u2014 "+(b.course||"Course"));
  L.push("Cluster: "+(b.cluster||"\u2014"));
  L.push("Primary SDG: "+(b.sdg?("SDG "+b.sdg):"\u2014"));
  L.push("Assessed under: PLO12");
  L.push("");
  b.comps.forEach((k,ci)=>{
    const c=byKey(k);
    L.push("\u2014 "+c.name.toUpperCase()+" \u2014");
    L.push("CLO (\u2192PLO12): "+(b.clo[k]||"\u2014"));
    L.push("Activity: "+(b.activity[k]||"\u2014"));
    L.push("Output: "+(b.output[k]||c.evidence));
    L.push("Rubric (criteria "+(ci*3+1)+"\u2013"+(ci*3+3)+"):");
    (b.rubric[k]||[]).forEach(r=>{
      L.push("  "+r.crit);
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


(async function(){
  await loadLocal();
  renderLedger();fillDisc();renderPedagogy();renderRubricPicker();renderBuild();
  document.getElementById("codeIn").value=state.code||"";
  document.getElementById("railCode").textContent=state.code||"not set";
  document.getElementById("railDisc").textContent=state.disc||"not set";
  document.getElementById("fCode").value=state.code||"";
  paintTicks();
  show("understand");
  if(!hasS)document.getElementById("railSaved").textContent="Progress saves in this browser.";
})();
</script>
