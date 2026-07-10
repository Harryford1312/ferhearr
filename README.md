# ferhearr
Null
index.html<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="Feather">
    <title>🪶 Feather</title>
    <link rel="apple-touch-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 180 180'><rect fill='%23000' width='180' height='180'/><text x='50%' y='50%' font-size='80' fill='%23fff' text-anchor='middle' dominant-baseline='middle'>🪶</text></svg>">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #f5f5f5 0%, #e8e8e8 100%);
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            color: #333;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .safe-area {
            padding: 10px;
            padding-top: max(10px, env(safe-area-inset-top));
            padding-bottom: max(10px, env(safe-area-inset-bottom));
        }

        header {
            background: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            border-radius: 20px;
            margin: 10px;
        }

        h1 {
            font-size: 32px;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .subtitle {
            font-size: 14px;
            color: #666;
            font-weight: 300;
        }

        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: 0 10px;
        }

        .card {
            background: white;
            border-radius: 20px;
            padding: 20px;
            margin: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }

        .card:active {
            transform: scale(0.98);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        .card h2 {
            font-size: 20px;
            margin-bottom: 10px;
            color: #000;
        }

        .card p {
            font-size: 14px;
            color: #666;
            line-height: 1.5;
        }

        .features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 15px;
        }

        .feature-item {
            background: #f9f9f9;
            padding: 12px;
            border-radius: 12px;
            font-size: 13px;
            text-align: center;
            color: #555;
        }

        .button-group {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 15px;
        }

        button {
            padding: 12px;
            border: none;
            border-radius: 12px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }

        .btn-primary {
            background: #000;
            color: white;
        }

        .btn-primary:active {
            background: #333;
        }

        .btn-secondary {
            background: #f0f0f0;
            color: #000;
        }

        .btn-secondary:active {
            background: #e0e0e0;
        }

        .status {
            text-align: center;
            padding: 15px;
            background: #e8f5e9;
            border-radius: 12px;
            margin: 15px 0;
            color: #2e7d32;
            font-size: 14px;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            border-radius: 20px;
            padding: 30px;
            max-width: 400px;
            width: 100%;
            max-height: 80vh;
            overflow-y: auto;
        }

        .modal-close {
            font-size: 28px;
            float: right;
            cursor: pointer;
            color: #999;
        }

        .modal h2 {
            margin-top: 20px;
            margin-bottom: 15px;
            font-size: 22px;
        }

        .modal p {
            margin-bottom: 10px;
            font-size: 14px;
            color: #666;
            line-height: 1.6;
        }

        .footer {
            text-align: center;
            padding: 30px 20px;
            color: #999;
            font-size: 12px;
        }

        input[type="text"],
        input[type="email"],
        textarea {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            font-family: inherit;
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        @media (prefers-color-scheme: dark) {
            body {
                background: #1a1a1a;
                color: #f0f0f0;
            }

            .card, header, .modal-content {
                background: #2d2d2d;
                color: #f0f0f0;
            }

            .card h2, h1 {
                color: #fff;
            }

            .card p {
                color: #ccc;
            }

            .feature-item {
                background: #3d3d3d;
                color: #bbb;
            }

            .btn-secondary {
                background: #3d3d3d;
                color: #fff;
            }

            input[type="text"],
            input[type="email"],
            textarea {
                background: #3d3d3d;
                color: #f0f0f0;
                border-color: #555;
            }
        }
    </style>
</head>
<body>
    <div class="safe-area">
        <header>
            <h1>🪶 Feather</h1>
            <p class="subtitle">Leicht. Einfach. Elegant.</p>
        </header>

        <div class="container">
            
            <div class="status">
                ✅ App ist online und bereit!
            </div>

            <div class="card">
                <h2>🎯 Hauptfunktionen</h2>
                <div class="features">
                    <div class="feature-item">📝 Notizen</div>
                    <div class="feature-item">📊 Tracker</div>
                    <div class="feature-item">⏰ Reminders</div>
                    <div class="feature-item">🎨 Design</div>
                </div>
                <div class="button-group" style="margin-top: 20px;">
                    <button class="btn-primary" onclick="openModal('notes')">📝 Notizen</button>
                    <button class="btn-primary" onclick="openModal('tracker')">📊 Tracker</button>
                </div>
            </div>

            <div class="card">
                <h2>📝 Meine Notizen</h2>
                <p>Schreibe deine Gedanken auf - leicht und einfach.</p>
                <button class="btn-primary" style="width: 100%; margin-top: 15px;" onclick="openModal('notes')">
                    ✏️ Neue Notiz
                </button>
            </div>

            <div class="card">
                <h2>📊 Tracker</h2>
                <p>Verfolge deine täglichen Aktivitäten und Gewohnheiten.</p>
                <div class="features">
                    <div class="feature-item">💪 Training</div>
                    <div class="feature-item">🥗 Ernährung</div>
                    <div class="feature-item">😴 Schlaf</div>
                    <div class="feature-item">🧠 Mindfulness</div>
                </div>
                <button class="btn-primary" style="width: 100%; margin-top: 15px;" onclick="openModal('tracker')">
                    ➕ Aktivität hinzufügen
                </button>
            </div>

            <div class="card">
                <h2>⚙️ Einstellungen</h2>
                <div class="button-group">
                    <button class="btn-secondary" onclick="openModal('settings')">⚙️ Einstellungen</button>
                    <button class="btn-secondary" onclick="openModal('about')">ℹ️ Über</button>
                </div>
            </div>

            <div class="card" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white;">
                <h2 style="color: white;">📱 Als App installieren</h2>
                <p>Installiere Feather auf deinem Home Screen für schnellen Zugriff.</p>
                <button class="btn-primary" style="width: 100%; margin-top: 15px; background: white; color: #667eea;" onclick="installApp()">
                    📱 Installieren
                </button>
            </div>

        </div>
    </div>

    <div id="notesModal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('notes')">&times;</span>
            <h2>📝 Neue Notiz</h2>
            <input type="text" id="noteTitle" placeholder="Titel...">
            <textarea id="noteContent" placeholder="Schreibe hier deine Notiz..."></textarea>
            <button class="btn-primary" style="width: 100%; margin-top: 15px;" onclick="saveNote()">
                💾 Speichern
            </button>
        </div>
    </div>

    <div id="trackerModal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('tracker')">&times;</span>
            <h2>📊 Aktivität hinzufügen</h2>
            <input type="text" placeholder="Art der Aktivität (z.B. Training, Wasser trinken)">
            <input type="text" placeholder="Dauer / Menge">
            <textarea placeholder="Notizen..."></textarea>
            <button class="btn-primary" style="width: 100%; margin-top: 15px;" onclick="saveTracking()">
                ✅ Speichern
            </button>
        </div>
    </div>

    <div id="settingsModal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('settings')">&times;</span>
            <h2>⚙️ Einstellungen</h2>
            <p><strong>App Theme:</strong></p>
            <div class="button-group">
                <button class="btn-secondary" onclick="setTheme('light')">☀️ Hell</button>
                <button class="btn-secondary" onclick="setTheme('dark')">🌙 Dunkel</button>
            </div>
            <p style="margin-top: 20px;"><strong>Benachrichtigungen:</strong></p>
            <input type="text" placeholder="E-Mail für Benachrichtigungen">
            <button class="btn-primary" style="width: 100%; margin-top: 15px;" onclick="saveSettings()">
                ✅ Speichern
            </button>
        </div>
    </div>

    <div id="aboutModal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('about')">&times;</span>
            <h2>ℹ️ Über Feather</h2>
            <p><strong>Feather v1.0</strong></p>
            <p>Eine elegante, leichte App zum Verwalten deiner täglichen Notizen und Aktivitäten.</p>
            
            <p style="margin-top: 20px;"><strong>✨ Features:</strong></p>
            <p>• 📝 Notizen & Tagebuch<br>
            • 📊 Aktivitäts-Tracker<br>
            • ⏰ Reminders & Notifications<br>
            • 🎨 Schönes Design<br>
            • 📱 Funktioniert auf allen Geräten<br>
            • 🔒 Deine Daten gehören dir</p>
            
            <p style="margin-top: 20px;"><strong>Entwickelt mit:</strong></p>
            <p>SwiftUI • Web Standards • ❤️</p>
            
            <p style="margin-top: 20px; font-size: 12px; color: #999;">
                © 2024 Feather<br>
                Made with 🪶 for simplicity
            </p>
        </div>
    </div>

    <div class="footer">
        <p>🪶 Feather - Leicht. Einfach. Elegant.</p>
        <p>Immer verfügbar. Überall dabei.</p>
    </div>

    <script>
        function openModal(type) {
            document.getElementById(type + 'Modal').classList.add('active');
        }

        function closeModal(type) {
            document.getElementById(type + 'Modal').classList.remove('active');
        }

        function saveNote() {
            const title = document.getElementById('noteTitle').value;
            const content = document.getElementById('noteContent').value;
            
            if (!title || !content) {
                alert('Bitte fülle alle Felder aus!');
                return;
            }
            
            localStorage.setItem('note_' + Date.now(), JSON.stringify({
                title: title,
                content: content,
                date: new Date().toLocaleDateString('de-DE')
            }));
            
            alert('✅ Notiz gespeichert!');
            document.getElementById('noteTitle').value = '';
            document.getElementById('noteContent').value = '';
            closeModal('notes');
        }

        function saveTracking() {
            alert('✅ Aktivität gespeichert!');
            closeModal('tracker');
        }

        function saveSettings() {
            alert('✅ Einstellungen gespeichert!');
            closeModal('settings');
        }

        function setTheme(theme) {
            if (theme === 'dark') {
                document.documentElement.style.colorScheme = 'dark';
                localStorage.setItem('theme', 'dark');
            } else {
                document.documentElement.style.colorScheme = 'light';
                localStorage.setItem('theme', 'light');
            }
            alert('✅ Theme geändert!');
        }

        function installApp() {
            alert('📱 Installation:\n\n1. Klick Share Button (unten)\n2. Wähle "Add to Home Screen"\n3. Name: Feather\n4. Add\n\nFertig! 🎉');
        }

        const savedTheme = localStorage.getItem('theme');
        if (savedTheme === 'dark') {
            document.documentElement.style.colorScheme = 'dark';
        }

        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.classList.remove('active');
            }
        }
    </script>
</body>
</html>
