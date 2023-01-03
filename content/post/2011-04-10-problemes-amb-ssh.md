---
title: "Problemes amb ssh"
date: "2011-04-10"
categories: 
  - "org2blog"
  - "ssh"
  - "terminal"
  - "xarxa"
---

Algunes vegades m'he trobat amb aquest problema, i avui he decidit veure com ho soluciono. M'agrada treballar amb ssh, tot i que ja havia tingut algun [problema](http://croniqueslinux.wordpress.com/2010/11/14/warning-remote-host-identification-has-changed/), avui m'he trobat de nou amb el problema següent:

port 22: Connection timed out 

i amb

port 22: Connection refused

Això m'ha passat perquè a l'ordinador que vull accedir té bloquejat el port 22. Certament, usant el programa **nmap** m'he trobat amb la següent resposta:

nmap -PN 192.168.x.x

i respon:

22/tcp closed ssh

La solució passa per obrir el port a l'ordinador. Des de la terminal:

/etc/init.d/ssh start  --> debian
/etc/init.d/sshd start  --> opensuse

Ara quan faig:

nmap -PN 192.168.x.x

i respon:

22/tcp open  ssh

Ja puc connectar-me via SSH ;)

En opensuse, es pot fer amb el yast: yast->sistema->serveis (nivells d'execusió), habilitar el servei "sshd"

Hi ha una [pàgina vella](http://tuxpepino.wordpress.com/2007/05/11/ssh-el-dios-de-la-administracion-remota/) però amb informació ben explicada.
