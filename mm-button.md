# mm-button

**Descripción:**
Componente de botón estándar de Mutua Madrileña para acciones de usuario. Implementa la identidad visual corporativa y soporta diferentes jerarquías y comportamientos.

## Identificador Técnico
- **Tag:** `<mm-button>`
- **Framework:** Web Component (compatible con Angular, React, Vue y JS nativo).

## Propiedades (Attributes/Inputs)
| Atributo | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | **Requerido.** El texto que lee el usuario. | Texto libre | `""` |
| `type` | `string` | Jerarquía visual del botón. | `primary`, `secondary`, `support`, `ghost` | `"primary"` |
| `html-type` | `string` | Tipo de botón nativo. | `button`, `submit`, `reset` | `"button"` |
| `disabled` | `boolean` | Deshabilita la interacción. | `true`, `false` | `false` |
| `size` | `string` | Tamaño del botón. | `small`, `medium` | `"medium"` |
| `icon` | `string` | Nombre del icono (opcional). | Ver catálogo de iconos | `null` |

## Métodos
| Método | Descripción |
| :--- | :--- |
| `disable()` | Deshabilita el botón. |
| `enable()` | Rehabilita el botón. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `buttonClick` | `CustomEvent` | Se lanza al hacer click o pulsar Enter. |

---

## Ejemplos para el LLM

### 1. Botón Principal (Primary)
```html
<mm-button label="Aceptar y continuar"></mm-button>
```

### 2. Botón Secundario / Cancelar
```html
<mm-button label="Volver" type="secondary"></mm-button>
```

### 3. Botón de Envío en Formulario (Angular)
```html
<mm-button 
  label="Enviar Datos" 
  html-type="submit" 
  [disabled]="form.invalid"
  (buttonClick)="onSend()">
</mm-button>
```

---

> [!IMPORTANT]
> **Instrucción de Diseño:** No utilices la etiqueta `<button>` de HTML. Utiliza siempre `<mm-button>` con la propiedad `label` para asegurar la accesibilidad y el diseño correcto.
