# rust-contextvm-sdk

Rust SDK for the [ContextVM protocol](https://contextvm.org) — MCP over Nostr.

A complete Rust implementation of the ContextVM protocol, enabling MCP (Model Context Protocol) servers to expose their capabilities through the Nostr network with decentralized discovery, cryptographic verification, and optional encryption.

## Features

- **Transport**: Client and server transports implementing MCP's `Transport` trait over Nostr
- **Gateway**: Bridge any MCP server to Nostr (expose local MCP servers to the network)
- **Proxy**: Connect to remote Nostr MCP servers as if they were local
- **Encryption**: NIP-44 encryption with NIP-59 gift wrapping for private communication
- **Discovery**: Server announcements and capability listings via replaceable events
- **Session Management**: Multi-client session tracking with automatic cleanup

## Protocol

Based on the [ContextVM Draft Specification](https://contextvm.org):

| Kind  | Description |
|-------|-------------|
| 25910 | ContextVM messages (ephemeral) |
| 1059  | Encrypted messages (NIP-59 Gift Wrap) |
| 11316 | Server announcement (replaceable) |
| 11317 | Tools list (replaceable) |
| 11318 | Resources list (replaceable) |
| 11319 | Resource templates list (replaceable) |
| 11320 | Prompts list (replaceable) |

## Status

🚧 In development — see [DESIGN.md](DESIGN.md) for implementation plan.

## References

- [ContextVM Specification](https://contextvm.org)
- [ContextVM TypeScript SDK](https://github.com/ContextVM/sdk)
- [Model Context Protocol](https://modelcontextprotocol.io)
- [Nostr Protocol](https://nostr.com)

## License

MIT
