# Fact Sheet – GitHub Pages (JaFi)

## 1. Überblick
GitHub Pages ist ein Hosting-Dienst von GitHub für statische Webseiten.  
Damit lassen sich Webseiten direkt aus einem Repository bereitstellen – kostenlos, einfach und ideal für Dokumentationen, Portfolios oder Projekthomepages.

GitHub Pages eignet sich vor allem, wenn du dein Informatik-Projekt öffentlich präsentieren oder deine README in eine vollwertige Doku-Seite umwandeln willst.

---

## 2. Funktionsweise
- Inhalte aus deinem Repository (Markdown oder HTML) werden von GitHub automatisch zu einer Website umgewandelt.
- Keine Server-Logik: nur statische Inhalte (HTML, CSS, JS).
- Optional kannst du Jekyll oder andere Site-Generatoren nutzen (z. B. Docusaurus, MkDocs).
- Deployment passiert automatisch bei jedem Push.

---

## 3. Einrichtung – Schritt für Schritt
1. Repository erstellen
    - Neues Repo auf GitHub anlegen (z. B. `mein-projekt`).
    - Falls noch nicht vorhanden: `README.md` hinzufügen.

2. Dateien für die Website vorbereiten  
   Zwei Varianten sind möglich:
    - Variante A (empfohlen):  
      Im Branch `main` den Ordner `/docs/` erstellen und dort eine `index.md` oder `index.html` ablegen.
    - Variante B:  
      Einen eigenen Branch `gh-pages` anlegen und die Website-Dateien dort ablegen.

3. GitHub Pages aktivieren
    - Gehe auf: `Settings → Pages`
    - Source: `Deploy from a branch`
    - Branch: `main` und `/docs` auswählen (oder `gh-pages`, falls du Variante B nutzt).
    - Speichern.

4. Warten & testen
    - Nach 1–2 Minuten ist die Seite live unter:  
      `https://<username>.github.io/<repo-name>/`

---

## 4. Verzeichnisstruktur – Best Practice
```plaintext
mein-projekt/
│
├── docs/                   # Alle Inhalte für GitHub Pages
│   ├── index.md             # Landing Page (Startseite)
│   ├── installation.md      # Installationsanleitung
│   ├── usage.md             # Nutzung & Beispiele
│   ├── api.md               # API Referenz
│   ├── faq.md               # Häufige Fragen
│   └── changelog.md         # Versionshinweise
│
├── README.md                # Repo-Doku für Entwickler
└── _config.yml              # (optional) Jekyll-Konfiguration
```

---

## 5. Typische Inhalte einer GitHub Pages Site
- Projektübersicht: Projektname, Kurzbeschreibung, Links zum Code, Issues, Releases

- Installation: Setup-Schritte, Dependencies
- Nutzung: Code-Beispiele, Screenshots
- API-Dokumentation: Endpunkte, Parameter, Rückgaben
- FAQ / Troubleshooting: bekannte Probleme und Lösungen
- Release Notes / Changelog: Änderungen und Bugfixes

---

## 6. Weitere Infos

- Nur statisch: kein PHP, keine Datenbank, kein Backend.
- Öffentlichkeit beachten: Inhalte sind für alle sichtbar. Keine Secrets oder private Daten ins Repo legen.
- Build-Fehler: Wenn Jekyll aktiviert ist, achte auf valide Front-Matter (--- Blöcke).
- Relative Pfade: Bilder/Links müssen korrekt relativ eingebunden sein. Beispiel: `![Screenshot](./img/demo.png)`
- Cache: Änderungen brauchen manchmal bis zu 1 Minute, bis sie sichtbar sind. Browser-Cache leeren hilft.

---

## 7. Wann GitHub Pages nutzen?

- Für Projektdokumentationen
- Als öffentliche Landing Page für Open-Source
- Für Präsentationen im Studium/Job (z. B. Informatik-Projekte)
- Für eigene Portfolios oder Blogs

---

## 8. Unterschied Wiki und Pages

- Wiki = Notizbuch für Entwickler
  - Es ist direkt im Repository unter dem Tab "Wiki" aufrufbar
  - Ist mit Markdown aufgebaut
  - Design ist simpel
  - Daten werden separat gespeichert (praktisch eigenes Repo)
- GitHub Pages = Visitenkarte fürs Projekt (öffentlich)
  - Eigene Webseite
  - Markdownm, HTML, CSS
  - Struktur kann man komplett selbst bestimmen
  - Zielgruppe ist oft öffentlich
  - Daten werden im bestehenden Repo integriert
    - `docs` Ordner im Projekt
    - Eigener Branch `gh-pages`


