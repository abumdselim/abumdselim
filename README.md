<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abu Md Selim - Full Stack Engineer</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    :root {
        --bg-dark: #0d1117;
        --bg-secondary: #161b22;
        --bg-tertiary: #21262d;
        --text-primary: #e6edf3;
        --text-secondary: #8b949e;
        --accent: #58a6ff;
        --accent-dark: #1f6feb;
        --success: #3fb950;
        --danger: #f85149;
        --border: #30363d;
    }

    body {
        background: var(--bg-dark);
        color: var(--text-primary);
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
        line-height: 1.6;
    }

    /* Animated grid background */
    body::before {
        content: '';
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: 
            linear-gradient(0deg, transparent 24%, rgba(88, 166, 255, .05) 25%, rgba(88, 166, 255, .05) 26%, transparent 27%, transparent 74%, rgba(88, 166, 255, .05) 75%, rgba(88, 166, 255, .05) 76%, transparent 77%, transparent),
            linear-gradient(90deg, transparent 24%, rgba(88, 166, 255, .05) 25%, rgba(88, 166, 255, .05) 26%, transparent 27%, transparent 74%, rgba(88, 166, 255, .05) 75%, rgba(88, 166, 255, .05) 76%, transparent 77%, transparent);
        background-size: 50px 50px;
        pointer-events: none;
        z-index: 0;
    }

    .container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 24px;
        position: relative;
        z-index: 1;
    }

    /* Header */
    header {
        padding: 60px 0 40px;
        border-bottom: 1px solid var(--border);
    }

    .header-content {
        display: flex;
        align-items: center;
        gap: 30px;
        margin-bottom: 30px;
    }

    .avatar {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        background: linear-gradient(135deg, var(--accent), #1f6feb);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 60px;
        border: 3px solid var(--accent);
        flex-shrink: 0;
        animation: pulse 3s ease-in-out infinite;
    }

    @keyframes pulse {
        0%, 100% { box-shadow: 0 0 0 0 rgba(88, 166, 255, 0.7); }
        50% { box-shadow: 0 0 0 20px rgba(88, 166, 255, 0); }
    }

    .header-info h1 {
        font-size: 2.5rem;
        margin-bottom: 8px;
        background: linear-gradient(135deg, var(--accent), #79c0ff);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .header-info .title {
        color: var(--accent);
        font-size: 1.2rem;
        margin-bottom: 12px;
        font-weight: 600;
    }

    .header-info .subtitle {
        color: var(--text-secondary);
        font-size: 0.95rem;
    }

    /* Quick Links */
    .quick-links {
        display: flex;
        gap: 12px;
        flex-wrap: wrap;
        margin-top: 16px;
    }

    .link-btn {
        display: inline-flex;
        align-items: center;
        gap: 6px;
        padding: 8px 16px;
        background: var(--bg-secondary);
        border: 1px solid var(--border);
        color: var(--accent);
        text-decoration: none;
        border-radius: 6px;
        font-size: 0.85rem;
        transition: all 0.3s ease;
        cursor: pointer;
    }

    .link-btn:hover {
        background: var(--accent-dark);
        color: white;
        border-color: var(--accent);
        transform: translateY(-2px);
    }

    /* Section */
    section {
        padding: 50px 0;
        border-bottom: 1px solid var(--border);
        scroll-margin-top: 80px;
    }

    .section-title {
        font-size: 2rem;
        margin-bottom: 30px;
        padding-bottom: 16px;
        border-bottom: 2px solid var(--accent);
        display: inline-block;
    }

    /* Tech Stack Grid */
    .tech-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
        gap: 20px;
        margin-bottom: 50px;
    }

    .tech-card {
        background: linear-gradient(135deg, var(--bg-secondary), var(--bg-tertiary));
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 20px;
        text-align: center;
        transition: all 0.3s ease;
        cursor: pointer;
        position: relative;
        overflow: hidden;
    }

    .tech-card::before {
        content: '';
        position: absolute;
        top: -50%;
        left: -50%;
        width: 200%;
        height: 200%;
        background: radial-gradient(circle, rgba(88, 166, 255, 0.1) 0%, transparent 70%);
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    .tech-card:hover {
        border-color: var(--accent);
        background: linear-gradient(135deg, rgba(88, 166, 255, 0.1), rgba(31, 110, 251, 0.05));
        transform: translateY(-8px);
    }

    .tech-card:hover::before {
        opacity: 1;
    }

    .tech-logo {
        font-size: 3.5rem;
        margin-bottom: 12px;
        position: relative;
        z-index: 1;
        filter: drop-shadow(0 0 8px rgba(88, 166, 255, 0.2));
        transition: transform 0.3s ease;
    }

    .tech-card:hover .tech-logo {
        transform: scale(1.15) rotate(5deg);
    }

    .tech-name {
        font-weight: 600;
        font-size: 0.95rem;
        color: var(--accent);
        position: relative;
        z-index: 1;
    }

    .tech-level {
        font-size: 0.75rem;
        color: var(--text-secondary);
        margin-top: 6px;
        position: relative;
        z-index: 1;
    }

    /* Category Sections */
    .category {
        margin-bottom: 50px;
    }

    .category-title {
        font-size: 1.3rem;
        color: var(--accent);
        margin-bottom: 20px;
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .category-title::before {
        content: '';
        width: 4px;
        height: 24px;
        background: var(--accent);
        border-radius: 2px;
    }

    /* Project Cards */
    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
        gap: 24px;
        margin-top: 30px;
    }

    .project-card {
        background: var(--bg-secondary);
        border: 1px solid var(--border);
        border-radius: 10px;
        overflow: hidden;
        transition: all 0.3s ease;
        position: relative;
    }

    .project-header {
        padding: 24px;
        background: linear-gradient(135deg, rgba(88, 166, 255, 0.1), rgba(31, 110, 251, 0.05));
        border-bottom: 1px solid var(--border);
    }

    .project-title {
        font-size: 1.3rem;
        color: var(--accent);
        margin-bottom: 6px;
    }

    .project-url {
        color: var(--text-secondary);
        font-size: 0.85rem;
        text-decoration: none;
    }

    .project-url:hover {
        color: var(--accent);
        text-decoration: underline;
    }

    .project-content {
        padding: 24px;
    }

    .project-desc {
        color: var(--text-secondary);
        margin-bottom: 16px;
        line-height: 1.6;
    }

    .status-badge {
        display: inline-block;
        padding: 6px 12px;
        background: rgba(63, 185, 80, 0.15);
        color: var(--success);
        border-radius: 20px;
        font-size: 0.75rem;
        font-weight: 600;
        margin-bottom: 12px;
        border: 1px solid var(--success);
    }

    .features {
        list-style: none;
        margin: 16px 0;
    }

    .features li {
        padding: 6px 0;
        padding-left: 20px;
        position: relative;
        color: var(--text-secondary);
        font-size: 0.9rem;
    }

    .features li::before {
        content: '▸';
        position: absolute;
        left: 0;
        color: var(--accent);
        font-weight: bold;
    }

    .tech-used {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        margin-top: 16px;
        padding-top: 16px;
        border-top: 1px solid var(--border);
    }

    .tech-badge {
        padding: 4px 10px;
        background: rgba(88, 166, 255, 0.1);
        border: 1px solid var(--accent);
        border-radius: 4px;
        font-size: 0.75rem;
        color: var(--accent);
    }

    .project-card:hover {
        border-color: var(--accent);
        box-shadow: 0 8px 24px rgba(88, 166, 255, 0.15);
        transform: translateY(-4px);
    }

    /* Philosophy Section */
    .philosophy-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 20px;
        margin-top: 30px;
    }

    .philosophy-card {
        background: linear-gradient(135deg, var(--bg-secondary), var(--bg-tertiary));
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 24px;
        transition: all 0.3s ease;
    }

    .philosophy-card:hover {
        border-color: var(--accent);
        background: linear-gradient(135deg, rgba(88, 166, 255, 0.1), rgba(31, 110, 251, 0.05));
    }

    .philosophy-icon {
        font-size: 2.5rem;
        margin-bottom: 12px;
    }

    .philosophy-title {
        font-size: 1.1rem;
        color: var(--accent);
        margin-bottom: 12px;
        font-weight: 600;
    }

    .philosophy-desc {
        color: var(--text-secondary);
        font-size: 0.9rem;
        line-height: 1.6;
    }

    /* Stats */
    .stats-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 20px;
        margin-top: 30px;
    }

    .stat-card {
        background: var(--bg-secondary);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 20px;
        text-align: center;
    }

    .stat-number {
        font-size: 2.5rem;
        color: var(--accent);
        font-weight: 800;
        margin-bottom: 8px;
    }

    .stat-label {
        color: var(--text-secondary);
        font-size: 0.9rem;
    }

    /* Connect Section */
    .connect-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-top: 30px;
    }

    .connect-card {
        background: var(--bg-secondary);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 20px;
        transition: all 0.3s ease;
    }

    .connect-card:hover {
        border-color: var(--accent);
        background: linear-gradient(135deg, rgba(88, 166, 255, 0.1), rgba(31, 110, 251, 0.05));
    }

    .connect-icon {
        font-size: 2rem;
        margin-bottom: 12px;
    }

    .connect-title {
        font-weight: 600;
        color: var(--accent);
        margin-bottom: 8px;
    }

    .connect-link {
        color: var(--text-secondary);
        text-decoration: none;
        word-break: break-all;
        transition: color 0.3s ease;
    }

    .connect-link:hover {
        color: var(--accent);
    }

    /* Footer */
    footer {
        padding: 40px 0;
        text-align: center;
        border-top: 1px solid var(--border);
        color: var(--text-secondary);
        font-size: 0.9rem;
    }

    .footer-divider {
        width: 100px;
        height: 2px;
        background: linear-gradient(90deg, transparent, var(--accent), transparent);
        margin: 20px auto 30px;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .header-content {
            flex-direction: column;
            text-align: center;
        }

        .header-info h1 {
            font-size: 2rem;
        }

        .tech-grid {
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        }

        .projects-grid {
            grid-template-columns: 1fr;
        }

        .quick-links {
            justify-content: center;
        }
    }

    /* Scroll animations */
    @keyframes fadeIn {
        from {
            opacity: 0;
            transform: translateY(20px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .fade-in {
        animation: fadeIn 0.6s ease forwards;
    }
</style>
```

</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <div class="header-content">
                <div class="avatar">💻</div>
                <div class="header-info">
                    <h1>Abu Md Selim</h1>
                    <div class="title">Full Stack Engineer • Founder @ IntacticSys</div>
                    <div class="subtitle">Building production systems that solve real problems. No vanity metrics.</div>
                    <div class="quick-links">
                        <a href="mailto:selim@intacticsys.com" class="link-btn">
                            <i class="fas fa-envelope"></i> Email
                        </a>
                        <a href="https://t.me/selimmmishu" class="link-btn" target="_blank">
                            <i class="fab fa-telegram"></i> Telegram
                        </a>
                        <a href="https://linkedin.com/in/aabumdselim" class="link-btn" target="_blank">
                            <i class="fab fa-linkedin"></i> LinkedIn
                        </a>
                        <a href="https://intacticsys.com" class="link-btn" target="_blank">
                            <i class="fas fa-globe"></i> IntacticSys
                        </a>
                    </div>
                </div>
            </div>
        </header>

```
    <!-- Tech Stack -->
    <section>
        <h2 class="section-title">Technology Stack</h2>

        <!-- Backend -->
        <div class="category">
            <h3 class="category-title">Backend</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-logo">🐍</div>
                    <div class="tech-name">Python</div>
                    <div class="tech-level">FastAPI • Django • asyncio</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🟩</div>
                    <div class="tech-name">Node.js</div>
                    <div class="tech-level">Express • NestJS</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">⚙️</div>
                    <div class="tech-name">Go</div>
                    <div class="tech-level">High-performance systems</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">📘</div>
                    <div class="tech-name">TypeScript</div>
                    <div class="tech-level">Type-safe backend</div>
                </div>
            </div>
        </div>

        <!-- Frontend -->
        <div class="category">
            <h3 class="category-title">Frontend</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-logo">⚛️</div>
                    <div class="tech-name">React</div>
                    <div class="tech-level">Hooks • Context • Performance</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">▲</div>
                    <div class="tech-name">Next.js</div>
                    <div class="tech-level">SSR • SSG • Full-stack</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">📘</div>
                    <div class="tech-name">TypeScript</div>
                    <div class="tech-level">Type safety • DX</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🎨</div>
                    <div class="tech-name">Tailwind CSS</div>
                    <div class="tech-level">Rapid design systems</div>
                </div>
            </div>
        </div>

        <!-- Databases -->
        <div class="category">
            <h3 class="category-title">Databases & Cache</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-logo">🐘</div>
                    <div class="tech-name">PostgreSQL</div>
                    <div class="tech-level">Relational • Battle-tested</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🍃</div>
                    <div class="tech-name">MongoDB</div>
                    <div class="tech-level">Document • Flexible</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🔴</div>
                    <div class="tech-name">Redis</div>
                    <div class="tech-level">Cache • Real-time</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🔎</div>
                    <div class="tech-name">Elasticsearch</div>
                    <div class="tech-level">Search • Analytics</div>
                </div>
            </div>
        </div>

        <!-- DevOps & Infrastructure -->
        <div class="category">
            <h3 class="category-title">DevOps & Infrastructure</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-logo">🐳</div>
                    <div class="tech-name">Docker</div>
                    <div class="tech-level">Containerization</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">☸️</div>
                    <div class="tech-name">Kubernetes</div>
                    <div class="tech-level">Orchestration • Scaling</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">☁️</div>
                    <div class="tech-name">AWS</div>
                    <div class="tech-level">EC2 • RDS • S3 • Lambda</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">⚡</div>
                    <div class="tech-name">CI/CD</div>
                    <div class="tech-level">GitHub Actions • Automation</div>
                </div>
            </div>
        </div>

        <!-- Development Tools -->
        <div class="category">
            <h3 class="category-title">Development Tools</h3>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-logo">🤖</div>
                    <div class="tech-name">Devin</div>
                    <div class="tech-level">AI Code Generation</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">💻</div>
                    <div class="tech-name">Cursor</div>
                    <div class="tech-level">AI-Powered IDE</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">✨</div>
                    <div class="tech-name">GitHub Copilot</div>
                    <div class="tech-level">Code Assistance</div>
                </div>
                <div class="tech-card">
                    <div class="tech-logo">🐙</div>
                    <div class="tech-name">Git</div>
                    <div class="tech-level">Version Control</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects -->
    <section>
        <h2 class="section-title">Featured Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-header">
                    <div class="project-title">🚀 The Chattala</div>
                    <a href="https://thechattala.com" class="project-url" target="_blank">thechattala.com</a>
                </div>
                <div class="project-content">
                    <div class="status-badge">✓ Live & Operational</div>
                    <p class="project-desc">Hyperlocal community platform connecting neighborhoods, shops, and service providers across South Asia.</p>
                    <ul class="features">
                        <li><strong>Community Module:</strong> Real-time posts, threaded discussions</li>
                        <li><strong>Shop Marketplace:</strong> 1-7 hour express delivery</li>
                        <li><strong>Services Network:</strong> Professional service providers</li>
                        <li><strong>Dual-Mode:</strong> Customer & provider ecosystem</li>
                    </ul>
                    <div class="tech-used">
                        <span class="tech-badge">Python</span>
                        <span class="tech-badge">React</span>
                        <span class="tech-badge">PostgreSQL</span>
                        <span class="tech-badge">AWS</span>
                        <span class="tech-badge">Docker</span>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <div class="project-title">🏢 IntacticSys</div>
                    <a href="https://intacticsys.com" class="project-url" target="_blank">intacticsys.com</a>
                </div>
                <div class="project-content">
                    <div class="status-badge">◉ Active</div>
                    <p class="project-desc">Bespoke software engineering firm building production systems for demanding technical challenges.</p>
                    <ul class="features">
                        <li><strong>Custom Development:</strong> Enterprise applications</li>
                        <li><strong>Architecture Design:</strong> Scalable systems</li>
                        <li><strong>Full-Stack Solutions:</strong> Backend to frontend</li>
                        <li><strong>Infrastructure:</strong> Cloud & DevOps</li>
                    </ul>
                    <div class="tech-used">
                        <span class="tech-badge">Python</span>
                        <span class="tech-badge">Node.js</span>
                        <span class="tech-badge">React</span>
                        <span class="tech-badge">PostgreSQL</span>
                        <span class="tech-badge">Kubernetes</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Philosophy -->
    <section>
        <h2 class="section-title">Engineering Philosophy</h2>
        <div class="philosophy-grid">
            <div class="philosophy-card">
                <div class="philosophy-icon">⚙️</div>
                <div class="philosophy-title">Quality First</div>
                <div class="philosophy-desc">Every line of code serves purpose. Technical debt avoided, not accumulated. Systems designed for maintainability and longevity.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">⚡</div>
                <div class="philosophy-title">Rapid Innovation</div>
                <div class="philosophy-desc">AI-assisted development accelerates iteration. Fast MVP validation, then meticulous production engineering. Move fast with confidence.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">🎯</div>
                <div class="philosophy-title">Real Impact</div>
                <div class="philosophy-desc">Systems that matter. Not feature factories. If it's worth building, it's worth building right. Problem-driven development.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">📚</div>
                <div class="philosophy-title">Continuous Learning</div>
                <div class="philosophy-desc">Code evolves, architectures improve, tools advance. Stay ahead by understanding fundamentals and embracing new approaches.</div>
            </div>
        </div>
    </section>

    <!-- Interests -->
    <section>
        <h2 class="section-title">Beyond Code</h2>
        <div class="philosophy-grid">
            <div class="philosophy-card">
                <div class="philosophy-icon">📖</div>
                <div class="philosophy-title">Philosophy</div>
                <div class="philosophy-desc">Kafka's absurdism. Plato's forms. Phenomenological inquiry. Deep thinking informs better system design and architectural decisions.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">🎬</div>
                <div class="philosophy-title">Cinema</div>
                <div class="philosophy-desc">Masterworks that challenge perspective. Narrative structure and visual composition inspire creative problem-solving and design thinking.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">📚</div>
                <div class="philosophy-title">Literature</div>
                <div class="philosophy-desc">Novels and history. Deep reading fuels systems thinking. Understanding human dynamics improves organizational design and team leadership.</div>
            </div>
            <div class="philosophy-card">
                <div class="philosophy-icon">🛠️</div>
                <div class="philosophy-title">Building</div>
                <div class="philosophy-desc">Architecture from first principles. Craftsmanship in every detail. Creating systems and products that stand the test of time.</div>
            </div>
        </div>
    </section>

    <!-- Stats -->
    <section>
        <h2 class="section-title">By The Numbers</h2>
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number">10+</div>
                <div class="stat-label">Years in Development</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">50+</div>
                <div class="stat-label">Production Deployments</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">2M+</div>
                <div class="stat-label">Users Impacted</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">∞</div>
                <div class="stat-label">Code Quality Standards</div>
            </div>
        </div>
    </section>

    <!-- Connect -->
    <section>
        <h2 class="section-title">Let's Connect</h2>
        <p style="color: var(--text-secondary); margin-bottom: 30px;">Building something ambitious? Let's discuss your next technical challenge.</p>
        
        <div class="connect-grid">
            <div class="connect-card">
                <div class="connect-icon">📧</div>
                <div class="connect-title">Email</div>
                <a href="mailto:selim@intacticsys.com" class="connect-link">selim@intacticsys.com</a>
            </div>
            <div class="connect-card">
                <div class="connect-icon">💬</div>
                <div class="connect-title">Telegram</div>
                <a href="https://t.me/selimmmishu" class="connect-link" target="_blank">@selimmmishu</a>
            </div>
            <div class="connect-card">
                <div class="connect-icon">💼</div>
                <div class="connect-title">LinkedIn</div>
                <a href="https://linkedin.com/in/aabumdselim" class="connect-link" target="_blank">@aabumdselim</a>
            </div>
            <div class="connect-card">
                <div class="connect-icon">🌐</div>
                <div class="connect-title">Web</div>
                <a href="https://intacticsys.com" class="connect-link" target="_blank">intacticsys.com</a>
            </div>
            <div class="connect-card">
                <div class="connect-icon">👥</div>
                <div class="connect-title">IntacticSys Socials</div>
                <a href="https://instagram.com/intacticsys" class="connect-link" target="_blank">@intacticsys</a>
            </div>
            <div class="connect-card">
                <div class="connect-icon">🚀</div>
                <div class="connect-title">The Chattala Socials</div>
                <a href="https://instagram.com/thechattala" class="connect-link" target="_blank">@thechattala</a>
            </div>
        </div>
    </section>
</div>

<!-- Footer -->
<footer>
    <div class="footer-divider"></div>
    <p>Engineering excellence in every line of code • Built with intention • Deployed with confidence</p>
    <p style="margin-top: 12px; font-size: 0.85rem;">Abu Md Selim © 2025</p>
</footer>

<script>
    // Smooth scroll for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({ behavior: 'smooth' });
            }
        });
    });

    // Intersection Observer for fade-in animations
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('fade-in');
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.tech-card, .project-card, .philosophy-card').forEach(el => {
        observer.observe(el);
    });
</script>
```

</body>
</html>