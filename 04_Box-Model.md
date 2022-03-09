# Box Model

## Cosa è una box?

Tutto in CSS ha una casella attorno e la comprensione di queste caselle è la chiave per poter creare layout con CSS o per allineare elementi con altri elementi.

Una box è composta da:

- Il suo contenuto
- Il **riempimento**, o `padding`, cioè lo spazio sulle due assi tra il contenuto ed il bordo.
- Il **bordo** (`border`) che circonda il contenuto
- Il **margine esterno** (`margin`) che è la distanza sulle due assi dal contenitore esterno o dai siblings di un elemento.

Tutti questi elementi contribuiscono alla dimensione della box. Come la box si comporta in relazione al suo esterno è definito dalla proprietà `display`.

## Display

In CSS abbiamo sostanzialmente due tipi principali di box: block box e inline box. Queste caratteristiche si riferiscono a come si comporta il box in termini di flusso della pagina e in relazione ad altri box nella pagina. Le box hanno anche un tipo di visualizzazione interna e un tipo di visualizzazione esterna. Per prima cosa, spiegheremo cosa intendiamo per block box e inline box. Spiegheremo quindi cosa si intende per tipo di visualizzazione interna ed esterna.

Se una box ha un tipo di visualizzazione block si comporterà nei seguenti modi:

- La casella si interromperà su una nuova riga.
- La scatola si estenderà nella direzione inline per riempire lo spazio disponibile nel suo contenitore. Nella maggior parte dei casi ciò significa che l'elemento diventerà largo quanto il suo contenitore, riempiendo il 100% dello spazio disponibile.
- Le proprietà `width` e `height` sono rispettate.
- Il riempimento, il margine e il bordo faranno sì che altri elementi vengano allontanati dalla scatola

Alcuni elementi HTML, come `<h1>` e `<p>`, utilizzano block come tipo di visualizzazione esterno per impostazione predefinita.

Se una box ha un tipo di visualizzazione esterno inline, allora:

- La casella non si interromperà su una nuova riga.
- Le proprietà `width` e `height` non verranno applicate.
- La spaziatura interna verticale, i margini e i bordi verranno applicati ma non causeranno l'allontanamento di altre caselle inline dalla casella.
- La spaziatura interna, i margini e i bordi orizzontali verranno applicati e le altre caselle in linea si allontaneranno dalla casella.

Il tipo di box applicato a un elemento è definito dalla proprietà css `display` e si riferisce al display esterno.

Esistono altri valori possibili per `display`, come inline-block, flex, inline-flex ecc.
