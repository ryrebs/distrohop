# distrohop

Setup a minimal environment for your favorite linux distro using Ansible.

_Supported Distros_:

<img src="./manjaro-icon.png" width="30" height="30"/>
<img src="./debian-icon.png" width="30" height="30"/>

Dependencies: 

 - python3.11 
 - pipenv
 - ansible

Getting started:

1. Install `pipenv`

2. Install other dependencies:

    `pipenv install` (On project root)

3. Run the playbook:

    `pipenv run python -m ansible playbook ./playbook.yml -K <options..>`

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
- browerser: [firefox, chromium]