# MEG@BIU Lab Website

Lab website for the MEG Laboratory (Goldstein Lab) at Bar-Ilan University's Gonda Brain Research Center.

Built with [Jekyll](https://jekyllrb.com/) + [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme, hosted on [GitHub Pages](https://pages.github.com/).

---

## Quick Setup — Deploy to GitHub Pages

### 1. Create the GitHub repository
- Go to GitHub → **New repository**
- Name it `YOUR_USERNAME.github.io` (for a user site) or any name (for a project site)
- Set it to **Public**
- Do NOT initialize with README (you already have one)

### 2. Push this site to GitHub
```bash
cd meglab-site
git init
git add .
git commit -m "Initial lab website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under "Source", select **GitHub Actions** (recommended) or **Deploy from a branch** → `main` / `root`
- Wait 2-3 minutes for the build

### 4. Custom domain (meglabbiu.org)
- The `CNAME` file is already included
- In your domain registrar (where you bought meglabbiu.org), update DNS:
  - Add an **A record** pointing to GitHub Pages IPs:
    ```
    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
    ```
  - Or add a **CNAME record**: `YOUR_USERNAME.github.io`
- In repo Settings → Pages, enter `meglabbiu.org` as custom domain
- Check "Enforce HTTPS"

---

## How to Edit Content

### Add a news post
Create a new file in `_posts/` with the format `YYYY-MM-DD-title.md`:
```markdown
---
title: "Your News Title"
date: 2026-04-01
---
Your news content here. You can use *markdown* formatting.
```

### Edit team members
Open `_data/team.yml` and add/remove entries. Place team photos in `assets/images/team/`.

### Add a publication
Open `_data/publications.yml` and add a new entry at the top:
```yaml
- year: 2026
  authors: "Author, A., Author, B."
  title: "Your paper title."
  journal: "Journal Name, vol, pages"
  link: "https://doi.org/..."
```

### Edit research descriptions
Open `_pages/research.md` and edit the markdown content directly.

---

## Local Preview (Optional)

If you want to preview changes locally before pushing:

### Option A: Docker (easiest)
```bash
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll serve
```

### Option B: Ruby/Jekyll
```bash
# Install Ruby (on Windows, use RubyInstaller or WSL)
gem install bundler
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`

---

## File Structure

```
meglab-site/
├── _config.yml          ← Main site configuration
├── _data/
│   ├── navigation.yml   ← Top nav bar links
│   ├── team.yml         ← Team member data
│   └── publications.yml ← Publication list
├── _pages/
│   ├── research.md      ← Research page
│   ├── team.md          ← Team page (reads from _data/team.yml)
│   ├── publications.md  ← Pubs page (reads from _data/publications.yml)
│   ├── news.md          ← News archive page
│   └── contact.md       ← Contact page
├── _posts/              ← News posts (YYYY-MM-DD-title.md)
├── assets/
│   └── images/
│       ├── hero-banner.jpg   ← Homepage hero image
│       └── team/             ← Team member photos
├── CNAME                ← Custom domain config
├── Gemfile              ← Ruby dependencies
├── index.md             ← Homepage (splash layout)
└── README.md            ← This file
```

---

## Customization

### Change the color skin
In `_config.yml`, change `minimal_mistakes_skin` to one of:
`default`, `air`, `aqua`, `contrast`, `dark`, `dirt`, `neon`, `mint`, `plum`, `sunrise`

### Add your hero image
Replace `assets/images/hero-banner.jpg` with your preferred image (the DALL·E space image from your Wix site, or any wide banner ~1200×400px).

### Add institutional logos
You can add logos to the footer or masthead by creating a custom `_includes/footer.html` override. See the [Minimal Mistakes docs](https://mmistakes.github.io/minimal-mistakes/docs/overriding-theme-defaults/) for details.

---

## Need Help?

- [Minimal Mistakes Documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
