# Finance SG

## Exercice 1: Calcul du payoff d'un put

**Put :** Droit de vente d'une action à une certain date d'expiration

**Calculer le payoff d'un put avec :**
- $K$ : le Strike (prix d'exercice)
- $S_t$ : prix du sous-jacent à un moment $t$

**Formule pour le payoff d'un put :**

$Payoff = max(0, K - S_t)$

**Graphe :**

Avec $K = 5$

![Figure_1](https://github.com/user-attachments/assets/0f969978-0d7c-4004-ad93-43eddde834bb)

**Conclusion :**
- Payoff maximale lorsque $S_t=0$ => Payoff maximale de valeur K
- Payoff linéaire descendant lorsque $0<S_t<K$
- Payoff de 0 lorsque $S_t>= K$

## Exercice 2: Calcul du payoff d'un put spread

**Put spread :** Achat d'un put puis vente 

**Calculer le payoff d'un put spread avec :**
- $K_1$ : le prix d'exercice d'achat du put
- $K_2$ : le prix d'exercice de vente du put
- $S_t$ : prix du sous-jacent à un moment $t$

**Formule pour le payoff d'un put spread :**

$Payoff = max(0, K_1 - S_t) - max(0, K_2 - S_t)$

**Graphe :**

Avec $K_1 = 6$ et $K_2 = 2$

![Figure_2](https://github.com/user-attachments/assets/9753cc7b-bddf-4a9a-b879-811ad07bb0e5)

**Conclusion :**
- Lorsque $S_t \leq K_2$, le payoff est: $K_1-K_2$
- Lorsque $K_2<S_t<K_1$, le payoff est: $K_1-S_t$
- Lorsque $S_t \geq K_1$, le payoff est 0

## Exercice 3: Calcul du taux de change Forward

**Taux Forward :** Taux déterminé à aujourd'hui pour faire un investissement plus tard

Appliqué dans l'exercice : **L'hypothèse d'Absence d'Opportunité d'Arbitage (AOA)**

**AOA :** stipule qu’il n’est pas possible d’élaborer une stratégie financière qui, à partir d’un coût d’investissement initial nul, assure un gain dans une date future.

**Implications :** Investir sur 2 ans revient à la même chose qu'en divisant les investissements sur plusieurs périodes (par exemple: investir 1 an puis une autre année à une date ultérieure)

**2 taux d'intérêts :**
- $S_1 = 0,04$ (4%), le taux d'intêret d'emprunt sur 1 an
- $S_2 = 0,05$ (5%), le taux d'intêret d'emprunt sur 2 ans

**Trouver le taux $f$, le taux lorsqu'on emprunte 1 an puis 1 an**

**Le taux sur 2 ans :**

$(1 + S_2)^2$

**D'après l'AOA :**

$(1 + S_2)^2 = (1 + S_1) * (1 + f)$

**En simplifiant :**

$f = \frac{(1 + S_2)^2}{(1 + S_1)} - 1$

$f \approx 0,06$

# Python

## Exercice 1

**Enoncé :** Ecrire une fonction qui prend en paramètre une liste, et retourner une liste avec les valeurs doublées

**Solution :**
```python
def list_double(l):
    return [x*2 for x in l]
```

## Exercice 2
**Enoncé :** Ecrire une fonction qui prend une chaine de caractères et qui retourne la chaine de caractères à l'envers

**Solutions :**

Sans boucle :
```python
def reverse_str(str):
    return str[::-1]
```

Avec boucle :
```python
def reverse_str(str):
  rev_str = ""
  for i in range(len(str) - 1, -1, -1):
      rev_str += str[i]
  return rev_str
```

## Exercice 3
**Enoncé :** Ecrire une fonction qui prend 2 chaines de caractères (s1 et s2), et qui retourne le nombre de fois que la chaine s2 apparait dans s1

**Solution :**

Sans boucle :
```python
def occurrences_substr(s1, s2):
    return s1.count(s2)
```

Avec boucle :
```python
def occurrences_substr(s1, s2):
    len_s1 = len(s1)
    len_s2 = len(s2)
    if len_s2 > len_s1:
        return 0
    occurrence = 0
    for i in range(0, len_s1 - len_s2 + 1):
        substr = s1[i: i + len_s2]
        if substr == s2:
            occurrence += 1
    return occurrence
```
