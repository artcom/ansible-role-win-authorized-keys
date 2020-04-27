# Win authorized_keys

Ansible role for setting authorized_keys on a Windows machine

## Role Variables
Available variables are listed below, along with default values `(see defaults/main.yml)`:
```yaml
win_authorized_keys_ssh_user_dir: "{{ ansible_user_dir }}"
win_authorized_keys_public_keys:
  operator: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}"
```

## Dependencies
None

## Example Playbook
```yaml
- hosts: all
  roles:
    - role: win-gitlab-app
```
