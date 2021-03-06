Build the best of OpenPOWER platform virtualization
***************************************************

Considering the speed of the development of new features, or even Hardware is
created in the OpenPOWER ecosystem, it's a challenge to get them in the
traditional stable GNU/Linux distribution scenario.

open-power-host-os/builds repository is a open source collaboration effort that
aims to help administrators to build and deploy the latest and greatest
capabilities in the OpenPOWER world through a build script that provides
software well packaged and designed for the `Supported GNU/Linux distributions`_

Supported GNU/Linux distributions
---------------------------------

* CentOS 7.2 PPC64LE

Installation
------------

RPM Based distributions
^^^^^^^^^^^^^^^^^^^^^^^
* Install epel repository (Extra Packages for Enterprise Linux):

::

# sudo yum install --downloadonly --downloaddir=. epel-release
# sudo yum localinstall epel-release-7-5.noarch.rpm # Note the version may change.

* Install

 - mock
 - PyYAML
 - git
 - python-pygit2

::

# sudo yum install -y mock PyYAML git python-pygit2

Settings
--------

 * Disable SMT

::

# sudo ppc64_cpu --smt=off

Running
-------

 * Build a single package

::

# sudo python host-os-build.py --package libvirt --verbose

 * Build all software

::

# sudo python host-os-build.py --package libvirt --verbose

Validating
----------

There is a whole repository dedicated to testing available at
https://github.com/open-power-host-os/tests

