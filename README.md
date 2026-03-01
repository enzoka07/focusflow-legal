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
