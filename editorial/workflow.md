# Overhang — Post Workflow & Pre-Publish Checklist

> **Forked from Drift's editorial memory on 2026-06-20.** The phases and checklist apply as-is. The illustrative examples below are *Drift* posts (Overhang has none yet) — they're kept to teach the pattern; replace them with Overhang examples as the course grows.

## The 7-Phase Workflow

Phases are not strictly sequential — enrichment often interrupts drafting, cleanup can repeat. The checklist at the end is the forcing function that closes every post.

### Phase 1 — Idea capture
Record in CLAUDE.md's Topic Pipeline. Each idea must pass the quality gate: *what specific claim does this post make that a practitioner would push back on?* No specific claim yet = it's a theme, not a post. Name (1) the claim, (2) a primary-source/evidence anchor, (3) the practitioner objection the post earns the right to rebut.
**Anti-pattern:** vague theme without argument.

### Phase 2 — Research/framing
For unfamiliar territory (private-credit structures, accounting treatment, capital flows), research-first is worth a dedicated session.
**Anti-pattern:** drafting before the argument's core contrast is clear. Starting from a source and working backward produces padding.

### Phase 3 — Draft
Produce `.draft.md`. May appear in `index.json` with `"draft": true`. Focus on argument flow and primary sourcing; don't polish prose yet.
**Anti-pattern:** over-polishing during drafting — style cleanup is cheap later; redrafting a muddled argument is expensive.

### Phase 4 — Targeted enrichment
Add case studies, news hooks, filings *after* the argument structure is solid. Bring the source, assess fit explicitly, then write it in.
**Anti-pattern:** adding a source that doesn't serve a specific argument gap.

### Phase 5 — Review
Panel reviewer system (`blog-review-panel` plugin). Calibrate depth to complexity:
- **Light (2):** Sam + Jordan — realism + reader patience.
- **Standard (4):** Sam + Alex + Jordan + Chris — adds engineering credibility + argument stress-test.
- **Full panel:** all reviewers + Dana synthesis — for high-stakes, novel-claim, or cross-disciplinary posts.

**Overhang note:** Priya (regulatory hawk) is tuned to banking regulation and maps poorly to capital-markets content. Either skip her or retune/swap toward a credit-markets / macro reviewer. Consider whether a markets-savvy persona belongs in the standard tier given Overhang's subject.

### Phase 6 — Cleanup passes
Run the slop-guard score check; threshold 70/100. Catch: em-dash clusters (3+/section), "not X but Y" pairs (>2/post), filler adjectives ("comprehensive," "actionable," "robust"), sentences >~25 words, passive constructions in explanatory text.
**Anti-pattern:** treating slop-guard as optional because the post "feels clean." The score is the gate, not the feeling.

### Phase 7 — Publish
Complete the pre-publish checklist below in the same session. Don't split publication across sessions.

---

## Pre-Publish Checklist

- [ ] **Slop score ≥ 70/100** — run the check; targeted cleanup pass if below.
- [ ] **Closing mode logged** — add/confirm the entry in the closing mode log in `voice.md`; check the prior 2 posts to avoid consecutive repeats.
- [ ] **Deferred reward prompt** — ask Ryan the closing check (see `voice.md`); wait for and log the response before finishing the session.
- [ ] **Forward links** — add reverse links in every post this one references, in the same session. Include cross-links to **Drift** where the topic connects (payments/GENIUS, FSB systemic risk, Economics-of-AI labor).
- [ ] **Footnotes** — sequential numbering, no orphans or doubles.
- [ ] **TL;DR** — "what's the point?" in 3–4 sentences: argument first, caveat/open question last.
- [ ] **index.json** — remove `"draft": true`; date = publish date.
- [ ] **CLAUDE.md** — move row from drafts to published table; update pipeline/series status.
- [ ] **Search index** — `npm run build:search` after publishing.

---

## Retroactive maintenance (periodic)
Run every ~5–6 posts or when a series completes: cross-link audit, glossary coverage, source/data updates (figures go stale fast in this domain), terminology simplification. The forward-link checklist item is the prevention; these sweeps are the catch-up.
