---
title: Opérateurs
---
# Opérateurs et algorithmie

## Opérateurs de base

### Opérateurs d'affectation

|  Opérateur |      Exemple      |     Equivalent à     |                                                     Description                                                    |    Output    |
|:----------:|:-----------------:|:--------------------:|:------------------------------------------------------------------------------------------------------------------:|:------------:|
|      `=`     |        `x = 7`        |                |                                              Affecte $7$ à la variable $x$                                             |       7      |
|     `+=`     |        `x += 2`      |      `x = x+2`  |                                        Affecte la valeur $x+2$ à la variable $x$                                       |       9      |
|     `-=`     |        `x -= 2`       |     `x = x-2`  |                                        Affecte la valeur $x-2$ à la variable $x$                                       |       5      |
|     `/=`     |        `x /= 2`       |   `x = x/2`    |                                        Affecte la valeur $x/2$ à la variable $x$                                       |      3.5     |
|     `%=`     |        `x %= 2`       |   `x = x%2`    |                      Affecte la valeur $x%$ (reste de la division euclidienne) à la variable $x$                      |       1      |
|     `//=`    |       `x //= 2`       |   `x = x//2`    |                    Affecte la valeur $x//2$ (quotient de la division euclidienne) à la variable $x$                    |       3      |
|     `**=`    |       `x **= 2`       |    `x = x**2`  |                                        Affecte $x^2$ à la variable $x$                                        |      49      |
|      `&=`    |      `C &= C2`    |      `C = C & C2`    |                    Affecte à la variable $C$ la valeur $True$ si $C$ et $C2$ valent $True$, $False$ sinon                  |     False    |
|     `\|=`    |     `C \|= C2`    |     `C = C \| C2`    |          Affecte à la variable $C$ la valeur True si   l’une des 2 variables $C$ ou $C2$ vaut $True$,   $False$ sinon        |      True    |
|     `^=`     |      `C ^= C2`    |      `C = C ^ C2`    |     Affecte à la variable $C$ la valeur True si   $C\|C2$ est $True$ ET $C\&C2$ est $False$   (OU exclusif), $False$ sinon    |      True    |


## Opérateurs de comparaison
| Opérateur | Exemple | Description | Output |
|:---------:|:-------:|:-----------:|:------:|
|     `==`    |  `x==7`   |    Égal     |  True  |
|     `!=`    |  `x!=7`   |   Différent |  False  |
|     `< `    |  `x<8`    |   Inférieur |  True  |
|     `> `    |  `x>7`    |   Supérieur | False  |
|     `<=`    |  `x<=7`   | Inférieur ou égal |  True  |
|     `>=`    |  `x>=9`   | Supérieur ou égal | False  |
|     `in`    |  `x in [3, 'pomme', True, 7]` |   Appartenance à une liste | True |
|    `not`    |  `not x`   |   Négation   | False |
| `and` | `x<10 and x>3`   |   ET logique | True |
| `or`  | `x<10 or x>3`    |   OU logique | True |

## Algorithmie 

### Expressions conditionnelles

- Simple bloc `if-then`

=== "Idée"
    <div class="grid" markdown>

    ```py
    if <condition>:
        <expression>
    ```

    Le bloc `<expression>` est exécuté si la condition `<condition>` est `True`.
    {.card}

    </div>

=== "Exemple"
    <div class="grid" markdown>

    ```py
    x = 3
    if x > 0:
        print('Hello World!')

    >>> Hello World!
    ```

    Puisque 3 est supérieur à 0, la condition est vraie et le bloc `print('Hello World!')` est exécuté.
    {.card}

    </div>

- Bloc `if-then-else`
=== "Idée"
    <div class="grid" markdown>

    ```py
    if <condition>:
        <expression_if>
    else:
        <expression_else>
    ```

    Si `<condition>` est `True`, le bloc `<expression_if>` est exécuté, sinon le bloc `<expression_else>` est exécuté.
    {.card}

    </div>

