<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img alt="Your coding agent connects to mcpmaster, one local MCP endpoint in front of github, stripe, linear, files and any other API. It runs commands through mcpv, which decrypts secrets in memory, injects them into one process and shows the agent only [redacted]." src="assets/banner-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://mcpmaster.sh/"><img alt="Cloud: mcpmaster.sh" src="https://img.shields.io/badge/cloud-mcpmaster.sh-8b7bff"></a>
  <a href="https://mcpmastersh.github.io/mcpmaster/"><img alt="mcpmaster website" src="https://img.shields.io/badge/website-mcpmaster-121216"></a>
  <a href="https://mcpmastersh.github.io/mcpv/"><img alt="mcpv website" src="https://img.shields.io/badge/website-mcpv-121216"></a>
  <img alt="License: Apache-2.0" src="https://img.shields.io/badge/license-Apache--2.0-121216">
</p>

We build small, local-first tools that let AI coding agents do real work
**without handing them the keys to everything**. Both run on your machine,
need no account and are free and open source.

## 🧰 Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/mcpmastersh/mcpmaster">
        <picture>
          <source media="(prefers-color-scheme: dark)" srcset="assets/mcpmaster-logo-dark.svg">
          <img src="assets/mcpmaster-logo-light.svg" width="44" height="44" alt="" align="left">
        </picture>
      </a>
      <h3><a href="https://github.com/mcpmastersh/mcpmaster">mcpmaster</a></h3>
      <b>Connect your agents to anything.</b><br>
      One local MCP endpoint for every OpenAPI, GraphQL and MCP server you
      use, with a web UI to manage them.
      <br><br>
      🔌 &nbsp;One connection for every API and MCP server<br>
      🧠 &nbsp;One <code>execute</code> tool, ~515 tokens instead of ~401,000<br>
      🧪 &nbsp;Snippets run sandboxed in QuickJS (WebAssembly)<br>
      🛡️ &nbsp;Block rules, read-only mode and review<br>
      <br>
      <pre lang="sh">npx mcpmaster up</pre>
      <a href="https://github.com/mcpmastersh/mcpmaster">Repository</a> ·
      <a href="https://mcpmastersh.github.io/mcpmaster/">Website</a> ·
      <a href="https://www.npmjs.com/package/mcpmaster">npm</a>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/mcpmastersh/mcpv">
        <picture>
          <source media="(prefers-color-scheme: dark)" srcset="assets/mcpv-logo-dark.svg">
          <img src="assets/mcpv-logo-light.svg" width="44" height="44" alt="" align="left">
        </picture>
      </a>
      <h3><a href="https://github.com/mcpmastersh/mcpv">mcpv</a></h3>
      <b>Your agent uses the keys. It never sees them.</b><br>
      Offline, encrypted secrets for AI agents. Keep <code>mcpm://</code>
      references in your <code>.env</code>; values stay in the vault.
      <br><br>
      🔐 &nbsp;AES-256-GCM vault, master key in the OS keychain<br>
      🧬 &nbsp;Values injected in memory into one process<br>
      🙈 &nbsp;Every secret in the output becomes <code>[redacted]</code><br>
      📴 &nbsp;No server, no account, no network<br>
      <br>
      <pre lang="sh">npx @mcpmastersh/mcpv init</pre>
      <a href="https://github.com/mcpmastersh/mcpv">Repository</a> ·
      <a href="https://mcpmastersh.github.io/mcpv/">Website</a> ·
      <a href="https://www.npmjs.com/package/@mcpmastersh/mcpv">npm</a>
    </td>
  </tr>
</table>

## 🔗 Better together

Each tool keeps one kind of key out of the chat:

| | Your agent can | Your agent never sees |
| --- | --- | --- |
| **mcpmaster** | call GitHub, Stripe, Linear and any API you connect | the API credentials, which are used, never shown, and stripped from responses |
| **mcpv** | run your app, tests and scripts with real secrets | the values, which reach one process in memory and print as `[redacted]` |

```bash
$ mcpv run -- npm run dev
db    postgres://app:[redacted]@db:5432
✓ listening on :3000
```

## 🤖 Works with

<p>
  <img src="assets/icons/claude.svg" width="16" height="16" alt=""> Claude Code &nbsp;·&nbsp;
  <img src="assets/icons/codex.svg" width="16" height="16" alt=""> Codex &nbsp;·&nbsp;
  <img src="assets/icons/cursor.svg" width="16" height="16" alt=""> Cursor &nbsp;·&nbsp;
  <img src="assets/icons/claude.svg" width="16" height="16" alt=""> Claude Desktop &nbsp;·&nbsp;
  <img src="assets/icons/vscode.svg" width="16" height="16" alt=""> VS Code &nbsp;·&nbsp;
  <img src="assets/icons/windsurf.svg" width="16" height="16" alt=""> Windsurf &nbsp;·&nbsp;
  <img src="assets/icons/opencode.svg" width="16" height="16" alt=""> OpenCode &nbsp;·&nbsp;
  <img src="assets/icons/mcp.svg" width="16" height="16" alt=""> any MCP client
</p>

## ☁️ mcpmaster Cloud

Don't want to run it yourself? **[mcpmaster.sh](https://mcpmaster.sh/)** is the
hosted version, built on the same integration engine. Nothing to install.

- ✅ A hosted endpoint for every agent, on any machine
- ✅ Workspaces with team roles, private workspaces behind OAuth
- ✅ Agent Secrets, using the same `mcpm://` addresses as mcpv
- ✅ Audit trail and instant access revocation

<p><a href="https://mcpmaster.sh/"><b>Start the 14-day trial →</b></a></p>

---

<sub>Found a bug or have an idea? Open an issue in
<a href="https://github.com/mcpmastersh/mcpmaster/issues">mcpmaster</a> or
<a href="https://github.com/mcpmastersh/mcpv/issues">mcpv</a>. Brand assets live in each repo's <code>brand/</code> folder.</sub>
