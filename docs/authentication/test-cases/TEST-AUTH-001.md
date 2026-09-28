---
id: TEST-AUTH-001
type: test-case
title: Issue token with valid credentials
requirements:
  - REQ-AUTH-001
acceptanceCriteria:
  - AC-AUTH-001-01
  - AC-AUTH-001-02
automation:
  file: tests/integration/authentication/issue-token.spec.ts
  framework: playwright
level: integration
---

# Issue token with valid credentials

## Given
A valid user account exists.

## When
The client calls `POST /oauth/token` with valid credentials.

## Then
The response status MUST be `200` and the response MUST contain `access_token`.
