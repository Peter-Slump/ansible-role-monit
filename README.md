# Ansible role Monit

Version: 0.1.0

Supported OS: Ubuntu

Ansible role Monit

- Configures a set of usefull OS monitoring configurations

## Role variables
```
# Used SSH port, used for monitoring configuration of sshd
monit_ssh_port: 22

# Mail server configuration, used to send notification mails.
monit_mailserver_enabled: False  # Indicates if mail server should be configured

monit_mailserver: smtp.example.com
monit_mail_port: 587
monit_mail_username: monit@example.com
monit_mail_password: some-secret-password
monit_mail_hostname: example.com
# TLSV1 or SSL
monit_mail_encryption: TLSV1

# Mail address to send the notification to.
monit_notify_email: monit@example.com
```

## Example
```
- hosts: all
  roles:
    - role: monit
      monit_notify_email: joe@example.com
```
