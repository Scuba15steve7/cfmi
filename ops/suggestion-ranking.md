# Suggestion ranking process

How CFMI turns public intake into a ranked research queue—and routes counterevidence into issue briefs. Implements [CHARTER.md](../CHARTER.md) and [METHODOLOGY.md](../METHODOLOGY.md) §1 (problem ranking) and §4.6 (issue briefs / steelman). Educational research only—not legal advice or voting instructions.

**Intake channels:** GitHub Issues with:

| Template | Labels | Purpose |
|----------|--------|---------|
| [Suggest a review](../.github/ISSUE_TEMPLATE/suggest-review.yml) | `suggestion` | New bill, regulation, or topic |
| [Suggest a correction / counterargument](../.github/ISSUE_TEMPLATE/counterevidence.yml) | `counterevidence`, `suggestion` | Evidence or steelman to improve a brief/review |

No paid intake services.

**Public artifacts:**

| Artifact | Role |
|----------|------|
| GitHub Issues (label `suggestion`) | Raw public suggestions (reviews + counterevidence) |
| GitHub Issues (label `counterevidence`) | Brief-improvement / both-sides feedback |
| [`ai-reviews/suggestions/QUEUE.md`](../ai-reviews/suggestions/QUEUE.md) | Status table: Pending / Ranked / Declined (review topics) |
| Issue briefs under [`ai-reviews/issues/`](../ai-reviews/issues/) | Destination for accepted counterevidence |
| [`ai-reviews/suggestions/`](../ai-reviews/suggestions/) | Optional dated ranking notes when a batch is scored |

---

## 1. Flow

### 1a. New review topics (`suggest-review.yml`)

1. **Suggest** — Anyone opens an issue with the review template. Interest disclosure is required.
2. **Screen** — AI (disclosed model/provider when known) plus a human editor check completeness, Charter fit, and disqualifiers.
3. **Rank** — Survivors are scored with Methodology §1 weights (below). Results are written to `QUEUE.md` (and optionally a note under `ai-reviews/suggestions/`).
4. **Queue** — Ranked items may become issue briefs, bill reviews, or sample-act tracks when capacity allows. Declines publish a short reason.

### 1b. Counterevidence / brief improvement (`counterevidence.yml`)

First-class intake—not a side channel.

1. **Submit** — Issue slug, evidence link, which side (reform / status-quo steelman / affected people / correction), what CFMI should change, interest disclosure.
2. **Screen** — Completeness (real public URL, identifiable slug), disclosure, and Charter disqualifiers (rent asks still declined).
3. **Classify** — Map to the brief’s Supporting reform, Counterarguments, or factual-correction path. Affected-people sources must be labeled clearly.
4. **Integrate or decline** — Accepted items update the brief (and CFMI response / passability section when material). Declines get a short public reason on the issue. These do **not** require a Methodology §1 composite rank unless they also propose a new review topic.
5. **Comment** — Link the updated brief (or decline reason) on the GitHub issue.

Party affiliation, donor status, and volume of comments do **not** change rank or acceptance. Charter fit, evidence quality, and published weights do.

---

## 2. Intake screen (before ranking or brief update)

Reject or hold as **Declined** (with reason) when:

| Check | Fail condition |
|-------|----------------|
| **Completeness** | No identifiable bill/regulation/topic/slug, or no usable public pointer |
| **Interest disclosure** | Missing or evasive disclosure (Methodology §5) |
| **Rent ask** | Primary goal is a subsidy, barrier, privilege, or named private benefit |
| **Commandeering** | Ask requires federal commandeering of states |
| **Opacity** | Ask depends on open-ended agency discretion without objective criteria |
| **Publication** | Requester demands private/non-public handling of substantive work |
| **Off-mission** | No plausible link to free markets, constitutional limits, or anti-capture |
| **Counterevidence URL** | Link is missing, broken, or not a public source (for `counterevidence` issues) |

Incomplete but salvageable issues may stay **Pending** with a request for clarification on the issue thread.

**Note:** A strong steelman *defense of current licensing or regulation* is on-mission when it improves the brief’s Counterarguments section. Declining that evidence as “pro-status-quo” is a process failure. Declining a request that CFMI *endorse a new barrier* is correct.

---

## 3. Ranking score (Methodology §1)

