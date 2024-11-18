---
title: Data Science
---
# Python pour la Data Science

Quelques packages indispensables pour la data science :

- :numpy: [NumPy](https://numpy.org/) intègre toutes les méthodes pour le calcul scientifique.
- <img style="vertical-align: middle" src="../../../../assets/scipy.png" width="20"> [SciPy](https://scipy.org/) propose plusieurs méthodes complémentaires à NumPy.
- :pandas: [Pandas](https://pandas.pydata.org/) intègre toutes les méthodes pour le datamanagement et se place en tant que référence dans le domaine.
- <img style="vertical-align: middle" src="../../../../assets/Matplotlib_icon.png" width="20"> [Matplotlib](https://matplotlib.org/stable/index.html) permet de générer des dataviz simples (dans le style de R-ggplot2).
- <img style="vertical-align: middle" src="../../../../assets/plotly.png" width="20"> [Plotly](https://plotly.com/python/) propose des méthodes de dataviz plus avancées avec graphes interactifs.
- <img style="vertical-align: middle" src="../../../../assets/seaborn.png" width="20"> [Seaborn](https://seaborn.pydata.org/) est basé sur matplotlib et fournit une interface permettant de générer des graphiques statistiques qualitatifs.
- <img style="vertical-align: middle" src="../../../../assets/scikit-learn.png" width="20"> [Scikit-learn](https://scikit-learn.org/stable/) dispose de tous les outils nécessaires pour construire effectuer une réduction de dimension, une classification, une régression, un score, …


## Pandas : quelques commandes utiles

On commencera par importer pandas comme vu précédemment : 
```py
import pandas as pd
```

??? note "En cas d'erreur"
    Si vous avez installé une distribution modulable de python, il vous faudra d'abord installer le package pandas. Pour cela, ouvrez un terminal et utilisez la commande suivante (1):
    {.annotate}

    1. `pip` est le gestionnaire de dépendances de python. Il s'occupe d'installer et de gérer sur votre machine les packages python de votre choix.

    ```bash
    pip install pandas
    ```

Pandas permet d'exécuter énormément de traitement différent sur les données. Pour un rapide coup d'oeil je vous renvoie vers cette [cheat sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf). On couvrira ici quelques points essentiels.


- Importer des données à partir d'un fichier (1):
{.annotate}

1. `pandas` accepte une grande quantité de formats différents (csv, xlsx, json, xml, pickle, etc.) qui ont chacun leurs spécificité, au besoin se référer à la documentation.

```py
df = pd.read_csv("data.csv", sep=";")
```

- Afficher les premières/dernières lignes du dataframe (1) :
```py

df.head()
df.tail()
```

Bon voilà on a l'idée le reste est vraaaaaiiiiiment pas intéressant