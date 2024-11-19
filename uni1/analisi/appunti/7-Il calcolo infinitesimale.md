
Il calcolo infinitesimale è una branca della matematica che si occupa dello studio del cambiamento. Uno degli strumenti fondamentali del calcolo infinitesimale è l'operazione di limite. L'operazione di limite serve a descrivere il comportamento di una funzione nei pressi di un punto di accumulazione per il suo dominio. In pratica, ci permette di capire cosa succede a una grandezza dopo un lungo periodo di tempo o per valori particolari della variabile indipendente.

### Limite Finito per x→x₀

Consideriamo una funzione $f(x)$ e un punto di accumulazione $x_0$ per il suo dominio. Diciamo che il limite di $f(x)$ per $x$ che tende a $x_0$ è uguale a $l$ (un numero reale) se per ogni valore di $\epsilon > 0$ esiste un valore di $\delta_\epsilon > 0$ tale che, se la distanza tra $x$ e $x_0$ è minore di $\delta_\epsilon$, allora la distanza tra $f(x)$ e $l$ è minore di $\epsilon$.

Possiamo scrivere questo concetto matematicamente come:

$$ \lim_{x \to x_0} f(x) = l $$

**Attenzione**: il punto di accumulazione $x_0$ potrebbe non appartenere al dominio di $f(x)$, quindi $f(x_0)$ potrebbe non essere definita. Inoltre, anche se il limite esiste, non è detto che $f(x_0)$ sia uguale a $l$.

**Esempio**:

Verificare il limite:

$$ \lim_{x \to 3} (x + 2) = 5 $$

Dalla definizione di limite, questo è vero se per ogni $\epsilon > 0$ esiste un $\delta_\epsilon > 0$ tale che:

$$ |x - 3| < \delta_\epsilon \Rightarrow |(x + 2) - 5| < \epsilon $$

Semplificando la seconda disuguaglianza, otteniamo:

$$ |x - 3| < \epsilon $$

Quindi, possiamo scegliere $\delta_\epsilon = \epsilon$. Questo dimostra che il limite è corretto.

### Limite Infinito per x→x₀

Se per ogni valore di $M > 0$ esiste un valore di $\delta_M > 0$ tale che, se la distanza tra $x$ e $x_0$ è minore di $\delta_M$, allora il valore assoluto di $f(x)$ è maggiore di $M$, diciamo che il limite di $f(x)$ per $x$ che tende a $x_0$ è infinito.

**Esempio**:

Verificare il limite:

$$ \lim_{x \to 3} f(x) = +\infty $$

Dalla definizione di limite infinito, questo è vero se per ogni $M > 0$ esiste un $\delta_M > 0$ tale che:

$$ |x - 3| < \delta_M \Rightarrow |f(x)| > M $$

### Asintoti

Un asintoto è una retta a cui il grafico della funzione tende. Esistono tre tipi di asintoti:

- **Asintoto verticale**: si ha un asintoto verticale di equazione $x = x_0$ se:

$$ \lim_{x \to x_0} f(x) = \infty $$

- **Asintoto orizzontale**: si ha un asintoto orizzontale di equazione $y = l$ se:

$$ \lim_{x \to \infty} f(x) = l $$

- **Asintoto obliquo**: si ha un asintoto obliquo di equazione $y = mx + q$ se esistono e sono finiti i seguenti limiti:

$$ \lim_{x \to \infty} [f(x) - (mx + q)] = 0 $$

$$ m = \lim_{x \to \infty} \frac{f(x)}{x} $$

$$ q = \lim_{x \to \infty} [f(x) - mx] $$

### Limite Destro e Sinistro

Il limite destro di $f(x)$ per $x$ che tende a $x_0$ si indica con:

$$ \lim_{x \to x_0^+} f(x) $$

e rappresenta il comportamento della funzione quando $x$ si avvicina a $x_0$ da destra.

Il limite sinistro di $f(x)$ per $x$ che tende a $x_0$ si indica con:

$$ \lim_{x \to x_0^-} f(x) $$

e rappresenta il comportamento della funzione quando $x$ si avvicina a $x_0$ da sinistra.

**Condizione necessaria e sufficiente** perché esista il limite di $f(x)$ per $x$ che tende a $x_0$ è che esistano e siano uguali il limite destro e il limite sinistro.

### Teorema di Unicità del Limite

Se esiste il limite di una funzione $f(x)$ per $x$ che tende a un punto di accumulazione $x_0$, allora questo limite è unico.

### Teorema della Permanenza del Segno

Se il limite di una funzione $f(x)$ per $x$ che tende a un punto di accumulazione $x_0$ è positivo, allora esiste un intorno di $x_0$ in cui la funzione è positiva.

### Operazioni con i Limiti

Le operazioni con i limiti si comportano in modo simile alle operazioni con i numeri reali, ma con alcune eccezioni che portano alle forme indeterminate. Ecco un riepilogo delle operazioni possibili, con le relative dimostrazioni quando applicabile:

### Somma di Limiti

Se $\lim_{x \to x_0} f(x) = l$ e $\lim_{x \to x_0} g(x) = m$, allora $\lim_{x \to x_0} [f(x) + g(x)] = l + m$.

**Dimostrazione**:

Per la definizione di limite, per ogni $\epsilon > 0$ esistono $\delta_1 > 0$ e $\delta_2 > 0$ tali che:

- Se $|x - x_0| < \delta_1$, allora $|f(x) - l| < \epsilon / 2$.
- Se $|x - x_0| < \delta_2$, allora $|g(x) - m| < \epsilon / 2$.

Scegliendo $\delta = \min(\delta_1, \delta_2)$, se $|x - x_0| < \delta$, allora entrambe le disuguaglianze precedenti sono vere. Utilizzando la disuguaglianza triangolare, otteniamo:

