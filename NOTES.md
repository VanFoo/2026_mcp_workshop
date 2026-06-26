# Teaching Notes

## User Profile
- New to MCP — no prior exposure
- Prefers Python (FastMCP v2)
- Wants a hands-on workshop style: learn by doing
- Goal: build a server AND an agent that uses it

## Workshop Structure (4 lessons)
1. **MCP Foundations** — architecture, primitives, communication flow (conceptual + quiz)
2. **Your First FastMCP Server** — build a Notes MCP server from scratch
3. **Primitives in Depth** — add resources and prompts to the server; use MCP Inspector
4. **Build an Agent** — wire the server into a Claude-powered agent that completes a real task

## Capstone Project
A **Notes & Tasks MCP Server** — simple, real-world, demonstrates all three primitives:
- Tools: `create_note`, `list_notes`, `delete_note`
- Resources: `notes://all`, `notes://{id}`
- Prompts: `summarize_notes` template

Agent task: "Summarize all my notes and create a new one with the summary."

## Preferences
- User did not express preference against community participation
