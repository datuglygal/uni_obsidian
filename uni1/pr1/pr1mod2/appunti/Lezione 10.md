- Limiti di interi e float
- enumerazioni
- typedef
- strutture
	- dichiarazione
	- inizializzazione
	- accesso 
	- modifica
- strutture annidate
---
### Limiti del compilatore

- la libreria limits definisce alcune costanti relative al range dei tipi int e char
	`#include <limits.h>`
- i range dipendono dal compilatore (standard C99:)
	- CHAR_BIT (bit per char, 8)
	- CHAR_MAX (+127)
	- CHAR_MIN (-127)
	- INT_MAX (almeno +32767)
	- INT_MIN (almeno -32767)

- superare il minimo: underflow
- superare il massimo: overflow

- `#include <float.h>`
- float: valore in singola precisione (32 bit)
- double: valore in doppia precisione (64 bit)
- lo standard C99 impone che il double abbia almeno lo stesso numero di bit del float
- la libreria float definisce:
	- FLT_MAX (massimo numero positivo di tipo float)

---
### Dichiarare nuovi tipi
nuovi tipi di dato:
- enumerazione: nuovo tipo ex. novo
- struttura

(definirli dopo le direttive di preprocessing e prima del main)

---
#### Enumerazioni
keyword: enum

```C
enum seme{CUORI, QUADRI, FIORI, PICCHE};
enum nome {valori che il tipo di dato può assumere(in maiuscolo)};
enum nome {0, 1, 2, 3}; //le enumerazioni sono interi mascherati, infatti:
enum seme {CUORI=1, QUADRI, FIORI, PICCHE};// la sequenza si aggiornerà, possiamo assegnare anche a ciascun nome un numero diverso, non in ordine(ma meglio non farlo)


#include <stdio.h>

enum seme{CUORI=3, QUADRI, FIORI, PICCHE};

int main(){

	enum seme s;
	s=FIORI;

	printf("Vlore di s:\n");
	printf("%d", s);//stamperà 2 se cuori=0, 5 se cuori=3, oppure il numero che assegnamo a FIORI


	switch (s){
		case CUORI:
		printf("CUORI");
		break;
		case QUADRI:
		printf("QUADRI");
		break;
		case FIORI:
		printf("FIORI");
		break;
		case PICCHE:
		printf("PICCHE");
		break;
		default:
		break;
		}

	return 0;
}
```

keyword: typedef

```C
//forma compatta
typedef enum {CUORI, QUORI, FIORI, PICCHE} Seme;//maiuscolo

//forma estesa
enum seme {CUORI, QUORI, FIORI, PICCHE};
typedef enum seme Seme; //maiuscolo


int main(){
	Seme s;
	return 0;
}


----------------------------------------------------------------------------------
//esempi di enumerazioni

typedef enum {LUN, MAR, MER, GIO, VEN, SAB, DOM} Giorno;
```


---
#### Strutture

```C
struct nomeStruttura
{
tipoCampo1 nomeCampo1;
tipoCampo2 nomeCampo2;
};

//esempio
struct Calciatore
{
float peso;
int altezzaCm;
char cognome [20];
};

//variabile
struct Calciatore c;

//typedef esteso (assieme alla parte dell esempio)
typedef struct Calciatore Calciatore;
//typedef compatto
typedef struct
{
	float peso;
	int atezzaCm;
	char cognome [20];
}Calciatore;


Calciatore c={84.1, 187, "Riva"};

//attraverso l' operatore punto possiamo accedere ai campi
c.peso = 84.1;
scanf("%d", &c.altezzaCm);

//copia dei dati
Calciatore c1, c2;
c2=c1;
//se proviamo a copiare un array o una stringa funziona perfettamente
```

##### Strutture annidate
una struttura B può contenere una struttura A come suo campo, a patto che A sia stata dichiarata prima

```C
typedef struct{
	float peso;
	int altezzaCm;
	char cognome [20]
} //finisci di copiare
```

#### Array di strutture
```C
Calciatore squadra [DIM]
squadra[i].peso;
```

#### Subroutine e strutture
- è possibile passare una struttura come parametro a un sottoprogramma
- è possibile creare un sottoprogramma che restituisca una struttura