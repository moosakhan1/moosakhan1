Below are all files you need. Create them in your `moosakhan1/moosakhan1` repo.

---

## 📄 README.md

```markdown
<h1 align="center">Hi 👋, I'm Moosa Khan</h1>
<div align="center">
  <a href="https://git.io/typing-svg" align="center">
    <img
      src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=26&weight=800&pause=1000&color=8651F7&center=true&vCenter=true&random=false&width=520&lines=Hi%2C+I+am+Moosa+Khan;From+Pakistan+%F0%9F%87%B5%F0%9F%87%B0;Dedicated+Developer+%F0%9F%9A%80;Continuous+Improver+%E2%9D%A4;Innovative+Thinker+%E2%9C%8C"
      alt="Typing SVG"
    />
  </a>
</div>

<h3 align="center">A passionate full‑stack developer from Pakistan</h3>

<img align="right" alt="Coding" width="380" src="https://camo.githubusercontent.com/1a28adbdab3fbb859ff593fcb88c8af70f97abebd21879da637ac2855d5a98ea/68747470733a2f2f7777772e77656232347a6f6e652e636f6d2f77702d636f6e74656e742f75706c6f6164732f323032322f30392f3263373738655f38396430396333383062376234613039626364626362333239633437333462335f6d76322e676966" />

<p>.</p>

- 🌱 I’m currently learning **Next.js, React.js, React Native, MongoDB & Strapi**  
- 📫 Reach me at **moosakhan033233@gmail.com**  
- 🌍 My projects: **https://vercel.com/moosa-khan1s-projects**

---

### 🧰 Languages & Tools
<p align="center">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" width="40" height="40" alt="HTML5"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" width="40" height="40" alt="CSS3"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="40" height="40" alt="JavaScript"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="40" height="40" alt="TypeScript"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" width="40" height="40" alt="React"/>
  <img src="https://cdn.worldvectorlogo.com/logos/nextjs-2.svg" width="40" height="40" alt="Next.js"/>
  <img src="https://reactnative.dev/img/header_logo.svg" width="40" height="40" alt="React Native"/>
  <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" width="40" height="40" alt="Tailwind CSS"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" width="40" height="40" alt="Node.js"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" width="40" height="40" alt="Express"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" width="40" height="40" alt="MongoDB"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redux/redux-original.svg" width="40" height="40" alt="Redux"/>
  <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" width="40" height="40" alt="Git"/>
  <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" width="40" height="40" alt="Postman"/>
  <img src="https://seeklogo.com/images/S/strapi-logo-3551DD3749-seeklogo.com.png" width="40" height="40" alt="Strapi"/>
</p>

---

### 🧊 3D Touch for the Profile (Images work in README)

> GitHub README cannot run JavaScript directly, but we can **embed generated 3D images** and link to a live Three.js demo.

#### 1) 3D Contribution Graph (auto‑generated)
After the workflow (below) runs, this image will appear:

<p align="center">
  <img src="./profile-3d-contrib/profile-night-rainbow.svg" alt="3D Contribution Graph" width="720"/>
</p>

#### 2) 3D Profile Card (static image)
<p align="center">
  <img src="https://raw.githubusercontent.com/insolitum/github-profile-3d-card/main/docs/img/profile-3d.gif" width="520" alt="3D Profile Card"/>
</p>

#### 3) Live Three.js Demo (hosted)
<p align="center">
  <a href="https://your-3d-demo.vercel.app" target="_blank">
    <img src="./three-demo/preview.gif" width="520" alt="Open Live 3D Demo"/>
  </a>
</p>

---

### 📈 GitHub Stats
<p>
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=moosakhan1&show_icons=true&locale=en&layout=compact" alt="Top Langs" />
</p>

<p>
  <img align="center" src="https://github-readme-stats.vercel.app/api?username=moosakhan1&show_icons=true&locale=en" alt="Stats" />
</p>

<p>
  <img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=moosakhan1" alt="Streak" />
</p>

---

> ✨ Tip: Replace `https://your-3d-demo.vercel.app` with your deployed Three.js demo link.
```

---

## ⚙️ .github/workflows/3d-contrib.yml (Generates 3D contribution SVG)

```yaml
name: Generate 3D Contribution Graph

on:
  schedule:
    - cron: '0 0 * * 1'   # Every Monday at 00:00 UTC
  workflow_dispatch: {}

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Generate 3D profile (night-rainbow)
        uses: yoshi389111/github-profile-3d-contrib@0.7.1
        with:
          username: moosakhan1
          theme: night-rainbow
          output-file: profile-3d-contrib/profile-night-rainbow.svg

      - name: Commit & Push
        run: |
          git config user.name "github-actions"
          git config user.email "github-actions@github.com"
          git add -A
          git commit -m "chore: update 3D contribution graph" || echo "No changes"
          git push
