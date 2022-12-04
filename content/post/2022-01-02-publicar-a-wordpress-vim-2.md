---
layout: post
title: "Publicar un article des de VIM 2"
date: 2021-01-02
categories: ["vim"]
tags: ["vim", "wordpress"]
---


Ja hem començat l’any 2022 i sempre venen ganes de començar projectes i [aprendre coses noves](https://croniqueslinux.wordpress.com/2022/01/02/publicar-un-article-des-de-vim/).

Porto anys usant **Emacs** i aquest any tinc ganes d’apendre a usar **Vim**. Una de les coses que més m’agrada d’**Emacs** és el _mode_ **Orgmode**. Entre d’altres coses, poder publicar a _WordPress_ directament amb articles escrits _org_.

També vull usar de forma més habitual el llenguatge de marques **Markdown**. Així que m’ha vingut la necessitat de publicar a _WordPress_ directament amb **Vim**

Passo a explicar els passos!

### Instal·lació

El primer que cal fer és instal·lar l’afegit (“Plugin”). Per fer-ho, jo he usat [Vundle](https://github.com/VundleVim/Vundle.vim). Un cop instal·lat he afegit el “PlugIn” a l’arxiu **.vimrc**:  
`vim ~/.vimrc`

I afegim la comanda:  
`Plugin 'mrpeterlee/VimWordpress'`

Ara, ho desem `:wq!` i tanquem l’arxiu.

> Com a nota a tenir en compte!  
> Cal afegir abans de la línia de .vimrc:  
> `filetype plugin indent on`

Un cop fet, passem a crear les dades del **Blog**, per fer-ho hem de crear l’arxiu:  
`vim ~/.vimpressrc`  
i afegir:  
`[Blog0]   blog_url = https://yoursite.com/   username = usuari   password = contrassenya`

Ara ja ho tenim tot preparat!

### Ús

Les comandes més habituals són:  
– :BlogList – Llista 30 posts recents.  
– :BlogList page – Llista 30 pàgines recents.  
– :BlogList post 100 – Llista 100 recent posts.  
– :BlogNew post – Escriu un post nou.  
– :BlogNew page – Escriu una pàgina nova.  
– :BlogSave – Desa.  
– :BlogSave draft – Desa com esborrany.  
– :BlogPreview local – Previsualitzar pàgina/post localment al navegador.  
– :BlogPreview publish – com “:BlogSave publish” amb el navegador obert.

### Escriure amb Markdown

Això m’ha portat una mica de cap, ja que no hi havia trobat massa referenciat, només alguna pàgina antiga i poc clares.

Per defecte cal esriure amb _HTML_, però jo prefereixo fer-ho amb _Markdown_ així que ens cal tenir instal·lada la llibreria de _Python i Markdown_ i per fer-ho en **Ubuntu** jo ho faig:  
`sudo apt install -y python-markdown`

Els articles han de començar amb l’encapçalament següent:  
`"=========== Meta ============   "StrID :   "Title : Publicar un article des de VIM   "Slug :   "Cats : VIM   "Tags : markdown, md, vim   "=============================   "EditType : post   "EditFormat : Markdown   "BlogAddr : [https://qqqqqqq.wordpress.com/](https://qqqqqqq.wordpress.com/)   "========== Content ==========`

Ara, cal tenir present que cal començar amb la capçalera indicant que ho farem amb `Markdown`:  
`"EditFormat : Markdown`

### Publicar

Finalment un cop el tenim escrit, res més fàcil que desar `:wq!` i publicar `:BlogPreview publish` i sen’s obre el navegador i ja podem veure-ho publicat.

Al publicar es crea un identifcador  
`"StrID : XXX`

En desar-ho , podem anar actualitzant modificant i tornant a publicar.

![😛](https://s0.wp.com/wp-content/mu-plugins/wpcom-smileys/twemoji/2/svg/1f61b.svg)

### Referències

-   [https://github.com/MrPeterLee/VimWordpress](https://github.com/MrPeterLee/VimWordpress)
-   [https://lesolivex.com/vim-wordpress-markdown/](https://lesolivex.com/vim-wordpress-markdown/)
-   [https://www.cyberhades.com/2012/05/11/vim-markdown-y-wordpress/](https://www.cyberhades.com/2012/05/11/vim-markdown-y-wordpress/)
-   [https://www.douban.com/note/332845887/?_i=1138206_Nc9GrG](https://www.douban.com/note/332845887/?_i=1138206_Nc9GrG)
-   [https://github.com/danielmiessler/VimBlog](https://github.com/danielmiessler/VimBlog)


[Font a Wordpress](https://croniqueslinux.wordpress.com/2022/01/02/publicar-un-article-des-de-vim-2/)
