<!doctype html>
<html lang="en-GB">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="color-scheme" content="light">
<title>Potentiometer → Voltage Divider | Interactive Demonstration</title>
<style>
:root{--bg:#f3f6fa;--paper:#fff;--ink:#172538;--muted:#52657a;--stroke:#dce5ee;--blue:#315fc3;--teal:#087f78;--orange:#b86e23;--softblue:#eaf1ff;--softteal:#e7f7f4;--shadow:0 12px 32px rgba(30,51,88,.07)}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.5 system-ui,-apple-system,"Segoe UI",Roboto,Arial,sans-serif}button,input,select{font:inherit}button:focus-visible,input:focus-visible,select:focus-visible,[role=slider]:focus-visible{outline:3px solid #79aaef;outline-offset:3px}
.shell{width:min(1100px,100%);margin:0 auto;padding:26px 24px 38px}
header{display:flex;gap:18px;align-items:start;justify-content:space-between;margin-bottom:20px}h1{margin:0;font-size:clamp(24px,3.2vw,34px);letter-spacing:-.045em;line-height:1.16;font-weight:770}header p{max-width:780px;color:var(--muted);margin:9px 0 0;font-size:15px}.eyebrow{font-size:11px;text-transform:uppercase;letter-spacing:.13em;color:var(--blue);font-weight:850;margin:0 0 8px} .tiny{font-size:12px;color:var(--muted)}
.config{background:var(--paper);border:1px solid var(--stroke);border-radius:16px;padding:20px 22px;margin-bottom:17px;box-shadow:var(--shadow);display:grid;grid-template-columns:1fr 1fr 1.2fr;gap:18px;align-items:start}
.control label{display:block;font-weight:720;font-size:13px;margin-bottom:7px}.inputgroup{display:flex;align-items:center;border:1px solid #bccddd;border-radius:10px;background:#fff;height:46px;overflow:hidden}.inputgroup:focus-within{outline:2px solid #a5bfef}.inputgroup input{width:100%;border:0;padding:10px 12px;min-width:0;outline:0;font-weight:700;font-variant-numeric:tabular-nums;color:var(--ink);background:transparent}.inputgroup span{padding:0 14px;background:#f3f6fa;border-left:1px solid var(--stroke);align-self:stretch;display:flex;align-items:center;color:var(--muted);font-size:13px;font-weight:700}
.segmented{display:flex;background:#eff3f8;padding:4px;border-radius:10px;height:46px;gap:3px}.segmented button{border:0;border-radius:8px;background:transparent;flex:1;cursor:pointer;color:#576c85;font-size:13px;font-weight:760}.segmented button[aria-pressed="true"]{background:var(--blue);color:#fff;box-shadow:0 2px 7px #254ca738}.segmented button:hover:not([aria-pressed=true]){background:#e0e8f4}
.compare{display:grid;grid-template-columns:1fr 1fr;gap:16px;align-items:stretch}.panel{border:1px solid var(--stroke);background:var(--paper);border-radius:17px;box-shadow:var(--shadow);padding:22px 23px 18px;min-width:0}.panel-header{display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap;margin-bottom:8px}.panel h2{margin:0;font-size:18px;line-height:1.28;letter-spacing:-.025em}.pill{font-size:11px;font-weight:750;color:var(--blue);background:var(--softblue);padding:5px 9px;border-radius:999px;white-space:nowrap}.pill.teal{background:var(--softteal);color:var(--teal)}
.dial-wrap{display:flex;justify-content:center;align-items:center;padding:4px 0 0;position:relative;min-height:283px}.dial-svg{width:min(310px,100%);max-height:287px;overflow:visible;touch-action:none;user-select:none}.dial-svg .clickable{cursor:grab;touch-action:none}.dial-svg.dragging .clickable{cursor:grabbing}.sliderrow{display:flex;align-items:center;gap:14px;margin:0 auto 10px;max-width:370px}.sliderrow input[type=range]{flex:1;accent-color:var(--teal);cursor:pointer;min-width:0}.position-chip{display:inline-flex;justify-content:center;min-width:78px;background:var(--softteal);color:#06665f;border-radius:8px;padding:5px 8px;font-variant-numeric:tabular-nums;font-weight:800}.sliderlabel{font-size:12px;color:var(--muted);text-align:center;margin-top:3px}.mini-values{display:flex;justify-content:center;gap:15px;margin:17px 0 0;padding-top:17px;border-top:1px solid var(--stroke)}.mini-values>div{min-width:0;flex:1;max-width:175px}.mini-values small{display:block;color:var(--muted);font-weight:650;font-size:12px}.mini-values b{display:block;font-size:18px;font-variant-numeric:tabular-nums;color:var(--ink)}
.circuit-wrap{display:flex;justify-content:center;align-items:center;height:302px;margin-top:3px}.circuit-svg{width:100%;height:100%;max-width:540px;overflow:visible}.resistance-values{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:6px}.value-box{border-radius:10px;padding:13px 15px;border:1px solid var(--stroke);background:#f8fafc}.value-box:first-child{border-color:#cbd9f7;background:#f2f6ff}.value-box:nth-child(2){border-color:#b6e3df;background:#effaf8}.value-box small{font-size:12px;display:block;color:var(--muted);font-weight:670}.value-box strong{font-size:23px;letter-spacing:-.03em;font-variant-numeric:tabular-nums;white-space:nowrap}.value-box:first-child strong{color:var(--blue)}.value-box:nth-child(2) strong{color:var(--teal)}
.results{margin-top:17px;background:#182c48;border:1px solid #182c48;border-radius:16px;box-shadow:var(--shadow);padding:20px 24px;color:#fff;display:grid;grid-template-columns:minmax(180px,1fr) minmax(230px,1.5fr) minmax(130px,1fr);align-items:center;gap:18px}.results .result-eyebrow{display:block;font-size:11px;letter-spacing:.11em;color:#b8cbea;text-transform:uppercase;font-weight:750}.results .big{font-size:clamp(30px,4.5vw,45px);font-weight:800;letter-spacing:-.05em;line-height:1.3;font-variant-numeric:tabular-nums;color:#86e0d5}.results .equation{font-size:15px;line-height:1.8;color:#e1ebfb;font-variant-numeric:tabular-nums}.results .equation strong{font-weight:800;color:#fff}.results .secondary{font-size:13px;color:#b7c7db}.results .secondary strong{display:block;font-size:18px;color:#fff;font-variant-numeric:tabular-nums}
.foot{padding:18px 3px 0;color:var(--muted);font-size:13px;line-height:1.58}.foot p{margin:0 0 6px}.foot strong{color:var(--ink)}
@media(max-width:800px){.shell{padding:16px 12px 27px}.config{grid-template-columns:1fr 1fr;gap:14px;padding:16px}.config .control:last-child{grid-column:1/-1}.compare{grid-template-columns:1fr}.panel{padding:17px}.circuit-wrap{height:300px}.results{grid-template-columns:1fr 1fr}.results>div:last-child{grid-column:1/-1;display:flex;align-items:center;gap:20px}.results .secondary strong{display:inline-block;margin-right:10px}}@media(max-width:450px){.shell{padding:13px 9px 26px}.config{gap:12px;padding:14px}.results{grid-template-columns:1fr;gap:8px;padding:18px}.results>div:last-child{grid-column:auto}.panel h2{font-size:16px}.resistance-values{gap:8px}.value-box{padding:10px}.value-box strong{font-size:19px}.circuit-wrap{height:260px}}@media(prefers-reduced-motion:reduce){*{scroll-behavior:auto!important;transition:none!important}}
</style>
</head>
<body>
<main class="shell">
<header>
  <div><div class="eyebrow">Interactive electronics demonstration</div><h1>Inside a potentiometer</h1><p>Turn the wiper to see how one potentiometer behaves like two resistors in series—and how their changing ratio determines the output voltage.</p></div>
</header>
<section class="config" aria-label="Circuit settings">
 <div class="control"><label for="vin">Supply voltage</label><div class="inputgroup"><input id="vin" type="number" min="0" max="48" step="0.1" value="9" aria-describedby="rangeVin"><span>V</span></div><span class="tiny" id="rangeVin">0–48 V DC</span></div>
 <div class="control"><label for="resistance">Potentiometer resistance</label><div class="inputgroup"><input id="resistance" type="number" min="0.1" max="1000" step="0.1" value="10" aria-describedby="rangeResistance"><span>kΩ</span></div><span class="tiny" id="rangeResistance">0.1–1000 kΩ</span></div>
 <div class="control"><label>Potentiometer taper</label><div class="segmented" role="group" aria-label="Select potentiometer taper"><button id="linear" type="button" aria-pressed="true">Linear</button><button id="log" type="button" aria-pressed="false">Log (audio)</button></div><span class="tiny" id="taper-explanation">Equal rotation gives equal changes in resistance.</span></div>
</section>
<div class="compare">
 <section class="panel" aria-label="Rotary potentiometer">
   <div class="panel-header"><h2>1. Rotate the wiper</h2><span class="pill">Physical control</span></div>
   <div class="dial-wrap">
    <svg class="dial-svg" id="dial" viewBox="0 0 320 300" xmlns="http://www.w3.org/2000/svg" role="slider" tabindex="0" aria-label="Potentiometer wiper position" aria-valuemin="0" aria-valuemax="100" aria-valuenow="50" aria-valuetext="50 per cent clockwise from minimum" aria-orientation="horizontal">
     <defs><radialGradient id="knobFill" cx="34%" cy="25%"><stop offset="0" stop-color="#ffffff"/><stop offset=".77" stop-color="#f1f5fb"/><stop offset="1" stop-color="#ccd9e8"/></radialGradient><filter id="knobShadow" x="-40%" y="-40%" width="180%" height="180%"><feDropShadow dx="0" dy="5" stdDeviation="7" flood-color="#233c61" flood-opacity=".19"/></filter></defs>
     <path id="dialTrack" fill="none" stroke="#e1e8f0" stroke-width="15" stroke-linecap="round"/><path id="dialProgress" fill="none" stroke="#087f78" stroke-width="15" stroke-linecap="round"/>
     <g id="ticks" stroke="#91a4bb" stroke-width="2"></g>
     <g class="clickable" id="dialHandle"><circle cx="160" cy="148" r="91" fill="url(#knobFill)" filter="url(#knobShadow)" stroke="#a9bdcf" stroke-width="1.5"/><circle cx="160" cy="148" r="72" fill="none" stroke="#d5e0ec" stroke-width="2"/><g id="pointer"><line x1="160" y1="148" x2="160" y2="83" stroke="#087f78" stroke-width="8" stroke-linecap="round"/><circle cx="160" cy="148" r="9" fill="#1e5368"/></g></g>
     <circle class="clickable" cx="160" cy="148" r="122" fill="transparent" stroke="transparent" stroke-width="1" pointer-events="all"/>
     <text x="40" y="275" text-anchor="middle" font-size="14" fill="#52657a" font-weight="750">0%</text><text x="280" y="275" text-anchor="middle" font-size="14" fill="#52657a" font-weight="750">100%</text>
    </svg>
   </div>
   <div class="sliderrow"><label for="position" class="tiny" style="white-space:nowrap;font-weight:720">Wiper</label><input id="position" type="range" min="0" max="100" value="50" step="0.1" aria-label="Wiper rotation percentage"><output id="positionDisplay" class="position-chip" for="position">50.0%</output></div>
   <div class="sliderlabel">Drag the knob, move the slider, or use ← / → on the focused knob.</div>
   <div class="mini-values"><div><small>Track resistance</small><b id="potTotal">10.00 kΩ</b></div><div><small>Wiper voltage</small><b id="potOutput">4.50 V</b></div></div>
 </section>
 <section class="panel" aria-label="Equivalent two-resistor voltage divider">
   <div class="panel-header"><h2>2. Equivalent voltage divider</h2><span class="pill teal">Electrical model</span></div>
   <div class="circuit-wrap">
   <svg class="circuit-svg" viewBox="0 0 520 345" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="circuitTitle circuitDesc">
     <title id="circuitTitle">Equivalent two-resistor circuit</title><desc id="circuitDesc">A DC supply connects a resistor R1 in series with a resistor R2 between positive supply and ground. Output is measured at the centre junction relative to ground. Values update with the wiper.</desc>
     <g stroke="#50627a" fill="none" stroke-width="3" stroke-linecap="round" stroke-linejoin="round">
       <path d="M100 52 H315 V93"/><path d="M315 147 V186"/><path d="M315 186 V221"/><path d="M315 275 V304 H100"/>
       <path d="M315 186 H451" stroke="#087f78" stroke-width="3.8"/>
       <path d="M100 52 V132"/><path d="M100 218 V304"/>
       <circle cx="100" cy="175" r="43" fill="#fff" stroke="#50627a"/><path d="M78 159 H96 M87 150 V168 M82 189 H93" stroke-width="2.8"/>
       <path d="M315 304 V316 M300 316 H330 M306 323 H324 M312 330 H318" stroke-width="2.7"/>
     </g>
     <rect x="289" y="93" width="52" height="54" rx="4" fill="#e8efff" stroke="#315fc3" stroke-width="2.6"/>
     <rect x="289" y="221" width="52" height="54" rx="4" fill="#e7f7f4" stroke="#087f78" stroke-width="2.6"/>
     <circle cx="315" cy="186" r="6" fill="#087f78"/><circle cx="451" cy="186" r="5" fill="#087f78"/>
     <text x="100" y="34" text-anchor="middle" font-size="16" font-weight="750" fill="#315fc3" id="topSupply">+9.00 V</text>
     <text x="61" y="180" text-anchor="end" font-size="13" font-weight="700" fill="#52657a">V<tspan baseline-shift="sub" font-size="10">in</tspan></text>
     <text x="366" y="116" font-size="15" font-weight="750" fill="#315fc3">R₁</text>
     <text x="366" y="245" font-size="15" font-weight="750" fill="#087f78">R₂</text>
     <rect x="370" y="156" width="135" height="52" rx="10" fill="#e7f7f4" stroke="#b1ded7"/>
     <text x="438" y="170" text-anchor="middle" font-size="11" font-weight="760" fill="#087f78">V<tspan baseline-shift="sub" font-size="9">out</tspan></text>
     <text id="diagramVout" x="438" y="194" text-anchor="middle" font-size="17" font-weight="800" fill="#075b56">4.50 V</text>
     <text x="355" y="333" font-size="13" fill="#52657a" font-weight="650">0 V (GND)</text>
   </svg>
   </div>
   <div class="resistance-values"><div class="value-box"><small>R₁ · wiper to +V</small><strong id="rTop">5.00 kΩ</strong></div><div class="value-box"><small>R₂ · wiper to GND</small><strong id="rBottom">5.00 kΩ</strong></div></div>
 </section>
</div>
<section class="results" aria-label="Live calculations">
  <div><span class="result-eyebrow">Output voltage</span><div class="big" id="bigVout" aria-live="off">4.50 V</div></div>
  <div><span class="result-eyebrow">Voltage-divider equation</span><div class="equation">V<sub>out</sub> = V<sub>in</sub> × R₂ / (R₁ + R₂)<br><strong id="workedEquation">9.00 × 5.00 / (5.00 + 5.00) = 4.50 V</strong></div></div>
  <div><span class="result-eyebrow">Supply current</span><div class="secondary"><strong id="current">0.900 mA</strong>V<sub>in</sub> / R<sub>total</sub></div></div>
</section>
<div class="foot"><p><strong>Notice:</strong> R₁ + R₂ always equals the potentiometer’s rated resistance. With no load connected to the wiper, changing the knob changes the voltage ratio—not the total resistance or supply current.</p><p id="modelnote"><strong>Model:</strong> Ideal potentiometer with a DC supply and an unloaded wiper (no contact resistance). Log taper uses an illustrative audio-taper curve with approximately 10% of the resistance below the wiper at 50% rotation; real components vary by manufacturer and orientation.</p></div>
</main>
<script>
(()=>{'use strict';
const E=id=>document.getElementById(id);
const s={vin:9,total:10,taper:'linear',position:50};
const cx=160,cy=148,r=120,start=135,end=405;
const deg2rad=d=>d*Math.PI/180;
function point(deg,radius){const a=deg2rad(deg);return {x:cx+Math.cos(a)*radius,y:cy+Math.sin(a)*radius};}
function arc(a,b,radius){const p1=point(a,radius),p2=point(b,radius);return `M ${p1.x.toFixed(3)} ${p1.y.toFixed(3)} A ${radius} ${radius} 0 ${b-a>180?1:0} 1 ${p2.x.toFixed(3)} ${p2.y.toFixed(3)}`;}
function fmt(n,d=2){const value=Math.abs(n)<1e-10?0:n;return value.toFixed(d);}
function fPos(x){return s.taper==='linear'?x:(Math.pow(81,x)-1)/80;}
function sync(){
 const x=s.position/100, f=fPos(x),rBottom=s.total*f,rTop=s.total-rBottom,vout=s.vin*f,current=s.vin/s.total;
 E('position').value=String(s.position);
 E('positionDisplay').textContent=fmt(s.position,1)+'%';
 E('dial').setAttribute('aria-valuenow',fmt(s.position,1));
 E('dial').setAttribute('aria-valuetext',fmt(s.position,1)+' per cent of clockwise travel');
 E('dialProgress').setAttribute('d',s.position>0?arc(start,start+(end-start)*x,r):'');
 E('pointer').setAttribute('transform',`rotate(${start+(end-start)*x+90} ${cx} ${cy})`);
 E('potTotal').textContent=fmt(s.total)+' kΩ';
 E('potOutput').textContent=fmt(vout)+' V';
 E('rTop').textContent=fmt(rTop)+' kΩ'; E('rBottom').textContent=fmt(rBottom)+' kΩ';
 E('topSupply').textContent='+'+fmt(s.vin)+' V';
 E('diagramVout').textContent=fmt(vout)+' V';
 E('bigVout').textContent=fmt(vout)+' V';
 E('workedEquation').textContent=`${fmt(s.vin)} × ${fmt(rBottom)} / (${fmt(rTop)} + ${fmt(rBottom)}) = ${fmt(vout)} V`;
 E('current').textContent=fmt(current,3)+' mA';
 E('taper-explanation').textContent=s.taper==='linear'?'Equal rotation gives equal changes in resistance.':'Idealised audio taper: 50% rotation gives 10% of Vᵢₙ (unloaded).';
 E('linear').setAttribute('aria-pressed',String(s.taper==='linear'));
 E('log').setAttribute('aria-pressed',String(s.taper==='log'));
}
E('dialTrack').setAttribute('d',arc(start,end,r));
for(let i=0;i<=10;i++){
 const a=start+(end-start)*i/10,p1=point(a,133),p2=point(a,i%5===0?148:140);
 const line=document.createElementNS('http://www.w3.org/2000/svg','line');
 for(const [key,val] of Object.entries({x1:p1.x,y1:p1.y,x2:p2.x,y2:p2.y}))line.setAttribute(key,String(val));
 E('ticks').appendChild(line);
}
function setPosition(v){s.position=Math.max(0,Math.min(100,Math.round(v*10)/10));sync();}
E('position').addEventListener('input',e=>setPosition(Number(e.target.value)));
E('linear').addEventListener('click',()=>{s.taper='linear';sync();});
E('log').addEventListener('click',()=>{s.taper='log';sync();});
function bindInput(id,key,min,max){
 const el=E(id);
 function update(){const v=Number(el.value);if(el.value.trim()!=='' && Number.isFinite(v)&&v>=min&&v<=max){s[key]=v;el.setCustomValidity('');sync();}else{el.setCustomValidity(`Enter a value between ${min} and ${max}.`);}}
 el.addEventListener('input',update);
 el.addEventListener('blur',()=>{if(!el.checkValidity()){el.value=String(s[key]);el.setCustomValidity('');}sync();});
}
bindInput('vin','vin',0,48);bindInput('resistance','total',.1,1000);
let dragging=false;
function pointerPosition(event){
 const svg=E('dial'),rect=svg.getBoundingClientRect(), px=(event.clientX-rect.left)*320/rect.width,py=(event.clientY-rect.top)*300/rect.height;
 let a=(Math.atan2(py-cy,px-cx)*180/Math.PI+360)%360;
 if(a<start)a+=360;
 a=Math.max(start,Math.min(end,a));setPosition((a-start)/(end-start)*100);
}
const svg=E('dial');
svg.addEventListener('pointerdown',event=>{if(event.button!==0)return;dragging=true;svg.classList.add('dragging');svg.setPointerCapture(event.pointerId);pointerPosition(event);event.preventDefault();});
svg.addEventListener('pointermove',event=>{if(dragging)pointerPosition(event);});
function stopDrag(){dragging=false;svg.classList.remove('dragging');}
svg.addEventListener('pointerup',stopDrag);svg.addEventListener('pointercancel',stopDrag);svg.addEventListener('lostpointercapture',stopDrag);
svg.addEventListener('keydown',e=>{const values={ArrowRight:1,ArrowUp:1,ArrowLeft:-1,ArrowDown:-1,PageUp:10,PageDown:-10};if(Object.prototype.hasOwnProperty.call(values,e.key)){e.preventDefault();setPosition(s.position+values[e.key]);}if(e.key==='Home'){e.preventDefault();setPosition(0);}if(e.key==='End'){e.preventDefault();setPosition(100);}});
sync();
})();
</script>
</body>
</html>
