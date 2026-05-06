# StructCalc prudenziale

Questa versione e' un predimensionatore strutturale prudenziale per paglioli/telai metallici semplici.

## Cosa e' cambiato

- La portata mostrata e' **utile netta**, non lorda.
- Il peso proprio di copertura e telaio viene sottratto dal risultato.
- Le azioni permanenti e variabili usano coefficienti distinti (`gammaG`, `gammaQ`).
- Le travi sono controllate sia a flessione sia a freccia `L/300`.
- Le gambe usano una inerzia minima semplificata e mostrano un avviso quando servono dati da tabellario.
- Il report non dichiara piu' verifiche non implementate come nodi, bulloni, saldature, torsione, LTB o FEM.

## Limiti importanti

Il risultato resta preliminare. Non sostituisce il calcolo di un tecnico abilitato e non verifica:

- nodi, saldature, bulloni e piastre di base;
- carichi concentrati, urti, vibrazioni e fatica;
- torsione e instabilita' flesso-torsionale;
- punzonamento o instabilita' locale;
- reazioni vincolari reali con solutore FEM.

## Esecuzione

```bash
npm install
npm run dev
```

Test del motore:

```bash
npm test
```

Nel workspace attuale `node.exe` risulta bloccato da Accesso negato, quindi i test sono stati aggiunti ma non eseguiti localmente.
