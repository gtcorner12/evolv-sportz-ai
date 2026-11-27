# EvolvSportz for AI assistants

Use [EvolvSportz](https://evolvsportz.com) from your AI assistant. Coaches plan practices from
animated drills, and club, site and team admins set up sites, teams, roles and invites by
chatting.

Nothing runs on your computer. EvolvSportz hosts an MCP server, and your assistant connects
to it and asks you to sign in to EvolvSportz once. The assistant always acts as you, with your
permissions, and every admin change it makes is logged.

**Server URL:** `https://evolvsportz-qtae-staging.azurewebsites.net/api/mcp`

> This currently points at the EvolvSportz staging site while production is set up.

## Claude Code and Cowork (plugin marketplace)

```
/plugin install evolvsportz --marketplace gtcorner12/evolv-sportz-ai
```

Or in two steps:

```
/plugin marketplace add gtcorner12/evolv-sportz-ai
/plugin install evolvsportz@evolvsportz
```

Then run `/mcp` and choose **evolvsportz** to sign in.

## Claude (web, desktop and mobile)

1. On claude.ai, open **Settings → Connectors** and choose **Add custom connector**.
2. Name it EvolvSportz and paste the server URL.
3. Choose **Connect**, sign in to EvolvSportz and approve.

## ChatGPT

1. On chatgpt.com, open **Plugins** in the sidebar, choose **Add**, then **Add custom MCP server**.
2. Paste the server URL and set authentication to **OAuth**.
3. Create it, then sign in to EvolvSportz and approve.

Saving changes needs a Business, Enterprise or Edu plan. On Business workspaces, only admins
can add custom servers.

## Google Gemini

1. On gemini.google.com, open **Settings → Connected Apps** and choose **Add a custom app**.
2. Paste the server URL, choose **Next**, then sign in to EvolvSportz and approve.

Google currently limits custom apps to personal accounts in the US, in English.

## Apple Intelligence

Not supported yet: Apple Intelligence doesn't connect to outside MCP servers.

## What's in this repository

| Path | What it is |
| --- | --- |
| `.claude-plugin/marketplace.json` | The Claude plugin marketplace |
| `plugins/evolvsportz/` | The plugin: it registers the EvolvSportz MCP server (`.mcp.json`) |

## License

[MIT](LICENSE)
