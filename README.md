<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sub-40 10K — 47-Week Complete Daily Plan</title>
<link href="https://fonts.googleapis.com/css2?family=Lexend:wght@300;400;500;600;700&family=Fira+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#f5f4f0;--white:#fff;--navy:#0e1c2e;--navy2:#1a2d44;
  --border:#dde2ea;--muted:#6b7a90;
  --amber:#c47a14;--amber-bg:rgba(196,122,20,.09);
  --green:#1a7a3c;--green-bg:rgba(26,122,60,.09);
  --blue:#1d5cbf;--blue-bg:rgba(29,92,191,.09);
  --orange:#d45a0c;--orange-bg:rgba(212,90,12,.09);
  --pink:#c41f6c;--pink-bg:rgba(196,31,108,.09);
  --grey-bg:rgba(107,122,144,.1);
  --gold:#8a5a08;--gold-bg:rgba(138,90,8,.1);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{background:var(--bg);color:var(--navy);font-family:'Lexend',sans-serif;font-weight:300;min-height:100vh;}

header{background:var(--navy);color:white;padding:36px 48px 32px;}
.eyebrow{font-family:'Fira Mono',monospace;font-size:11px;letter-spacing:3px;color:var(--amber);text-transform:uppercase;margin-bottom:10px;}
header h1{font-size:clamp(24px,4vw,46px);font-weight:700;letter-spacing:-1px;margin-bottom:8px;}
header p{font-size:12px;color:rgba(255,255,255,.4);max-width:600px;line-height:1.65;font-weight:300;}

.legend{display:flex;flex-wrap:wrap;gap:8px 18px;padding:12px 48px;background:white;border-bottom:1px solid var(--border);}
.leg-item{display:flex;align-items:center;gap:5px;font-family:'Fira Mono',monospace;font-size:10px;color:var(--muted);}
.leg-dot{width:8px;height:8px;border-radius:2px;flex-shrink:0;}

