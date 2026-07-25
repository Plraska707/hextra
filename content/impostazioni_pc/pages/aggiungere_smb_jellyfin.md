---
title: Aggiungere cartella SMB a Jellyfin
type: docs
weight: 8
next: /
---

1. Montare in locale la cartella SMB:

- `sudo mkdir /mnt/nas`
- `sudo apt-get install cifs-utils`
- `sudo mount -t cifs -o user=plraska //192.168.1.254/iliadbox/Video /mnt/nas`
- `sudo mount -t cifs -o user=plraska //192.168.1.254/iliadbox/Video/Film /mnt/nas/Film`
- `sudo mount -t cifs -o user=plraska //192.168.1.254/iliadbox/Video/Serie /mnt/nas/Serie`

2. Creare file .smb nella home con le credenziali di accesso:

- username = `plraska`
- password = `Cuor_di_mele`

3. Aggiungere queste righe al file /etc/fstab
`//192.168.1.254/iliadbox/Video     /mnt/nas        cifs    uid=0,credentials=/home/plraska/.smb,iocharset=utf8,vers=3.0,noperm 0 0`
`//192.168.1.254/iliadbox/Video/Film /mnt/nas/Film cifs credentials=/home/plraska/.smb,iocharset=utf8,vers=3.0,uid=0,gid=0,file_mode=0644,dir_mode=0755,_netdev,noserverino 0 0`
`//192.168.1.254/iliadbox/Video/Serie /mnt/nas/Serie cifs credentials=/home/plraska/.smb,iocharset=utf8,vers=3.0,uid=0,gid=0,file_mode=0644,dir_mode=0755,_netdev,noserverino 0 0`


4. Riferimenti:  
[Chris Tech Blog](https://chrisatech.wordpress.com/2022/06/20/jellyfin-installation-and-adding-an-smb-server-to-the-library/)