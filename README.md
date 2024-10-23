# Ansible-Role: acr-ansible-limesurvey

AIT-CyberRange: Installs and runs limesurvey via docker-compose

## Requirements

- Debian or Ubuntu 
- Gitlab

## Role Variables

```yaml
--- 
limesurvey_user: limesurvey
limesurvey_basepath: /opt/limesurvey

limesurvey_docker_repo_url: https://github.com/adamzammit/limesurvey-docker.git

limesurvey_admin_user: limesurvey
limesurvey_admin_password: limesurvey
limesurvey_admin_name: Lime Administrator
limesurvey_admin_email: limesurvey@cyberrange.at

limesurvey_timezone: Europe/Vienna

limesurvey_mysqldb_password: limesurvey_db_password

limesurvey_service_execstart: docker-compose up
limesurvey_ssl_cert: /etc/ssl/server.crt
limesurvey_ssl_key: /etc/ssl/server.key
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: limesurvey

```

## License

GPL-3.0

## Author

- Lenhard Reuter