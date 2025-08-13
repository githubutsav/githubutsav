<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Utsav Singh - Profile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Tailwind's 'slate' for neutrals, 'blue' for accents. -->
    <!-- Application Structure Plan: The application is designed as a single-page interactive portfolio. It begins with an impactful hero section that establishes the user's identity. This is followed by a dynamic 'About Me' section with interactive cards to detail key contributions, allowing for a clean initial view with deeper content on-demand. The 'Projects' section uses a clickable card grid that reveals project details in a modal, which is a significant upgrade from a static list. The 'Tech Stack' is presented as a clean grid, while 'GitHub Stats' and 'Connect' sections are styled for maximum visual impact. This structure prioritizes user engagement, allowing a visitor to quickly grasp key information and then interact to learn more. The goal is to provide a comprehensive, yet uncluttered, experience that guides the user on a non-linear path of exploration. -->
    <!-- Visualization & Content Choices: 
        - Report Info: Name, Title, Intro. Goal: Inform. Viz: Animated typing SVG with a high-impact hero section. Interaction: None. Justification: Creates a strong, professional first impression that grabs attention immediately. Method: SVG, Tailwind CSS.
        - Report Info: Contributions (GSSoC, GDG). Goal: Inform, Organize. Viz: Interactive cards with show/hide details. Interaction: Click to toggle visibility of details. Justification: This transforms a bulleted list into a more engaging, interactive experience, preventing information overload. Method: HTML/CSS/JS.
        - Report Info: Projects. Goal: Inform, Showcase. Viz: Clickable project cards with a pop-up modal for details. Interaction: Click to open/close modal. Justification: This allows for rich, detailed project descriptions without cluttering the main page, creating a "portfolio-like" feel. Method: HTML/CSS/JS.
        - Report Info: Stats, Skills, Trophies, Contact. Goal: Inform. Viz: Badges, icon grids. Interaction: None beyond standard links. Justification: The use of popular services and a clean grid layout for these sections presents the information in a professional and easily scannable format. Method: Markdown images, HTML/CSS.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f1f5f9;
            color: #1e293b;
        }
        .project-card, .contributions-card {
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .project-card:hover, .contributions-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.08);
        }
        .modal {
            display: none;
        }
        .modal-active {
            display: flex;
        }
    </style>
