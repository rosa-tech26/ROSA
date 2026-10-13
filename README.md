# ROSA

**Alerts come in. Playbooks run automatically. The ones ROSA has never seen before get a drafted fix from Claude — reasoning, confidence score, and a queue for you to approve before anything touches production.**

ROSA is a self-hosted IT auto-remediation dashboard for Windows infrastructure. It watches your servers, matches incoming alerts against a rule engine, and runs Ansible playbooks to fix the problem — no ticket, no human in the loop, for the issues it already knows how to handle.

## What it does

- **Ingests alerts** from Prometheus/Alertmanager, Slack, RSS feeds, or its own lightweight agent-free VM monitor
- **Auto-remediates** via a YAML rule engine + Ansible playbooks — disk cleanup, CPU/memory analysis, service restarts, and more
- **Drafts fixes for unknown alerts** using Claude: when nothing matches, it proposes a new rule + playbook with its reasoning and a confidence score, capped at 3 attempts, and queues it for human approval — it never runs an unapproved AI fix
- **Tracks configuration drift** across every managed server, flagging changes you didn't make
- **Full audit trail** of every action taken, with AI-run actions clearly badged
- **Real-time dashboard** — live alert feed over WebSocket, light/dark theme, accent colors

## Download

Grab the latest installer from the [Releases](../../releases) page: `ROSA-Setup.msi`.

1. Run the installer (Windows)
2. Open `http://localhost:5001`
3. Log in with `admin` / `changeme`
4. **Change the default password immediately** under Settings

## Licensing

Free tier covers up to 3 monitored servers, self-hosted, no account required. Need more servers? A license key unlocks higher caps — see Settings → License.

## Support

Open an [issue](../../issues) for bugs or feature requests.
