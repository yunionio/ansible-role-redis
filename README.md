# Ansible Role: Redis CI

In fact, this Role is the packaging of [davidwittman.redis](https://github.com/DavidWittman/ansible-redis).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    redis_slave: false 

Whether it is a slave node.

    redis_master_hostname: 

The hostname of redis mster node.

    redis_port: 6379

The port of redis.

About more variables, please see [davidwittman.redis](https://github.com/DavidWittman/ansible-redis).

## Dependencies

davidwittman.redis

## Example Playbook

playbook: 

```yaml
- name: configure the master redis server
  hosts: redis-master
  roles:
    - ansible-role-redis

- name: configure the slave redis server
  hosts: redis-slave
  vars:
    - redis_slave: true
    - redis_master_hostname: 10.168.222.140
  roles:
    - ansible-role-redis
```

inventory:

```yaml
[redis-master]
10.168.222.140

[redis-slave]
10.168.222.136
10.168.222.138
```

## License

APACHE.
