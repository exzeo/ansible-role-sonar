Ansible Role Sonar
=========

Installs Sonar Command Line on Debian/Ubuntu servers. 
Releases: https://github.com/SonarSource/sonar-scanner-cli/releases

Role Variables
--------------

```
# Version of 'sonar' to install, defaults to latest version
sonar_version: ""

# Toggling this will uninstall from the server
uninstall: false
```

Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.sonar
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.sonar
      vars:
        sonar_version: "4.6.2.2472"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.sonar
      vars:
        uninstall: true
```