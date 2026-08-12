---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: optimize
role: zram
---

# `mps.optimize.zram`

Install zram-tools and configure /etc/default/zramswap

## Default variables

| Variable | Default | Description |
|---|---|---|
| `zram_algo` | `zstd` | Compression algorithm for zram (e.g. zstd, lz4, lzo) |
| `zram_config_path` | `/etc/default/zramswap` | Path to the zramswap configuration file |
| `zram_packages` | `- zram-tools` | Apt packages required for zram swap |
| `zram_percentage` | `10` | Percentage of total RAM to use for zram swap |
| `zram_service` | `zramswap` | systemd service name for zramswap |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.optimize.zram
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 22
