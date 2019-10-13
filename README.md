Role Name
=========

Creates and mounts a swap file to hosts.

Supported Operating Systems
---------------------------

* Debian (Stretch)
* Ubuntu (Bionic)

Requirements
------------

* Ansible 2.8+ (on execution host)

Role Variables
--------------

Two variables defined in defaults/main.yml file are
* swap_size_mb
* swap_file

Please ensure that the the swap_size_mb variable is defined with only numeric characters and the size is read in megabytes. So to create a 512Mb of swap file, please declare the variable swap_size_mb as 512. The variable swap_file is absolute path of the swap file to be created. So if you want to create a swapfile named **extraswap** inside **/** directory, the variable should be defined as **/extraswap**

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-role-swap

Add as a submodule to your playbook repo
----------------------------------------

    git submodule add https://github.com/tekniqueltd/ansible-role-swap roles/swap

Author Information
------------------

Teknique DevOps Team

Credits
-------

Forked from [devster31/swap.yml](https://gist.github.com/devster31/74e48cc1c8e73c637bc7)
