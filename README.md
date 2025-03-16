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

3. Update `common-vars.yml`

4. Run the playbook:

   ```
   pipenv run runplaybook \
       -i inventory.yml \ (if remote node)
       -v \
       --flush-cache \
       --extra-vars="[vars..]" \
       --skip-tags [tags..] \
       --tags [tags..]
       --ask-pass \
       --ask-become
   ```

Tags: base, dev

Sample for localhost:

```
pipenv run runplaybook \
    -v \
    --flush-cache \
    --skip-tags [tags..] \
    --tags base,virtualbox,cleanup \
    --ask-become
```

Sample for remote managed node:

```
pipenv run runplaybook \
    -i inventory.yml \
    -v \
    --flush-cache \
    --skip-tags [tags..] \
    --tags base,dev,cleanup \
    --extra-vars="remote=yes" \
    --ask-pass \
    --ask-become
```

Base packages:

- apparmor
- firejail
- ufw
- clamav
- tlps
- redshift / gammastep
- yay
- firefox
- jdk-openjdk
- blueman

Dev packages:

- terminator
- git
- vim
- chromium
- default-jdk
- zplug
- zsh
- nvm
- golang
- docker
- docker compose
- codium
- virtualbox
- nodejs
- xpad
- eog
- brave
