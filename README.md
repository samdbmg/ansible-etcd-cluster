# etcd kicker

## Running (MWE)
A Vagrantfile is provided to spin up a three node cluster. Something like:

```
cd vagrant-demo
vagrant up
python vagrant2inventory.py > vagrant_inventory
ansible-playbook --private-key=~/.vagrant.d/insecure_private_key -i vagrant_inventory test-playbook.yml
```