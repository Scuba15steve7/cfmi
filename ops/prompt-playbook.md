# CFMI Prompt Playbook

**Operating rule:** Advance CFMI by pasting prompts into Cursor. The agent updates the repository.

**Current phase:** Mission + online presence + formation readiness.  
**Later phase:** AI-driven legislation and model bills (secondary).

---

## Phase 1 — Mission & presence (do these first)

| Step | Paste |
|------|--------|
| 1 | **M1** — Lock short public mission |
| 2 | **W1** — Build deployable website |
| 3 | **P1** — Align pitch to mission (not a flagship bill) |
| 4 | **R1** — Align README homepage story |
| 5 | **F1** — Formation checklist |
| 6 | **D1** — Commit when you ask |
| 7 | **G1** — GitHub Pages / go-live prep |

### M1 — Lock public mission
```
Write a short public mission statement (2–4 sentences) and a one-line tagline for CFMI, consistent with CHARTER.md. Put them in website/index.md, website/about.md, README.md, and pitch/one-pager.md. Do not change CHARTER.md principles. Lead with mission and online presence—not flagship legislation.
```

### W1 — Deployable site
```
Ensure docs/ is a minimal, professional static site for GitHub Pages (folder /docs). Mission-first homepage: brand, mission, principles link, about, charter, how to support—no flagship bill as the hero. Keep website/*.md conceptually aligned. Follow my frontend design rules. Keep it simple and donor-credible. Include docs/.nojekyll.
```

### P1 — Pitch = mission org
```
Rewrite pitch/one-pager.md as a mission-and-method nonprofit pitch. Proof at $0 = charter, methodology, site, transparency rules. List AI legislation and model bills as the upcoming product lane, not the lead ask.
```

### R1 — README face
```
Rewrite README.md so the repo face is: what CFMI is, mission, principles, status (bootstrap), links to charter/site/pitch, and how the project is built in Cursor. Move model bills and AI reviews to a clearly secondary “Work product (later / samples)” section.
```

### F1 — Formation checklist
```
Create ops/formation-checklist.md: 501(c)(3) vs (c)(4) decision tree, documents needed, Utah considerations if relevant, and prompts to draft bylaws/conflict-of-interest aligned to CHARTER.md. Mark attorney-review required. Do not claim we have tax status.
```

### D1 — Commit
```
Create a git commit for the current CFMI bootstrap (mission + presence phase). Do not push.
```

### G1 — Go live prep
```
Confirm ops/go-live.md has the exact manual clicks: public repo → push main → Settings → Pages → Deploy from branch main / folder /docs. Note custom .org is usually not free; use username.github.io/repo first. Do not push or commit unless I ask.
```

---

## Phase 2 — AI legislation (after presence)

Only after Phase 1 feels solid:

### L1 — Start AI review cadence
```
Set up ai-reviews/ as the first product lane: index README, refresh template, and review one real federal bill I paste or you propose. Mission and site stay primary in website/ and pitch/.
```

### L2 — First model act (when ready)
```
Draft [licensing / housing / other] model act to CFMI standards. Keep website messaging mission-first; link the bill as work product, not the hero.
```

Full older drafting prompts (B1–B4, C1–C3, etc.) remain valid in git history / ask the agent to restore them when Phase 2 starts. Prefer the Phase 1 prompts above until then.

---

## What still requires you offline

- GitHub account / login / creating the remote  
- Domain purchase (optional)  
- Counsel / formation signatures / IRS  
- Donor calls  
- Banking  

Prompt: `Prepare everything in-repo for [step]; give me the shortest manual checklist.`

---

*Playbook version: 0.2.1 — mission & presence first; site in docs/.*
