# Evidence to Lead, LLC — Website

> *Bridging research, leadership, and practice.*

A professional multi-page static website for **Evidence to Lead, LLC**, a boutique education research and strategy consultancy that helps organizations translate evidence into clear, actionable decisions.

---

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `about.html` | About |
| `services.html` | Services |
| `approach.html` | Approach |
| `insights.html` | Insights |
| `contact.html` | Contact |

---

## Project Structure

```
/
├── index.html          # Home page
├── about.html          # About / Founder bio
├── services.html       # Four service pillars
├── approach.html       # Clarify → Analyze → Translate → Implement
├── insights.html       # Essays, frameworks, policy briefs
├── contact.html        # Contact form + sidebar
│
├── style.css           # Global design system (tokens, typography, nav, footer)
├── home.css            # Home page styles
├── about.css           # About page styles
├── services.css        # Services page styles
├── approach.css        # Approach page styles
├── insights.css        # Insights page styles
├── contact.css         # Contact page styles
│
├── main.js             # Shared JS: nav behavior, scroll reveals, form handling
├── nav-footer.js       # Shared nav + footer injection
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Technology

- **HTML5** — semantic markup, ARIA labels, skip links
- **CSS3** — custom properties, grid, flexbox, intersection-based animations
- **Vanilla JavaScript** — no frameworks or dependencies
- **Google Fonts** — Playfair Display, Source Serif 4, Montserrat (loaded via CDN)

No build tools, bundlers, or package managers required.

---

## Design System

### Color Palette

| Token | Hex | Usage |
|---|---|---|
| `--navy` | `#0C3957` | Primary brand color, headings |
| `--teal` | `#2E8B8B` | Accent, CTAs, links |
| `--gold` | `#D1A23A` | Highlight, eyebrows, rules |
| `--gray` | `#C5C7C9` | Borders, muted UI |
| `--ivory` | `#F8F9FA` | Page backgrounds |

### Typography

| Role | Font |
|---|---|
| Display / Headings | Playfair Display |
| Body copy | Source Serif 4 |
| UI / Labels / Nav | Montserrat |

### Aesthetic

The design follows a **"Living Document"** direction — inspired by annotated policy papers and academic journals. Signature elements include:

- Dot-grid CSS texture on page backgrounds
- Ghost large numerals behind phase/card content
- Gold horizontal rule accents
- Geometric SVG illustrations (no raster images)
- Scroll-triggered reveal animations via `IntersectionObserver`

---

## Running Locally

No build step required. Serve from any static file server:

```bash
# Python (built-in)
python3 -m http.server 3000

# Node (npx)
npx serve .

# VS Code
# Use the Live Server extension
```

Then open `http://localhost:3000` in your browser.

---

## Deployment

This is a fully static site — it can be deployed to any static hosting provider:

- **GitHub Pages** — push to a `gh-pages` branch or configure from `main`
- **Netlify** — drag-and-drop the project folder or connect a Git repo
- **Vercel** — `vercel --prod` from the project root
- **AWS S3 + CloudFront** — upload files and configure static website hosting

No server-side processing, databases, or environment variables required.

---

## Customization

### Updating Contact Email

Find and replace `info@evidencetolead.com` across all HTML files.

### Adding a Real Contact Form

The form in `contact.html` currently simulates submission (client-side only). To process real submissions, replace the `submit` handler in `main.js` with a `fetch` call to a form service such as:

- [Formspree](https://formspree.io)
- [Netlify Forms](https://docs.netlify.com/forms/setup/) (add `netlify` attribute to `<form>`)
- [EmailJS](https://www.emailjs.com)

### Adding the Founder Portrait

Replace the SVG placeholder in `about.html` with an `<img>` tag pointing to a real photo:

```html
<!-- Replace this: -->
<div class="portrait-img" ...>
  <svg ...>...</svg>
</div>

<!-- With this: -->
<img src="assets/dr-matthew-finster.jpg" alt="Dr. Matthew Finster" class="portrait-img">
```

### Updating Metadata

Each page includes `<title>` and `<meta name="description">` tags. Update these to reflect any changes in positioning or content focus.

---

## Browser Support

| Browser | Support |
|---|---|
| Chrome / Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| iOS Safari | ✅ Full |
| Samsung Internet | ✅ Full |

Requires `IntersectionObserver` support (all modern browsers). No polyfills included.

---

## License

MIT — see [`LICENSE`](./LICENSE) for details.

---

*Built for Evidence to Lead, LLC. © 2025 Evidence to Lead, LLC.*
