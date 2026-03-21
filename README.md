<div align="center">

# CYPHR

![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

### Edge-Native API Key Management Service

Secure, low-latency API key management built on an edge-native serverless architecture.

**https://cyphr.pages.dev**

</div>

---

## Overview

Cyphr is a secure API key management service designed for fast, reliable storage and retrieval of secrets. It leverages edge computing, encryption, and caching to minimize latency while ensuring strong security guarantees.


## Features

- **Edge Encryption (AES-256-GCM)**
  Secrets are encrypted at the edge before persistence.

- **Low-Latency Reads**
  Cloudflare KV caching reduces P95 read latency by **~65%**.

- **Edge-Native Execution**
  Runs on Cloudflare Workers, bringing compute closer to users.

- **Minimal API Design**
  Clean and simple REST API for managing keys.

- **Dashboard Interface**
  Lightweight frontend for quick key management.


## Architecture
```
    ┌───────────────┐
    │     Client    │
    └──────┬────────┘
           │
           │ Authenticate
           ▼
    ┌──────────────────────────────┐
    │ Supabase Auth (GitHub OAuth) │
    └──────┬───────────────────────┘
           │
           │ JWT Token
           ▼
    ┌───────────────┐
    │     Client    │
    └──────┬────────┘
           │
           │ API Request (with JWT)
           ▼
    ┌──────────────────────┐
    │  Cloudflare Worker   │
    └──────┬───────────────┘
           │
           ├── Read → KV Cache
           │
           └── Write → AES-256-GCM → PostgreSQL (Neon)

```

- Edge layer handles request processing, encryption, and caching
- KV cache accelerates read-heavy workloads
- Database stores encrypted secrets
- Authentication handled via Supabase Auth


## Tech Stack

- **Frontend**: HTML, CSS, Bulma, JavaScript (ES6+)
- **Backend**: Node.js, Hono
- **Auth**: Supabase Auth
- **Database**: PostgreSQL (Neon)
- **Edge Runtime**: Cloudflare Workers
- **Caching**: Cloudflare KV

## Performance

- **~65% reduction in P95 read latency** using KV caching
- Optimized for read-heavy workloads

## Security

- AES-256-GCM encryption applied before persistence
- Stateless authentication model
- No plaintext secrets stored

## Notes

- Designed for developer-focused workflows
- Focused on performance and simplicity
- Not intended as a full enterprise secrets manager

## Author

Built by Aritra
