---
title: "ERC: Client de Xat de l'Emacs"
date: "2011-04-19"
categories: 
  - "emacs"
  - "org2blog"
---

![http://croniqueslinux.files.wordpress.com/2011/04/wpid-xaterc.png](images/wpid-xaterc.png)

ERC és un mode de l'emacs usat com a client d'IRC completo para Emacs. El seu nom ja ho diu: **E** macs internet **R** elay **C** hat

Per iniciar la sessió, només cal engegar l'emacs i fer _M-x erc_

Llavors s'inicia un minibuffer i ens pregunta el nick, contrasenya, canal IRC… Com a curiositat, tenim que en comptes de entrar a ERC fem _M-x irc_ ens entrarà directament a la xarxa IRC irc.freenode.net amb el compte predifinit que tenim a la sesió de la màquina. Hi ha diferents canals com ara #emacs,#gnu-es, #debian, #mediawiki, etc que podem triar fent:

/join #emacs

### Ordres per usar ERC

Hi ha moltes ordres, poso només algunes…

| ordre | explicació |
| --- | --- |
| /join #canal | entra al canal #canal |
| /msg <nickname> <message> | un missatge privat <message> a <nickname> |
| /help <keyword> | Ajuda de l'ordre <keyword> |
| /part <#channel> | surt del canal #canal |
| /who <#canal> | mostra els usuaris del #canal |
| /quit \[reason\] | surt de l'IRC amb missatge de comiat |
| /time | ens indica el temps que portem al canal |

### Més informació:

[Usando ERC (Emacs internet Relay Chat) en Emacs para IRC](http://www.blackhats.es/wordpress/?p=45) [ERC : Cliente de IRC para GNU Emacs](http://ovruni.wordpress.com/2011/03/30/erc-cliente-de-irc-para-gnu-emacs/) [http://www.javiervalcarce.eu/wiki/Emacs#ERC](http://www.javiervalcarce.eu/wiki/Emacs#ERC) [http://www.emacswiki.org/emacs/ERC](http://www.emacswiki.org/emacs/ERC)

### Manual

1. HTML (single file): [http://www.mwolson.org/static/doc/erc.html](http://www.mwolson.org/static/doc/erc.html)
2. HTML (multiple files): [http://www.mwolson.org/static/doc/erc/](http://www.mwolson.org/static/doc/erc/)
3. Info: [http://www.mwolson.org/static/doc/erc.info](http://www.mwolson.org/static/doc/erc.info)
4. PDF: [http://www.mwolson.org/static/doc/erc.pdf](http://www.mwolson.org/static/doc/erc.pdf)
