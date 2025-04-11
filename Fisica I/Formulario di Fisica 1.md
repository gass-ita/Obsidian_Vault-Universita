## Cinematica

### Moto Rettilineo Uniforme (MRU)
- Velocità costante:  
  $$
  v = \frac{\Delta x}{\Delta t} = \frac{x_f - x_i}{t_f - t_i}
  $$
- $$\lim_{x \to a}
$$
- Posizione in funzione del tempo:  
  $$
  x(t) = x_0 + vt
  $$

### Moto Rettilineo Uniformemente Accelerato (MRUA)
- Accelerazione costante:  
  $$
  a = \frac{\Delta v}{\Delta t} = \frac{v_f - v_i}{t_f - t_i}
  $$
- Velocità in funzione del tempo:  
  $$
  v(t) = v_0 + at
  $$
- Posizione in funzione del tempo:  
  $$
  x(t) = x_0 + v_0t + \frac{1}{2}at^2
  $$
---

### Moto Parabolico (nel piano xy)
- Componenti della velocità iniziale:  
  $$
  v_{0x} = v_0 \cos(\theta), \quad v_{0y} = v_0 \sin(\theta)
  $$
- Posizione in funzione del tempo:  
  $$
  x(t) = x_0 + v_{0x}t
  $$
  $$
  y(t) = y_0 + v_{0y}t - \frac{1}{2}gt^2
  $$
- Velocità in funzione del tempo:  
  $$
  v_x(t) = v_{0x}
  $$
  $$
  v_y(t) = v_{0y} - gt
  $$
- Gittata (se $y_0 = 0$ e $y_{finale} = 0$):  
  $$
  R = \frac{v_0^2 \sin(2\theta)}{g}
  $$
- Altezza massima (se $y_0 = 0$):  
  $$
  H = \frac{v_0^2 \sin^2(\theta)}{2g}
  $$
---

### Moto Circolare Uniforme (MCU)
- Velocità angolare:  
  $$
  \omega = \frac{\Delta \theta}{\Delta t} = \frac{2\pi}{T} = 2\pi f
  $$
- Velocità tangenziale:  
  $$
  v = \omega r
  $$
- Accelerazione centripeta:  
  $$
  a_c = \frac{v^2}{r} = \omega^2 r
  $$
- Periodo:  
  $$
  T = \frac{1}{f}
  $$
- Frequenza:  
  $$
  f = \frac{1}{T}
  $$

---

## Dinamica

### Leggi di Newton
- **Prima legge (Inerzia):**  
  Un corpo permane nel suo stato di quiete o di moto rettilineo uniforme a meno che non sia costretto a cambiarlo da forze esterne.

- **Seconda legge:**  
  $$
  \vec{F}_{net} = m \vec{a}
  $$

- **Terza legge (Azione e Reazione):**  
  Se un corpo A esercita una forza su un corpo B, il corpo B esercita una forza uguale e contraria su A.

### Forze Comuni
- Forza peso:  
  $$
  \vec{P} = m \vec{g}
  $$
- Forza normale:  
  $\vec{N}$ (forza di contatto perpendicolare alla superficie)

- Forza di attrito statico:  
  $$
  |\vec{f}_s| \leq \mu_s |\vec{N}|
  $$
- Forza di attrito cinetico:  
  $$
  |\vec{f}_k| = \mu_k |\vec{N}|
  $$
- Forza elastica (Legge di Hooke):  
  $$
  \vec{F}_{el} = -k \Delta \vec{x}
  $$
- Tensione: $\vec{T}$ (forza esercitata da una fune o un cavo)

### Lavoro ed Energia
- Lavoro di una forza costante:  
  $$
  W = \vec{F} \cdot \Delta \vec{r} = F \Delta r \cos(\theta)
  $$
- Lavoro di una forza variabile:  
  $$
  W = \int_{r_i}^{r_f} \vec{F} \cdot d\vec{r}
  $$
