<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>DSA Assignment 3 — Stacks & Queues</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Mono:ital,wght@0,300;0,400;0,500;1,400&family=Lora:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet"/>
<style>
  :root {
    --amber:   #F59E0B;
    --amber2:  #FBBF24;
    --fire:    #EF4444;
    --dark:    #0F0E0C;
    --surface: #1A1916;
    --card:    #211F1B;
    --border:  #2E2B24;
    --muted:   #6B6456;
    --light:   #E8E0D0;
    --white:   #FAF7F2;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--dark);
    color: var(--light);
    font-family: 'Lora', Georgia, serif;
    font-size: 16px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NOISE OVERLAY ── */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
    background-size: 200px 200px;
    pointer-events: none;
    z-index: 0;
  }

  /* ── SCROLLBAR ── */
  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: var(--dark); }
  ::-webkit-scrollbar-thumb { background: var(--amber); border-radius: 3px; }

  /* ── LAYOUT ── */
  .container { max-width: 1060px; margin: 0 auto; padding: 0 2rem; position: relative; z-index: 1; }

  /* ── HEADER ── */
  header {
    position: relative;
    padding: 5rem 0 4rem;
    overflow: hidden;
  }

  .header-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 70% 50%, rgba(245,158,11,0.12) 0%, transparent 70%),
      radial-gradient(ellipse 40% 80% at 10% 20%, rgba(239,68,68,0.08) 0%, transparent 60%);
    z-index: 0;
  }

  .header-rule {
    width: 3px; height: 80px;
    background: linear-gradient(to bottom, var(--fire), var(--amber));
    margin-bottom: 2rem;
    animation: grow-down 1s ease forwards;
  }

  @keyframes grow-down {
    from { height: 0; opacity: 0; }
    to   { height: 80px; opacity: 1; }
  }

  .course-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--amber);
    margin-bottom: 1rem;
    opacity: 0;
    animation: fade-up 0.6s 0.3s ease forwards;
  }

  h1.hero-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(3.2rem, 9vw, 7.5rem);
    line-height: 0.92;
    letter-spacing: 0.02em;
    color: #FF69B4;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fade-up 0.7s 0.5s ease forwards;
  }

  h1.hero-title span.accent {
    color: #FF1493;
    -webkit-text-stroke: 1px #FF1493;
  }

  .hero-meta {
    display: flex;
    gap: 3rem;
    align-items: center;
    flex-wrap: wrap;
    opacity: 0;
    animation: fade-up 0.7s 0.7s ease forwards;
  }

  .meta-item { display: flex; flex-direction: column; gap: 0.15rem; }
  .meta-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
  }
  .meta-value {
    font-family: 'DM Mono', monospace;
    font-size: 0.95rem;
    color: var(--amber2);
  }

  .header-divider {
    height: 1px;
    background: linear-gradient(to right, var(--amber), var(--fire), transparent);
    margin: 3rem 0 0;
    opacity: 0;
    animation: fade-in 1s 1s ease forwards;
  }

  @keyframes fade-up {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes fade-in {
    to { opacity: 1; }
  }

  /* ── TOC ── */
  .toc-section { padding: 3rem 0; }

  .toc-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .toc-item {
    background: var(--card);
    padding: 1.4rem 1.6rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    color: var(--light);
    transition: background 0.2s, color 0.2s;
    position: relative;
    overflow: hidden;
  }

  .toc-item::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0;
    width: 0; height: 2px;
    background: var(--amber);
    transition: width 0.3s ease;
  }

  .toc-item:hover { background: #27241E; color: var(--amber2); }
  .toc-item:hover::after { width: 100%; }

  .toc-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 2.2rem;
    color: #FF69B4;
    line-height: 1;
    min-width: 2.2rem;
  }

  .toc-text { font-size: 0.88rem; line-height: 1.35; }
  .toc-text strong { display: block; font-family: 'DM Mono', monospace; font-weight: 500; font-size: 0.82rem; }

  /* ── SECTION WRAPPER ── */
  .section {
    padding: 4rem 0;
    border-bottom: 1px solid var(--border);
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .section.visible { opacity: 1; transform: none; }

  /* ── SECTION HEADERS ── */
  .section-header {
    display: flex;
    align-items: flex-end;
    gap: 1.2rem;
    margin-bottom: 2.5rem;
  }

  .section-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 5rem;
    line-height: 1;
    color: var(--border);
    user-select: none;
    transition: color 0.3s;
  }
  .section:hover .section-num { color: var(--amber); }

  .section-title-wrap { flex: 1; }

  h2.section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    letter-spacing: 0.04em;
    color: #FF69B4;
    line-height: 1;
  }

  .section-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--fire);
  }

  /* ── SUBSECTION ── */
  h3.sub-title {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #FF69B4;
    margin-bottom: 0.8rem;
    margin-top: 2.2rem;
  }
  h3.sub-title:first-of-type { margin-top: 0; }

  p { margin-bottom: 1rem; color: #C9C0B0; }

  /* ── CALLOUT ── */
  .callout {
    border-left: 3px solid var(--amber);
    background: rgba(245,158,11,0.06);
    padding: 1rem 1.4rem;
    margin: 1.5rem 0;
    font-style: italic;
    color: #D4C9B5;
    border-radius: 0 4px 4px 0;
  }

  .callout-fire {
    border-left-color: var(--fire);
    background: rgba(239,68,68,0.06);
  }

  /* ── PILL BADGES ── */
  .badges { display: flex; flex-wrap: wrap; gap: 0.6rem; margin: 1rem 0; }
  .badge {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    padding: 0.3rem 0.8rem;
    border-radius: 2px;
    font-weight: 500;
    letter-spacing: 0.05em;
  }
  .badge-amber { background: rgba(245,158,11,0.15); color: var(--amber2); border: 1px solid rgba(245,158,11,0.3); }
  .badge-fire  { background: rgba(239,68,68,0.12); color: #FC8181; border: 1px solid rgba(239,68,68,0.3); }
  .badge-green { background: rgba(52,211,153,0.1); color: #6EE7B7; border: 1px solid rgba(52,211,153,0.25); }

  /* ── TABLES ── */
  .table-wrap { overflow-x: auto; margin: 1.5rem 0; }
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.875rem;
  }
  thead tr { background: rgba(245,158,11,0.12); }
  thead th {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--amber);
    padding: 0.85rem 1rem;
    text-align: left;
    border-bottom: 2px solid var(--amber);
  }
  tbody tr { border-bottom: 1px solid var(--border); transition: background 0.15s; }
  tbody tr:hover { background: rgba(255,255,255,0.03); }
  tbody td {
    padding: 0.8rem 1rem;
    color: #C9C0B0;
    vertical-align: top;
  }
  tbody td:first-child {
    font-family: 'DM Mono', monospace;
    font-size: 0.82rem;
    color: var(--amber2);
  }

  /* ── CODE BLOCKS ── */
  .code-wrap {
    position: relative;
    margin: 1.5rem 0;
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
  }

  .code-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #161410;
    padding: 0.6rem 1rem;
    border-bottom: 1px solid var(--border);
  }

  .code-lang {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .code-dots { display: flex; gap: 6px; }
  .code-dots span {
    width: 10px; height: 10px;
    border-radius: 50%;
  }
  .dot-r { background: #EF4444; }
  .dot-y { background: #F59E0B; }
  .dot-g { background: #22C55E; }

  pre {
    background: #0D0C0A;
    padding: 1.4rem 1.2rem;
    overflow-x: auto;
    margin: 0;
  }
  code {
    font-family: 'DM Mono', monospace;
    font-size: 0.82rem;
    line-height: 1.75;
    color: #D4C5A9;
  }

  /* syntax-like colouring via spans */
  .kw  { color: #F59E0B; }   /* keywords */
  .ty  { color: #FB923C; }   /* types */
  .fn  { color: #FCD34D; }   /* functions */
  .cm  { color: #4B5563; font-style: italic; } /* comments */
  .st  { color: #86EFAC; }   /* strings */
  .nm  { color: #93C5FD; }   /* numbers */
  .op  { color: #C084FC; }   /* operators */

  /* ── DRY-RUN TRACE ── */
  .trace-block {
    background: #0D0C0A;
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    margin: 1.5rem 0;
  }
  .trace-header {
    background: #161410;
    padding: 0.55rem 1rem;
    border-bottom: 1px solid var(--border);
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
  }
  .trace-row {
    display: grid;
    grid-template-columns: 1fr auto 1.4fr;
    gap: 0;
    border-bottom: 1px solid rgba(46,43,36,0.5);
    align-items: center;
    padding: 0.55rem 1rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.82rem;
    transition: background 0.15s;
  }
  .trace-row:hover { background: rgba(245,158,11,0.04); }
  .trace-row:last-child { border-bottom: none; }
  .trace-op   { color: var(--amber2); }
  .trace-arr  { color: var(--muted); font-size: 0.7rem; text-align: center; }
  .trace-state { color: #C9C0B0; }
  .trace-ret  { color: #86EFAC; font-size: 0.75rem; }

  /* ── CONCEPT CARDS ── */
  .concept-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0;
  }

  .concept-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1.4rem;
    transition: border-color 0.2s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }
  .concept-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 2px;
    background: linear-gradient(to right, var(--amber), var(--fire));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }
  .concept-card:hover { border-color: rgba(245,158,11,0.4); transform: translateY(-2px); }
  .concept-card:hover::before { transform: scaleX(1); }

  .concept-icon {
    font-size: 1.8rem;
    margin-bottom: 0.8rem;
    display: block;
  }
  .concept-card h4 {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #FF69B4;
    margin-bottom: 0.5rem;
  }
  .concept-card p {
    font-size: 0.85rem;
    color: #A89F90;
    margin: 0;
    line-height: 1.5;
  }

  /* ── LIFO / FIFO Visual ── */
  .principle-visual {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    flex-wrap: wrap;
    margin: 1.5rem 0;
  }

  .stack-viz {
    display: flex;
    flex-direction: column;
    gap: 3px;
    align-items: center;
  }

  .stack-viz-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 0.5rem;
  }

  .stack-block {
    width: 90px;
    padding: 0.4rem;
    text-align: center;
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    border-radius: 2px;
    transition: all 0.3s;
  }
  .sb-top    { background: rgba(239,68,68,0.2); border: 1px solid rgba(239,68,68,0.5); color: #FC8181; }
  .sb-mid    { background: rgba(245,158,11,0.12); border: 1px solid rgba(245,158,11,0.3); color: var(--amber2); }
  .sb-bottom { background: rgba(30,27,22,0.8); border: 1px solid var(--border); color: var(--muted); }

  .arrow-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    color: var(--fire);
    text-align: center;
    margin-bottom: 0.3rem;
  }

  .queue-viz {
    display: flex;
    gap: 3px;
    align-items: center;
    flex-wrap: wrap;
  }

  .queue-block {
    padding: 0.5rem 0.8rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    border-radius: 2px;
    border: 1px solid var(--border);
    color: var(--muted);
    background: var(--card);
  }
  .qb-front { background: rgba(239,68,68,0.15); border-color: rgba(239,68,68,0.4); color: #FC8181; }
  .qb-rear  { background: rgba(245,158,11,0.12); border-color: rgba(245,158,11,0.35); color: var(--amber2); }

  .viz-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--fire);
  }

  /* ── OVERFLOW / UNDERFLOW ── */
  .error-cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin: 1.5rem 0;
  }
  @media (max-width: 540px) { .error-cards { grid-template-columns: 1fr; } }

  .error-card {
    padding: 1.2rem;
    border-radius: 4px;
    border: 1px solid;
  }
  .err-overflow { border-color: rgba(239,68,68,0.4); background: rgba(239,68,68,0.07); }
  .err-underflow { border-color: rgba(251,191,36,0.35); background: rgba(251,191,36,0.06); }
  .error-card h4 {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 0.5rem;
  }
  .err-overflow h4 { color: #FC8181; }
  .err-underflow h4 { color: var(--amber2); }
  .error-card p { font-size: 0.85rem; color: #A89F90; margin: 0; line-height: 1.5; }

  /* ── ALGO STEPS ── */
  .algo-steps { list-style: none; margin: 1rem 0 1.5rem; }
  .algo-steps li {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    padding: 0.7rem 0;
    border-bottom: 1px dashed var(--border);
    font-size: 0.9rem;
    color: #C9C0B0;
  }
  .algo-steps li:last-child { border-bottom: none; }
  .step-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.5rem;
    color: var(--amber);
    line-height: 1;
    min-width: 1.5rem;
  }

  /* ── FOOTER ── */
  footer {
    padding: 3rem 0;
    text-align: center;
  }
  .footer-rule {
    height: 1px;
    background: linear-gradient(to right, transparent, var(--amber), var(--fire), transparent);
    margin-bottom: 2rem;
  }
  .footer-text {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
  }
  .footer-text span { color: var(--amber); }

  /* ── RESPONSIVE ── */
  @media (max-width: 680px) {
    .trace-row { grid-template-columns: 1fr auto; }
    .trace-state { display: none; }
    .section-num { font-size: 3rem; }
  }
</style>
</head>
<body>

<!-- ═══════════ HEADER ═══════════ -->
<header>
  <div class="header-bg"></div>
  <div class="container" style="position:relative;z-index:1;">
    <div class="header-rule"></div>
    <p class="course-tag">Department of Artificial Intelligence &nbsp;·&nbsp; Data Structures &amp; Algorithms</p>
    <h1 class="hero-title">STACKS<br><span class="accent">&amp; QUEUES</span></h1>
    <div class="hero-meta">
      <div class="meta-item">
        <span class="meta-label">Assignment</span>
        <span class="meta-value">DSA — 03</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Student Name</span>
        <span class="meta-value">Ayesha Javaid</span>
      </div>
      <div class="meta-item">
        <span class="meta-label">Student ID</span>
        <span class="meta-value">s2025376102</span>
      </div>
    </div>
    <div class="header-divider"></div>
  </div>
</header>

<!-- ═══════════ TABLE OF CONTENTS ═══════════ -->
<div class="container">
  <div class="toc-section">
    <div class="toc-grid">
      <a class="toc-item" href="#q1">
        <span class="toc-num">01</span>
        <div class="toc-text"><strong>Stack Theory</strong>LIFO, operations, overflow &amp; underflow</div>
      </a>
      <a class="toc-item" href="#q2">
        <span class="toc-num">02</span>
        <div class="toc-text"><strong>Stack Implementation</strong>Array &amp; Linked List in C++</div>
      </a>
      <a class="toc-item" href="#q3">
        <span class="toc-num">03</span>
        <div class="toc-text"><strong>Balanced Brackets</strong>Stack-based bracket checker</div>
      </a>
      <a class="toc-item" href="#q4">
        <span class="toc-num">04</span>
        <div class="toc-text"><strong>Queue Theory</strong>FIFO, operations, circular queue</div>
      </a>
      <a class="toc-item" href="#q5">
        <span class="toc-num">05</span>
        <div class="toc-text"><strong>Queue Implementation</strong>Linked List &amp; Circular Array</div>
      </a>
      <a class="toc-item" href="#q6">
        <span class="toc-num">06</span>
        <div class="toc-text"><strong>Postfix Evaluator</strong>Stack-based expression evaluation</div>
      </a>
    </div>
  </div>
</div>

<!-- ═══════════ Q1 — STACK THEORY ═══════════ -->
<div class="container">
<section class="section" id="q1">
  <div class="section-header">
    <span class="section-num">01</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 1</p>
      <h2 class="section-title">Stack Theory</h2>
    </div>
  </div>

  <h3 class="sub-title">What is a Stack?</h3>
  <p>A stack is a linear data structure in which insertion and deletion happen from one side only — called the <strong style="color:var(--amber2)">top</strong>. It follows the <strong style="color:var(--amber2)">LIFO</strong> principle: <em>Last In, First Out</em>. The item added last is the first one removed.</p>

  <div class="principle-visual">
    <div class="stack-viz">
      <div class="stack-viz-label">Stack (LIFO)</div>
      <div class="arrow-label">↑ push / pop ↑</div>
      <div class="stack-block sb-top">30 ← top</div>
      <div class="stack-block sb-mid">20</div>
      <div class="stack-block sb-bottom">10</div>
    </div>
    <div>
      <div class="badges">
        <span class="badge badge-amber">Stack of Plates</span>
        <span class="badge badge-amber">Browser Back Button</span>
        <span class="badge badge-amber">Undo Feature</span>
        <span class="badge badge-amber">Function Call Stack</span>
      </div>
      <p style="font-size:0.88rem;color:#A89F90;margin-top:0.5rem;">Real-life examples of LIFO behaviour. The last plate placed on the pile is the first one taken off.</p>
    </div>
  </div>

  <h3 class="sub-title">Core Stack Operations</h3>
  <div class="table-wrap">
    <table>
      <thead>
        <tr>
          <th>Operation</th>
          <th>Description</th>
          <th>Time Complexity</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>push()</td><td>Inserts an element into the stack at the top</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>pop()</td><td>Removes the top element from the stack</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>peek()</td><td>Returns the top element without removing it</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>isEmpty()</td><td>Checks whether the stack contains elements</td><td><span class="badge badge-green">O(1)</span></td></tr>
      </tbody>
    </table>
  </div>
  <p>All operations run in <strong style="color:var(--amber2)">O(1)</strong> time because they only access the top position.</p>

  <h3 class="sub-title">Stack Overflow vs. Stack Underflow</h3>
  <div class="error-cards">
    <div class="error-card err-overflow">
      <h4>⚠ Stack Overflow</h4>
      <p>Happens when we try to <strong>push</strong> into a <em>full</em> stack. The stack has no room for new elements.</p>
    </div>
    <div class="error-card err-underflow">
      <h4>⚠ Stack Underflow</h4>
      <p>Happens when we try to <strong>pop</strong> from an <em>empty</em> stack. There is nothing to remove.</p>
    </div>
  </div>
  <div class="callout">A good implementation should print proper error messages and stop the invalid operation safely.</div>

  <h3 class="sub-title">Array vs. Linked List Implementation</h3>
  <div class="table-wrap">
    <table>
      <thead>
        <tr><th>Feature</th><th>Array</th><th>Linked List</th></tr>
      </thead>
      <tbody>
        <tr><td>Memory</td><td>Fixed, pre-allocated</td><td>Dynamic, grows as needed</td></tr>
        <tr><td>Flexibility</td><td>Cannot grow after declaration</td><td>Can grow when needed</td></tr>
        <tr><td>Speed</td><td>Generally faster</td><td>Slightly slower</td></tr>
        <tr><td>Overhead</td><td>None</td><td>Extra pointer per node</td></tr>
      </tbody>
    </table>
  </div>
  <p>Arrays are usually <strong style="color:var(--amber2)">faster</strong>; linked lists are more <strong style="color:var(--amber2)">flexible</strong>.</p>

  <h3 class="sub-title">Dry Run Trace</h3>
  <div class="trace-block">
    <div class="trace-header">Operations &amp; Stack State</div>
    <div class="trace-row"><span class="trace-op">push(10)</span><span class="trace-arr">→</span><span class="trace-state">[10]</span></div>
    <div class="trace-row"><span class="trace-op">push(20)</span><span class="trace-arr">→</span><span class="trace-state">[10, 20]</span></div>
    <div class="trace-row"><span class="trace-op">push(5)</span><span class="trace-arr">→</span><span class="trace-state">[10, 20, 5]</span></div>
    <div class="trace-row"><span class="trace-op">pop() <span class="trace-ret">returns 5</span></span><span class="trace-arr">→</span><span class="trace-state">[10, 20]</span></div>
    <div class="trace-row"><span class="trace-op">peek() <span class="trace-ret">returns 20</span></span><span class="trace-arr">→</span><span class="trace-state">[10, 20]</span></div>
    <div class="trace-row"><span class="trace-op">push(30)</span><span class="trace-arr">→</span><span class="trace-state">[10, 20, 30]</span></div>
    <div class="trace-row"><span class="trace-op">pop() <span class="trace-ret">returns 30</span></span><span class="trace-arr">→</span><span class="trace-state">[10, 20]</span></div>
    <div class="trace-row"><span class="trace-op">pop() <span class="trace-ret">returns 20</span></span><span class="trace-arr">→</span><span class="trace-state">[10]</span></div>
  </div>
</section>

<!-- ═══════════ Q2 — STACK IMPLEMENTATION ═══════════ -->
<section class="section" id="q2">
  <div class="section-header">
    <span class="section-num">02</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 2</p>
      <h2 class="section-title">Stack Implementation</h2>
    </div>
  </div>

  <p>Both an <strong style="color:var(--amber2)">array-based</strong> and a <strong style="color:var(--amber2)">linked list-based</strong> stack are implemented below, followed by a <code style="font-family:'DM Mono',monospace;color:var(--amber2);font-size:0.85rem;">main()</code> driver to demonstrate their behaviour.</p>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><span class="dot-r"></span><span class="dot-y"></span><span class="dot-g"></span></div>
      <span class="code-lang">C++ &nbsp;·&nbsp; Array Stack &amp; Linked List Stack</span>
    </div>
    <pre><code><span class="kw">#include</span><span class="st">&lt;iostream&gt;</span>
<span class="kw">using namespace</span> std;

<span class="cm">// ─── Array-Based Stack ───────────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">Stack</span>{
    <span class="ty">int</span> arr[<span class="nm">10</span>];
    <span class="ty">int</span> top;

    <span class="kw">public</span>:
    <span class="fn">Stack</span>(){ top = <span class="op">-</span><span class="nm">1</span>; }

    <span class="ty">bool</span> <span class="fn">isEmpty</span>(){ <span class="kw">return</span> top == <span class="op">-</span><span class="nm">1</span>; }
    <span class="ty">bool</span> <span class="fn">isFull</span>(){  <span class="kw">return</span> top == <span class="nm">9</span>;  }

    <span class="ty">void</span> <span class="fn">push</span>(<span class="ty">int</span> val){
        <span class="kw">if</span>(<span class="fn">isFull</span>()){ cout&lt;&lt;<span class="st">"Stack Overflow"</span>&lt;&lt;endl; <span class="kw">return</span>; }
        arr[<span class="op">++</span>top] = val;
    }

    <span class="ty">int</span> <span class="fn">pop</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Stack Underflow"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="kw">return</span> arr[top<span class="op">--</span>];
    }

    <span class="ty">int</span> <span class="fn">peek</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Stack is Empty"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="kw">return</span> arr[top];
    }

    <span class="ty">void</span> <span class="fn">display</span>(){
        <span class="kw">for</span>(<span class="ty">int</span> i=top; i&gt;=<span class="nm">0</span>; i<span class="op">--</span>) cout&lt;&lt;arr[i]&lt;&lt;<span class="st">" "</span>;
        cout&lt;&lt;endl;
    }
};

<span class="cm">// ─── Linked List Node ─────────────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">Node</span>{
    <span class="kw">public</span>:
    <span class="ty">int</span>   data;
    <span class="ty">Node</span><span class="op">*</span> next;
    <span class="fn">Node</span>(<span class="ty">int</span> val){ data = val; next = <span class="kw">NULL</span>; }
};

<span class="cm">// ─── Linked List-Based Stack ──────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">StackLL</span>{
    <span class="ty">Node</span><span class="op">*</span> top;

    <span class="kw">public</span>:
    <span class="fn">StackLL</span>(){ top = <span class="kw">NULL</span>; }

    <span class="ty">bool</span> <span class="fn">isEmpty</span>(){ <span class="kw">return</span> top == <span class="kw">NULL</span>; }

    <span class="ty">void</span> <span class="fn">push</span>(<span class="ty">int</span> val){
        <span class="ty">Node</span><span class="op">*</span> newNode = <span class="kw">new</span> <span class="fn">Node</span>(val);
        newNode<span class="op">-&gt;</span>next = top;
        top = newNode;
    }

    <span class="ty">int</span> <span class="fn">pop</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Stack Underflow"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="ty">int</span> value = top<span class="op">-&gt;</span>data;
        <span class="ty">Node</span><span class="op">*</span> temp = top;
        top = top<span class="op">-&gt;</span>next;
        <span class="kw">delete</span> temp;
        <span class="kw">return</span> value;
    }

    <span class="ty">int</span> <span class="fn">peek</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Stack is Empty"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="kw">return</span> top<span class="op">-&gt;</span>data;
    }

    <span class="ty">void</span> <span class="fn">display</span>(){
        <span class="ty">Node</span><span class="op">*</span> temp = top;
        <span class="kw">while</span>(temp != <span class="kw">NULL</span>){ cout&lt;&lt;temp<span class="op">-&gt;</span>data&lt;&lt;<span class="st">" "</span>; temp = temp<span class="op">-&gt;</span>next; }
        cout&lt;&lt;endl;
    }
};

<span class="cm">// ─── Driver ───────────────────────────────────────────────────</span>
<span class="ty">int</span> <span class="fn">main</span>(){
    <span class="ty">Stack</span>   s1;
    <span class="ty">StackLL</span> s2;

    s1.<span class="fn">push</span>(<span class="nm">10</span>); s1.<span class="fn">push</span>(<span class="nm">20</span>); s1.<span class="fn">push</span>(<span class="nm">30</span>); s1.<span class="fn">push</span>(<span class="nm">40</span>); s1.<span class="fn">push</span>(<span class="nm">50</span>);
    s2.<span class="fn">push</span>(<span class="nm">10</span>); s2.<span class="fn">push</span>(<span class="nm">20</span>); s2.<span class="fn">push</span>(<span class="nm">30</span>); s2.<span class="fn">push</span>(<span class="nm">40</span>); s2.<span class="fn">push</span>(<span class="nm">50</span>);

    cout&lt;&lt;<span class="st">"Array Stack:"</span>&lt;&lt;endl;    s1.<span class="fn">display</span>();
    cout&lt;&lt;<span class="st">"Linked List Stack:"</span>&lt;&lt;endl; s2.<span class="fn">display</span>();

    s1.<span class="fn">pop</span>(); s1.<span class="fn">pop</span>();
    s2.<span class="fn">pop</span>(); s2.<span class="fn">pop</span>();

    cout&lt;&lt;<span class="st">"After popping:"</span>&lt;&lt;endl;
    s1.<span class="fn">display</span>(); s2.<span class="fn">display</span>();

    cout&lt;&lt;<span class="st">"Peek Value: "</span>&lt;&lt;s1.<span class="fn">peek</span>()&lt;&lt;endl;
    <span class="kw">return</span> <span class="nm">0</span>;
}</code></pre>
  </div>
</section>

<!-- ═══════════ Q3 — BALANCED BRACKETS ═══════════ -->
<section class="section" id="q3">
  <div class="section-header">
    <span class="section-num">03</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 3</p>
      <h2 class="section-title">Balanced Brackets Checker</h2>
    </div>
  </div>

  <h3 class="sub-title">Algorithm</h3>
  <ol class="algo-steps">
    <li><span class="step-num">1</span><span>The stack stores <strong style="color:var(--amber2)">opening brackets</strong> as they are encountered.</span></li>
    <li><span class="step-num">2</span><span>If a <strong style="color:var(--amber2)">closing bracket</strong> matches the top opening bracket, the stack pops that bracket.</span></li>
    <li><span class="step-num">3</span><span>At the end, if the stack is <strong style="color:var(--amber2)">empty</strong> the brackets are balanced; otherwise they are not.</span></li>
  </ol>

  <div class="concept-grid">
    <div class="concept-card">
      <span class="concept-icon">( )</span>
      <h4>Parentheses</h4>
      <p>Opening <code style="color:var(--amber2)">(</code> pushed; matched by <code style="color:#FC8181)">)</code> to pop.</p>
    </div>
    <div class="concept-card">
      <span class="concept-icon">[ ]</span>
      <h4>Square Brackets</h4>
      <p>Opening <code style="color:var(--amber2)">[</code> pushed; matched by <code style="color:#FC8181)">]</code> to pop.</p>
    </div>
    <div class="concept-card">
      <span class="concept-icon">{ }</span>
      <h4>Curly Braces</h4>
      <p>Opening <code style="color:var(--amber2)">{</code> pushed; matched by <code style="color:#FC8181)">}</code> to pop.</p>
    </div>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><span class="dot-r"></span><span class="dot-y"></span><span class="dot-g"></span></div>
      <span class="code-lang">C++ &nbsp;·&nbsp; isBalanced()</span>
    </div>
    <pre><code><span class="kw">#include</span><span class="st">&lt;iostream&gt;</span>
<span class="kw">#include</span><span class="st">&lt;stack&gt;</span>
<span class="kw">using namespace</span> std;

<span class="ty">bool</span> <span class="fn">isBalanced</span>(string expr){
    stack&lt;<span class="ty">char</span>&gt; s;

    <span class="kw">for</span>(<span class="ty">int</span> i=<span class="nm">0</span>; i&lt;expr.<span class="fn">length</span>(); i++){
        <span class="ty">char</span> ch = expr[i];

        <span class="kw">if</span>(ch == <span class="st">'('</span> || ch == <span class="st">'['</span> || ch == <span class="st">'{'</span>){
            s.<span class="fn">push</span>(ch);
        }
        <span class="kw">else if</span>(ch == <span class="st">')'</span> || ch == <span class="st">']'</span> || ch == <span class="st">'}'</span>){
            <span class="kw">if</span>(s.<span class="fn">empty</span>()) <span class="kw">return false</span>;

            <span class="kw">if</span>((ch == <span class="st">')'</span> &amp;&amp; s.<span class="fn">top</span>() == <span class="st">'('</span>) ||
               (ch == <span class="st">']'</span> &amp;&amp; s.<span class="fn">top</span>() == <span class="st">'['</span>) ||
               (ch == <span class="st">'}'</span> &amp;&amp; s.<span class="fn">top</span>() == <span class="st">'{'</span>)){
                s.<span class="fn">pop</span>();
            }
            <span class="kw">else return false</span>;
        }
    }
    <span class="kw">return</span> s.<span class="fn">empty</span>();
}</code></pre>
  </div>
</section>

<!-- ═══════════ Q4 — QUEUE THEORY ═══════════ -->
<section class="section" id="q4">
  <div class="section-header">
    <span class="section-num">04</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 4</p>
      <h2 class="section-title">Queue Theory</h2>
    </div>
  </div>

  <h3 class="sub-title">What is a Queue?</h3>
  <p>A queue is a linear data structure in which insertion happens from the <strong style="color:var(--amber2)">rear</strong> and deletion happens from the <strong style="color:var(--amber2)">front</strong>. It follows the <strong style="color:var(--amber2)">FIFO</strong> principle: <em>First In, First Out</em>.</p>

  <div class="principle-visual">
    <div>
      <div class="stack-viz-label">Queue (FIFO)</div>
      <div style="display:flex;align-items:center;gap:0.4rem;margin-top:0.5rem;">
        <span class="viz-label" style="writing-mode:vertical-rl;text-orientation:mixed;transform:rotate(180deg);margin-right:0.2rem;">dequeue ←</span>
        <div class="queue-viz">
          <div class="queue-block qb-front">5 <span style="font-size:0.6rem;display:block;color:#FC8181">front</span></div>
          <div class="queue-block">12</div>
          <div class="queue-block">8</div>
          <div class="queue-block qb-rear">20 <span style="font-size:0.6rem;display:block;color:var(--amber2)">rear</span></div>
        </div>
        <span class="viz-label" style="writing-mode:vertical-rl;text-orientation:mixed;margin-left:0.2rem;">→ enqueue</span>
      </div>
    </div>
    <div>
      <div class="badges">
        <span class="badge badge-amber">Bank Queue</span>
        <span class="badge badge-amber">Printer Jobs</span>
        <span class="badge badge-amber">CPU Scheduling</span>
        <span class="badge badge-amber">BFS Traversal</span>
      </div>
    </div>
  </div>

  <h3 class="sub-title">Core Queue Operations</h3>
  <div class="table-wrap">
    <table>
      <thead>
        <tr><th>Operation</th><th>Description</th><th>Time Complexity</th></tr>
      </thead>
      <tbody>
        <tr><td>enqueue()</td><td>Inserts an element from the rear side</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>dequeue()</td><td>Removes an element from the front side</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>front()</td><td>Returns the front element without removing it</td><td><span class="badge badge-green">O(1)</span></td></tr>
        <tr><td>isEmpty()</td><td>Checks whether the queue is empty</td><td><span class="badge badge-green">O(1)</span></td></tr>
      </tbody>
    </table>
  </div>

  <h3 class="sub-title">Circular Queue</h3>
  <div class="callout">
    A <strong>circular queue</strong> connects the last position back to the first. Empty spaces created after dequeue can be reused, making it more memory efficient. Front and rear move in a circular manner using the <strong>modulo operator</strong>.
  </div>

  <h3 class="sub-title">Array vs. Linked List Queue</h3>
  <div class="table-wrap">
    <table>
      <thead>
        <tr><th>Feature</th><th>Array Queue</th><th>Linked List Queue</th></tr>
      </thead>
      <tbody>
        <tr><td>Size</td><td>Fixed</td><td>Dynamic</td></tr>
        <tr><td>Wasted Space</td><td>May occur at front after dequeue</td><td>None</td></tr>
        <tr><td>Flexibility</td><td>Less flexible</td><td>More flexible (preferred)</td></tr>
        <tr><td>Overflow Risk</td><td>Even with empty spaces at front</td><td>Only when memory runs out</td></tr>
      </tbody>
    </table>
  </div>
  <p>Linked list implementation is generally <strong style="color:var(--amber2)">preferred</strong>. Array queues may face overflow even when empty spaces exist at the front.</p>

  <h3 class="sub-title">Dry Run Trace</h3>
  <div class="trace-block">
    <div class="trace-header">Operations &amp; Queue State</div>
    <div class="trace-row"><span class="trace-op">enqueue(5)</span><span class="trace-arr">→</span><span class="trace-state">[5]</span></div>
    <div class="trace-row"><span class="trace-op">enqueue(12)</span><span class="trace-arr">→</span><span class="trace-state">[5, 12]</span></div>
    <div class="trace-row"><span class="trace-op">enqueue(8)</span><span class="trace-arr">→</span><span class="trace-state">[5, 12, 8]</span></div>
    <div class="trace-row"><span class="trace-op">dequeue() <span class="trace-ret">returns 5</span></span><span class="trace-arr">→</span><span class="trace-state">[12, 8]</span></div>
    <div class="trace-row"><span class="trace-op">front() <span class="trace-ret">returns 12</span></span><span class="trace-arr">→</span><span class="trace-state">[12, 8]</span></div>
    <div class="trace-row"><span class="trace-op">enqueue(20)</span><span class="trace-arr">→</span><span class="trace-state">[12, 8, 20]</span></div>
    <div class="trace-row"><span class="trace-op">dequeue() <span class="trace-ret">returns 12</span></span><span class="trace-arr">→</span><span class="trace-state">[8, 20]</span></div>
    <div class="trace-row"><span class="trace-op">dequeue() <span class="trace-ret">returns 8</span></span><span class="trace-arr">→</span><span class="trace-state">[20]</span></div>
  </div>
</section>

<!-- ═══════════ Q5 — QUEUE IMPLEMENTATION ═══════════ -->
<section class="section" id="q5">
  <div class="section-header">
    <span class="section-num">05</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 5</p>
      <h2 class="section-title">Queue Implementation</h2>
    </div>
  </div>

  <p>Both a <strong style="color:var(--amber2)">linked list-based queue</strong> and a <strong style="color:var(--amber2)">circular array queue</strong> are implemented below.</p>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><span class="dot-r"></span><span class="dot-y"></span><span class="dot-g"></span></div>
      <span class="code-lang">C++ &nbsp;·&nbsp; Linked List Queue &amp; Circular Queue</span>
    </div>
    <pre><code><span class="kw">#include</span><span class="st">&lt;iostream&gt;</span>
<span class="kw">using namespace</span> std;

<span class="cm">// ─── Node ─────────────────────────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">Node</span>{
    <span class="kw">public</span>:
    <span class="ty">int</span>   data;
    <span class="ty">Node</span><span class="op">*</span> next;
    <span class="fn">Node</span>(<span class="ty">int</span> val){ data = val; next = <span class="kw">NULL</span>; }
};

