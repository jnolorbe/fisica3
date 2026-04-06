# Sesión 1: Ley de Coulomb
---

## I. Resumen Teórico 📚

### 1.1. Distribuciones Continuas de Carga
En ingeniería, a menudo tratamos con sistemas donde la carga eléctrica está distribuida en volúmenes, superficies o líneas. 

* **Densidad Lineal ($\lambda$):** Para hilos o varillas. $\lambda = \frac{dq}{dl}$ $[C/m]$.
* **Densidad Superficial ($\sigma$):** Para láminas o placas. $\sigma = \frac{dq}{dA}$ $[C/m^2]$.
* **Densidad Volumétrica ($\rho$):** Para sólidos conductores o dieléctricos. $\rho = \frac{dq}{dV}$ $[C/m^3]$.

**Distribución Uniforme vs. No Uniforme:**
- **Uniforme:** La densidad es constante en toda la geometría del cuerpo cargado.
- **No Uniforme:** La densidad depende de la posición. En este caso, la carga total o de una porción geométrica se halla mediante integración: $Q = \int dq$. Dependiendo de la geometría, $dq$ se reemplaza por $\lambda dl$, $\sigma dA$ o $\rho dV$.

### 1.2. Interacción Electrostática: Ley de Coulomb

La fuerza de interacción electrostática entre dos cargas puntuales $q_1$ y $q_2$ se define vectorialmente como:

$$\vec{F}_{12} = k \frac{q_1 q_2}{|\vec{r}_2 - \vec{r}_1|^3} (\vec{r}_2 - \vec{r}_1)$$

Donde $k = 9 \times 10^9 \, \text{N}\cdot\text{m}^2/\text{C}^2$. Se cumple la tercera ley de Newton: $\vec{F}_{12} = -\vec{F}_{21}$.

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig01.png
:width: 50%
:align: center
Figura 1. Fuerza electrostática entres dos cargas puntuales
:::

### 1.3. Principio de Superposición de una distribución discreta
Cuando una carga puntual $q_0$ interactúa con una distribución discreta de cargas puntuales, la fuerza total es la sumatoria de las contribuciones de cada carga puntual:

$$\vec{F}_{total} = \sum_{i=1}^{n} \vec{F}_i$$

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig02.png
:width: 50%
:align: center
Figura 2. Fuerzas neta de una distribución discreta de cargas
:::

### 1.4. Principio de Superposición de una distribuciones continua
Cuando una carga puntual $q_0$ interactúa con una distribución continua, la fuerza total es la suma integral de las fuerzas infinitesimales $d\vec{F}$ de cada elemento de carga $dq$:

$$\vec{F} = \int d\vec{F} = k q_0 \int \frac{dq}{|\vec{r}_o- \vec{r}|^3}(\vec{r}_o- \vec{r})$$

Dependiendo de la geometría, $dq$ se reemplaza por $\lambda dl$, $\sigma dA$ o $\rho dV$.

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig03.png
:width: 50%
:align: center
Figura 3. Fuerza neta de una distribución continua de carga
:::

---

## II. Problemas Resueltos 📌

### Problema 1: carga en una porcion 
```{admonition} Distribución continua de carga sobre un hilo
:class: important
Una barra de ámbar de longitud $L$ se sitúa sobre el eje $x$, desde $x=0$ hasta $x=L$. Tras ser frotada con seda, adquiere una distribución de carga no uniforme que sigue el modelo exponencial:

$\lambda(x) = \lambda_0 (e^{x/L} - 1)$

Donde $\lambda_0$ es una constante de densidad de referencia. Deducir la **carga eléctrica** contenida en la primera mitad de la barra (desde $x=0$ hasta $x=L/2$).

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig04.png
:width: 50%
:align: center
Figura 4. Distribución de carga lineal no uniforme
:::
```

```{admonition} Solución
:class: dropdown hint
#### 1. Marco Teórico e Hipótesis Inicial
* **Fenómeno:** Acumulación de carga no lineal en un cuerpo aislante (ámbar).
* **Ruta de solución:** Dado que la densidad $\lambda(x)$ no es constante, debemos integrar el diferencial de carga $dq = \lambda(x)dx$ en el intervalo solicitado $[0, L/2]$.
* **Predicción cualitativa:** En $x=0$, $\lambda(0) = \lambda_0(e^0 - 1) = 0$. La densidad crece a medida que avanzamos hacia $L$. Por lo tanto, esperamos que la carga en la primera mitad sea significativamente menor que en la segunda mitad.

#### 2. Resolución Técnica
1. **Planteamiento de la integral:**

   $Q_{parcial} = \int_{0}^{L/2} \lambda(x) dx = \int_{0}^{L/2} \lambda_0 (e^{x/L} - 1) dx$
   
   $Q_{parcial} = \lambda_0 \left[ L e^{x/L} - x \right]_{0}^{L/2}$

3. **Evaluación de límites:**

   $Q_{parcial} = \lambda_0 \left[ (L e^{1/2} - L/2) - (L e^0 - 0) \right]$

   $Q_{parcial} = \lambda_0 \left[ L\sqrt{e} - \frac{L}{2} - L \right] = \lambda_0 L \left( \sqrt{e} - 1.5 \right)$

4. **Resultado Numérico Aproximado:**
   Como $\sqrt{e} \approx 1.6487$:

   $Q_{parcial} \approx \lambda_0 L (1.6487 - 1.5) \approx 0.1487 \lambda_0 L$

#### 3. Discusión Crítica (Semáforo)
* 🔴 **Rojo:** Se asume que el frotamiento con seda produce un perfil exponencial perfecto. En la realidad, factores como la rugosidad del ámbar y la humedad ambiental introducen "ruido" en la distribución.
* 🟢 **Verde:** El resultado es consistente. En una distribución uniforme, la carga en la mitad sería $0.5 \lambda L$. Aquí es solo $\approx 0.15 \lambda_0 L$, confirmando que la carga está concentrada en el extremo distal.
* 🔵 **Azul:** La unidad final es Coulomb ($[C/m] \cdot [m] = [C]$), lo que valida el análisis dimensional.

#### 4. Análisis de Sensibilidad ("¿Y si...?")
* ¿Qué pasaría si calculamos la carga en la segunda mitad ($L/2$ a $L$)? El resultado sería aproximadamente $0.569 \lambda_0 L$. ¡La segunda mitad tiene casi **4 veces más carga** que la primera! Esto es crítico para evitar descargas puntuales en un solo extremo de un componente electrónico.

#### 5. Transferencia y Extensión
* **Ingeniería Electrónica:** Este modelo matemático es idéntico al de la **inyección de portadores minoritarios** en la base de un transistor de unión bipolar (BJT). La eficiencia del transistor depende de qué tan rápido decae esta "densidad" de carga.

✍️ **Hazlo Tú: Desafío de Modelado de Cargas Reales**

Para cada uno de los siguientes casos, plantea la integral de carga $Q = \int \lambda(x) dx$, resuelve analíticamente y reporta tu resultado final:

1. Sensor de Proximidad (Distribución Cuadrática): Un filamento de longitud $L = 0.20$ m posee una densidad $\lambda(x) = \lambda_0 (x/L)^2$. Si $\lambda_0 = 5.0 \, \mu\text{C/m}$, calcula la carga total en la varilla.

2. Línea con Atenuación (Distribución Exponencial): Una línea de transmisión de $L = 10.0$ m presenta una densidad $\lambda(x) = \lambda_0 e^{-x/L}$. Si $\lambda_0 = 12 \, \mu\text{C/m}$, calcula la carga contenida en el tramo final (desde $x = 5.0$ m hasta $x = 10.0$ m).

3. Interferencia de AC (Distribución Senoidal): Una antena de dipolo de longitud $L = 0.50$ m tiene una distribución inducida $\lambda(x) = \lambda_0 \sin(\pi x / L)$. Si $\lambda_0 = 2.0 \, \mu\text{C/m}$, calcula la carga neta en toda la antena.

**Reto Metacognitivo:** En el ejercicio de la Antena (3), si integraras la función $\lambda(x) = \lambda_0 \cos(\pi x / L)$ en el mismo intervalo $[0, L]$, el resultado matemático de la carga neta sería exactamente cero. Como ingeniero de Telecomunicaciones o Electrónica, ¿significa esto que no hay interacción eléctrica con cargas externas? ¿Qué diferencia física fundamental existe entre una distribución cuya integral de carga es $Q$ y una donde es $0$ pero con presencia de dipolos? 

```
---

