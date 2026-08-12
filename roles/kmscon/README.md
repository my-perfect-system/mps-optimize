---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: optimize
role: kmscon
---

# `mps.optimize.kmscon`

Install kmscon from trixie-backports and deploy its config

## Default variables

| Variable | Default | Description |
|---|---|---|
| `kmscon_conf_dst` | `{{ kmscon_config_dir }}/kmscon.conf` | Destination path for the kmscon config file |
| `kmscon_conf_src` | `{{ role_path }}/files/etc/kmscon/kmscon.conf` | Source path for the kmscon config file (role-relative) |
| `kmscon_config_dir` | `/etc/kmscon` | Directory where the kmscon config file is deployed |
| `kmscon_default_release` | `trixie-backports` | apt target release to use for kmscon packages |
| `kmscon_packages` | `- kmscon<br>- libtsm4` | Apt packages required for kmscon (typically pulled from backports) |

## Dependencies

None.

## Example usage

```yaml
- hosts: all
  roles:
    - mps.optimize.kmscon
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 25
