# Sesión 3: Flujo Eléctrico
---

## I. Resumen Teórico 📚

### 1.1. Líneas de Campo Eléctrico
Las líneas de campo son una herramienta topológica para mapear el campo vectorial $\vec{E}$ en el espacio. Sus propiedades fundamentales son:

* **Continuidad:** Se originan en cargas positivas (fuentes) y mueren en cargas negativas (sumideros), No pueden cerrarse sobre sí mismas ni cruzarse, ya que el vector intensidad de campo eléctrico  $\vec{E}$ en un punto es único. En la figura [1](#fig-lineasdipolo) se muestra las líneas de campo de un dipolo eléctrico. 

* **Densidad de Flujo Local:** El número de líneas que atraviesan un área unitaria normal a las mismas es proporcional a la magnitud $\|\vec{E}\|$.

* **Condición de Equilibrio:** En conductores en equilibrio electrostático, las líneas de campo son siempre perpendiculares a la superficie ($\vec{E} \times \hat{n} = 0$).

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig01.png
:name: fig-lineasdipolo
:width: 40%
:align: center
:caption: Figura 1. Líneas de flujo eléctrico de un dipolo
:::


### 1.2. Flujo Eléctrico ($\phi_E$)

Evaluá la cantidad de campo eléctrico que atraviesa perpendicularmente una superficie, Figura [2](#fig-flujo). Se define como el producto escalar entre el campo eléctrico y el área elemental:

\begin{equation}
d\phi_E = \vec{E} \cdot \hat{n} dS
\end{equation}

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig05.png
:name: fig-flujo
:width: 40%
:align: center
:caption: Figura 2. Flujo eléctrico sobre una área elemental.
:::

El flujo eléctrico tiene unidades del SI de voltio-metro ($V m$), o, equivalentemente, newton-metro cuadrado por culombio($Nm^2 C^{−1}$). Por lo tanto, las unidades base del SI del flujo eléctrico son $kgm^3 s^{−3}A^{−1}$.

### 1.3. Ley de Gauss

El flujo eléctrico neto ($\phi_E$) a través de cualquier superficie cerrada, denominada superficie gaussiana, es igual a la carga neta encerrada ($q_{enc}$) dividida por la permitividad del medio.

\begin{equation}
\oint_S \vec{E} \cdot d\vec{S} = \frac{q_{enc}}{\varepsilon}
\end{equation}

> *⚠️ Nota Metodológica para el Estudiante* 
>
> Esta ley facilita el cálculo de la magnitud del campo en distribuciones con alta simetría esférica. El uso de la Ley de Gauss requiere primero reconocer que el campo eléctrico en distribuciones esfericas depende de la carga encerrada por la superficie gaussiana, por lo que es preciso identificar diferentes regiones, dentro y fuera de la distribución de la carga esférica. 

### 1.2. Relación entre $\varepsilon_o$ y $k$

Friedrich Gauss (1835), introdujo la constante $\varepsilon$ denominada permitividad eléctrica del medio, como una medida de la resistencia que ofrece el medio a la formación de un campo eléctrico en su seno. En el espacio libre o vacío, $\varepsilon = \varepsilon_0$ la intensidad del campo eléctrico es máxima. En otros medios como el agua, aceite, etc., la permitividad eléctrica es mayor, $\varepsilon_o \le \varepsilon$ lo que reduce la intensidad del campo eléctrico resultante.

Para deducir la relación entre ambas constantes, vamos a deducir la magnitud del campo eléctrico generado por una carga puntual en el vacío o aire usando la ley de Gauss y lo vamos a comparar con el resultado obtenido de la Ley de Coulomb. 

El campo eléctrico generado por una carga puntual tiene una alta simetria esférica, es decir el campo eléctrico tiene la misma magnitud en cualquier punto situado a una distancia $r$ de la carga puntual. Este hecho permite selecionar estratégicamente una superficie gaussiana esférica de radio $r$ que encierre a la carga puntual y el flujo neto estara dado por:

\begin{equation*}
\oint_{SG} \vec{E} \cdot d\vec{S} = \frac{q}{\varepsilon_o}
\end{equation*}

Dado que el campo eléctrico es normal a la superficie gaussiana y además su magnitud es constante sobre esta, la integral anterior se puede escribir: 

\begin{equation*}
E \oint_{SG} dS = \frac{q}{\varepsilon_o}
\end{equation*}

La integral cerrada del área elemental sobre toda la superficie gaussiana es precismanet el área de la superficie esférica gaussiana, $S = 4\pi r^2$

\begin{equation*}
E (4\pi r^2) = \frac{q}{\varepsilon_o}
\end{equation*}

\begin{equation*}
E = \frac{1}{4\pi \varepsilon_o} \frac{q}{r^2}
\end{equation*}

De acuerdo a la ley de Coulomb, el campo eléctrico de una carga puntual es $E = k q/r^2$, comparando con el resultado anterior obtenemos la relación entre ambas constantes.

\begin{equation}
k = \frac{1}{4\pi \varepsilon_o}
\end{equation}

De acuerdo a esta relación el valor de la permitividad eléctrica del aire o vacío es $\varepsilon_0 = 8.85 \times 10^{-12} F/m$.

---

## II. Problemas Resueltos 



### Problema N° 1: Flujo neto de una distribución de cargas
```{admonition} Flujo eléctrico de un disco y segmento cargados
:class: important
Un disco de área S y un hilo de longitud L estan cargados positivamente, con densidades de carga uniforme $\sigma$ y $\lambda$, tal como se muestra en la figura [3](#fig-leygauss), donde se ha dibujado sus lineas de campo. Deducir el flujo neto sobre las superficies gaussianas SG1 y SG2 que encierran a ambos cuerpos cargados. 

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig04.png
:name: fig-leygauss
:width: 50%
:align: center
:caption: Figura 3. Apicación de la Ley de Gauss.
:::
```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Ruta de la solución:** Aplicar la Ley de Gauss. 
   - **Predicción cualitativa:** El flujo neto sobre las dos superficies gaussianas SG1 y SG2, sin importar la forma de dichas superficies, es proporcional a la carga neta encerrada, es decir la suma de la carga del disco y del hilo.

2. **Resolución**
   - La carga neta encerrada es:

   \begin{equation*}
   q_{enc}= \lambda L + \sigma S
   \end{equation*}

   - Por lo tanto el flujo es:

   \begin{equation*}
   \oint_{SG1} \vec{E} \cdot d\vec{S} = \oint_{SG2} \vec{E} \cdot d\vec{S} = \frac{\lambda L + \sigma S}{\varepsilon_o}
   \end{equation*}

3. **Discusión Crítica:**
   - No importa la forma de la superficie gaussiana el flujo netos es siempre el mismo.

4. **Análisis de Sensibilidad:**
   - Si ambos cuerpos tuvieran igual cantidad de carga pero de signos opuestos el flujo resultante seria nulo.
   - Si ambos cuerpo tuvieran cargas negativas el flujo neto sería negativo.

5. **Extensión:**
   - La medición del campo electrostático es importante en sectores industriales donde las descargas electrostáticas pueden cuasar fallas en los equipos.
```
---

### Problema N° 2: Campo eléctrico de una esfera dieléctrica
```{admonition} Aplicación de la Ley de Gauss para simetrías esféricas
:class: important
Deducir la magnitud de la intesidad de campo eléctrico $\vec{E}$ en el interior y exterior de una nube esférica de radio $R$ con densidad de carga volumétrica $\rho$ constante.

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig05a.png
:name: fig-esferadielectrica
:width: 30%
:align: center
:caption: Figura 4. Esfera con cavidad cargada uniformemente.
:::

```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
- **Ruta de la solución:** Aplicar la ley de Gauss con superficies gaussianas concéntricas para $r < R$ y $r > R$.
- **Predicción cualitativa:** El campo en el interior se incrementa desde el centro y disminuye fuera de la nube esférica cargada.

2. **Resolución:**
- Se seleccionan dos superficies gaussianas esféricas concentricas, SG1 y SG2 de radio $r < R$ y $r > R$, respectivamente.

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig06.png
:name: fig-esferacargada
:width: 50%
:align: center
:caption: Figura 5. Superficies gaussianas concentricas alrededor de una esfera cargada.
:::

- **Fuera ($r > R$):**

   - La carga encerrada por la superficie gaussiana SG2, es toda la carga esférica:  $ q_{enc}= \rho  \frac{4}{3}\pi R^3$

   - Reemplazando en la Ley de Gauss y despejando la magnitud de la intensidad del campo eléctrico obtnemos:

   \begin{equation*}
   \oint_{SG2} EdS = \frac{q_{enc}}{\varepsilon_o}
   \end{equation*}

   \begin{equation*}
   E(4\pi r^2) = \frac{\rho \frac{4}{3}\pi R^3}{\varepsilon_0}
   \end{equation*}

   \begin{equation*}
   E = \frac{\rho R^3}{3\varepsilon_0 r^2}
   \end{equation*}


- **Dentro ($r < R$):** 

   - La carga encerrada por la superficie gaussiana SG1, es una porción de la carga esférica: $ q_{enc}= \rho  \frac{4}{3}\pi r^3$

   - Reemplazando en la Ley de Gauss y despejando la magnitud de la intensidad del campo eléctrico:

   \begin{equation*}
   \oint_{SG1} EdS = \frac{q_{enc}}{\varepsilon_o}
   \end{equation*}

   \begin{equation*}
   \oint_{SG1} EdS = \frac{q_{enc}}{\varepsilon_o}
   \end{equation*}

   \begin{equation*}
   E(4\pi r^2) = \frac{\rho \frac{4}{3}\pi r^3}{\varepsilon_0}
   \end{equation*}

   \begin{equation*}
   E = \frac{\rho r}{3\varepsilon_0}
   \end{equation*}


3. **Discusión Crítica:**
   - Se observa continuidad en la frontera $r = R$, donde el campo es máximo y ambos resultados dan $E_{max} = \frac{\rho R}{3\varepsilon_0}$.

4. **Análisis de Sensibilidad:**
   - Se verifica la predicción cualitativa, el campo en el interior de la esfera se incrementa linealmente desde el centro, hasta alcanzar su valor máximo en la superficie, luego disminuye cuadráticmante con la distancia al centro, tal como se observa en la gráfica de la figura [6](#fig-esferacargada).

   \begin{equation*}
   E =
   \begin{cases}
   \frac{\rho R}{3\varepsilon_0} \frac{r}{R} & r \le R \\
   \\
   \frac{\rho R}{3\varepsilon_0} \frac{R^2}{r^2} & R \le r 
   \end{cases}
   \end{equation*}

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig11.png
   :name: fig-esferacargada
   :width: 50%
   :align: center
   :caption: Figura 6. Superficies Gaussianas concentricas alrededor de una esfera cargada.
   :::

5. **Extensión:**
   - Base para modelar la distribución de carga en núcleos atómicos o gotas de rocío electrizadas.
```
---

### Problema N° 3: Campo eléctrico de una esfera conductora
```{admonition} Aplicación de la Ley de Gauss para simetrías esfericas
:class: important
Una esfera de densidad de carga uniforme $\rho$ posee una cavidad esférica, ta como se muestra en la figura. Deducir el campor eléctrico en el interior de la cavidad esférica.

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig05b.png
   :name: fig-esferaconductora
   :width: 30%
   :align: center
   :caption: Figura 7. Esfera con cavidad cargada uniformemente.
   :::

```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Ruta de la solución:** Aplicar la ley de Gauss con superficies gaussianas concéntricas para $r < R$ y $r > R$.
   - **Predicción cualitativa:** El campo es nulo en el interior de la esfera y disminuye fuera de la esfera.

2. **Resolución:**

   - Se seleccionan dos superficies gaussianas esféricas concentricas, SG1 y SG2 de radio $r < R$ y $r > R$, respectivamente.

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig06a.png
   :name: fig-esferacargada
   :width: 50%
   :align: center
   :caption: Figura 8. Superficies Gaussianas concentricas alrededor de una esfera conductora cargada.
   :::

- **Fuera ($r > R$):**

   - La carga encerrada por la superficie gaussiana SG2, es toda la carga esférica:  $ q_{enc}= \sigma (4\pi R^2)$

   - Reemplazando en la Ley de Gauss y despejando la magnitud de la intensidad del campo eléctrico:

   \begin{equation*}
   \oint_{SG2} EdS = \frac{q_{enc}}{\varepsilon_o}
   \end{equation*}

   \begin{equation*}
   E(4\pi r^2) = \frac{\sigma (4\pi R^2)}{\varepsilon_0}
   \end{equation*}

   \begin{equation*}
   E = \frac{\sigma}{\varepsilon_0} \frac{R^2}{r^2}
   \end{equation*}


- **Dentro ($r < R$):** 

   - La carga encerrada por la superficie gaussiana SG1 es una nula: $q_{enc}= 0$, por lo tanto el flujo eléctrico es nulo y en consecuencia el campo eléctrico también

   \begin{equation*}
   E = 0
   \end{equation*}


3. **Discusión Crítica:**
   - Se observa discontinuidad en la superficie de la esfera, $r = R$, donde el campo es máximo: $E = \frac{\sigma}{\varepsilon_0}$.

4. **Análisis de Sensibilidad:**
   - Se verifica la predicción cualitativa, el campo en el interior es  nula y dimsinuye fuera de esta.

   \begin{equation*}
   E =
   \begin{cases}
   0 & r \le R \\
   \\
   \frac{\sigma}{\varepsilon_0} \frac{R^2}{r^2} & R \le r 
   \end{cases}
   \end{equation*}

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig12.png
   :name: fig-esferacargada
   :width: 50%
   :align: center
   :caption: Figura 9. Superficies Gaussianas concentricas alrededor de una esfera cargada.
   :::

5. **Extensión:**
   - Base para crear armaduras eléctricas.
```
---

### Problema N° 4: Campo eléctrico en el interior de una esfera hueca

```{admonition} Aplicación del Principio de superposición
:class: important
Una esfera de densidad de carga uniforme $\rho$ posee una cavidad esférica, tal como se muestra en la figura. Deducir el campo eléctrico en el interior de la cavidad esférica.

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig07a.png
   :name: fig-esferahuecacargada
   :width: 30%
   :align: center
   :caption: Figura 10. Esfera con cavidad cargada uniformemente.
   :::
```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Ruta de la solución:** Completar la cavidad con carga positiva y negativa, luego sumar los campos de la esfera sólida ($\rho$) positiva y de la esfera negativa ($-\rho$) en el hueco.
   - **Predicción cualitativa:** De acuerdo a la Ley de Gauss, el campo sobre en el interior de la cavidad esferica es nulo o constante.

2. **Resolución:**
   - Completamos la cavidad con carga positiva para obtener una esfera solida cuyo campo en el interior en el punto P esta dado por:
   
   \begin{equation*}
   \vec{E_1} = \frac{\rho}{3\varepsilon_0} \vec{r_1}
   \end{equation*}

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig08b.png
   :name: fig-esferapositiva
   :width: 50%
   :align: center
   :caption: Figura 11. Campo en el interior de una esfera con carga positiva.
   :::

   - Ahora analizamos el campo generado en el punto P por la esfera negativa que llena la cavidad. Usando la Ley de Gauss se deduce:
   
   \begin{equation*}
   \vec{E_2} = \frac{\rho}{3\varepsilon_0} \vec{r_2}
   \end{equation*}

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig08a.png
   :name: fig-esferanegativa
   :width: 50%
   :align: center
   :caption: Figura 12. Campo en el interior de una esfera con carga negativa
   :::
   
   - Superponemos el capo de la esfera positiva maciza y el de la esfera negativa que llena la cavidad y el resultado es el campo en el interior de la cavidad esferica.
   
   \begin{equation*}
   \vec{E}_{total} = \vec{E}_{1} + \vec{E}_{2}
   \end{equation*}

   \begin{equation*}
   \vec{E}_{total} = \frac{\rho}{3\varepsilon_0} \vec{r_1} - \frac{\rho}{3\varepsilon_0} \vec{r_2}
   \end{equation*}

   - De la geometría se deduce que la diferencia de ambos vectores es $\vec{r_2} - \vec{r_1} = a \hat{i}$, por lo tanto:

   \begin{equation*}
   \vec{E}_{total} = \frac{\rho }{3\varepsilon_0} a \hat{i} 
   \end{equation*}

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig08.png
   :name: fig-esferahuecapositiva
   :width: 50%
   :align: center
   :caption: Figura 13. Campo en el interior de una esfera hueca.
   :::

3. **Discusión Crítica:**
   - El resultado es un campo constante dirigido hacia la derecha.

4. **Análisis de Sensibilidad:**
   - La magnitud del campo depende solo de la distancia entre centros $|\vec{b}|$.

5. **Extensión:**
   - Útil para analizar defectos de fabricación en aisladores poliméricos sólidos.
---
```

### Desafío N° 3: Cilindro Infinito Cargado
**Enunciado:** Hallar $\vec{E}$ para un cilindro largo de radio $R$ y densidad $\rho$.

1. **Marco Teórico e Hipótesis Inicial:**
   - **Fenómeno dominante:** Simetría cilíndrica axial.
   - **Ruta de la solución:** Superficie gaussiana cilíndrica de radio $r$ y longitud $L$.

2. **Resolución Técnica:**
   - **Fuera ($r > R$):** $E(2\pi r L) = \frac{\rho (\pi R^2 L)}{\varepsilon_0} \implies \vec{E} = \frac{\rho R^2}{2\varepsilon_0 r} \hat{r}$
   - **Dentro ($r < R$):** $E(2\pi r L) = \frac{\rho (\pi r^2 L)}{\varepsilon_0} \implies \vec{E} = \frac{\rho r}{2\varepsilon_0} \hat{r}$

3. **Discusión Crítica:**
   - A diferencia de la esfera, fuera del cilindro el campo decae como $1/r$.

4. **Análisis de Sensibilidad:**
   - Si $L$ no fuera infinito, aparecerían efectos de borde que invalidarían la Ley de Gauss simplificada.

5. **Transferencia y Extensión:**
   - Modelado de cables coaxiales de alta tensión.

---

### Desafío N° 4: Cavidad Esférica dentro de un Cilindro Infinito
**Enunciado:** Analizar el campo en una cavidad esférica dentro de un cilindro infinito cargado.

1. **Marco Teórico e Hipótesis Inicial:**
   - **Fenómeno dominante:** Superposición de geometrías cilindro-esfera.
   - **Ruta de la solución:** $\vec{E}_{cilindro} - \vec{E}_{esfera}$.

2. **Resolución Técnica:**
   En un punto dentro de la cavidad: $\vec{E} = \frac{\rho \vec{r}_{perp}}{2\varepsilon_0} - \frac{\rho \vec{r}_{esf}}{3\varepsilon_0}$

3. **Discusión Crítica:**
   - El campo no es uniforme en la cavidad debido a que las simetrías no se cancelan linealmente.

4. **Análisis de Sensibilidad:**
   - El campo es cero solo en el punto donde se intersectan el eje del cilindro y el centro de la esfera.

5. **Transferencia y Extensión:**
   - Análisis de burbujas de aire en cables de potencia.

---

### Desafío N° 5: Plano Infinito Cargado
**Enunciado:** Hallar $\vec{E}$ para un plano con densidad superficial $\sigma$.

1. **Marco Teórico e Hipótesis Inicial:**
   - **Fenómeno dominante:** Simetría plana.
   - **Ruta de la solución:** Cilindro gaussiano "pillbox" atravesando el plano.

2. **Resolución Técnica:**
   $2EA = \frac{\sigma A}{\varepsilon_0} \implies \vec{E} = \frac{\sigma}{2\varepsilon_0} \hat{n}$

3. **Discusión Crítica:**
   - El campo es independiente de la distancia $z$. Esto es una idealización de "punto cercano".

4. **Análisis de Sensibilidad:**
   - Si el plano tiene espesor, se trata como una distribución volumétrica (ver Ejemplo 6).

5. **Transferencia y Extensión:**
   - Principio de operación de capacitores y deflactores de haces.

---

### Desafío N° 6: Cavidad Esférica en una Placa Infinita
**Enunciado:** Analizar el campo en una cavidad esférica dentro de una placa gruesa de densidad $\rho$.

1. **Marco Teórico e Hipótesis Inicial:**
   - **Fenómeno dominante:** Superposición en medios extensos.
   - **Ruta de la solución:** Campo de placa sólida ($\vec{E} = \frac{\rho z}{\varepsilon_0} \hat{k}$) menos campo de esfera.

2. **Resolución Técnica:**
   $\vec{E}_{total} = \frac{\rho z}{\varepsilon_0} \hat{k} - \frac{\rho \vec{r}_{esf}}{3\varepsilon_0}$

3. **Discusión Crítica:**
   - La superposición muestra un gradiente de campo que depende de la profundidad $z$ en la placa.

4. **Análisis de Sensibilidad:**
   - La asimetría del campo dentro de la cavidad aumenta conforme esta se aleja del plano central.

5. **Transferencia y Extensión:**
   - Estudio de porosidad en blindajes electromagnéticos.

---
