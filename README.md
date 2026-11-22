# Cynthia, by Planet Leads — Cursor Plugin

![Cynthia, by Planet Leads](assets/logo.svg)

**Cynthia, by Planet Leads — created by Ramel Hyman.**

Cynthia is a verified-answer AI. She answers questions about Planet Leads
Academy's 35 courses and Planet Leads services **verbatim from an
owner-approved fact store** — and when a question isn't covered by a verified
fact, she says she doesn't know instead of guessing.

## What this plugin does

This plugin is a **thin connector**. It contains no Cynthia server code and no
fact store. Installing it adds one MCP server to Cursor — `cynthia` — which
connects to Cynthia's live hosted MCP server:

```
https://cynthia-mcp-server.onrender.com/mcp
```

Once installed, Cursor's agent can call Cynthia's tools to ask her questions
and get verified answers about:

- Planet Leads Academy's 35 courses (subjects, lesson counts, prices, bundles)
- Planet Leads services
- Cynthia herself — her capabilities, channels, and how to work with her

## Install

1. In Cursor, open the Marketplace and search for **Cynthia, by Planet Leads**
   (`cynthia-by-planet-leads`), or install this plugin from its repository.
2. Click **Install**. No API key or configuration is required — the plugin's
   `mcp.json` points at Cynthia's hosted server, and the free tier of that
   server answers right away.
3. Ask Cursor's agent a question about Planet Leads Academy or Planet Leads,
   and it can route the question to Cynthia.

## Configuration

None required. The entire configuration is the bundled `mcp.json`:

```json
{
  "mcpServers": {
    "cynthia": {
      "url": "https://cynthia-mcp-server.onrender.com/mcp"
    }
  }
}
```

There are no secrets, tokens, or variables in this plugin.

## Honest notes

- **Answers come from a verified fact store.** Cynthia answers only from
  facts her owner has approved, word for word. She does not improvise,
  speculate, or fill gaps — an uncovered question gets an honest
  "I don't know."
- **Cynthia is a hosted service.** This plugin is only a pointer to her live
  server; Cynthia herself, her fact store, and her other channels stay hosted
  and proprietary. Nothing of hers is included in this repository.
- **Planet Leads Academy is not accredited and awards no degrees.** Cynthia's
  facts state this plainly, and so do we.
- **Paid Cynthia tiers exist** (for example, paid per-call access and
  white-label tiers) and are sold through Planet Leads' existing channels.
  This plugin covers the free hosted connection only.
- This plugin's own code (the manifest, MCP config, docs, and logo) is
  released under the **MIT License** — see [LICENSE](LICENSE). The MIT license
  applies to this wrapper only, not to Cynthia or her hosted service.

## About Planet Leads

Planet Leads 🚀 — created by Ramel Hyman. Cynthia is "Cynthia, by Planet
Leads — created by Ramel Hyman."

- Academy courses, bundles, and Cynthia products:
  https://planetleads.gumroad.com
- Contact: planetleads1@gmail.com
