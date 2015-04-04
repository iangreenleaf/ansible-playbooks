# Ian's Ansible playbooks #

[Ansible](http://www.ansibleworks.com/) playbooks for my various apps.

Contains bits and pieces from other generous souls.

This is all the explanation you're gonna get for the moment.

## Deploy ##

    ansible-galaxy install -r roles.csv -f -p galaxy

### Dev ###

    ansible-playbook tracks.yml -i ./ansible_hosts

### Prod ###

    ansible-playbook tracks.yml
