---
title: "Promblemes amb ffmpeg: libxvidcore.so.4"
date: "2011-01-15"
categories: 
  - "fedora"
  - "terminal"
---

### Porto uns dies amb problemes en treballar amb ffmpeg

### ![](images/ffmpeg.jpg "ff")

### Exactament, Fedora14 em diu:

**$ ffmpeg: error while loading shared libraries: libxvidcore.so.4: cannot enable executable stack as shared object requires: Permission denied**

### La solució:

**$ su**
**$ contrasenya**

**$ execstack -c /usr/lib/libxvidcore.so.4
;)**
