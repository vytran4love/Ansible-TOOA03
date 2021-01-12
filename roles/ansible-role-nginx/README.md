Role Name
=========

main-nginx-role.yml on host 192.168.1.101 and 192.168.1.102

Requirements
------------

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

$ ansible-inventory -i hosts --graph
	@all:
	  |--@remote_101:
	  |  |--192.168.1.101
	  |--@remote_102:
	  |  |--192.168.1.102
	  |--@ungrouped:
	  
$ ansible-playbook main-nginx-role.yml -i hosts -e hostname=all

$ ansible-playbook main-nginx-role.yml -i hosts -e hostname=all -t install

$ ansible-playbook main-nginx-role.yml -i hosts -e hostname=all -t config

$ ansible-playbook main-nginx-role.yml -i hosts -e hostname=all -e force_use_external_vhost=true -t config

License
-------

Author Information
------------------
