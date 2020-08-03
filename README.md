# Ansible Role: Gradle

Installs Gradle on Debian/Ubuntu or Windows/Windows Core.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```

```

## Dependencies

None.

## Example Playbook

requirements.yml
```
- name: gradle
  src: <repo_url>
  version: <branch_name>
  scm: git
```

playbook.yml
```
- hosts: servers
  roles:
    - gradle
```
