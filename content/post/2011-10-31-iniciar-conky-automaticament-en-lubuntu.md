---
title: "Iniciar Conky automàticament en Lubuntu"
date: "2011-10-31"
categories: 
  - "conky"
  - "lubuntu"
  - "lxde"
---

Aquest cap de setmana he instal·lat a un netbook **Point Of View** (POV) la nova [Lubuntu](https://wiki.ubuntu.com/Lubuntu) 11.10 ocelot oneiric. La veritat és que consumeix menys RAM, i va bastant lleugera. Va amb l'entorn d'escriptori lleuger [LXDE](http://lxde.org/es/lxde).

Seguidament he instal·lat [conky](http://conky.sourceforge.net/) que és molt configurable i tenim molts [exemples](http://desktopspotting.com/26/best-conky-configs-for-linux-desktop/) a la xarxa per donar-li l'aspecte que més ens agradi. Si no el tenim instal·lat, només cal:

`sudo apt-get install conky-all`

L'únic problema que he tingut és que no s'inciava de forma automàtica. La solució ha estat editar /etc/xdg/lxsession/Lubuntu/autostart i afegir @conky. Jo ho he fet amb emacs:

`sudo emacs /etc/xdg/lxsession/Lubuntu/autostart`

Un cop afegit @conky i desat he reiniciat el netbook. Ja tinc funcionant conky en iniciar Lubuntu.

Com a idea general podem veure que si afegim qualsevol programa amb @ tindrem el programa executat en iniciar el sistema.

En una altra distro caldrà editar l'arxiu **autostart** que correspongui, sempre ho trobarem a /etc/xdg/lxsession/distroinstal·lada/autostart :-)

**fonts:** [Un Tux Suelto](http://www.untuxsuelto.com/2009/03/iniciar-aplicaciones-automaticamente-en.html) (parla d'iniciar programes en general a LXDE)  
[Ubuntizando el planeta](http://www.ubuntizandoelplaneta.com/2010/10/iniciar-aplicaciones-automaticamente-en.html) (Iniciar aplicaciones automáticamente en Linux Mint LXDE)
