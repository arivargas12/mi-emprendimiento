---
version: alpha
name: LUMÉ
description: "Design system de velas aromáticas artesanales y bienestar para un refugio de calma y desconexión"
colors:
  primary: "#1F4E3D"
  primary-hover: "#173C2F"
  primary-active: "#122E24"
  on-primary: "#FFFFFF"
  secondary: "#E6BEAE"
  secondary-hover: "#DEC0B2"
  on-secondary: "#2D2723"
  tertiary: "#EF8275"
  tertiary-strong: "#B8512E"
  tertiary-hover: "#9E4322"
  on-tertiary: "#FFFFFF"
  neutral: "#FBF8F4"
  surface: "#FFFFFF"
  surface-warm: "#F4ECE4"
  on-surface: "#2D2723"
  on-surface-variant: "#6E645D"
  disabled: "#E8E4DF"
  on-disabled: "#5C544E"
  success: "#2E6F40"
  on-success: "#FFFFFF"
  error: "#B83A3A"
  on-error: "#FFFFFF"
typography:
  headline-display:
    fontFamily: Cormorant Garamond
    fontSize: 44px
    fontWeight: 600
    lineHeight: 1.15
  headline-lg:
    fontFamily: Cormorant Garamond
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Playfair Display
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  title-md:
    fontFamily: Playfair Display
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 15px
    fontWeight: 600
    lineHeight: 1
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1
  accent-script:
    fontFamily: Caveat
    fontSize: 20px
    fontWeight: 500
    lineHeight: 1.2
rounded:
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-active:
    backgroundColor: "{colors.primary-active}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-secondary-hover:
    backgroundColor: "{colors.secondary-hover}"
    textColor: "{colors.on-secondary}"
  button-accent:
    backgroundColor: "{colors.tertiary-strong}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-accent-hover:
    backgroundColor: "{colors.tertiary-hover}"
    textColor: "{colors.on-tertiary}"
  badge-scent:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 4px 10px
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.title-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-product-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
  card-blog:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.title-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-blog-hover:
    backgroundColor: "{colors.surface-warm}"
    textColor: "{colors.on-surface}"
  hero-banner:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.lg}"
    padding: "{spacing.2xl}"
  cart-summary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  tag-category:
    backgroundColor: "{colors.surface-warm}"
    textColor: "{colors.primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 14px
  tag-offer:
    backgroundColor: "{colors.tertiary-strong}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 12px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 16px
  input-field-focus:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
  input-field-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
    typography: "{typography.body-sm}"
  message-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.success}"
    typography: "{typography.body-sm}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# LUMÉ — Design system

## Overview

LUMÉ es una marca de velas aromáticas artesanales elaboradas con cera de soja 100% natural, fragancias botánicas puras y diseño de autor. El sistema de diseño está concebido para Catalina (23 años, estudiante universitaria), quien busca transformar su habitación en un refugio de desconexión y calma al finalizar sus jornadas de estudio o trabajo.

La identidad visual equilibra cinco pilares fundamentales:
- **Estético:** Inspiración editorial, fotografía con luz natural tenue y paleta suave de inspiración Instagram y Pinterest.
- **Minimalista:** Estructura limpia y despejada, con generoso espacio negativo para permitir pausas visuales y una lectura relajada.
- **Confort:** Predominio de tonos cálidos y texturas orgánicas que transmiten abrigo, evitando superficies blancas frías y saturadas.
- **Artesanal:** Detalles cuidados que evocan recipientes de cerámica, etiquetas de papel lino y dedicatorias con tipografía manuscrita.
- **Aromaterapia:** Matices verdes botánicos y notas olfativas visualizadas de forma sensorial y ordenada.

---

## Colors

La paleta sigue una proporción equilibrada (60% neutros cálidos, 30% secundarios almendrados y 10% acentos botánicos y terracota):

