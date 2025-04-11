Consideriamo $f: \mathbb R \to \mathbb R$ si definisce _derivata parziale_ di $f$ nel punto $x_0$ rispetto alla variabile $x_i$ il limite, se esiste finito, del rapporto incrementale
$$\frac{\partial f}{\partial x_i} (x_0) := \lim_{h \to 0}\frac{f(x_0 + h e_i) - f(x_0)}{h}$$
Dove $e_i$ è il versore della variabile $x_i$ 

$f$ si dirà _derivabile_ in $\bar x$ se ammette derivate parziali rispetto a tutte le variabili $x_i$
#### Osservazione
rispetto alle funzioni in una variabile, quando lavoriamo in $\mathbb R ^n$ non è sempre vera la seguente implicazione
$$
	 \text{derivabilità} \centernot \implies \text{continuità}$$
 Infatti, una funzione può essere derivabile in un punto ma non continua in quel punto.
##### Esempio
Sia:
$$f(x, y) = \begin{cases}\frac{xy}{x^2+y^2} & (x, y) \neq (0, 0) \\ 0 & (x, y) = (0, 0)\end{cases}$$
Verifichiamo la continuità
$$\lim_{(x,y)\to(0,0)} \frac{xy}{x^2+y^2}$$
Prendiamo una successione di punti tendente a $(0,0)$ come $(\frac{1}{n}, \frac{1}{n})$ e $(0, \frac{1}{n})$ osserviamo subito che per $n \to \infty$ con la prima parametrizzazione $f(\frac{1}{n}, \frac{1}{n}) \to \frac{1}{2}$ mentre $f(0, \frac{1}{n}) \to 0$.
Quindi la funzione _non_ è continua.
Osserviamo invece il comportamento per quanti riguarda la derivabilità su $(0, 0)$ lungo gli assi la funzione è _identicamente nulla_ e quindi risulta che 
$\nabla f(0, 0) = (0, 0)$
 Pertanto, la funzione è derivabile in $(0, 0)$, ma non continua in quel punto.
 
### Gradiente di una funzione
Sia $f: \mathbb R^n \to \mathbb R$ definiamo _l'hessiano_ di $f$ come il _vettore riga_ contenente le derivate parziali di $f$ rispetto a tutte le variabili $x_i$, cioè il vettore $\left( \frac{\partial f}{\partial x_1}, \frac{\partial f}{\partial x_2}, \dots, \frac{\partial f}{\partial x_n} \right)$.
$$
\nabla f(\bar x) = \left( \frac{\partial f}{\partial x_1} (\bar x), \frac{\partial f}{\partial x_2}  (\bar x), \dots, \frac{\partial f}{\partial x_n} (\bar x) \right)$$

Se $f: \mathbb R^n \to \mathbb R^m$ _l'hessiano_ è definibile come la matrice $\nabla f \in M[m \times n]$ 
$$
 \nabla f = \begin{pmatrix} \frac{\partial f_1}{\partial x_1} & \cdots & \frac{\partial f_1}{\partial x_n} \\ \vdots & \ddots & \vdots \\ \frac{\partial f_m}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_n} \end{pmatrix}
$$
Quando $f$ è di questo tipo l'hessiano viene anche chiamato matrice jacobiana.
### Derivata direzionale di una funzione
Possiamo definire un tipo di derivata più generale rispetto alle derivate parziali ovvero le derivate direzionali.
Dato un versore $\mathbf v \in \mathbb R$ e data una funzione $f : A \subset \mathbb{R}^n \to \mathbb{R}$ la derivata direzionale nel punto $\bar x \in A$ è definita da:
$$
\frac{\partial f}{\partial \mathbf v}(\bar x) := \lim_{h \to 0} \frac{f(\bar x + \mathbf v h) - f(\bar x)}{h}
$$
 La derivata direzionale è la velocità di variazione della funzione lungo la direzione specificata dal versore $\mathbf v$ nel punto $\bar x$.

