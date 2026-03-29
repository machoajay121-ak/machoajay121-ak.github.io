# machoajay121-ak.github.io
Supply Chain - Revisits
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Strategic Sourcing — Learning Guide</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0f0f0f;
    --cream: #faf7f2;
    --amber: #d4820a;
    --amber-light: #f5c842;
    --teal: #1a6b6b;
    --teal-light: #e0f2f2;
    --rose: #a83240;
    --rose-light: #fde8ea;
    --slate: #2e3a4a;
    --slate-mid: #5a6a7a;
    --slate-light: #eef1f4;
    --white: #ffffff;
    --border: #e2ddd6;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    line-height: 1.7;
    font-size: 16px;
  }

  /* HERO */
  .hero {
    background: var(--slate);
    color: var(--white);
    padding: 80px 40px 60px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 320px; height: 320px;
    border-radius: 50%;
    background: radial-gradient(circle, #f5c84244 0%, transparent 70%);
    pointer-events: none;
  }
  .hero::after {
    content: '';
    position: absolute;
    bottom: -80px; left: 10%;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: radial-gradient(circle, #1a6b6b44 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-label {
    font-size: 11px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--amber-light);
    margin-bottom: 16px;
    font-weight: 500;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.4rem, 5vw, 4rem);
    font-weight: 900;
    line-height: 1.1;
    max-width: 700px;
  }
  .hero h1 span { color: var(--amber-light); }
  .hero-sub {
    margin-top: 20px;
    color: #b8c8d8;
    max-width: 560px;
    font-size: 1.05rem;
  }
  .hero-meta {
    margin-top: 32px;
    display: flex;
    gap: 32px;
    flex-wrap: wrap;
  }
  .hero-meta-item {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }
  .hero-meta-item .num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 700;
    color: var(--amber-light);
  }
  .hero-meta-item .lbl {
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #8899aa;
  }

  /* NAV TABS */
  .nav-tabs {
    background: var(--white);
    border-bottom: 2px solid var(--border);
    display: flex;
    overflow-x: auto;
    padding: 0 32px;
    gap: 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 12px rgba(0,0,0,0.06);
  }
  .nav-tab {
    padding: 18px 24px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.5px;
    color: var(--slate-mid);
    border-bottom: 3px solid transparent;
    cursor: pointer;
    white-space: nowrap;
    transition: all 0.2s;
    text-decoration: none;
  }
  .nav-tab:hover { color: var(--teal); }
  .nav-tab.active { color: var(--teal); border-bottom-color: var(--teal); }

  /* LAYOUT */
  .container { max-width: 900px; margin: 0 auto; padding: 60px 32px; }

  /* SECTION HEADER */
  .section-header {
    margin-bottom: 40px;
  }
  .section-tag {
    display: inline-block;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--amber);
    margin-bottom: 10px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 700;
    color: var(--slate);
    line-height: 1.2;
  }
  .section-desc {
    margin-top: 12px;
    color: var(--slate-mid);
    font-size: 1.05rem;
    max-width: 620px;
  }

  /* CONCEPT CARDS */
  .concept-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
    margin-bottom: 48px;
  }
  .concept-card {
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 12px;
    padding: 28px 24px;
    position: relative;
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .concept-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 28px rgba(0,0,0,0.09);
  }
  .concept-card .icon {
    font-size: 2rem;
    margin-bottom: 14px;
    display: block;
  }
  .concept-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--slate);
    margin-bottom: 10px;
  }
  .concept-card p {
    font-size: 0.93rem;
    color: var(--slate-mid);
    line-height: 1.65;
  }
  .concept-card.amber { border-top: 4px solid var(--amber); }
  .concept-card.teal  { border-top: 4px solid var(--teal); }
  .concept-card.rose  { border-top: 4px solid var(--rose); }
  .concept-card.slate { border-top: 4px solid var(--slate); }

  /* ANALOGY BLOCK */
  .analogy {
    background: linear-gradient(135deg, var(--teal-light) 0%, #f0fafa 100%);
    border-left: 5px solid var(--teal);
    border-radius: 0 12px 12px 0;
    padding: 28px 32px;
    margin: 40px 0;
  }
  .analogy .analogy-label {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 10px;
  }
  .analogy p {
    font-size: 1.05rem;
    color: var(--slate);
  }
  .analogy strong { color: var(--teal); }

  /* COMPARE TABLE */
  .compare-table {
    width: 100%;
    border-collapse: collapse;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 16px rgba(0,0,0,0.07);
    margin: 32px 0;
  }
  .compare-table thead tr {
    background: var(--slate);
    color: var(--white);
  }
  .compare-table thead th {
    padding: 18px 20px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    text-align: left;
  }
  .compare-table tbody tr:nth-child(odd) { background: var(--white); }
  .compare-table tbody tr:nth-child(even) { background: var(--slate-light); }
  .compare-table tbody td {
    padding: 14px 20px;
    font-size: 0.93rem;
    color: var(--slate);
    border-bottom: 1px solid var(--border);
    vertical-align: top;
  }
  .compare-table tbody td:first-child {
    font-weight: 600;
    color: var(--slate-mid);
    width: 30%;
  }
  .tag-bad {
    display: inline-block;
    background: var(--rose-light);
    color: var(--rose);
    font-size: 11px;
    font-weight: 600;
    border-radius: 20px;
    padding: 2px 10px;
  }
  .tag-good {
    display: inline-block;
    background: var(--teal-light);
    color: var(--teal);
    font-size: 11px;
    font-weight: 600;
    border-radius: 20px;
    padding: 2px 10px;
  }

  /* STEPS */
  .steps { margin: 40px 0; }
  .step {
    display: flex;
    gap: 24px;
    margin-bottom: 32px;
    position: relative;
  }
  .step:not(:last-child)::after {
    content: '';
    position: absolute;
    left: 22px;
    top: 52px;
    width: 2px;
    height: calc(100% - 10px);
    background: var(--border);
  }
  .step-num {
    width: 46px;
    height: 46px;
    border-radius: 50%;
    background: var(--slate);
    color: var(--white);
    font-family: 'Playfair Display', serif;
    font-weight: 700;
    font-size: 1.1rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    z-index: 1;
  }
  .step-body { padding-top: 6px; }
  .step-body h4 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--slate);
    margin-bottom: 6px;
  }
  .step-body p {
    font-size: 0.93rem;
    color: var(--slate-mid);
    line-height: 1.65;
  }
  .step-body .tip {
    margin-top: 10px;
    background: #fffbf0;
    border: 1px solid #f5c84255;
    border-radius: 8px;
    padding: 10px 14px;
    font-size: 0.87rem;
    color: #8a6400;
  }
  .step-body .tip::before { content: '💡 '; }

  /* MATRIX */
  .matrix-wrap {
    margin: 40px 0;
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 16px;
    padding: 32px;
    box-shadow: 0 2px 16px rgba(0,0,0,0.05);
  }
  .matrix-wrap h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.25rem;
    font-weight: 700;
    color: var(--slate);
    margin-bottom: 24px;
  }
  .matrix-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 12px;
    max-width: 600px;
    margin: 0 auto;
  }
  .matrix-cell {
    border-radius: 10px;
    padding: 20px;
    min-height: 130px;
  }
  .matrix-cell h4 { font-size: 0.9rem; font-weight: 700; margin-bottom: 8px; }
  .matrix-cell p  { font-size: 0.82rem; line-height: 1.6; }
  .matrix-cell.strategic { background: #fff0e8; color: #7a3300; border: 1.5px solid #f5a050; }
  .matrix-cell.leverage  { background: #e8f5ee; color: #0a4f22; border: 1.5px solid #4caf50; }
  .matrix-cell.bottleneck{ background: #fde8ea; color: #7a0018; border: 1.5px solid #e57373; }
  .matrix-cell.noncritical{ background: var(--slate-light); color: var(--slate); border: 1.5px solid var(--border); }
  .matrix-axis {
    display: flex;
    justify-content: space-between;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--slate-mid);
    margin-top: 12px;
    padding: 0 4px;
    font-weight: 600;
  }
  .matrix-y-label {
    writing-mode: vertical-rl;
    transform: rotate(180deg);
    text-align: center;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--slate-mid);
    font-weight: 600;
    margin-right: 8px;
    align-self: center;
  }
  .matrix-inner { display: flex; }

  /* HIGHLIGHT BOX */
  .highlight-box {
    border-radius: 14px;
    padding: 28px 32px;
    margin: 32px 0;
  }
  .highlight-box.amber {
    background: linear-gradient(135deg, #fffbf0 0%, #fff9e6 100%);
    border: 1.5px solid #f5c84266;
  }
  .highlight-box.rose {
    background: var(--rose-light);
    border: 1.5px solid #e8a0a8;
  }
  .highlight-box h4 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    margin-bottom: 14px;
  }
  .highlight-box.amber h4 { color: #7a5200; }
  .highlight-box.rose h4 { color: var(--rose); }
  .highlight-box ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .highlight-box li {
    font-size: 0.93rem;
    display: flex;
    gap: 10px;
    align-items: flex-start;
  }
  .highlight-box.amber li::before { content: '✓'; color: var(--amber); font-weight: 700; flex-shrink: 0; }
  .highlight-box.rose li::before  { content: '✗'; color: var(--rose);  font-weight: 700; flex-shrink: 0; }
  .highlight-box li span { color: var(--slate); line-height: 1.55; }

  /* QUIZ */
  .quiz-block {
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 14px;
    padding: 28px 32px;
    margin: 28px 0;
  }
  .quiz-block .q-label {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--rose);
    margin-bottom: 12px;
  }
  .quiz-block .question {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--slate);
    margin-bottom: 16px;
  }
  .options { display: flex; flex-direction: column; gap: 10px; }
  .option {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 12px 16px;
    border: 1.5px solid var(--border);
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.18s;
    font-size: 0.93rem;
    color: var(--slate);
    user-select: none;
  }
  .option:hover { border-color: var(--teal); background: var(--teal-light); }
  .option.correct { border-color: var(--teal); background: var(--teal-light); color: var(--teal); }
  .option.wrong   { border-color: var(--rose); background: var(--rose-light); color: var(--rose); }
  .option .opt-letter {
    width: 28px; height: 28px;
    border-radius: 50%;
    background: var(--slate-light);
    display: flex; align-items: center; justify-content: center;
    font-weight: 700; font-size: 12px;
    flex-shrink: 0;
  }
  .option.correct .opt-letter { background: var(--teal); color: var(--white); }
  .option.wrong   .opt-letter { background: var(--rose); color: var(--white); }
  .quiz-feedback {
    margin-top: 14px;
    padding: 12px 16px;
    border-radius: 8px;
    font-size: 0.9rem;
    display: none;
  }
  .quiz-feedback.show { display: block; }
  .quiz-feedback.correct-fb { background: var(--teal-light); color: var(--teal); }
  .quiz-feedback.wrong-fb   { background: var(--rose-light);  color: var(--rose); }

  /* DIVIDER */
  .section-divider {
    border: none;
    border-top: 2px solid var(--border);
    margin: 60px 0;
  }

  /* KEY TERMS */
  .terms-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
    margin: 32px 0;
  }
  .term-card {
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 20px 18px;
  }
  .term-card .term {
    font-weight: 700;
    font-size: 0.95rem;
    color: var(--teal);
    margin-bottom: 6px;
  }
  .term-card .def {
    font-size: 0.87rem;
    color: var(--slate-mid);
    line-height: 1.6;
  }

  /* SUMMARY CARD */
  .summary-card {
    background: var(--slate);
    color: var(--white);
    border-radius: 16px;
    padding: 40px 36px;
    margin-top: 40px;
  }
  .summary-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 20px;
    color: var(--amber-light);
  }
  .summary-points {
    display: flex;
    flex-direction: column;
    gap: 14px;
  }
  .summary-point {
    display: flex;
    gap: 14px;
    align-items: flex-start;
    font-size: 0.95rem;
    color: #c8d8e8;
    line-height: 1.6;
  }
  .summary-point .num {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--amber-light);
    flex-shrink: 0;
    line-height: 1.4;
  }

  /* SECTION VISIBILITY */
  .page-section { display: none; }
  .page-section.active { display: block; }

  /* RESPONSIVE */
  @media (max-width: 600px) {
    .container { padding: 40px 16px; }
    .hero { padding: 50px 20px 40px; }
    .matrix-grid { grid-template-columns: 1fr; }
    .nav-tabs { padding: 0 12px; }
    .nav-tab { padding: 16px 14px; font-size: 12px; }
    .compare-table thead th, .compare-table tbody td { padding: 12px 14px; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-label">Procurement Mastery Series</div>
  <h1>Strategic<br><span>Sourcing</span><br>Simplified</h1>
  <p class="hero-sub">A complete learning guide — from the basics to expert-level strategy — in plain, simple language.</p>
  <div class="hero-meta">
    <div class="hero-meta-item">
      <span class="num">7</span>
      <span class="lbl">Step Process</span>
    </div>
    <div class="hero-meta-item">
      <span class="num">3</span>
      <span class="lbl">Sourcing Types</span>
    </div>
    <div class="hero-meta-item">
      <span class="num">4</span>
      <span class="lbl">Matrix Quadrants</span>
    </div>
    <div class="hero-meta-item">
      <span class="num">5</span>
      <span class="lbl">Quiz Questions</span>
    </div>
  </div>
</div>

<!-- NAV -->
<nav class="nav-tabs">
  <a class="nav-tab active" onclick="showSection('basics')">📘 Basics</a>
  <a class="nav-tab" onclick="showSection('types')">📂 3 Types</a>
  <a class="nav-tab" onclick="showSection('process')">⚙️ 7-Step Process</a>
  <a class="nav-tab" onclick="showSection('matrix')">📊 Kraljic Matrix</a>
  <a class="nav-tab" onclick="showSection('pitfalls')">⚠️ Pitfalls</a>
  <a class="nav-tab" onclick="showSection('terms')">📖 Key Terms</a>
  <a class="nav-tab" onclick="showSection('quiz')">🧠 Quiz</a>
</nav>

<!-- ========== SECTION 1: BASICS ========== -->
<section id="basics" class="page-section active">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 1</span>
    <h2 class="section-title">What is Strategic Sourcing?</h2>
    <p class="section-desc">Let's start from the very beginning — understanding what "sourcing" even means, and why it matters.</p>
  </div>

  <div class="analogy">
    <div class="analogy-label">Simple Analogy</div>
    <p><strong>Buying</strong> is like going to a shop and paying for milk. <strong>Strategic sourcing</strong> is like deciding — before you even go — <em>which dairy farm gives the best quality, at the best cost, reliably, for the next 3 years.</em> One is a transaction; the other is a strategy.</p>
  </div>

  <table class="compare-table">
    <thead>
      <tr>
        <th>Aspect</th>
        <th><span class="tag-bad">Buying (Transactional)</span></th>
        <th><span class="tag-good">Strategic Sourcing</span></th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Focus</td><td>Place order, make payment</td><td>Analyse, plan, partner, optimise</td></tr>
      <tr><td>Time Horizon</td><td>Immediate / short-term</td><td>Long-term, continuous</td></tr>
      <tr><td>Supplier Relationship</td><td>One-off or arm's length</td><td>Partnership & collaboration</td></tr>
      <tr><td>Cost View</td><td>Just the price tag</td><td>Total Cost of Ownership (TCO)</td></tr>
      <tr><td>Team Involved</td><td>Only procurement</td><td>Finance, Engineering, Logistics, Marketing</td></tr>
      <tr><td>Data Needed</td><td>Minimal</td><td>Rich, clean spend data</td></tr>
    </tbody>
  </table>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Core Goals</span>
    <h2 class="section-title">What does Strategic Sourcing aim to achieve?</h2>
  </div>

  <div class="concept-grid">
    <div class="concept-card amber">
      <span class="icon">💰</span>
      <h3>Reduce Total Cost of Ownership</h3>
      <p>Not just buying cheap — but considering ALL costs: delivery, maintenance, downtime, quality issues. A cheap part that breaks often is NOT cheap.</p>
    </div>
    <div class="concept-card teal">
      <span class="icon">🤝</span>
      <h3>Better Supplier Relationships</h3>
      <p>Moving from "us vs. them" to genuine partnerships where suppliers help you innovate, reduce waste, and improve quality over time.</p>
    </div>
    <div class="concept-card rose">
      <span class="icon">📉</span>
      <h3>Rationalise the Supplier Base</h3>
      <p>Fewer, stronger supplier relationships = more bargaining power, less complexity, and more focus on what matters.</p>
    </div>
    <div class="concept-card slate">
      <span class="icon">🔄</span>
      <h3>Continuous Improvement</h3>
      <p>Strategic sourcing is never "done." Markets change, prices change, new suppliers emerge — you keep monitoring and improving.</p>
    </div>
  </div>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">History</span>
    <h2 class="section-title">Where did Strategic Sourcing come from?</h2>
  </div>
  <div class="concept-card slate" style="margin-bottom:0;">
    <span class="icon">🏭</span>
    <h3>Born in the 1980s — Western Automotive Industry</h3>
    <p>As competition intensified globally (especially from Japanese manufacturers), Western companies — particularly in automotive — began looking beyond price to cut costs smarter. They started analysing their entire spending, studying supplier markets, and building long-term supply partnerships. Technology like spend analysis tools and classification systems like <strong>UNSPSC</strong> (a product coding system) made this analysis possible at scale. This practice spread worldwide and eventually reached India where it's now growing fast.</p>
  </div>
</div>
</section>

<!-- ========== SECTION 2: TYPES ========== -->
<section id="types" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 2</span>
    <h2 class="section-title">The 3 Types of Sourcing</h2>
    <p class="section-desc">Not all procurement is "strategic." Here's how to tell them apart.</p>
  </div>

  <div class="concept-grid">
    <div class="concept-card rose">
      <span class="icon">🔥</span>
      <h3>1. Reactive Sourcing</h3>
      <p><strong>What it is:</strong> Fire-fighting. Someone needs something NOW and you scramble to find it.<br><br><strong>Characteristics:</strong> No planning, high stress, poor prices, high risk.<br><br><strong>Example:</strong> The factory line has stopped. Buy bolts from whoever has them today — cost doesn't matter.</p>
    </div>
    <div class="concept-card amber">
      <span class="icon">📋</span>
      <h3>2. Tactical Sourcing</h3>
      <p><strong>What it is:</strong> Medium-term arrangements for low-value, low-risk items.<br><br><strong>Characteristics:</strong> Short contracts, some planning, limited analysis.<br><br><strong>Example:</strong> Setting up an annual contract for office stationery with a local vendor.</p>
    </div>
    <div class="concept-card teal">
      <span class="icon">♟️</span>
      <h3>3. Strategic Sourcing</h3>
      <p><strong>What it is:</strong> A structured, analytical, collaborative process for high-value or high-risk categories.<br><br><strong>Characteristics:</strong> Data-driven, cross-functional teams, long-term partnerships, continuous monitoring.<br><br><strong>Example:</strong> A 5-year engineered components supply agreement negotiated after thorough supplier market analysis.</p>
    </div>
  </div>

  <div class="analogy">
    <div class="analogy-label">Quick Memory Trick</div>
    <p>Think of it like health care. <strong>Reactive</strong> = rushing to the emergency room. <strong>Tactical</strong> = annual check-ups. <strong>Strategic sourcing</strong> = a full wellness plan with your doctor — understanding root causes, preventing problems, optimising your long-term health.</p>
  </div>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Key Concept</span>
    <h2 class="section-title">What is Total Cost of Ownership (TCO)?</h2>
  </div>

  <table class="compare-table">
    <thead>
      <tr>
        <th>What you see</th>
        <th>What TCO also includes</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Purchase price: ₹1,000</td><td>Freight / delivery cost</td></tr>
      <tr><td></td><td>Quality inspection costs</td></tr>
      <tr><td></td><td>Rejection / rework costs</td></tr>
      <tr><td></td><td>Storage / inventory costs</td></tr>
      <tr><td></td><td>Maintenance & repairs</td></tr>
      <tr><td></td><td>Downtime if supplier fails</td></tr>
      <tr><td></td><td>Disposal / end-of-life costs</td></tr>
    </tbody>
  </table>
  <p style="color:var(--slate-mid); font-size:0.93rem; margin-top:-16px;">👉 A supplier quoting ₹900 but with frequent rejections and high freight may actually cost MORE than one quoting ₹1,100 with zero defects and free delivery.</p>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Strategy Design</span>
    <h2 class="section-title">Centralised vs. Decentralised Sourcing</h2>
  </div>
  <div class="concept-grid">
    <div class="concept-card teal">
      <span class="icon">🏢</span>
      <h3>Centralised</h3>
      <p>All sourcing decisions come from one central team. Gives <strong>more bargaining power</strong> (buying in bulk), consistent standards, and unified supplier relationships.<br><br><em>Best for:</em> Large companies with common needs across locations.</p>
    </div>
    <div class="concept-card amber">
      <span class="icon">🏘️</span>
      <h3>Decentralised</h3>
      <p>Local teams make their own sourcing decisions. Gives <strong>more flexibility</strong> and faster response to local needs.<br><br><em>Best for:</em> Businesses with very different regional needs or local supply markets.</p>
    </div>
  </div>
</div>
</section>

<!-- ========== SECTION 3: PROCESS ========== -->
<section id="process" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 3</span>
    <h2 class="section-title">The 7-Step Strategic Sourcing Process</h2>
    <p class="section-desc">This is the heart of strategic sourcing. Follow these steps in order — skip one, and the whole process weakens.</p>
  </div>

  <div class="steps">
    <div class="step">
      <div class="step-num">1</div>
      <div class="step-body">
        <h4>Spend Analysis</h4>
        <p>First, understand <em>what</em> you're buying, <em>how much</em> you're spending, and <em>from whom</em>. Group similar items together (called "categories"). This step reveals patterns — like discovering you buy the same bolt from 12 different suppliers at 12 different prices!</p>
        <div class="tip">Clean, accurate data is essential here. Bad data = bad decisions. This is why technology tools and classification systems (like UNSPSC) matter.</div>
      </div>
    </div>
    <div class="step">
      <div class="step-num">2</div>
      <div class="step-body">
        <h4>Supplier Market Assessment</h4>
        <p>Who are the potential suppliers out there? Map the supply market — local, national, global. Understand supplier capabilities, capacities, and financial health. This step tells you if you have 2 or 20 options to choose from.</p>
        <div class="tip">More supplier options = more leverage for you in negotiation.</div>
      </div>
    </div>
    <div class="step">
      <div class="step-num">3</div>
      <div class="step-body">
        <h4>Supply Market Evaluation</h4>
        <p>Go deeper. Study supply & demand dynamics, pricing trends, raw material costs, geopolitical risks. Understand <em>why</em> prices are what they are and where they might go. This is like knowing the weather forecast before planning a trip.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">4</div>
      <div class="step-body">
        <h4>Strategy Building</h4>
        <p>Based on your analysis, decide your approach. Will you consolidate suppliers? Go global? Enter a long-term contract or stay flexible? Will you collaborate deeply with one supplier or maintain competition among several?</p>
        <div class="tip">Different categories need different strategies. High-risk items need different approaches than low-risk commodities.</div>
      </div>
    </div>
    <div class="step">
      <div class="step-num">5</div>
      <div class="step-body">
        <h4>Bidding Process (RFQ / RFP)</h4>
        <p>Issue requests for quotes (RFQ) or proposals (RFP) to shortlisted suppliers. This creates competitive pressure and gives you comparable data. Be clear about your requirements — specs, delivery, quality standards, terms.</p>
        <div class="tip">Unclear RFQs = incomparable bids = poor decisions. Invest time in writing great specifications.</div>
      </div>
    </div>
    <div class="step">
      <div class="step-num">6</div>
      <div class="step-body">
        <h4>Supplier Selection & Negotiation</h4>
        <p>Evaluate bids on total cost (not just price!), quality, reliability, capacity, and fit. Then negotiate — not just on price, but on payment terms, delivery schedules, quality guarantees, and continuous improvement commitments.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">7</div>
      <div class="step-body">
        <h4>Supplier Integration & Continuous Monitoring</h4>
        <p>Onboard the selected supplier properly. Set clear KPIs (Key Performance Indicators). Monitor performance regularly. Build the relationship. And keep scanning the market — because strategic sourcing never truly ends.</p>
        <div class="tip">A good supplier today might not be the best supplier in 3 years. Keep evaluating.</div>
      </div>
    </div>
  </div>

  <div class="section-header" style="margin-top: 48px;">
    <span class="section-tag">Who is involved?</span>
    <h2 class="section-title">Cross-Functional Team</h2>
    <p class="section-desc">Strategic sourcing isn't just a "procurement team" job. It requires everyone who touches the product or service.</p>
  </div>
  <div class="concept-grid">
    <div class="concept-card teal">
      <span class="icon">⚙️</span>
      <h3>Engineering / Technical</h3>
      <p>Defines specifications, evaluates supplier technical capability, drives value engineering.</p>
    </div>
    <div class="concept-card amber">
      <span class="icon">💼</span>
      <h3>Finance</h3>
      <p>Validates cost models, approves budgets, tracks savings, performs should-cost analysis.</p>
    </div>
    <div class="concept-card rose">
      <span class="icon">🚚</span>
      <h3>Logistics / Supply Chain</h3>
      <p>Evaluates freight costs, delivery lead times, inventory impact, and supply continuity.</p>
    </div>
    <div class="concept-card slate">
      <span class="icon">📣</span>
      <h3>Marketing / Business</h3>
      <p>Ensures sourcing decisions align with brand standards, customer expectations, and business strategy.</p>
    </div>
  </div>
</div>
</section>

<!-- ========== SECTION 4: MATRIX ========== -->
<section id="matrix" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 4</span>
    <h2 class="section-title">The Kraljic Matrix</h2>
    <p class="section-desc">A simple but powerful tool to decide <em>how much attention</em> to give each category of items you buy.</p>
  </div>

  <div class="analogy">
    <div class="analogy-label">Simple Analogy</div>
    <p>Imagine you're managing a hospital. You wouldn't treat a common cold the same way you treat a rare heart disease. Similarly, the Kraljic Matrix helps you decide how to treat each category of spend — based on <strong>how much you spend</strong> and <strong>how risky the supply is</strong>.</p>
  </div>

  <div class="matrix-wrap">
    <h3>The Kraljic 2×2 Matrix</h3>
    <div class="matrix-inner">
      <div class="matrix-y-label">↑ Supply Risk (High → Low) ↓</div>
      <div style="flex:1;">
        <div class="matrix-grid">
          <div class="matrix-cell strategic">
            <h4>♟️ Strategic Items</h4>
            <p><strong>High Spend + High Risk</strong><br>E.g., Specialised engine components. Need deep supplier partnerships, joint development, tight monitoring.</p>
          </div>
          <div class="matrix-cell leverage">
            <h4>💪 Leverage Items</h4>
            <p><strong>High Spend + Low Risk</strong><br>E.g., Standard steel. Many suppliers available. Use competitive bidding, consolidate volumes to get best prices.</p>
          </div>
          <div class="matrix-cell bottleneck">
            <h4>🚨 Bottleneck Items</h4>
            <p><strong>Low Spend + High Risk</strong><br>E.g., A rare seal/gasket. Few suppliers. Risk of production stoppage. Build safety stock, find alternatives.</p>
          </div>
          <div class="matrix-cell noncritical">
            <h4>📦 Non-Critical Items</h4>
            <p><strong>Low Spend + Low Risk</strong><br>E.g., Office pens. Automate purchasing, use catalogues, reduce procurement effort here.</p>
          </div>
        </div>
        <div class="matrix-axis">
          <span>← Low Spend</span>
          <span>High Spend →</span>
        </div>
      </div>
    </div>
    <p style="margin-top:16px; font-size:0.87rem; color:var(--slate-mid);">💡 Most of your strategic sourcing effort should go to <strong>Strategic</strong> and <strong>Leverage</strong> quadrants — that's where you get the biggest return on your time.</p>
  </div>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Applying the Matrix</span>
    <h2 class="section-title">What to do in each quadrant?</h2>
  </div>
  <table class="compare-table">
    <thead>
      <tr><th>Quadrant</th><th>Your Goal</th><th>Key Strategy</th></tr>
    </thead>
    <tbody>
      <tr><td>Strategic</td><td>Reduce risk + maximise value</td><td>Deep partnerships, joint innovation, SRM programs</td></tr>
      <tr><td>Leverage</td><td>Reduce cost</td><td>Competitive bidding, volume consolidation, dual sourcing</td></tr>
      <tr><td>Bottleneck</td><td>Secure supply</td><td>Safety stock, alternate supplier development, long-term contracts</td></tr>
      <tr><td>Non-Critical</td><td>Reduce effort & admin</td><td>Catalogues, e-procurement, vendor managed inventory</td></tr>
    </tbody>
  </table>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Balancing Act</span>
    <h2 class="section-title">Competition vs. Collaboration</h2>
    <p class="section-desc">One of the biggest philosophical tensions in strategic sourcing.</p>
  </div>
  <div class="concept-grid">
    <div class="concept-card rose">
      <span class="icon">⚔️</span>
      <h3>Competition</h3>
      <p>Keeping multiple suppliers competing against each other ensures you always get fair prices and aren't held hostage.<br><br><em>Risk:</em> Suppliers won't invest in your relationship or innovate for you if they feel insecure.</p>
    </div>
    <div class="concept-card teal">
      <span class="icon">🤝</span>
      <h3>Collaboration</h3>
      <p>Partnering deeply with fewer suppliers drives innovation, quality, and joint cost reduction.<br><br><em>Risk:</em> Over-dependence on one supplier; reduced competitive pressure on pricing.</p>
    </div>
  </div>
  <p style="margin-top: 8px; color:var(--slate-mid); font-size:0.93rem;">✅ The Kraljic matrix helps you decide <em>which balance</em> is right for each category. Strategic items = collaboration. Leverage items = competition.</p>
</div>
</section>

<!-- ========== SECTION 5: PITFALLS ========== -->
<section id="pitfalls" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 5</span>
    <h2 class="section-title">Common Mistakes & Pitfalls</h2>
    <p class="section-desc">Even well-intentioned organisations fail at strategic sourcing. Here's why — and how to avoid it.</p>
  </div>

  <div class="highlight-box rose">
    <h4>❌ Top Pitfalls to Avoid</h4>
    <ul>
      <li><span><strong>No top management support.</strong> If senior leaders don't champion it, teams won't prioritise it and resources won't be allocated.</span></li>
      <li><span><strong>Poor data quality.</strong> Spend analysis only works with clean, accurate, categorised data. Garbage in = garbage out.</span></li>
      <li><span><strong>Treating it as a one-time exercise.</strong> Strategic sourcing is continuous. Doing it once and forgetting is useless.</span></li>
      <li><span><strong>Skipping market analysis.</strong> Negotiating without understanding the supply market is like bargaining blindfolded.</span></li>
      <li><span><strong>No cross-functional involvement.</strong> Procurement alone can't capture all the value. Engineering, finance, and logistics must all be at the table.</span></li>
      <li><span><strong>Ignoring technology.</strong> Trying to do spend analysis on spreadsheets or manage suppliers without proper tools severely limits impact.</span></li>
      <li><span><strong>Lack of rigour in execution.</strong> Taking shortcuts in the 7-step process produces mediocre results and erodes credibility.</span></li>
    </ul>
  </div>

  <div class="highlight-box amber" style="margin-top:28px;">
    <h4>✅ What Success Looks Like</h4>
    <ul>
      <li><span>CEO / CFO-level commitment and visible support for the programme.</span></li>
      <li><span>A dedicated, empowered cross-functional team with clear accountability.</span></li>
      <li><span>Clean, well-classified spend data updated regularly.</span></li>
      <li><span>Proper technology — spend analytics platforms, e-sourcing tools, SRM systems.</span></li>
      <li><span>Continuous monitoring — quarterly supplier reviews, market price tracking, KPIs.</span></li>
      <li><span>A culture of improvement — always asking "can we do this better?"</span></li>
      <li><span>Savings tracked, reported, and credited back to the business clearly.</span></li>
    </ul>
  </div>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Special Situations</span>
    <h2 class="section-title">What about SMEs? Supplier-dominant markets?</h2>
  </div>
  <div class="concept-grid">
    <div class="concept-card amber">
      <span class="icon">🏪</span>
      <h3>For Small & Medium Enterprises (SMEs)</h3>
      <p>SMEs often lack the volume to have bargaining power alone. Solutions include:<br><br>• <strong>Consortia buying</strong> — join with other SMEs to buy collectively<br>• <strong>Focus on fewer categories</strong> — be strategic where it counts most<br>• <strong>Build strong relationships</strong> — smaller buyers can win with loyalty and reliability</p>
    </div>
    <div class="concept-card rose">
      <span class="icon">🏭</span>
      <h3>When Suppliers Have All the Power</h3>
      <p>In markets with few suppliers (monopoly/oligopoly), traditional competitive bidding doesn't work. Instead:<br><br>• <strong>Partner deeply</strong> — become their preferred customer<br>• <strong>Develop alternate suppliers</strong> — invest in new entrants<br>• <strong>Value engineering</strong> — redesign specs to open up more supply options</p>
    </div>
  </div>

  <div class="section-header" style="margin-top:48px;">
    <span class="section-tag">Measurement</span>
    <h2 class="section-title">How do you measure savings?</h2>
  </div>
  <table class="compare-table">
    <thead>
      <tr><th>Type of Saving</th><th>What it means</th><th>Example</th></tr>
    </thead>
    <tbody>
      <tr><td>Hard Savings</td><td>Real cash out of the budget</td><td>Last year paid ₹100/unit. Now paying ₹85/unit → ₹15 saved per unit</td></tr>
      <tr><td>Cost Avoidance</td><td>Price would have gone up, but you held it</td><td>Supplier wanted 10% increase; you negotiated it to 0%</td></tr>
      <tr><td>Value Add</td><td>Better quality, faster delivery, fewer defects</td><td>Supplier rejection rate drops from 5% to 0.5%</td></tr>
      <tr><td>Process Savings</td><td>Time and admin cost reduced</td><td>Automated ordering saves 10 hours/week of manual work</td></tr>
    </tbody>
  </table>
</div>
</section>

<!-- ========== SECTION 6: TERMS ========== -->
<section id="terms" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 6</span>
    <h2 class="section-title">Key Terms & Definitions</h2>
    <p class="section-desc">Your quick reference glossary — all in plain language.</p>
  </div>

  <div class="terms-grid">
    <div class="term-card">
      <div class="term">Strategic Sourcing</div>
      <div class="def">A structured, analytical, long-term approach to procurement that goes beyond price to optimise total value.</div>
    </div>
    <div class="term-card">
      <div class="term">TCO (Total Cost of Ownership)</div>
      <div class="def">The complete cost of acquiring, using, and disposing of a product — not just its purchase price.</div>
    </div>
    <div class="term-card">
      <div class="term">Spend Analysis</div>
      <div class="def">The process of collecting, cleaning, and analysing spending data to identify patterns and opportunities.</div>
    </div>
    <div class="term-card">
      <div class="term">Kraljic Matrix</div>
      <div class="def">A 2×2 tool that categorises purchased items by spend impact and supply risk to prioritise sourcing strategy.</div>
    </div>
    <div class="term-card">
      <div class="term">UNSPSC</div>
      <div class="def">United Nations Standard Products and Services Code — a global classification system for categorising products and services.</div>
    </div>
    <div class="term-card">
      <div class="term">RFQ / RFP</div>
      <div class="def">Request for Quotation / Request for Proposal — formal documents sent to suppliers asking for price or solution bids.</div>
    </div>
    <div class="term-card">
      <div class="term">SRM (Supplier Relationship Management)</div>
      <div class="def">A systematic approach to managing interactions with suppliers to maximise mutual value and minimise risk.</div>
    </div>
    <div class="term-card">
      <div class="term">Cross-Functional Team</div>
      <div class="def">A group of people from different departments (procurement, finance, engineering, etc.) working together on sourcing decisions.</div>
    </div>
    <div class="term-card">
      <div class="term">Value Engineering</div>
      <div class="def">Redesigning a product or specification to achieve the same function at a lower cost, often done with supplier input.</div>
    </div>
    <div class="term-card">
      <div class="term">Value Analysis</div>
      <div class="def">Reviewing an existing product or process to eliminate unnecessary costs while maintaining required quality and function.</div>
    </div>
    <div class="term-card">
      <div class="term">Should-Cost Analysis</div>
      <div class="def">A method to estimate what a product or service should cost based on its raw materials, labour, and overhead — used in negotiation.</div>
    </div>
    <div class="term-card">
      <div class="term">Supplier Rationalisation</div>
      <div class="def">Reducing the number of suppliers to consolidate spend with fewer, stronger partners — improving leverage and reducing complexity.</div>
    </div>
    <div class="term-card">
      <div class="term">CPSM</div>
      <div class="def">Certified Professional in Supply Management — a globally recognised procurement qualification (ISM, USA).</div>
    </div>
    <div class="term-card">
      <div class="term">CPIM</div>
      <div class="def">Certified in Planning and Inventory Management — focuses more on production planning & inventory, less on sourcing strategy.</div>
    </div>
    <div class="term-card">
      <div class="term">KPI</div>
      <div class="def">Key Performance Indicator — measurable targets used to track supplier performance (e.g., on-time delivery rate, defect rate).</div>
    </div>
  </div>

  <div class="summary-card">
    <h3>🧠 The Big Picture — In One Paragraph</h3>
    <div class="summary-points">
      <div class="summary-point">
        <span class="num">→</span>
        <span>Strategic sourcing is about moving from reactive, price-only buying to a disciplined, data-driven process that considers total cost, supplier relationships, and market intelligence — all working together through cross-functional teams — to create real, measurable, and sustained value for your organisation.</span>
      </div>
    </div>
  </div>
</div>
</section>

<!-- ========== SECTION 7: QUIZ ========== -->
<section id="quiz" class="page-section">
<div class="container">
  <div class="section-header">
    <span class="section-tag">Module 7</span>
    <h2 class="section-title">Test Your Knowledge</h2>
    <p class="section-desc">Five quick questions to check your understanding. Click an option to see if you got it right!</p>
  </div>

  <!-- Q1 -->
  <div class="quiz-block">
    <div class="q-label">Question 1 of 5</div>
    <div class="question">What is the key difference between "buying" and "strategic sourcing"?</div>
    <div class="options">
      <div class="option" onclick="answer(this, false, 'q1')"><span class="opt-letter">A</span> Buying uses money; strategic sourcing uses credit</div>
      <div class="option" onclick="answer(this, true, 'q1')"><span class="opt-letter">B</span> Buying is transactional; strategic sourcing is analytical, long-term, and value-focused</div>
      <div class="option" onclick="answer(this, false, 'q1')"><span class="opt-letter">C</span> Strategic sourcing only works for large companies</div>
      <div class="option" onclick="answer(this, false, 'q1')"><span class="opt-letter">D</span> They mean the same thing</div>
    </div>
    <div class="quiz-feedback" id="q1-feedback"></div>
  </div>

  <!-- Q2 -->
  <div class="quiz-block">
    <div class="q-label">Question 2 of 5</div>
    <div class="question">In the Kraljic Matrix, which quadrant should receive the most strategic attention and deepest supplier partnerships?</div>
    <div class="options">
      <div class="option" onclick="answer(this, false, 'q2')"><span class="opt-letter">A</span> Non-Critical Items</div>
      <div class="option" onclick="answer(this, false, 'q2')"><span class="opt-letter">B</span> Leverage Items</div>
      <div class="option" onclick="answer(this, true, 'q2')"><span class="opt-letter">C</span> Strategic Items (High Spend + High Risk)</div>
      <div class="option" onclick="answer(this, false, 'q2')"><span class="opt-letter">D</span> Bottleneck Items</div>
    </div>
    <div class="quiz-feedback" id="q2-feedback"></div>
  </div>

  <!-- Q3 -->
  <div class="quiz-block">
    <div class="q-label">Question 3 of 5</div>
    <div class="question">What does TCO stand for, and why does it matter?</div>
    <div class="options">
      <div class="option" onclick="answer(this, false, 'q3')"><span class="opt-letter">A</span> Total Contract Output — it measures how many contracts you sign</div>
      <div class="option" onclick="answer(this, false, 'q3')"><span class="opt-letter">B</span> Trade Cost Override — it overrides the quoted price</div>
      <div class="option" onclick="answer(this, true, 'q3')"><span class="opt-letter">C</span> Total Cost of Ownership — it captures all costs (delivery, quality, maintenance) not just purchase price</div>
      <div class="option" onclick="answer(this, false, 'q3')"><span class="opt-letter">D</span> Tier Cost Organisation — it organises supplier tiers</div>
    </div>
    <div class="quiz-feedback" id="q3-feedback"></div>
  </div>

  <!-- Q4 -->
  <div class="quiz-block">
    <div class="q-label">Question 4 of 5</div>
    <div class="question">Which is the FIRST step in the strategic sourcing 7-step process?</div>
    <div class="options">
      <div class="option" onclick="answer(this, false, 'q4')"><span class="opt-letter">A</span> Bidding Process (RFQ)</div>
      <div class="option" onclick="answer(this, false, 'q4')"><span class="opt-letter">B</span> Supplier Selection & Negotiation</div>
      <div class="option" onclick="answer(this, true, 'q4')"><span class="opt-letter">C</span> Spend Analysis</div>
      <div class="option" onclick="answer(this, false, 'q4')"><span class="opt-letter">D</span> Strategy Building</div>
    </div>
    <div class="quiz-feedback" id="q4-feedback"></div>
  </div>

  <!-- Q5 -->
  <div class="quiz-block">
    <div class="q-label">Question 5 of 5</div>
    <div class="question">What is a major reason strategic sourcing programmes fail?</div>
    <div class="options">
      <div class="option" onclick="answer(this, false, 'q5')"><span class="opt-letter">A</span> Too many suppliers available in the market</div>
      <div class="option" onclick="answer(this, false, 'q5')"><span class="opt-letter">B</span> It is too expensive to implement</div>
      <div class="option" onclick="answer(this, true, 'q5')"><span class="opt-letter">C</span> Lack of top management support, poor data quality, and treating it as a one-time exercise</div>
      <div class="option" onclick="answer(this, false, 'q5')"><span class="opt-letter">D</span> Procurement teams are too experienced</div>
    </div>
    <div class="quiz-feedback" id="q5-feedback"></div>
  </div>

  <div class="summary-card" style="margin-top:48px;">
    <h3>🎓 Well Done!</h3>
    <div class="summary-points">
      <div class="summary-point"><span class="num">1</span><span>Strategic sourcing is an analytical, long-term, collaborative approach — not just price bargaining.</span></div>
      <div class="summary-point"><span class="num">2</span><span>Always think in terms of Total Cost of Ownership, not just quoted price.</span></div>
      <div class="summary-point"><span class="num">3</span><span>Use the Kraljic Matrix to prioritise where to focus your energy.</span></div>
      <div class="summary-point"><span class="num">4</span><span>Follow all 7 steps — don't cut corners. The process is designed for a reason.</span></div>
      <div class="summary-point"><span class="num">5</span><span>Success requires clean data, cross-functional teams, technology, and top management support.</span></div>
      <div class="summary-point"><span class="num">6</span><span>Strategic sourcing is continuous — it never truly ends. Keep monitoring and improving.</span></div>
    </div>
  </div>
</div>
</section>

<script>
  const feedbackMessages = {
    correct: "✅ Correct! Well done.",
    wrong: "❌ Not quite. Review the section and try to recall the correct concept."
  };

  function answer(el, isCorrect, qId) {
    const parent = el.parentElement;
    if (parent.querySelector('.correct') || parent.querySelector('.wrong')) return; // already answered
    
    el.classList.add(isCorrect ? 'correct' : 'wrong');
    
    if (!isCorrect) {
      // highlight the correct one
      const opts = parent.querySelectorAll('.option');
      opts.forEach(opt => {
        if (opt !== el) {
          // find correct by re-checking onclick
          const fn = opt.getAttribute('onclick');
          if (fn && fn.includes('true')) opt.classList.add('correct');
        }
      });
    }
    
    const fb = document.getElementById(qId + '-feedback');
    fb.textContent = isCorrect ? feedbackMessages.correct : feedbackMessages.wrong;
    fb.className = 'quiz-feedback show ' + (isCorrect ? 'correct-fb' : 'wrong-fb');
  }

  function showSection(id) {
    document.querySelectorAll('.page-section').forEach(s => s.classList.remove('active'));
    document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    event.target.classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
</script>
</body>
</html>
