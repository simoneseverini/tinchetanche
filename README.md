# tinchetanche — versione minimale

Un sito di lettura essenziale, in italiano e in inglese, per GitHub Pages.
Niente database, piattaforme esterne o abbonamenti.

## Come pubblicare un nuovo articolo

Scegli **Add file → Create new file** e chiama il file, per esempio:

`_posts/2026-10-17-il-primo-articolo.md`

Incolla questo modello e sostituisci titolo, data, categoria e testo:

```markdown
---
title: "Il titolo del primo articolo"
date: 2026-10-17
lang: it
categoria: Idee
---

Qui comincia il primo paragrafo.

Qui il secondo. Si può usare *corsivo*, **grassetto** e [un link](https://example.org).

## Un sottotitolo

Un altro paragrafo.
```

Poi fai **Commit changes**. L'articolo compare nella homepage all'inizio del flusso, in ordine di data, e ha anche un URL permanente. Per un testo in inglese, usa `lang: en`; per la categoria si può scrivere `Storie`, `Opinioni`, `Idee`, o lasciarla via.

**Importante:** il nome del file deve iniziare con una data (`AAAA-MM-GG-...md`). La data del file e quella nel blocco iniziale devono corrispondere. Per un articolo già pubblicato, modifica il file Markdown esistente senza crearne un secondo.

## Come funziona lo scorrimento infinito

Gli articoli sono ordinati dal più recente al più vecchio. La pagina ne mostra quattro; avvicinandosi al fondo, ne rivela altri quattro automaticamente, senza pulsanti. Se JavaScript è disattivato, rimangono comunque tutti leggibili. Questa prima versione carica il testo completo della pagina; quando il numero di articoli sarà molto elevato, potremo aggiungere il caricamento a pagine senza cambiare il modo in cui si scrivono i post.

## Struttura

- `index.html`: homepage e scorrimento.
- `style.css`: tipografia e aspetto grafico.
- `_config.yml`: configurazione Jekyll.
- `_layouts/post.html`: pagina dedicata a ogni singolo articolo.
- `_posts/`: un file Markdown per ogni testo.
- `CNAME`: collegamento al dominio personalizzato.

## Nota importante

L'archivio **non è stato caricato automaticamente su GitHub**. Il sito esistente resterà com'è fino a quando non eseguirai il commit. Se le impostazioni GitHub Pages usano un'azione personalizzata che pubblica file HTML statici senza eseguire Jekyll, sarà necessario configurare una build Jekyll (o passare a «Deploy from a branch»).
