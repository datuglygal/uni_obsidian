### Autovalutazione 24-10-24
- un vettore bidimensionale con più di una riga viene memorizzato come un unico array monodimensionale dove il primo elemento di ogni riga segue l'ultimo elemento della riga precedente.
- Un array monodimensionale ha solo una dimensione invece quello bidimensionale ne ha due. La prima cella di un vettore bidimensionale è rappresentata dalla coppia di indici 0 e 0.
- Con quali indici accedo alla cella della seconda colonna e terza riga? [2][1]
- se inizializzo una matrice senza specificarne la dimensione non succede niente se specifico almeno la seconda dimensione. La prima viene dedotta dall'inizializzazione.
- Posso copiare una matrice in un’altra utilizzando l’operatore di assegnamento, ma solo se si scorre cella per cella con un costrutto iterativo.
- una matrice può essere di tutti i tipi
- per stampare il contenuto della cella di un vettore bidimensionale devo usare un segnaposto che dipende dal tipo del vettore.


### Array di caratteri (stringhe)
(array di caratteri)

#### Inizializzazione
`char nome [DIM];`
carattere di -> escape \0 (conviene quindi aggiungere 1 a DIM per inserire \0)


- omettere la dimensione della stringa
`char squadra[] = "Cagliari Calcio";`

- avere più spazio che non viene utilizzato
`char squadra [25] = "Dinamo Sassari";`
	gli spazi che non vengono utilizzati vengono riempiti con \0

- avere meno spazio di quello necessario
`char squadra [8] = "Cagliari";`
	non esiste abbastanza spazio per memorizzare lo \0

#### Memorizzazione
`char stringa [20];`
`scanf("%s", stringa);`
SENZA LA &

legge una sequenza di lettere fino all'invio o uno spazio
	per risolvere il problema dello spazio:
	`scanf("%[^\n]s, squadra);`

per eliminare il problema dell'invio dopo ogni scanf:
	`getchar();`, 
	oppure inserire uno spazio prima del % nello scanf
		`scanf(" %[^\n]s, squadra);`

possiamo limitare il numero di caratteri letti della scanf utilizzando "%ns"
	`scanf(" %16s, squadra);`
	in questo caso inserendo più caratteri di quelli possibili, solo i primo 16 verranno salvati, i restanti verranno salvati nel buffer
		per pulire il buffer
		`while (getchar() != '\n') {}`

possiamo usare una MACRO per indicare il numero massimo di caratteri:
```C
	#define LIM_STRING 16
	#define LIMIT_INPUT "16" //16 ma stringa
	scanf(" %"LIMIT_INPUT"[^\n]s, squadra);
```

al posto di printf posso usare puts
`puts(stringa)`
a differenza del puts, con il printf posso printare una stringa in mezzo ad un testo usando %s


### Libreria string.h

- `strcpy(stringa1, stringa2);` -> copia stringa1 in stringa2
- `strlen(stringa);`  -> restituisce la lunghezza della stringa (la lunghezza del carattere \0 non viene restituita)
- `strncpy( s1, s2, max);` copia solo i primi max caratteri di s2 sulla stringa s1
- `strcat (char [] s1, char []s2);` -> salva in s1 s1+s2
- `strncat (s1, s2, num);` -> concatena solo i primi max caratteri
- `strcmp(char [ ]s1, char []s2); `-> 0 se le stringhe sono uguali, <0 se s1<s2; >0 se s1>s2 (alfabeticamente)
il singolo apice serve per i caratteri, il doppio per le stringhe

### memorizzazione di più stringhe
matrici di caratteri.
(ogni riga corrisponde ad una stringa)
`char arrayStringhe[R][C];`
nei printf, inserire il numero della colonna significa stampare solo un carattere.



### Esercizi
1 e 2, date due stringhe in input stampa la più lunga e calcoli quanto è lunga senza usare strlen
```C
#include <stdio.h>  
#include <string.h>  
  
#define DIM 15  
  
int main(void) {  
  
    char s1[DIM+1], s2[DIM+1];  
    int i;  
  
    printf("inserisci la prima stringa: ");  
    scanf("%s", s1);  
  
    printf("\niserisci la seconda stringa: ");  
    scanf("%s", s2);  
  
    printf("\nLa stringa piu' lunga e' ");  
    if (strlen(s1)>= strlen(s2))  
        printf("%s", s1);  
    else  
        printf("%s", s2);  
  
    while ( s1[i]!= '\0') {  
        i++;  
    }  
  
    printf("\nLa stringa 1 e' lunga %d", i);  
  
  
    return 0;  
}
```

3
scambio stringhe senza strcpy
```C
#include <stdio.h>  
#include <string.h>  
  
#define DIM 15  
  
int main(void) {  
  
    //creazione stringhe e variabili  
    char s1[DIM+1], s2[DIM+1];  
    int len;  
  
    //input stringhe  
    printf("inserisci la prima stringa: ");  
    scanf("%s", s1);  
  
    printf("\niserisci la seconda stringa: ");  
    scanf("%s", s2);  
  
    //output stringhe prima dello scambio  
    printf ("\nprima della copia"  
            "\n[s1]%s "  
            "\n[s2]%s", s1,s2);  
  
    //creazione variabile   
if (strlen (s1)>= strlen(s2))  
        len= strlen(s1);  
    else  
        len= strlen(s2);  
  
    //scambio stringhe  
    for (int i=0; i<len+1; i++) {  
        s1[i]=s2[i];  
    }  
      
    //output stringhe dopo lo scambio  
    printf ("\ndopo la copia"  
           "\n[s1]%s "  
           "\n[s2]%s", s1,s2);  
  
  
    return 0;  
}
```