<span class="cm">// ─── Linked List Queue ────────────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">Queue</span>{
    <span class="ty">Node</span><span class="op">*</span> front;
    <span class="ty">Node</span><span class="op">*</span> rear;

    <span class="kw">public</span>:
    <span class="fn">Queue</span>(){ front = rear = <span class="kw">NULL</span>; }

    <span class="ty">bool</span> <span class="fn">isEmpty</span>(){ <span class="kw">return</span> front == <span class="kw">NULL</span>; }

    <span class="ty">void</span> <span class="fn">enqueue</span>(<span class="ty">int</span> val){
        <span class="ty">Node</span><span class="op">*</span> newNode = <span class="kw">new</span> <span class="fn">Node</span>(val);
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ front = rear = newNode; <span class="kw">return</span>; }
        rear<span class="op">-&gt;</span>next = newNode;
        rear = newNode;
    }

    <span class="ty">int</span> <span class="fn">dequeue</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Queue Underflow"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="ty">int</span> value = front<span class="op">-&gt;</span>data;
        <span class="ty">Node</span><span class="op">*</span> temp = front;
        front = front<span class="op">-&gt;</span>next;
        <span class="kw">delete</span> temp;
        <span class="kw">return</span> value;
    }

    <span class="ty">int</span> <span class="fn">Front</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Queue is Empty"</span>&lt;&lt;endl; <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>; }
        <span class="kw">return</span> front<span class="op">-&gt;</span>data;
    }

    <span class="ty">void</span> <span class="fn">display</span>(){
        <span class="ty">Node</span><span class="op">*</span> temp = front;
        <span class="kw">while</span>(temp != <span class="kw">NULL</span>){ cout&lt;&lt;temp<span class="op">-&gt;</span>data&lt;&lt;<span class="st">" "</span>; temp = temp<span class="op">-&gt;</span>next; }
        cout&lt;&lt;endl;
    }

    <span class="op">~</span><span class="fn">Queue</span>(){
        <span class="kw">while</span>(front != <span class="kw">NULL</span>){ <span class="ty">Node</span><span class="op">*</span> temp=front; front=front<span class="op">-&gt;</span>next; <span class="kw">delete</span> temp; }
    }
};

