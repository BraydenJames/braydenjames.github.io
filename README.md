<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Weave</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Montserrat:wght@400;500;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #121214;
            --surface-color: rgba(26, 26, 30, 0.75);
            --border-color: rgba(255, 255, 255, 0.08);
            --text-primary: #F1F5F9;
            --text-secondary: #94A3B8;
            --primary-cyan: #00E5FF;
            --primary-blue: #3B82F6;
            --primary-teal: #13EFB2;
            --primary-orange: #FF9F1C;
            --gradient-cool: linear-gradient(135deg, var(--primary-cyan), var(--primary-blue));
            --gradient-spectrum: linear-gradient(90deg, var(--primary-cyan), var(--primary-teal), var(--primary-orange));
            --font-display: 'Montserrat', sans-serif;
            --font-body: 'Inter', sans-serif;
        }

        .light-theme {
            --bg-color: #F8FAFC;
            --surface-color: rgba(255, 255, 255, 0.85);
            --border-color: rgba(15, 23, 42, 0.08);
            --text-primary: #0F172A;
            --text-secondary: #475569;
            --primary-cyan: #0284C7;
            --primary-blue: #1D4ED8;
            --primary-teal: #0D9488;
            --primary-orange: #C2410C;
            --gradient-cool: linear-gradient(135deg, var(--primary-cyan), var(--primary-blue));
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: var(--font-body);
            line-height: 1.6;
            overflow-x: hidden;
            transition: background-color 0.4s ease, color 0.4s ease;
        }

        /* Animated Ambient Background Glows */
        .ambient-glow {
            position: fixed;
            width: 50vw;
            height: 50vw;
            border-radius: 50%;
            filter: blur(140px);
            opacity: 0.12;
            z-index: -1;
            pointer-events: none;
            transition: opacity 0.5s ease;
        }

        .glow-1 {
            top: -10vw;
            left: -10vw;
            background: radial-gradient(circle, var(--primary-cyan) 0%, transparent 80%);
            animation: float-slow 20s infinite alternate;
        }

        .glow-2 {
            bottom: -10vw;
            right: -10vw;
            background: radial-gradient(circle, var(--primary-orange) 0%, transparent 80%);
            animation: float-slow 25s infinite alternate-reverse;
        }

        @keyframes float-slow {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(5vw, 5vw) scale(1.1); }
        }

        /* Layout Container */
        .page-wrapper {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 24px;
            display: flex;
            flex-direction: column;
            gap: 40px;
        }

        /* Header Styling */
        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 24px;
            backdrop-filter: blur(10px);
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .app-logo {
            width: 48px;
            height: 48px;
            border-radius: 12px;
            background: var(--gradient-cool);
            padding: 2px;
            box-shadow: 0 4px 20px rgba(0, 229, 255, 0.25);
        }

        .app-logo-inner {
            width: 100%;
            height: 100%;
            border-radius: 10px;
            background-color: #121214;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-display);
            font-weight: 800;
            font-size: 20px;
            color: var(--primary-cyan);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .title-group h1 {
            font-family: var(--font-display);
            font-weight: 700;
            font-size: 26px;
            letter-spacing: -0.5px;
            background: var(--gradient-cool);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .title-group p {
            font-size: 14px;
            color: var(--text-secondary);
            font-weight: 500;
        }

        .header-controls {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        button.btn-ctrl {
            background-color: var(--surface-color);
            border: 1px solid var(--border-color);
            color: var(--text-primary);
            padding: 10px 16px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 500;
            font-family: var(--font-body);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        button.btn-ctrl:hover {
            border-color: var(--primary-cyan);
            box-shadow: 0 0 10px rgba(0, 229, 255, 0.15);
            transform: translateY(-1px);
        }

        /* Search Bar */
        .search-container {
            position: relative;
            width: 100%;
        }

        .search-input {
            width: 100%;
            background-color: var(--surface-color);
            border: 1px solid var(--border-color);
            color: var(--text-primary);
            padding: 14px 20px 14px 50px;
            border-radius: 14px;
            font-size: 16px;
            font-family: var(--font-body);
            transition: all 0.3s ease;
            backdrop-filter: blur(12px);
        }

        .search-input:focus {
            outline: none;
            border-color: var(--primary-cyan);
            box-shadow: 0 0 15px rgba(0, 229, 255, 0.1);
        }

        .search-icon {
            position: absolute;
            left: 18px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-secondary);
            font-size: 18px;
            pointer-events: none;
        }

        /* Two Column Body Layout */
        .main-content {
            display: grid;
            grid-template-columns: 280px 1fr;
            gap: 40px;
            align-items: start;
        }

        /* Navigation Sidebar */
        .sidebar {
            position: sticky;
            top: 40px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            padding: 24px;
            background-color: var(--surface-color);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            backdrop-filter: blur(12px);
        }

        .sidebar h2 {
            font-family: var(--font-display);
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: var(--text-secondary);
            margin-bottom: 8px;
        }

        .sidebar-menu {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .sidebar-link {
            display: block;
            padding: 10px 14px;
            border-radius: 10px;
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 14px;
            font-weight: 500;
            transition: all 0.3s ease;
            border-left: 2px solid transparent;
        }

        .sidebar-link:hover, .sidebar-link.active {
            color: var(--text-primary);
            background-color: rgba(0, 229, 255, 0.05);
            border-left-color: var(--primary-cyan);
            padding-left: 18px;
        }

        /* Document Styling */
        .doc-body {
            display: flex;
            flex-direction: column;
            gap: 32px;
        }

        .doc-section {
            background-color: var(--surface-color);
            border: 1px solid var(--border-color);
            border-radius: 24px;
            padding: 32px;
            backdrop-filter: blur(12px);
            transition: opacity 0.3s ease, transform 0.3s ease, border-color 0.3s ease;
        }

        .doc-section.highlighted-section {
            border-color: var(--primary-cyan);
            box-shadow: 0 0 20px rgba(0, 229, 255, 0.08);
        }

        .doc-section h2 {
            font-family: var(--font-display);
            font-size: 22px;
            font-weight: 700;
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 12px;
            color: var(--text-primary);
        }

        .section-icon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            border-radius: 8px;
            background-color: rgba(0, 229, 255, 0.1);
            color: var(--primary-cyan);
            font-size: 18px;
            font-weight: bold;
        }

        .doc-section p {
            color: var(--text-secondary);
            font-size: 15px;
            margin-bottom: 16px;
        }

        .doc-section ul {
            list-style: none;
            margin-bottom: 16px;
            padding-left: 8px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .doc-section li {
            position: relative;
            color: var(--text-secondary);
            font-size: 15px;
            padding-left: 24px;
        }

        .doc-section li::before {
            content: "✦";
            position: absolute;
            left: 0;
            color: var(--primary-cyan);
            font-size: 14px;
        }

        /* Quick facts banner styling */
        .infobox-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 16px;
            margin: 16px 0;
        }

        .infobox {
            background-color: rgba(255, 255, 255, 0.02);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .infobox h3 {
            font-family: var(--font-display);
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--text-primary);
        }

        .infobox p {
            margin: 0;
            font-size: 13.5px;
        }

        .infobox.accent-cyan { border-left: 4px solid var(--primary-cyan); }
        .infobox.accent-teal { border-left: 4px solid var(--primary-teal); }
        .infobox.accent-orange { border-left: 4px solid var(--primary-orange); }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-color);
            padding-top: 24px;
            margin-top: 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            color: var(--text-secondary);
            font-size: 13.5px;
        }

        footer a {
            color: var(--primary-cyan);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: var(--text-primary);
        }

        /* Print Override */
        @media print {
            body {
                background: white !important;
                color: black !important;
            }
            .ambient-glow, .sidebar, .header-controls, .search-container, footer {
                display: none !important;
            }
            .main-content {
                grid-template-columns: 1fr !important;
            }
            .doc-section {
                border: none !important;
                background: transparent !important;
                padding: 0 0 40px 0 !important;
                page-break-inside: avoid;
            }
            .doc-section h2 {
                color: black !important;
            }
            .doc-section p, .doc-section li {
                color: #333 !important;
            }
            .infobox {
                border: 1px solid #ccc !important;
                background: transparent !important;
            }
        }

        /* Responsiveness */
        @media (max-width: 900px) {
            .main-content {
                grid-template-columns: 1fr;
            }
            .sidebar {
                position: relative;
                top: 0;
            }
            header {
                flex-direction: column;
                align-items: flex-start;
                gap: 16px;
            }
            .header-controls {
                width: 100%;
                justify-content: space-between;
            }
        }
    </style>
</head>
<body>

    <!-- Ambient Gradient Background Elements -->
    <div class="ambient-glow glow-1" id="glow1"></div>
    <div class="ambient-glow glow-2" id="glow2"></div>

    <div class="page-wrapper">
        <header>
            <div class="logo-section">
                <div class="app-logo">
                    <div class="app-logo-inner">W</div>
                </div>
                <div class="title-group">
                    <h1>WEAVE PRIVACY POLICY</h1>
                    <p>Last updated: June 13, 2026</p>
                </div>
            </div>
            <div class="header-controls">
                <button class="btn-ctrl" onclick="toggleTheme()" id="themeBtn">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="5"/><path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"/></svg>
                    Theme Mode
                </button>
                <button class="btn-ctrl" onclick="window.print()">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M6 9V2h12v7M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"/><path d="M6 14h12v8H6z"/></svg>
                    Print PDF
                </button>
            </div>
        </header>

        <!-- Dynamic Filter Search -->
        <div class="search-container">
            <span class="search-icon">🔍</span>
            <input type="text" class="search-input" id="searchBar" placeholder="Search privacy topics (e.g. data security, Gemini Nano, prompts)..." onkeyup="filterSections()">
        </div>

        <div class="main-content">
            <!-- Table of Contents Menu -->
            <aside class="sidebar">
                <h2>Navigation</h2>
                <ul class="sidebar-menu">
                    <li><a href="#overview" class="sidebar-link active" onclick="activateLink(this)">Overview</a></li>
                    <li><a href="#no-personal-data" class="sidebar-link" onclick="activateLink(this)">Personal Information</a></li>
                    <li><a href="#prompts-storage" class="sidebar-link" onclick="activateLink(this)">AI Prompt Storage</a></li>
                    <li><a href="#on-device" class="sidebar-link" onclick="activateLink(this)">On-Device AI Privacy</a></li>
                    <li><a href="#google-play" class="sidebar-link" onclick="activateLink(this)">Google Play Telemetry</a></li>
                    <li><a href="#sharing" class="sidebar-link" onclick="activateLink(this)">Data Third-Parties</a></li>
                    <li><a href="#security" class="sidebar-link" onclick="activateLink(this)">Data Security</a></li>
                    <li><a href="#contact" class="sidebar-link" onclick="activateLink(this)">Contact &amp; Rights</a></li>
                </ul>
            </aside>

            <!-- Main Policy Document Body -->
            <div class="doc-body" id="policyBody">
                
                <!-- Overview Section -->
                <section class="doc-section" id="overview">
                    <h2><span class="section-icon">1</span>Overview</h2>
                    <p>Welcome to <strong>Weave</strong> (the "App"), an interactive word-blank generator powered by artificial intelligence. We respect your privacy and are committed to maintaining a secure, transparent environment. This policy outlines exactly how data is processed when you build templates and stitch stories together using our App.</p>
                    <p>We believe in <strong>data minimization</strong>. We only process data that is technically necessary to run the AI engine or automatically captured by publishing platforms to ensure app stability.</p>
                    <div class="infobox-grid">
                        <div class="infobox accent-cyan">
                            <h3>No Accounts</h3>
                            <p>Weave requires no registrations, user profiles, or logins. Your identity remains anonymous to us.</p>
                        </div>
                        <div class="infobox accent-teal">
                            <h3>Local Processing</h3>
                            <p>On compatible devices, stories can be generated 100% locally on-device using Gemini Nano.</p>
                        </div>
                        <div class="infobox accent-orange">
                            <h3>No Hidden Tracking</h3>
                            <p>We do not track your location, read contacts, or embed covert advertising sdk trackers.</p>
                        </div>
                    </div>
                </section>

                <!-- Personal Information Section -->
                <section class="doc-section" id="no-personal-data">
                    <h2><span class="section-icon">2</span>Personal Information</h2>
                    <p>Weave does not collect, harvest, or request any personal identifiers. When you download and play Weave:</p>
                    <ul>
                        <li>We do not collect names, email addresses, phone numbers, or account details.</li>
                        <li>We do not access your device's camera, microphone, contact lists, photos, or physical location.</li>
                        <li>No profiling or behavioral marketing identifiers are established.</li>
                    </ul>
                </section>

                <!-- Prompts Storage Section -->
                <section class="doc-section" id="prompts-storage">
                    <h2><span class="section-icon">3</span>AI Prompt Storage</h2>
                    <p>When using our Cloud Generation mode (powered by Firebase Vertex AI), Weave processes the subject and tone parameters you select to create the customized story template.</p>
                    <p><strong>What is stored on the Cloud:</strong></p>
                    <ul>
                        <li><strong>The AI Prompt payload:</strong> The theme sentence and tone choice (e.g. <em>"A clumsy zombie cook-off in space"</em> under a <em>"Goofy"</em> tone) are transmitted to and processed by our cloud models to construct the JSON story structure.</li>
                        <li><strong>System logs:</strong> Anonymous, high-level prompt payloads may be logged temporarily to monitor quality, assess response parsing errors, and prevent service abuse.</li>
                    </ul>
                    <p>We do not associate these prompts with any user identity, as we have no user databases or registration systems.</p>
                </section>

                <!-- On-Device AI Privacy Section -->
                <section class="doc-section" id="on-device">
                    <h2><span class="section-icon">4</span>On-Device AI Privacy (Gemini Nano)</h2>
                    <p>If you toggle on <strong>Offline Mode (Gemini Nano)</strong>, the App routes prompt calculations locally on your physical device using Android's system-level <strong>AICore</strong> services.</p>
                    <ul>
                        <li>Your prompt parameters (theme text and tone selection) do not leave your device.</li>
                        <li>All story rendering and blank-filling occurs 100% locally in secure sandbox device memory.</li>
                        <li>Google Play Services manages the background installation of the Gemini Nano model file via Private Compute Services, keeping calculations localized.</li>
                    </ul>
                </section>

                <!-- Google Play Telemetry Section -->
                <section class="doc-section" id="google-play">
                    <h2><span class="section-icon">5</span>Google Play Console Telemetry</h2>
                    <p>Weave uses standard, platform-level telemetry provided automatically by the Google Play Store console when distributing the application.</p>
                    <p><strong>What Google Play Console tracks automatically:</strong></p>
                    <ul>
                        <li><strong>Stability logs:</strong> Application Not Responding (ANR) occurrences and crash dump logs to help us trace code bugs.</li>
                        <li><strong>Performance metrics:</strong> Device hardware profiles, screen sizes, operating system versions, and aggregated country locations.</li>
                        <li><strong>Usage counts:</strong> Installation counts, active daily counts, and uninstall metrics.</li>
                    </ul>
                    <p>All telemetry data is aggregated, anonymized, and processed in accordance with the Google Play Developer Distribution Agreement.</p>
                </section>

                <!-- Sharing Section -->
                <section class="doc-section" id="sharing">
                    <h2><span class="section-icon">6</span>Data Sharing with Third-Parties</h2>
                    <p>We do not sell, rent, trade, or distribute your data. Prompt data is sent exclusively to the cloud infrastructure services required to generate stories:</p>
                    <ul>
                        <li><strong>Firebase / Google Cloud Platform (GCP):</strong> Hosts the cloud-based generative AI systems used when Cloud Mode is selected. Data transmission is encrypted and processed according to Google Cloud privacy standards.</li>
                        <li><strong>Google Android OS / AICore:</strong> Manages localized processing resources on-device.</li>
                    </ul>
                </section>

                <!-- Security Section -->
                <section class="doc-section" id="security">
                    <h2><span class="section-icon">7</span>Data Security</h2>
                    <p>All communication between the App and the cloud servers (when using online generation modes) is secured using standard **HTTPS/TLS encryption** protocols. This ensures your prompt entries cannot be intercepted by third-parties during transit.</p>
                </section>

                <!-- Contact Section -->
                <section class="doc-section" id="contact">
                    <h2><span class="section-icon">8</span>Contact &amp; Your Rights</h2>
                    <p>Since we do not compile user accounts, profile indices, or personal identifiers, we hold no records capable of identifying individual users. Consequently, we cannot search for, modify, or delete specific user data upon request, as no such records exist.</p>
                    <p>For any questions regarding our data policies or app configurations, you can contact the developer team at:</p>
                    <ul>
                        <li><strong>Email:</strong> brayden.reesor@gmail.com</li>
                    </ul>
                </section>

            </div>
        </div>

        <footer>
            <p>&copy; 2026 Weave. All rights reserved.</p>
        </footer>
    </div>

    <script>
        // Smooth theme toggling
        function toggleTheme() {
            document.body.classList.toggle('light-theme');
            const isLight = document.body.classList.contains('light-theme');
            const themeBtn = document.getElementById('themeBtn');
            
            if (isLight) {
                themeBtn.innerHTML = `
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
                    Dark Theme
                `;
            } else {
                themeBtn.innerHTML = `
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="5"/><path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"/></svg>
                    Theme Mode
                `;
            }
        }

        // Active state navigation scrolling
        function activateLink(element) {
            const links = document.querySelectorAll('.sidebar-link');
            links.forEach(l => l.classList.remove('active'));
            element.classList.add('active');
        }

        // Section filter search logic
        function filterSections() {
            const query = document.getElementById('searchBar').value.toLowerCase().trim();
            const sections = document.querySelectorAll('.doc-section');
            const sidebarLinks = document.querySelectorAll('.sidebar-link');

            sections.forEach(section => {
                const text = section.innerText.toLowerCase();
                const targetId = section.getAttribute('id');
                const matchingLink = Array.from(sidebarLinks).find(l => l.getAttribute('href') === `#${targetId}`);

                if (text.includes(query)) {
                    section.style.display = 'block';
                    section.style.opacity = '1';
                    section.style.transform = 'translateY(0)';
                    if (matchingLink) matchingLink.style.display = 'block';
                    
                    // Highlight matching search section border temporarily if query is active
                    if (query.length > 2) {
                        section.classList.add('highlighted-section');
                    } else {
                        section.classList.remove('highlighted-section');
                    }
                } else {
                    section.style.opacity = '0';
                    section.style.transform = 'translateY(20px)';
                    setTimeout(() => {
                        if (!text.includes(query)) {
                            section.style.display = 'none';
                        }
                    }, 200);
                    if (matchingLink) matchingLink.style.display = 'none';
                }
            });
        }

        // Scrollspy to set active link based on viewport scroll offset
        window.addEventListener('scroll', () => {
            const sections = document.querySelectorAll('.doc-section');
            const scrollPos = window.scrollY || document.documentElement.scrollTop || document.body.scrollTop;
            const sidebarLinks = document.querySelectorAll('.sidebar-link');

            sections.forEach(section => {
                const top = section.offsetTop - 100;
                const bottom = top + section.offsetHeight;

                if (scrollPos >= top && scrollPos < bottom) {
                    const activeId = section.getAttribute('id');
                    sidebarLinks.forEach(link => {
                        if (link.getAttribute('href') === `#${activeId}`) {
                            link.classList.add('active');
                        } else {
                            link.classList.remove('active');
                        }
                    });
                }
            });
        });
    </script>
</body>
</html>
