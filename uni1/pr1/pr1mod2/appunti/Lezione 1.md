esercizi per casa.
- Esercizio 1
	Scrivere un programma in cui vengono dichiarate tre variabili intere a, b, c, a cui viene assegnato un valore a piacere. Il programma deve visualizzare, poi, il risultato dei tre seguenti calcoli: • a–b+c • a–b+c*a • (a/b) % c
	-
- Esercizio 2
	Scrivere un programma in cui si dichiarano due variabili A e B e si assegnino a esse due valori a piacere dello studente. Il programma deve ora scambiare il contenuto di A e di B. • Esempio: se inizialmente A contiene 15 e B 7, dopo lo scambio A contiene 7 e B 15. Stampare i valori delle due variabili prima e dopo lo scambio
	
	```C
	int a,b,c; //inserisco una terza variabile c  
    a=6;  
    b=5;  
    c=0;  
    //stampo i vaori iniziali di a e b  
    printf("a=%d b=%d\n",a,b);  
  
    //inverto i valori passando per la terza variabile  
    c=a;  
    a=b;  
    b=c;  
  
    //stampo i valori invertiti  
    printf("a=%d b=%d\n",a,b);

	```
- Esercizio3
	Versione 1: scrivere un programma in cui si dichiarano tre variabili intere A, B, e C e si assegnino a esse tre valori a piacere dello studente. Il programma deve calcolare la media dei tre valori, memorizzarla in una variabile di tipo float e visualizzarla con 2 decimali. Versione 2: ripetere l'esercizio della versione 1 dichiarando tre variabili di tipo float

	```C
	//dichiarazione variabili  
	int a,b,c;  
	float media;  
	media=0;  
	a=8;  //assegno dei valori alle tre variabili
	b=3;  
	c=5;  
	media=(float)(a+b+c)/3;  //formula della media
	  
	printf("media=%.2f\n",media); //stampo il risultato
		```
- Esercizio4
	Scrivere un programma che, dato un numero complessivo di gatti e il numero di questi per fila, fornisca in output: • il numero di file risultanti • il numero di gatti rimanenti nel caso in cui l’ultima fila non sia completa.

	```C
	int numGatti,gattiPerFila;  
	  
	printf("Inserisci numero di gatti: ");  
	scanf("%d",&numGatti);  
	printf("Inserisci numero di gatti per fila: ");  
	scanf("%d",&gattiPerFila);  
	  
	printf("Il numero di file e': %d \n" ,numGatti/gattiPerFila);  
	  
	if ((numGatti%gattiPerFila)!=0)  
	    printf("Il numero di gatti rimanenti e': %d \n", numGatti%gattiPerFila);  
	  
	printf("%d gatti in fila per %d col resto di %d si unirono... \n", numGatti, gattiPerFila, numGatti%gattiPerFila);
		```
- Esercizio5
	Scrivere un programma che, ricevuto in input un numero di gradi Celsius, lo trasformi in Fahrenheit secondo la formula F=(C*1.8) + 32. Effettuare poi la conversione inversa secondo la formula C=(F-32)/1.8 e controllare mediante stampa a video la correttezza del risultato.
	
	```C
		float celsius;  
	printf("Inserisci gradi celsius per la conversione: ");  
	scanf("%f",&celsius);  
	  
	printf("La conversione in fahrenheit vale: %.2f \n", celsius*1.8+32);  
	printf("La riconversione in celsius vale: %.2f, valore originale %.2f \n", ((celsius*1.8+32)-32)/1.8, celsius );
		```
- Esercizio6
	Scrivere un programma che permetta il calcolo del polinomio 5x4 - 8x3 + 4x2 + 3x – 4. Assegnare alla variabile x un valore a piacere e stampare il risultato a video

	```C
		int x;  
	printf("Inserisci un valore di x per il quale risolvere il polinomio 5x^4-8x^3+4x^2+3x-4 \n");  
	scanf("%d",&x);  
	  
	printf("il valore del polinomio con x=%d vale %.0f" ,x,5* pow(x,4)-8* pow(x,3)+4*pow(x,2)+3*(x)-4);
		```
- Esercizio7
	Scrivere un programma che permetta di calcolare il costo finale di un certo prodotto. Assegnare a piacere il prezzo del prodotto in una variabile float prezzoProdotto e associare a una macro IVA una percentuale a piacere. Stampare poi in output il seguente messaggio: Importo iniziale: ___.__ EUR 
	IVA applicata (__%): __.__ EUR 
	Importo finale: __.__ EUR

	```C
	#define Iva 22   
    float prezzoProdotto;  
    printf("inserisci il prezzo del prodotto: ");  
    scanf("%f",&prezzoProdotto);  
  
    printf("prezzo iniziale: %.2f \n" , prezzoProdotto);  
    printf("iva applicata: %.2f %% \n", (float)Iva);  
    printf("prezzo finale: %.2f \n ", prezzoProdotto + prezzoProdotto*((float)Iva/100));  
	```


test di autovalutazione del primo giorno di lezione
- <font color="#92cddc">macro</font>:
	- Una macro è un modo per dare un nome simbolico a valori che vengono utilizzati più volte all'interno del programma e deve essere definita con le direttive di preprocessing. La sua keyword è "#define".
	- Le macro vanno scritte tutte in maiuscolo
	- Una macro è un insieme di istruzioni che viene espanso nel codice sorgente, mentre una variabile è un'area di memoria che contiene un valore e può essere modificata durante l'esecuzione.
- <font color="#92cddc">printf</font>()
	- Serve a stampare output formattato su terminale.
	- la funzione 'printf()' riceve in ingresso almeno un parametro di tipo stringa.
	- Usando "%.3f" nel formato di printf posso stampare un numero in virgola mobile visualizzando solo le prime tre cifre decimali
	- printf(“%c”, 5 + ‘a’); stamperà f
- <font color="#92cddc">main</font>()
	- restituisce un tipo int.
- <font color="#92cddc">i magic numbers</font>
	- Costanti numeriche hard-coded nel codice, che dovrebbero essere evitate perché rendono il codice meno leggibile e più difficile da mantenere.