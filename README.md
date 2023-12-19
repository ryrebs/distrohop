# distrohop

Setup a minimal environment for your favorite linux distro using Ansible.

_Supported Distros_:

<p float="left">
    <img src="images/manjaro-icon.png" width="30" height="30"/>
    <img src="images/debian-icon.png" width="30" height="30"/>
</p>

Dependencies: 

 - python3.11 
 - pipenv
 - ansible

Getting started:

1. Install `pipenv`

2. Install other dependencies:

    `pipenv install` (On project root)

3. Run the playbook:

    `pipenv run runplaybook [ansible-options]`

Simple setup:

    <distro-name>-task.yml - Task related files
    <distro-name>-handlers.yml - Handlers
    common-vars.yml - Variables common to all distros

Base packages:

- apparmor
- firejail
- clamav
- tlp
- docker
- docker compose
- redshift
- yay
- terminator
- vim
- zsh
- git
- nvm
- golang
- browsers: [firefox, chromium]
- jdk-openjdk 