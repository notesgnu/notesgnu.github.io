---
layout: post
title:  "GIT dóna Error en user.mail"
date:   2016-04-26 7:00:00
categories: git
tags: git comandes
---

![Git](https://git-scm.com/images/logo@2x.png  "GIT")

Avui m'he trobat que quan he intentat fer un

    git commit -m "nou article"

M'ha donat el següent error:

> git: fatal unable to auto-detect email address (got "some wrong email")

Em demana que configuri:

> git config -\-global user.mail "you@example.com"
 
Estic usant la **Linkat** lleugera (lUbuntu 14.04) i sembla que és un error en configurar
~~user.mail~~ que li falta una **e**. Si no vull que canviï tota la configuració del **git** no cal posar *-\-global*.

Per solucionar-ho només cal fer la comanda:

    git config --global user.email "you@example.com"
    
     
Finalment podem veure com ha quedat amb la comanda:

    $ git config --local -l


:star:
