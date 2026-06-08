# Ansible Role: Docker

Installeert Docker Engine op Ubuntu (Jammy/Noble) en voegt specifieke gebruikers toe aan de `docker` groep zodat zij containers kunnen draaien zonder sudo.

## Role Variables

| Variabele | Standaardwaarde | Omschrijving |
|-----------|-----------------|--------------|
| `docker_users` | `['iac', 'testuser']` | Een lijst met gebruikersnamen die aan de docker groep worden toegevoegd. |

## Example Playbook

```yaml
---
- hosts: all
  become: true
  roles:
    - role: postname.ocker
      vars:
        docker_users:
          - iac
          - testuser
```
