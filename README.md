# Ansible Role: Jenkins Slave CI

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    jenkins_home: /var/jenkins

The home directory of Jenkins.

    jenkins_slave_name: slave

The name of Jenkins slave node.

    jenkins_master_hostname: localhost

The system hostname of Jenkins master node.

    jenkins_master_port: 8080

The HTTP port for Jenkins master node.

    jenkins_master_username: admin
    jenkins_master_password: admin

The admin account credentials of Jenkins master node.

## Dependencies

davidwittman.redis

## Example Playbook

```yaml
```

## License

APACHE.
