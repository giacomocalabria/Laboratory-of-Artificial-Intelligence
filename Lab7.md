Consideriamo ancora l'esempio della rete bayesiana che gestisce lo spruzzino, assumiamo che quella è una descrizione realistica della relazione causale tra le quattro variabili.

Vogliamo stimare il *causal effects* sulla pioggia e sull'erba bagnata

Non possiamo modificare fisicamente la variabile *R* associata alla pioggia. Tuttavia possiamo usare le probabilità dai dati osservati del meteo per elaborare il vincolo causa-effetto "as if"

To this end, we can compute the effect of the intervention

$$
P(G=\text {true}|do(R=\text{true}))
$$

or simply $P(g|do(r))$, by using the adjustment formula for the only parent of $R$, which is $C$

We want to estimate the **causal effects** of the rain on the "wetness" of the grass.

$$
    P(g|do(r)) = \sum_{z\in C}{P(g|z,r)P(z))}=P(g|c,r)P(c)+P(g|r,!c)P(!c)
$$

The probability distribution is already given by the network.