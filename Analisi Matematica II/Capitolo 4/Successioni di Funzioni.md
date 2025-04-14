Sia $f_k$ una _successione di funzioni_ dove $f_i: E \subset \mathbb{R} \rightarrow \mathbb{R}$ 
diremo che $f_k$ tende puntualmente a $f: A \rightarrow \mathbb{R}$ su un sottoinsieme $A \subset E$ se:
$$\forall x \in A, \quad \forall \epsilon > 0, \quad \exists \bar{k} \in \mathbb{N}: \quad \forall k > \bar{k}, \quad |f_k(x) - f(x)| < \epsilon$$
diremo invece che $f_k$ tende _uniformemente_ a $f: A \rightarrow \mathbb{R}$ su un sottoinsieme $A \subset E$ se possiamo togliere la dipendenza dalla scelta di $\bar{k}$ da $x \in A$:
$$\forall \epsilon > 0, \quad \exists \bar{k} \in \mathbb{N}: \quad \forall k > \bar{k}, \quad |f_k(x) - f(x)| < \epsilon \quad \forall x \in A$$
#### Definiamo una Norma
Sia $\mathcal{F}_b(E)$ l'insieme formato da tutte le funzioni _limitate_ definite sull'insieme $E$
definiamo la _norma infinito_ su questo insieme come:
$$f \in \mathcal{F}_b(E) \quad \|f\|_\infty = \sup_{x \in E}\{|f(x)|\}$$
Se voglio limitarmi su un sottoinsieme $A \subset E$
$$\|f\|_{\infty,\,A} = \sup_{x \in A}\{|f(x)|\}$$
Osserviamo una somiglianza tra la definizione di _tendenza uniforme_ e di _norma infinito_ possiamo infatti dimostrare la seguente equivalenza:

$$f_k \rightarrow_u f \Leftrightarrow \|f_k - f\|_\infty \rightarrow 0$$
si può vedere infatti che
$$f_k \rightarrow_u f \Leftrightarrow \forall \epsilon > 0, \quad \exists \bar{k} \in \mathbb{N}: \quad \forall k > \bar{k} \quad |f_k(x) - f(x)| < \epsilon \quad \forall x \in A$$
ovvero:
$$\forall \epsilon > 0, \quad \exists \bar{k} \in \mathbb{N}: \quad \forall k > \bar{k} \quad \|f_k(x) - f(x)\|_\infty < \epsilon$$
In modo intuitivo possiamo definire una distanza $d_\infty:  \mathcal{F}_b(E) \times  \mathcal{F}_b(E) \rightarrow \mathbb{R}^+$ definita come $d_\infty(f, g) = ||f - g||_\infty$ 
Se costruiamo adesso lo _spazio metrico_ costituito da $(\mathcal{F}_b(E), d_\infty)$ si ha che
$$f_k \rightarrow f \Leftrightarrow f_k \rightarrow_u f$$
## Proprietà dello spazio metrico $\mathcal{F}_b(E)$
### Chiusura del sottospazio
Si ha che lo spazio metrico appena formato è _chiuso_ ovvero che ogni successione di funzione convergente, e quindi uniformemente convergente, converge ad una funzione in $\mathcal{F}_b(E)$ 
$$\text{sia} \, (f_k) \subset \mathcal{F}_b(E), \quad f_k \rightarrow_uf \Rightarrow f \in \mathcal{F}_b(E)$$
inoltre si ha che 
$$||f_k||_\infty \rightarrow ||f||_\infty$$
#### Dimostrazione
Dalla proprietà triangolare delle norme si ha che
1. $\|f_k - f\|_\infty + \|f_k\|_\infty \geq \|f\|_\infty$
2. $\|f_k - f\|_\infty + \|f\|_\infty \geq \|f_k\|_\infty$
Per dimostrare che $f \in \mathcal{F}_b(E)$ basterà far vedere che $||f||_\infty < \infty$
Dalla prima disuguaglianza si ha che:
$$\|f - f_k\|_\infty + \|f_k\|_\infty \geq \|f\|_\infty$$
Ricordando $f_k$ è limitata $||f_k||_\infty < \infty$ inoltre, dato che $f_k \rightarrow_u f$ si ha che:
$$\forall \epsilon > 0, \quad \exists \bar{k} \in \mathbb{N}: \quad \forall k > \bar{k} \quad \|f_k(x) - f(x)\|_\infty < \epsilon$$
quindi
$$\|f\|_\infty < \infty$$
inoltre mettendo a sistema le due disequazioni si ha che
$$ \bigl | \|f_k\|_\infty - \|f\|_\infty \bigr| \leq \|f_k - f\|_\infty < \epsilon $$
Che, dalla definizione di limite valida la tesi. $\square$

