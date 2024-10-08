
#### <font color="#31859b">Insiemi ed elementi.</font>
<font color="#b7dde8">Definizione</font> (Georg Cantor):
	Un insieme è una collezione di oggetti determinati e distinti della nostra percezione o del nostro pensiero, concepiti come un tutto unico. Tali oggetti si dicono elementi dell’insieme.

La definizione deve essere univoca e <u>non soggettiva</u>. Deve sempre essere possibile stabilire che un oggetto appartiene o non appartiene all’insieme.

#### <font color="#31859b">Rappresentazione degli insiemi</font>

- Gli insiemi si indicano con lettere maiuscole mentre i loro elementi con lettere minuscole.  
	- <font color="#b7dde8">Intensiva</font> o per proprietà 
		- A={numeri naturali dispari e minori di 4} 
		- è l'unica rappresentazione utile per descrivere elementi non finiti o finiti e non decidibili.
		
	- <font color="#b7dde8">Estensiva</font> o per elencazione
		- B={1,3} 
		
	- <font color="#b7dde8">Grafica</font> (diagrammi di Eulero Venn)

#### <font color="#31859b">Appartenenza</font> 
- Un oggetto è elemento di un insieme se la proprietà che caratterizza l’insieme è vera per quell’oggetto. 
	Altrimenti l’oggetto non appartiene all’insieme aA

#### <font color="#31859b">Cardinalità</font>
- Si dice cardinalità di un insieme la quantità dei suoi elementi. 
	"#A"
	
- A={numeri naturali maggiori di 4 e minori di 7} 
	"#A"= 2

#### <font color="#31859b">Uguaglianza</font>
- Due insiemi sono uguali se hanno gli stessi elementi.
	A=B  x,(xA  xB)

	A={insieme dei numeri naturali minori di 5} B={x|x  N  x < 5}

#### <font color="#31859b">Insieme vuoto</font>
- Si dice insieme vuoto l’insieme che non contiene alcun elemento.
	={x|xA  x A}

	A = {numeri naturali dispari minori di 1} = 
	L’insieme vuoto ha cardinalità 0

#### <font color="#31859b">Sottoinsiemi</font>
- Un insieme A è sottoinsieme di un insieme B se tutti gli elementi di A sono anche elementi di B.
	AB x,(xA → xB)

	Sottoinsiemi propri
	Sottoinsiemi impropri: A, 
	<font color="#3f3f3f">(esempi nelle slide)</font>
#### <font color="#31859b">Insieme delle parti</font>
- L’insieme delle parti di un insieme A è un insieme i cui elementi sono tutti i sottoinsiemi, propri ed impropri dell’insieme A.

#### <font color="#31859b">Unione</font>
- Si dice insieme unione degli insiemi A e B un insieme C avente come elementi tutti gli elementi di A o di B, presi una sola volta.
	AB={x|xA  xB}

	A={numeri naturali minori di 3}       2,1
	B={numeri naturali dispari minori di 4}      3,1
	C=AB={numeri naturali minori di 4}      3,2,1

	proprietà <font color="#3f3f3f">(nelle slide)</font>
	- Commutativa
	- Associativa
	- Assorbimento
	- "somma con 0"

#### <font color="#31859b">Intersezione</font>
- Si dice insieme intersezione degli insiemi A e B un insieme C avente come elementi tutti gli elementi di A e di B.
	AB={x|xA  xB}
es.
- A={numeri naturali minori di 4} 
- B={numeri naturali compresi tra 1 e 7} 
- C= AB={numeri naturali compresi tra 1 e 4}

	proprietà 	<font color="#3f3f3f">(nelle slide)</font>
	- commutativa
	- associativa
	- assorbimento
	- "zero nella moltiplicazione"
	- distributiva tra intersezione e unione

#### <font color="#31859b">Differenza</font>
- Si dice insieme differenza degli insiemi A e B un insieme C avente come elementi tutti gli elementi di A che non appartengano a B.
	A\B={x|xA  xB}

es.
- A={numeri naturali dispari minori di 4}
- B={numeri naturali compresi tra 2 e 7}
- C=A\B={1}

	##### <font color="#31859b">Complementazione</font>
	- Se B è un sottoinsieme di A l’operazione di differenza prende il nome di complementazione ma si definisce allo stesso modo.
	-  Si dice complementare di B rispetto ad A l’insieme degli elementi di A che non appartengono a B.

	L’insieme rispetto al quale stiamo effettuando l’operazione di complementazione prende il nome di insieme <font color="#92cddc">universo</font> U.

	<font color="#92cddc">Attenzione</font>: E’ sempre necessario precisare rispetto a quale insieme universo stiamo effettuando la complementazione.
	Esempio: CRN  CQN

	es
		A={numeri naturali minori di 4} 
		B={numeri naturali compresi tra 2 e 4} 
		CaB={1,2}

#### <font color="#31859b">Il prodotto cartesiano</font>
- Si definisce coppia ordinata ogni insieme di due elementi in cui si specifica l’ordine con cui compaiono i due oggetti.
- (a,b)
- Il prodotto cartesiano AxB è l’insieme delle coppie ordinate (a,b) con a appartenente ad A e b appartenente a B. 
	- AXB={(a,b)| aA  bB}
- La cardinalità di AxB è il prodotto delle cardinalità di A e di B
	##### <font color="#31859b">Rappresentazione</font> 
	- <font color="#3f3f3f">(per la rappresentazione cartesiana non ci sono le frecce nelle slide per la mancanza di ordine degli elementi dell'insieme)</font>

	##### <font color="#31859b">Proprietà</font>
	- ~~commutativa~~
	- ~~associativa~~
	- distributiva
	- i prodotti cartesiani con l'insieme vuoto restituiscono sempre un insieme vuoto
- es per casa
	- Dati gli insiemi A = {le lettere della parola rosa} B = {*,#,@} Determinare il prodotto cartesiano BxA e farne una rappresentazione cartesiana.
	- Dato il seguente prodotto cartesiano L=AxB={(a,1),(b,1)} determinare gli insiemi A e B
	- A={x|xN  x2-x-6=0} B={x|xZ  (2x-1)(x2-x-6)=0} Rappresentare A e B per elencazione. I due insiemi sono uguali? A è sottoinsieme di B? Determinare P(B), AB, AB, A\B, AxB. Posso determinare CBA?
	- bo gli altri sono nelle slide

	##### <font color="#31859b">Insiemi e logica</font>

	esiste una corrispondenza tra operazioni insiemistiche e connettivi(uso quantificatori). 
	<font color="#3f3f3f">(slide 40)</font>
