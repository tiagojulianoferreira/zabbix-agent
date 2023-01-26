zabbix-agent
=========

Esta role Ansible implementa o agente do Zabbix em hosts a serem monitorados. Ela gera um usuário e uma chave PSK que são exibidos nos console de execução da playbook.

Requirements
------------

- Credenciais de acesso SSH ao host alvo.

Role Variables
--------------

São obrigatórias as seguintes variáveis:

```
zabbix_server: zabbix.example.com
zabbix_version: 5.4
```

Example Playbook
----------------

```
- name: Garante a instalação e configuração do Zabbix Agent
  hosts: webserver1
  gather_facts: true
  become: true
  vars:
    zabbix_server: zabbix.example.com
    zabbix_version: 5.4
  roles:
    - zabbix-agent
```

License
-------

BSD

Author Information
------------------

Tiago Juliano Ferreira.
