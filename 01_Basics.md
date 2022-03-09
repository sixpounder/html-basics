# HTML

HTML sta per **HyperText Markup Language**. Non è un linguaggio di programmazione, è un linguaggio di strutturazione e descrizione di un documento, subset di **XML**.

## Definizioni ed elementi di base

### Tag

La struttura di un documento html è gerarchica e basata su singoli elementi chiamati **tag**.

Un tag è un singolo elemento formato come segue

```html
<tag-name attr1="value1" attr2="value2">
    Contenuto del tag
</tag-name>
```

dove:

- `tag-name` è l'identificativo del tag. HTML supporta un set definito di tags, ognuno con un proprio significato semantico.

- Ogni tag può avere da `0` a `n` attributi associati, specificati dopo `tag-name` ma prima del simbolo `>` che ne delimita il contenuto, nella forma `attribute_name="attribute_value"` e seprati da spazio l'uno dall'altro.

- Il contenuto del tag può essere testo semplice (detto anche *text node*), un altro tag, un altra serie di tag oppure una combinazione delle precedenti.

- La parte di chiusura `</tag-name>` non supporta attributi, ed è un errore formale aggiungerne in questa sede.

La struttura gerarchica deve sempre essere rispettata, è un errore formale ad esempio chiudere un tag dopo la chiusura di un tag figlio.

### Eccezioni

Alcuni tag, specialmente nella sezione di intestazione del documento, fanno eccezione al formato `<tag></tag>`, e vanno specificati in un formato detto _self closing_. Esempio nella prossima sezione.

Alcuni tag come ad esempio `<input>` sono _auto closing_, in quanto non permettono contenuto al loro interno ma solo attributi. Questi tag sono utilizzati nel formato seguente:

```html
<input attr="..." attr2="..." />
```

### Esempio

Un esempio di documento gerarchicamente non valido:

```html
<article>
    <h1>
        Intestazione
    </article> <!-- Chiusura di div quando h1 non è ancora chiuso-->

    <p>
        Paragrafo articolo
    </p>

    <p>
        Paragrafo articolo
    </p>
</h1>
```

Un esempio di documento gerarchicamente valido:

```html
<article>
    <h1>
        Intestazione
    </h1>

    <p>
        Paragrafo articolo
    </p>

    <p>
        Paragrafo articolo
    </p>
</article>
```
