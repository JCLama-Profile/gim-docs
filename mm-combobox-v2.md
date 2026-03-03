# mm-combobox-v2

**Descripción:**
Componente selector desplegable (Select) avanzado que permite la búsqueda interna y el filtrado por texto.

## Identificador Técnico
- **Tag:** `<mm-combobox-v2>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Descripción superior del campo. | Texto libre | `"Opciones"` |
| `placeholder` | `string` | Texto informativo dentro del campo ("Selecciona..."). | Texto libre | `"Selecciona una opción"` |
| `options` | `Array` | Listado de opciones (soporta `string[]` o `{value, label}[]`). | `Array` | `[]` |
| `search` | `boolean` | Habilita campo de búsqueda interno. | `true`, `false` | `false` |
| `disabled` | `boolean` | Desactiva la interacción con el selector. | `true`, `false` | `false` |
| `up` | `boolean` | Fuerza el despliegue hacia arriba. | `true`, `false` | `false` |
| `value` | `string` | Valor seleccionado inicialmente. | Texto libre | `""` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `setValue(value)` | `value: string` | Establece el valor seleccionado. |
| `setOptions(options)` | `options: Array` | Actualiza la lista de opciones dinámicamente. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `change` | `CustomEvent` | Emitido cuando el usuario selecciona una nueva opción. |
| `click` | `CustomEvent` | Emitido al interactuar con el componente. |

---

## Ejemplos para el LLM

### 1. Select con Búsqueda Activa (Nativo / HTML)
```html
<mm-combobox-v2 
  id="provincia-select" 
  label="Provincia" 
  placeholder="Busca tu provincia..." 
  search="true">
</mm-combobox-v2>

<script>
  const cb = document.querySelector('#provincia-select');
  cb.options = [
    { value: 'M', label: 'Madrid' },
    { value: 'B', label: 'Barcelona' },
    { value: 'V', label: 'Valencia' }
  ];
</script>
```

### 2. Uso en Formulario de Angular
```html
<mm-combobox-v2 
  [options]="provincias" 
  formControlName="provincia" 
  ngDefaultControl 
  label="Provincia de nacimiento">
</mm-combobox-v2>
```

---
> [!TIP]
> **Instrucción:** Usa `mm-combobox-v2` sempre que tengas una lista desplegable con más de 5 opciones para facilitar la selección.
