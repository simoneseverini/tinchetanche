# Inutili Press — istruzioni

Il sito ha lo **stesso stile minimale di Tinchetanche**. Gli elementi del catalogo si generano automaticamente dai file Markdown nella cartella `_books`.

## Pubblicazione iniziale su GitHub

1. Crea un nuovo repository pubblico, per esempio `simoneseverini/inutilipress` (se già esiste, usa quello). **Non** caricare questi file nel repository di Tinchetanche.
2. Estrai lo ZIP e carica nella radice del nuovo repository **tutti i file e le cartelle**: `index.html`, `style.css`, `_config.yml`, `CNAME`, `_books/` e questo `LEGGIMI.md`. Mantieni la struttura delle cartelle. Non caricare direttamente lo ZIP.
3. In **Settings → Pages** seleziona **Deploy from a branch**, branch **main**, directory **/(root)**. Imposta **Custom domain** a `inutilipress.com`.
4. In Cloudflare imposta i quattro record A del dominio principale verso gli indirizzi GitHub Pages: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`. Imposta il proxy a **DNS only** (nuvola grigia). Puoi aggiungere `www` come CNAME verso `simoneseverini.github.io` se desideri usare anche www.
5. Dopo l'attivazione del certificato in GitHub, seleziona **Enforce HTTPS**.

Il sito usa **Jekyll** (già integrato in GitHub Pages). Non creare un file `.nojekyll`.

## Aggiungere un libro

1. In `_books` crea un nuovo file, per esempio `_books/il-secondo-libro.md`.
2. Incolla una struttura come questa e modifica i campi:

```yaml
---
title: "Titolo del libro"
author: "Nome autore"
order: 2
lang: it
cover: "https://indirizzo-della-copertina.jpg"
amazon_url: "https://www.amazon.com/dp/ASIN-VERIFICATO"
---

Breve presentazione del libro. Puoi usare il normale Markdown.
```

3. Fai **Commit changes**. Il sito mostrerà automaticamente il nuovo libro **sopra** quelli che hanno un numero `order` inferiore.

Il numero `order` controlla soltanto la posizione, non viene mostrato ai lettori. Ogni libro avrà sempre la stessa struttura: **copertina, titolo, autore, testo e link Amazon**.

Per cambiare testo, immagine o link di `Truthsick`, modifica solamente `_books/truthsick.md`.

## Nota sulle copertine

La copertina di *Truthsick* viene caricata da un indirizzo immagine di Amazon.com recuperato in una precedente versione. Se Amazon cambia quell'indirizzo, aggiorna il campo `cover:` nel file del libro. La pagina d'acquisto è `https://www.amazon.com/dp/B0HLBGSLFG`.
