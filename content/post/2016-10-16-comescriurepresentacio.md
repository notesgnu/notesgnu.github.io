---
title: "Com escriure una presentació"
date: 2016-10-16
author: "msales24"
categories:  ["org-mode"]
tags: ["org-mode", "emacs"]
id: 20240424183756
---

# COM ESCRIURE UNA PRESENTACIÓ  
amb **EMACS** i **Org-mode**

> Podeu descarregar-vos la [presentació](http://xtec.cat/%7Emsales24/orgmode/presentacio.htmlpresentacio.pdf) i el codi en [.org](http://xtec.cat/%7Emsales24/orgmode/presentacio.htmlpresentacio.zip)

## 1 Alguns aspectes

### 1.1 Què anem a fer?

A continuació explicarem com fer una presentació de manera molt senzilla a partir de notes, usant:

-   [Org mode](http://orgmode.org/) i
-   [Emacs](https://www.gnu.org/software/emacs/)
-   i [LaTeX](https://www.latex-project.org/) (classe [Beamer](https://es.wikipedia.org/wiki/Beamer)).

Són eines **lliures** que ens permeten a partir d'unes marques senzilles, realitzar presentacions en **PDF** que podem veure en qualsevol ordinador _exactament_ com nosaltres el veiem al nostre.

### 1.2 Com ho fem?

A partir d'un text pla, i editant-lo amb **Org mode**, ens permet amb un llenguatge de marques molt senzill, crear i editar presentacions. Això ens dóna molts avantatges:

-   **No cal saber LaTeX** per començar, tot i que amb el temps ens facilitarà molt la feina.
-   A partir d'unes notes **tenim un document de qualitat**:
    -   podem moure les diapositives
    -   podem afegir taules, imatges,….
    -   podem crear un índex de treballar i fer un seguiment de la feina
    -   podem exportar-ho a altres formats (html, odt, LaTeX…)

### 1.3 Què necessitem

-   Tenir una instal·lació de LaTeX [TeX Live](http://www.tug.org/texlive/)
-   Tenir instal·lat **Emacs** i **Org mode** (per fer la exportació)

## 2 Comencem a fer Presentacions

### 2.1 El títol

La primera diapositiva és el títol. Normalment hi posem el títol, l'autor i la data:

-   el **títol** del document
    
    ```
    <span style="color: #b3b3b3;">#+TITLE:</span> <span style="color: #afeeee; font-weight: bold;">Posem el títol del document</span>
    ```
    
    (si no el posem, no ens apareixerà a la presentació)
    

### 2.2 L'autor

-   el nom de l'**autor/a**
    
    ```
    <span style="color: #b3b3b3;">#+AUTHOR:</span> <span style="color: #afeeee;">Nom i Cognom</span>
    ```
    

### 2.3 La data

-   la **data**
    
    ```
    <span style="color: #b3b3b3;">#+DATE:</span> <span style="color: #afeeee;">16 d'octubre de 2016</span>
    ```
    
    (podem usar la macro de LaTeX macro `\today`, o escriure directament _today_)
    

### 2.4 aspectes de lletra

Pots escriure posant el text entre marques, així tenim **bold**, _italic_, underlined, `verbatim`, `code` ‘+strike-through+’ i també pode posar una línia de codi:

```
codi
```

```
<span style="color: #ffffff; background-color: #000000; text-decoration: underline;">*bold*</span>
<span style="background-color: #ff0000; text-decoration: underline;">/italic/</span>
<span style="text-decoration: underline;">_underlined_</span>
<span style="color: #b3b3b3;">=verbatim=</span> 
<span style="color: #b3b3b3;">~code~</span>
<span style="text-decoration: line-through;">+strike-through+</span>
<span style="color: #b3b3b3;">: codi</span>
```

### 2.5 opcions

Si no volem que surti alguna part del títol, podem afegir a les opcions **nil**, per exemple:

```
<span style="color: #00ffff;">#+OPTIONS: author:nil</span>
```

_Es poden incloure moltes més coses (email, logos, nomde centre…), però aquest taller és només per fer un inici…_

### 2.6 L'estructura

les presentacions festes amb Org mode aprofiten els títols per marcar cada diapositiva. Per defecte…

-   els títols que marquem amb un '\*' esdevenen cada diapo
-   Els nivells inferiors formaran part de **blocs i altres estructures de la diapo**
-   la diapo de la **taula de continguts** (toc) es crea sola

Si no volem que aparegui la taula de continguts, llavors a les opcions posem **nil**:

```
<span style="color: #00ffff;">#+OPTIONS: toc:nil</span>
<span style="color: #00ffff;">* Diapo 1</span>
el contingut
<span style="color: #0000ff;">** bloc</span>
blocs interns
```

### 2.7 Per crear una diapo

Podem crear una llista:

-   item 1
-   item 2
-   item 3

igual com ho fem amb el mode Org:

```
<span style="color: #00ffff;">* A title</span>
- item 1
- item 2
- item 3
```

### 2.8 Usant imatges

podem afegir imatges:

![orgmode.png](http://xtec.cat/%7Emsales24/orgmode/presentacio.htmlimatges/orgmode.png)

```
<span style="color: #00ffff;">#+ATTR_LaTeX: :width 100</span>
 <span style="color: #00ffff; text-decoration: underline;">file:imatges/orgmode.png</span>
```

### 2.9 orgmode inserir imatges de web

-   imatge online  
    1.  si exportem a html podem usar imatges de la web:  
        
        ![emacs.png](https://www.gnu.org/software/emacs/images/emacs.png)<sup><a id="fnr.1" class="footref" href="http://xtec.cat/%7Emsales24/orgmode/presentacio.html#fn.1">1</a></sup>
        
    2.  si exportem a PDF  
        
        hem de tenir les imatges en local
        

### 2.10 Creant una taula de continguts

A les opcions `#+OPTIONS:` podem canviar l'opció `H` al nivell que volem els títols, per exemple a `2`:

```
<span style="color: #00ffff;">#+OPTIONS: H:2 toc:t</span>
```

així tenim que ara el primer nivell esdevé seccions i el segon nivell són les diapos.

### 2.11 comentaris

el comentaris es fan amb # seguit d'un espai al davant d'una frase… així no surt la frase a l'exportar-se. [http://orgmode.org/manual/Comment-lines.html](http://orgmode.org/manual/Comment-lines.html)

### 2.12 notes de peu

`C-x C- f` introdueix notes de peu i genera un apartat de notes de peu:

```
text amb nota de peu<span style="color: #00ffff; text-decoration: underline;">[fn:1]</span>
text dos<span style="color: #00ffff; text-decoration: underline;">[fn:2]</span>

<span style="color: #00ffff;">* footnotes</span>
<span style="color: #00ffff; text-decoration: underline;">[fn:1]</span> nota 1 
<span style="color: #00ffff; text-decoration: underline;">[fn:2]</span> nota 2
```

C-u C-c C-x f més opcions de notes de peu

## 3 Editant les presentacions

### 3.1 Per començar

Carreguem el mode amb:

```
M-x org-beamer-mode RET
```

Si volem que es carregui directament a l'obrir el fitxer escrivim al principi:

```
<span style="color: #00ffff;">#+STARTUP: beamer</span>
```

### 3.2 Recepta final ràpida

El primer, agafem un document ja fet amb **Org mode**, ens posem al principi

1.  escrivim:  
    
    ```
    <span style="color: #00ffff;">#+STARTUP: beamer</span>
    ```
    
2.  teclegem:  
    
    ```
    C-c C-e #
    ```
    
    i demanem amb la tecla `TAB` l'opció `default`
    
    Omplim l'autor, títol, data i d'altres aspectes… i ja podem exportar…
    

### 3.3 Per exportar a PDF

El primer que es cal és carregar el mode menor **Beamer** per a **org-mode**. Si no el tenim iniciat, ho podem activar teclejant:

```
M-x org-beamer-mode
```

ara ja tenim unes comandes **extra** al menú de l'exportació de LaTeX

`C-c C-e l B`

Export as LaTeX buffer (Beamer).

`C-c C-e l b`

Export as LaTeX file (Beamer).

`C-c C-e l P`

**Export as PDF file** (Beamer).

`C-c C-e l O`

Export as PDF file and **open** (Beamer).

### 3.4 Exportar com article

Usem `beamerarticle`, per exemple:

```
<span style="color: #00ffff;">#+startup: beamer</span>
<span style="color: #00ffff;">#+LaTeX_CLASS: article</span>
<span style="color: #00ffff;">#+LaTeX_CLASS_OPTIONS: [a4paper,twoside,11pt]</span>
<span style="color: #00ffff;">#+BEAMER_THEME: default</span>
<span style="color: #00ffff;">#+LATEX_HEADER: \usepackage{beamerarticle}</span>
```

### 3.5 Per exportar a ODT

Executem la comanda:

```
M-x org-odt-export-to-odt
```

Ara si volem exportar de nou només cal

-   **C-c C-e o**

i ja podem exportar-ho a **odt**

### 3.6 conversor odt a orgmode

[https://bitbucket.org/josemaria.alkala/odt2org/wiki/Home](https://bitbucket.org/josemaria.alkala/odt2org/wiki/Home)

### 3.7 convertir a wiki

Podem exportar a altres llenguatges de marques usant **pandoc**, per exempe si volem en llenguatge **MediaWiki**:

```
pandoc -s -S -t mediawiki --toc document.org -o document.wiki
```

més informació a la pàgina de [Pandoc](http://pandoc.org/demos.html)

### 3.8 Incloure altres documents

Podem incloure altres documents en un document principal, usant `#+INCLUDE:`:

```
<span style="color: #00ffff;">#+INCLUDE: "CAPITOL1.org"</span>
<span style="color: #00ffff;">#+include: "CAPITOL2.org"</span>
<span style="color: #00ffff;">#+include: "CAPITOL3.org"</span>
```

### 3.9 Incloure una taula

Per incloure una taula usem el format típic d'orgmode:

   
|   | a | b | c |
| --- | --- | --- | --- |
| x | 1 | 2 | 3 |
| y | 4 | 5 | 6 |
| z | 7 | 8 | 9 |

L'exemple del codi a escriure:

```
<span style="color: #87cefa;">|   | a | b | c |</span>
<span style="color: #87cefa;">|---+---+---+---|</span>
<span style="color: #87cefa;">| x | 1 | 2 | 3 |</span>
<span style="color: #87cefa;">| y | 4 | 5 | 6 |</span>
<span style="color: #87cefa;">| z | 7 | 8 | 9 |</span>
```

### 3.10 importar taules

exportem una taula de full de càlcul a cvs

```
M-x org-table-import
```

i escrivim la taula amb el nom

### 3.11 orgmode en altres editors

-   **editor online** d'orgmode i altres llenguatges de marques [http://markup.rocks/](http://markup.rocks/)
-   Sublime Text editor, with Org syntax [https://github.com/danielmagnussons/orgmode](https://github.com/danielmagnussons/orgmode)
-   orgmode a l'editor atom [https://atom.io/packages/org](https://atom.io/packages/org)
-   orgzly per a **android** [http://www.orgzly.com/](http://www.orgzly.com/)

### 3.12 més informació

-   questions [https://stackoverflow.com/questions/tagged/org-mode](https://stackoverflow.com/questions/tagged/org-mode)
-   documentació [http://orgmode.org/manual/index.html](http://orgmode.org/manual/index.html)
-   comunitat [http://orgmode.org/worg/](http://orgmode.org/worg/)
-   exemples i receptes [http://ehneilsen.net/notebook/orgExamples/org-examples.html](http://ehneilsen.net/notebook/orgExamples/org-examples.html)

## 4 Llicència

### 4.1 Llicència

-   Basat en [reference card org-beamer](https://github.com/fniessen/refcard-org-beamer/) de Fabrice Niessen

![by_petit.png](http://xtec.cat/%7Emsales24/orgmode/presentacio.htmlimatges/by_petit.png)

[Aquesta obra està subjecta a una llicència de Reconeixement 4.0 Internacional de Creative Commons](https://creativecommons.org/licenses/by/4.0/deed.ca)

1.  Sou lliure de:  
    
    -   Compartir — copiar i redistribuir el material en qualsevol mitjà i format
    -   Adaptar — remesclar, transformar i crear a partir del material per a qualsevol finalitat, fins i tot comercial.
    

## Footnotes:

<sup><a id="fn.1" class="footnum" href="http://xtec.cat/%7Emsales24/orgmode/presentacio.html#fnr.1">1</a></sup>

[http://orgmode.org/manual/Images-in-HTML-export.html](http://orgmode.org/manual/Images-in-HTML-export.html)

Date: 16 d'octubre de 2016
Author: Manel Sales
Created: 2016-10-16 dg 19:30
[Validate](http://validator.w3.org/check?uri=referer)
