Configured on Ubuntu 18.04.01 and Ansible 2.5.1

1) Run sudo apt-get install ansible curl - install both.
2) Local user must have admin right privileges and password must be set up as '123'
3) Copy the two .yaml files to desktop
4) CD to Desktop and run the playbooks with commands:
	a) ansible-playbook elk.yaml --extra-vars "ansible_become_pass=123"
	b) ansible-playbook logstash.yaml --extra-vars "ansible_become_pass=123"

Running files as local admin:
 I could have used '--ask-become-pass' to ask for elevated privileges each time - but i think this is unneccesary and time consuming for the task. Another option was Using Ansible vault to create a secret file - but requires more input from the User to set it up intially.




