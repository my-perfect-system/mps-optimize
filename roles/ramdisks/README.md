---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: optimize
role: ramdisks
---

# `mps.optimize.ramdisks`

Mount a path as tmpfs with backup/restore

## Default variables

| Variable | Default | Description |
|---|---|---|
| `ramdisks_backup_marker` | `{{ ramdisks_backup_path }}/.backup_done` | Marker file under ramdisks_backup_path; its presence indicates backup completed |
| `ramdisks_backup_path` | `/tmp/var-log-backup` | Where to back up existing contents before mounting tmpfs |
| `ramdisks_fstab_marker` | `# {mark} ANSIBLE MANAGED: tmpfs {{ ramdisks_mount }}` | blockinfile marker for the fstab entry |
| `ramdisks_mount` | `/var/log` | Absolute path to mount as tmpfs |
| `ramdisks_opts` | `mode=1777,nosuid,nodev` | Mount options for the tmpfs entry |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.optimize.ramdisks
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 6
