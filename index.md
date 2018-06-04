---
layout: default
---
{% include variables.md %}

# OpenPOWER Host OS

The OpenPOWER Host OS is an open source project that consists of a set
of software components, including the Linux kernel and KVM
virtualization technologies such as QEMU, with added code to provide
support for OpenPOWER hardware.

The project provides the core [components](#components) and a simple
build framework that allows the packaging and installation atop a
traditional GNU/Linux distribution with the intent of facilitating
development/experimentation with POWER.

### What's new
Explore our [latest release]({{ latest_release.url }}).
{% if latest_release.highlights %}
Here are its highlights:

{{ latest_release.highlights }}
{% endif %}

### Components

Host OS delivers a packaged version of a set of open source projects,
installable over a GNU/Linux distribution. The list of Host OS
components is (without dependencies):

[kernel](https://github.com/open-power-host-os/linux.git)\\
[qemu](https://github.com/open-power-host-os/qemu.git)\\
[libvirt](https://github.com/open-power-host-os/libvirt.git)\\
[ppc64-diag](https://github.com/open-power-host-os/ppc64-diag.git)\\
[libvpd](https://github.com/open-power-host-os/libvpd.git)\\
[lsvpd](https://github.com/open-power-host-os/lsvpd.git)\\
[libservicelog](https://github.com/open-power-host-os/libservicelog.git)\\
[servicelog](https://github.com/open-power-host-os/servicelog.git)\\
[SLOF ](https://github.com/open-power-host-os/slof.git)


### Versioning

The project as a whole has an independent versioning not tied to the
schedules of individual components.

Development versions are periodically built and validated via a [test
suite](https://github.com/open-power-host-os/tests). The latest tested
tag is [{{ latest_devel.release_tag }}]({{ latest_devel.url }}). The full
list of development tags is [here](/tags/devel). For released tags, look
[here](/tags/release).

About every 6 months a tag containing a more significant set of
features is promoted to stable. The current stable tag is [{{
latest_stable.release_tag }}]({{ latest_stable.url }}).


### Getting Started

The [Quick Start guide]({{ builds_repo }}/blob/master/README.md) explains how you
can create packages ready for installation on CentOS and optionally a
bootable Host OS ISO file.

Host OS components are packaged by a [build script]({{ builds_repo }})
that reads from a git repository containing packages [metadata]({{
versions_repo }}). You are encouraged to build your own version and
experiment with the various components and their features.


### Going further

During your exploration time with POWER and Host OS, feel free to ask
questions, raise issues, contribute code and interact with the
packages maintainers.

One way to share your ideas, specially when regarding single Host OS
components, is via the "Issues" page at the component's GitHub
repository.

For those wishing to continuously develop and build packages on top of
Host OS, the [tests]({{ tests_repo }}) and [infrastructure]({{
infra_repo }}) repositories will be of use in reproducing the build
system and test infrastructure.


#### Contact us via:

IRC: #hostos @freenode\\
email:
[open-power-host-os@mailinglist.openpowerfoundation.org](mailto:open-power-host-os@mailinglist.openpowerfoundation.org)
([subscription link](http://lists.mailinglist.openpowerfoundation.org/mailman/listinfo/open-power-host-os))

---
\\
Other references:\\
1- [https://developer.ibm.com/open/openprojects/openpower-host-os/](https://developer.ibm.com/open/openprojects/openpower-host-os/)
