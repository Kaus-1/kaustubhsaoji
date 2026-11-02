# Publishing this site on GitHub Pages

Your site is built from the [al-folio](https://github.com/alshedivat/al-folio) academic theme and is ready to publish. Follow these steps once; after that, every time you push a change, GitHub rebuilds and redeploys the site automatically.

---

## 1. Create the GitHub repository

You have two options for the URL:

| You want the URL to be… | Name the repository… | `baseurl` in `_config.yml` |
|---|---|---|
| `https://YOURNAME.github.io` (recommended) | `YOURNAME.github.io` (use your exact GitHub username) | leave blank (already set) |
| `https://YOURNAME.github.io/website` | anything, e.g. `website` | set to `/website` |

1. Go to <https://github.com/new>.
2. Set the repository name as above, keep it **Public**, and **do not** add a README/.gitignore (this folder already has them).
3. Click **Create repository**.

## 2. Edit two lines in `_config.yml`

Open `_config.yml` and set:

- `url:` → `https://YOURNAME.github.io` (your real username)
- `baseurl:` → leave blank for the `YOURNAME.github.io` repo, **or** `/website` if you used a project repo (see table above).

While you're there, you can also fill in your social links in `_data/socials.yml` (LinkedIn, Google Scholar, ORCID, GitHub — just uncomment and fill the lines you want).

## 3. Push this folder to the repository

From inside this folder, in a terminal:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOURNAME/YOURNAME.github.io.git
git push -u origin main
```

(Replace the remote URL with your repo's URL.)

## 4. Turn on GitHub Pages + Actions

1. In your repo, go to **Settings → Actions → General** and make sure Actions are allowed, and that **Workflow permissions** is set to **Read and write permissions** (needed so the build can publish). Save.
2. Push any commit (step 3 already did). Go to the **Actions** tab — you'll see the **Deploy site** workflow running. It takes ~2–4 minutes the first time.
3. The workflow publishes the built site to a branch called **`gh-pages`**. Go to **Settings → Pages** and set **Source → Deploy from a branch**, **Branch → `gh-pages` / `root`**. Save.
4. Wait a minute, then open `https://YOURNAME.github.io`. Done. 🎉

> If the Actions tab shows a red ✗ on the first run, it's almost always the "Read and write permissions" setting in step 4.1 — set it, then re-run the job from the Actions tab.

---

## Making changes later

Edit files locally and `git push` — the site rebuilds itself. The files you'll touch most:

| What you want to change | File |
|---|---|
| Home page bio & research interests | `_pages/about.md` |
| Your profile photo | add `assets/img/prof_pic.jpg`, then uncomment the `image:` line in `_pages/about.md` |
| News items (the dated feed) | add/edit files in `_news/` |
| Projects | add/edit files in `_projects/` (and swap the placeholder images in `assets/img/projects/`) |
| Publications | `_bibliography/papers.bib` (BibTeX) |
| CV page content | `_data/cv.yml` |
| Downloadable CV PDF | replace `assets/pdf/Kaustubh_Saoji_CV.pdf` |
| Social links | `_data/socials.yml` |
| Site title, colours, metadata | `_config.yml` and `assets/css/main.scss` |

### Your custom theme

The teal/indigo "bio" colour theme and the animated protein ribbon on the home page live in **`assets/css/main.scss`** (everything below the big `Kaustubh's customisations` comment). The accent colour is one line — change `--global-theme-color`.

### Preview locally (optional)

If you want to see changes before pushing, install Ruby + Jekyll and run:

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. This is optional — GitHub builds the real site for you on every push.

---

## A couple of things to double-check

- **Author order on the publication.** I filled in the *Drug Discovery Today* citation from the public record, but please confirm the exact author order in `_bibliography/papers.bib` against your published PDF.
- **Add your links.** The site has no LinkedIn/Scholar/GitHub icons until you fill them in `_data/socials.yml`.
- **Profile photo.** The home page looks great without one, but a photo helps — see the table above.
