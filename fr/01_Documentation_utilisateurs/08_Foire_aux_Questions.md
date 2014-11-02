Il est possible que nous n'ayons pas répondu à toutes vos questions dans les parties précédentes. La FAQ regroupe certaines interrogations qui n'ont pas trouvé leur réponse ailleurs.

## C'est quoi ce /i à la fin de l'URL ?

Bien entendu, le ''/i'' n'est pas là pour faire joli ! Il s'agit d'une question de performances et de praticité :

* Cela permet de servir les icônes, images, styles, scripts sans cookie. Sans cela, ces fichiers seraient souvent re-téléchargés, en particulier lorsque Persona ou le formulaire de connexion sont utilisés. De plus, les requêtes vers ces ressources seraient plus lourdes.
* La racine publique ''./p/'' peut être servie sans restriction d'accès HTTP (qui peut avantageusement être mise en place dans ''./p/i/'').
* Cela permet d'éviter des problèmes pour des fichiers qui doivent être publics pour bien fonctionner, comme ''favicon.ico'', ''robots.txt'', etc.
* Cela permet aussi d'avoir un logo FreshRSS plutôt qu'une page blanche pour accueillir l'utilisateur par exemple dans le cas de la restriction d'accès HTTP ou lors de l'attente du chargement plus lourd du reste de l'interface.

## Pourquoi le robots.txt se trouve dans un sous-répertoire ?

Afin d'améliorer la sécurité, FreshRSS est découpé en deux parties : une partie publique (le répertoire ''./p'') et une partie privée (tout le reste !). Le robots.txt se trouve donc dans le sous-répertoire ''./p''.

Comme expliqué dans les [conseils de sécurité](fr/users/installation/security), il est recommandé de faire pointer un sous-domaine vers ce sous-répertoire afin que seule la partie publique ne soit accessible par un navigateur web. De cette manière http://demo.freshrss.org/ pointe vers le répertoire ''./p'' et le robots.txt se trouve bien à la racine du site : http://demo.freshrss.org/robots.txt.

L'explication est la même pour les fichiers ''favicon.ico'' et ''.htaccess''.
