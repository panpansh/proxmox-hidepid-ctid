# proxmox-hidepid-ctid

/etc/pve/lxc/{ctid}
```bash
lxc.autodev: 1

lxc.mount.auto: 
lxc.mount.auto: sys:mixed cgroup:mixed
lxc.mount.entry: proc proc proc rw,remount,nodev,nosuid,noexec,relatime,hidepid=2 0 0
lxc.mount.entry: proc/sys proc/sys proc ro,bind,relative 0 0
lxc.mount.entry: proc/sys/net proc/sys/net proc rw,bind,relative 0 0
lxc.mount.entry: proc/sysrq-trigger proc/sysrq-trigger proc ro,bind,relative 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/cpuinfo proc/cpuinfo none bind,optional 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/diskstats proc/diskstats none bind,optional 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/meminfo proc/meminfo none bind,optional 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/stat proc/stat none bind,optional 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/swaps proc/swaps none bind,optional 0 0
lxc.mount.entry: /var/lib/lxcfs/proc/uptime proc/uptime none bind,optional 0 0

lxc.mount.entry: /dev/null var/jail/dev/null none bind,ro 0 0
lxc.mount.entry: /dev/random var/jail/dev/random none bind,ro 0 0
lxc.mount.entry: /dev/urandom var/jail/dev/urandom none bind,ro 0 0
lxc.mount.entry: /dev/console var/jail/dev/console none bind,ro 0 0
lxc.mount.entry: /dev/tty var/jail/dev/tty none bind,ro 0 0
```
