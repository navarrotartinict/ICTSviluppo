# landing/

Le landing page delle campagne, una per cartella.

| Cartella | Contenuto |
|---|---|
| [`_modello/`](_modello/) | Landing di base in un unico file `index.html` (HTML + CSS, nessuna libreria esterna): hero con CTA, vantaggi, prova sociale, FAQ, form contatti (solo struttura), footer |

## Come usarla

1. **Duplica** `_modello/` con un nome chiaro, es. `landing/webinar-b2b/`.
2. **Sostituisci i testi tra parentesi quadre** `[ ... ]`. Puoi chiedere a Claude: *"Adatta `landing/webinar-b2b/index.html` al brief di `campagne/2026-11-webinar-b2b/brief.md` seguendo `brand/linee-guida.md`."*
3. **Colori e font**: si cambiano in un solo punto, in cima al file, nella sezione `:root` (es. `--colore-primario`).
4. **Il form non invia dati**: prima di usare la landing davvero va collegato allo strumento di raccolta contatti (CRM, piattaforma email…). [DA COMPILARE: quale strumento usiamo?]
5. Per vederla sul tuo computer basta fare doppio clic su `index.html`: si apre nel browser.

> Le landing qui sono **anteprime di lavoro**. La pubblicazione definitiva (dominio, cookie banner, tracciamenti, privacy) va concordata a parte. [DA COMPILARE: dove pubblichiamo le landing definitive?]

---

## Anteprima online con GitHub Pages

GitHub Pages è un servizio gratuito di GitHub che trasforma i file del repository in un sito web visibile da un link.

### ⚠️ Prima di attivarlo, leggi qui

- **Il sito di GitHub Pages è pubblico**: chiunque abbia il link può vedere *tutti* i file del repository pubblicati (anche `brand/linee-guida.md`, i brief, i report). Non è indicizzato con facilità, ma non è privato.
- Con un account GitHub **gratuito**, Pages funziona solo se il repository è **pubblico**. Con un piano a pagamento (Pro, Team, Enterprise) funziona anche su repository privati, ma il sito resta comunque pubblico (salvo GitHub Enterprise Cloud con accesso privato).
- Valuta quindi con l'azienda se va bene che questi materiali siano consultabili online. Se non va bene, l'alternativa è tenere le landing in un repository separato e pubblico, dedicato solo alle anteprime.

### Passo passo

1. Apri il repository su GitHub: `https://github.com/navarrotartinict/ICTSviluppo`.
2. Clicca **Settings** (Impostazioni), l'ultima scheda in alto a destra. Serve essere amministratore del repository.
3. Nel menu a sinistra, nella sezione *Code and automation*, clicca **Pages**.
4. In **Build and deployment** → **Source**, scegli **Deploy from a branch**.
5. In **Branch**:
   - nel primo menu scegli **`main`** (la landing ci sarà dopo il merge della pull request; se vuoi vederla prima, puoi scegliere temporaneamente `setup-struttura-marketing`);
   - nel secondo menu lascia **`/ (root)`**;
   - clicca **Save**.
6. Attendi 1-3 minuti. Puoi seguire l'avanzamento nella scheda **Actions** del repository (vedrai un'attività chiamata *pages build and deployment*: quando ha la spunta verde, il sito è pronto).
7. Torna in **Settings → Pages**: in alto comparirà *"Your site is live at …"* con il link.
8. L'anteprima della landing sarà a questo indirizzo:

   **`https://navarrotartinict.github.io/ICTSviluppo/landing/_modello/`**

   Ogni nuova landing sarà a `https://navarrotartinict.github.io/ICTSviluppo/landing/nome-cartella/`.

### Perché c'è un file `.nojekyll` nella radice

GitHub Pages di base usa uno strumento (Jekyll) che **nasconde le cartelle che iniziano con `_`**, come `_modello`. Il file vuoto `.nojekyll` nella radice del repository disattiva questo comportamento: non cancellarlo, altrimenti l'anteprima di `_modello` restituisce "404 – pagina non trovata".

### Aggiornamenti e disattivazione

- Ogni volta che una modifica viene unita (merge) nel branch scelto, il sito si aggiorna da solo in pochi minuti.
- Per spegnere il sito: **Settings → Pages → Source**, scegli **None** (oppure il pulsante *Unpublish site*, se presente).
