### Definizione

introduciamo le funzioni $e_k$ dove $k \in \mathbb{Z}$ definite nel seguente modo
$$e_k(x) = \begin{cases}1 & k = 0 \\ cos(kx) & k > 0 \\ sin(-kx) & k < 0\end{cases}$$

##### osservazione

è semplice osservare che:
$$\int_{-\pi}^\pi e_k(x) \cdot e_h(x) dx = \begin{cases}0 & k \neq h \\ 2\pi & k = h = 0 \\ \pi & k = h \neq 0\end{cases}$$

### Definizione (funzioni periodiche)

sia $f: \mathbb{R} \rightarrow \mathbb{R}$, $f$ è detta periodica con periodo $T > 0$ se
$$f(x + T) = f(x)$$
se $f: [-\pi; \pi) \rightarrow \mathbb{R}$ possiamo definire una estensione periodica con periodo $T = 2\pi$

$$\overline{f}(x) = f(x - 2\pi m) \quad \text{for} \quad x \in [(2m-1) \pi; (2m + 1) \pi)$$

### Definizione (funzioni continue a tratti)

Diremo che la funzione $f$ è _continua a tratti_ sull'intervallo $[a; b]$ se:
esistono

$$a = t_0 < t_1 < \ldots < t_n = b$$
tali che la funzione risulta di classe $C^0$ sugli intervalli $(t_i; t_{i + 1}) \quad \forall i \in \{1, 2, \ldots, n\}$  

ed inoltre
$$\exists \lim_{h\rightarrow 0^\pm} f(x) \in \mathbb{R}$$

#### Definizione

Diremo che $f$ è di classe $C^1$ a tratti sull'intervallo $[a, b]$ se:
$\forall i \quad (t_i,t_{i+1})$ $f$ è di classe $C^1$ e inoltre

1) $\exists \lim_{h \rightarrow 0^+} \frac{f(t_i+h) - f(t_i^+)}{h} = f'(t_i^+) \in \mathbb{R}$
2) $\exists \lim_{h \rightarrow 0^-} \frac{f(t_i+h) - f(t_i^-)}{h} = f'(t_i^-) \in \mathbb{R}$
3) se chiamo $f': [t_i; t_{i+ 1}] \rightarrow \mathbb{R}$ dove $$f'(t) = \begin{cases}f'(t_i^-) & t = t_i \\ f'(t) & t \in (t_i, t_{i+1})\\ f'(t_i^+) & t = t_{i+1}\end{cases}$$
 $f'$ deve risultare continua su $[t_i, t_{i+1}]$

### Coefficienti di Fourier e la Serie di Fourier

Data una funzione $f: [-\pi; \pi] \rightarrow \mathbb{R}$ una funzione integrabile su $[-\pi; \pi]$ definiamo i suoi _coefficienti di Fourier_ $a_0, a_k, b_k \quad k > 0 \quad k \in \mathbb(N)$

$$a_0 = \frac{1}{\pi}\int_{-\pi}^\pi f(x) \cdot e_0(x) dx = \frac{1}{\pi}\int_{-\pi}^\pi f(x)dx $$
$$a_k = \frac{1}{\pi}\int_{-\pi}^\pi f(x) \cdot e_k(x) dx = \frac{1}{\pi}\int_{-\pi}^\pi f(x) \cdot cos(kx) dx $$
$$b_k = \frac{1}{\pi}\int_{-\pi}^\pi f(x) \cdot e_{-k}(x) dx = \frac{1}{\pi}\int_{-\pi}^\pi f(x) \cdot sin(kx) dx $$

Definiamo adesso la _Serie di Fourier_ come:
$$\frac{a_0}{2} + \sum_{k=0}^{\infty}a_k cos(kx) + b_k sin(kx)$$
e le somme parziali $S_n(x)$ come
$$S_n(x) = \frac{a_0}{2} + \sum_{k=0}^{n}a_k cos(kx) + b_k sin(kx)$$

### Lemma

$\forall t \in \mathbb{R}$ si ha che
$$\frac{1}{2} + \sum_{i=1}^{n} cos(it) = \frac{sin(t(n + 1/2))}{2 sin(t/2)}$$

#### Dimostrazione

Dimostriamo per induzione
per $n = 0$ osserviamo facilmente che si verifica la tesi, verifichiamo adesso che
$n - 1 \Rightarrow n$