<span class="cm">// ─── Circular Array Queue ─────────────────────────────────────</span>
<span class="kw">class</span> <span class="ty">CircularQueue</span>{
    <span class="ty">int</span> arr[<span class="nm">6</span>];
    <span class="ty">int</span> front;
    <span class="ty">int</span> rear;

    <span class="kw">public</span>:
    <span class="fn">CircularQueue</span>(){ front = rear = <span class="op">-</span><span class="nm">1</span>; }

    <span class="ty">bool</span> <span class="fn">isFull</span>(){  <span class="kw">return</span> (rear <span class="op">+</span> <span class="nm">1</span>) <span class="op">%</span> <span class="nm">6</span> == front; }
    <span class="ty">bool</span> <span class="fn">isEmpty</span>(){ <span class="kw">return</span> front == <span class="op">-</span><span class="nm">1</span>; }

    <span class="ty">void</span> <span class="fn">enqueue</span>(<span class="ty">int</span> val){
        <span class="kw">if</span>(<span class="fn">isFull</span>()){ cout&lt;&lt;<span class="st">"Queue Overflow"</span>&lt;&lt;endl; <span class="kw">return</span>; }
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()) front = rear = <span class="nm">0</span>;
        <span class="kw">else</span>          rear = (rear <span class="op">+</span> <span class="nm">1</span>) <span class="op">%</span> <span class="nm">6</span>;
        arr[rear] = val;
    }

    <span class="ty">void</span> <span class="fn">dequeue</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Queue Underflow"</span>&lt;&lt;endl; <span class="kw">return</span>; }
        <span class="kw">if</span>(front == rear) front = rear = <span class="op">-</span><span class="nm">1</span>;
        <span class="kw">else</span>              front = (front <span class="op">+</span> <span class="nm">1</span>) <span class="op">%</span> <span class="nm">6</span>;
    }

    <span class="ty">void</span> <span class="fn">display</span>(){
        <span class="kw">if</span>(<span class="fn">isEmpty</span>()){ cout&lt;&lt;<span class="st">"Queue is Empty"</span>&lt;&lt;endl; <span class="kw">return</span>; }
        <span class="ty">int</span> i = front;
        <span class="kw">while</span>(i != rear){ cout&lt;&lt;arr[i]&lt;&lt;<span class="st">" "</span>; i = (i<span class="op">+</span><span class="nm">1</span>)<span class="op">%</span><span class="nm">6</span>; }
        cout&lt;&lt;arr[rear]&lt;&lt;endl;
    }
};

