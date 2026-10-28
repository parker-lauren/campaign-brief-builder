# Retro mode — the self-healing protocol

## When to be here

ONLY when the user explicitly asks to improve the process: "let's do a retro," "the template's missing something," "update the brief process/skill," "we learned something from that campaign." Never enter retro mode from run mode on your own initiative. A marketer building their fifth brief must never trigger a process change — stability is the default.

## The core rule: the system never heals itself silently

The temptation is to let the skill rewrite its own SKILL.md/template after each brief. **Do not.** This is a discipline-enforcement system; a system that auto-edits itself based on the last brief will drift exactly the way we work to stop *claims* from drifting. One weird brief teaches a bad lesson; the lesson compounds silently; months later the process has degraded and nobody decided that on purpose.

So retro follows the same loop as everything else in this skill: **observe → distinguish one-off from systemic → propose scoped change with evidence → human ratifies → apply + version + changelog.** Improvement is deliberate, evidence-backed, and versioned — never automatic.

## The protocol

### 1. Gather signal
- Read the **Process Friction Log** since the last retro (the accumulated one-line notes from run mode).
- Read the specific brief(s) or campaign the user points to.
- If the trigger is a *completed campaign* (not just a finished brief), look for outcome signal: did the brief's claims hold up? Did a "Validated" claim fail in-market? Did an untracked competitor decide deals? That's the richest input — the process learning from real results.

### 2. Distinguish one-off from systemic (the tiering discipline, applied to process)
For each candidate learning, judge: is this **one-off** ("that brief was weird") or **systemic** ("this will recur across briefs")? Only systemic goes forward. Evidence of systemic = the same friction appeared in multiple briefs, or a structural gap that any brief of this type would hit. A single odd occurrence is noise — the same standard you'd apply to a customer claim.

Say which is which, and why. Do not propose a change on a single data point unless it's a clear structural hole (e.g. "the template genuinely has nowhere to put X, and every displacement brief needs X").

### 3. Propose scoped changes with evidence
For each systemic learning, propose a *specific, minimal* change:
- **What** changes (the exact section/rule/stage — and the diff, concretely).
- **Where** (template section? a stage in `stages.md`? an enforcement rule in SKILL.md?).
- **Evidence** (which briefs, which friction-log entries, which campaign result).
- **Scope** (does this affect all brief types, or just displacement?).

Prefer the smallest change that solves it. Resist the urge to redesign — the process survived N briefs; respect that.

### 4. Human ratifies
Present the proposals grouped and ranked by leverage. The user approves, rejects, or edits each — the same propose-then-ratify pattern as writing to a brief's source of truth. Nothing changes until they approve.

### 5. Apply + version + changelog
On approval:
- Make the change to the template and/or SKILL.md and/or the relevant reference file.
- **Version it.** Bump a version marker on the template and/or skill (e.g. Template v3 → v4) with a dated line describing what changed and why (which retro, which evidence). The process artifacts get the same changelog discipline the briefs do.
- Note the version so future briefs record which template version produced them — this prevents old briefs being judged against new standards, and lets you roll back a change that turns out wrong.
- Clear or mark the friction-log entries that this retro addressed, so the next retro starts clean.

## What NOT to do in retro
- Don't act on one-offs.
- Don't redesign the whole system because one thing chafed.
- Don't apply changes without ratification.
- Don't forget to version — an unversioned change to a living process is how drift hides.
- Don't touch briefs currently in flight; changes apply to new briefs (and existing ones only if the user chooses to migrate them).
