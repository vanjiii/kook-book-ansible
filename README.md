# kook-book-ansible

Ansible config for github.com/vanjiii/kook-book-server

## Usage

``` bash
ansible-playbook playbook.yaml --ask-vault-pass
# pass: Secret123
```

This will checkout `kook-book-server` repo into `code` direcotory, build and
run the server. If changes are present into the source code it will execute
health-check handler.

Currently it uses ansible secrets. To use Hashicorp vault for secrets management:<br>
- run the `docker-compose.yaml` in `./hashicorp-vault`;
- remove ansible-vault code from the playbook
- uncomment hashicorp code
- NB: read `./hashicorp-vault/README.md` for login or genenaral info

To create new secrets file:
``` bash
ansible-vault create secret.yaml
```
