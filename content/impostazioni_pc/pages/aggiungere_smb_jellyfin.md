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

2. Creare file .smb nella home con le credenziali di accesso:

- username = `plraska`
- password = `Cuor_di_mele`

3. Aggiungere queste righe al file /etc/fstab
`//192.168.1.254/iliadbox/Video     /mnt/nas        cifs    uid=0,credentials=/home/plraska/.smb,iocharset=utf8,vers=3.0,noperm 0 0`

4. Riferimenti:  
[Chris Tech Blog](https://chrisatech.wordpress.com/2022/06/20/jellyfin-installation-and-adding-an-smb-server-to-the-library/)