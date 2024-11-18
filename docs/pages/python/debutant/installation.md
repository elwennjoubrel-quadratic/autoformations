---
title: Installation
---
# Installation

Pour programmer en Python, on n'a besoin que de deux éléments : un interpréteur Python, et un environnement de développement.

## Interpréteur Python

On pourrait utiliser divers interpréteurs, mais l'on abordera ici la verison la plus simple.

=== "Windows"
    Installer [Python depuis python.org](https://www.python.org/downloads/windows/).

    > Si vous n'avez pas les droits administrateurs, il est également possible de télécharger Python depuis le Microsoft Store ou, le cas échéant, le store d'entreprise de votre organisation.

=== "macOS"
    macOS ne supporte pas l'installation de Python depuis python.org. Il est donc nécessaire d'installer un gestionnaire de paquets, [Homebrew](https://brew.sh/). Une fois Homebrew installé, il suffit d'exécuter la commande `brew install python` dans un terminal.

=== "Linux"
    Si vous avez besoin d'informations pour installer Python sous Linux, passez sous Windows.

Pour vérifer que Python a bien été insallé, ouvrez un terminal et lancez la commande suivante :
```bash
python3 --version
```

??? note "Autres options"
    Si vous n'utilisez Python que pour la Data Science, vous pouvez également regarder du côté d'[Anaconda](https://www.anaconda.com/download). Cette distribution permet d'installer facilement de nombreuses librairies utiles pour la Data Science, mais peut pêcher en simplicité et en légèreté hors de ce cadre.


## IDE (environnement de développement)

Il existe de nombreux environnements de développement pour Python. Toujours dans une optique de versatilité, on se tourne ici vers Visual Studio Code.

VSCode est un éditeur de texte gratuit et open-source développé par Microsoft qui supporte, en plus de Python, de très nombreux langages (1). Il est très populaire dans la communauté des développeurs, en raison de sa flexibilité, de sa vitesse et de sa richesse en extensions. Il est également très bien supporté par la communauté Python, avec de nombreuses extensions disponibles pour faciliter le développement en Python.
{.annotate}

1. On parle ici de plus de 30 langages parmis les plus courants (Python, C, C++, Java, HTML, JavaScript, etc.) et les langages de DataScience usuels (SAS, R).

Pour installer Visual Studio Code, rendez-vous sur la [page de téléchargement](https://code.visualstudio.com/download) et suivez les instructions d'installation.


### Extensions VSCode

Il est possible d'installer des extensions pour Visual Studio Code afin d'ajouter des fonctionnalités, comme par exemple l'intégration de Git, la possibilité de déboguer du code, de visualiser des jeux de données, de lire de très nombreux types de fichiers (images, pdf, csv, etc.)


### VSCode pour Python

Dans le cadre de ce cours, on se contentera de l'extension Python pour Visual Studio Code, qui permet d'exécuter du code Python directement depuis l'éditeur, et de bénéficier de l'autocomplétion et de la coloration syntaxique.

Pour l'installer, ouvrez Visual Studio Code, puis cliquez sur l'icône d'extensions dans la barre latérale gauche. Dans la barre de recherche, tapez `Python` et installez l'extension `Python` de Microsoft.


### Projet VSCode

Pour créer un projet Python, il suffit de créer un dossier, puis d'ouvrir ce dossier avec Visual Studio Code. Il est possible de créer un fichier `.py` à la racine du dossier, qui sera le point d'entrée de votre projet. Il est également possible de créer un fichier `.ipynb` à la racine du dossier, qui sera un notebook Jupyter. Ce fichier peut être ouvert directement dans Visual Studio Code, ou dans Jupyter Lab. Pour ouvrir un notebook Jupyter dans Visual Studio Code, il suffit de cliquer sur le bouton `Open with Jupyter` dans la barre d'outils du fichier. Pour ouvrir un notebook Jupyter dans Jupyter Lab, il suffit de lancer la commande `jupyter lab` dans un terminal, puis de cliquer sur le fichier dans l'interface de Jupyter Lab.