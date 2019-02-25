# On the server:

	pkg_add wget
	mkdir -p /srv/nfs/root
	wget https://mirror.yandex.ru/openbsd/6.4/arm64/base64.tgz
	tar -xvzf base64.tgz -C /srv/nfs/root
	tar -xvzf /srv/nfs/root/var/sysmerge/etc.tgz -C /srv/nfs/root
	
	mkdir /srv/nfs/root/swap
	dd if=/dev/zero of=/srv/nfs/swap bs=1M count=128

# This directory:
1. Rename server_root/tftpboot/ID to your Raspberry ID
2. check EVERY file
except server_root/etc/rc.conf.local and server_root/tftpboot/*
to replace IP, MAC and hostnames to yours.

Default parameters:
Server IP: 192.168.1.179
Client IP: 192.168.1.112

3. Copy all files to server's root.

# Default credentials:
Username: root
Password: <empty>
