# Testsy

Check releases, investigate failed runs and preserve regression coverage.

Documentation: https://testsy.dev/docs/mcp/

Install it in Claude Code:

```text
/plugin marketplace add testsy-ai/testsy-claude-plugins
/plugin install testsy@testsy
```

In the Claude desktop app, add the same repository as a marketplace under Customize, then install Testsy from it. The plugin brings the three skills and the Testsy connection (https://app.testsy.dev/mcp). There is no key to set: the first time Claude calls a Testsy tool you sign in in the browser and choose the workspace (in Claude Code, /mcp shows the connection and its sign-in). For CI or another headless session, add the connection with a workspace API key instead:

```sh
claude mcp add --transport http testsy https://app.testsy.dev/mcp --header "Authorization: Bearer $TESTSY_AI_API_KEY"
```

To load a local copy, run `claude --plugin-dir /absolute/path/to/this/folder`.

This is an integration package prepared for local testing. A directory listing or live-client validation is not implied. Keep API keys out of prompts and version control. Runs use the workspace allowance and perform the test's actions. MIT applies to these integration files only.
