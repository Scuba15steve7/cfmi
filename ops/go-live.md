# Go live — GitHub Pages ($0)

Shortest path from this laptop to a public URL. No paid domain required.

**Do not use a custom `.org` yet.** Custom domains usually cost money (registrar + sometimes DNS). Start with:

`https://scuba15steve7.github.io/cfmi/`

**GitHub account:** `scuba15steve7`  
**Recommended repo name:** `cfmi` (short Pages path)

---

## 1. Commit locally (Cursor / terminal)

When you are ready:

```
Create a git commit for the current CFMI site and ops docs. Do not push.
```

Or commit yourself. Include at least `docs/`, `ops/go-live.md`, and related README / website notes.

---

## 2. Create a public GitHub repo (browser)

1. Open [https://github.com/new](https://github.com/new) and sign in as **scuba15steve7**.
2. **Repository name** — `cfmi` (recommended).
3. **Public** — select Public.
4. **Do not** check “Add a README” / “Add .gitignore” / “Choose a license” if this folder already has a git history (avoids merge noise).
5. Click **Create repository**.

Optional CLI (only if `gh` is installed and authenticated as scuba15steve7):

```bash
gh repo create cfmi --public --source=. --remote=origin
# Do not push until you ask Cursor to push, or push yourself after commit.
```

---

## 3. Push this project (terminal)

After the empty public repo exists:

```bash
git remote add origin https://github.com/scuba15steve7/cfmi.git
git branch -M main
git push -u origin main
```

Or ask Cursor: *Commit if needed, then push to origin.* Use SSH instead of HTTPS if that is how you authenticate.

---

## 4. Turn on GitHub Pages (browser)

1. Open [https://github.com/scuba15steve7/cfmi](https://github.com/scuba15steve7/cfmi).
2. Click **Settings**.
3. In the left sidebar, click **Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. **Branch:** `main`.
6. **Folder:** `/docs` (not `/ (root)`).
7. Click **Save**.

Wait one to two minutes. Refresh the Pages settings page; the live URL appears at the top when the first deploy finishes.

Site URL:

`https://scuba15steve7.github.io/cfmi/`

Homepage file served: `docs/index.html`. Assets under `docs/css`, `docs/js`, `docs/assets`. `docs/.nojekyll` keeps GitHub from running Jekyll on the folder.

---

## 5. After the URL works

1. Open the site; check Home, About, Charter, and that CSS / hero load.
2. Confirm the Bootstrap **Repository** link in `docs/index.html` points to `https://github.com/scuba15steve7/cfmi` (already set in-repo).
3. Optional later: custom domain under **Settings → Pages → Custom domain** (usually not free).

---

## Manual-only checklist

| Step | Who |
|------|-----|
| GitHub login as scuba15steve7 | You |
| Create public repo `cfmi` | You |
| Push | You (or ask Cursor after commit) |
| Settings → Pages → `main` / `/docs` | You |
| Custom `.org` | Skip until budget exists |

---

*If Pages shows 404: confirm the branch is `main`, folder is `/docs`, and `docs/index.html` is on that branch.*
