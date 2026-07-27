<style>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@500;600&family=Inter:wght@400;500&family=JetBrains+Mono:wght@700&display=swap');

:root {
  --graphite: #1a1d23;
  --slate: #495057;
  --equity-green: #00b894;
  --capital-blue: #0984e3;
  --revenue-gold: #fdcb6e;
  --white: #ffffff;
  --off-white: #f8f9fa;
  
  --color-bg: #ffffff;
  --color-surface: #f8f9fa;
  --color-text-primary: #1a1d23;
  --color-text-secondary: #495057;
  --color-accent-growth: #00b894;
  --color-accent-tech: #0984e3;
  --color-accent-gold: #fdcb6e;
  --color-border: #dee2e6;
  
  --font-display: 'IBM Plex Mono', monospace;
  --font-body: 'Inter', sans-serif;
  --font-data: 'JetBrains Mono', monospace;
}

@media (prefers-color-scheme: dark) {
  :root {
    --color-bg: #0d1117;
    --color-surface: #161b22;
    --color-text-primary: #f8f9fa;
    --color-text-secondary: #adb5bd;
    --color-accent-tech: #74b9ff;
    --color-border: #30363d;
  }
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: var(--color-bg);
  color: var(--color-text-primary);
  font-family: var(--font-body);
  line-height: 1.6;
}

.profile-container {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

.profile-header {
  text-align: center;
  margin-bottom: 3rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--color-border);
}

.name {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 600;
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.title {
  font-family: var(--font-body);
  font-size: 1.125rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.25rem;
}

.location {
  font-family: var(--font-body);
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.social-links {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  margin-top: 1rem;
}

.social-links a {
  color: var(--color-accent-tech);
  text-decoration: none;
  font-size: 0.9rem;
  font-weight: 500;
  transition: color 0.2s;
}

.social-links a:hover {
  color: var(--color-accent-growth);
}

.hero-revenue {
  margin-bottom: 3rem;
  padding: 2rem;
  background: var(--color-surface);
  border-radius: 8px;
  border: 1px solid var(--color-border);
}

.section-label {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text-secondary);
  margin-bottom: 1.5rem;
}

.revenue-track {
  margin-bottom: 2rem;
  position: relative;
}

.revenue-track:last-child {
  margin-bottom: 0;
}

.revenue-metrics {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 0.5rem;
}

.metric-start,
.metric-end {
  font-family: var(--font-data);
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-accent-gold);
}

.flow-line-container {
  flex: 1;
  position: relative;
  height: 6px;
  background: var(--color-border);
  border-radius: 3px;
  overflow: hidden;
}

.flow-line {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: linear-gradient(90deg, var(--color-accent-growth) 0%, var(--color-accent-tech) 100%);
  transform: translateX(-100%);
  animation: revenue-flow 3s ease-out forwards;
}

@keyframes revenue-flow {
  to { transform: translateX(0); }
}

@media (prefers-reduced-motion: reduce) {
  .flow-line {
    animation: none;
    transform: translateX(0);
  }
}

.track-label {
  font-size: 0.875rem;
  color: var(--color-text-secondary);
  display: block;
  margin-top: 0.5rem;
}

.track-sublabel {
  font-size: 0.75rem;
  color: var(--color-text-secondary);
  font-style: italic;
}

.narrative {
  margin-bottom: 3rem;
  font-size: 1.125rem;
  line-height: 1.7;
  color: var(--color-text-primary);
}

.achievement-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.card {
  padding: 1.5rem;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 8px;
}

.card h3 {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 0.75rem;
  color: var(--color-accent-tech);
}

.card p {
  font-size: 0.9rem;
  line-height: 1.6;
  color: var(--color-text-primary);
}

.tech-stack {
  margin-bottom: 3rem;
}