per $n - 1$ si ha
$$\frac{1}{2} + \sum_{i=1}^{n - 1} cos(it) =^? \frac{sin(t(n - 1/2))}{2 sin(t/2)}$$
quindi resta da dimostrare che
$$\frac{sin(t(n - 1/2))}{2 sin(t/2)} + cos(nt) = \frac{sin(t(n + 1/2))}{2 sin(t/2)}$$

Utilizziamo le formule di somma per seno e coseno e vediamo che
$$\frac{sin(t(n - 1/2))}{2 sin(t/2)} + cos(nt) = \frac{sin(tn)cos(t/2) - cos(tn)sin(t/2)}{2sin(t/2)} + cos(nt)$$
Facendo adesso l'MCD tra i due termini del risultato si ha che
$$\frac{sin(tn)cos(t/2) - cos(tn)sin(t/2)}{2sin(t/2)} + cos(nt) = \frac{sin(tn)cos(t/2) + cos(tn)sin(t/2)}{2sin(t/2)} + cos(nt)$$
Che riapplicando al contrario il seno della somma verifica la tesi. $\square$

### Proposizione: Disuguaglianza di Bessel

sia $f: [-\pi; \pi] \rightarrow \mathbb{R}$ limitata e integrabile e siano $a_0,\, a_k\,\text{e}\, b_k$ i suoi _coefficienti di Fourier_ si avrà allora che
$$\frac{1}{\pi}\int_{-\pi}^{\pi} f^2(x) dx \geq \frac{a^2_0}{2} + \sum_{k = 1}^{\infty}a_k^2 + b_k^2$$

#### Dimostrazione

