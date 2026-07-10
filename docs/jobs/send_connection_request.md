# Job: send_connection_request

## Purpose

Send a LinkedIn connection request to an approved prospect.

---

## Trigger

Created only after:

- Prospect discovered
- Prospect enriched
- Prospect scored
- Outreach approved by a human

---

## Input

```json
{
  "job_id": "...",
  "prospect_id": "...",
  "linkedin_profile_url": "...",
  "connection_note": "..."
}
```

---

## Success

```json
{
  "ok": true,
  "status": "completed"
}
```

---

## Failure

Examples:

- Session expired
- Already connected
- Invitation already sent
- Daily limit reached
- Profile unavailable

---

## Retry Policy

- Retry only for temporary failures.
- Never retry permanent failures automatically.
