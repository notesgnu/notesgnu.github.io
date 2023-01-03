---
title: "Iniciar el servidor NFS"
date: "2010-04-01"
categories: 
  - "terminal"
  - "ubuntu"
  - "xarxa"
---

[![](images/gnome-terminal.png "Gnome-terminal")](http://croniqueslinux.files.wordpress.com/2010/02/gnome-terminal.png)

Per poder iniciar el servidor NFS, necessita que s'inici el **portmap**:

_**$**_ _**sudo /etc/init.d/portmap start**_

Ara només cal iniciar el servei NFS:

**_$ sudo /etc/init.d/nfs-kernel-server restart_**

Si del volem aturar:

**_**_$ sudo /etc/init.d/nfs-kernel-server stop_**_**
;)
