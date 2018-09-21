## How to run

Use the 'cloud' vault pass to run the play

```
ansible-playbook 00_site.yml --ask-vault-pass
```

Because I put the encrypted var file in the host_vars folder, even if I run an ad-hoc command using ansible, it will prompt for the vault password

This command will now fail as it need a password in order to decrypt the secret.yml file

```
ansible servers -a 'cat /etc/motd'
``` 

## Note to self

Try not to use encrypted file sin host_vars or group_vars if you are constantly using ad-hoc commands.
This is a non issue otherwise but it's a small detail that makes dubugging harder. Or just use password files :)


