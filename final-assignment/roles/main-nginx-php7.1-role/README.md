Role Name
=========

Final assignment install nginx and php7.1

Requirements
------------

When access default web server is php-info, 1 domain is php-info, 1 domain is hello-world
Client can resolve domain by edit /etc/hosts

Role Variables
--------------

Default domain is mtuan.com, if you need to change domain, append -e domain=tuantest.com in the command ansible-playbook 

Dependencies
------------

No dependencies

Example Playbook
----------------

$ ansible-inventory -i hosts --graph
```
@all:
  |--@ungrouped:
  |--@web-server:
  |  |--192.168.1.101
  |  |--192.168.1.102
```
$ ansible-playbook main-nginx-php7.1-role.yml -i hosts -e hostname=web-server[0]

$ ansible-playbook main-nginx-php7.1-role.yml -i hosts -e hostname=web-server[1] -e domain=tuantest.com

Step by step install 
```
$ ansible-playbook main-nginx-php7.1-role.yml -i hosts -e hostname=web-server[0] -t install-nginx
$ ansible-playbook main-nginx-php7.1-role.yml -i hosts -e hostname=web-server[0] -t install-php7.1
$ ansible-playbook main-nginx-php7.1-role.yml -i hosts -e hostname=web-server[0] -t config-nginx
```
License
-------

...

Author Information
------------------

...