---
title: Clone Github
permalink: /docs/clone/
---

### Les logiciels
---

- [Kodi 17.6](https://kodi.tv/download).
- [Visual studio code](https://code.visualstudio.com/).
- [Git 2.18.0](https://git-scm.com/).

### Visual studio code
---
- Télécharger et lancer visual studio code.
- Lancer la palette de commande.

![Imgur](https://i.imgur.com/DUUgck0.png)

- Taper **git cloner** 
- Dans **url de dépôt** taper **https://github.com/Kodi-vStream/venom-xbmc-addons.git**
- Choisissez le dossier de destination et valider.
- Cliquez sur ouvrir le dépôt.

![Imgur](https://i.imgur.com/lg7nKKa.png)


### Kodi
---

- Lancer kodi et installer le depot de vstream puis vstream.
- Aller dans les informations de vstream.

![Imgur](https://i.imgur.com/Twrod4y.png)

- Désactiver la mise a jour automatique.

![Imgur](https://i.imgur.com/ivSSPQ3.jpg)


### Les dossiers
---

- Rendez-vous dans le dossier du clone de github. (**venom-xbmc-addons**).
- Crée un lien vers le dossier **plugin-video-vstream**.
- Sous Windows ne faite pas un raccourci mais un lien symbolique.
 
 ```mklink /D C:\Users\USER\AppData\Roaming\Kodi\addons\plugin.video.vstream C:\Users\USER\Documents\venom-xbmc-addons\plugin.video.vstream```

![Imgur](https://i.imgur.com/dprD0Zm.png)

- Couper le lien.
- Rendez-vous dans le dossier d’installation de vstream.

![Imgur](https://i.imgur.com/zy45Gw9.png)

- Supprimer le dossier **plugin.video.vstream**.
- Coller le lien du dossier puis renommer le lien en **plugin.video.vstream**.

![Imgur](https://i.imgur.com/XgBHMDn.png)

- Vous voila avec la version bêta en direct.


### Visual studio code
---

- Relancer visual studio code.
- Si vous avez activer l’ autofetch le logiciel vous informeras si un pull est disponible. (en bas a gauche le petit (1).
- **Dans tous les cas**, Il vous suffis de cliquez sur le petit cercle pour faire la récupération.

![Imgur](https://i.imgur.com/Q6vI4Wd.png)

![Imgur](https://i.imgur.com/uLopahe.png)

---

Voilà ça mettra à jour votre dossier plugin.video.vstream.
