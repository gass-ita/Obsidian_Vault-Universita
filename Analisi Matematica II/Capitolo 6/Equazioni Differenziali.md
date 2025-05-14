Un'equazione differenziale è un espressione che lega la derivata n-esima di una funzione $u$ con una funzione $F$ che dipende dalle altre derivate della funzione:
Ad esempio possiamo generalizzare questo scrivendo che una generica equazione differenziale è esprimibile come:
$$u^{(n)}(t) = F(t, u ,u', u'', \dots, u^{(n-1)})$$
Dove $F$ sarà quindi una funzione $$F: \mathbb R^n \to \mathbb R$$
Tipicamente ci limitiamo a trovare una soluzione $u$ di un'equazione differenziale in un dominio che notoriamente è un intervallo, saremo interessati a cercare quindi una funzione $$u: I \to \mathbb R$$che soddisfi la nostra equazione.
Solitamente questo tipo di equazioni nascono da problemi fisici come quelli relativi alla _meccanica_ e alla _termodinamica_.

---

se prendiamo ad esempio l'equazione differenziale:
$$u'(t) = f({u(t)}) \cdot g(t)$$
Questa è una classica equazione differenziale a _variabili separabili_.
Un esempio di una funzione di questo tipo è:
$$u'(t) = \sqrt{u(t)}$$
dove quindi appare che $f(u) = \sqrt{u}$ e $g(t) = 1$
per risolvere questo tipo di equazioni differenziali applichiamo questo procedimento:

$$\frac{u'(t)}{\sqrt{u(t)}} = 1$$
integrando entrambi i lati dell'equazione otteniamo che:
$$\int\frac{u'(t)}{\sqrt{u(t)}} dt = \int1 dt$$
Applicando una sostituzione $u(t) = u$ si ha che
$$\int\frac{1}{\sqrt{u}} du = t + c$$
$${2}{\sqrt{u}} = t + c$$
e quindi che:
$$u(t) = \frac{(t + c)^2}{4}$$
Se fissiamo un valore iniziale per cui la funzione $u$ deve _passare_ $(t_0, u_0)$ si ha che possiamo trovare una soluzione alla nostra equazione.

---
# Una osservazione importante 
Una equazione differenziale ordinaria (ovvero che coinvolge una funzione $u$ di una variabile) di ordine $n$ può sempre essere ricondotta ad una funzione differenziale di ordine $1$ vettoriale:
infatti se consideriamo una generica equazione differenziale si ha che questa sarà della forma:
$$u^{(n)}(t) = F(t, u', u'', \dots, u^{(n-1)})$$
Se consideriamo il vettore $V \in \mathbb R^n$ definito come:
$$V_1 = u, \, \dots \, , \, V_n = u^{(n - 1)}$$
Abbiamo che l'equazione differenziale è riscrivibile come:
$$\begin{cases} V_1' = u' = V_2 \\ V_2' = u'' = V_3 \\ \dots \\V_n' = F(t,u, u', u'', \dots, u^{(n-1)})  \end{cases} $$
Possiamo scrivere la nostra equazione differenziale come:
$$V' = f(t, V)$$
ovvero come una equazione differenziale di ordine $1$
Dove:
$$f: I \times \mathbb R^n \to \mathbb R^n$$
Risulterà quindi che qualunque equazione differenziale ordinaria sarà esprimibile come:
$$\begin{cases} u'(t) = f(t, u) \\ u(t_0) = u_0 \end{cases}$$
Dove: 
$$u: \mathbb R \to \mathbb R^n \quad f: I \times \mathbb R^n \to \mathbb R^n \quad (t_0, u_0) \in I \times \mathbb R^n$$

---

# Teorema di Esistenza e Unicità delle Soluzioni locali del Problema di Cauchy

Per trattare questo argomento sarà necessario rinfrescare il concetto di _locale lipshipizianità_ rispetto ad una variabile di una funzione $f: I \times \mathbb R^n \to \mathbb R^n$
Diremo, infatti, che una funzione $f(t, u)$ di questo tipo è _localmente lipshipziana_ rispetto alla variabile $u$ se esiste un intorno $U$ del punto $(\bar t, \bar u)$: 
$$\exists c > 0: \quad \|f(t, u) - f(t, v)\| \leq c \, \|u - v\| \quad \forall (t, u) \in U $$
Si può dimostrare che condizione necessaria e sufficiente affinché una funzione $g(t)$ è _lipshipziana_ è far vedere che $g'(t)$ è limitata:
$$|g(u) - g(v)| = \left|\int_u^v g'(s)\right| \, ds \leq \int_u^v |g'(s)| \, ds \leq \int_u^v C \, ds = C(u - v) = C |u - v|$$
#### Teorema per funzioni del 1° ordine
Sia $f: A \subset (I \times \mathbb R) \to \mathbb R$ una funzione di classe $\mathcal C^1$, e quindi _lipshipziana_ per la seconda variabile, e siano $(t_0, u_0) \in A$ 
sia dato il seguente _problema di Cauchy_
$$\begin{cases} u'(t) = f(t, u(t)) \\ u(t_0) = u_0\end{cases}$$
Si avrà allora che:
$$\exists \, r_0 : \, \exists! \, u:(t_0 - r_0, t_0 + r_0) \to [u_0 - \rho, u_0 - \rho] \, \text{soluzione del sistema}$$











