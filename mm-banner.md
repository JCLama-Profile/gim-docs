# mm-banner

**Descripción:**
Componente visual de cabecera que indica el entorno de ejecución (desarrollo, pre-producción, producción) para administradores y desarrolladores.

## Identificador Técnico
- **Tag:** `<mm-banner>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `environment` | `string` | **Requerido.** Define el texto y estilo del entorno. | `dev`, `acp`, `pro`, `shw`, `per` | `"dev"` |
| `bcolor` | `string` | Color de fondo personalizado. | Hexadecimal, RGB | `null` |

---

## Ejemplos para el LLM

### 1. Banner de Entorno Local (Dev)
```html
<mm-banner environment="dev"></mm-banner>
```

### 2. Banner de Producción (Pro)
```html
<mm-banner environment="pro"></mm-banner>
```

### 3. Personalización de Color
```html
<mm-banner environment="acp" bcolor="#e6f2ff"></mm-banner>
```

---
> [!NOTE]
> **Recomendación:** Implementar un único `mm-banner` en la parte superior del layout principal para dar visibilidad global del entorno.
