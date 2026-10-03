# Tecnologías del proyecto — LUMÉ

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetar la estructura, contenido y diseño visual del sitio sin frameworks ni gestores de contenido |
| Versionado | Git y GitHub | Control de versiones, registro de avance mediante commits y respaldo del repositorio en la nube |
| Publicación | GitHub Pages | Alojamiento y despliegue del sitio web estático para visualización pública gratuita |
| Diseño | Whimsical | Creación de moodboards, wireframes, componentes visuales y flujos de usuario |
| Diseño | Google Stitch | Generación y visualización del prototipo en alta fidelidad a partir de las especificaciones |
| IA | Antigravity / Gemini | Asistencia en la definición de requerimientos, estructuración de ideas y generación de código |
| Editor | Antigravity IDE | Entorno de desarrollo para editar archivos Markdown, HTML y CSS |

## Qué es funcional y qué es prototipo

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegación general entre landing, blog y tienda | Funcional |
| Navegación de artículos del blog por categorías | Funcional |
| Visualización de ficha de producto con pirámide olfativa e intensidad | Funcional |
| Compartir artículos del blog en WhatsApp e Instagram | Funcional (enlaces directos y a redes) |
| Consulta de guías de encendido y cuidado de velas en el blog | Funcional |
| Lectura de reseñas y valoraciones de compradores | Funcional (maquetación fija de testimonios) |
| Formulario de captación de correos (10% descuento y guía de aromaterapia) | Prototipo visual |
| Buscador de productos por aroma o sensación | Prototipo visual |
| Filtros de la tienda (familia olfativa, tamaño, precio) | Prototipo visual |
| Selección interactiva de variantes y agregado al carrito de compras | Prototipo visual |
| Personalización de etiqueta, envase y mensaje de regalo | Prototipo visual |
| Calculadora de costo de despacho y tiempo de entrega por comuna | Prototipo visual |
| Formulario de compra rápida / checkout como invitado | Prototipo visual |
| Formulario para enviar comentarios en artículos del blog | Prototipo visual |
| Lista de productos favoritos / deseos | Prototipo visual |
| Cuestionario recomendador de fragancias según estado de ánimo | Prototipo visual |

## Integraciones para una versión real

- **Pasarela de pago:** Transbank (Webpay Plus) o Mercado Pago para procesar transacciones seguras con tarjetas de débito y crédito.
- **Logística y despacho:** Integración con API de couriers o agregadores (como Shipit, Envíame, Starken o Chilexpress) para calcular tarifas dinámicas y plazos de entrega según comuna en tiempo real.
- **Email marketing y CRM:** Herramienta como Mailchimp o Brevo para almacenar los correos captados y automatizar el envío del cupón de 10% y el PDF de aromaterapia.
- **Plataforma e-commerce / Backend:** Backend con base de datos (o Shopify Storefront API / WooCommerce) para almacenar órdenes personalizadas (dedicatorias), persistir el carrito y gestionar inventario.
- **Motor de búsqueda y filtros:** Servicio indexado como Algolia o Meilisearch para ofrecer búsqueda rápida por notas aromáticas y filtros instantáneos.
- **Sistema de reseñas:** Servicio de opiniones verificadas (como Judge.me o Yotpo) para que compradores reales puedan subir comentarios y fotos.

## Restricciones

- **Plazo:** Del 29 de septiembre al 14 de octubre (Fase 1: Requerimientos al 5 de octubre; Fase 2: Specs al 12 de octubre; Fase 3: Prototipo en Stitch al 14 de octubre).
- **Marca:** Emprendimiento ficticio; no cuenta con manual de identidad previo. La paleta de colores, tipografías y componentes visuales se definirán formalmente en la Fase 2 (Specs de diseño).
- **Dispositivos:** Diseño adaptable (*responsive*) para celular y escritorio, con enfoque prioritario en celular (*mobile-first*), ya que la proto-persona (Catalina) navega y compra principalmente desde su teléfono.
