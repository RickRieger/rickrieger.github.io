# Rick Rieger — Business Analyst & Developer

### 🔗 Live site: **[rickrieger.github.io](https://rickrieger.github.io/)**

My personal website: who I am, what I do as a Business Analyst at Dominion Leasing Software (SOWs, SQL, Crystal Reports, ASP.NET / Visual Basic maintenance), my interest in cloud computing, my coding projects, and a way to get in touch.

---

## Page sections

| Section | Component | What's in it |
|---|---|---|
| Nav | `src/components/section/Navbar.js` | Sticky top bar with section links; collapses to a ☰ menu on phones |
| Hero | `Hero.js` | Name, title, tagline, headshot, GitHub / LinkedIn / resume links |
| About | `About.js` | Background: current role, Army service, education and bootcamps |
| What I Do | `Experience.js` | Current role with four focus areas, plus grouped skill chips |
| Cloud Computing | `Cloud.js` | Interest in cloud, hands-on work so far, where I'm headed |
| Projects | `Projects.js`, `layouts/Project.js`, `layouts/ExercisesCard.js` | Full-stack apps, front-end sites, and a list of bootcamp exercises |
| Contact | `Contact.js` | Formspree contact form and social links |
| Footer | `Footer.js` | Copyright and back-to-top link |

## Editing content

**All text, projects and links are in [`src/profile.js`](src/profile.js).** You don't need to touch the components to change wording.

- **Add a project with a picture:** add an entry to `projects` (full-stack) or `miscellaneous` (front-end) with an `id`, then add a matching class with a `background-image` in [`src/styles/images.css`](src/styles/images.css). Put local images in `src/assets/`.
- **Add a small exercise:** add one line to `exercises`. It shows on the text-only "Bootcamp Exercises" card.
- **Restyle:** colors, radius and shadows are CSS variables at the top of [`src/styles/main.css`](src/styles/main.css).

## Built with

| Technology | Used for |
|---|---|
| React 17 (Create React App) | Component-based single-page site |
| Hand-written CSS | Layout and theme (`src/styles/main.css`); no CSS framework |
| Inter (Google Fonts), Font Awesome 5 | Typography and icons |
| AOS | Subtle fade-in as sections scroll into view |
| Formspree | Contact form backend. Emails are labeled `[Portfolio]` and include a `source` field. |
| GitHub Actions + GitHub Pages | Builds and hosts the site |

## Run it locally

```bash
npm ci
npm run build      # outputs to build/
```

On Node 17 or newer, set `NODE_OPTIONS=--openssl-legacy-provider` before building, because react-scripts 4 uses webpack 4. To preview the build locally, also set `PUBLIC_URL=.` and serve the `build/` folder with any static file server.

## Deployment

[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) runs on every push to `main`. It installs dependencies on Node 16, builds, and publishes `build/` to GitHub Pages. Because this repo is named `rickrieger.github.io`, it's served at the root address. My other project sites (for example `/Mits/`) are served from their own repos.

## History

- **2026-11-23:** New site. The design started as a redesign of my earlier React portfolio ([portfolio-template](https://github.com/RickRieger/portfolio-template), still live at [rickrieger.github.io/portfolio-template](https://rickrieger.github.io/portfolio-template/)) and moved here so both sites can exist. Original template credit: [kaustubhai/portfolio-template](https://github.com/kaustubhai/portfolio-template) (MIT license, see `LICENSE`).
- **2021-03-15:** This repo first held a small HTML practice page from my first bootcamp weeks. It's preserved on the [`legacy-2021-html-practice`](https://github.com/RickRieger/rickrieger.github.io/tree/legacy-2021-html-practice) branch.
