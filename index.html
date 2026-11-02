<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>كتاب الفيزياء 3D — البندول البسيط</title>
<style>
  :root{
    --bg:#0b1020; --panel:rgba(16,22,40,.86); --line:rgba(120,160,255,.25);
    --txt:#e8eefc; --muted:#9fb0d0; --accent:#5ee0c0; --accent2:#7aa2ff;
  }
  *{box-sizing:border-box}
  html,body{margin:0;height:100%;overflow:hidden;background:var(--bg);color:var(--txt);
    font-family:"Segoe UI",Tahoma,"Noto Kufi Arabic",system-ui,sans-serif;}
  canvas{display:block}

  #ui{
    position:fixed;top:14px;right:14px;width:302px;max-height:calc(100% - 28px);
    overflow-y:auto;background:var(--panel);border:1px solid var(--line);
    border-radius:16px;padding:14px 16px;backdrop-filter:blur(10px);
    box-shadow:0 10px 40px rgba(0,0,0,.5);font-size:13px;z-index:10;
  }
  #ui::-webkit-scrollbar{width:6px}
  #ui::-webkit-scrollbar-thumb{background:rgba(122,162,255,.3);border-radius:6px}

  #ui h1{font-size:15px;margin:0 0 4px;letter-spacing:.2px}
  #ui .sub{margin:0 0 12px;color:var(--muted);font-size:11.5px;line-height:1.5}

  .row{display:flex;justify-content:space-between;align-items:baseline;
    margin:10px 0 4px;font-size:12px;color:var(--muted)}
  .row span:last-child{color:var(--accent);font-variant-numeric:tabular-nums;font-weight:600}

  input[type=range]{width:100%;-webkit-appearance:none;appearance:none;height:4px;
    border-radius:4px;background:linear-gradient(90deg,#3b4a7a,#2a3358);
    outline:none;margin:0 0 4px;cursor:pointer}
  input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;width:15px;height:15px;
    border-radius:50%;background:var(--accent);border:2px solid #0b1020;
    box-shadow:0 0 10px rgba(94,224,192,.6)}
  input[type=range]::-moz-range-thumb{width:15px;height:15px;border-radius:50%;
    background:var(--accent);border:2px solid #0b1020;box-shadow:0 0 10px rgba(94,224,192,.6)}

  .chips{display:flex;gap:6px;margin:2px 0 4px}
  .chips button{flex:1;padding:5px 0;font-size:11px;border-radius:8px;
    border:1px solid var(--line);background:rgba(122,162,255,.08);color:var(--txt);
    cursor:pointer;font-family:inherit;transition:.15s}
  .chips button:hover{background:rgba(122,162,255,.22)}

  .btns{display:flex;gap:8px;margin:14px 0 12px}
  .btns button{flex:1;padding:9px 0;border-radius:10px;border:1px solid transparent;
    font-family:inherit;font-size:12.5px;font-weight:700;cursor:pointer;
    background:linear-gradient(180deg,#5ee0c0,#2fb99c);color:#06231d;transition:.15s}
  .btns button:hover{filter:brightness(1.08)}
  #resetBtn{background:rgba(122,162,255,.12);color:var(--txt);border-color:var(--line)}

  .stats{display:grid;gap:6px;margin-bottom:12px;font-size:12px}
  .stats div{display:flex;justify-content:space-between;align-items:center;
    background:rgba(255,255,255,.035);padding:6px 10px;border-radius:8px}
  .stats b{color:var(--accent2);font-variant-numeric:tabular-nums}

  .bars{display:grid;gap:7px;margin-bottom:12px}
  .bar{display:grid;grid-template-columns:56px 1fr;align-items:center;
    gap:8px;font-size:11px;color:var(--muted)}
  .track{height:8px;border-radius:8px;background:rgba(255,255,255,.07);overflow:hidden}
  .track i{display:block;height:100%;width:0%;border-radius:8px;transition:width .08s linear}
  #keBar{background:linear-gradient(90deg,#5ee0c0,#2fb99c)}
  #peBar{background:linear-gradient(90deg,#7aa2ff,#4b6fd6)}
  #totBar{background:linear-gradient(90deg,#ffd36e,#e2a53a)}

  .note{font-size:10.5px;color:var(--muted);line-height:1.7;margin:0;
    border-top:1px solid rgba(255,255,255,.07);padding-top:10px}

  @media (max-width:560px){
    #ui{width:auto;right:10px;left:10px;top:auto;bottom:10px;max-height:50vh}
  }
</style>
</head>
<body>

<div id="ui">
  <h1>📘 كتاب الفيزياء 3D</h1>
  <p class="sub">تجربة البندول البسيط — اسحب المشهد للتدوير، والعجلة للتقريب</p>

  <div class="row"><label>الطول L</label><span id="lVal">0.80 m</span></div>
  <input id="L" type="range" min="0.30" max="1.00" step="0.01" value="0.80">

  <div class="row"><label>الجاذبية g</label><span id="gVal">9.81 m/s²</span></div>
  <input id="g" type="range" min="1.60" max="24.80" step="0.01" value="9.81">
  <div class="chips">
    <button data-g="1.62">القمر</button>
    <button data-g="9.81">الأرض</button>
    <button data-g="24.79">المشتري</button>
  </div>

  <div class="row"><label>زاوية البداية θ₀</label><span id="aVal">35°</span></div>
  <input id="a0" type="range" min="5" max="80" step="1" value="35">

  <div class="row"><label>التخميد</label><span id="dVal">0.00</span></div>
  <input id="damp" type="range" min="0" max="0.40" step="0.01" value="0">

  <div class="btns">
    <button id="playBtn">إيقاف مؤقت</button>
    <button id="resetBtn">إعادة</button>
  </div>

  <div class="stats">
    <div><span>الدوري النظري T</span><b id="tTheo">—</b></div>
    <div><span>الدوري المقاس</span><b id="tMeas">—</b></div>
    <div><span>السرعة الزاوية ω</span><b id="omega">—</b></div>
  </div>

  <div class="bars">
    <div class="bar"><span>حركية</span><div class="track"><i id="keBar"></i></div></div>
    <div class="bar"><span>كامنة</span><div class="track"><i id="peBar"></i></div></div>
    <div class="bar"><span>كلية</span><div class="track"><i id="totBar"></i></div></div>
  </div>

  <p class="note">
    لاحظ: الزمن الدوري لا يعتمد على الكتلة. وللزوايا الصغيرة T = 2π√(L/g).
    كبّر الزاوية إلى 80° وشوف الفرق بين النظري والمقاس — هذا تأثير السعة الكبيرة.
  </p>
</div>

<script type="importmap">
{
  "imports": {
    "three": "https://unpkg.com/three@0.160.0/build/three.module.js",
    "three/addons/": "https://unpkg.com/three@0.160.0/examples/jsm/"
  }
}
</script>

<script type="module">
import * as THREE from 'three';
import { OrbitControls } from 'three/addons/controls/OrbitControls.js';

/* ================= إعداد المشهد ================= */
const scene = new THREE.Scene();
scene.background = new THREE.Color(0x0b1020);
scene.fog = new THREE.Fog(0x0b1020, 9, 20);

const camera = new THREE.PerspectiveCamera(45, innerWidth / innerHeight, 0.1, 100);
camera.position.set(2.8, 2.3, 4.3);

const renderer = new THREE.WebGLRenderer({ antialias: true });
renderer.setPixelRatio(Math.min(devicePixelRatio, 2));
renderer.setSize(innerWidth, innerHeight);
renderer.shadowMap.enabled = true;
renderer.shadowMap.type = THREE.PCFSoftShadowMap;
renderer.toneMapping = THREE.ACESFilmicToneMapping;
renderer.toneMappingExposure = 1.05;
document.body.appendChild(renderer.domElement);

/* ================= الإضاءة ================= */
scene.add(new THREE.HemisphereLight(0x9db8ff, 0x141a30, 1.15));

const key = new THREE.DirectionalLight(0xffffff, 2.4);
key.position.set(3.5, 6, 4);
key.castShadow = true;
key.shadow.mapSize.set(1024, 1024);
key.shadow.camera.near = 1;
key.shadow.camera.far = 22;
key.shadow.camera.left = -6;
key.shadow.camera.right = 6;
key.shadow.camera.top = 6;
key.shadow.camera.bottom = -6;
key.shadow.bias = -0.0006;
scene.add(key);

const rim = new THREE.DirectionalLight(0x7aa2ff, 1.4);
rim.position.set(-4, 2.5, -3.5);
scene.add(rim);

/* ================= الأرضية ================= */
const floor = new THREE.Mesh(
  new THREE.CircleGeometry(14, 64),
  new THREE.MeshStandardMaterial({ color: 0x0e1530, roughness: 1, metalness: 0 })
);
floor.rotation.x = -Math.PI / 2;
floor.position.y = -0.22;
floor.receiveShadow = true;
scene.add(floor);

/* ================= الكتاب ================= */
const book = new THREE.Group();
scene.add(book);

const PW = 1.7, PD = 2.3, PT = 0.06;

const pageMat  = new THREE.MeshStandardMaterial({ color: 0xf3f0e6, roughness: 0.92, metalness: 0.0 });
const coverMat = new THREE.MeshStandardMaterial({ color: 0x2a3a6b, roughness: 0.55, metalness: 0.15 });
const spineMat = new THREE.MeshStandardMaterial({ color: 0x1d2a52, roughness: 0.7,  metalness: 0.1  });

// الصفحة اليمنى (صفحة التجربة)
const rightPage = new THREE.Mesh(new THREE.BoxGeometry(PW, PT, PD), pageMat);
rightPage.position.set(PW / 2, 0, 0);
rightPage.receiveShadow = true;
book.add(rightPage);

// الصفحة اليسرى
const leftPage = new THREE.Mesh(new THREE.BoxGeometry(PW, PT, PD), pageMat);
leftPage.position.set(-PW / 2, 0, 0);
leftPage.receiveShadow = true;
book.add(leftPage);

// الأغلفة
const coverGeo = new THREE.BoxGeometry(PW + 0.14, 0.08, PD + 0.14);
const coverR = new THREE.Mesh(coverGeo, coverMat);
coverR.position.set(PW / 2, -0.07, 0);
coverR.receiveShadow = true;
book.add(coverR);

const coverL = new THREE.Mesh(coverGeo, coverMat);
coverL.position.set(-PW / 2, -0.07, 0);
coverL.receiveShadow = true;
book.add(coverL);

// الكعب
const spine = new THREE.Mesh(new THREE.BoxGeometry(0.13, 0.21, PD + 0.14), spineMat);
spine.position.set(0, -0.105, 0);
spine.castShadow = true;
book.add(spine);

/* ================= البندول ================= */
const PIVOT = new THREE.Vector3(0.88, 1.22, 0);

const pend = new THREE.Group();
pend.position.copy(PIVOT);
book.add(pend);

// المحور
const pivotMesh = new THREE.Mesh(
  new THREE.SphereGeometry(0.05, 18, 14),
  new THREE.MeshStandardMaterial({ color: 0xcfe0ff, roughness: 0.25, metalness: 0.7 })
);
pivotMesh.castShadow = true;
pend.add(pivotMesh);

// القضيب: أسطوانة طولها 1 ممتدة من 0 إلى -1 ثم نُحجّمها بـ L
const rodGeo = new THREE.CylinderGeometry(0.013, 0.013, 1, 10);
rodGeo.translate(0, -0.5, 0);
const rod = new THREE.Mesh(
  rodGeo,
  new THREE.MeshStandardMaterial({ color: 0x8fa8d8, roughness: 0.35, metalness: 0.6 })
);
rod.castShadow = true;
pend.add(rod);

// الكرة
const bob = new THREE.Mesh(
  new THREE.SphereGeometry(0.125, 28, 20),
  new THREE.MeshStandardMaterial({
    color: 0x5ee0c0, emissive: 0x0e6b58, emissiveIntensity: 0.7,
    roughness: 0.22, metalness: 0.35
  })
);
bob.castShadow = true;
pend.add(bob);

// قوس مسار الحركة (نصف قطر 1 ثم نُحجّمه بـ L)
const arcMat = new THREE.LineBasicMaterial({ color: 0x7aa2ff, transparent: true, opacity: 0.38 });
const arcPts = [];
const ARC_MAX = 1.45; // ≈ 83°
const N = 72;
for (let i = 0; i <= N; i++) {
  const a = -ARC_MAX + (2 * ARC_MAX) * i / N;
  arcPts.push(new THREE.Vector3(Math.sin(a), -Math.cos(a), 0));
}
const arc = new THREE.Line(new THREE.BufferGeometry().setFromPoints(arcPts), arcMat);
pend.add(arc);

/* ================= الكاميرا والتحكم ================= */
const controls = new OrbitControls(camera, renderer.domElement);
controls.target.set(0.5, 0.62, 0);
controls.enableDamping = true;
controls.dampingFactor = 0.08;
controls.minDistance = 2.2;
controls.maxDistance = 9;
controls.minPolarAngle = 0.12;
controls.maxPolarAngle = Math.PI * 0.52;
controls.update();

/* ================= الحالة والفيزياء ================= */
const state = {
  L: 0.80,
  g: 9.81,
  a0: 35 * Math.PI / 180,
  damp: 0.0,
  theta: 0,
  omega: 0,
  t: 0,
  running: true,
  period: null,
  lastCross: null,
  E0: 1
};

let prevTheta = 0;
let acc = 0;
const DT = 1 / 240;

function reset() {
  state.theta = state.a0;
  state.omega = 0;
  state.t = 0;
  state.period = null;
  state.lastCross = null;
  state.E0 = Math.max(1e-6, state.g * state.L * (1 - Math.cos(state.a0)));
  prevTheta = state.theta;
  acc = 0;
  updateVisual();
  updateReadout();
}

function physics(dt) {
  acc += dt;
  let guard = 0;
  while (acc >= DT && guard++ < 800) {
    acc -= DT;

    // θ'' = -(g/L) sinθ - c·θ'   (أويلر شبه الضمني = مستقر)
    const alpha = -(state.g / state.L) * Math.sin(state.theta) - state.damp * state.omega;
    state.omega += alpha * DT;
    state.theta += state.omega * DT;
    state.t += DT;

    // قياس الزمن الدوري عبر عبور الصفر في الاتجاه الموجب
    if (prevTheta < 0 && state.theta >= 0) {
      if (state.lastCross !== null) state.period = state.t - state.lastCross;
      state.lastCross = state.t;
    }
    prevTheta = state.theta;
  }
}

function updateVisual() {
  rod.scale.y = state.L;
  rod.rotation.z = state.theta;

  bob.position.set(
    Math.sin(state.theta) * state.L,
    -Math.cos(state.theta) * state.L,
    0
  );

  arc.scale.set(state.L, state.L, 1);
}

/* ================= واجهة المستخدم ================= */
const $ = id => document.getElementById(id);

function updateReadout() {
  const T = 2 * Math.PI * Math.sqrt(state.L / state.g);
  $('tTheo').textContent = T.toFixed(2) + ' ث';
  $('tMeas').textContent = state.period ? state.period.toFixed(2) + ' ث' : '—';
  $('omega').textContent = state.omega.toFixed(2) + ' rad/s';

  const v = state.L * state.omega;
  const ke = 0.5 * v * v;
  const pe = state.g * state.L * (1 - Math.cos(state.theta));
  const tot = ke + pe;
  const E0 = state.E0;

  $('keBar').style.width  = Math.min(100, ke  / E0 * 100) + '%';
  $('peBar').style.width  = Math.min(100, pe  / E0 * 100) + '%';
  $('totBar').style.width = Math.min(100, tot / E0 * 100) + '%';
}

$('L').addEventListener('input', e => {
  state.L = +e.target.value;
  $('lVal').textContent = state.L.toFixed(2) + ' m';
  reset();
});

$('g').addEventListener('input', e => {
  state.g = +e.target.value;
  $('gVal').textContent = state.g.toFixed(2) + ' m/s²';
});

document.querySelectorAll('.chips button').forEach(b => {
  b.addEventListener('click', () => {
    $('g').value = b.dataset.g;
    $('g').dispatchEvent(new Event('input'));
  });
});

$('a0').addEventListener('input', e => {
  state.a0 = (+e.target.value) * Math.PI / 180;
  $('aVal').textContent = e.target.value + '°';
  reset();
});

$('damp').addEventListener('input', e => {
  state.damp = +e.target.value;
  $('dVal').textContent = state.damp.toFixed(2);
});

$('playBtn').addEventListener('click', () => {
  state.running = !state.running;
  $('playBtn').textContent = state.running ? 'إيقاف مؤقت' : 'تشغيل';
});

$('resetBtn').addEventListener('click', reset);

/* ================= الحلقة الرئيسية ================= */
const clock = new THREE.Clock();
let uiAcc = 0;

function animate() {
  requestAnimationFrame(animate);

  const dt = Math.min(clock.getDelta(), 0.05);

  if (state.running) physics(dt);
  updateVisual();
  controls.update();
  renderer.render(scene, camera);

  uiAcc += dt;
  if (uiAcc > 0.1) { uiAcc = 0; updateReadout(); }
}

addEventListener('resize', () => {
  camera.aspect = innerWidth / innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(innerWidth, innerHeight);
});

reset();
animate();
</script>
</body>
</html>
