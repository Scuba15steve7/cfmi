# Federal Election Transparency Package

**Status:** Design memo · constitutional floor for *federal* elections (not a scored bill)  
**Domain:** Congressional / presidential-election administration transparency, custody, citizenship verification  
**Slug:** `federal-election-transparency-package`  
**Companion model outline:** [Federal Election Transparency and Citizenship Verification Standards Act](../../model-legislation/federal-election-transparency-and-audit-standards-act.md)  
**Parent brief:** [election-administration-integrity.md](election-administration-integrity.md)  
**Last updated:** 2026-08-02

Educational research only—not legal advice, voting instructions, or counsel to any person.

**AI constraint note:** Obey [ops/anti-narrative-capture.md](../../ops/anti-narrative-capture.md). No unverified fraud rates, stolen-election claims, or “everything fine” slogans. Mechanism and threat-model only.

---

## Goal (founder brief)

Federal law that closes **mechanism gaps** so federal elections have full transparency and security—without state-level holes that create doubt—on a **constitutional path**: Elections Clause authority for congressional elections; careful treatment of presidential electors; **no commandeering** of states for state/local offices. Secure + transparent without subtle holes. Reduce doubt about outcomes by making process auditable—not by narrative.

Distinguish two layers:

| Layer | Question answered | SAVE-like? |
|-------|-------------------|------------|
| **Citizenship verification** | Are federal registrants eligible citizens under published pathways? | Yes (core SAVE debate) |
| **Transparency / audit package** | Can the public verify custody, list quality, curing, observers, and what audits measured? | Broader; often missing even if citizenship rules pass |

---

## Constitutional hook (plain language)

### What Congress may prescribe

- **Congressional elections (House and Senate).** Article I, Section 4 (Elections Clause): states prescribe times, places, and manner of holding elections for Senators and Representatives; **Congress may at any time make or alter such regulations** (except places of choosing Senators). This is the cleanest hook for uniform *federal-election* transparency, custody, observer, data, and registration-verification rules that apply when those offices are on the ballot.
- **Presidential electors.** Article II and the Twelfth Amendment allocate electors to states; Congress has roles in timing and counting. Federal floor rules that attach to *federal* ballots and *federal* registration for presidential contests should be drafted tightly, with severability, and should not purport to run state elections for state offices. Treat presidential scope as **careful extension**, not as automatic identity with the Elections Clause for Congress.
- **Citizenship for federal voting.** Congress may condition *federal* voter registration on citizenship verification pathways consistent with existing citizenship requirements for federal elections (NVRA / related). That is distinct from rewriting state constitutions for state offices.

### What must remain state-run (no commandeering)

