On the server:
1. pkg_add wget
2. mkdir -p /srv/nfs/root
3. wget https://mirror.yandex.ru/openbsd/6.4/arm64/base64.tgz
4. tar -xvzf base64.tgz -C /srv/nfs/root
5. tar -xvzf /srv/nfs/root/var/sysmerge/etc.tgz -C /

6. check EVERY file
except server_root/etc/rc.conf.local and server_root/tftpboot/*
to replace IP, MAC and hostnames to yours.
Don't forget to replace Raspberry ID on server_root/tftpboot/<ID>

Default parameters:
Server IP: 192.168.1.179
Client IP: 192.168.1.112

7. Copy all files to server's root.
