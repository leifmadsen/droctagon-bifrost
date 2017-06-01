droctagon-bifrost
=================

This is an Ansible playbook (and roles) for spinning up Bifrost.

Bifrost is a system that leverages Ironic to bootstrap baremetal machines 
using PXE booting and installing an operating system via disk image.

Bifrost itself is also an Ansible playbook, but, it requires some tweaks that
are both not trivial. Use of this playbook helps to bootstrap some of the
configuration of Bifrost itself and provides an example configuration for your
network.

Usage
-----

Simply clone this repo and run it with:

::

    $ ansible-playbook -i inventory/bifrost.inventory bifrost.yml

But, you're even more likely going to configure it first...

Configuration
-------------

Inventory: Copy the ``./inventory/example/`` into a new inventory environment
directory (e.g. ``./inventory/testing/``).

You'll then want to create your own suite of JSON inventory that's specific to
the baremetal nodes that you're going to manage with Bifrost.

More on this later, but, you'll find the file you want to customize as
``./inventory/<your_environment>/group_vars/bifrost.yml``

Dr Octagon
----------

This playbook is part of the Dr. Octagon Lab, a series of tools to manage a
laboratory for NFV on OpenShift and OpenStack.

![Dr. Octagon NFV Laboratory](http://i.imgur.com/lQOHIBC.png)
