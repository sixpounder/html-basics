# Stili

Un documento HTML può essere stilizzato tramite CSS (Cascading Style Sheet) oppure tramite attributi `style` associati ai tag che si vuole stilizzare.

I CSS possono essere sia file singoli scaricati da un server ed applicati al documento tramite un tag `link` nell'intestazione del documento oppure possono essere inseriti _inline_ nel documento stesso tramite un tag `style` sempre nell'intestazione.

Nelle email di solito si utilizza la seconda opzione, dal momento che la quasi totalità degli agents non permette richieste HTTP in fase di rendering di un documento per ragioni di sicurezza.

Gli agents hanno di solito un set predefinito di regole per il rendering di alcuni tag come `<i>`, `<b>`, `<h1>`, `<h2>` e così via, ma è la norma personalizzare questi aspetti tramite CSS o style attributes.

## Quando utilizzare CSS e quando style attributes?

Quasi sempre la scelta giusta è utilizzare il linguaggio CSS, molto più leggibile, manutenibile e facilmente modificabile. Gli style attributes hanno senso in alcune situazioni che però esulano dallo scope di questa introduzione (eg. creazione di componenti dinamici javascript).
