# FocusFlow
FocusFlow
<!DOCTYPE html>

<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FocusFlow – Support</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0f0f13;
    --surface: #18181f;
    --border: #2a2a35;
    --purple: #a78bfa;
    --purple-dim: #7c3aed;
    --indigo: #818cf8;
    --text: #e8e8f0;
    --muted: #6b6b80;
    --accent: #c4b5fd;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-weight: 400;
    line-height: 1.7;
    min-height: 100vh;
  }

/* Noise texture overlay */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background-image: url(“data:image/svg+xml,%3Csvg viewBox=‘0 0 256 256’ xmlns=‘http://www.w3.org/2000/svg’%3E%3Cfilter id=‘noise’%3E%3CfeTurbulence type=‘fractalNoise’ baseFrequency=‘0.9’ numOctaves=‘4’ stitchTiles=‘stitch’/%3E%3C/filter%3E%3Crect width=‘100%25’ height=‘100%25’ filter=‘url(%23noise)’ opacity=‘0.03’/%3E%3C/svg%3E”);
pointer-events: none;
z-index: 0;
}

nav {
position: fixed;
top: 0; left: 0; right: 0;
z-index: 100;
padding: 20px 40px;
display: flex;
justify-content: space-between;
align-items: center;
background: rgba(15,15,19,0.8);
backdrop-filter: blur(20px);
border-bottom: 1px solid var(–border);
}
.nav-logo {
font-family: ‘DM Serif Display’, serif;
font-size: 1.4rem;
background: linear-gradient(135deg, var(–purple), var(–indigo));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
text-decoration: none;
}
.nav-links { display: flex; gap: 32px; }
.nav-links a {
color: var(–muted);
text-decoration: none;
font-size: 0.9rem;
font-weight: 500;
transition: color 0.2s;
letter-spacing: 0.02em;
}
.nav-links a:hover { color: var(–accent); }

main { position: relative; z-index: 1; }

