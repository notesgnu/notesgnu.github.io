---
title: "Dropbox a l'Unity"
date: "2011-05-12"
categories: 
  - "dropbox"
  - "emacs"
  - "org2blog"
---

![](images/logo.png "dropbox")

Fa temps que uso Dropbox, però amb l'actualització de l'Ubuntu del portàtil m'he trobat que no apareix la icona del Dropbox a la barra superior. Per fer això només cal fer el següent, a la terminal escrivim: $ gsettings get com.canonical.Unity.Panel systray-whitelist i ens retorna el que té predeterminat a la barra… `['JavaEmbeddedFrame', 'Mumble', 'Wine', 'Skype', 'hp-systray', 'scp-dbus-service']`

Jo no uso ni wine ni Skype, així que els esborro, si cal els podeu deixar… Per afegir dropbox, només cal modificar la barra escrivint a la terminal: $ gsettings set com.canonical.Unity.Panel systray-whitelist "\['dropbox', 'JavaEmbeddedFrame', 'Mumble', 'turpial', 'scp-dbus-service'\]"

;)
