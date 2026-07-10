# LinkedIn Connector - Authenticate

## Purpose

Authenticate the LinkedIn Connector so it can execute future jobs.

This action establishes and verifies an authenticated session. It does not perform any outreach or business logic.

---

## Action

authenticate

---

## Input

| Field | Type | Description |
|--------|------|-------------|
| account_id | string | Internal account identifier |
| connector_id | string | Connector name (`linkedin`) |

---

## Output

| Field | Type | Description |
|--------|------|-------------|
| authenticated | boolean | Authentication successful |
| session_id | string | Active session identifier |
| expires_at | timestamp | Session expiration time |

---

## Result

Success

```json
{
  "ok": true,
  "status": "ok",
  "data": {
    "authenticated": true,
    "session_id": "...",
    "expires_at": "..."
  }
}
```

Failure

```json
{
  "ok": false,
  "status": "failed",
  "error": "Authentication failed"
}
```

---

## Rules

- Never expose credentials.
- Store session information server-side only.
- Return a standard Result object.
- Do not execute any LinkedIn actions during authentication.
