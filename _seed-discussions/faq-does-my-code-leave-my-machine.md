# Does my code leave my machine? (Privacy & data)

**Q: Does Label Alchemy send my code to a server?**

**In the default (deterministic) mode: no.** The scanner, naming engine, and apply step are all
local. Nothing is sent anywhere — it works fully offline.

**In AI naming mode with a cloud provider:** the **string values** from your source files are sent
to the LLM provider you configured (Anthropic, OpenAI, etc.) to get name suggestions. The file-type
context and a surrounding code fragment may also be sent to help the model name accurately. Full
file contents, file paths, and org credentials are **not** sent.

**Want AI naming but zero data leaving your machine?** Use **Ollama** or **LM Studio** as your
provider — both run the model locally, so nothing leaves your machine even in AI mode.

**Other privacy facts:**
- **No telemetry.** Label Alchemy does not phone home or collect usage statistics.
- **Secrets are encrypted.** API keys and license keys live in VS Code's encrypted secret storage
  (`vscode.SecretStorage`) — never in `settings.json`, never logged, never in plain text.
- The **only** external connections are license validation (Lemon Squeezy) and LLM API calls when
  you've turned AI naming on.

📖 Full privacy policy: https://docs.labelalchemy.dev/privacy
