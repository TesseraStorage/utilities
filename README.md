# Tessera Utilities — Public Catalog

An index-only catalog of open-source utilities. The catalog **points at**
public repositories; no utility code is hosted here or inside any Tessera
service. Anyone — Tessera included — consumes the identical public package
from the linked repository, with zero modifications.

**Machine-readable index:** [`marketplace.json`](./marketplace.json)

## Standard disclaimers (apply to every entry)

- **Open-source only.** Every listed utility is permissively licensed.
- **Not Tessera-signed.** Listing here is not an endorsement, audit,
  warranty, or signature by Tessera.
- **The human is responsible.** You decide what to install, what to include,
  and what to confirm. Read a utility's own documentation before use.
- **As-is, use at your own risk.** No warranties of any kind.
- **Ordinary client objects only.** If a utility offers a Tessera
  destination, it uses ordinary `per_action` client objects — no privileged
  paths, no special metadata, no billing exceptions.
- **Local-first.** A utility must remain fully functional without Tessera.

## Entries

### #1 — agent-env-backup

Human-controlled **encrypted** backup/restore CLI for agent (or human)
working environments: config files, memory/notes, handoffs, CLI state, and
any explicitly approved credentials.

- **Repository:** https://github.com/TesseraStorage/agent-env-backup
- **License:** MIT
- **Pin:** tag `v0.1.0-rc1`, commit `e298c161a580dc30d6edbacb6e274bafc9311f43`
- **Install:**
  ```bash
  pip install "git+https://github.com/TesseraStorage/agent-env-backup@v0.1.0-rc1"
  ```
- **What it does:** encrypts your chosen files into a single archive
  (AES-256-GCM; the key is derived from a 12-word seed that is shown once
  and never stored). Nothing is written or transmitted in cleartext.
  Restore walks a plain-text checklist (`RECONSTITUTE.yaml`) behind
  per-step confirmation gates, with a fixed action allow-list and a dry-run
  mode. Local-first; no network calls in this release.
- **Cold start:** the README contains a "drop this prompt" snippet you can
  paste into a fresh chat so any agent can coach you through a restore —
  without ever seeing your seed.

_Standard disclaimers above apply._
