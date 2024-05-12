Ansible Role: atb-ansible-windowseventcollector
=========

Setup a Windows Event Collector based on the [Windows Event Forwarding repo from Palantir](https://github.com/palantir/windows-event-forwarding). In my setup I further utilized [Winlogbeat](https://www.elastic.co/de/beats/winlogbeat) to ship the collected logs to a [Kafka broker](https://kafka.apache.org/). Thus, it can be easily adopted to forward logs to an ELK-Stack.

Requirements
------------

pywinrm

Role Variables
--------------

```
kafka_broker_ip: 192.168.10.3
```

Dependencies
------------

A domain joined server is necessary with internet access as during play necessary binaries were downloaded. For plug and play a GPO pointing to the WEC is required. <br>

Reference roles:
- [atb-ansible-msclient](https://github.com/ait-testbed/atb-ansible-msclient)
- [atb-ansible-simplekafka](https://github.com/ait-testbed/atb-ansible-simplekafka)


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - atb-ansible-msclient
         - atb-ansible-windowseventcollector

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
