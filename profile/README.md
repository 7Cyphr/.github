<div align="center">

[![cyphr-logo-round.png](https://i.postimg.cc/1t18y0Hk/cyphr-logo-round.png)](https://postimg.cc/v1XYzVCh)

# CYPHR

![License](https://img.shields.io/badge/License-AGPLv3-blue?style=for-the-badge)

### Edge-Native API Key Management Service

Secure, low-latency API key management service built on an edge-native serverless architecture.

### **https://cyphr.pages.dev**

</div><br>


## Why CYPHR ?

Most key management solutions either introduce unnecessary latency or are overly complex.

CYPHR focuses on:

- Fast read access through edge caching.
- Strong encryption guarantees.
- Minimal operational overhead.

## Features

- **Edge Encryption (AES-256-GCM)**<br>
  Secrets are encrypted at the edge before persistence.

- **Low-Latency Reads**<br>
  Cloudflare KV caching keeps key retrieval fast, wherever your requests come from.

- **Edge-Native Execution**<br>
  Runs on Cloudflare Workers for globally distributed execution.

- **Minimal API Design**<br>
  Simple and predictable API for managing keys.

- **Lightweight Dashboard**<br>
  Fast interface for managing secrets.

## Quick Start

1. Sign in using GitHub
2. Store an API key
3. Retrieve secrets via the dashboard

CYPHR handles encryption, caching, and storage automatically.

## Architecture

Below is a simple system design diagram to explain the basic flow of data

[![cypher_architecture.png](https://i.postimg.cc/MT1S1zJF/cypher_architecture.png)](https://postimg.cc/phV4HbTf)

## Security

- AES-256-GCM encryption at REST before persistence.
- Stateless authentication model.
- No plaintext secrets stored.

## Tech Stack

- **Client**: HTML, CSS, Bulma, JavaScript (ES6+)
- **Server**: Node.js, Hono
- **Auth**: Supabase Auth
- **Database**: PostgreSQL (Neon)
- **Edge Runtime**: Cloudflare Workers
- **Caching**: Cloudflare KV

## Notes

- Designed for developer-focused workflows.
- Focused on performance and simplicity.
- Encryption and decryption happen server-side; secrets are encrypted at rest.
- Decryption only on demand. Plaintext key is never cached, logged or exposed.
- Does not support full End-to-End Encryption (for now).

## Repositories

- Client: https://github.com/NexusWasLost/cyphr-client
- Server: https://github.com/NexusWasLost/cyphr-api

## Contributor

Built by Aritra
