# 🚀 Guida all'Uso di Antigravity nei Progetti Transformer

Questo documento serve come "promemoria" o cheatsheet (bignami) per usare velocemente tutto il potenziale che abbiamo configurato su Antigravity. Consultalo ogni volta che ti viene un dubbio su come impartirmi ordini.

---

## 1. Il Nucleo: `GEMINI.md`
Il file `C:\Users\walter.guillen\.gemini\GEMINI.md` è il mio cervello. **TU NON DEVI FARE NULLA.**
- Lo leggo in automatico ogni volta che apri una chat in questo o in altri progetti (argos, troy, bookof).
- Se mi fai una domanda tecnica senza nessun comando speciale, io erediterò comunque le tue Global Rules: codice in inglese, testo in italiano, divieto di rompere i container di PixiJS e niente crash se le paytable in XML falliscono in 404.

---

## 2. Cambiare Stile (Meta-Prompt)
Vuoi che ti dia risposte più asciutte? O più prolisse? Vuoi che io parli "meno da capo architetto"? Puoi attivarmi in volo uno di questi stili usando il simbolo chiocciola (`@`) oppure nominandolo in chat:

- *"Oggi usiamo @GEMINI_CARE.md per questa task"* -> (Meno focus sul mio "Ruolo" da esperto, più orientato ai Risultati pratici).
- *"Applica @GEMINI_RTF.md"* -> (Role, Task, Format: molto minimalista).
- *"Switcha a @GEMINI_RACE.md"* -> (Bilanciato per dettare cosa mi aspetto a lungo termine dal tuo bugfix).

Questi file vivono in `C:\Users\walter.guillen\.gemini`.

---

## 3. Comandi Rapidi (Slash Workflows)
Per analizzare il codice, fare refactoring o aggiungere componenti interi (Bonus, Freespin) abbiamo trasformato le tue direttive in veri e propri comandi magici.
Per attivarli, **digita semplicemente lo slash `/` seguito dalla parola** e poi spiegami cosa vuoi fare. 
Ecco il menu completo a tua disposizione:

### 🧩 Workflows Architetturali
- `/bonus` -> "Analizza il codice selezionato sapendo che deve obbedire alla piramide BonusMode, BonusStage, SpotPhase dei transformer."
- `/freespin` -> "Creiamo una nuova label nei giri gratuiti (FreespinMode, ExtraSpinPanel)."
- `/symbols` -> "Aiutami a instanziare un nuovo SymbolSprite dinamico nei rulli."
- `/gulp` -> "Refattorizza la mia task gulp o migriamo questo minify a Webpack."

### 🔬 Workflows di Quality Assurance
Apri o seleziona un file JS/ES6, e lanciami uno di questi:
- `/unused` -> Io controllerò il file e ti dirò se ci sono variabili, file importati o asset grafici di Pixi caricati ma che non chiami mai in tutto il codice.
- `/duplicated` -> Cancellerò porzioni di logica Pixi o richieste fetch incollate mille volte e creerò un _helper_ elegantissimo. 
- `/security-risk` -> Analizzerò brutalmente il file per avvertirti se ci sono `totalWin` o loop logici che potrebbero andare in botta (Type Warning) o che farebbero crollare l'app se il serve non risponde bene.
- `/overengineering` -> Ti sgriderò gentilmente se hai creato 4 interfacce dove bastava un semplice `.forEach()` in Vanilla JS, semplificandoti la vita!

---

💡 **Esempio Super Efficace di Messaggio:**
> "Ehi, seleziona tutto `main.js`. Lancia **/unused** e poi applica uno switch stile **/overengineering**. Trovami la logica spazzatura." 

---

## 4. Prompt Files di Contesto (`.prompt.md`)

Per task tecniche focalizzate su un'area specifica del codice, usa i **Prompt Files**. Caricano automaticamente il contesto giusto (gerarchia classi, gotcha noti, nodi config) senza che tu debba rispiegarlo ogni volta.

Vivono in `C:\Users\walter.guillen\.gemini\prompts\` e li attivi con `/nomefile` nella chat di Copilot (oppure con `#nomefile.prompt.md`).

### 📄 Prompt Files Disponibili

| Comando | File | Quando usarlo |
|---|---|---|
| `/bonus` | `bonus.prompt.md` | Lavori su BonusMode, BonusStage, SpotPhase, WheelPhase, CoinPhase |
| `/paytable` | `paytable.prompt.md` | Lavori sulla tabella dei pagamenti: posizioni, scroll, config.json, griglia dinamica |

### 🔑 Cosa contiene ogni Prompt File
- **Gerarchia delle classi** coinvolte
- **Nodi chiave del `config.json`** da modificare
- **Gotcha e bug noti** già documentati (es. bug scroll portrait con scale 0.5)
- **Regola d'oro**: non modificare i file base del framework, solo gli override game-specific

---

💡 **Tips d'uso:**
> "Usa `/paytable`. Perché il testo della Label5 si sovrappone alla Label6 in portrait?"

> "Usa `/bonus`. Come si resetta lo stato di BonusStage al close?"
