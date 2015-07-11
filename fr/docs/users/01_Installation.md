# Les pré-requis sur le serveur

FreshRSS est un logiciel développé en PHP reposant sur le modèle client - serveur. C'est-à-dire qu'il vous faudra un serveur web pour en profiter. Ensuite, FreshRSS ne demande pas une configuration très fournie et peut donc, en théorie, tourner sur la plupart des serveurs mutualisés.

Il est toutefois de votre responsabilité de vérifier que votre hébergement permettra de faire tourner FreshRSS avant de nous taper dessus. Dans le cas où les informations listées ci-dessous ne seraient pas à jour, vous pourrez.

 | Logiciel         | Recommandé                                                                                                | Fonctionne aussi avec          | 
 | --------         | -----------                                                                                                | ---------------------          | 
 | Serveur web      | **Apache 2**                                                                                               | Nginx                          | 
 | PHP              | **PHP 5.3.7+**                                                                                             | PHP 5.2+                       | 
 | Modules PHP      | Requis : libxml, cURL, PDO_MySQL, PCRE et ctype \\ Recommandé : JSON, Zlib, mbstring et iconv, ZipArchive |                                | 
 | Base de données | **MySQL 5.0.3+**                                                                                           | SQLite 3.7.4+                  | 
 | Navigateur       | **Firefox**                                                                                                | Chrome, Opera, Safari or IE 9+ | 

## Note importante

FreshRSS **PEUT** fonctionner sur la version de PHP 5.3.3. En effet, nous utilisons des fonctions spécifiques pour la connexion par formulaire et notamment la bibliothèque ''password_compat''. Celle-ci est compatible avec PHP >= 5.3.7 ou certaines versions plus anciennes incluant un patch spécifique. Cela dépend de la distribution :

*  CentOS et la Red Hat Enterprise Linux 6.5 sont supportés.
*  En revanche, **Debian avec PHP 5.3.3 n'est pas supporté !** ([Plus d'informations](https://github.com/ircmaxell/password_compat#requirements))

# Choisir la bonne version de FreshRSS

FreshRSS possède trois versions différentes (nous parlons de branches) qui sortent à des fréquences plus ou moins rapides. Aussi prenez le temps de comprendre à quoi correspond chacune de ces versions.

## La version stable

[Téléchargement](https://github.com/FreshRSS/FreshRSS/archive/master.zip)

Cette version sort lorsqu'on considère qu'on a répondu à nos objectifs en terme de nouvelles fonctionnalités. Deux versions peuvent ainsi sortir de façon très rapprochée si les développeurs travaillent bien. En pratique, comme nous nous fixons de nombreux objectifs et que nous travaillons sur notre temps libre, les versions sont souvent assez espacées (plusieurs mois). Son avantage est que le code est particulièrement stable et vous ne devriez pas faire face à de méchants bugs.

## La version béta

[Téléchargement](https://github.com/FreshRSS/FreshRSS/archive/beta.zip)

Afin de pallier au rythme irrégulier de la version stable, nous avons mis en place un système de sorties à intervalle de 1 mois environ. Le code est un peu moins stable (nous n'avons pas le temps de tester en profondeur) mais nous faisons en sorte qu'elle soit utilisable de la façon la plus optimale qu'il soit. Son avantage est de pouvoir profiter des dernières nouveautés de FreshRSS de façon relativement rapide.

## La version de développement

[Téléchargement](https://github.com/FreshRSS/FreshRSS/archive/dev.zip)

Comme son nom l'indique, il s'agit de la version sur laquelle les développeurs travaillent. **Elle est donc totalement instable !** Si vous souhaitez recevoir les améliorations au jour le jour, vous pouvez l'utiliser, mais attention à bien suivre les évolutions sur Github (via [le flux RSS de la branche](https://github.com/FreshRSS/FreshRSS/commits/dev.atom) par exemple). On raconte que les développeurs principaux l'utilisent quotidiennement sans avoir de soucis. Sans doute savent-ils ce qu'ils font…

# Installation sur Apache

**TODO**

Cette partie n'a pas encore été écrite. Néanmoins, comme il s'agit d'une bête application PHP, cela ne pose généralement pas de soucis à installer :)

# Installation sur Nginx

**TODO**

Cette partie n'a pas encore été écrite. Vous pouvez néanmoins suivre [un article dédié](http://www.pihomeserver.fr/2013/05/08/raspberry-pi-home-server-installer-un-agregateur-de-flux-rss-pour-remplacer-google-reader/).

# Conseils de sécurité

**TODO**
