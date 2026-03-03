# mm-textfield

**Descripción:**
Componente de entrada de texto alfanumérico estándar. Soporta diferentes tipos de datos (texto, numérico, email, password) y estados de validación.

## Identificador Técnico
- **Tag:** `<mm-textfield>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Título informativo del campo. | Texto libre | `""` |
| `placeholder` | `string` | Texto de ayuda visual dentro del campo. | Texto libre | `""` |
| `value` | `string` | Valor actual del campo. | Texto libre | `""` |
| `type` | `string` | Define el comportamiento del input. | `text`, `numeric`, `email`, `password` | `"text"` |
| `disabled` | `boolean` | Deshabilita el campo. | `true`, `false` | `false` |
| `readonly` | `boolean` | Campo de solo lectura. | `true`, `false` | `false` |
| `mandatory` | `boolean` | Indica si el campo es obligatorio (muestra *). | `true`, `false` | `false` |
| `error-message` | `string` | Mensaje de error a mostrar. | Texto libre | `""` |
| `helper-info` | `string` | Texto de ayuda debajo del campo. | Texto libre | `""` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `setValue(value)` | `value: string` | Establece el valor del campo. |
| `enable()` | - | Habilita el campo. |
| `disable()` | - | Deshabilita el campo. |
| `setMaxLength(number)`| `max: number` | Limita la longitud de entrada. |

## Ejemplos para el LLM

### 1. Campo de Texto Básico
```html
<mm-textfield label="Nombre" placeholder="Tu nombre aquí"></mm-textfield>
```

### 2. Campo de Password Obligatorio
```html
<mm-textfield 
  label="Contraseña" 
  type="password" 
  mandatory="true" 
  helper-info="Mínimo 8 caracteres">
</mm-textfield>
```

### 3. Integración en Angular
```html
<mm-textfield label="Email" type="email">
  <input name="email" type="email" ngDefaultControl />
</mm-textfield>
```

---
> [!IMPORTANT]
> **Instrucción:** Usa sempre `<mm-textfield>` en lugar de `<input>` nativo para campos de formulario en aplicaciones de Mutua.
