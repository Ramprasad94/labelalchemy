# Roadmap

This is the public, directional roadmap for **Label Alchemy**. It reflects where the project is
headed — not firm commitments or dates. Label Alchemy is built and maintained by a solo developer,
so priorities shift with user feedback and what's most impactful to build next.

> 📌 **No dates, no guarantees.** Items move between sections as work happens. The best way to
> influence what gets built is to tell me what you need (see below).

## How to influence the roadmap

1. **Have an idea?** Post it in [Discussions → Ideas](../../discussions/categories/ideas).
2. **Want something that's already there?** Give it a 👍 — upvotes are the strongest signal I use
   to prioritize. The most-wanted ideas rise to the top of this list.
3. **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml) — fixes are
   prioritized ahead of new features.

Upvotes guide ordering; they are not a delivery-date commitment.

---

## 🟢 Shipped

Already available in Label Alchemy today:

- **Multi-file-type scanner** — Apex (`.cls`), LWC (`.js` / `.html`), Aura (`.cmp` / `.app` / `.js`)
  with smart false-positive suppression (API names, SOQL, framework refs, debug calls, comments).
- **Deterministic naming (default, $0, offline)** — local Snake_Case names with light context
  prefixes (`Error_`, `Placeholder_`, `Button_`), filler-word stripping, 40-char limit, uniqueness.
- **AI naming (opt-in, BYOK)** — Anthropic, OpenAI, Gemini, DeepSeek, OpenRouter, Ollama, LM Studio,
  and any custom OpenAI-compatible endpoint; output always sanitized to a valid Salesforce name.
- **Diff review panel** — component-grouped, collapsible, per-label checkboxes, live-validated
  editable names, VS Code native diff editor, LWC sidecar preview, filter box.
- **Streaming apply** — O(1-file) memory; CustomLabels XML merge that never overwrites existing
  labels; automatic LWC `@salesforce/label` import + getter; repeated-string reuse.
- **Folder Audit Report (free)** — total counts, breakdown by component type, top-offenders table,
  per-file drill-down, plus an "≈ N hrs estimated manual conversion" cost-estimate KPI.
- **Bulk convert** *(Pro)* — apply conversions across all files from an Audit Report.
- **Deploy to Org** *(Pro)* — one-click deploy with a production hard-block; scoped entry points
  (Last Conversion / This File / This Folder); manifest-based deploy for large change sets.
- **Audit CSV export** *(Pro)* — file path, component, string count, plus the estimate summary.

For per-version detail, see the [Changelog](CHANGELOG.md) (canonical release notes live on the
[Marketplace](https://marketplace.visualstudio.com/items/ramprasad94.labelalchemy/changelog) and
[GitHub Releases](../../releases)).

---

## 🟡 In progress / next up

- **Project-context-aware AI naming** *(Pro)* — richer names that consider the broader
  component/project context, beyond today's light deterministic context hints.
- **Conflict / duplicate-label detection** — before writing XML, flag strings whose value already
  matches an existing label under a different name; offer reuse or proceed.

---

## 🔵 Planned / exploring

Directional ideas, roughly in order of interest — upvote in
[Ideas](../../discussions/categories/ideas) to push these up:

- **Org-wide string dedup & label reuse** — propose an existing label before creating a new one,
  across the org (today's reuse is within a single scan).
- **Flow labels** — detect hard-coded text in screen Flows.
- **CI / PR scan mode** — a CLI/Action that scans files changed in a branch and comments on PRs
  with findings (team-licensing use case).
- **Bulk folder scan summary report** — a richer shareable report on top of the folder scan.
- **Multi-language label generation** — generate translations for labels via an LLM.

---

*This roadmap is a living document and will change. Nothing here is a promise of a specific feature
or date. Thanks for helping shape Label Alchemy! 🙏*