$\forall n \geq 0$ si ha che
$$\int_{-\pi}^{\pi}(f(x) - S_n(x))^2 dx \geq 0$$
Espandendo il quadrato si ha che
$$\int_{-\pi}^{\pi}f^2(x) + S_n^2(x) - 2f(x)S_n(x)dx \geq 0$$
Portando al secondo membro $S_n^2$ e $- 2f(x)S_n(x)$
$$\int_{-\pi}^{\pi}f^2(x) dx \geq \underbrace{\int_{-\pi}^{\pi}2f(x)S_n(x)dx}_i - \underbrace{\int_{-\pi}^{\pi} S_n^2(x) dx}_{ii}$$
Analizziamo i due fattori separatamente
$$\int_{-\pi}^{\pi}2f(x)S_n(x)dx = \int_{-\pi}^{\pi}2f[x](\frac{a_0}{2}+ \sum_{k=0}^{\infty}a_k cos(kx) + b_k sin(kx))dx = $$
$$ = a_0\int_{-\pi}^{\pi}f(x)dx + \sum_{k=0}^{\infty} 2a_k \int_{-\pi}^{\pi}f(x)cos(kx)dx + 2b_k\int_{-\pi}^{\pi} f(x)sin(kx)]dx$$
$$ = \pi a_0^2 + \sum_{k=0}^{\infty}2\pi a_k^2 + 2\pi b_k^2$$
D'altra parte
$$\int_{-\pi}^{\pi} S_n^2(x) dx = \int_{-\pi}^{\pi} [\frac{a_0}{2} + \sum_{k=0}^{\infty}a_k cos(kx) + b_k sin(kx)]^2dx= $$
Espandendo il quadrato all'interno dell'integrale abbiamo:
$$= \underbrace{\int_{-\pi}^{\pi} \left( \frac{a_0^2}{4} + \sum_{k=1}^{n} \left( a_k^2 \cos^2(kx) + b_k^2 \sin^2(kx) \right) \right) dx}_{\text{quadrati dei due termini}} + $$$$ + \underbrace{\int_{-\pi}^{\pi} \left( 2\frac{a_0}{2} \left( \sum_{k=1}^{n} a_k \cos(kx) + b_k \sin(kx) \right) \right) dx}_{\text{doppio prodotto tra i due termini}} + $$$$\underbrace{\int_{-\pi}^{\pi} 2 \sum_{\substack{i,j=1 \\ i \ne j}}^{n}
\left( a_i \cos(ix) + b_i \sin(ix) \right)
\left( a_j \cos(jx) + b_j \sin(jx) \right) dx}_{\text{prodotti misti}} +$$$$+ \underbrace{\int_{-\pi}^\pi \left(2 \sum_{i=1}^n(a_k\cos(kx)b_k\sin(kx))\right)dx}_{\text{doppio prodotto all'interno della somma}}$$
Notiamo però come gli ultimi 3 termini si annullano infatti
$$a_0 \left(\sum_{k=1}^{n}
    a_k \underbrace{\int_{-\pi}^{\pi} \cos(kx) \, dx}_{0}
    +
    b_k \underbrace{\int_{-\pi}^{\pi} \sin(kx) \, dx}_{0}
\right) = 0$$
Il secondo sviluppando i prodotti si ha che:
$$2 \sum_{\substack{i,j=1 \\ i \ne j}}^{n} \int_0^\pi a_i a_j \cos(ix) \cos(jx) + a_i b_j \cos(ix) \sin(jx) + b_i a_j \sin(jx) \cos(ix) + b_i b_j \sin(ix) \sin(jx) \, dx = 0$$
Similmente con il terzo.
Si ha quindi che:
$$\int_{-\pi}^{\pi} S_n^2(x) dx = \int_{-\pi}^{\pi} \left( \frac{a_0^2}{4} + \sum_{k=1}^{n} \left( a_k^2 \cos^2(kx) + b_k^2 \sin^2(kx) \right) \right) dx $$
Che è possibile esprimere come:
$$ \frac{\pi a_0^2}{2} + \sum_{k=1}^{n}\left(a_k^2\int_{- \pi}^\pi \cos^2(kx) dx+b_k^2\int_{- \pi}^\pi \sin^2(kx) dx\right) = \frac{\pi a_0^2}{2} + \sum_{k=1}^{n}\left( a_k^2 \pi+ b_k^2 \pi\right)$$
Dividendo per $\pi$ si ottiene la tesi. $\square$

#### Osservazione
Da questo teorema si ottiene che, poiché $f: [-\pi, \pi] \rightarrow \mathbb{R}$ ed è integrabile si avrà che
$$\infty > \int_{-\pi}^{\pi} f^2(x) dx \geq \frac{a^2_0}{2} + \sum_{k = 1}^{\infty}a_k^2 + b_k^2$$di conseguenza la serie
$$\sum_{k = 1}^{\infty} a_k^2 + b_k^2 < \infty$$
e quindi $a_k \rightarrow 0$ e $b_k \rightarrow 0$ e quindi:
$$\int_{-\pi}^{\pi} f(x)cos(kx) \rightarrow 0$$
$$\int_{-\pi}^{\pi} f(x)sin(kx) \rightarrow 0$$
### Teorema (convergenza puntuale delle funzioni $\mathcal{C}^1$ a tratti)
Sia $f \in \mathcal{C}^1$ a tratti con $f: [- \pi, \pi) \rightarrow \mathbb{R}$ e siano $a_0, \,a_k, \,b_k$ i suoi coefficienti di Fourier si ha allora che la serie di Fourier converge puntualmente a $$\frac{f(x^+) + f(x^-)}{2}$$
#### Dimostrazione
Esplicitiamo  $a_0, \,a_k, \,b_k$ all'interno di $S_n(x)$
$$S_n(x) = \frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \cdot \frac{1}{2} \, dy + \sum_{k=1}^{n} \left[ \left( \frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \cos(ky) \, dy \right) \cos(kx) + \left( \frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \sin(ky) \, dy \right) \sin(kx) \right]
$$
Raccogliendo i termini in un singolo integrale si ottiene che
$$\frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \left[ \frac{1}{2} + \sum_{k=1}^{n} \left( \cos(ky) \cos(kx) + \sin(ky) \sin(kx) \right) \right] \, dy
$$
Osserviamo che per le identità trigonometriche della somma si ha che:
$$\frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \left[ \frac{1}{2} + \sum_{k=1}^{n} \underbrace{\left( \cos(ky) \cos(kx) + \sin(ky) \sin(kx) \right)}_{\cos(k(y-x))} \right] \, dy
$$
$$\frac{1}{\pi} \int_{-\pi}^{\pi} f(y) \left[ \frac{1}{2} + \sum_{k=1}^{n} \cos(k(y-x)) \right] \, dy$$
Sostituiamo $t = y - x$
$$\frac{1}{\pi} \int_{-\pi - x}^{\pi - x} f(t + x) \left[ \frac{1}{2} + \sum_{k=1}^{n} \cos(kt) \right] \, dy$$
Avevamo visto che 
$$\frac{1}{\pi} \int_{-\pi - x}^{\pi - x} f(t + x) \left[ \underbrace{\frac{1}{2} + \sum_{k=1}^{n} \cos(kt)}_{\frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)}} \right] \, dy$$
$$\frac{1}{\pi} \int_{-\pi - x}^{\pi - x} f(t + x) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dy$$
Estendiamo $f$ a $\mathbb{R}$ $2\pi$ periodica, otteniamo quindi che:
$$\frac{1}{\pi} \int_{-\pi}^{\pi} \bar{f}(t + x) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dy \quad (*)$$
Osserviamo che possiamo togliere le $x$ dagli estremi di integrazione poiché la funzione è $2\pi$ periodica.
Osserviamo che:
$$\int_{-\pi}^{0} \left( \frac{1}{2} + \sum_{k=1}^{n} \cos(kt) \right) \, dt = \frac{\pi}{2}
$$
Questo perché $\cos(kt)$ integrato da $-\pi$ a $0$ da sempre 0
Similmente:
$$\int_{0}^{\pi} \left( \frac{1}{2} + \sum_{k=1}^{n} \cos(kt) \right) \, dt = \frac{\pi}{2}$$
Osserviamo che:
$$\frac{1}{\pi} \int_{-\pi}^{0} f(x^-) \frac{\sin\left( \left( n + \frac{1}{2} \right) t \right)}{2 \sin(t/2)} dt + \frac{1}{\pi} \int_{0}^{\pi} f(x^+) \frac{\sin\left( \left( n + \frac{1}{2} \right) t \right)}{2 \sin(t/2)} dt \quad (\bullet)$$ 
Ci da la tesi
Resta quindi da dimostrare che 
$$(*) - (\bullet) \rightarrow 0$$

