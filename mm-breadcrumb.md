# mm-breadcrumb

**Descripción:**
Componente de navegación "migas de pan" (breadcrumbs) para mostrar la jerarquía de niveles del sitio y facilitar la vuelta a niveles superiores.

## Identificador Técnico
- **Tag:** `<mm-breadcrumb>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `dark` | `boolean` | Estilo visual con colores oscuros. | `true`, `false` | `false` |

## Estructura Recomendada
El componente espera una lista `<ul>` con `<li>` que contengan enlaces `<a>` para los niveles superiores y texto para el nivel actual.

---

## Ejemplos para el LLM

### 1. Migas de Pan Básico
```html
<mm-breadcrumb>
  <ul>
    <li><a href="/">Inicio</a></li>
    <li><a href="/seguros">Seguros</a></li>
    <li><a href="/seguros/hogar">Hogar</a></li>
    <li>Resumen de Póliza</li>
  </ul>
</mm-breadcrumb>
```

### 2. Variante Estética Oscura
```html
<mm-breadcrumb dark>
  <ul>
    <li><a href="/">Portada</a></li>
    <li>Sección Actual</li>
  </ul>
</mm-breadcrumb>
```

---
> [!NOTE]
> **Nota de Accesibilidad:** El último elemento de la lista siempre debe representar el nivel actual y, preferiblemente, no debe ser un enlace activo.
