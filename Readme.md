# ovsd package for OpenWRT/LEDE

### NOTE: as of April 2021 this has been merged into the [OpenWrt master](https://github.com/openwrt/packages/tree/master/net/ovsd) and is set for becoming part of future OpenWrt releases. 

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
