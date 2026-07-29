## FASE 1: Mapeo de Entidades (Análisis Técnico)

1. **Contexto Dominio:** Componentes satelitales optimizados mediante *Design for Additive Manufacturing* (DfAM) para plataformas LEO/SATCOM.
2. **Entidades Clave:**
* **Elemento Izquierdo:** Bracket estructural primario con matriz de estructura *lattice* interna y *thickening* selectivo para disipación/resistencia modal bajo cargas de lanzamiento.
* **Elemento Derecho:** Antena RF (bocina/horn o alimentador) con integración multifuncional (guía de ondas integrada y canales de refrigeración disipativa interna).
* **Tecnología de Fabricación:** PBF-LB/M (SLM/DMLS) en aleaciones metálicas (Al/Ti).


3. **Nivel de Abstracción:** Diagrama esquemático técnico/ingenieril de componentes (vistas en corte/sección transversal e isometría técnica) alineado al estándar de publicación IEEE.

---

## FASE 2: Auditoría y Reporte de Hallazgos Críticos

### 1. Contraste de Coherencia

El prompt base describe una composición *side-by-side* de dos componentes clave descritos en la Sección 2.3 y la *Figura 2*. Sin embargo, adolece de omisiones de anotación gráfica fundamentales para cumplir con un estándar científico navegable.

### 2. Lista de Discrepancias Técnicas (Explícita)

* **Ausencia de Texto Explicativo Incrustado:** El prompt solicita *"sin texto incrustado"*, lo cual invalida la capacidad de la figura para señalar explícitamente las características descritas en el texto: *"Geometría lattice interna"*, *"Canales térmicos/RF integrados"* y *"Sección en corte A-A'"*.
* **Falta de Indicadores de Sección/Corte:** No se especifican líneas de corte transversal ni planos de detalle para evidenciar que las geometrías internas son imposibles de lograr por mecanizado convencional (característica central señalada en el pie de figura).
* **Ausencia de Identificación de Componentes:** No hay etiquetas o títulos de sub-figuras (a) y (b) para la distinción clara entre la parte estructural y la parte electromagnética (RF).

### 3. Ajuste de Control de Estilo IEEE

* **Paleta:** Azul cobalto (`#0047AB`) para destacar geometrías aditivas/canales internos y Gris Técnico (`#4A4A4A`) para bordes, paredes estructurales y achurado técnico de corte.
* **Líneas y Tipografía:** Líneas vectoriales continuas de grosor uniforme, achurado (hatching) estándar para cortes mecánicos y tipografía Sans-Serif limpia (Helvetica/Arial).

---

## FASE 3: Explicación y Justificación de Pre-ejecución

### 1. Disposición Espacial y Composición Gráfica

* **Distribución en dos paneles:**
* **Panel Izquierdo (a):** *Bracket Estructural DfAM*. Vista isométrica con corte parcial (*cutaway*) mostrando la piel exterior sólida y el relleno de matriz *lattice* (geometría celular triangular/hexagonal) en el núcleo.
* **Panel Derecho (b):** *Antena / Alimentador RF Integrado*. Vista en sección transversal longitudinal que expone la trayectoria cónica del alimentador, la guía de ondas interna y los canales concéntricos de disipación térmica.


* **Anotaciones y Texto Incrustado:**
* Etiquetas con líneas de llamada (*leaders*) hacia las geometrías internas: *"Estructura Lattice Interna (PBF-LB/M)"*, *"Canal RF / Guía de Ondas Monolítica"*, *"Canales de Refrigeración Integrados"*.
* Títulos de sub-paneles: **(a) Bracket Estructural** y **(b) Antena RF SATCOM**.



### 2. Justificación Técnica

Esta representación dividida ilustra de forma directa la hipótesis del artículo: la fabricación aditiva en hardware espacial abarca tanto la **optimización de masa estructural** (panel a) como la **consolidación multifuncional RF-térmica** (panel b), evidenciando las cavidades internas inaccesibles para el mecanizado sustractivo tradicional.

---

> ### ⚠️ ADVERTENCIAS PARA EL USUARIO (Puntos de Validación)
> 
> 
> Por favor, valida los siguientes puntos antes de proceder a la generación final:
> 1. **Idioma de las Etiquetas:** ¿Deseas que los textos incrustados dentro del esquema estén en **Español** o en **Inglés** (estándar preferido en revistas IEEE)?
> 2. **Nivel de Detalle del Core Lattice:** ¿Prefieres una celda unitaria regular (tipo panal/triangular) o una estructura celular estocástica/orgánica (tipo optimización topológica)?
> 
> 

---

## FASE 4: Ejecución Silenciosa

*(En espera de tu confirmación o instrucciones de ajuste sobre las advertencias antes de proceder con la generación de `fig2.png`).*