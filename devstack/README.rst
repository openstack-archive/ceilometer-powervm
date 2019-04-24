========================
Installing with Devstack
========================

1. Download DevStack::

    $ git clone https://opendev.org/openstack/devstack /opt/stack/devstack

2. Modify DevStack's local.conf to pull in both Ceilometer and this project by adding::

    [[local|localrc]]
    ...
    enable_plugin ceilometer opendev.org/openstack/ceilometer
    enable_plugin ceilometer-powervm opendev.org/openstack/ceilometer-powervm

3. See ceilometer-powervm/doc/source/devref/usage.rst, then configure
   the installation through options in local.conf as needed::

    [[local|localrc]]
    ...

   Example devstack config files for all-in-one, compute, and control nodes `can be 
   found here <https://opendev.org/openstack/ceilometer-powervm/src/branch/master/devstack>`_

4. Run ``stack.sh`` from devstack::

    $ cd /opt/stack/devstack
    $ ./stack.sh