/* Hero */
.hero {
min-height: 100vh;
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
text-align: center;
padding: 120px 40px 80px;
position: relative;
overflow: hidden;
}
.hero-glow {
position: absolute;
width: 600px;
height: 600px;
background: radial-gradient(circle, rgba(124,58,237,0.15) 0%, transparent 70%);
top: 50%; left: 50%;
transform: translate(-50%, -50%);
pointer-events: none;
}
.app-icon {
width: 96px;
height: 96px;
background: linear-gradient(135deg, #7c3aed, #4f46e5);
border-radius: 22px;
display: flex;
align-items: center;
justify-content: center;
margin: 0 auto 32px;
font-size: 2.5rem;
box-shadow: 0 20px 60px rgba(124,58,237,0.4);
animation: float 4s ease-in-out infinite;
}
@keyframes float {
0%, 100% { transform: translateY(0); }
50% { transform: translateY(-8px); }
}
.hero h1 {
font-family: ‘DM Serif Display’, serif;
font-size: clamp(2.5rem, 6vw, 4.5rem);
line-height: 1.1;
margin-bottom: 20px;
background: linear-gradient(135deg, #fff 0%, var(–accent) 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}
.hero p {
font-size: 1.15rem;
color: var(–muted);
max-width: 480px;
margin-bottom: 48px;
}
.btn {
display: inline-block;
padding: 14px 32px;
background: linear-gradient(135deg, var(–purple-dim), #4f46e5);
color: white;
text-decoration: none;
border-radius: 12px;
font-weight: 600;
font-size: 0.95rem;
transition: all 0.3s;
box-shadow: 0 8px 32px rgba(124,58,237,0.3);
}
.btn:hover {
transform: translateY(-2px);
box-shadow: 0 16px 40px rgba(124,58,237,0.4);
}

/* Sections */
section {
max-width: 900px;
margin: 0 auto;
padding: 80px 40px;
}
.section-label {
font-size: 0.75rem;
font-weight: 600;
letter-spacing: 0.12em;
text-transform: uppercase;
color: var(–purple);
margin-bottom: 12px;
}
h2 {
font-family: ‘DM Serif Display’, serif;
font-size: 2.2rem;
margin-bottom: 40px;
color: var(–text);
}

/* FAQ */
.faq-grid { display: grid; gap: 16px; }
.faq-item {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 16px;
padding: 24px 28px;
transition: border-color 0.2s;
}
.faq-item:hover { border-color: var(–purple); }
.faq-item h3 {
font-size: 1rem;
font-weight: 600;
margin-bottom: 8px;
color: var(–text);
}
.faq-item p { color: var(–muted); font-size: 0.95rem; }

/* Contact */
.contact-card {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 24px;
padding: 48px;
text-align: center;
position: relative;
overflow: hidden;
}
.contact-card::before {
content: ‘’;
position: absolute;
top: 0; left: 0; right: 0;
height: 2px;
background: linear-gradient(90deg, var(–purple-dim), var(–indigo));
}
.contact-card h3 {
font-family: ‘DM Serif Display’, serif;
font-size: 1.8rem;
margin-bottom: 12px;
}
.contact-card p { color: var(–muted); margin-bottom: 32px; }
.email-link {
display: inline-flex;
align-items: center;
gap: 10px;
padding: 16px 32px;
background: var(–bg);
border: 1px solid var(–border);
border-radius: 12px;
color: var(–accent);
text-decoration: none;
font-weight: 500;
transition: all 0.2s;
}
.email-link:hover {
border-color: var(–purple);
background: rgba(124,58,237,0.08);
}

/* Footer */
footer {
border-top: 1px solid var(–border);
padding: 40px;
text-align: center;
color: var(–muted);
font-size: 0.85rem;
}
footer a { color: var(–muted); text-decoration: none; margin: 0 16px; }
footer a:hover { color: var(–accent); }
.footer-links { margin-bottom: 16px; }

@media (max-width: 600px) {
nav { padding: 16px 20px; }
.nav-links { gap: 16px; }
section { padding: 60px 20px; }
.contact-card { padding: 32px 20px; }
}
</style>

</head>
<body>

<nav>
  <a href="index.html" class="nav-logo">FocusFlow</a>
  <div class="nav-links">
    <a href="#faq">FAQ</a>
    <a href="#contact">Support</a>
    <a href="privacy.html">Datenschutz</a>
    <a href="terms.html">AGB</a>
  </div>
</nav>

<main>
  <div class="hero">
    <div class="hero-glow"></div>
    <div class="app-icon">🎯</div>
    <h1>FocusFlow<br>Support</h1>
    <p>Wir helfen dir dabei, das Beste aus FocusFlow herauszuholen.</p>
    <a href="#contact" class="btn">Kontakt aufnehmen</a>
  </div>

  <section id="faq">
    <div class="section-label">Häufige Fragen</div>
    <h2>FAQ</h2>
    <div class="faq-grid">
      <div class="faq-item">
        <h3>Was ist FocusFlow Premium?</h3>
        <p>FocusFlow Premium schaltet alle erweiterten Funktionen frei – unbegrenzte Aufgaben, Habits, detaillierte Statistiken und mehr. Erhältlich als Monats- oder Jahresabo.</p>
      </div>
      <div class="faq-item">
        <h3>Wie kann ich mein Abo kündigen?</h3>
        <p>Du kannst dein Abo jederzeit über die iOS-Einstellungen kündigen: Einstellungen → Apple ID → Abonnements → FocusFlow.</p>
      </div>
      <div class="faq-item">
        <h3>Wie stelle ich meine Käufe wieder her?</h3>
        <p>Öffne FocusFlow → Profil → Käufe wiederherstellen. Melde dich dazu mit derselben Apple ID an, mit der du das Abo ursprünglich abgeschlossen hast.</p>
      </div>
      <div class="faq-item">
        <h3>Werden meine Daten in der Cloud gespeichert?</h3>
        <p>Deine Daten werden lokal auf deinem Gerät gespeichert. Es findet keine Übertragung auf externe Server statt.</p>
      </div>
      <div class="faq-item">
        <h3>Auf wie vielen Geräten kann ich FocusFlow nutzen?</h3>
        <p>FocusFlow kann auf allen deinen iOS-Geräten genutzt werden, die mit derselben Apple ID verknüpft sind.</p>
      </div>
      <div class="faq-item">
        <h3>Ich habe ein Problem – was tun?</h3>
        <p>Schreibe uns eine E-Mail an hello.aerohq@gmail.com. Wir antworten in der Regel innerhalb von 1–2 Werktagen.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="section-label">Kontakt</div>
    <h2>Wir sind für dich da</h2>
    <div class="contact-card">
      <h3>Support kontaktieren</h3>
      <p>Hast du ein Problem oder eine Frage? Schreib uns – wir helfen dir gerne weiter.</p>
      <a href="mailto:hello.aerohq@gmail.com" class="email-link">
        ✉️ hello.aerohq@gmail.com
      </a>
    </div>
  </section>
</main>

<footer>
  <div class="footer-links">
    <a href="privacy.html">Datenschutzrichtlinie</a>
    <a href="terms.html">Nutzungsbedingungen</a>
    <a href="#contact">Support</a>
  </div>
  <p>© 2025 Enzo Kaiser · FocusFlow</p>
</footer>

</body>
</html>
<!DOCTYPE html>

<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FocusFlow – Datenschutzrichtlinie</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0f0f13;
    --surface: #18181f;
    --border: #2a2a35;
    --purple: #a78bfa;
    --purple-dim: #7c3aed;
    --indigo: #818cf8;
    --text: #e8e8f0;
    --muted: #6b6b80;
    --accent: #c4b5fd;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-weight: 400;
    line-height: 1.8;
    min-height: 100vh;
  }
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(15,15,19,0.8);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'DM Serif Display', serif;
    font-size: 1.4rem;
    background: linear-gradient(135deg, var(--purple), var(--indigo));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-decoration: none;
  }
  .nav-links { display: flex; gap: 32px; }
  .nav-links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

.page-header {
padding: 140px 40px 60px;
max-width: 760px;
margin: 0 auto;
}
.section-label {
font-size: 0.75rem;
font-weight: 600;
letter-spacing: 0.12em;
text-transform: uppercase;
color: var(–purple);
margin-bottom: 12px;
}
.page-header h1 {
font-family: ‘DM Serif Display’, serif;
font-size: 3rem;
margin-bottom: 16px;
}
.page-header .meta {
color: var(–muted);
font-size: 0.9rem;
}

.content {
max-width: 760px;
margin: 0 auto;
padding: 0 40px 100px;
}
.content h2 {
font-family: ‘DM Serif Display’, serif;
font-size: 1.6rem;
margin: 48px 0 16px;
color: var(–text);
padding-bottom: 12px;
border-bottom: 1px solid var(–border);
}
.content h3 {
font-size: 1rem;
font-weight: 600;
margin: 24px 0 8px;
color: var(–accent);
}
.content p { color: #b0b0c0; margin-bottom: 16px; font-size: 0.95rem; }
.content ul {
list-style: none;
margin: 0 0 16px;
padding: 0;
}
.content ul li {
color: #b0b0c0;
font-size: 0.95rem;
padding: 6px 0 6px 20px;
position: relative;
}
.content ul li::before {
content: ‘–’;
position: absolute;
left: 0;
color: var(–purple);
}
.highlight-box {
background: var(–surface);
border: 1px solid var(–border);
border-left: 3px solid var(–purple);
border-radius: 0 12px 12px 0;
padding: 20px 24px;
margin: 24px 0;
}
.highlight-box p { color: var(–text); margin: 0; font-size: 0.95rem; }
a { color: var(–accent); text-decoration: none; }
a:hover { text-decoration: underline; }

footer {
border-top: 1px solid var(–border);
padding: 40px;
text-align: center;
color: var(–muted);
font-size: 0.85rem;
}
footer a { color: var(–muted); text-decoration: none; margin: 0 16px; }
footer a:hover { color: var(–accent); }
.footer-links { margin-bottom: 16px; }

@media (max-width: 600px) {
nav { padding: 16px 20px; }
.nav-links { gap: 16px; }
.page-header, .content { padding-left: 20px; padding-right: 20px; }
}
</style>

</head>
<body>

<nav>
  <a href="index.html" class="nav-logo">FocusFlow</a>
  <div class="nav-links">
    <a href="index.html">Support</a>
    <a href="privacy.html">Datenschutz</a>
    <a href="terms.html">AGB</a>
  </div>
</nav>

<div class="page-header">
  <div class="section-label">Rechtliches</div>
  <h1>Datenschutz&shy;richtlinie</h1>
  <p class="meta">Zuletzt aktualisiert: Januar 2025</p>
</div>

<div class="content">

  <div class="highlight-box">
    <p>Kurz zusammengefasst: FocusFlow speichert alle deine Daten ausschließlich lokal auf deinem Gerät. Es werden keine persönlichen Daten an externe Server übertragen oder Dritten weitergegeben.</p>
  </div>

  <h2>1. Verantwortlicher</h2>
  <p>Verantwortlich im Sinne der Datenschutz-Grundverordnung (DSGVO) ist:</p>
  <p>
    Enzo Kaiser<br>
    Deutschland<br>
    E-Mail: <a href="mailto:hello.aerohq@gmail.com">hello.aerohq@gmail.com</a>
  </p>

  <h2>2. Welche Daten werden verarbeitet?</h2>

  <h3>Lokal auf deinem Gerät gespeicherte Daten</h3>
  <p>FocusFlow speichert folgende Daten ausschließlich lokal auf deinem Gerät (UserDefaults / lokaler Speicher):</p>
  <ul>
    <li>Aufgaben, Beschreibungen, Prioritäten und Fälligkeitsdaten</li>
    <li>Gewohnheiten (Habits) und deren Erledigungshistorie</li>
    <li>Focus-Sessions und Zeiterfassungsdaten</li>
    <li>Dein Nutzerprofil (Name, Punkte, Level, tägliche Ziele)</li>
    <li>App-Einstellungen und Benachrichtigungseinstellungen</li>
  </ul>
  <p>Diese Daten verlassen dein Gerät nicht und werden von uns nicht eingesehen, gesammelt oder verarbeitet.</p>

  <h3>Daten bei In-App-Käufen (Apple)</h3>
  <p>Käufe und Abonnements werden ausschließlich über Apples StoreKit abgewickelt. Wir erhalten dabei keine Zahlungsdaten. Apple verarbeitet die Transaktionsdaten gemäß der <a href="https://www.apple.com/de/privacy/" target="_blank">Apple Datenschutzrichtlinie</a>.</p>

  <h3>Absturz- und Fehlerberichte</h3>
  <p>Im Falle eines App-Absturzes kann Apple anonymisierte Absturzberichte an uns übermitteln. Diese enthalten keine persönlich identifizierbaren Informationen.</p>

  <h2>3. Zweck der Datenverarbeitung</h2>
  <p>Die lokal gespeicherten Daten dienen ausschließlich dem Betrieb der App – also der Anzeige, Verwaltung und Analyse deiner Aufgaben, Gewohnheiten und Focus-Sessions.</p>

  <h2>4. Benachrichtigungen</h2>
  <p>Wenn du Benachrichtigungen aktivierst, werden lokale Push-Benachrichtigungen auf deinem Gerät geplant. Diese Daten werden nicht übertragen. Du kannst Benachrichtigungen jederzeit unter iOS-Einstellungen → FocusFlow deaktivieren.</p>

  <h2>5. Deine Rechte (DSGVO)</h2>
  <p>Da wir keine personenbezogenen Daten auf unseren Servern speichern, liegen alle Daten direkt unter deiner Kontrolle. Du hast folgende Möglichkeiten:</p>
  <ul>
    <li>Alle App-Daten löschen: Profil → Alle Daten löschen</li>
    <li>Vollständige Datenlöschung: App deinstallieren</li>
    <li>Auskunft über gespeicherte Daten: Kontaktiere uns per E-Mail</li>
  </ul>
  <p>Gemäß DSGVO hast du das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit sowie Widerspruch. Für Anfragen wende dich bitte an: <a href="mailto:hello.aerohq@gmail.com">hello.aerohq@gmail.com</a></p>

  <h2>6. Datensicherheit</h2>
  <p>Deine Daten werden lokal auf deinem Gerät gespeichert und sind durch die iOS-Sicherheitsmechanismen (Geräteverschlüsselung, App-Sandbox) geschützt. Wir empfehlen, dein Gerät mit einem Passcode zu sichern.</p>

  <h2>7. Kinder</h2>
  <p>FocusFlow richtet sich nicht gezielt an Kinder unter 13 Jahren. Wir sammeln wissentlich keine Daten von Kindern.</p>

  <h2>8. Änderungen dieser Datenschutzrichtlinie</h2>
  <p>Wir behalten uns vor, diese Datenschutzrichtlinie bei Bedarf anzupassen. Die aktuelle Version ist stets auf dieser Seite abrufbar. Bei wesentlichen Änderungen informieren wir dich über ein App-Update.</p>

  <h2>9. Kontakt</h2>
  <p>Bei Fragen zum Datenschutz erreichst du uns unter:<br>
  <a href="mailto:hello.aerohq@gmail.com">hello.aerohq@gmail.com</a></p>

  <h2>10. Beschwerderecht</h2>
  <p>Du hast das Recht, dich bei einer Datenschutz-Aufsichtsbehörde zu beschweren. Die zuständige Behörde in Deutschland findest du unter: <a href="https://www.bfdi.bund.de" target="_blank">www.bfdi.bund.de</a></p>

</div>

<footer>
  <div class="footer-links">
    <a href="index.html">Support</a>
    <a href="privacy.html">Datenschutzrichtlinie</a>
    <a href="terms.html">Nutzungsbedingungen</a>
  </div>
  <p>© 2025 Enzo Kaiser · FocusFlow</p>
</footer>

</body>
</html>
