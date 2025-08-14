<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Arian Milkshake Making Guide</title>
  <meta name="description" content="Arian Milkshake Making Guide — learn the basics, browse recipes, and build your perfect milkshake." />
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🥤</text></svg>">
  <style>
    :root{
      --bg: #0f0f12;
      --panel: #16161b;
      --muted: #a8a8b3;
      --text: #f6f6f9;
      --accent: #7c5cff;
      --accent-2: #23d5ab;
      --ring: rgba(124,92,255,.35);
      --card: #1b1b22;
      --good: #3ddc97;
      --warn: #ffcc66;
      --danger: #ff6b6b;
      --radius: 14px;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --grid-gap: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 800px at 20% -10%, #1b1b22 0%, #0f0f12 50%, #0a0a0d 100%);
      color:var(--text);
      line-height:1.6;
    }

    a{color:var(--accent); text-decoration:none}
    a:hover{text-decoration:underline}
    .container{max-width:1100px; margin:0 auto; padding:24px}

    /* Header / Nav */
    header{
      position:sticky; top:0; z-index:50;
      background: rgba(15,15,18,.65);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(255,255,255,.06);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      gap:16px; padding:10px 0;
    }
    .brand{
      display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.3px;
    }
    .brand .logo{
      width:34px; height:34px; display:grid; place-items:center;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      color:#0b0b10; border-radius:10px; font-weight:900;
      box-shadow: var(--shadow);
    }
    nav a{padding:8px 12px; border-radius:10px; color:var(--text)}
    nav a:hover{background:rgba(255,255,255,.06); text-decoration:none}

    /* Hero */
    .hero{
      display:grid; grid-template-columns: 1.1fr .9fr; gap:30px;
      padding: 36px 0 14px;
    }
    .hero .card{
      background: linear-gradient(180deg, rgba(124,92,255,.12), rgba(124,92,255,0) 60%);
      border:1px solid rgba(124,92,255,.25);
    }
    .card{
      background: var(--card);
      border:1px solid rgba(255,255,255,.06);
      border-radius: var(--radius);
      padding: 20px;
      box-shadow: var(--shadow);
    }
    h1{font-size: clamp(30px, 3.6vw, 44px); line-height:1.2; margin:0 0 10px}
    h2{font-size: clamp(22px, 2.6vw, 30px); margin:0 0 8px}
    p.muted{color:var(--muted); margin-top:6px}

    .hero-cta{display:flex; gap:10px; flex-wrap:wrap; margin-top:12px}
    .btn{
      appearance:none; border:1px solid rgba(255,255,255,.12);
      color:var(--text); background: #1f1f28; padding:10px 14px; border-radius:12px;
      cursor:pointer; font-weight:600;
      transition: transform .05s ease, background .2s ease, border-color .2s ease;
    }
    .btn:hover{transform: translateY(-1px); background:#242430}
    .btn.primary{
      background: linear-gradient(135deg, var(--accent) 0%, var(--accent-2) 100%);
      color:#0b0b10; border-color:transparent;
    }
    .grid{
      display:grid; gap:var(--grid-gap);
      grid-template-columns: repeat(12, 1fr);
    }
    .col-6{grid-column: span 6}
    .col-12{grid-column: span 12}

    /* Recipe cards */
    .recipes{
      margin-top: 26px;
    }
    .cards{
      display:grid; grid-template-columns: repeat( auto-fit, minmax(240px, 1fr) );
      gap: var(--grid-gap);
    }
    .recipe{
      position:relative; overflow:hidden
    }
    .recipe .topline{
      display:flex; align-items:center; justify-content:space-between; gap:10px; margin-bottom:6px
    }
    .pill{
      font-size:12px; color:#0b0b10; background: var(--good); padding:4px 8px; border-radius:999px; font-weight:700;
    }
    .badge{font-size:12px; color:var(--muted)}
    .recipe h3{margin:6px 0 8px}
    .recipe ul{margin:0 0 8px 18px; padding:0}
    .mini{
      font-size:12px; color:var(--muted)
    }

    /* Tools / steps */
    .steps{display:grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap:var(--grid-gap); margin-top:8px}
    .step{display:flex; gap:12px}
    .step .num{width:28px;height:28px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:grid;place-items:center;color:#0b0b10;font-weight:900;flex:0 0 28px}

    /* Calculator & Builder */
    .panel-title{display:flex; align-items:center; justify-content:space-between}
    .field{display:grid; gap:6px; margin:8px 0}
    label{font-weight:600}
    input[type="number"], select, input[type="range"]{
      width:100%; padding:10px 12px; border-radius:10px; border:1px solid rgba(255,255,255,.12);
      background:#1f1f28; color:var(--text);
      outline:none; box-shadow: none;
    }
    input[type="range"]{padding:0; height:36px}
    .out{
      background:#13131a; border:1px solid rgba(255,255,255,.06); border-radius:12px; padding:12px; font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace
    }
    .row{display:grid; grid-template-columns: 1fr 1fr; gap:10px}
    .kicker{font-size:13px; letter-spacing:.2px; color:var(--muted); text-transform:uppercase}
    .note{font-size:13px; color:var(--muted)}

    footer{
      margin: 30px 0 60px; color:var(--muted); text-align:center;
    }

    @media (max-width: 860px){
      .hero{grid-template-columns:1fr}
      .col-6{grid-column: span 12}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand" aria-label="Site brand">
        <div class="logo" aria-hidden="true">AM</div>
        <span>Arian Milkshake Making Guide</span>
      </div>
      <nav aria-label="Main navigation">
        <a href="#recipes">Recipes</a>
        <a href="#how-to">How-To</a>
        <a href="#calculator">Calculator</a>
        <a href="#builder">Builder</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <!-- HERO -->
    <section class="hero">
      <div class="card">
        <h1>Make ridiculously good milkshakes 🥤</h1>
        <p class="muted">Fast, creamy, and customizable. Learn the basics, browse tried‑and‑true recipes, and build your perfect shake.</p>
        <div class="hero-cta">
          <a class="btn primary" href="#builder">Build Your Shake</a>
          <a class="btn" href="#recipes">See Popular Recipes</a>
        </div>
        <p class="note">Tip: Aim for a <strong>2:1 ice cream : milk</strong> ratio by volume. Too thick? Add milk 1 tbsp at a time. Too thin? Add a scoop.</p>
      </div>
      <div class="card" role="img" aria-label="Decorative milkshake gradient">
        <h2 class="kicker">Quick Basics</h2>
        <ul>
          <li><strong>Base ratio:</strong> 2 scoops ice cream + ¾ cup milk per shake</li>
          <li><strong>Blend:</strong> 20–30 sec, pulse if needed</li>
          <li><strong>Glass prep:</strong> Chill glass 10 min for thicker feel</li>
          <li><strong>Add‑ins:</strong> 2–4 tbsp chunky mix‑ins at the end</li>
        </ul>
        <p class="mini">All amounts are suggestions—adjust to taste.</p>
      </div>
    </section>

    <!-- RECIPES -->
    <section id="recipes" class="recipes">
      <div class="panel-title">
        <h2>Popular Recipes</h2>
        <span class="kicker">Tap a card to view details</span>
      </div>
      <div class="cards" role="list">
        <article class="card recipe" role="listitem" tabindex="0">
          <div class="topline">
            <span class="pill">Classic</span>
            <span class="badge">~5 min</span>
          </div>
          <h3>Vanilla Dream</h3>
          <ul>
            <li>2 scoops vanilla ice cream</li>
            <li>¾ cup (180 ml) whole milk</li>
            <li>½ tsp vanilla extract</li>
            <li>1 tbsp sugar (optional)</li>
          </ul>
          <p class="mini">Blend smooth. Top with whipped cream + sprinkles.</p>
        </article>

        <article class="card recipe" role="listitem" tabindex="0">
          <div class="topline">
            <span class="pill" style="background:#7ec8ff">Chocolate</span>
            <span class="badge">~6 min</span>
          </div>
          <h3>Double Choc</h3>
          <ul>
            <li>2 scoops chocolate ice cream</li>
            <li>¾ cup (180 ml) milk</li>
            <li>1½ tbsp cocoa + 1 tbsp syrup</li>
            <li>Pinch of salt</li>
          </ul>
          <p class="mini">Salt brightens chocolate flavor—don’t skip it.</p>
        </article>

        <article class="card recipe" role="listitem" tabindex="0">
          <div class="topline">
            <span class="pill" style="background:#ff8db2">Fruit</span>
            <span class="badge">~6 min</span>
          </div>
          <h3>Strawberry Burst</h3>
          <ul>
            <li>2 scoops vanilla or strawberry ice cream</li>
            <li>½ cup (120 ml) milk + ½ cup strawberries</li>
            <li>1–2 tsp sugar or honey</li>
          </ul>
          <p class="mini">Blend berries first if using frozen.</p>
        </article>

        <article class="card recipe" role="listitem" tabindex="0">
          <div class="topline">
            <span class="pill" style="background:#ffd166">Cookie</span>
            <span class="badge">~7 min</span>
          </div>
          <h3>Cookies & Cream</h3>
          <ul>
            <li>2 scoops vanilla</li>
            <li>¾ cup (180 ml) milk</li>
            <li>4–5 crushed chocolate sandwich cookies</li>
          </ul>
          <p class="mini">Fold in half the cookies at the end for chunks.</p>
        </article>

        <article class="card recipe" role="listitem" tabindex="0">
          <div class="topline">
            <span class="pill" style="background:#3ddc97">Vegan</span>
            <span class="badge">~5 min</span>
          </div>
          <h3>Banana Almond</h3>
          <ul>
            <li>1 frozen banana (in chunks)</li>
            <li>½ cup (120 ml) almond milk</li>
            <li>2 scoops dairy‑free vanilla</li>
            <li>½ tsp cinnamon</li>
          </ul>
          <p class="mini">Banana adds body—use less milk as needed.</p>
        </article>
      </div>
    </section>

    <!-- HOW-TO STEPS -->
    <section id="how-to" class="card" style="margin-top:24px">
      <h2>How to Make a Great Milkshake</h2>
      <div class="steps">
        <div class="step">
          <div class="num">1</div>
          <div>
            <strong>Chill gear.</strong>
            <div class="mini">Freeze the glass and briefly chill your blender jar for max thickness.</div>
          </div>
        </div>
        <div class="step">
          <div class="num">2</div>
          <div>
            <strong>Add liquids first.</strong>
            <div class="mini">Milk at the bottom helps the blades catch.</div>
          </div>
        </div>
        <div class="step">
          <div class="num">3</div>
          <div>
            <strong>Use short pulses.</strong>
            <div class="mini">Blend 20–30 seconds. Pulse with mix‑ins to keep chunks.</div>
          </div>
        </div>
        <div class="step">
          <div class="num">4</div>
          <div>
            <strong>Tune the texture.</strong>
            <div class="mini">Too thick → add 1–2 tbsp milk. Too thin → add ½–1 scoop ice cream.</div>
          </div>
        </div>
      </div>
    </section>

    <!-- CALCULATOR -->
    <section id="calculator" class="grid" style="margin-top:24px">
      <div class="col-6">
        <div class="card">
          <h2>Servings Calculator</h2>
          <p class="muted">Base per 1 shake: <strong>2 scoops ice cream</strong>, <strong>¾ cup (180 ml) milk</strong>, <strong>½ tsp vanilla</strong>, <strong>1 tbsp sugar</strong> (optional).</p>
          <div class="field">
            <label for="servings">Servings: <span id="servingsLabel" aria-live="polite">1</span></label>
            <input type="range" id="servings" min="1" max="8" value="1" />
          </div>
          <div class="out" id="calcOut" aria-live="polite"></div>
          <p class="note">Estimates only. Sweetness varies with ice cream brand.</p>
        </div>
      </div>
      <div class="col-6">
        <div class="card">
          <h2>Nutrition (estimate per serving)</h2>
          <p class="muted">Based on vanilla base with whole milk; toppings not included.</p>
          <ul>
            <li>Calories: ~360</li>
            <li>Protein: ~8 g</li>
            <li>Carbs: ~45 g</li>
            <li>Fat: ~16 g</li>
            <li>Sugar: ~40 g</li>
          </ul>
          <p class="note">For lighter shakes: use 2% milk, less sugar, or add frozen fruit.</p>
        </div>
      </div>
    </section>

    <!-- BUILDER -->
    <section id="builder" class="card" style="margin-top:24px">
      <h2>Build Your Milkshake</h2>
      <div class="row">
        <div>
          <div class="field">
            <label for="base">Base Flavor</label>
            <select id="base">
              <option value="vanilla">Vanilla</option>
              <option value="chocolate">Chocolate</option>
              <option value="strawberry">Strawberry</option>
              <option value="cookies">Cookies &amp; Cream</option>
              <option value="banana">Banana (dairy‑free)</option>
            </select>
          </div>
          <div class="field">
            <label for="milk">Milk Type</label>
            <select id="milk">
              <option value="whole">Whole Milk</option>
              <option value="two">2% Milk</option>
              <option value="almond">Almond Milk</option>
              <option value="oat">Oat Milk</option>
            </select>
          </div>
          <div class="row">
            <div class="field">
              <label for="thickness">Thickness</label>
              <select id="thickness">
                <option value="classic">Classic</option>
                <option value="thick">Extra Thick</option>
                <option value="thin">Sippable</option>
              </select>
            </div>
            <div class="field">
              <label for="mixins">Mix‑ins (optional)</label>
              <select id="mixins" multiple size="4" aria-label="Choose one or more mix-ins">
                <option value="chips">Chocolate chips</option>
                <option value="cookie">Cookie pieces</option>
                <option value="strawberry">Strawberries</option>
                <option value="banana">Banana</option>
              </select>
            </div>
          </div>
          <button class="btn primary" id="buildBtn">Generate Instructions</button>
        </div>
        <div>
          <div class="field">
            <label>Instructions</label>
            <div class="out" id="buildOut">Choose options and click “Generate Instructions.”</div>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div>© <span id="year"></span> Arian Milkshake Making Guide • Made with love &amp; lactose (optional)</div>
    </footer>
  </main>

  <script>
    // Utilities
    const round = (n, p=2) => Math.round(n * Math.pow(10, p)) / Math.pow(10, p);

    // Servings calculator
    const servingsEl = document.getElementById('servings');
    const servingsLabel = document.getElementById('servingsLabel');
    const calcOut = document.getElementById('calcOut');

    function renderCalc() {
      const s = Number(servingsEl.value);
      servingsLabel.textContent = s;

      // Base per serving
      const iceCreamScoops = 2 * s;
      const milkMl = 180 * s; // 3/4 cup ≈ 180 ml
      const milkCups = round(milkMl / 240, 2); // 1 cup ~ 240 ml
      const vanillaTsp = 0.5 * s;
      const sugarTbsp = 1 * s;

      calcOut.innerHTML = `
        <div><strong>For ${s} ${s===1?'shake':'shakes'}:</strong></div>
        <ul style="margin:8px 0 0 18px">
          <li>${iceCreamScoops} scoops ice cream</li>
          <li>${milkMl} ml milk <span class="mini">(~${milkCups} cups)</span></li>
          <li>${vanillaTsp} tsp vanilla extract</li>
          <li>${sugarTbsp} tbsp sugar <span class="mini">(optional)</span></li>
        </ul>
      `;
    }
    servingsEl.addEventListener('input', renderCalc);
    renderCalc();

    // Builder tool
    const baseEl = document.getElementById('base');
    const milkEl = document.getElementById('milk');
    const thickEl = document.getElementById('thickness');
    const mixinsEl = document.getElementById('mixins');
    const buildBtn = document.getElementById('buildBtn');
    const buildOut = document.getElementById('buildOut');

    function build() {
      const base = baseEl.value;
      const milk = milkEl.value;
      const thickness = thickEl.value;
      const mixins = Array.from(mixinsEl.selectedOptions).map(o => o.textContent);

      // Base amounts
      let scoops = 2, milkMl = 180;
      if (thickness === 'thick') { milkMl -= 40; scoops += 0.5; }
      if (thickness === 'thin')  { milkMl += 40; }

      // Flavor notes
      const baseName = {
        vanilla: 'Vanilla',
        chocolate: 'Chocolate',
        strawberry: 'Strawberry',
        cookies: 'Cookies & Cream',
        banana: 'Banana (dairy‑free)'
      }[base];

      const milkName = {
        whole: 'whole milk',
        two: '2% milk',
        almond: 'almond milk',
        oat: 'oat milk'
      }[milk];

      const extras = [];
      if (base === 'chocolate') extras.push('1 tbsp chocolate syrup + 1 tbsp cocoa, pinch of salt');
      if (base === 'strawberry') extras.push('½ cup strawberries, 1–2 tsp sugar');
      if (base === 'cookies') extras.push('4–5 crushed cookies');
      if (base === 'banana') extras.push('½ tsp cinnamon, 1 frozen banana');

      const mixText = mixins.length ? `Fold in ${mixins.join(', ')} at the end (pulse 2–3×).` : 'Add toppings if you like and serve.';

      buildOut.innerHTML = `
        <div><strong>${baseName} milkshake</strong> with <strong>${milkName}</strong> — ${thickness}.</div>
        <ol style="margin:8px 0 0 18px">
          <li>Add ${milkMl} ml ${milkName} to blender.</li>
          <li>Add ${scoops} scoops ice cream.</li>
          ${extras.length ? `<li>Add: ${extras.join('; ')}.</li>` : ''}
          <li>Blend 20–30 sec until smooth.</li>
          <li>${mixText}</li>
          <li>Pour into a chilled glass. Enjoy! 🥤</li>
        </ol>
        <div class="mini">Tip: If too thick, add milk 1–2 tbsp at a time. If thin, add ½ scoop and pulse.</div>
      `;
    }
    buildBtn.addEventListener('click', build);

    // Year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
