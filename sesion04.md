# Sesión 4: Potencial Eléctrico
---

## I. Resumen Teórico 📚

### 1.1. El campo electrostático es conservativo

El campo eléctrico generado por una carga puntual $q$ en el origen es:

$$\vec{E} = \frac{1}{4\pi\varepsilon_0} \frac{q}{r^2} \hat{r}$$

Para verificar que es conservativo, calculamos la circulación entre dos puntos $A$ y $B$:

$$\int_A^B \vec{E} \cdot d\vec{l} = \frac{q}{4\pi\varepsilon_0} \int_A^B \frac{\hat{r} \cdot d\vec{r}}{r^2} = \frac{q}{4\pi\varepsilon_0} \int_{r_A}^{r_B} \frac{dr}{r^2} = \frac{q}{4\pi\varepsilon_0} \left(\frac{1}{r_A} - \frac{1}{r_B}\right)$$

**Resultado fundamental:** La integral es **independiente del camino** seguido entre $A$ y $B$. Depende únicamente de las posiciones inicial y final. Esto demuestra que el campo electrostático es **conservativo**.

Como corolario, la circulación sobre cualquier camino cerrado es nula:

$$\oint \vec{E} \cdot d\vec{l} = 0$$

---

### 1.2. Definición de potencial eléctrico

Para todo campo conservativo existe una **función escalar** $V$ tal que:

$$\vec{E} = -\nabla V$$

El signo negativo indica que el campo apunta en la dirección de **decrecimiento** del potencial.

El potencial se define a partir de la energía potencial por unidad de carga:

$$V(P) = \frac{U(P)}{q_0} = -\int_{\text{ref}}^{P} \vec{E} \cdot d\vec{l}$$

donde $\text{ref}$ es un punto de referencia donde $V = 0$.

---

### 1.3. Potencial de una carga puntual

Tomando el punto de referencia en el infinito ($V(\infty) = 0$):