$$\frac{1}{\pi} \int_{-\pi}^{0} \bar{f}(t + x) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dt + \frac{1}{\pi} \int_{0}^{\pi} \bar{f}(t + x) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dt \quad (*)$$
andando a fare la differenza $(*) - (\bullet)$ si ottiene:
$$\frac{1}{\pi} \int_{-\pi}^{0} (\bar{f}(t + x) - f(x^-)) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dt + \frac{1}{\pi} \int_{0}^{\pi} (\bar{f}(t + x) - f(x^+)) \frac{\sin\left(\left(n + \frac{1}{2}\right)t\right)}{2 \sin\left(\frac{t}{2}\right)} \, dt \quad (*)$$
Definamo per compattezza una funzione $G$:
$$G(x;t) = \begin{cases} \frac{\bar{f}(x+t) - f(x^+)}{2 \sin(t/2)} & t \in [0, \pi) \\ \frac{\bar{f}(x+t) - f(x^-)}{2 \sin(t/2)} & t \in [-\pi, 0) \end{cases}$$
in modo da scrivere l'integrale in modo compatto come:
$$\frac{1}{\pi} \int_{-\pi}^{\pi} G(x;t) \sin\left(\left(n + \frac{1}{2}\right)t\right) \, dt \quad (**)$$
Osserviamo in modo semplice che $G(x, t)$ è di continua a tratti:
il problema si ha per $t \rightarrow 0$ ma scrivendo:
$$\frac{\bar{f}(x+t) - f(x^+)}{t} \cdot \frac{t/2}{\sin(t/2)} \xrightarrow{t \to 0^+} f'(x^+)$$
e similmente per $t \rightarrow 0^-$
Osservo anche che posso scrivere:
$$\sin\left(\left(n + \frac{1}{2}\right)t\right) = \sin(nt) \cos\left(\frac{t}{2}\right) + \cos(nt) \sin\left(\frac{t}{2}\right)$$
e quindi ho che 
$$\frac{1}{\pi} \int_{-\pi}^{\pi} G(x;t) \left( \sin(nt) \cos\frac{t}{2} + \cos(nt) \sin\frac{t}{2} \right) dt \quad (**)$$
$$\frac{1}{\pi} \int_{-\pi}^{\pi} G(x;t) \left( \sin(nt) \cos\frac{t}{2} \right) dt + \frac{1}{\pi} \int_{-\pi}^{\pi} G(x;t) \left( \cos(nt) \sin\frac{t}{2} \right) dt \quad (**)$$
Se quindi chiamiamo:
$$F_1 = G(x;t) \sin \frac{t}{2}$$
$$F_2 = G(x;t) \cos \frac{t}{2}$$
otteniamo che:
$$= \underbrace{\frac{1}{\pi} \int_{-\pi}^{\pi} F_1(x,t) \sin(nt) dt}_{b_n \,\text{di} \, F_1} + \underbrace{\frac{1}{\pi} \int_{-\pi}^{\pi} F_2(x,t) \cos(nt) dt}_{a_n \,\text{di} \, F_2}$$
i quali convergono entrambi a 0 per la conseguenza della _Disuguaglianza di Bessel_

