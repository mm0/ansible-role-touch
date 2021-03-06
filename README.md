Ansible Role: Touch v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-touch.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-touch)

An Ansible role that simply runs the touch module.

Occassionally, you will need to touch a file between role executions, there is no built-in way to do this, instead use this role in between.

See Also: ansible-role-directory


Requirements
--

None 

Role Variables
--

Available variables are listed below, along with default values:

```yml
owner: ubuntu # owner of final directory uploaded remotely
group: ubuntu 
mode: 644 # mode for remote directory
files: # a list of files to touch
```

Dependencies
--

None 

Example Playbook
--

```yml
- hosts: webservers
  roles:
  - { role: ansible-role-touch,
      files: ["/var/log/mylog","/var/log/mylog.2""],
      owner: ubuntu,
      group: ubuntu,
      mode: "0755"
    }
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
