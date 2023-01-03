---
title: "Un blog amb Jekyll"
date: "2015-03-29"
categories: 
  - "emacs"
  - "git"
  - "jekyll"
---

![](images/logo-2x.png)

Avui he decidit escriure alguna cosa, ja fa temps que no escric res. Així que he volgut provar una cosa que em ronda el cap fa dies, fer un bloc usant **git** i **jekyll**. Els motius són varis, però la idea d epoder escriure un bloc des d'EMACS i sincronitzar amb GIT, i amb el nom senzill… és irresistible.

S'usa per escriure el llenguatge de marques **[MarkDown](http://daringfireball.net/projects/markdown/)** i per defecte l'extensió .md, i **Emacs** compta amb markdown-mode que facilita la seva escriptura. Així que seguim amb **EMACS** :-)

Anem a per feina…

## Instal·lar-ho tot!

Primer que res cal instal·lar _git, ruby i jekyll_:

sudo apt-get install git ruby jekyll

Compte! també cal tenir instal·lat l'intèrpret de JavaScript (_nodejs_):

sudo apt-get install nodejs

## Creem pàgina en local

Ara, crearem l'espai per treballar en local, podem crear un blog usant **Jekyll**:

jekyll new jekyll-blog 

Però si volem crear una carpeta per sincronitzar amb **git**, ens cal que tingui el mateix nom d'usuari de Github. Per fer això podem usar **Jekyll**:

jekyll new nomusuari.github.io

o també **GIT**:

git init nomusuari.github.io

## Plantilles

Si volem podem trobar [plantilles](http://jekyllthemes.org/) de **Jekyll**, i així podem usar-ne una que ens agradi, només caldrà descomprimir tot el contingut del _zip_ dins de la nostra carpeta que hem creat abans.

## Iniciem el servidor local

Per poder navegar en el nostre blog i veure com va quedant, el podem executar amb:

jekyll serve

## Configurem GIT

Tot seguit ens cal configurar **git**, cal tenir un compte a Github:

git config --global user.name "nomusuari"
git config --global user.email "identificadordelcorreu"

## Sincronitzem amb GITHUB

Un cop veiem que el blog està al nostre gust, ara podem clonar-lo a la xarxa usant el Git. Així podem sincronitzar el nostre bloc i penjar-lo a la xarxa, primer entrem a la carpeta:

cd nomusuari.github.io

I cada vegada que fem un **push** s'actualitzarà.

git add --all
git commit -m "Initial commit"
git push -u origin master

Ens demanarà el nom d'usuari i després la contrasenya…

I amb tot això, ja ens ha de funcionar! ;-)

## Algunes solucions!

En algun cas podem trobar algun problema amb el **Ruby**, he trobat possibles solucions com ara:

sudo apt-get ruby-dev

o

sudo apt-get install ruby1.9.1-dev

és a dir instal·lant el **Ruby** en desenvolupament, i concretament la versió 1.9.1

Una altra cosa és poder instal·lar-lo com a **gema de Ruby**:

sudo gem install Jekyll

Un altre error que m'ha sortit alguna vegada és la manca de la **gema de Ruby (redcarpet)**, això m'ha passat en ubuntu 14.04 i derivades... vol dir que ens cal fer el que he comentat abans, i seguint els passos:

sudo apt-get install ruby1.9.1-dev
sudo gem install jekyll

En el cas d'**Ubuntu-mate** em donava un error amb els paquets _ruby\*dev_, així que al final he vist una solució, instal·lar:

sudo apt-get install ruby1.9.1-full

Un altre error que m'ha sortit instal·lant **Jekyll** a un altre netbook ha estat:

_/usr/lib/ruby/1.9.1/rubygems/custom\_require.rb:36:in \`require': iconv will be deprecated in the future, use String#encode instead_.

**La solució**:

sudo apt-get install rubygems-integration

## Fonts:

[http://raulavila.com/2015/01/como-hice-el-blog/](http://raulavila.com/2015/01/como-hice-el-blog/)

[http://efrenfuentes.net/creando-blog-con-github-jekyll-disqus/](http://efrenfuentes.net/creando-blog-con-github-jekyll-disqus/)

[http://jorgecasar.github.io/blog/como-crear-tu-blog-en-github-pages/](http://jorgecasar.github.io/blog/como-crear-tu-blog-en-github-pages/)

[http://blog.desdelinux.net/hacer-blog-jekyll/](http://blog.desdelinux.net/hacer-blog-jekyll/)

[http://www.hostdime.com.co/blog/como-crear-un-blog-con-jekyll-una-guia-para-principiantes/](http://www.hostdime.com.co/blog/como-crear-un-blog-con-jekyll-una-guia-para-principiantes/)

[http://onezetty.esy.es/gnu/como-hacer-un-blog-con-jekyll/](http://onezetty.esy.es/gnu/como-hacer-un-blog-con-jekyll/)

[https://pages.github.com/](https://pages.github.com/) [http://rogerdudler.github.io/git-guide/index.es.html](http://rogerdudler.github.io/git-guide/index.es.html)
