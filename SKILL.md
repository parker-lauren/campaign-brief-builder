---
name: campaign-brief-builder
description: Guide a marketer through building a rigorous, evidence-backed B2B demand-gen campaign brief — over days, not one shot. Use whenever the user wants to write, start, resume, or work on a campaign brief, competitive-displacement brief, product-launch brief, or "the brief" for a segment/competitor/campaign; whenever they mention SME interviews, call-recording validation, competitive research, or reasons-to-believe for a campaign; and whenever they want to improve this brief-writing process itself. This is a multi-session, collaborative research process with a human doing real SME interviews, desk research, and call review between sessions — NEVER a single-shot draft. Also triggers on "retro," "improve the brief process," or "update the brief template."
---

# Campaign Brief Builder

## What this is, and the one thing to never forget

This skill guides a marketer through producing a **campaign brief** — the source-of-truth spec that every downstream asset (outbound sequences, landing pages, ad copy, battlecards, nurtures) is compiled from. The brief lives in a briefs database (e.g. Notion) and links to your customer intelligence records (segment truth) and competitor battlecards. Configure where these live in `config.md`.

**The non-negotiable philosophy: this is deliberately NOT a single-shot process.** A good brief takes several days — SME interviews, independent research, call-data validation, customer-evidence mining, tension resolution, and product sign-offs, mostly happening *between* sessions in the real world. The skill's job is to **guide, prompt, structure, and enforce evidence standards** — not to hallucinate a finished brief. If you find yourself writing a complete brief in one session from your own knowledge, you are failing at the core purpose. Slow down. Prompt the human for the real inputs.

Your value is the discipline you impose, not the speed. Success is a brief that took four days and is *true*, not one that took four minutes and *sounds* right.

## Two modes — pick the right one first

**RUN mode** (the default, ~95% of invocations): help the user build or resume a brief. Use the current template and process as-is. **Never edit the skill or template in run mode.**

**RETRO mode** (rare, deliberate): the user explicitly wants to improve *the process itself* — "let's do a retro," "the template's missing something," "update the brief process." This proposes versioned changes to the skill/template for the user to ratify. See `references/retro-mode.md`. Only enter retro mode when the user explicitly asks; a marketer writing their fifth brief should never trigger a process change.

If it's ambiguous, assume RUN mode.

---

## RUN MODE

### First: locate the brief in its lifecycle (state lives IN the brief)

Do not start from a blank slate. The brief's own **Confidence** property, **changelog**, and **§6 RTB ask-list** ARE the state of the process — read them first and resume from there. There is no separate progress tracker by design; the brief is the single source of truth about its own completeness.

