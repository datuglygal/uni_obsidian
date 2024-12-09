## Appunti sulla Rappresentazione dell'Informazione in Sistemi Digitali

### 1. Introduzione alla Rappresentazione dell'Informazione

#### 1.1 Concetti Generali

- La rappresentazione dell'informazione coinvolge due aspetti fondamentali:
    - La scelta di una grandezza fisica che rappresenti l'informazione.
    - L'associazione di un valore di tale grandezza ad ogni possibile "aspetto" dell'informazione da rappresentare.

#### 1.2 Scelta della Grandezza Fisica

- La scelta della grandezza fisica è guidata da considerazioni tecnologiche.
- Con l'avvento dell'elettronica, si utilizzano principalmente fenomeni elettrici come tensione e corrente.

#### 1.3 Rappresentazione Analogica e Digitale

- **Rappresentazione Analogica**: la grandezza rappresentante varia in modo continuo.
- **Rappresentazione Digitale**: la grandezza rappresentante può assumere solo un numero discreto di valori.
- La rappresentazione digitale è meno fedele ma più robusta e affidabile rispetto a quella analogica.

#### 1.4 Rappresentazione Digitale Binaria

- **Rappresentazione Digitale Binaria**: utilizza solo due valori della grandezza rappresentante (0 e 1).
- **Vantaggi**:
    - Grande robustezza e affidabilità.
    - Ridotto consumo energetico e minore sensibilità al rumore.
- **Svantaggi**:
    - Minore potere rappresentativo.
- Per superare questo limite, si associa ad ogni "aspetto" dell'informazione un insieme di rappresentanti elettronici, ognuno dei quali fornisce una cifra binaria (bit) della sequenza che rappresenta l'informazione.

#### 1.5 Codifica Binaria

- Le informazioni vengono rappresentate in termini di stringhe di bit.
- Il passaggio dall'informazione alla stringa che la rappresenta richiede tecniche di codifica.

### 2. Sistemi di Numerazione e Conversione di Base

#### 2.1 Sistemi di Numerazione Posizionali

- Un sistema di numerazione è un insieme di simboli e regole per rappresentare i numeri.
- Un sistema di numerazione è **posizionale** se il valore di un simbolo (cifra) dipende dalla sua posizione nella sequenza che rappresenta il numero.
- Il sistema decimale è un sistema posizionale basato su 10 cifre (0-9).
- **Esempio**: 1475 = 1 ∙ 10³ + 4 ∙ 10² + 7 ∙ 10¹ + 5 ∙ 10⁰

#### 2.2 Notazione Posizionale

- In un sistema con base B ≥ 2 e insieme di simboli β = {0, 1, 2, …, B-1}, la stringa di n cifre `bn-1bn-2 … b1b0` si interpreta come: `bn-1 ∙B^(n-1) + bn-2 ∙ B^(n-2) + … + b1 ∙ B¹ + b0 ∙ B⁰`
- **Esempi**:
    - **Sistema Ottale (B=8)**: 417₈ = 4 ∙ 8² + 1 ∙ 8¹ + 7 ∙ 8⁰ = 271₁₀
    - **Sistema Esadecimale (B=16)**: 22₁₆ = 2 ∙ 16¹ + 2 ∙ 16⁰ = 34₁₀
    - **Sistema Binario (B=2)**: 10011₂ = 1 ∙ 2⁴ + 0 ∙ 2³ + 0 ∙ 2² + 1 ∙ 2¹ + 1 ∙ 2⁰ = 19₁₀
- La numerazione binaria è fondamentale nei calcolatori elettronici.
- I sistemi ottale ed esadecimale semplificano la conversione tra basi e la base 2.

#### 2.3 Conversione di Base

