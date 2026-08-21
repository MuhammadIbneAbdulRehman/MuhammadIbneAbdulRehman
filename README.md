<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad - Full Stack Developer</title>
    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #e0e0e0;
            line-height: 1.7;
            padding: 40px 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-radius: 24px;
            padding: 50px 60px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8), inset 0 1px 1px rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.06);
        }

        /* ===== TYPOGRAPHY ===== */
        h1 {
            font-size: 2.8rem;
            font-weight: 700;
            background: linear-gradient(135deg, #f093fb, #f5576c, #4facfe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-align: center;
            margin-bottom: 4px;
        }

        h2 {
            font-size: 2rem;
            font-weight: 600;
            color: #f0f0f0;
            margin: 40px 0 16px 0;
            padding-bottom: 10px;
            border-bottom: 2px solid rgba(79, 172, 254, 0.3);
        }

        h2 .emoji {
            -webkit-text-fill-color: initial;
        }

        h3 {
            font-size: 1.3rem;
            font-weight: 600;
            color: #c8d6e5;
            margin: 28px 0 10px 0;
        }

        h4 {
            font-size: 1.1rem;
            font-weight: 600;
            color: #a8c8e8;
            margin: 20px 0 6px 0;
        }

        p {
            margin-bottom: 12px;
            color: #d0d0d0;
        }

        a {
            color: #4facfe;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: #f5576c;
            text-decoration: underline;
        }

        /* ===== SUBTITLE ===== */
        .subtitle {
            text-align: center;
            font-size: 1.2rem;
            color: #b0b0b0;
            margin-bottom: 10px;
            font-weight: 300;
            letter-spacing: 0.5px;
        }

        /* ===== BADGES ===== */
        .badge-container {
            text-align: center;
            margin: 20px 0 10px 0;
        }

        .badge-container a {
            display: inline-block;
            margin: 4px 6px;
            transition: transform 0.2s ease;
        }

        .badge-container a:hover {
            transform: translateY(-2px);
        }

        .badge-container img {
            border-radius: 6px;
        }

        /* ===== STATS ROW ===== */
        .stats-row {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin: 20px 0 10px 0;
        }

        .stats-row img {
            border-radius: 6px;
        }

        /* ===== SKILLS GRID ===== */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 24px;
            margin: 20px 0 10px 0;
        }

        .skill-card {
            background: rgba(255, 255, 255, 0.04);
            border-radius: 16px;
            padding: 20px 24px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(79, 172, 254, 0.3);
            transform: translateY(-4px);
            box-shadow: 0 12px 30px -10px rgba(0, 0, 0, 0.5);
        }

        .skill-card h4 {
            margin-top: 0;
            color: #f0f0f0;
        }

        .skill-card .skill-desc {
            font-size: 0.9rem;
            color: #999;
            margin-bottom: 10px;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tags span {
            background: rgba(79, 172, 254, 0.15);
            color: #b0d4f0;
            padding: 4px 14px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
            border: 1px solid rgba(79, 172, 254, 0.1);
        }

        /* ===== PROJECTS ===== */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
            margin: 20px 0 10px 0;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.04);
            border-radius: 16px;
            padding: 24px;
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.3s ease;
        }

        .project-card:hover {
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(79, 172, 254, 0.25);
            transform: translateY(-4px);
            box-shadow: 0 12px 30px -10px rgba(0, 0, 0, 0.5);
        }

        .project-card .featured {
            display: inline-block;
            background: rgba(245, 87, 108, 0.2);
            color: #f5576c;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            padding: 2px 12px;
            border-radius: 12px;
            margin-bottom: 8px;
            border: 1px solid rgba(245, 87, 108, 0.2);
        }

        .project-card h3 {
            margin-top: 0;
            margin-bottom: 6px;
            color: #f0f0f0;
        }

        .project-card p {
            font-size: 0.95rem;
            color: #b0b0b0;
            margin-bottom: 12px;
        }

        .project-card .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
            margin: 10px 0 14px 0;
        }

        .project-card .tech-tags span {
            background: rgba(255, 255, 255, 0.06);
            color: #c0c0c0;
            padding: 2px 12px;
            border-radius: 12px;
            font-size: 0.75rem;
            border: 1px solid rgba(255, 255, 255, 0.06);
        }

        .project-card .project-links a {
            font-size: 0.9rem;
            margin-right: 16px;
        }

        /* ===== EXPERIENCE & EDUCATION ===== */
        .exp-item, .edu-item {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            padding: 18px 24px;
            margin-bottom: 16px;
            border-left: 3px solid #4facfe;
            transition: all 0.3s ease;
        }

        .exp-item:hover, .edu-item:hover {
            background: rgba(255, 255, 255, 0.06);
            border-left-color: #f5576c;
        }

        .exp-item .meta, .edu-item .meta {
            font-size: 0.85rem;
            color: #888;
            margin-bottom: 4px;
        }

        .exp-item ul, .edu-item ul {
            list-style: none;
            padding-left: 0;
            margin-top: 8px;
        }

        .exp-item ul li, .edu-item ul li {
            padding: 2px 0 2px 20px;
            position: relative;
            color: #c0c0c0;
            font-size: 0.95rem;
        }

        .exp-item ul li::before, .edu-item ul li::before {
            content: "▸";
            position: absolute;
            left: 0;
            color: #4facfe;
        }

        /* ===== CONTACT TABLE ===== */
        .contact-table {
            width: 100%;
            max-width: 500px;
            margin: 16px auto;
            border-collapse: collapse;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            overflow: hidden;
        }

        .contact-table td {
            padding: 12px 18px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            color: #c0c0c0;
        }

        .contact-table td:first-child {
            font-weight: 600;
            color: #a0b0c0;
            width: 80px;
        }

        .contact-table tr:last-child td {
            border-bottom: none;
        }

        /* ===== FOOTER ===== */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.06);
            color: #666;
            font-size: 0.9rem;
        }

        .footer .heart {
            color: #f5576c;
        }

        .quote {
            text-align: center;
            font-size: 1.1rem;
            font-style: italic;
            color: #a0b0c0;
            margin: 30px 0 10px 0;
            padding: 16px;
            border-left: 3px solid #4facfe;
            border-right: 3px solid #4facfe;
            background: rgba(79, 172, 254, 0.05);
            border-radius: 8px;
        }

        /* ===== DIVIDER ===== */
        hr {
            border: none;
            height: 1px;
            background: linear-gradient(to right, transparent, rgba(79, 172, 254, 0.3), transparent);
            margin: 40px 0;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 768px) {
            .container {
                padding: 24px 20px;
            }

            h1 {
                font-size: 2rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .stats-row {
                gap: 10px;
            }

            .stats-row img {
                width: 100%;
                max-width: 300px;
            }

            .contact-table td {
                padding: 8px 12px;
                font-size: 0.9rem;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 16px 12px;
            }

            h1 {
                font-size: 1.6rem;
            }

            .badge-container a {
                display: inline-block;
                margin: 3px;
            }

            .badge-container img {
                max-width: 140px;
            }
        }

        /* ===== SCROLLBAR ===== */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.02);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb {
            background: rgba(79, 172, 254, 0.3);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: rgba(79, 172, 254, 0.5);
        }
    </style>
