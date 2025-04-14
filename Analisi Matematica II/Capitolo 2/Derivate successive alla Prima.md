Così come abbiamo definito la [[Derivabilità di una Funzione in più Variabili|derivata prima direzionale]] come il _limite del rapporto incrementale lungo una direzione_ di una funzione in più variabili, ottenendo così una nuova funzione $\frac{\partial f}{\partial x_i}$ possiamo _derivare ulteriormente_ questa funzione ottenendo _derivate seconde, terze_ e così via.
Infatti ogni derivata direzionale di $f$, $\frac{\partial f}{\partial x_i}$, potrebbe ammettere derivate parziali per ogni altra variabile $x_i$.
##### Definizione (derivate seconde)
Sia $f: A \subset \mathbb R^n \to \mathbb R^k$ una funzione con $A$ aperto, prendiamo $i \in \{1, \dots, n\}$ e supponiamo che esista $\frac{\partial f}{\partial x_i}$, diremo che $f$ ammette derivata seconda in $\bar x$ rispetto a $x_i$ e $x_j$ se $\frac{\partial f}{\partial x_i}$ è derivabile rispetto a $x_j$ in $\bar x$ e scriveremo:
$$\frac{\partial^2 f}{\partial x_i \partial x_j}(\bar x) := \lim_{h \to 0} \frac{\frac{\partial f}{\partial x_i}(\partial + h e_j) - \frac{\partial f}{\partial x_i}(\bar x)}{h}$$
Nel caso in cui $i = j$ scriveremo semplicemente:
$$\frac{\partial^2 f}{\partial^2 x_i}(\bar x)$$
##### Definizione (Hessiano di una Funzione)
Se, in una funzione derivabile, tutte le sue derivate parziali sono derivabili in $\bar x$ si può definire l'Hessiano di una funzione come
$$\nabla^2f(\bar x) = \begin{pmatrix} \frac{\partial^2 f}{\partial x_1^2}(\bar x) & \frac{\partial^2 f}{\partial x_1 \partial x_2}(\bar x) & \cdots & \frac{\partial^2 f}{\partial x_1 \partial x_n}(\bar x) \\ \frac{\partial^2 f}{\partial x_2 \partial x_1}(\bar x) & \frac{\partial^2 f}{\partial x_2^2}(\bar x) & \cdots & \frac{\partial^2 f}{\partial x_2 \partial x_n}(\bar x) \\ \vdots & \vdots & \ddots & \vdots \\ \frac{\partial^2 f}{\partial x_n \partial x_1}(\bar x) & \frac{\partial^2 f}{\partial x_n \partial x_2}(\bar x) & \cdots & \frac{\partial^2 f}{\partial x_n^2}(\bar x) \end{pmatrix} \in M_{n, n}$$
L'Hessiano, come con le derivate seconde in _Analisi I_ ci fornisce informazioni su massimi e minimi della funzione.
L'Hessiano è fondamentale per determinare la natura dei punti critici di una funzione, poiché permette di analizzare la concavità e identificare se un punto è un massimo, un minimo o un punto di sella

