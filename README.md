# Reverse email lookup by Senderscope

Reverse email lookup, email finder and email verifier as a plugin for Claude. See who owns a work email (name, title, seniority, company, LinkedIn), find a work email from a name and company domain or a LinkedIn profile, and run email verification on any address with [Senderscope](https://senderscope.app), without leaving Claude.

## Install

```sh
/plugin marketplace add senderscope/plugin
/plugin install senderscope@senderscope
```

The plugin adds the remote MCP server `https://senderscope.app/mcp` and a skill. The first tool call opens senderscope.app for sign-in and consent. Without the plugin, add the same URL as a custom connector in Claude (Settings → Connectors) or run `claude mcp add --transport http senderscope https://senderscope.app/mcp`.

## Tools

| Tool | What it does | Cost |
| --- | --- | --- |
| `get_account` | Your plan and credits left | free |
| `lookup_email` | Work email → name, title, seniority, company, LinkedIn and deliverability | 1 credit if found |
| `find_email` | Name + company domain, or a LinkedIn URL → a verified work email | 1 credit if found |
| `verify_email` | Deliverable, accept-all, role or personal address, SPF and DMARC | 1 credit per answer |
| `list_lookups` | Your recent lookups from any source | free |
| `get_lookup` | One past result, without a new lookup | free |

Every plan works, and a free account comes with 5 lookups to try it, no card. Professional data only; people can opt out at https://senderscope.app/opt-out/.

[Website](https://senderscope.app) · [MCP & API](https://senderscope.app/mcp-api/) · [Privacy](https://senderscope.app/privacy/) · MIT license
