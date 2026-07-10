# POST /execute

## Purpose

Executes a single approved job.

The UGA Automation Platform sends a job to a connector.

The connector executes it and returns a standard Result.

---

## Request

```json
{
  "job_id": "...",
  "connector": "linkedin",
  "action": "send_connection_request",
  "payload": {}
}
```

---

## Response

```json
{
  "ok": true,
  "status": "ok",
  "data": {},
  "error": null
}
```

---

## Rules

- One request executes one action.
- The connector never decides what action to run.
- The connector always returns a Result.
```