<span class="cm">// ─── Driver ───────────────────────────────────────────────────</span>
<span class="ty">int</span> <span class="fn">main</span>(){
    <span class="ty">Queue</span> q;
    q.<span class="fn">enqueue</span>(<span class="nm">10</span>); q.<span class="fn">enqueue</span>(<span class="nm">20</span>); q.<span class="fn">enqueue</span>(<span class="nm">30</span>);
    q.<span class="fn">enqueue</span>(<span class="nm">40</span>); q.<span class="fn">enqueue</span>(<span class="nm">50</span>);
    q.<span class="fn">display</span>();

    q.<span class="fn">dequeue</span>(); q.<span class="fn">dequeue</span>();
    q.<span class="fn">display</span>();

    <span class="ty">CircularQueue</span> cq;
    cq.<span class="fn">enqueue</span>(<span class="nm">1</span>); cq.<span class="fn">enqueue</span>(<span class="nm">2</span>); cq.<span class="fn">enqueue</span>(<span class="nm">3</span>);
    cq.<span class="fn">enqueue</span>(<span class="nm">4</span>); cq.<span class="fn">enqueue</span>(<span class="nm">5</span>); cq.<span class="fn">enqueue</span>(<span class="nm">6</span>);
    cq.<span class="fn">enqueue</span>(<span class="nm">7</span>);  <span class="cm">// overflow — queue is full</span>
    cq.<span class="fn">display</span>();

    cq.<span class="fn">dequeue</span>(); cq.<span class="fn">dequeue</span>();
    cq.<span class="fn">enqueue</span>(<span class="nm">7</span>); cq.<span class="fn">enqueue</span>(<span class="nm">8</span>);
    cq.<span class="fn">display</span>();

    <span class="kw">return</span> <span class="nm">0</span>;
}</code></pre>
  </div>
