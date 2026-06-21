# Overhang — Structure & Formatting

> **Forked from Drift's editorial memory on 2026-06-20.** These structural rules are domain-agnostic and apply as-is; adjust only if Overhang's subject demands it.

**Paragraph length:** 2–3 sentences max. No exceptions for "important" sections.
**Why:** Long paragraphs read like white papers. Short paragraphs force the writing to earn its place.
**How to apply:** If a paragraph runs past 3 sentences, ask whether the last 1–2 sentences can become a footnote or be cut.

---

**Footnotes:** Use `[^1]:` syntax aggressively. Every interesting statistic, citation, or research detail that doesn't drive the sentence-level argument should be a footnote. Max 6–8 per post. Primary sources (filings, working papers, regulator/central-bank docs, earnings transcripts).

---

**Alerts:** `> [!NOTE]`, `> [!WARNING]`, `> [!IMPORTANT]`, `> [!TIP]`, `> [!CAUTION]` — rendered as styled callouts. Standard posts: 1–2 max. Number/finance-heavy posts: up to ~4, e.g. a `[!TIP]` with a `**Plain terms:**` header to translate an opaque concept (PIK toggle, FTP, mark-to-model) for non-specialist readers.
**Redundancy check:** before adding a TIP, read the surrounding paragraph — if the prose already explains the term informally, skip it.

---

**References section:** None. Footnotes carry citations. No separate `## References` block.

---

**Opening paragraph:** Don't assume prior knowledge. Start from a relatable experience or concrete scenario before introducing terminology. Lead with the problem before naming the concept; vary the *form* so it doesn't become a template.

---

**The open question:** Should appear in the lede (or early) AND in the closing. Don't save the most interesting framing for the end. Closing *form* should vary — see the closing mode taxonomy in `voice.md`.

---

**TL;DR block:** Every post (except the overture) opens with a TL;DR blockquote immediately after the front matter, before the first paragraph. Format: `> **TL;DR:** [3–4 sentences]`. The thing a reader should leave knowing — argument first, caveat or open question at the end. Write it last.

---

## Rendering gotchas (inherited — apply to all posts)

- **Use `≈`, never `~`, for approximations** — marked.js pairs single tildes into strikethrough.
- **No Mermaid, no inline SVG** — save SVGs to `img/` and reference with `<img src="../img/...">`; use hardcoded hex colors (CSS vars don't resolve inside external SVGs).
- **`<details>/<summary>`** pop-outs supported; interior must be HTML, not markdown.
- **Pull quotes (`[!QUOTE]`):** max 2/post, spaced ≥1 section apart; external quotes need `— Author, *Work* (year)` attribution. Strategies A–E documented in Drift's CLAUDE.md (Pullquote selection strategies) — reuse until Overhang develops its own.