## Lo spazio metrico $\mathcal{C}_b(E)$ 
Analizziamo adesso il sottospazio metrico di $\mathcal{F}_b(E)$ formato dalle funzioni _limitate_ e _continue_ dove è definito la stessa distanza $d_\infty$
### Chiusura del sottospazio
Anche in questo caso lo spazio $\mathcal{C}_b(E)$ risulta chiuso
$$\text{sia} \, (f_k) \subset \mathcal{C}_b(E), \quad f_k \rightarrow_uf \Rightarrow 
f \in \mathcal{C}_b(E)$$
#### Dimostrazione
per dimostrare questa preposizione basterà mostrare che _successioni di funzioni continue tendono uniformemente a funzioni continue_, combinando il risultato di chiusura per il sottospazio precedente avremmo la tesi.

$$\text{sia} \, (f_k) \subset \mathcal{C}_b(E), \quad \text{si avrà che} \, f_k \,\text{è continua}$$
fissiamo $x \in E$ si avrà che
$$\left \lvert f_k(x) - f_k(y) \right \lvert < \epsilon \quad \forall y \in B_{\delta}(x)$$
inoltre si ha che $f_k \rightarrow_uf$ quindi:
$$\exists \bar{k}: \quad \forall k>\bar{k} \quad ||f_k - f||_\infty < \epsilon$$
e in particolare
$$||f_\bar{k} - f||_\infty < \epsilon$$
si ha quindi che 
$$|f(x) - f(y)| \leq |f(x) - f_\bar{k}(x)| + |f_\bar{k}(x) - f_\bar{k}(y)| + |f_\bar{k}(y) - f(y)| < 3 \epsilon$$ $\square$

### Completezza del sottospazio
Un altra proprietà dello spazio metrico definito sull'insieme $\mathcal{C}_b(E)$ è che è completo ovvero che _ogni successione di Cauchy risulta convergente_
$$f_k \text{ di Cauchy } \Rightarrow f_k \rightarrow_u f$$
#### Dimostrazione 
Prendiamo una generica successione di funzioni di Cauchy $(f_k) \subset \mathcal{C}_b(E)$
si avrà quindi che:
$$\forall \epsilon > 0, \quad \exists \bar{k}: \quad \forall h,k > \bar{k} \quad \|f_k - f_h\|_\infty < \epsilon$$
fissato un $x \in E$ 
$$\forall \epsilon > 0, \quad \exists \bar{k}: \quad \forall h,k > \bar{k} \quad |f_k(x) - f_h(x)| < \epsilon$$
Abbiamo quindi una successione reale di Cauchy, quindi che $f_k \rightarrow_p f$ 
Facendo tendere adesso $h \rightarrow \infty$ otteniamo che:
$$\forall \epsilon > 0, \quad \exists \bar{k}: \quad \forall h,k > \bar{k} \quad \|f_k - f\|_\infty < \epsilon$$
e quindi che $f_k \rightarrow_u f$. $\square$

## Integrali di una Successione di Funzioni
Un fatto interessante sulle successioni di funzione, in particolare riguardo quelle _integrabili_ è il legame che hanno quest'ultime con l'integrale della funzione a cui tendono.
$$\text{sia} \, f_k:E \rightarrow \mathbb{R} \quad \text{una successione di funzioni integrabili in senso classico}$$
$$f_k \rightarrow_u f$$
Si avrà allora che:
$$f \quad \text{è integrabile in senso calssico}$$
$$\int_E f_k(x) dx \rightarrow \int_E f(x) dx$$
#### Dimostrazione
##### Fatto preliminare
$$f \quad \text{è integrabile} \Leftrightarrow \exists g;h \, \text{funzioni integrabili}: g \leq f \leq h \quad \int_Eh-g < \epsilon$$
La prima implicazione ($\Rightarrow$) è semplice scegliendo come $g$ e $h$ le funzioni semplici date dalla definizione di integrabilità
La seconda implicazione ($\Leftarrow$) ci dice che 
$$f \quad \text{è integrabile} \Leftarrow \exists g;h \, \text{funzioni integrabili}: g \leq f \leq h \quad \int_Eh-g < \epsilon$$
$g$ e $h$ sono integrabili, dalla definizione esisteranno quindi $\phi^+$, $\phi^-$, $\psi^+$, $\psi^-$ funzioni semplici, tali che:
$$\phi^- \leq h \leq \phi^+$$
$$\int_E\phi^+ - \phi^- < \epsilon$$
$$\psi^- \leq g \leq \psi^+$$$$\int_E\psi^+ - \psi^- < \epsilon$$
di conseguenza si osserva che
$$\psi^- \leq f \leq \phi +$$
e si ha che 
$$\int_E \phi^+ - \psi^- dx= \int_E \phi^+ - h dx - \int_E h - g dx - \int_E g - \psi^- \leq \int_E \phi^+ - \phi^- dx - \int_E h - g dx - \int_E \psi^+ - \psi^- < 3 \epsilon$$
$\square$
Tornando al teorema da dimostrare si ha che $f_k$ è limitata $\forall k \in \mathbb{N}$ e quindi $f$ è limitata, inoltre $f_k \rightarrow_u f$ e quindi:
$$\forall \epsilon > 0 \quad \exists \bar{k} : \forall k>\bar{k} \quad |f_k(x) - f(x)| < \epsilon \quad \forall x \in E$$ e quindi:
$$f_\bar{k}(x) - \epsilon < f(x) < f_\bar{k}(x) + \epsilon$$
e quindi utilizzando il fatto precedente si ha che $f$ è integrabile
infine per dimostrare l'ultimo limite 
$$\left | \int_E f_k(x) - f(x) dx\right | \leq  \int_E \left |f_k(x) - f(x)\right | dx < \int_E \epsilon =  m(E) \epsilon \quad \forall k > \bar{k}$$
che dalla definizione di limite ci da la tesi. $\square$ 
## Il sottospazio vettoriale $\mathcal{C}^1$ 
### Definiamo l'insieme
$f: [a, b] \rightarrow \mathbb{R}^n$ è di classe $\mathcal{C}^1$ sull'intervallo chiuso $[a, b]$.