```
|f(x) + g(x) - (l + m)| = |(f(x) - l) + (g(x) - m)|
                         ≤ |f(x) - l| + |g(x) - m|
                         <  ε/2 + ε/2
                         = ε
```

Questo dimostra che $\lim_{x \to x_0} [f(x) + g(x)] = l + m$.

### Differenza di Limiti

Se $\lim_{x \to x_0} f(x) = l$ e $\lim_{x \to x_0} g(x) = m$, allora $\lim_{x \to x_0} [f(x) - g(x)] = l - m$. La dimostrazione è analoga a quella per la somma.

### Prodotto di Limiti

Se $\lim_{x \to x_0} f(x) = l$ e $\lim_{x \to x_0} g(x) = m$, allora $\lim_{x \to x_0} [f(x) \cdot g(x)] = l \cdot m$.

**Dimostrazione (idea generale):**

La dimostrazione si basa sulla manipolazione algebrica e sulla definizione di limite. Si sfrutta il fatto che, dato che f(x) e g(x) hanno limite finito, si possono trovare intorni di x₀ in cui f(x) e g(x) sono limitate.

### Potenza di Limiti

Se $\lim_{x \to x_0} f(x) = l$, allora $\lim_{x \to x_0} [f(x)]^n = l^n$ per ogni intero positivo n. La dimostrazione può essere fatta per induzione su n.

### Divisione di Limiti

Se $\lim_{x \to x_0} f(x) = l$ e $\lim_{x \to x_0} g(x) = m$ con $m \neq 0$, allora $\lim_{x \to x_0} [f(x) / g(x)] = l / m$.

**Dimostrazione (idea generale):**

Si dimostra prima il caso per l'inverso di g(x), ovvero 1/g(x), e poi si usa il fatto che il limite del prodotto è il prodotto dei limiti. Per l'inverso, si sfrutta il fatto che g(x) è diversa da zero in un intorno di x₀.

### Inverso di un Limite

Se $\lim_{x \to x_0} f(x) = l$ con $l \neq 0$, allora $\lim_{x \to x_0} [1 / f(x)] = 1 / l$. La dimostrazione è un caso particolare della divisione di limiti.

### Forme Indeterminate

Le seguenti operazioni con i limiti possono portare a risultati indefiniti, noti come **forme indeterminate**:

- $+\infty - \infty$
- $0 \cdot \infty$
- $\infty / \infty$
- $0 / 0$
- $0^0$

Per risolvere queste forme indeterminate, sono necessari metodi specifici come la scomposizione, la razionalizzazione, la regola di de l'Hôpital, o altri .

### Funzioni Continue

Una funzione $f(x)$ si dice **continua** in un punto $x_0$ del suo dominio se il limite di $f(x)$ per $x$ che tende a $x_0$ è uguale a $f(x_0)$.

### Funzioni Discontinue

Una funzione $f(x)$ si dice **discontinua** in un punto $x$ del suo dominio se non è continua in quel punto. Esistono tre tipi di discontinuità:

- **Discontinuità di prima specie**: il limite destro e il limite sinistro esistono finiti ma sono diversi.
- **Discontinuità di seconda specie**: almeno uno tra il limite destro e il limite sinistro è infinito o non esiste.
- **Discontinuità di terza specie**: il limite destro e il limite sinistro esistono finiti e sono uguali, ma sono diversi da $f(x)$.

### Teorema di Weierstrass

Se una funzione $f(x)$ è continua in un intervallo chiuso e limitato $[a, b]$, allora ammette massimo e minimo assoluto in quell'intervallo.

### Limite di Funzione Composta

Siano $f(x)$ e $g(x)$ due funzioni. Se esiste il limite di $f(x)$ per $x$ che tende a $x_0$ ed è uguale a $l$, e se esiste il limite di $g(y)$ per $y$ che tende a $l$ ed è uguale a $L$, allora esiste il limite di $g(f(x))$ per $x$ che tende a $x_0$ ed è uguale a $L$.

### Infiniti e Infinitesimi

Una funzione $f(x)$ si dice **infinitesima** in un punto $x_0$ se il suo limite per $x$ che tende a $x_0$ è uguale a $0$.

Una funzione $f(x)$ si dice **infinita** in un punto $x_0$ se il suo limite per $x$ che tende a $x_0$ è infinito.

### Confronto tra Infiniti e Infinitesimi

È possibile confrontare tra loro infiniti e infinitesimi per determinare il loro ordine.

### Complessità Computazionale

La complessità computazionale si occupa dello studio delle risorse (tempo di calcolo e memoria) necessarie per l'esecuzione di un algoritmo. Si analizza come varia il tempo di esecuzione di un programma al variare dei dati su cui opera.

Si utilizzano diverse notazioni per indicare la complessità computazionale, come ad esempio:

- O(1): costante
- O(n): lineare
- O(log n): logaritmica
- O(n log n): N-logaritmica
- O(n^2): polinomiale
- O(2^n): esponenziale
- O(n!): fattoriale




## Operazioni con i Limiti e Disuguaglianza Triangolare



### Disuguaglianza Triangolare

La disuguaglianza triangolare afferma che la somma delle lunghezze di due lati di un triangolo è sempre maggiore o uguale alla lunghezza del terzo lato. In termini matematici, per qualsiasi numero reale $a$ e $b$:

$$ |a + b| ≤ |a| + |b| $$

La disuguaglianza triangolare è utilizzata in diverse dimostrazioni relative ai limiti, come ad esempio nella dimostrazione della somma di limiti.

Le fonti fornite non approfondiscono ulteriormente la disuguaglianza triangolare. Se si desidera una trattazione più dettagliata, si consiglia di consultare un testo di analisi matematica o di algebra lineare.