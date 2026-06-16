#  Portfolio

A personal portfolio website built with plain HTML, CSS, and JavaScript —
no frameworks, no build step. Includes a light/dark mode toggle and a
6-color accent picker (Teal, Purple, Blue, Rose, Amber, Green).

## Project structure

```
siddhi-portfolio/
├── index.html      # the entire site (single file)
├── vercel.json      # deployment config (security headers, clean URLs)
├── package.json     # for local preview only — no build required
└── README.md
```

## Preview locally

You don't need Node or any build tools — just open `index.html` in your
browser. If you want a local server (for things like relative paths or
testing), run:

```bash
npx serve .
```

Then visit the URL it prints (usually `http://localhost:3000`).

---

## Deploy to Vercel

### Option A — Vercel CLI (fastest)

1. Install the CLI if you don't have it:
   ```bash
   npm install -g vercel
   ```
2. From inside this project folder, run:
   ```bash
   vercel
   ```
3. Follow the prompts (log in, confirm project name, accept defaults —
   it's a static site so no build command is needed).
4. To push to production:
   ```bash
   vercel --prod
   ```

Vercel will give you a live URL like `siddhi-waghmare.vercel.app`.

### Option B — GitHub + Vercel Dashboard (recommended for updates)

1. Create a new GitHub repository and push this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new) and import the
   GitHub repo.
3. Framework Preset: choose **"Other"** (it's a static site — Vercel
   will detect `index.html` automatically).
4. Leave Build Command and Output Directory **empty**.
5. Click **Deploy**.

Every future `git push` to `main` will auto-redeploy your site.

---

## Custom domain

Once deployed, go to your project on Vercel → **Settings → Domains** →
add your domain (e.g. `siddhiwaghmare.dev`) and follow the DNS
instructions Vercel provides.

---

## Editing content

Everything — text, links, projects, skills, colors — lives inside
`index.html`. Key sections are clearly commented:

- `<!-- ── ABOUT ── -->`
- `<!-- ── EXPERIENCE ── -->`
- `<!-- ── PROJECTS ── -->`
- `<!-- ── RESEARCH ── -->`
- Theme/accent picker logic is at the bottom in `<script>`

To update your résumé link, social links, or email, search for
`waghmaresiddhi1607@gmail.com`, `github.com/wsiddhi`, and
`linkedin.com/in/siddhi-waghmare-tech` and replace with updated values.
