---
title: Aprire alla rete locale
type: docs
weight: 4
---

Per aprire una cartella alla condivisione su rete locale:
- aprire con sudo il file di configurazione: sudo vim /etc/samba/smb.conf
- aggiungere la cartella che si vuole condividere con questa struttura:

[sambashare]  
&nbsp;&nbsp;&nbsp;&nbsp;comment = Samba on Ubuntu  
&nbsp;&nbsp;&nbsp;&nbsp;path = /home/plraska/sambashare  
&nbsp;&nbsp;&nbsp;&nbsp;read only = no  
&nbsp;&nbsp;&nbsp;&nbsp;browsable = yes