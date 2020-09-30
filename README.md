# Win authorized_keys
Ansible role for setting authorized_keys on a Windows machine

## Requirements
None

## Role Variables
Available variables are listed below, along with default values `(see defaults/main.yml)`:
```yaml
ssh_user: null
ssh_user_dir: null
public_keys: null

```
Required variables (role will fail if the variables are not set):
```yaml
ssh_user: "string"
ssh_user_dir: "string"
public_keys:
  user_name_key: "string"
```

## Dependencies
* [check-required-variables](https://github.com/artcom/ansible-role-check-required-variables)

## Example Playbook
```yaml
- hosts: all
  tasks:
    - import_role:
        name: win-authorized-keys
      vars:
        ssh_user: "{{ ansible_user }}"
        ssh_user_dir: "{{ ansible_user_dir }}"
        public_keys:
          operator: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}"
```

## License
MIT
