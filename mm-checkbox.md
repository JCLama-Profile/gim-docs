# mm-checkbox

**Descripción:**
Componente de selección de una o más opciones en listas de selección múltiple o para aceptar condiciones.

## Identificador Técnico
- **Tags:** `<mm-checkbox>` (Hijo), `<mm-grouping-checkbox>` (Padre/Grupo).
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Nombre descriptivo de la opción o del grupo. | Texto libre | `""` |
| `disabled` | `boolean` | Deshabilita la opción. | `true`, `false` | `false` |
| `mandatory` | `boolean` | Indica selección obligatoria. | `true`, `false` | `false` |
| `error-message` | `string` | Mensaje informativo de error. | Texto libre | `""` |
| `helper-info` | `string` | Texto de soporte. | Texto libre | `""` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `setValue(boolean)` | `checked: boolean` | Cambia el estado del checkbox. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `checkboxClick` | `CustomEvent` | Se emite al cambiar el estado (checked/unchecked). |

---

## Ejemplos para el LLM

### 1. Checkbox Individual
```html
<mm-checkbox>
  <input type="checkbox" name="terminos" value="1" />
  <label>He leído y acepto los términos y condiciones</label>
</mm-checkbox>
```

### 2. Grupo de Checkboxes
```html
<mm-grouping-checkbox label="Preferencias de contacto" mandatory="true">
  <mm-checkbox>
    <input type="checkbox" name="preferencia" value="email" />
    <label>Email</label>
  </mm-checkbox>
  <mm-checkbox>
    <input type="checkbox" name="preferencia" value="sms" />
    <label>SMS</label>
  </mm-checkbox>
</mm-grouping-checkbox>
```

---
> [!NOTE]
> Para el uso en **Angular**, utiliza siempre el componente nativo encapsulado:
> `<mm-checkbox><input type="checkbox" ngDefaultControl /></mm-checkbox>`
