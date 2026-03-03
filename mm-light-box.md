# mm-light-box (Modal)

**Descripción:**
Componente de ventana modal o emergente (lightbox) para mostrar contenido sobre la interfaz principal, requiriendo atención del usuario.

## Identificador Técnico
- **Tag:** `<mm-light-box>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `label` | `string` | Título que aparece en la cabecera del modal. | Texto libre | `""` |
| `id-lightbox`| `string` | **Requerido.** ID del elemento disparador (ej: botón).| ID enlace | `""` |
| `close-outside`| `boolean` | Permite cerrar al hacer clic fuera del contenido. | `true`, `false` | `true` |
| `render-open` | `boolean` | Indica si el modal nace abierto. | `true`, `false` | `false` |

## Métodos
| Método | Descripción |
| :--- | :--- |
| `open()` | Abre el modal programáticamente. |
| `close()` | Cierra el modal programáticamente. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `opened` | `boolean` | Se emite al abrir (`true`) o cerrar (`false`) el modal. |

---

## Ejemplos para el LLM

### 1. Modal activado por Botón
```html
<mm-button id="btnEliminar" label="Eliminar Registro" type="support"></mm-button>

<mm-light-box label="¿Estás seguro?" id-lightbox="btnEliminar">
  <p>Esta acción no se puede deshacer.</p>
  <div style="display:flex; gap:10px;">
    <mm-button label="Cancelar" type="secondary" onclick="this.closest('mm-light-box').close()"></mm-button>
    <mm-button label="Confirmar Borrado"></mm-button>
  </div>
</mm-light-box>
```

### 2. Uso Programático (JS)
```javascript
const myModal = document.querySelector('mm-light-box');
myModal.open(); // Para abrir sin necesidad de clic en el id-lightbox
```

---
> [!IMPORTANT]
> **Nota de Implementación:** El atributo `id-lightbox` es fundamental para que el componente asocie correctamente el disparador. Si abres el modal por código, asegúrate de que el modal esté presente en el DOM.
