# Civic Action Pack

**Status:** Product specification for CFMI’s public AI dig  
**Implements:** [CHARTER.md](../CHARTER.md), [METHODOLOGY.md](../METHODOLOGY.md)  
**Architecture:** [ai-investigation-architecture.md](ai-investigation-architecture.md)  
**Narrative discipline:** [anti-narrative-capture.md](anti-narrative-capture.md)  
**Viral / conspiracy leads:** [claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md)  
**Scale pattern mining:** [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md)  
**Sources:** [external-sources-and-grokipedia.md](external-sources-and-grokipedia.md)

Educational research only—not legal advice, voting instructions, or counsel to any person. **CFMI does not claim IRS tax-exempt status.**

---

## 1. What the tool is

CFMI is an **AI tool** that digs into legislation or public topics to help people:

1. **Understand** the operative issue (mechanisms, not slogans);
2. **Find** constitutional / free-market / people-over-bureaucracy solutions; and
3. **Expose** what looks off—**suspicion flags** and disclosed conflicts from **public records**, labeled by proof level—not private detective work or unverified bribery claims.

Free markets are a primary instrument against artificial barriers and cronyism. Charter principles bind every dig. AI is a disclosed aid under published rules—never an authority. Absolute proof of corruption is **not** required to publish a suspicion flag (METHODOLOGY §7.5).

---

## 2. What a Civic Action Pack produces

When a dig is accepted for publication (human editor required), the pack includes:

| Component | Purpose |
|-----------|---------|
| **Diagnosis** | Plain-language statement of the operative barrier, power shift (bureaucracy/privilege vs. accountable people), and who pays / who is blocked |
| **Charter score** | Rubric scores and Hard Flags against [CHARTER.md](../CHARTER.md) / [METHODOLOGY.md](../METHODOLOGY.md) |
| **Both sides** | Steelmanned arguments for reform and for the status quo, with linked evidence—not vibe or caucus scripts ([anti-narrative-capture.md](anti-narrative-capture.md)) |
| **Influence leads** | Disclosed lobbying / money trails from **public filings** (LDA, OpenSecrets-style aggregators, FEC where relevant)—paired with Hard Flags; no doxxing, no unverified motive claims. When the pack claims influence or corruption surfaces, include a **conflict graph / pattern table** from [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) |
| **Suspicion flags** *(mandatory)* | Dual **Flag + Proof-status** table so citizens can scrutinize patterns even when corruption / quid pro quo is **not established**. Labels: **Suspicion flag** · **Supported conflict of interest (disclosed)** · **Corruption / quid pro quo** (rare). See §2.1 and METHODOLOGY §7.5 |
| **Fix language** | Open alignment / amendment / least-coercive rollback language that does not create new rents, barriers, or opaque discretion |
| **Legislator letter** | Sample constituent letter (educational template)—facts, Charter conflicts, asked fix; user adapts and sends |
| **Social blurb** | Short shareable summary with links to the pack and sources—not a whip or GOTV script |
| **Origin claim** *(optional)* | When the dig started from a viral/influencer/conspiracy-framed lead: short quote + link labeled as **lead, not CFMI finding**, plus per-sub-claim triage grades—see [claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md) |

Optional companions when the dig warrants them: issue brief, influence memo, sample act outline for bipartisan comment.

### 2.1 Suspicion flags section (template — mandatory)

Every published Civic Action Pack (and influence dig companion) must include a **Suspicion flags** section—even when no corruption chain exists. Do not omit the section or replace it with a bare “not established.”

```markdown
## Suspicion flags

| Flag (what looks off) | Public label | Proof-status | Sources |
|-----------------------|--------------|--------------|---------|
| … | Suspicion flag | strong / moderate / weak *as suspicion*; quid pro quo: not established | URL / filing |
| … | Supported conflict of interest (disclosed) | Filings support disclosed tie; quid pro quo: not established \| supported | URL / filing |

**Note:** Suspicion flags are publishable by design. “Not established” applies to corruption / quid pro quo unless a public-record chain supports it—it does not erase the Flag column.
```

---

## 3. How a dig runs

Bounded hierarchical investigation ([ai-investigation-architecture.md](ai-investigation-architecture.md)):

