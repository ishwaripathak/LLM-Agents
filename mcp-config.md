# MCP Connectors Configuration

This file documents the MCP (Model Context Protocol) connectors used with Claude Desktop for LLM Agent workflows.

---

## 1. Blinkit MCP

**Purpose:** Grocery shopping and ordering via Blinkit

### Download & Installation
- **GitHub Repo:** https://github.com/anshuopinion/blinkit-mcp
- **NPM Package:** https://www.npmjs.com/package/blinkit-mcp
- **Install command:** `npx -y blinkit-mcp`

### Configuration (`claude_desktop_config.json`)
```json
{
  "mcpServers": {
    "blinkit-mcp": {
      "command": "npx",
      "args": ["-y", "blinkit-mcp"]
    }
  }
}
```

### Reference Links
- NPM Package: https://www.npmjs.com/package/blinkit-mcp
- Blinkit Website: https://blinkit.com

### Capabilities
- Search for products
- Add/remove items from cart
- Check cart contents
- Manage delivery addresses
- Login and checkout

---

## 2. Playwright MCP

**Purpose:** Browser automation tasks (navigating websites, filling forms, clicking elements)

### Download & Installation
- **GitHub Repo:** https://github.com/microsoft/playwright-mcp
- **NPM Package:** https://www.npmjs.com/package/@playwright/mcp
- **Install command:** `npx -y @playwright/mcp`
- **Install browsers:** `npx playwright install`

### Configuration (`claude_desktop_config.json`)
```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@playwright/mcp"]
    }
  }
}
```

### Reference Links
- NPM Package: https://www.npmjs.com/package/@playwright/mcp
- Playwright Docs: https://playwright.dev
- GitHub: https://github.com/microsoft/playwright-mcp

### Capabilities
- Navigate to URLs
- Click, type, fill forms
- Take screenshots
- Snapshot page accessibility tree
- Handle browser tabs
- Upload/drop files

---

## Combined Configuration

```json
{
  "mcpServers": {
    "blinkit-mcp": {
      "command": "npx",
      "args": ["-y", "blinkit-mcp"]
    },
    "playwright": {
      "command": "npx",
      "args": ["-y", "@playwright/mcp"]
    }
  }
}
```

---

> **Note:** These connectors must remain configured in `claude_desktop_config.json` to function. Claude's memory only stores preferences — the actual MCP server config is required for tool execution.
