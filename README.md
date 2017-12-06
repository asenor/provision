# Provision

## Configuration

Create vars.yml and inventory:

```
cp vars.yml.dist vars.yml
cp inventory.dist inventory
```

Edit both files to meet your needs.

## Run

```
ansible-playbook playbook.yml
```
