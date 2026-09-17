<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Revanna Kumar - Developer and Computer Science Engineering Student">
    <title>Revanna Kumar | Developer Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #0f172a;
            color: #e2e8f0;
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: #020617;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #1e293b;
        }

        nav h2 {
            color: #38bdf8;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav ul li a {
            color: #e2e8f0;
            text-decoration: none;
            transition: 0.3s;
        }

        nav ul li a:hover {
            color: #38bdf8;
        }

        /* Hero */
        .hero {
            min-height: 90vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(135deg, #0f172a, #172554);
        }

        .hero-content {
            max-width: 800px;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #38bdf8;
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            color: white;
        }

        .hero h3 {
            color: #38bdf8;
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        .hero p {
            color: #cbd5e1;
            font-size: 1.1rem;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: #38bdf8;
            color: #020617;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            margin: 5px;
            transition: 0.3s;
        }

        .btn:hover {
            background: #0ea5e9;
            transform: translateY(-2px);
        }

        .btn-outline {
            background: transparent;
            color: #38bdf8;
            border: 2px solid #38bdf8;
        }

        .btn-outline:hover {
            background: #38bdf8;
            color: #020617;
        }

        /* Sections */
        section {
            padding: 80px 8%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 45px;
        }

        .section-title h2 {
            font-size: 2.3rem;
            color: white;
        }

        .section-title span {
            color: #38bdf8;
        }

        /* About */
        .about {
            max-width: 900px;
            margin: auto;
            text-align: center;
        }

        .about p {
            color: #cbd5e1;
            font-size: 1.05rem;
            margin-bottom: 15px;
        }

        /* Education */
        .education-card {
            max-width: 800px;
            margin: auto;
            background: #1e293b;
            padding: 30px;
            border-radius: 12px;
            border-left: 5px solid #38bdf8;
        }

        .education-card h3 {
            color: #38bdf8;
            margin-bottom: 8px;
        }

        .education-card p {
            color: #cbd5e1;
        }

        /* Skills */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
        }

        .skill {
            background: #1e293b;
            padding: 25px;
            text-align: center;
            border-radius: 10px;
            transition: 0.3s;
        }

        .skill:hover {
            transform: translateY(-5px);
            background: #263449;
        }

        .skill h3 {
            color: #38bdf8;
            margin-bottom: 8px;
        }

        .skill p {
            color: #cbd5e1;
        }

        /* Projects */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .project {
            background: #1e293b;
            padding: 25px;
            border-radius: 12px;
            transition: 0.3s;
        }

        .project:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }

        .project h3 {
            color: #38bdf8;
            margin-bottom: 10px;
        }

        .project p {
            color: #cbd5e1;
            margin-bottom: 15px;
        }

        /* Goals */
        .goals {
            max-width: 850px;
            margin: auto;
        }

        .goals ul {
            list-style: none;
        }

        .goals li {
            background: #1e293b;
            padding: 15px 20px;
            margin-bottom: 12px;
            border-radius: 8px;
            border-left: 4px solid #38bdf8;
        }

        /* Contact */
        .contact {
            text-align: center;
        }

        .contact p {
            color: #cbd5e1;
            margin-bottom: 20px;
        }

        .social-links a {
            display: inline-block;
            margin: 8px;
            color: #38bdf8;
            text-decoration: none;
            border: 1px solid #38bdf8;
            padding: 10px 18px;
            border-radius: 6px;
            transition: 0.3s;
        }

        .social-links a:hover {
            background: #38bdf8;
            color: #020617;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 25px;
            background: #020617;
            color: #94a3b8;
        }

        /* Mobile */
        @media (max-width: 700px) {
            nav {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h3 {
                font-size: 1.2rem;
            }

            section {
                padding: 60px 5%;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->
    <nav>
        <h2>Revanna Kumar</h2>

        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>


    <!-- Hero Section -->
    <section class="hero" id="home">

        <div class="hero-content">

            <!-- Replace profile.jpg with your actual photo -->
            <img src="profile.jpg" alt="Revanna Kumar" class="profile-img">

            <h1>Hi, I'm Revanna Kumar</h1>

            <h3>Developer | CSE Student | Tech Enthusiast</h3>

            <p>
                I am a Computer Science and Engineering student pursuing
                Bachelor of Engineering at KVG College of Engineering.
                I am passionate about software development, programming,
                web technologies and building innovative solutions.
            </p>

            <a href="#about" class="btn">Explore My Profile</a>
            <a href="#contact" class="btn btn-outline">Contact Me</a>

        </div>

    </section>


    <!-- About Section -->
    <section id="about">

        <div class="section-title">
            <h2>About <span>Me</span></h2>
        </div>

        <div class="about">

            <p>
                Hello! I'm <strong>Revanna Kumar</strong>, a passionate
                developer and Computer Science and Engineering student.
            </p>

            <p>
                I am currently pursuing my Bachelor of Engineering (BE)
                in Computer Science and Engineering at
                <strong>KVG College of Engineering</strong>.
            </p>

            <p>
                I enjoy learning new technologies, solving programming
                problems and developing applications that can solve
                real-world problems. I am continuously improving my
                technical and problem-solving skills through projects,
                practice and self-learning.
            </p>

            <p>
                My goal is to become a skilled software developer and
                contribute to meaningful technology projects while
                continuously learning and growing in the field of
                computer science.
            </p>

        </div>

    </section>


    <!-- Education Section -->
    <section id="education">

        <div class="section-title">
            <h2>My <span>Education</span></h2>
        </div>

        <div class="education-card">

            <h3>Bachelor of Engineering - Computer Science & Engineering</h3>

            <p>
                <strong>KVG College of Engineering</strong>
            </p>

            <p>
                Currently pursuing BE in Computer Science and Engineering.
            </p>

            <p>
                Focus areas include programming, software development,
                data structures, web development, databases and
                emerging technologies.
            </p>

        </div>

    </section>


    <!-- Skills Section -->
    <section id="skills">

        <div class="section-title">
            <h2>Technical <span>Skills</span></h2>
        </div>

        <div class="skills-container">

            <div class="skill">
                <h3>HTML</h3>
                <p>Web Structure & Semantic HTML</p>
            </div>

            <div class="skill">
                <h3>CSS</h3>
                <p>Responsive Web Design</p>
            </div>

            <div class="skill">
                <h3>JavaScript</h3>
                <p>Interactive Web Applications</p>
            </div>

            <div class="skill">
                <h3>Python</h3>
                <p>Programming & Problem Solving</p>
            </div>

            <div class="skill">
                <h3>Java</h3>
                <p>Object-Oriented Programming</p>
            </div>

            <div class="skill">
                <h3>C / C++</h3>
                <p>Programming Fundamentals</p>
            </div>

            <div class="skill">
                <h3>Git & GitHub</h3>
                <p>Version Control & Collaboration</p>
            </div>

            <div class="skill">
                <h3>SQL</h3>
                <p>Database Management</p>
            </div>

        </div>

    </section>


    <!-- Projects Section -->
    <section id="projects">

        <div class="section-title">
            <h2>My <span>Projects</span></h2>
        </div>

        <div class="projects-container">

            <div class="project">

                <h3>Personal Portfolio</h3>

                <p>
                    A responsive personal portfolio website created using
                    HTML, CSS and JavaScript to showcase my skills,
                    education and projects.
                </p>

                <a href="#" class="btn">View Project</a>

            </div>


            <div class="project">

                <h3>Student Management System</h3>

                <p>
                    A project designed to manage student information,
                    academic details and records using programming and
                    database concepts.
                </p>

                <a href="#" class="btn">View Project</a>

            </div>


            <div class="project">

                <h3>Web Development Project</h3>

                <p>
                    A web-based application developed to practice
                    frontend development, responsive design and
                    user-friendly interfaces.
                </p>

                <a href="#" class="btn">View Project</a>

            </div>

        </div>

    </section>


    <!-- Goals Section -->
    <section>

        <div class="section-title">
            <h2>My <span>Goals</span></h2>
        </div>

        <div class="goals">

            <ul>
                <li>Become a professional software developer.</li>
                <li>Build real-world applications and projects.</li>
                <li>Improve my problem-solving and programming skills.</li>
                <li>Learn modern web and software development technologies.</li>
                <li>Contribute to open-source projects.</li>
                <li>Continuously learn and adapt to new technologies.</li>
            </ul>

        </div>

    </section>


    <!-- Contact Section -->
    <section id="contact">

        <div class="section-title">
            <h2>Contact <span>Me</span></h2>
        </div>

        <div class="contact">

            <p>
                I'm always interested in learning, collaborating and
                working on interesting technology projects.
            </p>

            <div class="social-links">

                <!-- Replace # with your actual links -->

                <a href="https://github.com/" target="_blank">
                    GitHub
                </a>

                <a href="https://www.linkedin.com/" target="_blank">
                    LinkedIn
                </a>

                <a href="mailto:your-email@example.com">
                    Email
                </a>

            </div>

        </div>

    </section>


    <!-- Footer -->
    <footer>

        <p>
            © 2026 Revanna Kumar. All Rights Reserved.
        </p>

        <p>
            Built with HTML & CSS ❤️
        </p>

    </footer>

</body>
</html>
