---
title: Fonctions
---
# Fonctions, packages et modules

## Fonctions

Une fonction est une portion de code qui effectue une tâche spécifique définie par l'utilisateur. Elle peut prendre des paramètres en entrée et renvoyer un résultat en sortie. Les fonctions permettent de structurer le code, de le rendre plus lisible et plus modulaire.
{.card}

```py
def <function_name>(<arg1>, <arg2>, ...):
    <instructions>
    return <output>
```

Exemple d'utilisation : compter le nombre de valeurs impaires dans une liste.
En définissant cette fonction pour l'appeler plus tard on gagne en lisibilité, et on peut réutiliser cette fonction pour d'autres listes sans avoir à réécrire le code.
{.card}

```py
def count_odd_numbers(numbers):
    count = 0
    for number in numbers:
        if number % 2 == 1:
            count += 1
    return count

print(count_odd_numbers[1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

>>> 5
```

## Packages et modules

Un package python est un répertoire contenant une collection de modules. Un module peut être vu comme un sous-package. Chaque module contient des méthodes associées qui ne sont applicables que pour des objets appartenant à la classe du module.

!!! example "Exemple"
    Dans le package `datetime`, on trouve notamment le module `date` qui définit une fonction `today()` qui renvoie la date du jour. On peut donc écrire :
    ```py
    import datetime
    print(datetime.date.today())

    >>> 2024-10-02
    ```

    Il va de soi que l'appel de la fonction `today()` sans référence à `datetime` n'aboutit pas, vous obtiendrez une `NameError`.


### Différentes méthodes d'import

Il existe plusieurs façons d'importer des modules ou des packages en Python. Reprenons le même exemple :

=== "Package"
    ```py
    import datetime
    print(datetime.date.today())

    >>> 2024-10-02
    ```

=== "Package avec alias"
    ```py
    import datetime as dt
    print(dt.date.today())

    >>> 2024-10-02
    ```

=== "Module"
    ```py
    from datetime import date
    print(date.today())

    >>> 2024-10-02
    ```

=== "Fonction"
    ```py
    from datetime.date import today
    print(today())

    >>> 2024-10-02
    ```

=== "Tous les modules (à éviter)"
    ```py
    from datetime import *
    print(date.today())

    >>> 2024-10-02
    ```

De cette manière, on peut être aussi fin que possible dans les imports, éviter de surcharger le code d'imports inutiles, et nommer nos packages et modules comme on le souhaite.

??? tip "Bonne pratique"
    On évitera d'user des alias à outrance et on priviliégiera les alias les plus clairs possibles, ou admis par la communauté. Par exemple, on utilisera `np` pour `numpy`, `pd` pour `pandas`, `plt` pour `matplotlib.pyplot`, etc.