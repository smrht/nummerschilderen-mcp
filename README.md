<img src="logo-400.png" alt="Nummerschilderen.com shop advisor logo" width="96" height="96">

# Nummerschilderen.com shop advisor MCP server

**Search paint-by-number kits, get size and price advice for your own photo, shop info. No login.**

Remote MCP server: `https://mcp.nummerschilderen.com/mcp` (Streamable HTTP) · Website: [nummerschilderen.com](https://nummerschilderen.com/)

## What it does

The shop advisor of Nummerschilderen.com lets an AI assistant search the live catalogue of paint-by-number kits (schilderen op nummer), advise on canvas size and price for a kit made from your own photo based on its resolution and aspect ratio, and return the shop's current delivery, returns, FAQ and contact information. Prices come live from the shop.

Read-only and without login. It cannot look up or change orders; ordering happens on nummerschilderen.com.

## Connect

- **Server URL:** `https://mcp.nummerschilderen.com/mcp`
- **Transport:** Streamable HTTP
- **Authentication:** No authentication. Public, read-only endpoint.

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the server URL.

**Claude Code:**

```bash
claude mcp add --transport http nummerschilderen https://mcp.nummerschilderen.com/mcp
```

**Cursor, VS Code, Cline, Windsurf and other clients** (`mcp.json` / `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "nummerschilderen": {
      "type": "http",
      "url": "https://mcp.nummerschilderen.com/mcp"
    }
  }
}
```

Cline uses `"type": "streamableHttp"`; see [llms-install.md](llms-install.md).

## Tools

| Tool | What it does |
|---|---|
| `search_products` | Search kits by theme, size or price; live prices and links. |
| `photo_size_advice` | Size and price advice for a custom kit from a photo's resolution. |
| `shop_info` | Delivery, returns, FAQ and contact text. |

## Example prompts

- Find a paint-by-number kit with a landscape, 40x50 cm.
- My photo is 3024x4032 pixels. Which canvas size works for a custom kit, and what does it cost?
- How long does delivery to Belgium take?

## Links

- Website: https://nummerschilderen.com/
- Documentation: https://nummerschilderen.com/ai-assistent/
- Privacy policy: https://nummerschilderen.com/privacybeleid/
- Terms: https://nummerschilderen.com/algemene-voorwaarden/

## Keywords

paint by numbers, custom paint by number from photo, paint by number kit, craft shop, canvas painting kit.

Nederlands: schilderen op nummer, schilderen op nummer eigen foto, nummerschilderen, schilderij op nummer, hobbypakket schilderen.

## More MCP servers by Samautomation

- [Scamchecker.nl](https://scamchecker.nl/): Check a suspicious email, SMS, WhatsApp message or link for scam signals (Netherlands, Belgium). ([listing](https://github.com/smrht/scamchecker-mcp))
- [Klussenbeheer](https://samdesk.nl/klussenbeheer/): Job management for Dutch service companies: jobs, customers, planning, quotes and invoices. ([listing](https://github.com/smrht/klussenbeheer-mcp))
- [Muziek maken met AI](https://muziekmakenmetai.nl/): Make an original song from a prompt or your own lyrics. Two versions per song, MP3 download. ([listing](https://github.com/smrht/muziekmakenmetai-mcp))
- [Beheer je WP](https://beheerjewp.nl/): Manage a WordPress site from your AI assistant: read, search, propose edits, Search Console data. ([listing](https://github.com/smrht/beheerjewp-mcp))
- [UlazAI Media](https://ulazai.com/): Create private AI images with your UlazAI account: pick a model, confirm, generate, download. ([listing](https://github.com/smrht/ulazai-mcp))
- [Backlinkswinkel](https://backlinkswinkel.nl/): Search Dutch websites for backlinks, check metrics and prices, order after confirmation, track. ([listing](https://github.com/smrht/backlinkswinkel-mcp))
- [Backlinksbeheer](https://backlinksbeheer.nl/): Read your stored backlinks, link checks and lost-link alerts per domain. Read-only. ([listing](https://github.com/smrht/backlinksbeheer-mcp))
- [Samautomation Video](https://samautomation.work/): Render an MP4 from your own images, clips, voice-over and timed captions. JSON to video. ([listing](https://github.com/smrht/samautomation-video-mcp))
- [PDF Samenvoegen](https://pdfsamenvoegen.nl/): Merge your own PDFs in a confirmed order and get one downloadable PDF. ([listing](https://github.com/smrht/pdfsamenvoegen-mcp))
- [Diamond Painting Converter](https://diamondpaintingconverter.com/): Find your purchased diamond painting patterns and download the PDF with DMC colour legend. ([listing](https://github.com/smrht/diamondpaintingconverter-mcp))
- [DiamondPaintingWinkel.nl shop advisor](https://diamondpaintingwinkel.nl/): Search diamond painting kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/diamondpaintingwinkel-mcp))
- [AI Rechtshulp](https://ai-rechtshulp.nl/): Search Dutch and EU case law with ECLI sources and verify quotes against the judgment. ([listing](https://github.com/smrht/ai-rechtshulp-mcp))
- [SamDesk Support](https://samdesk.nl/support/plugin/): Read your SamDesk support inbox, find customer agreements and draft replies. Read-only. ([listing](https://github.com/smrht/samdesk-support-mcp))

## Publisher

Samautomation, Wognum, the Netherlands · https://samautomation.work

This repository holds the public listing (README, `server.json`, install notes). The server itself is hosted by the publisher; there is nothing to install or build.