- States continue to **administer** elections: staffing, polling places, equipment procurement, canvass boards under state structure.
- Congress may set a **minimum transparency and verification floor for federal contests**; it may not order state legislatures or executives to rewrite state/local election law for state offices ([Printz](https://supreme.justia.com/cases/federal/us/521/898/) / anti-commandeering doctrine—Charter competitive federalism).
- **Strict non-preemption of stronger state protections** where compatible: if a state already publishes more data, stronger observer rights, or tighter custody for federal contests, federal law is a floor, not a ceiling that weakens those protections.
- **No federal takeover of state races.** Dual-ballot or dual-registration designs must be allowed: states may keep separate rules for state/local offices so long as federal contests meet the floor. Prefer “when a federal office is on the ballot, these federal-election rules apply to that contest and its federal registrants” over nationalizing secretary-of-state offices.

### One-sentence constitutional claim

Congress may prescribe manner/transparency/verification rules for **federal** elections under the Elections Clause (and carefully for presidential contests), while states keep administration of their own offices and retain room to exceed the federal floor—without commandeering state machinery for purely state races.

---

## Threat models & gaps (mechanism, not slogans)

Each row is a **residual risk surface**—not a claim that outcomes were stolen.

| Threat / gap | Mechanism | Why doubt persists if unaddressed | What “secure” messaging often skips |
|--------------|-----------|-----------------------------------|-------------------------------------|
| **Registration / list accuracy** | Deaths, moves, duplicates, inactive voters; NVRA notice/wait rules; incomplete NCOA / interstate match ([GAO-19-485](https://www.gao.gov/products/gao-19-485)) | Public sees outdated rolls without published error metrics | “We clean rolls” ≠ published match rates, appeals, false-positive rates |
| **Citizenship attestation gaps** | Penalty-of-perjury checkbox without documentary or database verification at registration | Citizenship is required in law but under-verified in process | Conflating *legal bar* with *operational verification* |
| **Mail chain-of-custody** | Application → outbound → USPS/drop box → intake → tabulation; seals/logs vary by state | Breaks or opacity at any hop fuel narrative without answerable logs | Barcodes alone ≠ published custody summaries |
| **Ballot curing opacity** | Signature reject → notice → cure window; criteria and rates unevenly published | Selective curing stories fill the vacuum | Cure exists ≠ public reject/cure rates by jurisdiction |
| **Drop-box custody** | Placement, surveillance, collection schedules, bipartisan collection—state-variable | Unlogged collections are an integrity *and* access controversy | “Drop boxes are fine” without custody SOP publication |
| **Observer access** | Statute may allow observers but distance, credentials, or “interference” rules gut meaningful view | “Bipartisan observers present” while unable to see material steps | Presence ≠ meaningful access under published rules |
| **Audit scope (RLA ≠ eligibility)** | Risk-limiting audits test tabulation consistency with paper; they do not verify citizenship or full mail custody | Quoting RLA as proof of “eligibility secure” is scope abuse | Hand tally ≠ citizenship check ([parent brief](election-administration-integrity.md)) |
| **Public data lag** | Metrics delayed past certification or released as PDFs only | Researchers and voters cannot reconcile claims to data | “Transparency” without machine-readable, timely release |
| **Delayed certification opacity** | Extensions, disputes, or administrative delay without published milestone clocks | Creates space for outcome doubt even when counts are lawful | Process delay without public milestone logs |

---

## Least-coercive instrument ladder

Prefer earlier rungs before later ones. Each rung should have published objective criteria.

### 1. Mandatory public machine-readable reporting (floor zero)

For federal-election jurisdictions, publish on a fixed calendar (e.g., 7 / 30 / 90 days post-election and quarterly for lists):

- List metrics: active/inactive, notices sent, removals by reason, interstate match hits/appeals, death-file hits  
- Mail/absentee: issued, returned, rejected (by reason), cured, pending  
- Custody log *summaries*: collection events, seal breaks, chain handoffs (counts and exception rates—not necessarily every personal identifier)  
- Observer: credentialed requests granted/denied and denial reasons  

**Charter fit:** Radical transparency; least coercive; no new discretion.

### 2. Uniform federal-election audit & transparency floor

- Pre-commit audit **scope** in writing (what is measured / not measured).  
- Require paper or voter-verifiable record for federal contests where feasible under existing HAVA trajectories.  
- Publish RLA (or equivalent) results with scope legend: “tabulation consistency—not eligibility.”  
- Certification milestone clock: public status when milestones slip.  

### 3. Citizenship verification for **federal** registration (least-false-positive design)

- **Documentary pathway** (passport, birth certificate + photo ID, REAL ID indicating citizenship, military records as listed)—SAVE-like.  
- **Alternative pathways:** sworn evidence + database corroboration (SSA, DHS SAVE system access where authorized, state vital records) with published match criteria.  
- **Provisional / fail-safe for citizens:** if verification pending, cast provisional or conditioned federal ballot with cure window; fee waivers for vital records; name-change procedures.  
- **Do not chill the failsafe** with criminal exposure for good-faith acceptance of alternative evidence under published criteria—penalties should target knowing falsification and willful refusal to apply objective rules, not honest processing of hard cases.

### 4. SAVE Act–style elements — keep / modify / reject

Evaluated against Charter + passability (see also parent [SAVE section](election-administration-integrity.md#save-act--accurate-description-both-sides)). Living text: [H.R. 22](https://www.congress.gov/bill/119th-congress/house-bill/22) · [CRS IF12902](https://www.congress.gov/crs_external_products/IF/PDF/IF12902/IF12902.3.pdf).

| Element | CFMI posture | Rationale |
|---------|--------------|-----------|
| Documentary proof of citizenship at **federal** registration | **Keep (modified)** | Closes attestation gap; Elections Clause / federal-election scope |
| Listed acceptable documents | **Keep** with periodic update process | Objective criteria beat case-by-case whim |
| Alternate evidence process for those without listed docs | **Keep and strengthen** | Passability + false-positive control; publish acceptance rates |
| Database access for citizenship corroboration | **Keep with privacy/minimization rules** | Least-coercive complement to paper docs |
| Ongoing removal of noncitizens from federal rolls | **Keep with due process** | Notice, appeal, published criteria; no silent purges |
| Private right of action / official penalties | **Modify heavily** | Broad private ROA and chill on failsafes → opaque risk and capture; prefer state AG / limited standing + objective enforcement |
| Soft failsafe + harsh official criminal exposure | **Reject as packaged** | Creates security theater: rule exists, administrators fear using it |
| Nationalizing state/local election rules | **Reject** | Commandeering / federalism Charter violation |
| Treating RLA as citizenship proof | **Reject** (not in SAVE text, but in messaging) | Scope abuse |

### 5. What NOT to do

- Vague “security” waivers or “as the chief election official deems appropriate” escapes from data/custody floors.  
- Partisan election boards with **opaque discretion** and unpublished criteria.  
- Federal takeover of state races or ERIC monopoly mandates (require *interoperable* list coordination; do not entrench one vendor/consortium).  
- Unverified national fraud percentages as the justification finding.  
- Anti-scrutiny rules that treat published metrics or observer access as “disinformation.”

---

## Model package outline

**Title:** Federal Election Transparency and Citizenship Verification Standards Act  

Full section skeleton and impact statements: [model-legislation/federal-election-transparency-and-audit-standards-act.md](../../model-legislation/federal-election-transparency-and-audit-standards-act.md).

Sections (summary):

1. Definitions  
2. Federal election scope (congressional; careful presidential; dual-system for state offices)  
3. Public machine-readable data mandates  
4. Chain-of-custody & drop-box minimums for federal ballots  
5. Observer rights (meaningful access + non-interference rules)  
6. List maintenance coordination without ERIC monopoly  
7. Citizenship verification pathways (documentary + alternative + provisional fail-safe)  
8. Audits covering tabulation *and* eligibility sampling where feasible  
9. Enforcement: limited private right of action **or** state AG / DOJ civil; anti-chill for good-faith failsafe  
10. Severability; strict non-preemption of stronger compatible state rules; non-commandeering for state offices  

---

## Both sides + CFMI response

### Steelman opposition

- **Suppression / false positives:** Documentary rules can block citizens without ready passport/birth certificate, name-change mismatches, or mail/online registrants ([Brennan opposition](https://www.brennancenter.org/our-work/research-reports/brennan-center-letter-congress-opposing-save-act); [document-access advocacy](https://www.brennancenter.org/our-work/analysis-opinion/213-million-american-citizens-voting-age-dont-have-ready-access)).  
- **Unfunded mandates:** Data systems, custody logging, and verification staff cost money; states will resist bare mandates.  
- **Federalism:** States run elections; blunt federal rules can ignore high-performing states and paper over weak ones with compliance theater.  
- **Prevalence:** Layered safeguards already exist; large-scale outcome-changing noncitizen voting is not established as a single national rate—so heavy verification is disproportionate.

### Steelman support

- **Uniform federal floor:** Citizenship is already required; attestation-without-verification is an enforcement gap ([Heritage Action](https://heritageaction.com/blog/myth-vs-fact-the-safeguard-american-voter-eligibility-act-h-r-22-s-128)).  
- **Doubt reduction:** Published metrics, custody summaries, and scoped audits answer skepticism better than slogans.  
- **List difficulty is real:** GAO documents incomplete sources—not proof of conspiracy, but proof that “rolls are fine” is not self-evident.  
- **Mail shifts surfaces:** Even [CISA mail-voting risk materials](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf) discuss residual registration and infrastructure risks alongside controls.

### CFMI response

1. **Accept** access and false-positive concerns as design constraints—not as reasons to refuse any verification.  
2. **Accept** need for auditable eligibility and custody for federal contests—not as a license for outcome conspiracies.  
3. **Path:** transparency floor first; citizenship pathways with strong failsafe second; limited enforcement that does not chill the failsafe; no commandeering of state offices.  
4. **Reject** “everything fine” and “everything stolen”; reject vague security waivers and partisan opaque boards.  
5. **Magnitude:** national noncitizen voting rates remain **not established** as a single CFMI number; design still addresses verification and transparency gaps.

---

## Hidden barriers (looks compliant, resists scrutiny)

| Surface compliance | How scrutiny is resisted |
|--------------------|---------------------------|
| “Observers allowed” | Distances, credential caps, or “interference” rules that prevent seeing material steps |
| “Audits completed” | Scope limited to tabulation; eligibility and custody never sampled; results as non-machine-readable PDFs |
| “Rolls maintained under NVRA” | Activity counts (notices sent) without accuracy KPIs, appeal outcomes, or match error rates |
| “Cure process available” | Opaque reject criteria; no public reject/cure rates by reason |
| “Chain of custody” | Forms exist but exception logs unpublished; drop-box collection unlogged |
| “Alternative evidence under SAVE-style bill” | Failsafe chilled by official liability—paper compliance, practical documentary-only |
| “Secure election” press line | Soft definition: cyber + canvassing sold as total eligibility proof |

---

## Top 5 concrete reforms (priority order)

1. **Machine-readable public metrics** for federal-election list quality, mail reject/cure rates, and custody-exception summaries—on a fixed calendar.  
2. **Pre-committed audit scopes** + public milestone clocks through certification; RLA results labeled as tabulation-only unless eligibility sampling is included.  
3. **Meaningful observer access rules** for federal contests (what may be viewed; denial reasons published).  
4. **Citizenship verification for federal registration** with documentary + database + sworn alternative pathways and a **usable** provisional/fail-safe (anti-chill).  
5. **Interoperable interstate list coordination** with due-process removals—no ERIC (or any single consortium) monopoly mandate.

---

## SAVE Act fit (summary)

| Question | Answer |
|----------|--------|
| Is SAVE the whole package? | **No.** It is mainly citizenship-at-registration + roll cleanup. Transparency/custody/observer/audit-scope gaps remain. |
| Does CFMI keep the core? | **Yes, modified** for federal elections with stronger failsafe and less chilling enforcement. |
| What to add around SAVE? | Public data floor, custody summaries, observer rights, scoped audits, non-commandeering for state offices. |
| Passability hinge | Access advocates need workable alternatives; integrity advocates need measurable verification—not slogans. |

---

## Sources (key)

- [H.R. 22 — SAVE Act](https://www.congress.gov/bill/119th-congress/house-bill/22) · [text](https://www.congress.gov/bill/119th-congress/house-bill/22/text)  
- [CRS IF12902](https://www.congress.gov/crs_external_products/IF/PDF/IF12902/IF12902.3.pdf)  
- [GAO-19-485](https://www.gao.gov/products/gao-19-485) · [GAO-05-478](https://www.gao.gov/assets/gao-05-478.pdf)  
- [CISA mail-voting risk assessment](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf)  
- [Heritage Action — SAVE myth/fact](https://heritageaction.com/blog/myth-vs-fact-the-safeguard-american-voter-eligibility-act-h-r-22-s-128)  
- [Brennan — oppose SAVE](https://www.brennancenter.org/our-work/research-reports/brennan-center-letter-congress-opposing-save-act)  
- U.S. Const. art. I, § 4; art. II; Amend. XII  

---

## Improve this package

- [docs/feedback.html](../../docs/feedback.html) · [counterevidence issue](https://github.com/scuba15steve7/cfmi/issues/new?template=counterevidence.yml)  
- Invite: constitutional critiques of presidential scope drafting; state metric schemas already in use; cost estimates for data floor; steelman unfunded-mandate fixes (conditional grants vs bare mandate).
