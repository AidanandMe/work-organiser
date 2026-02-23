# Work Organiser 🗂️

An AI-powered personal work management assistant built on top of Claude, 
using the Model Context Protocol (MCP).

## What it does

Work Organiser connects Claude directly to your local project folders 
and a live task board, turning Claude into a proactive work assistant 
that understands your real projects and priorities.

**In one conversation, Claude can:**
- 📁 Read your local project folders and subfolders
- 🔍 Search the web for relevant conference deadlines, calls for papers, 
  and events aligned with your work
- ✅ Automatically create prioritised tasks with due dates on your board
- 🗓️ Cross-reference opportunities against your active projects

**Use case:** An AI/Digital Humanities educator and entrepreneur asks 
Claude to scan her 5 active project folders, find relevant upcoming 
academic conferences and submission deadlines, and populate her task 
board for the week — all in a single prompt.

Requirements

Node.js ≥ 24.13.0
pnpm
A Cloudflare account (free, no sign-up required for temporary tunnels)


Setup
1. Clone and install
bashgit clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
pnpm install
2. Configure environment
Copy the example env file and fill in your credentials:
bashcp .env.example .env
Edit .env with your Supabase and Clerk keys (see .env.example for required variables).
3. Start the dev server
bashpnpm dev
The server runs on http://localhost:3000 by default.

Connecting to Claude
Because this app runs locally, you need a public URL to connect it to Claude. Use a Cloudflare quick tunnel — it's free and requires no account.
Each time you start the server:
Step 1 — Start the dev server (in one terminal):
bashpnpm dev
Step 2 — Open a new terminal and start the tunnel:
bashnpx cloudflared tunnel --url http://localhost:3000
You'll see output like:
Your quick Tunnel has been created! Visit it at:
https://some-random-words.trycloudflare.com

⚠️ Important: This URL changes every time you run the tunnel. You must update your Claude connector each session.

Step 3 — Add the connector in Claude:

Go to Claude.ai → Settings → Connectors
Add or update the MCP connector URL:

   https://your-tunnel-url.trycloudflare.com/mcp

The tool will appear as "Working Organiser" in Claude


Using the app
Once connected, you can ask Claude things like:

"Show me my task board"
"What conferences are coming up?"
"Add a new task: prepare ZzORP pitch deck"
"What deadlines do I have this week?"


Why the URL changes
Cloudflare quick tunnels are temporary by design — the URL regenerates every time the tunnel restarts. This is fine for development and demos.
For a permanent URL, you can set up a named Cloudflare tunnel with a custom domain — but this requires a Cloudflare account and is beyond the scope of this prototype.

Project structure
├── src/
│   └── ...          # Skybridge MCP app source
├── .env.example     # Environment variable template
├── package.json
└── README.md

Built with

Skybridge — Alpic's open-source MCP framework
Claude — Anthropic's AI assistant
Cloudflare Tunnels — for local-to-public URL bridging
Supabase — backend storage
Clerk — authentication


Submitted to
Claude Code London Hack Night — "Build an MCP App"
Theme: Solve an everyday at-work issue
Solo Team: The Anthropologist
