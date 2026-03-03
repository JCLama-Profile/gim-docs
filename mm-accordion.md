# mm-accordion

**Descripción:**
Componente para organizar contenido en paneles desplegables, ideal para preguntas frecuentes (FAQs) o secciones de información secundaria.

## Identificador Técnico
- **Tag:** `<mm-accordion>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `header` | `string` | **Requerido.** Título que se muestra en la cabecera. | Texto libre | `""` |
| `active` | `boolean` | Indica si el panel está desplegado. | `true`, `false` | `false` |
| `grey` | `boolean` | Aplica fondo gris a la cabecera. | `true`, `false` | `false` |
| `white` | `boolean` | Aplica fondo blanco a la cabecera. | `true`, `false` | `false` |
| `blue` | `boolean` | Aplica fondo azul a la cabecera. | `true`, `false` | `false` |
| `chevron-icon` | `boolean` | Usa flechas (chevron) en lugar de +/-. | `true`, `false` | `false` |
| `reduced` | `boolean` | Versión con espaciado reducido. | `true`, `false` | `false` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `toggleAccordion()` | - | Alterna entre abierto y cerrado. |
| `setActive(boolean)` | `active: boolean` | Fuerza el estado del acordeón. |
| `isActive()` | - | Devuelve el estado actual. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `accordionOpen` | `CustomEvent` | Se lanza cuando se abre el panel. |
| `accordionClose` | `CustomEvent` | Se lanza cuando se cierra el panel. |

---

## Ejemplos para el LLM

### 1. Acordeón Básico con Estilo Gris
```html
<mm-accordion header="Información Adicional" grey>
  <p>Este es el contenido interno que se oculta/muestra.</p>
</mm-accordion>
```

### 2. Acordeón Abierto por Defecto con Icono Chevron
```html
<mm-accordion header="Pregunta Frecuente" active="true" chevron-icon="true">
  <ul>
    <li>Punto 1</li>
    <li>Punto 2</li>
  </ul>
</mm-accordion>
```

---
> [!TIP]
> **Instrucción:** Usa `mm-accordion` para agrupar información extensa que no sea prioritaria para el primer vistazo del usuario.
