test di autovalutazione

input di caratteri tramite scanf() e getchar():
- nella gestione dell’input, nel caso in cui si acquisisca, mediante scanf, un carattere dopo una precedente scanf si potrebbe creare un problema<span style="background:rgba(3, 135, 102, 0.2)"> perchè nel buffer rimane il tasto invio che viene consumato dalla scanf dedicata al carattere</span>
- per gestire al meglio l’input di caratteri la getchar() viene utilizzata <span style="background:rgba(3, 135, 102, 0.2)">per intercettare il tasto invio senza interferire con scanf() multiple</span>
- per gestire al meglio l’input di caratteri ci sono soluzioni alternative alla getchar(), ossia <span style="background:rgba(3, 135, 102, 0.2)">lasciare uno spazio prima del segnaposto nella scanf. "scanf(" %c", &a);"</span>
- <span style="background:rgba(3, 135, 102, 0.2)">Non</span> è necessario usare la getchar() per l’input di valori numeri, <span style="background:rgba(3, 135, 102, 0.2)">perché quando si fa la scanf() di un valore numerico tutti i caratteri vengono scartati</span>

Cast implicito ed esplicito:
- <span style="background:rgba(3, 135, 102, 0.2)">Il cast implicito avviene senza che il programmatore lo espliciti con il comando es:(float)</span>
- L’operatore di casting ha effetto su <span style="background:rgba(3, 135, 102, 0.2)">tutti gli operandi</span>
- Che cosa si ottiene assegnando a una variabile float il risultato della divisione tra i due interi 2 e 7? <span style="background:rgba(3, 135, 102, 0.2)">La variabile conterrà 0,00</span>
- Che tipo di cast viene effettuato se dividiamo un float per un intero ? <span style="background:rgba(3, 135, 102, 0.2)">Cast implicito dell'intero in float</span>

- Come viene assegnato un carattere ad una variabile char? <span style="background:rgba(3, 135, 102, 0.2)">char c = 'a';</span>
- gli operatori composti sono <span style="background:rgba(3, 135, 102, 0.2)">+=, -=, *=, /= e %=</span>


la libreria math (`#include math.h`)
- potenza -> pow(a,b)
- radice -> sqrt (b)
- alcune macro come M_PI



#### Il costrutto di selezione if-else

#### Operatori booleani 
AND &&         `if(voto >=18 && voto <=30)`

OR ||      `if (voto <18 || voto >30)`

importante perchè non te lo ricordi mai! 
- differenza tra = e ==
	`if(risultato ==3)` , "se il risultato <u>vale</u> tre"
	x=5 -> la variabile x <u>prende</u> il valore 5

il valore di verità falso viene assegnato il valore 0;
il valore di verità vero viene assegnato il valore 1;
in C, qualsiasi numero diverso da 0 è automaticamente vero
sempre in C, gli operatori && e || vengono valutati fintanto che basta per stabilire se un'espressione è vera o falsa.

la variabile `_Bool`, va inclusa con `#include <stdbool.h>`; che include `_Bool (condizione 1, condizione 2)` e `bool`
```C

	int votoPR1, votoFDI, votoAM;
	_Bool condizione1, condizione2, condizione3;

	 votoPR1= 27;
	 votoFDI= 30;
	 votoAM= 24;

	condizione1= votoPR1 >=18 && votoPR1 <=30;
	condizione1= votoFDI >=18 && votoFDI <=30;
	condizione1= votoAM >=18 && votoAM <=30;
	if(condizione1 && condizione2 && condizione3){
		printf ("hai passato tutti gli esami del primo semestre!");
	} else {
		printf ("hai ancora esamii da dare!")}
```



esercizio lezione 
con età di tre persone, scrivi le età di ciascuno e scrivi chi è il più anziano.

```C
void esercizioLezione7() {  
    //età tre persone, età relativa ad ogni persona, età del più anziano  
    int eta1, eta2, eta3;  
    //input età  
    printf("eta' Pino: ");  
    scanf("%d", &eta1);  
    printf("eta' Maurizio: ");  
    scanf("%d", &eta2);  
    printf("eta' Piochio: ");  
    scanf("%d", &eta3);  
    //stampa le età di ciascuno  
    printf("Pino ha %d anni \n", eta1);  
    printf("Maurizio ha %d anni \n", eta2);  
    printf("Piochio ha %d anni \n", eta3);  
    //il più anziano  
    if (eta1>=eta2 && eta1>=eta3) {  
        printf("Pino e' il piu' anziano, con %d anni di eta' ", eta1);  
    } else if (eta2>=eta1 && eta2>=eta3) {  
        printf("Maurizio e' il piu' anziano, con %d anni di eta' ", eta2);  
    } else if (eta3>=eta1 && eta3>=eta2) {  
        printf("Piochio e' il piu' anziano, con %d anni di eta' ", eta3);  
    } else {  
        printf("Pino, Maurizio e Piochio hanno tutti la stessa eta' \n");  
    }  
  
}
```


