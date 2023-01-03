---
title: "Turpial a l'Unity i en català"
date: "2011-05-15"
categories: 
  - "emacs"
  - "org2blog"
  - "turpial"
---

![](images/turpial_icon.png "turpial")

Ja fa un temps que vaig escriure sobre [Turpial](http://turpial.org.ve/), i de [com traduïr-lo](http://croniqueslinux.wordpress.com/2011/03/09/traduint-turpial/). Per tenir la versió ja traduïda des dels repositoris a l'Ubuntu, només cal afegir el ppa

sudo add-apt-repository ppa:effie-jayx/turpial-devel

un cop afegit el repositori de desenvolupament, només cal instal·lar-lo

sudo apt-get update
sudo apt-get install turpial

això ens instal·larà la versió 1.5rc1 i ja està en català.

La segona qüestió a resoldre és que aparegui a la barra superior de l'Unity. Per fer això he seguit les indicacions de [effiejayx’s blog](http://effiejayx.wordpress.com/2011/05/06/icono-de-turpial-en-bandeja-de-sistema-en-unity-ubuntu-11-04/). Així que anem per feina, ara a la terminal escrivim:

gsettings get com.canonical.Unity.Panel systray-whitelist

i ens retorna el que té predeterminat a la barra… `['JavaEmbeddedFrame', 'Mumble', 'Wine', 'Skype', 'hp-systray', 'scp-dbus-service']`

Jo no uso ni wine ni Skype, així que els esborro, si cal els podeu deixar… Per afegir el Turpial només cal modificar la barra escrivint a la terminal:

gsettings set com.canonical.Unity.Panel systray-whitelist "\['JavaEmbeddedFrame', 'Mumble', **'turpial'**, 'scp-dbus-service'\]"

En la pàgina [omgubuntu.co.uk](http://www.omgubuntu.co.uk/2011/03/how-to-hide-or-show-app-tray-applets-in-ubuntu-11-04/) ens ensenya altres opcions ;)
