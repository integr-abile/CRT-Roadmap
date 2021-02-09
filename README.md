# Roadmap Progetto CRT

Considerati gli sviluppi del software EquatIO e considerata l'esperienza di SpeechMatE e del lavoro di trascrizione di formule matematiche.

- EquatIO
  - non funziona per la lingua italiana
  - non fornisce supporto per navigazione ed editing semantico o svolgimento di un'espressione matematica

Considerati i punti precedenti abbiamo pensato alla seguente Roadmap:

1. Trascrivere le registrazioni di formule matematiche (quelle appartenenti ad un set controllato di formule che abbiamo chiesto a degli insegnanti di leggere) annotando, per ogni concetto matematico i **sinonimi**, i **diversi modi di dire un certo concetto**. Un concetto può essere un'espressione o un concetto singolo. Per esempio: l'espressione di un integrale può definirsi un concetto, così come una potenza, così come un simbolo, come il "+". Fare un'analisi delle frequenze dei vari modi di dire un certo concetto o sinonimi (per definire anche i numeri per creare l'*Handbook for spoken mathematics in italiano*)
   1. Nel frattempo cercare di definire un altro set di formule da far leggere per aumentare il dataset esistente, pur restando nel dominio delle categorie di formule scelte per la dettatura
2. Fare clustering su quello che Cristian ha trascritto per eliminare eventuali outlier
   1. vediamo su tutti i cluster sono separabili secondo le nostre categorie scelte (a quali ci penseremo, ma per esempio possono essere insiemi, algebra, matrici)
3. Classificazione vedendo come il clustering ha diviso e assegnando delle etichette semantiche
4. Wizard of Oz (WOZ) con documentazione riguardo a che termini non usare nello svolgimento dell'esercizio
   1. L'esercizio è simile al seguente: Si mette l'utente nella condizione di passare da una *formula 1* ad una *formula 2* **dettando un processo di calcolo**
      1. La terminologia è **vincolata** da quello che è emerso *dall'handbook for spoken mathematics* con la possibilità di aggiungere stop words
      2. C'è **massima libertà** sui termini da usare per la navigazione ed editing. In pratica è un WOZ al contrario: vogliamo capire come la maggior parte dei partecipanti al test si immagina di esprimere a voce la navigazione considerando anche la componente istintiva
5. Analizzare le strategie di passaggio dalla *formula 1* alla *formula 2* per vedere se esistono modelli ricorrenti di navigazione ed editing che rispondono alla domanda: "come la gente modificherebbe l'espressione?"
   1. Quello che implementeremo è quello che hanno effettivamente detto? Magari è più efficiente e veloce fare in un altro modo, ma dobbiamo avere un metro di confronto, ma prima dobbiamo avere un WOZ base (quello al punto 4)
