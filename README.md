<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Andreia Tiveron</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0d0d;
    --surface: #161616;
    --border: #222;
    --text: #e8e8e8;
    --muted: #666;
    --accent: #e8e8e8;
    --font: 'JetBrains Mono', 'Fira Mono', monospace;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font);
    font-size: 14px;
    line-height: 1.7;
    min-height: 100vh;
  }

  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    padding: 1.2rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid var(--border);
    background: rgba(13,13,13,0.92);
    backdrop-filter: blur(8px);
    z-index: 100;
  }

  .nav-logo { color: var(--text); font-size: 13px; letter-spacing: 0.05em; }
  .nav-logo span { color: var(--muted); }

  .nav-links { display: flex; gap: 2rem; }
  .nav-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 12px;
    letter-spacing: 0.08em;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--text); }

  main { max-width: 680px; margin: 0 auto; padding: 0 2rem; }

  section { padding: 6rem 0 4rem; }

  .hero { padding-top: 10rem; min-height: 100vh; display: flex; flex-direction: column; justify-content: center; }

  .hero h1 {
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 400;
    letter-spacing: -0.02em;
    line-height: 1.1;
    margin-bottom: 1.5rem;
  }

  .hero h1 em {
    font-style: normal;
    color: var(--muted);
  }

  .hero p {
    color: var(--muted);
    font-size: 13px;
    max-width: 440px;
    margin-bottom: 2.5rem;
  }

  .hero-links { display: flex; gap: 1.5rem; }
  .hero-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 12px;
    letter-spacing: 0.06em;
    border-bottom: 1px solid var(--border);
    padding-bottom: 2px;
    transition: color 0.2s, border-color 0.2s;
  }
  .hero-links a:hover { color: var(--text); border-color: var(--text); }

  .label {
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 2rem;
  }

  .divider {
    width: 24px;
    height: 1px;
    background: var(--border);
    margin-bottom: 2rem;
  }

  .about p {
    color: #aaa;
    font-size: 14px;
    line-height: 1.8;
    margin-bottom: 1rem;
  }

  .stack-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    margin-top: 1.5rem;
  }

  .stack-cell {
    background: var(--bg);
    padding: 1.25rem;
  }

  .stack-cell h3 {
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 0.75rem;
    font-weight: 400;
  }

  .stack-cell ul { list-style: none; }
  .stack-cell ul li {
    font-size: 13px;
    color: #bbb;
    padding: 3px 0;
  }
  .stack-cell ul li::before {
    content: '─ ';
    color: var(--border);
  }

  .projects { display: flex; flex-direction: column; gap: 1px; background: var(--border); border: 1px solid var(--border); margin-top: 1.5rem; }

  .project {
    background: var(--bg);
    padding: 1.5rem 1.25rem;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    transition: background 0.2s;
    text-decoration: none;
    color: inherit;
  }

  .project:hover { background: var(--surface); }

  .project-info h3 { font-size: 14px; font-weight: 400; margin-bottom: 0.3rem; }
  .project-info p { font-size: 12px; color: var(--muted); }
  .project-tag {
    font-size: 11px;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 2px 8px;
    white-space: nowrap;
    margin-top: 2px;
  }

  .contact-block {
    margin-top: 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }

  .contact-row {
    background: var(--bg);
    padding: 1rem 1.25rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .contact-row span { font-size: 12px; color: var(--muted); }
  .contact-row a {
    font-size: 13px;
    color: #bbb;
    text-decoration: none;
    transition: color 0.2s;
  }
  .contact-row a:hover { color: var(--text); }

  footer {
    border-top: 1px solid var(--border);
    padding: 2rem;
    text-align: center;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.06em;
    margin-top: 4rem;
  }

  @media (max-width: 540px) {
    .stack-grid { grid-template-columns: 1fr; }
    .nav-links { display: none; }
  }
</style>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400&display=swap" rel="stylesheet">
</head>
<body>

<nav>
  <div class="nav-logo">andreia<span>.dev</span></div>
  <div class="nav-links">
    <a href="#sobre">sobre</a>
    <a href="#stack">stack</a>
    <a href="#projetos">projetos</a>
    <a href="#contato">contato</a>
  </div>
</nav>

<main>
  <section class="hero">
    <h1>Andreia Tiveron<br><em>backend & devops</em></h1>
    <p>Construindo sistemas que escalam, pipelines que automatizam e infraestrutura que não quebra às 3h da manhã.</p>
    <div class="hero-links">
      <a href="https://github.com/andreiabtiveron" target="_blank">github ↗</a>
      <a href="https://linkedin.com/in/andreiativeron" target="_blank">linkedin ↗</a>
      <a href="mailto:andreiabtiveron@gmail.com">email ↗</a>
    </div>
  </section>

  <section id="sobre">
    <div class="label">sobre</div>
    <div class="divider"></div>
    <div class="about">
      <p>Engenheira focada em backend e infraestrutura. Gosto de sistemas bem desenhados, automação de verdade e observabilidade que funciona quando você mais precisa.</p>
      <p>Atualmente explorando Platform Engineering e SRE — acredito que a diferença entre um sistema bom e um ótimo está na confiabilidade.</p>
    </div>
  </section>

  <section id="stack">
    <div class="label">stack</div>
    <div class="divider"></div>
    <div class="stack-grid">
      <div class="stack-cell">
        <h3>backend</h3>
        <ul>
          <li>Python</li>
          <li>Node.js</li>
          <li>Go</li>
          <li>PostgreSQL</li>
          <li>Redis</li>
        </ul>
      </div>
      <div class="stack-cell">
        <h3>devops & cloud</h3>
        <ul>
          <li>Docker</li>
          <li>Kubernetes</li>
          <li>Terraform</li>
          <li>GitHub Actions</li>
          <li>AWS</li>
        </ul>
      </div>
      <div class="stack-cell">
        <h3>observabilidade</h3>
        <ul>
          <li>Prometheus</li>
          <li>Grafana</li>
          <li>Nginx</li>
          <li>Linux</li>
        </ul>
      </div>
      <div class="stack-cell">
        <h3>agora</h3>
        <ul>
          <li>Platform Engineering</li>
          <li>SRE</li>
          <li>Distributed tracing</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="projetos">
    <div class="label">projetos</div>
    <div class="divider"></div>
    <div class="projects">
      <a class="project" href="https://github.com/andreiabtiveron" target="_blank">
        <div class="project-info">
          <h3>em breve</h3>
          <p>Adicione seus projetos aqui</p>
        </div>
        <span class="project-tag">github ↗</span>
      </a>
    </div>
  </section>

  <section id="contato">
    <div class="label">contato</div>
    <div class="divider"></div>
    <div class="contact-block">
      <div class="contact-row">
        <span>email</span>
        <a href="mailto:andreiabtiveron@gmail.com">andreiabtiveron@gmail.com</a>
      </div>
      <div class="contact-row">
        <span>linkedin</span>
        <a href="https://linkedin.com/in/andreiativeron" target="_blank">andreiativeron</a>
      </div>
      <div class="contact-row">
        <span>github</span>
        <a href="https://github.com/andreiabtiveron" target="_blank">andreiabtiveron</a>
      </div>
    </div>
  </section>
</main>

<footer>andreia tiveron · 2025</footer>

</body>
</html>
