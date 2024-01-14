# awx_deploy

Install k3d on target machine

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [ansible_awx_k3d_awx_extra_settings](#ansible_awx_k3d_awx_extra_settings)
  - [ansible_awx_k3d_awx_operator_version](#ansible_awx_k3d_awx_operator_version)
  - [ansible_awx_k3d_awx_public_domain](#ansible_awx_k3d_awx_public_domain)
  - [ansible_awx_k3d_kustomize_target](#ansible_awx_k3d_kustomize_target)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.15.0`

## Default Variables

### ansible_awx_k3d_awx_extra_settings

#### Default value

```YAML
ansible_awx_k3d_awx_extra_settings:
  - setting: TOWER_URL_BASE
    value: '"https://{{ ansible_awx_k3d_awx_public_domain }}"'
```

### ansible_awx_k3d_awx_operator_version

#### Default value

```YAML
ansible_awx_k3d_awx_operator_version: 2.7.1
```

### ansible_awx_k3d_awx_public_domain

#### Default value

```YAML
ansible_awx_k3d_awx_public_domain: >-
  awx-{{ ansible_all_ipv4_addresses | first | replace('.', '-') }}.nip.io"
```

### ansible_awx_k3d_kustomize_target

#### Default value

```YAML
ansible_awx_k3d_kustomize_target: /root/aws-setup
```

## Discovered Tags

**_kubenamespace_**


## Dependencies

None.

## License

GPL-3.0-only

## Author

Thorsten Bruhns
