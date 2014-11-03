[Version française](README.fr.md)

# FreshRSS documentation

This repository contains FreshRSS documentation source code. If you only need to browse the documentation, browse [doc.freshrss.org](http://doc.freshrss.org).

## How-to contribute?

At the moment, FreshRSS documentation is far from being complete. We need all the help we can get to fill the blanks. If you are willing to contribute, this document provide basic directions to do it. If you want to know how all of this works, please refer to the "How it works?" section.

1. [Fork the Github project](https://github.com/FreshRSS/documentation).
2. Pull your fork on your computer or modify it directly on Github.
3. The French documentation is located in the ```./fr``` folder.
4. The documentation use Markdown syntax. This syntax is pretty straightforward. If you need some guidance, read the [Github guide to Markdown](https://guides.github.com/features/mastering-markdown/).
5. Make a "pull request" on the official repository.
6. You are done! Your changes will go through a team review then merged. Then, we will update [doc.freshrss.org](http://doc.freshrss.org).

## Translate the documentation.

At the moment, the documentation is available in French for practical reasons. We are looking for people willing to translate it to English (or other languages). Please contact us on Github if you want to contribute. The process is identical to the later process except you will need to write the documentation in its own language folder, ```./en``` for English, ```./es``` for Spanish, etc.

## How it works?

FreshRSS documentation is generated with [Daux.io](http://daux.io/). The writing process follows 3 simple steps:

1. Writing the documentation in Markdown [on Github](https://github.com/FreshRSS/documentation).
2. Pulling the documentation source code on [doc.freshrss.org](http://doc.freshrss.org) where Daux.io is installed.
3. Generating the HTML documentation automatically with the Daux.io instance.

If you want to browse the result locally, you need to [install Daux.io](https://github.com/justinwalsh/daux.io) on your computer and clone [FreshRSS/documentation](https://github.com/FreshRSS/documentation) repository in ```./daux.io/documentation``` folder. You need to configure the ```./daux.io/global.json``` file with the following values:

```json
{
    "docs_directory": "documentation",
    "valid_markdown_extensions": ["md", "markdown"]
}
```