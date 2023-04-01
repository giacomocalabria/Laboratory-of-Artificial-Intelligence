# Prolog: PROgramming in LOGics

Prolog is an declarative programming language. Tu gli dici cosa vuoi e Prolog lo fa per te.

Prolog approssima la First-Order Logic FOL ed è basato sulla dimostrazione automatica dei teoremi nella FOL.

Ogni programma è un insieme di **clausole di Horn** (clausole composte da disgiunzioni di literal, con al più uno vero/positivo)

Prolog lavora con i simboli, non con i numeri

## Anatomia di un programma in Prolog

Un programma in Prolog è composto da un insieme di clausole di Horn che rappresentano:

* FATTI: su oggetti e sulle relazioni tra essi
* REGOLE: definite dagli oggetti e dalle relazioni
* OBIETTIVI: clausole senza testa, che esprimono ciò che l'utente vuole sapere o realizzare.

Definiamo una regola come segue:

```prolog
colleague(X,Y) :- work(X,Z), work(Y,Z).
```

Definiamo i fatti così:

```prolog
work(emp1, deepmind).
work(emp2, deepmind).
work(emp3, ibm).
work(emp4, ibm).
```

Definiamo invece così gli obiettivi:

```prolog
:- colleague(X,Y).
```

NOTA BENE: in Prolog ogni clausola termina con il punto `.`

### Interrogazioni a Prolog

Una volta definito la base di conoscenza nel programma, tramite fatti e regole possiamo porre interrogazioni all'ambiente Prolog

Prolog applica l'inferenza sui nuovi fatti dal programma e risponde alle interrogazioni

Esempio: vogliamo sapere se
