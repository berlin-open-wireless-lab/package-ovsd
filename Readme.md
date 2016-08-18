# ovsd package for OpenWRT/LEDE

This repository provides the necessary files to install [ovsd](https://github.com/berlin-open-wireless-lab/ovsd), a daemon to tie in Open vSwitch devices with OpenWRT/LEDE's network interface daemon, netifd.


## Installation

Install this as a feed by adding the following line to `feeds.conf` in your OpenWRT/LEDE source tree:
```
src-git ovs https://github.com/berlin-open-wireless-lab/packages-ovsd.git
```
Next, run
```bash
scripts/feeds update ovs
scripts/feeds install ovsd
```
from the same directory. There should now be a package `ovsd` selectable in `Network` when you run
`make menuconfig`.