#### Corollario
Se $f \in \mathcal{C}^1$ a tratti e $f$ è continua $\Rightarrow$ la serie di Fourier tende puntualmente a $f$

### Teorema
La serie di Fourier tende _totalmente_ a $f$
#### Dimostrazione
Supponiamo $f \in \mathcal{C}^1$ con $f$ $2 \pi$ periodica si ha allora che anche $f'$ è anch'essa $2\pi$ periodica.
Chiamiamo $a_0, \, a_k, \, b_k$ i coefficienti di Fourier di $f$ e $\alpha_0, \, \alpha_k, \, \beta_k$ i coefficienti di $f'$
Vediamo che 
$$\pi \alpha_0 = \int_{-\pi}^{\pi} f'(x) \,dx = f(\pi) - f(-\pi) = 0$$
$$\pi \alpha_k = \int_{-\pi}^\pi f'(x) \cos(kx) \,dx = \cos(kx)f(x)\big]_{-\pi}^\pi + k \int_{-\pi}^\pi f(x) sin(kx) = k \pi b_k$$
E quindi:
$$
\alpha_k = kb_k
$$
Similmente si può vedere che 
$$\beta_k = - k a_k$$
quindi per dimostrare il teorema dobbiamo far vedere che:
$$\sum_{k = 0}^\infty \|a_k\cos(kx) + b_k\sin(kx)\|_\infty \leq \sum_{k = 0}^\infty \|a_k\cos(kx)\|_\infty + \|b_k\sin(kx)\|_\infty \leq$$
$$\leq \sum_{k = 0}^\infty \|a_k\|_\infty + \|b_k\|_\infty \leq \sum_{k = 0}^\infty |a_k| + |b_k| = \sum_{k = 0}^\infty \frac{|\beta_k|}{k} + \frac{|\alpha_k|}{k} \leq$$
Utilizzando adesso due volte la disuguaglianza $st \le \frac{1}{2}s^2 + \frac{1}{2}t^2$ 
$$\sum_{k = 0}^\infty \frac{1}{k^2} + \frac{1}{2} \sum_{k = 0}^\infty \beta_k^2 + \alpha_k^2 < \infty$$
quindi la serie di Fourier converge uniformemente a $f$ su $[-\pi, \pi]$.
##### Corollario
Se $f \in \mathcal C^1$ ed è $2\pi$ periodica allora la *disuguaglianza di Bessel* diventa un uguaglianza:
$$\frac{1}{\pi}\int_{-\pi}^{\pi} f^2(x) dx = \frac{a^2_0}{2} + \sum_{k = 1}^{\infty}a_k^2 + b_k^2$$
###### Dimostrazione
Si ha che 
$S_n \xrightarrow{\text{unif}} f$ e quindi che $S_n^2 \xrightarrow{\text{unif}} f^2$
da un teorema sulle funzioni uniformemente convergenti si ha che:
$$\int_{-\pi}^\pi S_n^2(x) \, dx \to \int_{-\pi}^\pi f^2(x) \, dx$$
Ma nella dimostrazione del teorema di Bessel avevamo visto che:
$$\int_{-\pi}^\pi S_n^2(x) \, dx = \pi\left(\frac{a_0^2}{2}+ \sum_{k = 0}^\infty a_k^2 + b_k^2\right)$$
e quindi:
$$\frac{1}{\pi}\int_{-\pi}^{\pi} S_n^2(x) dx \to \frac{a^2_0}{2} + \sum_{k = 1}^{\infty}a_k^2 + b_k^2$$
dalla continuità di $f$ e quindi di $f^2$ si ha che 
$$\frac{1}{\pi}\int_{-\pi}^{\pi} f^2(x) dx = \frac{a^2_0}{2} + \sum_{k = 1}^{\infty}a_k^2 + b_k^2$$
$\square$
