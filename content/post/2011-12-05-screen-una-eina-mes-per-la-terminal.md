---
title: "Screen: una eina més per la terminal"
date: "2011-12-05"
categories: 
  - "terminal"
---

Fa uns dies que he descobert **screen** una eina molt útil per treure molt de suc del treball en la terminal. Sovint fem diferents tasques des de la terminal, i screen ens pot permetre fer més senzill el control i execució de les comandes. És a dir, tenir moltes sessions de treminal funcionant a la vegada en la mateixa terminal.

Una de les caracterísiques que trobo força interessants és que podem tancar la terminal i queda el pocrés persistent. Més tard reiniciem la terminal i tornar a l'aplicació executada.

Per instal·lar-la, només cal fer el de sempre:  
apt-get install screen (debian i derivats)  
yum install -y screen (fedora i derivats)  
zypper in screen (opensuse i derivats)  

Si volem configurar-lo, ho podem fer escrivint ~/.screenrc les característiques que desitgem que tingui.

### algunes ordres senzilles

$ screen comanda (executa una comanda amb screen  
$ screen -ls (ens llista les comandes en execució)  
$ screen -x (ens llista les comandes executant-se)  
$ screen -r (ens reacopla a la comada executant-se)  
$ exit (surt d'screen i torna a la terminal)  

### Les dreceres de teclat

Ctrl+a (C-a) és la forma base per executar altres combinacions:  
C-a ? ens dóna ajuda i funcions  
C-a 0 - 9 ens permet moure'ns entre les diferents finestres d'screen  
C-a C-n va a la finestra següent  
C-a C-p va a la finestra prèvia  
C-a C-a va a l'última finestra prèvia  
C-a a canvia el nom de la sessió  
C-a " ens llista les sessions en execució  
C-a k tanca la sessió  
C-a c crea una nova fiestra d'screen  
C-a C-d desconecta la sessió i torna a la terminal, queda executant-se  
C-a x bloqueja totes les sessions amb una contrassenya  
C-a a neteja de la memòria un C-a polsat per error  

Sempre podem obtenir més informació  
$ man screen

### fonts

font: [http://rz0r.blogspot.com/2007/12/screen-otra-util-herramienta-en-linux.html](http://rz0r.blogspot.com/2007/12/screen-otra-util-herramienta-en-linux.html)  
font: [http://guimi.net/blogs/hiparco/uso-basico-de-screen-en-linux/](http://guimi.net/blogs/hiparco/uso-basico-de-screen-en-linux/)  
Manual a magazine.redhat.com [http://magazine.redhat.com/2007/09/27/a-guide-to-gnu-screen/](http://magazine.redhat.com/2007/09/27/a-guide-to-gnu-screen/)
