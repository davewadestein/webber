<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Dave Wade-Stein | Freelance Technical Instructor</title>
  <meta name="description" content="Freelance technical instructor for Python, data, and analytics teams. Fast onboarding, hands-on workshops, measurable outcomes." />
  <style>
    :root{
      --bg:#0b1020; --panel:#111a33; --card:#0f1730;
      --text:#eaf0ff; --muted:#b8c4ffcc; --soft:#8ea2ff55;
      --accent:#7aa2ff; --accent2:#7dffcf; --danger:#ff7a7a;
      --radius:18px;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --max: 1080px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:var(--sans);
      background: radial-gradient(1200px 700px at 20% 10%, rgba(122,162,255,.25), transparent 55%),
                  radial-gradient(1000px 700px at 85% 15%, rgba(125,255,207,.18), transparent 50%),
                  linear-gradient(180deg, var(--bg), #070a14 70%);
      color:var(--text);
      line-height:1.45;
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:var(--max); margin:0 auto; padding:28px 18px 64px;}
    header{
      display:flex; align-items:center; justify-content:space-between;
      gap:14px; padding:10px 0 22px;
    }
    .brand{display:flex; align-items:center; gap:12px;}
    .logo{
      width:40px; height:40px; border-radius:12px;
      background: linear-gradient(135deg, rgba(122,162,255,.9), rgba(125,255,207,.8));
      box-shadow: var(--shadow);
    }
    .brand strong{display:block; font-size:14px; letter-spacing:.2px}
    .brand span{display:block; font-size:12px; color:var(--muted)}
    nav{display:flex; gap:14px; flex-wrap:wrap; justify-content:flex-end}
    nav a{
      font-size:13px; color:var(--muted);
      padding:8px 10px; border-radius:12px;
      border:1px solid transparent;
    }
    nav a:hover{border-color:var(--soft); color:var(--text)}
    .hero{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap:18px;
      align-items:stretch;
      margin-top:10px;
    }
    @media (max-width: 900px){ .hero{grid-template-columns:1fr} }
    .panel{
      background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border: 1px solid rgba(255,255,255,.08);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding:22px;
      overflow:hidden;
      position:relative;
    }
    .panel:before{
      content:"";
      position:absolute; inset:-2px;
      background: radial-gradient(600px 200px at 20% 0%, rgba(122,162,255,.20), transparent 60%),
                  radial-gradient(500px 200px at 80% 0%, rgba(125,255,207,.14), transparent 55%);
      pointer-events:none;
      filter: blur(2px);
    }
    .panel > *{position:relative}
    h1{
      margin:0 0 10px;
      font-size: clamp(28px, 4vw, 44px);
      letter-spacing:-.5px;
      line-height:1.08;
    }
    .sub{
      margin:0 0 16px;
      color:var(--muted);
      font-size:16px;
      max-width:60ch;
    }
    .tagrow{display:flex; gap:10px; flex-wrap:wrap; margin:14px 0 0}
    .tag{
      font-size:12px;
      padding:7px 10px;
      border-radius:999px;
      background: rgba(122,162,255,.12);
      border:1px solid rgba(122,162,255,.25);
      color: #dbe6ff;
    }
    .ctaRow{display:flex; gap:10px; flex-wrap:wrap; margin-top:18px}
    .btn{
      display:inline-flex; align-items:center; justify-content:center; gap:10px;
      padding:11px 14px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.06);
      color:var(--text);
      font-weight:600;
      font-size:14px;
      cursor:pointer;
      transition: transform .08s ease, background .12s ease, border-color .12s ease;
    }
    .btn:hover{transform: translateY(-1px); border-color: rgba(255,255,255,.22)}
    .btn.primary{
      background: linear-gradient(135deg, rgba(122,162,255,.95), rgba(125,255,207,.65));
      border-color: transparent;
      color:#071023;
    }
    .btn.primary:hover{filter:saturate(1.1)}
    .fine{font-size:12px; color:var(--muted); margin-top:10px}
    .kpi{
      display:grid; grid-template-columns:1fr 1fr;
      gap:12px; margin-top:6px;
    }
    .k{
      background: rgba(10,16,33,.55);
      border:1px solid rgba(255,255,255,.09);
      border-radius: 16px;
      padding:14px;
    }
    .k strong{display:block; font-size:18px}
    .k span{display:block; color:var(--muted); font-size:12px; margin-top:3px}
    .mono{font-family:var(--mono)}
    section{margin-top:22px}
    .grid3{display:grid; grid-template-columns:repeat(3,1fr); gap:12px}
    @media (max-width: 900px){ .grid3{grid-template-columns:1fr} }
    .card{
      background: rgba(10,16,33,.55);
      border:1px solid rgba(255,255,255,.09);
      border-radius: var(--radius);
      padding:16px;
      box-shadow: 0 10px 24px rgba(0,0,0,.20);
    }
    .card h3{margin:0 0 8px; font-size:16px}
    .card p{margin:0; color:var(--muted); font-size:13px}
    .list{margin:10px 0 0; padding-left:18px; color:var(--muted); font-size:13px}
    .list li{margin:6px 0}
    .split{
      display:grid; grid-template-columns:1fr 1fr; gap:12px;
    }
    @media (max-width: 900px){ .split{grid-template-columns:1fr} }

    form{display:grid; gap:10px; margin-top:10px}
    input, textarea, select{
      width:100%;
      padding:12px 12px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background: rgba(255,255,255,.06);
      color: var(--text);
      outline: none;
      font-size:14px;
    }
    textarea{min-height:120px; resize:vertical}
    label{font-size:12px; color:var(--muted)}
    .row2{display:grid; grid-template-columns:1fr 1fr; gap:10px}
    @media (max-width: 700px){ .row2{grid-template-columns:1fr} }
    footer{
      margin-top:28px;
      padding-top:18px;
      border-top:1px solid rgba(255,255,255,.10);
      color:var(--muted);
      font-size:12px;
      display:flex; justify-content:space-between; gap:12px; flex-wrap:wrap;
    }
    .pill{
      display:inline-flex; align-items:center; gap:8px;
      padding:7px 10px; border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.04);
    }
  </style>
