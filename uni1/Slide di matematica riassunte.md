

## Logica

### Introduzione alla Logica

- La logica è la scienza del ragionamento corretto, focalizzata sull'identificazione di principi e metodi per distinguere i ragionamenti validi.
- Aristotele, nel IV secolo a.C., fu un pioniere nella formalizzazione del ragionamento corretto con la sua dialettica. Questo può essere considerato come il primo tentativo di costruire una logica formale.
- La logica aristotelica, la prima forma di calcolo letterale, ha gettato le basi per l'algebra. Ha introdotto l'astrazione usando lettere per rappresentare concetti generali.
- Aristotele ha stabilito una disciplina scientifica per la logica, riducendo la composizione degli enunciati a operazioni algebriche dopo aver individuato analogie tra oggetti algebrici e logici.

### Proposizioni e Valori di Verità

- Una proposizione, o enunciato, è un'espressione linguistica che può essere vera o falsa.
- Ogni proposizione ha un valore di verità associato, che può essere vero (V) o falso (F).
- L'informatica utilizza due valori, creando una **logica binaria**, per rappresentare vari stati come il passaggio di corrente, la riflessione della luce o la magnetizzazione.
- Una proposizione è decidibile se il suo valore di verità può essere determinato in un numero finito di passaggi.

### Principi Fondamentali della Logica Binaria

- **Principio di identità:** Ogni proposizione ha lo stesso valore di verità di se stessa.
- **Principio di non contraddizione:** Una proposizione non può essere contemporaneamente vera e falsa.
- **Principio del terzo escluso:** Una proposizione può essere solo vera o falsa, senza altri valori di verità possibili.
- Un enunciato semplice ha un valore di verità immediatamente determinabile.

### Connettivi Logici e Enunciati Composti

- I connettivi logici, o operatori, combinano proposizioni elementari per creare **enunciati composti**.
- **Connettivi unari** operano su una singola proposizione, mentre i **connettivi binari** collegano due proposizioni.
- I connettivi binari includono:
    - Congiunzione (AND, ∧): vera solo se entrambe le proposizioni sono vere.
    - Disgiunzione (OR, ∨): vera se almeno una delle proposizioni è vera.
    - Disgiunzione esclusiva (XOR, ⊕): vera se solo una delle due proposizioni è vera.
    - Implicazione (→): falsa solo se l'antecedente è vero e il conseguente è falso.
    - Implicazione inversa (←): vera se il conseguente è vero, indipendentemente dall'antecedente.
    - Doppia implicazione (se e solo se, ↔): vera se entrambe le proposizioni hanno lo stesso valore di verità.

### Tipi di Condizioni Logiche

- **Condizione sufficiente:** Se p è vero, allora q è sicuramente vero. Tuttavia, q potrebbe essere vero anche se p è falso.
- **Condizione necessaria:** Se p è vero, allora q potrebbe essere vero. Ma se p è falso, allora q è sicuramente falso.
- **Condizione necessaria e sufficiente:** p è equivalente a q. Se uno è vero, anche l'altro è vero, e viceversa.

### Porte Logiche

- Le porte logiche sono circuiti elementari che implementano le funzioni degli operatori logici, come NOT, AND e OR.

### Proposizioni Aperte e Quantificatori

- Una proposizione aperta, o predicato, contiene variabili. Il suo valore di verità dipende dal valore assegnato alle variabili.
- Il dominio di una variabile è l'insieme dei valori che può assumere.
- L'insieme di verità di un predicato comprende i valori del dominio che rendono il predicato vero.
- I quantificatori chiudono un predicato:
    - **Quantificatore universale (∀):** "per ogni".
    - **Quantificatore esistenziale (∃):** "esiste".
    - **Quantificatore esistenziale unico (∃!):** "esiste un solo".
- Negazione dei quantificatori:
    - **¬(∀x, p(x)) ⇔ ∃x, ¬p(x):** "Non tutti gli x soddisfano p(x)" è equivalente a "Esiste almeno un x che non soddisfa p(x)".
    - **¬(∃x, p(x)) ⇔ ∀x, ¬p(x):** "Non esiste un x che soddisfa p(x)" è equivalente a "Tutti gli x non soddisfano p(x)".

### Metodi Deduttivi

- **Modus ponens:** Se p è vero e p implica q, allora q è vero.
- **Riduzione all'assurdo:** Se assumere ¬p porta a una contraddizione, allora p deve essere vero.
- **Induzione matematica:** Si dimostra che una proprietà è vera per un caso base, quindi si assume che sia vera per un valore arbitrario n e si dimostra che è vera per n+1.

## Insiemi

### Definizione e Rappresentazione degli Insiemi

- Un insieme è una collezione di oggetti distinti, concepiti come un'unica entità. Gli oggetti sono gli elementi dell'insieme.
- La definizione di un insieme deve essere univoca e non soggettiva, permettendo di determinare se un oggetto appartiene o meno all'insieme.
- Gli insiemi sono indicati con lettere maiuscole, mentre gli elementi con lettere minuscole.
- Rappresentazioni degli insiemi:
    - **Intensiva (per proprietà):** Descrive gli elementi tramite una proprietà caratteristica.
    - **Estensiva (per elencazione):** Elenca tutti gli elementi dell'insieme.
    - **Grafica (diagrammi di Eulero-Venn):** Rappresenta gli insiemi con cerchi o altre forme chiuse.

