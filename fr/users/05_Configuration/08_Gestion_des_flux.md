## Informations

## Archivage

## Identification

## Avancé

### Récupérer un flux tronqué

La question revient régulièrement, je vais essayer de clarifier ici comment on peut récupérer un flux RSS tronqué avec FreshRSS. Sachez avant tout que la manière de s'y prendre n'est absolument pas "user friendly", mais elle fonctionne :)

Sachez aussi que par cette manière vous générez beaucoup plus de trafic vers les sites d'origines et qu'ils peuvent vous bloquer par conséquent. Les performances de FreshRSS sont aussi moins bonnes car vous devez alors aller chercher le contenu des articles un par un. C'est donc une fonctionnalité à utiliser avec parcimonie !

Ce que j'entends par "Chemin CSS des articles sur le site d’origine" correspond en fait au "chemin" constitué par les IDs et les classes (en html, correspond aux attributs id et class) pour récupérer uniquement la partie intéressante qui correspond à l'article. L'idéal est que ce chemin commence par un id (qui est unique pour la page)

#### Exemple 1 : Rue89

Pour trouver ce chemin, il faut se rendre à l'adresse d'un des articles tronqués (par exemple http://www.rue89.com/2013/10/15/prof-maths-jai-atteint-lextase-dihn-pedagogie-inversee-246635). Il faut alors chercher le "bloc" HTML correspondant au contenu de l'article (dans le code source !)

On trouve ici que le bloc qui englobe uniquement le contenu de l'article est ```<div class="content clearfix">```. On ne va garder que la classe .content ici. Néanmoins, comme je le disais plus haut, il est préférable de commencer le chemin avec un id. Si on remonte au bloc parent, il s'agit du bloc ```<div id="article">``` et c'est parfait ! Le chemin sera donc ```#article .content```

#### Liste de correspondances site -> chemin css

*  Rue89 : ```#article .content```
*  PCINpact : ```#actu_content```
*  Lesnumériques : ```article#body div.text.clearfix```

