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
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 22

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
