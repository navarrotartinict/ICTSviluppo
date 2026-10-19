# ICT Sviluppo – Spazio di lavoro Marketing

Questo repository è lo spazio di lavoro del marketing di **ICT Sviluppo**: qui teniamo linee guida del brand, template, archivio dei contenuti, campagne, landing page e report KPI.

Serve a due cose:

1. **Avere tutto in un unico posto**, con la cronologia di ogni modifica (chi ha cambiato cosa e quando).
2. **Dare contesto a Claude**: quando chiediamo un contenuto, Claude legge i file di questo repository (tono di voce, glossario, template) e produce testi coerenti con il brand.

> ⚠️ Molti file contengono segnaposto `[DA COMPILARE: ...]`. Finché non sono compilati, Claude non ha le informazioni reali su ICT Sviluppo e non deve inventarle.

---

## Mappa delle cartelle

| Cartella | Cosa contiene |
|---|---|
| [`brand/`](brand/) | Linee guida (tono di voce, lessico, posizionamento) e glossario dei termini Shopify/e-commerce |
| [`template/`](template/) | Modelli pronti: post LinkedIn, newsletter, script TikTok, scaletta podcast, scheda lezione, brief campagna |
| [`contenuti/`](contenuti/) | Archivio di tutto ciò che pubblichiamo, con i risultati |
| [`campagne/`](campagne/) | Una cartella per ogni campagna, con brief e report |
| [`landing/`](landing/) | Landing page HTML; `_modello/` è la base da duplicare |
| [`report/`](report/) | Report KPI periodici (mensili, trimestrali) |

Le cartelle e i file che iniziano con `_` (es. `_modello`, `_esempio-campagna`) sono **modelli da copiare**, non contenuti reali.

---

## Come lavorarci con Claude

Indica sempre a Claude **quali file usare come riferimento**. Esempi di richieste:

1. *"Scrivi un post LinkedIn sul replatforming verso Shopify Plus usando `template/post-linkedin.md` e `brand/linee-guida.md`."*
2. *"Prepara lo script di un TikTok da 45 secondi su 3 errori comuni nel checkout, seguendo `template/script-tiktok.md` e il `brand/glossario.md`."*
3. *"Crea la scaletta della prossima puntata del podcast su [tema] con `template/scaletta-podcast.md`; controlla in `contenuti/archivio.md` di non ripetere argomenti già trattati."*
4. *"Crea una nuova campagna in `campagne/2026-11-nome-campagna/` partendo da `campagne/_esempio-campagna/` e compila il brief con questi dati: ..."*
5. *"Duplica `landing/_modello/` in `landing/webinar-b2b/` e adatta i testi al brief di `campagne/2026-11-webinar-b2b/brief.md`."*
6. *"Leggi `contenuti/archivio.md` e dimmi quali argomenti hanno funzionato meglio negli ultimi 3 mesi."*

---

## Flusso di lavoro consigliato

Non modifichiamo mai direttamente il branch `main`: `main` contiene sempre la versione "approvata".

1. **Branch** – crea un ramo di lavoro separato con un nome chiaro (es. `post-linkedin-novembre`, `campagna-black-friday`).
2. **Modifiche** – scrivi o fai scrivere a Claude i contenuti sul branch, con commit dai messaggi chiari in italiano (es. *"Aggiunge brief campagna Black Friday"*).
3. **Pull request** – apri una pull request (PR) verso `main`: è la richiesta di unire le modifiche, con una descrizione di cosa è cambiato.
4. **Revisione** – rileggi le modifiche nella scheda *Files changed* della PR, lascia commenti, chiedi correzioni.
5. **Merge** – quando è tutto ok, premi *Merge pull request*: le modifiche entrano in `main`. Poi puoi eliminare il branch.

---

## Anteprima delle landing con GitHub Pages

Le istruzioni per pubblicare un'anteprima online delle landing sono in [`landing/README.md`](landing/README.md).
