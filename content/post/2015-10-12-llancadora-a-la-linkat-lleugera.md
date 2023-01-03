---
title: "Llançadora a la Linkat lleugera"
date: "2015-10-12"
categories: 
  - "linkat"
  - "lubuntu"
---

Ja fa temps que uso Lubuntu com a distribució per defecte. Ara que ha sortit la nova [Linkat Lleugera](http://linkat.xtec.cat/portal_linkat/wikilinkat/index.php/Linkat_lleugera), he migrat de la meva Lubuntu a una Linkat. A més a més, a la meva aula hi ha quatre ordinadors de sobretaula que ara també van amb la nova Linkat lleugera! ![Logo-linkat-lleugera.png](images/Logo-linkat-lleugera.png)

Ha estat **la solució que feia temps que esperava**. Per desgràcia a les escoles no sempre tenim la última tecnologia, i aquest mes de setembre quan vaig començar el curs, tenia a la nova aula quatre ordinadors amb Windows XP. Així que sense pensar-m'ho dos cops, vaig migrar a la Linkat! De cop i volta han reviscolat!!! Van molt més ràpid, fluïds i amb tot el que necessito.

Una cosa que m'he trobat és que no tenia la llançadora a la carpeta Treball. Així, que he decidit escriure de com l'he afegit a l'escriptori.

Anem a l'escriptori i creem un fitxer amb el nom que volem i _.desktop_, per exemple: **_treball.desktop_** Amb un editor, jo uso emacs, a dins escrivim:

\[Desktop Entry\]
Version=1.0
Name=Treball
Exec=pcmanfm "smb://192.168.0.240/treball"
Terminal=false
Type=Application
Icon=preferences-system-network

si volem entrar per ssh en comptes de samba, tan senzill com canviar-ho per:

Exec=pcmanfm "sftp://192.168.0.240/treball"

Ara desem i ja podem anar a l'escriptori i usar l'enllaç. Si volem, podem fer botó dret del ratolí a sobre i en el menú podem editar-lo.

[![Selecció_001](https://croniqueslinux.files.wordpress.com/2015/10/seleccic3b3_001.png?w=300)](https://croniqueslinux.files.wordpress.com/2015/10/seleccic3b3_001.png)

I finalment ja tenim a l'escriptori l'enllaç a les carpetes compartides. Aquest sistema serveix per fer enllaços directes a altres programes.

;-)
