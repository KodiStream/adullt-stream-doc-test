---
title: Lecteurs
permalink: /docs/lecteurs/
---


### Lecteurs externe
---

Le lecteur de Kodi à ces defauts, aussi pour améliorer la lecture vous pouvez faire sortir la video, music et même le streaming sur un lecteur externe pour cela il suffis d'ajouter un fichier playercorefactory.xml à votre dossier userdata.


**Trouvé le dossier userdata** : [Voir ici](https://vstream.ga/docs/folder/)

**Céer un fichier playercorefactory.xml** : 

- le lecteur externe sera VLC Windows. 
- Mode plein ecrand activé.
- Kodi reduit pendant la lecture.

```xml
<playercorefactory>
<players>
<player name="VLC" type="ExternalPlayer" audio="true" video="true">
<filename>C:\Program Files\VideoLAN\VLC\vlc.exe</filename>
<args>--fullscreen</args>
<hidexbmc>true</hidexbmc>
<hideconsole>false</hideconsole>
<warpcursor>none</warpcursor>
</player>
</players>
<rules action="prepend">
<rule video="true" player="VLC"/>
</rules>
</playercorefactory>
```

**Un grand choix d'option** :

Constulter le Wiki officiel de Kodi pour en savoir plus sur les differentes options disponible. Les plus interessantes (Filetype,Filename). [Wiki Kodi](https://kodi.wiki/view/External_players)

**Les lecteurs Android** : 

Un grand choix de lecteur s'offre à vous, ceux d'Android sont les plus importants car ce sont ceux qui ont le plus de soucis de Codec. [Wiki Kodi](https://kodi.wiki/view/HOW-TO:Use_external_players_on_Android#Basic_playercorefactory.xml_file)
