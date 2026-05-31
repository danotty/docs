# Local Preview Guide for Mintlify Documentation

## Installation

### Option 1: Install Mintlify CLI globally with npm
```bash
npm i -g mintlify
```

### Option 2: Install with yarn
```bash
yarn global add mintlify
```

### Option 3: Install with pnpm
```bash
pnpm add -g mintlify
```

## Running Local Development Server

Once installed, navigate to your docs directory and run:

```bash
cd d:\signalarkdocs
mintlify dev
```

This will:
- Start a local development server (usually at http://localhost:3000)
- Watch for file changes and auto-reload
- Show you exactly how your docs will look when deployed

## Troubleshooting

### If `mintlify` command is not found:
- Make sure npm's global bin directory is in your PATH
- Try running: `npx mintlify dev` instead

### If you get port conflicts:
- Mintlify will automatically try the next available port
- Or specify a custom port: `mintlify dev --port 3001`

### If you see errors about missing files:
- Make sure you're in the correct directory (d:\signalarkdocs)
- Verify docs.json exists in the current directory

## What to Check in Preview

1. **Navigation**: Verify "MCP Automation" appears in the sidebar
2. **MCP Pages**: Click through all 9 MCP documentation pages
3. **Updated Content**: Spot-check a few updated pages to ensure content is current
4. **Links**: Test internal links between pages
5. **Code Blocks**: Verify code examples render correctly
6. **Tables**: Check that tables in tool-reference.mdx display properly

## Stopping the Server

Press `Ctrl+C` in the terminal to stop the development server.
