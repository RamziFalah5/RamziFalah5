<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ramzi Abu Falah | Portfolio</title>

    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
      rel="stylesheet"
    />

    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
    />

    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      :root {
        --bg: #07111f;
        --bg2: #0c1a2f;
        --card: rgba(10, 22, 40, 0.82);
        --card-border: rgba(255, 255, 255, 0.08);
        --text: #f3f7ff;
        --muted: #aeb9d1;
        --green: #19e37d;
        --green-dark: #0f9d58;
        --cyan: #28d7ff;
        --blue: #3b82f6;
        --purple: #8b5cf6;
        --orange: #ff9d2e;
        --pink: #ff4fd8;
        --shadow: 0 20px 60px rgba(0, 0, 0, 0.45);
      }

      body {
        font-family: "Poppins", sans-serif;
        color: var(--text);
        background:
          radial-gradient(circle at top left, rgba(0, 195, 255, 0.12), transparent 30%),
          radial-gradient(circle at top right, rgba(25, 227, 125, 0.12), transparent 28%),
          linear-gradient(135deg, #020814 0%, #061120 35%, #07111f 100%);
        min-height: 100vh;
        padding: 26px;
      }

      a {
        text-decoration: none;
        color: inherit;
      }

      .container {
        max-width: 1450px;
        margin: 0 auto;
      }

      .layout {
        display: grid;
        grid-template-columns: 380px 1fr;
        gap: 26px;
        align-items: start;
      }

      .card {
        background: var(--card);
        backdrop-filter: blur(18px);
        border: 1px solid var(--card-border);
        border-radius: 28px;
        box-shadow: var(--shadow);
      }

      .sidebar {
        padding: 30px 28px;
        position: sticky;
        top: 20px;
      }

      .avatar-wrap {
        width: 100%;
        display: flex;
        justify-content: center;
        margin-bottom: 24px;
      }

      .avatar {
        width: 255px;
        height: 255px;
        border-radius: 50%;
        border: 4px solid rgba(255, 255, 255, 0.14);
        object-fit: cover;
        background: linear-gradient(135deg, #162033, #0b1322);
        display: block;
      }

      .name {
        font-size: 2.1rem;
        font-weight: 800;
        line-height: 1.1;
        text-align: left;
      }

      .username {
        margin-top: 8px;
        color: var(--muted);
        font-size: 1.1rem;
      }

      .follow-btn {
        margin: 22px 0;
        display: block;
        width: 100%;
        text-align: center;
        padding: 15px 18px;
        border-radius: 16px;
        font-weight: 700;
        font-size: 1.1rem;
        background: linear-gradient(135deg, #1d293b, #273549);
        border: 1px solid rgba(255, 255, 255, 0.08);
        transition: 0.3s ease;
      }

      .follow-btn:hover {
        transform: translateY(-2px);
        background: linear-gradient(135deg, #253449, #30455e);
      }

      .mini-role {
        font-size: 1.05rem;
        color: #e8eefc;
        margin-bottom: 18px;
        line-height: 1.8;
      }

      .stats-row {
        color: var(--muted);
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        font-size: 1rem;
        margin-bottom: 22px;
      }

      .stats-row strong {
        color: white;
      }

      .info-list {
        display: grid;
        gap: 14px;
      }

      .info-item {
        display: flex;
        align-items: center;
        gap: 12px;
        color: #eef3ff;
        font-size: 1rem;
        word-break: break-word;
      }

      .info-item i {
        width: 22px;
        text-align: center;
        color: #c9d7f5;
        font-size: 1.1rem;
      }

      .main {
        padding: 28px;
      }

      .top-badges {
        display: flex;
        flex-wrap: wrap;
        gap: 14px;
        margin-bottom: 24px;
      }

      .rank-badge {
        display: inline-flex;
        align-items: center;
        gap: 10px;
        padding: 12px 18px;
        border-radius: 16px;
        font-weight: 700;
        font-size: 1.05rem;
        background: linear-gradient(135deg, rgba(255,255,255,0.08), rgba(255,255,255,0.04));
        border: 1px solid rgba(255,255,255,0.07);
      }

      .rank-badge i {
        font-size: 1.2rem;
      }

      .hero {
        text-align: center;
        padding: 18px 8px 10px;
        border-top: 1px solid rgba(255,255,255,0.08);
        border-bottom: 1px solid rgba(255,255,255,0.08);
      }

      .hero h1 {
        font-size: clamp(2rem, 4vw, 3.4rem);
        font-weight: 800;
        margin-bottom: 18px;
      }

      .hero p {
        font-size: clamp(1rem, 2vw, 1.35rem);
        color: #ebf3ff;
        font-weight: 600;
        line-height: 1.9;
      }

      .hero .accent {
        color: var(--green);
      }

      .cta-text {
        font-size: 2rem;
        font-weight: 800;
        color: #17ff6d;
        margin: 28px 0 18px;
        text-align: center;
      }

      .cta-buttons {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 16px;
        margin-bottom: 28px;
      }

      .cta-buttons a {
        padding: 14px 24px;
        border-radius: 16px;
        font-size: 1.05rem;
        font-weight: 700;
        color: white;
        border: 1px solid rgba(255,255,255,0.08);
        box-shadow: 0 10px 25px rgba(0,0,0,0.25);
        transition: 0.3s ease;
      }

      .cta-buttons a:hover {
        transform: translateY(-3px) scale(1.02);
      }

      .btn-green {
        background: linear-gradient(135deg, #0f9d58, #18c76f);
      }

      .btn-blue {
        background: linear-gradient(135deg, #2563eb, #3b82f6);
      }

      .btn-purple {
        background: linear-gradient(135deg, #6d28d9, #8b5cf6);
      }

      .section {
        margin-top: 28px;
      }

      .section-title {
        display: flex;
        align-items: center;
        gap: 12px;
        font-size: 1.8rem;
        font-weight: 800;
        margin-bottom: 22px;
      }

      .section-title i {
        color: #ffb627;
      }

      .social-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(135px, 1fr));
        gap: 16px;
      }

      .social-card {
        min-height: 118px;
        border-radius: 22px;
        padding: 18px 16px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 10px;
        text-align: center;
        border: 1px solid rgba(255,255,255,0.08);
        transition: 0.3s ease;
        position: relative;
        overflow: hidden;
      }

      .social-card::before {
        content: "";
        position: absolute;
        inset: 0;
        background: linear-gradient(135deg, rgba(255,255,255,0.10), transparent);
        opacity: 0.9;
      }

      .social-card > * {
        position: relative;
        z-index: 1;
      }

      .social-card i {
        font-size: 2rem;
      }

      .social-card span {
        font-size: 0.95rem;
        font-weight: 700;
        line-height: 1.5;
        word-break: break-word;
      }

      .social-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 18px 32px rgba(0,0,0,0.28);
      }

      .email-bg {
        background: linear-gradient(135deg, #ea4335, #ff8a65);
      }

      .linkedin-bg {
        background: linear-gradient(135deg, #0077b5, #1da1f2);
      }

      .whatsapp-bg {
        background: linear-gradient(135deg, #10b981, #25d366);
      }

      .github-bg {
        background: linear-gradient(135deg, #111827, #374151);
      }

      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
        gap: 16px;
      }

      .skill-box {
        border-radius: 22px;
        padding: 18px 12px;
        text-align: center;
        background: linear-gradient(135deg, rgba(255,255,255,0.08), rgba(255,255,255,0.03));
        border: 1px solid rgba(255,255,255,0.08);
        transition: 0.3s ease;
      }

      .skill-box:hover {
        transform: translateY(-4px);
      }

      .skill-box i {
        font-size: 2.15rem;
        margin-bottom: 12px;
      }

      .skill-box h3 {
        font-size: 1rem;
        font-weight: 700;
      }

      .c1 i { color: #3b82f6; }
      .c2 i { color: #8b5cf6; }
      .c3 i { color: #6b21a8; }
      .c4 i { color: #38bdf8; }
      .c5 i { color: #f97316; }
      .c6 i { color: #7c3aed; }
      .c7 i { color: #facc15; }
      .c8 i { color: #22c55e; }

      .achievements-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 18px;
      }

      .achievement {
        border-radius: 22px;
        padding: 22px 18px;
        background: linear-gradient(135deg, rgba(255,255,255,0.07), rgba(255,255,255,0.03));
        border: 1px solid rgba(255,255,255,0.08);
        text-align: center;
        transition: 0.3s ease;
      }

      .achievement:hover {
        transform: translateY(-5px);
      }

      .achievement .icon {
        width: 72px;
        height: 72px;
        margin: 0 auto 14px;
        border-radius: 50%;
        display: grid;
        place-items: center;
        font-size: 1.9rem;
        color: white;
      }

      .achievement h3 {
        font-size: 1.1rem;
        margin-bottom: 8px;
      }

      .achievement p {
        color: var(--muted);
        font-size: 0.95rem;
        line-height: 1.7;
      }

      .gold { background: linear-gradient(135deg, #f59e0b, #facc15); }
      .green { background: linear-gradient(135deg, #10b981, #22c55e); }
      .blue { background: linear-gradient(135deg, #2563eb, #38bdf8); }
      .purple { background: linear-gradient(135deg, #7c3aed, #c026d3); }

      .bottom-banner {
        margin-top: 30px;
        padding: 18px 22px;
        border-radius: 18px;
        background: linear-gradient(90deg, rgba(0,255,136,0.16), rgba(0,170,255,0.12));
        border: 1px solid rgba(255,255,255,0.08);
        color: #f0f8ff;
        text-align: center;
        font-weight: 700;
        letter-spacing: 0.4px;
      }

      @media (max-width: 1080px) {
        .layout {
          grid-template-columns: 1fr;
        }

        .sidebar {
          position: static;
        }
      }

      @media (max-width: 640px) {
        body {
          padding: 14px;
        }

        .sidebar,
        .main {
          padding: 20px 16px;
        }

        .avatar {
          width: 210px;
          height: 210px;
        }

        .name {
          font-size: 1.8rem;
        }

        .section-title {
          font-size: 1.4rem;
        }

        .cta-text {
          font-size: 1.55rem;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="layout">
        <aside class="sidebar card">
          <div class="avatar-wrap">
            <!-- بدل الصورة هاي بصورتك -->
            <img
              class="avatar"
              src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=900&q=80"
              alt="Ramzi Abu Falah"
            />
          </div>

          <h2 class="name">Ramzi Abu Falah</h2>
          <p class="username">Ramzi • ✨</p>

          <a href="#" class="follow-btn">Follow</a>

          <p class="mini-role">
            Computer Science Student | Full Stack Developer
          </p>

          <div class="stats-row">
            <span><strong>Problem Solving</strong></span>
            <span>•</span>
            <span><strong>Web Development</strong></span>
          </div>

          <div class="info-list">
            <div class="info-item">
              <i class="fa-solid fa-graduation-cap"></i>
              <span>Birzeit University</span>
            </div>

            <div class="info-item">
              <i class="fa-solid fa-location-dot"></i>
              <span>Palestine</span>
            </div>

            <div class="info-item">
              <i class="fa-solid fa-envelope"></i>
              <span>1230594@student.birzeit.edu</span>
            </div>

            <div class="info-item">
              <i class="fa-brands fa-linkedin"></i>
              <a
                href="https://www.linkedin.com/in/ramzi-abufalah-a8a019382?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app"
                target="_blank"
              >
                LinkedIn Profile
              </a>
            </div>

            <div class="info-item">
              <i class="fa-brands fa-whatsapp"></i>
              <a href="https://wa.me/972569770594" target="_blank">
                +972 56 977 0594
              </a>
            </div>
          </div>
        </aside>

        <main class="main card">
          <div class="top-badges">
            <a
              class="rank-badge"
              href="https://gh-most-followed.pages.dev/palestine"
              target="_blank"
            >
              <i class="fa-brands fa-github"></i>
              <span>Most Followed Users - Palestine</span>
            </a>

            <a
              class="rank-badge"
              href="https://committers.top/palestine"
              target="_blank"
            >
              <i class="fa-solid fa-trophy"></i>
              <span>Top Committers - Palestine</span>
            </a>
          </div>

          <section class="hero">
            <h1>Hi, I'm <span class="accent">Ramzi Abu Falah</span></h1>
            <p>
              Computer Science Student | Full Stack Developer | Problem Solver
            </p>
          </section>

          <div class="cta-text">Check My Profiles</div>

          <div class="cta-buttons">
            <a
              class="btn-green"
              href="https://www.linkedin.com/in/ramzi-abufalah-a8a019382?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app"
              target="_blank"
            >
              <i class="fa-brands fa-linkedin"></i> My LinkedIn
            </a>

            <a
              class="btn-blue"
              href="mailto:1230594@student.birzeit.edu"
              target="_blank"
            >
              <i class="fa-solid fa-envelope"></i> My Email
            </a>

            <a
              class="btn-purple"
              href="https://wa.me/972569770594"
              target="_blank"
            >
              <i class="fa-brands fa-whatsapp"></i> WhatsApp
            </a>
          </div>

          <section class="section">
            <h2 class="section-title">
              <i class="fa-solid fa-map-pin"></i>
              My Social Accounts
            </h2>

            <div class="social-grid">
              <a
                class="social-card email-bg"
                href="mailto:1230594@student.birzeit.edu"
                target="_blank"
              >
                <i class="fa-solid fa-envelope"></i>
                <span>Student Email</span>
              </a>

              <a
                class="social-card linkedin-bg"
                href="https://www.linkedin.com/in/ramzi-abufalah-a8a019382?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app"
                target="_blank"
              >
                <i class="fa-brands fa-linkedin-in"></i>
                <span>LinkedIn</span>
              </a>

              <a
                class="social-card whatsapp-bg"
                href="https://wa.me/972569770594"
                target="_blank"
              >
                <i class="fa-brands fa-whatsapp"></i>
                <span>WhatsApp</span>
              </a>

              <a
                class="social-card github-bg"
                href="https://committers.top/palestine"
                target="_blank"
              >
                <i class="fa-brands fa-github"></i>
                <span>GitHub Related</span>
              </a>
            </div>
          </section>

          <section class="section">
            <h2 class="section-title">
              <i class="fa-solid fa-screwdriver-wrench"></i>
              Top Technical Skills & Tools
            </h2>

            <div class="skills-grid">
              <div class="skill-box c1">
                <i class="fa-brands fa-html5"></i>
                <h3>HTML5</h3>
              </div>

              <div class="skill-box c2">
                <i class="fa-brands fa-css3-alt"></i>
                <h3>CSS3</h3>
              </div>

              <div class="skill-box c3">
                <i class="fa-brands fa-js"></i>
                <h3>JavaScript</h3>
              </div>

              <div class="skill-box c4">
                <i class="fa-brands fa-react"></i>
                <h3>React</h3>
              </div>

              <div class="skill-box c5">
                <i class="fa-solid fa-database"></i>
                <h3>SQL</h3>
              </div>

              <div class="skill-box c6">
                <i class="fa-brands fa-git-alt"></i>
                <h3>Git</h3>
              </div>

              <div class="skill-box c7">
                <i class="fa-solid fa-lightbulb"></i>
                <h3>Problem Solving</h3>
              </div>

              <div class="skill-box c8">
                <i class="fa-solid fa-laptop-code"></i>
                <h3>Full Stack</h3>
              </div>
            </div>
          </section>

          <section class="section">
            <h2 class="section-title">
              <i class="fa-solid fa-trophy"></i>
              Achievements
            </h2>

            <div class="achievements-grid">
              <div class="achievement">
                <div class="icon gold">
                  <i class="fa-solid fa-code"></i>
                </div>
                <h3>Problem Solving</h3>
                <p>
                  Strong analytical thinking and solid experience solving coding
                  and algorithmic problems.
                </p>
              </div>

              <div class="achievement">
                <div class="icon green">
                  <i class="fa-solid fa-layer-group"></i>
                </div>
                <h3>Full Stack Path</h3>
                <p>
                  Building modern web interfaces and working toward complete
                  full stack development.
                </p>
              </div>

              <div class="achievement">
                <div class="icon blue">
                  <i class="fa-solid fa-graduation-cap"></i>
                </div>
                <h3>Computer Science</h3>
                <p>
                  Academic background in Computer Science with focus on software,
                  logic, and system thinking.
                </p>
              </div>

              <div class="achievement">
                <div class="icon purple">
                  <i class="fa-solid fa-rocket"></i>
                </div>
                <h3>Portfolio Growth</h3>
                <p>
                  Actively improving projects, coding skills, and professional
                  online presence.
                </p>
              </div>
            </div>
          </section>

          <div class="bottom-banner">
            Designed with passion for clean code, strong UI, and real growth.
          </div>
        </main>
      </div>
    </div>
  </body>
</html>
