# MCP Connectors Configuration

This file documents the MCP (Model Context Protocol) connectors used with Claude Desktop for LLM Agent workflows.

---

## 1. Blinkit MCP

**Purpose:** Grocery shopping and ordering via Blinkit

### Download & Installation
- **GitHub Repo:** https://github.com/hereisSwapnil/blinkit-mcp
- - **NPM Package:** https://www.npmjs.com/package/blinkit-mcp
  - - **Install command:** `npx -y blinkit-mcp`
   
    - ### Configuration (`claude_desktop_config.json`)
    - ```json
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
