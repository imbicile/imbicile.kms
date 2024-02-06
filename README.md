# Role Name

KMS Server

## Sources

https://github.com/Wind4/vlmcsd

## Binary

Replace empty binary `/files`

## Windows Activation

```
 slmgr.vbs -upk
 slmgr.vbs -ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
 slmgr.vbs -skms <IP или FQDN хоста KMS>:1688
 slmgr.vbs -ato
 slmgr.vbs -dlv
```

## Example Playbook

```
- name: Install KMS server
  hosts:
    - all
  become: true
  roles:
    - role: imbicile.kms
      tags: kms
```
