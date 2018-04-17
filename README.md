# Provision

## Configuration

Create vars.yml and hosts:

```
cp vars.yml.dist vars.yml
cp hosts.dist hosts
```

Edit both files to meet your needs.

## Run

```
ansible-playbook playbook.yml
```
