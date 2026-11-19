# Testsy

Check releases, investigate failed runs and preserve regression coverage.

Documentation: https://testsy.dev/docs/mcp/

Install it in Claude Code:

```text
/plugin marketplace add testsy-ai/testsy-claude-plugins
/plugin install testsy@testsy
```

Set TESTSY_AI_API_KEY securely in the environment first. To load a local copy instead, run `claude --plugin-dir /absolute/path/to/this/folder`. The bundled .mcp.json supplies the remote HTTP server. Restart the session and inspect /mcp and /skills.

This is an integration package prepared for local testing. A directory listing or live-client validation is not implied. Keep API keys out of prompts and version control. Runs use the workspace allowance and perform the test's actions. MIT applies to these integration files only.
