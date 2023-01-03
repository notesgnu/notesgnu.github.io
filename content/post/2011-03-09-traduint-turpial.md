---
title: "Traduint Turpial"
date: "2011-03-09"
categories: 
  - "eines"
  - "org2blog"
---

Avui, després de temps usant el programa [Pino](http://pino-app.appspot.com/) com a client de twitter i d'identi.ca, i cansat d'usar eines API per gestionar el twitter. Al final he decidit cercar-ne un altre. Per una banda, ja tenia el [Gwibber](http://gwibber.com/) però mai m'ha agradat, i sempre m'he liat una mica. Així que m'he decidit per [Turpial](http://turpial.org.ve/). ![](images/turpial_logo.png) El problema és que em surt en anglès, així que explico com instal·lar-ho i deixar-ho en català:

### per instal·lar:

Cal seguir les [instruccions](http://turpial.org.ve/downloads/) de la pàgina oficial.

Per exemple, per `ubuntu`:

sudo add-apt-repository ppa:effie-jayx/turpial
sudo apt-get update
sudo apt-get install turpial

O per `Fedora`:

wget http://turpial.org.ve/files/fedora/stable/turpial-1.3.4-1.fc14.noarch.rpm

i instal·lem turpial-1.3.4-1.fc14.noarch.rpm

### per traduir:

Ja fa temps que sóc usuari de [transifex](http://www.transifex.net) i allí està la [pàgina](http://www.transifex.net/projects/p/turpial/resource/i18n-Turpial/) de traducció de Turpial a altres llengües. He triat l'opció en català, i m'he baixat l'arxiu (que acaba en \*.po)

Que es pot baixar des d'aquí: [http://www.transifex.net/projects/p/turpial/resource/i18n-Turpial/l/ca/download/](http://www.transifex.net/projects/p/turpial/resource/i18n-Turpial/l/ca/download/)

Amb el programa [Poedit](http://www.poedit.net/) es pot modificar, millorar, acabar de traduir, i un cop acabat ho podem tornar a compartir a la pàgina de [transifex](http://www.transifex.net).

Quan es desa, ens genera dos arxius, un acaba en \*.po que podem seguir modificant; i un segon arxiu \*.mo que és el que usem per tenir-ho traduit quan l'executem.

Ara per tenir-lo traduit a l'ordinador, només cal copiar-lo a la carpeta on es desen els arxius de llengua:

sudo cp turpial.mo /usr/share/locale/ca/LC\_MESSAGES/

Això és aplicable a dáltres programes que volguem tenir traduits.

També encoratjo a que ajudeu a fer traduccions…

;)
