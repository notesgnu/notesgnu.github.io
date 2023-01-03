---
title: "Fer una entrada al wordpress amb Emacs"
date: "2011-01-26"
categories: 
  - "emacs"
  - "org2blog"
---

Després de provar-ho uns dies, i d'insistir-hi, al final me n'he sortit! Es poden publicar els blocs amb l'emacs, per poder-ho fer he triat: emacs, wordpress i el mode de l'emacs conegut com org2blog!

Primer quue res, cal tenir instal·lat l'emacs. Per instal·lar l'org2blog ho podem fer seguint els passos de la pàgina

[https://github.com/punchagan/org2blog](https://github.com/punchagan/org2blog)

Si volem baixar el paquet directament del git, podem fer-ho instal·lant-lo. Per exemple, si tenim una distro basada en paquest deb:

$ sudo apt-get install git

o per exemple en fedora:

$ sudo yum install git

o amb opensuse o derivats:

$ su

$ zypper in git

un cop fet això, ara baixem el git: $ git clone [http://github.com/punchagan/org2blog.git](http://github.com/punchagan/org2blog.git)

ara copiem la carpeta creada amb el git, que s'anomena 'org2blog' a dins de la carpeta de l'emacs ~/.emacs.d/

Org2blog necessita un altre mode anomenat XML-RPC, que es pot baixar des de

[https://launchpad.net/xml-rpc-el](https://launchpad.net/xml-rpc-el)

$ wget [http://launchpad.net/xml-rpc-el/trunk/1.6.8/+download/xml-rpc.el](http://launchpad.net/xml-rpc-el/trunk/1.6.8/+download/xml-rpc.el)

i ho copiem a la carpeta de l'emacs on tenim 'org2blog…

Per a que l'emacs pugui iniciar els modes afegits, cal especificar-ho al document de configuració personalitzada de l'emacs

$ emacs ~/.emacs

i a dins afegim:

(setq load-path (cons "~/.emacs.d/org2blog/" load-path))

(require 'org2blog)

Això especifica on és el mode org2blog.el i els altres \*.el

Seguidament podem triar que ens precarregui directament certes configuracions dels nostres blocs afegint al .emacs:

$ emacs ~/.emacs

i a dins afegim:

(setq org2blog/wp-blog-alist

'(("wordpress"

:url "[http://username.wordpress.com/xmlrpc.php](http://username.wordpress.com/xmlrpc.php)"

:username "username"

:default-title "Hello World"

:default-categories ("org2blog" "emacs")

:tags-as-categories nil)

("my-blog"

:url "[http://username.server.com/xmlrpc.php](http://username.server.com/xmlrpc.php)"

:username "admin")))

 

On canviem 'username' per les nostres dades…

Un cop ho tenim tot, ara només cal començar a publicar!!! Iniciem l'emacs, i després amb (M=tecla Alt)

M-x org2blog/wp-new-entry

ara, ens pregunta si volem login, diem "y", després ens demana el bloc, i li direm el nom que hem configurat abans, per exemple "wordpress", i seguidament ens demana la contrasenya.

Un cop ho tenim escrit, publiquem amb: C-c p >> és a dir: Control + c i soltant premem p

A la font: [https://github.com/punchagan/org2blog](https://github.com/punchagan/org2blog) podem trobar en anglès totes les combinacions de teclat per treballar amb emacs.

;)
