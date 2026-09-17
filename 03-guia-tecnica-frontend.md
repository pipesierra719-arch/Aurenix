# AURENIX — Guía Técnica Frontend

> Extraído del prototipo `aurenix-v3.html` (landing en HTML/CSS/JS puro + Three.js). Úsalo como punto de partida en vez de reinventar estilos cada vez que construyamos algo nuevo (dashboard, nueva página, componente, etc.).

## 1. Stack usado en el prototipo

- HTML/CSS/JS vanilla (sin framework)
- Fuentes vía Google Fonts: `Space Grotesk` (400;500;600;700) y `Manrope` (400;500;600;700)
- `three.js` r128 (CDN cdnjs) para la animación 3D del hero (red de nodos/pulsos que representa el "sistema" de adquisición)
- `IntersectionObserver` para revelar el ciclo D.A.S. al hacer scroll
- Glow ambiental que cambia de frío (Titanium) a cálido (Gold) según el progreso de scroll

## 2. Variables CSS base (copiar/pegar en cualquier nuevo build)

```css
:root{
  --obsidian:#0B0D10;
  --obsidian-hover:#12161C;
  --graphite:#15191F;
  --elevated:#1B2027;
  --gold:#C9A227;
  --gold-hover:#E0B83A;
  --gold-active:#A98516;
  --titanium:#8E98A7;
  --titanium-hover:#AAB3C0;
  --ice:#F2F4F7;
  --line: rgba(142,152,167,0.22);
  --maxw: 1120px;
}
```

## 3. Reglas de tipografía

```css
h1,h2,h3,.display{
  font-family:'Space Grotesk', sans-serif;
  font-weight:600;
  letter-spacing:-0.01em;
}
body{
  font-family:'Manrope', sans-serif;
  font-size:16px;
  line-height:1.6;
}
```

Selección de texto personalizada: `::selection{ background:var(--gold); color:var(--obsidian); }`
Foco accesible: outline dorado de 2px con offset de 3px.

## 4. Componentes clave del prototipo

- **Header/nav:** fijo (`position:fixed`), fondo Obsidian semitransparente + `backdrop-filter: blur(10px)`, borde inferior sutil en `--line`.
- **Botón primario (`.btn-primary`):** fondo Gold, texto Obsidian, hover `--gold-hover`, active `--gold-active`.
- **Botón secundario (`.btn-ghost`):** transparente, borde `--line`, hover pasa el borde a `--titanium-hover`.
- **Hero:** fondo con patrón de puntos sutil en Gold (radial-gradient de 1px), máscara de degradado hacia abajo, título grande con `clamp()` para responsive, visual 3D (red de nodos) al costado.
- **Fórmula de fases:** línea de texto tipo `Digitalizar → Adquirir → Convertir...` con separadores en Gold.
- **Secciones:** `padding: 108px 0`, separadas por `border-top: 1px solid var(--line)`.
- **Ciclo D.A.S.:** se revela con animación al entrar en viewport (`IntersectionObserver`, threshold 0.3), clase `.in-view`.
- **Glow ambiental:** dos capas de `radial-gradient` fijas (`.scene-glow.cool` y `.scene-glow.warm`) cuya opacidad se interpola según el scroll de la página (frío al inicio, cálido al final).
- **Visual 3D del hero:** esfera de Fibonacci con 32 "nodos" (usuarios), líneas de conexión en Titanium, un "hub" central en Gold (AURENIX) que emite pulsos dorados hacia la red — metáfora visual de adquisición/sistema en tiempo real.

## 5. Patrones a reutilizar en nuevos desarrollos

- Cualquier nueva pantalla (dashboard de cliente, reporte, propuesta interactiva) debería heredar las variables CSS de la sección 2 y las dos tipografías, para mantener consistencia sin copiar el HTML completo.
- Si se construye un dashboard funcional (React, etc.), migrar estas variables a un archivo de tema (`theme.ts` / `tailwind.config` / CSS vars) en lugar de hardcodear hex sueltos.
- Mantener el patrón de "moderación del dorado": en componentes nuevos, el gold debe reservarse para acciones, estados destacados o números clave — nunca como color de fondo grande.
- Para gráficos/dashboards de datos (fase Optimizar/Escalar del D.A.S.), Titanium es el color por defecto para series neutras, y Gold se reserva para resaltar el dato o la fase "ganadora" de un experimento.

## 6. Pendiente / a definir cuando avancemos con código real

- Si el siguiente desarrollo será una landing más (HTML/CSS/JS) o una app con framework (React, Next, etc.) — esto cambia cómo migramos las variables y componentes.
- Sistema de componentes para el "D.A.S. Operating File" por cliente (tablas de fases, badges de estado DEFICIENTE/FUNCIONAL/PREPARADA/OPTIMIZADA, registro de experimentos) — todavía no existe una UI para esto, solo el concepto.
