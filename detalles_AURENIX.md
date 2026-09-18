# Prompt --- Implementación del Funnel Comercial AURENIX

## Contexto

Estás trabajando sobre el sitio web actual de **AURENIX**.

AURENIX es un sistema de adquisición digital para negocios. Su propuesta
se estructura en:

**Digitalizar → Adquirir → Convertir → Optimizar → Escalar →
Automatizar**

La arquitectura comercial y los precios definidos en Notion son la
**fuente de verdad**:

**AURENIX --- Service & Value Architecture + Pricing & Unit Economics**

No inventes nuevos servicios, precios, garantías ni condiciones
comerciales.

------------------------------------------------------------------------

# Objetivo de esta implementación

Modificar el sitio web para que el proceso comercial deje de ser:

**CTA → Calendario → llamada genérica**

y pase a ser:

**CTA → Formulario de contexto → Revisión → Calendario → Descubrimiento
AURENIX → Siguiente paso**

El objetivo es que, antes de hablar con un prospecto, AURENIX ya tenga
suficiente contexto para que la conversación sea específica, estratégica
y orientada a determinar si existe una oportunidad real de trabajo.

La llamada inicial **no debe presentarse como el Diagnóstico AURENIX**.

Debe existir una separación clara entre:

### Descubrimiento AURENIX

-   Gratis
-   30 minutos
-   Primera conversación
-   Comprender el negocio
-   Identificar el principal cuello de botella
-   Determinar si existe encaje para trabajar juntos

### Diagnóstico AURENIX

-   \$350.000 COP
-   3--5 días hábiles
-   Análisis formal del negocio
-   Auditoría del estado actual
-   Infraestructura
-   Adquisición
-   Conversión
-   Identificación del cuello de botella
-   Hipótesis
-   Prioridades
-   Roadmap
-   Si el cliente contrata implementación dentro de 30 días, el valor
    del diagnóstico puede acreditarse contra la implementación.

------------------------------------------------------------------------

# 1. Nueva arquitectura del CTA "Agendar una llamada"

El botón:

**Agendar una llamada**

NO debe llevar directamente al calendario.

Debe llevar al siguiente flujo:

``` text
AGENDAR UNA LLAMADA
        ↓
FORMULARIO AURENIX
        ↓
REVISIÓN DE INFORMACIÓN
        ↓
CALENDARIO
        ↓
DESCUBRIMIENTO AURENIX — 30 MIN
        ↓
SIGUIENTE PASO
```

------------------------------------------------------------------------

# 2. Formulario de contexto

Crear una pantalla/formulario antes del calendario.

## Título

**Antes de agendar, conozcamos tu negocio.**

## Texto

> Queremos que la conversación tenga contexto desde el primer minuto.
> Cuéntanos brevemente qué haces, cómo consigues clientes actualmente y
> qué quieres mejorar. Revisaremos esta información antes de la llamada
> para llegar con una perspectiva inicial sobre tu situación.

## Campos

### Información básica

-   Nombre
-   Empresa / negocio
-   Sitio web o Instagram
-   Correo electrónico
-   WhatsApp

### Negocio

**¿Qué vende tu negocio?**

Campo de texto.

### Adquisición actual

**¿Cómo consigues clientes actualmente?**

Permitir selección múltiple cuando sea posible:

-   Referidos
-   Instagram
-   Facebook
-   TikTok
-   WhatsApp
-   Publicidad
-   Google
-   Marketplace
-   Tienda física
-   Otro

### Problema principal

**¿Cuál es actualmente tu principal problema para conseguir más
clientes?**

Campo de texto amplio.

### Rango aproximado de ventas mensuales

-   Menos de \$5M COP
-   \$5M--\$10M COP
-   \$10M--\$30M COP
-   \$30M--\$50M COP
-   Más de \$50M COP
-   Prefiero no decirlo

### Objetivo

**¿Qué quieres conseguir durante los próximos 3--6 meses?**

Campo de texto.

### Prioridad

**¿Qué te gustaría mejorar primero?**

Campo de texto.

------------------------------------------------------------------------

# 3. CTA del formulario

Botón:

**Continuar al calendario**

Al completar correctamente el formulario debe mostrarse:

> **Información recibida.**
>
> Ya tenemos una primera perspectiva de tu negocio. Ahora selecciona el
> horario que mejor te funcione para conversar.

Botón:

**Seleccionar horario**

------------------------------------------------------------------------

# 4. Integración del calendario

Mantener la integración existente si funciona correctamente.

La URL debe seguir siendo configurable mediante:

``` text
NEXT_PUBLIC_CALENDLY_URL
```

No hardcodear una URL falsa.

No crear una integración artificial si ya existe una funcional.

## Nombre del evento

**Descubrimiento AURENIX**

## Duración

**30 minutos**

## Descripción

Usar contenido en español:

> Una conversación inicial para entender tu negocio, identificar el
> principal cuello de botella en tu proceso de adquisición y determinar
> si tiene sentido trabajar juntos.
>
> Revisaremos la información que nos compartiste antes de la llamada
> para que la conversación tenga un objetivo concreto.