=== "Exemple"
    <div class="grid" markdown>

    ```py
    x = 3
    if x <= 0:
        print('x is negative')
    else:
        print('x is positive')

    >>> x is positive
    ```

    Puisque `x`est supérieur à 0, la condition est fausse et le bloc `print('x is positive')` est exécuté.
    {.card}

    </div>

- Bloc `if-then-elif-then-else`
=== "Idée"
    <div class="grid" markdown>

    ```py
    if <condition_if>:
        <expression_if>
    elif <condition_elif>:
        <expression_elif>
    else:
        <expression_else>
    ```

    Si `<condition_if>` est `True`, le bloc `<expression_if>` est exécuté, sinon si `<condition_elif>` est `True`, le bloc `<expression_elif>` est exécuté, sinon le bloc `<expression_else>` est exécuté.
    {.card}

    </div>

=== "Exemple"
    <div class="grid" markdown>

    ```py
    x = 3
    if x < 0:
        print('x is negative')
    elif x == 0:
        print('x is zero')
    else:
        print('x is positive')

    >>> x is positive
    ```

    Puisque `x` est strictement supérieur à 0, les conditions `< 0` et `== 0` sont fausses et le bloc `print('x is positive')` est exécuté.
    {.card}

    </div>


### Boucles

Contrairement à d’autres langages, les boucles sont assez performantes en Python. Même s’il ne faut pas en abuser, leur utilisation est très simple et ne provoque normalement pas de lenteur lors de l’exécution comme il est souvent le cas en R.

!!! warning "Attention"
    En Python, le premier index est 0.

- Boucle `for`

=== "Parcours par index"
    <div class="grid" markdown>

    ```py
    names = ['Alice', 'Bob', 'Charles']
    for i in range(len(names)):  # (1)
        print(f'Hello {names[i]}!')  # (2)
    
    >>> Hello Alice!
    >>> Hello Bob!
    >>> Hello Charles!
    ```

    1. <ul><li>La fonction `range(n)` génère la suite d'entiers naturels $0,1, ..., n-1$.</li><li>La fonction `len(list)` renvoie la longueur de la liste.</li></ul>
    2. *`f-string`* : permet d'insérer des variables dans une chaîne de caractères. La syntaxe est `f'chaîne de caractères {variable}'`.

    La boucle `for` itère sur la variable `i` qui prendra les valeurs générées par `range` et exécutera le bloc d'instructions pour chaque valeur de `i`.
    {.card}

    </div>

=== "Parcours par élément"
    <div class="grid" markdown>
    
    ```py
    names = ['Alice', 'Bob', 'Charles']
    for name in names:
        print(f'Hello {name}!')
    ```

    La boucle `for` itère sur directement sur les valeurs de la liste `names` et exécutera le bloc d'instructions pour chaque valeur de `name`.
    {.card}

    </div>


- Boucle `while`

=== "Idée"
    <div class="grid" markdown>

    ```py
    while <condition>:
        <expression>
    ```

    La boucle `while` permet d'éxecuter une instruction tant que la condition est `True`.
    {.card}

    </div>

=== "Exemple"
    <div class="grid" markdown>

    ```py
    k, stop = 2, 5
    while k < stop:
        print(f"Le carré de {k} vaut {k**2}.")
        k += 1

    >>> Le carré de 2 vaut 4
    >>> Le carré de 3 vaut 9
    >>> Le carré de 4 vaut 16
    ```

    La boucle `while` itère tant que `k` est inférieur à `stop` et exécutera le bloc d'instructions pour chaque valeur de `k`.
    {.card}

    </div>

!!! warning "Attention"
    La boucle while continuera à tourner tant que la condition sera vérifiée, il faut donc faire attention à ce que le bloc définisse une action qui mettra fin à la véracité de la condition (1).
    {.annotate}
    
    1. Dans l'exemple ci-dessus, `k` est incrémenté de 1 à chaque tour de boucle, ce qui permet de sortir de la boucle lorsque `k` est égal à `stop`.