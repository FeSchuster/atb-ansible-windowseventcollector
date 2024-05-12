Ansible Role: atb-ansible-windowseventcollector
=========

Setup a Windows Event Collector based on the [Windows Event Forwarding repo from Palantir](https://github.com/palantir/windows-event-forwarding). In my setup I further utilized [Winlogbeat](https://www.elastic.co/de/beats/winlogbeat) to ship the collected logs to a [Kafka broker](https://kafka.apache.org/). Thus, it can be easily adopted to forward logs to an ELK-Stack.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

```
kafka_broker_ip: 192.168.10.3
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
