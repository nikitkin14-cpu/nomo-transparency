# Architecture Overview

## High-level structure
[Your Device] <--E2E Encrypted--> [Nomo Server] <--E2E Encrypted--> [Recipient Device]
| |
└─────────────────── Your Private Key (never leaves) ───────────────────────┘



## Components

### Client
- Web-based (desktop + mobile browsers)
- Native apps planned (Tauri for desktop, Android later)
- All encryption happens here

### Server
- Routes encrypted messages
- Does NOT store decrypted content
- Acts as a relay, not a reader

### Authentication
- Ed25519 key pairs
- No passwords, no phones, no emails
- Your key IS your identity

### Encryption Protocol (planned full implementation)
- X3DH for key agreement
- Double Ratchet for forward secrecy
- Signal-grade protection

---

## What makes Nomo different

| Feature | Nomo | Telegram | Signal |
|--------|------|----------|--------|
| No phone number | ✅ | ❌ | ❌ |
| Open crypto core | ✅ | ❌ | ✅ |
| Mesh networks planned | ✅ | ❌ | ❌ |
| Free AI planned | ✅ | ❌ | ❌ |

---

*For technical details, see [nomo-crypto-core](https://github.com/nikitkin14-cpu/nomo-crypto-core) (coming soon).*
