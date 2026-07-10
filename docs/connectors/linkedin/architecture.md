# LinkedIn Connector Architecture

## Purpose

The LinkedIn Connector is an independent execution service.

It receives jobs from the UGA Automation Platform, executes LinkedIn actions, and returns standardized results.

It contains no business logic.

---

## Responsibilities

- Authenticate LinkedIn sessions
- Execute approved jobs
- Return standardized results
- Handle retries
- Report errors
- Log execution

---

## Does NOT

- Score prospects
- Generate outreach
- Decide workflow
- Store business data
- Bypass approval

Those responsibilities remain inside UGA Recruitment Command.
