---
title: "WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!"
date: "2010-11-14"
categories: 
  - "terminal"
  - "xarxa"
---

Avui després d'actualitzar el servidor, m'he trobat amb un problema! resulta que tota la feina que intentava fer a través de SSH no funcionava!

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

Què podia fer?

llegint per internet, he trobat la idea en [systemadmin.es](http://systemadmin.es/2009/02/warning-remote-host-identification-has-changed) així que he esborrat el fitxer on es desen els fingerprints i a començar de nou!

$ sudo rm /home/user/.ssh/known\_hosts

i ja ha funcionat perfectament!

;)
