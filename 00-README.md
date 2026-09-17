# AURENIX — Base de Conocimiento del Proyecto

Esta carpeta es la "memoria" del proyecto AURENIX. La idea es que **cualquier trabajo futuro (código, copy, diseño, contenido) parta de estos archivos** en lugar de reconstruir el contexto cada vez.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `01-contexto-aurenix.md` | Qué es AURENIX, qué problema resuelve, para quién, el sistema D.A.S. (6 fases), propuesta de valor, posicionamiento y mensajes. **Léelo cuando necesites entender el negocio, escribir copy o tomar decisiones de producto.** |
| `02-identidad-marca.md` | Branding: paleta de color, tipografía, personalidad de marca, tono verbal, qué evitar visualmente. **Léelo cuando necesites diseñar o justificar una decisión visual.** |
| `03-guia-tecnica-frontend.md` | Extracción técnica del prototipo `aurenix-v3.html`: variables CSS, tipografías, componentes (nav, hero, botones, secciones), patrones de animación. **Léelo cuando vayamos a escribir o modificar código (web, landing, dashboard, etc.).** |

## Cómo lo vamos a usar de aquí en adelante

Cuando pidas ayuda con código, diseño o contenido para AURENIX, puedes simplemente decir "usa el contexto de AURENIX" y yo reviso estos archivos antes de trabajar, en vez de que tengas que repetir la información en cada conversación.

Si en algún momento el negocio o el branding cambian (nueva paleta, nuevo mensaje, nueva fase del D.A.S.), lo ideal es actualizar el archivo correspondiente aquí en vez de mantener la info solo en la conversación — así no se pierde ni se desactualiza.

## Recomendaciones adicionales (opcional, para cuando quieras ampliar esto)

Cosas que no incluí todavía porque el material fuente aún no las define del todo, pero que valdría la pena crear más adelante como archivos independientes:

- **`04-arquitectura-servicios-precios.md`** — cuando definan los paquetes (Foundation / Growth / Scale mencionados en tus documentos) y sus precios, para no mezclar pricing con identidad de marca.
- **`05-casos-clientes/`** — una carpeta con un archivo por cliente (ej. `zeus-pet-shop.md`, `olyra.md`) siguiendo la estructura de "D.A.S. Operating File" que ya definiste (contexto, diagnóstico, hipótesis, experimentos, datos, decisiones). Esto te sirve tanto de historial real como de dataset para entrenar mensajes/casos de éxito.
- **`06-glosario.md`** — un diccionario corto de términos propios (D.A.S., Fase, Cuello de botella, Experimento, Criterio de salida) para que el copy y el código usen siempre el mismo vocabulario.
- **`07-componentes-ui.md`** — a medida que construyan más pantallas (dashboard de cliente, reportes, etc.), catalogar componentes reutilizables (cards, badges de fase, tablas de métricas) para no reinventar estilos en cada pantalla nueva.

No es necesario crear estos ahora — los menciono para que sepas que la estructura puede crecer de forma ordenada en vez de amontonar todo en un solo documento gigante.