</section>

<!-- ═══════════ Q6 — POSTFIX EVALUATOR ═══════════ -->
<section class="section" id="q6">
  <div class="section-header">
    <span class="section-num">06</span>
    <div class="section-title-wrap">
      <p class="section-tag">Question 6</p>
      <h2 class="section-title">Evaluate Postfix Expression</h2>
    </div>
  </div>

  <h3 class="sub-title">Algorithm</h3>
  <ol class="algo-steps">
    <li><span class="step-num">1</span><span>Traverse the expression <strong style="color:var(--amber2)">left to right</strong>.</span></li>
    <li><span class="step-num">2</span><span>If the character is a <strong style="color:var(--amber2)">digit</strong>, push it into the stack.</span></li>
    <li><span class="step-num">3</span><span>If the character is an <strong style="color:var(--amber2)">operator</strong>, pop two values, perform the operation, and push the result back.</span></li>
    <li><span class="step-num">4</span><span>The <strong style="color:var(--amber2)">final value</strong> remaining in the stack is the answer.</span></li>
  </ol>

  <div class="trace-block" style="margin-bottom:1.5rem;">
    <div class="trace-header">Example Evaluations</div>
    <div class="trace-row"><span class="trace-op">"23+"</span><span class="trace-arr">→</span><span class="trace-state trace-ret">Result: 5</span></div>
    <div class="trace-row"><span class="trace-op">"53*2+"</span><span class="trace-arr">→</span><span class="trace-state trace-ret">Result: 17</span></div>
    <div class="trace-row"><span class="trace-op">"842-*"</span><span class="trace-arr">→</span><span class="trace-state trace-ret">Result: 16</span></div>
  </div>

  <div class="code-wrap">
    <div class="code-header">
      <div class="code-dots"><span class="dot-r"></span><span class="dot-y"></span><span class="dot-g"></span></div>
      <span class="code-lang">C++ &nbsp;·&nbsp; evaluatePostfix()</span>
    </div>
    <pre><code><span class="kw">#include</span><span class="st">&lt;iostream&gt;</span>
