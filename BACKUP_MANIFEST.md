# Backup Manifest

This private repo stores durable Zemetia/Hermes data that should survive container resets.

Included:
- `SOUL.md` — Zemetia persona
- `memories/` — durable user/business memory files
- `skills/` — local skills and skill templates
- `config.yaml` — Hermes config without `.env` secrets
- `plans/`, `hooks/`, `skins/`, `workspace/` when present
- `home/.gitconfig`, `home/.ssh/config`, and public SSH key only

Excluded intentionally:
- `.env`, `auth.json`, API tokens, credentials
- private SSH keys
- runtime DBs: `state.db`, `kanban.db`, sqlite WAL/SHM files
- logs, sessions, browser/cache folders
- dependency/build folders: `node_modules`, `.venv`, `site-packages`, `dist`, `build`

Raw session transcripts are excluded because they can contain passwords or private chat content.
