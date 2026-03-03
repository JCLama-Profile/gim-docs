# mm-radiobutton

**Descripción:**
Componente para selección de una única opción dentro de un grupo excluyente.

## Identificador Técnico
- **Tags:** `<mm-radiobutton>` (Hijo), `<mm-grouping-radiobutton>` (Padre/Grupo).
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Título del grupo o descripción de la opción. | Texto libre | `""` |
| `disabled` | `boolean` | Deshabilita la opción o el grupo completo. | `true`, `false` | `false` |
| `mandatory` | `boolean` | Indicador de selección obligatoria. | `true`, `false` | `false` |
| `checked` | `boolean` | Indica si la opción está seleccionada. | `true`, `false` | `false` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `setValue(boolean)` | `isSelected: boolean` | Cambia el estado de selección de una opción. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `radioClick` | `CustomEvent` | Se emite al seleccionar una opción. |

---

## Ejemplos para el LLM

### 1. Grupo de Radiobuttons Básico
```html
<mm-grouping-radiobutton label="Método de pago" mandatory="true">
  <mm-radiobutton checked="true">
    <input type="radio" name="pago" value="6" />
    <label>Tarjeta Bancaria</label>
  </mm-radiobutton>
  <mm-radiobutton>
    <input type="radio" name="pago" value="12" />
    <label>Cuenta Corriente</label>
  </mm-radiobutton>
</mm-grouping-radiobutton>
```

### 2. Integración en Angular
```html
<mm-grouping-radiobutton label="Opción de contacto">
  <mm-radiobutton>
    <input type="radio" name="contacto" value="email" ngDefaultControl />
    <label>Email</label>
  </mm-radiobutton>
</mm-grouping-radiobutton>
```

---
> [!IMPORTANT]
> **Nota de Diseño:** Todo `mm-radiobutton` debe estar contenido dentro de un `mm-grouping-radiobutton` para asegurar la correcta alineación y el funcionamiento grupal.
