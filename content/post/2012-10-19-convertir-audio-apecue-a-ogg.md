---
title: "Convertir audio (APE+CUE a OGG)"
date: "2012-10-19"
categories: 
  - "audio"
  - "ffmpeg"
  - "ogg"
---

Ja fa molt de temps se'm va ocurrer usar [http://www.monkeysaudio.com/](http://www.monkeysaudio.com/) per fer còpies de seguretat dels meus discs de música. Aquest programa convertia el CD d'àudio en dos fitxers, un acabat en [APE](http://es.wikipedia.org/wiki/Monkey%27s_Audio) i un altre amb l'extenció [CUE](http://es.wikipedia.org/wiki/Cue_sheet). Després d'uns quants anys me'ls he retrobat en un disc dur extern i, avui, he volgut passar-los a **OGG**. Així que mans a l'obra…  
Primer que res, caldrà instal·lar alguns paquets, en el cas de **debian** jo he instal·lat els següents, que no tenia instal·lats:

 apt-get install ffmpeg monkeys-audio vorbis-tools bchunk flac wacpack cuetools shntool mp3info

En el cas de **Debian Testing** m'ha donat un error el libavcodec53, així que l'he reinstal·lat :-)  
Ara anem a convertir l'arxiu **APE** a **WAV** amb:

mac arxiuaconvertir.ape arxiufinal.wav -d

Ara ens queda dividir el gran arxiu que ens ha quedat en les pistes, la informació la tenim a l'arxiu **CUE**. En l'arxiu CUE hi ha la informació d'on comença i on acaba la pista, i és aquesta informació que s'usa per dividir-ho.  
Així, per dividir l'arxiu **WAV** usant la informació **CUE** usarem la comanda _bchunk_:

bchunk -w arxiu.wav nomarxius.cue result

result és el nom que tindran els arxius al separar-se quedant result01.wav, result02.wav, result03.wav …. I finalment ja podem convertir els arxius de **WAV** a **OGG** usant les eines **vorbis-tools**:

oggenc -b 256 \*.wav

el 256 fa referència a un bitrate de 256 kbps.  

També podem usar altres eines per convertir. Així, una altra possibilitat és usar **ffmpeg**: per convertir en **OGG**

ffmpeg -i audio.wav  -acodec libvorbis audio.ogg

o a **MP3**:

ffmpeg -i audio.wav -acodec libmp3lame audio.mp3

Fonts:  
[https://wiki.archlinux.org/index.php/APE%2BCUE\\\_Splitting](https://wiki.archlinux.org/index.php/APE+CUE_Splitting)  
[http://tuxarena.blogspot.com.es/2009/04/how-to-convert-ape-to-ogg-vorbis-or-mp3.html](http://tuxarena.blogspot.com.es/2009/04/how-to-convert-ape-to-ogg-vorbis-or-mp3.html)  
[http://linuxconfig.org/ffmpeg-audio-format-conversions](http://linuxconfig.org/ffmpeg-audio-format-conversions)
