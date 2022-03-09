# Struttura di un documento HTML

La struttura di un documento HTML deve rispettare il seguente schema minimo:

```html
<!DOCTYPE html>
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
<!DOCTYPE html>
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
<!DOCTYPE html>
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

I tag permessi in questa sezione sono molteplici. Omettiamo dalla lista seguente i tag riguardanti la sezione di intestazione del documento in quanto descritti in precedenza, quelli di stile perché oggetto di una sezione apposita e quelli di scripting perché non di interessa in questo contesto.

### Basilari

| Tag           | Descrizione                           |
|---------------|---------------------------------------|
| `<h1> ~ <h6>` | Definizione delle intestazioni HTML   |
| `<p>`         | Definisce un paragrafo                |
| `<br />`      | Interruzione di riga                  |
| `<hr />`      | Inserisce una linea orizzontale       |
| `<!--...-->`  | Definisce un commento                 |


### Formattazione

| Tag           | Descrizione                               |
|---------------|-------------------------------------------|
| `<acronym>`   | Definisce un acronimo                     |
| `<abbr>`      | Definisce una abbreviazione               |
| `<address>`   | Definisce un indirizzo fisico o virtuale  |
| `<b>`         | Definisce un testo in grassetto           |
| `<bdo>`       | Definisce la direzione di un testo        |
| `<big>`       | Definisce un testo ingrandito             |
| `<blockquote>`| Definisce una citazione multilinea        |
| `<center>`    | **Deprecato** Definisce un testo centrato |
| `<cite>`      | Definisce una citazione                   |
| `<code>`      | Definisce uno snippet di codice           |
| `<del>`       | Definisce un testo cancellato             |
| `<dfn>`       | Definisce una definizione di un termine   |
| `<em>`        | Definisce un testo enfatizzato            |
| `<i>`         | Definisce un testo in corsivo             |
| `<ins>`       | Definisce un testo inserito               |
| `<kbd>`       | Definisce un testo digitato sulla tastiera|
| `<pre>`       | Definisce un testo preformattato          |
| `<q>`         | Definisce una piccola citazione           |
| `<s>`         | **Deprecato** Definisce un testo barrato  |
| `<small>`     | Definisce un testo di dimensioni ridotte  |
| `<strong>`    | Definisce un testo marcato                |
| `<sub>`       | Definisce un testo a pedice               |
| `<sup>`       | Definisce un testo in apice               |
| `<tt>`        | Definisce un testo come da telescrivente  |
| `<var>`       | Definisce una parte di testo variabile    |

### Data entry

| Tag           | Descrizione                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------|
| `<form>`      | Definisce un modulo HTML per l’inserimento da parte dell’utente                                   |
| `<input />`   | Definisce un controllo di inserimento dati                                                        |
| `<textarea>`  | Definisce un controllo di testo multilinea                                                        |
| `<button>`    | Definisce un pulsante                                                                             |
| `<select>`    | Definisce una lista di selezione (conosciuto anche con i nomi di menu a tendina e drop-down list) |
| `<optgroup>`  | Definisce un gruppo di opzioni correlate in una lista di selezione                                |
| `<option>`    | Definisce un’opzione in una lista di selezione                                                    |
| `<label>`     | Definisce un’etichetta per un elemento di input                                                   |
| `<fieldset>`  | Definisce un bordo intorno agli elementi in un modulo                                             |
| `<legend>`    | Definisce una didascalia per un elemento fieldset                                                 |


### Frames

| Tag           | Descrizione                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------|
| `<frame />`   | Definisce una finestra (un frame) in un frameset                                                  |
| `<frameset>`  | Definisce un gruppo di frames                                                                     |
| `<noframes>`  | Definisce un contenuto alternativo per quegli utenti che non supportano i frames                  |
| `<iframe>`    | Definisce un frame in linea                                                                       |

### Immagini

| Tag           | Descrizione                                           |
|---------------|-------------------------------------------------------|
| `<img />`     | Definisce una immagine                                |
| `<map>`       | Definisce una immagine-mappa                          |
| `<area />`    | Definisce un’area all’interno di una immagine-mappa   |

### Collegamenti (Ipertesti)

| Tag           | Descrizione                                                   |
|---------------|---------------------------------------------------------------|
| `<a>`         | Definisce un’àncora                                           |
| `<link />`    | Definisce la relazione tra il documento ed una risorsa esterna|

### Liste

| Tag           | Descrizione                                                           |
|---------------|-----------------------------------------------------------------------|
| `<ul>`        | Definisce una lista non ordinata                                      |
| `<ol>`        | Definisce una lista ordinata                                          |
| `<li>`        | Definisce un oggetto della lista                                      |
| `<dl>`        | Definisce una lista di definizioni                                    |
| `<dt>`        | Definisce un termine (un oggetto) in una lista di definizioni         |
| `<dd>`        | Definisce la descrizione di un termine in una lista di definizioni    |

### Tabelle

| Tag           | Descrizione                                                           |
|---------------|-----------------------------------------------------------------------|
| `<table>`     | Definisce una tabella                                                 |
| `<caption>`   | Definisce una didascalia per la tabella                               |
| `<th>`        | Definisce l’intestazione di cella in una tabella                      |
| `<tr>`        | Definisce la riga di una tabella                                      |
| `<td>`        | Definisce la cella di una tabella                                     |
| `<thead>`     | Raggruppa il contenuto delle intestazioni in una tabella              |
| `<tbody>`     | Raggruppa il contenuto del corpo in una tabella                       |
| `<tfoot>`     | Raggruppa il contenuto del piè di pagina in una tabella               |
| `<col />`     | Definisce i valori di attributo per una o più colonne in una tabella  |
| `<colgroup>`  | Definisce un gruppo di colonne in una tabella per la formattazione    |