1. **Orchestrator** frames the bill/topic, power-shift test, and depth caps.  
2. **Specialist lanes** (in parallel as needed): text/mechanism, root cause, influence/money from public records, counters, safeguards, fix language.  
3. **Source discipline** — primary filings and statutes first; encyclopedias and secondary explainers (including Grokipedia when used) are **non-authoritative** context under [external-sources-and-grokipedia.md](external-sources-and-grokipedia.md).  
4. **Anti-narrative filter** — high-consensus and viral claims are hypotheses to test ([anti-narrative-capture.md](anti-narrative-capture.md)).  
5. **Viral claim triage** (when intake is conspiracy-framed or influencer-driven) — falsifiable sub-claims → records dig → grades; dual steelman; no rumor laundering and no reflexive dismissal ([claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md)).  
6. **Deep public-records layer** — after stated reasons, attempt LDA/OpenSecrets, FEC, disclosed IE/opaque vehicles, 990 funders, revolving door, STOCK Act/PFDs where findable ([METHODOLOGY.md](../METHODOLOGY.md) §7.6 · architecture §3.3a).  
6a. **Scale pattern mining** — required when the pack will publish influence / special-interest / corruption-surface claims: map-reduce cross-dataset edges into a conflict graph / pattern table ([ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) · METHODOLOGY §7.7 · playbook **I6**).  
7. **Human editor** accepts, revises, or rejects before anything is a public CFMI product.

Public intake: GitHub Issues — suggest a review, request an action pack dig, or submit counterevidence (see [docs/tool.html](../docs/tool.html)).

### 3.1 Pre-publish checklist (influence claims)

Before any Civic Action Pack (or companion) publishes influence, special-interest, or corruption-surface claims:

- [ ] Stated reasons documented for each key blocker / advocacy side  
- [ ] **Deep records layer completed before publishing influence claims** (METHODOLOGY §7.6)  
- [ ] **Scale pattern mine completed** when influence/corruption-surface claims appear (METHODOLOGY §7.7 · [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md)) — conflict graph / pattern table with Flag + Proof-status  
- [ ] Output table present: Actor | Stated reason | Disclosed $ / org ties | **Flag** | **Proof-status**  
- [ ] **Suspicion flags** section present (§2.1)—even when quid pro quo is not established  
- [ ] Layers separated with public labels: Suspicion flag · Supported conflict (disclosed) · Corruption/quid pro quo (rare; default not established); flags not upgraded to corruption without a chain  
- [ ] Dual output used—flags not buried under a single “not established” close  
- [ ] Aggregate/noisy donor data labeled as such—no vote-buying inference from industry totals alone; false-positive note present  
- [ ] Human editor sign-off

---

## 4. Anti-capture (non-negotiable)

- No donor, suggester, or affiliate may purchase scores, silence, Hard Flag removal, or preferred fix language.  
- Asks for subsidies, entry barriers, opaque discretion, or named private privileges are **declined and logged**.  
- Interest disclosure is mandatory on public suggestions (Methodology).  
- Influence leads never become private investigation, harassment, or conspiracy fiction.  
- Viral/conspiracy intake is a **lead** only—publish Suspicion flags + Proof-status and graded public-record facts; do not launder unverified theories as proven corruption ([claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md)).  
- Open bipartisan comment never means adding rents to buy support.

Full rules: Charter § Funding and Anti-Capture; Methodology stakeholder rules.

---

## 5. 501(c)(3) education vs. lobbying (note)

**Default formation path** is a **501(c)(3)** educational/research model ([formation-checklist.md](formation-checklist.md))—**attorney-review required; no tax status claimed.**

| In lane (education / research) | Out of lane without counsel / (c)(4) |
|--------------------------------|--------------------------------------|
| Scoring bills and topics under published rubrics | Directing people how to vote |
| Publishing conflicts, both sides, and open fix language | Grassroots lobbying campaigns as the lead product |
| Sample legislator letters and social blurbs as **educational templates** | Coordinated contact campaigns that become substantial lobbying |
| Circulating sample acts for bipartisan **comment** | Whip counts, PAC activity, or candidate support |
| Disclosed influence trails from public filings | Private investigation or unverified accusation |

Until counsel advises otherwise, treat Civic Action Packs as **educational research outputs**, not lobbying directives. If vote-urging or substantial lobbying becomes a program, revisit entity design with counsel (possible (c)(4) companion)—do not invent tax status in public copy.

---

## 6. Related artifacts

| Artifact | Role |
|----------|------|
| [ai-investigation-architecture.md](ai-investigation-architecture.md) | How digs are orchestrated |
| [anti-narrative-capture.md](anti-narrative-capture.md) | Resist vibe capture from either side |
| [claim-triage-from-viral-sources.md](claim-triage-from-viral-sources.md) | Viral/conspiracy claims as leads; records grades; optional Origin claim field |
| [ai-scale-pattern-mining.md](ai-scale-pattern-mining.md) | Cross-dataset map-reduce; conflict graph / pattern table; required on influence packs |
| [external-sources-and-grokipedia.md](external-sources-and-grokipedia.md) | Source hierarchy; Grokipedia as non-API secondary |
| [suggestion-ranking.md](suggestion-ranking.md) | How public suggestions are screened |
| [docs/tool.html](../docs/tool.html) | Public Tool page |
| Issue templates | `suggest-review.yml`, `request-action-pack.yml`, `counterevidence.yml` |

---

*People over bureaucracy. Free markets as instrument. Methods public. AI never the authority.*
