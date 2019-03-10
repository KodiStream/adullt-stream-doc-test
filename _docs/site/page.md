---
title: Pages
permalink: /docs/page/
---

### Creer une page
---

- Ajouter une nouvelle page dans le dossier _docs/ 
(create new file exemple.md)
Votre fichier doit commencer par ces quelques lignes.

```
---
title: My Page
permalink: /docs/my-page/
---

Hello World!
```

Le nom donné en permalink ici my-page est celui de l'url.

- Editer `_data/docs.yml` vous pouvez créer un nouveau menu ou utiliser ceux déja présent.

```
- title: Bien débuter
  docs:
  - home
  - installation
  - clone
  - themes
  - customization
  - my-page
  
```

ou

```  
- title: Nouveau menu
  docs:
  - my-page
```

### Editer une page
---

- Sur chaque page ce trouve un lien (modifier cette page)
- Il vous suffis de modifier le fichier .md et de faire un pull request.

### Lien utilise
---
- CSS bootstrap : https://getbootstrap.com/docs/4.1/getting-started/introduction/
- Editeur de texte Markdown : https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
- Markdown live : https://markdown-it.github.io/
