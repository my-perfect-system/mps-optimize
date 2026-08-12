# AGENTS.md — odem-optimize

System-level performance tuning — zram, tmpfs ramdisks, userspace
console. All roles are system-wide (no per-user loops).

## Galaxy

- **namespace**: `odem`
- **name**: `optimize`
- **version**: `0.3.1`
- **dependencies**: `odem.base >=0.1.0`, `ansible.posix >=1.0.0`

## Roles

| Role | Description | Complexity |
|---|---|---|
| `odem.optimize.kmscon` | Userspace console (replaces kernel `vt`). Static config copy. | 1 |
| `odem.optimize.ramdisks` | Backup → unmount → convert tmpfs dirs → mount → restore. Block-gated `when:` with marker file for idempotency. | 2 |
| `odem.optimize.zram` | zram-generator config (blockinfile) + restart. | 1 |

## Conventions

- All three roles are system-level (no per-user logic, no identity dependency).
- `ramdisks` uses a `convert.yml` sub-step for the multi-step mount/unmount orchestration.
- Disabled roles are silently skipped (no `when:` on the whole role — each role applies if the play includes it).
