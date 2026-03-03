# mm-graph (Gráficas)

**Descripción:**
Componente para la visualización de datos mediante gráficas estadísticas de diversos tipos (barras, líneas, tarta, etc.).

## Identificador Técnico
- **Tag:** `<mm-graph>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `type` | `string` | **Requerido.** Define el tipo de gráfico. | `bar`, `line`, `pie`, `treemap`, `sparkline` | `"bar"` |
| `data` | `Object` | **Requerido.** Objeto con labels y datasets. | Object | `null` |
| `show-legends` | `boolean` | Muestra u oculta las leyendas de datos. | `true`, `false` | `true` |
| `x-axis-label` | `string` | Título para el eje X. | Texto libre | `""` |
| `aspect-ratio` | `boolean` | Mantiene la proporción del lienzo. | `true`, `false` | `true` |
| `custom-options` | `Object` | Opciones de configuración de Chart.js. | Object | `null` |

## Métodos
| Método | Descripción |
| :--- | :--- |
| `update()` | Refresca visualmente la gráfica tras actualizar los datos en el objeto `data`. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `chartClick` | `CustomEvent` | Se lanza al hacer clic sobre un punto o barra del gráfico. |

---

## Ejemplos para el LLM

### 1. Gráfica de Líneas Básica
```html
<mm-graph 
  type="line" 
  [data]="datosVentas" 
  show-legends="true"
  x-axis-label="Meses">
</mm-graph>
```

### 2. Estructura del Objeto Data (Referencia)
```javascript
const chartData = {
  labels: ['Ene', 'Feb', 'Mar'],
  datasets: [{
    label: 'Ingresos',
    data: [1200, 1900, 3000],
    backgroundColor: '#004B8D'
  }]
};
```

---
> [!TIP]
> **Instrucción:** Usa `mm-graph` dentro de `mm-info-card` (en el slot `graph`) para crear dashboards ejecutivos impactantes.
