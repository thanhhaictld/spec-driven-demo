---
id: TEST-AUTH-002
type: test-case
title: Reject expired credentials
requirements:
  - REQ-AUTH-001
acceptanceCriteria:
  - AC-AUTH-001-03
automation:
  file: tests/integration/authentication/issue-token.spec.ts
  framework: playwright
level: integration
---

# Reject expired credentials

## Given
An expired credential is supplied.

## When
The client calls `POST /oauth/token`.

## Then
The response MUST return HTTP `401`.
