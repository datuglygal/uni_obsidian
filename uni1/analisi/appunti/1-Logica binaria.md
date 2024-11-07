il "corretto ragionamento", propagare verità dalle premesse alla conclusione
- <font color="#92cddc">Aristotele</font> (300 a.c.), formalismo e calcolo letterale
- <font color="#92cddc">George Boole</font>(1800) correlazione Aristotele-logica, formalismo moderno
- <font color="#92cddc">Claude Shannon</font>, correlazione logica-circuito, previsione del risultato, sommatori (basi processori)

- Una <font color="#92cddc">proposizione</font> o <font color="#92cddc">enunciato</font> è una espressione del linguaggio, cioè una sequenza di suoni con contenuto linguistico organizzati in parole e frasi, per la quale ha senso domandarsi se essa sia <font color="#9bbb59">vera</font> o <font color="#c0504d">falsa</font>. (solo nel caso in cui sia oggettivo)


#### Principi di logica binaria
- <font color="#92cddc">Identità</font>: ogni preposizione ha lo stesso valore di verità di se stessa
- <font color="#92cddc">Non contraddizione</font>: una preposizione non può essere contemporaneamente vera e falsa
- <font color="#92cddc">Il terzo escluso</font>: non esistono altri valor oltre a vero e falso

#### Connettivi logici
- se il valore di verità si può determinare subito si tratta di un enunciato <font color="#92cddc">semplice</font>
- se l'enunciato è collegato ad altri tramite operatori logici o connettivi si tratta di un enunciato <font color="#92cddc">composto</font>
	- se un valore di verità finale ritorna come quello iniziale si parla di <font color="#92cddc">identità</font> i, altrimenti si tratta di <font color="#92cddc">negazione</font> ¬

	I connettivi logici agiscono su n oggetti
	- 1) <font color="#92cddc">unari</font>, es. il coseno in matematica
	- 2) <font color="#92cddc">binari</font>

### Connettivi binari

##### Congiunzione ∧
- et, e, AND
	restituisce vero solo quando entrambi i valori in ingresso sono veri

| <center>p</center> | <center>q</center> | <center>p∧q</center> |
| ------------------ | ------------------ | -------------------- |
| <center>V</center> | <center>V</center> | <center>V</center>   |
| <center>V</center> | <center>F</center> | <center>F</center>   |
| <center>F</center> | <center>V</center> | <center>F</center>   |
| <center>F</center> | <center>F</center> | <center>F</center>   |
	

##### Disgiunzione (non esclusiva) ∨
- vel, o, OR
	restituisce vero quando almeno un valore in ingresso è vero

| <center>p</center> | <center>q</center> | <center>p∨q</center> |
| ------------------ | ------------------ | -------------------- |
| <center>V</center> | <center>V</center> | <center>V</center>   |
| <center>V</center> | <center>F</center> | <center>V</center>   |
| <center>F</center> | <center>V</center> | <center>V</center>   |
| <center>F</center> | <center>F</center> | <center>F</center>   |

##### Disgiunzione esclusiva ⊕
- aut aut, o, XOR
	restituisce vero se uno e solamente un valore in ingresso è vero

| <center>p</center> | <center>q</center> | <center>p⊕q</center> |
| ------------------ | ------------------ | -------------------- |
| <center>V</center> | <center>V</center> | <center>F</center>   |
| <center>V</center> | <center>F</center> | <center>V</center>   |
| <center>F</center> | <center>V</center> | <center>V</center>   |
| <center>F</center> | <center>F</center> | <center>F</center>   |

##### Implicazione semplice o materiale ->
- se... allora
- qui è importante il valore di antecedente e conseguente, "se p allora q"
- diverso da implicazione logica ⇒
	
| <center>p</center> | <center>q</center> | <center>p ->q</center> |
| ------------------ | ------------------ | ---------------------- |
| <center>V</center> | <center>V</center> | <center>V</center>     |
| <center>V</center> | <center>F</center> | <center>F</center>     |
| <center>F</center> | <center>V</center> | <center>V</center>     |
| <center>F</center> | <center>F</center> | <center>V</center>     |
- esempio:
	- p= consegui la laurea
	- q= ti regalano una vacanza

- Consegui la laurea e ti regalano una vacanza
- <font color="#953734">Consegui la laurea e non ti regalano una vacanza</font>
- Non consegui la laurea e ti regalano una vacanza
- Non consegui la laurea e non ti regalano una vacanza

	si tratta di una condizione sufficiente: 
	- se c'è il presupposto p allora q vale di sicuro. Se non c'è p, q potrebbe comunque valere.

#### Implicazione inversa <-
- solo se

| <center>p</center> | <center>q</center> | p<- q              |
| ------------------ | ------------------ | ------------------ |
| <center>V</center> | <center>V</center> | <center>V</center> |
| <center>V</center> | <center>F</center> | <center>V</center> |
| <center>F</center> | <center>V</center> | <center>F</center> |
| <center>F</center> | <center>F</center> | <center>V</center> |
	si tratta di una condizione necessaria. Se c'è il presupposto p, allora q può valere, se non c'è q allora p non vale. "solo se"  


#### Implicazione doppia ⇔
- se e solo se 

| <center>p</center> | <center>q</center> | p⇔q                |
| ------------------ | ------------------ | ------------------ |
| <center>V</center> | <center>V</center> | <center>V</center> |
| <center>V</center> | <center>F</center> | <center>F</center> |
| <center>F</center> | <center>V</center> | <center>F</center> |
| <center>F</center> | <center>F</center> | <center>V</center> |
	Si tratta di una condizione necessaria e sufficiente, p è la stessa cosa di q, uno implica l'altro e viceversa.


##### Condizione necessaria, sufficiente, necessaria e sufficiente

|                 | necessaria                                                                                                                  | non necessaria                                                                                                                        |
| --------------- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| sufficiente     | se la condizione <br>- è vera, l'evento <br>   si verifica<br>- è falsa, l'evento<br>   non si verifica<br>                 | se la condizione<br>- è vera, l'evento <br>  si verifica<br>- è falsa, L'evento <br>  può verificarsi <br>  oppure no                 |
| non sufficiente | se la condizione<br>- è vera, l'evento <br>   può verificarsi <br>   oppure no<br>- è falsa, l'evento<br>   non si verifica | se la condizione<br>- è vera, l'evento<br>  può verificarsi<br>  oppure no<br>- è falsa, l'evento<br>  può verificarsi<br>  oppure no |

---

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











esercizi
- ogni numero che termina con tre è primo-> non tutti i numeri che terminano con tre sono primi-> Esiste almeno un numero che termina con tre che non è primo.
- Esiste un pentagono con quattro lati-> Non esiste un pentagono che ha quattro lati
- Esiste un numero irrazionale con sviluppo decimale limitato-> non esiste un numero irrazionale con uno sviluppo decimale limitato. 

