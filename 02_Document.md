# Struttura di un documento HTML

La struttura di un documento HTML deve rispettare il seguente schema minimo:

```html
<html lang="it">
    <head>
        <!-- Intestazione del documento -->
    </head>
    <body>
        <!-- Corpo del documento -->
    </body>
</html>
```

_Nota_: diamo per assunto il riferimento allo standard HTML5, ignorando versioni precedenti come HTML4 o HTML4 Transitional in quanto obsoleti

## Nodo radice

Il nodo radice è sempre un tag nel formato `<html lang="...">`, e contiene l'intero documento. Ogni documento ha una ed una sola radice.

## Intestazione del documento

Il tag `<head>` è unico all'interno del documento e deve essere il primo figlio di `<html>`. Contiene informazioni di base sul documento, come ad esempio il titolo, utilizzato dai renderer (eg: browsers) per decorare il tab della pagina che contiene il documento stesso.

```html
<html lang="it">
    <head>
        <title>Il mio documento</title>
    </head>
    <body>
        <!-- Corpo del documento -->
    </body>
</html>
```

Contiene altre informazioni come i riferimenti alle icone del documento, il set di caratteri utilizzato, la descrizione per i motori di ricerca, regole di gestione del viewport, stili importati e altro. Vedremo nel dettaglio alcuni di questi elementi.

Esempio (notare i tag come `meta` e `link` sono _self closing_ mentre non lo è il tag `title`)

```html
<html lang="it">
    <head>
        <meta charset="UTF-8">
        <title>What’s The Frequency, Kenneth? - Remix · R.E.M.</title>
        <meta name="description" content="Listen on Spotify: R.E.M.'s greatest hits and most popular tracks on Spotify right now including Losing My Religion, Everybody Hurts, Shiny Happy People, Man On The Moon &amp;amp; more!">
        <meta property="googlebot" content="notranslate">
        <link rel="icon" sizes="16x16" type="image/png" href="https://open.scdn.co/cdn/images/favicon16.c498a969.png">
    </head>
    <body>
        <!-- Corpo del documento -->
    </body>
</html>
```

Alcuni di questi tag sono utilizzati direttamente dal browser, altri sono custom e utilizzati in altre situazioni. Ad esempio:

```html
<meta property="googlebot" content="notranslate">
```

Questo elemento viene parsato dal crawler di Google e serve ad informare l'indexer di registrare questo documento come un documento da non tradurre (non verrà proposto il link di traduzione nella pagina dei risultati di ricerca di Google).

## Corpo del documento

Il tag `body` rappresenta il corpo del documento, tipicamente quello che contiene contenuto renderizzabile da un agent come un browser (o un client email).

