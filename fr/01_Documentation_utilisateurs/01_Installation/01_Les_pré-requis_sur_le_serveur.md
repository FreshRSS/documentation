FreshRSS est un logiciel développé en PHP reposant sur le modèle client - serveur. C'est-à-dire qu'il vous faudra un serveur web pour en profiter. Ensuite, FreshRSS ne demande pas une configuration très fournie et peut donc, en théorie, tourner sur la plupart des serveurs mutualisés.

Il est toutefois de votre responsabilité de vérifier que votre hébergement permettra de faire tourner FreshRSS avant de nous taper dessus. Dans le cas où les informations listées ci-dessous ne seraient pas à jour, vous pourrez.

 | Logiciel         | Recommandé                                                                                                | Fonctionne aussi avec          | 
 | --------         | -----------                                                                                                | ---------------------          | 
 | Serveur web      | **Apache 2**                                                                                               | Nginx                          | 
 | PHP              | **PHP 5.3.7+**                                                                                             | PHP 5.2+                       | 
 | Modules PHP      | Requis : libxml, cURL, PDO_MySQL, PCRE et ctype \\ Recommandé : JSON, Zlib, mbstring et iconv, ZipArchive |                                | 
 | Base de données | **MySQL 5.0.3+**                                                                                           | SQLite 3.7.4+                  | 
 | Navigateur       | **Firefox**                                                                                                | Chrome, Opera, Safari or IE 9+ | 

### Note importante

FreshRSS **PEUT** fonctionner sur la version de PHP 5.3.3. En effet, nous utilisons des fonctions spécifiques pour la connexion par formulaire et notamment la librairie ''password_compat''. Celle-ci est compatible avec PHP >= 5.3.7 ou certaines versions plus anciennes incluant un patch spécifique. Cela dépend de la distribution :


*  CentOS et la Red Hat Enterprise Linux 6.5 sont supportés.

*  En revanche, **Debian avec PHP 5.3.3 n'est pas supporté !**

[Plus d'informations](https///github.com/ircmaxell/password_compat#requirements).