### Appartenenza, Cardinalità e Uguaglianza

- Un oggetto appartiene a un insieme se la proprietà che definisce l'insieme è vera per quell'oggetto.
- La cardinalità di un insieme (#A) è il numero dei suoi elementi.
- Due insiemi sono uguali (A=B) se hanno gli stessi elementi.

### Insieme Vuoto e Sottoinsiemi

- L'insieme vuoto (∅) non contiene elementi e ha cardinalità 0.
- Un insieme A è un sottoinsieme di B (A ⊆ B) se tutti gli elementi di A sono anche elementi di B.
- I sottoinsiemi propri di B sono diversi da B stesso e dall'insieme vuoto.
- Esempi di relazioni di sottoinsieme includono la gerarchia dei file system e l'organizzazione degli utenti in un sistema LDAP.

### Insieme delle Parti

- L'insieme delle parti di A (P(A)) contiene tutti i sottoinsiemi di A, inclusi quelli propri e impropri.
- Se A ha cardinalità n, allora P(A) ha cardinalità 2^n.

### Operazioni Insiemistiche

- **Unione (A ∪ B):** L'insieme che contiene tutti gli elementi di A e B, senza ripetizioni.
- **Intersezione (A ∩ B):** L'insieme che contiene gli elementi presenti sia in A che in B.
- **Differenza (A \ B):** L'insieme che contiene gli elementi di A che non appartengono a B.
- **Complementazione (C_UA):** L'insieme degli elementi dell'insieme universo U che non appartengono ad A.
- Le operazioni insiemistiche possono essere correlate ai connettivi logici e utilizzate per schemi di ragionamento.

### Coppie Ordinate e Prodotto Cartesiano

- Una coppia ordinata (a,b) è un insieme di due elementi in cui l'ordine è significativo.
- Il prodotto cartesiano AxB è l'insieme di tutte le coppie ordinate (a,b), dove a ∈ A e b ∈ B.
- La cardinalità di AxB è il prodotto delle cardinalità di A e B.
- Il prodotto cartesiano può essere rappresentato tramite elencazione, tabella a doppia entrata o graficamente.

## Relazioni e Funzioni

### Relazioni Binarie

- Una relazione binaria tra due insiemi A e B è un sottoinsieme del loro prodotto cartesiano AxB.
- Se A=B, si parla di relazione in un insieme.
- Le relazioni possono essere rappresentate tramite elencazione, proprietà caratteristica, diagramma a frecce, tabella a doppia entrata o rappresentazione cartesiana.
- Le relazioni binarie trovano applicazioni in informatica, ad esempio nei database relazionali.

### Proprietà delle Relazioni

- **Riflessiva:** Ogni elemento è in relazione con se stesso.
- **Antiriflessiva:** Nessun elemento è in relazione con se stesso.
- **Simmetrica:** Se a è in relazione con b, allora anche b è in relazione con a.
- **Antisimmetrica:** Se a è in relazione con b e b è in relazione con a, allora a=b.
- **Transitiva:** Se a è in relazione con b e b è in relazione con c, allora a è in relazione con c.

### Relazioni di Equivalenza e d'Ordine

- **Relazione di equivalenza:** Una relazione riflessiva, simmetrica e transitiva. Esempi: uguaglianza, equi-estensione, congruenza, similitudine.
- **Relazione d'ordine:** Una relazione antisimmetrica e transitiva. Può essere riflessiva o meno. Esempi: essere maggiore di, essere minore o uguale di, essere più alto di.

### Funzioni

- Una funzione da A a B è una relazione che associa ad ogni elemento di A uno e un solo elemento di B.
- A è il dominio, B il codominio e l'insieme di tutte le immagini degli elementi di A è l'immagine della funzione.
- Una funzione può essere vista come una trasformazione che riceve un input e produce un output.

### Grafico di una Funzione

- Il grafico di una funzione f è l'insieme di tutte le coppie ordinate (x,y) tali che x ∈ A e y=f(x) ∈ B.
- Il grafico può essere rappresentato nel piano cartesiano.

### Tipi di Funzioni

- **Iniettiva:** Elementi distinti del dominio hanno immagini distinte.
- **Suriettiva:** L'immagine della funzione coincide con il codominio.
- **Bigettiva (biunivoca):** Iniettiva e suriettiva.
- **Funzione identità:** Associa ad ogni elemento se stesso. È biunivoca.

### Composizione di Funzioni

- Date due funzioni f:A→B e g:B→C, la funzione composta g∘f:A→C applica prima f a x e poi g al risultato.
- La composizione di funzioni non è commutativa.

### Funzione Inversa

- Data una funzione biunivoca f:A→B, la funzione inversa f⁻¹:B→A associa ad ogni elemento y ∈ B l'unico elemento x ∈ A tale che f(x)=y.
- La composizione di una funzione con la sua inversa è la funzione identità.

## Insiemi Numerici

### Numeri Naturali (N)

- I numeri naturali servono per contare.
- Sono un insieme ordinato e le operazioni di somma, moltiplicazione ed elevamento a potenza producono risultati maggiori o uguali ai termini coinvolti.
- Le operazioni di sottrazione, divisione ed estrazione di radice sono definite solo sotto certe condizioni.
- Proprietà delle operazioni: commutativa, associativa, elemento neutro, distributiva, legge di annullamento del prodotto.

### Numeri Interi (Z)

- Gli interi includono i numeri naturali e i loro opposti.
- Ogni intero ha un opposto che, sommato ad esso, dà 0.
- Il valore assoluto di un intero è il suo modulo.
- Le operazioni di somma, moltiplicazione ed elevamento a potenza hanno le stesse proprietà dei naturali.
- La sottrazione e la divisione possono produrre risultati minori dei termini coinvolti.
- L'esponente negativo è definito come l'inverso della potenza con esponente positivo.

### Numeri Razionali (Q)

- I razionali sono numeri esprimibili come frazioni p/q, dove p e q sono interi e q ≠ 0.
- Ogni razionale diverso da 0 ha un inverso che, moltiplicato per esso, dà 1.
- Le operazioni di somma, moltiplicazione, sottrazione e divisione hanno le stesse proprietà degli interi.
- L'estrazione di radice con indice pari è definita solo per basi positive.

### Numeri Irrazionali

- I numeri irrazionali non sono esprimibili come frazioni.
- La radice quadrata di 2 è un esempio di numero irrazionale.

### Numeri Reali (R)

- I numeri reali includono i razionali e gli irrazionali.
- Possono essere approssimati tramite numeri decimali.
- I numeri macchina sono una rappresentazione discreta dei numeri reali utilizzabile dai computer.
- Assiomi dei numeri reali: commutatività, associatività, distributività, elemento neutro, opposto, inverso, dicotomia, asimmetria, proprietà dell'ordinamento, completezza.
- La legge di annullamento del prodotto vale anche per i numeri reali.
- Regole dei segni per la moltiplicazione.
- Somma, sottrazione, moltiplicazione e divisione mantengono o invertono l'ordine a seconda del segno dei termini coinvolti.
- Passaggio all'opposto e all'inverso: effetti sull'ordine.
- Le potenze con esponente reale sono definite solo per basi positive.
- Definizione e proprietà del logaritmo.

## Topologia della Retta Reale

### Intervalli

- Un intervallo è un sottoinsieme di R costituito da tutti i punti compresi tra due estremi a e b.
- Gli intervalli possono essere:
    - **Chiusi:** includono gli estremi.
    - **Aperti:** escludono gli estremi.
    - **Limitati:** hanno estremi finiti.
    - **Illimitati:** hanno almeno un estremo infinito.
- L'insieme vuoto è un intervallo.

### Intorni

- Un intorno di un punto x₀ ∈ R è un intervallo aperto che contiene x₀.
- Gli intorni possono essere:
    - **Circolari:** hanno lo stesso raggio a destra e a sinistra di x₀.
    - **Sinistri:** si estendono solo a sinistra di x₀.
    - **Destri:** si estendono solo a destra di x₀.

### Punti Interni, Esterni e di Frontiera

- Un punto x₀ è:
    - **Interno** ad un insieme A se appartiene ad A ed esiste un intorno circolare di x₀ interamente contenuto in A.
    - **Esterno** ad A se non appartiene ad A ed esiste un intorno circolare di x₀ interamente contenuto nel complementare di A.
    - **Di frontiera** per A se non è né interno né esterno.

### Punti di Accumulazione

- Un punto x₀ è di accumulazione per un insieme A se ogni suo intorno contiene almeno un punto di A diverso da x₀.
- Non è necessario che x₀ appartenga ad A.
- Il Teorema di Bolzano-Weierstrass afferma che ogni sottoinsieme infinito e limitato di R ha almeno un punto di accumulazione.

### Insiemi Aperti e Chiusi

- Un insieme è **aperto** se è costituito solo da punti interni.
- Un insieme è **chiuso** se il suo complementare è aperto.

### Maggioranti, Minoranti, Estremo Superiore ed Inferiore

- Un **maggiorante** di un insieme A ⊆ R è un numero maggiore o uguale a tutti gli elementi di A.
- Un **minorante** di A è un numero minore o uguale a tutti gli elementi di A.
- L'**estremo superiore** di A è il più piccolo dei suoi maggioranti.
- L'**estremo inferiore** di A è il più grande dei suoi minoranti.
- Ogni sottoinsieme non vuoto e limitato di R ha estremo superiore ed inferiore finiti.

### Massimo e Minimo

- Il **massimo** di A è l'estremo superiore di A se appartiene ad A.
- Il **minimo** di A è l'estremo inferiore di A se appartiene ad A.
- Ogni sottoinsieme non vuoto, chiuso e limitato di R ha massimo e minimo.