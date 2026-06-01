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
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    },
    "blinkit-mcp": {
      "command": "uv",
      "args": [
        "run",
        "--with", "mcp[cli],playwright",
        "python",
        "C:\\path\\to\\Downloads\\blinkit-mcp-main\\blinkit-mcp-main\\main.py"
      ],
      "cwd": "C:\\path\\to\\Downloads\\blinkit-mcp-main\\blinkit-mcp-main",
      "env": {
        "HEADLESS": "false"
      }
    }
  }

      }
      ```

      ### Reference Links
      - NPM Package: https://www.npmjs.com/package/blinkit-mcp
