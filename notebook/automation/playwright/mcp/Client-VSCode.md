# Configure Playwright MCP in VS Code  

This guide explains how to set up the Playwright MCP server in VS Code and customize its configuration to use a locally installed Chromium browser instead of Google Chrome.  

> **Prerequisites**  
> * GitHub Copilot Chat (vscode built-in)  
> * Node.js - required to run the Playwright MCP server  
> * Chromium - optional for customization  

## Install Playwright MCP    
Follow the official Playwright documentation under the VS Code section to install and configure the MCP server: https://playwright.dev/docs/getting-started-mcp#vs-code  
  
Once the setup is complete, VS Code should have an MCP configuration file(`mcp.json`) containing the Playwright MCP server configuration.  

## Optional Customization: Use Local Chromium
Playwright MCP use Google Chrome as default browser configuration. If you prefer to use an existing Chromium installation on your machine, you can explicitly configure the browser executable path.  

1. Open the `mcp.json` configuration file in VS Code.
2. Locate the Playwright MCP server configuration, identified by `@playwright/mcp@latest`.
3. Add the following arguments to the `args` array:
   - `--browser=chromium`
   - `--executable-path=/usr/bin/chromium`


After modification, the configuration should look similar to the following:  

```json
{
  "servers": {
    "microsoft/playwright-mcp": {
      "type": "stdio",
      "command": "npx",
      "args": [
        "@playwright/mcp@latest",
        "--browser=chromium",
        "--executable-path=/usr/bin/chromium"
      ],
      "gallery": "https://api.mcp.github.com",
      "version": "0.0.1-seed"
    }
  },
  ......
}
```

**Note:** The Chromium executable path may vary depending on your Linux distribution. Update `--executable-path` accordingly. To check the Chromium executable path, run:  
```bash
which chromium
```


