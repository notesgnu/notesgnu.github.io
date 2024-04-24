---
title: "Editar o gestionar coneixement"
date: 2023-07-25
author: "msaliko"
categories:  ["PKM"]
tags: ["opendocument", "markdown"]
id: 20240424193028
---

# Editar o gestionar coneixement 

Sovint em trobo cercant i analitzant un bon editor per les notes que prenc. Això sempre em porta a provar noves eines, nous formats de text i a dedicar-hi molt de temps.

Fent una mica la mirada endarrere, m’adono que el gran problema és el temps invertit i la manca de resultats. Hi ha la teoria de Pareto on la major part de les vegades el 20% de l’esforç genera el 80% dels resultats. Per això, cal fer una aturada i pensar-hi.

M’agrada molt consultar informació, llegir i aprendre coses. Totes les notes les he intentat de registrar en paper, a blogs, en digital, etc…

El primer gran dilema:

## El format

Clar, tenir un document en paper és genial, el problema és com consultar-lo, com organitzar-lo, i que al final no acabi en un calaix o en un arxivador en un raconet.  
Una opció, en digital és trobar el format. Per descomptat, ha de ser en un estàndard obert. El problema És com tornarem al contingut, hi haurà algun programa que ens deixi obrir-lo, i finalment, no haver de dedicar temps a refer-lo?

Aquí vaig tenir el dilema entre dos editors, la famosa guerra de l’Emacs i Vim. Al final, he après a fer anar els dos, i són dues eines que serveixen per coses diferents, i no trobo cap problema saber fer anar les dues. Al final, personalment, em vaig decantar a usar Emacs. El format _org_ amb _Org-mode_ ha estat genial, és molt potent. I al poc temps vaig trobar _Markdown_. Així que vaig passar al segon dilema, org o markdown.

En un principi, el guanyador va ser org, però durant uns anys. El gran problema, treballar amb totes les funcionalitats depenia d’emacs, i no sempre tenia Emacs a mà. Finalment, em vaig decantar per _Markdown_, menys potent, però ja em feia servei per escriure.

Un cop decidit el format, em vaig trobar que Emacs va començar a fer-se gran, amb molts modes i constantment depenent de l’eina. Markdown ja em deixava lliure de l’eina!!!

## L’eina

Un cop alliberat de l’eina, va començar el gran problema, quina fer servir?, quantes?, com?  
El procés va ser complicat, passat per Emacs, Vim (de nou), Joplinapp, Zettlr, Obsidian, Logseq, i un llarg etc.

El problema era d’inici el concepte de «Per a què?», Clar si volem editar un llibre, segur que refem la idea inicial i anem a org o a LaTeX, o amb LyX (més visual). Si volem gestionar coneixement…. Bum! Llavors no estem buscant un EDITOR sinó un GESTOR!

Editar coneixement per després fer-ne què?, publicar-lo, llavors segur que em decanto per LaTeX i LyX. Però, és molt poc habitual que acabi passant. Tot i que hi ha e paquet de markdown per LaTeX que permet fusionar-ho.  
Gestionar coneixement, llavors necessito una eina per enllaçar, cercar, unir idees, compartir-les i continuar modificant. És una escriptura viva.

## Conclusió

Finalment, m’he decantat per Zettlr, tot i que no estic lligat a l’eina, ja que el format _Markdown_ m’allibera a usar la que vulgui, fins i tot, estic provant Visual Studio Code (que ja explicaré un altre dia). Si finalment vull editar en un llibre digital o per imprimir, es pot editar o convertir amb _Pandoc_ al format que vulgui, o des de la mateixa eina permet exportar.