### Problema 2: Interacción Vectorial de Cargas Puntuales
```{admonition} Distribución discreta de cargas
:class: important
Deducir la fuerza neta sobre la carga puntual $q_1 = +20 \mu C$ debido a la interacción con las cargas $q_2 = -30 \, \mu C$ y $q_3=+40 \, \mu C$. 

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig05.png
:width: 70%
:align: center
Figura 5. Distribución de tres cargas puntuales
:::
```

```{admonition} Solución
:class: dropdown hint

#### 1. Marco Teórico e Hipótesis Inicial
* **Fenómeno:** Superposición de fuerzas electrostáticas en un sistema discreto.
* **Ruta de solución:** EAplicaremos la forma vectorial de la Ley de Coulomb. Calcularemos cada vector de fuerza respecto al origen y realizaremos la suma vectorial..
* **Predicción cualitativa:** $q_1$ (positiva) será atraída por $q_2$ (hacia el tercer cuadrante) y repelida por $q_3$ (hacia el primer cuadrante). La dirección final dependerá de cuál interacción predomine.


#### 2. Resolución Técnica
1. **Definición de vectores posición y distancias:**

   - De $q_2$ a $q_1$: $\vec{r}_{21} = \vec{r}_1 - \vec{r}_2 = (2,2) - (-3, 1) = (5\hat{i} + 1\hat{j})$ m.  
     $|\vec{r}_{21}| = \sqrt{5^2 + 1^2} = \sqrt{26} \approx 5.10$ m.

   - De $q_3$ a $q_1$: $\vec{r}_{31} = \vec{r}_1 - \vec{r}_3 = (2,2) - (1, -3) = (1\hat{i} + 5\hat{j})$ m.  
     $|\vec{r}_{31}| = \sqrt{1^2 + 5^2} = \sqrt{26} \approx 5.10$ m.

2. **Cálculo de fuerzas individuales:**

   - $\vec{F}_{21} = k \frac{q_2\,q_1}{|\vec{r}_{21}|^3}\,\vec{r}_{21} \approx (-0.2035\hat{i} - 0.0407\hat{j}) N$

   - $\vec{F}_{31} = k \frac{q_3\,q_1}{|\vec{r}_{31}|^3}\,\vec{r}_{31} \approx (0.0543\hat{i} + 0.2715\hat{j})N$

3. **Superposición (Fuerza Neta):**
   - $\vec{F}_{neta} = \vec{F}_{21} + \vec{F}_{31}$
   - **$\vec{F}_{neta} \approx (-0.149\hat{i} + 0.231\hat{j})N$**

#### 3. Discusión Crítica (Semáforo)
* 🔴 **Rojo:** Se asume que las cargas están fijas en el espacio. En un sistema real de partículas libres, estas fuerzas provocarían una aceleración inmediata, desarmando la configuración en milisegundos.
* 🟢 **Verde:** El resultado muestra que la carga $q_1$ tiende a moverse hacia el segundo cuadrante, lo cual es coherente ya que la repulsión de $q_3$ en el eje $y$ es más fuerte que la atracción de $q_2$.
* 🔵 **Azul:** Las magnitudes ($\approx 0.2$ N) son pequeñas para objetos macroscópicos, pero muy intensas para partículas atómicas.

#### 4. Análisis de Sensibilidad ("¿Y si...?")
* Si la carga $q_3$ se hiciera aproximadamente 3.75 veces su valor ($+150 \, \mu\text{C}$), la atracción horizontal de $q_2$, sería contrarestado, haciendo que la fuerza neta sea practicamente vertical.

#### 5. Transferencia y Extensión
* **Biomédica:** En la técnica de **Electroforesis**, se aplican fuerzas similares para separar proteínas o fragmentos de ADN en un gel. La precisión en la ubicación de los electrodos (nuestras cargas puntuales) determina la resolución del diagnóstico.
```
---

