# Validatore di Carte di Credito

Questo progetto è un validatore di numeri di carta di credito, realizzato per identificare le carte valide e non valide all'interno di un insieme di numeri. Utilizza l'algoritmo di Luhn per verificare la validità dei numeri di carta, e fornisce una lista delle compagnie che hanno emesso le carte non valide.

## Funzionalità del Progetto

Il codice include i seguenti componenti:

- **validateCred**: verifica se un numero di carta di credito è valido utilizzando l'algoritmo di Luhn.
- **findInvalidCards**: ricerca le carte di credito non valide in un array.
- **idInvalidCardCompanies**: restituisce un array delle compagnie che hanno emesso carte non valide, basato sul numero iniziale della carta (prima cifra).

## Descrizione delle Funzioni

### `validateCred(array)`

Questa funzione prende in input un array di cifre (numero di carta di credito) e applica l'algoritmo di Luhn per verificarne la validità. Restituisce `true` se la carta è valida e `false` altrimenti.

### `findInvalidCards(array)`

Questa funzione accetta un array di numeri di carte e utilizza `validateCred` per filtrare le carte non valide, restituendole in un nuovo array.

### `idInvalidCardCompanies(array)`

Questa funzione prende in input un array di carte non valide e identifica le compagnie emittenti in base alla prima cifra del numero di carta:
- `3`: Amex (American Express)
- `4`: Visa
- `5`: Mastercard
- `6`: Discover

Se la carta non appartiene a una di queste compagnie, la funzione stampa "Company not found". Restituisce un array delle compagnie che hanno emesso carte non valide, senza duplicati.

## Esecuzione del Progetto

1. **Clonazione del Repository**: Clona il repository nella tua macchina locale.
2. **Esecuzione del Codice**: Esegui il codice in un ambiente JavaScript, come Node.js o un browser.

   ```
   let invalidcard = findInvalidCards(batch);
   console.log(idInvalidCardCompanies(invalidcard));
   ```
3. **Risultato**: L’output mostrerà le compagnie che hanno emesso carte di credito non valide.

## Struttura del Codice
- Dati: Array batch, che contiene sia numeri di carte valide che non valide, e array valid1, invalid1, ecc., che rappresentano singoli numeri di carta.
- Funzioni: validateCred, findInvalidCards, idInvalidCardCompanies per validare e analizzare le carte di credito.

## Esempi di Utilizzo
Di seguito alcuni esempi di utilizzo delle funzioni principali:

Verifica di una carta valida:
```
console.log(validateCred(valid1)); // true se il numero è valido
```

Trovare carte non valide:
```
let invalidCards = findInvalidCards(batch);
console.log(invalidCards); // Array di carte non valide
```

Identificazione delle compagnie che hanno emesso carte non valide:
```
console.log(idInvalidCardCompanies(invalidCards)); // Compagnie emittenti carte non valide
```

## Note
Questo progetto è stato sviluppato come esercizio didattico su Codecademy, con l'obiettivo di esercitarsi nella manipolazione di array, funzioni e algoritmi di validazione in JavaScript.
