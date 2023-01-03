---
title: "Conèixer informació del sistema"
date: "2011-07-07"
categories: 
  - "terminal"
---

Avui em calia saber el model del cpu de l'ordinador, per això he usat a la terminal la següent comada:

$ cat /proc/cpuinfo | grep "model name"

Si volem tota la informació podem:

$ cat /proc/cpuinfo 

Si volem saber una en concret, només cap modificar el grep amb la dada que volem:

$ cat /proc/cpuinfo | grep "flags"

Com a nota interessant tenim que Si al resultat surt lm, llavors 64 bit, i si surt Protected Mode, és de 32 bits.

Hi ha la comanda **uname** que ens mostra informació de la nostra distro instal·lada, fins i tot per saber si el kernel és de 32 o 64 bits.

$ uname -m

Si la resposta és x86\_64, llavors és 64 bits. Si ens indica i386, i486, i586 o i686, llavors és de 32 bits. Si volem saber totes les dades del sistema operatiu:

$ uname -a

Si volem saber l'ús de la memòria actual, només cal escriure:

$ free -m

També tenim la comanda **lshw** que ens llista tota la informació del maquinari.

$ lshw

si volem tenir-ho tot en un document .txt només cal afegir.

$ lshw > info.txt

Si mirem l'apartat _\*-cpu_ podrem llegir les dades del cpu, i allí podem saber si la cpu suporta 64 bits si diu: \[width: 64 bits\]

Hi ha una altra comada **dmidecode** que ens dóna un bon munt d'informació del sistema, la bios, etc…

$ sudo dmidecode

Finalment si volem saber el límit de capacitat de RAM que soporta el meu ordinador:

$ sudo dmidecode | grep Maximum

Desitjo que us siga d'ajuda! ;-)
