Una curva regolare in $\mathbb R^n$ non è altro che una _funzione_ $\gamma: [a, b] \to \mathbb R^n$ di classe $C^1(a, b)$ e tale che si abbiano le seguenti proprietà:
- $\gamma$ è continua su $[a, b]$
- Esiste la derivata sull'estremo destro e sinistro dell'intervallo
$$\exists \lim_{t\to a^+} \frac{\gamma(t) - \gamma(a)}{t - a} = \gamma'(a)$$
$$\exists \lim_{t\to b^-} \frac{\gamma(t) - \gamma(b)}{t - b} = \gamma'(b)$$
- Risulta che la derivata della funzione è sempre diversa dal vettore nullo
$$\forall t \in [a, b] \quad \gamma'(t) \neq \vec 0$$
Quest'ultima proprietà ci sarà utile per definire un _vettore tangente_ alla nostra curva, elemento utile per descrivere la lunghezza di una curva.
##### Notazione
A volte potremmo chiamare la derivata di $\gamma$ come la sua _velocità_
Inoltre chiameremo la sua immagine come il _sostegno_ di $\gamma$
$$\gamma([a, b]) \subset R^n$$
### Esempi
##### Rette parametriche
Abbiamo già analizzato degli esempi di curve in $\mathbb R^n$ con le curve parametriche:
Se prendiamo infatti un vettore direzione:
$$\vec v \in \mathbb R^n \smallsetminus \{0\}$$
E un punto d'appoggio:
$$\vec p \in \mathbb R^n$$
$$\gamma(t) = \vec v t \ + \ \vec p$$
$\gamma$ risulterà la parametrizzazione di una retta.
Se limitiamo la funzione su un intervallo si avrà che 
$$\gamma(t) \Big|_{[a,b]}$$è la parametrizzazione di un segmento che fa parte della retta $\gamma$.
Verifichiamo che questa retta soddisfi le caratteristiche richieste.
La retta è una funzione di classe $C^\infty$ l'unico problema che potremmo riscontrare è un annullamento della derivata ma se osserviamo abbiamo che:
$$\gamma(t) = (v_1 t + p_1, \dots, v_n + p_n)$$
e quindi che:
$$\gamma ' (t) = (v_1, \dots, v_n) = \vec v \neq \vec 0$$
#### Grafici di funzione
 Un altro esempio di curva può essere ottenuto considerando il grafico di una funzione reale. Sia infatti una funzione $f: [a, b] \to \mathbb R$ di classe $C^1$, allora possiamo definire la curva
$$\gamma(t) = (t, f(t))$$
che parametrizza il grafico di $f$ nell'intervallo $[a, b]$. Tale curva rispetta le proprietà richieste e rappresenta una curva in $\mathbb R^2$.
Questo concetto può essere esteso a $\mathbb R^n$ prendendo una funzione di classe $C^1$ in $\mathbb R^{n - 1}$ 

 Verifichiamo adesso che questa curva rispetti le proprietà richieste:
 il vettore $(t, f(t))$ è composto dalla funzione identità che è di classe $C^\infty$ e da $f \in C^1$ quindi anche la curva $\gamma$ è di classe $C^1$, come richiesto. 
 Inoltre se andiamo a calcolare la derivata del vettore si ha che questo è uguale a: $$\gamma'(t) = (1, f'(t)) \neq \vec 0$$
 Si ha intuitivamente che questo vettore non è altro che il vettore tangente alla curva in $\mathbb R^n$

Questa proprietà vale, in realtà, per ogni _curva regolare_ grazie a questo teorema:

### Teorema
Sia $\gamma$ una _curva regolare_
$$\gamma : [a, b] \to \mathbb R^n$$
e sia $t \in [a, b]$ allora esiste sempre un $I(t)$ intorno di $t$ dove la curva $\gamma\Big|_{I(t)}$ è una funzione dipendente da una variabile.
##### Dimostrazione
Supponiamo che $n = 2$, ma la dimostrazione è facilmente estensibile ad ogni valore di $n$
sappiamo che $\gamma$ è regolare e che quindi la sua derivata non si annulla mai, si ha quindi che:
$$\gamma'(t) \neq \vec 0$$
e quindi che $\gamma_1'(t) \neq 0$ oppure $\gamma_2'(t) \neq 0$
supponiamo ad esempio che $\gamma_2'(t) > 0$
Poiché si ha anche che $\gamma \in C^1$ si ha che $\gamma'$ è continua si avrà un intorno di $t$ dove $\gamma'_2 (x) > 0$ per le $x \in I(t)$.
quindi in questo sotto intervallo la funzione è continua e crescente di conseguenza invertibile, esisterà quindi:
$$\exists \gamma^{-1}_2: J \to I$$
e si ha anche che $J$ è un intervallo perché $\gamma$ è continua.
inoltre $\gamma^{-1}_2$  è crescente.
per concludere la dimostrazione osserviamo che:
$$\gamma(s) = (\gamma_1(s), \gamma_2(s))$$
ma per valori $s \in I$
si ha che $y = \gamma_2(s)$ e, di conseguenza $s = \gamma^{-1}_2(y)$
quindi possiamo scrivere la curva localmente come  
$$\gamma(s) = \big(\gamma_1(\gamma_2^{-1}(y)), y\big),$$  
dimostrando che $\gamma$ è una funzione dipendente da una variabile nell'intorno $I(t)$.

