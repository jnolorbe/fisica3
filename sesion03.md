# Sesión 3: Flujo Eléctrico
---

## I. Resumen Teórico 📚

### 1.1. Líneas de Campo Eléctrico
Las líneas de campo no son entes físicos, sino una herramienta topológica para mapear el campo vectorial $\vec{E}$ en el espacio. Sus propiedades fundamentales son:

* **Continuidad:** Se originan en cargas positivas (fuentes) y mueren en cargas negativas (sumideros). No pueden cerrarse sobre sí mismas ni cruzarse, ya que el vector $\vec{E}$ en un punto es único.
* **Densidad de Flujo Local:** El número de líneas que atraviesan un área unitaria normal a las mismas es proporcional a la magnitud $\|\vec{E}\|$.
* **Condición de Equilibrio:** En conductores en equilibrio electrostático, las líneas de campo son siempre perpendiculares a la superficie ($\vec{E} \times \hat{n} = 0$).

### 1.2. Flujo Eléctrico ($\Phi_E$)

Representa el "conteo" neto de líneas de campo que atraviesan una superficie. Se define escalarmente mediante el producto punto:
    $$\Phi_E = \int_S \vec{E} \cdot d\vec{A}$$

### 1.3. Ley de Gauss

Establece que el flujo neto a través de una superficie cerrada (superficie gaussiana) es proporcional a la carga neta encerrada:

$$\oint_S \vec{E} \cdot d\vec{A} = \frac{Q_{enc}}{\varepsilon}$$
    
Donde $\varepsilon$ es la permitividad del medio. En el vacío, $\varepsilon = \varepsilon_0$. La presencia de medios materiales (agua, aceite, etc.) aumenta la permitividad, reduciendo la intensidad del campo eléctrico.

### 1.2. Relación entre la permitividad y la constante eléctrica
A partir de una carga puntual y una superficie gaussiana esférica, se deduce que:
$$\oint \vec{E} \cdot d\vec{A} = E(4\pi r^2) = \frac{q}{\varepsilon_0} \implies E = \frac{1}{4\pi\varepsilon_0} \frac{q}{r^2}$$

Esto vincula la constante de Coulomb $k$ con la permitividad: $k = \frac{1}{4\pi\varepsilon_0}$.

---

## II. Problemas Resueltos 

### Problema N° 1: Esfera con Densidad de Carga Volumétrica Uniforme
**Enunciado:** Hallar $\vec{E}$ en todo el espacio para una esfera de radio $R$ con densidad $\rho$ constante.

1. **Planteamiento:**
   - **Ruta de la solución:** Aplicar superficies gaussianas concéntricas para $r < R$ y $r > R$.
   - **Predicción cualitativa:** El campo crecerá linealmente desde el centro y decaerá cuadráticamente fuera.

2. **Resolución Técnica:**
   - **Fuera ($r > R$):** $E(4\pi r^2) = \frac{\rho \frac{4}{3}\pi R^3}{\varepsilon_0} \implies \vec{E} = \frac{\rho R^3}{3\varepsilon_0 r^2} \hat{r}$
   - **Dentro ($r < R$):** $E(4\pi r^2) = \frac{\rho \frac{4}{3}\pi r^3}{\varepsilon_0} \implies \vec{E} = \frac{\rho r}{3\varepsilon_0} \hat{r}$

3. **Discusión Crítica:**
   - Se observa continuidad en la frontera $r = R$, donde ambos resultados dan $E = \frac{\rho R}{3\varepsilon_0}$.

4. **Análisis de Sensibilidad:**
   - Si el medio no fuera el vacío, el campo disminuiría proporcionalmente al factor de permitividad relativa del material.

5. **Transferencia y Extensión:**
   - Base para modelar la distribución de carga en núcleos atómicos o gotas de rocío electrizadas.

---

### Desafío N° 2: Campo en una Cavidad Esférica (Esfera)
**Enunciado:** Una esfera de radio $R$ y densidad $\rho$ tiene una cavidad de radio $a$ desplazada un vector $\vec{b}$.

1. **Marco Teórico e Hipótesis Inicial:**
   - **Fenómeno dominante:** Principio de Superposición.
   - **Ruta de la solución:** Sumar los campos de una esfera sólida ($\rho$) y una esfera negativa ($-\rho$) en el hueco.

2. **Resolución Técnica:**
   $\vec{E}_{total} = \frac{\rho \vec{r}}{3\varepsilon_0} + \frac{-\rho (\vec{r}-\vec{b})}{3\varepsilon_0} = \frac{\rho \vec{b}}{3\varepsilon_0}$

3. **Discusión Crítica:**
   - El resultado es un vector constante. El campo dentro de la cavidad es **uniforme**.

4. **Análisis de Sensibilidad:**
   - La magnitud del campo depende solo de la distancia entre centros $|\vec{b}|$.

5. **Transferencia y Extensión:**
   - Útil para analizar defectos de fabricación en aisladores poliméricos sólidos.

---

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
