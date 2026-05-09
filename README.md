# khamblenlearning.github.io
Learning Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Leading from Here — Program Overview</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink: #1a1a2e;
    --ink-soft: #3d3d5c;
    --gold: #c9a84c;
    --gold-light: #e8d49a;
    --cream: #f9f6ef;
    --cream-dark: #efe9d8;
    --sage: #5a7a6a;
    --rust: #b85c38;
    --rule: rgba(201,168,76,0.3);
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--ink);
    font-size: 15px;
    line-height: 1.7;
  }

  /* ── COVER ── */
  .cover {
    min-height: 100vh;
    background: var(--ink);
    display: grid;
    grid-template-rows: 1fr auto;
    position: relative;
    overflow: hidden;
    padding: 60px;
  }

  .cover::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 70% 40%, rgba(201,168,76,0.08) 0%, transparent 60%),
      repeating-linear-gradient(
        0deg,
        transparent,
        transparent 59px,
        rgba(201,168,76,0.06) 59px,
        rgba(201,168,76,0.06) 60px
      ),
      repeating-linear-gradient(
        90deg,
        transparent,
        transparent 59px,
        rgba(201,168,76,0.04) 59px,
        rgba(201,168,76,0.04) 60px
      );
  }

  .cover-eyebrow {
    position: relative;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .cover-eyebrow::after {
    content: '';
    flex: 1;
    max-width: 80px;
    height: 1px;
    background: var(--gold);
    opacity: 0.5;
  }

  .cover-main {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 0 40px;
  }

  .cover-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(52px, 8vw, 96px);
    font-weight: 700;
    color: var(--cream);
    line-height: 1.0;
    letter-spacing: -0.02em;
    margin-bottom: 8px;
  }

  .cover-title em {
    font-style: italic;
    color: var(--gold);
  }

  .cover-subtitle {
    font-family: 'Playfair Display', serif;
    font-size: clamp(18px, 2.5vw, 28px);
    font-weight: 400;
    font-style: italic;
    color: rgba(249,246,239,0.55);
    margin-bottom: 48px;
  }

  .cover-divider {
    width: 60px;
    height: 2px;
    background: var(--gold);
    margin-bottom: 32px;
  }

  .cover-meta {
    display: flex;
    gap: 48px;
    flex-wrap: wrap;
  }

  .cover-meta-item {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }

  .cover-meta-label {
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    opacity: 0.7;
  }

  .cover-meta-value {
    font-size: 14px;
    font-weight: 500;
    color: var(--cream);
  }

  .cover-footer {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    border-top: 1px solid rgba(201,168,76,0.2);
    padding-top: 24px;
    font-size: 11px;
    color: rgba(249,246,239,0.3);
    letter-spacing: 0.08em;
  }

  .portfolio-badge {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    opacity: 0.6;
    border: 1px solid rgba(201,168,76,0.3);
    padding: 6px 14px;
    border-radius: 2px;
  }

  /* ── LAYOUT ── */
  .page {
    max-width: 900px;
    margin: 0 auto;
    padding: 80px 60px;
  }

  @media (max-width: 640px) {
    .cover { padding: 40px 32px; }
    .page { padding: 60px 32px; }
  }

  /* ── SECTION HEADERS ── */
  .section-label {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .section-label::before {
    content: '';
    width: 24px;
    height: 1px;
    background: var(--gold);
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 4vw, 40px);
    font-weight: 700;
    color: var(--ink);
    line-height: 1.2;
    margin-bottom: 32px;
  }

  .section-title em {
    font-style: italic;
    color: var(--sage);
  }

  /* ── DIVIDERS ── */
  .page-divider {
    border: none;
    border-top: 1px solid var(--cream-dark);
    margin: 72px 0;
  }

  /* ── PROSE ── */
  .prose {
    color: var(--ink-soft);
    font-size: 15px;
    line-height: 1.8;
  }
  .prose p + p { margin-top: 16px; }
  .prose strong { color: var(--ink); font-weight: 500; }

  /* ── PROGRAM SNAPSHOT ── */
  .snapshot-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 2px;
    margin: 40px 0;
    border: 2px solid var(--ink);
  }

  .snapshot-cell {
    background: white;
    padding: 28px 24px;
    border-right: 2px solid var(--ink);
  }
  .snapshot-cell:last-child { border-right: none; }

  .snapshot-cell-label {
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 8px;
  }

  .snapshot-cell-value {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 4px;
  }

  .snapshot-cell-desc {
    font-size: 12px;
    color: var(--ink-soft);
    line-height: 1.4;
  }

  /* ── PHILOSOPHY BLOCK ── */
  .philosophy-block {
    background: var(--ink);
    color: var(--cream);
    padding: 48px 52px;
    margin: 40px 0;
    position: relative;
    overflow: hidden;
  }

  .philosophy-block::before {
    content: '\201C';
    font-family: 'Playfair Display', serif;
    font-size: 200px;
    color: rgba(201,168,76,0.08);
    position: absolute;
    top: -20px;
    left: 30px;
    line-height: 1;
    pointer-events: none;
  }

  .philosophy-block blockquote {
    font-family: 'Playfair Display', serif;
    font-size: clamp(18px, 2.5vw, 24px);
    font-style: italic;
    font-weight: 400;
    line-height: 1.6;
    position: relative;
    color: var(--cream);
    margin-bottom: 20px;
  }

  .philosophy-block cite {
    font-size: 12px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    font-style: normal;
  }

  /* ── AUDIENCE BLOCK ── */
  .audience-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    margin: 32px 0;
  }

  @media (max-width: 580px) {
    .audience-grid { grid-template-columns: 1fr; }
    .snapshot-grid { grid-template-columns: 1fr 1fr; }
    .snapshot-cell { border-right: none; border-bottom: 2px solid var(--ink); }
    .snapshot-cell:last-child { border-bottom: none; }
  }

  .audience-card {
    padding: 28px;
    border: 1px solid var(--cream-dark);
    background: white;
  }

  .audience-card-icon {
    font-size: 24px;
    margin-bottom: 12px;
  }

  .audience-card h4 {
    font-family: 'Playfair Display', serif;
    font-size: 17px;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 8px;
  }

  .audience-card p {
    font-size: 13px;
    color: var(--ink-soft);
    line-height: 1.6;
  }

  /* ── CURRICULUM MAP ── */
  .curriculum-table {
    width: 100%;
    border-collapse: collapse;
    margin: 32px 0;
    font-size: 13.5px;
  }

  .curriculum-table thead tr {
    background: var(--ink);
    color: var(--cream);
  }

  .curriculum-table thead th {
    padding: 14px 16px;
    text-align: left;
    font-weight: 500;
    letter-spacing: 0.06em;
    font-size: 11px;
    text-transform: uppercase;
  }

  .curriculum-table thead th:first-child {
    width: 40px;
    text-align: center;
  }

  .curriculum-table tbody tr {
    border-bottom: 1px solid var(--cream-dark);
    transition: background 0.15s;
  }

  .curriculum-table tbody tr:hover { background: rgba(201,168,76,0.05); }

  .curriculum-table tbody td {
    padding: 16px;
    vertical-align: top;
    color: var(--ink-soft);
  }

  .curriculum-table tbody td:first-child {
    text-align: center;
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 700;
    color: var(--gold);
    width: 40px;
    vertical-align: middle;
  }

  .curriculum-table .module-title {
    font-weight: 500;
    color: var(--ink);
    font-size: 14px;
    margin-bottom: 2px;
  }

  .curriculum-table .module-desc {
    font-size: 12.5px;
    color: var(--ink-soft);
  }

  .tag {
    display: inline-block;
    font-size: 10px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 3px 8px;
    border-radius: 2px;
    font-weight: 500;
    margin: 2px 2px 2px 0;
  }

  .tag-elearning { background: rgba(90,122,106,0.12); color: var(--sage); }
  .tag-debrief   { background: rgba(201,168,76,0.15); color: #8a6d1a; }
  .tag-jobaid    { background: rgba(184,92,56,0.1);  color: var(--rust); }
  .tag-video     { background: rgba(26,26,46,0.08);  color: var(--ink); }
  .tag-assess    { background: rgba(90,122,106,0.18); color: #3d6050; }

  /* ── SESSION FLOW ── */
  .flow-row {
    display: flex;
    gap: 0;
    margin: 32px 0;
    overflow-x: auto;
  }

  .flow-step {
    flex: 1;
    min-width: 130px;
    padding: 24px 20px;
    background: white;
    border: 1px solid var(--cream-dark);
    border-right: none;
    position: relative;
    text-align: center;
  }

  .flow-step:last-child { border-right: 1px solid var(--cream-dark); }

  .flow-step::after {
    content: '›';
    position: absolute;
    right: -14px;
    top: 50%;
    transform: translateY(-50%);
    font-size: 22px;
    color: var(--gold);
    z-index: 2;
    font-weight: 300;
  }

  .flow-step:last-child::after { display: none; }

  .flow-step-num {
    font-family: 'Playfair Display', serif;
    font-size: 32px;
    font-weight: 700;
    color: var(--cream-dark);
    line-height: 1;
    margin-bottom: 8px;
  }

  .flow-step-title {
    font-size: 12px;
    font-weight: 500;
    color: var(--ink);
    margin-bottom: 6px;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  .flow-step-desc {
    font-size: 11.5px;
    color: var(--ink-soft);
    line-height: 1.5;
  }

  .flow-step-time {
    margin-top: 10px;
    font-size: 11px;
    color: var(--gold);
    font-weight: 500;
  }

  /* ── DELIVERABLES MENU ── */
  .deliverables-list {
    list-style: none;
    margin: 32px 0;
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .deliverables-list li {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    padding: 20px 24px;
    background: white;
    border: 1px solid var(--cream-dark);
    transition: border-color 0.15s;
  }

  .deliverables-list li:hover { border-color: var(--gold); }

  .del-icon {
    font-size: 20px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  .del-content { flex: 1; }

  .del-title {
    font-weight: 500;
    color: var(--ink);
    font-size: 14px;
    margin-bottom: 3px;
  }

  .del-desc {
    font-size: 12.5px;
    color: var(--ink-soft);
    line-height: 1.5;
  }

  .del-optional {
    font-size: 10px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold);
    background: rgba(201,168,76,0.1);
    padding: 2px 7px;
    border-radius: 2px;
    flex-shrink: 0;
    align-self: flex-start;
    margin-top: 2px;
  }

  /* ── OUTCOMES ── */
  .outcomes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin: 32px 0;
  }

  .outcome-card {
    padding: 24px;
    border-left: 3px solid var(--gold);
    background: white;
  }

  .outcome-card p {
    font-size: 13.5px;
    color: var(--ink-soft);
    line-height: 1.6;
  }

  .outcome-card strong {
    display: block;
    font-size: 13px;
    font-weight: 500;
    color: var(--ink);
    margin-bottom: 6px;
    text-transform: uppercase;
    letter-spacing: 0.06em;
  }

  /* ── CUSTOMIZATION NOTE ── */
  .customize-box {
    background: rgba(90,122,106,0.08);
    border: 1px solid rgba(90,122,106,0.25);
    border-left: 3px solid var(--sage);
    padding: 24px 28px;
    margin: 32px 0;
  }

  .customize-box h4 {
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--sage);
    margin-bottom: 10px;
  }

  .customize-box p, .customize-box ul {
    font-size: 13.5px;
    color: var(--ink-soft);
    line-height: 1.7;
  }

  .customize-box ul {
    padding-left: 18px;
    margin-top: 8px;
  }

  .customize-box ul li { margin-bottom: 4px; }

  /* ── PRINT / PAGE BREAKS ── */
  @media print {
    .cover { min-height: auto; page-break-after: always; }
    .page { padding: 40px; }
    .page-divider { margin: 40px 0; }
  }
</style>
</head>
<body>

<!-- ══════════════════════════════════════
     COVER
══════════════════════════════════════ -->
<section class="cover">
  <div class="cover-eyebrow">Leadership Development Program</div>

  <div class="cover-main">
    <h1 class="cover-title">Leading<br><em>from Here</em></h1>
    <p class="cover-subtitle">A Foundation Program for New &amp; Emerging Managers</p>
    <div class="cover-divider"></div>
    <div class="cover-meta">
      <div class="cover-meta-item">
        <span class="cover-meta-label">Format</span>
        <span class="cover-meta-value">Cohort-Based, Ongoing</span>
      </div>
      <div class="cover-meta-item">
        <span class="cover-meta-label">Audience</span>
        <span class="cover-meta-value">First-Time Managers</span>
      </div>
      <div class="cover-meta-item">
        <span class="cover-meta-label">Modules</span>
        <span class="cover-meta-value">6 Topics</span>
      </div>
      <div class="cover-meta-item">
        <span class="cover-meta-label">Cadence</span>
        <span class="cover-meta-value">Monthly Debriefs</span>
      </div>
    </div>
  </div>

  <div class="cover-footer">
    <span>[Client / Organization Name]</span>
    <span class="portfolio-badge">Portfolio Template</span>
    <span>[Year]</span>
  </div>
</section>

<!-- ══════════════════════════════════════
     PROGRAM OVERVIEW
══════════════════════════════════════ -->
<main class="page">

  <div class="section-label">About This Program</div>
  <h2 class="section-title">What Is <em>Leading from Here</em>?</h2>

  <div class="prose">
    <p><strong>Leading from Here</strong> is a cohort-based leadership development program designed specifically for new and emerging managers — people who have recently made the leap from individual contributor to people leader, or who are preparing to do so.</p>
    <p>Rather than a single training event, this program is built around a sustained learning cadence: short, focused pre-work paired with live debrief sessions where participants apply, discuss, and teach what they've learned. The result is a program that builds not just knowledge, but habits, language, and community.</p>
    <p>Each topic is explored over a full session cycle — pre-work to prepare, a live debrief to process and practice, and a job aid to sustain the skill on the job.</p>
  </div>

  <!-- Snapshot stats -->
  <div class="snapshot-grid">
    <div class="snapshot-cell">
      <div class="snapshot-cell-label">Program Length</div>
      <div class="snapshot-cell-value">6 months</div>
      <div class="snapshot-cell-desc">One topic per month, delivered in sequence</div>
    </div>
    <div class="snapshot-cell">
      <div class="snapshot-cell-label">Cohort Size</div>
      <div class="snapshot-cell-value">8–16</div>
      <div class="snapshot-cell-desc">Optimal for peer learning and discussion</div>
    </div>
    <div class="snapshot-cell">
      <div class="snapshot-cell-label">Session Length</div>
      <div class="snapshot-cell-value">90 min</div>
      <div class="snapshot-cell-desc">Live debrief per module (ILT or vILT)</div>
    </div>
    <div class="snapshot-cell">
      <div class="snapshot-cell-label">Pre-Work Time</div>
      <div class="snapshot-cell-value">~30 min</div>
      <div class="snapshot-cell-desc">Self-paced eLearning or video per topic</div>
    </div>
  </div>

  <hr class="page-divider">

  <!-- ── DESIGN PHILOSOPHY ── -->
  <div class="section-label">Design Philosophy</div>
  <h2 class="section-title">Why It's Built <em>This Way</em></h2>

  <div class="philosophy-block">
    <blockquote>
      "Leadership is not learned in a classroom. It's practiced in the moment — and then reflected on with people who are going through the same thing."
    </blockquote>
    <cite>— Program Design Principle</cite>
  </div>

  <div class="prose">
    <p>Most leadership training fails not because the content is wrong, but because there's no bridge between learning and doing. <strong>Leading from Here</strong> closes that gap with three design principles:</p>
  </div>

  <div class="outcomes-grid" style="margin-top: 24px;">
    <div class="outcome-card">
      <strong>Spaced Learning</strong>
      <p>Topics are spread over months, not days — giving participants time to practice between sessions and return with real experience to discuss.</p>
    </div>
    <div class="outcome-card">
      <strong>Peer Accountability</strong>
      <p>The cohort model creates mutual accountability. Participants know they'll be asked to teachback, which deepens engagement with pre-work.</p>
    </div>
    <div class="outcome-card">
      <strong>Practical Anchoring</strong>
      <p>Every session ends with a concrete commitment and a job aid — so skills transfer to the daily work of managing people, not just the training room.</p>
    </div>
  </div>

  <hr class="page-divider">

  <!-- ── TARGET AUDIENCE ── -->
  <div class="section-label">Who This Is For</div>
  <h2 class="section-title">Target <em>Audience</em></h2>

  <div class="audience-grid">
    <div class="audience-card">
      <div class="audience-card-icon">🎯</div>
      <h4>Primary Audience</h4>
      <p>Employees who have recently been promoted into their first management role, typically within the past 0–18 months. They are managing 2–8 direct reports and navigating the shift from doing to leading.</p>
    </div>
    <div class="audience-card">
      <div class="audience-card-icon">🔭</div>
      <h4>Secondary Audience</h4>
      <p>High-potential individual contributors being developed for a future leadership role. Participating in advance prepares them for the mindset shifts they'll need before promotion.</p>
    </div>
    <div class="audience-card">
      <div class="audience-card-icon">✅</div>
      <h4>Ideal Conditions</h4>
      <p>Program works best when participants are nominated cohort-style, have manager support, and operate in an organization that values leadership development as an ongoing investment — not a one-time event.</p>
    </div>
    <div class="audience-card">
      <div class="audience-card-icon">⚠️</div>
      <h4>Not Designed For</h4>
      <p>Senior or executive leaders, experienced managers seeking advanced development, or organizations looking for a standalone one-day workshop. Separate programs are recommended for those audiences.</p>
    </div>
  </div>

  <hr class="page-divider">

  <!-- ── CURRICULUM MAP ── -->
  <div class="section-label">Curriculum Map</div>
  <h2 class="section-title">The <em>Six Topics</em></h2>

  <div class="prose">
    <p>Each topic follows the same session cycle: pre-work → debrief → sustain. The modules are designed to build on each other sequentially, though individual sessions can also stand alone for organizations that prefer a modular approach.</p>
  </div>

  <table class="curriculum-table">
    <thead>
      <tr>
        <th>#</th>
        <th>Module Title</th>
        <th>Core Focus</th>
        <th>Suggested Deliverables</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>
          <div class="module-title">The Mindset Shift</div>
          <div class="module-desc">From individual contributor to leader</div>
        </td>
        <td>Identity, letting go, defining your leadership role</td>
        <td>
          <span class="tag tag-elearning">eLearning</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-jobaid">Job Aid</span>
        </td>
      </tr>
      <tr>
        <td>2</td>
        <td>
          <div class="module-title">1:1s &amp; Feedback</div>
          <div class="module-desc">Building connection through regular conversation</div>
        </td>
        <td>Effective 1:1 structure, giving and receiving feedback</td>
        <td>
          <span class="tag tag-video">Video</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-jobaid">Job Aid</span>
          <span class="tag tag-assess">Assessment</span>
        </td>
      </tr>
      <tr>
        <td>3</td>
        <td>
          <div class="module-title">Goals &amp; Accountability</div>
          <div class="module-desc">Setting expectations that actually stick</div>
        </td>
        <td>Goal-setting frameworks, following through, course correcting</td>
        <td>
          <span class="tag tag-elearning">eLearning</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-jobaid">Job Aid</span>
        </td>
      </tr>
      <tr>
        <td>4</td>
        <td>
          <div class="module-title">Trust &amp; Psychological Safety</div>
          <div class="module-desc">Creating an environment where people can do their best work</div>
        </td>
        <td>Trust behaviors, safety vs. comfort, inclusive leadership</td>
        <td>
          <span class="tag tag-video">Video</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-assess">Assessment</span>
        </td>
      </tr>
      <tr>
        <td>5</td>
        <td>
          <div class="module-title">Performance Conversations</div>
          <div class="module-desc">Addressing issues early and with care</div>
        </td>
        <td>Difficult conversations, performance frameworks, documentation</td>
        <td>
          <span class="tag tag-elearning">eLearning</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-jobaid">Job Aid</span>
          <span class="tag tag-assess">Assessment</span>
        </td>
      </tr>
      <tr>
        <td>6</td>
        <td>
          <div class="module-title">Leading Through Change</div>
          <div class="module-desc">Keeping your team grounded when things are uncertain</div>
        </td>
        <td>Change communication, resilience, managing upward and downward</td>
        <td>
          <span class="tag tag-video">Video</span>
          <span class="tag tag-debrief">Debrief</span>
          <span class="tag tag-jobaid">Job Aid</span>
        </td>
      </tr>
    </tbody>
  </table>

  <div class="customize-box">
    <h4>📌 Customization Note</h4>
    <p>The module sequence above is a recommended default. Clients may choose to:</p>
    <ul>
      <li>Reorder topics to align with internal priorities or a current organizational challenge</li>
      <li>Add a module (e.g., Delegation, Coaching Skills, Hiring &amp; Onboarding)</li>
      <li>Replace eLearning pre-work with a reading, podcast, or short video for any given module</li>
      <li>Extend the cadence to bi-monthly for a 12-month program</li>
    </ul>
  </div>

  <hr class="page-divider">

  <!-- ── SESSION FLOW ── -->
  <div class="section-label">Session Design</div>
  <h2 class="section-title">How Each <em>Session Works</em></h2>

  <div class="prose">
    <p>Every module follows the same repeatable cycle, making it easy for both facilitators and participants to know what to expect. The structure is designed to maximize discussion time and minimize passive delivery.</p>
  </div>

  <div class="flow-row">
    <div class="flow-step">
      <div class="flow-step-num">01</div>
      <div class="flow-step-title">Pre-Work</div>
      <div class="flow-step-desc">Self-paced eLearning, video, or reading completed before the session</div>
      <div class="flow-step-time">~30 min</div>
    </div>
    <div class="flow-step">
      <div class="flow-step-num">02</div>
      <div class="flow-step-title">Open &amp; Check-In</div>
      <div class="flow-step-desc">Facilitator opens, connects to previous topic, quick group check-in</div>
      <div class="flow-step-time">10 min</div>
    </div>
    <div class="flow-step">
      <div class="flow-step-num">03</div>
      <div class="flow-step-title">Teachbacks</div>
      <div class="flow-step-desc">2–3 participants share a key insight, story, or application from pre-work</div>
      <div class="flow-step-time">20 min</div>
    </div>
    <div class="flow-step">
      <div class="flow-step-num">04</div>
      <div class="flow-step-title">Discussion</div>
      <div class="flow-step-desc">Facilitated deep-dive: scenarios, debate, or skill practice</div>
      <div class="flow-step-time">45 min</div>
    </div>
    <div class="flow-step">
      <div class="flow-step-num">05</div>
      <div class="flow-step-title">Commit &amp; Close</div>
      <div class="flow-step-desc">Individual commitment, job aid distribution, preview of next topic</div>
      <div class="flow-step-time">15 min</div>
    </div>
  </div>

  <hr class="page-divider">

  <!-- ── DELIVERABLES MENU ── -->
  <div class="section-label">Deliverables Menu</div>
  <h2 class="section-title">What Can Be <em>Built</em></h2>

  <div class="prose">
    <p>Not every module requires every deliverable. The list below represents the full menu of available assets — selected based on client goals, budget, and delivery modality.</p>
  </div>

  <ul class="deliverables-list">
    <li>
      <span class="del-icon">📋</span>
      <div class="del-content">
        <div class="del-title">Course Outline</div>
        <div class="del-desc">Topic overview, learning objectives, content outline, and instructional notes. Used as the design blueprint before development begins.</div>
      </div>
    </li>
    <li>
      <span class="del-icon">🎞️</span>
      <div class="del-content">
        <div class="del-title">Storyboard</div>
        <div class="del-desc">Slide-by-slide script and visual direction for the eLearning pre-work module. Includes on-screen text, narration, interactions, and visual notes.</div>
      </div>
    </li>
    <li>
      <span class="del-icon">🎙️</span>
      <div class="del-content">
        <div class="del-title">Debrief Guide</div>
        <div class="del-desc">Facilitator-facing session runbook with timing, teachback prompts, discussion questions, facilitation tips, and activity instructions.</div>
      </div>
    </li>
    <li>
      <span class="del-icon">📓</span>
      <div class="del-content">
        <div class="del-title">Participant Guide</div>
        <div class="del-desc">Learner-facing session workbook with reflection prompts, note-taking space, activity worksheets, and post-session action planning.</div>
      </div>
    </li>
    <li>
      <span class="del-icon">✅</span>
      <div class="del-content">
        <div class="del-title">Assessment / Knowledge Check</div>
        <div class="del-desc">Pre- and/or post-session quiz tied to learning objectives. Used to measure knowledge gain and identify gaps. Can include scenario-based questions.</div>
      </div>
      <span class="del-optional">Optional</span>
    </li>
    <li>
      <span class="del-icon">🗂️</span>
      <div class="del-content">
        <div class="del-title">Job Aid / Quick Reference Card</div>
        <div class="del-desc">A one-page (print or digital) post-session reference tool. Designed to be used on the job, not in training — frameworks, conversation starters, checklists.</div>
      </div>
    </li>
    <li>
      <span class="del-icon">🎬</span>
      <div class="del-content">
        <div class="del-title">Video Script</div>
        <div class="del-desc">Full production script for a micro-learning video (3–7 min). Includes scene descriptions, speaker notes, and on-screen text cues. Can be recorded by client SMEs or professional talent.</div>
      </div>
      <span class="del-optional">Optional</span>
    </li>
    <li>
      <span class="del-icon">💻</span>
      <div class="del-content">
        <div class="del-title">eLearning Module Mockup</div>
        <div class="del-desc">Interactive HTML/web prototype demonstrating the look, feel, and interactions of the digital pre-work module. Used for client review and as a development-ready reference.</div>
      </div>
      <span class="del-optional">Optional</span>
    </li>
  </ul>

  <hr class="page-divider">

  <!-- ── PROGRAM OUTCOMES ── -->
  <div class="section-label">Expected Outcomes</div>
  <h2 class="section-title">What Participants <em>Walk Away With</em></h2>

  <div class="outcomes-grid">
    <div class="outcome-card">
      <strong>Clarity</strong>
      <p>A clear mental model of what it means to lead — and how their role has changed.</p>
    </div>
    <div class="outcome-card">
      <strong>Skills</strong>
      <p>Practical frameworks and language for feedback, accountability, and difficult conversations.</p>
    </div>
    <div class="outcome-card">
      <strong>Confidence</strong>
      <p>Repeated practice and teachback builds the confidence to lead proactively — not reactively.</p>
    </div>
    <div class="outcome-card">
      <strong>Community</strong>
      <p>Relationships with peers navigating the same challenges — a network that often outlasts the program.</p>
    </div>
    <div class="outcome-card">
      <strong>Habits</strong>
      <p>Job aids and commitments build consistent routines around 1:1s, goal-setting, and feedback.</p>
    </div>
    <div class="outcome-card">
      <strong>Organizational Impact</strong>
      <p>Improved team engagement, fewer escalations, and stronger internal promotion pipelines.</p>
    </div>
  </div>

  <hr class="page-divider">

  <!-- ── NEXT STEPS ── -->
  <div class="section-label">For Clients</div>
  <h2 class="section-title">Getting <em>Started</em></h2>

  <div class="prose">
    <p>Every implementation of <strong>Leading from Here</strong> begins with a short discovery conversation to understand your organization's context, goals, and constraints. From there, we tailor the module sequence, select the right deliverables for each topic, and agree on a timeline for design, development, and delivery.</p>
  </div>

  <div class="customize-box">
    <h4>📋 Typical Engagement Phases</h4>
    <ul>
      <li><strong>Discovery</strong> — Stakeholder interviews, audience analysis, goals alignment (1–2 weeks)</li>
      <li><strong>Design</strong> — Course outlines, session flow, deliverable selection per module (2–3 weeks)</li>
      <li><strong>Development</strong> — Storyboards, guides, job aids, assessments, mockups (4–8 weeks)</li>
      <li><strong>Pilot</strong> — First cohort delivery with feedback loop for iteration (Month 1)</li>
      <li><strong>Ongoing</strong> — Continued delivery, quarterly review, and program refinement</li>
    </ul>
  </div>

  <div style="text-align:center; padding: 48px 0 20px; color: var(--ink-soft); font-size: 13px;">
    <div style="font-family: 'Playfair Display', serif; font-size: 22px; color: var(--ink); margin-bottom: 8px; font-style: italic;">Leading from Here</div>
    <div style="letter-spacing: 0.12em; text-transform: uppercase; font-size: 10px;">Portfolio Template &nbsp;·&nbsp; [Your Name / Studio] &nbsp;·&nbsp; [Contact Info]</div>
  </div>

</main>
</body>
</html>