<span class="kw">#include</span><span class="st">&lt;stack&gt;</span>
<span class="kw">using namespace</span> std;

<span class="ty">int</span> <span class="fn">evaluatePostfix</span>(string expr){
    stack&lt;<span class="ty">int</span>&gt; s;

    <span class="kw">for</span>(<span class="ty">int</span> i=<span class="nm">0</span>; i&lt;expr.<span class="fn">length</span>(); i++){
        <span class="ty">char</span> ch = expr[i];

        <span class="kw">if</span>(<span class="fn">isdigit</span>(ch)){
            s.<span class="fn">push</span>(ch <span class="op">-</span> <span class="st">'0'</span>);
        }
        <span class="kw">else</span>{
            <span class="ty">int</span> val2 = s.<span class="fn">top</span>(); s.<span class="fn">pop</span>();
            <span class="ty">int</span> val1 = s.<span class="fn">top</span>(); s.<span class="fn">pop</span>();

            <span class="kw">switch</span>(ch){
                <span class="kw">case</span> <span class="st">'+'</span>: s.<span class="fn">push</span>(val1 <span class="op">+</span> val2); <span class="kw">break</span>;
                <span class="kw">case</span> <span class="st">'-'</span>: s.<span class="fn">push</span>(val1 <span class="op">-</span> val2); <span class="kw">break</span>;
                <span class="kw">case</span> <span class="st">'*'</span>: s.<span class="fn">push</span>(val1 <span class="op">*</span> val2); <span class="kw">break</span>;
                <span class="kw">case</span> <span class="st">'/'</span>:
                    <span class="kw">if</span>(val2 == <span class="nm">0</span>){
                        cout&lt;&lt;<span class="st">"Division by zero not allowed"</span>&lt;&lt;endl;
                        <span class="kw">return</span> <span class="op">-</span><span class="nm">1</span>;
                    }
                    s.<span class="fn">push</span>(val1 <span class="op">/</span> val2); <span class="kw">break</span>;
            }
        }
    }
    <span class="kw">return</span> s.<span class="fn">top</span>();
}

