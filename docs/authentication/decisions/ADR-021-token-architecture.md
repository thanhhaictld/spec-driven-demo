---
id: ADR-021
type: decision
title: Token architecture
status: accepted
---

# ADR-021 — Token architecture

Use short-lived access tokens and rotating refresh tokens. Token/session state is persisted in the `sessions` table.
