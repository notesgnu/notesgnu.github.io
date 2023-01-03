---
title: "Com fer un blog amb Hugo"
date: "2020-06-01"
tags: 
  - "blog"
  - "hugo"
  - "jekyll"
  - "org"
  - "terminal"
---

Porto dies remenant i pensant opcions per deixar **Jekyll**. Estic content amb el rendiment que he tingut fins ara, però m’ah començat a donar problemes. Moltes errors amb les _gemes_ i no es veu igual en local com a la xarxa.

Una de les opcions que he trobat és **Hugo**. Al principi una mica diferent a **Jekyll**.

He trobat que és molt ràpid i dona menys problemes. Això sí, no he acabat de trobar el _tema_ que s’ajusti als meus gustos. També he vist que la capçalera i la configuració són una mica diferents.

A continuació explico com he fet les proves.

# Instaŀlar Hugo

El primer que faig és instal·lar **Hugo**:

sudo apt install hugo

**NOTA**: en Ubuntu s’instaŀla una versió antiga que dona problemes amb temes més moderns. Així que he instaŀlat la [versió actual des de la pàgina](https://github.com/gohugoio/hugo/releases) i l’he instaŀlat:

sudo apt install ./hugo\_0.72.0\_Linux-64bit.deb

Després ja podem crear el primer lloc amb:

hugo new site nombre\_del\_lloc

ara ja ens avisa que tenim la carpeta preparada amb el missatge:

Congratulations! Your new Hugo site is created in /xx/xx/xx/nombre\_del\_lloc
Just a few more steps and you're ready to go:
1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
  create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

entrem dins i iniciem el git:

cd nom\_del\_lloc
git init

Ara ja tenim el lloc preparat.

# Més informació

Només ens cal cercar un tema que ens agradadi a: [https://themes.gohugo.io/](https://themes.gohugo.io/)

Per escriure els articles amb **emacs** hi ha l’opció de fer-ho amb org-mode segons s’explica a:

- [https://ox-hugo.scripter.co/](https://ox-hugo.scripter.co/)

amb alguns exemples usant ox-hugo + Hugo:

- [https://ox-hugo.scripter.co/doc/examples/](https://ox-hugo.scripter.co/doc/examples/)
