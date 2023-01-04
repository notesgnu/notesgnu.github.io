---
title: "Eliminar Kernels vells"
date: "2010-04-19"
categories: 
  - "terminal"
  - "ubuntu"
---

Per esborrar kernells vells, que es van acumulant a l'Ubuntu i al seu grub, sempre podem fer el següent:

- saber les versions que tenim a l'ordinador amb:

```
sudo dpkg -l | grep linux-image
```

- eliminar les versions velles amb:

```
sudo apt-get remove --purge elkernelvell
```
per elimnar-ho canviem 'elkernelvell' per _linux-image-2.6.31-14-generic_

i ja ho tenim!

:star:
