---
namespace: odem
collection: optimize
role: kmscon
---

# `odem.optimize.kmscon`

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
    - odem.optimize.kmscon
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 25

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
