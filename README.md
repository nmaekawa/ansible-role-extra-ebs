extra-ebs
=========

given a device and a mountpoint, creates the filesystem in the device (ext4)
and mounts it.

requirements
------------

target os is ubuntu 16.04 or higher

role variables
--------------

ebs_device: default is /dev/xvdf
ebs_mountpoint: default is /mnt/extra_ebs


example playbook
----------------
    - hosts: all
      tasks:
         - include_role:
             name: ansible-role-extra-ebs
           vars:
              ebs_mountpoint: /opt/data
              ebs_device: /dev/sdb

License
-------

MIT

