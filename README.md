Role Name
=========

Installs NTOP Monitoring...http://www.ntop.org/

Requirements
------------

None

Role Variables
--------------

````
---
# defaults file for ansible-ntop
ntop_debian_apt_url: 'http://apt-stable.ntop.org/{{ ansible_distribution_version }}/all'
ntop_debian_package: apt-ntop-stable.deb
````

Dependencies
------------

Ansible Galaxy role(s)
- mrlesmithjr.redis-server

````
ansible-galaxy install -r ntop_requirements.yml
````


Example Playbook
----------------

---
- name: NTOP Network Monitoring
  hosts: ntop-servers
  remote_user: remote
  sudo: true
  vars:
  roles:
    - mrlesmithjr.redis-server
    - mrlesmithjr.ntop
  tasks:

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com
