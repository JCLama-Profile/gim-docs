# mm-card-slider

**Descripción:**
Componente carrusel (carousel) para navegar entre un listado horizontal de elementos o tarjetas (cards).

## Identificador Técnico
- **Tag:** `<mm-card-slider>`
- **Framework:** Web Component.

## Propiedades (Attributes/Inputs)
| Atributos | Tipo | Descripción | Valores | Por defecto |
| :--- | :--- | :--- | :--- | :--- |
| `last-card` | `boolean` | Posiciona el scroll en la última tarjeta. | `true`, `false` | `false` |

## Métodos
| Método | Parámetros | Descripción |
| :--- | :--- | :--- |
| `addCard(newCard)` | `newCard: HTMLElement` | Añade una tarjeta dinámicamente. |

## Eventos
| Evento | Detalle | Descripción |
| :--- | :--- | :--- |
| `selected` | `CustomEvent` | Emitido con el atributo `data-value` de la tarjeta clicada. |

---

## Ejemplos para el LLM

### 1. Carrusel de Tarjetas Estático
```html
<mm-card-slider>
  <div class="item" data-value="card1">
    <mm-info-card main-title="Tarjeta 1" counter="A"></mm-info-card>
  </div>
  <div class="item" data-value="card2">
    <mm-info-card main-title="Tarjeta 2" counter="B"></mm-info-card>
  </div>
  <div class="item" data-value="card3">
    <mm-info-card main-title="Tarjeta 3" counter="C"></mm-info-card>
  </div>
</mm-card-slider>
```

### 2. Gestión de Selección (JS)
```javascript
const slider = document.querySelector('mm-card-slider');
slider.addEventListener('selected', (e) => {
  console.log('Tarjeta seleccionada ID:', e.detail);
});
```

---
> [!IMPORTANT]
> **Nota Técnico:** Cada elemento hijo debe tener la clase `class="item"` para que el carrusel asigne el espaciado y la animación correctos. Use `data-value` para identificar el elemento seleccionado en el evento.
