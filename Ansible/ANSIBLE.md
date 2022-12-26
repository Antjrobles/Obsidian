---
title: "Ansible"
description: Automation Servers
created: 08-10-2022 
tags:
- Program
- Automation
- Linux
- Servers
---
# INTRODUCTION AND LINKS
#### DESCRIPTION
Ansible is a software tool that provides simple but powerful automation for cross-platform computer support. It is primarily intended for IT professionals, who use it for application deployment, updates on workstations and servers, cloud provisioning, configuration management, intra-service orchestration, and nearly anything a systems administrator does on a weekly or daily basis. Ansible doesn't depend on agent software and has no additional security infrastructure, so it's easy to deploy. 
#### LINKS
- [Home Page](https://www.ansible.com/)
- [Docs](https://docs.ansible.com/ansible/latest/index.html)

## ANSIBLE COMANDS

- `ansible all --list-hosts`  - Listar todos los "hosts" disponibles
- `ansible all -m ping` - Hacer Ping a los hosts
- `ansible (all o nombre del host,ip ...) -m gather_facts` - Obtener información de los hosts.
```bash
ansible (all o nombre del host,ip ...) -m shell -a "ls -l"
 # Ejecutar comando en los hosts.
```
