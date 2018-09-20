## Running the playbook

As this is a brand new instance with only a root user we need to pass some parameters to the ansible command in order to succesfully connect.
The following command will ask for the root password and for the ansible vault pass.

Change it for your configuration or environment

```
ansible-playbook configure_user.yml --ask-vault-pass -u root -k
```

The current vault pass for the secrets.yml file is 'devops'. You can use the following command if you want to change the password associated with that file

```
ansible-vault rekey secrets.yml
```