.tech-stack h2 {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.stack-category {
  margin-bottom: 1.5rem;
}

.stack-category h3 {
  font-family: var(--font-body);
  font-size: 0.875rem;
  font-weight: 500;
  color: var(--color-text-secondary);
  margin-bottom: 0.5rem;
}

.stack-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.stack-item {
  font-size: 0.875rem;
  padding: 0.25rem 0.75rem;
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: 4px;
  color: var(--color-text-primary);
}

.next {
  margin-bottom: 3rem;
  padding: 1.5rem;
  background: var(--color-surface);
  border-left: 3px solid var(--color-accent-growth);
}

.next h2 {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text-secondary);
  margin-bottom: 0.75rem;
}

.next p {
  font-size: 0.95rem;
  line-height: 1.6;
}

.timeline {
  margin-bottom: 2rem;
}

.timeline h2 {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.timeline-item {
  margin-bottom: 1.5rem;
}

.timeline-company {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text-primary);
  margin-bottom: 0.25rem;
}

.timeline-roles {
  font-size: 0.875rem;
  color: var(--color-text-secondary);
  line-height: 1.5;
}

.education {
  margin-bottom: 2rem;
}

.education h2 {
  font-family: var(--font-display);
  font-size: 0.875rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-text-secondary);
  margin-bottom: 1rem;
}

.education-item {
  margin-bottom: 0.75rem;
  font-size: 0.9rem;
}

.education-degree {
  font-weight: 500;
  color: var(--color-text-primary);
}

.education-school {
  color: var(--color-text-secondary);
}

