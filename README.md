# Barbería Distrito

Landing page para una barbería en Bogotá. HTML / CSS / JS puros, mobile-first, sin build step, sin dependencias.

🔗 **Live:** https://yici52.github.io/-barberia-distrito/

## Stack

- HTML5 + CSS3 + JavaScript vanilla
- Google Fonts (Bebas Neue + Inter), carga no bloqueante
- Imágenes generadas con [Pollinations.ai](https://image.pollinations.ai) (IA, seed fijo)
- Hosted en GitHub Pages

## Estructura

```
.
├── index.html       Todo el sitio (HTML, CSS y JS inline)
├── favicon.svg      Favicon SVG escalable
├── robots.txt       Permite todos los crawlers
├── sitemap.xml      Una URL — la página de inicio
└── README.md        Este archivo
```

## Features

- **SEO**: Open Graph, Twitter Cards, JSON-LD `HairSalon` schema, canonical, sitemap.
- **Accesibilidad**: WCAG 2.2 AA. Skip link, focus-visible, `prefers-reduced-motion`, ARIA correcto, contraste AA verificado.
- **Performance**: lazy load de imágenes y del iframe de Maps, `content-visibility` en secciones below-the-fold, preload de fuentes, defer de JS.
- **Seguridad**: CSP estricto, `Permissions-Policy`, `Referrer-Policy`, sandbox del iframe, honeypot anti-bot, rate-limit cliente, sanitización de inputs.
- **UX**: menú mobile, scroll hint, back-to-top, reveal on scroll, validación inline en formularios.

## Cambios típicos

| Quiero cambiar… | Buscar en `index.html` |
|---|---|
| Número de WhatsApp | `573001234567` (3 lugares) |
| Precios | bloque `<!-- SERVICIOS -->` |
| Dirección y horarios | bloque `<!-- AGENDAR -->` → `.info-list` |
| Texto del hero | bloque `<!-- HERO -->` |
| Datos del Schema.org | bloque `<script type="application/ld+json">` |

## Verificar

```bash
# HTML válido
open "https://validator.w3.org/nu/?doc=https://yici52.github.io/-barberia-distrito/"

# Schema válido
open "https://search.google.com/test/rich-results?url=https://yici52.github.io/-barberia-distrito/"

# Performance
npx lighthouse https://yici52.github.io/-barberia-distrito/ --view
```

## Roadmap

- [ ] Reemplazar imágenes IA por fotos reales del local
- [ ] Integrar Wompi para pagos de turnos premium
- [ ] Self-hostear fuentes para eliminar dependencia de Google
- [ ] Connect newsletter a Mailchimp / Brevo
- [ ] Migrar a Vercel / Netlify para CSP sin `'unsafe-inline'`