```

> After the first run completes, the image path `./profile-3d-contrib/profile-night-rainbow.svg` in your README will start working.

---

## 🎮 three-demo (Simple Three.js site you can deploy to Vercel)

Create a folder named `three-demo` at the repo root with the following files.

### three-demo/index.html

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Moosa Khan • Three.js Demo</title>
    <link rel="stylesheet" href="./style.css" />
  </head>
  <body>
    <canvas id="scene"></canvas>
    <div class="badge">Three.js • Moosa Khan</div>
    <script type="module" src="./main.js"></script>
  </body>
</html>
```

### three-demo/style.css

```css
* { box-sizing: border-box; }
html, body { margin: 0; height: 100%; background: radial-gradient(#0f1226, #04050f); }
#scene { display: block; width: 100vw; height: 100vh; }
.badge {
  position: fixed; left: 50%; bottom: 24px; transform: translateX(-50%);
  padding: 8px 14px; border-radius: 999px; font: 600 14px/1.2 system-ui;
  color: white; backdrop-filter: blur(6px); background: rgba(255,255,255,0.08);
  letter-spacing: .3px; border: 1px solid rgba(255,255,255,0.15);
}
```

### three-demo/main.js

```js
import * as THREE from 'https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js';
import { OrbitControls } from 'https://cdn.jsdelivr.net/npm/three@0.160.0/examples/jsm/controls/OrbitControls.js';

const canvas = document.getElementById('scene');
const renderer = new THREE.WebGLRenderer({ canvas, antialias: true, alpha: true });
renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
renderer.setSize(window.innerWidth, window.innerHeight);

const scene = new THREE.Scene();
scene.fog = new THREE.Fog(0x0b0e23, 8, 30);

const camera = new THREE.PerspectiveCamera(60, window.innerWidth / window.innerHeight, 0.1, 100);
camera.position.set(6, 4, 8);

const controls = new OrbitControls(camera, renderer.domElement);
controls.enableDamping = true;
controls.autoRotate = true;
controls.autoRotateSpeed = 0.7;

// Lighting
const hemi = new THREE.HemisphereLight(0x88aaff, 0x080820, 1.1);
scene.add(hemi);
const dir = new THREE.DirectionalLight(0xffffff, 1.0);
dir.position.set(5, 10, 7);
scene.add(dir);

// Star field
const starGeom = new THREE.BufferGeometry();
const starCount = 800;
const positions = new Float32Array(starCount * 3);
for (let i = 0; i < starCount; i++) {
  positions[i * 3 + 0] = (Math.random() - 0.5) * 60;
  positions[i * 3 + 1] = (Math.random() - 0.5) * 60;
  positions[i * 3 + 2] = (Math.random() - 0.5) * 60;
}
starGeom.setAttribute('position', new THREE.BufferAttribute(positions, 3));
const starMat = new THREE.PointsMaterial({ size: 0.05 });
const stars = new THREE.Points(starGeom, starMat);
scene.add(stars);

// Floating wireframe torus + cube
const torus = new THREE.Mesh(
  new THREE.TorusGeometry(2.2, 0.7, 16, 100),
  new THREE.MeshPhysicalMaterial({ wireframe: true, transmission: 0.4, roughness: 0.2, reflectivity: 0.5 })
);
scene.add(torus);

const cube = new THREE.Mesh(
  new THREE.BoxGeometry(1.2, 1.2, 1.2),
  new THREE.MeshStandardMaterial({ metalness: 0.6, roughness: 0.2 })
);
cube.position.set(0, 0.6, 0);
scene.add(cube);

// Responsive
window.addEventListener('resize', () => {
  camera.aspect = window.innerWidth / window.innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(window.innerWidth, window.innerHeight);
});

let t = 0;
function animate() {
  requestAnimationFrame(animate);
  t += 0.01;
  torus.rotation.x += 0.003;
  torus.rotation.y += 0.004;
  cube.rotation.x += 0.02;
  cube.rotation.y += 0.015;
  cube.position.y = 0.6 + Math.sin(t) * 0.2;
  controls.update();
  renderer.render(scene, camera);
}
animate();
```

> Deploy the `three-demo` folder to **Vercel** (as a separate project). After deploy, update the README link: `https://your-3d-demo.vercel.app`.

---

## 🖼 Optional: Create a GIF preview

1. Open your deployed Three.js page in the browser.
2. Record \~5–10 seconds with a screen recorder.
3. Convert to GIF (e.g., ezgif.com) and save it as `three-demo/preview.gif` in the repo. The README already references this path.

---

## ✅ What to do now

1. **Commit** these files to `moosakhan1/moosakhan1`.
2. Go to the **Actions** tab and enable workflows if prompted.
3. Run the **“Generate 3D Contribution Graph”** workflow once (`Run workflow`).
4. Deploy `three-demo` to Vercel and update the demo link in README.

That’s it — your profile will have a clean layout, stats, and a genuine 3D flavor ✨.
