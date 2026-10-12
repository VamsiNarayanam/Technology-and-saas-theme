# Stackly Technology — Graphite Signal

ThemeForest-ready static HTML template for technology and SaaS brands. Includes marketing pages (when bundled), authentication screens, client and admin dashboards, and a styled 404 page.

## Quick start

1. Unzip the package to a folder on your computer.
2. **Option A:** Open `index.html` directly in a modern browser (double-click or drag into the window).
3. **Option B (recommended):** Serve the folder with a local static server so relative paths and future AJAX behave consistently, for example:
   - **Node:** `npx serve .`
   - **Python 3:** `python -m http.server 8080`
   - **PHP:** `php -S localhost:8080`
4. Visit `http://localhost:8080` (or the port shown by your tool).

Auth and dashboard demos:

- `login.html` — sign-in layout
- `register.html` — registration layout
- `client.html` — client dashboard
- `admin.html` — admin dashboard
- `404.html` — error page

## Folder structure

```
├── index.html              # Homepage
├── about.html
├── services.html
├── blogs.html
├── blog-single.html
├── contact.html
├── login.html
├── register.html
├── client.html             # Client dashboard
├── admin.html              # Admin dashboard
├── 404.html
├── css/
│   └── style.css           # Graphite Signal design system
├── js/
│   └── main.js             # Preloader, nav, AOS, sliders, forms, pagination, dashboards
├── Images/
│   └── *.webp              # Optimized theme imagery (<98KB each)
└── README.md
```

## Customization

### Colors and typography

Edit CSS custom properties at the top of `css/style.css` under `:root`:

| Token | Default | Usage |
|-------|---------|--------|
| `--ink`, `--slate` | Dark graphite | Headers, sidebars, dark sections |
| `--signal`, `--signal-2` | Blue / teal | Primary actions, accents |
| `--panel`, `--cloud` | Light surfaces | Page background, cards |
| `--font-display` | Sora | Headings |
| `--font-body` | Manrope | Body copy |
| `--font-mono` | IBM Plex Mono | Labels, KPIs, eyebrows |

Google Fonts are loaded in each HTML file; swap the `<link>` URLs and token values together if you change families.

### Scripts and styles

- Global styles: `css/style.css`
- Behavior: `js/main.js` (loaded with `defer` on all pages)
- Icons: Font Awesome 6 via CDN (replace with self-hosted files for offline builds if required)

### Forms

Forms with `data-validate` show client-side validation states only. Connect `action` attributes to your backend or SaaS auth provider before production use.

## Browser support

- Chrome, Edge, Firefox, Safari (last two major versions)
- Responsive layouts from ~320px upward
- `prefers-reduced-motion` respected for animations, preloader, and scroll effects
- Progressive enhancement: content remains readable if JavaScript is disabled (pagination and drawers fall back to full table / desktop sidebar)

## Features

- **Preloader** — `.preloader` fades out on window load
- **Sticky header** — scroll state via `.site-header.is-scrolled`
- **Mobile navigation** — `.nav-toggle` with `aria-expanded`
- **AOS-style scroll reveals** — `[data-aos]` attributes
- **Marquee** — infinite logo/text bands (marketing pages)
- **Slider** — `[data-slider]` carousels with dots and autoplay
- **FAQ accordion** — `.faq__item` toggle pattern
- **Blog filters & pagination** — `[data-blog-grid]`, `[data-pagination]`
- **Form validation UI** — `form[data-validate]`, `.field__error`, `.is-invalid`
- **Dashboard drawer** — `.dash`, `.sidebar-toggle`, `.dash-overlay`, `.is-sidebar-open`
- **Table pagination** — `[data-table-page]` with `[data-table-pager]` and `data-per-page`
- **404 page** — `.error-page` with gradient code treatment

## Images

- Store assets in `Images/` as **WebP** for performance.
- Target **under 98 KB** per image where possible (hero and auth panels may be larger; compress with Squoosh, ImageOptim, or similar).
- Use descriptive `alt` text on all meaningful images; decorative backgrounds use `aria-hidden="true"` where appropriate.
- Referenced examples in this slice: `auth-panel.webp`, `team-1.webp`.

## Credits

- Fonts: [Google Fonts](https://fonts.google.com/) — Sora, Manrope, IBM Plex Mono
- Icons: [Font Awesome 6](https://fontawesome.com/)

## License

Use according to your ThemeForest / marketplace license. Do not redistribute as a standalone template outside license terms.