* Se $f$ è di classe $\mathcal{C}^1$ sull'aperto $(a, b)$.
* $f$ continua su $a$ e $b$.
* Denotando con $f'(a)$ la derivata destra di $f$ in $a$.
  $f'(b)$ la derivata sinistra di $f$ in $b$.
  $f'(x) \quad x \in (a, b)$.

$\Rightarrow \quad f'$ continua su $a$ e $b$.
### Teorema
$f_k : [a, b] \rightarrow \mathbb{R}$ di classe $\mathcal{C}^1([a, b])$ SE $f_k$ e $f'_k$ sono tali che: $f'_k \rightarrow_{u} g$ e $f_k \rightarrow_{u} f$ $\Rightarrow g= f'$

#### Dimostrazione
Le funzioni $f_k$ soddisfano il _teorema fondamentale del calcolo integrale_ poiché funzioni sono classe $\mathcal{C}^1$ 
e quindi hanno derivate prime integrabili $\forall [a, x] \subset [a, b]$.
$$
f_k(x) = f_k(a) + \int_a^x f'_k(t) \, dt
$$
Sappiamo inoltre che $f' \rightarrow_u g$
Pertanto si ha che $g \in \mathcal{C}^0$ e quindi $g$ è integrabile
Si ha inoltre che
$$
\int_a^xf'_k(t) dt \rightarrow \int_a^xg(t) dt
$$
Inoltre poiché $f_k \rightarrow_u f$ si ha che $f_k(x) \rightarrow_p f(x)$ e quindi dalla tesi del _teorema fondamentale del calcolo integrale_ si ha che
$$
f(x) = f(a) + \int_a^xg(t) dt
$$
da cui risulta che 
$$
f' = g
$$
$\square$

## Una norma per $\mathcal{C}^1$
 Si definisce una norma per $\mathcal{C}^1$ come $\|f\|_{\mathcal{C}^1} = \sup_{x \in [a,b]} |f(x)| + \sup_{x \in [a,b]} |f'(x)|$.
 che equivale a dire utilizzando le $||\cdot||_\infty$
 $$
 \|f\|_{\mathcal{C}^1} = \|f\|_\infty + \|f'\|_\infty$$
## Completezza dello spazio metrico ($\|f\|_{\mathcal{C}^1}$, $\|\cdot\|_{\mathcal{C}^1}$)
Lo spazio metrico $(\mathcal{C}^1$,$\|\cdot\|_{\mathcal{C}^1})$ è completo, il che implica che ogni successione di Cauchy di funzioni in $\mathcal{C}^1$ converge uniformemente a una funzione che è anch'essa di classe $\mathcal{C}^1$.
### Dimostrazione
Prendiamo una generica successione $f_k$ di Cauchy secondo la norma $\|\cdot\|_{\mathcal{C}^1}$
$$
\forall \epsilon  >0 \quad \exists \bar{k}: \quad \forall k, h > \bar{k} \quad \|f_k - f_h\|_{\mathcal{C}^1} < \epsilon
$$
ovvero che 
$$
\|f_k - f_h\|_\infty + \|f_k' - f_h'\|_\infty < \epsilon$$
si ha quindi che 
- $\|f_k - f_h\|_\infty < \epsilon$
- $\|f_k' - f_h'\|_\infty < \epsilon$
di conseguenza $f_k$ e $f'_k$ sono successioni di Cauchy in $\mathcal{C}^0$.
Si ha quindi che $f_k \rightarrow_u f \in \mathcal{C}^0$ e $f'_k \rightarrow_u g \in \mathcal{C}^0$ e inoltre che $f' = g$ di conseguenza si ha che $f \in \mathcal{C}^1$ 
per completare la dimostrazione basta osservare che mandando $h \rightarrow \infty$
$$
\|f_k - f\|_\infty + \|f_k' - f'\|_\infty \rightarrow 0$$
e quindi 
$$
\|f_k - f\|_{\mathcal{C}^1} \rightarrow 0
$$
$\square$ 
 