- **Conversione da Binario a Decimale**: si calcola il polinomio di potenze del 2.
- **Conversione da Decimale a Binario**: si usano divisioni successive per 2, i resti delle divisioni formano la rappresentazione binaria.
- **Conversione tra Base Bk e Base B**: si sostituisce ogni cifra in base Bk con la sua rappresentazione in base B.
- **Conversione tra Basi Generiche**: si può convertire alla base 10 e poi alla base desiderata.

### 3. Aritmetica Binaria

#### 3.1 Operazioni Aritmetiche di Base

- **Somma**: 0 + 0 = 0, 0 + 1 = 1, 1 + 0 = 1, 1 + 1 = 0 (con riporto di 1)
- **Sottrazione**: 0 - 0 = 0, 0 - 1 = 1 (con prestito di 1), 1 - 0 = 1, 1 - 1 = 0
- **Moltiplicazione**: 0 x 0 = 0, 0 x 1 = 0, 1 x 0 = 0, 1 x 1 = 1
- **Divisione**: 0 : 1 = 0, 1 : 1 = 1 (la divisione per zero non è definita)

### 4. Rappresentazione dei Numeri Negativi

#### 4.1 Parole e Byte

- I numeri sono rappresentati in raggruppamenti di bit chiamati **parole**.
- Una parola di 8 bit è chiamata **byte**.
- Una parola di n bit può rappresentare 2ⁿ numeri diversi.

#### 4.2 Convenzioni per i Numeri Negativi

- Il bit più a sinistra (bit più significativo) indica il segno: 0 per positivo, 1 per negativo.
- **Rappresentazione in Modulo e Segno**:
    - Il segno è rappresentato dal bit più a sinistra.
    - Il modulo (valore assoluto) è rappresentato dai restanti bit.
    - Svantaggi: due rappresentazioni per lo zero, richiede unità aritmetica per la sottrazione.
- **Rappresentazione in Complemento**:
    - Permette di effettuare sottrazioni usando l'unità aritmetica di somma.
    - **Complemento a 9 (decimale)**: si sottrae ogni cifra del numero da 9.
    - **Complemento a 10 (decimale)**: si calcola il complemento a 9 e si aggiunge 1.
    - **Complemento a 1 (binario)**: si complementano tutti i bit.
    - **Complemento a 2 (binario)**: si effettua il complemento a 1 e si aggiunge 1.
    - Il complemento a 2 è la rappresentazione più utilizzata.
    - Vantaggi: una sola rappresentazione dello zero, calcoli più semplici.

#### 4.3 Sottrazione in Complemento

- La sottrazione si effettua sommando al minuendo il complemento del sottraendo.
- Se c'è riporto, la differenza è positiva.
- Se non c'è riporto, la differenza è negativa.
- Esempi dettagliati sono forniti nei sorgenti.

#### 4.4 Overflow

- Si verifica quando il risultato di un'operazione non è rappresentabile correttamente con n bit.
- **Regola Pratica (complemento a 2)**: si ha overflow se c'è riporto al di fuori del bit di segno e non sul bit di segno, o viceversa.
- Esempi di overflow sono riportati nei sorgenti.

### 5. Numeri Frazionari e Virgola Mobile

#### 5.1 Numeri Frazionari

- **Rappresentazione**: `0, b-1b-2 … b-m` dove bi ∈ β = {0, 1, …, B-1}
- **Interpretazione**: `b-1 ∙B^(-1) + b-2 ∙ B^(-2) + … + b-m ∙ B^(-m)`
- **Esempi**:
    - 0,356₁₀ = 3 ∙ 10⁻¹ + 5 ∙ 10⁻² + 6 ∙ 10⁻³
    - 0,101₂ = 1 ∙ 2⁻¹ + 0 ∙ 2⁻² + 1 ∙ 2⁻³
- **Conversione Binario-Decimale**: si valuta l'espressione `b-1 ∙2^(-1) + … + b-m ∙ 2^(-m)`.
- **Conversione Decimale-Binario**: si usa il metodo delle moltiplicazioni successive.

#### 5.2 Numeri in Virgola Fissa

- **Rappresentazione**: si usa un numero fisso di bit per la parte intera e un numero fisso di bit per la parte frazionaria.
- **Esempi**: vedi sorgenti.

#### 5.3 Numeri in Virgola Mobile

- **Rappresentazione**: il numero viene espresso come prodotto di due fattori: uno con le cifre significative e l'altro come potenza della base.
- **Esempi**:
    - 127000000 = 127 ∙ 10⁶
    - 0,0000015 = 15 ∙ 10⁻⁷
- **Forma Generalizzata**: `± xn-1 … x1x0 , y-1y-2…y-m ∙ B^(±ak-1…a1a0)`
- **Esponente (o Caratteristica)**: `±ak-1…a1a0`
- **Mantissa**: `± xn-1 … x1x0 , y-1y-2…y-m`
- **Rappresentazione Esponenziale Normalizzata**: la prima cifra significativa si trova immediatamente a destra della virgola.
- **Ulteriori Convenzioni**:
    - Non si rappresentano i caratteri non necessari (zero iniziale, virgola, segno di prodotto, base).
    - Lunghezza fissa della mantissa.
    - Polarizzazione dell'esponente (aggiunta di una costante per renderlo sempre positivo).

#### 5.4 Standard IEEE 754

- **Definizione**: standard per la rappresentazione dei numeri in virgola mobile.
- **Formati Base**:
    - Mezza precisione (16 bit).
    - Precisione singola (32 bit).
    - Precisione doppia (64 bit).
    - Precisione quadrupla (128 bit).
- **Struttura**: `s (segno) exp (esponente) M (mantissa)`
- **Particolarità**:
    - L'esponente è polarizzato (`exp = E + bias`).
    - La mantissa è normalizzata con la parte intera sempre uguale a 1 (hidden bit).
- **Casi Particolari**: dettagli nei sorgenti per ogni formato.
- **Numeri Denormalizzati**: consentono di rappresentare valori più piccoli del più piccolo numero normalizzato.
- **Esempi**: vedi sorgenti.

#### 5.5 Operazioni in Virgola Mobile

- **Somma/Sottrazione**: richiede l'uguaglianza degli esponenti, si trasla la mantissa del numero con esponente minore, si effettua l'operazione e si normalizza il risultato.
- **Moltiplicazione**: si sommano gli esponenti, si moltiplicano le mantisse, si normalizza il risultato.
- **Divisione**: si sottraggono gli esponenti, si dividono le mantisse, si normalizza il risultato.

### 6. Informazioni Alfanumeriche

#### 6.1 Codifica Alfanumerica

- Le informazioni testuali/alfanumeriche sono rappresentate da sequenze di bit.
- Si stabilisce una corrispondenza biunivoca tra caratteri e configurazioni binarie (codifica).
- **Codifica ASCII (American Standard Code for Information Interchange)**:
    - Originariamente su 7 bit, estesa a 8 bit (ASCII standard e ASCII esteso).
    - **ASCII Standard**: supporta 128 caratteri (lettere inglesi, punteggiatura, simboli matematici, caratteri di controllo).
    - **ASCII Esteso**: supporta 256 caratteri, inclusi caratteri accentati.
- **Codifica Unicode**:
    - Codifica su 2 byte (estesa a 21 bit).
    - Include ASCII esteso, caratteri di molte lingue, simboli matematici, ideogrammi, Braille.
- **Codifica BCD (Binary Coded Decimal)**:
    - Rappresenta le singole cifre decimali su 4 bit.
    - Meno compatta della codifica binaria ma preserva la struttura decimale.
    - Utilizzata per input/output, trasmissione dati, applicazioni gestionali e finanziarie.
- **Esempi**: vedi sorgenti.

### 7. Algebra Booleana e Reti Logiche

#### 7.1 Sistemi Digitali e Reti Logiche

