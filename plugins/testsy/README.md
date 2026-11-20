# Testsy

Testsy runs QA tests written in plain English on websites and on iOS and Android apps, and returns a verdict for every check with its evidence: a replay, video, the values it saw, console and network.

Documentation: https://testsy.dev/docs/mcp/ · Sign up: https://app.testsy.dev

Install it in Claude Code:

```text
/plugin marketplace add testsy-ai/testsy-claude-plugins
/plugin install testsy@testsy
```

In the Claude desktop app, add the same repository as a marketplace under Customize, then install Testsy from it. The plugin brings the three skills and the Testsy connection (https://app.testsy.dev/mcp). There is no key to set: the first time Claude calls a Testsy tool you sign in in the browser and choose the workspace (in Claude Code, /mcp shows the connection and its sign-in). For CI or another headless session, add the connection with a workspace API key instead (replace YOUR_API_KEY; the plugin itself reads no key):

```sh
claude mcp add --transport http testsy https://app.testsy.dev/mcp --header "Authorization: Bearer YOUR_API_KEY"
```

To load a local copy, run `claude --plugin-dir /absolute/path/to/this/folder`.

Keep API keys in your secret store, out of prompts and version control. A run uses the workspace allowance and performs real actions on the site or app it is pointed at, so use it on apps and accounts you are allowed to test. These integration files are MIT licensed.
