# Do I need an AI/LLM (or an API key) to use Label Alchemy?

**Q: Is AI required? What is BYOK?**

**No — AI is not required.** The default naming mode is fully **deterministic**: it runs locally
with no API key, no network call, and no cost. It splits each string into meaningful words, strips
filler words, detects a context hint from the surrounding code (error message, placeholder, button,
etc.), applies your label prefix if configured, and enforces the 40-character Salesforce name limit.

**AI naming is opt-in (BYOK = Bring Your Own Key).** Label Alchemy has no AI subscription of its
own — if you enable AI naming, you provide an API key for whichever provider you choose. Your key is
stored in VS Code's encrypted secret storage and used only to call that provider on your behalf.

**Supported providers:** Anthropic (Claude), OpenAI, Google Gemini, DeepSeek, OpenRouter, Ollama,
LM Studio, and any custom OpenAI-compatible endpoint.

**Can I use AI naming for free?** Yes — per-file AI naming works on the free tier, and with
**Ollama** or **LM Studio** the model runs locally at $0. **Project-wide AI naming** (which reuses
your existing labels and follows your naming convention across the codebase) requires a license.

Either way, every suggested name is **editable** in the diff panel before you approve, and the
Approve button stays disabled until all names are valid — so the model can never push an invalid
Salesforce name into your codebase.

📖 Provider setup guide: https://docs.labelalchemy.dev/providers
