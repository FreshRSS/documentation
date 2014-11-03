[English version](README.md)

# Documentation de FreshRSS

Ce dépôt contient le code source de la documentation de FreshRSS. Si vous souhaitez simplement la consulter, veuillez vous rendre sur [doc.freshrss.org](http://doc.freshrss.org).

## Comment contribuer ?

La documentation de FreshRSS est aujourd'hui encore trop incomplète. Nous avons besoin d'aide pour la compléter. Si vous souhaitez aider, les points suivants donnent quelques indications sur comment procéder. Si vous souhaitez savoir comment tout ça fonctionne, veuillez vous référer à la partie « Comment ça fonctionne ? ».

1. Faites [un fork du projet sur Github](https://github.com/FreshRSS/documentation).
2. Récupérez votre dépôt sur votre ordinateur ou faites les modifications directement sur Github.
3. Le répertoire  ```./fr``` contient la documentation en français.
4. La documentation est écrite en Markdown. La syntaxe est assez intuitive et ne pose généralement pas de problème. Quelques indications [sont données sur Github](https://guides.github.com/features/mastering-markdown/).
5. Faites ensuite une "pull request" sur le dépôt officiel.
6. Vous n'avez rien d'autre à faire ! Vos améliorations seront probablement discutées puis acceptées. Ensuite, [doc.freshrss.org](http://doc.freshrss.org) sera mis à jour.

## Traduire la documentation.

Aujourd'hui, la documentation est écrite principalement en français pour des raisons pratiques. Nous cherchons des personnes prêtes à traduire la documentation vers l'anglais (et éventuellement d'autres langues !). Si vous souhaitez participer, n'hésitez pas à vous manifester sur Github. La démarche est la même que celle décrite dans la partie précédente sauf que vous devrez probablement rédiger dans le répertoire ```./en``` pour l'anglais, ```./es``` pour l'espagnol, etc.

## Comment ça fonctionne ?

La documentation de FreshRSS utilise [Daux.io](http://daux.io/) pour être générée. L'écriture de cette documentation passe par 3 étapes :

1. La documentation est écrite en Markdown [sur Github](https://github.com/FreshRSS/documentation).
2. Le dépôt est récupéré régulièrement dans une installation de Daux.io sur [doc.freshrss.org](http://doc.freshrss.org).
3. La documentation est générée en HTML automatiquement par le serveur.

Si vous souhaitez voir le résultat directement en local, vous devez [installer Daux.io](https://github.com/justinwalsh/daux.io) chez vous et cloner la documentation du dépôt [FreshRSS/documentation](https://github.com/FreshRSS/documentation) dans ```./daux.io/documentation```. Le fichier ```./daux.io/global.json``` doit être paramétré de la façon suivante :

```json
{
    "docs_directory": "documentation",
    "valid_markdown_extensions": ["md", "markdown"]
}
```
