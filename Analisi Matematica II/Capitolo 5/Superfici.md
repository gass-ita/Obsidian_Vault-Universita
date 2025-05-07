Per procedere con la trattazione delle superfici è necessario rinfrescare il concetto di _prodotto vettoriale_.
Il prodotto vettoriale è una funzione che associa una coppia di vettori ad un terzo vettore.
In generale se abbiamo 2 vettori il prodotto scalare tra questi è:
$$
\left|\begin{pmatrix}
a_1, & a_2, & a_3 \\
b_1, & b_2, & b_3 \\
\vec e_1, & \vec e_2, & \vec e_3
\end{pmatrix}\right| = (a_2b_3 - a_3b_2,\, a_3b_1 -a_1 b_3,\,a_1b_2 - a_2 b_1)
$$
Questa operazione ha delle peculiarità particolari.
#### Proprietà
- $a \times b = - b \times a$ 
- $a \times b = \vec 0 \Leftrightarrow a = \lambda b \quad \text{o} \quad b = \lambda a$ 
- $(a \times b) \cdot c = (b \times c) \cdot a = (c \times a) \cdot b$
da cui consegue anche che:
- $a \times a = \vec 0$
- $a \times \lambda a = \vec 0$
- $(a \times b) \cdot a = 0$
osserva come l'ultima conseguenza deriva dal fatto che il prodotto scalare restituisce un vettore ortogonale ai due di partenza, quindi il prodotto scalare con uno dei due sarà sempre nullo.

Una superficie parametrica non è altro che una funzione:
$$A \subset \mathbb R^2$$
$$\phi: A \to \mathbb R^n \quad \text{continua}$$
E il suo sostegno non sarà altro che l'insieme dei punti che la compongono ovvero:
$$\phi(A) \subset \mathbb R^n$$
#### Insiemi Connessi e Disconnessi
Per definire la regolarità di una curva ci servirà in concetto di insieme _connesso_ e _disconnesso_

Un insieme si dice _disconnesso_ se:
Riesco a trovare due insiemi aperti che ricoprono l'insieme ma i due non hanno intersezione e allo stesso tempo hanno almeno un elemento in comune con l'insieme dato:
- $U \cap V = \emptyset$
-  $U \cup V \supseteq A$
- $A \cap U \neq \emptyset \quad \text{e} \quad A \cap V \neq \emptyset$
![[Pasted image 20250504141148.png]]
#### Superfici Regolari
Una superficie regolare è una funzione che va da un insieme $K = \bar A \subset \mathbb R^2$  dove $A$ è un insieme aperto, limitato e connesso con le seguenti proprietà:
$$\phi: K \to \mathbb R^3$$
- $\phi \in C^1(A)$
- $\phi \in C^0(K)$
- $\phi$ iniettiva su $A$
- $\frac{\partial \phi}{\partial x} \times \frac{\partial \phi}{\partial y} \neq \vec 0$
L'ultima proprietà sta a dire che i vettori tangenti alla superficie rispetto alla direzione $x$ e $y$ non sono mai paralleli tra loro o si annullano in qualche punto
Come nel caso delle _curve_ indichiamo con $\phi(K) \subset \mathbb R^3$ il sostegno della superficie.
### Teorema del Dini
Il teorema del dini ci permette di passare in modo agevole da una rappresentazione implicita di una curva ad una esplicita in un intorno di un punto quando si presentano determinate condizioni.
Questo teorema ci assicura della esistenza di una funzione che descrive il luogo degli zeri della nostra superficie come funzione di una singola variabile.
In realtà l'enunciato del teorema non si limita alle sole superfici ma si estende in modo più generale alle funzioni di classe $C^1$
#### Enunciato
Sia $F:A \subset \mathbb R^2 \to \mathbb R$ una funzione di classe $C^1$ 
Supponiamo $(x_0, y_0) \in A$ tale che $F(x_0, y_0) = 0$ supponiamo inoltre che la derivata parziale rispetto a $y$ non si annulli in $(x_0, y_0)$.
Sarà possibile trovare una funzione $g$ che va da un intorno di $x_0 = I$ ad un intorno di $y_0 = J$
$$I(x_0, y_0) = I \times J$$
$$g: I \to J \quad | \quad F(x, g(x)) = 0$$
Inoltre il teorema ci esplicita anche il valore della derivata prima di $g$:
$$g'(x) = -\frac{\frac{\partial F}{\partial x}(x, g(x))}{{\frac{\partial F}{\partial y}(x, g(x))}}$$
In particolare questo enunciato ci dice che sarà possibile esplicitare, almeno localmente, una superficie o in particolare, come visto nel _teorema delle curve come funzioni_, una curva come funzione di una variabile
### Esempio
Supponiamo di avere 
$$f(x; y) = x^2 + y^2 - 1$$
Il grafico di questa funzione rappresenta una circonferenza.
Sia $(x_0, y_0) = (0, 1)$
Osserviamo che la funzione $f$ si annulla in questo punto e che inoltre la derivata parziale rispetto alla $y$ è diversa da 0
Localmente, quindi, sarà possibile esplicitare il grafico di $f$ come una funzione dipendente solo da $x$:
$$y(x) = \sqrt{1 - x^2}$$
![[Pasted image 20250504144605.png]]Vediamo come il grafico mostrato rappresenta esattamente il luogo degli zeri della funzione viola