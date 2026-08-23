# Deploying this yourself

This folder is the whole design as **one self-contained file**, renamed `index.html`.
Every script, font and asset is inlined. No build step, no dependencies, no CDN.

---

## The three ways, easiest first

### 1 · Just open it
Double-click `index.html`. It runs offline in any browser. Nothing to install.

### 2 · Vercel — drag and drop
Go to vercel.com, drag this `deploy` folder onto the dashboard. It goes live in about
twenty seconds at a `*.vercel.app` URL. Vercel serves `index.html` at the root
automatically, so there is nothing to configure — no framework, no build command, no
output directory.

### 3 · GitHub Pages
Make a repo, drop `index.html` in the root, push. Then **Settings → Pages → Source:
deploy from a branch → main / root.** Live in a minute at
`https://<user>.github.io/<repo>`.

Netlify and Cloudflare Pages both work the same way — drag the folder, done.

---

## One thing to be careful about

**This has no authentication.** Anyone with the URL sees everything. And the fixtures are
not neutral — tenant names, revenue figures, the account matrix, the vault obligations.
Fine for a private link you share deliberately; not fine indexed by Google.

If you deploy it publicly, use a host that can put a password in front:

- **Vercel** — Deployment Protection (password or Vercel Auth) on the project
- **Cloudflare Pages** — Access policy
- **Netlify** — site-level password

Or keep it as a local file and open it when you need it, which needs no host at all.

---

## What this is and is not

**Is:** the complete design. Every surface, both themes, all interactions, ⌘K, the spine,
the summons, the Mind. Real logic reading real catalogues.

**Is not:** the product. No database, no auth, no writes. Every figure is a fixture. Nothing
you click changes anything anywhere — which is exactly what makes it safe to hand to someone
to look at.

---

## If you want to change it after deploying

Don't edit `index.html` — it is compiled output, one long line in places, and an edit there
is lost the next time it is rebuilt. Changes happen in the source
(`PAIGE Super Admin Shell v3.dc.html` + `paige-ia.js`), and a fresh `index.html` gets
generated from that.