- Energia cinetica:  
  $$
  K = \frac{1}{2}mv^2
  $$
- Teorema dell'energia cinetica:  
  $$
  W_{tot} = \Delta K = K_f - K_i
  $$
- Energia potenziale gravitazionale:  
  $$
  U_g = mgh
  $$
- Energia potenziale elastica:  
  $$
  U_e = \frac{1}{2}k(\Delta x)^2
  $$
- Forza conservativa:  
  Il lavoro compiuto da una forza conservativa non dipende dal percorso.

- Energia meccanica totale:  
  $$
  E = K + U
  $$
- Conservazione dell'energia meccanica (in assenza di forze non conservative):  
  $$
  E_i = E_f \Rightarrow K_i + U_i = K_f + U_f
  $$
- Potenza media:  
  $$
  P_{avg} = \frac{W}{\Delta t}
  $$
- Potenza istantanea:  
$$P = \vec{F} \cdot \vec{v}$$

### Quantità di Moto e Impulso
- Quantità di moto:  
$$\vec{p} = m \vec{v}$$
## Moti oscillatori sul piano verticale
Il moto oscillatorio verticale riguarda il movimento di un corpo sospeso che oscilla sotto l'azione della forza gravitazionale.
Se un moto non compie delle piccole oscillazioni non è possibile utilizzare le approssimazioni del _pendolo semplici_ questo ci costringe ad utilizzare le formule dell'energia e le proprietà della sua conservazione.
sappiamo che, dato un certo angolo $\theta$ rispetto alla verticale possiamo conoscere la _variazione di altezza_ $\Delta h$ tra la posizione verticale con $\theta = 0$:
$$\Delta h = L(1 - \cos(\theta))$$
Consideriamo un moto oscillatorio dove il corpo parte da fermo ad un angolo $\theta_0$ rispetto alla verticale con velocità iniziale $v_0 = 0$.
Osserviamo che possiamo calcolare l'altezza del corpo rispetto alla posizione verticale attraverso la formula vista prima:
$$h_i = L(1 - \cos(\theta_0))$$
Poiché l'energia cinetica del corpo al tempo $t_0$ è $0$ l'energia totale del corpo è esclusivamente quella potenziale gravitazionale.
$$E = m g L(1 - \cos(\theta_0))$$
Osserviamo adesso la variazione di energia cinetica rispetto l'angolo $\theta$:
$$\frac{1}{2} m v^2(\theta) = -mg\Delta h_\theta = mg L (\cos(\theta) - \cos(\theta_0))$$
si ha quindi che:
$$v^2(\theta) = 2 g L ((\cos(\theta) - \cos(\theta_0))$$
Si ha quindi che l'accelerazione centripeta necessaria per mantenere il moto:
$$
\vec{a}_c = \frac{v^2(\theta)}{L} = 2g\left(\cos(\theta) - \cos(\theta_0)\right)
$$
e quindi la forza centripeta necessaria:
$$
F_c = m \cdot a_c = m \cdot 2g \left(\cos(\theta) - \cos(\theta_0)\right)
$$
La tensione della corda dovrà quindi sostenere la forza centripeta e la componente della forza peso in direzione normale e quindi si ha che
$$
T(\theta) = m \cdot 2g \left(\cos(\theta) - \cos(\theta_0)\right) + m g \cos(\theta)$$
da dove si deriva che per calcolare la tensione del filo durante una oscillazione che parte con un angolo rispetto alla verticale $\theta_0$ 
$$
\boxed{T(\theta) = mg(3\cos(\theta) - 2 \cos(\theta_0))}
$$
inoltre si ha che:
$$\boxed{v(\theta) = \sqrt{2 g L ((\cos(\theta) - \cos(\theta_0))}}$$
Queste relazioni ci permettono di comprendere il comportamento dinamico di un corpo in moto oscillatorio.
