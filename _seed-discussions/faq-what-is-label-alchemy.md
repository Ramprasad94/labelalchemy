# What does Label Alchemy do?

**Q: What is Label Alchemy, and what problem does it solve?**

Label Alchemy is a VS Code extension that converts hard-coded strings in Salesforce source files
(Apex, LWC, Aura) into Custom Labels. It finds the strings, generates valid Salesforce label names,
shows you a diff, and writes the changes only when you approve.

**What it supports:**
- Apex classes (`.cls`)
- LWC JavaScript (`.js` inside an `lwc/` bundle) and LWC HTML (`.html`)
- Aura JavaScript (`.js`) and Aura markup (`.cmp`, `.app`)

**The workflow in short:**
1. **Scan** a file or a whole folder — it finds user-facing strings and skips API names, SOQL,
   debug calls, and commented-out code.
2. **Name** — valid Snake_Case names (≤40 chars) are generated locally; every name is editable.
3. **Review** — a diff panel and VS Code's native diff editor show exactly what will change.
4. **Apply** — your source files and `CustomLabels.labels-meta.xml` are updated; for LWC HTML the
   sibling `.js` getter/import is added automatically.

It works with any Salesforce DX project structure regardless of org type, and runs alongside the
Salesforce Extensions Pack.

📖 Full docs: https://docs.labelalchemy.dev · 🗺️ Roadmap: see [ROADMAP.md](../../blob/main/ROADMAP.md)
