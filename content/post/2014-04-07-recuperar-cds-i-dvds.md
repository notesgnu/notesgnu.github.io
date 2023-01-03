---
title: "Recuperar CDs i DVDs"
date: "2014-04-07"
categories: 
  - "reparar"
  - "terminal"
---

Amb el temps m'he trobat que molts CDs que he gravat, deixen de funcionar, i sovint sembla que les dades i música desada ja no es pot recuperar.

Hi ha moltes eines pensades per fer-ho, tan GUI com CLI, fins i tot tenim distribucions fetes especialment per tasques d'aquest tipus.

En aquest cas usaré **GNU ddrescue** una comanda que permet recuperar dades. Així podem crear imatges de cds, dvds, usbs i discos durs des d'on recuperar-ne. Si no el tenim instal·lat, res més senzill (en la linkat 12.04 o en Ubuntu i derivades):

sudo apt-get install ddrescue

La comanda és:

ddrescue \[options\] infile outfile \[logfile\]

En un cas pràctic, vull reparar un CD, així que ara només ens cal iniciar la comanda:

ddrescue –n –b 2048 /dev/cdrom nomimatge.iso fitxerlog.txt

- La **\-b** diu la mida dels blocs que té els CDs, és a dir 2048 bytes.
- La **\-n** és per fer que duri menys temps, intentarà recuperar les parts llegibles.
- Si veiem que tenim molts errors, llavors substituim la **\-n** per **\-d** que és un mode directe per llegir tantes dades com sigui possible.

Mentre no canviem el log ni la ISO, podem seguir treballant sobre la mateixa imatge, és a dir, que després d'una passada, podem fer-ne tantes com vulguem i anirá afegint dades sobre la ISO creada. Cal tenir en compte que si tenim que recuperar un disc dur o un usb, llavors aconsello fer prèviament una còpia amb **dd**. Així evitem modificar res sobre el disc malmés i treballarem directament sobre la imatge. Així podríem començar a treballar sobre una partició:

dd-rescue /dev/hda1 hda1.img

Aquesta imatge és una còpia bit a bit exacta. Si volem provar de reparar-la, podem pasar **fsck**

sudo fsck -y ~/hda1.img

Ara, podem crear una carpeta on muntar la imatge _hda1.img_.

mkdir -p /lloc/on/volem/muntar/recuperar

i ara muntem la imatge:

mount -o loop,ro -t filesystemtype hda1.img /lloc/on/volem/muntar/recuperar

En qualsevol moment podem aturar el procés amb CRTL+c i després, podem reiniciar i seguirà on ho hem deixat. Si volem més informació:

ddrescue -help

Espero que sigui d'utilitat ;-)
