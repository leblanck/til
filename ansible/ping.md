# Sending a Ping to All Hosts

Often when setting up new inventory/host files to use with Ansible I like to 'ping' these hosts to check basic connectivity. Ansible ping doesn't send standard ping packets, it instead will SSH into that host.

To run an Ansible ping: 

```
ansible all -m ping -v -i hosts
```
