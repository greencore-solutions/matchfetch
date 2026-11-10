# matchfetch

> Words in, barcode out, with how sure. Give a shopper's phrase or a merchant's offer line and a country; get back one barcode with a confidence, or the candidates when it is ambiguous (never a guess), or unknown. Every result carries four verification readings (source authority, disagreement, freshness and authorisation) and one result: verified, listed, stale or unknown. Price and stock are never verified from the record: they are read live, or unknown.

Built and run by [wefetch](https://wefetch.ai/). This is the public connect kit, MIT. It holds no deploy code and no keys.

## Connect

- Endpoint: `https://matchfetch.ai/mcp` (MCP, streamable HTTP)
- Agent card: `https://matchfetch.ai/.well-known/agent-card.json` (copy in this repo, `agent-card.json`)
- For agents: https://matchfetch.ai/llms.txt
- Site: https://matchfetch.ai/
- Official MCP Registry: `ai.matchfetch/matchfetch` (`server.json` in this repo)

Any client that speaks streamable HTTP:

```json
{
  "url": "https://matchfetch.ai/mcp",
  "transport": "streamable-http"
}
```

Claude Code:

```bash
claude mcp add --transport http matchfetch https://matchfetch.ai/mcp
```

List the tools with `python examples/generic_mcp_client.py`.

## Tools

| Tool | What it does |
|---|---|
| `match_product` | Words in, barcode out, with how sure. |

Artificial intelligence makes mistakes. Check what matters.
