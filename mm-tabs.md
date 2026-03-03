# mm-tabs

**Descripción:**
Componente para dividir el contenido de una sección en pestañas seleccionables, ideal para paneles de configuración o perfiles con mucha información.

## Identificador Técnico
- **Tags:** `<mm-tab>` (Contenedor), `<mm-tab-header>` (Cabeceras), `<mm-tab-content>` (Cuerpos).
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
### `<mm-tab>`
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `type` | `string` | Define el estilo visual. | `line`, `header`, `button` | `"line"` |

### `<mm-tab-header>`
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `content` | `string` | **Requerido.** ID del `mm-tab-content` asociado. | ID | `""` |
| `active` | `boolean` | Indica si esta pestaña es la inicial. | `true`, `false` | `false` |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `tabChange` | `CustomEvent` | Se lanza al cambiar la pestaña activa. |

---

## Ejemplos para el LLM

### 1. Sistema de Pestañas Tipo Línea (Line)
```html
<mm-tab type="line">
  <mm-tab-header slot="tab-header" content="tab1" active>Resumen</mm-tab-header>
  <mm-tab-header slot="tab-header" content="tab2">Datos Personales</mm-tab-header>
  
  <mm-tab-content id="tab1" slot="tab-content" class="active">
    <p>Contenido del resumen...</p>
  </mm-tab-content>
  <mm-tab-content id="tab2" slot="tab-content">
    <p>Formulario de datos personales...</p>
  </mm-tab-content>
</mm-tab>
```

### 2. Estilo Pestaña Botón (Button)
```html
<mm-tab type="button">
  <mm-tab-header slot="tab-header" content="op1" active>Opción A</mm-tab-header>
  <mm-tab-header slot="tab-header" content="op2">Opción B</mm-tab-header>
  
  <mm-tab-content id="op1" slot="tab-content" class="active">Texto A</mm-tab-content>
  <mm-tab-content id="op2" slot="tab-content">Texto B</mm-tab-content>
</mm-tab>
```

---
> [!IMPORTANT]
> **Nota de Estilo:** El uso de `slot="tab-header"` y `slot="tab-content"` es obligatorio para posicionar correctamente los elementos dentro del componente.