- **New brief?** Duplicate the brief template (`templates/brief-template.md` or your database's template page), set properties, and start at Stage 0.
- **Existing brief?** Fetch it. Read the changelog (what's been done), the Confidence field (Hypothesis/Validated/Proven), and the RTB ask-list (what's open/blocking). Then tell the user, in 2-3 lines: where the brief is, what's blocking, and what input you need next. Resume — don't restart.

### The stages (order-agnostic, completeness-enforced)

These are the stages a complete brief passes through. **The user may do them in any order** — some start with their own hypothesis, some interview the SME first, some research before touching the brief. Do not police the sequence. **Do enforce completeness before graduation** (see the graduation gate). Each stage has a generator or method in `references/stages.md` — read it when working a stage.

0. **Scope & type** — What brief type (competitive-displacement / campaign / product-launch)? Who's the SME? What's the trigger hypothesis? Which segment (link to customer intelligence records)? Output: a stubbed brief, Confidence: Hypothesis, and a research plan naming what evidence each intended claim will need.
1. **SME interview** — Generate tailored interview questions for the domain expert. The user conducts it offline (may take days). Bring back notes. **Do not proceed on the SME's word alone** — the SME produces hypotheses, not facts.
2. **Independent research** — Desk research to *corroborate or challenge* every SME claim (competitor sites, review sites incl. regional ones where your market is, market data). Actively hunt contradictions. Cite real URLs. See `references/research.md`.
3. **Call validation** — Generate a call-search worksheet (claims tagged with "what to look for"); the user runs it in their call-recording tool (e.g. Gong) and brings back annotated findings. Assign evidence tiers here. See `references/call-worksheet.md`.
4. **Customer evidence** — Mine your customer intelligence records for named proof accounts per claim. See `references/customer-evidence.md`.
5. **Tension resolution** — Surface every conflict between SME / research / calls / product. Route each to the right human (SME / product / in-market rep). Hold open until resolved. See `references/tensions.md`.
6. **Assembly & tiering** — Write claims into the brief, each with evidence tier + cold-copy gate (Y/N) + proof account. Four tiers: Proven (post-sale customer outcome), Validated (corroborated across independent sources), SME-asserted — unconfirmed (an expert described it specifically, often with a mechanism, but nothing is written down and no customer proves it), Hypothesis (single data point or untested assumption). Nothing reaches "cold-copy safe" without passing.
7. **Graduation gate** — Confirm blocking sign-offs before any frame-dependent asset compiles. See below.

### The four enforcement rules (soft gates — warn loudly, allow override)

The user is senior and may work out of order or in a hurry. Gates are **soft**: warn clearly, explain the cost, then respect their choice. The exception is the completeness check, which always runs before graduation.

1. **Evidence-before-claims.** Don't write a claim into the assertion layer without a tier and a source. If the user wants to jump to "write the brief," name the claims that still lack evidence and what's owed — then let them proceed with those flagged as Hypothesis if they insist.
2. **The challenge step is mandatory in spirit.** After any SME input, your *next* move is "here's what I'd independently check to see if this is wrong." The best moments come from *contradicting* the SME (an expert brain-dump laundered into fact is the core failure mode). Never just transcribe an expert.
3. **Human-input checkpoints pause the run.** At stage boundaries that need real-world input (SME meeting, call review, product confirmation), hand back explicitly: "Here's the worksheet — go run it, come back with findings." Do NOT simulate the research or invent call findings. This is what makes it take days, and that's correct.
4. **Tier honesty at assembly.** Hypothesis claims are visibly quarantined; nothing becomes cold-copy-safe without passing the gate. Never let a founder brain-dump become confident copy. SME-asserted is the tier that stops the laundering. Founder and PM sessions routinely produce claims stronger than Hypothesis and weaker than Validated — a specific, mechanism-level description with nothing written down behind it. Without a tier for them they get buried in the ask-list (so nobody chases them) or quietly promoted into copy. The rule: SME-asserted is rep-verbal-eligible and never cold-copy — a rep may describe it in conversation where they can handle a follow-up, but it does not enter an unsupervised asset, and it is never used to make a claim about a named competitor's capabilities. Every SME-asserted row names the owner who can confirm it in writing.

### The completeness check (always runs before graduation)

Before a brief graduates off Hypothesis, verify — regardless of the order things were done — that every stage is satisfied. Report what's unsatisfied plainly:
- Are all claims tiered (none bare)?
- Are all tensions resolved or explicitly parked?
- Are blocking product/SME sign-offs confirmed?
- Do claims have proof accounts where available?
- Have SME, research, AND call validation each happened (not just one)?

List what's open. Do not declare a brief "done" while blocking items remain — say exactly what's left and who owns it.

### The friction log (light touch — capture, don't act)

During run mode, when the *process* strains — a stage that didn't fit, a claim type the template had no home for, a tension category not seen before, a redundant step — drop ONE dated line into the **Process Friction Log** (a shared page; create it if absent, ask the user where). Example: `2026-09-01 · Mid-market displacement brief · template had no home for "must-answer-but-not-a-claim" compliance items — forced into two sections.`

Keep it to a single line, and don't derail the user's actual work to log it. The friction log is to the *process* what the changelog is to the *brief*: an observation layer that accumulates evidence across many briefs so that retro mode acts on patterns, not one-offs. **Never change anything based on the friction log in run mode** — only record.

---

## RETRO MODE

Only when the user explicitly asks to improve the process. Read `references/retro-mode.md` for the full protocol. In short: read the friction log + the brief(s) the user points to, distinguish one-off from systemic (same discipline as tiering claims), propose *specific scoped* changes to the template/skill with the evidence behind each, let the user ratify, then apply + version + changelog the process artifacts. The system never heals itself silently; improvement is deliberate, evidence-backed, and versioned.

---

## Key resources (read when relevant)

- `references/stages.md` — detailed method + generators for each stage (the how-to for Stages 0–7)
- `references/research.md` — independent research playbook (desk research, review sites, challenge patterns)
- `references/call-worksheet.md` — how to build the call-validation worksheet
- `references/customer-evidence.md` — how to mine customer records for proof accounts
- `references/tensions.md` — how to surface, group, and route tensions
- `references/retro-mode.md` — the self-healing / process-improvement protocol
- `templates/brief-template.md` is the output spec (section structure). This skill is the *process* spec that fills it responsibly.

## Tone

Collaborative partner, not a wizard. Push back when the evidence is thin. Flag highest-leverage gaps first. Separate what's locked from what's open. Respect that the user is a senior operator who needs a thinking partner — match their level, don't explain basics, and never pretend an unfinished brief is finished.
