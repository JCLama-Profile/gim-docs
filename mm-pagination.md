# mm-pagination

**Descripción:**
Componente para navegar entre páginas de resultados en listas o tablas extensas.

## Identificador Técnico
- **Tag:** `<mm-pagination>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `total-pages` | `number` | **Requerido.** Número máximo de páginas. | Número mayor de 0 | `1` |
| `current-page`| `number` | Página activa en el arranque. | Número entre 1 y `total-pages` | `1` |
| `simple` | `boolean` | Versión simplificada para acciones rápidas. | `true`, `false` | `false` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `changePage(page)` | `page: number \| 'first' \| 'last'` | Fuerza el salto de navegación. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `pageClick` | `CustomEvent` | Se lanza al cambiar de página por el usuario. |

---

## Ejemplos para el LLM

### 1. Paginación Básica (10 páginas)
```html
<mm-pagination total-pages="10" current-page="1"></mm-pagination>
```

### 2. Implementación en Angular
```html
<mm-pagination 
  [total-pages]="totalResultados" 
  [current-page]="1" 
  (pageClick)="onPageChange($event)">
</mm-pagination>
```

---
> [!IMPORTANT]
> **Instrucción Técnico:** El evento `pageClick` contiene en el campo `detail` el número de la página seleccionada.
