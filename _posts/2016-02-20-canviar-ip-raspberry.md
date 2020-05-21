---
layout: post
title:  "Canviar la IP de la Raspberry"
date:   2016-02-20 7:00:00
categories: raspberry
tags: ip configuració
---

![Raspberry](https://raw.githubusercontent.com/croniqueslinux/croniqueslinux.github.io/master/images/raspberrypi.gif  "Raspberry")

Tinc una [Raspberry](https://www.raspberrypi.org) Pi2 amb una ip dinàmica. Ara vull una fixa per poder gestionar-la per `ssh`. Explico els passos que he seguit.

Per posar una ip fixa per cable a una Raspberry Pi2 primer cal fer una còpia de l'antic, ens servirà si volem tornar a deixar-ho com ho tinc ara.

    sudo cp /etc/network/interfaces interfaces.old

Després anem editar el fitxer on es desa la configuració de xarxa:

    sudo nano -w /etc/network/interfaces

Dins de l'arxiu cal editar-ho:

	 # auto lo # ho comento i deixo l'antic per si ho vull desfer fàcilment. I canvio lo --> eth0
      auto eth0
      iface lo inet loopback
    
    # iface eth0 inet manual ## canvio manual --> static

      iface eth0 inet static
      address 192.168.1.XX 
      netmask 255.255.255.0
      gateway 192.168.1.1
  
Un cop desat reiniciem la **Raspberry** i comprovem que ha canviat la ip, amb la comanda `ipconfig` podem saber quina ip tenim ara.

:star:
