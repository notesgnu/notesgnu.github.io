---
title: "Donar permisos a un directori en Terminal"
date: "2010-01-07"
categories: 
  - "terminal"
---

![](images/terminal.png)

A mesura que avancem en el món Gnu/Linux ens anem endinsant en l'ús de la Terminal...

Per donar permisos nomes cal entrar a la terminal i escriure com a root:
```
sudo chmod 777 /lloc/on/és/la\_carpeta o arxiu
```
ex:

```
sudo chmod 777 /home/linux/imatges
```
així es donarà tots els permisos a la carpeta imatges de l'usuari 'linux'.

també podem fer-ho amb:

```
sudo chmod **-Rf** 777 /home/linux/imatges
```

on `-R` mana que ho faci recursivament a tot el que hi conté i `f` fa que no es visualitzen els possibles errors.

per saber-ne més del **chmod** → [Viquipèdia](http://ca.wikipedia.org/wiki/Chmod)

:+1:
