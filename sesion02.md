# Sesión 2: Campo Eléctrico
---

## I. Resumen Teórico 📚

### 1.1. Campo eléctrico de una carga puntual

El campo eléctrico de una carga puntual $Q$ en un punto $P$ esta dado por:

$$\vec{E}_{p} = k \frac{Q}{|\vec{r}_p - \vec{r}|^3} (\vec{r}_p - \vec{r})$$

Donde $k = 9 \times 10^9 \, \text{N}\cdot\text{m}^2/\text{C}^2$. 

### 1.3. Principio de Superposición de una distribución discreta
el campo eléctrico neto en un punto $P$ debido a una configuración de cargas puntuales esta dado opor:

$$\vec{E}_{total} = \sum_{i=1}^{n} \vec{E}_i$$

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s02_fig07.png
:width: 50%
:align: center
:::

### 1.4. Principio de Superposición de una distribuciones continua
El campo de una distribución continua esta dado por:

$$\vec{E} = \int d\vec{E} = k \int \frac{dq}{|\vec{r}_o- \vec{r}|^3}(\vec{r}_o- \vec{r})$$

Dependiendo de la geometría, $dq$ se reemplaza por $\lambda dl$, $\sigma dA$ o $\rho dV$.

---

## II. Problemas Resueltos 📌

### Problema 1: Interacción Anillo - Hilo Coaxial
```{admonition} Fuerza entre un anillo y un hilo cargado
:class: important
Un anillo de radio $R$ se encuentra en el plano $xz$ con su centro en el origen $(0,0,0)$. Sobre el eje $y$, se ubica un hilo conductor de longitud $L$ que comienza en $y = h$ y termina en $y = L+h$. Ambos tienen una densidad de carga lineal $\lambda$ positiva. Deducir la fuerza neta que el hilo ejerce sobre el anillo.

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s02_fig04.png
:width: 50%
:align: center
:::
```

```{admonition} Solución
:class: dropdown hint

**1. Planteamiento:**

* **Ruta de la solución:** 
    1.  Determinar el campo eléctrico $\vec{E}_a$ producido por el anillo en un punto genérico $y$ sobre su eje de simetría.
    2.  Calcular la fuerza diferencial $d\vec{F}$ que este campo ejerce sobre un elemento de carga $dq_h$ del hilo.
    3.  Integrar la expresión resultante a lo largo de la extensión del hilo ($h$ hasta $L+h$).
* **Predicción cualitativa:** Debido a la simetría radial del anillo, las componentes laterales del campo se anulan. La fuerza resultante debe ser puramente axial en la dirección $+\hat{j}$ (repulsiva).

**2. Resolución:**

**A. Campo Eléctrico del Anillo en el Eje $y$:**
Considerando el anillo en el plano $xz$, el campo en un punto $P(0, y, 0)$ viene dado por:

$\vec{E}_a(y) = \frac{k Q_{anillo} y}{(R^2 + y^2)^{3/2}} \hat{j}$

Sabiendo que $Q_{anillo} = \lambda (2\pi R)$:

$\vec{E}_a(y) = \frac{2\pi k R \lambda y}{(R^2 + y^2)^{3/2}} \hat{j}$

**B. Fuerza Diferencial sobre el Hilo ($d\vec{F}$):**

Un elemento diferencial del hilo $dq_h = \lambda dy$ situado en la posición $y$ experimenta una fuerza debida al campo del anillo:

$d\vec{F} = dq_h \cdot \vec{E}_a(y)$

$d\vec{F} = (\lambda dy) \left( \frac{2\pi k R \lambda y}{(R^2 + y^2)^{3/2}} \right) \hat{j} = 2\pi k R \lambda^2 \frac{y}{(R^2 + y^2)^{3/2}} dy \hat{j}$

**C. Integración y Cálculo de la Fuerza Neta:**

La fuerza total es la suma integral de todas las fuerzas diferenciales desde el extremo inferior ($y=h$) hasta el superior ($y=L+h$):

$\vec{F} = 2\pi k R \lambda^2 \int_{h}^{L+h} \frac{y}{(R^2 + y^2)^{3/2}} dy \hat{j}$

Para resolver, usamos el cambio de variable $u = R^2 + y^2 \rightarrow du = 2y dy$:

$\int \frac{y}{(R^2 + y^2)^{3/2}} dy = -\frac{1}{\sqrt{R^2 + y^2}}$

Evaluando en los límites:

$\vec{F} = 2\pi k R \lambda^2 \left[ -\frac{1}{\sqrt{R^2 + (L+h)^2}} - \left( -\frac{1}{\sqrt{R^2 + h^2}} \right) \right] \hat{j}$

**Resultado Final:**
$\vec{F} = 2\pi k R \lambda^2 \left( \frac{1}{\sqrt{R^2 + h^2}} - \frac{1}{\sqrt{R^2 + (L+h)^2}} \right) \hat{j}$

**3. Discusión Crítica:**
* 🟢 **Verde (idealización):** La densidad de carga es uniforme.  
* 🟡 **Ámbar (Validación):** La dirección $+\hat{j}$ es coherente con la repulsión de cargas del mismo signo.
* 🔴 **Rojo (Interpretación):** Si el hilo se acerca al anillo, existe una distancia en la que el hilo experimentará la máxima fuerza de repulsión.

**4. Análisis de Sensibilidad:**

* **¿Y si el hilo fuera infinito ($L \to \infty$)?** La fuerza se estabiliza en un valor finito: $\vec{F} = \frac{2\pi k R \lambda^2}{\sqrt{R^2 + h^2}} \hat{j}$. Esto es útil para calcular tensiones mecánicas en cables de gran longitud cerca de bobinas.

**5. Transferencia y Extensión:**

* **Aplicación:** Este modelo se utiliza para calcular la fuerza de levitación o atracción en actuadores electrostáticos.

✍️ **Hazlo Tú: Profundiza el análisis**

Resuelve el problema con algunas variaciones:

1. Demostrar que la fuerza de repulsión es máxima cuando $h = R/\sqrt{2}$.

2. Demostrar que la fuerza es máxima si el radio del anillo es:

    $R_{opt} = \sqrt{ \frac{h^{4/3}(L+h)^2 - (L+h)^{4/3}h^2}{(L+h)^{4/3} - h^{4/3}} }$
```
---

### Problema 2: Interacción Disco - Hilo Coaxial
```{admonition} Fuerza entre un Disco - Hilo Coaxial
:class: important
Un disco de radio $R$ se encuentra en el plano $xz$ con su centro en el origen. El disco posee una densidad de carga superficial uniforme $\sigma$. Sobre el eje $y$, se coloca un hilo conductor de longitud $L$ que se extiende desde $y=h$ hasta $y=h+L$, con una densidad de carga lineal $\lambda$. Determine la fuerza neta que el disco ejerce sobre el hilo

::: {figure} https://github.com/jnolorbe/fisica3/blob/main/figuras/s02_fig05.png
:width: 70%
:align: center
:::
```

```{admonition} Solución
:class: dropdown hint

**1. Planteamiento:**

* **Fenómeno dominante:** Interacción de campos eléctricos generados por distribuciones superficiales sobre distribuciones lineales.
* **Ruta de la solución:** 
    
    1. Partir de la expresión del campo eléctrico axial de un disco.
    2. Definir un diferencial de fuerza $d\vec{F}$ sobre un elemento infinitesimal del hilo.
    3. Integrar dicha fuerza a lo largo de la extensión del hilo.

* **Predicción cualitativa:** La fuerza será puramente axial ($+\hat{j}$) debido a la simetría del disco. Se espera que la magnitud sea mayor que la de un anillo (a igual carga total) debido a la proximidad de la carga en el centro del disco.

**2. Resolución:**

**A. Campo Eléctrico del Disco en el eje $y$:**
El campo producido por un disco de radio $R$ en un punto $y$ de su eje es:
$\vec{E}_{disco}(y) = \frac{\sigma}{2\epsilon_0} \left( 1 - \frac{y}{\sqrt{y^2 + R^2}} \right) \hat{j}$

**B. Fuerza Diferencial sobre el Hilo:**
Un elemento de carga $dq = \lambda dy$ en el hilo, ubicado en una posición $y$ arbitraria, experimenta una fuerza:

$d\vec{F} = dq \cdot \vec{E}_{disco}(y) = (\lambda dy) \frac{\sigma}{2\epsilon_0} \left( 1 - \frac{y}{\sqrt{y^2 + R^2}} \right) \hat{j}$

**C. Integración de la Fuerza Neta:**
La fuerza total $\vec{F}$ es la integral desde $y = h$ hasta $y = h+L$:

$\vec{F} = \frac{\sigma \lambda}{2\epsilon_0} \int_{h}^{h+L} \left( 1 - \frac{y}{\sqrt{y^2 + R^2}} \right) dy \hat{j}$

Resolviendo las integrales inmediatas:

1. $\int 1 \, dy = y$

2. $\int \frac{y}{\sqrt{y^2 + R^2}} dy = \sqrt{y^2 + R^2}$ (usando sustitución $u = y^2 + R^2$)

Evaluando los límites de integración:

$\vec{F} = \frac{\sigma \lambda}{2\epsilon_0} \left[ \left( y - \sqrt{y^2 + R^2} \right) \right]_{h}^{h+L} \hat{j}$

**Resultado Final:**

$\vec{F} = \frac{\sigma \lambda}{2\epsilon_0} \left[ L - \sqrt{(h+L)^2 + R^2} + \sqrt{h^2 + R^2} \right] \hat{j}$

**3. Discusión Crítica:**

* 🟢 **Verde (Análisis Dimensional):** La expresión es consistente. El término entre corchetes tiene unidades de longitud $[L]$. Al multiplicar por $[\sigma \lambda / \epsilon_0]$, se obtienen Newtons.
* 🟡 **Ámbar (Caso del Plano Infinito):** Si el radio del disco crece indefinidamente ($R \to \infty$), los términos con raíz dominan y se cancelan parcialmente, tendiendo a un valor de campo uniforme. Sin embargo, para un plano infinito real, la fuerza sobre el hilo sería $F = \frac{\sigma \lambda L}{2\epsilon_0}$, lo cual es independiente de la distancia $h$.
* 🔴 **Rojo (Interacción Cercana):** Si el hilo toca el disco ($h=0$), la fuerza es finita: $F = \frac{\sigma \lambda}{2\epsilon_0} (L - \sqrt{L^2+R^2} + R)$. Esto es físicamente coherente ya que no hay una carga puntual que cause una divergencia infinita.

**4. Análisis de Sensibilidad:**

* **¿Y si $R \ll h$?** El disco debe comportarse como una carga puntual $Q = \sigma (\pi R^2)$. Al expandir las raíces mediante series de Taylor, se recuperaría la Ley de Coulomb para distribuciones puntuales.
* **¿Y si el hilo tiene densidad variable $\lambda(y) = cy$?** La integral se volvería más compleja, requiriendo métodos de integración por partes, lo cual modelaría mejor un cable real bajo tensión variable.

**5. Transferencia y Extensión:**
* **Aplicación en FIEE:** Este cálculo es fundamental para determinar la fuerza de deflexión en **actuadores de microespejos (MEMS)**
```
---