4 (con libreria)
```C
#include <stdio.h>  
#include <string.h>  
  
#define DIM 30  
//date due stringhe stampa la maggiore alfabeicamente, sia con funzioni di libreria che senza  
int main(void) {  
    //creazione stringhe e variabili  
    char s1[DIM+1], s2[DIM+1];  
    int alph;  
  
    //input stringhe  
    printf("inserisci la prima stringa: ");  
    scanf("%s", s1);  
  
    printf("\niserisci la seconda stringa: ");  
    scanf("%s", s2);  
  
    alph=strcmp(s1,s2);  
    if (alph>0)  
        printf("\n%s", s1);  
    else if (alph<0)  
        printf("\n%s", s2);  
    else  
        printf("\nLe due stringhe sono uguali");  
  
    return 0;  
}
```
(senza libreria)

```C
#include <stdio.h>  
  
#define DIM 30  
//date due stringhe stampa la maggiore alfabeicamente, sia con funzioni di libreria che senza  
int main(void) {  
    //creazione stringhe e variabili  
    char s1[DIM+1], s2[DIM+1];  
    int i=0;  
  
    //input stringhe  
    printf("inserisci la prima stringa: ");  
    scanf("%s", s1);  
  
    printf("\niserisci la seconda stringa: ");  
    scanf("%s", s2);  
  
   while (s1[i]==s2[i])  
       i++;  
	if (s1[i]== '\0' && s2[i]== '\0')
	printf("\nLe due stringhe sono identiche");
  
    if (s1[i]> s2[i])  
        printf("%s", s1);  
    else if
        printf("%s", s2);  
     
  
  
    return 0;  
}
```

4 ma controlla il caps :)

```C
#include <stdio.h>  
#include <string.h>  
  
#define DIM 30   
//date due stringhe stampa la maggiore alfabeicamente, sia con funzioni di libreria che senza  
int main(void) {  
    //creazione stringhe e variabili  
    char s1[DIM+1], s2[DIM+1];  
    int alph;  
  
    //input stringhe  
    printf("inserisci la prima stringa: ");  
    scanf("%s", s1);  
  
    printf("\niserisci la seconda stringa: ");  
    scanf("%s", s2);  
  
    for (int i=0; i<strlen(s1); i++) {  
        if (s1[i]>= 'a')  
            s1[i]= s1[i]- ('a'-'A');  
    }  
    for (int i=0; i<strlen(s2); i++) {  
        if (s2[i]>= 'a')  
            s2[i]= s2[i]- ('a'-'A');  
    }  
  
    alph=strcmp(s1,s2);  
    if (alph>0)  
        printf("\n%s", s1);  
    else if (alph<0)  
        printf("\n%s", s2);  
    else  
        printf("\nLe due stringhe sono uguali");  
  
    return 0;  
}
```


### Autovalutazione 05-11-24

-

Lezione 8: Autovalutazione (Aula Magna exFisica)
Punti:
89%
Non corretto
1.Che differenza c’è tra un array di caratteri e una stringa?

Non c'è differenza ma la stringa deve avere il carattere di escape dopo l'ultimo carattere.

La stringa è un tipo nativo che può essere usato come un array.

Non c'è differenza. Semplicemente la stringa ha il carattere & dopo l'ultimo carattere.

L'array di caratteri è un array invece la stringa è una variabile.
Esatto
2.Con quale tipo deve essere dichiarata una stringa?

Qualsiasi tipo tranne bool

Qualsiasi tipo

String

Char
Esatto
3.A cosa serve il carattere di escape null ( '\0' )?

Serve per indicare l'inizio della stringa.

Viene inserito a discapito del programmatore.

Serve per indicare la fine della stringa.

Serve per indicare la metà della stringa.
Esatto
4.Quali tra queste è un'inizializzazione di stringa valida?

char stringa = "Cagliari Calcio";

char stringa[25 + 1] = "Cagliari Calcio";

int stringa[25 + 1] = "Cagliari Calcio";

char stringa;
Esatto
5.È possibile definire e inizializzare una stringa senza specificare la sua dimensione?

No, non è possibile.

Sì, il compilatore calcola automaticamente la dimensione guardando altre stringhe già definite.

Sì, il compilatore calcola automaticamente la dimensione della stringa (compreso il carattere di escape)

Dipende dal tipo di compilatore
Esatto
6.Quale segnaposto si usa per stampare e acquisire una stringa?

%s

%c

&s

È a discapito del programmatore
Esatto
7.Come si può effettuare la copia di una stringa?

Si può fare in due modi: con la funzione strcpy della libreria string.h oppure copiando carattere per carattere con un costrutto iterativo.

Si può fare solo copiando carattere per carattere con un costrutto iterativo.

Si può fare solo utilizzando la funzione strcpy della libreria string.h

Non si può fare.
Esatto
8.Come si può calcolare la lunghezza di una stringa?

Si può fare solo contando carattere per carattere con un costrutto iterativo.

Si può fare solo con la funzione strlen della libreria string.h

Si può fare in due modi: con la funzione strlen della libreria string.h oppure contando carattere per carattere con un costrutto iterativo.

Non si può fare.
Esatto
9.È possibile stampare il contenuto di una stringa utilizzando un costrutto iterativo? Se sì, come?

Con un for stampando carattere per carattere.

Con una printf utilizzando il segnaposto %s.

Con una printf utilizzando il segnaposto %c

Non si può fare.