#### Definizione 
sia $\gamma$ una curva regolare possiamo definire il suo _versore tangente_:
$$\tau_\gamma(t) := \frac{\gamma'(t)}{\|\gamma'(t)\|}$$
### Riparametrizzazione di una curva
Sia $\gamma$ e $\sigma$ due curve regolari, queste si diranno _equivalenti_ se:
$$\exists p: [a,b] \to [c, d] \quad \text{biunivoca e di classe } C^1$$
Grazie alla quale si ha che
$$\gamma(t) = \sigma(p(t))$$
Se $p$ è monotona crescente allora le due curve hanno la stessa direzione mentre viceversa hanno direzione opposta
#### Lemma
il versore tangente è invariate a meno del segno a seguito di una riparametrizzazione:
$$\tau_\gamma(t) = \tau_\sigma(p(t))$$
se hanno la stessa direzione
$$\tau_\gamma(t) = - \tau_\sigma(p(t))$$
se hanno direzione opposta.
#### Dimostrazione
ricordiamo che abbiamo che
$$\gamma(t) = \sigma(p(t))$$
di conseguenza $\gamma'(t)$ è esprimibile come:
$$
\gamma'(t) = p'(t) \sigma'(p(t))$$
e quindi la sua norma sarà uguale a 
$$\|\gamma'(t)\| = |p'(t)| \ \|\sigma'(p(t))\|$$
di conseguenza il versore tangente si potrà scrivere come


$$\tau_\gamma(t) = \pm \tau_\sigma(p(t))$$
$\square$
### Lunghezza di una curva
si ha che la lunghezza di una curva regolare in $\mathbb R^n$ è uguale a:
$$L(\gamma) = \int_a^b\|\gamma'(t)\| \ dt$$
#### Teorema
 Sia $\gamma$ una curva regolare, allora la lunghezza della curva è indipendente dalla parametrizzazione scelta.
 Ovvero si ha che
 $L(\gamma) = L(\sigma)$ per ogni parametrizzazione equivalente $\sigma$.
#### Dimostrazione
$$L(\gamma) = \int_a^b \|\gamma'(t)\| \ dt = \int_a^b |p'(t)| \|\sigma'(p(t))\| \ dt$$
Dividiamo i casi in cui le funzioni equivalenti abbiano stesso verso o verso opposto e quindi che $p'$ sia strettamente maggiore o minore di 0
**Stesso verso**
si ha che 
$$\int_a^b |p'(t)| \|\sigma'(p(t))\| \ dt = \int_a^b \|\sigma'(p(t))\| \ p'(t) \ dt$$
effettuando ora la sostituzione $p(t) = x$ si ottiene che:
osservando che data la monotonia di $p$ si ha che 
$$
p(a) = c \quad p(b) = d
$$
$$L(\gamma) = \int_c^d \|\sigma'(x)\| \ dx = L(\sigma)$$
**Verso opposto**
$$\int_a^b |p'(t)| \|\sigma'(p(t))\| \ dt = -\int_a^b \|\sigma'(p(t))\| \ p'(t) \ dt$$
In questo caso
$$p(a) = d \quad p(b) = c$$
Effettuando nuovamente la sostituzione
$$L(\gamma) = -\int_d^c \|\sigma'(x)\| \ dx =\int_c^d \|\sigma'(x)\| \ dx = L(\sigma)$$
### Teorema
La lunghezza di una curva è sempre maggiore o uguale della distanza tra il suo punto di inizio e di fine.
$$L(\gamma) \geq \|\gamma(b) - \gamma(a)\|$$
#### Dimostrazione
Se la curva è chiusa la dimostrazione è immediata, prendiamo il caso quindi in cui $\gamma(a) \neq \gamma(b)$ 
prendiamo un vettore $\vec v \in \mathbb R^n$
si ha che:
$$\vec v \cdot (\gamma (b)) - \gamma (a)) = \vec v \int_a^b\gamma'(t) \ dt$$
per la disuguaglianza triangolare abbiamo che:
$$\left| \vec{v} \cdot \int_a^b \gamma'(t) \, dt \right| \leq \|\vec{v}\| \int_a^b \|\gamma'(t)\| \, dt = \|\vec v\| \ L(\gamma)
$$
ovvero si ha quindi che:
$$\vec v \cdot (\gamma (b)) - \gamma (a)) \leq \|\vec v\| \ L(\gamma)$$
Scegliendo adesso $\vec v = \gamma (b) - \gamma (a)$, e ricordando che il prodotto scalare tra un vettore e se stesso è il quadrato della sua norma, otteniamo:
$$\|\gamma (b)) - \gamma (a)\|^2 \leq \|\gamma (b)) - \gamma (a)\| \ L(\gamma)$$
e quindi la tesi che:
$$\|\gamma (b)) - \gamma (a)\| \leq L(\gamma)$$
