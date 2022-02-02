# Clash Premium Installer

Simple clash premium core installer with full tun support for Linux.

修改自Kr328原脚本适配OpenWrt Snapshot



### Usage

openwrt snapshot已经从fw3转到fw4(使用nftables)

官方源码snapshot默认编译cgroups

需要安装kmod-tun, cgroup-tools, cgroupfs-mount, coreutils-install, bash, git-http

clash nftables规则会和fw4默认规则冲突导致lan无法连接, 需要修改规则, 由于个人仅把op作旁路网关，所以建议省事直接清空op默认fw4规则

```bash
nft delete table inet fw4
```
