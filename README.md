# OpenPOWER Host OS web page
---

This repository uses [Jekyll](https://jekyllrb.com/) to produce a
static web page with information about OpenPOWER Host OS, its
components and release tags.

The posts in
[_posts](https://github.com/open-power-host-os/open-power-host-os.github.io/tree/master/_posts)
are created in an automated way each time a tag is built and tested by
the [build
script](https://github.com/open-power-host-os/builds/blob/master/lib/subcommands/build_release_notes.py).

Every post contains information about the release tag, the specific
commit IDs from the [build
script](https://github.com/open-power-host-os/builds) and [packages
metadata](https://github.com/open-power-host-os/versions) that were
used to build it and the branches and commit IDs of the packages
themselves.

Regular and stable release tags show up under
[/tags/](https://open-power-host-os.github.io/tags) and
[/tags/stable/](https://open-power-host-os.github.io/tags/stable) in
the web page, respectively.
