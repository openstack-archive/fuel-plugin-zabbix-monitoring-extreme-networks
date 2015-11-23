==================
Installation Guide
==================

Installing Extreme Networks hardware monitoring extension
=========================================================

To install Extreme Networks hardware monitoring extension for Zabbix plugin,
follow these steps:

1. Download and install the Zabbix plugin for Fuel from the
   `Fuel Plugins Catalog <https://www.mirantis.com/products/
   openstack-drivers-and-plugins/fuel-plugins/>`_.
2. Download and install the SNMP trap daemon for Zabbix plugin from the
   `Fuel Plugins Catalog <https://www.mirantis.com/products/
   openstack-drivers-and-plugins/fuel-plugins/>`_.
3. Download the Extreme Networks hardware monitoring extension for Zabbix
   plugin from the `Fuel Plugins Catalog <https://www.mirantis.com/products/
   openstack-drivers-and-plugins/fuel-plugins/>`_.
4. Copy all three plugins from your local machine to a previously deployed
   Fuel Master node using ssh. If you do not have the Fuel Master node yet,
   see `Quick Start Guide <https://software.mirantis.com/quick-start/>`_::

    # scp zabbix_monitoring-2.5-2.5.0-1.noarch.rpm \
      root@<The_Fuel_Master_node_IP>:/tmp
    # scp zabbix_snmptrapd-1.0-1.0.0-1.noarch.rpm \
      root@<The_Fuel_Master_node_IP>:/tmp
    # scp zabbix_monitoring_extreme_networks-1.0-1.0.0-1.noarch.rpm \
      root@<The_Fuel_Master_node_IP>:/tmp

5. Log into the Fuel Master node. Install each of the three plugins using
   the following commands::

    # cd /tmp
    # fuel plugins --install \
      zabbix_monitoring-2.5-2.5.0-1.noarch.rpm
    # fuel plugins --install \
      zabbix_snmptrapd-1.0-1.0.0-1.noarch.rpm
    # fuel plugins --install \
      zabbix_monitoring_extreme_networks-1.0-1.0.0-1.noarch.rpm

6. Make sure the plugins were installed correctly::

    # fuel plugins
    id | name                               | version  | package_version
    ---|------------------------------------|----------|----------------
    1  | zabbix_monitoring                  | 2.5.0    | 3.0.0
    2  | zabbix_snmptrapd                   | 1.0.0    | 2.0.0
    3  | zabbix_monitoring_extreme_networks | 1.0.0    | 2.0.0

