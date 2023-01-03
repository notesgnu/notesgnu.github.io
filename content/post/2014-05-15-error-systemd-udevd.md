---
title: "Error systemd-udevd"
date: "2014-05-15"
---

Després d'actualitzar el eeepc 1000he a la nova Lubuntu 14.04 en el moment del boot ha començat a donar un munt d'errors tipus

**systemd-udevd\[xxxx\]: failed to execute '/usr/lib/udev/socket:@/org/freedesktop/hal/udev\_event' : No such file or directory**

[![IMG_20140515_133254](http://croniqueslinux.files.wordpress.com/2014/05/img_20140515_133254.jpg?w=300)](http://croniqueslinux.files.wordpress.com/2014/05/img_20140515_133254.jpg)

Buscant una mica he trobat la solució:

eliminar "hal"

així que:

**_sudo apt-get remove hal_**

 

 

i ara tot solucionat!
