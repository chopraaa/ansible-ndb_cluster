# ansible-ndb_cluster

Ansible playbooks for installing and configuring a NDB cluster across 3 nodes.

## Usage

```
ansible-playbook main.yml -i inventory
```

## Sample Inventory

```ini
[ndb-master]
master ansible_host=139.59.80.36 ansible_private_host=10.139.216.161

[ndb-slaves]
node01 ansible_host=139.59.95.94 ansible_private_host=10.139.56.133
node02 ansible_host=139.59.94.207 ansible_private_host=10.139.56.180

[ndb-client]
master

[all:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_user=root
```

## Author

Varun Chopra (@chopraaa)