### Problema 3: Fuerza de una Barra sobre carga puntual
```{admonition} Ley de Coulomb para distribuciones de carga continua
:class: important

Una varilla delgada de longitud $L$ se ubica sobre el eje $x$ desde $x = -L/2$ hasta $x = L/2$. La varilla posee una densidad de carga que varía linealmente: $\lambda(x) = \lambda_o(x+L/2)$, donde $ \lambda_o$ es una constante con unidades de $[C/m^2]$. Una carga puntual $+q_0$ se sitúa en el eje $y$ a una distancia $a$ del origen (en la mediatriz de la barra). Deducir la expresión vectorial de la fuerza neta sobre $q_0$.

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig06.png
:width: 50%
:align: center
Figura 6. Fuerzas de una linea cargada sobre una carga puntual
:::
```

```{admonition} Solución
:class: dropdown hint
:class: dropdown hint

#### 1. Marco Teórico e Hipótesis Inicial
* **Fenómeno:** Interacción electrostática con una distribución lineal asimétrica.
* **Ruta de solución:** Definimos el diferencial de carga $dq = \lambda_o(x + L/2)dx$. El vector posición desde $dq$ hacia $q_0$ es $\vec{r} = -x\hat{i} + a\hat{j}$. Plantearemos la integral vectorial y resolveremos para cada componente.
* **Predicción cualitativa:** Como la carga aumenta hacia la derecha, habrá una fuerza de repulsión hacia la izquierda (componente $-x$) y hacia arriba (componente $+y$).

#### 2. Resolución Técnica

1. **Elementos Vectoriales:**
   - $dq = \lambda_o(x - L/2)dx$
   - $\vec{r}_o - \vec{r} = -x\hat{i} + a\hat{j}$ (de $dq$ a $q_0$) 
   - $|\vec{r}_o - \vec{r}|^3 = (x^2 + a^2)^{3/2}$

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s01_fig07.png
:width: 50%
:align: center
Figura 7. Elementos vectorial del problema
:::

2. **Principio de superposición:**

   $$\vec{F} = \int d\vec{F} = k q_0 \int_{-L/2}^{L/2} \frac{[\lambda_o(x + L/2)dx]}{(x^2 + a^2)^{3/2}} (-x\hat{i} + a\hat{j})$$

3. **Componente $X$ (Empuje Lateral):**
   $$F_x = -k \lambda_o q_0 \left[ \int_{-L/2}^{L/2} \frac{x^2 dx}{(x^2 + a^2)^{3/2}} + \frac{L}{2} \int_{-L/2}^{L/2} \frac{x dx}{(x^2 + a^2)^{3/2}} \right]$$
   
   *La segunda integral es cero por ser una función impar en un intervalo simétrico*

   $$F_x = -k \lambda_o q_0 \left[ \ln\left(x + \sqrt{x^2 + a^2}\right) - \frac{x}{\sqrt{x^2 + a^2}} \right]_{-L/2}^{L/2}$$

4. **Componente $Y$ (Empuje Vertical):**
   $$F_y = k \lambda_o q_0 a \left[ \int_{-L/2}^{L/2} \frac{x dx}{(x^2 + a^2)^{3/2}} + \frac{L}{2} \int_{-L/2}^{L/2} \frac{dx}{(x^2 + a^2)^{3/2}} \right]$$
   
   *La primera integral es cero. Solo sobrevive el término constante de la densidad.*
   
   $$F_y = \frac{k \lambda_o q_0 a L}{2} \left[ \frac{x}{a^2\sqrt{x^2 + a^2}} \right]_{-L/2}^{L/2} = \frac{k \lambda_o q_0 L}{a} \left[ \frac{L/2}{\sqrt{(L/2)^2 + a^2}} \right]$$

5. **Resultado Vectorial:**
   $\vec{F} = F_x \hat{i} + F_y \hat{j}$ (con los valores evaluados anteriormente).

#### 3. Discusión Crítica (Semáforo)
* 🔴 **Rojo:** Se ignora la polarización que $q_0$ podría inducir en la varilla si esta fuera conductora (efecto imagen).
* 🟢 **Verde:** La componente $F_y$ resulta positiva y $F_x$ negativa, lo cual coincide con la asimetría de la carga acumulada hacia la derecha.
* 🔵 **Azul:** Este modelo representa un cable que ha sido cargado por fricción de forma desigual, un problema común en el blindaje de equipos de **Telecomunicaciones**.

#### 4. Análisis de Sensibilidad ("¿Y si...?")
* Si $L \to 0$ manteniendo $Q$ constante, $F_x$ debe tender a cero y $F_y$ debe recuperar la forma de la Ley de Coulomb para carga puntual. Esto valida que la asimetría es un efecto de la extensión geométrica.

#### 5. Transferencia y Extensión
* **En la industría:** En procesos de pintura electrostática, una boquilla que no distribuye la carga uniformemente genera fuerzas laterales que provocan un acabado desigual.
````
---

## 📓 Actividades para el Portafolio Digital

Como futuro ingeniero, tu portafolio es la evidencia de tu capacidad para modelar la realidad física con rigor. Resuelve al menos dos de los siguientes desafíos en tu **Diario de Aprendizaje** utilizando la **Estrategia de los 5 Bloques**. 

> **Instrucción de Auditoría IA:** Puedes apoyarte en herramientas de IA para el cálculo, pero tu misión principal es **auditar** el resultado. Identifica si la IA olvidó el diferencial de área ($r dr d\theta$), si confundió los límites de integración o si ignoró la naturaleza vectorial de la fuerza. **Tu nota depende de tu capacidad para corregir a la máquina.**

---
### Desafío 1: El Sensor Curvo (Distribución Lineal Polar)
Un hilo delgado en forma de semicircunferencia de radio $R$ se ubica en los cuadrantes I y II del plano $xy$. La densidad de carga no es uniforme y depende de la posición angular $\theta$ según el modelo:
$$\lambda(\theta) = \lambda_0 \sin(\theta)$$
* **La Tarea:** Determina la carga total contenida únicamente en el primer cuadrante (de $\theta = 0$ a $\theta = \pi/2$).
* **Conflicto de Ingeniería:** ¿Por qué la carga es máxima a $90^\circ$ y nula en los extremos del hilo ($0^\circ$ y $180^\circ$)? 

### Desafío 2: El Disco de Control (Distribución Superficial)
Un disco aislante de radio $R$, componente de un sensor de presión, tiene una carga concentrada en el centro que decae linealmente hacia la periferia:
$$\sigma(r) = \sigma_0 \left( 1 - \frac{r}{R} \right)$$
* **La Tarea:** Calcula la carga total contenida en la porción central del disco, definida por un radio interno $r = R/2$.
* **Reto Crítico:** Si pides a una IA que plantee el diferencial de área $dA$, ¿Cuál es la diferencia entre usar $r \, dr \, d\theta$ o $2 \pi dr$.

### Desafío 3: El Núcleo Esférico (Distribución Volumétrica)
En un modelo de blindaje para instrumentación biomédica, se analiza una esfera de radio $R$ donde la carga es máxima en el origen y decae exponencialmente:
$$\rho(r) = \rho_0 e^{-r/R}$$
* **La Tarea:** Determina la carga total encerrada dentro de una esfera interna de radio $r = R/4$.
* **Reto Crítico:** Este modelo es análogo a la densidad de portadores en una unión semiconductora esférica. ¿Cómo afecta esta caída exponencial a la fuerza que ejercería sobre una carga puntual comparado con una distribución uniforme?

### Desafío 4: Estabilidad en la Celda Hexagonal (Distribución Discreta)
Se colocan 6 cargas puntuales en los vértices de un hexágono regular de lado $d$. Las cargas en los vértices alternan su signo: $+q, -q, +q, -q, +q, -q$. Una carga de prueba $+q_0$ se ubica exactamente en el centro del hexágono.
* **La Tarea:** Determina vectorialmente la fuerza neta sobre $q_0$.
* **Reto Metacognitivo:** Antes de calcular, usa la simetría. Si todas las cargas fueran del mismo signo, la fuerza sería cero. Al alternar signos, ¿se rompe el equilibrio o la simetría radial aún genera una cancelación total? Justifica analíticamente.

### Desafío 5: El Anillo Deflector (Fuerza Axial)
Un anillo delgado de radio $R$ tiene una carga total $Q$ distribuida uniformemente. 
* **La Tarea:** Deduce la expresión de la fuerza eléctrica sobre una carga puntual $q_0$ situada en el eje axial (eje $z$) a una distancia $z$ del centro del anillo.
* **Análisis de Sensibilidad:** Demuestra mediante derivadas en qué valor de $z$ la fuerza experimenta su valor máximo. Como ingeniero en electrónica, si este anillo fuera parte de un sistema de enfoque de haces de electrones, ¿en qué región situarías el haz para obtener la máxima deflexión?

---