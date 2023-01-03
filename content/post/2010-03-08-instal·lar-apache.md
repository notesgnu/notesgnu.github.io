---
title: "Instal·lar  APACHE"
date: "2010-03-08"
categories: 
  - "programari"
  - "terminal"
---

![apache](images/apache-2.png)

Apache (viquipèdia): **Apache HTTP Server** és un [servidor](http://ca.wikipedia.org/wiki/Servidor "Servidor") [HTTP](http://ca.wikipedia.org/wiki/HTTP "HTTP") (de [pàgines web](http://ca.wikipedia.org/wiki/P%C3%A0gina_web "Pàgina web")) de [codi obert](http://ca.wikipedia.org/wiki/Codi_obert "Codi obert") [multiplataforma](http://ca.wikipedia.org/wiki/Multiplataforma "Multiplataforma") desenvolupat per [Apache Software Foundation](http://ca.wikipedia.org/wiki/Apache_Software_Foundation "Apache Software Foundation").

....

Per instal·lar-lo només cal escriure l'ordre següent a la terminal:

**$ sudo apt-get install apache2**

i per configurar-ho només cal editar:

**/etc/apache2/apache2.conf**

(recorda de fer una còpia de seguretat de la configuració inicial)

per aturar el servei o per iniciar-ho tenim l'ordre:

_**\# etc/init.d/apache2 restart**_

_**\# etc/init.d/apache2 stop**_

_**\# etc/init.d/apache2 start**_
