### Autovalutazione lez.6
- Il costrutto For viene utilizzato per effettuare un salto condizionato del flusso d'esecuzione di un programma quando si sa a priori il numero di iterazioni da fare.
- Nessuna delle componenti del for è obbligatoria.
- la componente del for legata all’incremento viene eseguita al termine dell'esecuzione delle istruzioni del blocco
- il goto dev'essere evitato perchè utilizzandolo si compie un salto incondizionato del flusso d'esecuzione del programma che va contro i principi della programmazione strutturata.
- Si può dichiarare un vettore senza specificarne la dimensione, 
	 `int vect[] = {1, 2, 3};`
- un vettore può essere di tutti i tipi
- la prima cella di un vettore è rappresentata dall'indice 0
- In fase di dichiarazione [] serve per specificare la dimensione dell'array e in una fase diversa serve per accedere a una cella dell'array specificata dall'indice.
- Si può copiare un vettore in un altro usando l'operatore di assegnamento, ma bisogna farlo cella per cella (meglio con un costrutto iterativo). Es. vect1[0] = vect2[0]; vect1[1] = vect2[1]; etc.
- Se il programma mi chiede di creare un vettore statico con dimensione inserita dall'utente in input, posso creare un vettore statico con una certa dimensione abbastanza grande e controllare l'input dell'utente affinché il valore che inserisca sia minore della grandezza del vettore.


### Array multidimensionali

se un array è l'insieme dei voti di un esame, e devo gestire più esami, posso creare quella che si chiama matrice.

es.-> 
`int votiPrimoSemestre[NUM_ESAMI][NUM_STUDENTI];`
`int matrice[righe][colonne];`


es. -> `int votiPrimoSemestre[NUM_ESAMI][NUM_STUDENTI];`

|        | studente0 | studente1 | studente2 | studente3 |
| ------ | --------- | --------- | --------- | --------- |
| esame0 |           |           |           |           |
| esame1 |           |           |           |           |
| esame2 |           |           |           |           |

```C
#include <stdio.h>

#define NUM_ESAMI 5
#define NUM_STUDENTI 10

int main(void){
	//voti degli studenti
	int votiPR1[NUM_STUDENTI]
	int votiPrimoSemestre[NUM_ESAMI][NUM_STUDENTI;
	//init seed
	srand(time(NULL));

	//scorrimento array
	for (int i=0; i<NUM_STUDENTI; i++){
		votiPR1[i] = MIN+ rand()%(MAX-MIN+1);
		}
	//scorrimento matrice
	for(int i=0; i<NUM_ESAMI; j++){
		for(int j=0; j<NUM_STUDENTI; j++){
			votiPrimoSemestre [i][j]= MIN+ rand()%(MAX-MIN+1);
			printf("%d\t", votiPrimoSemestre[i][j]);
		}
		printf("\n");
	}
}
```

### Organizzazione della memoria

un array monodimensionale (es.3) in memoria viene salvato come una lunga riga di elementi 

|     |     |     |
| --- | --- | --- |
un array bidimensionale (es 2x3), che per comodità visualizziamo come una tabella, in memoria viene sempre salvato come una lunga riga di elementi.

visualizzazione per comodità

| <font color="#00b050">1</font> | <font color="#00b050">2</font> |
| ------------------------------ | ------------------------------ |
| 3                              | 4                              |
| <font color="#31859b">5</font> | <font color="#31859b">6</font>                              |
visualizzazione in memoria

| <font color="#00b050">1</font> | <font color="#00b050">2</font> | 3   | 4   | <font color="#31859b">5</font> | <font color="#31859b">6</font>   |
| ------------------------------ | ------------------------------ | --- | --- | ------------------------------ | --- |


### Inizializzazione matrici

- per inizializzare una matrice di tipo `int matrice[righe][colonne];`
	`int matrice[2][3]= {{1,2,3},{1,2,3}};`
	
- è anche inizializzabile come array singolo, inserendoli in ordine di riga
	`int matrice[2][3]= {{1,2,3,1,2,3}};`
	
- gli elementi non inizializzati vengono posti a zero

- posso omettere il valore delle righe, es.
	`int matrice[][3]= {{1,2,3},{1,2,3}};`