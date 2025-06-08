<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yuvraj Kumar Mahato - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2c3e50;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --accent: #e74c3c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1517694712202-14dd9538aa97?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover;
            opacity: 0.2;
            z-index: 0;
        }
        
        header > * {
            position: relative;
            z-index: 1;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            margin-bottom: 1rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        h2 {
            font-size: 1.8rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--primary);
        }
        
        h3 {
            font-size: 1.4rem;
            color: var(--dark);
            margin: 1rem 0;
        }
        
        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 1.5rem;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .section {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
            margin-bottom: 2rem;
        }
        
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
        }
        
        .experience-item, .education-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }
        
        .experience-item:last-child, .education-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        .job-title, .degree {
            font-weight: 600;
            color: var(--dark);
            margin-bottom: 0.3rem;
        }
        
        .company, .university {
            font-weight: 500;
            color: var(--primary);
        }
        
        .date {
            font-size: 0.9rem;
            color: #777;
            margin-bottom: 0.5rem;
        }
        
        ul {
            padding-left: 1.5rem;
        }
        
        li {
            margin-bottom: 0.5rem;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .skill-category {
            flex: 1;
            min-width: 250px;
        }
        
        .skill-tag {
            display: inline-block;
            background-color: var(--light);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            margin: 0.3rem;
            font-size: 0.9rem;
            transition: all 0.3s;
        }
        
        .skill-tag:hover {
            background-color: var(--primary);
            color: white;
            transform: scale(1.05);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-link {
            color: var(--dark);
            font-size: 1.5rem;
            transition: color 0.3s, transform 0.3s;
        }
        
        .social-link:hover {
            color: var(--primary);
            transform: scale(1.2);
        }
        
        .project-card {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        
        .project-content {
            padding: 1.5rem;
        }
        
        .project-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .project-description {
            margin-bottom: 1rem;
            color: #666;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .tech-tag {
            background-color: var(--light);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-link {
            display: inline-block;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .project-link:hover {
            color: var(--secondary);
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
            text-align: center;
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            font-size: 1rem;
            color: #666;
        }
        
        footer {
            text-align: center;
            padding: 2rem 0;
            color: #666;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .grid-container {
                grid-template-columns: 1fr;
            }
            
            .skills-container {
                flex-direction: column;
            }
        }
        
        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animated {
            animation: fadeIn 0.6s ease-out forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        .delay-4 { animation-delay: 0.8s; }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <!-- Replace with your actual image -->
            <img src="https://avatars.githubusercontent.com/u/60013703?v=4" alt="Yuvraj Kumar Mahato" class="profile-img">
            <h1>Yuvraj Kumar Mahato</h1>
            <p class="tagline">Computer Engineer | Software Developer | AI & ML Enthusiast</p>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Kathmandu, Nepal</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+977-9864040186</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>yuvrajkumarmahato@gmail.com</span>
                </div>
            </div>
            <div class="social-links">
                <a href="https://github.com/yuvraj333" target="_blank" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/in/yuvraj-kumar-mahato14ab871b3/" target="_blank" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://twitter.com/yuvrajkumarmah5" target="_blank" class="social-link">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="https://www.facebook.com/yuvraj.kushwaha.9659" target="_blank" class="social-link">
                    <i class="fab fa-facebook-f"></i>
                </a>
                <a href="https://www.instagram.com/yuvrajkushwaha90" target="_blank" class="social-link">
                    <i class="fab fa-instagram"></i>
                </a>
            </div>
        </div>
    </header>

    <div class="container">
        <section class="section animated">
            <h2>Professional Summary</h2>
            <p>Innovative and Self-Motivated Computer Engineer with a strong foundation in software development, AI, and cloud technologies. Passionate about leveraging Python, machine learning, and scalable architectures to build smart solutions that address real-world challenges. Proven leadership in driving collaborative tech projects, with a commitment to continuous learning and innovation.</p>
        </section>

        <div class="grid-container">
            <section class="section animated delay-1">
                <h2>Experience</h2>
                
                <div class="experience-item">
                    <h3 class="job-title">Software Developer (Freelancer)</h3>
                    <p class="company">Remote</p>
                    <p class="date">Aug 2020 – Present</p>
                    <ul>
                        <li>Design and develop AI-powered and full-stack web/mobile applications.</li>
                        <li>Build scalable systems using Python (Django, Flask, FastAPI), JavaScript, and React.js.</li>
                        <li>Integrated machine learning models and managed cloud/database deployments.</li>
                        <li>Collaborate with clients for requirements, testing, and product delivery using Git, Docker, and Linux.</li>
                    </ul>
                </div>
                
                <div class="experience-item">
                    <h3 class="job-title">Python Developer – AI & Backend Focus</h3>
                    <p class="company">Annil Technologies, Lalitpur</p>
                    <p class="date">Jan 2024 – Jul 2024</p>
                    <ul>
                        <li>Developed backend logic and REST APIs using Django/Flask.</li>
                        <li>Managed MySQL/PostgreSQL databases and Dockerized applications.</li>
                        <li>Collaborated on AI model integration and deployment.</li>
                        <li>Used Git and Linux for version control and DevOps.</li>
                    </ul>
                </div>
            </section>

            <section class="section animated delay-2">
                <h2>Education</h2>
                <div class="education-item">
                    <h3 class="degree">Bachelor of Engineering in Computer Engineering</h3>
                    <p class="university">Nepal Engineering College, Pokhara University</p>
                    <p class="date">Nov 2018 – Aug 2023</p>
                    <p>CGPA: 3.242 / 4.0 (79%) | Full Scholarship Recipient</p>
                </div>
                
                <h2 style="margin-top: 2rem;">Certifications</h2>
                <ul>
                    <li>Python for Everybody – University of Michigan (Coursera, 2020)</li>
                    <li>Full-Stack Web Development – Johns Hopkins University (Coursera, 2020)</li>
                </ul>
                
                <h2 style="margin-top: 2rem;">Leadership & Achievements</h2>
                <ul>
                    <li>Full Scholarship Recipient for B.E. in Computer Engineering (Pokhara University)</li>
                    <li>Member, Google Developer Student Club (Funded by Google)</li>
                    <li>Project Management & Technical Lead, NEC Ingenium 2023</li>
                    <li>Former Secretary, NEC IT Club</li>
                </ul>
            </section>
        </div>

        <section class="section animated delay-3">
            <h2>Technical Skills</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Programming</h3>
                    <div>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">C++</span>
                        <span class="skill-tag">C#</span>
                        <span class="skill-tag">Java</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>AI/ML</h3>
                    <div>
                        <span class="skill-tag">Deep Learning</span>
                        <span class="skill-tag">CNN</span>
                        <span class="skill-tag">Scikit-learn</span>
                        <span class="skill-tag">OpenCV</span>
                        <span class="skill-tag">Pandas</span>
                        <span class="skill-tag">LLM</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Backend</h3>
                    <div>
                        <span class="skill-tag">Django</span>
                        <span class="skill-tag">Flask</span>
                        <span class="skill-tag">FastAPI</span>
                        <span class="skill-tag">Node.js</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Frontend</h3>
                    <div>
                        <span class="skill-tag">React.js</span>
                        <span class="skill-tag">HTML5</span>
                        <span class="skill-tag">CSS3</span>
                        <span class="skill-tag">Tailwind CSS</span>
                        <span class="skill-tag">Bootstrap</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Databases</h3>
                    <div>
                        <span class="skill-tag">MS SQL Server</span>
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">PostgreSQL</span>
                        <span class="skill-tag">SQLite</span>
                        <span class="skill-tag">MongoDB</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & DevOps</h3>
                    <div>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">Docker</span>
                        <span class="skill-tag">Linux</span>
                        <span class="skill-tag">VS Code</span>
                        <span class="skill-tag">Nginx</span>
                        <span class="skill-tag">Heroku</span>
                        <span class="skill-tag">Render</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Cloud Technologies</h3>
                    <div>
                        <span class="skill-tag">AWS</span>
                        <span class="skill-tag">Google Cloud</span>
                        <span class="skill-tag">Azure</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="section animated delay-4">
            <h2>Featured Projects</h2>
            <div class="grid-container">
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">LLM based Product Recommendation System</h3>
                        <p class="project-description">FastAPI-based recommendation system powered by GPT-3.5, featuring PostgreSQL for data storage, caching, user authentication, and feedback handling.</p>
                        <div class="project-tech">
                            <span class="tech-tag">FastAPI</span>
                            <span class="tech-tag">PostgreSQL</span>
                            <span class="tech-tag">OpenAI GPT-3.5</span>
                            <span class="tech-tag">Caching</span>
                            <span class="tech-tag">User Authentication</span>
                        </div>
                        <a href="https://github.com/yuvraj333/llm-product-recommendation-system" target="_blank" class="project-link">View on GitHub →</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Skin Disease Detection & Remedies Suggestion</h3>
                        <p class="project-description">AI-based web & mobile app to detect skin conditions and suggest remedies using CNN models.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Flask</span>
                            <span class="tech-tag">CNN Models</span>
                            <span class="tech-tag">HTML5</span>
                            <span class="tech-tag">CSS3</span>
                            <span class="tech-tag">JavaScript</span>
                        </div>
                        <a href="https://github.com/yuvraj333/Skin-Disease-Detection-and-RemediesSuggestions" target="_blank" class="project-link">View on GitHub →</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Rice Leaf Disease Detection System</h3>
                        <p class="project-description">AI-powered mobile/web app for farmers to identify rice leaf diseases using camera or gallery images.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Flask</span>
                            <span class="tech-tag">OpenCV</span>
                            <span class="tech-tag">Machine Learning</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">Bootstrap</span>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-content">
                        <h3 class="project-title">Student Management System For CSE Department</h3>
                        <p class="project-description">Web app to manage student, teacher, syllabus, routine, notices, and results online.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">HTML5</span>
                            <span class="tech-tag">CSS3</span>
                            <span class="tech-tag">Bootstrap</span>
                            <span class="tech-tag">SQLite3</span>
                        </div>
                        <a href="https://github.com/yuvraj333/Student-Management-System-For-CSE-Department" target="_blank" class="project-link">View on GitHub →</a>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=yuvraj333&show_icons=true&theme=transparent&include_all_commits=true&count_private=true&rank_icon=github" alt="GitHub Stats" style="width: 100%;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs?username=yuvraj333&show_icons=true&locale=en&layout=compact&theme=transparent" alt="Top Languages" style="width: 100%;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=yuvraj333&theme=transparent" alt="GitHub Streak" style="width: 100%;">
                </div>
            </div>
        </section>

        <section class="section">
            <h2>Get In Touch</h2>
            <p>I'm currently looking for new opportunities in software development, particularly in Python and AI-related projects. Feel free to reach out if you'd like to collaborate or just say hello!</p>
            <div style="text-align: center; margin-top: 2rem;">
                <a href="mailto:yuvrajkumarmahato@gmail.com" style="display: inline-block; background-color: var(--primary); color: white; padding: 1rem 2rem; border-radius: 30px; text-decoration: none; font-weight: 600; transition: all 0.3s;">Contact Me</a>
            </div>
        </section>
    </div>

    <footer>
        <div class="container">
            <p>© 2024 Yuvraj Kumar Mahato. All rights reserved.</p>
            <p style="margin-top: 0.5rem;">
                <span style="margin-right: 1rem;"><i class="fas fa-map-marker-alt"></i> Kathmandu, Nepal</span>
                <span><i class="fas fa-phone"></i> +977-9864040186</span>
            </p>
        </div>
    </footer>
</body>
</html>
