<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>GitHub Profile · Abrham Asrat</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
    <style>
        /* ── reset & base ── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #e6edf3;
        }

        .profile-card {
            max-width: 1000px;
            width: 100%;
            background: #161b22;
            border-radius: 24px;
            padding: 2.5rem 2.8rem;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);
            border: 1px solid #30363d;
            transition: all 0.2s;
        }

        /* ── typography ── */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: -0.01em;
        }

        h1 {
            font-size: 2.6rem;
            margin-bottom: 0.15rem;
            background: linear-gradient(135deg, #f0f6fc 0%, #8b949e 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subhead {
            font-size: 1.1rem;
            color: #8b949e;
            font-weight: 400;
            margin-bottom: 0.5rem;
        }

        .tagline {
            font-size: 1.05rem;
            color: #c9d1d9;
            margin-bottom: 1.5rem;
            border-left: 3px solid #58a6ff;
            padding-left: 1rem;
            background: rgba(88, 166, 255, 0.05);
            border-radius: 0 8px 8px 0;
        }

        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin: 2rem 0 1rem 0;
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: #f0f6fc;
            border-bottom: 1px solid #30363d;
            padding-bottom: 0.5rem;
        }

        .section-title i {
            color: #58a6ff;
            font-size: 1.2rem;
            width: 1.6rem;
            text-align: center;
        }

        /* ── badges ── */
        .badge-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem 0.9rem;
            margin: 0.8rem 0 0.2rem 0;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            background: #21262d;
            padding: 0.3rem 0.9rem 0.3rem 0.7rem;
            border-radius: 40px;
            font-size: 0.8rem;
            color: #c9d1d9;
            border: 1px solid #30363d;
            transition: 0.15s;
            text-decoration: none;
        }

        .badge i {
            font-size: 0.85rem;
            color: #58a6ff;
        }

        .badge:hover {
            background: #30363d;
            border-color: #58a6ff;
            color: #f0f6fc;
        }

        /* ── social links ── */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem 1.8rem;
            margin: 0.8rem 0 0.2rem 0;
        }

        .social-links a {
            color: #8b949e;
            text-decoration: none;
            font-size: 0.95rem;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.15s;
            border-radius: 6px;
            padding: 0.2rem 0.4rem;
        }

        .social-links a i {
            font-size: 1.2rem;
            width: 1.4rem;
            text-align: center;
            color: #8b949e;
            transition: 0.15s;
        }

        .social-links a:hover {
            color: #f0f6fc;
        }
        .social-links a:hover i {
            color: #58a6ff;
        }

        /* ── grid: what i do ── */
        .do-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
            gap: 0.8rem 1.2rem;
            margin: 0.5rem 0 0.2rem 0;
        }

        .do-item {
            display: flex;
            align-items: flex-start;
            gap: 0.6rem;
            background: #0d1117;
            padding: 0.7rem 1rem;
            border-radius: 12px;
            border: 1px solid #21262d;
        }

        .do-item i {
            color: #58a6ff;
            font-size: 1.1rem;
            margin-top: 0.15rem;
            width: 1.4rem;
            text-align: center;
        }

        .do-item strong {
            color: #f0f6fc;
            font-weight: 600;
        }

        .do-item span {
            color: #c9d1d9;
            font-size: 0.92rem;
        }

        /* ── tech stack pills ── */
        .tech-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem 0.7rem;
            margin: 0.6rem 0 0.2rem 0;
        }

        .tech-pill {
            background: #0d1117;
            border: 1px solid #30363d;
            padding: 0.25rem 1rem 0.25rem 0.9rem;
            border-radius: 40px;
            font-size: 0.8rem;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            color: #c9d1d9;
        }

        .tech-pill i {
            color: #58a6ff;
            font-size: 0.85rem;
        }

        .tech-pill .dot {
            display: inline-block;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            margin-right: 2px;
        }
        .dot.js {
            background: #f7df1e;
        }
        .dot.ts {
            background: #3178c6;
        }
        .dot.py {
            background: #3776ab;
        }
        .dot.ng {
            background: #dd0031;
        }
        .dot.react {
            background: #61dafb;
        }
        .dot.node {
            background: #539e43;
        }
        .dot.dotnet {
            background: #512bd4;
        }
        .dot.sql {
            background: #00758f;
        }
        .dot.mongo {
            background: #47a248;
        }
        .dot.docker {
            background: #2496ed;
        }

        /* ── experience & project cards ── */
        .exp-item,
        .project-item {
            background: #0d1117;
            border-radius: 14px;
            padding: 1.1rem 1.4rem;
            margin-bottom: 0.9rem;
            border: 1px solid #21262d;
            transition: 0.15s;
        }

        .exp-item:hover,
        .project-item:hover {
            border-color: #30363d;
            background: #11161e;
        }

        .exp-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.4rem 1rem;
        }

        .exp-header h3 {
            font-size: 1.05rem;
            color: #f0f6fc;
        }

        .exp-header .company {
            color: #58a6ff;
            font-weight: 500;
        }

        .exp-header .date {
            color: #8b949e;
            font-size: 0.8rem;
            background: #21262d;
            padding: 0.1rem 0.8rem;
            border-radius: 30px;
            white-space: nowrap;
        }

        .exp-desc {
            margin-top: 0.4rem;
            padding-left: 0.2rem;
            color: #c9d1d9;
            font-size: 0.92rem;
        }

        .exp-desc ul {
            list-style: none;
            padding: 0;
        }

        .exp-desc li {
            position: relative;
            padding-left: 1.4rem;
            margin-bottom: 0.25rem;
        }

        .exp-desc li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: #58a6ff;
        }

        .project-item .proj-title {
            font-size: 1.05rem;
            font-weight: 600;
            color: #f0f6fc;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .project-item .proj-title i {
            color: #58a6ff;
            font-size: 0.9rem;
        }

        .project-item .proj-desc {
            color: #c9d1d9;
            font-size: 0.92rem;
            margin-top: 0.2rem;
        }

        .project-item .proj-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem 0.7rem;
            margin-top: 0.5rem;
        }

        .project-item .proj-tags span {
            background: #21262d;
            padding: 0.1rem 0.7rem;
            border-radius: 30px;
            font-size: 0.7rem;
            color: #8b949e;
            border: 1px solid #30363d;
        }

        /* ── education ── */
        .edu-block {
            background: #0d1117;
            border-radius: 14px;
            padding: 1.1rem 1.4rem;
            border: 1px solid #21262d;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }

        .edu-block .edu-left {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 0.3rem 1.2rem;
        }

        .edu-block .edu-left h3 {
            font-size: 1.05rem;
            color: #f0f6fc;
        }

        .edu-block .edu-left .uni {
            color: #8b949e;
            font-weight: 400;
        }

        .edu-block .edu-left .cgpa {
            background: #21262d;
            padding: 0.1rem 0.8rem;
            border-radius: 30px;
            font-size: 0.8rem;
            color: #58a6ff;
            border: 1px solid #30363d;
        }

        .edu-block .edu-right {
            color: #8b949e;
            font-size: 0.85rem;
        }

        /* ── extra (tiktok) ── */
        .extra-item {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            background: #0d1117;
            padding: 0.4rem 1.2rem 0.4rem 1rem;
            border-radius: 40px;
            border: 1px solid #21262d;
            color: #c9d1d9;
            font-size: 0.9rem;
        }

        .extra-item i {
            color: #58a6ff;
            font-size: 1.1rem;
        }

        /* ── footer / meta ── */
        .footer-note {
            margin-top: 2.2rem;
            padding-top: 1.2rem;
            border-top: 1px solid #21262d;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 0.8rem;
            font-size: 0.85rem;
            color: #8b949e;
        }

        .footer-note i {
            color: #58a6ff;
        }

        .footer-note .badge-sm {
            display: inline-flex;
            align-items: center;
            gap: 0.3rem;
            background: #21262d;
            padding: 0.15rem 0.8rem;
            border-radius: 30px;
            border: 1px solid #30363d;
            font-size: 0.75rem;
            color: #c9d1d9;
        }

        /* ── responsive ── */
        @media (max-width: 640px) {
            .profile-card {
                padding: 1.5rem 1.2rem;
            }
            h1 {
                font-size: 2rem;
            }
            .exp-header {
                flex-direction: column;
                align-items: flex-start;
            }
            .edu-block {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.5rem;
            }
            .social-links {
                gap: 0.8rem 1.2rem;
            }
        }
    </style>
</head>
<body>

    <div class="profile-card">

        <!-- ─── HEADER ─── -->
        <div style="display:flex; flex-wrap:wrap; justify-content:space-between; align-items:center; gap:0.5rem 1rem;">
            <div>
                <h1>Abrham Asrat</h1>
                <div class="subhead">
                    <i class="fas fa-code" style="color:#58a6ff; margin-right:0.3rem;"></i>
                    Full‑Stack Web Developer &bull; Software Engineer
                </div>
            </div>
            <div style="display:flex; gap:0.5rem; flex-wrap:wrap;">
                <span class="badge"><i class="fas fa-map-pin"></i> Addis Ababa, ET</span>
                <span class="badge"><i class="fas fa-briefcase"></i> Open to work</span>
            </div>
        </div>

        <!-- tagline -->
        <div class="tagline">
            <i class="fas fa-rocket" style="color:#58a6ff; margin-right:0.6rem;"></i>
            Building scalable, design‑first web apps &bull; MERN &bull; ASP.NET &bull; Python/FastAPI &bull; AI/LLM (RAG)
        </div>

        <!-- badges: followers + views -->
        <div class="badge-row">
            <a href="https://github.com/Abrham-Asrat" class="badge">
                <i class="fab fa-github"></i> @Abrham‑Asrat
            </a>
            <a href="#" class="badge">
                <i class="fas fa-users"></i> 12 followers
            </a>
            <a href="#" class="badge">
                <i class="fas fa-eye"></i> 45 profile views
            </a>
            <span class="badge"><i class="fas fa-graduation-cap"></i> B.Sc. SWE · 3.65/4.0</span>
        </div>

        <!-- social links -->
        <div class="social-links">
            <a href="https://www.linkedin.com/in/abrham-asrat-8862b8366" target="_blank">
                <i class="fab fa-linkedin-in"></i> LinkedIn
            </a>
            <a href="mailto:abrhamasrat10@gmail.com">
                <i class="fas fa-envelope"></i> Email
            </a>
            <a href="https://abrham-portfolio-ab.vercel.app/" target="_blank">
                <i class="fas fa-globe"></i> Portfolio
            </a>
            <a href="https://github.com/Abrham-Asrat" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
        </div>

        <!-- ─── WHAT I DO ─── -->
        <div class="section-title">
            <i class="fas fa-laptop-code"></i> What I Do
        </div>
        <div class="do-grid">
            <div class="do-item">
                <i class="fas fa-layer-group"></i>
                <div><strong>Full‑Stack Dev</strong><br /><span>MEAN, MERN, ASP.NET, FastAPI</span></div>
            </div>
            <div class="do-item">
                <i class="fas fa-paint-brush"></i>
                <div><strong>UI/UX Design</strong><br /><span>Accessible, design‑first experiences</span></div>
            </div>
            <div class="do-item">
                <i class="fas fa-cloud-upload-alt"></i>
                <div><strong>DevOps &amp; Deploy</strong><br /><span>Netlify, Vercel, VPS, Docker</span></div>
            </div>
            <div class="do-item">
                <i class="fas fa-brain"></i>
                <div><strong>AI / LLM</strong><br /><span>RAG, LLM integration, Python</span></div>
            </div>
        </div>

        <!-- ─── TECH STACK ─── -->
        <div class="section-title">
            <i class="fas fa-code"></i> Tech Stack
        </div>

        <div style="margin-bottom:0.3rem;"><span style="color:#8b949e; font-size:0.85rem; font-weight:500;">Languages</span></div>
        <div class="tech-pills">
            <span class="tech-pill"><span class="dot js"></span> JavaScript</span>
            <span class="tech-pill"><span class="dot ts"></span> TypeScript</span>
            <span class="tech-pill"><span class="dot py"></span> Python</span>
        </div>

        <div style="margin:0.6rem 0 0.3rem 0;"><span style="color:#8b949e; font-size:0.85rem; font-weight:500;">Frontend</span></div>
        <div class="tech-pills">
            <span class="tech-pill"><span class="dot ng"></span> Angular 19</span>
            <span class="tech-pill"><span class="dot react"></span> React.js</span>
            <span class="tech-pill"><i class="fab fa-bootstrap"></i> Bootstrap</span>
            <span class="tech-pill"><i class="fab fa-css3-alt"></i> Tailwind CSS</span>
        </div>

        <div style="margin:0.6rem 0 0.3rem 0;"><span style="color:#8b949e; font-size:0.85rem; font-weight:500;">Backend &amp; DB</span></div>
        <div class="tech-pills">
            <span class="tech-pill"><span class="dot node"></span> Node.js / Express</span>
            <span class="tech-pill"><span class="dot dotnet"></span> ASP.NET Core</span>
            <span class="tech-pill"><i class="fab fa-python"></i> Django (DRF) / FastAPI</span>
            <span class="tech-pill"><span class="dot sql"></span> PostgreSQL / MySQL / MSSQL</span>
            <span class="tech-pill"><span class="dot mongo"></span> MongoDB / Firebase</span>
        </div>

        <div style="margin:0.6rem 0 0.3rem 0;"><span style="color:#8b949e; font-size:0.85rem; font-weight:500;">DevOps &amp; Tools</span></div>
        <div class="tech-pills">
            <span class="tech-pill"><span class="dot docker"></span> Docker</span>
            <span class="tech-pill"><i class="fab fa-linux"></i> Linux</span>
            <span class="tech-pill"><i class="fab fa-git-alt"></i> Git / GitHub</span>
            <span class="tech-pill"><i class="fas fa-cloud"></i> Netlify / Vercel / VPS</span>
            <span class="tech-pill"><i class="fas fa-sync-alt"></i> CI/CD</span>
        </div>

        <!-- ─── EXPERIENCE ─── -->
        <div class="section-title">
            <i class="fas fa-briefcase"></i> Experience
        </div>

        <div class="exp-item">
            <div class="exp-header">
                <h3>Full‑Stack Engineer / Web Developer Intern</h3>
                <span class="company">CREAVERS Service PLC</span>
                <span class="date">Feb 2025 – Jun 2025</span>
            </div>
            <div class="exp-desc">
                <ul>
                    <li>Built secure auth &amp; dynamic dashboards for a large‑scale E‑Health Platform using Angular 19, ASP.NET Core Web API, and MSSQL.</li>
                    <li>Collaborated cross‑functionally to ship production features supporting real‑world clinical workflows.</li>
                </ul>
            </div>
        </div>

        <!-- ─── PROJECTS ─── -->
        <div class="section-title">
            <i class="fas fa-folder-open"></i> Key Projects
        </div>

        <!-- Med-Connect -->
        <div class="project-item">
            <div class="proj-title">
                <i class="fas fa-heartbeat"></i> Med‑Connect
                <span style="font-size:0.7rem; background:#21262d; padding:0.1rem 0.7rem; border-radius:30px; color:#58a6ff; border:1px solid #30363d;">10k+ req</span>
            </div>
            <div class="proj-desc">
                Digital healthcare platform connecting patients with verified doctors — telemedicine, secure records, peer‑reviewed insights. Cut manual admin work by ~50%.
            </div>
            <div class="proj-tags">
                <span>Angular</span><span>ASP.NET Core</span><span>MSSQL</span><span>Real‑time</span>
            </div>
        </div>

        <!-- Travel Around -->
        <div class="project-item">
            <div class="proj-title">
                <i class="fas fa-plane"></i> Travel Around — Ethiopia
            </div>
            <div class="proj-desc">
                Bilingual (English/Amharic) tour &amp; booking platform showcasing Ethiopia’s heritage. Multi‑day packages, pricing, itinerary, newsletter &amp; social integration.
            </div>
            <div class="proj-tags">
                <span>React</span><span>Node.js</span><span>MongoDB</span><span>Tailwind</span>
            </div>
        </div>

        <!-- ELIT ENT -->
        <div class="project-item">
            <div class="proj-title">
                <i class="fas fa-stethoscope"></i> ELIT ENT Center
            </div>
            <div class="proj-desc">
                Official website for a specialized ENT clinic — physician profile, service listings, and online booking engineered to handle 2k+ requests reliably.
            </div>
            <div class="proj-tags">
                <span>Angular</span><span>ASP.NET Core</span><span>MSSQL</span>
            </div>
        </div>

        <!-- Bankist + Food Recipe (compact) -->
        <div style="display:grid; grid-template-columns:1fr 1fr; gap:0.9rem; margin-top:0.9rem;">
            <div class="project-item" style="margin:0;">
                <div class="proj-title" style="font-size:0.95rem;">
                    <i class="fas fa-university"></i> Bankist UI
                </div>
                <div class="proj-desc" style="font-size:0.85rem;">
                    Minimalist digital banking interface — DOM manipulation, animations, responsive.
                </div>
                <div class="proj-tags"><span>Vanilla JS</span><span>CSS3</span></div>
            </div>
            <div class="project-item" style="margin:0;">
                <div class="proj-title" style="font-size:0.95rem;">
                    <i class="fas fa-utensils"></i> Food Recipe App
                </div>
                <div class="proj-desc" style="font-size:0.85rem;">
                    Full‑stack recipe browsing &amp; bookmarking with ingredient‑based filtering.
                </div>
                <div class="proj-tags"><span>React</span><span>Node.js</span><span>MongoDB</span></div>
            </div>
        </div>

        <!-- ─── EDUCATION ─── -->
        <div class="section-title">
            <i class="fas fa-graduation-cap"></i> Education
        </div>
        <div class="edu-block">
            <div class="edu-left">
                <h3>B.Sc. in Software Engineering</h3>
                <span class="uni">Arba Minch University</span>
                <span class="cgpa"><i class="fas fa-star" style="color:#f7df1e; font-size:0.7rem;"></i> 3.65 / 4.00</span>
            </div>
            <div class="edu-right">2021 – 2026</div>
        </div>

        <!-- ─── ADDITIONAL ─── -->
        <div class="section-title" style="margin-top:1.6rem;">
            <i class="fas fa-podcast"></i> Beyond Code
        </div>
        <div style="display:flex; flex-wrap:wrap; gap:0.8rem;">
            <span class="extra-item">
                <i class="fab fa-tiktok"></i> Tech Content Creator · TikTok
                <span style="color:#8b949e; font-size:0.75rem; background:#21262d; padding:0.1rem 0.7rem; border-radius:30px;">20k+ views</span>
            </span>
            <span class="extra-item">
                <i class="fas fa-handshake"></i> Freelance available · 20–30 hrs/week
            </span>
        </div>

        <!-- ─── FOOTER ─── -->
        <div class="footer-note">
            <span>
                <i class="fas fa-code-branch"></i> 8 public repos · 12 followers
            </span>
            <span>
                <span class="badge-sm"><i class="fas fa-check-circle" style="color:#3fb950;"></i> Available for collab</span>
                <span class="badge-sm"><i class="fas fa-file-alt"></i> <a href="#" style="color:#58a6ff; text-decoration:none;">View CV</a></span>
            </span>
        </div>

    </div>

</body>
</html>
