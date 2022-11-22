# redis rule
Ansible role to create a 3 nodes redis server with 3 snetinels. Active passive clustering with authentication
## How to test the Role
The role use ansible molecule to create infrastructure and run the playbooks on local machine. The driver used for molecule con be both podman or docker.

A "cluster" scenario has been created in order to test deployment on 3 nodes.

### Commands

* Check ansible-lint of a 3 nodes scenario: molecule lint -s cluster
* Converge infrastructure: molecule converge -s cluster --destroy=never
* Test everything: molecule test -s cluster --destroy=never
