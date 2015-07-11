Avec le nombre croissant d'articles stockés par FreshRSS, il devient important d'avoir des filtres efficaces pour n'afficher qu'une partie des articles. Il existe plusieurs méthodes qui filtrent selon des critères différents. Ces méthodes peuvent être combinées dans la plus part des cas.

##Par catégorie

C'est la méthode la plus simple. Il suffit de cliquer sur le titre d'une catégorie dans le panneau latéral. Il existe deux catégories spéciales qui sont placées en haut du-dit panneau :
  * *Flux principal* qui affiche uniquement les articles des flux marqués comme visible dans cette catégorie
  * *Favoris* qui affiche uniquement les articles, tous flux confondus, marqués comme favoris

##Par flux

Il existe plusieurs méthodes pour filtrer les articles par flux :
  * en cliquant sur le titre du flux dans le panneau latéral
  * en cliquant sur le titre du flux dans le détail de l'article
  * en filtrant dans les options du flux dans le panneau latéral
  * en filtrant dans la configuration du flux

##Par statut

Chaque article possède deux attributs qui peuvent être combinés. Le premier attribut indique si l'article a été lu ou non. Le second attribut indique si l'article a été noté comme favori ou non.

Dans la version 0.7.x, les filtres sur les attributs sont accessibles depuis la liste déroulante qui gère l'affichage des articles. Dans cette version, il n'est pas possible de combiner les filtres. Par exemple, on ne peut pas afficher les articles lus qui ont été notés comme favori.

À partir de la version 0.8, les filtres sur les attributs sont directement accessibles. Il est maintenant possible de les combiner. Comme il est possible de faire toutes les combinaisons, il y en a certaines qui retournent le même résultat. Par exemple, si les quatre filtres sont activés ou désactivés, le résultat sera le même.

Par défaut, le filtre n'affiche que les articles qui n'ont pas été lus.

##Par contenu

Il est possible de filtrer les articles par leur contenu en entrant une chaine de caractères dans le champ de recherche prévu à cet effet.

##Par mot-clé

À partir de la version 0.7.x, il est possible de filtrer les articles en utilisant des mots-clé. Ils doivent être saisis dans le champ de recherche utilisé pour le filtrage par contenu.

  * par auteur :
```
author:<nom>
```
  * par titre :
```
intitle:<titre>
```
  * par URL :
```
inurl:<url>
```

Attention à ne pas introduire d'espace entre le mot-clé et la valeur recherchée.
Il est important de noter que les mots-clé ne peuvent pas être combinés entre eux.

À partir de la version 0.8.x, la recherche par mot-clé s'est enrichi de la recherche par date. Le format utilisé est le format [ISO 8601](http://en.wikipedia.org/wiki/ISO_8601#Time_intervals).

```
date:<date>
```

Il est également possible de combiner les mots-clé pour faire un filtrage encore plus précis.