------------------------------------------------------------------------

# 5. Importante: idioma

Todo el contenido controlado por AURENIX debe estar en español.

Esto incluye:

-   Formulario
-   Botones
-   Mensajes
-   Confirmaciones
-   Descripciones
-   Microcopy
-   Estados de carga
-   Errores
-   Textos alrededor del calendario

Si Calendly u otra plataforma externa muestra elementos nativos en
inglés que no pueden traducirse desde nuestra implementación, NO hackear
la interfaz.

Mantener en español todo lo que sí controla AURENIX.

------------------------------------------------------------------------

# 6. Sección "Qué sucede después de contactarnos"

Reemplazar cualquier copy que genere confusión.

Debe comunicar este proceso:

### 01 --- Conocemos tu negocio

Completas algunas preguntas para que podamos entender qué vendes, cómo
consigues clientes y dónde está el problema.

### 02 --- Analizamos tu situación

Revisamos la información antes de la llamada para llegar con contexto.

### 03 --- Tenemos una conversación de 30 minutos

Identificamos el principal cuello de botella y determinamos si tiene
sentido trabajar juntos.

**Esta primera conversación no tiene costo.**

### 04 --- Si existe una oportunidad

Si el negocio requiere un análisis más profundo, podemos avanzar al:

**Diagnóstico AURENIX --- \$350.000 COP**

Incluye análisis, hipótesis, prioridades y roadmap.

Si posteriormente se contrata la implementación dentro de 30 días, el
valor del diagnóstico puede acreditarse contra la implementación.

### 05 --- Construimos

Si existe encaje, definimos el alcance, inversión y plan de
implementación correspondiente.

------------------------------------------------------------------------

# 7. FAQ

Revisar toda la sección FAQ para eliminar contradicciones.

## ¿Cuánto cuesta trabajar con AURENIX?

Utilizar:

> El Diagnóstico AURENIX tiene un valor de **\$350.000 COP**.
>
> Las implementaciones parten desde **\$3.500.000 COP**, dependiendo del
> alcance.
>
> Los servicios de Growth / Optimización están entre **\$1.500.000 y
> \$2.500.000 COP mensuales**, según el alcance.
>
> La inversión publicitaria, software de terceros y desarrollos
> extraordinarios se cotizan por separado.

------------------------------------------------------------------------

## ¿La primera llamada tiene algún costo?

> No. La primera conversación es un **Descubrimiento AURENIX de 30
> minutos sin costo**.
>
> Su objetivo es entender tu negocio, identificar el principal cuello de
> botella y determinar si tiene sentido avanzar.
>
> Si se requiere un análisis más profundo, podemos avanzar al
> Diagnóstico AURENIX, cuyo valor es de \$350.000 COP.

------------------------------------------------------------------------

## ¿Qué incluye el Diagnóstico AURENIX?

> Analizamos el estado actual del negocio, infraestructura digital,
> adquisición, conversión y principales cuellos de botella.
>
> A partir de esa información construimos hipótesis, prioridades y un
> roadmap de acción.
>
> El diagnóstico tiene una duración estimada de **3--5 días hábiles**.

------------------------------------------------------------------------

## ¿Cuánto tarda implementar el sistema?

> Una implementación típica puede tomar entre **3 y 6 semanas**,
> dependiendo del alcance, complejidad y recursos necesarios.

------------------------------------------------------------------------

## ¿Qué pasa si el sistema no funciona?

No prometer resultados garantizados.

Utilizar:

> AURENIX no garantiza una cantidad específica de ventas o clientes.
>
> Trabajamos mediante diagnóstico, hipótesis, implementación, medición y
> aprendizaje.
>
> Los datos y la evidencia determinan qué debemos mantener, modificar o
> descartar.

------------------------------------------------------------------------

## ¿Con qué tipo de negocios trabajan?

> Trabajamos principalmente con negocios que tienen una oferta definida,
> cierta capacidad operativa, algunas ventas existentes y disposición
> para invertir en construir un sistema de adquisición medible.
>
> AURENIX no se plantea simplemente como un servicio de publicación de
> contenido ni como una promesa de resultados garantizados.

------------------------------------------------------------------------

# 8. CTA "Construir mi sistema"

Este CTA puede continuar dirigiendo directamente a WhatsApp.

Mantener:

**Construir mi sistema**

Opcionalmente utilizar un mensaje prellenado.

Ejemplo:

> Hola, quiero conocer cómo AURENIX podría ayudar a mi negocio a
> construir un sistema de adquisición.

No convertir este CTA en el mismo flujo obligatorio del calendario.

------------------------------------------------------------------------

# 9. Confirmación después de agendar

Después de completar la reserva debe mostrarse una confirmación clara en
español.

## Título

**Tu sesión está agendada.**

## Mensaje

> Revisaremos la información que compartiste antes de la conversación
> para llegar con contexto y aprovechar mejor los 30 minutos.

No prometer resultados específicos de la llamada.

------------------------------------------------------------------------

# 10. Analítica

Si ya existe infraestructura de analytics, conservarla.

Agregar, si es compatible con la arquitectura actual, los siguientes
eventos:

``` text
cta_build_system_click
cta_book_call_click
qualification_form_started
qualification_form_completed
calendar_opened
call_booked
```

No romper analytics existentes.

------------------------------------------------------------------------

# 11. Diseño

Mantener completamente la identidad visual actual de AURENIX:

### Dirección

**Dark Tech + Electric Gold**

### Colores principales

``` text
Obsidian: #0B0D10
Graphite: #15191F
Aure Gold: #C9A227
```

No introducir:

-   Morados
-   Violetas
-   Gradientes genéricos de IA
-   Azul SaaS genérico
-   Cambios innecesarios de identidad

El formulario debe sentirse como una parte natural del sistema AURENIX y
no como una página externa desconectada.

------------------------------------------------------------------------

# 12. No implementar todavía

En esta iteración NO agregar:

-   Testimonios
-   Logos de clientes
-   Casos de éxito
-   Resultados inventados
-   Métricas ficticias
-   Claims de ventas
-   Garantías de resultados

Esta fase se concentra exclusivamente en corregir y construir el funnel
comercial.

------------------------------------------------------------------------

# 13. Reglas comerciales

La implementación debe respetar estas reglas:

-   Primera conversación: gratis.
-   Diagnóstico profundo: \$350.000 COP.
-   Implementación: desde \$3.500.000 COP.
-   Growth / Optimización: \$1.500.000--\$2.500.000 COP/mes.
-   Automatización: desde \$1.500.000 COP según proyecto.
-   Inversión publicitaria: separada.
-   Software de terceros: separado.
-   Desarrollo extraordinario: separado.
-   No garantizar ventas.
-   No ofrecer horas estratégicas ilimitadas.
-   Trabajo fuera de alcance = nueva cotización.
-   Growth se plantea después de que exista una base/sistema sobre el
    cual optimizar.
-   Automatización se plantea cuando el volumen y estabilidad del
    negocio justifican su implementación.

------------------------------------------------------------------------

# 14. Experiencia que debe percibir el prospecto

La experiencia final debe comunicar implícitamente:

> "AURENIX no quiere venderme una solución genérica. Primero quiere
> entender mi negocio, revisar mi situación y llegar a la conversación
> con contexto."

El prospecto debe entender claramente que:

**No está comprando una llamada.**

Está entrando en un proceso de evaluación:

``` text
CONTEXTO
   ↓
DESCUBRIMIENTO
   ↓
DIAGNÓSTICO (SI APLICA)
   ↓
IMPLEMENTACIÓN
   ↓
OPTIMIZACIÓN
   ↓
ESCALA
   ↓
AUTOMATIZACIÓN
```

------------------------------------------------------------------------

# 15. Validación técnica obligatoria

Antes de finalizar:

1.  Ejecutar build.
2.  Ejecutar lint si existe.
3.  Verificar TypeScript.
4.  Verificar responsive.
5.  Verificar navegación.
6.  Verificar todos los CTA.
7.  Verificar formulario.
8.  Verificar validaciones.
9.  Verificar transición formulario → calendario.
10. Verificar `NEXT_PUBLIC_CALENDLY_URL`.
11. Verificar confirmación posterior.
12. Verificar eventos de analytics si existen.
13. Revisar que no existan textos contradictorios sobre el precio del
    diagnóstico.
14. Buscar específicamente cualquier texto que diga que el "Diagnóstico"
    es gratuito y corregirlo.
15. Revisar desktop y mobile.

------------------------------------------------------------------------

# 16. Entrega final

Cuando termines, entrega un reporte breve con:

### Cambios realizados

-   Qué componentes modificaste.
-   Qué páginas/secciones modificaste.
-   Qué copy cambiaste.

### Funnel final

Mostrarlo así:

``` text
CTA
↓
Formulario
↓
Revisión
↓
Calendario
↓
Descubrimiento AURENIX
↓
Diagnóstico (si aplica)
↓
Implementación
```

### Integración

Indicar:

-   Cómo está configurado Calendly.
-   Si utiliza `NEXT_PUBLIC_CALENDLY_URL`.
-   Qué queda pendiente configurar manualmente.

### Analytics

Indicar qué eventos fueron agregados o conservados.

### Tests

Indicar:

-   Build
-   Lint
-   TypeScript
-   Responsive
-   Links
-   Formulario
-   Calendario

### Pendientes

Indicar únicamente aquello que realmente requiere una acción manual.

------------------------------------------------------------------------

# Criterio final de éxito

La implementación estará terminada cuando un visitante pueda entrar al
sitio y entender, sin confusión:

**AURENIX primero quiere conocer mi negocio → revisa mi contexto → tengo
una conversación inicial gratuita de 30 minutos → si existe una
oportunidad, puedo avanzar a un diagnóstico profundo → posteriormente se
define la implementación.**

No debe existir ninguna contradicción entre:

-   Descubrimiento gratuito
-   Diagnóstico pagado
-   Implementación
-   Growth
-   Automatización
-   Precios
-   CTA
-   Calendario

La experiencia debe sentirse como un **sistema comercial profesional**,
no como un formulario añadido al sitio.
