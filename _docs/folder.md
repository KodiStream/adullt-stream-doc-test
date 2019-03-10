---
title: Dossier
permalink: /docs/folder/
---

### Dossier de Kodi
---

- Android : **Android/data/org.xbmc.kodi/files/.kodi/**
- iOS : **/private/var/mobile/Library/Preferences/Kodi/**
- Linux : **~/.kodi/**
- Mac : **/Users/%USER%/Library/Application Support/Kodi/**
- OpenELEC : **/storage/.kodi/**
- Windows : **%APPDATA%\roaming\kodi\**
- Windows 10 (Store) : **\Users\%USER%\AppData\Local\Packages\XBMCFoundation.Kodi_xxx\LocalCache\Roaming\Kodi\**

1) Remplacer **kodi** par **xbmc** suivant la version installée.

2) le dossier **addons** contient tous vos addons installés. (vstream, youtube, etc..)

3) le dossier **userdata** contient tous les fichiers relatif à votre compte Kodi (Playercorefactory, Keymap)

4) Appdatta et .kodi sont des fichiers caches.


### Dossier vStream
---

- **plugin.video.vstream**

1) Ajouter un site \resources\sites\votre site.py

2) Ajouter un host \resources\hosters\votre host.py


### Dossier log
---

**Android**
- <data/sdcard/Android>/data/org.xbmc.kodi/cache/temp/kodi.log
- /sdcard/Android/data/org.xbmc.kodi/files/.kodi/temp/kodi.log

**iOS/ATV2**
- private/var/mobile/Library/Preferences/kodi.log

**Linux**
- $HOME/.kodi/temp/kodi.log

**Mac OS X**
- /Users/<username>/Library/Logs/kodi.log

**Windows**
- %APPDATA%\Kodi\kodi.log
- C:\Users\%USER%\AppData\Roaming\Kodi

**Windows 10 (Store)**
- C:\Users\%USER%\AppData\Local\Packages\XBMCFoundation.Kodi_xxx\LocalCache\Roaming\Kodi