@media (max-width: 768px) {
  .achievement-cards {
    grid-template-columns: 1fr;
  }
  
  .revenue-metrics {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
  
  .flow-line-container {
    width: 100%;
  }
  
  .metric-start,
  .metric-end {
    font-size: 1.25rem;
  }
  
  .social-links {
    flex-direction: column;
    gap: 0.75rem;
  }
}
</style>

<div class="profile-container">
  <header class="profile-header">
    <h1 class="name">Vismit Patel</h1>
    <p class="title">Senior Software Engineer 2</p>
    <p class="location">Fremont, CA</p>
    <nav class="social-links">
      <a href="https://linkedin.com/in/vismitpatel">LinkedIn</a>
      <a href="https://github.com/vismit">GitHub</a>
      <a href="mailto:vismitkpatel@gmail.com">Email</a>
    </nav>
  </header>

  <section class="hero-revenue">
    <h2 class="section-label">Revenue Architecture</h2>
    
    <div class="revenue-track revenue-track--primary">
      <div class="revenue-metrics">
        <span class="metric-start">$10M</span>
        <div class="flow-line-container">
          <div class="flow-line"></div>
        </div>
        <span class="metric-end">$300M</span>
      </div>
      <span class="track-label">Carta Cap Table <span class="track-sublabel">Aug 2017 – Oct 2022</span></span>
    </div>

    <div class="revenue-track revenue-track--secondary">
      <div class="revenue-metrics">
        <span class="metric-start">$0</span>
        <div class="flow-line-container">
          <div class="flow-line"></div>
        </div>
        <span class="metric-end">$20M</span>
      </div>
      <span class="track-label">Carta Total Compensation <span class="track-sublabel">Oct 2022 – Present, Founding Engineer</span></span>
    </div>
  </section>

  <section class="narrative">
    <p>I've spent nine years at Carta building fintech products that scale. Helped grow the Cap Table business from $10M to $300M ARR. As a founding engineer on Total Compensation, turned a hackathon prototype into a $20M ARR business while leading strategic partnerships with Morgan Stanley Wealth Management and pioneering AI integration with Claude.</p>
  </section>

  <section class="achievement-cards">
    <article class="card card--systems">
      <h3>Systems Architecture</h3>
      <p>Architected microservices and scaled Securities capabilities using Python/Django/React within high-concurrency service-oriented environment. Modernized legacy infrastructure through strategic refactoring and Domain-Driven Design principles.</p>
    </article>

    <article class="card card--partnerships">
      <h3>Strategic Partnerships</h3>
      <p>Orchestrated technical execution of Carta–Morgan Stanley Wealth Management partnership for IPO support and financial guidance. Led Carta–Rippling partnership integration and architected high-scale external benchmarking APIs for third-party ecosystem.</p>
    </article>

    <article class="card card--ai">
      <h3>AI & Platform Innovation</h3>
      <p>Architected Model Context Protocol (MCP) infrastructure enabling custom AI skills and secure platform access. Implemented Claude Code agent workflows, custom skills/plugins, and expanded API surface for developer ecosystem.</p>
    </article>
  </section>

  <section class="tech-stack">
    <h2>Tech Stack</h2>
    
    <div class="stack-category">
      <h3>Languages</h3>
      <div class="stack-list">
        <span class="stack-item">Python</span>
        <span class="stack-item">TypeScript</span>
        <span class="stack-item">JavaScript</span>
        <span class="stack-item">SQL</span>
      </div>
    </div>

    <div class="stack-category">
      <h3>Frameworks & Tools</h3>
      <div class="stack-list">
        <span class="stack-item">Django</span>
        <span class="stack-item">React</span>
        <span class="stack-item">Celery</span>
        <span class="stack-item">Redis</span>
        <span class="stack-item">REST API</span>
        <span class="stack-item">gRPC</span>
        <span class="stack-item">Kafka</span>
        <span class="stack-item">Temporal</span>
        <span class="stack-item">SFTP</span>
      </div>
    </div>

    <div class="stack-category">
      <h3>Infrastructure & AI</h3>
      <div class="stack-list">
        <span class="stack-item">AWS S3</span>
        <span class="stack-item">Postgres</span>
        <span class="stack-item">Docker</span>
        <span class="stack-item">Kubernetes</span>
        <span class="stack-item">Terraform</span>
        <span class="stack-item">CI/CD</span>
        <span class="stack-item">Claude Code</span>
        <span class="stack-item">MCP</span>
      </div>
    </div>

    <div class="stack-category">
      <h3>Architecture</h3>
      <div class="stack-list">
        <span class="stack-item">Microservices</span>
        <span class="stack-item">Event-Driven Architecture</span>
        <span class="stack-item">Domain-Driven Design</span>
        <span class="stack-item">Service-Oriented Architecture</span>
      </div>
    </div>
  </section>

  <section class="next">
    <h2>What's Next</h2>
    <p>I'm seeking staff+ roles where I can drive technical leadership, architect scalable systems, build 0→1 products, or tackle scaling challenges where technical solutions create measurable business value. Whether it's fintech, infrastructure, or AI integration—I'm drawn to problems where engineering excellence compounds into revenue and impact.</p>
  </section>

  <section class="timeline">
    <h2>Experience</h2>
    
    <div class="timeline-item">
      <div class="timeline-company">Carta — San Francisco, CA</div>
      <div class="timeline-roles">
        Senior Software Engineer 2 <span style="color: var(--color-text-secondary);">|</span> Mar 2021 – Present<br>
        Senior Software Engineer <span style="color: var(--color-text-secondary);">|</span> Oct 2019 – Mar 2021<br>
        Software Engineer <span style="color: var(--color-text-secondary);">|</span> Aug 2017 – Oct 2019
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-company">NetApp — Sunnyvale, CA</div>
      <div class="timeline-roles">
        MTS Software Intern <span style="color: var(--color-text-secondary);">|</span> Jun 2016 – Dec 2016
      </div>
    </div>
  </section>

  <section class="education">
    <h2>Education</h2>
    <div class="education-item">
      <span class="education-degree">Master of Science in Computer Science and Engineering</span><br>
      <span class="education-school">Santa Clara University, 2015–2017</span>
    </div>
    <div class="education-item">
      <span class="education-degree">Bachelor of Engineering in Electronics and Communication</span><br>
      <span class="education-school">Gujarat Technological University, 2008–2012</span>
    </div>
  </section>
</div>