$$V(r) = -\int_{\infty}^{r} \frac{q}{4\pi\varepsilon_0 r'^2} dr' = \frac{q}{4\pi\varepsilon_0} \left[\frac{1}{r'}\right]_{\infty}^{r} = \frac{1}{4\pi\varepsilon_0} \frac{q}{r}$$

**Características:**
- Decae como $1/r$ (más lento que el campo $1/r^2$)
- Positivo para $q \gt; 0$, negativo para $q \lt; 0$
- Singularidad en $r = 0$ (idealización de carga puntual)

---

### 1.4. Principio de superposición para el potencial

Como las ecuaciones de Maxwell son lineales, el potencial de un sistema de cargas es la suma escalar de potenciales individuales:

$$V = \sum_{i} \frac{1}{4\pi\varepsilon_0} \frac{q_i}{r_i}$$

**Ventaja clave:** El potencial es escalar, por lo que no requiere suma vectorial (a diferencia del campo $\vec{E}$).

---

### 1.5. Extensión a distribuciones continuas de carga

| Tipo de distribución | Elemento de carga | Potencial |
|---------------------|-------------------|-----------|
| **Lineal** ($\lambda$) | $dq = \lambda\, dl$ | $V = \dfrac{1}{4\pi\varepsilon_0} \displaystyle\int \dfrac{\lambda\, dl}{r}$ |
| **Superficial** ($\sigma$) | $dq = \sigma\, dS$ | $V = \dfrac{1}{4\pi\varepsilon_0} \displaystyle\int \dfrac{\sigma\, dS}{r}$ |
| **Volumétrica** ($\rho$) | $dq = \rho\, dV$ | $V = \dfrac{1}{4\pi\varepsilon_0} \displaystyle\int \dfrac{\rho\, dV}{r}$ |

En todos los casos, $r$ es la distancia desde el elemento de carga $dq$ hasta el punto de evaluación.

---

### 1.6. Campo eléctrico como gradiente del potencial

La relación fundamental en coordenadas cartesianas:

$$\vec{E} = -\nabla V = -\left(\frac{\partial V}{\partial x}\hat{\imath} + \frac{\partial V}{\partial y}\hat{\jmath} + \frac{\partial V}{\partial z}\hat{k}\right)$$

En coordenadas cilíndricas:

$$\vec{E} = -\left(\frac{\partial V}{\partial \rho}\hat{\rho} + \frac{1}{\rho}\frac{\partial V}{\partial \phi}\hat{\phi} + \frac{\partial V}{\partial z}\hat{k}\right)$$

En coordenadas esféricas:

$$\vec{E} = -\left(\frac{\partial V}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial V}{\partial \theta}\hat{\theta} + \frac{1}{r\sin\theta}\frac{\partial V}{\partial \phi}\hat{\phi}\right)$$

**Importancia práctica:** Es frecuentemente más sencillo calcular $V$ (integral escalar) y luego derivar, que calcular $\vec{E}$ directamente (integral vectorial).

---

### 1.7. Superficies equipotenciales

**Definición:** Lugares geométricos donde $V = \text{constante}$.

**Propiedades fundamentales:**

| Propiedad | Justificación |
|-----------|---------------|
| $\vec{E} \perp$ equipotencial | Si $d\vec{l}$ es tangente a la equipotencial, $dV = -\vec{E} \cdot d\vec{l} = 0$, luego $\vec{E} \perp d\vec{l}$ |
| No se realiza trabajo sobre equipotenciales | $W = q_0 \Delta V = 0$ si $\Delta V = 0$ |
| Las líneas de campo apuntan de mayor a menor $V$ | $\vec{E} = -\nabla V$, el gradiente apunta en dirección de máximo crecimiento |


:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s04_fig1.png
:name: fig-equipotencialdipolo
:width: 60%
:align: center
Curvas equipotenciales de un dipolo.
:::

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s04_fig2.png
:name: fig-equipotencialhilo
:width: 60%
:align: center
Curvas equipotenciales de un hilo cargado.
:::

**Ejemplos de equipotenciales:**

| Distribución | Superficies equipotenciales |
|-------------|----------------------------|
| Carga puntual | Esferas concéntricas |
| Hilo infinito | Cilindros coaxiales |
| Placa infinita | Planos paralelos |
| Dipolo eléctrico | Esferas tangentes en el origen |

---

### 1.8. Energía potencial electrostática

La energía potencial de una carga $q_0$ en un punto con potencial $V$:

$$U = q_0 V$$

Para un sistema de cargas puntuales, la energía de interacción:

$$U = \frac{1}{2} \sum_{i \neq j} \frac{1}{4\pi\varepsilon_0} \frac{q_i q_j}{r_{ij}} = \frac{1}{2} \sum_{i} q_i V_i$$

donde $V_i$ es el potencial en la posición de $q_i$ debido a todas las demás cargas.

---

### 1.9. Resumen de relaciones fundamentales

| Concepto | Expresión | Interpretación |
|----------|-----------|---------------|
| Potencial de carga puntual | $V = \dfrac{q}{4\pi\varepsilon_0 r}$ | Escalar, decae como $1/r$ |
| Campo desde potencial | $\vec{E} = -\nabla V$ | El campo es el gradiente negativo |
| Diferencia de potencial | $V_B - V_A = -\displaystyle\int_A^B \vec{E} \cdot d\vec{l}$ | Trabajo por unidad de carga |
| Condición de referencia | $V(\infty) = 0$ (cargas finitas) | Convención estándar |
| Potencial en conductor | $V = \text{constante}$ | Equilibrio electrostático |

---

**Nota histórica:** El concepto de potencial eléctrico fue desarrollado por George Green (1828) y simultáneamente por Carl Friedrich Gauss. La función de Green, fundamental en la teoría del potencial, lleva su nombre en honor a estas contribuciones.


## II. Problemas Resueltos 

### Problema N° 1
**Potencial y campo de un dipolo eléctrico**
```{admonition} Expansión multipolar y coordenadas polares
:class: important
Un dipolo eléctrico consiste en dos cargas $+q$ y $-q$ separadas una distancia $d$. Calcular el potencial eléctrico en un punto $P$ muy alejado del dipolo ($r \gg d$), determinar las superficies equipotenciales y obtener el campo eléctrico usando el gradiente en coordenadas polares.
```
```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Geometría:** Dos cargas puntuales sobre el eje $z$, centradas en el origen, separación $d$.
   - **Ruta:** Potencial exacto → aproximación para $r \gg d$ → gradiente polar.
   - **Predicción:** El potencial debe decaer más rápido que $1/r$ (anulación parcial de cargas opuestas).

2. **Resolución:**

   - **Distancias exactas:**
   
     Para un punto $P(r,\theta)$ en coordenadas polares:
     
     $$r_+ = \sqrt{r^2 + \left(\frac{d}{2}\right)^2 - rd\cos\theta}$$
     
     $$r_- = \sqrt{r^2 + \left(\frac{d}{2}\right)^2 + rd\cos\theta}$$

   - **Potencial exacto:**
   
     $$V = \frac{q}{4\pi\varepsilon_0}\left(\frac{1}{r_+} - \frac{1}{r_-}\right)$$

   - **Aproximación para $r \gg d$ (serie de potencias):**
   
     Factorizando $r$:
     
     $$\frac{1}{r_\pm} = \frac{1}{r}\left[1 \mp \frac{d}{r}\cos\theta + \left(\frac{d}{2r}\right)^2\right]^{-1/2}$$
     
     Usando $(1+x)^{-1/2} \approx 1 - \frac{x}{2} + \frac{3x^2}{8}$ con $x = \mp\frac{d}{r}\cos\theta + O(d^2/r^2)$:
     
     $$\frac{1}{r_+} - \frac{1}{r_-} \approx \frac{1}{r}\left[\left(1 + \frac{d\cos\theta}{2r}\right) - \left(1 - \frac{d\cos\theta}{2r}\right)\right] = \frac{d\cos\theta}{r^2}$$

   - **Potencial del dipolo (aproximación dipolar):**
   
     Definiendo el **momento dipolar** $\vec{p} = q\vec{d}$ (vector de $-q$ a $+q$):
     
     $$V(r,\theta) = \frac{1}{4\pi\varepsilon_0} \frac{p\cos\theta}{r^2} = \frac{1}{4\pi\varepsilon_0} \frac{\vec{p}\cdot\hat{r}}{r^2}$$

   - **Superficies equipotenciales:**
   
     $V = \text{constante} \Rightarrow \frac{\cos\theta}{r^2} = C$
     
     Ecuación implícita: $r^2 = \frac{\cos\theta}{C}$
     
     Son **esferas tangentes al origen** en el plano ecuatorial ($\theta = \pi/2$).

   - **Campo eléctrico: gradiente en coordenadas polares:**
   
     $$\vec{E} = -\nabla V = -\left(\frac{\partial V}{\partial r}\hat{r} + \frac{1}{r}\frac{\partial V}{\partial\theta}\hat{\theta}\right)$$
     
     Derivadas:
     
     $$\frac{\partial V}{\partial r} = -\frac{2p\cos\theta}{4\pi\varepsilon_0 r^3}$$
     
     $$\frac{\partial V}{\partial\theta} = -\frac{p\sin\theta}{4\pi\varepsilon_0 r^2}$$
     
     Por tanto:
     
     $$\vec{E} = \frac{p}{4\pi\varepsilon_0 r^3}(2\cos\theta\,\hat{r} + \sin\theta\,\hat{\theta})$$
     
     Forma vectorial equivalente:
     
     $$\vec{E} = \frac{1}{4\pi\varepsilon_0 r^3}\left[3(\vec{p}\cdot\hat{r})\hat{r} - \vec{p}\right]$$

3. **Discusión Crítica:**
   - **Decaimiento:** $V \propto 1/r^2$ y $E \propto 1/r^3$, más rápido que carga puntual ($1/r$, $1/r^2$) debido a la cancelación parcial de cargas opuestas.
   - **Simetría azimutal:** Independiente de $\phi$ (rotacional alrededor del eje del dipolo).
   - **Líneas de campo:** Emergen del polo positivo, terminan en el negativo, densidad máxima en el eje.
   - **Campo en eje** ($\theta = 0$): $E = \frac{2p}{4\pi\varepsilon_0 r^3}\hat{r}$ (máxima intensidad).
   - **Campo en ecuador** ($\theta = \pi/2$): $E = \frac{p}{4\pi\varepsilon_0 r^3}\hat{\theta}$ (mitad de intensidad, dirección opuesta al dipolo).

4. **Análisis de Sensibilidad:**
   - Para $\theta = \pi/2$: $V = 0$ pero $E \neq 0$. El plano ecuatorial es equipotencial ($V=0$) pero no libre de campo.
   - Para $r \to \infty$: tanto $V$ como $E$ se anulan, pero la aproximación dipolar requiere $r \gg d$.

5. **Extensión:**
   - **Expansión multipolar:** El dipolo es el primer término no nulo de la expansión en serie de $1/r$ para distribuciones con carga neta cero. Términos superiores: cuadripolo, octupolo, etc.
   - **Moleculas polares:** El agua, HCl y otros compuestos poseen momento dipolar permanente, responsable de la alta permitividad del agua ($\varepsilon_r \approx 80$).
   - **Radiación dipolar:** Oscilaciones del dipolo emiten ondas electromagnéticas (antenas, transiciones atómicas).

```
---

### Problema N° 2
**Potencial y campo de un hilo cargado finito**
```{admonition} Gradiente en coordenadas cartesianas
:class: important
Un hilo recto de longitud finita $L$ posee densidad lineal de carga uniforme $\lambda$. El hilo se extiende desde $z = -L/2$ hasta $z = +L/2$ sobre el eje $z$. Calcular el potencial eléctrico en un punto $P(x,y,z)$ arbitrario del espacio y deducir el campo eléctrico aplicando el gradiente en coordenadas cartesianas.
```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Geometría:** Hilo sobre eje $z$, punto $P(x,y,z)$ en coordenadas cartesianas arbitrarias.
   - **Ruta:** Integrar potencial de elementos $dq = \lambda\,dz'$ → derivar para obtener $\vec{E} = -\nabla V$.
   - **Predicción:** Cerca del hilo ($\rho \ll L$, $|z| < L/2$), campo similar al hilo infinito; lejos ($r \gg L$), campo de carga puntual $Q = \lambda L$.

2. **Resolución:**

   - **Distancia de un elemento al punto P:**
   
     Un elemento $dq = \lambda\,dz'$ en $(0,0,z')$ está a distancia:
     
     $$r = \sqrt{x^2 + y^2 + (z-z')^2} = \sqrt{\rho^2 + (z-z')^2}$$
     
     donde $\rho = \sqrt{x^2 + y^2}$ es la distancia perpendicular al hilo.

   - **Potencial por integración:**
   
     $$V(x,y,z) = \frac{\lambda}{4\pi\varepsilon_0} \int_{-L/2}^{L/2} \frac{dz'}{\sqrt{\rho^2 + (z-z')^2}}$$
     
     Sustitución $u = z - z'$, $du = -dz'$:
     
     $$V = \frac{\lambda}{4\pi\varepsilon_0} \int_{z-L/2}^{z+L/2} \frac{du}{\sqrt{\rho^2 + u^2}}$$
     
     La integral estándar:
     
     $$\int \frac{du}{\sqrt{\rho^2 + u^2}} = \ln\left|u + \sqrt{\rho^2 + u^2}\right|$$
     
     Evaluando:
     
     $$V(\rho,z) = \frac{\lambda}{4\pi\varepsilon_0} \ln\left[\frac{(z+L/2) + \sqrt{\rho^2 + (z+L/2)^2}}{(z-L/2) + \sqrt{\rho^2 + (z-L/2)^2}}\right]$$
     
     Definiendo $R_\pm = \sqrt{\rho^2 + (z \mp L/2)^2}$ (distancias a los extremos):
     
     $$V(\rho,z) = \frac{\lambda}{4\pi\varepsilon_0} \ln\left(\frac{R_+ + z + L/2}{R_- + z - L/2}\right)$$

   - **Verificación de límites:**
     
     - **Sobre el plano perpendicular medio** ($z = 0$):
       
       $$V(\rho,0) = \frac{\lambda}{4\pi\varepsilon_0} \ln\left[\frac{\sqrt{\rho^2 + L^2/4} + L/2}{\sqrt{\rho^2 + L^2/4} - L/2}\right]$$
       
       Para $\rho \gg L$: $V \approx \frac{\lambda L}{4\pi\varepsilon_0 \rho} = \frac{Q}{4\pi\varepsilon_0 \rho}$ (carga puntual).
       
       Para $\rho \ll L$: $V \approx \frac{\lambda}{2\pi\varepsilon_0} \ln\left(\frac{L}{\rho}\right)$ (hilo infinito aproximado).

   - **Campo eléctrico: gradiente cartesiano:**
     
     $$\vec{E} = -\nabla V = -\left(\frac{\partial V}{\partial x}\hat{\imath} + \frac{\partial V}{\partial y}\hat{\jmath} + \frac{\partial V}{\partial z}\hat{k}\right)$$
     
     Usando $\rho^2 = x^2 + y^2$ y la regla de la cadena:
     
     $$\frac{\partial V}{\partial x} = \frac{\partial V}{\partial \rho}\frac{\partial \rho}{\partial x} = \frac{x}{\rho}\frac{\partial V}{\partial \rho}$$
     
     $$\frac{\partial V}{\partial y} = \frac{y}{\rho}\frac{\partial V}{\partial \rho}$$
     
     La derivada respecto a $\rho$:
     
     $$\frac{\partial V}{\partial \rho} = \frac{\lambda}{4\pi\varepsilon_0}\left[\frac{\rho}{R_+(R_+ + z + L/2)} - \frac{\rho}{R_-(R_- + z - L/2)}\right]$$
     
     Simplificando con $\frac{1}{R_\pm + (z \mp L/2)} = \frac{R_\pm - (z \mp L/2)}{\rho^2}$:
     
     $$\frac{\partial V}{\partial \rho} = \frac{\lambda}{4\pi\varepsilon_0 \rho}\left[\frac{R_+ - (z+L/2)}{R_+} - \frac{R_- - (z-L/2)}{R_-}\right] = \frac{\lambda}{4\pi\varepsilon_0 \rho}(\cos\theta_- - \cos\theta_+)$$
     
     donde $\cos\theta_\pm = \frac{z \mp L/2}{R_\pm}$ son los cosenos de los ángulos desde $P$ a los extremos del hilo.
     
     Componente radial:
     
     $$E_\rho = -\frac{\partial V}{\partial \rho} = \frac{\lambda}{4\pi\varepsilon_0 \rho}(\cos\theta_+ - \cos\theta_-)$$
     
     Componente $z$:
     
     $$\frac{\partial V}{\partial z} = \frac{\lambda}{4\pi\varepsilon_0}\left(\frac{1}{R_+} - \frac{1}{R_-}\right)$$
     
     $$E_z = -\frac{\partial V}{\partial z} = \frac{\lambda}{4\pi\varepsilon_0}\left(\frac{1}{R_-} - \frac{1}{R_+}\right)$$

3. **Discusión Crítica:**
   - **Límites verificados:** 
     - Para $L \to \infty$ con $\rho \ll L$: $E_\rho \to \frac{\lambda}{2\pi\varepsilon_0 \rho}$ (hilo infinito), $E_z \to 0$.
     - Para $\rho \gg L$: $E_\rho \approx \frac{\lambda L}{4\pi\varepsilon_0 \rho^2} = \frac{Q}{4\pi\varepsilon_0 \rho^2}$ (carga puntual), $E_z \approx 0$.
   - **Simetría:** Independencia de $\phi$ (rotacional alrededor del eje $z$), reflejada en que $V$ depende solo de $\rho$ y $z$.
   - **Equipotenciales:** Superficies de revolución alrededor del eje $z$, ni esferas ni cilindros exactos.

4. **Análisis de Sensibilidad:**
   - **Cerca del centro** ($\rho \ll L$, $|z| \ll L/2$): campo dominado por geometría local, aproximación de hilo infinito válida.
   - **Cerca de extremos** ($|z| \approx L/2$, $\rho \ll L$): efectos de borde significativos, componente $E_z$ no despreciable.
   - **Lejos del hilo** ($r = \sqrt{\rho^2 + z^2} \gg L$): campo aproximadamente radial desde el centro, con pequeñas correcciones dipolares si $z \neq 0$.

5. **Extensión:**
   - **Aro cargado:** Límite $L \to 0$ con $Q = \lambda L$ constante (anillo de carga), campo sobre el eje calculable directamente.
   - **Disco cargado:** Integración bidimensional, campo axial conocido: $E_z = \frac{\sigma}{2\varepsilon_0}\left(1 - \frac{z}{\sqrt{z^2 + R^2}}\right)$.
   - **Métodos numéricos:** Para geometrías arbitrarias, integración numérica (cuadratura gaussiana, Monte Carlo) o elementos finitos.

```
---

### Problema N° 3
**Potencial y campo de una esfera con densidad radial**
```{admonition} Compara dos soluciones diferentes
:class: important
Una esfera de radio $R$ posee densidad de carga volumétrica $\rho(r) = \rho_0 \left(1 - \frac{r}{R}\right)$. Calcular el potencial eléctrico en todo el espacio y deducir el campo eléctrico usando el gradiente en coordenadas esféricas. Verificar que ambos métodos (Gauss y gradiente) coinciden.

```
```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Geometría:** Simetría esférica, densidad dependiente solo de $r$.
   - **Ruta:** Calcular campo por Gauss → integrar para obtener $V$ → verificar $\vec{E} = -\nabla V$.
   - **Predicción:** Campo nulo en el centro, máximo en la superficie, decaimiento $1/r^2$ fuera.

2. **Resolución:**

   - **Carga total:**
   
     $$Q = \int_0^R \rho(r) 4\pi r^2 dr = 4\pi\rho_0 \int_0^R \left(r^2 - \frac{r^3}{R}\right)dr$$
     
     $$Q = 4\pi\rho_0 \left[\frac{R^3}{3} - \frac{R^3}{4}\right] = \frac{\pi\rho_0 R^3}{3}$$

   - **Campo por Ley de Gauss (previo):**
     
     - **Interior ($r \leq R$):**
       
       Carga encerrada:
       
       $$q_{enc}(r) = 4\pi\rho_0 \int_0^r \left(r'^2 - \frac{r'^3}{R}\right)dr' = 4\pi\rho_0 \left(\frac{r^3}{3} - \frac{r^4}{4R}\right)$$
       
       Campo:
       
       $$E(r) = \frac{q_{enc}}{4\pi\varepsilon_0 r^2} = \frac{\rho_0}{\varepsilon_0}\left(\frac{r}{3} - \frac{r^2}{4R}\right)$$
     
     - **Exterior ($r \geq R$):**
       
       $$E(r) = \frac{Q}{4\pi\varepsilon_0 r^2} = \frac{\rho_0 R^3}{12\varepsilon_0 r^2}$$

   - **Potencial por integración:**
     
     Tomando $V(\infty) = 0$:
     
     - **Exterior ($r \geq R$):**
       
       $$V(r) = \int_r^{\infty} E\,dr' = \frac{Q}{4\pi\varepsilon_0 r} = \frac{\rho_0 R^3}{12\varepsilon_0 r}$$
     
     - **Interior ($r \leq R$):**
       
       $$V(r) = V(R) + \int_r^R E(r')\,dr'$$
       
       Con $V(R) = \frac{\rho_0 R^2}{12\varepsilon_0}$:
       
       $$V(r) = \frac{\rho_0 R^2}{12\varepsilon_0} + \frac{\rho_0}{\varepsilon_0}\int_r^R \left(\frac{r'}{3} - \frac{r'^2}{4R}\right)dr'$$
       
       $$V(r) = \frac{\rho_0 R^2}{12\varepsilon_0} + \frac{\rho_0}{\varepsilon_0}\left[\frac{R^2}{6} - \frac{r^2}{6} - \frac{R^2}{12} + \frac{r^3}{12R}\right]$$
       
       $$V(r) = \frac{\rho_0}{12\varepsilon_0}\left(R^2 + 2R^2 - 2r^2 - R^2 + \frac{r^3}{R}\right)$$
       
       $$V(r) = \frac{\rho_0 R^2}{12\varepsilon_0}\left(2 - \frac{2r^2}{R^2} + \frac{r^3}{R^3}\right)$$

   - **Verificación: campo como gradiente:**
     
     En coordenadas esféricas con simetría radial:
     
     $$\vec{E} = -\frac{dV}{dr}\hat{r}$$
     
     Para $r \leq R$:
     
     $$\frac{dV}{dr} = \frac{\rho_0 R^2}{12\varepsilon_0}\left(-\frac{4r}{R^2} + \frac{3r^2}{R^3}\right) = -\frac{\rho_0}{\varepsilon_0}\left(\frac{r}{3} - \frac{r^2}{4R}\right)$$
     
     Por tanto:
     
     $$E(r) = \frac{\rho_0}{\varepsilon_0}\left(\frac{r}{3} - \frac{r^2}{4R}\right)$$
     
     ✓ Coincide exactamente con el resultado de Gauss.

3. **Discusión Crítica:**
   - **Continuidad:** $V(r)$ y $dV/dr$ son continuas en $r = R$, garantizando campo finito y no singular.
   - **Máximo del potencial:** En el centro ($r = 0$): $V(0) = \frac{\rho_0 R^2}{6\varepsilon_0}$.
   - **Comparación con densidad uniforme:** Para $\rho = \text{constante}$, $V(0) = \frac{3\rho R^2}{6\varepsilon_0}$; aquí es menor ($2/3$) porque la carga se concentra hacia el centro, reduciendo el potencial en el exterior.
   - **Presión electrostática:** La carga interior ejerce fuerza de expansión sobre la carga exterior. La presión en $r = R$ es $P = \frac{\rho_0^2 R^2}{24\varepsilon_0}$.

4. **Análisis de Sensibilidad:**
   - **Perfil de densidad:** Si $\rho(r) = \rho_0 (r/R)^n$, el campo en el centro es nulo solo para $n > -2$. Para $n = -2$ (singularidad), el campo diverge logarítmicamente.
   - **Cascara esférica:** Límite $\rho_0 \to \infty$, $R \to R_0$ con $\sigma = \rho_0(R-R_0)$ finito recupera el conductor: campo interior nulo, discontinuidad en la superficie.

5. **Extensión:**
   - **Modelos atómicos:** Distribuciones $\rho(r)$ similares modelan núcleos atómicos (modelo de gota líquida) o estrellas degeneradas (enanas blancas).
   - **Condensadores esféricos:** La dependencia radial de $\rho$ afecta la capacitancia efectiva y la energía almacenada.
   - **Método de elementos finitos:** Para $\rho(r)$ arbitraria (tabulada experimentalmente), la integración numérica reemplaza las formas analíticas.

```
---

## III. Actividades para el Portafolio Digital 📓

Resuelve al menos dos de los siguientes desafíos en tu **Diario de Aprendizaje** utilizando la **Estrategia de los 5 Bloques**. 


### Desafío N° 1
**Equipotenciales de un Dipolo Eléctrico**
```{admonition} Visualización de campo dipolar
:class: important
Dos cargas puntuales $+q$ y $-q$ están separadas una distancia $d = 2a$ sobre el eje $x$, centradas en el origen. 

**(a)** Deducir la expresión exacta del potencial en el plano $xy$.

**(b)** Obtener la aproximación dipolar para $r \gg a$.

**(c)** Graficar las curvas equipotenciales en el plano $xy$ usando Python, comparando el potencial exacto con la aproximación dipolar para diferentes regiones del espacio.

**(d)** Superponer las líneas de campo eléctrico sobre las equipotenciales y analizar la ortogonalidad.
```
---

### Desafío N° 2
**Equipotenciales de un Cuadrupolo Lineal**
```{admonition} Expansión multipolar de orden superior
:class: important
Tres cargas están dispuestas sobre el eje $x$: $+q$ en $x = -a$, $-2q$ en $x = 0$, y $+q$ en $x = +a$.

**(a)** Demostrar que el momento dipolar neto es nulo y que el término dominante en el potencial lejano es el cuadrupolar.

**(b)** Deducir la expresión del potencial cuadrupolar en el plano $xy$.

**(c)** Graficar las curvas equipotenciales y comparar con las de un dipolo, destacando las diferencias de simetría.
```
---

### Desafío N° 3
**Equipotenciales de un Anillo Cargado**
```{admonition} Simetría axial y potencial en el eje
:class: important
Un anillo de radio $R$ posee carga total $Q$ distribuida uniformemente. El anillo está en el plano $xy$, centrado en el origen.

**(a)** Deducir la expresión del potencial en cualquier punto del eje $z$.

**(b)** Obtener el potencial en cualquier punto del espacio usando integración numérica.

**(c)** Graficar las equipotenciales en el plano $rz$ (donde $r = \sqrt{x^2 + y^2}$) y verificar que en el eje $z$ coinciden con la expresión analítica.

```
---
### Desafío N° 4
**Equipotenciales de un Condensador Cilíndrico**
```{admonition} Campo radial y distribución de carga en conductores
:class: important
Dos cilindros conductores coaxiales de longitud infinita tienen radios $a$ (interior, carga $+\lambda$) y $b$ (exterior, carga $-\lambda$).

**(a)** Deducir el potencial en la región $a < r < b$ usando la Ley de Gauss.

**(b)** Graficar las equipotenciales en el plano transversal $xy$ y las superficies equipotenciales en 3D.

**(c)** Analizar qué ocurre con las equipotenciales si los cilindros son de longitud finita $L$ (efectos de borde).
```
---

## Desafío N° 5
**Equipotenciales de una Esfera con Cavidad Excéntrica**
```{admonition} Superposición y campo uniforme en la cavidad
:class: important
Una esfera sólida de radio $R = 2a$ posee densidad de carga uniforme $\rho$. Contiene una cavidad esférica de radio $a$ cuyo centro está desplazado una distancia $d = a$ del centro de la esfera.

**(a)** Demostrar que el campo en la cavidad es uniforme y calcular el potencial en su interior.

**(b)** Graficar las equipotenciales en un corte diametral que contenga ambos centros.

**(c)** Superponer el campo vectorial en la cavidad para visualizar su uniformidad.
```
---
