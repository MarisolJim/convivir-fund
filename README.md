# Convivir Fund

Marketing website for the **Convivir Fund**, a mini-grant fund that provides direct
financial support to students who are traditionally underserved by existing aid
programs. Grants are not scholarships — they are $500 emergency and hardship funds
designed to remove financial barriers so students can stay focused on their education.

The fund is currently in pilot, in partnership with [DIY Girls](https://www.diygirls.org),
and is not accepting open applications at this time.

## What the fund supports

- **Basic Needs** — food-insecure students and those facing housing or financial instability.
- **Participation Costs** — fees, uniforms, and equipment for sports, clubs, and activities.
- **Relief for Student Workers** — helping working students reduce hours and focus on school.

## Tech stack

- [Astro](https://astro.build) 5 — static site framework
- [Tailwind CSS](https://tailwindcss.com) 4 (via `@tailwindcss/vite`)
- Fonts: Oswald (display) + Inter (body), loaded from Google Fonts
- [Netlify Forms](https://docs.netlify.com/forms/setup/) — powers the contact form

## Project structure

```
src/
├── components/
│   ├── ContactForm.astro   # Netlify-backed contact form
│   ├── Footer.astro
│   └── Header.astro
├── layouts/
│   └── Layout.astro        # shared HTML shell (head, header, footer)
├── pages/
│   ├── index.astro         # home
│   ├── about.astro
│   └── contact.astro
└── styles/
    └── global.css          # Tailwind entry + theme tokens
```

## Getting started

Requires Node.js. Install dependencies and start the dev server:

```bash
npm install
npm run dev
```

The site runs at `http://localhost:4321` by default.

## Scripts

| Command           | Action                                        |
| ----------------- | --------------------------------------------- |
| `npm run dev`     | Start the local dev server                    |
| `npm run start`   | Alias for `npm run dev`                        |
| `npm run build`   | Build the production site to `./dist`         |
| `npm run preview` | Preview the production build locally          |

## Deployment

The site is built as a static bundle (`npm run build` → `dist/`) and deployed on
Netlify. The contact form relies on Netlify Forms, so form submissions only work
once the site is deployed to Netlify (not in local dev).

## License

See [LICENSE](LICENSE).
