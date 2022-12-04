---
layout: post
title: "Escrivint al WordPress des de l’EMACS"
date: 2021-05-29
categories: ["emacs"]
tags: ["org2blog", "emacs"]
---

Per poder publicar des d’`Emacs` a un blog hi ha diverses maneres. Tot i això, en el meu cas, ja fa temps que uso [org2blog](https://github.com/org2blog/org2blog). Des dels primers inicis a ara, ha tingut diversos canvis, i la veritat és que em funciona molt bé.

Passo a compartir com ho faig.

## instal·lació

Primer que res, cal quenir-ho instal·lat. Per fer-ho, només cal seguir les instruccions de la seva pàgina.

Dins del nostre .emacs afegim:

(add-to-list 'package-archives
	     '("melpa-stable" . "https://stable.melpa.org/packages/") t)

i també

(require 'org2blog)
(require 'org2blog-autoloads)

I fem un `M-x package-install` i posem `org2blog`

finalment, si volem tenir la llista de blogs al nostre .emacs, el model a seguir és aquest:

(setq org2blog/wp-blog-alist
      '(("myblog"
	 :url "https://myblog.com/xmlrpc.php"
	 :username "username")))

En un principi, ja ho tenim tot preparat!

## Escrivim

Per fer aparèixer el menú, podem cridar-ho amb:

M-x org2blog-user-interface

Tot i això, prefereixo crear una combinació de tecles, jo he triat `'C-c o'` i ho he posat a la meva .emacs:

(global-set-key "\C-co" 'org2blog-user-interface)

Ara triem **[e]**, nou búfer. Ens demanarà el blog on volem escriure i la seva contrassenya. I un cop ja contacta amb el nostre blog, ens crea una plantilla amb les dades bàsiques per començar:

#+ORG2BLOG:
#+DATE: [2021-05-29 ds. 19:06]
#+OPTIONS: toc:nil num:nil todo:nil pri:nil tags:nil ^:nil
#+CATEGORY: org2blog
#+TAGS: Emacs, Lisp
#+DESCRIPTION:
#+TITLE: títol

Ara escrivim a dins i modifiquem les dades que calguin. I un cop ho tinguem, podem desar-ho per més endavant, o ho podem publicar!

## Publiquem

Res més fàcil que escriure

org2blog/wp-post-buffer

o fer `'C-c o'` i a continuació **[l]**.

Però per anar, encara més ràpid, tinc afegit al meu .emacs:

(global-set-key [f11] 'org2blog-buffer-post-publish)

i amb **[F11]** ja ho publica!

## Conclusió

Amb aquestes petites idees i tot el potencial de `ORGMODE` ja tenim una gran eina per publicar al nostre WordPress.

Un cop publicat el document tindrà assignat `#+POSTID: NUM`, aquest número farà que cada vegada que el tronem a obrir i a modificar, al publicar de nou, ens modifica l’article del blog i no en crea cap de nou.

Salut!

![😉](https://s0.wp.com/wp-content/mu-plugins/wpcom-smileys/twemoji/2/svg/1f609.svg)

[font org2blog](https://github.com/org2blog/org2blog)

[Publicat a Wordpress](https://croniqueslinux.wordpress.com/2021/05/29/escrivint-al-wordpress-des-de-lemacs/)
