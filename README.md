<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SP-XD GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        }
        
        body {
            background-color: #0d1117;
            color: #c9d1d9;
            padding: 20px;
            line-height: 1.5;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 20px 0;
            border-bottom: 1px solid #30363d;
        }
        
        .gif-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        
        .gif-container img {
            max-width: 60%;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 255, 255, 0.3);
        }
        
        .gif-container img:nth-child(2) {
            max-width: 40%;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 15px 0;
        }
        
        .badge {
            background-color: #161b22;
            padding: 5px 10px;
            border-radius: 20px;
            border: 1px solid #30363d;
            display: flex;
            align-items: center;
            font-size: 14px;
        }
        
        .badge img {
            height: 20px;
            margin-right: 5px;
        }
        
        .spotify-container {
            background: linear-gradient(to right, #1DB954, #191414);
            padding: 15px;
            border-radius: 10px;
            margin: 20px auto;
            max-width: 400px;
            display: flex;
            align-items: center;
            box-shadow: 0 0 10px rgba(29, 185, 84, 0.4);
        }
        
        .spotify-logo {
            font-size: 30px;
            color: #1DB954;
            background-color: #191414;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
        }
        
        .now-playing {
            flex-grow: 1;
        }
        
        .now-playing h4 {
            color: white;
            margin-bottom: 5px;
        }
        
        .now-playing p {
            font-size: 14px;
            color: #b3b3b3;
        }
        
        .tools-section {
            margin: 30px 0;
        }
        
        .tools-title {
            background-color: #161b22;
            padding: 10px 15px;
            border-radius: 5px;
            display: inline-block;
            margin-bottom: 15px;
            border: 1px solid #30363d;
            font-weight: 600;
            color: #58a6ff;
        }
        
        .tools-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .code-block {
            background-color: #161b22;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 20px;
            margin: 20px 0;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            color: #c9d1d9;
            position: relative;
            overflow-x: auto;
        }
        
        .code-block pre {
            margin: 0;
            padding: 0;
        }
        
        .code-keyword {
            color: #ff7b72;
        }
        
        .code-class {
            color: #d2a8ff;
        }
        
        .code-string {
            color: #a5d6ff;
        }
        
        .code-comment {
            color: #8b949e;
        }
        
        .info-section {
            margin: 20px 0;
            padding: 20px;
            background-color: #161b22;
            border-radius: 10px;
            border: 1px solid #30363d;
        }
        
        .info-section ul {
            padding-left: 20px;
        }
        
        .info-section li {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
        }
        
        .info-section li img {
            width: 20px;
            margin-right: 10px;
        }
        
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 20px 0;
        }
        
        .stats-card {
            background-color: #161b22;
            border: 1px solid #30363d;
            border-radius: 10px;
            overflow: hidden;
            flex: 1;
            min-width: 250px;
        }
        
        .stats-card img {
            width: 100%;
            display: block;
        }
        
        .code-cycle {
            text-align: center;
            margin: 40px 0;
        }
        
        .code-cycle h3 {
            margin-bottom: 20px;
            color: #58a6ff;
        }
        
        .emoji-container {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 20px;
        }
        
        .emoji-container img {
            width: 80px;
            animation: float 3s ease-in-out infinite;
        }
        
        .emoji-container img:nth-child(1) {
            animation-delay: 0s;
        }
        
        .emoji-container img:nth-child(2) {
            animation-delay: 0.5s;
        }
        
        .emoji-container img:nth-child(3) {
            animation-delay: 1s;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #8b949e;
            border-top: 1px solid #30363d;
            margin-top: 30px;
        }
        
        @media (max-width: 768px) {
            .gif-container img {
                max-width: 100%;
            }
            
            .stats-container {
                flex-direction: column;
            }
            
            .emoji-container {
                gap: 20px;
            }
            
            .emoji-container img {
                width: 60px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="gif-container">
                <img src="https://github.com/SP-XD/SP-XD/blob/main/images/hellocoders_rounded.gif?raw=true" alt="Hello Coders">
                <img src="https://github.com/SP-XD/SP-XD/blob/main/images/dev-working_rounded.gif?raw=true" alt="Workspace">
            </div>
            
            <div class="badges">
                <div class="badge">
                    <img src="https://visitor-badge.glitch.me/badge?page_id=SP-XD" alt="Profile views">
                </div>
                <div class="badge">
                    <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FSP-XD&count_bg=%2379C83D&title_bg=%23555555&icon=mediafire.svg&icon_color=%23E7E7E7&title=HITS&edge_flat=false" alt="Hits">
                </div>
                <div class="badge">
                    <i class="fab fa-telegram"></i> SP-XD
                </div>
            </div>
        </header>
        
        <div class="spotify-container">
            <div class="spotify-logo">
                <i class="fab fa-spotify"></i>
            </div>
            <div class="now-playing">
                <h4>Vibing to Music</h4>
                <p>Currently playing on Spotify</p>
            </div>
        </div>
        
        <div class="tools-section">
            <div class="tools-title">🛠 Tools I use :</div>
            <div class="tools-badges">
                <!-- Badges will be generated by JS -->
            </div>
            
            <div class="code-block">
                <pre>
<span class="code-comment">// tools_I_use organized</span>

<span class="code-keyword">class</span> <span class="code-class">About</span> <span class="code-keyword">extends</span> <span class="code-class">Me</span> { 
  <span class="code-keyword">const</span> myTools = {  
    <span class="code-string">"ProgramingLanguages"</span> : { <span class="code-string">"Dart"</span>, <span class="code-string">"Go"</span>, <span class="code-string">"Python"</span>, <span class="code-string">"Javascript"</span>, <span class="code-string">"Java"</span>, <span class="code-string">"c++"</span> },
    <span class="code-string">"OtherLanguages"</span> : { <span class="code-string">"HTML"</span>, <span class="code-string">"CSS"</span>, <span class="code-string">"Bash"</span>, <span class="code-string">"Json"</span>, <span class="code-string">"Markdown"</span> },
    <span class="code-string">"Database"</span> : { <span class="code-string">"Firebase"</span>, <span class="code-string">"Sqlite"</span> },
    <span class="code-string">"Editors"</span> : { <span class="code-string">"Vscode"</span>, <span class="code-string">"Xcode"</span>, <span class="code-string">"Sublime"</span>, <span class="code-string">"Neovim"</span> },
    <span class="code-string">"Platforms"</span> : { <span class="code-string">"Mac"</span>, <span class="code-string">"GNU/Linux"</span>, <span class="code-string">"Windows"</span> },
    <span class="code-string">"OtherTools"</span> : { <span class="code-string">"Git"</span>, <span class="code-string">"Figma"</span>, <span class="code-string">"Photoshop"</span>, <span class="code-string">"Gimp"</span>, <span class="code-string">"Lightroom"</span> }
  };
}
                </pre>
            </div>
        </div>
        
        <div class="info-section">
            <ul>
                <li>
                    <img src="https://github.com/SP-XD/SP-XD/blob/main/images/Developer.gif?raw=true" alt="Developer">
                    I'm currently learning <strong>Flutter & WebDev</strong>
                </li>
                <li>
                    <img src="https://github.com/SP-XD/SP-XD/blob/main/images/hyperkitty.gif?raw=true" alt="Linux">
                    I like exploring <strong>GNU/Linux</strong>
                </li>
                <li>
                    <img src="https://github.com/SP-XD/SP-XD/blob/main/images/message.gif?raw=true" alt="Message">
                    Ask me about <strong>Pc building, Movies, or anything</strong>
                </li>
                <li>
                    <img src="https://github.com/SP-XD/SP-XD/blob/main/images/letterbox.gif?raw=true" alt="Telegram">
                    Find me on Telegram: <strong><a href="https://t.me/spxd007" style="color: #58a6ff; text-decoration: none;">丂𝙋⚡乂𝘿</a></strong>
                </li>
                <li>
                    <img src="https://github.com/SP-XD/SP-XD/blob/main/images/lightning.gif?raw=true" alt="Fun fact">
                    Fun fact: Banging your head against a wall for one hour burns <strong>150 calories</strong>
                </li>
            </ul>
        </div>
        
        <div class="stats-container">
            <div class="stats-card">
                <img src="https://raw.githubusercontent.com/SP-XD/profile-summary-cards/master/profile-summary-card-output/nord_dark/3-stats.svg" alt="GitHub Stats">
            </div>
            <div class="stats-card">
                <img src="https://raw.githubusercontent.com/SP-XD/profile-summary-cards/master/profile-summary-card-output/nord_dark/1-repos-per-language.svg" alt="Repos per Language">
            </div>
            <div class="stats-card">
                <img src="https://raw.githubusercontent.com/SP-XD/profile-summary-cards/master/profile-summary-card-output/nord_dark/2-most-commit-language.svg" alt="Most Commit Language">
            </div>
        </div>
        
        <div class="code-cycle">
            <h3>Code Cycle</h3>
            <div class="emoji-container">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Face%20with%20Spiral%20Eyes.png" alt="Broken system!">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Relieved%20Face.png" alt="It's working!">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Smilies/Astonished%20Face.png" alt="It's working but you don't know how!">
            </div>
        </div>
        
        <footer>
            <p>Made with ❤️ | GitHub Profile Recreation</p>
        </footer>
    </div>
    
    <script>
        // Tools badges data
        const tools = [
            { name: "Go", color: "#00ADD8", icon: "go" },
            { name: "Flutter", color: "#02569B", icon: "flutter" },
            { name: "React Native", color: "#61DAFB", icon: "react" },
            { name: "Java", color: "#ED8B00", icon: "java" },
            { name: "Dart", color: "#0175C2", icon: "dart" },
            { name: "C++", color: "#00599C", icon: "cplusplus" },
            { name: "C", color: "#00599C", icon: "c" },
            { name: "Python", color: "#FFD43B", icon: "python" },
            { name: "Javascript", color: "#F7DF1E", icon: "javascript" },
            { name: "Json", color: "#5E5C5C", icon: "json" },
            { name: "Html", color: "#E34F26", icon: "html5" },
            { name: "Css", color: "#1572B6", icon: "css3" },
            { name: "Bash", color: "#4EAA25", icon: "gnubash" },
            { name: "Markdown", color: "#000000", icon: "markdown" },
            { name: "GNU/Linux", color: "#FCC624", icon: "linux" },
            { name: "Vscode", color: "#0078D4", icon: "visualstudiocode" },
            { name: "Sublime Text", color: "#FF9800", icon: "sublimetext" },
            { name: "Neovim", color: "#57A143", icon: "neovim" },
            { name: "Firebase", color: "#FFCA28", icon: "firebase" },
            { name: "Sqlite", color: "#003B57", icon: "sqlite" },
            { name: "Git", color: "#F05032", icon: "git" },
            { name: "Photoshop", color: "#31A8FF", icon: "adobephotoshop" },
            { name: "Lightroom", color: "#31A8FF", icon: "adobelightroom" },
            { name: "Gimp", color: "#5C5543", icon: "gimp" },
            { name: "Figma", color: "#F24E1E", icon: "figma" },
            { name: "Heroku", color: "#430098", icon: "heroku" },
            { name: "Chakra-UI", color: "#319795", icon: "chakraui" }
        ];
        
        // Generate tool badges
        const toolsContainer = document.querySelector('.tools-badges');
        
        tools.forEach(tool => {
            const badge = document.createElement('div');
            badge.className = 'badge';
            badge.style.backgroundColor = `${tool.color}33`; // Add opacity
            badge.style.border = `1px solid ${tool.color}`;
            badge.innerHTML = `<i class="fab fa-${tool.icon}"></i> ${tool.name}`;
            toolsContainer.appendChild(badge);
        });
        
        // Simple animation for stats cards
        const statsCards = document.querySelectorAll('.stats-card');
        statsCards.forEach((card, index) => {
            card.style.transition = 'transform 0.3s ease';
            card.addEventListener('mouseenter', () => {
                card.style.transform = 'translateY(-5px)';
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0)';
            });
        });
    </script>
</body>
</html>