- **Primary (`#1F4E3D` - Verde Bosque Botánico):** Color insignia de la marca. Se utiliza en el botón primario de compra (`button-primary`), enlaces activos y el logotipo principal. **No se utiliza** en fondos de páginas completas ni en textos largos de párrafos para evitar una sensación de pesadez visual.
- **Secondary (`#E6BEAE` - Almendra Seda):** Fondo contenedor para tarjetas de producto (`card-product`), módulos testimoniales y secciones intercaladas de la landing. Otorga calidez y confort artesanal. En interacción, transiciona a `secondary-hover` (`#DEC0B2`).
- **Tertiary & Tertiary Strong (`#EF8275` / `#B8512E` - Salmón Dulce y Terracota Cálido):** Color de acento de alta visibilidad. `#B8512E` se emplea en badges de ofertas (`tag-offer`), botones de acento (`button-accent`) y contador del carrito para asegurar contraste accesible (ratio > 4.9:1 con texto blanco). `#EF8275` se reserva para chips interactivos de aromas (`badge-scent`) con texto oscuro (`#2D2723`, ratio 5.7:1). **No se utiliza** en titulares ni en fondos de sección completos.
- **Neutral (`#FBF8F4` - Lino Marfil Artesanal):** El lienzo base de todas las pantallas (`page`). Reemplaza el blanco digital puro para simular la textura mate de la cera de soja y el papel de algodón.
- **Surface (`#FFFFFF` - Blanco Puro):** Reservado para campos de formulario (`input-field`), tarjetas de blog destacadas y pop-ups, generando contraste sutil y nitidez sobre el fondo neutro.
- **Surface Warm (`#F4ECE4` - Marfil Crema):** Superficie de apoyo para chips de categoría (`tag-category`) y fondos alternos de hover.
- **Text (`#2D2723` - Carbón Espresso Cálido):** Títulos, subtítulos y cuerpo de texto principal. Garantiza un contraste sobresaliente (13.9:1 sobre fondo neutro) sin la rigidez del negro `#000000`.
- **Text Secondary (`#6E645D` - Gris Moca Suave):** Bajadas de encabezado, notas olfativas de salida/corazón/fondo, metadatos y fechas del blog. Cumple estándar WCAG AA (5.2:1).
- **Success (`#2E6F40` - Verde Salvia Matcha):** Notificaciones de cupón de 10% aplicado, productos agregados con éxito al carrito y estados de stock disponible.
- **Error (`#B83A3A` - Carmín Terroso):** Mensajes de validación en formularios de envío, avisos de campos requeridos y alertas de stock agotado.

---

## Typography

El sistema tipográfico combina la nobleza de una serif editorial con la máxima legibilidad de una sans-serif contemporánea en dispositivos móviles:

- **Títulos (`Cormorant Garamond`):** Se emplea en `headline-display` (44px) y `headline-lg` (32px). Confiere sofisticación clásica y serenidad. Se escribe en caja alta y baja (Title Case), nunca en mayúsculas sostenidas completas.
- **Subtítulos y nombres de producto (`Playfair Display`):** Utilizada en `headline-md` (24px) y `title-md` (18px) para nombres de velas en el catálogo y títulos de artículos. Aporta peso visual y distinción.
- **Textos de interfaz y lectura (`Plus Jakarta Sans`):** Aplicada en `body-md` (16px), `body-sm` (14px) y `label-md` (15px). Sus formas geométricas y amplias aberturas aseguran una lectura fluida en pantallas móviles al consultar ingredientes, dimensiones y tiempos de despacho.
- **Detalle de autor / Dedicatoria (`Caveat`):** Utilizada en `accent-script` (20px) para simular la caligrafía a mano en mensajes personalizados de etiquetas y notas de regalo.

### Reglas de jerarquía tipográfica:
1. En cada pantalla existe un único `h1` en `headline-display` o `headline-lg`.
2. Los párrafos de lectura mantienen un `lineHeight` mínimo de 1.6 para garantizar lectura relajada.
3. Los botones y etiquetas usan peso seminegrita (`fontWeight: 600`) para jerarquizar la interactividad.

---

## Layout

- **Ancho máximo de contenedor:** 1200px centrado horizontalmente (`max-width: 1200px; margin: 0 auto;`).
- **Márgenes laterales:** 16px en mobile, 24px en tablet y 32px en desktop.
- **Escala de espaciado:** Uso estricto de múltiplos de 8px (`xs: 4px`, `sm: 8px`, `md: 16px`, `lg: 24px`, `xl: 32px`, `2xl: 48px`, `3xl: 64px`).

### Breakpoints y adaptación responsive:
1. **Mobile (hasta 767px):**
   - Grilla de tienda en 1 columna (o 2 columnas compactas para catálogo rápido).
   - Menú de navegación condensado en panel lateral deslizable (hamburguesa).
   - Filtros de catálogo en drawer deslizable desde la parte inferior.
   - Carrito de compras en vista vertical con estimador de despacho apilado.
   - Espaciado vertical entre secciones: `spacing.xl` (32px).
2. **Tablet (768px a 1023px):**
   - Catálogo de tienda en 2 columnas con tarjetas expandidas.
   - Menú superior visible con enlaces esenciales y buscador rápido.
   - Espaciado vertical entre secciones: `spacing.2xl` (48px).