.phase-nav{display:flex;background:white;border-bottom:2px solid var(--navy);overflow-x:auto;}
.phase-btn{flex:1;min-width:140px;padding:12px 16px;background:white;border:none;border-right:1px solid var(--border);border-bottom:3px solid transparent;margin-bottom:-2px;cursor:pointer;font-family:'Lexend',sans-serif;font-size:12px;font-weight:500;color:var(--muted);text-align:left;white-space:nowrap;transition:all .15s;line-height:1.4;}
.phase-btn.active{color:var(--navy);border-bottom-color:var(--amber);background:#fffdf8;}
.phase-btn:hover{background:var(--bg);}
.phase-btn small{display:block;font-weight:300;font-size:10px;color:var(--muted);margin-top:1px;}

.week-nav{display:flex;flex-wrap:wrap;gap:6px;padding:14px 48px;background:var(--bg);border-bottom:1px solid var(--border);align-items:center;}
.week-nav-label{font-family:'Fira Mono',monospace;font-size:10px;color:var(--muted);margin-right:4px;white-space:nowrap;}
.week-btn{padding:5px 10px;background:white;border:1px solid var(--border);border-radius:3px;cursor:pointer;font-family:'Fira Mono',monospace;font-size:10px;color:var(--muted);transition:all .15s;white-space:nowrap;}
.week-btn.active{background:var(--navy);color:white;border-color:var(--navy);}
.week-btn:hover:not(.active){border-color:var(--navy);color:var(--navy);}
.week-btn.wk-cut{background:#f0f4f8;}
.week-btn.wk-race{border-color:var(--amber);color:var(--amber);}
.week-btn.wk-cut.active,.week-btn.wk-race.active{background:var(--navy);color:white;}

.mileage-bar{display:flex;align-items:center;gap:16px;padding:10px 48px;background:var(--navy);border-bottom:2px solid var(--navy2);}
.mileage-total{font-family:'Fira Mono',monospace;font-size:20px;font-weight:500;color:var(--amber);}
.mileage-label{font-family:'Fira Mono',monospace;font-size:10px;color:rgba(255,255,255,.35);letter-spacing:2px;text-transform:uppercase;}
.mileage-bar-desc{font-family:'Fira Mono',monospace;font-size:10px;color:rgba(255,255,255,.25);margin-left:auto;text-align:right;}

.week-note{padding:10px 48px;background:#fffdf5;border-bottom:1px solid #e8dfc8;font-family:'Fira Mono',monospace;font-size:11px;color:var(--gold);line-height:1.6;}
.week-note strong{color:var(--amber);}

.grid-wrap{padding:16px 48px 56px;overflow-x:auto;}
.week-grid{display:grid;grid-template-columns:repeat(7,minmax(182px,1fr));gap:8px;min-width:1274px;}

.day-card{background:white;border:1px solid var(--border);border-radius:5px;overflow:hidden;display:flex;flex-direction:column;}
.day-hdr{padding:8px 12px;background:var(--navy);color:white;font-family:'Fira Mono',monospace;font-size:11px;font-weight:500;letter-spacing:1.5px;}

.badge{display:inline-block;font-family:'Fira Mono',monospace;font-size:9px;font-weight:500;letter-spacing:1.5px;text-transform:uppercase;padding:2px 7px;border-radius:2px;margin-bottom:5px;}
.b-easy{background:var(--green-bg);color:var(--green);}
.b-long{background:var(--blue-bg);color:var(--blue);}
.b-tempo{background:var(--orange-bg);color:var(--orange);}
.b-intervals{background:var(--pink-bg);color:var(--pink);}
.b-race{background:var(--gold-bg);color:var(--gold);}
.b-rest{background:var(--grey-bg);color:var(--muted);}
.b-strength{background:var(--amber-bg);color:var(--amber);}

.wucd{font-family:'Fira Mono',monospace;font-size:9px;color:#aaa;margin-bottom:4px;line-height:1.4;}
.wucd span{color:var(--amber);}

.run-section{padding:11px 12px;border-bottom:1px solid var(--border);}
.run-rest{padding:10px 12px;background:#f8f7f4;display:flex;flex-direction:column;justify-content:center;min-height:60px;border-bottom:1px solid var(--border);}
.run-str-only{padding:10px 12px;background:#fffbf3;border-bottom:1px solid #eeddb5;display:flex;align-items:center;}
.run-dist{font-family:'Fira Mono',monospace;font-size:15px;font-weight:500;margin-bottom:2px;}
.run-pace{font-family:'Fira Mono',monospace;font-size:10px;color:var(--amber);font-weight:500;margin-bottom:4px;}
.run-note{font-size:10px;color:var(--muted);line-height:1.5;}

.str-section{padding:10px 12px;background:#fafbfc;flex:1;}
.str-head{font-family:'Fira Mono',monospace;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--amber);margin-bottom:7px;}
.ex{padding:5px 0;border-bottom:1px solid #eef0f4;}
.ex:last-child{border-bottom:none;}
.ex-top{display:flex;justify-content:space-between;align-items:baseline;gap:4px;}
.ex-name{font-size:11px;font-weight:500;flex:1;line-height:1.3;}
.ex-wt{font-family:'Fira Mono',monospace;font-size:10px;font-weight:500;color:var(--navy2);white-space:nowrap;}
.ex-sets{font-family:'Fira Mono',monospace;font-size:9px;color:var(--muted);margin-top:1px;}
.ex-cue{font-size:9.5px;color:var(--muted);line-height:1.4;margin-top:1px;}

@media(max-width:640px){
  header,.legend,.week-nav,.mileage-bar,.week-note,.grid-wrap{padding-left:16px;padding-right:16px;}
}
</style>
</head>
<body>

<header>
  <div class="eyebrow">47-Week Complete Plan · 45kg · Sub-40 10K</div>
  <h1>Every Week. Every Day.</h1>
  <p>All 47 weeks with correct session distances including warm-up and cool-down. Weekly mileage shown per week. Cutback weeks marked ↓, race weeks marked ★.</p>
</header>

<div class="legend">
  <div class="leg-item"><div class="leg-dot" style="background:var(--green)"></div>Easy Run</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--blue)"></div>Long Run</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--orange)"></div>Tempo</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--pink)"></div>Intervals</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--gold)"></div>Race</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--amber)"></div>+ Strength</div>
  <div class="leg-item"><div class="leg-dot" style="background:var(--muted)"></div>Rest</div>
</div>

<nav class="phase-nav">
  <button class="phase-btn active" onclick="setPhase(0)">Phase 1 — Rebuild<small>Weeks 1–8</small></button>
  <button class="phase-btn" onclick="setPhase(1)">Phase 2 — Aerobic Base<small>Weeks 9–20</small></button>
  <button class="phase-btn" onclick="setPhase(2)">Phase 3 — Speed Dev.<small>Weeks 21–36</small></button>
  <button class="phase-btn" onclick="setPhase(3)">Phase 4 — Peak &amp; Race<small>Weeks 37–47</small></button>
</nav>

<div class="week-nav"><span class="week-nav-label">WEEK →</span><div id="week-nav"></div></div>
<div class="mileage-bar">
  <div>
    <div class="mileage-label">Weekly Volume</div>
    <div class="mileage-total" id="mileage-total">—</div>
  </div>
  <div class="mileage-bar-desc" id="mileage-desc"></div>
</div>
<div class="week-note" id="week-note"></div>
<div class="grid-wrap"><div class="week-grid" id="week-grid"></div></div>

<script>
const DAYS=['MON','TUE','WED','THU','FRI','SAT','SUN'];
function lerp(a,b,t){return Math.round((a+(b-a)*Math.min(1,Math.max(0,t)))*2)/2;}

// ── Run constructors — all include numeric km field ───────────────────────────
const R={
  rest:(n='Full rest.')=>({type:'rest',km:0,distance:'—',pace:null,wucd:null,note:n}),
  easy:(km,pace,note='')=>({type:'easy',label:'Easy Run',km,distance:km+'km',pace,wucd:null,note:note||'Conversational pace throughout.'}),
  long:(km,pace,note='')=>({type:'long',label:'Long Run',km,distance:km+'km',pace,wucd:null,note:note||'Comfortable effort. Should finish feeling you had more.'}),
  quality:(type,label,wu,workDesc,cd,totalKm,qualPace,note)=>({
    type,km:totalKm,label,distance:'~'+totalKm+'km',pace:qualPace,
    wucd:{wu,cd},workDesc,note:note||''
  }),
  race:(desc,distKm)=>({type:'race',label:'Race',km:distKm||10,distance:(distKm||10)+'km',pace:'Race effort',wucd:null,note:desc}),
  strOnly:()=>({type:'str-only',km:0,distance:null,pace:null,wucd:null,note:null}),
};
const T=(wu,work,cd,km,pace,note)=>R.quality('tempo','Tempo',wu,work,cd,km,pace,note);
const I=(wu,work,cd,km,pace,note)=>R.quality('intervals','Intervals',wu,work,cd,km,pace,note);
const ex=(name,sets,reps,weight,cue='')=>({name,sets,reps,weight,cue});

// ── Strength sessions ─────────────────────────────────────────────────────────
function p1StrA(w,mode){
  const s=mode==='race'?2:3;
  const rdlW=w<4?'BW':w<6?'5kg DB':'8kg DB';
  const bridge=w<3?'Glute Bridge':'SL Glute Bridge';
  const breps=w<3?(mode==='race'?'12':'15'):(mode==='race'?'8/leg':'12/leg');
  const band=w<3?'Light band':'Medium band';
  return {label:'Day A — Posterior Chain',exercises:[
    ex(bridge,s,breps,'BW','Hold 2s at top. Drive hips fully each rep.'),
    ex('Romanian Deadlift',s,mode==='race'?'8':'12',rdlW,'Hinge from hips. Feel hamstring stretch.'),
    ex('SL Calf Raise',s,mode==='race'?'8/leg':'12/leg','BW','3s up, 3s down. Full heel drop off a step.'),
    ex('Side-lying Clam',s,'12–15/side',band,'Isolate glute med. No hip rolling.'),
    ex('Dead Bug',s,mode==='race'?'6/side':'8/side','BW','Lower back to floor. Slow and controlled.'),
    mode==='race'?ex('Couch Stretch',2,'60s/side','—','Mobility priority pre-race.'):ex('Hip Flexor Stretch',2,'45s/side','—','90/90 on floor. Breathe into front hip.'),
  ]};
}
function p1StrB(w,mode){
  const s=mode==='race'?2:3;
  const sqType=w<2?'Split Squat':'Bulgarian Split Squat';
  const dlW=w<5?'BW':'5kg DB';
  const band=w<3?'Light band':'Medium band';
  return {label:'Day B — Single-Leg + Core',exercises:[
    ex(sqType,s,mode==='race'?'6/leg':'10/leg','BW','Front shin stays vertical. Feel the glute.'),
    ex('SL Deadlift',s,mode==='race'?'5/leg':'8/leg',dlW,'Hinge on one leg. Free leg back. Balance first.'),
    ex('Hip Abduction (band)',s,'12–15/side',band,'Standing. Slow kick outward. Pelvis level.'),
    ex('Copenhagen Adduction',s,mode==='race'?'5/side':'8/side','BW — bent knee','Side plank, top leg on bench, lift lower.'),
    ex('Pallof Press',s,'10/side',band,'2s pause at extension. Hips square.'),
    mode==='race'?ex('Couch Stretch',2,'60s/side','—','Mobility priority race week.'):ex('Ankle Dorsiflexion Drill',2,'10/side','—','Knee-to-wall. Heel stays down.'),
  ]};
}
function p2StrA(w,mode){
  const s=mode==='normal'?4:3;
  const t=Math.min(w/10,1);
  const htKg=lerp(25,55,t),calfKg=lerp(8,16,t),rdlKg=lerp(8,16,t);
  const nordic=w<4?'Heavy band':w<8?'Light band/unassisted':'Unassisted';
  const ns=mode==='cutback'?2:3;
  return {label:'Day A — Posterior Chain (Loaded)',exercises:[
    ex('SL RDL',s,mode==='race'?'5/leg':'8/leg',rdlKg+'kg DB','4s eccentric. Hamstring stretch throughout.'),
    ex('Hip Thrust',s,mode==='race'?'5':'8',htKg+'kg','Drive through heels. Full glute squeeze.'),
    ex('SL Calf Raise (weighted)',s,mode==='race'?'6/leg':'10/leg',calfKg+'kg DB','3s down, explosive up. Full ROM.'),
    ex('Nordic Hamstring Curl',ns,w<4?'5':'6–8',nordic,'Lower as slowly as possible.'),
    ex('Copenhagen (straight leg)',ns,'10–12/side','BW','No pelvis drop.'),
    ex('Plank + Hip Extension',ns,'8/side','BW','Hold 3s per rep. Don\'t rotate hips.'),
  ]};
}
function p2StrB(w,mode){
  const s=mode==='normal'?4:3;
  const t=Math.min(w/10,1);
  const bssKg=lerp(8,15,t),stepKg=lerp(8,12,t),glbKg=lerp(10,18,t);
  const sub=mode==='cutback'?2:3;
  return {label:'Day B — Single-Leg Strength',exercises:[
    ex('Bulgarian Split Squat',s,mode==='race'?'5/leg':'8/leg',bssKg+'kg/hand','Upright torso. 3s lowering.'),
    ex('Step-Up (high box)',sub,mode==='race'?'7/leg':'10/leg',stepKg+'kg/hand','Push from top leg only. Drive knee up.'),
    ex('Banded Hip Drive Walk',sub,'20 steps','Heavy band','Drive hip fully each step.'),
    ex('SL Glute Bridge (loaded)',sub,mode==='race'?'8/leg':'12/leg',glbKg+'kg DB','Max glute squeeze at top.'),
    ex('Pallof Press',sub,'10/side','Heavy band','2s pause. Hips square.'),
    ex('Couch Stretch',2,'60s/side','—','Hip flexor release after squats.'),
  ]};
}
function p3StrA(w,mode){
  const s=mode==='normal'?4:3;
  const t=Math.min(w/14,1);
  const htKg=lerp(35,42,t),calfKg=lerp(14,20,t),rdlKg=lerp(16,20,t);
  const ps=mode==='cutback'||mode==='race'?2:3;
  const ns=mode==='cutback'?2:3;
  return {label:'Day A — Power (Plyos First)',exercises:[
    ex('Pogo Jumps',ps,mode==='race'?'15':'20','BW','Stiff ankles. Fast contacts. Minimal knee bend.'),
    ex('SL Pogo Jump',ps,mode==='race'?'8/leg':'10/leg','BW','Build contact speed each week.'),
    ex('Hip Thrust (explosive)',s,mode==='race'?'4':'6',htKg+'kg','Explosive concentric. Fast as possible.'),
    ex('SL RDL',s,mode==='race'?'4/leg':'6/leg',rdlKg+'kg DB','Maintain strength. 4s eccentric.'),
    ex('SL Calf Raise (explosive)',s,mode==='race'?'5/leg':'8/leg',calfKg+'kg DB','3s slow down, explosive drive up.'),
    ex('Nordic Curl',ns,'6–8','Unassisted','Critical as running speeds increase.'),
  ]};
}
function p3StrB(w,mode){
  const s=mode==='normal'?4:3;
  const t=Math.min(w/14,1);
  const bssKg=lerp(10,16,t),stepKg=lerp(10,14,t);
  const ps=mode==='race'?2:mode==='cutback'?3:4;
  const sub=mode==='cutback'?2:3;
  return {label:'Day B — Power + Running Mechanics',exercises:[
    ex('Bounding',ps,mode==='race'?'30m':'40m','BW','Drive off each leg powerfully. Exaggerated stride.'),
    ex('Box Jump',sub,mode==='race'?'3':'5','BW — 40cm','Max effort. Land softly. Step down, reset.'),
    ex('Bulgarian SS (explosive)',s,mode==='race'?'3/leg':'5/leg',bssKg+'kg/hand','Lighter load, maximum speed out of hole.'),
    ex('A-Skip + Arm Drive',ps,'30m','BW','Aggressive knee drive. Arm punch in opposition.'),
    ex('Step-Up + Knee Drive',sub,'8/leg',stepKg+'kg/hand','Drive free knee up hard at top.'),
    ex('Copenhagen',sub,'10/side','BW','Maintain pelvic stability.'),
  ]};
}
function p4StrA(w,mode){
  const isRace=mode==='race',isTaper=mode==='taper1'||mode==='taper2';
  const s=isRace?1:isTaper?2:mode==='cutback'?3:4;
  const t=Math.min(w/6,1);
  const htKg=lerp(40,45,t),rdlKg=lerp(18,20,t),isoKg=lerp(8,12,t);
  const ps=isRace?1:isTaper?2:mode==='cutback'?3:4;
  const exs=[ex('SL Pogo (max speed)',ps,isRace?'5s/leg':isTaper?'8s/leg':'10s/leg','BW','Count contacts. Beat last session.')];
  if(!isRace) exs.push(ex('Depth Drop → Jump',isTaper?2:s,isTaper?'4':'5','BW — 30cm','Step off, land stiff, jump immediately.'));
  exs.push(
    ex('Hip Thrust (explosive)',s,isRace?'3':'5',htKg+'kg','Maximal explosive concentric.'),
    ex('SL RDL (maintain)',s,isRace?'3/leg':'5/leg',rdlKg+'kg DB','Heavy. Controlled. Don\'t let strength decay.'),
    ex('Calf Raise Iso Hold',s,isRace?'20s/leg':'30s/leg','BW+'+isoKg+'kg','Rise, hold at top, lower slowly.'),
    ex('Nordic Curl',isRace?1:2,'5–6','Unassisted','Injury prevention at goal-race speeds.'),
  );
  return {label:isRace?'Day A — Race Week (Light)':isTaper?'Day A — Taper Maintenance':'Day A — Reactive + Maintain',exercises:exs};
}
function p4StrB(w,mode){
  const isTaper=mode==='taper1'||mode==='taper2';
  const s=isTaper?2:mode==='cutback'?3:4;
  const t=Math.min(w/6,1);
  const bssKg=lerp(16,20,t);
  return {label:isTaper?'Day B — Taper Mechanics':'Day B — Speed-Specific Mechanics',exercises:[
    ex('Hurdle Hops',s,isTaper?'5 hurdles':'6 hurdles','BW — 30cm','Stiff ankles. Minimum ground contact time.'),
    ex('SL Bound (max distance)',s,isTaper?'4/leg':'5/leg','BW','Maximum distance each bound.'),
    ex('Fast Leg Drill',s,isTaper?'12s':'15s','BW','Max cadence in place. Knees up.'),
    ex('Bulgarian SS (heavy+explosive)',s,isTaper?'3/leg':'4/leg',bssKg+'kg/hand','Heavy and fast. Maximum power per rep.'),
    ex('Copenhagen',2,'10/side','BW','Maintain lateral stability.'),
    ex('Running Mobility Circuit',1,'5 min','—','Leg swings, hip circles, lunge+rotation.'),
  ]};
}

// ── Quality sessions (tempo & intervals) ────────────────────────────────────
// All distances are numeric km totals (WU + reps + recovery jogs + CD)
const P1_THU=[
  null,null,null,null,
  T(2,'15min @ 5:45–6:00/km',2,6.5,'5:45–6:00/km','WU 2km easy → 15min tempo → CD 2km. Do not start the tempo until fully warmed up. First quality session of the plan.'),
  T(2,'20min @ 5:45–6:00/km',2,7.5,'5:45–6:00/km','WU 2km → 20min tempo → CD 2km. Should feel comfortably hard — not easy, not a struggle.'),
  T(2,'25min @ 5:45–6:00/km',2,8.5,'5:45–6:00/km','WU 2km → 25min tempo → CD 2km. Longest tempo of Phase 1. Keep it controlled.'),
  null,
];

const P2_THU=[
  T(2,'2×15min @ 5:30–5:45/km, 3min easy jog between',2,10,'5:30–5:45/km','WU 2km → 15min → 3min jog → 15min → CD 2km. The jog between reps is active — don\'t stop.'),
  T(2,'2×20min @ 5:30–5:45/km, 3min easy jog between',2,11.5,'5:30–5:45/km','WU 2km → 20min → 3min → 20min → CD 2km. Back off pace slightly if form deteriorates in rep 2.'),
  T(2,'30min continuous @ 5:30–5:45/km',2,9.5,'5:30–5:45/km','WU 2km → 30min tempo → CD 2km. First long continuous tempo. Settle into a rhythm.'),
  T(2,'20min @ 5:30–5:45/km (cutback week)',2,7.5,'5:30–5:45/km','WU 2km → 20min → CD 2km. Cutback week — short tempo.'),
  T(2,'35min continuous @ 5:15–5:30/km',2,10.5,'5:15–5:30/km','WU 2km → 35min → CD 2km. Pace picks up slightly this block.'),
  T(2,'3×12min @ 5:15–5:30/km, 2min easy jog between',2,11.5,'5:15–5:30/km','WU 2km → 12min → 2min → 12min → 2min → 12min → CD 2km. 36 total minutes of tempo.'),
  T(2,'40min continuous @ 5:15–5:30/km',2,11.5,'5:15–5:30/km','WU 2km → 40min → CD 2km. If you fade in the last 10min, ease off pace rather than stopping.'),
  T(2,'25min @ 5:15–5:30/km (cutback week)',2,8.5,'5:15–5:30/km','WU 2km → 25min → CD 2km. Brief and quality.'),
  T(2.5,'3×15min @ 5:00–5:20/km, 2min easy jog between',2,14,'5:00–5:20/km','WU 2.5km → 15min → 2min → 15min → 2min → 15min → CD 2km. 45 total minutes of threshold.'),
  T(2.5,'45min continuous @ 5:00–5:20/km',2,13.5,'5:00–5:20/km','WU 2.5km → 45min → CD 2km. Continuous threshold. Heart rate high and stable.'),
  T(2.5,'50min continuous @ 5:00–5:20/km',2,14.5,'5:00–5:20/km','WU 2.5km → 50min → CD 2km. Phase 2 peak tempo. 50 minutes at threshold.'),
  null,
];

const P3_TUE=[
  I(2.5,'6×800m @ 4:45–5:05/km, 90s easy jog between',1.5,10,'4:45–5:05/km','WU 2.5km → 6×800m (90s jog recovery) → CD 1.5km. Last rep should not be dramatically slower than first.'),
  I(2.5,'5×1000m @ 4:45–5:05/km, 2min easy jog between',1.5,10,'4:45–5:05/km','WU 2.5km → 5×1000m (2min jog) → CD 1.5km. Hold pace consistently across all 5 reps.'),
  I(2.5,'4×1200m @ 4:45–5:05/km, 2min easy jog between',1.5,10,'4:45–5:05/km','WU 2.5km → 4×1200m (2min jog) → CD 1.5km. The first 600m of each rep should feel controlled.'),
  I(2.5,'5×800m @ controlled effort, 2min jog between',1.5,9,'4:55–5:10/km','WU 2.5km → 5×800m (2min jog) → CD 1.5km. Cutback week — same structure, slightly relaxed.'),
  I(2.5,'3×2000m @ 10k effort, 3min easy jog between',1.5,11,'4:45–5:05/km','WU 2.5km → 3×2000m (3min jog) → CD 1.5km. 10k effort for 2km per rep.'),
  I(2.5,'6×1000m @ 10k effort, 2min easy jog between',1.5,11.5,'4:45–5:05/km','WU 2.5km → 6×1000m (2min jog) → CD 1.5km. 6km of hard running total. Reps 5 and 6 should feel very hard.'),
  I(2.5,'5×1200m @ 10k effort, 2min easy jog between',1.5,11,'4:45–5:05/km','WU 2.5km → 5×1200m (2min jog) → CD 1.5km. Consistency across reps more important than raw pace.'),
  I(2.5,'6×800m @ controlled effort, 2min jog between',1.5,10,'4:50–5:05/km','WU 2.5km → 6×800m (2min jog) → CD 1.5km. Cutback week intervals.'),
  I(2.5,'8×600m @ faster than 10k pace, 90s jog between',1.5,10.5,'4:35–4:55/km','WU 2.5km → 8×600m (90s jog) → CD 1.5km. Short sharp reps. Quick turnover, not maximum sprint.'),
  I(2.5,'2 sets of 5×400m @ mile effort, 60s jog within set, 3min jog between sets',1.5,9.5,'4:35–4:50/km','WU 2.5km → 5×400m → 3min → 5×400m → CD 1.5km. Speed work. Hard but not sprint.'),
  I(2.5,'4×1600m @ 10k effort, 3min easy jog between',1.5,12,'4:35–4:55/km','WU 2.5km → 4×1600m (3min jog) → CD 1.5km. Peak interval session of Phase 3.'),
  null,
  I(2.5,'6×1000m @ 4:00/km (goal race pace), 90s easy jog between',1.5,11,'4:00/km','WU 2.5km → 6×1000m (90s jog) → CD 1.5km. First goal-pace reps. Should feel hard but manageable.'),
  I(2.5,'4×2000m @ 4:00/km, 2min easy jog between',1.5,13,'4:00/km','WU 2.5km → 4×2000m (2min jog) → CD 1.5km. 2km per rep at goal pace. Focus on even splits.'),
  R.quality('intervals','Progression Run',2,'3km easy → 4km @ 5:00–5:15/km → 3km @ 4:00/km',2,14,'4:00/km (final 3km)','WU 2km → continuous 10km progression run → CD 2km. Simulates race demands on tired legs.'),
  I(2.5,'5×1000m @ controlled effort, 2min jog between',1.5,10,'4:45–5:00/km','WU 2.5km → 5×1000m (2min jog) → CD 1.5km. Cutback week. Focus on form.'),
];

const P3_THU=[
  T(2.5,'30min @ 4:55–5:15/km',2,10.5,'4:55–5:15/km','WU 2.5km → 30min tempo → CD 2km. Keep this clearly below Tuesday\'s interval intensity.'),
  T(2.5,'35min @ 4:55–5:15/km',2,11.5,'4:55–5:15/km','WU 2.5km → 35min → CD 2km. Sustained and controlled rather than sharp.'),
  T(2.5,'40min @ 4:55–5:15/km',2,12.5,'4:55–5:15/km','WU 2.5km → 40min → CD 2km. Phase 3 early-block peak tempo.'),
  null,
  T(2.5,'40min @ 4:55–5:15/km',2,12.5,'4:55–5:15/km','WU 2.5km → 40min → CD 2km. Manage energy across both Tue and Thu quality sessions.'),
  T(2.5,'45min @ 4:55–5:15/km',2,13.5,'4:55–5:15/km','WU 2.5km → 45min → CD 2km. The week total is the highest quality load so far.'),
  T(2.5,'50min @ 4:55–5:15/km',2,14.5,'4:55–5:15/km','WU 2.5km → 50min → CD 2km. Phase 3 mid-block peak tempo.'),
  null,
  T(2.5,'50min @ 4:45–5:05/km',2,15,'4:45–5:05/km','WU 2.5km → 50min → CD 2km. Pace ticks up slightly. This should feel similar difficulty to week 27 — fitness has grown.'),
  T(2.5,'55min @ 4:45–5:05/km',2,16,'4:45–5:05/km','WU 2.5km → 55min → CD 2km. Longest threshold session combined with 4×1600m Tue — hardest week of Phase 3.'),
  T(2.5,'55min @ 4:45–5:05/km',2,16,'4:45–5:05/km','WU 2.5km → 55min → CD 2km. Phase 3 peak tempo. Hold pace, focus on form in final 15min.'),
  null,
  T(2.5,'3×15min @ 4:20–4:40/km, 2min easy jog between',2,15.5,'4:20–4:40/km','WU 2.5km → 15min → 2min → 15min → 2min → 15min → CD 2km. Sub-threshold pace. 45 total minutes.'),
  T(2.5,'4×12min @ 4:20–4:40/km, 90s easy jog between',2,16,'4:20–4:40/km','WU 2.5km → 4×12min (90s jog) → CD 2km. 48 minutes of sub-threshold. Very demanding.'),
  T(2.5,'4×10min @ 4:00–4:20/km, 90s easy jog between',2,15,'4:00–4:20/km','WU 2.5km → 4×10min (90s jog) → CD 2km. First Thursday sessions at or near goal pace.'),
  null,
];

const P4_TUE=[
  I(2.5,'6×1000m @ 4:00/km, 90s easy jog between',1.5,11,'4:00/km','WU 2.5km → 6×1000m (90s jog) → CD 1.5km. If 4:00/km is unmanageable for 1km, extend Phase 3.'),
  I(2.5,'4×2000m @ 4:00/km, 2min easy jog between',1.5,13,'4:00/km','WU 2.5km → 4×2000m (2min jog) → CD 1.5km. Longest goal-pace reps so far.'),
  I(2.5,'3×3000m @ 4:00/km, 3min easy jog between',1.5,14,'4:00/km','WU 2.5km → 3×3000m (3min jog) → CD 1.5km. 3km per rep. By rep 3 the recovery will barely feel enough.'),
  I(2.5,'5×1000m @ 4:00/km, 90s easy jog between',1.5,10,'4:00/km','WU 2.5km → 5×1000m (90s jog) → CD 1.5km. Cutback week — fewer reps, same pace.'),
  I(2.5,'7×1000m @ 4:00/km, 90s easy jog between',1.5,12.5,'4:00/km','WU 2.5km → 7×1000m (90s jog) → CD 1.5km. More reps than week 37. 7km of goal-pace running.'),
  I(2.5,'5×2000m @ 4:00/km, 2min easy jog between',1.5,15,'4:00/km','WU 2.5km → 5×2000m (2min jog) → CD 1.5km. 10km of goal-pace running. Highest quality session of the plan.'),
  I(2.5,'4×2500m @ 4:00/km, 2min 30s easy jog between',1.5,15,'4:00/km','WU 2.5km → 4×2500m (2.5min jog) → CD 1.5km. Longest goal-pace reps. This is as hard as the training gets.'),
  I(2.5,'6×1000m @ 4:00/km, 90s easy jog between',1.5,11,'4:00/km','WU 2.5km → 6×1000m (90s jog) → CD 1.5km. Cutback week. Pace standard maintained.'),
  I(2.5,'5×1000m @ 4:00/km, 90s easy jog between',1.5,10,'4:00/km','WU 2.5km → 5×1000m (90s jog) → CD 1.5km. Taper — volume reduced but pace maintained.'),
  I(2,'4×800m @ 4:00/km, 2min easy jog between',1.5,8,'4:00/km','WU 2km → 4×800m (2min jog) → CD 1.5km. Final pre-race sharpener. Brief and sharp. Don\'t fatigue yourself.'),
  null,
];

const P4_THU=[
  T(2.5,'3×15min @ 4:20–4:40/km, 2min easy jog between',2,15.5,'4:20–4:40/km','WU 2.5km → 3×15min (2min jog) → CD 2km. Sub-threshold alongside goal-pace intervals Tue.'),
  T(2.5,'4×12min @ 4:20–4:40/km, 90s easy jog between',2,16,'4:20–4:40/km','WU 2.5km → 4×12min (90s jog) → CD 2km. 48 minutes of sub-threshold. Very hard by rep 4.'),
  T(2.5,'50min continuous @ 4:20–4:40/km',2,16,'4:20–4:40/km','WU 2.5km → 50min → CD 2km. Ease off pace rather than stopping if you fade after 35min.'),
  null,
  T(2.5,'3×15min @ 4:20–4:40/km, 2min easy jog between',2,15.5,'4:20–4:40/km','WU 2.5km → 3×15min (2min jog) → CD 2km. Should feel slightly more controlled than week 37.'),
  T(2.5,'4×12min @ 4:20–4:40/km, 90s easy jog between',2,16,'4:20–4:40/km','WU 2.5km → 4×12min (90s jog) → CD 2km. Alongside 5×2000m Tue — highest combined quality week.'),
  T(2.5,'55min continuous @ 4:20–4:40/km',2,17,'4:20–4:40/km','WU 2.5km → 55min → CD 2km. Longest sub-threshold session. Hardest week of Phase 4.'),
  null,
  T(2.5,'20min @ 4:00–4:10/km (taper sharpener)',2,9.5,'4:00–4:10/km','WU 2.5km → 20min at goal pace → CD 2km. Brief taper session. Do not extend it.'),
  R.easy(6,'6:00–6:30/km','Easy 4km + 4×20s strides. Stay loose. Race is 6 days away.'),
  R.rest('Full rest. Everything is already in the bank. Do not run.'),
];

// ── Build all 47 weeks ────────────────────────────────────────────────────────
function buildWeeks(){
  const weeks=[];

  // PHASE 1
  const ep1=w=>w<4?'6:30–7:30/km':'6:15–7:15/km';
  const p1Tu=[5,6,7,5,8,8,9,6];
  const p1ThEasy=[6,7,8,6,0,0,0,5];
  const p1Sat=[5,6,6,5,7,7,8,0];
  const p1Long=[10,12,13,10,14,15,16,0];
  const p1Wed=[0,0,5,0,5,5,5,5]; // 0 = rest
  const p1isCut=[0,0,0,1,0,0,0,0];
  const p1isRace=[0,0,0,0,0,0,0,1];
  const p1notes=[
    'First week back. All runs are easy — conversational throughout. Strength is bodyweight only. Focus on feeling the right muscles, not the weight.',
    'Small volume increase. Running stays easy. Start to feel the difference between glute med (clam) and glute max (bridge/RDL).',
    'Wednesday easy run added. Longest run so far. Strength continues BW — earn added load through technique quality first.',
    '<strong>Cutback week.</strong> Volume drops to ~65% of week 3. The body adapts during recovery. Do not compensate with extra effort.',
    'First quality session: 15min tempo Thursday. WU 2km → 15min tempo → CD 2km = ~6.5km total. That\'s the complete session.',
    'Tempo extends to 20min. WU 2km → 20min → CD 2km = ~7.5km total. Strength adds first 5kg DB to the RDL.',
    'Phase 1 peak. WU 2km → 25min → CD 2km = ~8.5km total. Strength adds first DB to SL deadlift.',
    '<strong>Race week.</strong> 5k or 10k tune-up Sunday. Run it honestly — this result calibrates Phase 2 paces. Strength cuts back.',
  ];
  for(let w=0;w<8;w++){
    const thuTempo=P1_THU[w];
    const thuRun=p1isRace[w]?R.easy(5,ep1(w),'Easy + 4×20s strides.'):
      thuTempo?thuTempo:R.easy(p1ThEasy[w],ep1(w));
    const wedRun=p1Wed[w]>0?R.easy(p1Wed[w],ep1(w)):R.rest('Rest or easy cross-train: swim, cycle, yoga.');
    const mode=p1isRace[w]?'race':p1isCut[w]?'cutback':'normal';
    const wn=w+1;
    weeks.push({phaseIdx:0,weekNum:wn,isCut:!!p1isCut[w],isRace:!!p1isRace[w],
      label:p1isRace[w]?`Wk${wn}★`:p1isCut[w]?`Wk${wn}↓`:`Wk${wn}`,
      note:p1notes[w],
      days:[
        {run:R.rest(),str:null},
        {run:R.easy(p1Tu[w],ep1(w)),str:p1StrA(w,mode)},
        {run:wedRun,str:null},
        {run:thuRun,str:null},
        {run:R.strOnly(),str:p1StrB(w,mode)},
        {run:p1Sat[w]>0?R.easy(p1Sat[w],ep1(w)):R.rest('Full rest before race.'),str:null},
        {run:p1isRace[w]?R.race('5k or 10k tune-up. Target: ~28–32min (5k) or ~57–62min (10k). Calibrates Phase 2 paces.',10):R.long(p1Long[w],ep1(w)),str:null},
      ]
    });
  }

  // PHASE 2
  const ep2=w=>w<4?'6:15–7:00/km':w<8?'6:00–6:45/km':'5:55–6:40/km';
  const lp2=w=>w<4?'6:20–7:05/km':w<8?'6:10–6:55/km':'6:00–6:45/km';
  const p2isCut=[0,0,0,1,0,0,0,1,0,0,0,0];
  const p2isRace=[0,0,0,0,0,0,0,0,0,0,0,1];
  const p2Tu=[10,10,10,8,11,11,12,8,12,12,12,8];
  const p2Wed=[7,7,8,0,8,8,8,0,8,8,8,6];
  const p2Sat=[8,9,9,7,10,10,10,8,11,11,11,0];
  const p2Long=[16,18,19,14,20,21,22,16,23,24,25,0];
  const p2notes=[
    'Phase 2 begins. Strength goes loaded for the first time. Running adds structured tempo Thursday. This is the template for the next 12 weeks.',
    'Tempo extends to 2×20min — 40 total minutes of threshold. Strength loads tick up. Keep easy runs truly easy.',
    'First 30min continuous tempo. Long run approaches 20km. Strength loads continue to build.',
    '<strong>Cutback week.</strong> Running drops to ~65%. Strength keeps same loads, one fewer set.',
    'Second block begins. 35min continuous tempo at slightly faster pace. Hip thrust now around 34kg.',
    '3×12min cruise intervals. Slightly easier feel than continuous tempo, same total quality volume.',
    '40min continuous tempo. Long run reaches 22km. Hip thrust now around 40kg.',
    '<strong>Cutback week.</strong> Running and strength both ease. Let the previous 3 weeks consolidate.',
    'Final Phase 2 block. 3×15min — 45 total minutes of threshold. Hardest tempo block yet.',
    '45min continuous tempo. Should feel similar difficulty to earlier sessions — fitness has grown.',
    '50min continuous tempo. Phase 2 peak. Long run reaches 25km. Hardest week of Phase 2.',
    '<strong>Race week.</strong> 10k tune-up Sunday. Target 52–55min. Strength cut back.',
  ];
  for(let w=0;w<12;w++){
    const thuQ=P2_THU[w];
    const thuRun=p2isRace[w]?R.easy(6,ep2(w),'Easy + 4×20s strides.'):thuQ||R.easy(7,ep2(w));
    const wedRun=p2Wed[w]>0?R.easy(p2Wed[w],ep2(w)):R.rest('Rest.');
    const satRun=p2isRace[w]?R.rest('Full rest.'):R.easy(p2Sat[w],ep2(w));
    const sunRun=p2isRace[w]?R.race('10k race. Target ~52–55min. Run it honestly.',10):R.long(p2Long[w],lp2(w));
    const mode=p2isRace[w]?'race':p2isCut[w]?'cutback':'normal';
    const wn=w+9;
    weeks.push({phaseIdx:1,weekNum:wn,isCut:!!p2isCut[w],isRace:!!p2isRace[w],
      label:p2isRace[w]?`Wk${wn}★`:p2isCut[w]?`Wk${wn}↓`:`Wk${wn}`,
      note:p2notes[w],
      days:[
        {run:R.rest(),str:null},
        {run:R.easy(p2Tu[w],ep2(w)),str:p2StrA(w,mode)},
        {run:wedRun,str:null},
        {run:thuRun,str:null},
        {run:R.strOnly(),str:p2StrB(w,mode)},
        {run:satRun,str:null},
        {run:sunRun,str:null},
      ]
    });
  }

  // PHASE 3
  const ep3=w=>w<8?'5:55–6:40/km':'5:45–6:30/km';
  const lp3=w=>w<8?'6:10–6:55/km':'6:00–6:45/km';
  const p3isCut=[0,0,0,1,0,0,0,1,0,0,0,0,0,0,0,1];
  const p3isRace=[0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,0];
  const p3Wed=[8,8,8,6,8,8,8,6,8,8,8,6,8,8,8,6];
  const p3Sat=[10,10,11,8,11,11,12,8,12,12,12,0,12,12,12,8];
  const p3Long=[22,23,24,16,24,25,25,16,25,25,25,0,24,25,25,16];
  const p3notes=[
    'Intervals introduced for the first time. Strength adds plyometrics (pogos, bounds). Two quality run sessions per week from now on.',
    'Interval reps get longer (1000m). Hold pace consistently across all reps.',
    '4×1200m — longest reps so far. Start each rep feeling ready to run the whole thing. Don\'t go out too hard.',
    '<strong>Cutback week.</strong> Intervals stay but volume and effort reduce. Strength dials back. Essential recovery after two hard weeks.',
    '3×2000m — step up in rep length. 10k effort for 2km per rep is a new challenge.',
    '6×1000m — high rep count at 10k effort. 6km of hard running total.',
    '5×1200m at 10k effort. Phase 3 mid-peak. Combined with 50min tempo Thu, one of the hardest weeks so far.',
    '<strong>Cutback week.</strong> Second mid-block recovery. Strength also eases. Genuinely recover.',
    '8×600m — short sharp reps to build top-end speed.',
    '2×(5×400m) — speed work. Building top-end speed that makes 10k pace feel more manageable.',
    'Phase 3 peak: 4×1600m + 55min tempo Thursday. Hardest training week of Phase 3.',
    '<strong>Race week.</strong> Target ~46–48min 10k. If you hit this, Phase 4 and sub-40 are within reach.',
    'Final Phase 3 block. Goal-pace exposure begins: 6×1000m at 4:00/km. Sub-threshold Thursday.',
    '4×2000m at goal pace + sub-threshold Thursday. Very demanding week.',
    'Progression run Tuesday + 4×10min at goal pace Thursday.',
    '<strong>Cutback week.</strong> End of Phase 3. Prepare for Phase 4.',
  ];
  for(let w=0;w<16;w++){
    const tueQ=p3isRace[w]?R.easy(8,ep3(w),'Easy before race weekend.'):P3_TUE[w];
    const thuQ=P3_THU[w];
    const thuRun=p3isRace[w]?R.easy(5,ep3(w),'Easy + 4×20s strides.'):
      p3isCut[w]?R.easy(8,ep3(w)):thuQ||R.easy(8,ep3(w));
    const satRun=p3isRace[w]?R.rest('Full rest.'):R.easy(p3Sat[w],ep3(w));
    const sunRun=p3isRace[w]?R.race('10k race. Target ~46–48min. Phase 3 benchmark.',10):R.long(p3Long[w],lp3(w));
    const mode=p3isRace[w]?'race':p3isCut[w]?'cutback':'normal';
    const wn=w+21;
    weeks.push({phaseIdx:2,weekNum:wn,isCut:!!p3isCut[w],isRace:!!p3isRace[w],
      label:p3isRace[w]?`Wk${wn}★`:p3isCut[w]?`Wk${wn}↓`:`Wk${wn}`,
      note:p3notes[w],
      days:[
        {run:R.rest(),str:null},
        {run:tueQ||R.easy(8,ep3(w)),str:p3StrA(w,mode)},
        {run:R.easy(p3Wed[w],ep3(w)),str:null},
        {run:thuRun,str:null},
        {run:R.strOnly(),str:p3StrB(w,mode)},
        {run:satRun,str:null},
        {run:sunRun,str:null},
      ]
    });
  }

  // PHASE 4
  const ep4='5:45–6:30/km',lp4='6:00–6:45/km';
  const p4isCut=[0,0,0,1,0,0,0,1,0,0,0];
  const p4isRace=[0,0,0,0,0,0,0,0,0,0,1];
  const p4isTaper=[0,0,0,0,0,0,0,0,1,1,0];
  const p4Long=[24,24,25,16,24,25,25,16,18,12,0];
  const p4Sat=[12,12,12,8,12,12,12,8,10,5,3];
  const p4Wed=[8,8,8,6,8,8,8,6,8,6,4];
  const p4notes=[
    'Phase 4 begins. Goal-pace intervals: 6×1000m at 4:00/km. Sub-threshold Thursday. If 4:00/km is unmanageable for 1km, extend Phase 3. Strength shifts to reactive.',
    '4×2000m at goal pace — reps get longer. The hardest combination of sessions in the plan begins.',
    '3×3000m at goal pace. Longest goal-pace reps. 50min sub-threshold Thursday.',
    '<strong>Cutback week.</strong> 5×1000m at goal pace. Strength keeps loads, fewer sets.',
    '7×1000m — more reps than week 37. Fitness building noticeably.',
    '5×2000m — 10km of goal-pace running. Alongside 4×12min sub-threshold Thu, the highest combined quality week of the plan.',
    '4×2500m — longest goal-pace session. 55min continuous sub-threshold Thursday.',
    '<strong>Cutback week.</strong> 6×1000m. Let the big block adaptations consolidate.',
    '<strong>Taper begins</strong> (2 weeks out). Volume drops ~30% but intensity maintained. Legs should feel unusually good by end of week.',
    'Final taper week. Very low volume. Keep sharpness. Sleep well, eat well, stay off your feet.',
    '🎯 <strong>Race week.</strong> Fitness is built. Trust it. Race plan: go out at 4:00/km. Not 3:55. Hit 20:00 at 5km. Finish strong.',
  ];
  for(let w=0;w<11;w++){
    const isTaper=!!p4isTaper[w];
    const mode=p4isRace[w]?'race':p4isTaper[w]?`taper${w-7}`:p4isCut[w]?'cutback':'normal';
    const tueQ=P4_TUE[w];
    const thuQ=P4_THU[w];
    const tueRun=p4isRace[w]?R.easy(5,'6:00–6:30/km','Easy + 4×20s strides.'):tueQ||R.easy(8,ep4);
    const thuRun=thuQ||(p4isCut[w]?R.easy(8,ep4):R.easy(8,ep4));
    const satRun=p4isRace[w]?R.easy(3,'6:00–6:30/km','Short shakeout + 2–3 light strides.'):R.easy(p4Sat[w],ep4);
    const sunRun=p4isRace[w]?R.race('🎯 Sub-40 10K. Start at 4:00/km. Hold 20:00 at 5km. Finish strong.',10):
      p4Long[w]>0?R.long(p4Long[w],lp4):R.rest('Rest. Race is tomorrow.');
    const friStr=p4isRace[w]?null:p4StrB(w,mode);
    const wn=w+37;
    let lbl=`Wk${wn}`;
    if(p4isRace[w]) lbl=`Wk${wn}🎯`;
    else if(isTaper) lbl=`Wk${wn}↓T`;
    else if(p4isCut[w]) lbl=`Wk${wn}↓`;
    weeks.push({phaseIdx:3,weekNum:wn,isCut:!!p4isCut[w]||isTaper,isRace:!!p4isRace[w],
      label:lbl,note:p4notes[w],
      days:[
        {run:R.rest(),str:null},
        {run:tueRun,str:p4StrA(w,mode)},
        {run:R.easy(p4Wed[w],ep4),str:null},
        {run:thuRun,str:null},
        {run:p4isRace[w]?R.rest('Full rest.'):R.strOnly(),str:friStr},
        {run:satRun,str:null},
        {run:sunRun,str:null},
      ]
    });
  }
  return weeks;
}

const ALL=buildWeeks();
let cPhase=0,cWeek=0;

function weekKm(w){
  return w.days.reduce((s,d)=>s+(d.run?d.run.km:0),0);
}

const BC={easy:'b-easy',long:'b-long',tempo:'b-tempo',intervals:'b-intervals',race:'b-race',rest:'b-rest','str-only':'b-strength'};
function phaseWeeks(p){return ALL.filter(w=>w.phaseIdx===p);}

function renderNav(){
  const pw=phaseWeeks(cPhase);
  document.getElementById('week-nav').innerHTML=pw.map((w,i)=>{
    let c='week-btn';
    if(w.isRace) c+=' wk-race';
    else if(w.isCut) c+=' wk-cut';
    if(i===cWeek) c+=' active';
    return `<button class="${c}" onclick="setWeek(${i})">${w.label}</button>`;
  }).join('');
}

function renderMileage(){
  const w=phaseWeeks(cPhase)[cWeek];
  if(!w) return;
  const total=weekKm(w);
  document.getElementById('mileage-total').textContent='~'+total+'km';
  const label=w.isRace?'Race week — volume reduced intentionally':
    w.isCut?'Cutback week — reduced volume is deliberate':
    'Total running this week (incl. WU/CD)';
  document.getElementById('mileage-desc').textContent=label;
}

function renderNote(){
  const w=phaseWeeks(cPhase)[cWeek];
  document.getElementById('week-note').innerHTML=w?w.note:'';
}

function renderGrid(){
  const w=phaseWeeks(cPhase)[cWeek];
  if(!w) return;
  document.getElementById('week-grid').innerHTML=w.days.map((d,i)=>{
    const {run,str}=d;
    let runHTML;
    if(!run||run.type==='str-only'){
      runHTML=`<div class="run-str-only"><span class="badge b-strength">Strength Only</span></div>`;
    } else if(run.type==='rest'){
      runHTML=`<div class="run-rest"><span class="badge b-rest">Rest</span>${run.note?`<div class="run-note" style="margin-top:4px">${run.note}</div>`:''}</div>`;
    } else {
      let wucdHTML='';
      if(run.wucd){
        const{wu,cd}=run.wucd;
        wucdHTML=`<div class="wucd"><span>${wu}km easy WU</span> → work → <span>${cd}km easy CD</span></div>`;
      }
      const noteText=run.workDesc||run.note||'';
      runHTML=`<div class="run-section">
        <span class="badge ${BC[run.type]||'b-rest'}">${run.label}</span>
        <div class="run-dist">${run.distance}</div>
        <div class="run-pace">${run.pace||''}</div>
        ${wucdHTML}
        ${noteText?`<div class="run-note">${noteText}</div>`:''}
      </div>`;
    }
    let strHTML='';
    if(str){
      strHTML=`<div class="str-section">
        <div class="str-head">💪 ${str.label}</div>
        ${str.exercises.map(e=>`<div class="ex">
          <div class="ex-top"><div class="ex-name">${e.name}</div><div class="ex-wt">${e.weight}</div></div>
          <div class="ex-sets">${e.sets}×${e.reps}</div>
          ${e.cue?`<div class="ex-cue">${e.cue}</div>`:''}
        </div>`).join('')}
      </div>`;
    }
    return `<div class="day-card"><div class="day-hdr">${DAYS[i]}</div>${runHTML}${strHTML}</div>`;
  }).join('');
}

function setPhase(p){
  cPhase=p;cWeek=0;
  document.querySelectorAll('.phase-btn').forEach((b,i)=>b.classList.toggle('active',i===p));
  renderNav();renderMileage();renderNote();renderGrid();
}
function setWeek(i){
  cWeek=i;
  document.querySelectorAll('.week-btn').forEach((b,j)=>b.classList.toggle('active',j===i));
  renderMileage();renderNote();renderGrid();
}
setPhase(0);
</script>
</body>
</html>
