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

# Filename of Gradle redistributable package
gradle_redis_filename: "gradle-{{ gradle_version }}-bin.zip"

# If this is the default installation, /etc/profile.d/gradle.sh will be set.
gradle_is_default_installation: false
```

`gradle_download_dir` default is `%TEMP%/ansible/downloads` on Windows, `$HOME/.ansible/tmp/downloads` on Linux.

`gradle_install_dir` default is `C:/Gradle` on Windows, `/opt/gradle` on Linux.

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
