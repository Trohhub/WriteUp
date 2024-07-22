# Write up challenge Root me

**Table of Contents**

- [Write up challenge Root me](#write-up-challenge-root-me)
  - [HTTP - Directory indexing](#http---directory-indexing)
  - [HTTP - Headers](#http---headers)
  - [HTTP - POST](#http---post)
  - [HTTP - Redirection invalide](#http---redirection-invalide)
  - [HTTP - Verb tampering](#http---verb-tampering)

## HTTP - Directory indexing
En commencant le challenge on démarre sur une page blance, dans ce cas premier réflexe est d'effectuer, sois un curl, sois inspecter la page.

Suite à quoi une information en commentaire est donné, un chemin "admin/pass.html" cependant en faisant cela nous arrivont sur une page qui est un vérité un leures et nous dis de continuer de chercher.

Après une rapide réflexion on peut voir que dans le chemin donné on passe par un dossier "admin" et bingo, on arrive sur une page avec diverse chose, le "pass.html" qui est un leure mais un autre dossier est visible "backup/", don celui ci donne accès à un "admin.txt" avec le mot de passe pour le challenge.


## HTTP - Headers
En arrivant sur la page de démarrage du challenge un indice nous est donné: "Content is not the only part of an HTTP response"! Et donc par déduction il va falloir aller fouiller plus loin, en utilisant curl on peut utiliser le paramètre "-v" pour obtenir des informations supplémentaire dons les Header du site et dans le Header il y a un paramètre très interessant : "Header-Rootme-Admin: none".

La réponse est maintenant toute faites ! il suffit maintenant de refaire un curl en venant override la donné voulu ce qui donne "curl -v -H "Header-Rootme-Admin: true" http://challenge01.root-me.org/web-serveur/ch5/" ainsi le mot passe nous est donné.

## HTTP - POST
Ici il y a un score à battre, donc premier réflexe est de regarder dans l'inspecteur d'élément,  et on y voit plein de chose don la formule pour choisir le fameux nombre "aléatoire". Et ici, réponse toute bête, il suffit d'enlever la formule, et de la remplacer par un nombre assez grand pour battre le score, puis d'appuyer sur le bouton "Give a try!" 

## HTTP - Redirection invalide
Ce qu'on veut ici c'est les donnés de la page "index.html", de ce fait il suffit simplement de faire une chose simple, étant donné que le site est une passoire, il suffit de faire un curl vers l'index, ce qui donné "curl http://challenge01.root-me.org/web-serveur/ch32/index.php" et le mot de passe nous est rêvélé.


## HTTP - Verb tampering
En arrivant sur la page il demande automatiquement de quoi se login, dans ce cas réflexe c'est de faire un curl -v de la page, et au début du curl il y a ceci "GET /web-serveur/ch8/ HTTP/1.1" indiquant qu'il récupère une méthode GET pour valider le login, mais si on override pour à la place du GET on met autre chose, un PUT par exemple "curl -v http://challenge01.root-me.org/web-serveur/ch8/ -X PUT", et si cela n'est pas sécuriser cela fonctionne, comme ici, ce qui passe outre la sécurité et donne accès au mot de passe.