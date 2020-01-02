Role Name
=========

jenkins

[![Build Status](https://travis-ci.org/cmihai-ansible/jenkins.svg?branch=master)](https://travis-ci.org/cmihai-ansible/jenkins)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/jenkins](https://galaxy.ansible.com/crivetimihai/jenkins)

```bash
ansible-galaxy install crivetimihai.jenkins
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
jenkins_remove_packages: true
jenkins_enable_service: true
jenkins_enable_selinux: true
jenkins_firewall_configure: true
jenkins_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install jenkins on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: jenkins is configured
      import_role:
        name: crivetimihai.jenkins
      vars:
        jenkins_remove_packages: true
        jenkins_enable_service: true
        jenkins_firewall_configure: true
        jenkins_firewall_rules:
          - service:
      tags: jenkins
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