</head>

<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <strong>Dave Wade-Stein</strong>
          <span>Freelance Technical Instructor • Python • Data • Analytics</span>
        </div>
      </div>

      <nav aria-label="Site">
        <a href="#services">Services</a>
        <a href="#process">Process</a>
        <a href="#proof">Proof</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <div class="hero">
      <div class="panel">
        <h1>Hands-on training that gets teams productive fast.</h1>
        <p class="sub">
          I design and deliver practical workshops for engineering, analytics, and data teams—focused on
          usable skills, real examples, and measurable outcomes.
        </p>

        <div class="ctaRow">
          <a class="btn primary" href="#contact">Book a 20-minute call</a>
          <a class="btn" href="#services">See training options</a>
          <!-- Replace with your LinkedIn / calendar link -->
          <a class="btn" href="https://www.linkedin.com/" target="_blank" rel="noreferrer">LinkedIn</a>
        </div>
        <div class="fine">
          Typical engagements: 1–2 day workshops • 3–6 week upskilling series • custom team enablement
        </div>

        <div class="tagrow" aria-label="Topics">
          <span class="tag">Python fundamentals → mastery</span>
          <span class="tag">Pandas / NumPy</span>
          <span class="tag">APIs & automation</span>
          <span class="tag">PySpark / big data</span>
          <span class="tag">ML basics</span>
          <span class="tag">LLMs for productivity</span>
        </div>
      </div>

      <div class="panel">
        <h2 style="margin:0 0 8px; font-size:18px;">Quick snapshot</h2>
        <p class="sub" style="margin:0 0 14px;">
          Ideal for teams who want less theory, more “I can do this tomorrow.”
        </p>

        <div class="kpi">
          <div class="k">
            <strong>Instructor-led</strong>
            <span>Live, interactive, Q&A-heavy</span>
          </div>
          <div class="k">
            <strong>Outcome-based</strong>
            <span>Skills check + artifacts delivered</span>
          </div>
          <div class="k">
            <strong class="mono">~70%</strong>
            <span>Hands-on time (typical)</span>
          </div>
          <div class="k">
            <strong>Remote / onsite</strong>
            <span>Colorado + travel</span>
          </div>
        </div>

        <div class="fine">
          Replace these metrics with your real stats (classes taught, satisfaction, teams trained, etc.).
        </div>
      </div>
    </div>

    <section id="services" class="panel" aria-label="Services">
      <h2 style="margin:0 0 10px;">Services</h2>
      <div class="grid3">
        <div class="card">
          <h3>1–2 Day Workshops</h3>
          <p>Fast skill lift with exercises your team can reuse.</p>
          <ul class="list">
            <li>Python for analysts / engineers</li>
            <li>Data wrangling with Pandas</li>
            <li>APIs, automation, and testing basics</li>
          </ul>
        </div>

        <div class="card">
          <h3>Upskilling Series</h3>
          <p>Weekly sessions + office hours + practice plan.</p>
          <ul class="list">
            <li>3–6 weeks, 60–120 min/week</li>
            <li>Assignments + code review</li>
            <li>Manager visibility into progress</li>
          </ul>
        </div>

        <div class="card">
          <h3>Team Enablement</h3>
          <p>Tailored training for your stack and workflows.</p>
          <ul class="list">
            <li>Custom notebooks & reference guides</li>
            <li>Capstone aligned to your data</li>
            <li>Playbooks & reusable templates</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="process" class="panel" aria-label="Process">
      <h2 style="margin:0 0 10px;">How it works</h2>
      <div class="split">
        <div class="card">
          <h3>1) Quick discovery (20 minutes)</h3>
          <p>Audience, current skill level, and what “success” looks like.</p>
          <ul class="list">
            <li>Who’s attending and why?</li>
            <li>What must change after training?</li>
            <li>Constraints: time, tools, data sensitivity</li>
          </ul>
        </div>
        <div class="card">
          <h3>2) Proposal in plain English</h3>
          <p>Agenda, outcomes, prerequisites, and pricing—no fluff.</p>
          <ul class="list">
            <li>Recommended format + options</li>
            <li>Deliverables (slides, labs, rubrics)</li>
            <li>Logistics (remote/onsite, recording, etc.)</li>
          </ul>
        </div>
        <div class="card">
          <h3>3) Delivery + artifacts</h3>
          <p>Interactive sessions + hands-on labs + Q&A.</p>
          <ul class="list">
            <li>Exercises + solutions</li>
            <li>Reference notebooks</li>
            <li>Optional: assessment + report-out</li>
          </ul>
        </div>
        <div class="card">
          <h3>4) Follow-through</h3>
          <p>Optional office hours and a practical next-steps plan.</p>
          <ul class="list">
            <li>Office hours / code review</li>
            <li>Team “do this next” checklist</li>
            <li>Manager-friendly summary</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="proof" class="panel" aria-label="Proof">
      <h2 style="margin:0 0 10px;">Proof</h2>
      <div class="grid3">
        <div class="card">
          <h3>Testimonial</h3>
          <p>“Add a short quote here about clarity, pacing, and practical takeaways.”</p>
          <p class="fine">— Name, Title, Company</p>
        </div>
        <div class="card">
          <h3>Case result</h3>
          <p>“Example: reduced onboarding time for analysts by X weeks after a Python + data series.”</p>
          <p class="fine">Keep it specific and measurable.</p>
        </div>
        <div class="card">
          <h3>Credibility</h3>
          <p>List credentials: years teaching, platforms, notable clients, etc.</p>
          <p class="fine">Avoid buzzwords; use concrete facts.</p>
        </div>
      </div>
    </section>

    <section id="contact" class="panel" aria-label="Contact">
      <h2 style="margin:0 0 10px;">Contact</h2>
      <p class="sub" style="margin-top:0;">
        Tell me a bit about your team and what you want them to be able to do. I’ll respond with next steps.
      </p>

      <!-- UPDATE THIS EMAIL -->
      <div class="pill" style="margin:8px 0 14px;">
        <span aria-hidden="true">✉️</span>
        <span class="mono">you@example.com</span>
        <span style="opacity:.8;">(replace this)</span>
      </div>

      <form id="leadForm">
        <div class="row2">
          <div>
            <label for="name">Name</label>
            <input id="name" name="name" autocomplete="name" placeholder="Your name" required />
          </div>
          <div>
            <label for="email">Email</label>
            <input id="email" name="email" type="email" autocomplete="email" placeholder="you@company.com" required />
          </div>
        </div>

        <div class="row2">
          <div>
            <label for="company">Company</label>
            <input id="company" name="company" autocomplete="organization" placeholder="Company / team" />
          </div>
          <div>
            <label for="format">What do you want?</label>
            <select id="format" name="format">
              <option>Workshop (1–2 days)</option>
              <option>Upskilling series (3–6 weeks)</option>
              <option>Custom / unsure</option>
            </select>
          </div>
        </div>

        <div>
          <label for="message">What outcomes are you aiming for?</label>
          <textarea id="message" name="message" placeholder="Example: ‘Analysts can clean data with Pandas, write reusable functions, and automate a weekly report.’" required></textarea>
        </div>

        <div class="ctaRow">
          <button class="btn primary" type="submit">Send inquiry</button>
          <!-- Replace with Calendly/Cal.com link if you use one -->
          <a class="btn" href="#" onclick="alert('Replace this with your scheduling link (Calendly/Cal.com).'); return false;">
            Scheduling link
          </a>
        </div>

        <div id="formNote" class="fine" role="status" aria-live="polite"></div>
      </form>
    </section>

    <footer>
      <div>© <span id="year"></span> Dave Wade-Stein • Freelance Technical Instructor</div>
      <div class="pill">Built as a single static file (easy to host)</div>
    </footer>
  </div>

  <script>
    // Update footer year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Mailto lead form (simple + no backend)
    // Update to your actual email:
    const DEST_EMAIL = "you@example.com";

    const form = document.getElementById("leadForm");
    const note = document.getElementById("formNote");

    form.addEventListener("submit", (e) => {
      e.preventDefault();

      const data = new FormData(form);
      const name = (data.get("name") || "").toString().trim();
      const email = (data.get("email") || "").toString().trim();
      const company = (data.get("company") || "").toString().trim();
      const format = (data.get("format") || "").toString().trim();
      const message = (data.get("message") || "").toString().trim();

      if (!name || !email || !message) {
        note.textContent = "Please fill in name, email, and outcomes.";
        note.style.color = "var(--danger)";
        return;
      }

      const subject = encodeURIComponent(`Training inquiry (${format}) — ${company || "No company listed"}`);
      const body = encodeURIComponent(
        `Name: ${name}\n` +
        `Email: ${email}\n` +
        `Company: ${company}\n` +
        `Engagement type: ${format}\n\n` +
        `Outcomes / details:\n${message}\n`
      );

      const mailto = `mailto:${DEST_EMAIL}?subject=${subject}&body=${body}`;
      window.location.href = mailto;

      note.textContent = "Opening your email client… If it doesn't open, copy/paste your message and email me directly.";
      note.style.color = "var(--muted)";
      form.reset();
    });
  </script>
</body>
</html>
