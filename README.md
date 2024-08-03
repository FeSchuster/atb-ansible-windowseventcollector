Ansible Role: atb-ansible-windowseventcollector
=========

Setup a Windows Event Collector based on the [Windows Event Forwarding repo from Palantir](https://github.com/palantir/windows-event-forwarding). In my setup I further utilized [Winlogbeat](https://www.elastic.co/de/beats/winlogbeat) to ship the collected logs to a [Kafka broker](https://kafka.apache.org/). Thus, it can be easily adopted to forward logs to an ELK-Stack for example.

Requirements
------------

A domain joined server is necessary with internet access as during play necessary binaries will be downloaded. For plug and play a GPO pointing to the WEC is required and included in [domain promotion role](https://github.com/ait-testbed/atb-ansible-primarydc). 

Reference roles:
- [atb-ansible-msclient](https://github.com/ait-testbed/atb-ansible-msclient)
- [atb-ansible-simplekafka](https://github.com/ait-testbed/atb-ansible-simplekafka)

Role Variables
--------------

```yaml
kafka_broker_ip: {{ kafka_IP }}
```

Dependencies
------------
pywinrm

Example Playbook
----------------
```yaml
    - hosts: servers
      roles:
         - atb-ansible-msclient
         - atb-ansible-windowseventcollector
```

License
-------

MIT

Author Information
------------------

Sebahattin Sahin
