---
title: "tmux, per veure la terminal d'una altra manera"
date: "2012-03-18"
categories: 
  - "terminal"
---

Ja fa uns dies vaig parlar de l'eina **screen**, avui vull parlar de tmux. [tmux](http://tmux.sourceforge.net/) és una terminal multiplexer que permet moltes coses. Una d'elles és tenir varies finestres a la vegada en la mateixa terminal. També permet deixar una sessió funcionant, tancar la terminal, però continuar funcionant.

Algunes de les dreceres de teclat per al seu ús:  
C-b c > crea una finestra nova  
C-b % > divideix la finestra en vertical  
C-b " > divideix la finestra en horitzontal  
C-b o > permet canviar entre les diferents terminals actives per tmux  
C-b ! > tanca totes les terminals de la mateixa finestra deisant només l'actual.  
C-b w > llista les finestres actuals del tmux  
C-b p > finestra anterior (previous)  
C-b n > finestra següent (next)  
C-b & > mata la finestra on ens trobem i totes les seves terminals  
C-b q > llista les diferents terminals de la mateixa finestra, escollint el número podem canviar-nos  
C-b x > tanca la finestra  
C-b , > permet canviar el nom de la finestra  
C-b d > surt de tmux deixant-lo funcionant, per tornar a accedir només cal esciure **tmux attach**.  
C-b ? > llista la drecera de teclat  

Hi ha una pàgina amb molta més informació [sobre tmux i screen.](http://www.dayid.org/os/notes/tm.html)
