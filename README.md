# ansible-role-bdocker
Ansible Role to install bdocker in a cluster


## Inventory file sample:

[ui]
cluster-ui bdocker_role="client"

[frontend]
cluster bdocker_role="accounting"

[wn]
cluster-wn01 bdocker_role="working"
cluster-wn02 bdocker_role="working"

[storage]
st


## How to add this role to your playbook

 - name: Install bdocker
   hosts: all
   become: yes

   roles:
   - { role: ansible-role-bdocker, tags: [ 'bdocker' ] }


