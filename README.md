# ZELENA – Website

Investoren-One-Pager für ZELENA (Medizinalhanf & CBD aus der Ukraine), dreisprachig DE / EN / UK.
Statische Seite ohne Build-Schritt – direkt auf Netlify deploybar.

## Struktur

| Pfad | Inhalt |
|---|---|
| `index.html` | Die Seite (HTML, CSS, JS und alle drei Sprachversionen in einer Datei) |
| `favicon/` | Favicons (SVG, ICO, PNG, Apple Touch Icon) |
| `assets/og-image.png` | Vorschaubild für Social Media (1200 × 630) |
| `brand/` | Logo-Varianten als SVG + PNG (quer, gestapelt, nur Bildmarke; farbig und weiss) |
| `robots.txt` | Erlaubt Google, Bing und alle gängigen KI-Crawler (GPTBot, ClaudeBot, PerplexityBot, …) |
| `sitemap.xml` | Sitemap inkl. hreflang und Bild |
| `llms.txt` | Kurzfassung der Seite für KI-Suchmaschinen |
| `site.webmanifest` | Web-App-Manifest (Icons, Theme-Farbe) |
| `netlify.toml` | Netlify-Konfiguration (Security-Header, Caching) |

## Vor dem Livegang anpassen

1. **Domain:** `https://zelena-cbd.ch` ist ein Platzhalter. Suchen & Ersetzen in `index.html`, `sitemap.xml`, `robots.txt`, `llms.txt`.
2. **Mailadresse:** In `index.html` die Konstante `INVEST_MAIL` (aktuell `invest@zelena-cbd.ch`).
3. **Platzhalter im Lizenz-Abschnitt:** Lizenznummer, Behörde, Name des Professors und des Spitals (gestrichelt markiert, `class="ph"`).
4. **Rendite-Aussage** (20 % p.a., vertraglich fixiert) rechtlich prüfen lassen (FIDLEG).

## Sprachen

Die Sprache wird per Umschalter oben rechts gewählt und im Browser gespeichert.
Direktlinks: `/` (DE), `/#en`, `/#uk`.

## SEO & KI-Sichtbarkeit

- Meta-Tags für Google, Open Graph (Facebook, LinkedIn, WhatsApp) und Twitter/X
- Strukturierte Daten (schema.org JSON-LD): Organization, WebSite, WebPage, InvestmentOrDeposit, FAQPage
- `robots.txt` lässt KI-Crawler ausdrücklich zu, `llms.txt` liefert ihnen die Kernfakten
- Canonical, hreflang (de/en/uk), Sitemap

## Deployment (Netlify)

Repo mit Netlify verbinden, Build Command leer lassen, Publish Directory `.` – fertig.
