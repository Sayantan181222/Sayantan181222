<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sayantan Mandal // System</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #050508;
            font-family: 'Share Tech Mono', monospace;
            color: #00FFCC;
            overflow-x: hidden;
        }
        /* Cyberpunk Grid Background */
        .grid-bg {
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 204, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 204, 0.1) 1px, transparent 1px);
            background-size: 40px 40px;
            z-index: -1;
        }
        .container {
            padding: 40px;
            max-width: 800px;
            margin: 0 auto;
        }
        h1 {
            font-size: 2.5rem;
            color: #fff;
            text-shadow: 0 0 10px #00FFCC;
            margin-bottom: 5px;
        }
        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background-color: #00FFCC;
            animation: blink 1s infinite;
            vertical-align: middle;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
        .role {
            color: #FF00AA;
            text-shadow: 0 0 10px #FF00AA;
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        .tabs {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
            border-bottom: 2px solid #1a1a2e;
        }
        .tab-btn {
            background: none;
            border: none;
            color: #5e5e72;
            font-family: 'Share Tech Mono', monospace;
            font-size: 1rem;
            cursor: pointer;
            padding: 10px 15px;
            transition: all 0.3s;
        }
        .tab-btn:hover, .tab-btn.active {
            color: #00FFCC;
            text-shadow: 0 0 8px #00FFCC;
            border-bottom: 2px solid #00FFCC;
        }
        .content-box {
            border: 1px solid #1a1a2e;
            padding: 20px;
            background: rgba(13, 17, 23, 0.8);
            border-radius: 5px;
            min-height: 200px;
        }
        ul { list-style-type: none; padding: 0; }
        li { margin-bottom: 10px; }
        .highlight { color: #FFEA00; }
        a { color: #00FFCC; text-decoration: none; }
        a:hover { text-decoration: underline; }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet">
</head>
<body>
    <div class="grid-bg"></div>

    <div class="container">
        <h1>Sayantan Mandal<span class="cursor"></span></h1>
        <div class="role">&gt; AI & SYSTEMS ENGINEER // CODEFORCES: 1556</div>

        <div class="tabs">
            <button class="tab-btn active" onclick="showTab('about', this)">&gt; About_Me.sys</button>
            <button class="tab-btn" onclick="showTab('projects', this)">&gt; Projects.sys</button>
            <button class="tab-btn" onclick="showTab('skills', this)">&gt; Skills.sys</button>
        </div>

        <div class="content-box" id="content">
            <!-- Default Content -->
            <ul>
                <li>&gt; <span class="highlight">STATUS:</span> ACTIVE</li>
                <li>&gt; <span class="highlight">EDUCATION:</span> B.Tech in AI & Data Science (CGPA: 8.65)</li>
                <li>&gt; <span class="highlight">EXPERIENCE:</span> SDE Intern @ BISAG (FastAPI, Neo4j, OSINT)</li>
                <li>&gt; <span class="highlight">ACHIEVEMENTS:</span> Meta PyTorch OpenEnv Finalist | CF Global Rank 397</li>
                <li>&gt; <span class="highlight">CONTACT:</span> sayantanman508@gmail.com</li>
            </ul>
        </div>
    </div>

    <script>
        const contentData = {
            about: `
                <ul>
                    <li>&gt; <span class="highlight">STATUS:</span> ACTIVE</li>
                    <li>&gt; <span class="highlight">EDUCATION:</span> B.Tech in AI & Data Science (CGPA: 8.65)</li>
                    <li>&gt; <span class="highlight">EXPERIENCE:</span> SDE Intern @ BISAG (FastAPI, Neo4j, OSINT)</li>
                    <li>&gt; <span class="highlight">ACHIEVEMENTS:</span> Meta PyTorch OpenEnv Finalist | CF Global Rank 397</li>
                    <li>&gt; <span class="highlight">CONTACT:</span> sayantanman508@gmail.com</li>
                </ul>
            `,
            projects: `
                <ul>
                    <li>&gt; <span class="highlight">[C++] Dedupex:</span> Systems-level backup engine using Rabin fingerprinting & SHA256.</li>
                    <li>&gt; <span class="highlight">[Python] PhishSentry:</span> Automated phishing detection pipeline. Docker, AWS, MLflow.</li>
                    <li>&gt; <span class="highlight">[Python] EduMatrix:</span> Predictive analytics model forecasting student performance (90% R²).</li>
                    <li>&gt; <span class="highlight">[LLM] OpenEnv Triage:</span> RAG pipeline using LangChain & FAISS for disaster management.</li>
                </ul>
            `,
            skills: `
                <ul>
                    <li>&gt; <span class="highlight">LANGUAGES:</span> Java, Python, C++, C, SQL</li>
                    <li>&gt; <span class="highlight">AI/ML:</span> LangChain, RAG, FAISS, TensorFlow, PyTorch</li>
                    <li>&gt; <span class="highlight">BACKEND:</span> FastAPI, Flask, PostgreSQL, MongoDB, Neo4j</li>
                    <li>&gt; <span class="highlight">DEVOPS:</span> Docker, AWS (EC2, S3), CI/CD, Linux, MLflow</li>
                </ul>
            `
        };

        function showTab(tabName, btn) {
            // Update content
            document.getElementById('content').innerHTML = contentData[tabName];
            
            // Update active button
            let buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(b => b.classList.remove('active'));
            btn.classList.add('active');
        }
    </script>
</body>
</html>
