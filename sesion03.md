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
Líneas de campo eléctrico de un dipolo.
:::

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig02.png
:name: fig-lineashilo
:width: 40%
:align: center
Líneas de campo eléctrico de un hilo cargado positivamente.
:::


### 1.2. Flujo Eléctrico ($\phi_E$)

Evalua la cantidad de campo eléctrico que atraviesa perpendicularmente una superficie, Figura [2](#fig-flujo). Se define como el producto escalar entre el campo eléctrico y el área elemental.

\begin{equation}
d\phi_E = \vec{E} \cdot \hat{n} dS
\end{equation}

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig03.png
:name: fig-flujo
:width: 40%
:align: center
Flujo eléctrico sobre una área elemental.
:::

El flujo eléctrico tiene unidades del SI de voltio-metro ($V m$), o, equivalentemente, newton-metro cuadrado por culombio($Nm^2 C^{−1}$). Por lo tanto, las unidades base del SI del flujo eléctrico son $kgm^3 s^{−3}A^{−1}$.

### 1.3. Ley de Gauss

El flujo eléctrico neto ($\phi_E$) a través de cualquier superficie cerrada, denominada superficie gaussiana, es igual a la carga neta encerrada ($q_{enc}$) dividida por la permitividad del medio.

\begin{equation}
\oint_S \vec{E} \cdot d\vec{S} = \frac{q_{enc}}{\varepsilon}
\end{equation}

> *⚠️ Nota Metodológica para el Estudiante* 
>
> Esta ley facilita el cálculo de la magnitud del campo en distribuciones con alta simetría esférica. En este caso las superficies gaussianas elegidas son superficies esféricas donde el campo eléctrico es normal a la superficie y la ecuacion de la Ley de Gauss adopta una forma más simple.

\begin{equation}
\oint_S E dS = \frac{q_{enc}}{\varepsilon}
\end{equation}

### 1.4. Relación entre $\varepsilon_o$ y $k$

En 1785 Charles-Augustin de Coulomb, usando una balanza de torsión, verificó que la fuerza de atracción o repulsión entre esferas cargadas varía inversamente con el cuadrado de la distancia. El experimento se realizó en aire a presión atmosférica. Coulomb no buscaba determinar una constante numérica — las unidades de carga aún no estaban definidas — pero sus resultados, en unidades actuales del SI, corresponden a $k \approx 8.7 \times 10^9 \, Nm^2/C^2$, el valor aceptado hoy es $k = 8.99 \times 10^9 \, Nm^2/C^2$.

En 1835 Friedrich Gauss formuló su ley del flujo eléctrico. La constante $\varepsilon$  que aparece en ella — posteriormente denominada **permitividad eléctrica** — fue interpretada por Maxwell y otros como una medida de cómo el medio material afecta la intensidad del campo eléctrico. En el espacio vacío, $\varepsilon = \varepsilon_0$ y el campo eléctrico es máximo. En otros medios materiales (aire, agua, aceite, etc.), la permitividad eléctrica es mayor, $\varepsilon_o \le \varepsilon$ lo que reduce el campo eléctrico resultante. 

Para deducir la relación entre ambas constantes, vamos a deducir la magnitud del campo eléctrico generado por una carga puntual usando la Ley de Gauss y lo vamos a comparar con el resultado obtenido de la Ley de Coulomb. 

El campo eléctrico generado por una carga puntual tiene simetría esférica: su magnitud es la misma en cualquier punto a distancia $r$. Seleccionamos una superficie gaussiana esférica de radio $r$ que encierre la carga. Como el campo es radial (normal a la esfera) y su magnitud depende solo de $r$:

\begin{equation*}
E \oint_{SG} dS = \frac{q}{\varepsilon_o}
\end{equation*}

La integral cerrada del área elemental es el área de la esfera, $S = 4\pi r^2$:

\begin{equation*}
E (4\pi r^2) = \frac{q}{\varepsilon_o}
\end{equation*}

Despejando:

\begin{equation*}
E = \frac{1}{4\pi \varepsilon_o} \frac{q}{r^2}
\end{equation*}

De la Ley de Coulomb, el campo de una carga puntual es $E = kq/r^2$. Comparando ambas expresiones:

\begin{equation}
k = \frac{1}{4\pi \varepsilon_o}
\end{equation}

De esta relación se obtiene la **permitividad eléctrica del vacío**:

$$\varepsilon_o = 8.85 \times 10^{-12} \, \mathrm{F/m}$$

El aire tiene $\varepsilon \approx 1.0006 \varepsilon_o$, prácticamente idéntico.

### 1.5. Permitividad relativa $\varepsilon_r = \varepsilon/\varepsilon_0$

| Medio | $\varepsilon_r$ (estática, $\sim 20 \mathrm{°C}$) | Notas |
|-------|-----------------------------------|-------|
| **Vacío** | 1 (exacto, por definición) | Referencia universal |
| **Aire (1 atm)** | 1.00059 | $\approx 1$ para la mayoría de cálculos |
| **Agua destilada** | $\sim 80$ | Fuerte dependencia con temperatura y frecuencia |
| **Parafina** | 2.1 – 2.3 | Aislante sólido, estabilidad química |
| **Mica** | 5 – 7 | Excelente aislante de alta frecuencia |
| **Vidrio (pyrex)** | 4 – 6 | Dependiente de composición |
| **Porcelana** | 5 – 7 | Aisladores de alta tensión |
| **Titanato de estroncio** |  $\sim 300$ | Condensadores de alta capacitancia compactos |
| **Poliestireno** | 2.5 – 2.7 | Plástico dieléctrico común |


> **Nota:** El término *constante dieléctrica* ($\kappa$) es sinónimo histórico de $\varepsilon_r$. Se prefiere hoy **permitividad relativa** porque no es estrictamente constante: varía con frecuencia del campo aplicado, temperatura y presión del medio. Para el agua a 20°C y 1 atm, por ejemplo, $\varepsilon_r \approx 80$ para campos estáticos, pero cae a $\sim 1.84$ para campos oscilantes a frecuencias ópticas $\sim 10^{15}  \mathrm{Hz}$.

---

## II. Problemas Resueltos 

### Problema N° 1 
**Flujo neto del campo de un disco y un hilo cargado**
```{admonition} Flujo neto a través de superficies gaussianas arbitrarias
:class: important
Un disco de área S y un hilo de longitud L estan cargados positivamente, con densidades de carga uniforme $\sigma$ y $\lambda$, tal como se muestra en la figura [3](#fig-leygauss), donde se ha dibujado sus lineas de campo. Deducir el flujo neto sobre las superficies gaussianas SG1 y SG2 que encierran a ambos cuerpos cargados. 

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig04.png
:name: fig-leygauss
:width: 50%
:align: center
Ley de Gauss para el campo eléctrico de dos cuerpos cargados.
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

   - Por lo tanto el flujo neto es:

   \begin{equation*}
   \oint_{SG1} \vec{E} \cdot d\vec{S} = \oint_{SG2} \vec{E} \cdot d\vec{S} = \frac{\lambda L + \sigma S}{\varepsilon_o}
   \end{equation*}

3. **Discusión Crítica:**
   - Para cualquier superficie gaussiana que encierre ambos cuerpos completamente, el flujo neto es idéntico e independiente de la forma de la superficie gaussiana.

4. **Análisis de Sensibilidad:**
   - Si ambos cuerpos tuvieran igual cantidad de carga pero de signos opuestos el flujo resultante seria nulo.
   - Si ambos cuerpos tuvieran cargas negativas el flujo neto sería negativo.

5. **Extensión:**
   - - Este ejercicio demuestra conceptualmente que el flujo neto es idéntico sin importar la forma de la superficie gaussiana, siempre que encierre la misma carga neta. Esta libertad permite elegir **superficies gaussianas convenientes** — esferas, cilindros, cajas — que coincidan con la simetría de la distribución de carga, lo que permite calcular la magnitud del campo eléctrico a partir del flujo neto.

```
---

### Problema N° 2
**Campo eléctrico de una esfera cargada uniformemente**
```{admonition} AAplicación de la Ley de Gauss a simetría esférica
:class: important
Deducir la magnitud de la intensidad de campo eléctrico $\vec{E}$ en el interior y exterior de una nube esférica de radio $R$ con densidad de carga volumétrica $\rho$ constante.

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig05.png
:name: fig-esferadielectrica
:width: 30%
:align: center
Esfera con cavidad cargada uniformemente.
:::

```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
- **Ruta de la solución:** Aplicar la Ley de Gauss con superficies Gaussianas concéntricas para $r < R$ y $r > R$.
- **Predicción cualitativa:** El campo en el interior crece linealmente desde el centro y decae cuadráticamente fuera de la esfera cargada.

2. **Resolución:**
- Se seleccionan dos superficies Gaussianas esféricas concéntricas, SG1 y SG2, de radios $r < R$ y $r > R$ respectivamente.

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig06.png
:name: fig-esferacargadavolumen
:width: 50%
:align: center
Superficies gaussianas concentricas alrededor de una esfera cargada.
:::

- **Fuera ($r > R$):**

   - La carga encerrada por la superficie gaussiana SG2, es toda la carga esférica: $ q_{enc}= \rho  \frac{4}{3}\pi R^3$

   - Aplicando la Ley de Gauss:

   \begin{equation*}
   \oint_{SG2} EdS = \frac{q_{enc}}{\varepsilon_o}
   \end{equation*}

   \begin{equation*}
   E(4\pi r^2) = \frac{\rho \frac{4}{3}\pi R^3}{\varepsilon_0}
   \end{equation*}

   \begin{equation*}
   E = \frac{\rho}{3\varepsilon_0} \frac{R^3}{r^2}
   \end{equation*}

- **Dentro ($r < R$):** 

   - La carga encerrada por la superficie gaussiana SG1, es una fracción porporcional al volumen: $ q_{enc}= \rho  \frac{4}{3}\pi r^3$

   - Aplicando la Ley de Gauss:

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
   E = \frac{\rho}{3\varepsilon_0}  r
   \end{equation*}

3. **Discusión Crítica:**
   - En la frontera $r = R$, ambas expresiones coinciden $E(r=R) = \frac{\rho R}{3\varepsilon_0}$. Este valor representa el campo máximo, ya que el campo crece linealmente en el interior y decrece cuadráticamente en el exterior.

4. **Análisis de Sensibilidad:**

   - El campo crece linealmente en el interior ($E \propto r$) y decae cuadráticamente en el exterior ($E \propto 1/r^2$), confirmando la predicción cualitativa. La forma funcional completa:
   
   \begin{equation*}
   E(r) = \frac{\rho R}{3\varepsilon_0} \times
   \begin{cases}
   \dfrac{r}{R} & r \leq R \\[12pt]
   \dfrac{R^2}{r^2} & r \geq R
   \end{cases}
   \end{equation*}
   
   donde el prefactor común $\frac{\rho R}{3\varepsilon_0}$ es el campo máximo en la superficie

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig07.png
   :name: fig-esferacargada
   :width: 80%
   :align: center
   Variación del campo eléctrico en el interior y exterio de una esfera cargada uniformemente.
   :::

5. **Extensión:**
   - Modelo simplificado de nubes de tormentas cargadas.
```
---

### Problema N° 3
**Campo eléctrico de una esfera conductora cargada**
```{admonition} Conductor en equilibrio electrostático
:class: important
Una esfera conductora de radio $R$ se carga con carga total $Q$ uniformemente distribuida en su superficie. Deducir el campo eléctrico en el interior ($r < R$) y exterior ($r > R$) de la esfera.

:::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig08.png
:name: fig-esferaconductora01
:width: 30%
:align: center
Esfera conductora cargada.
:::
```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Ruta de la solución:** Aplicar la Ley de Gauss con superficies gaussianas esféricas concéntricas para $r < R$ y $r > R$.
   - **Predicción cualitativa:** En equilibrio electrostático, la carga reside en la superficie del conductor, por lo que el campo en el interior es nulo. Fuera de la esfera, el campo decae cuadráticamente como el de una carga puntual.

2. **Resolución:**

   - Se seleccionan dos superficies Gaussianas esféricas concéntricas, SG1 ($r < R$) y SG2 ($r > R$).

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig09.png
   :name: fig-esferacacondcutora02
   :width: 50%
   :align: center
   Superficies Gaussianas concentricas alrededor de una esfera conductora cargada.
   :::

   - **Dentro ($r < R$):**

     La carga encerrada por SG1 es nula: $q_{enc} = 0$, ya que la carga reside exclusivamente en la superficie del conductor.

     Aplicando la Ley de Gauss para la superficie gaussiana esférica SG1:

     \begin{equation*}
     \oint_{SG1} EdS = \frac{q_{enc}}{\varepsilon_o} = 0 
     \end{equation*}
     
     Por tanto:

     \begin{equation*}
     E = 0
     \end{equation*}

   - **Fuera ($r > R$):**

     La carga encerrada por SG2 es toda la carga de la esfera: $q_{enc} = Q = \sigma (4\pi R^2)$, donde $\sigma$ es la densidad superficial de carga.

     Aplicando la Ley de Gauss para la superficie gaussiana esférica SG2:
     
     \begin{equation*}
     \oint_{SG2} EdS = \frac{q_{enc}}{\varepsilon_o}
     \end{equation*}

     \begin{equation*}
     E(4\pi r^2) = \frac{\sigma (4\pi R^2)}{\varepsilon_0}
     \end{equation*}

     Despejando:
     
     \begin{equation*}
     E = \frac{\sigma}{\varepsilon_0} \frac{R^2}{r^2}
     \end{equation*}

3. **Discusión Crítica:**
   - **Equilibrio electrostático:** En un conductor la carga se distribuye en la superficie del conductor hasta que se alcance el equilibrio electrostático que ocrre cuando el campoe léctrico en el interior se anula
   - **Discontinuidad en la superficie:** En $r = R$, el campo salta de $0$ a $\sigma/\varepsilon_0$. Esta discontinuidad es característica de una distribución superficial de carga.
   - **Analogía exterior:** Para $r > R$, el campo es idéntico al de una carga puntual $Q$ concentrada en el centro.

4. **Análisis de Sensibilidad:**
   - **Verificación de predicción:** El campo es nulo en el interior y decae como $1/r^2$ en el exterior, confirmando la predicción cualitativa.

   La forma funcional completa:
   
   \begin{equation*}
   E(r) = 
   \begin{cases}
   0 & r \leq R \\[8pt]
   \dfrac{\sigma}{\varepsilon_0} \dfrac{R^2}{r^2} = \dfrac{1}{4\pi\varepsilon_0} \dfrac{Q}{r^2} & r \geq R
   \end{cases}
   \end{equation*}
   
   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig10.png
   :name: fig-campoesferaconductora
   :width: 80%
   :align: center
   Magnitud del campo eléctrico de una esfera conductora cargada en función de la distancia al centro $r/R$.
   :::

   > **Nota:** En $r = R$ la función presenta una discontinuidad de salto. El valor $E = 0$ corresponde al límite por el interior; $E = \sigma/\varepsilon_0$ al límite por el exterior. La notación $r \leq R$ y $r \geq R$ es convencional pero implica valores distintos en el punto de contacto.

5. **Extensión:**
   - **Blindaje electrostático (jaula de Faraday):** El campo nulo en el interior de un conductor hueco cargado externamente protege el contenido de campos eléctricos. Este principio aplica desde cables coaxiales hasta habitaciones blindadas para experimentos sensibles.
   - **Presión electrostática:** La carga superficial experimenta una fuerza repulsiva debida al campo de las cargas vecinas, generando una presión $P = \sigma^2/(2\varepsilon_0)$ que tiende a expandir la esfera.
```
---

### Problema N° 4
**Campo eléctrico en el interior de una esfera hueca**

```{admonition} Aplicación del Principio de superposición
:class: important
Una esfera de densidad de carga uniforme $\rho$ positiva posee una cavidad esférica de radio $2a$, tal como se muestra en la figura. Deducir el campo eléctrico en el interior de la cavidad esférica.

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig11.png
   :name: fig-esferahuecacargada
   :width: 30%
   :align: center
   Esfera cargada positivamente con cavidad en su interior.
   :::
```

```{admonition} Solución
:class: dropdown hint

1. **Planteamiento:**
   - **Ruta de la solución:** Completar la cavidad con carga positiva y negativa, luego sumar los campos de la esfera sólida ($\rho$) positiva y de la esfera negativa ($-\rho$) en el hueco.
   - **Predicción cualitativa:** De acuerdo a la Ley de Gauss, el campo en el interior de la cavidad esferica es nulo o constante.

2. **Resolución:**
   
   - **Paso 1:** Completamos la cavidad con carga de densidad $+\rho$ para formar una esfera sólida completa. El campo en un punto P interior es:
 
   \begin{equation*}
   \vec{E}_1 = \frac{\rho}{3\varepsilon_0} \vec{r}_1
   \end{equation*}

   donde $\vec{r}_1$ es el vector desde el centro de la esfera completa (O) al punto P

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig12.png
   :name: fig-esferapositiva
   :width: 50%
   :align: center
   Campo en el punto P debido a la esfera completa de densidad $+\rho$.
   :::

   - **Paso 2:** Consideramos ahora una esfera de densidad $-\rho$ que ocupa exactamente la región de la cavidad. El campo que esta esfera "negativa" produce en su interior es:
      
   \begin{equation*}
   \vec{E}_2 = \frac{-\rho}{3\varepsilon_0} \vec{r}_2
   \end{equation*}

   donde $\vec{r}_2$ es el vector desde el centro de la cavidad (O') al punto P.

   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig13.png
   :name: fig-esferanegativa
   :width: 50%
   :align: center
   Campo en el punto P debido a la esfera de densidad $-\rho$.
   :::
   
   - **Paso 3 (Superposición):** El campo real en la cavidad es la suma:   

   \begin{equation*}
   \vec{E}_{total} = \vec{E}_1 + \vec{E}_2
   \end{equation*}

   \begin{equation*}
   \vec{E}_{total} = \frac{\rho}{3\varepsilon_0} \vec{r}_1 - \frac{\rho}{3\varepsilon_0} \vec{r}_2
   \end{equation*}

   - **Paso 4 (Geometría):** De la figura, la diferencia de vectores de posición es:

   \begin{equation*}
   \vec{r}_1 - \vec{r}_2 = a \hat{i}
   \end{equation*}

   donde $a \hat{i}$ es el vector desde el centro de la esfera completa (O) al centro de la cavidad (O'), constante para cualquier punto P en la cavidad.
   
   :::{figure} https://raw.githubusercontent.com/jnolorbe/fisica3/main/figuras/s03_fig14.png
   :name: fig-esferahuecapositiva
   :width: 50%
   :align: center
   Campo en el interior de una esfera hueca.
   :::

   - **Resultado final:**
   
   \begin{equation*}
   \vec{E} = \frac{\rho}{3\varepsilon_0} \, a \hat{i}
   \end{equation*}

   El resultado es un campo eléctrico **uniforme** (misma magnitud y dirección en toda la cavidad).

3. **Discusión Crítica:**
   - **Campo uniforme:** El resultado $\vec{E} = \frac{\rho}{3\varepsilon_0}\, a \hat{i}$ es independiente de la posición dentro de la cavidad. Cualquier punto en el hueco "siente" el mismo campo, una propiedad notable de la simetría esférica rota.
   - **Dirección del campo:** El campo apunta desde el centro de la esfera positiva hacia el centro de la cavidad (suponiendo $\rho > 0$). Si los centros coinciden ($\vec{d} = 0$), el campo se anula, recuperando la simetría esférica completa.
   - **Validez del método:** El principio de superposición permite crear cargas ficticias (la $-\rho$  en la cavidad) que no existen físicamente, y cancelan exactamente la carga real $+\rho$ que habría estado allí.

4. **Análisis de Sensibilidad:**
   - **Independencia del tamaño de la cavidad:** La magnitud del campo depende solo del desplazamiento $\vec{OO'}$. Una cavidad pequeña desplazada produce el mismo campo que una cavidad grande con el mismo desplazamiento de centros.

5. **Extensión:**
   - **Defectos en dieléctricos:** Cavidades o inclusiones de aire en materiales aislantes (poros, burbujas) crean campos internos no nulos bajo polarización, iniciando descargas parciales que degradan el aislante.
---
```

## III. Actividades para el Portafolio Digital 📓

Resuelve al menos dos de los siguientes desafíos en tu **Diario de Aprendizaje** utilizando la **Estrategia de los 5 Bloques**. 


### Desafío N° 1
**Campo eléctrico en la frontera de un cilindro infinito cargado**

Comparar la magnitud del campo eléctrico $\vec{E}$ justo en la superficie de un cilindro muy largo de radio $R$, analizando los límites por el interior ($r \to R^-$) y por el exterior ($r \to R^+$), para dos configuraciones de carga:

- **Caso A:** La carga total $Q$ se distribuye uniformemente en el **volumen** del cilindro, con densidad $\rho$ constante.

- **Caso B:** La misma carga total $Q$ se distribuye uniformemente en la **superficie** del cilindro, con densidad $\sigma$ constante.

- Deducir en qué caso el campo es mayor en la frontera y si existe discontinuidad al atravesar la superficie.
---

### Desafío N° 2
**Campo eléctrico en una cavidad esférica dentro de un cilindro cargado muy largo**

Analizar el campo eléctrico $\vec{E}$ en el interior de una cavidad esférica de radio $a$, cuyo centro está desplazado una distancia $d$ del eje del cilindro. El cilindro es muy largo (asumir infinito), de radio $R$ ($a + d < R$), y posee densidad de carga volumétrica uniforme $+\rho$.

Deducir:
- La magnitud y dirección del campo en cualquier punto de la cavidad.
- Si el campo es uniforme o depende de la posición dentro de la cavidad.
- La condición para que el campo se anule en la cavidad.
---

### Desafío N° 3
**Campo eléctrico en una cavidad esférica dentro de una placa infinita cargada**

Una placa infinita de espesor $e$ posee densidad de carga volumétrica uniforme $+\rho$. En su interior se tiene una cavidad esférica de radio $a$, cuyo centro está desplazado una distancia $d$ de la superficie media de la placa ($a < d < e - a$).

Analizar el campo eléctrico $\vec{E}$ en el interior de la cavidad. Deducir:
- Si el campo es uniforme o depende de la posición dentro de la cavidad.
- La magnitud y dirección del campo en el centro de la cavidad.
- La condición para que el campo se anule en algún punto de la cavidad.
---

### Desafío N° 4
**Campo eléctrico en una cavidad esférica excéntrica**

Una esfera sólida de radio $R$ posee densidad de carga volumétrica uniforme $+\rho$. Contiene una cavidad esférica de radio $a$ cuyo centro está desplazado una distancia $d$ del centro de la esfera ($d + a < R$). La cavidad contiene además una carga puntual $+q$ en su centro.

Determinar:
- El campo eléctrico en cualquier punto de la cavidad.
- La fuerza neta sobre la carga puntual $q$.
- Si la fuerza depende de la posición de $q$ dentro de la cavidad (suponiendo que se desplaza ligeramente del centro).

### Desafío N° 5
**Campo eléctrico de un cable coaxial con densidad volumétrica no uniforme**

Un cable coaxial largo consiste en:
- Un cilindro interior sólido de radio $R_1$, con densidad de carga volumétrica $\rho(r) = \rho_0 \left(1 - \frac{r}{R_1}\right)$ (decreciente hacia la periferia).
- Un cilindro exterior hueco de radio interno $R_2$ y externo $R_3$, con densidad superficial $\sigma$ uniforme en su cara interna.

Deducir:
- El campo eléctrico en las tres regiones: $r < R_1$, $R_1 < r < R_2$, y $r > R_3$.
- La condición sobre $\sigma$ para que el campo sea nulo fuera del cable ($r > R_3$).
- La diferencia clave al aplicar Gauss con densidad no uniforme versus uniforme.
---
