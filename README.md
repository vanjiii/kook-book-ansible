# kook-book-ansible

Ansible config for github.com/vanjiii/kook-book-server

## Usage

``` bash
ansible-playbook playbook.yaml
```

This will checkout `kook-book-server` repo into `code` direcotory, build and
run the server. If changes are present into the source code it will execute
health-check handler.
