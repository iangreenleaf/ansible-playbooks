# Ian's Ansible playbooks #

[Ansible](http://www.ansibleworks.com/) playbooks for my various apps.

Contains bits and pieces from other generous souls.

This is all the explanation you're gonna get for the moment.

## Deploy ##

    ansible-galaxy install -r galaxy-roles.yml -f -p galaxy

### Dev ###

    vagrant up
    ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory --become playbook.yml

### Prod ###

    ansible-playbook playbook.yml
