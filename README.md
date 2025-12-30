# Awesome X402 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for the X402 protocol, the HTTP 402 Payment Required standard for machine-to-machine payments.

## Contents

- [Official Resources](#official-resources)
- [Protocol Documentation](#protocol-documentation)
- [Quickstart Guides](#quickstart-guides)
- [Protocol Implementations](#protocol-implementations)
- [SDKs & Client Libraries](#sdks--client-libraries)
- [Server Frameworks & Middleware](#server-frameworks--middleware)
- [Facilitators](#facilitators)
- [Example Applications](#example-applications)
- [AI Agent Integration](#ai-agent-integration)
- [Tools](#tools)
- [Testing & Development](#testing--development)
- [Articles & Blog Posts](#articles--blog-posts)
- [Community](#community)
- [Ecosystem Projects](#ecosystem-projects)
- [Security & Audits](#security--audits)
- [Related Protocols](#related-protocols)

## Official Resources

- [x402 Protocol Specification](https://github.com/coinbase/x402) - Official open-source protocol implementation by Coinbase.
- [x402 Foundation](https://x402.org) - Protocol foundation website with overview and documentation.
- [x402 Whitepaper](https://x402.org/x402-whitepaper.pdf) - Technical deep dive into protocol architecture.
- [Coinbase Developer Platform Docs](https://docs.cdp.coinbase.com/x402) - Complete implementation guide and API reference.
- [Protocol Specifications](https://github.com/coinbase/x402/tree/main/specs) - Detailed technical specifications.
  - [Payment Schemes](https://github.com/coinbase/x402/tree/main/specs/schemes) - Different payment flow types.
  - [EVM Implementation](https://github.com/coinbase/x402/blob/main/specs/schemes/exact/scheme_exact_evm.md) - Ethereum Virtual Machine specifics.

## Protocol Documentation

- [How x402 Works](https://docs.cdp.coinbase.com/x402/how-it-works) - Complete payment flow explanation with diagrams.
- [Payment Requirements Schema](https://github.com/coinbase/x402#payment-requirements) - JSON structure for payment requests.
- [Payment Payload Format](https://github.com/coinbase/x402#payment-payload) - Client payment submission format.
- [Verification & Settlement](https://github.com/coinbase/x402#verification-and-settlement) - Payment validation process.
- [EIP-3009 TransferWithAuthorization](https://eips.ethereum.org/EIPS/eip-3009) - Gasless transfer standard used by x402.
- [HTTP 402 Status Code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/402) - The long-dormant HTTP status.

## Quickstart Guides

- [Seller Quickstart](https://docs.cdp.coinbase.com/x402/quickstart-sellers) - Accept your first payment.
- [Buyer/Client Setup](https://docs.cdp.coinbase.com/x402/quickstart-buyers) - Make automated payments.
- [One-Line Integration](https://github.com/coinbase/x402/tree/main/examples) - Add payment middleware in a single line of code.
- [Base Sepolia Testnet Setup](https://docs.cdp.coinbase.com/x402/network-support) - Get test USDC and start testing.
- [Production Deployment Checklist](https://github.com/coinbase/x402/blob/main/DEPLOYMENT.md) - Go live on Base mainnet.

## Protocol Implementations

### TypeScript/JavaScript

- [x402-typescript](https://github.com/coinbase/x402/tree/main/typescript) ⭐ **Official** - Complete TypeScript implementation.
  - Core protocol types and utilities
  - Payment verification and settlement logic
  - Multi-chain support (Base, Base Sepolia, Ethereum, Solana)
- [x402-express](https://github.com/coinbase/x402/tree/main/examples/typescript/servers/express) - Express.js middleware example.

### Python

- [x402](https://pypi.org/project/x402/) ⭐ **Official** - Python SDK on PyPI.
  - FastAPI middleware integration
  - Requests session with auto-payments
  - Payment requirement generation

### Rust

- [x402-rs](https://github.com/x402-rs/x402-rs) ⭐ **Community** - Production-grade Rust implementation.
  - Axum middleware
  - Reqwest client wrapper
  - Self-hostable facilitator
  - Multi-chain support
- [x402-axum](https://github.com/x402-rs/x402-rs/tree/main/x402-axum) - Axum web framework integration.
- [x402-reqwest](https://github.com/x402-rs/x402-rs/tree/main/x402-reqwest) - Reqwest HTTP client wrapper.

## SDKs & Client Libraries

### JavaScript/TypeScript

- [x402-got](https://www.npmjs.com/package/x402-got) - Got HTTP client integration.
- [viem](https://viem.sh/) - TypeScript library for signing payments.
- [ethers.js](https://docs.ethers.org/) - Ethereum library.

### Rust

- [alloy](https://github.com/alloy-rs/alloy) - High-performance Ethereum library.

## Server Frameworks & Middleware

### Node.js/TypeScript

**Next.js**
- [x402-next](https://www.npmjs.com/package/x402-next) - App Router middleware.
- [Next.js route protection](https://github.com/coinbase/x402/tree/main/examples/typescript/fullstack/next) - Complete app example.
- [Mainnet production example](https://github.com/coinbase/x402/tree/main/examples/typescript/fullstack/mainnet) - Base mainnet ready.

**Hono**
- [Browser wallet example](https://github.com/coinbase/x402/tree/main/examples/typescript/fullstack/browser-wallet-example) - React + Hono full-stack.

### Python

**FastAPI**
- [FastAPI example](https://github.com/coinbase/x402/tree/main/examples/python) - Complete implementation.

### Rust

**Axum**
- [Axum server example](https://github.com/x402-rs/x402-rs/tree/main/x402-axum-example) - Full implementation.

## Facilitators

- [Coinbase CDP Facilitator](https://docs.cdp.coinbase.com/x402/facilitator) - Official hosted facilitator on Base.
- [Cloudflare Workers Facilitator](https://developers.cloudflare.com/workers/examples/x402/) - Edge computing facilitator.
- [x402-rs Facilitator](https://github.com/x402-rs/x402-rs#facilitator) - Self-hosted Rust facilitator.

## Example Applications

- [Weather API Service](https://github.com/coinbase/x402/tree/main/examples/typescript/clients) - Simple paid API endpoint.
- [Video Paywall](https://www.quicknode.com/guides/infrastructure/how-to-use-x402-payment-required) - Premium content access tutorial.
- [Farcaster Mini App](https://github.com/coinbase/x402/tree/main/examples/typescript/fullstack/farcaster-miniapp) - Social app integration.
- [REST API with Auth Pricing](https://github.com/coinbase/x402/tree/main/examples/typescript/fullstack/auth_based_pricing) - SIWE + dynamic pricing.
- [Axios Client](https://github.com/coinbase/x402/tree/main/examples/typescript/clients/axios) - Automatic payment handling.
- [Fetch Client](https://github.com/coinbase/x402/tree/main/examples/typescript/clients/fetch) - Fetch API wrapper.
- [Python Client](https://github.com/coinbase/x402/tree/main/examples/python/client) - Python example.

## AI Agent Integration

- [MCP Server Setup Guide](https://docs.cdp.coinbase.com/x402/mcp-server) - Claude Desktop integration.
- [NEAR AI](https://near.ai) - Cross-chain agent settlements.
- [Phidata Agents](https://github.com/phidatahq/phidata) - Multi-modal agents.
- [Google A2A x402 Extension](https://github.com/google-agentic-commerce/a2a-x402) - Agent commerce protocol.

## Tools

- [Foundry](https://getfoundry.sh/) - Smart contract development toolkit.

## Testing & Development

- [Base Sepolia Testnet](https://docs.base.org/docs/network-information) - Primary testnet.
- [USDC Faucet](https://faucet.circle.com/) - Get test USDC.
- [Base Bridge](https://bridge.base.org/) - Bridge test ETH.

## Articles & Blog Posts

- [Introducing x402](https://www.coinbase.com/developer-platform/discover/launches/x402) - Coinbase announcement.
- [Cloudflare and x402](https://blog.cloudflare.com/x402/) - Cloudflare integration.
- [What is X402](https://blog.thirdweb.com/what-is-x402-protocol) - Thirdweb explainer.
- [x402 Growth](https://finance.yahoo.com/news/coinbase-x402-ai-payments-protocol-130700006.html) - Yahoo Finance coverage.

## Community

- [GitHub Discussions](https://github.com/coinbase/x402/discussions) - Technical Q&A.
- [Dev.to #x402](https://dev.to/t/x402) - Tutorials and articles.

## Ecosystem Projects

- [Coinbase Developer Platform](https://coinbase.com/cloud) - Hosted facilitator service.
- [thirdweb Nebula](https://thirdweb.com/nebula) - AI agent transaction framework.
- [Chainlink](https://chain.link) - Oracle network integration.

## Security & Audits

- [Circle USDC Audits](https://www.circle.com/en/usdc/security-audits) - USDC contract audits.
- [EIP-3009 Security](https://eips.ethereum.org/EIPS/eip-3009#security-considerations) - Security considerations.
- [Payment Verification](https://github.com/coinbase/x402/blob/main/SECURITY.md) - Verification implementation.
- [Coinbase Bug Bounty](https://hackerone.com/coinbase) - Report vulnerabilities.

## Related Protocols

- [Lightning Network](https://lightning.network/) - Bitcoin micropayments.
- [Request Network](https://request.network/) - Payment request protocol.
- [ERC-20](https://eips.ethereum.org/EIPS/eip-20) - Token standard.
- [HTTP 402 RFC](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) - Original specification.

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.
