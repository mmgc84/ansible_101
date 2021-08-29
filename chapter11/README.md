# Ansible Custom Dynamic Inventory Example

This folder contains custom PHP and Python dynamic inventory scripts for use with Ansible.

The scripts has comments for all the different parts of the code which generate and return the inventory in the proper JSON format expected by Ansible.

## Testing these scripts

A Vagrantfile is provided, so you can build a three local VMs to test with the inventory scripts. Make sure you have Vagrant and VirtualBox installed, and run `vagrant up` inside this folder to build the two VMs, with the IP addresses `192.168.60.10`, `192.168.60.11` and `192.168.60.12`.

Then run the following command to test the inventory file with Ansible:

    # For the the Python script.
    $ ansible all -i inventory/inventory.php -m ping
    $ ansible all -i inventory/inventory.php -m debug -a "var=example_variable"

    # For the Python script.
    $ ansible all -i inventory/inventory.py -m ping
    $ ansible all -i inventory/inventory.py -m debug -a "var=example_variable"