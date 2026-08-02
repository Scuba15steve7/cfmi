# CFMI Prompt Playbook

**Operating rule:** Advance CFMI by pasting prompts into Cursor. The agent updates the repository.

**Current phase:** Mission + online presence + formation readiness (501(c)(3) educational/research default).  
**Product model:** Score legislation → publish conflicts → open fix language → sample acts for bipartisan comment.

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
Write a short public mission statement (2–4 sentences) and a one-line tagline for CFMI, consistent with CHARTER.md.
Lead with: research-funded AI; score bills; publish conflicts with free markets and constitutional limits;
open bipartisan fix language and sample bills; minimize unintended consequences; Charter binds.
Put them in website/index.md, website/about.md, README.md, pitch/one-pager.md, and docs/*.html.
Do not change CHARTER.md principles. Do not claim tax status.
```

### W1 — Deployable site
```
Ensure docs/ is a minimal, professional static site for GitHub Pages (folder /docs). Mission-first homepage:
brand, mission (score / publish conflicts / fix language / sample acts), principles link, about, charter,
how to support—no flagship bill as the hero. Keep website/*.md conceptually aligned. Follow my frontend
design rules. Keep it simple and donor-credible. Include docs/.nojekyll.
```

### P1 — Pitch = mission org
```
Rewrite pitch/one-pager.md as a mission-and-method nonprofit pitch for research-funded AI legislative analysis.
Proof at $0 = charter, methodology, site, formation checklist, transparency rules. Lead with score / publish
conflicts / fix language / bipartisan sample acts—not a single flagship bill.
```

### R1 — README face
```
Rewrite README.md so the repo face is: what CFMI is, mission, principles, status (bootstrap), links to
charter/site/pitch/formation-checklist, and how the project is built in Cursor. Move model bills and AI
reviews to a clearly secondary “Work product (later / samples)” section.
```

### F1 — Formation checklist
```
Create or refresh ops/formation-checklist.md: default 501(c)(3) for this educational/research model;
note that heavy vote-lobbying may need a future (c)(4); Utah considerations if relevant; prompts to draft
bylaws/conflict-of-interest aligned to CHARTER.md. Mark attorney-review required throughout.
Do not claim we have tax status.
```

### D1 — Commit
```
Create a git commit for the current CFMI bootstrap (mission + presence + formation checklist). Do not push.
```

### G1 — Go live prep
```
Confirm ops/go-live.md has the exact manual clicks: public repo → push main → Settings → Pages → Deploy from
branch main / folder /docs. Note custom .org is usually not free; use username.github.io/repo first.
Do not push or commit unless I ask.
```

---

## Phase 2 — Scoring & sample acts (after presence)

Only after Phase 1 feels solid. Investigation design: [`ops/ai-investigation-architecture.md`](ai-investigation-architecture.md) (bounded hierarchy—orchestrator + six specialist lanes + depth-limited digs), [`ops/anti-narrative-capture.md`](anti-narrative-capture.md) (consensus claim tester), [`ops/claim-triage-from-viral-sources.md`](claim-triage-from-viral-sources.md) (viral/conspiracy claim triage), and [`ops/ai-scale-pattern-mining.md`](ai-scale-pattern-mining.md) (scale pattern mining / conflict graphs).

### L1 — Start scoring cadence
```
Set up ai-reviews/ as the first product lane: index README, refresh template for score + publish conflicts +
open fix/alignment language, and review one real federal bill I paste or you propose. Mission and site stay
primary in website/ and pitch/.
```

### L2 — First sample act for bipartisan comment (when ready)
```
Draft [licensing / housing / other] sample act to CFMI standards for open bipartisan review and comment.
Keep website messaging mission-first; link the bill as work product, not the hero.
```

### I1 — Run bounded investigation (orchestrator)
```
Run a CFMI bounded hierarchical investigation on [BILL ID or ISSUE SLUG] per
ops/ai-investigation-architecture.md. Use the §7.1 orchestrator prompt. Spawn the six fixed
specialist lanes (Task/sub-agents); depth-limited digs only on Hard Flags (max depth 2 unless I approve 3).
Synthesize a publish package; do not publish—hand off for human edit. Obey CHARTER.md and METHODOLOGY.md.
```

### I2 — Specialist lane (paste per sub-agent)
```
Use the specialist template in ops/ai-investigation-architecture.md §7.2 for lane [N: NAME] on
[narrow scope]. Return the structured findings block only. No further spawning unless depth dig was requested.
```

### I3 — Influence companion after Hard Flags
```
Parent review has Hard Flags on [bill]. Draft an influence memo per METHODOLOGY §7 and
ai-reviews/influence-template.md using only public LDA/OpenSecrets/sponsors. Pair with open fix language.
Mark gaps "not established from public filings in this pass." No motive claims.
```

### I4 — Consensus claim stress-test
```
Run the CFMI Consensus claim tester on this high-consensus claim (institutional or viral):

"[PASTE CLAIM VERBATIM — e.g. 'Mail voting is secure' or 'The election was stolen']"

Scope: [jurisdiction / process facet — e.g. federal registration / State X mail custody]

Obey ops/anti-narrative-capture.md and ops/ai-investigation-architecture.md §3.2a / §9.
Use the copy-paste prompt in anti-narrative-capture.md §6.

Hard bans: no vibe-based reassurance; no vibe-based alarm; no unverified fraud rates or outcome
conspiracies as fact; training-data prevalence ≠ truth.
Require: definition of secure/unsafe; threat model; operative mechanisms; what audits measure vs don't;
error vs fraud; state variation where relevant.
Return the structured FOR/AGAINST block only. Escalate digs only on disclosed messaging funding,
audit scope gaps, statute vs practice, or legal standards for challenging rolls.
Mark gaps "not established from public sources in this pass." Do not publish—hand off for human edit.
Worked example domain: ai-reviews/issues/election-administration-integrity.md
```

### I5 — Triage viral claim
```
Run CFMI viral / conspiracy claim triage on this origin claim (quote verbatim):

"[PASTE CLAIM — e.g. influencer or viral assertion about SAVE Act stall / election process]"

Source / date: [URL or description]
Scope: [jurisdiction / bill / process facet]

Obey ops/claim-triage-from-viral-sources.md and METHODOLOGY §7.5–§7.6.
Use the copy-paste prompt in claim-triage-from-viral-sources.md §8.

Hard bans: do not launder rumor into CFMI voice; do not dismiss as false merely because it is
labeled a conspiracy theory; no quid pro quo without a public-record chain.
Require: falsifiable sub-claims; steelman of mainstream denial AND steelman of the claim;
deep public-records dig; grade each sub-claim Supported / Partially supported / Not established /
Contradicted; what would need to be true; what records would prove it; what was checked;
FOIA/journalist handoffs when public records do not exist.
Return the structured triage block only. Optional Civic Action Pack field: Origin claim + grades.
Do not publish—hand off for human edit. Method sample (not an endorsement): claim-triage §7.
```

### I6 — Scale pattern mine
```
Run CFMI scale pattern mining on:

Target: [BILL ID / ISSUE / NAMED ACTORS]
Date window: [e.g. 2024–2026]
Pattern classes: [donor↔vote timing | advocacy overlaps | family/employer |
schedule priority inversion | bill-text clones | revolving door — all that apply]

Obey ops/ai-scale-pattern-mining.md and METHODOLOGY §7.5–§7.7.
Use the copy-paste prompt in ai-scale-pattern-mining.md §10.

Hard bans: never upgrade a Suspicion flag to corruption / quid pro quo without a
public-record chain; do not bury Flags under a single "not established"—use dual
Flag + Proof-status; no doxxing; news = leads only; mark paywalls / incomplete LDA /
opaque vehicles as gap + FOIA handoff; state false-positive risks.
Require: multi-agent map-reduce (or sole-agent shard simulation); structured edges
Actor A — Relation — Actor B — Source — Grade; conflict graph / pattern table with
public labels (Suspicion flag · Supported conflict disclosed · Corruption/quid pro quo);
layers (A)/(B)/(C)/(D) separated.
Required on SAVE-class digs and Civic Action Packs with influence claims.
Stub of checked vs next queries: ai-reviews/claim-triage-thune-save-act-deep.md Appendix A.
Do not publish—hand off for human edit.
```

Full older drafting prompts (B1–B4, C1–C3, etc.) remain valid in git history / ask the agent to restore them when Phase 2 starts. Prefer the Phase 1 prompts above until then.

---

## What still requires you offline

- GitHub account / login / creating the remote  
- Domain purchase (optional)  
- Counsel / formation signatures / IRS (see [formation-checklist.md](formation-checklist.md))  
- Donor calls  
- Banking  

Prompt: `Prepare everything in-repo for [step]; give me the shortest manual checklist.`

---

*Playbook version: 0.3.5 — suspicion flags publishable by design (Flag + Proof-status); mission locked to score/conflicts/fix/sample; formation default 501(c)(3); Phase 2 I1–I6.*
