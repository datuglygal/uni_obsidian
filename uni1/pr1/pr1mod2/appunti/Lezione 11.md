21-11-2024

- [[Lezione 11#Puntatori|Puntatori]]
- 

---
## Puntatori

```C
//tipo *nomeVariabile
int *puntatore
int *p1, p2 //solo p1 è puntatore, p2 è una variabile
float *p3, *p4; //p3 e p4 sono due puntatori a float
//è possibile creare puntatori per qualsiasi tipo di variabile

int *puntatore = NULL; //il puntatore è una variabile, inizializzata a zero
//quando creiamo un puntatore lo inizializziamo o ad un indirizzo o a NULL (inizializzarlo sempre)
puntatore = &numero; //puntatore prende l'indirizzo di memoria di numero
printf("Indirizzo puntato dal puntatore: %p", puntatore); //%p

printf("il contenuto di numero è: %d", *puntatore); //stampa il contenuto del puntatore come intero
printf("il contenuto di doppio è: %d", doppio);

printf("%p : %d", pNumero, *pNumero); // indirizzo e contenuto


/*----------------------------------------------------------------------------------------------------*/

int numero=25;
int *puntatore =NULL;
puntatore = &numero;


void subroutine (int *numero){
	*numero= 5000;
	numero=NULL;
}


/*----------------------------------------------------------------------------------------------------*/
int main(){
	int numero=7;
	int *pNumero= &numero;

	printf("Numero prima: %d", numero); //numero prima: 7
	doppio(pNumero); //non dichiarando il puntatore potremmo mettere &numero
	printf("Numero dopo: %d", numero); //numero dopo: 14
}

void doppio(int *p){
	(*p)= 2*(*p);
	p=NULL; //in questo caso non serve a nulla, modifichiamo la copia del puntatore
}
```

---
#### Puntatori e subroutine
utile per restituire più valori da una subroutine
es.

```C
int subroutine (int x, int y){
	int sum= x+y;
	int dif= x-y;
	return sum;
	return dif; //viene ignorato
}


//con puntatore

int main(){
	int x=5;
	int y=6;
	int somma, diff;

	printf("Valori prima e dopo: %d - %d", somma, diff);
	sommaDiff(x, y, &somma, &diff);

	printf("La somma di x e y è %d", somma);
	printf("La differenza tra x e y è %d", diff);

	return 0;
}

void sommaDifferenza (int x, int y, *resSomma, *resDiff){
	*resSomma= x+y
	*resDiff= x-y;
}
```

---
#### Aritmetica dei puntatori

```C
int var=5;
int *p= &var; //dichiara un puntatore intero che punta alla locazione di memoria in cui è memorizzata var

printf("Il puntatore punta a %p e contiene %d", p, *p);
p++; //va avanti
printf("Il puntatore punta a %p e contiene %d", p, *p);

/*---------------------------------------------------------------*/
//esempio
int v[]= {10, 20, 30, 40, 50};
int i;
int *p = NULL;

p = v; //non &v, v è già puntatore

for (i=0; i<5; i++){
	printf("%d", *p);
	p++;
} //farlo sempre con una variabile, altrimenti perdiamo i valori iniziali
```


``` C
typedef struct {
	float peso;
	int altezzaCm;
	
}
```



```caacculo
cacaccacacacacac
```




pa = blabla (scrive detro la cella di memoria della variabile pa)

`*pa` = bla bla (scrive dentro alla cella puntata dal contenuto di pa)