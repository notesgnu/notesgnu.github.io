---
layout: post
title:  "Editor uText"
date:   2016-01-23 16:13:38
categories: markdown, editor
tags: markdown
---

![utext]({{ base.url }}/images/utext.png)

És un editor senzill de [markdown](https://ca.wikipedia.org/wiki/Markdown). Aquest llenguatge el va crear John Gruber fugint del llenguatge de marques html, i facilitar l'edició amb la lectura i escriptura.

![md]({{ base.url }}/images/md.jpg)

És un editor senzill de [markdown](https://ca.wikipedia.org/wiki/Markdown). Aquest llenguatge el va crear John Gruber fugint del llenguatge de marques html, i facilitar l'edició amb la lectura i escriptura.
Podem trobar molts editors com ara ReTex, Retext, MdCharm, UberWriter, Springseed, Remarkable, CuteMarkEd, Haroopad,  i n'hi ha en línia com [StackEdit](https://stackedit.io/editor).
En el meu cas, normalment uso **Emacs** amb el [mode-markdown](http://jblevins.org/projects/markdown-mode/), però aquest cop m'he interessat per un que he trobat molt interessant, per la seva senzillesa **uText**.

Amb aquest editor [uText](https://launchpad.net/utext) podem prendre notes i usar-les en blogs, així com exportar-ho a Pdf, odt, latex, html, ...

## instal·lació
Per instal·lar aquest editor:
Terminal obert de la cursa, App Launcher, o a través de les tecles de drecera `Ctrl + Alt + T`. Quan s'obre, executar sota ordres per fer-ho des PPA del desenvolupador:

    sudo add-apt-repository ppa:atareao/utext
    sudo apt-get update
    sudo apt-get install utext

Si volem, també podem baixar-nos el **deb** directament de la pàgina [PPA](http://ppa.launchpad.net/atareao/utext/ubuntu/pool/main/u/utext/):

	 http://ppa.launchpad.net/atareao/utext/ubuntu/pool/main/u/utext/utext_0.3.9-0extras15.04.0_all.deb

Hi ha l'opció d'usar *l'apt* de l'ubuntu a partir de [la seva pàgina](https://apps.ubuntu.com/cat/applications/utext/)

## en català
Per defecte no me l'he trobat traduït al català, i mans a l'obra, n'he fet una traducció a [la secció traduccions](https://translations.launchpad.net/utext/trunk/+pots/po/ca). Seria un plaer que hi contribuïu i en feu una traducció més acurada.

Finalment he anat a la pàgina de traduccions del [launchpad](https://translations.launchpad.net/utext/trunk/+pots/po/ca/+export) i l'exportat en format `mo`.

Un cop baixat cal crear una carpeta anomenada `ca_ES`, i a dins crear una altra carpeta anomenada `LG_MESSAGES`, i a dins copiar el fitxer `*.mo` que us heu baixat. Un cop ho tingueu cal desar-ho a la carpeta:

    /opt/extras.ubuntu.com/utext/share/locale-langpack
    
Ara cada vegada que inicieu el programa, podreu veure directament en català els menús.

:+1:
