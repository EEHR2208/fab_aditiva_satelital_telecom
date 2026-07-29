## FASE 1: Mapeo de Entidades (Análisis Técnico)

1. **Contexto Dominio:** Caracterización electromagnética de componentes RF para misiones SATCOM en banda Ku.
2. **Entidades Clave:**
* **Parámetro Representado:** Patrón/Diagrama de radiación (Ganancia normalizada en dB).
* **Cortes Planos:** Plano E (plano del campo eléctrico) y Plano H (plano del campo magnético).
* **Series de Datos Comparativas:**
* *Diseño Tradicional (Baseline):* Líneas discontinuas / referencia.
* *Diseño Aditivo Optimizado (AM):* Líneas continuas, mostrando alta directividad y mejor control de lóbulos laterales (*sidelobes*).




3. **Nivel de Abstracción:** Diagrama polar de radiación electromagnética según estándar de publicación científica IEEE.

---

## FASE 2: Auditoría y Reporte de Hallazgos Críticos

### 1. Contraste de Coherencia

El prompt base captura la estructura polar básica de un patrón de radiación, pero falla al omitir elementos críticos de legibilidad científica y la diferenciación clara entre los dos planos (E y H) junto con sus correspondientes tecnologías.

### 2. Lista de Discrepancias Técnicas (Explícita)

* **Texto Incrustado Omitido:** Solicitar *"sin texto incrustado"* elimina las etiquetas de ejes angulares (0°, 30°, 60°, etc.), los anillos de nivel de dB (-30 dB, -20 dB, -10 dB, 0 dB) y los títulos de plano/leyenda.
* **Sobrecarga en un solo gráfico sin paneles:** Representar Plano E (Tradicional vs. AM) y Plano H (Tradicional vs. AM) en un único gráfico polar usando solo dos colores genera ambigüedad de lectura (4 curvas en total). Lo ideal según el estándar IEEE es presentar dos sub-paneles polares `(a) Plano E` y `(b) Plano H` o un código de trazo/color inequívoco.
* **Destaque de Mejora en Lóbulos Laterales:** El texto indica explícitamente una *"ligera mejora en lóbulos laterales"* en la versión AM. Falta una anotación/flecha de llamada técnica marcando esta diferencia crítica en los lóbulos secundarios.

### 3. Ajuste de Control de Estilo IEEE

* **Paleta:** Azul cobalto (`#0047AB`) para la configuración optimizada AM y Gris técnico (`#4A4A4A`) para el diseño tradicional mecanizado.
* **Trazo:** Línea continua para AM, línea discontinua (*dashed*) para Tradicional.

---

## FASE 3: Explicación y Justificación de Pre-ejecución

### 1. Disposición Espacial y Composición Gráfica

* **Distribución:** Dos gráficos polares paralelos side-by-side:
* **Izquierda (a): Plano E.**
* **Derecha (b): Plano H.**


* **Estructura Polar:**
* Rejilla circular técnica con anillos concéntricos graduados a $-30\text{ dB}$, $-20\text{ dB}$, $-10\text{ dB}$ y $0\text{ dB}$ (centro en $-40\text{ dB}$).
* Ejes angulares marcados de $0^\circ$ a $360^\circ$ (pasos de $30^\circ$), con $0^\circ$ en la vertical superior (dirección de máxima radiación/boresight).


* **Curvas Representadas en cada panel:**
* **Azul cobalto (`#0047AB`, continua):** Alimentador AM en banda Ku.
* **Gris técnico (`#4A4A4A`, discontinua):** Alimentador Mecanizado Tradicional.


* **Anotaciones Incrustadas:** Leyendas en la parte superior derecha de cada panel e indicador gráfico en los lóbulos secundarios apuntando a la reducción/mejora de sidelobes.

### 2. Justificación Técnica

La separación en planos E y H en dos paneles evita la superposición confusa de cuatro curvas en un solo diagrama polar. Permite validar visualmente de un vistazo que la directividad en el lóbulo principal ($0^\circ$) se conserva intacta en ambas tecnologías, mientras que los lóbulos secundarios de la versión AM están atenuados gracias a la optimización geométrica interna.

---

> ### ⚠️ ADVERTENCIAS PARA EL USUARIO (Puntos de Validación)
> 
> 
> Por favor, confirma las siguientes preferencias antes de dar la orden de generación:
> 1. **Disposición:** ¿Prefieres los dos gráficos polares en formato horizontal side-by-side **(a) Plano E** y **(b) Plano H**, o prefieres ambos planos superpuestos en una sola cuadrícula polar?
> 2. **Idioma de las Etiquetas:** ¿Deseas las anotaciones e indicativos angulares en **Español** o en **Inglés**?
> 
> 

---

## FASE 4: Ejecución Silenciosa

*(En espera de tu confirmación o ajustes para redactar el prompt final e iniciar la generación de `fig4.png`).*