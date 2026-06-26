# Mission: Model Context Protocol (MCP)

## Why
Build a practical, end-to-end understanding of MCP — from what it is, to running a real Python server, to wiring it into an AI agent. The goal is to be able to design and ship an MCP server that gives a Claude-powered agent meaningful real-world capabilities.

## Success looks like
- Explain MCP's architecture (host, client, server) and all three primitives (tools, resources, prompts) without notes
- Build a working FastMCP server in Python from scratch with at least one tool, one resource, and one prompt
- Write a Python agent using the Anthropic SDK that connects to that server and uses its tools to complete a task
- Debug a misbehaving MCP server using the MCP Inspector

## Constraints
- New to MCP — no prior exposure
- Python is the language of choice (FastMCP v2)
- Workshop style: hands-on, learn-by-doing, not just reading

## Out of scope
- TypeScript / Node MCP SDKs
- Remote / HTTP transport and OAuth (focus on local stdio first)
- MCP client development (focus is on the server + agent side)
- Production deployment and scaling
