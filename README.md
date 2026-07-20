# Little Wins Health — site files & hosting guide

Domain: **littlewinshealth.com**
Brand name on the page: **Little Wins Health**

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | Homepage (this MUST stay named `index.html` — it's what loads at your domain root) |
| `diabetes.html` | Diabetes category page (the article grid) |
| `how-diabetes-happens.html` | Article: What actually happens in your body when you have diabetes |
| `diabetes-increasing-us.html` | Article: Is diabetes increasing in the US? |

All pages link to each other correctly. Open `index.html` in a browser to check it works before uploading.

---

## Option 1 — Netlify (easiest, ~5 minutes)

1. Go to **app.netlify.com/drop**
2. Drag this whole `littlewins-site` folder onto the page
3. It goes live immediately at a random URL like `brave-lion-123.netlify.app`
4. Click **"Sign up to keep this site"** and create a free account (Netlify won't let you edit or keep it otherwise)
5. In Site settings → Change site name, rename it to something like `littlewinshealth`

To update later: drag the folder onto the site's "Deploys" tab again. That's it.

### Connecting littlewinshealth.com
1. Buy the domain (Namecheap or Cloudflare, ~$12/yr)
2. In Netlify: **Domain settings → Add custom domain →** type `littlewinshealth.com`
3. Netlify shows you nameservers (like `dns1.p03.nsone.net`). Copy them.
4. In your registrar, find **Nameservers**, choose "Custom DNS", paste them in
5. Wait 10 minutes to a few hours. HTTPS is set up automatically and free.

---

## Option 2 — GitHub Pages (free, more "developer" path)

1. Create a free account at **github.com**
2. Click **New repository**, name it `littlewinshealth`, set it **Public**, click Create
3. Click **uploading an existing file**, drag in all the `.html` files, click Commit
4. Go to **Settings → Pages**
5. Under "Branch", choose `main` and `/ (root)`, click Save
6. Wait ~1 minute. Your site is at `yourusername.github.io/everydaybetter`

### Connecting littlewinshealth.com
1. In Settings → Pages → Custom domain, enter `littlewinshealth.com`, Save
2. At your registrar, add these DNS records:
   - Four **A records** for `@` pointing to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME** for `www` pointing to `yourusername.github.io`
3. Back in GitHub Pages settings, tick **Enforce HTTPS** once it becomes available

---

## After you're live — the actual checklist

- [ ] Buy `littlewinshealth.com`
- [ ] Deploy via Netlify or GitHub Pages
- [ ] Connect the domain, confirm HTTPS works
- [ ] Set up **Google Search Console** (free) and submit your site so Google indexes it
- [ ] Set up analytics — Plausible or Google Analytics — so you can see what people read
- [ ] Swap the newsletter form for a real one (**MailerLite** or **Buttondown** have free tiers). Right now the form is a demo: it shows a success message but doesn't store the email anywhere.
- [ ] Write an **About** and **Editorial policy** page — for a health site, saying who you are and how you source things matters a lot for reader trust and for Google
- [ ] Keep publishing. Aim for the diabetes cluster first before opening new categories.

## Notes / things to know

- These pages are plain HTML with no build step and no dependencies. They'll work anywhere, forever, and load fast.
- The two charts and all infographics are hand-built SVG/CSS — no image files to lose, nothing to license.
- The newsletter form is **not functional yet** — it's a front-end demo only.
- Every page carries a medical disclaimer. Keep it there.
- The footer mentions affiliate links. Only keep that line once you actually use them, and follow FTC disclosure rules.
