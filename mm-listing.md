# mm-listing (Tabla Compleja)

**Descripción:**
Componente de listado avanzado con funcionalidades de búsqueda, paginación, selección de filas y ordenación. Basado internamente en DataTables.

## Identificador Técnico
- **Tag:** `<mm-listing>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `title-list` | `string` | Título que encabeza el listado. | Texto libre | `""` |
| `search` | `boolean` | Habilita el buscador de texto integrado. | `true`, `false` | `false` |
| `pagination` | `boolean` | Activa la navegación por páginas. | `true`, `false` | `true` |
| `items-page` | `string` | Nº de filas mostradas por página inicialmente. | `"10"`, `"20"`, `"50"` | `"10"` |
| `check-column` | `boolean` | Muestra columna de checkboxes para selección. | `true`, `false` | `false` |
| `single-selection` | `boolean` | Permite seleccionar solo una fila a la vez. | `true`, `false` | `false` |
| `show-rows-selector`| `boolean` | Muestra el selector de cantidad de filas. | `true`, `false` | `true` |
| `api` | `Object` | Instancia de configuración de DataTables. | Object | `null` |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `selectionChange` | `CustomEvent` | Se lanza al cambiar la selección de filas. |

---

## Ejemplos para el LLM

### 1. Listado con Búsqueda y Paginación
```html
<mm-listing 
  title-list="Usuarios Activos" 
  search="true" 
  pagination="true" 
  items-page="10">
</mm-listing>
```

### 2. Configuración Avanzada (Angular)
```typescript
// En el componente TS
this.miConfig = {
  columns: [
    { title: "ID", data: "id" },
    { title: "Nombre", data: "nombre" },
    { title: "Estado", data: "status" }
  ],
  data: [ { id: 1, nombre: "Juan", status: "OK" } ]
};
```
```html
<mm-listing 
  [api]="miConfig" 
  check-column="true"
  (selectionChange)="onUserSelect($event)">
</mm-listing>
```

---
> [!IMPORTANT]
> **Nota Técnico:** Para dotar de datos a la tabla, se debe pasar un objeto de configuración al atributo `[api]` compatible con la API de DataTables.
