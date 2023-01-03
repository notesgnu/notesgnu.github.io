---
title: "Accents amb un teclat americà"
date: "2012-12-25"
categories: 
  - "catala"
  - "lubuntu"
  - "lxde"
---

![file://http://croniqueslinux.files.wordpress.com/2012/12/wpid-teclat.jpg](images/wpid-teclat.jpg)  
Ja fa uns anys que vaig anar de viatge a la Xina i em vaig comprar un EeePC 1000HE, del que estic molt content. Hi vaig instal·lar Ubuntu (gnome), i en la configuració del teclat vaig triar la "tecla **compose**", és a dir, em permetia usar una de les tecles com a comodí per accentuar. Amb el temps m'he passat a **Lubuntu** en el notebook, en especial per optimitzar recursos de la màquina, i prioritzar les eines per sobre de l'aspecte.

El canvi va anar molt bé, tot i que el teclat està en format USA, i en l'escriptori **LXDE** no havia trobat la manera de gestionar la tecla compose!

Aquests dies de festa, m'ha permés trobar la solució… configurar l'_autostart_ de **LXDE**.

Així, res més senzill que editar el fitxer de configuració:

sudo emacs /etc/xdg/lxsession/Lubuntu/autostart

En aquest cas he optat per la tecla "menu" com a tecla comodí per fer el compose, així, a dins cal afegir:

@setxkbmap -option "compose:menu"

Ara cada vegada que la mantinc premuda la tecla "menu"i tot seguit ' + a em dóna á.

si volem usar una altra tecla, només cal canviar l'opció per la tecla que volem!  
`compose:ralt`  
`compose:lwin`  
`compose:rwin`  
`compose:menu`  
`compose:rctrl`  
`compose:caps`  

;-)

[font de la imatge](http://farm1.staticflickr.com/32/92385549_3465edc5c1_q.jpg)
