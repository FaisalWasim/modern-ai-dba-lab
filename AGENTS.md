# AGENTS.md

## Purpose

This repository simulates safe modern DBA and infrastructure workflows.

AI agents and automation tools operating in this repository must follow these rules.

---

## Database Safety Rules

- Never automatically apply destructive migrations
- Always require rollback plans
- Warn on table rewrites
- Warn on ACCESS EXCLUSIVE locks
- Prefer concurrent indexes on large tables
- Flag long-running transactions
- Prefer additive schema changes first

---

## Terraform Safety Rules

- Always review terraform plan output
- Never destroy production infrastructure automatically
- Warn on security group exposure changes
- Validate formatting before merge
- Require human approval before apply

---

## CI/CD Rules

- All pull requests must pass validation checks
- Migration validation must run before merge
- Terraform validation must run before merge
- Production deployments require approval

---

## AI Review Expectations

AI tools should:

- Explain risks clearly
- Suggest rollback strategies
- Identify locking concerns
- Detect dangerous ALTER statements
- Summarize infrastructure changes
- Help generate documentation

AI tools must NOT:

- Auto-approve production changes
- Ignore failed validation checks
- Apply destructive operations automatically
