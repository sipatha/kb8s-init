### Create Ansible vault password

`ansible-vault create secrets/nodes_passwd.yaml`

add `sudo_pass:kadmin`. this willbe encrypted

### Running as sudo

In the `inventory/hosts` file add the variable to ensure the script run as sudo

### Running the playbook

USe the command to run the playbook;

`ansible-playbook playbooks/apt.yaml -i inventory/hosts --ask-vault-pass --extra-vars '@secrets/nodes_passwd.yaml'`


172.200.1.94 kb-m0 kb-m0.vmbt.local
172.200.1.50 kb-w0 kb-w0.vmbt.local
172.200.1.198 kb-w1 kb-w1.vmbt.local