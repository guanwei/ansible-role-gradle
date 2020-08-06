# Ansible Role: Gradle

Installs Gradle on Debian/Ubuntu or Windows/Windows Core.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
# Gradle version number
gradle_version: 6.5.1

# Mirror to download the Gradle redistributable package from
gradle_mirror: "https://services.gradle.org/distributions"

# Directory to store files downloaded for Gradle installation
gradle_download_dir: "{{ x_ansible_download_dir | default(ansible_env.HOME + '/.ansible/tmp/downloads') }}"

# Base Gradle installation directory
gradle_install_dir: "/opt/gradle"

# If this is the default installation, /etc/profile.d/gradle.sh will be set.
gradle_is_default_installation: false
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
