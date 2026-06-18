# SORAN Barber Shop – Dessau

Moderne Website für den SORAN Barber Shop in Dessau, gebaut mit Astro, Tailwind CSS und deployed auf Cloudflare Pages.

## Tech Stack

- [Astro](https://astro.build/) – Statischer Site Generator
- [Tailwind CSS](https://tailwindcss.com/) – Utility-first CSS Framework
- [Cloudflare Pages](https://pages.cloudflare.com/) – Hosting & CDN

## Projektstruktur

```
├── src/
│   ├── components/      # Wiederverwendbare Astro-Komponenten
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   ├── layouts/         # Seitenlayouts
│   │   └── Layout.astro
│   ├── pages/           # Routen (jede .astro-Datei = eine Route)
│   │   ├── index.astro
│   │   ├── impressum.astro
│   │   └── datenschutz.astro
│   └── styles/          # Globale Styles
│       └── global.css
├── public/              # Statische Assets (Bilder, Favicon)
├── .github/workflows/   # GitHub Actions
│   └── deploy.yml       # Automatisches Deployment zu Cloudflare Pages
├── astro.config.mjs
├── tailwind.config.mjs
├── wrangler.jsonc
└── package.json
```

## Lokale Entwicklung

```bash
npm install
npm run dev
```

Die Entwicklungsumgebung startet unter `http://localhost:4321`.

## Build

```bash
npm run build
```

Das Ergebnis landet im `dist/`-Ordner.

## Deployment

Das Projekt wird automatisch bei jedem Push auf `main` über GitHub Actions zu Cloudflare Pages deployed.

### Manuelles Deployment

Falls nötig:

```bash
npx wrangler pages deploy dist --project-name=soran-barbier
```

## Was noch fehlt / nächste Schritte

- [ ] Echte Adresse, Telefonnummer und E-Mail eintragen (`impressum.astro`, `datenschutz.astro`, `Footer.astro`)
- [ ] echte Bilder für den Shop einbauen (Hero, Team, Gallery)
- [ ] Google Maps-Embed in die Kontakt-Section einfügen
- [ ] Online-Terminbuchung verlinken (z. B. Treatwell, Square)
- [ ] Social-Media-Links aktualisieren (Instagram, Facebook)
- [ ] Öffnungszeiten und Preisliste pflegen
- [ ] SEO: Schema.org LocalBusiness JSON-LD ergänzen
