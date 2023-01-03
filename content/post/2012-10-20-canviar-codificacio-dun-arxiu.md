---
title: "Canviar codificació d'un arxiu"
date: "2012-10-20"
categories: 
  - "terminal"
  - "utf-8"
---

Avui m'ha passat que un arxiu vell (en text pla) i m'he trobat que en obrir-lo amb **gedit** o **emacs** m'he trobat que no es veia correctament. Així que he decidit convertir-lo a utf-8 a veure si es veia correctament. El primer que he fet és saber en quina codificació el tenia, i per fer-ho he usat la comanda **file**:

file arxiu.txt

I m'ha donat com a resposta: `arxiu.txt: ISO-8859 text, with CRLF line terminators` I ara a convertir-lo:

iconv --from-code=ISO-8859-1 --to-code=UTF-8 arxiuantic.txt > arxiunou.txt
També ho podem escriure així:
iconv -s -f ISO-8859-1 -t UTF-8 "arxiuantic.txt" > "arxiunou.txt"

I Ja ho tenim! :-)

Ara, cal comentar un cas especial. Resulta que també m'he trobat amb un arxiu que el tenia en xinès, en fer la comanda **file**, m'he trobat que em deia que també era ISO-8859 però en fer la comanda de conversió no ho feia correctament. I al final he recordat que l'arxiu l'havia escrit amb un programa de windows (d'això ja fa uns quants anys) i que el xinès simplificat el codifica en [cp936](http://en.wikipedia.org/wiki/Code_page_936 "codificació xinès"), així que la solució ha estat:

iconv -s -f cp936 -t utf-8 "arxiuanticxines.txt" > "arxiunouxines.txt"

Ara, en comptes de llegir "Ì«Ñô" ja puc llegir  "太阳"

:-P

fonts: [http://www.ehow.com/how\\\_12119808\\\_convert-iso-utf8.html](http://www.ehow.com/how_12119808_convert-iso-utf8.html) [http://blogofsysadmins.com/cambiar-la-codificacion-de-archivos-de-iso-8859-1-a-utf-8](http://blogofsysadmins.com/cambiar-la-codificacion-de-archivos-de-iso-8859-1-a-utf-8)
