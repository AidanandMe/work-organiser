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

## Demo

Built and demoed via video for the Anthropic Claude Hack Night, London — 
February 2026.

**Use case:** An AI/Digital Humanities educator and entrepreneur asks 
Claude to scan her 5 active project folders, find relevant upcoming 
academic conferences and submission deadlines, and populate her task 
board for the week — all in a single prompt.

## Tech Stack

- [Skybridge](https://skybridge.sh) — MCP app framework
- Supabase — database and storage
- React + TypeScript — frontend
- Express — backend server
- Anthropic Claude — AI layer via MCP

## Setup

See `.env.example` for required environment variables.
```bash
pnpm install
pnpm dev
```

## Team

Built by **Larissa** — Anthropologist, AI educator, digital humanities researcher

