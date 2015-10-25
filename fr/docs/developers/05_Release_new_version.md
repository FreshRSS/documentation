# Préparer la sortie

Afin d'avoir le plus de retour possible avant une sortie, il est préférable de l'annoncer sur GitHub en créant un ticket dédié ([voir les exemples](https://github.com/FreshRSS/FreshRSS/search?utf8=%E2%9C%93&q=Call+for+testing&type=Issues)). Ceci est à faire **au moins une semaine à l'avance**.

Il est aussi recommandé de faire l'annonce sur mailing@freshrss.org.

# S'assurer de l'état de dev

Avant de sortir une nouvelle version de FreshRSS, il faut vous assurer que le code est stable et ne présente pas de bugs majeurs. Idéalement, il faudrait que nos tests soient automatisés et exécutés avant toute publication.

Il faut aussi **vous assurer que le fichier CHANGELOG est à jour** dans la branche de dev avec les mises à jour de la ou les version(s) à sortir.

# Processus Git

```bash
$ git checkout master # ou git checkout beta
$ git pull
$ git merge --no-ff dev
$ vim constants.php
# Mettre à jour le numéro de version x.y.z de FRESHRSS_VERSION
$ git commit -a
Version x.y.z
$ git tag -a x.y.z
Version x.y.z
$ git push && git push --tags
```

# Mise à jour des services FreshRSS

Trois services sont à mettre à jour immédiatement après une sortie :

- update.freshrss.org (en mettant à jour [FreshRSS/update.freshrss.org](https://github.com/FreshRSS/update.freshrss.org)). Pour tester les scripts de migration, il est possible d'utiliser dev.update.freshrss.org ;
- rss.freshrss.org ;
- demo.freshrss.org (identifiants publics : `demo` / `demodemo`).

# Annoncer publiquement la sortie

Lorsque tout fonctionne, il est temps d'annoncer la sortie au monde entier !

- sur GitHub en créant [une nouvelle release](https://github.com/FreshRSS/FreshRSS/releases/new) ;
- sur le blog de freshrss.org au minimum pour les versions stables (écrire l'article sur [FreshRSS/freshrss.org](https://github.com/FreshRSS/freshrss.org)).
- sur Twitter (compte [@FreshRSS](https://twitter.com/FreshRSS)) ;
- et sur mailing@freshrss.org ;

# Lancer la prochaine version de développement

```bash
$ git checkout dev
$ vim constants.php
# Mettre à jour le numéro de version de FRESHRSS_VERSION
$ vim CHANGELOG.md
# Préparer la section pour la prochaine version
$ git add CHANGELOG.md && git commit && git push
```
