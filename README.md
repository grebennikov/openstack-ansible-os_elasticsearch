# ECS Elasticsearch

An `openstack-ansible` compatible role for Elasticsearch deployment on
ECS platforms.

## Original Work

This play is heavily based on the original [Ansible Elasticsearch][1]
repo released by Elastic. Significant portions of the original work
have been rewritten, but the basis for many process flows remain. The
original repository should be referenced for any future changes to
the Elasticsearch installation process, and adapted into this play
accordingly.

### Specific Modifications

* Dropped all support for `systemd`. We'll worry about that when we worry
about running Ubuntu 16.04LTS.
* Dropped all support for RHEL/CentOS operating systems.
* Implemented our own procedure for installing Java on Ubuntu.
* Added Python installation support, with `pbr`.
* Followed the `openstack-ansible` layout and moved some playbook features
into the [ECS Infrastructure][2] playbook.

## Copyright

Copyright &copy; 2016 Internet Solutions (Pty) Ltd

## License

Licensed under the Apache Software License 2.0. See LICENSE for details.

[1]: https://github.com/elastic/ansible-elasticsearch/
[2]: https://git.lab.isoc.co.za/elasticcloud/infrastructure/
