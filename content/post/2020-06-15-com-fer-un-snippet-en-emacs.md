---
title: "Com fer un snippet en Emacs"
date: "2020-06-15"
tags: 
  - "emacs"
  - "org"
  - "orgmode"
  - "terminal"
---

Sovint piquem codi i volem guanyar temps usant una plantilla. Un pedaç de codi s’anomena **snippet**, i és això el que fem.

Per fer això, tenim `YASnippet`. Per instaŀlar-ho, res més fàcil:

M-x package-install yasnippet

Per actualitzar-lo sense inciar emacs, si no ho volem fer, funcionarà en inciar.

M-x yas-reload-all

Seguidament, ja podem usar-lo. Cal tenir carregat el mode.

M-x yas-minor-mode

El podem carregar sempre que vulguem o fer-ho automàticament afegint el codi al teu `.emacs`:

(require 'yasnippet)
(yas-global-mode 1)

Per crear la primera plantilla, s’ha de fer:

C-c & C-n

el contingut ha de ser:

\# name: nom que volem
# key: paraulaclau
# --
codi que volem

La part de dalt és la capçalera que defineix l’snippet, i amb la clau (key) el nom per cridar-lo.

Per inserir el que volem:

C-c & C-s

També ho podem fer encara més senzill, si recordem la paraula clau, podeu escriure-la i inmeditament `TAB` i ens sortirà el codi directament. Per això és molt important usar paraules claus que no ens porti a equivocar-nos.

fonts:

- [https://github.com/joaotavora/yasnippet](https://github.com/joaotavora/yasnippet)
- [https://www.blackhats.es/wordpress/?p=66](https://www.blackhats.es/wordpress/?p=66)
- [https://bengalaa.wordpress.com/2014/12/13/haciendo-snippets-con-yasnippet/](https://bengalaa.wordpress.com/2014/12/13/haciendo-snippets-con-yasnippet/)