## III. Actividades para el Portafolio Digital 📓

Resuelve al menos dos de los siguientes desafíos en tu **Diario de Aprendizaje** utilizando la **Estrategia de los 5 Bloques**. 

### Desafío 1: Propulsión ionica
En los sistemas de propulsión iónica y microscopía electrónica, se utilizan cilindros cargados para acelerar o enfocar partículas. Se presenta una corteza cilíndrica delgada de radio $R$ y longitud $L$, con una densidad de carga superficial uniforme $\sigma$. El cilindro se ubica sobre el eje $y$, desde $y = 0$ hasta $y = L$.

1. **Analísis Vectorial:** Deduzca la expresión vectorial del campo eléctrico $\vec{E}$ en un punto $P$ sobre el eje axial. Su solución debe ser válida tanto para puntos exteriores ($y_p > L$) como para puntos interiores ($0 < y_p < L$).
2. **Visualización y Morfología del Campo:** 
Utilice GeoGebra o MATLAB para graficar la magnitud del campo $E_y$ en función de la posición $y_p$. Realice una gráfica comparativa para tres geometrías distintas ¿Cómo cambia la "suavidad" del campo en el interior del cilindro al variar la relación $L/R$?: 
    - a) Cilindro largo ($L = 5R$)
    - b) Cilindro cuadrado ($L = R$)
    - c) Anillo ancho ($L = 0.2R$)
3. **Optimización:** Demuestre analíticamente (mediante derivación) que el campo alcanza sus valores máximos y mínimos locales cerca de las "bocas" del cilindro ($y = 0$ y $y = L$).
4. **El Salto de Frontera y Singularidades:** Evalúe matemáticamente qué sucede cuando el punto $P$ cruza exactamente el plano de la base ($y_p = 0$ o $y_p = L$). 
* ¿Existe una discontinuidad en el valor del campo? 
* Explique físicamente este fenómeno: ¿Es una falla del modelo matemático o un comportamiento real de las superficies cargadas?
5. **Convergencia Geométrica ($R \gg L$):** Si el radio $R$ se vuelve mucho más grande que la longitud $L$, realice una expansión en serie de potencias de su resultado. 
* ¿A qué distribución conocida se aproxima el sistema? 
* ¿Se comporta como un anillo cargado o como un disco con un agujero? Justifique su respuesta basándose en las líneas de campo.
6. **Aplicación: Ingeniería de Frenado Iónico** Imagine que este cilindro se usa para frenar un ion positivo que viene desde el infinito. 
* Si el radio $R$ es fijo por limitaciones de espacio, ¿existe una longitud $L$ óptima que maximice la fuerza de frenado antes de que la partícula entre al cilindro? Justifique su propuesta de diseño.

