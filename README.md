# ansible-apps_controlm_agent

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_controlm_agent-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_controlm_agent)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_controlm_agent.svg)](https://github.com/lotusnoir/ansible-apps_controlm_agent/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_controlm_agent?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_controlm_agent)
[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/lotusnoir/apps_controlm_agent)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/lotusnoir/apps_controlm_agent)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Install anc configure BMC control-M agent in order to launch cron tasks
## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

As the package cannot be downloaded by a public link, you need to provide a path or url in order to install it, with default variables, this role dont change anything on the system. You need to set the config variables like in the exemple in order to start configuration.

## Examples

        ---
        - hosts: apps_controlm_agent
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_controlm_agent
          vars:
            controlm_agent_install_method: url # or file
            controlm_agent_install_url: "http://downloadpackage/xxxxxxxxx"
            controlm_agent_primary_server: "servername.exemple.fr"
            controlm_agent_auth_server: "servername.exemple.fr"



## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