<span class="ty">int</span> <span class="fn">main</span>(){
    cout&lt;&lt;<span class="fn">evaluatePostfix</span>(<span class="st">"23+"</span>)&lt;&lt;endl;    <span class="cm">// Output: 5</span>
    cout&lt;&lt;<span class="fn">evaluatePostfix</span>(<span class="st">"53*2+"</span>)&lt;&lt;endl;  <span class="cm">// Output: 17</span>
    cout&lt;&lt;<span class="fn">evaluatePostfix</span>(<span class="st">"842-*"</span>)&lt;&lt;endl;  <span class="cm">// Output: 16</span>
    <span class="kw">return</span> <span class="nm">0</span>;
}</code></pre>
  </div>
</section>
</div>

<!-- ═══════════ FOOTER ═══════════ -->
<footer>
  <div class="container">
    <div class="footer-rule"></div>
    <p class="footer-text">
      <span>Ayesha Javaid</span> &nbsp;·&nbsp; <span>s2025376102</span> &nbsp;·&nbsp;
      DSA Assignment 3 — Stacks &amp; Queues &nbsp;·&nbsp;
      Department of Artificial Intelligence
    </p>
  </div>
</footer>

<script>
  // Scroll-reveal for sections
  const sections = document.querySelectorAll('.section');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.06 });
  sections.forEach(s => observer.observe(s));
</script>
</body>
</html>
