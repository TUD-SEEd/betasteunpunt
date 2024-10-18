# Hoofdstuk

## Sectie
Dit is een sectie, met een hele mooie formule:

$$ F = m\cdot a$$ (eq:Newton)

Vergelijking {eq}`eq:Newton` geeft de tweede wet van Newton weer in formule vorm.

```{figure} https://teachbooks.github.io/Showing-Physics/main/_images/FP.JPG
---
width: 80%
figclass: margin
name: fig_zijbalk
---
Een figuur in de zijbalk
```

### Subsectie

```{warning}
Verander alleen iets als je weet hoe dat moet!
```

Voeg eens een figuur toe, zoals {numref}`figuur {number} <fig_zijbalk>`

```{note}
Er kan niet zo veel mis gaan...
```

```{exercise} 
:label: ex_Alfabet

Zeg het alfabet achterste voren op.
```

```{solution} ex_Alfabet
:label: sol_Alfabet
:class: dropdown

ZYXWVU
```

```{figure} https://www.optischefenomenen.nl/cache/images/8/6/5/figuur-van-thiery-310x0-30.png
---
width: 70%
align: center
---
A figure from the internet
```

```{exercise}
:label: my-exercise

Recall that $n!$ is read as "$n$ factorial" and defined as
$n! = n \times (n - 1) \times \cdots \times 2 \times 1$.

There are functions to compute this in various modules, but let's
write our own version as an exercise.

In particular, write a function `factorial` such that `factorial(n)` returns $n!$
for any positive integer $n$.
```

````{solution} my-exercise
:label: my-solution
:class: dropdown

Here's one solution.

```{code-block} python
def factorial(n):
    k = 1
    for i in range(n):
        k = k * (i + 1)
    return k

factorial(4)
```
````