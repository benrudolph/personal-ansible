## Setup

```
pip install -r requirements.txt
ansible-galaxy install -r requirements.yml
ansible-playbook deploy.yml -u root
```

## Running the playbook

To run all roles first setup the proper ansible vault password in `~/.ansible-password` (currently only needed
for the `pd` role).

```
ansible-playbook deploy.yml -u root --diff --vault-id ~/.ansible-password --extra-vars "@secrets.yml"
```

Running with tags. There are multiple tags available:

```
common
zsh
rbenv
node
swap
postgresql
pd
```
