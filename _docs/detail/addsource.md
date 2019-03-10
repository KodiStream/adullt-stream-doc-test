---
title: Ajouter une source
permalink: /docs/add/
---

### Pour commencer
---

Tout d'abord vérifiez que le site n'existe pas déjà (même sous un autre nom) et que quelqu'un n'est pas déjà sur le coup. Il y a également un répertoire de sources commencées mais par encore terminées.

Pour vous aider, vous pouvez partir du fichier squelette https://github.com/Kodi-vStream/venom-xbmc-addons/blob/Beta/ajouter_une_source.py. (Il est fortement conseillé de partir de ce fichier, plutôt que d'une autre source existante.)

Placez ce fichier dans le répertoire "site" de Vstream pour le voir s'afficher dans "toutes les sources". Si ce n'est pas le cas vous avez surement une erreur de syntaxe ou de mise en page. Malheureusement pour vous, a cette étape Vstream "cache" toute les erreurs dans les logs (pour éviter de tout planter), donc si vous lisez :

`01:16:19 T:6276 NOTICE: [PLUGIN] Vstream: Load Plugin masource_org`   
`01:16:19 T:6276 NOTICE: [PLUGIN] Vstream: Cant import plugin masource_org`

C'est que vous avez effectivement un problème dans le code. Si vous êtes vraiment perdu, le site http://infoheap.com/python-lint-online/ peut vous aider a trouver la ligne en défaut.

Le début est facile, mais vous allez surement ralentir en arrivant aux regex (expressions régulières). Pour vous aider, le site https://regex101.com/ sera votre meilleur ami, pensez a mettre en option (le petit drapeau a droite) "GMIS".

En cas de blocage total, mettez votre fichier sur un site comme http://pastebin.com/, et demandez un coup de main sur le Github en passant le lien.

Merci de faire un effort pour au moins commencer le fichier avant de demander de l'aide.

Une fois fini, vous pouvez aussi le proposer en version officielle, sans votre feu vert, votre fichier ne sera pas réutilisé.


### Exemple de méthode sous Firefox pour trouver les regex.
---

Sélectionnez la partie de la page qui vous intéresse, (quelques titres/images/liens), clic droit "code source de la sélection", copier/coller le code obtenu sur le site regex101 (ou celui que vous préférez), et il ne vous reste plus qu'à tester vos regex.

Pour avoir un explication sur les regex, le plus simple étant de chercher "tutorial expression régulière" sur google (trop de choses à expliquer ici).  
  
Les plus utilisées sur Vstream sont par exemple:   

- code html   
`<code html><balise1>titre du film<balise2></balise3><code à n'en plus finir et qui peut changer><img="url du poster"><balise7><a ref="lien"><\a><balise9>`   
- Regex   
`<balise1>(.+?)<balise2>.+?<img="([^"]+)"><balise7><a ref="(.+?)">`   

(.+?) : n'importe quel caractère, une fois ou plus, en prenant la chaîne la plus courte possible, et on capture.   
.+? : n'importe quel caractère, une fois ou plus, en prenant la chaîne la plus courte possible, mais on s'en fiche.   
([^"]+) : Tout les caractères sauf le ", une fois ou plus et on la capture.   

Dans l'exemple précédent on se retrouve avec:   
aEntry[0] : titre du film   
aEntry[1] : url du poster   
aEntry[2] : lien   

### Image
---
[![Demo](http://zupimages.net/up/17/14/145p.jpg)](http://zupimages.net/up/17/14/145p.jpg)

### Logiciel Utile
---

+ Editeur Python: 
  - [Sublime Text](http://www.sublimetext.com/)
  - [Notepad++](http://notepad-plus-plus.org/fr/)   

+ Test ``sPattern``: 
  - [Pythex](http://pythex.org/)