</head>
<body>

<div class="container">

    <!-- ===== HEADER ===== -->
    <h1>Hi 👋, I'm Muhammad</h1>
    <p class="subtitle">Full Stack Developer | MERN Stack Specialist | BSCS Student</p>

    <!-- ===== TYPING ANIMATION ===== -->
    <p align="center">
        <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&width=435&lines=Full+Stack+Developer;MERN+Stack+Specialist;Building+Exceptional+Digital+Experiences;Open+to+New+Opportunities" alt="Typing SVG">
    </p>

    <!-- ===== BADGES ===== -->
    <div class="badge-container">
        <a href="mailto:muhammadcaptain303@gmail.com">
            <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
        </a>
        <a href="#">
            <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio">
        </a>
        <a href="https://github.com/your-username">
            <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
        </a>
    </div>

    <!-- ===== PROFILE VIEWS ===== -->
    <p align="center">
        <img src="https://komarev.com/ghpvc/?username=your-username&label=Profile%20Views&color=0e75b6&style=flat" alt="Profile Views">
    </p>

    <hr>

    <!-- ===== ABOUT ME ===== -->
    <h2>🧑‍💻 About Me</h2>

    <p>
        I am a passionate <strong>Full Stack Developer</strong> with expertise in the <strong>MERN stack</strong> and a keen eye for creating immersive web experiences. Currently pursuing my <strong>BSCS degree at Education University, Lahore</strong>, I combine academic knowledge with practical experience to build applications that are not just functional, but exceptional.
    </p>

    <p>
        From developing coworking space platforms to creating AI-powered business card scanners, I thrive on turning complex problems into elegant solutions. My journey includes internships at <strong>Prime Consultants</strong> where I honed my skills in real-world project development.
    </p>

    <!-- ===== STATS ROW ===== -->
    <div class="stats-row">
        <img src="https://img.shields.io/badge/Projects_Completed-10+-blue?style=for-the-badge" alt="Projects">
        <img src="https://img.shields.io/badge/Experience-3%2B_Years-green?style=for-the-badge" alt="Experience">
        <img src="https://img.shields.io/badge/Client_Satisfaction-100%25-brightgreen?style=for-the-badge" alt="Satisfaction">
    </div>

    <hr>

    <!-- ===== SKILLS ===== -->
    <h2>🚀 Tech Stack</h2>

    <div class="skills-grid">

        <div class="skill-card">
            <h4>🎨 Frontend</h4>
            <p class="skill-desc">Building responsive and interactive user interfaces</p>
            <div class="skill-tags">
                <span>React</span>
                <span>Next.js</span>
                <span>TypeScript</span>
                <span>Tailwind CSS</span>
                <span>HTML5</span>
                <span>CSS3</span>
            </div>
        </div>

        <div class="skill-card">
            <h4>⚙️ Backend</h4>
            <p class="skill-desc">Creating robust server-side applications</p>
            <div class="skill-tags">
                <span>Node.js</span>
                <span>Express.js</span>
                <span>REST APIs</span>
                <span>GraphQL</span>
            </div>
        </div>

        <div class="skill-card">
            <h4>🗄️ Databases</h4>
            <p class="skill-desc">Designing and optimizing data structures</p>
            <div class="skill-tags">
                <span>MongoDB</span>
                <span>Mongoose</span>
                <span>PostgreSQL</span>
                <span>Redis</span>
            </div>
        </div>

        <div class="skill-card">
            <h4>🔐 Auth & Security</h4>
            <p class="skill-desc">Implementing secure user authentication</p>
            <div class="skill-tags">
                <span>JWT</span>
                <span>OAuth</span>
                <span>Google Auth</span>
                <span>GitHub Auth</span>
                <span>Bcrypt</span>
            </div>
        </div>

        <div class="skill-card">
            <h4>📦 CMS & Platforms</h4>
            <p class="skill-desc">Working with popular content management systems</p>
            <div class="skill-tags">
                <span>WordPress</span>
                <span>Wix</span>
                <span>Shopify</span>
                <span>Webflow</span>
            </div>
        </div>

        <div class="skill-card">
            <h4>🛠️ Tools</h4>
            <p class="skill-desc">Utilizing modern development workflows</p>
            <div class="skill-tags">
                <span>VS Code</span>
                <span>Cursor</span>
                <span>Git</span>
                <span>GitHub</span>
                <span>Docker</span>
                <span>Postman</span>
            </div>
        </div>

    </div>

    <hr>

    <!-- ===== PROJECTS ===== -->
    <h2>🏗️ Featured Projects</h2>

    <div class="projects-grid">

        <div class="project-card">
            <span class="featured">⭐ Featured</span>
            <h3>🏢 COZONES</h3>
            <p>A comprehensive coworking space rental platform where users can discover, book, and manage workspace rentals on hourly, daily, or monthly basis.</p>
            <div class="tech-tags">
                <span>React</span>
                <span>Node.js</span>
                <span>MongoDB</span>
                <span>Express</span>
            </div>
            <div class="project-links">
                <a href="#">🔗 Live Demo</a>
                <a href="#">📂 Repository</a>
            </div>
        </div>

        <div class="project-card">
            <span class="featured">⭐ Featured</span>
            <h3>🏗️ Prime Consultants</h3>
            <p>A professional construction consultancy website featuring services showcase, project portfolio, and an innovative cost calculator.</p>
            <div class="tech-tags">
                <span>React</span>
                <span>JavaScript</span>
                <span>CSS</span>
                <span>Node.js</span>
            </div>
            <div class="project-links">
                <a href="#">🔗 Live Demo</a>
                <a href="#">📂 Repository</a>
            </div>
        </div>

        <div class="project-card">
            <span class="featured">⭐ Featured</span>
            <h3>📇 Card Scan Pro</h3>
            <p>An AI-powered business card scanner application using Gemini API that automatically extracts and organizes contact information.</p>
            <div class="tech-tags">
                <span>React</span>
                <span>Gemini API</span>
                <span>OCR</span>
                <span>Node.js</span>
            </div>
            <div class="project-links">
                <a href="#">🔗 Live Demo</a>
                <a href="#">📂 Repository</a>
            </div>
        </div>

        <div class="project-card">
            <h3>🔍 Prime Assessment Services</h3>
            <p>A comprehensive house inspection application with structured workflows for property assessments and detailed reporting.</p>
            <div class="tech-tags">
                <span>React</span>
                <span>MongoDB</span>
                <span>Express</span>
                <span>Node.js</span>
            </div>
            <div class="project-links">
                <a href="#">🔗 Live Demo</a>
                <a href="#">📂 Repository</a>
            </div>
        </div>

        <div class="project-card">
            <h3>🏗️ Case Forte Global</h3>
            <p>A building materials e-commerce platform with organized product catalogs and streamlined procurement workflows.</p>
            <div class="tech-tags">
                <span>WordPress</span>
                <span>WooCommerce</span>
                <span>PHP</span>
                <span>MySQL</span>
            </div>
            <div class="project-links">
                <a href="#">🔗 Live Demo</a>
                <a href="#">📂 Repository</a>
            </div>
        </div>

        <div class="project-card">
            <h3>📌 More Projects</h3>
            <p>Check out my GitHub repositories for more projects and contributions!</p>
            <br>
            <div class="project-links">
                <a href="https://github.com/your-username?tab=repositories">
                    <img src="https://img.shields.io/badge/View_All_Projects-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
                </a>
            </div>
        </div>

    </div>

    <hr>

    <!-- ===== EXPERIENCE ===== -->
    <h2>💼 Experience</h2>

    <div class="exp-item">
        <h4>💻 Web Developer Intern</h4>
        <div class="meta">Prime Consultants · Lahore, Pakistan · 2023 - Present</div>
        <p>Working as a Web Developer Intern, responsible for developing and maintaining multiple client projects including construction consultancy platforms, coworking space marketplaces, and AI-powered applications.</p>
        <ul>
            <li><strong>COZONES</strong> - Coworking space rental platform</li>
            <li><strong>Prime Consultants</strong> - Construction consultancy website</li>
            <li><strong>Card Scan Pro</strong> - AI business card scanner</li>
            <li><strong>Prime Assessment</strong> - House inspection application</li>
        </ul>
    </div>

    <hr>

    <!-- ===== EDUCATION ===== -->
    <h2>🎓 Education</h2>

    <div class="edu-item">
        <h4>🏛️ BSCS (Bachelor of Science in Computer Science)</h4>
        <div class="meta">Education University, Lahore · 2021 - Present · Seventh Semester</div>
        <p>Pursuing a comprehensive degree in Computer Science with focus on software engineering, web development, and modern programming paradigms.</p>
        <ul>
            <li>Active member of Computer Science Society</li>
            <li>Participated in coding competitions</li>
            <li>Developed multiple academic projects</li>
        </ul>
    </div>

    <div class="edu-item">
        <h4>🏫 ICS (Intermediate in Computer Science)</h4>
        <div class="meta">Punjab College, Lahore · 2019 - 2021 · Completed</div>
        <p>Completed intermediate education with focus on Computer Science, Mathematics, and Physics, building a strong foundation for technical studies.</p>
        <ul>
            <li>Excellent academic performance</li>
            <li>Strong foundation in programming basics</li>
            <li>Active participation in tech events</li>
        </ul>
    </div>

    <div class="edu-item">
        <h4>🏫 Matriculation (Science Group)</h4>
        <div class="meta">Universal Public School, Lahore · 2017 - 2019 · Completed</div>
        <p>Completed secondary education with Science group, developing analytical thinking and problem-solving skills.</p>
        <ul>
            <li>Science fair participant</li>
            <li>Mathematics excellence award</li>
        </ul>
    </div>

    <hr>

    <!-- ===== GITHUB STATS ===== -->
    <h2>📊 GitHub Stats</h2>

    <p align="center">
        <img src="https://github-readme-stats.vercel.app/api?username=your-username&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats" width="48%">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=your-username&theme=radical&hide_border=true" alt="GitHub Streak" width="48%">
    </p>

    <p align="center">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=your-username&layout=compact&theme=radical&hide_border=true" alt="Top Languages" width="48%">
    </p>

    <hr>

    <!-- ===== CONTACT ===== -->
    <h2>📫 Let's Connect</h2>

    <p style="text-align: center;">I'm currently open to new opportunities, freelance projects, and collaborations. Let's discuss how I can help bring your ideas to life!</p>

    <div class="badge-container">
        <a href="mailto:muhammadcaptain303@gmail.com">
            <img src="https://img.shields.io/badge/Email-muhammadcaptain303%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
        </a>
        <a href="#">
            <img src="https://img.shields.io/badge/Portfolio-Visit-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio">
        </a>
        <a href="https://github.com/your-username">
            <img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
        </a>
    </div>

    <table class="contact-table">
        <tr>
            <td>📧 Email</td>
            <td>muhammadcaptain303@gmail.com</td>
        </tr>
        <tr>
            <td>📱 Phone</td>
            <td>+92 327 409 7597</td>
        </tr>
        <tr>
            <td>📍 Location</td>
            <td>Lahore, Pakistan</td>
        </tr>
    </table>

    <hr>

    <!-- ===== QUOTE & FOOTER ===== -->
    <div class="quote">
        "Building exceptional digital experiences, one line of code at a time."
    </div>

    <div class="footer">
        Made with <span class="heart">❤️</span> by Muhammad
        <br>
        <span style="font-size: 0.8rem; color: #555;">© 2026 · All Rights Reserved</span>
    </div>

</div>

</body>
</html>
