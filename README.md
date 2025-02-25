# Finance SG

## Exercice 1: Calcul du payoff d'un put

**Put :** Droit de vente d'une action à une certain date d'expiration

**Calculer le payoff d'un put avec :**
- $K$ : le Strike (prix d'exercice)
- $S_t$ : prix du sous-jacent à un moment $t$

**Formule pour le payoff d'un put :**

$Payoff = max(0, K - S_t)$

Graphe :

Conclusion :
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

Graphe :

Conclusion :
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
