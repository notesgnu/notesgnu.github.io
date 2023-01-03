---
title: "instal·lar un paquet experimental a Debian"
date: "2012-10-16"
categories: 
  - "emacs"
  - "org2blog"
---

Avui per un problema amb el network-manager he decidit instal·lar un paquet des del repositori **experimental** al portàtil on tinc instal·lat Debian (Testing). El primer que he vist és que hi havia la nova versió del **network-manager** 9.6 i amb alguns problemes corregits. Sempre quan instal·lem un paquet des del repositori experimental cal tenir present que no són segurs del tot, ja que des de Debian no n'asseguren el correcte funcionament.

El primer que farem és afegir el repositori a: **/etc/apt/sources.list**

deb http://ftp.de.debian.org/debian experimental main 

Si voleu un repositori més a prop podeu canviar el codi del país …ftp.de.debian… > …ftp.es.debian… :-P Un cop afegit cal actualitzar.

apt-get update

I finalment cal instal·lar-ho des del repositori que volem amb la comanda:

apt-get install -t experimental network-manager

Finalment si voleu deshabilitar l'experimental, només caldria tornar a editar de nou **/etc/apt/sources.list** i comentar-ho:

#deb http://ftp.de.debian.org/debian experimental main 

:-)
