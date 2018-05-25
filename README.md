# ansible-beats

[![Build Status](https://travis-ci.org/kjenney/ansible-beats.svg?branch=master)](https://travis-ci.org/kjenney/ansible-beats)

Install and configure Elastic [beats](https://www.elastic.co/products/beats) v6.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: kjenney.beats }

Variables
---------

For complete documentation on configuration options see the [metricbeat](https://www.elastic.co/guide/en/beats/metricbeat/master/index.html), [filebeat](https://www.elastic.co/guide/en/beats/filebeat/master/index.html) and [packetbeat](https://www.elastic.co/guide/en/beats/packetbeat/master/index.html) documentation.

`beats_package_name` *(default "metricbeat")* The package name of the beat. Valid options are "metricbeat", "filebeat" "packetbeat" or "heartbeat".

`beats_package_version` *(default "6.2.2")* The package version of the beat.

`beats_install` *(default true)* Whether to install the beat.

`beats_config` *(default "")* The yaml configuration for the beat. If undefined by the user, no configuration will be applied.

`beats_geoip` *(default false)* Wether to install [geoip](https://dev.maxmind.com/geoip/legacy/) for use by the beat.

Acknowledgements
----------------

This role is based on [JMatt Peterson's](https://github.com/jmatt) Ansible Galaxy role [`jmatt.beats`](https://galaxy.ansible.com/jmatt/beats/). This role installs v6, hence the new role.

License
-------

The MIT License. See the [LICENSE file](https://github.com/lsst-sqre/ansible-beats/blob/master/LICENSE).
