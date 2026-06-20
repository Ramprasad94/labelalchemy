# Roadmap

This is the public, directional roadmap for **Label Alchemy**. It reflects where the project is
headed — not firm commitments or dates. Label Alchemy is built and maintained by a solo developer,
so priorities shift with user feedback and what's most impactful to build next.

> 📌 **No dates, no guarantees.** Items move between sections as work happens. The best way to
> influence what gets built is to tell me what you need (see below). Gated features are marked
> **(Paid)** — they require a license; everything else is free.

## How to influence the roadmap

1. **Have an idea?** Post it in [Discussions → Ideas](../../discussions/categories/ideas).
2. **Want something that's already there?** Give it a 👍 — upvotes are the strongest signal I use
   to prioritize. The most-wanted ideas rise to the top of this list.
3. **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml) — fixes are
   prioritized ahead of new features.

Upvotes guide ordering; they are not a delivery-date commitment.

---

## 🟢 Shipped

Available in Label Alchemy today:

- **Multi-file-type scanner** — Apex (`.cls`), LWC (`.js` / `.html`), Aura (`.cmp` / `.app` / `.js`)
  with smart false-positive suppression (API names, SOQL, framework refs, debug calls, comments) and
  a test-class skip toggle.
- **Deterministic naming (default, $0, offline)** — local Snake_Case (or PascalCase) names with light
  context prefixes, filler-word stripping, 40-char limit, and uniqueness.
- **AI naming (opt-in, BYOK)** — Anthropic, OpenAI, Gemini, DeepSeek, OpenRouter, Ollama, LM Studio,
  and any custom OpenAI-compatible endpoint; per-file scope is free; output always sanitized to a
  valid Salesforce name. Tunable style, case, guidance, and optional label descriptions.
- **Organize labels into categories** — set a Salesforce category per label or per file in the review
  panel; written straight to the label's `<categories>`.
- **Smart label reuse** — identical text collapses to one label, within a scan **and** across scans
  (by reading your existing labels file).
- **Diff review panel** — component-grouped, collapsible, per-label checkboxes, live-validated
  editable names, VS Code native diff editor, LWC sidecar preview, filter box.
- **Streaming apply** — O(1-file) memory; CustomLabels XML merge that never overwrites existing
  labels; automatic LWC `@salesforce/label` import + getter.
- **Change record** — every convert writes a timestamped `labelalchemy-changes/` folder
  (`summary.md`, `summary.csv`, `package.xml`) with a one-click Open summary.
- **Folder Audit Report** — counts by component type, top-offenders, per-file drill-down, and an
  "≈ N hrs estimated manual conversion" cost-estimate KPI.
- **Built-in technical denylist** — HTTP verbs, MIME/charset tokens, and dynamic-SOQL fragments
  never get flagged.
- **Bulk convert (Paid)** — apply conversions across the whole project in one deduped pass.
- **Deploy to Org (Paid)** — one-click deploy with a production hard-block; file / folder /
  last-conversion entry points; manifest deploy for large change sets.
- **Project-wide AI naming (Paid)** — reuses existing labels and follows your naming convention
  across the codebase.
- **Custom denylist (Paid)** — teach the scanner to ignore your brand names, enum values, and status
  codes; commit it so the whole team scans the same way.
- **Catch diverging-name duplicates (Paid)** — flag a value that already has a label under a
  different name; reuse-or-create prompt at write time.
- **Audit CSV export (Paid)** — export the Audit Report for architects, QA, or clients.
- **Self-serve license management** — activate, and move a seat between machines yourself with
  Deactivate License on This Device.

For per-version detail, see the [Changelog](CHANGELOG.md) (canonical release notes live on the
[Marketplace](https://marketplace.visualstudio.com/items/ramprasad94.labelalchemy/changelog) and
[GitHub Releases](../../releases)).

---

## 🟡 In progress / next up

- **PR / git-diff CI scan** — catch new hard-coded strings in changed files before they merge
  (a building block for the Team plan).
- **Deeper project-context AI naming (Paid)** — richer naming that draws on component-bundle context
  and an org-SOQL glossary, beyond today's project-wide reuse.
- **Async / batch / dry-run deploy (Paid)** — preview and stage larger deploys.

---

## 🔵 Planned / exploring

Directional ideas, roughly in order of interest — upvote in
[Ideas](../../discussions/categories/ideas) to push these up:

- **Team plan** — shared team config & naming enforcement, centralized billing & seat management
  (a per-seat subscription; [join the waitlist](https://labelalchemy.dev/#team-waitlist)).
- **AI scan cost / scope pre-estimate** — a heads-up on size before a large AI naming run.
- **Flow labels** — detect hard-coded text in screen Flows.
- **Multi-language label generation** — generate translations for labels via an LLM.
- **Org-wide reporting** — reuse and coverage insights across an org.

---

*This roadmap is a living document and will change. Nothing here is a promise of a specific feature
or date. For current pricing and tiers, see [labelalchemy.dev/#pricing](https://labelalchemy.dev/#pricing).
Thanks for helping shape Label Alchemy! 🙏*
