### [[Lezione 1]]
- Anatomia di un programma in C
- Direttive di preprocessing
- Commenti
- Variabili
- Tipi di dato
- Operatori aritmetici
- Assegnamento
- Stampa su terminale
- Acquisizione valori da input

### [[Lezione 2]]
- Cast implicito ed esplicito 
- Problematiche acquisizione valori da input
- [[Lezione 2#tipo char e valori interi |Dettagli sul tipo char]]
- Operatori: priorità e associatività
- Operatori composti

### [[Lezione 3]]
- La libreria math
- Il costrutto di selezione in C: if-else
	- If concatenati
	- If annidati
	- Dangling else
	- Suggerimenti
- Espressioni booleane
- [[Lezione 3#Operatori booleani| Operatori booleani]]
- Confronti tra char

### [[Lezione 4]]
- [[Lezione 4#Indentazione|Indentazione]]
- [[Lezione 4#Generazione casuale di numeri|Generazione di numeri casuali]]
- [[Lezione 4#Lo switch|Switch-case]]
- [[Lezione 4#Operatore ternario|Operatore ternario]]

### [[Lezione 5]]
- [[Lezione 5#Operatori incremento e decremento|Operatori incremento e decremento]]
- Costrutti iterativi
- [[Lezione 5#While|While]]
- [[Lezione 5#Do While|Do While]]

### [[Lezione 6]]
- Costrutti iterativi
	- [[Lezione 6#Il for|For]]
- [[Lezione 6#Array|Gli Array]]
	- Array e indici
	- Inizializzazione
	- Esempi utilizzo
	- Insidie ed errori comuni

### [[Lezione 7]]
- [[Lezione 7#Array multidimensionali|Array multidimensionali]]
- [[Lezione 7#Organizzazione della memoria|Organizzazione della memoria]]
- inizializzazione matrici

### [[Lezione 8]]
- Array di caratteri (stringhe)
	- Memorizzazione
	- Inizializzazione
	- Inserimento
	- Stampa stringhe
- Libreria string.h
	- copia
	- lunghezza
	- concatenazione
	- comparazione



### Da ricordare per il parziale
- while(getchar()!='\n); per pulire il buffer.
- controllo doppioni e massim* inserit*
```C
if(n_giocatori<MAX_PLAYERS && doppio==false) {  //se ho meno dei giocatori massimi e non ho ancora trovato un doppione
    printf("\nInserisci giocatore n%d:",n_giocatori);  
    scanf(" %s",nomi_giocatori[n_giocatori]);  
  
    for(int i=0; i<n_giocatori; i++) {  //controllo dei doppioni
        if(strcmp(nomi_giocatori[i], nomi_giocatori[n_giocatori])==0) {  
            printf("\ngiocatore gia' inserito.");  
            doppio=true;  
        }  
    }  
	if(doppio==false) {  //nel caso in cui il giocatore non esistesse già, calcolo tutti i suoi lanci e avviso che l'ho aggiunto, aumentando il numero attuale di giocatori
        printf("Giocatore aggiunto.\n");  
        n_giocatori++;  
        for (int j=0; j<THROWS_N; j++) {  
            lanci [n_giocatori-1][j]= (min+rand()%(max-min+1))/pow(10,DEC);  
        }  
    }  
}else if(n_giocatori==MAX_PLAYERS)  //se ho raggunto il numero totale di giocatori
    printf("\nMassimo numero di giocatori raggiunto.");
```
- Controllo maiuscole e minuscole
```C
for(int j=0; j< strlen(listaBirre[i]);j++) {

  //trasformazione della prima lettera in maiuscola e le restanti in minuscole
	 if(j==0 && listaBirre[i][j]>='a') {//se è la prima lettera ed è minuscola
		listaBirre[i][j]-= ('a'-'A');//trasformo in maiuscola
		
	}else if (j>0)//dalla seconda lettera fino a strlen(listabirre[i])
	if (listaBirre[i][j]<'a')//se è maiuscola
	listaBirre [i][j]+= ('a'-'A');//trasformo in minuscola
}
```
