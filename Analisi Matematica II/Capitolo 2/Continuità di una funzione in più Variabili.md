Definiamo le funzioni che vanno da $\mathbb{R}^n \rightarrow \mathbb{R}$ 
Sia $A \subset \mathbb R^n$ un insieme aperto
$$
 f: A \to \mathbb{R}
$$
Se chiamiamo $x = (x_1, x_2, \ldots, x_n)$ si ha che
$$
f(x_1, x_2, \ldots, x_n) \in \mathbb R

$$
## Definizione di Continuità
Ricordiamo la definizione di continuità in un punto $\bar x$.
$f: A \rightarrow \mathbb R$ si dirà continua in $\bar x$ se:
$$
\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A\ \|x - \bar x\| < \delta \Rightarrow |f(x) - f(\bar x)| < \epsilon$$
in maniera equivalente potremo dire che $f$ è continua mediante successioni:
$$
\forall (x^k) \quad x^k \xrightarrow{k\rightarrow \infty} \bar{x} \Rightarrow f(x^k)  \xrightarrow{k\rightarrow \infty} 
f(\bar{x})$$
Osserviamo che con $x^k$ intendiamo una successione di vettori, evitiamo la scrittura $x_k$ poiché potrebbe confondere con _l'elemento k-esimo_ della del vettore $x$.

Possiamo definire la continuità anche per funzioni che vanno da $\mathbb R^n \to \mathbb R^m$ in maniera $\epsilon \delta$

$$
\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A \ \|x - \bar x\| < \delta \Rightarrow \|f(x) - f(\bar x)\| < \epsilon
$$
Osserviamo che un modo più semplice per verificare la continuità di una funzione di questo tipo in un punto basta verificare che ogni $f_k(x)$ sia continua
#### Dimostrazione
Partiamo con il dimostrare che se $f$ è continua in $\bar x$ allora ogni sua componente è continua:
Se $f$ è continua allora 
$$\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A \ \|x - \bar x\| < \delta \Rightarrow \|f(x) - f(\bar x)\| < \epsilon$$
Ma se $$ \|f(x) - f(\bar x)\| < \epsilon \Rightarrow \forall k \in (1, \dots, m) \quad |f(x) - f(k)| < \epsilon$$Poiché l'ipotenusa di un triangolo rettangolo è sempre maggiore o uguale di un qualunque suo cateto.

D'altra parte dimostriamo l'implicazione inversa
$$\forall k \in (1, \dots, m)  \quad\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A \ \|x - \bar x\| < \delta \Rightarrow |f_k(x) - f_k(\bar x)| < \epsilon$$
con $\epsilon$ fissato scegliamo $\bar \delta = \min_{k \leq m}(\delta)$ in questo modo si ha che:
$$\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A \ \|x - \bar x\| < \bar \delta \Rightarrow |f_k(x) - f_k(\bar x)| < \epsilon \quad \forall k \in (1, \dots, m) $$
ricordando che 
$$\|f(x) - f(\bar x)\| = \sqrt{\sum_{i = 1}^k\left( f(x) - f(\bar x)\right)^2}$$
Si nota facilmente che:
$$\sqrt{\sum_{i = 1}^k\left( f(x) - f(\bar x)\right)^2} < \sqrt{\sum_{i = 1}^k\left(\epsilon\right)^2}$$
e quindi che:
$$\|f(x) - f(\bar x)\| < \epsilon \sqrt k$$
$\square$

