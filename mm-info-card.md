# mm-info-card

**Descripción:**
Componente de tarjeta (Card) para mostrar indicadores, resúmenes destacados o gráficos embebidos.

## Identificador Técnico
- **Tag:** `<mm-info-card>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `type` | `string` | **Requerido.** Estilo visual de la tarjeta. | `graph-card`, `short-graph-card`, `highlight-card` | `"graph-card"` |
| `main-title` | `string` | Título principal de la tarjeta. | Texto libre | `""` |
| `counter` | `string` | Valor destacado (ej: "12", "€ 1.5M"). | Texto libre | `""` |

## Slots
| Slot | Descripción |
| :--- | :--- |
| `graph` | Introducir componentes de gráfica (ej: `mm-charts`). |

---

## Ejemplos para el LLM

### 1. Tarjeta con Indicador Destacado (Highlight)
```html
<mm-info-card type="highlight-card" main-title="Total Siniestros Abiertos" counter="24"></mm-info-card>
```

### 2. Tarjeta con Gráfica Embebida
```html
<mm-info-card type="graph-card" main-title="Distribución Mensual">
  <div slot="graph">
    <!-- Aquí iría el componente mm-charts -->
    <p>Área para gráfica...</p>
  </div>
</mm-info-card>
```

---
> [!TIP]
> **Instrucción:** Usa `mm-info-card` para dashboards o páginas de resumen de datos donde el usuario necesite visualizar KPIs rápidamente.
