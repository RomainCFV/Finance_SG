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
