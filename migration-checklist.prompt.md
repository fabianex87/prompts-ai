---
description: 'Checklist tecnica per la migrazione da Gulp a Webpack: raccoglie tutte le informazioni chiave, punti di controllo e vincoli per guidare la trasformazione del progetto slot machine JS (ES5/ES6)/PixiJS.'
tools: ['edit', 'search', 'search/usages', 'read/problems']
---

# MIGRATION CHECKLIST – Gulp → Webpack

## Obiettivo
Raccogliere e aggiornare tutte le informazioni operative e i punti di controllo necessari per una migrazione efficace da Gulp a Webpack.

## Informazioni chiave da raccogliere
1. **Tipologia degli asset**
   - JS, CSS, immagini, font, JSON, altri
   - Modalità di import e uso
2. **Task Gulp critiche**
   - Build, copy, minify, release, ftp, debug, compressione, ecc.
   - Task personalizzate e automazioni
3. **Struttura delle dipendenze**
   - Librerie e plugin Gulp/Webpack usati
   - Versioni, incompatibilità note
4. **Entry point e output**
   - File di ingresso (main.js, index.html, ecc.)
   - Destinazione bundle/output
5. **Gestione ambienti**
   - Dev, prod, test, release
   - Variabili, config, override
6. **Modularizzazione**
   - Organizzazione moduli JS (ES5, require, globali)
   - Dipendenze legacy
7. **Vincoli di compatibilità**
   - Browser target, supporto mobile, requisiti legacy
8. **Step manuali**
   - Operazioni non automatizzate da Gulp da replicare in Webpack
9. **Obiettivi di ottimizzazione**
   - Minificazione, splitting, caching, hot reload, ecc.

## Come usare questo file
- Aggiorna ogni punto con le informazioni specifiche del progetto.
- Usa questa checklist come base per richieste, troubleshooting e pianificazione della migrazione.
- Integra con link, note, riferimenti a prompt specifici (gulp.md, webpack.md, ecc.).

---

## Esempio di compilazione

### 1. Tipologia degli asset
- JS: ES5, main.js, moduli bonus/freespin
- CSS: style.css, fontsEmbeded.css
- Immagini: PNG, GIF, SVG in assets/
- Font: TTF, font embedded in CSS
- JSON: config.json, environment.json

### 2. Task Gulp critiche
- debug, release, ftp, compress, copy-default-assets, override-css, ecc.

### 3. Struttura delle dipendenze
- Gulp: gulp, gulp-rename, gulp-sourcemaps, gulp-minify, gulp-sftp-up4, ecc.
- Webpack: webpack, style-loader, css-loader, copy-webpack-plugin, ecc.

### 4. Entry point e output
- Entry: src/main.js, index.html
- Output: dist/, DEBUG/, RELEASE/

### 5. Gestione ambienti
- Variabili in environment.json
- Task dedicate per dev/prod/release

### 6. Modularizzazione
- Moduli JS (ES5/ES6), globali, require
- Bonus, freespin, symbols, ecc.

### 7. Vincoli di compatibilità
- Browser: Chrome, Firefox, Edge
- Mobile: iOS, Android
- Legacy: IE non supportato

### 8. Step manuali
- Copia manuale di asset non gestiti da Gulp
- Override di config in fase di release

### 9. Obiettivi di ottimizzazione
- Minificazione JS/CSS
- Splitting bundle
- Hot reload in dev

---

## SOLUZIONE FINALE
Usa questa checklist come riferimento operativo per la migrazione, aggiornando i punti secondo le esigenze del progetto. Integra con i prompt tecnici per risposte e automazioni mirate.
