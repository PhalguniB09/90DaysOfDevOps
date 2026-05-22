# Linux Troubleshooting Runbook

# Target service: SSH
# Environment basics
- uname -a: display information about the Linux system/kernel
- cat /etc/os-release: displays detailed information about the Linux distribution (OS)

# Filesystem sanity
- mkdir /runbook-demo: created a runbook-demo folder
- cp /etc/hosts /runbook-demo/hosts-copy && ls -l /runbook-demo: copied the /etc/hosts file to this location w/runbook-demo/hosts-copy & listed the directory

# CPU / Memory
- htop: live interactive process viewer along with CPU, Memory, PID & other details. Using this, identified the process (k3s server) consuming the max CPU [10%] & Memory [19.1%].
- ps aux | grep -i "server": Using this command, validated the process (k3s server) consuming the max CPU & Memory on our Linux system.
- free -h: helped me to identify how much memory (RAM) is used & is left on system.

# Disk / IO
- df -h: diplay the size of my current disk, current consumption & storage left
- du -sh: display size of the current directory in a human-readable format

# Network 
- ss -tun: display the established connections. Here, t means TCP, u means UDP and n represents numeric addresses/ports
- ss -tuln: show ports/services currently listening for network connections on your Linux system.
- curl https://example.com: to check whether an application is running correctly
- wget https://example.com: download content/files from a URL

# Logs
- journalctl -u ssh: to get the logs of ssh service from the systemd journal in a pager format

