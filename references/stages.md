# Stages — detailed method

The user may work these in any order. Each stage below has its purpose, the method, and its exit criterion (what "satisfied" means for the completeness check). Read the linked reference files for the stages that have their own playbook.

## Stage 0 — Scope & type

**Purpose:** Frame the brief before any content. A wrong frame here wastes days downstream (in one campaign, the brief was framed as "replace incumbent X" when the real motion was intercepting a move to a bigger platform — caught only by asking "who are we actually competing against, at what price point?").

**Method — ask the user:**
- **Brief type?** Competitive-displacement (win vs. a target we're displacing) / Campaign (a demand play, no single named competitor) / Product-launch. This selects which template modules apply — displacement briefs get the §4 displacement module; others delete it.
- **Who's the SME?** The domain expert whose brain-dump seeds this (a founder, a rep, a product lead).
- **Trigger hypothesis?** What event makes *now* the moment for this buyer?
- **Segment?** Link the relevant customer intelligence records — segment truth lives there, not restated in the brief.
- **Economic sanity check** (for displacement): does the price logic even support the motion? (e.g. a low-cost incumbent can't justify a six-figure switch on its own, so the real trigger must be a bigger business change.)

**Output:** A stubbed brief (duplicate the template), Confidence: Hypothesis, properties set, and a short **research plan** listing the claims you expect to make and what evidence each will need. Log the creation in the changelog.

**Exit criterion:** Brief exists in the DB, type + segment + trigger hypothesis set, research plan drafted.

## Stage 1 — SME interview

**Purpose:** Capture the expert's mental model — the hypotheses to then test. NOT to capture facts.

**Method:** Generate interview questions tailored to the SME's altitude:
- *Strategy/founder altitude*: category, positioning, hook, competitive white space, why-now.
- *In-market/rep altitude*: what actually happens in deals, real shortlist, win/loss language, ground-truth on the trigger.
- *Product altitude*: exact capability boundaries, what we can/can't claim, integration status, certifications.

Give the user the questions as a doc they can walk into a meeting with. They conduct it offline — this may take days. They bring back notes (possibly a transcript).

**Critical:** When notes come back, your NEXT action is Stage 2 (challenge), never "write it into the brief as fact." Flag the whole SME input as Hypothesis until corroborated.

**Exit criterion:** SME interview conducted, notes captured, and every load-bearing SME claim logged as a hypothesis to test.

## Stage 2 — Independent research

See `references/research.md`. **Purpose:** corroborate or *challenge* every SME claim with outside evidence. Hunt contradictions actively — the most valuable corrections come from research disagreeing with the SME. Cite real URLs only; never fabricate a source. Tier findings: Confirmed / Corrected / Hypothesis / Rejected.

**Exit criterion:** Every SME claim has been checked against independent sources; corrections captured; sources cited with links.

## Stage 3 — Call validation

See `references/call-worksheet.md`. **Purpose:** validate claims against real buyer calls and capture verbatim buyer language. Generate a worksheet (each claim + "what to search for" + "what would confirm/challenge"); the user runs it in their call-recording tool (e.g. Gong) and returns annotated findings. This is where evidence tiers get assigned and where the highest-value output — verbatim buyer phrases — gets captured.

**Exit criterion:** Claims validated/challenged against calls; buyer-language quotes captured with source + date; tiers assigned.

## Stage 4 — Customer evidence

See `references/customer-evidence.md`. **Purpose:** attach named proof accounts to each claim by mining customer records. Distinguish proof-of-pain (why they moved — usually available) from proof-of-outcome (post-sale result — usually NOT recorded yet; keep that gap visible). Flag verbatims as clearance-pending.

**Exit criterion:** Claims carry named proof accounts where they exist; the outcome-evidence gap is explicitly noted.

## Stage 5 — Tension resolution

See `references/tensions.md`. **Purpose:** surface every conflict (SME vs. research vs. calls vs. product vs. existing docs), group by whether they're genuine judgment calls vs. data gaps, and route each to the right human. Hold tensions open — visibly, in the brief — until resolved. Don't silently pick a side.

**Exit criterion:** Every tension is either resolved (with the resolution logged) or explicitly parked with an owner and a "pending X" note.

## Stage 6 — Assembly & tiering

**Purpose:** write the brief. Only now. Every claim gets: evidence tier (Hypothesis / SME-asserted / Validated / Proven), cold-copy gate (Y/N — separate from tier; a Validated claim can still be N), and a proof account where one exists. SME-asserted claims are always N on cold-copy and always carry a named confirmation owner.

**Exit criterion:** Brief fully written; every claim tiered and gated; landmines listed; nothing bare.

## Stage 7 — Graduation gate

**Purpose:** decide whether the brief can leave Hypothesis and whether frame-dependent assets can compile. Run the completeness check (in SKILL.md). Confirm blocking sign-offs (product truth-in, leadership frame confirmation). Distinguish assets that inherit only the *settled* layer (can compile now) from those that inherit the *open* frame (must wait). Tag each asset with which brief sections it inherits, so a later brief change flags the right assets.

**Exit criterion:** Blocking sign-offs confirmed; Confidence upgraded from Hypothesis; settled-layer assets cleared to compile.
