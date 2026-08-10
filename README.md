# Your site — go live in about 15 minutes

This is one file: `index.html`. No build step, no dependencies. GitHub Pages will serve it as-is.

## 1. Connect the contact form (do this first — 3 min)

The form currently posts to a placeholder. Until you fix this, submissions go nowhere.

1. Go to [formspree.io](https://formspree.io) and sign up free (50 submissions/month free tier).
2. Create a new form. Set the destination email to `scarlett.michanco@gmail.com`.
3. Formspree gives you a form ID that looks like `myznrqkw`. Copy it.
4. Open `index.html`, find this line (Ctrl+F for `YOUR_FORM_ID`):
   ```html
   <form id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. Replace `YOUR_FORM_ID` with your real ID.
6. Formspree will send you one confirmation email the first time someone submits — click the link in it to activate the form. Send yourself a test message once the site is live to trigger this.

## 2. Create the GitHub repo (5 min)

1. Go to [github.com/new](https://github.com/new).
2. Name it whatever you like — `scarlett-michanco` or `ai-agent-studio` both work. It doesn't have to match your username.
3. Set it to **Public** (required for free GitHub Pages).
4. Don't initialize with a README (you already have one here).
5. Create the repo, then on your machine:
   ```bash
   cd path/to/this/folder
   git init
   git add .
   git commit -m "Launch site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

## 3. Turn on GitHub Pages (2 min)

1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment," set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main`, folder `/ (root)`, then **Save**.
4. Wait 1-2 minutes. Your site goes live at:
   `https://YOUR_USERNAME.github.io/YOUR_REPO/`

## 4. Optional: a real domain instead of `github.io`

If you buy a domain (e.g. `scarlettmichanco.com` on Namecheap/Google Domains, ~$12/yr):
1. In the repo root, create a file named `CNAME` (no extension) containing just your domain, e.g. `scarlettmichanco.com`.
2. At your domain registrar, add a `CNAME` record pointing to `YOUR_USERNAME.github.io`.
3. Back in **Settings → Pages**, enter the custom domain and check "Enforce HTTPS" once it's available.

This isn't required to launch tomorrow — the free `github.io` URL works immediately and you can add a domain anytime later without breaking anything.

## 5. Before you share the link, check:

- [ ] Formspree ID is swapped in (step 1) — send yourself a real test submission
- [ ] Phone number and email in the footer/contact section are correct
- [ ] Page title in the browser tab reads correctly
- [ ] Open it on your phone — everything's readable and the form works

## Updating content later

Everything is in `index.html` — copy in the `<body>`, styling in the `<style>` block at the top. No framework, so you (or Claude) can edit text directly: search for the phrase you want to change and replace it.

If you land a project and want to swap a service description, update a stat, or add a new case study to the "Selected work" grid, just copy an existing `.work-card` block and edit the text — the layout adapts automatically.