Score each screened suggestion **0–5** on each criterion, then apply weights. Higher composite = higher priority.

| Criterion | Weight | Question |
|-----------|--------|----------|
| **Constitutional stakes** | 25% | Does the status quo stretch enumerated powers, federalism, separation of powers, or property/contract protections? |
| **Market distortion** | 25% | How large and durable are artificial barriers, subsidies, or opaque discretion? |
| **Corruption / rent surface** | 20% | How easy is political allocation or capture relative to open competition? |
| **Tractability** | 15% | Can a least-coercive, rules-based fix or alignment language be drafted and audited? |
| **Spillover & precedent** | 10% | Would a good fix or sample act travel to other states or domains? |
| **Evidence quality** | 5% | Are harms documented with public data, not anecdotes alone? |

**Composite** = weighted average of the six scores (normalize each 0–5 contribution by its weight).

**Charter overlay (qualitative, published in the note):**

- Which Core Principles are implicated?
- Any Hard-Flag pattern from Methodology §2 (discretion, rents, barriers) even before a full bill review?
- Least-coercive path available? If not, say so.

AI produces a draft score sheet; a named human editor accepts, revises, or rejects before `QUEUE.md` moves to **Ranked** or **Declined**.

---

## 4. Status definitions

| Status | Meaning |
|--------|---------|
| **Pending** | Received; awaiting screen or clarification |
| **Ranked** | Screened and scored; composite and short rationale published |
| **Declined** | Screened out; public reason required (disclosure fail, rent ask, off-mission, etc.) |

Optional follow-on labels on the GitHub issue (e.g. `ranked`, `declined`) may mirror the queue when useful. The queue table is the source of truth for site-facing status.

---

## 5. Publishing a ranking batch

When ranking one or more suggestions:

1. Open or update rows in [`QUEUE.md`](../ai-reviews/suggestions/QUEUE.md).
2. Optionally add `ai-reviews/suggestions/YYYY-MM-DD-batch.md` with per-criterion scores, Charter notes, model/provider, rubric version (`METHODOLOGY` problem-ranking), date, and human editor.
3. Comment on the GitHub issue with a link to the queue row (and batch note if any).
4. Do **not** treat donor requests or private DMs as a parallel queue—redirect to the public template.

---

## 6. What ranking is not

- Not a promise that CFMI will draft a bill or publish a full review on a deadline.
- Not endorsement of the suggestion’s politics or preferred outcome.
- Not legal advice, voting instructions, or counsel to any person.
- Not pay-for-play: support never buys rank or silence.

---

## 7. Operator prompts (copy-paste)

**Review topics:**

```
Rank open CFMI suggestions labeled "suggestion" that are still Pending in
ai-reviews/suggestions/QUEUE.md (and any new GitHub issues using
.github/ISSUE_TEMPLATE/suggest-review.yml). Skip pure counterevidence issues
(label counterevidence)—handle those with the brief-improvement prompt.

Follow ops/suggestion-ranking.md:
1) Screen for disclosure, completeness, and Methodology disqualifiers.
2) Score survivors with Methodology §1 weights + Charter overlay.
3) Update QUEUE.md (Pending / Ranked / Declined with reason).
4) Optionally write ai-reviews/suggestions/YYYY-MM-DD-batch.md.
5) Comment on each issue with the result link.

Disclose model/provider if known. Human editor must accept before publishing Ranked/Declined.
Do not commit or push unless I ask.
```

**Counterevidence / brief improvement:**

```
Process open GitHub issues labeled "counterevidence" (template
.github/ISSUE_TEMPLATE/counterevidence.yml).

Follow ops/suggestion-ranking.md §1b and METHODOLOGY.md §4.6:
1) Screen disclosure, public URL, and identifiable issue slug.
2) Classify: Supporting reform / Counterarguments / Affected people / Correction.
3) For accepted items, update the matching ai-reviews/issues/*.md Voices &
   evidence tables; revise CFMI response or passability section if material.
4) Decline rent asks and fake/unverifiable links with a public reason.
5) Comment on each issue with the brief link or decline reason.

Steelman counters are required for adoption-ready briefs—do not dismiss
pro-status-quo evidence that improves the Counterarguments section.
Disclose model/provider if known. Human editor must accept before merging.
Do not commit or push unless I ask.
```