3. **Desktop (desde 1024px):**
   - Catálogo de tienda en grilla de 3 o 4 columnas.
   - Barra lateral izquierda fija para filtros olfativos y rango de precios.
   - Ficha de producto a 2 columnas (galería a la izquierda, pirámide olfativa y personalización a la derecha).
   - Espaciado vertical entre secciones: `spacing.3xl` (64px).

---

## Elevation & Depth

LUMÉ rechaza las sombras oscuras, duras y artificiales. La jerarquía se construye mediante **estratificación de color cálido y bordes sutiles de arcilla (`#E2D6CB`)**:

- **Nivel 0 (Base plana):** Fondo de página `neutral` (`#FBF8F4`).
- **Nivel 1 (Superficie apoyada):** Tarjetas de producto (`card-product`) y bloques secundarios sobre `secondary` (`#E6BEAE`) con borde sutil de 1px en `#E2D6CB`.
- **Nivel 2 (Flotante suave / Hover):** En estado hover, las tarjetas de catálogo y blog elevan su sombra mediante un resplandor cálido difuminado: `box-shadow: 0 8px 24px rgba(45, 39, 35, 0.08);` y se elevan 3px en el eje vertical (`transform: translateY(-3px)`).
- **Nivel 3 (Modales y navegación fija):** Navbar fijo y panel de carrito deslizante con sombra envolvente: `box-shadow: 0 12px 32px rgba(45, 39, 35, 0.12);` y fondo marfil semitransparente con desenfoque de fondo (`backdrop-filter: blur(8px)`).

---

## Shapes

- **Bordes redondeados completos (`rounded.full` / `9999px`):** Reservados para elementos de interacción rápida: botones (`button-primary`, `button-secondary`, `button-accent`), chips de categorías (`tag-category`), insignias de aromas (`badge-scent`) e insignias de oferta (`tag-offer`). Su silueta de píldora evoca suavidad y calma táctil.
- **Bordes redondeados intermedios (`rounded.md` / `8px`):** Empleados en tarjetas de producto (`card-product`), tarjetas de artículos (`card-blog`), contenedores de imágenes y campos de entrada de texto (`input-field`).
- **Bordes redondeados amplios (`rounded.lg` / `16px`):** Utilizados en banners destacados (`hero-banner`), modales de suscripción y contenedores de la pirámide olfativa.

---

## Components

### Botón Primario (`button-primary`)
El componente de llamada a la acción principal para agregar al carrito y finalizar la compra.
- **Estructura:** Forma de píldora completa (`rounded.full`), tipografía `label-md`, fondo `#1F4E3D`, texto blanco `#FFFFFF`.
- **Reglas concretas:**
  - El texto del botón debe ser un verbo directo en infinitivo o imperativo ("Agregar al carrito", "Finalizar compra").
  - Mantiene un padding horizontal mínimo de 24px para facilitar el tap en pantallas táctiles móviles.
- **Estados:**
  - *Normal:* Fondo `{colors.primary}`, texto `{colors.on-primary}`.
  - *Hover:* Fondo `{colors.primary-hover}` (`#173C2F`), transición suave de 200ms.
  - *Active:* Fondo `{colors.primary-active}` (`#122E24`), escala 0.98.
  - *Disabled:* Fondo `{colors.disabled}` (`#E8E4DF`), texto `{colors.on-disabled}` (`#5C544E`), cursor no permitido.

### Botón Secundario (`button-secondary`)
Utilizado para acciones alternativas como "Ver producto", "Seguir comprando" o "Explorar tienda".
- **Estructura:** Forma de píldora completa, fondo blanco `{colors.surface}`, texto y borde en `{colors.primary}`.
- **Estados:**
  - *Normal:* Fondo blanco con borde de 1.5px en verde botánico.
  - *Hover:* Fondo `{colors.secondary-hover}` (`#DEC0B2`) con texto `{colors.on-secondary}` (`#2D2723`).

### Botón de Acento (`button-accent`)
Llamadas a la acción secundarias de alta conversión, como el botón de suscripción al 10% OFF o "Comprar ahora".
- **Estructura:** Forma de píldora completa, fondo terracota `{colors.tertiary-strong}` (`#B8512E`), texto blanco `{colors.on-tertiary}`.
- **Estados:**
  - *Hover:* Fondo `{colors.tertiary-hover}` (`#9E4322`).

### Tarjeta de Producto (`card-product`)
La unidad fundamental del catálogo y de las recomendaciones de la tienda.
- **Estructura:**
  1. Contenedor de imagen en proporción 1:1 o 4:5 con esquinas `rounded.md`.
  2. Insignia flotante superior izquierda para "Nuevo" o "10% OFF" usando `tag-offer`.
  3. Botón de favoritos (ícono de corazón) en la esquina superior derecha con fondo blanco translúcido.
  4. Familia olfativa en tipografía `label-sm` y color `{colors.on-surface-variant}`.
  5. Nombre del producto en `title-md` (`Playfair Display`), limitado a máximo 2 líneas.
  6. Precio en tipografía `label-md` en color `{colors.on-surface}`, siempre visible.
  7. Botón de compra rápida (`button-primary`).
