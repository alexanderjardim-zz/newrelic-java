newrelic-java
=============

Ansible role for deploy New Relic Java agent

Requirements
------------

You need a working java container.

Role Variables
--------------

- **newrelic_license_key**: your New Relic license key 
- **newrelic_dir**: New Relic agent installation directory. Defaults to '/home/vagrant/newrelic'
- **newrelic_download_dir**: where your control machine will download New Relic. Defaults to '~/Downloads'
- **newrelic_version**: New Relic version that will be installed. Defaults to '3.7.0'
- **newrelic_container**: Which java container will you use? Defaults to 'tomcat'. This is the only one supported right now. If you to use with another contaner, you will have to do the '-javaagent' setup by yourself.
- **newrelic_download_url**: Where will you get New Relic package from? Defaults to *https://oss.sonatype.org/content/repositories/releases/com/newrelic/agent/java/newrelic-java/{{newrelic_version}}/newrelic-java-{{newrelic_version}}.zip*. Thanks sonatype.org :-D

Dependencies
------------

none

Example Playbook
-------------------------

    - hosts: all
      roles:
         - { role: alexanderjardim.newrelic-java-agent, newrelic_license_key: 'qwroibwvioqygvqe' }

License
-------

BSD

Author Information
------------------

alexander.ramos.jardim+newrelic-java@gmail.com
