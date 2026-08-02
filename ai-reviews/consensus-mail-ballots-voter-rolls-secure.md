# Consensus Claim Stress-Test (I4): Mail Ballots & Voter Rolls

**Status:** Published research product (human editor gate still applies for external reuse)  
**Playbook:** [`ops/prompt-playbook.md`](../ops/prompt-playbook.md) **I4**  
**Rules:** [`ops/anti-narrative-capture.md`](../ops/anti-narrative-capture.md) · [`ops/ai-investigation-architecture.md`](../ops/ai-investigation-architecture.md) §3.2a  
**Parent brief:** [`issues/election-administration-integrity.md`](issues/election-administration-integrity.md)  
**Review date:** 2026-08-02  
**Human editor:** CFMI bootstrap  
**AI assistance:** Consensus claim tester draft under anti-narrative-capture v0.1.0; human-edited.  
**Interest disclosure (editor):** none

Educational research only—not legal advice, voting instructions, or counsel to any person.

---

## Executive summary

**Claim tested:** “Mail-in balloting and voter rolls are secure.”

The claim is **institutional / mixed**: high-frequency reassurance from officials and NGOs, often answered by viral alarm. Neither vibe closes the question.

**FOR (steeled):** Layered state procedures (registration → validation → secrecy separation → canvassing), paper trails where used, signature/ID/cure regimes, USPS election-mail tooling, and post-election tabulation audits make *large-scale undetected tabulation manipulation* difficult in many jurisdictions. Mail-ballot *rejection* systems catch a non-trivial share of defective returns (EAC/Ballotpedia: ~1.2% of ~48M mail ballots rejected in 2024, often signature-related). Prosecuted fraud samples exist but are a tiny fraction of ballots cast.

**AGAINST (steeled):** “Secure” is routinely **undefined**. CISA’s own mail-voting risk assessment finds registration-data integrity is a *comparatively higher* risk in mail environments than in person, and that operational risk shifts to printers/USPS/drop-box storage. GAO finds list-maintenance data sources (NCOA, death files, interstate tools) help but are **incomplete**. NVRA notice-and-wait rules legally constrain how fast movers leave rolls. Citizenship is usually **attested**, not document-verified, at federal registration. RLAs answer tabulation questions—not citizenship of every registrant. Heritage’s fraud database is a **sampling of detected cases**, not a prevalence study; Brennan-style “vanishingly rare” claims measure prosecutions/caught cases, not undetected upper bounds.

**CFMI recommendation:** **NARROW** the claim. Accept as working hypotheses only jurisdiction-specific, threat-model-scoped statements (e.g., “this state’s RLA supported the reported *tabulation* outcome under stated risk limit”). Reject national slogans that erase state variation, audit scope, or residual list/custody gaps. Do **not** assert unverified national fraud rates or stolen-election claims. Do **not** conclude “everything is fine.”

---

## 1. Consensus claim tester (structured return)

### 1. Consensus claim (quoted)

> “Mail-in balloting and voter rolls are secure.”

### 2. Claim type

**Institutional** (primary), with **mixed** viral counters. Training-data prevalence of reassurance is **not** treated as truth.

### 3. Strongest case FOR (mechanisms + sources)

