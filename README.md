# `odem.optimize` Ansible Collection

System-level performance and console optimizations for Debian 13.
All roles are system-wide (no per-user logic).

## Galaxy metadata

- **namespace**: `odem`
- **name**: `optimize`
- **version**: `0.3.1`
- **dependencies**: `odem.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

| Role | Purpose |
|---|---|
| [`odem.optimize.kmscon`](roles/kmscon/README.md) | Userspace console (replaces kernel `vt`). |
| [`odem.optimize.ramdisks`](roles/ramdisks/README.md) | tmpfs ramdisks — backup → convert → restore with idempotent marker file. |
| [`odem.optimize.zram`](roles/zram/README.md) | zram-generator config + restart. |

## Installation

```bash
ansible-galaxy collection install odem.optimize
```

## Usage

```yaml
- hosts: all
  become: true
  roles:
    - odem.optimize.zram
    - odem.optimize.ramdisks
    - odem.optimize.kmscon
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
