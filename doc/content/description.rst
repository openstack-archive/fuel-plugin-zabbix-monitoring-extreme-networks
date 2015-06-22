================================================================
Extreme Networks hardware monitoring extension for Zabbix plugin
================================================================

Extreme Networks hardware monitoring extension plugin extends Zabbix plugin
functionality by adding monitoring of incoming SNMP traps sent from Extreme
Networks hardware via management network to management VIP address. For more
information about networks, see the `Logical Networks <https://docs.mirantis
.com/openstack/fuel/fuel-6.1/reference-architecture.html#logical-networks>`_
section of MOS documentation. The plugin configures snmptt to parse and pass
Extreme Networks specific traps to Zabbix. It also configures Zabbix by adding
Template with appropriate items and triggers and by creating Hosts for each
Extreme Networks hardware.

Requirements
============

================================== ===============
Requirement                        Version/Comment
================================== ===============
Fuel                               6.1
Zabbix plugin for Fuel             1.0.0
SNMP trap daemon for Zabbix plugin 1.0.0
================================== ===============

