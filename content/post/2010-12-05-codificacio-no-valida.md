---
title: "Codificació no vàlida"
date: "2010-12-05"
categories: 
  - "fedora"
  - "opensuse"
  - "terminal"
  - "ubuntu"
---

Avui estava copiant uns documents antics d'un disc dur vell al meu ordinador. I me m'he trobat un munt de símbols ? i al final de l'extensió la expressió "codificació no vàlida". Sempre que em passava això, el que feia era renombrar-ho, però aquesta vegada eren molts. Després de cercar molt, he trobat que això passa perquè la codificació que tenien era iso-8859-9, i el meu ordinador treballa amb utf8. La solució me l'ha donat la comanda CONVMV!!!

No la tenia instal·lada, així que primer cal:

en Fedora com a root: yum install convmv (ubuntu, 'apt-get install convmv', en opensuse no ho he provat, suposo que amb un 'zypper in convmv'), i ara executem la conversió de codificació:

**$ convmv -f iso-8859-9 -t utf8 --notest -r /lloc/on/tenim/elsdocuments/** I en uns segons tot perfecte!!! :P
