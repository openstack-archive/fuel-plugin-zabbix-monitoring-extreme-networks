=============================================================================
Guide to the Extreme Networks hardware monitoring extension for Zabbix plugin
=============================================================================

Extreme Networks hardware monitoring extension plugin extends Zabbix plugin
functionality by adding monitoring of incoming SNMP traps sent from Extreme
Networks hardware via management network to Zabbix VIP address. For more
information about networks, see the `Logical Networks <https://docs.mirantis
.com/openstack/fuel/fuel-7.0/reference-architecture.html#logical-networks>`_
section of MOS documentation. The plugin configures snmptt to parse and pass
Extreme Networks specific traps to Zabbix. It also configures Zabbix by adding
Template with items and triggers and by creating Hosts for each Extreme
Networks hardware.

Requirements
============

================================== ================================
Requirement                        Version/Comment
================================== ================================
Fuel                               7.0, 8.0, 9.0, 9.1, 9.2 and 10.0
Zabbix plugin for Fuel             2.5.3
SNMP trap daemon for Zabbix plugin 1.1.2
================================== ================================

