# Editor Immagini Online

Editor professionale per ritagliare, ruotare e modificare immagini direttamente dal browser. Nessuna installazione richiesta, tutto viene elaborato localmente nel tuo browser per la massima privacy.

## 🎯 Caratteristiche

- **Caricamento facile**: Carica immagini e PDF tramite selezione file o drag & drop
- **Ritaglio personalizzato**: Area di ritaglio trascinabile e ridimensionabile con 8 maniglie di controllo
- **Dimensioni preset**: 
  - Fototessera (260×315 px = 33×40 mm a 200 DPI)
  - Firma (251×50 px)
  - Dimensioni personalizzate
- **Zoom avanzato**: Regolazione da 5% a 200% con visualizzazione in tempo reale
  - Lo zoom si applica solo all'immagine, non all'area di selezione
  - Possibilità di zoomare per ritagliare con precisione l'area desiderata
- **Rotazione**: 
  - Rotazione rapida a 90° e -90°
  - Rotazione precisa con ruota interattiva per regolazioni di qualsiasi grado
- **Specchiatura**: Flip orizzontale e verticale
- **Filtro bianco e nero**: Conversione istantanea in scala di grigi
- **Controllo qualità immagine**:
  - Regolazione DPI (default 200 DPI per fototessere)
  - Compressione automatica per rispettare la dimensione massima in KB (default 35 KB)
- **Esportazione**: Salva in formato JPG con nome file che include dimensioni e DPI

## 🚀 Utilizzo

1. Apri l'editor nel browser
2. Carica un'immagine o PDF (clicca "Scegli File" o trascina il file nell'area centrale)
3. Applica le modifiche desiderate:
   - Seleziona un preset (Fototessera/Firma) o inserisci dimensioni personalizzate
   - Posiziona e ridimensiona l'area di ritaglio trascinandola
   - Regola lo zoom per far rientrare perfettamente l'immagine nell'area selezionata
   - Ruota l'immagine se necessario
   - Specchia orizzontalmente o verticalmente
   - Applica il filtro bianco e nero se necessario
4. Imposta DPI e dimensione massima file
5. Esporta l'immagine cliccando "Esporta JPG"

## 🎨 Funzionalità Avanzate

### Zoom Intelligente
Il sistema di zoom è progettato per funzionare come i migliori editor professionali:
- L'immagine viene ingrandita/rimpicciolita **sotto** l'area di selezione
- L'area di selezione rimane fissa (non si ingrandisce)
- L'area ritagliata corrisponde esattamente a ciò che vedi nella cornice di selezione
- Perfetto per centrare volti nelle fototessere o dettagli specifici

### Supporto PDF
- Carica file PDF multipagina
- Visualizza e seleziona la pagina desiderata
- Converti pagine PDF in immagini ritagliate

### Fototessere Conformi
Il preset "Fototessera" genera immagini con specifiche corrette:
- Dimensioni: 33×40 mm
- Risoluzione: 200 DPI
- Pixel: 260×315 px
- Formato: JPG compresso
- Peso file: configurabile (default 35 KB)

## 🔒 Privacy

Tutte le operazioni vengono eseguite localmente nel tuo browser. Le immagini e i PDF non vengono mai caricati su server esterni. I tuoi dati rimangono sul tuo dispositivo.

## 💻 Tecnologie

- HTML5 Canvas per l'elaborazione delle immagini
- PDF.js per il supporto PDF
- JavaScript vanilla (nessuna dipendenza esterna)
- Design moderno con gradiente teal
- Interfaccia drag & drop intuitiva
- Font Google: DM Sans

## 📱 Compatibilità

Funziona su tutti i browser moderni:
- Chrome/Edge (consigliato)
- Firefox
- Safari
- Opera

## 🎓 Credits

Born from the collaboration between **Maria Natasha Fragalà & AI**

## 📄 Licenza

Copyright © 2026 - Maria Natasha Fragalà

## 🔗 Demo

Accedi all'applicazione: [Inserisci qui il tuo URL GitHub Pages]

---

## 📝 Note Tecniche

### Come funziona il ritaglio con zoom

Il sistema utilizza un approccio a doppio canvas:
1. Un canvas temporaneo applica tutte le trasformazioni (rotazione, flip, bianco e nero)
2. Le coordinate dell'area di selezione vengono convertite considerando il fattore di zoom
3. Il canvas finale estrae l'area corretta e applica la compressione per rispettare i KB impostati

**Formula chiave**: 
- Coordinate reali = Coordinate visibili / Fattore di zoom
- Esempio: con zoom 150%, un'area di 300px cattura 200px dall'immagine originale

Questo garantisce che l'immagine salvata corrisponda esattamente a ciò che l'utente vede nell'area di selezione.
