- modulo e segno
	per i numeri negativi, convenzionalmente si fa iniziare il numero binario con 1, per la sua versione positiva si antepone uno zero

	per fare la somma tra numeri, andiamo ad utilizzare solo il modulo del numero, escludendo quindi il primo bit (utilizzato per indicare la positività o la negatività del numero)

	Il tipo di operazione che svolgiamo varierà a seconda dei valori di a e b.
	- +a+b, semplice somma tra i due moduli
	- +a-b con |a|>|b|, sottrazione tra il modulo di a e quello di b, risultato positivo
	- +a-b con |a|<|b|, sottrazione tra il modulo di b e quello di a, con risultato negativo

- rappresentazione in complemento
	es. complemento a 9 di 2607.
	prendo tante cifre, ciascuna uguale a 9, quante le cifre del numero di partenza, in questo caso 9999
	per ottenere il complemento a nove vado quindi a sottrarre ad ogni cifra uguale a nove la sua rispettiva cifra iniziale
	(9999 - 2607 = 7392)

	per calcolare il complemento a 10 si calcola il complemento a 9 e poi si aggiunge 1 all'ultima cifra

	es. sottrazione in complemento 10
	
	2876-41= 2835

	sommiamo il minuendo col complemento a 10 del sottraendo, estendendolo al numero di cifre del minuendo (41 -> 9959)

	2876+
	9959=
	12835, il riporto viene scartato, quindi torniamo a 2835. 