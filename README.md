ANSIBLE-ROLE-GIT
=================

Ansible role install Git


## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: git+https://github.com/redbeard28/ansible-role-git.git
  version: master
  name: git
````

or
```yaml
- src: redbeard28.git
```

More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible 2.9+


Role Variables
--------------

```yaml
---
# none
```

Dependencies
------------

 - redbeard28.bootstrap

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redbeard28.git, tags: mytags }


Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
namespace=redbeard28 image=debian tag="buster-basetools" molecule converge 
namespace=redbeard28 image=debian tag="buster-basetools" molecule verify
namespace=redbeard28 image=debian tag="buster-basetools" molecule lint 
```

or
```bash
namespace=redbeard28 image=debian tag="buster-basetools" molecule test 
```

Author Information
------------------

Jeremie CUADRADO[¹](mailto:info@redbeard-consulting.fr) from Redbeard-Consulting
