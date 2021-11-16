# JSNAPY EXAMPLE: VALIDATE CHASSIS ALARMS

This example will show how to use JSNAPY to make sure there aren't any alarms on the box

## To run the playbook

Two options provided:

### Dockerfile

1. build the container image with

```sh
make container
```

2. run the playbook within the container

```sh
make ansible
```

### Your own Python environment

1. install python dependencies 

```sh
pip install -r docker/requirements.txt
```

2. change into Ansible directory 

```
cd ansible
```

3. install Juniper Ansible modules 

```sh
ansible-galaxy install juniper.junos
```

4. type 

```sh
ansible-playbook pb.jsnapy.chassis.alarms.yaml
```

## Dependencies

Official Juniper Ansible modules

```sh
ansible-galaxy install juniper.junos
```

## How it works

The playbook works like this:

- We will be requesting the chassis alarm information
- The output will be stored as an object called `test_alarms`
- We assert the pass/fail within the playbook

## examples screenshot
![ansible-playbook pb.jsnapy.chassis.alarms.yaml](./static/images/screenshot.png)