### Funzione Differenziabile
 Una funzione  $f: A \subset \mathbb{R}^n \to \mathbb{R}$  è detta _differenziabile_ in un punto $\bar{x}$ se esiste un’approssimazione lineare della funzione vicino a quel punto, ovvero se si può scrivere:
 $$
 \lim_{x \to \bar x} \frac{f(x) - f(\bar x) - \nabla f(\bar x) (x - \bar x)}{\| x - \bar x\|} = 0
$$
Ovvero, utilizzando la teoria degli _o-piccoli_:
$$
f(x) = f(\bar x) + \nabla f(\bar x)(x - \bar x) + o({\| x - \bar x\|})$$
Questa proprietà implica che la funzione è continua in $\bar{x}$ e che le derivate direzionali sono calcolabili utilizzando la formula $\frac{\partial f}{\partial \mathbf v}(\bar x) = \nabla f(\bar x) \cdot \mathbf v$ 
##### Dimostrazione
- $f$ è [[Continuità di una funzione in più Variabili |continua]] in $\bar x$ 
dalla definizione di continuità si deve avere che:
$$\forall \epsilon > 0, \quad \exists \delta > 0: \quad \forall x \in A\ \|x - \bar x\| < \delta \Rightarrow |f(x) - f(\bar x)| < \epsilon$$
Osserviamo che:
$$|f(x) - f(\bar x)| = |f(x) - f(\bar x) - \nabla f(\bar x)(x - \bar x) + \nabla f(\bar x)(x - \bar x) | \leq$$
$$\leq \underbrace{|f(x) - f(\bar x) - \nabla f(\bar x)(x - \bar x) |}_a + \underbrace{| \nabla f(\bar x)(x - \bar x) |}_b$$
osserviamo che se $f$ è [[Derivabilità di una Funzione in più Variabili#Funzione Differenziabile|differenziabile]] il primo addendo $(a)$ tende a zero e quindi 
$$\exists \delta_a : \quad \forall x \in A\ \|x - \bar x\| < \delta_a \Rightarrow |f(x) - f(\bar x) - \nabla f(\bar x)(x - \bar x) | < \epsilon$$
Inoltre anche il secondo termine $(b)$ è infinitesimo perché:
$$| \nabla f(\bar x)(x - \bar x) | \leq \| \nabla f(\bar x)\|\|(x - \bar x)\| \to 0$$
dalla definizione di limite si ha la tesi
$\square$
- $\frac{\partial f}{\partial \mathbf v}(\bar x) = \nabla f(\bar x) \cdot \mathbf v$ 
Ricordiamo la definizione di derivata direzionale:
$$\lim_{h \to 0} \frac{f(\bar x + \mathbf v h) - f(\bar x)}{h}$$
chiamiamo $x = \bar x + \mathbf v h$ si ha che $x \to \bar x$
Per la differenziabilità si ha quindi che:
$$\lim_{h \to 0} \frac{f(\bar x + \mathbf v h) - f(x) - \nabla f(\bar x)(\mathbf v h)}{\|\mathbf v h\|} = 0$$
Si ha quindi che:
$$\lim_{h \to 0} \frac{f(\bar x + \mathbf v h) - f(x) - \nabla f(\bar x)(\mathbf v h)}{|h|\|\mathbf v\|} = 0$$
Osservo che:
$$\frac{\nabla f (\bar x)(\mathbf v h)}{|h|} = sign(h) \nabla f(\bar x) \mathbf v$$
e quindi che 
$$
 \lim_{h \to 0^+} \frac{f(\bar x + \mathbf v h) - f(\bar x)}{h} = \nabla f(\bar x)  \mathbf v \quad\text{e}\quad \lim_{h \to 0^-} \frac{f(\bar x + \mathbf v h) - f(\bar x)}{h} = \nabla f(\bar x) \mathbf v$$
da cui si ha la tesi.
$\square$
In sintesi, la differenziabilità di una funzione implica la continuità e consente di calcolare le derivate direzionali attraverso il prodotto scalare con il gradiente, fornendo così un quadro completo del comportamento locale della funzione.
$$
f \text{  è differenziabile in } \bar{x} \Rightarrow \text{ è continua e } \frac{\partial f}{\partial \mathbf v}(\bar x) = \nabla f(\bar x) \cdot \mathbf v$$


### Teorema del Differenziale Totale
test
