# Ansible Role: Kibana 5


An Ansible Role that installs Kibana on RedHat/CentOS or Debian/Ubuntu.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    kibana_version: "5.4"

The version of kibana to install (major and minor only).

    kibana_server_port: 5601
    kibana_server_host: "0.0.0.0"

The FQDN or IP address and port Kibana should use.

    kibana_elasticsearch_url: "http://localhost:9200"

The URL (including port) over which Kibana will connect to Elasticsearch.

Note that upgrading from 4.x to 5.x:
Kibana 4.x used a different config location than 5.0+, so if you’re upgrading from 4.x, you will need to copy the configurations from your old config (/opt/kibana/config/kibana.yml) to your new config (/etc/kibana/kibana.yml).


Note that the default vars are in a hash so unless you copy the entire set you will need to set your hash_behaviour to merge



## Dependencies

None.

## Example Playbook

    - hosts: kibana
      roles:
        - ansible-role-kibana


## Kibana configuration

https://www.elastic.co/guide/en/kibana/current/settings.html


## License

MIT / BSD

## Author Information
George Boobyer

This role based on a role created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).

Updated with elements from https://github.com/sansible/kibana.
