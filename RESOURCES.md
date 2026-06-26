# MCP Resources

## Knowledge

- [Official MCP Docs — Introduction](https://modelcontextprotocol.io/docs/getting-started/intro)
  The canonical entry point. Covers the USB-C analogy and what MCP enables. Reach for this first.

- [Official MCP Architecture Overview](https://modelcontextprotocol.io/docs/learn/architecture)
  Deep dive into host/client/server roles, JSON-RPC 2.0 data layer, stdio vs HTTP transports, and all primitives. Primary reference for Lesson 1.

- [FastMCP Official Docs — Create an MCP Server](https://gofastmcp.com/tutorials/create-mcp-server)
  Hands-on FastMCP tutorial: installation, `@mcp.tool`, `@mcp.resource`, `@mcp.prompt` decorators, and running with stdio. Primary reference for Lesson 2.

- [FastMCP Client Docs](https://gofastmcp.com/clients/client)
  How to use the Python FastMCP client to connect to a server and call tools programmatically. Key for Lesson 4 (agent integration).

- [Anthropic Agent SDK Overview](https://code.claude.com/docs/en/agent-sdk/overview)
  Claude Agent SDK for building agents that can use MCP servers. Reference for Lesson 4.

- [MCP Python SDK (official)](https://github.com/modelcontextprotocol/python-sdk)
  The low-level official SDK. Useful for understanding what FastMCP wraps. Not used directly in the workshop.

- [DataCamp — Building an MCP Server and Client with FastMCP 2.0](https://www.datacamp.com/tutorial/building-mcp-server-client-fastmcp)
  End-to-end tutorial covering both server and client. Good cross-reference for Lessons 2–4.

- [MCP Inspector (GitHub)](https://github.com/modelcontextprotocol/inspector)
  The official debugging tool. Exposes a browser UI to call tools and inspect responses. Essential for Lesson 2.

## Wisdom (Communities)

- [r/mcp (Reddit)](https://reddit.com/r/mcp)
  Growing community for MCP discussion, server showcases, and troubleshooting.

- [MCP Discord (via Anthropic)](https://discord.gg/anthropic)
  Official Anthropic community with an #mcp channel. Good for real-time help.

- [GitHub modelcontextprotocol org](https://github.com/modelcontextprotocol)
  The source of truth for specs, SDKs, and reference servers. Browsing real server implementations is one of the fastest ways to gain wisdom.
