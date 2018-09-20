## How to run the playbook

In order to see the playbook fail and recover use

```
 ansible-playbook site.yml --extra-vars "should_fail=True"
```

If you want it to succed use the following command

```
 ansible-playbook site.yml --extra-vars "should_fail=False"
```

Using the --extra-vars enables us to overwrite the existing var in the playbook