| Mechanism | Why it supports a *narrow* security claim | Sources |
|-----------|---------------------------------------------|---------|
| Layered mail process | Registration required; envelope validation (signature/ID/witness/notary as state law); ballot separated from identity package; double-voting checks; canvass | [CISA mail-voting risk assessment](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf) (controls side); [CISA safeguards infographic](https://www.cisa.gov/resources-tools/resources/mail-voting-election-integrity-safeguards-infographic); [NASS OPEX white paper](https://www.nass.org/sites/default/files/2021-01/opex-white-paper-nass-winter21.pdf) |
| Rejection / cure catch defects | Non-matching/missing signatures, late arrival, envelope defects → ballot not counted; many states offer cure | [EAC EAVS 2024](https://www.eac.gov/sites/default/files/2025-07/2024_EAVS_Report_508.pdf); [Ballotpedia rejected-ballots analysis](https://ballotpedia.org/Election_results,_2024:_Analysis_of_rejected_ballots) (~1.2% rejection; ~40.7% of rejections non-matching signature) |
| Decentralization + cyber posture | States run elections; federal cyber support framed as resilience vs nation-state/criminal cyber threats | [NASS cybersecurity letter](https://www.nass.org/sites/default/files/Election%20Cybersecurity/2.21.25%20NASS%20Board%20Letter%20to%20Sec.%20Noem.pdf); CISA election infrastructure materials |
| Tabulation auditability | Paper ballots + RLAs / hand recounts can statistically check that *reported outcomes match ballots cast* (when paper trail and custody hold) | [Verified Voting — RLA overview](https://verifiedvoting.org/audits/whatisrla/); [EAC RLA practical application](https://www.eac.gov/sites/default/files/eac_assets/1/6/Risk-Limiting_Audits_-_Practical_Application_Jerome_Lovato.pdf) |
| Detected fraud is sparse in public samples | Heritage sampling + Brennan critique both show *caught* cases are small vs total ballots—consistent with rarity of *prosecuted* fraud, if not with zero residual risk | [Heritage — About the Election Fraud Database](https://www.heritage.org/article/about-the-election-fraud-database); [Brennan — Heritage database assessment](https://www.brennancenter.org/our-work/research-reports/heritage-fraud-database-assessment) |
| Voter experience / process surveys | SPAE-style surveys show generally functional reported experience alongside partisan confidence gaps | [MIT Election Lab — How We Voted 2020](https://electionlab.mit.edu/articles/how-we-voted-2020); [How We Voted 2024 PDF](https://electionlab.mit.edu/sites/default/files/2025-07/HowWeVotedIn2024.pdf) |

**Steelman sentence:** Under many state rulebooks, mail voting is a managed risk with compensating controls analogous to in-person layers; officials are correct that viral “everything is stolen” claims usually skip canvassing, paper trails, and rejection mechanics.

### 4. Strongest case AGAINST (mechanisms + sources)

| Mechanism / gap | Why it undercuts the *unqualified* claim | Sources |
|-----------------|------------------------------------------|---------|
| Soft definition of “secure” | Cyber hardening ≠ eligibility verification ≠ perfect rolls ≠ perfect out-of-office custody | Anti-narrative-capture §2–3; CISA scope notes (infrastructure/ops, not endorsement of practice) |
| Registration integrity risk higher in mail | Voter not present to resolve identity/eligibility; altered/deleted registration can block ballot without provisional path | [CISA mail-voting risk assessment](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf) key findings |
| Risk shifts off election office | Printers, mail facilities, USPS, drop boxes, warehouse storage of completed ballots for days/weeks | Same CISA assessment |
| Incomplete list data | NCOA misses movers who never file change-of-address; death files and interstate matches have coverage/latency limits | [GAO-19-485](https://www.gao.gov/products/gao-19-485); [GAO-05-478](https://www.gao.gov/assets/gao-05-478.pdf) |
| NVRA removal constraints | Change-of-residence removals generally require written confirmation **or** notice + wait through ~two federal general elections if no response/vote | [52 U.S.C. § 20507](https://www.law.cornell.edu/uscode/text/52/20507); [Husted v. A. Philip Randolph Institute](https://www.supremecourt.gov/opinions/17pdf/16-980_f2q3.pdf) (2018); [DOJ NVRA list-maintenance guidance](https://www.justice.gov/crt/media/1366561/dl) |
| Citizenship verification gap | Federal elections require citizenship; common path is attestation under penalty of perjury, not documentary proof at registration (SAVE Act is *proposed* reform) | [H.R. 22 SAVE Act](https://www.congress.gov/bill/119th-congress/house-bill/22); GAO-05-478 historical notes on noncitizen ID difficulty |
| Audit scope mismatch | RLAs verify tabulation vs paper; they do **not** prove every ballot was cast by an eligible citizen or that rolls were accurate | [Carter Center RLA guide](https://cartercentee50c07c05.blob.core.windows.net/blobcartercentee50c07c05/wp-content/uploads/2022/06/risk-limiting-audits-guide.pdf) (RLA cannot compensate for fraudulent ballots in the paper trail) |
| Interstate tool fragmentation | ERIC helps many states match movers/deaths/duplicates; multiple states withdrew 2022–2023 amid privacy/partisanship controversies—alternatives uneven | [Ballotpedia ERIC](https://ballotpedia.org/Electronic_Registration_Information_Center_(ERIC)); [AP — Texas leaves ERIC](https://apnews.com/article/texas-voting-registration-fraud-eric-324d63f035ec22785839bc1b632410b0) |
| Detection ≠ prevalence | Heritage database is explicitly a **sampling** of proven cases; critics note it is not a rate study; both sides misuse it | [Heritage About page](https://www.heritage.org/article/about-the-election-fraud-database); [Brennan assessment](https://www.brennancenter.org/our-work/research-reports/heritage-fraud-database-assessment); [USA TODAY / FRONTLINE investigation](https://www.pbs.org/wgbh/frontline/article/heres-why-concerns-about-absentee-ballot-fraud-are-overhyped/) |

**Steelman sentence:** Even if large-scale tabulation theft is implausible in many paper+canvass systems, residual risks on **who is on the roll**, **who receives a ballot**, and **custody outside the polling place** are documented by agencies—not invented by viral threads—and national slogans paper over those gaps.

### 5. What “secure / unsafe” would have to mean for each case to hold

| If the claim means… | FOR can hold when… | AGAINST holds when… |
|---------------------|---------------------|----------------------|
| **Tabulation integrity** (outcome matches ballots accepted) | Paper trail + meaningful RLA/recount + observed canvass | Paper trail weak, custody broken, or audit sold beyond scope |
| **Cyber availability/integrity of systems** | MFA, access control, vendor controls, incident response | Compressed expansion, weak authentication, electronic ballot return (CISA: high risk) |
| **Eligibility of every registrant** | Documentary/database verification with published error rates | Attestation-only + incomplete death/move/citizenship matching |
| **Perfect roll currency** (no dead/moved/duplicate records) | Near-real-time interstate + vital records + NCOA with short removal lags | NVRA wait periods + incomplete NCOA + ERIC exits without equal substitutes |
| **Mail custody end-to-end** | Seals, dual control, tracking, observer rights, drop-box rules published and followed | Opaque storage, weak observer access, third-party handling without logs |
| **“Stolen election” / outcome conspiracy** | *Never* established by this claim’s evidence base | Viral claim fails mechanism test—**reject as fact** |

### 6. What audits / datasets measure vs do not measure

| Tool / dataset | Typically measures | Does **not** measure |
|----------------|--------------------|----------------------|
| Logic & accuracy tests | Equipment configured to mark/count correctly pre-election | Eligibility; custody after ballots leave office |
| Risk-limiting audit (RLA) | Statistical confidence that reported *winner* matches voter-marked paper (given trustworthy ballot set) | Citizenship; whether ineligible persons cast ballots that entered the set; full mail chain-of-custody forensics |
| Hand recount | Full or partial re-tabulation of paper | Same eligibility limits as RLA |
| EAVS rejection stats | How many mail ballots rejected and (partly) why | Whether accepted ballots were all eligible; undetected forged signatures that *matched* |
| NCOA / death files / ERIC-style matches | *Signals* for movers, deaths, duplicates among participating jurisdictions | Complete universe of movers/deaths; noncitizen status at scale |
| Heritage fraud database | Sampling of *detected & adjudicated* cases (per Heritage) | National fraud rate; undetected fraud; not a scientific prevalence estimate |
| Brennan / prosecution-count rarity claims | Caught/prosecuted cases relative to ballots (advocacy framing) | Upper bound on undetected ineligible voting |
| Cyber assessments (CISA) | Infrastructure/ops risk surfaces and controls | Proof of zero residual eligibility risk |

### 7. Disclosed funding / messaging orgs (public only)

| Org / voice | Role in claim ecosystem | Note |
|-------------|-------------------------|------|
| CISA / EAC / NASS / state SoS offices | Institutional “manageable risk / layered safeguards” messaging | Government / official associations—incentives to maintain public confidence; still publish residual-risk docs |
| Brennan Center | “Fraud vanishingly rare”; opposes SAVE-style documentary rules | Advocacy; funding via org disclosures—**detail not re-pulled this pass** → deeper 990 dig **not established in this pass** |
| Heritage / Heritage Action | List accuracy, ERIC reform, fraud sampling database, SAVE support | Advocacy; database explicitly a sampling—**not** a census of fraud |
| ERIC | Multistate list-matching cooperative | Contested after 2022–23 withdrawals; privacy/governance critiques vs conspiracy claims—separate fact layers |
| MIT Election Lab (SPAE) | Academic/survey process experience | Not a custody forensic |

Full Form 990 / LDA mapping for messaging shops: **not established from public sources in this pass** (escalation dig available; not required to NARROW the claim).

### 8. Statutory gaps vs practice gaps

| Gap type | Content |
|----------|---------|
| **Statutory** | NVRA §8 notice-and-wait for many move-based removals; federal citizenship requirement without uniform documentary verification at registration; HAVA/NVRA attestation architecture; state variation in signature standards, drop boxes, ballot tracking, observer rights |
| **Practice** | Incomplete use of available match sources; ERIC exits without published substitute metrics; uneven publication of list-quality KPIs; cure access variation; observer/log transparency uneven; selling RLA headlines as total security |
| **Measurement** | No authoritative public national rate of ineligible voting that survives adversarial methodology review—**not established in this pass** |

### 9. Residual unknowns → “not established from public sources in this pass”

1. National magnitude of noncitizen registration or voting as a single credible rate.  
2. Undetected fraudulent mail ballots that passed signature checks.  
3. Comparative list-error rates (dead/moved/duplicate) by state with harmonized methodology after ERIC fragmentation.  
4. How often chain-of-custody log gaps are material vs clerical.  
5. Net effect of SAVE Act–style documentary rules on false exclusions vs false inclusions (empirical, not slogan).  
6. Detailed donor maps for all major messaging NGOs (deferred).

### 10. Recommendation

**NARROW** — Do not ACCEPT the unqualified national claim. Do not REJECT the existence of real layered controls. Escalate digs (optional, depth-capped) on: (a) audit scope vs headlines for named states; (b) statute vs practice on list maintenance KPIs; (c) legal standards for private roll challenges; (d) disclosed funding of messaging orgs if influence Hard Flags fire.

---

## 2. Threat models (what “secure” must specify)

Before using the word secure, name the adversary and asset:

| Threat model | Asset | Plausible scale question | Typical controls |
|--------------|-------|--------------------------|------------------|
| **T1 Tabulation error/malware** | Vote totals | Can reported winner diverge from paper? | Paper, L&A, RLA, recounts |
| **T2 Registration cyber integrity** | Who gets a ballot / which ballot style | Targeted deletion/alteration of records | Access control, monitoring, voter notification |
| **T3 List pollution (error)** | Rolls include dead, moved, duplicates | Opportunity for accidental or opportunistic misuse | NCOA, vital records, ERIC/alt interstate, NVRA process |
| **T4 Ineligible registrant (citizenship etc.)** | Ballot cast by ineligible person | Attestation vs documentation; detection investment | Affirmation, DMV/SSA match limits, prosecution, proposed SAVE tools |
| **T5 Mail custody / ballot harvesting / drop box** | Voted ballot outside polls | State-law dependent; third-party handling | Tracking, seals, dual control, criminal law, observers |
| **T6 Signature forgery that matches file** | Accepted fraudulent return | Harder to observe than missing signature | Comparison standards, bipartisan boards, cure (helps voters; limited against skilled forgery) |
| **T7 Disinformation / confidence attack** | Public belief | Distinct from ballot integrity | Transparency with *scoped* claims |

**Error vs fraud:** Clerical mismatches, lawful-but-slow NVRA removals, and intentional illegality are different. Do not conflate inactive registrations with stolen elections; do not treat “no prosecution” as “no gap.”

**State variation:** All-mail states, excuse-required absentee states, and same-day registration states are not one system. National slogans that erase that fail this pass.

---

## 3. Narrative vs mechanism

| Public narrative | Operative mechanism | Scrutiny note |
|------------------|---------------------|---------------|
| “Mail voting is completely safe” | State-specific validation + third-party infrastructure; CISA lists residual risks *and* controls | Ask which state’s code and which threat model |
| “Rolls are cleaned regularly” | Maintenance activity ≠ published accuracy; NVRA wait; incomplete NCOA | Demand match criteria, notice volumes, removal stats |
| “Audits proved the election” | RLA/hand count = tabulation check if paper/custody hold | Publish pre-committed scope |
| “Voter fraud is vanishingly rare” | Prosecution/caught-case counts | Detection investment and upper bounds remain open |
| “Heritage proves massive fraud” | Sampling of adjudicated cases over years | Heritage itself says not exhaustive; not a rate |
| “ERIC is a partisan steal tool” / “ERIC is untouchable” | Multistate matching co-op with governance/privacy debates; exits real | Separate conspiracy from legitimate data-governance critique |
| “The election was stolen” | Outcome claim without precinct mechanisms | **Not established**; fails hard bans |

---

## 4. Hidden barriers to scrutiny (if any)

| Barrier | Status |
|---------|--------|
| Soft “secure” definition that ends inquiry | **Present** in institutional messaging |
| Audit headlines exceeding audit scope | **Present** |
| Uneven public metrics on list quality / interstate match results | **Present** |
| Legal friction for private challenges (standing, NVRA notice, deadlines) | **Present** — state-variable; deep dig **partially** established via NVRA text / *Husted* |
| Treating mechanism questions as illegitimate (“denialism”) | **Present** in some media/official frames |
| Viral totalizing narratives that skip canvass mechanics | **Present** on the alarm side |

Least-coercive response is **more measurable transparency**, not gag norms or security theater.

---

## 5. CFMI findings

### Established (from public sources in this pass)

1. Mail and in-person voting both carry risks; CISA documents mail-specific shifts (registration integrity comparatively higher; third-party ops; storage of returned ballots).  
2. Compensating controls (validation, separation, tracking, layered cyber) are real and vary by state.  
3. List maintenance data sources help and are incomplete (GAO).  
4. NVRA constrains many move-based removals via notice-and-wait (subject to *Husted*-consistent designs).  
5. Common post-election audits answer **tabulation** questions more than **eligibility** questions.  
6. EAVS shows material mail-ballot rejection activity (defects are detected at scale; does not prove all accepted ballots eligible).  
7. Unqualified national “secure” and “stolen” slogans both fail mechanism standards.

### Contested

1. Whether attestation-plus-criminal-penalty is “enough” citizenship enforcement vs documentary proof (SAVE Act debate).  
2. Whether ERIC withdrawals net-harm list accuracy vs privacy/governance gains from alternatives.  
3. How to interpret Heritage sampling vs Brennan rarity framing (both are advocacy uses of incomplete detection data).  
4. Whether signature verification error rates (false reject vs false accept) are acceptable—state practice varies; national equilibrium **not established**.

### Not established from public sources in this pass

1. Any single national fraud rate (high or “zero”).  
2. Outcome-determinative ineligible mail voting as a proven national pattern.  
3. Zero residual risk on rolls or mail custody.  
4. That RLAs “proved everything” about elections writ large.

### Least-coercive transparency improvements (Charter-aligned)

1. **Publish audit scopes** before Election Day: what will/won’t be tested.  
2. **List-quality dashboards:** movers flagged, notices sent, removals completed, interstate match participation, appeal/cure rates—machine-readable.  
3. **Mail custody logs** with observer access rules stated in plain language.  
4. **Citizenship/eligibility tools** that minimize false exclusion: published match criteria, alternative evidence paths, fee waivers for vital records—evaluate SAVE-style text on least-coercion, not team.  
5. **Reject anti-scrutiny norms** and **reject unverified outcome conspiracies** equally.

### Open questions (carry to parent brief)

1. Best public methodologies for state-comparable inactive/duplicate/death rates post-ERIC exits?  
2. Empirical signature false-accept rates under production workloads?  
3. Materiality of drop-box/chain-of-custody incidents after bipartisan canvass (case studies, not vibes)?  
4. SAVE Act alternative-evidence path: workable in practice or chilled by penalties?  
5. Which states already publish the KPI set in the least-coercive list above?

---

## 6. Sources (selected)

**Agency / official**

- [CISA — Mail-in Voting in 2020 Infrastructure Risk Assessment (PDF)](https://www.cisa.gov/sites/default/files/publications/cisa-mail-in-voting-infrastructure-risk-assessment_508.pdf)  
- [CISA — Mail-voting election integrity safeguards](https://www.cisa.gov/resources-tools/resources/mail-voting-election-integrity-safeguards-infographic)  
- [EAC — EAVS 2024 Comprehensive Report (PDF)](https://www.eac.gov/sites/default/files/2025-07/2024_EAVS_Report_508.pdf)  
- [GAO-19-485 — Voter registration / list management](https://www.gao.gov/products/gao-19-485)  
- [GAO-05-478 — Accurate voter registration lists (PDF)](https://www.gao.gov/assets/gao-05-478.pdf)  
- [NASS — Maintaining Ballot Integrity with Vote by Mail (PDF)](https://www.nass.org/sites/default/files/2021-01/opex-white-paper-nass-winter21.pdf)  
- [DOJ — NVRA list maintenance guidance](https://www.justice.gov/crt/media/1366561/dl)  
- [Supreme Court — *Husted* opinion (PDF)](https://www.supremecourt.gov/opinions/17pdf/16-980_f2q3.pdf)

**Academic / reference**

- [MIT Election Lab — How We Voted 2020](https://electionlab.mit.edu/articles/how-we-voted-2020) · [2024 PDF](https://electionlab.mit.edu/sites/default/files/2025-07/HowWeVotedIn2024.pdf)  
- [Verified Voting — Risk-limiting audits](https://verifiedvoting.org/audits/whatisrla/)  
- [Ballotpedia — 2024 rejected ballots](https://ballotpedia.org/Election_results,_2024:_Analysis_of_rejected_ballots) · [ERIC](https://ballotpedia.org/Electronic_Registration_Information_Center_(ERIC))

**Advocacy (label as such)**

- [Heritage — About the Election Fraud Database](https://www.heritage.org/article/about-the-election-fraud-database)  
- [Brennan Center — Heritage Fraud Database: An Assessment](https://www.brennancenter.org/our-work/research-reports/heritage-fraud-database-assessment)  
- [Brennan — Letter opposing SAVE Act](https://www.brennancenter.org/our-work/research-reports/brennan-center-letter-congress-opposing-save-act)  
- [Heritage Action — SAVE Act myth/fact](https://heritageaction.com/blog/myth-vs-fact-the-safeguard-american-voter-eligibility-act-h-r-22-s-128)

**News (descriptive)**

- [AP — Texas resigns from ERIC](https://apnews.com/article/texas-voting-registration-fraud-eric-324d63f035ec22785839bc1b632410b0)  
- [PBS FRONTLINE — absentee fraud concerns / Heritage database investigation](https://www.pbs.org/wgbh/frontline/article/heres-why-concerns-about-absentee-ballot-fraud-are-overhyped/)

**Legislation**

- [H.R. 22 — SAVE Act (119th Congress)](https://www.congress.gov/bill/119th-congress/house-bill/22)

---

## 7. Editor’s note

AI-assisted I4 pass. Recommendation **NARROW** accepted. No unverified national fraud rates. No “everything is fine.” Human editor: CFMI bootstrap.

### Copy-paste next prompts

```
Escalate dig (depth 1): For three named states (one ERIC member, one ERIC exit, one all-mail),
publish what their 2022–2024 post-election audits measured vs did not; cite official audit reports only.
```

```
Score living SAVE Act text (H.R. 22 or current vehicle) against CHARTER + METHODOLOGY:
least-coercive verification, false-positive safeguards, discretion, Hard Flags. Pair open fix language.
```

```
I4 on viral claim: "The election was stolen." Same anti-narrative rules; return structured FOR/AGAINST only.
```
