---
title:  "Linkatitzar Lubuntu 18.04"
date:   2020-05-24 
categories: ["linkat"]
tags: ["lubuntu", "linkat"]
---

![de Lubuntu a Linkat](images/lubuntulinkat.png)

Avui he agafat el meu vell Eeepc que vaig comprar en un viatge a Xina, i he volgut passar-lo a Linkat. He aprofitat que ja tenia una Lubuntu funcional, així que seguint les indicacions de la pàpigna, m'he trobat amb un problema.

## el problema
Quan he intentat instal.lar el paquet **linkat-repos_18.04-5_all.deb**

m'ha donat el següent error:

```
El paquet gksu no està instal·lat.

```
i si vull instal.lar-lo, em diu:

```
El paquet gksu no té versió disponible, però un altre paquet
en fa referència. Això normalment vol dir que el paquet falta,
s'ha tornat obsolet o només és disponible des d'una altra font.
E: El paquet «gksu» no té candidat d'instal·lació

```

## la solució
Bé, ara anem a buscar la solució...

Anem als repositoris de Ubuntu 17.10 i ens baixem el paquet:

```
wget http://mirrors.edge.kernel.org/ubuntu/pool/universe/libg/libgksu/libgksu2-0_2.0.13~pre1-6ubuntu8_i386.deb
sudo apt install ./libgksu2-0_2.0.13~pre1-6ubuntu8_i386.deb

wget http://mirrors.kernel.org/ubuntu/pool/universe/g/gksu/gksu_2.0.2-9ubuntu1_i386.deb
sudo apt install ./gksu_2.0.2-9ubuntu1_i386.deb

```

En un principi ja ho tenim! ara ja podem instalar el paquet per linkatitzar!

-------------------------------------------------------------------------------

Nota: m'he trobat que no em deixa, perquè em demana el paquet **libgtop-2.0-10**
així que he fet el mateix procès:

```
wget http://es.archive.ubuntu.com/ubuntu/pool/main/libg/libgtop2/libgtop-2.0-10_2.32.0-1_i386.deb
sudo apt install ./libgtop-2.0-10_2.32.0-1_i386.deb

```


fonts: 
- [Transformació a la Linkat Lleugera](http://linkat.xtec.cat/portal_linkat/wikilinkat/index.php/Lubuntu#Transformaci.C3.B3_a_la_Linkat_Lleugera "Transformació a la Linkat Lleugera")
- [Instalar Gksu en Ubuntu 18.04 y derivados](https://www.sololinux.es/instalar-gksu-en-ubuntu-18-04-y-derivados/ "Instalar Gksu en Ubuntu 18.04 y derivados") 
