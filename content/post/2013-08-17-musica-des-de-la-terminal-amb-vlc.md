---
title: "Música des de la Terminal amb VLC"
date: "2013-08-17"
categories: 
  - "terminal"
---

Sovint uso programes per escoltar música des de programes visuals, són bonics, estètics, senzills de controlar, a un clic de ratolí. Però moltes vegades tinc la sensació que només vull escoltar música, sense fer cap cosa més enllà que el fet d'acompanyar la feina que faig. Així que trobo l'opció d'escoltrar la música des de la terminal, alliberem ús de **RAM** i que ens centrem realment en la feina que estem fent. Si tenim instal·lat el programa **VLC**, ja podem fer-ho. Res més senzill que a la terminal escriure:

vlc -I ncurses audio.ogg

o directament:

nvlc audio.ogg

Si premem "h" ens donarà l'ajuda:  
  
h,H Mostra / Amaga quadre d'ajuda  
i Mostra / Amaga caixa d'informació  
m Mostra / Amaga quadre de metadades  
L Mostra / Amaga quadre de missatges  
P Mostra / Amaga quadre de llista de reproducció  
B Mostra / Amaga navegador de fitxers  
x Mostra / Amaga quadre d'objectes  
S Mostra / Amaga quadre d'estadístiques  
Esc Tanca Afegeix/Cerca entrada  
Ctrl-l Actualitza la pantalla  

a Puja el volum  
z Baixa el volum  
q Sortir del programa  
<espai> Pausa / Reprodueix  
n, p Element de la llista de reproducció anterior/següent  
<Intro> Afegeix el fitxer seleccionat a la llista de reproducció  
e Expulsa (si és aturat)  
<espai> Afegeix el directori seleccionat a la llista de reproducció  
. Mostra/Amaga els fitxers ocults  
D Elimina de la llista de reproducció  
Fletxa dreta/esquerra Avança i retocedeix l'audio  
r Activa/Desactiva reproducció a l'atzar  
l Activa/Desactiva bucle a la Llista de reproducció  
R Activa/Desactiva Repeteix tema  
o Ordena llista de reproducció per títol  
O Inverteix l'ordre de llista de reproducció per títol  
g Vés fins a l'ítem que s'està reproduint ara  
/ Cerca un ítem  
  
De forma gràfica em consum més de 40mb la reproducció de la cançó, en canvi des de terminal, fent la mateixa feina, no arriba als 14mb! No és massa, però per a què consumir més ram de la necessària? A més a més, i l'executem des d'una eina com **byobu**, com jo faig, pots tancar la terminal i segueix funcionant! Pots anar a la terminal i tornar a executar **byobu** i podem tornar a fer canvis, com aturar, iniciar, pausar, etc…
