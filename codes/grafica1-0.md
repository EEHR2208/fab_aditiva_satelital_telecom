### PASO 1 — ANÁLISIS PREVIO

1. **Tipo de gráfico:** Gráfico de líneas dual-axis (dos ejes Y con diferente escala) sobre un eje X continuo.
2. **Datos observados:**
* **Eje X:** Número de unidades producidas (rango: $1$ a $200$, escala lineal).
* **Eje Y izquierdo (Costo Acumulado):** Escala monetaria (rango aprox. $\$0$ a $\$100\text{k}$ o unidades relativas).
* *Serie Tradicional (Costo):* Inicia en un valor alto por utillaje NRE ($\sim \$85\text{k}$) a $N=1$ y desciende con pendiente suave.
* *Serie AM (Costo):* Inicia significativamente más bajo ($\sim \$30\text{k}$) a $N=1$ y decrece suavemente, mostrando una ventaja constante del 35%–55% en el rango LEO ($10$–$200$).


* **Eje Y derecho (Lead-Time en Semanas):** Escala de tiempo (rango: $0$ a $16$ semanas).
* *Serie Tradicional (Lead-Time):* Valor constante en $14$ semanas.
* *Serie AM (Lead-Time):* Valor constante en $5$ semanas.




3. **Elementos estructurales:**
* **Ejes:** Doble eje Y (izquierdo: Costo Acumulado; derecho: Lead-Time). Eje X: Número de Unidades.
* **Leyenda:** Cuatro entradas organizadas según norma IEEE (Costo Tradicional, Costo AM, Lead-Time Tradicional, Lead-Time AM).
* **Zona Sombreada:** Región destacada entre $N=10$ y $N=200$ para identificar la zona óptima de "Constelaciones LEO".
* **Anotaciones/Líneas de referencia:** Guías horizontales discontinuas en $14$ y $5$ semanas para visibilidad del Lead-Time.


4. **Estilo:**
* **Paleta de colores:** Azul cobalto (`#0047AB`) para el método Tradicional, Gris técnico (`#4A4A4A`) para Fabricación Aditiva (AM).
* **Estilo de líneas y marcadores:** Líneas continuas con marcadores cuadrados (`s`) para Tradicional y circulares (`o`) para AM. Líneas discontinuas (`--`) para el Lead-Time.
* **Fondo:** Blanco puro, sin grid decorativo salvo líneas de guía principales, estilo publicación IEEE.


5. **Ambigüedades:**
* `# ASUNCIÓN:` Como los datos exactos del prompt LaTeX representan un modelo teórico parametrizado de costo/tiempo, se simulará la curva de costo mediante un modelo de aprendizaje/escala estándar donde la fabricación aditiva ahorra entre 35% y 55% en el rango $N \in [10, 200]$.



---

### PASO 2 — GENERACIÓN DEL CÓDIGO

```python
# === IMPORTS ===
import matplotlib.pyplot as plt
import numpy as np

# === PARÁMETROS DEL GRÁFICO ===
# Configuración de dimensiones y límites
fig_width, fig_height = 9, 6
dpi_quality = 300

# Rangos de ejes
x_min, x_max = 1, 200
y_cost_min, y_cost_max = 0, 100
y_time_min, y_time_max = 0, 16

# Puntos clave y parámetros del modelo
n_puntos = 50
leo_zone_min, leo_zone_max = 10, 200
lead_time_trad_val = 14
lead_time_am_val = 5

# Colores (Estándar IEEE / Paleta Solicitada)
color_trad = "#0047AB"       # Azul Cobalto
color_am = "#4A4A4A"         # Gris Técnico
color_leo_zone = "#0047AB"   # Sombra para zona LEO
alpha_zone = 0.08            # Transparencia de la zona destacada

# Estilos de línea y marcadores
marker_trad = 's'
marker_am = 'o'
marker_size = 5
mark_every = 4
line_width_main = 2.0
line_width_dash = 1.5

# Tipografía y formato IEEE
font_family = 'sans-serif'
font_size_labels = 11
font_size_title = 12
font_size_legend = 9.5

# === DATOS ===
# Eje X: Número de unidades
x_unidades = np.linspace(x_min, x_max, n_puntos)

# Modelo de Costos: Tradicional (alto costo inicial de utillaje/tooling NRE)
# ASUNCIÓN: Curva de costo unitario acumulado ajustada a amortización de utillaje
costo_trad = 85.0 * (x_unidades ** -0.15)

# Modelo de Costos: AM (sin utillaje inicial, reducción entre 35% y 55%)
# ASUNCIÓN: Reducción efectiva del ~45% respecto al tradicional en el rango medio
costo_am = 45.0 * (x_unidades ** -0.12)

# Lead-time constante (semanas)
lead_time_trad = np.full_like(x_unidades, lead_time_trad_val)
lead_time_am = np.full_like(x_unidades, lead_time_am_val)

# === FIGURA ===
# Configuración general del estilo
plt.rcParams['font.family'] = font_family
fig, ax_cost = plt.subplots(figsize=(fig_width, fig_height), dpi=dpi_quality)

# Crear el segundo eje Y para Lead-Time
ax_time = ax_cost.twinx()

# 1. Región sombreada: Ventaja AM en Constelaciones LEO
ax_cost.axvspan(leo_zone_min, leo_zone_max, color=color_leo_zone, alpha=alpha_zone, zorder=1,
                label='Zona LEO (10-200 un.)')

# 2. Curvas de Costo (Eje Y Izquierdo)
line1, = ax_cost.plot(x_unidades, costo_trad, color=color_trad, linestyle='-', linewidth=line_width_main,
                       marker=marker_trad, markevery=mark_every, markersize=marker_size,
                       label='Costo Tradicional ($kUSD)', zorder=3)

line2, = ax_cost.plot(x_unidades, costo_am, color=color_am, linestyle='-', linewidth=line_width_main,
                       marker=marker_am, markevery=mark_every, markersize=marker_size,
                       label='Costo Fabricación Aditiva ($kUSD)', zorder=3)

# 3. Curvas de Lead-Time (Eje Y Derecho)
line3, = ax_time.plot(x_unidades, lead_time_trad, color=color_trad, linestyle='--', linewidth=line_width_dash,
                       label=f'Lead-Time Tradicional ({lead_time_trad_val} sem.)', zorder=2)

line4, = ax_time.plot(x_unidades, lead_time_am, color=color_am, linestyle='--', linewidth=line_width_dash,
                       label=f'Lead-Time AM ({lead_time_am_val} sem.)', zorder=2)

# 4. Configuración de Ejes y Límites
ax_cost.set_xlim(x_min, x_max)
ax_cost.set_ylim(y_cost_min, y_cost_max)
ax_time.set_ylim(y_time_min, y_time_max)

# 5. Etiquetas de Ejes y Título
ax_cost.set_xlabel('Número de Unidades (Volumen de Producción)', fontsize=font_size_labels, fontweight='bold', labelpad=10)
ax_cost.set_ylabel('Costo Acumulado por Unidad ($kUSD)', fontsize=font_size_labels, fontweight='bold', color='black')
ax_time.set_ylabel('Lead-Time Total (Semanas)', fontsize=font_size_labels, fontweight='bold', color='black')
plt.title('Análisis Comparativo de Costo Acumulado y Lead-Time: Tradicional vs. AM',
          fontsize=font_size_title, fontweight='bold', pad=15)

# 6. Guías horizontales de Lead-Time
ax_time.axhline(y=lead_time_trad_val, color=color_trad, linestyle=':', alpha=0.4, linewidth=1.0)
ax_time.axhline(y=lead_time_am_val, color=color_am, linestyle=':', alpha=0.4, linewidth=1.0)

# 7. Anotaciones explicativas incrustadas
# ASUNCIÓN: Ubicación estratégica de texto explicativo para cumplimiento de estándar IEEE
ax_cost.annotate(f'Reducción Lead-Time\n(14 sem $\\rightarrow$ 5 sem)',
                 xy=(120, lead_time_am_val), xytext=(120, 8),
                 arrowprops=dict(arrowstyle="->", color=color_am, lw=1.2),
                 fontsize=9, color=color_am, fontweight='bold', ha='center')

# 8. Combinar leyendas de ambos ejes en una posición limpia
lineas = [line1, line2, line3, line4]
etiquetas = [l.get_label() for l in lineas]
ax_cost.legend(lineas, etiquetas, loc='upper right', frameon=True, facecolor='white',
               framealpha=0.9, fontsize=font_size_legend)

# 9. Estilo de cuadrícula y fondo
ax_cost.grid(True, linestyle=':', alpha=0.5, color='gray')
ax_cost.set_facecolor('white')

# === RENDER ===
plt.tight_layout()
plt.show()

```