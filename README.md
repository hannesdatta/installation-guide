# Module: Guide for Reproducible Science and Programming Practices for Researchers

This module is based on a fork of https://pp4rs.github.io/installation-guide,
and we would like to acknowledge Lachlan Deer (`@lachlandeer`) as well as the
Department of Economics at the University of Zurich for their fantastic work
on the original repository.

```
Lachlan Deer, Adran Etter, Julian Langer & Max Winkler, 2017, Installation Guide, Programming Practices for Research in Economics, University of Zurich
```

## Meta-Information

*   Module maintainer: Hannes Datta (`@hannesdatta`)
*   Tilburg University
*   Current version of website: [https://hannesdatta.github.io/reproducible-science-guide/](https://hannesdatta.github.io/reproducible-science-guide/)

## Building the Site

We use [MkDocs]() to build the the course websites for this course.

* First, clone our repository and switch to the tilburg-update branch (the master branch is reserved for the original project).
```{.bash}
git clone https://github.com/hannesdatta/reproducible-science-guide.git
git checkout tilburg-update
```

* Install MkDocs with the following command:
```{.bash, id:"j29ie3c7"}
pip install mkdocs
```

* Install the `materials` theme for MkDocs:
```{.bash}
pip install mkdocs-material
```

* Look at a copy of the site served locally on your machine:
```{.bash, id:"j29ie3c7"}
mkdocs serve
```
* Post the site to github pages using:
```{.bash, id:"j29ie3c7"}
mkdocs gh-deploy
```

* If this is the first time you are making changes to the github pages, please fetch the gh-pages branch first.
```{.bash}
git branch -D gh-pages
git fetch origin gh-pages:gh-pages
```

## Want to Contribute?

* See the contributing guide [here](CONTRIBUTING.md).
* By contributing you agree to abide by the [Code of Conduct](CONDUCT.md)

## License

All materials are licensed under a Creative Commons CC-BY-NC-SA license. The license allows you to copy, remix and redistribute any of our publicly available materials, under the condition that you attribute the work (details in the license) and do not make profits from it. More information is available [here](LICENSE.md)

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />

This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.