- **Sistema Digitale**: macchina che elabora segnali digitali (valori da un insieme finito, tipicamente binario).
- **Reti Logiche**: modelli per dispositivi con segnali a due valori.
- **Algebra delle Reti (o Algebra di Commutazione)**: permette la progettazione logica dei dispositivi.
- **Tipi di Reti**:
    - **Reti Combinatorie**: l'uscita dipende solo dall'ingresso.
    - **Reti Sequenziali**: l'uscita dipende dall'ingresso e dallo stato della rete.

#### 7.2 Algebra Booleana

- **Definizione**: algebra definita su un insieme di due elementi (0 e 1), con tre operazioni fondamentali:
    - **Prodotto Logico (AND)**: il risultato è 1 se e solo se entrambi gli operandi sono 1.
    - **Somma Logica (OR)**: il risultato è 1 se almeno uno degli operandi è 1.
    - **Complementazione (NOT)**: inverte il valore dell'operando.
- **Proprietà**:
    - Idempotenza, Associativa, Commutativa, Distributiva, Elementi Neutri, Elementi Forzanti, Assorbimento, Negazione, Doppia Negazione, Teorema di De Morgan.
- **Principio di Dualità**: data una proprietà, si ottiene la proprietà duale scambiando somma e prodotto, e 0 e 1.

#### 7.3 Porte Logiche

- **Definizione**: dispositivi elettronici che implementano gli operatori dell'algebra booleana.
- **Simboli Standard**: vedi sorgenti.
- Le espressioni algebriche possono essere trasformate in schemi logici e viceversa.

#### 7.4 Altre Applicazioni dell'Algebra Booleana

- **Logica delle Proposizioni**: si applica ai enunciati che possono essere veri o falsi.
- **Teoria degli Insiemi**: si applica alle operazioni su insiemi (unione, intersezione, complemento).

### 8. Forme Canoniche e Minimizzazione

#### 8.1 Forme Canoniche

- **Definizione**: forme standard per rappresentare funzioni logiche.
- **Tipi**:
    - **Prima Forma Canonica (Somma di Prodotti)**: somma di mintermini (prodotti fondamentali).
    - **Seconda Forma Canonica (Prodotto di Somme)**: prodotto di maxtermini (somme fondamentali).
- Si ottengono dalle tabelle di verità.
- Sono uniche per ogni funzione.
- Possono essere convertite l'una nell'altra usando il Teorema di De Morgan.
- Esempi dettagliati nei sorgenti.

#### 8.2 Minimizzazione

- **Obiettivo**: trovare l'espressione con il minor costo di realizzazione (numero di porte logiche).
- **Metodo delle Mappe di Karnaugh**:
    - Rappresentazione grafica della tabella di verità.
    - Si raggruppano le celle adiacenti in cui la funzione vale 1 (per la forma SP) o 0 (per la forma PS).
    - I raggruppamenti formano sottocubi (o sottomappe).
    - Ogni sottocubo corrisponde a un implicante (prodotto di variabili).
    - Gli implicanti primi essenziali coprono celle in modo esclusivo.
    - L'espressione minima contiene tutti gli implicanti primi essenziali.
- **Metodi Algoritmici (Quine-McCluskey)**: individuazione sistematica degli implicanti e selezione della copertura minima.
- **Condizioni di Indifferenza**: configurazioni di ingresso per cui il comportamento della rete non è specificato, utili per semplificare l'espressione.

### Conclusioni

Questi appunti forniscono una panoramica completa sulla rappresentazione dell'informazione in sistemi digitali. Partendo dai concetti base di codifica binaria, si esplorano i sistemi di numerazione, l'aritmetica binaria, la rappresentazione dei numeri negativi e frazionari, e la virgola mobile. Si introduce quindi l'algebra booleana, fondamentale per la progettazione di reti logiche, e si illustrano le forme canoniche per la rappresentazione e la minimizzazione delle funzioni logiche. Si conclude con cenni alle altre applicazioni dell'algebra booleana in logica delle proposizioni e teoria degli insiemi.