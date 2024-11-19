### Subroutine

- <font color="#b2a2c7">funzione</font> se restituisce un valore, <font color="#fac08f">procedura</font> se non restituisce nulla (void)
- dividere il codice in moduli che descrivono sottoproblemi
- evitare di scrivere lo stesso codice più volte
- leggibilità

```C
//sintassi
tipo nome_sottoprogramma(parametri che la subroutine riceve)

//esempi
int somma(int,int);
float calcolaPrezzoConIva (float prezzo, float iva);
int print_menu();
```

prima del main, dopo le direttive di preprocessing


una funzione successiva può richiamare una funzione precedente, ma non viceversa. La funzione precedente non "sa dell'esistenza" di quella successiva(se le implemento prima del main).

- dichiaro le subroutine prima del main, vado a definirle/implementarle dopo il main, questo ci permette di evitare il problema.

#### Precisazioni

- possibile
	- posso dichiarare variabili locali accessibili solo dall'interno del sottoprogramma
	- utilizzare variabili globali
	- eseguire qualsiasi tipo di istruzione del linguaggio C
	- invocare altri sottoprogrammi
- non possibile
	- utilizzare variabili dichiarate altrove
	- richiamare il main
		- (sarebbe meglio non farlo)

es.
```C
int main(){
int x=10, y=5, sum=0;
sum=somma(x,y);
}
```
- non devono necessariamente restituire un valore
- non devono necessariamente ricevere parametri
	- per indicare l'assenza di parametri e/o valori restituiti, si utilizza un tipo particolare, il tipo <font color="#b7dde8">void</font>
	-
	es
```C
	void eseguiScelta (int scelta);
	eseguiScelta(5);
```
"eseguiScelta" è un tipo void, quindi non restituisce un valore, e prende il parametro intero "scelta".
Successivamente chiamo la funzione "eseguiScelta" e inserisco il valore 5 come "int scelta"
	-
	es senza parametri
```C
	void stampaMenu ( );
	stampaMenu( );
```
"stampaMenu" è un tipo void, che non richiede nessun parametro in input
	-
	funzione
```C
	int somma (int x, int y);
	s=somma (10, 20);
```
somma è una funzione intera che chiede due interi in input

funzione senza parametri
```C
	float tassoInteresse ( void );
	ti = tassoInteresse( );
```


## Return
return è una keyword che ci permette di restituire un valore a chi lo chiama

`return espressione;`

- return è un operatore con precedenza molto alta, ovviamente deve rispettare il tipo di valore specificato nella dichiarazione della funzione
- una funzione può restituire solo un valore, nel caso in cui andassimo ad inserire più return, il primo return sarebbe quello considerato, volendo questo è possibile solo se i due return sono alternative tra loro (utilizzando ad esempio un if-else)


esistono altre modalità per restituire più di un valore:
- strutture 
- puntatori


## Parametri
esistono due modalità di passeggio dei parametri alla funzione:
- Per valore: i parametri vengono copiati in nuove variabili che sono visibili solo al sottoprogramma
- Per indirizzo o riferimento: i parametri che vengono passati sono quelli originali.
	
	In C esiste solo il passaggio per valore
	- gli array fanno eccezione a questa regola (vedremo il motivo quando studieremo i puntatori)

##### tipi di parametri

- attuali: parametri che il chiamante fornisce al programma
- formali: parametri che la funzione utilizza

```C
int somma(int a, int b);

int main ()
{
	int x=5, y=10;
	int sum;
	sum = somma(x,y); //parametri attuali
	printf("La somma è %d", sum);

	return 0;
}

int somma(int a, int b) //parametri formali
{
	//sum non è visibile dal main e cesserà di esistere una volta finito il sottoprogramma
	int sum= a+b;
	return sum;
}
```


### Variabili globali

variabili dichiarate all'esterno del main o dalle funzioni (scope globale)

sono accessibili da qualsiasi punto del codice (il main e le altre funzioni) e modificabili senza bisogno di passarle come parametri

```C
void fun (void);

//variabile globale
int numero = 0;

int main()
{
	printf("Valore %d", numero);
	fun();
	printf("Valore %d", numero);
	return 0;
}

void fun( void )
{
	scanf("%d", &numero);
}
```
(non usarle :) )


è possibile passare un array o una matrice alla subroutine

- array
```C
void stampa (int[]); //prototipo subroutine

//definizione subroutine
void stampa (int array []){
	int i;
	for (I=0; i<DIM; i++)
	printf("%3d", array [i]);
}
```
è sempre consigliato passare la dimensione dell'array come parametro (ad esempio al posto del DIM)
ogni modifica che effettuo sull'array è sempre visibile anche nella funzione chiamante

- matrici
```C
#define C 5
void stampaMatrice (int matrice [][C]); //prototipo subroutine, (intestazione)

//definizione subroutine
void stampaMatrice (int matrice [][C]){
int i, j;
for (i=0; i<R; i++)
	for (j=)
}
//da finire di copiare
```


### variabili static
- anteponendo la keyword static alla dichiarazione di una variabile all'interno di un blocco se ne modifica la durata di memorizzazione e lo scope
- una variabile static non viene distrutta all'uscita dal bocco, ma rimane in memoria, mantenendo staticamente il suo valore, inoltre viene inizializzata solo una volta
- una variabile static può essere vista e modificata solo nello scope in cui è stata dichiarata

```C
void test ( void){
	static int numero=0;
	numero++;
	printf("%d\n", numero);
}
int main (){
test(); 
//da finire di copiare
}
```

### variabili const
anteponendo la keyword const alla dichiarazione ed eventuale inizializzazione di una variabile, si trasforma in oggetto di sola lettura.
- diversa dalla `#define` 
	- la define consente di definire macro (numeri, caratteri o stringhe), la keyword const può essere anteposta a qualsiasi tipo di oggetto  (array, strutture, etc.)
	- le const sono soggette alle regole di scope delle variabili, mentre le macro no
	- le macro sono gestite dal preprocessore, e non dal compilatore

```C
void stampa (const int a []){
	 for (i=0; i<DIM; i++)
	 printf("%d", a [i]);
}
int main(){
	int a[DIM];
	...
	stampa(a);
}
```
- in questo modo l'array non viene modificato in alcun modo