- **Reglas concretas:**
  - El precio nunca se oculta ni requiere interacción previa para ser visualizado.
  - Si el producto está agotado: imagen desaturada al 40%, badge de "Agotado" y botón primario en estado disabled.
  - En hover: la imagen realiza un suave zoom del 103% con transición de 300ms y la tarjeta gana elevación de Nivel 2.

### Tarjeta de Blog (`card-blog`)
Muestra de artículos y consejos de bienestar en la página de blog y secciones de contenido.
- **Estructura:** Imagen panorámica (proporción 16:9), etiqueta de categoría en `tag-category`, título del artículo en `title-md`, extracto descriptivo de máximo 3 líneas y tiempo estimado de lectura en `body-sm`.
- **Estados:**
  - *Hover:* El fondo de la tarjeta cambia sutilmente a `{colors.surface-warm}` y el título subraya con línea de 1px en `{colors.primary}`.

### Banner de Captación y Hero (`hero-banner`)
Módulo principal de bienvenida y captación de leads en la landing page.
- **Estructura:** Contenedor envolvente con fondo `secondary` (`#E6BEAE`) y bordes `rounded.lg`. Contiene título principal en `headline-display`, bajada explicativa en `body-md`, campo de texto `input-field` para el correo y botón `button-accent` con el texto "OBTENER MI 10% OFF".

### Resumen del Carrito (`cart-summary`)
Contenedor del proceso de compra previa al checkout.
- **Estructura:** Tarjeta blanca `{colors.surface}` con bordes `rounded.md`. Contiene listado de productos con miniatura y dedicatoria personalizada, controles de cantidad (+/-), selector de comuna con cálculo automático de despacho, desglose financiero (Subtotal, Despacho, Total) y botón `button-primary` para continuar al checkout.

### Campo de Texto (`input-field`)
Inputs de formulario para captación de correos, dedicatorias y cálculo de comuna.
- **Estructura:** Fondo `{colors.surface}`, texto `{colors.on-surface}`, borde de 1px en `#E2D6CB`, radio `rounded.md` (8px).
- **Estados:**
  - *Focus:* Borde de 2px en `{colors.primary}` y sombra suave perimetral sin cambiar el color de fondo.
  - *Error:* Borde de 2px en `{colors.error}` acompañado de mensaje explicativo en `message-error`.
  - *Disabled:* Fondo `{colors.disabled}` con texto `{colors.on-disabled}`.

---

## Do's and Don'ts

### Do's (Lo que siempre se hace)
- **Mantener siempre el fondo marfil cálido (`#FBF8F4`)** en todas las vistas generales para preservar la atmósfera acogedora y estética de LUMÉ.
- **Mostrar siempre la composición olfativa (Salida, Corazón, Fondo)** e intensidad de cada vela en su ficha de producto para dar seguridad a Catalina antes de comprar.
- **Verificar que todo texto sobre fondos de color cumpla contraste WCAG AA** (mínimo 4.5:1), usando `#B8512E` para texto blanco sobre terracota y `#2D2723` sobre almendra.
- **Ofrecer compra directa como invitado en el checkout**, sin obligar a Catalina a crear una cuenta antes de pagar.
- **Informar el costo y tiempo estimado de despacho** de manera transparente mediante el calculador de comuna antes del paso final de pago.
- **Preservar espaciados generosos de al menos 16px** alrededor de botones y controles interactivos en dispositivos móviles.

### Don'ts (Lo que nunca se hace)
- **Nunca usar blanco puro brillante (`#FFFFFF`) como fondo de pantalla completa**, ya que resulta frío, estéril y rompe con la sensación de confort y luz de vela.
- **Nunca utilizar sombras negras duras o desenfoques pesados** (`box-shadow: 0 10px 20px #000000`); la profundidad se expresa con capas cálidas y bordes suaves.
- **Nunca emplear mayúsculas sostenidas (All Caps) en párrafos o títulos largos**, para no generar una sensación agresiva o estridente.
- **Nunca ocultar el precio de los productos en las tarjetas del catálogo**; Catalina debe tener total transparencia mientras explora.
- **Nunca saturar la interfaz con colores brillantes de alerta**; los estados de éxito y error deben respetar la tonalidad botánica y terrosa del sistema de diseño.