---

### Desafío 2: Electrodo cuadrado

En el diseño de microchips, sensores capacitivos y blindajes para componentes electrónicos, las superficies cuadradas son la norma. A diferencia del disco, una placa cuadrada carece de simetría radial, lo que genera variaciones en la intensidad del campo al acercarse a las esquinas. Se tiene una lámina cuadrada delgada de lado $L$ situada en el plano $xz$, centrada en el origen $(0,0,0)$. La lámina posee una densidad de carga superficial uniforme $\sigma$. 

1. **Analísis Vectorial:** Deduzca la expresión vectorial del campo eléctrico $\vec{E}$ en un punto $P(0, y, 0)$.
* **Instrucción:** Divida la lámina en hilos diferenciales de ancho $dz$ y longitud $L$. Utilice el resultado conocido del campo de un hilo delgado finito. 

2. **Visualización:** Utilice Geogebra o Matlab para graficar $E_y$ vs $y$. Compare esta curva con la de un disco de radio $R = L/2$ y misma densidad $\sigma$.
* **Discusión:** ¿Por qué para valores de $y$ muy pequeños la lámina cuadrada "parece" generar un campo más intenso que el disco? Analice la contribución de las esquinas del cuadrado. Si la gráfica muestra una discontinuidad en $y=0$, analice si es un error de la función $\arctan$ o una propiedad física de la lámina.

3. **Límite de Plano Infinito:** Demuestre mediante límites que cuando $L \to \infty$, el campo recupera el valor constante $\sigma/2\epsilon_0$. ¿A partir de qué distancia $y$ (en términos de $L$) el error de considerar la placa como "infinita" supera el $10\%$?
* **Límite de Carga Puntual:** Para $y \gg L$, el sistema se comporta directamente como una carga puntual?

4. **Reflexión:** Si esta placa fuera un electrodo en un sensor de presión, ¿cómo afectaría la falta de simetría radial a la uniformidad del campo si el sensor no estuviera perfectamente centrado? Investigue el concepto de **fuerzas de borde** en placas cuadradas.

---

### Desafío 3: El Domo Electrostático

En el diseño de sensores de partículas y en el análisis de campos en la punta de electrodos de alta tensión, las geometrías semiesféricas son comunes. A diferencia de la esfera completa (donde el campo interno es cero), la **hemiesfera** presenta un campo neto en su centro que debe ser calculado con precisión para evitar la ruptura dieléctrica en aplicaciones de potencia. Se tiene una cáscara hemisférica delgada de radio $R$ situada en el semiespacio superior ($y \geq 0$), centrada en el origen $(0,0,0)$. La cáscara posee una densidad de carga superficial uniforme $\sigma$. 

1.  **Analísis Vectorial:** Deducir la expresión vectorial del campo eléctrico $\vec{E}$ en el **centro de la curvatura** (el origen). 
- Compare este resultado con el campo de un disco del mismo radio $R$ en su centro ($E = \sigma/2\epsilon_0$). ¿Por qué la curvatura de la hemiesfera reduce el campo a la mitad a pesar de tener más área cargada? 
- Extienda su análisis para un punto $P(0, y, 0)$ arbitrario sobre el eje.

2. **Visualización:** Utilice Geogebra o Matlab para graficar la intensidad del campo desde $y = -2R$ hasta $y = 2R$. 
* **Hallazgo Principal:** Identifique si existe alguna discontinuidad o cambio de pendiente al cruzar el plano base ($y = 0$) o al pasar por el "techo" del domo ($y = R$).

3. **Casos Límite:** 
- Si unimos dos hemiesferas con cargas opuestas para formar una esfera, ¿cuál sería el campo en el centro?
- Si el radio $R$ crece hacia el infinito manteniendo $\sigma$ constante, ¿el campo en el centro cambia? Explique la independencia o dependencia del radio en este resultado.
- ¿Qué sucedería si la carga no fuera uniforme, por ejemplo $\sigma(\theta) = \sigma_0 \cos\theta$? ¿Cómo afectaría esto al diseño de un sensor de posición?

---