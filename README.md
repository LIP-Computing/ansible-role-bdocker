# ansible-role-bdocker
Ansible Role to install bdocker in a cluster
At this point in time, this role assumes that you are working with systemd enabled OSs.


## Inventory file sample:
<pre>
 <code>
[ui]
cluster-ui bdocker_role="client"

[frontend]
cluster bdocker_role="accounting"

[wn]
cluster-wn01 bdocker_role="working"
cluster-wn02 bdocker_role="working"

[storage]
st
 </code>
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

