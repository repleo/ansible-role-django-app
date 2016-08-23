# Ansible Role: git server via https by nginx

[![Build Status](https://travis-ci.org/repleo/ansible-role-django-app.svg?branch=master)](https://travis-ci.org/repleo/ansible-role-django-app)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-repleo.django--app-660198.svg?style=flat)](https://galaxy.ansible.com/repleo/django-app)

Ansible role for installing a Django application with a Postgres database and NGINX / uWSGI application server stack.

## Requirements

Only tested on ubuntu and debian for now.

## Role Variables

Available variables are listed below, along with default values:

```yaml
www_domain: "example.com",
dbuser: "example",
dbpassword: "3x4mple",
dbname: "example",
ssl_cert: "example.com_chain.pem",
ssl_key: "example.com.key"
```


## Dependencies

 - repleo.nginx - Installs nginx server and configures virtual host for given domainname.
 - repleo.postgresql - Installs database server and configures database.

## Example Playbook

    - hosts: servers
      roles:
      - { role: repleo.django-app,
                www_domain: "example.com",
                dbuser: "example",
                dbpassword: "3x4mple",
                dbname: "example",
                ssl_cert: "example.com_chain.pem",
                ssl_key: "example.com.key"
        }

## License

GPL v3 - (c) 2016, Repleo, Amstelveen

Author Information
------------------

Repleo, Amstelveen, Holland -- www.repleo.nl  
Jeroen Arnoldus (jeroen@repleo.nl)
