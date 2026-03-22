<div align="center">

[![cyphr_logo_round.png](https://i.postimg.cc/wTLFcnSy/cyphr_logo_round.png)](https://postimg.cc/fJWxMqWD)

# CYPHR

![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

### Edge-Native API Key Management Service

Secure, low-latency API key management service built on an edge-native serverless architecture.

**https://cyphr.pages.dev**

</div><br>


## Why Cyphr ?

Most key management solutions either introduce unnecessary latency or are overly complex.

Cyphr focuses on:

- Fast read access through edge caching.
- Strong encryption guarantees.
- Minimal operational overhead.

## Features

- **Edge Encryption (AES-256-GCM)**<br>
  Secrets are encrypted at the edge before persistence.

- **Low-Latency Reads**<br>
  P95 read latency reduced by **~65%** using Cloudflare KV caching.

- **Edge-Native Execution**<br>
  Runs on Cloudflare Workers for globally distributed execution.

- **Minimal API Design**<br>
  Simple and predictable API for managing keys.

- **Lightweight Dashboard**
  Fast interface for managing secrets.

## Quick Start

1. Sign in using GitHub
2. Store an API key
3. Retrieve secrets via the dashboard

Cyphr handles encryption, caching, and storage automatically.

## Architecture

Below is a simple system design diagram to explain the basic flow of data

[![cypher_architecture.png](https://i.postimg.cc/MT1S1zJF/cypher_architecture.png)](https://postimg.cc/phV4HbTf)

## Performance

- **~65% reduction in P95 read latency** using KV caching.
- Optimized for read-heavy workloads.

## Security

- AES-256-GCM encryption applied before persistence.
- Stateless authentication model.
- No plaintext secrets stored.

## Tech Stack

- **Frontend**: HTML, CSS, Bulma, JavaScript (ES6+)
- **Backend**: Node.js, Hono
- **Auth**: Supabase Auth
- **Database**: PostgreSQL (Neon)
- **Edge Runtime**: Cloudflare Workers
- **Caching**: Cloudflare KV

## Notes

- Designed for developer-focused workflows.
- Focused on performance and simplicity.
- Not intended as a full enterprise secrets manager.

## Repositories

- Frontend: https://github.com/NexusWasLost/cyphr-client
- Backend: https://github.com/NexusWasLost/cyphr-server

## Contributor

Built by Aritra
