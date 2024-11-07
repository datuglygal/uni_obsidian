autovalutazione lezione 5
- non esiste differenza tra x+=1, x= x+1, x++.
- Che differenza c’è tra queste due espressioni: y = x++ * 5 e y = ++x * 5 ? Nella prima y ha come valore x * 5 senza l'incremento e, nella seconda, prima si incrementa x e poi si moltiplica per 5
- Per la teoria del linguaggio, il costrutto preferibile se dobbiamo eseguire un numero definito di iterazioni è il for
- se le iterazioni sono un numero indefinito, invece while o do while.
- Il Do While si utilizza quando non si sa il numero di iterazioni da fare, ma si sa che almeno una bisogna farla. Il While invece quando non si sa proprio il numero di iterazioni.
- la condizione all'interno del while è necessaria, altrimenti non compila
- il blocco del codice all'interno del while non è obbligatorio, ma si potrebbe finire in un loop infinito
- le parentesi graffe nel do while sono obbligatorie solo nel caso di più istruzioni all'interno del blocco. Il punto e virgola dopo il while invece è sempre obbligatorio.
- è possibile inserire un ciclo do while all'interno di un while, e quindi "annidare" i cicli.


### Il for
- prevede un numero di iterazioni definite, a differenza del while e del do while

```C
	for (inizializzazione; condizione; incremento) {
	blocco di codice
	}

	for (int i=0; i<10; i++){
	printf("\n io non sono un ingegnere!");
	}
	//dopo aver finito il numero di cicli esce (ovviamente).



	//esempi di cose che possono succedere
	
		for (int i=0; i>10; i++){
		printf("\n io non sono un ingegnere!");
			//non entrerà mai nel ciclo

		for (int i=0; i<10; i--){
		printf("\n io non sono un ingegnere!");
			//non uscirà mai dal ciclo
```
 a seconda di dove vado a dichiarare l'indice i, il suo valore sarà accessibile in zone diverse.
se dichiaro la variabile dentro al for, il suo valore sarà accessibile solo dentro al for, altrimenti, dichiarandola al suo esterno, sarà accessibile ovunque nella zona in cui è stata dichiarata (ad es. all'interno del main)

su C99 è possibile dichiarare la variabile all'interno del for, nelle versioni precedenti non era possibile

for (int i=0; i<10; i+=(i>=5 ? 2:1)) , se i>=5 incrementa i di 2, altrimenti incrementa di 1

for( ; ; ) è un loop infinito
il break causa l'immediata uscita dal ciclo, ma meglio evitare.
continue, invece, mi fa saltare l'iterazione attuale.



esiste anche il goto ma meglio non usarlo :)



### Array
tipi di dato non primitivi
definibili come una "singola maxi variabile"

```C

#include <stdlib.h>
#include <time.h>

#define NUM_STUDENTI 5
#define MAX_VOTO 31
#define MIN_VOTO 18

int main (void){
	//voti degli studenti di pr1
	int voti [NUM_STUDENTI]; //crea l'array senza inizializzare valori
	int voti1 [NUM_STUDENTI] = {30,23,33,28,27}; // crea un array con NUM_STUDENTI valori e assegna a ciascuna cella un valore preciso
	int voti2 [NUM_STUDENTI] = {}; //crea l'array e inizializza tutti i valori a zero
	int voti3 [] = {30,23,33,28,27}; //sa che ci sono 5 elementi
	//init seed
	srand (time(NULL));
	
	for (int i=0; i< NUM_STUDENTI; i++){
		voti [i]= MIN_VOTO + rand()%(MAX_VOTO- MIN_VOTO+1);
		printf("il voto dello studente [%d]: %d", i, voti[i]);
		}
		//printf (%d, voti);
}
```


| indice i   | 0   | 1   | 2   | 3   | ... | n-1  |
| ---------- | --- | --- | --- | --- | --- | ---- |
| voto esame | 27  | 28  | 30  | 23  | ... | voto |


```C
//ricerca massimo e minimo
for (int i =0; i<NUM_STUDENTI ; i++) {
//if per il minimo
if (voti [i]<min)
	min= voti [i];

if (voti [i]>max)
	max= voti[i];
}
```


per generare una copia di un array intero, è impossibile agire su tutto l'array; dobbiamo copiare singolarmente ogni valore al suo interno.
es.
- votiPR1copia = votiPR1;
	sbagliato, stiamo agendo sulla cella di memoria dell'array

```C
 for (int i=0; i< NUM_STUDENTI; i++)
	votiPR1copia[i]= votiPR1;
```
giusto, copio singolarmente ogni valore.




##### esercizi in aula
non ho voglia di completarlo, spero lo mandino :)
```C
#include <stdio.h>  
  
int main(void) {  
    //Scrivere un programma che acquisisca numeri float in successione.  
    //Per ogni numero inserito dovrà essere la calcolata la media e    //stampato il minore ed il maggiore inseriti fino a quel momento.    //Il programma deve terminare nel momento in cui si inserisce 0 o un numero qualsiasi negativo  
  
    float valoreUtente;  
    float media, minore= -1, maggiore=-1;  
  
    do {  
        printf("inserire un valore reale positivo: ");  
        scanf("%f", &valoreUtente);  
  
        if (valoreUtente>0) {  
            if(minore==-1&& maggiore==-1) {  
                minore=valoreUtente;  
                maggiore=valoreUtente;  
            } else {  
                if (valoreUtente<minore) {  
                    minore=valoreUtente;  
                } else if (valoreUtente>maggiore) {  
                    maggiore=valoreUtente;  
                }  
            }  
        }  
    } while   
return 0;  
}
```