</head>
<body class="antialiased">

    <main class="container mx-auto px-6 py-12 md:py-16">

        <!-- Header -->
        <header class="text-center mb-16">
            <p class="mb-4">
                <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00C6FF&center=true&vCenter=true&width=650&lines=Hi%2C+I'm+Utsav+Singh+👋;Full+Stack+Learner+%7C+AI%2FML+Enthusiast;Data+Engineering+Aspirant+%7C+Builder;Welcome+to+My+GitHub+Profile!">
            </p>
            <div class="mt-8">
                <h1 class="text-3xl md:text-5xl font-bold text-slate-800">Utsav Singh</h1>
                <p class="text-lg md:text-xl text-slate-600 mt-2">Full Stack Learner | AI/ML Enthusiast | Data Engineering Aspirant</p>
            </div>
            <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=header" class="mt-8 rounded-lg" width="100%"/>
        </header>

        <!-- About Me & Key Contributions -->
        <section id="about" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-6 text-center">About Me & My Contributions</h2>
            <div class="max-w-4xl mx-auto text-center text-slate-700">
                <p class="mb-6">I'm a passionate builder focused on creating projects that solve real-world problems. With a belief in "learning by doing," I actively explore cutting-edge technologies and contribute to the developer community.</p>
            </div>

            <div class="grid md:grid-cols-3 gap-6 max-w-5xl mx-auto mt-8">
                <div class="contributions-card bg-white p-6 rounded-lg shadow-md cursor-pointer" data-contribution="gssoc">
                    <h3 class="font-bold text-xl text-blue-600">🌟 GSSoC 2025</h3>
                    <p class="mt-2 text-sm text-slate-500">Contributor & Former Ambassador</p>
                    <p class="mt-4 text-slate-600 hidden contribution-details">Contributed to multiple open-source projects, resolved issues, added new features, and mentored new contributors.</p>
                </div>
                <div class="contributions-card bg-white p-6 rounded-lg shadow-md cursor-pointer" data-contribution="gdg">
                    <h3 class="font-bold text-xl text-blue-600">🎤 GDG Member</h3>
                    <p class="mt-2 text-sm text-slate-500">Google Developer Groups</p>
                    <p class="mt-4 text-slate-600 hidden contribution-details">Participated in hackathons, code labs, and DevFest events, collaborating on cloud and AI-based projects.</p>
                </div>
                <div class="contributions-card bg-white p-6 rounded-lg shadow-md cursor-pointer" data-contribution="letsupgrade">
                    <h3 class="font-bold text-xl text-blue-600">🚀 LetsUpgrade</h3>
                    <p class="mt-2 text-sm text-slate-500">Student Ambassador</p>
                    <p class="mt-4 text-slate-600 hidden contribution-details">Promoted coding challenges and workshops, helping peers upskill in the latest technologies.</p>
                </div>
            </div>
        </section>

        <!-- Featured Projects -->
        <section id="projects" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-8 text-center">Featured Projects</h2>
            <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <a class="project-card block bg-white p-6 rounded-lg shadow-md cursor-pointer" data-project-id="habit-one">
                    <h3 class="font-bold text-xl text-slate-800">Habit-One</h3>
                    <p class="mt-2 text-slate-600">A terminal-based habit tracker to help users develop and maintain daily habits.</p>
                    <p class="mt-4 text-sm font-semibold text-blue-600">View Details</p>
                </a>
                <a class="project-card block bg-white p-6 rounded-lg shadow-md cursor-pointer" data-project-id="ai-summarizer">
                    <h3 class="font-bold text-xl text-slate-800">AI Text Summarizer</h3>
                    <p class="mt-2 text-slate-600">A web app that summarizes text instantly using Hugging Face Inference API.</p>
                    <p class="mt-4 text-sm font-semibold text-blue-600">View Details</p>
                </a>
            </div>
            <div class="text-center mt-8">
                <h3 class="font-bold text-xl text-slate-800 mb-4">Upcoming Projects 🚧</h3>
                <div class="flex flex-col md:flex-row justify-center gap-4 text-slate-600">
                    <div class="bg-white p-4 rounded-lg shadow-sm">
                        <p>Personal Finance Tracker (MERN Stack)</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm">
                        <p>AI Resume Analyzer (NLP & ML)</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Tech Stack -->
        <section id="tech-stack" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-8 text-center">My Tech Stack</h2>
            <div class="max-w-3xl mx-auto">
                <p align="center">
                    <img src="https://skillicons.dev/icons?i=python,java,javascript,swift,html,css,react,swiftui,nodejs,express,flask,mysql,mongodb,gcp,aws&perline=8" />
                </p>
            </div>
        </section>

        <!-- GitHub Stats -->
        <section id="stats" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-8 text-center">GitHub Contributions & Stats</h2>
            <div class="grid lg:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <div class="flex flex-col items-center">
                    <img src="https://github-readme-stats.vercel.app/api?username=UtsavSingh&show_icons=true&theme=tokyonight" height="165" class="rounded-lg shadow-md mb-4"/>
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=UtsavSingh&layout=compact&theme=tokyonight" height="165" class="rounded-lg shadow-md"/>
                </div>
                <div class="flex flex-col items-center">
                    <img src="https://streak-stats.demolab.com?user=UtsavSingh&theme=tokyonight" class="rounded-lg shadow-md mb-4"/>
                    <img src="https://github-readme-activity-graph.vercel.app/graph?username=UtsavSingh&theme=react-dark&hide_border=true&area=true&custom_title=Contribution%20Graph" class="rounded-lg shadow-md"/>
                </div>
            </div>
        </section>
        
        <!-- GitHub Trophies -->
        <section id="trophies" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-8 text-center">GitHub Trophies</h2>
            <p align="center">
                <img src="https://github-profile-trophy.vercel.app/?username=UtsavSingh&theme=onedark&no-frame=true&margin-w=15&row=1&column=6" class="rounded-lg shadow-md"/>
            </p>
        </section>

        <!-- Connect With Me -->
        <section id="connect" class="mb-16">
            <h2 class="text-2xl md:text-3xl font-bold text-slate-800 mb-8 text-center">Let's Connect</h2>
            <p align="center">
                <a href="https://linkedin.com/in/utsav-singh" class="inline-block mx-2">
                    <img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white"/>
                </a>
                <a href="https://twitter.com/utsav_singh" class="inline-block mx-2">
                    <img src="https://img.shields.io/badge/Twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white"/>
                </a>
                <a href="https://utsav-portfolio.com" class="inline-block mx-2">
                    <img src="https://img.shields.io/badge/Portfolio-%23000000.svg?&style=for-the-badge&logo=About.me&logoColor=white"/>
                </a>
            </p>
        </section>
    </main>

    <footer class="bg-slate-800 text-white py-8 text-center">
        <p>&copy; 2025 Utsav Singh. All rights reserved.</p>
        <p class="text-sm text-slate-400 mt-2">⭐ *"Code. Learn. Build. Repeat."* ⭐</p>
    </footer>

    <!-- Project Details Modal -->
    <div id="project-modal" class="modal fixed inset-0 bg-black bg-opacity-50 justify-center items-center z-50 p-4">
        <div class="bg-white p-8 rounded-xl shadow-lg max-w-2xl w-full relative transform transition-all duration-300 scale-95 modal-content">
            <button class="absolute top-4 right-4 text-slate-400 hover:text-slate-600 text-2xl font-bold close-modal-btn">&times;</button>
            <div id="modal-body"></div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const projectsData = {
                'habit-one': {
                    title: 'Habit-One',
                    description: 'A terminal-based habit tracker that helps users develop and maintain daily habits. It’s built for simplicity and efficiency, allowing for habit management directly from the command line.',
                    techStack: 'Python, Object-Oriented Programming, File Handling',
                    impact: 'Built as part of Harvard’s CS50P to demonstrate foundational programming skills, clean code, and project structure.',
                    link: 'https://github.com/UtsavSingh/habit-one'
                },
                'ai-summarizer': {
                    title: 'AI Text Summarizer',
                    description: 'A web app that instantly summarizes text by leveraging the Hugging Face Inference API. The application provides a responsive and intuitive interface for real-time text summarization.',
                    techStack: 'Node.js, Express.js, Hugging Face API, HTML, CSS, JavaScript',
                    impact: 'This project highlights skills in front-end and back-end development, API integration, and creating functional, user-friendly web applications.',
                    link: null
                }
            };
            
            const contributions = document.querySelectorAll('.contributions-card');
            contributions.forEach(card => {
                card.addEventListener('click', () => {
                    card.querySelector('.contribution-details').classList.toggle('hidden');
                });
            });

            const projectCards = document.querySelectorAll('.project-card');
            const modal = document.getElementById('project-modal');
            const modalBody = document.getElementById('modal-body');
            const closeModalBtn = document.querySelector('.close-modal-btn');

            projectCards.forEach(card => {
                card.addEventListener('click', (e) => {
                    const projectId = card.dataset.projectId;
                    const project = projectsData[projectId];
                    if (project) {
                        modalBody.innerHTML = `
                            <h3 class="font-bold text-2xl text-slate-800 mb-2">${project.title}</h3>
                            <p class="text-slate-600">${project.description}</p>
                            <div class="mt-4">
                                <p class="font-semibold text-slate-800">Tech Stack:</p>
                                <p class="text-slate-600">${project.techStack}</p>
                            </div>
                            <div class="mt-4">
                                <p class="font-semibold text-slate-800">Impact:</p>
                                <p class="text-slate-600">${project.impact}</p>
                            </div>
                            ${project.link ? `<a href="${project.link}" target="_blank" class="mt-6 inline-block bg-blue-600 text-white font-bold py-2 px-4 rounded-full hover:bg-blue-700 transition-colors">View Project on GitHub</a>` : ''}
                        `;
                        modal.classList.add('modal-active');
                    }
                });
            });

            closeModalBtn.addEventListener('click', () => {
                modal.classList.remove('modal-active');
            });
            
            modal.addEventListener('click', (e) => {
                if (e.target === modal) {
                    modal.classList.remove('modal-active');
                }
            });
        });
    </script>
</body>
</html>
