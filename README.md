/* ---------- Base ---------- */
:root {
  --bg: #f5f7fb;
  --card: #ffffff;
  --text: #1a1f2b;
  --muted: #5d667a;
  --primary: #0f766e;
  --primary-dark: #0b5f59;
  --border: #e4e8f0;
  --shadow: 0 8px 24px rgba(16, 24, 40, 0.08);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: "Segoe UI", Tahoma, sans-serif;
  background: linear-gradient(180deg, #f7f9fc 0%, #eef3fb 100%);
  color: var(--text);
  line-height: 1.6;
}

/* ---------- Layout ---------- */
.container {
  width: min(1100px, 92%);
  margin: 0 auto;
}

section {
  padding: 72px 0;
}

.section-title {
  font-size: 2rem;
  margin-bottom: 22px;
}

/* ---------- Navbar ---------- */
header {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(8px);
  border-bottom: 1px solid var(--border);
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 72px;
}

.logo {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text);
  text-decoration: none;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 18px;
}

.nav-links a {
  text-decoration: none;
  color: var(--text);
  font-weight: 500;
}

.nav-links a:hover {
  color: var(--primary);
}

/* ---------- Hero ---------- */
.hero {
  min-height: 80vh;
  display: grid;
  place-items: center;
  text-align: center;
}

.hero h1 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  line-height: 1.2;
  margin-bottom: 16px;
}

.hero p {
  max-width: 700px;
  margin: 0 auto 26px;
  color: var(--muted);
  font-size: 1.05rem;
}

.btn {
  display: inline-block;
  text-decoration: none;
  background: var(--primary);
  color: #fff;
  padding: 12px 22px;
  border-radius: 10px;
  font-weight: 600;
  transition: 0.2s ease;
}

.btn:hover {
  background: var(--primary-dark);
  transform: translateY(-1px);
}

/* ---------- About ---------- */
.about p {
  color: var(--muted);
  max-width: 800px;
}

/* ---------- Projects ---------- */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.project-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 18px;
  box-shadow: var(--shadow);
  transition: 0.2s ease;
}

.project-card:hover {
  transform: translateY(-4px);
}

.project-card h3 {
  margin-bottom: 8px;
}

.project-card p {
  color: var(--muted);
  margin-bottom: 12px;
}

.project-card a {
  color: var(--primary);
  text-decoration: none;
  font-weight: 600;
}

/* ---------- Contact ---------- */
.contact-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 24px;
  box-shadow: var(--shadow);
}

.contact-list {
  list-style: none;
  display: grid;
  gap: 10px;
}

.contact-list a {
  color: var(--primary);
  text-decoration: none;
}

/* ---------- Footer ---------- */
footer {
  border-top: 1px solid var(--border);
  padding: 24px 0;
  text-align: center;
  color: var(--muted);
}

/* ---------- Responsive ---------- */
@media (max-width: 900px) {
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .nav {
    height: auto;
    padding: 14px 0;
    flex-direction: column;
    gap: 10px;
  }

  .nav-links {
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .projects-grid {
    grid-template-columns: 1fr;
  }

  section {
    padding: 56px 0;
  }
}
