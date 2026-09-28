---
id: REQ-AUTH-001
type: requirement
title: Issue access token
status: approved
priority: critical
owner: platform-team
links:
  api:
    - POST /oauth/token
  database:
    - sessions
  decisions:
    - ADR-021
  tests:
    - TEST-AUTH-001
    - TEST-AUTH-002
---

# Issue access token

When valid credentials are supplied, the authentication service MUST issue an OAuth 2.0 access token.

## Acceptance Criteria

### AC-AUTH-001-01
Valid credentials MUST return HTTP `200`.

### AC-AUTH-001-02
The response MUST contain `access_token`.

### AC-AUTH-001-03
Expired credentials MUST return HTTP `401`.

### AC-AUTH-001-04
Access-token lifetime MUST NOT exceed 60 minutes.
