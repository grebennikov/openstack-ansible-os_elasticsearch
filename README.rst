OpenStack-Ansible Elasticsearch
########################

Ansible role that installs and configures OpenStack elasticsearch. elasticsearch is
installed behind the Apache webserver listening on port 9200 by default.

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required Variables
==================

This list is not exhaustive at present. See role internals for further
details.

.. code-block:: yaml

    # elasticsearch TCP listening port
    elasticsearch_service_port: 9200

Example Playbook
================

.. code-block:: yaml

   - name: Install elasticsearch server
     hosts: elasticsearch_all
     user: root
     roles:
        - { role: "os_elasticsearch", tags: [ "os-elasticsearch" ] }
     vars:
       is_metal: "{{ properties.is_metal|default(false) }}"
