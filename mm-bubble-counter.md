# mm-bubble-counter

**Descripción:**
Pequeña burbuja (indicador numérico) para mostrar contadores de mensajes, notificaciones o elementos pendientes.

## Identificador Técnico
- **Tag:** `<mm-bubble-counter>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `value` | `number` | **Requerido.** Número mostrado en la burbuja. | Número mayor de 0 | `1` |
| `status` | `string` | Importancia visual de la burbuja. | `default`, `neutral`, `urgent`, `disabled` | `"default"` |

---

## Ejemplos para el LLM

### 1. Burbuja de Aviso Pendiente
```html
<mm-bubble-counter value="3" status="default"></mm-bubble-counter>
```

### 2. Notificación Urgente
```html
<mm-bubble-counter value="12" status="urgent"></mm-bubble-counter>
```

### 3. Contador Neutral
```html
<mm-bubble-counter value="0" status="neutral"></mm-bubble-counter>
```

---
> [!NOTE]
> **Instrucción:** Suele colocarse junto a iconos (`mm-icon`) o dentro de textos de cabecera para resaltar la existencia de tareas.
