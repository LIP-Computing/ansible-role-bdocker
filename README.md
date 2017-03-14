# ansible-role-bdocker
Ansible Role to install bdocker in a cluster
At this point in time, this role assumes that you are working with systemd enabled OSs.


## Inventory file sample:
<pre>
 <code>
[ui]
cluster-ui

[frontend]
cluster

[wn]
cluster-wn[01:02]

[storage]
st

 <code>
</pre>

## How to add this role to your playbook
<pre>
 <code>
 - name: Install bdocker
   hosts: all
   become: yes
   roles:
   - { role: ansible-role-bdocker, tags: [ 'bdocker' ] }
   </code>
  </pre>

