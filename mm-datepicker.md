# mm-datepicker

**Descripción:**
Componente selector de fecha y hora que permite la selección manual o mediante un widget de calendario desplegable.

## Identificador Técnico
- **Tag:** `<mm-datepicker>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Título del campo. | Texto libre | `""` |
| `placeholder` | `string` | Ayuda visual ("dd/mm/aaaa"). | Texto libre | `""` |
| `type` | `string` | Tipo de selector. | `date`, `time`, `datetime` | `"date"` |
| `date-range` | `boolean` | Habilita la selección de un rango de fechas. | `true`, `false` | `false` |
| `min-date` | `string` | Fecha mínima permitida. | `"dd/mm/aaaa"` | `null` |
| `max-date` | `string` | Fecha máxima permitida. | `"dd/mm/aaaa"` | `null` |
| `today-selector`| `boolean` | Añade botón para seleccionar el día de hoy. | `true`, `false` | `false` |
| `disabled` | `boolean` | Deshabilita el componente. | `true`, `false` | `false` |
| `mandatory` | `boolean` | Indica campo obligatorio. | `true`, `false` | `false` |
| `value` | `string` | Valor de la fecha. | `"dd/mm/aaaa"` | `""` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `setValue(value)` | `string\|Date` | Establece la fecha programáticamente. |
| `getDate()` | - | Devuelve la fecha seleccionada. |
| `openDatepicker()`| - | Abre el widget de calendario. |
| `clearDate()` | - | Resetea el valor del campo. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `change` | `CustomEvent` | Emitido al cambiar el valor (excepto tipo time). |
| `timeChange` | `CustomEvent` | Emitido al cambiar la hora (solo tipo time). |

---

## Ejemplos para el LLM

### 1. Selector de Fecha con Rango y Límite
```html
<mm-datepicker 
  label="Rango de vacaciones" 
  date-range="true" 
  min-date="01/01/2024" 
  max-date="31/12/2024">
</mm-datepicker>
```

### 2. Integración en Angular
```html
<mm-datepicker 
  label="Fecha de nacimiento" 
  formControlName="fechaNac" 
  ngDefaultControl>
</mm-datepicker>
```

---
> [!IMPORTANT]
> **Nota de Angular:** Se requiere el atributo `ngDefaultControl` para que el componente se sincronice correctamente con los Reactive Forms si no se usa un Wrapper específico.
