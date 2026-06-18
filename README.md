# SORAN Barbier – Website

Moderne Website für den lokalen Barbier-Shop **SORAN** in Dessau-Roßlau.

## 🚀 Tech Stack

- [Astro](https://astro.build/) – schnelles, statisches Site-Rendering
- [Tailwind CSS](https://tailwindcss.com/) – Utility-First CSS
- [Cloudflare Pages](https://pages.cloudflare.com/) – Hosting & Deployment
- [Wrangler](https://developers.cloudflare.com/workers/wrangler/) – CLI für Cloudflare

## 📁 Projektstruktur

```
/
├── public/              # Statische Assets (Bilder, Favicon)
├── src/
│   ├── components/      # Wiederverwendbare Astro-Komponenten
│   │   ├── Header.astro
│   │   └── Footer.astro
│   ├── layouts/         # Seiten-Layouts
│   │   └── Layout.astro
│   ├── pages/           # Astro-Seiten (Routing)
│   │   ├── index.astro
│   │   ├── impressum.astro
│   │   └── datenschutz.astro
│   ├── styles/
│   │   └── global.css   # Tailwind + Custom Styles
│   └── config.ts        # Site-Konfiguration
├── astro.config.mjs     # Astro-Konfiguration
├── tailwind.config.mjs  # Tailwind-Farben & Animationen
└── wrangler.jsonc       # Cloudflare-Deployment-Konfig
```

## 🛠️ Entwicklung

```bash
# Dependencies installieren
npm install

# Dev-Server starten
npm run dev

# Produktions-Build
npm run build

# Preview lokal mit Wrangler
npm run preview
```

## 🌐 Deployment

### Automatisch via GitHub + Cloudflare Pages

1. Repo auf GitHub pushen
2. In [Cloudflare Dashboard](https://dash.cloudflare.com/) → Pages → "Create a project"
3. GitHub-Account verbinden und Repo auswählen
4. Build-Einstellungen:
   - **Build command:** `npm run build`
   - **Build output:** `dist`

### Manuell via Wrangler CLI

```bash
npm run deploy
```

## 📝 Anpassungen

| Datei | Zweck |
|-------|-------|
| `src/config.ts` | Seiten-Titel, Beschreibung, URL |
| `tailwind.config.mjs` | Farben, Fonts, Animationen |
| `src/pages/index.astro` | Hauptseite mit allen Sektionen |
| `src/styles/global.css` | Globale Styles & Button-Klassen |

## 📄 Lizenz

Privat – SORAN Barbier Dessau.
