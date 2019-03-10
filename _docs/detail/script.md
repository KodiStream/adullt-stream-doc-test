---
title: Script
permalink: /docs/script/
---

### Script Bash par Venom
---

```bash
#!/bin/bash

#texte recherche
TEXT='avatar'

#categorie 1 Films - 2 Séries et Mangas - 3 Divers
CAT='1'

curl -i \
-H "Accept: application/json" \
-H "Content-Type:application/json" \
-X POST --data '{"jsonrpc":"2.0","method":"GUI.ActivateWindow","params":{"window":"videos","parameters":["plugin://plugin.video.vstream/?function=searchMovie&sCat='$CAT'&searchtext='$TEXT'&site=globalSearch"]},"id":"1"}}' http://localhost:8080/jsonrpc?request=
```

http://localhost:8080/ ou localhost peux être l'ip de votre Kodi.

**Fonctionnement:**

- Créer un fichier json.sh avec le code si dessus.
- (Linux) Dans un terminal executer : bash /cible du fichier/json.sh.
- (windows) Aucune idée.

### Script Bash par 1shad
---

```bash
#!/bin/sh

#
# exemples d'utilisation:
# $ json.sh -t "les bracelets rouges"
# $ json.sh -t "les bracelets rouges" -c 2 -p 8080 -i localhost
#

text=""
ip="localhost"
port="8080"
categorie="1"


# ecrit un message d'aide
usage() {
    echo "Usage: json.sh [-hipc] [ -t <TEXT> ]"
    echo ""
    echo "      -h: Affiche ce message d'aide"
    echo "      -i: Adresse ip de Kodi (default: localhost)"
    echo "      -p: Le port (default: 8080)"
    echo "      -c: La catégorie (1:film, 2:series et mangas, 3:divers; default: 1)"
    echo "      -t: Le text à rechercher"
    echo ""
    exit 1
}

# recupere les paramètres de la ligne de commande
while getopts c:t:i:p: option ; do
    case "$option" in
    c)
        opt_c=1
        categorie="${OPTARG}"
        ;;
    t)
        opt_t=1
        text="${OPTARG}"
        ;;
    i)
        opt_i=1
        ip="${OPTARG}"
        ;;
    p)
        opt_p=1
        port="${OPTARG}"
        ;;
    *)
        usage
        ;;
    esac
done

# sort et affiche le message d'aide si aucune option n'est choisie
# ou que le texte a rechercher est vide
if [ $(( opt_c + opt_t + opt_i + opt_p )) -eq 0 ] || ! [ -n "$text" ] ; then
    usage
fi

# sort et affiche le message d'aide si le paramètre catégorie n'est pas 1 ou 2 ou 3
if ! ( echo "$categorie" | grep -E '^[123]$' >/dev/null) ; then
    usage
fi

# execute la requete
curl -i \
-H "Accept: application/json" \
-H "Content-Type:application/json" \
-X POST --data '{"jsonrpc":"2.0","method":"GUI.ActivateWindow","params":{"window":"videos","parameters":["plugin://plugin.video.vstream/?function=searchMovie&sCat='"$categorie"'&searchtext='"$text"'&site=globalSearch"]},"id":"1"}}' http://${ip}:${port}/jsonrpc?request=
```

Vous pouvez retrouver la conversation : https://github.com/Kodi-vStream/venom-xbmc-addons/issues/1966
