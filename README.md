# ROSA

- **Author**:        rosa-tech26
- **Description**:   Self-hosted IT auto-remediation dashboard — watches alerts, runs Ansible playbooks automatically, and drafts fixes with Claude for anything it hasn't seen before
- **Version**:       1.0.0

## Introduction

ROSA closes the loop between an alert firing and the fix actually happening. It watches your Windows infrastructure, matches incoming alerts against a rule engine, and runs Ansible playbooks to remediate — no ticket, no human in the loop, for the issues it already knows how to handle.

- Real-time visibility into every alert and remediation as it happens
- Auto-remediation for known problems — disk cleanup, CPU/memory analysis, service restarts
- An AI layer (Claude) that drafts a fix for alerts nothing matches, with its reasoning and a confidence score, queued for your approval
- A full audit trail of every action taken, so nothing runs invisibly
- Configuration drift detection across every managed server

## Features

- **Alert ingestion** — Prometheus/Alertmanager, Slack, RSS feeds, or ROSA's own lightweight agent-free VM monitor
- **Rule-based auto-remediation** — YAML rule engine + Ansible playbooks, fully editable
- **AI Resolutions (opt-in)** — when no rule matches, Claude proposes a new rule + playbook; every proposal is queued on the Approvals page and capped at 3 attempts per issue — it never runs an unapproved AI fix
- **Configuration drift detection** — flags changes you didn't make, across every server
- **Full audit trail** — every action logged, AI-run actions clearly badged
- **Real-time dashboard** — live alert feed over WebSocket, light/dark theme, accent colors

## Download

Grab the latest installer from the [Releases](../../releases) page: `ROSA-Setup.msi`.

1. Run the installer (Windows)
2. Open `http://localhost:5001`
3. Log in with `admin` / `changeme`
4. **Change the default password immediately** under Settings

## Licensing

Free tier covers up to 3 monitored servers, self-hosted, no account required. Need more servers? A license key unlocks higher caps — see Settings → License.

## Release Notes

- **v1.0.0** / 2026-10-13
  - First public release

## Support

Open an [issue](../../issues) for bugs or feature requests.