---
Molto spesso l'Hessiano di una funzione è una matrice simmetrica, in alcune condizioni si ha infatti che:
$$\frac{\partial^2 f}{\partial x_i \partial x_j}(\bar x) = \frac{\partial^2 f}{\partial x_j \partial x_i}(\bar x)$$
Si ha infatti il seguente teorema:
### Teorema di Schwarz
Sia $f$ una funzione $f: A \subset \mathbb R^n \to \mathbb R$ che ammette
$$\frac{\partial^2 f}{\partial x_i \partial x_j}(\bar x) \quad \text{e} \quad \frac{\partial^2 f}{\partial x_j \partial x_i}(\bar x)$$
e supponiamo che tali derivate siano _continue_ allora si ha che
$$\frac{\partial^2 f}{\partial x_i \partial x_j}(\bar x) = \frac{\partial^2 f}{\partial x_j \partial x_i}(\bar x)$$
###### Dimostrazione
Dimostreremo il teorema per $n = 2$
Supponiamo, quindi, che $f$ dipenda da due variabili $x_1$ e $x_2$.
Vogliamo dimostrare quindi che:
$$\frac{\partial^2 f}{\partial x_1 \partial x_2}(\bar x_1, \bar x_2) = \frac{\partial^2 f}{\partial x_2 \partial x_1}(\bar x_1, \bar x_2)$$
Chiamiamo il punto $x \in A$ dove $x = (x_1, x_2)$ e chiamiamo la differenza $h := x_1 - \bar x_1$ e $k := x_2 - \bar x_2$
Nella definizione di derivata manderemo $h \to 0$ e $k \to 0$ avremo quindi che $x_1 \to \bar x_1$ e $x_2 \to \bar x_2$.
Definiamo adesso la funzione $G(h, k)$
$$G(h, k) = \boxed{f(\bar{x}_1 + h, \bar{x}_2 + k) - f(\bar{x}_1 + h, \bar{x}_2)} \boxed{+ f(\bar{x}_1, \bar{x}_2)  - f(\bar{x}_1, \bar{x}_2 + k)}$$
Possiamo scrivere la funzione $G(h, k)$ può essere espressa mediante funzioni in una singola variabile:
Se chiamo ad esempio:
$$F(t) := f(t, x_2 + k) - f(t, x_2)$$
Possiamo esprimere $G(h, k)$ come:
$$G(h, k) = F(\bar x_1 + h) - F(\bar x_1)$$
Per il teorema di Lagrange posso esprimere questa differenza come:
$$F(\bar x_1 + h) - F(\bar x_1) = F'(\xi_1) h \quad \xi_1 \in \{\bar x_1, \bar x_1 + h\}$$
Osserviamo però che $F'$ è esprimibile come:
$$F'(t) = \frac{d}{dt}f(t, x_2 + k) - \frac{d}{dt}f(t, x_2)$$
Ma poiché la t occupa sempre la prima variabile $F'$ è esprimibile anche come
$$F'(t) = \frac{\partial}{\partial x_1}f(x_1, \bar x_2 + k) - \frac{\partial}{\partial x_1}f(x_1, \bar x_2)$$
Si ha quindi che:
$$G(h, k) = \left(\frac{\partial}{\partial x_1}f(\xi_1, \bar x_2 + k) - \frac{\partial}{\partial x_1}f(\xi_1, \bar x_2)\right )h$$
Procedendo in un modo simile possiamo definire la funzione $H$
$$H(s) = \frac{\partial}{\partial x_1}f(\xi_1, s)$$
E osservare che:
$$\frac{d}{ds}H(s) = \frac{\partial^2 f}{\partial x_1 \partial x_2}(\xi_1, s)$$
Quindi otteniamo che, applicando nuovamente _Lagrange_
$$G(h, k) = H(\bar x_2 + k) - H (\bar x_2)$$
e quindi che:
$$G(h, k) = \frac{\partial^2 f}{\partial x_1 \partial x_2}(\xi_1, \xi_2) hk \quad \xi_2 \in \{\bar x_2, \bar x_2+k\}$$
Procedendo in modo analogo con gli opportuni aggiustamenti otteniamo che:
$$G(h, k) = \frac{\partial^2 f}{\partial x_2 \partial x_1}(\eta_1, \eta_2) hk \quad \eta_1 \in \{\bar x_1, \bar x_1 + h\} \quad \eta_2 \in \{\bar x_2, \bar x_2 + k\}$$
e quindi che 

$$\frac{\partial^2 f}{\partial x_1 \partial x_2}(\xi_1, \xi_2) = \frac{\partial^2 f}{\partial x_2 \partial x_1}(\eta_1, \eta_2)$$
in conclusione per $h \to 0$ e $k \to 0$ si ha che $\xi_1, \eta_1 \to \bar x_1$ e $\xi_2,\eta_2 \to \bar x_2$ si ha che per la continuità di $\frac{\partial^2 f}{\partial x_1 \partial x_2}$ e $\frac{\partial^2 f}{\partial x_2 \partial x_1}$ si ha la tesi.
$\square$
