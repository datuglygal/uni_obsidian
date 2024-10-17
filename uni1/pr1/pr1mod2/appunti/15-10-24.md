#### autovalutazione lezione 4
- Posso generare un numero casuale tra 0 e 10 usando la formula "0 + rand()%(10 - 0 + 1)"
- per generare un numero casuale tra -10 e 10 invece è (-10) + rand()%(10 - (-10) + 1)
- per generare un numero float casuale tra 0 e 1, :
	max *= pow(10, esponente);
	min *= pow(10, esponente);
	opzione2 = min
- se genero più di un numero casuale la funzione srand() va invocata solo una volta nel main dopo la dichiarazione delle variabili
- il caso default non è obbligatorio
- l'istruzione "break" serve ad interrompere il flusso del blocco di un case.
- Nello switch, non posso mettere come entrata di un case la valutazione di un'espressione non costante, in questo caso è opportuno usare il costrutto if-else
- Lo switch è utile quando i valori che una variabile può assumere sono noti a priori.
- il pezzo di codice stamperà case a e case b
- l'indentazione serve a rendere il codice più leggibili.

### Operatori incremento e decremento
++ incrementa la variabile di 1
-- -- decrementa la variabile di 1
(precedenze nelle slide)
es.
- i++, rende i e poi incrementa
- ++i, incrementa i e poi lo rende

```C
int a=5;
b= a++;
```
b vale 5

```C
int a=5;
b= ++a;
```
b vale 6


è sempre preferibile incrementare o decrementare in una riga separata rispetto alle altre operazioni per evitare "undefined behaviors", non definiti dalle regole del C, variano in ogni compilatore, anche sulla stessa macchina.

### While
	while (/*condizione){}
esempio
```C
#include <stdio.h>  
  
#define NUM_STUDENTI 5  
  
int main(void) {  
    int voto, cnt=0;  //definisco una variabile counter, inizializzandola a zero(in questo caso)
    float media =0;  
    
  //finchè il numero cnt (counter) è minore del numero finale di studenti, ripete il ciclo, incrementando di 1 il contatore ogni volta.
    while(cnt < NUM_STUDENTI) {  
        printf("Voto: ");  
        scanf("%d", &voto);  
        media +=voto;  
        cnt++;  
}  
  
    media = media/NUM_STUDENTI;  
    printf("Media = %.2f\n", media);  
    return 0;  
}
```

possiamo anche rendere il numero di studenti totali tramite una variabile che richiediamo all'utente

```C
#include <stdio.h>    
  
int main(void) {  
    int voto, studenti, cnt=0; 
    float media =0;  

	printf("inserisci il numero degli studenti: ");
	scanf("d", &studenti);

    while(cnt < studenti) {  
        printf("Voto: ");  
        scanf("%d", &voto);  
        media +=voto;  
        cnt++;  
}  
  
    media = media/studenti;  
    printf("Media = %.2f\n", media);  
    return 0;  
}
```
ovviamente, se assegniamo a "studenti" un valore negativo, il ciclo non partirà, perchè la variabile cnt è maggiore.


### Do While
fai questo... mentre()

```C
#include <stdio.h>  
#define MIN 6  
#define MAX 20  
int main(void) {  
    int voto, studenti, cnt=0;  
    float media =0;  
  
    do {  
        printf("inserisci il numero degli studenti: ");  
        scanf("d", &studenti);  
    } while (studenti< MIN || studenti>MAX);  
  
    while(cnt < studenti) {  
        printf("Voto: ");  
        scanf("%d", &voto);  
        media +=voto;  
        cnt++;  
    }  
  
    media = media/studenti;  
    printf("Media = %.2f\n", media);  
    return 0;  
}
```

```C
#include <stdio.h>  
#define MIN 6  
#define MAX 20  
int main(void) {  
    int voto, studenti, cnt=0;  
    float media =0;  
  
    do {  
        printf("inserisci il numero degli studenti: ");  
        scanf("%d", &studenti);  
        if (studenti< MIN || studenti>MAX) {  
            printf("hai inserito un numero non valido, inserisci un numero compreso tra %d e %d \n", MIN, MAX);  
        }  
    } while (studenti< MIN || studenti>MAX);  
  
    while(cnt < studenti) {  
        printf("Voto: ");  
        scanf("%d", &voto);  
        media +=voto;  
        studenti++;  
    }  
  
    media = media/studenti;  
    printf("Media = %.2f\n", media);  
    return 0;  
}
```


### esercizi

Scrivere un programma che esegua la divisione tra due numeri, chiedendo di inserire nuovamente il divisore finché questo non è diverso (non è diverso == uguale) da 0
```C
#include <stdio.h>  
  
int main(void) {  
    //Scrivere un programma che esegua la divisione tra due numeri,  
    //chiedendo di inserire nuovamente il divisore finché questo non è diverso    //(non è diverso == uguale) da 0  
    float dividendo, divisore, risultato;  
  
    printf("inserisci il dividendo: ");  
    scanf("%f", &dividendo);  
  
    do {  
        printf("inserisci il divisore: ");  
        scanf("%f", &divisore);  
  
        if( divisore == 0) {  
            printf("il divisore non puo' essere uguale a zero.\n");  
        }  
    } while (divisore == 0);  
  
    risultato = dividendo/divisore;  
    printf("%.2f/%.2f=%.2f\n",dividendo, divisore, risultato);  
    return 0;  
}
```

Calcolare il numero di cifre che compongono un numero intero inserito dall'utente

```C
#include <stdio.h>  
  
int main(void) {  
//Calcolare il numero di cifre che compongono un numero intero inserito dall'utente  
  
    int num, len=0;  
  
    printf("inserisci un numero: ");  
    scanf("%d", &num);  
  
    do {  
         num/=10;  
        len++;  
    }while(num!=0);  
  
    printf("il numero inserito ha %d cifre: ", len);  
  
    return 0;  
}
```

