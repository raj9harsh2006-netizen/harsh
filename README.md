# harsh <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Harsh Raj — Finance Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Newsreader:ital,opsz,wght@0,6..72,400;0,6..72,500;0,6..72,600;1,6..72,400&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#1B2A4A;
    --ink-soft:#3C4A68;
    --paper:#EEF1EF;
    --paper-deep:#E2E7E3;
    --card:#FBFCFB;
    --gold:#B8860B;
    --teal:#2F6F6B;
    --line: rgba(27,42,74,0.18);
    --line-strong: rgba(27,42,74,0.35);
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.55;
  }
  ::selection{ background: var(--gold); color:#fff; }

  h1,h2,h3{
    font-family:'Newsreader', serif;
    font-weight:600;
    margin:0;
    letter-spacing:-0.01em;
  }
  .mono{ font-family:'IBM Plex Mono', monospace; }
  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.72rem;
    letter-spacing:0.16em;
    text-transform:uppercase;
    color:var(--ink-soft);
  }
  a{ color:inherit; }

  .wrap{ max-width:1040px; margin:0 auto; padding:0 32px; }

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:50;
    background:rgba(238,241,239,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{
    display:flex; align-items:center; justify-content:space-between;
    height:64px;
  }
  .nav-name{ font-family:'Newsreader', serif; font-weight:600; font-size:1.05rem; }
  .nav-links{ display:flex; gap:28px; }
  .nav-links a{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.75rem;
    letter-spacing:0.06em;
    text-decoration:none;
    color:var(--ink-soft);
    text-transform:uppercase;
    padding:6px 0;
    border-bottom:2px solid transparent;
    transition:border-color .2s ease, color .2s ease;
  }
  .nav-links a:hover{ color:var(--ink); border-color:var(--gold); }
  .nav-toggle{ display:none; }

  /* ---------- HERO / STATEMENT ---------- */
  header.hero{ padding:64px 0 0; }
  .statement{
    background:var(--card);
    border:1px solid var(--line-strong);
    border-radius:2px;
    box-shadow:0 1px 0 var(--line), 0 18px 40px -28px rgba(27,42,74,0.35);
    overflow:hidden;
  }
  .statement-head{
    display:flex; justify-content:space-between; align-items:flex-start;
    padding:36px 40px 28px;
    border-bottom:1px dashed var(--line-strong);
    gap:24px;
    flex-wrap:wrap;
  }
  .statement-head h1{ font-size:2.6rem; margin-top:6px; }
  .statement-role{ color:var(--ink-soft); font-size:1.05rem; margin-top:8px; max-width:46ch; }
  .statement-id{ text-align:right; }
  .statement-id .mono{ font-size:0.78rem; color:var(--ink-soft); display:block; margin-bottom:4px;}
  .seal{
    display:inline-flex; align-items:center; gap:8px;
    margin-top:14px;
    border:1.5px solid var(--gold);
    color:var(--gold);
    padding:6px 12px;
    border-radius:999px;
    font-family:'IBM Plex Mono', monospace;
    font-size:0.72rem;
    letter-spacing:0.08em;
    text-transform:uppercase;
    transform:rotate(-3deg);
  }
  .seal svg{ width:14px; height:14px; }

  .ledger-strip{
    display:grid;
    grid-template-columns:repeat(4, 1fr);
  }
  .ledger-item{
    padding:26px 28px;
    border-right:1px dashed var(--line);
    position:relative;
  }
  .ledger-item:last-child{ border-right:none; }
  .ledger-figure{
    font-family:'IBM Plex Mono', monospace;
    font-size:1.9rem;
    font-weight:600;
    color:var(--ink);
    display:flex; align-items:baseline; gap:6px;
  }
  .ledger-figure .tick{
    color:var(--teal);
    font-size:1.1rem;
  }
  .ledger-label{
    font-size:0.78rem;
    color:var(--ink-soft);
    margin-top:6px;
    max-width:22ch;
  }
  .statement-foot{
    display:flex; flex-wrap:wrap; gap:18px 28px;
    padding:22px 40px 30px;
    border-top:1px dashed var(--line-strong);
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem;
    color:var(--ink-soft);
  }
  .statement-foot a{ text-decoration:none; border-bottom:1px solid var(--line-strong); }
  .statement-foot a:hover{ color:var(--gold); border-color:var(--gold); }

  section{ padding:76px 0; }
  section.alt{ background:var(--paper-deep); }
  .section-head{ display:flex; align-items:baseline; gap:16px; margin-bottom:40px; }
  .section-head .idx{ font-family:'IBM Plex Mono', monospace; color:var(--gold); font-size:0.85rem; }
  .section-head h2{ font-size:1.7rem; }
  .section-rule{ flex:1; height:1px; background:var(--line-strong); margin-left:8px; }

  .summary-text{ max-width:70ch; font-size:1.08rem; color:var(--ink-soft); }
  .summary-text strong{ color:var(--ink); font-weight:600; }

  /* ---------- EXPERIENCE ---------- */
  .entry{
    display:grid;
    grid-template-columns:170px 1fr;
    gap:28px;
    padding:26px 0;
    border-top:1px solid var(--line);
  }
  .entry:last-child{ border-bottom:1px solid var(--line); }
  .entry-date{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem;
    color:var(--ink-soft);
    padding-top:4px;
  }
  .entry-role{ font-size:1.18rem; font-weight:600; font-family:'Newsreader', serif;}
  .entry-org{ color:var(--gold); font-size:0.85rem; margin-top:2px; font-family:'IBM Plex Mono', monospace; letter-spacing:0.02em;}
  .entry ul{ margin:14px 0 0; padding:0; list-style:none; }
  .entry li{
    position:relative;
    padding-left:26px;
    margin-bottom:10px;
    font-size:0.95rem;
    color:var(--ink-soft);
  }
  .entry li::before{
    content:"✓";
    position:absolute; left:0; top:0;
    color:var(--teal);
    font-family:'IBM Plex Mono', monospace;
    font-weight:600;
  }

  /* ---------- PROJECTS ---------- */
  .proj-grid{ display:grid; grid-template-columns:1fr 1fr; gap:24px; }
  .proj-card{
    background:var(--card);
    border:1px solid var(--line-strong);
    padding:26px 28px;
  }
  .proj-tag{ font-family:'IBM Plex Mono', monospace; font-size:0.72rem; color:var(--teal); text-transform:uppercase; letter-spacing:0.06em;}
  .proj-card h3{ font-size:1.2rem; margin-top:8px; }
  .proj-card ul{ margin:14px 0 0; padding:0; list-style:none; }
  .proj-card li{ position:relative; padding-left:22px; margin-bottom:9px; font-size:0.92rem; color:var(--ink-soft); }
  .proj-card li::before{ content:"—"; position:absolute; left:0; color:var(--line-strong); }

  /* ---------- SKILLS AS STAMPS ---------- */
  .stamp-grid{ display:flex; flex-wrap:wrap; gap:14px; }
  .stamp{
    border:1.5px solid var(--ink);
    color:var(--ink);
    padding:9px 16px;
    font-family:'IBM Plex Mono', monospace;
    font-size:0.8rem;
    border-radius:3px;
    position:relative;
    transform:rotate(var(--r,0deg));
  }
  .stamp:nth-child(3n){ --r:-1.3deg; border-color:var(--teal); color:var(--teal); }
  .stamp:nth-child(3n+1){ --r:1deg; }
  .stamp:nth-child(3n+2){ --r:-0.6deg; border-color:var(--gold); color:var(--gold); }

  .core-skills{
    display:flex; flex-wrap:wrap; gap:10px 24px;
    margin-top:36px;
    padding-top:26px;
    border-top:1px dashed var(--line-strong);
  }
  .core-skills span{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem;
    color:var(--ink-soft);
  }
  .core-skills span::before{ content:"·"; margin-right:10px; color:var(--gold); }
  .core-skills span:first-child::before{ display:none; }

  /* ---------- CERTS / EDU ---------- */
  .two-col{ display:grid; grid-template-columns:1fr 1fr; gap:56px; }
  .list-row{
    display:flex; justify-content:space-between; gap:16px;
    padding:16px 0;
    border-top:1px solid var(--line);
    font-size:0.94rem;
  }
  .list-row:last-child{ border-bottom:1px solid var(--line); }
  .list-row .name{ color:var(--ink); }
  .list-row .meta{ color:var(--ink-soft); font-family:'IBM Plex Mono', monospace; font-size:0.78rem; white-space:nowrap; padding-top:2px;}

  .edu-block{ padding:16px 0; border-top:1px solid var(--line); }
  .edu-block:last-child{ border-bottom:1px solid var(--line); }
  .edu-block .deg{ font-weight:600; }
  .edu-block .sch{ color:var(--ink-soft); font-size:0.9rem; margin-top:2px;}
  .edu-block .yr{ font-family:'IBM Plex Mono', monospace; font-size:0.78rem; color:var(--gold); }

  /* ---------- ACHIEVEMENTS ---------- */
  .achv-list{ display:grid; gap:16px; }
  .achv{
    display:flex; gap:16px; align-items:flex-start;
    padding:18px 22px;
    background:var(--card);
    border:1px solid var(--line);
  }
  .achv .tick{ color:var(--gold); font-family:'IBM Plex Mono', monospace; font-weight:600; }

  /* ---------- FOOTER ---------- */
  footer{
    background:var(--ink);
    color:var(--paper);
    padding:56px 0 40px;
  }
  footer h2{ color:#fff; font-size:1.6rem; }
  footer .sub{ color:rgba(238,241,239,0.7); max-width:50ch; margin-top:10px; }
  .foot-links{ display:flex; flex-wrap:wrap; gap:24px 32px; margin-top:30px; }
  .foot-links a{
    text-decoration:none;
    font-family:'IBM Plex Mono', monospace;
    font-size:0.85rem;
    border-bottom:1px solid rgba(238,241,239,0.35);
    padding-bottom:3px;
  }
  .foot-links a:hover{ border-color:var(--gold); color:var(--gold); }
  .foot-bottom{
    margin-top:48px; padding-top:20px;
    border-top:1px solid rgba(238,241,239,0.15);
    font-family:'IBM Plex Mono', monospace;
    font-size:0.72rem;
    color:rgba(238,241,239,0.5);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:8px;
  }

  /* reveal on scroll */
  .reveal{ opacity:0; transform:translateY(14px); transition:opacity .6s ease, transform .6s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  @media (max-width: 780px){
    .wrap{ padding:0 20px; }
    .nav-links{ display:none; }
    .statement-head{ flex-direction:column; }
    .statement-id{ text-align:left; }
    .ledger-strip{ grid-template-columns:1fr 1fr; }
    .ledger-item{ border-bottom:1px dashed var(--line); }
    .ledger-item:nth-child(2n){ border-right:none; }
    .entry{ grid-template-columns:1fr; gap:8px; }
    .proj-grid, .two-col{ grid-template-columns:1fr; }
    .statement-head h1{ font-size:2rem; }
  }
  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    .reveal{ opacity:1; transform:none; transition:none; }
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="nav-name">Harsh Raj</div>
    <div class="nav-links">
      <a href="#summary">Summary</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#credentials">Credentials</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <div class="statement">
      <div class="statement-head">
        <div>
          <div class="eyebrow">Statement of Qualifications</div>
          <h1>Harsh Raj</h1>
          <div class="statement-role">Finance Analyst — Financial Reporting, Reconciliation &amp; Business Intelligence</div>
          <div class="seal">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 13l4 4L19 7"/></svg>
            Reconciled &amp; Verified
          </div>
        </div>
        <div class="statement-id">
          <span class="mono">Muzaffarpur, Bihar 842002</span>
          <span class="mono">+91 79922 19005</span>
          <span class="mono">raj9harsh2006@gmail.com</span>
        </div>
      </div>

      <div class="ledger-strip">
        <div class="ledger-item">
          <div class="ledger-figure"><span class="tick">✓</span>30%</div>
          <div class="ledger-label">Cut in audit error-flags after rebuilding vendor payment reconciliation</div>
        </div>
        <div class="ledger-item">
          <div class="ledger-figure"><span class="tick">✓</span>3+</div>
          <div class="ledger-label">Audit cycles at a CA firm with zero discrepancies</div>
        </div>
        <div class="ledger-item">
          <div class="ledger-figure"><span class="tick">✓</span>20–40%</div>
          <div class="ledger-label">Reduction in monthly / weekly reporting time across roles</div>
        </div>
        <div class="ledger-item">
          <div class="ledger-figure"><span class="tick">✓</span>6</div>
          <div class="ledger-label">Industry certifications completed in under 2 years</div>
        </div>
      </div>

      <div class="statement-foot">
        <a href="https://linkedin.com/in/harsh-raj-a0b5622b5" target="_blank" rel="noopener">linkedin.com/in/harsh-raj-a0b5622b5</a>
        <span>BBA Finance — Expected 2026</span>
        <span>Tools: Tally · Excel (Advanced) · Power BI · Tableau · SQL</span>
      </div>
    </div>
  </div>
</header>

<section id="summary">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">01</span>
      <h2>Summary</h2>
      <div class="section-rule"></div>
    </div>
    <p class="summary-text reveal">
      Finance analyst with audit and reconciliation experience across <strong>3+ audit cycles</strong> at a CA firm —
      rebuilt vendor payment reconciliation in Excel, cutting audit error-flags <strong>30%</strong> and monthly reporting
      time <strong>20%</strong>. Currently completing a <strong>BBA in Finance</strong> (expected 2026). Strong in Tally
      reconciliation, Advanced Excel (VLOOKUP, INDEX-MATCH, Pivot Tables), and Power BI / Tableau reporting.
    </p>
  </div>
</section>

<section id="experience" class="alt">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">02</span>
      <h2>Internship &amp; Work Experience</h2>
      <div class="section-rule"></div>
    </div>

    <div class="entry reveal">
      <div class="entry-date">Jul – Aug 2025</div>
      <div>
        <div class="entry-role">Data Operations &amp; Audit Assistant (Internship)</div>
        <div class="entry-org">Sanjeev Kumar and Associates — CA Firm · Sanjeev Kumar (CA)</div>
        <ul>
          <li>Cut audit error-flags 30% by rebuilding vendor payment reconciliation in Excel — replaced manual cross-checks with VLOOKUP-based templates the whole team still uses.</li>
          <li>Cut monthly reporting time 20% with Tableau dashboards that gave partners a live view of invoice and cost trends instead of static spreadsheets.</li>
          <li>Zero discrepancies across 3 audit cycles reconciling procurement and vendor data in Tally — the firm's cleanest audit run that year.</li>
        </ul>
      </div>
    </div>

    <div class="entry reveal">
      <div class="entry-date">Jun 2025</div>
      <div>
        <div class="entry-role">Data Analytics Job Simulation (Virtual Internship)</div>
        <div class="entry-org">Deloitte</div>
        <ul>
          <li>Delivered 4 business insight recommendations, as measured by project evaluation scores, by completing a real-world data analytics simulation focused on financial and demand trend analysis.</li>
          <li>Improved data accuracy by 25%, as measured by pre- and post-cleaning dataset quality metrics, by applying INDEX-MATCH and Pivot Table techniques to cleanse and analyse multi-source financial and logistics datasets.</li>
        </ul>
      </div>
    </div>

    <div class="entry reveal">
      <div class="entry-date">Jun – Jul 2024</div>
      <div>
        <div class="entry-role">Vendor &amp; Campaign Operations (Internship)</div>
        <div class="entry-org">Fintech Shine Pvt. Ltd.</div>
        <ul>
          <li>Built an Excel Pivot Table tracker replacing manual weekly reporting, cutting reporting time 40% and giving stakeholders same-day visibility instead of end-of-week.</li>
          <li>Coordinated 3+ vendor teams across a live campaign, hitting 100% of delivery deadlines.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">03</span>
      <h2>Academic Projects</h2>
      <div class="section-rule"></div>
    </div>
    <div class="proj-grid">
      <div class="proj-card reveal">
        <div class="proj-tag">Excel / Power BI</div>
        <h3>Cost &amp; Supply Chain Analysis</h3>
        <ul>
          <li>Identified 4 critical cost and process bottlenecks via root-cause analysis of 500+ inventory and logistics records, using INDEX-MATCH and HLOOKUP to map costs against demand data.</li>
          <li>Proposed a vendor consolidation strategy projected to cut process costs by an estimated 18%, benchmarking supplier lead times and procurement cycle data.</li>
          <li>Communicated findings to 3 stakeholder groups via a Power BI report visualising logistics costs, inventory turnover, and demand variance trends.</li>
        </ul>
      </div>
      <div class="proj-card reveal">
        <div class="proj-tag">Power BI</div>
        <h3>HR Analytics Dashboard</h3>
        <ul>
          <li>Reduced HR reporting effort by 50% by developing a Power BI dashboard tracking attrition, workforce distribution, and performance KPIs for 200+ employee records.</li>
          <li>Surfaced 3 high-impact attrition risk segments via department-level drill-down analysis using slicers and dynamic filters.</li>
          <li>Generated 5 strategic HR recommendations by translating raw workforce data into actionable insights using DAX measures.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="skills" class="alt">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">04</span>
      <h2>Technical Skills</h2>
      <div class="section-rule"></div>
    </div>
    <div class="stamp-grid reveal">
      <div class="stamp">Tally — Bookkeeping &amp; Reconciliation</div>
      <div class="stamp">Excel — VLOOKUP / HLOOKUP / INDEX-MATCH</div>
      <div class="stamp">Excel — Pivot Tables &amp; DAX</div>
      <div class="stamp">Power BI</div>
      <div class="stamp">Tableau</div>
      <div class="stamp">SQL — Basic</div>
      <div class="stamp">Financial Reporting</div>
      <div class="stamp">Vendor Payment Reconciliation</div>
      <div class="stamp">Audit Support</div>
      <div class="stamp">Budgeting &amp; Variance Analysis</div>
      <div class="stamp">ERP Fundamentals</div>
      <div class="stamp">Dashboard Development</div>
    </div>
    <div class="core-skills reveal">
      <span>Financial Reporting &amp; Analysis</span>
      <span>Reconciliation &amp; Audit Support</span>
      <span>Budgeting &amp; Variance Analysis</span>
      <span>Vendor &amp; Procurement Data</span>
      <span>KPI &amp; Dashboard Reporting</span>
      <span>Data Verification &amp; QA</span>
    </div>
  </div>
</section>

<section id="credentials">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">05</span>
      <h2>Certifications &amp; Education</h2>
      <div class="section-rule"></div>
    </div>
    <div class="two-col">
      <div class="reveal">
        <div class="eyebrow" style="margin-bottom:10px;">Certifications</div>
        <div class="list-row">
          <span class="name">Data Analytics Job Simulation</span>
          <span class="meta">Deloitte · Jun 2025</span>
        </div>
        <div class="list-row">
          <span class="name">iON Career Edge — Young Professional</span>
          <span class="meta">TCS · Mar 2024</span>
        </div>
        <div class="list-row">
          <span class="name">Power BI Certification</span>
          <span class="meta">Microsoft</span>
        </div>
        <div class="list-row">
          <span class="name">Tableau Certification</span>
          <span class="meta">Tableau</span>
        </div>
      </div>
      <div class="reveal">
        <div class="eyebrow" style="margin-bottom:10px;">Education</div>
        <div class="edu-block">
          <div class="deg">BBA — Finance</div>
          <div class="sch">Uttaranchal University, Dehradun, India</div>
          <div class="yr">Expected 2026</div>
        </div>
        <div class="edu-block">
          <div class="deg">Senior Secondary — Science (PCM)</div>
          <div class="sch">St. Xavier's Jr/Sr School, Muzaffarpur, Bihar</div>
          <div class="yr">2021 – 2023</div>
        </div>
        <div class="edu-block">
          <div class="deg">Secondary — Science</div>
          <div class="sch">St. Xavier's Jr/Sr School, Muzaffarpur, Bihar</div>
          <div class="yr">2020 – 2021</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="alt">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="idx">06</span>
      <h2>Achievements &amp; Extracurricular</h2>
      <div class="section-rule"></div>
    </div>
    <div class="achv-list">
      <div class="achv reveal"><span class="tick">✓</span><span>Completed 6 industry certifications across finance-adjacent SCM, data analytics, and digital marketing within 2 years, demonstrating consistent self-directed upskilling.</span></div>
      <div class="achv reveal"><span class="tick">✓</span><span>Selected for the Deloitte Data Analytics Job Simulation — a competitive virtual programme focused on real-world business and financial analytics problem-solving.</span></div>
      <div class="achv reveal"><span class="tick">✓</span><span>Led a cross-functional team of 4 in a university case study, delivering a cost-optimisation and demand forecasting proposal to faculty evaluators.</span></div>
      <div class="achv reveal"><span class="tick">✓</span><span>Recognised by TCS iON as a Young Professional — completed training in professional skills, business communication, and data-driven decision-making frameworks.</span></div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <h2>Let's reconcile the details.</h2>
    <p class="sub">Open to finance analyst, reporting, and reconciliation roles. English &amp; Hindi.</p>
    <div class="foot-links">
      <a href="mailto:raj9harsh2006@gmail.com">raj9harsh2006@gmail.com</a>
      <a href="tel:+917992219005">+91 79922 19005</a>
      <a href="https://linkedin.com/in/harsh-raj-a0b5622b5" target="_blank" rel="noopener">LinkedIn</a>
      <span>Muzaffarpur, Bihar 842002</span>
    </div>
    <div class="foot-bottom">
      <span>Harsh Raj — Finance Analyst</span>
      <span>Statement generated 2026</span>
    </div>
  </div>
</footer>

<script>
  const els = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{
      if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); }
    });
  }, { threshold: 0.15 });
  els.forEach(el=> io.observe(el));
</script>

</body>
</html>
