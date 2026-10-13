# Arquitectura de la información — LUMÉ

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

```text
Inicio (landing)
├── Tienda (catálogo general)
│   ├── Categoría: Florales y Frescas
│   ├── Categoría: Cítricas y Energizantes
│   ├── Categoría: Amaderadas y Cálidas
│   ├── Categoría: Dulces y Especiadas
│   ├── Ficha de producto (detalle, pirámide olfativa y personalización)
│   ├── Carrito de compras (con estimador de despacho)
│   └── Checkout (finalizar compra como invitado)
├── Blog
│   ├── Categoría: Aromaterapia y Bienestar
│   ├── Categoría: Cuidado de Velas
│   ├── Categoría: Decoración e Inspiración
│   ├── Categoría: Regalos y Ocasiones Especiales
│   └── Artículo de blog (con comentarios y compartir)
├── Nosotros (historia artesanal de LUMÉ y valores)
├── Contacto (formulario y enlace a WhatsApp/Instagram)
├── Preguntas frecuentes (FAQ: envíos, cuidados y tiempos)
├── Términos y condiciones
├── Política de privacidad
└── 404 (Página de error con enlace de retorno al inicio)
```

### Dónde ocurre cada funcionalidad

| # | Funcionalidad | Página donde ocurre | Ubicación y contexto en el sitio |
|---|---|---|---|
| 1 | Captación de leads (10% dcto. y guía digital) | **Inicio (landing)** y pie de página | Sección destacada de suscripción en la landing y accesible en el footer global. |
| 2 | Navegar artículos por categoría | **Blog** | Cabecera y barra de categorías de la página principal del blog. |
| 3 | Comentar un artículo | **Artículo de blog** | Sección inferior al final de cada publicación del blog. |
| 4 | Compartir artículo en WhatsApp / Instagram | **Artículo de blog** | Barra de botones para compartir al inicio y cierre del artículo. |
| 5 | Buscar productos por aroma o sensación | **Header global** y **Tienda** | Barra de búsqueda disponible en el encabezado general y en el catálogo. |
| 6 | Filtrar productos (familia, tamaño, precio) | **Tienda** | Barra lateral o superior de filtros dentro del catálogo de la tienda. |
| 7 | Ver detalle, variantes y agregar al carrito | **Ficha de producto** | Panel principal del producto con selector de tamaño, aroma y botón de compra. |
| 8 | Consultar pirámide olfativa e intensidad | **Ficha de producto** | Pestaña o bloque informativo con notas de salida, corazón, fondo e intensidad. |
| 9 | Personalizar vela (etiqueta y dedicatoria) | **Ficha de producto** | Formulario integrado en la ficha para escribir el mensaje de la etiqueta y dedicatoria. |
| 10 | Calcular costo y tiempo de despacho | **Carrito de compras** y **Ficha** | Calculadora por comuna antes de pasar a la pasarela de pago. |
| 11 | Compra rápida / Checkout como invitado | **Checkout** | Pantalla única de pago y datos de envío sin registro de cuenta obligatorio. |
| 12 | Consultar reseñas y valoraciones | **Ficha de producto** e **Inicio** | Reseñas y calificaciones con estrellas bajo la descripción del producto y destacados en landing. |
| 13 | Guardar en lista de favoritos | **Tienda** y **Ficha de producto** | Botón en las tarjetas del catálogo y junto al título en la ficha de producto. |
| 14 | Cuestionario recomendador de aromas (quiz) | **Inicio (landing)** y **Tienda** | Sección interactiva de ayuda para encontrar fragancias según el estado de ánimo o espacio. |
| 15 | Guías de encendido y cuidado seguro | **Artículo de blog** y **Ficha** | Artículos dedicados en el blog con enlace directo desde la ficha técnica de la vela. |

---

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

**Proto-persona:** Catalina (23 años, estudiante universitaria).  
**Objetivo:** Encontrar una vela relajante desde su celular por la noche para ambientar su habitación de estudio y preparar su compra.

```text
Instagram (Reel nocturno: "Crea tu ritual de desconexión y calma después de estudiar")
→ [Clic en enlace del sticker / bio de LUMÉ]
→ Inicio (landing)
→ [Lee la propuesta de valor y hace clic en "Explorar tienda"]
→ Tienda (catálogo general)
→ [Aplica filtro por familia olfativa "Florales y Frescas" y busca sensación "Relajación"]
→ [Revisa las tarjetas de productos, ve valoraciones de 5 estrellas y hace clic en "Brisa de Lavanda & Manzanilla"]
→ Ficha de producto (Brisa de Lavanda & Manzanilla)
→ [Revisa notas olfativas de salida, corazón y fondo; selecciona formato de 220 g en frasco ámbar]
◇ ¿Desea personalizar la vela como regalo o con un mensaje especial?
   ├── Sí → [Activa casilla "Personalizar vela", redacta mensaje en etiqueta y dedicatoria]
   └── No → [Mantiene la etiqueta estándar de LUMÉ]
◇ ¿Tiene dudas con el despacho o el aroma?
   ├── Sí → [Clic en botón "Consultar por WhatsApp"] → WhatsApp (asesoría rápida y retorno al sitio)
   └── No → [Continúa directo en la ficha]
→ [Clic en "Agregar al carrito"]
→ Carrito de compras
→ [Revisa el resumen del pedido e ingresa su comuna para calcular costo y fecha estimada de despacho]
→ [Clic en "Continuar compra"]
→ Checkout (finalizar compra como invitado)
→ Fin: Carrito listo para pagar sin registro obligatorio
```

### Flujo 2: contenido

**Proto-persona:** Catalina.  
**Objetivo:** Resolver una duda sobre el cuidado de sus velas buscando en Google, descubriendo un producto afín y suscribiéndose a un beneficio.

```text
Google (Búsqueda: "cómo evitar que una vela de soja haga túnel y se consuma al medio")
→ Artículo de blog ("El secreto del primer encendido: cómo evitar el efecto túnel en tus velas y hacerlas durar el doble")
→ [Lee los consejos prácticos de tiempo de quemado y recorte de mecha]
→ [Encuentra la recomendación integrada: velas de cera de soja 100% natural con mecha de algodón puro]
◇ ¿Qué decide hacer tras leer la recomendación del artículo?
   ├── Opción A: Comprar la vela recomendada
   │   → [Hace clic en la tarjeta del producto destacado "Calma Profunda (Lavanda & Sándalo)"]
   │   → Ficha de producto
   │   → [Selecciona tamaño de 220 g y hace clic en "Agregar al carrito"]
   │   → Carrito de compras
   │   → Fin: Producto añadido al carrito listo para el checkout
   │
   └── Opción B: Guardar consejos y aprovechar descuento
       → [Baja al bloque final del artículo y escribe su correo en el formulario de captación]
       → [Recibe confirmación con código de 10% de descuento y Guía Digital de Aromaterapia]
       → [Hace clic en "Compartir artículo en WhatsApp" para enviarlo a una amiga de la universidad]
       → Fin: Lead captado con cupón y contenido compartido
```

---

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

Las categorías están organizadas por **familias olfativas y sensaciones**, que es la manera intuitiva en que Catalina busca aromas según el ambiente que desea crear:

| Categoría | Productos |
|---|---|
| **Florales y Frescas** | • Vela *Brisa de Lavanda & Manzanilla* (220 g / 350 g, relajación y descanso nocturno)<br>• Vela *Jardín de Jazmín Blanco & Peonía* (220 g, frescura suave y elegante)<br>• Vela *Lino Limpio & Flor de Algodón* (220 g, sensación de orden y pureza)<br>• Set Trío Mini Florales (3 x 90 g, formato para probar aromas) |
| **Cítricas y Energizantes** | • Vela *Amanecer de Mandarina & Bergamota* (220 g / 350 g, vitalidad y despertar matutino)<br>• Vela *Limón Verbena & Té Verde* (220 g, concentración para estudio y trabajo)<br>• Vela *Pomelo Rosado & Romero* (220 g, estímulo mental y frescura activa)<br>• Vela viajera *Mandarina Citrus* (lata metálica de 120 g) |
| **Amaderadas y Cálidas** | • Vela *Bosque de Cedro & Sándalo Dulce* (220 g / 350 g, calma profunda y meditación)<br>• Vela *Ámbar Dorado & Hojas de Tabaco* (220 g, sofisticación y aroma envolvente)<br>• Vela *Palo Santo & Salvia Blanca* (220 g, limpieza energética y equilibrio)<br>• Vela *Fuego de Hogar* (250 g con mecha de madera crepitante) |
| **Dulces y Especiadas** | • Vela *Vainilla Bourbon & Haba Tonka* (220 g / 350 g, dulzura reconfortante y calidez)<br>• Vela *Canela Especiada & Manzana Asada* (220 g, ambiente acogedor de otoño/invierno)<br>• Vela *Caramelo Salado & Café Tostado* (220 g, notas gourmand intensas)<br>• Vela *Chai Latte & Jengibre* (220 g, sensación reconfortante de tarde) |

> **Filtros complementarios en la tienda:**
> - **Familia olfativa:** Florales, Cítricas, Amaderadas, Dulces.
> - **Sensación deseada:** Relajación / Dormir, Concentración / Estudio, Energía / Ánimo, Calidez / Confort.
> - **Formato / Tamaño:** Mini lata (90-120 g), Frasco ámbar clásico (220 g), Doble mecha grande (350 g), Set de regalo.
> - **Rango de precio:** $8.990 a $24.990 CLP.

---

### Categorías del blog

El blog de LUMÉ funciona como una estrategia de atracción y fidelización de contenidos conectada a las necesidades diarias de Catalina:

| Categoría | Idea de artículo | Necesidad o motivación de Catalina | Producto relacionado |
|---|---|---|---|
| **Aromaterapia y Bienestar** | *"5 aromas ideales para estudiar sin estrés y descansar mejor por las noches"* | Necesita desconectarse tras largas jornadas universitarias frente a pantallas y preparar su ambiente para conciliar el sueño sin ansiedad. | Vela *Brisa de Lavanda & Manzanilla* y Vela *Limón Verbena & Té Verde*. |
| **Cuidado de Velas** | *"El secreto del primer encendido: cómo evitar el efecto túnel en tus velas y hacerlas durar el doble"* | Le frustra que una vela cara se consuma despareja o pierda su aroma; busca consejos prácticos y sencillos para optimizar su compra. | Vela *Bosque de Cedro & Sándalo Dulce* y Kit de accesorios LUMÉ (cortapabilos y apagavelas). |
| **Decoración e Inspiración** | *"Cómo transformar tu escritorio o habitación en un rincón aesthetic y acogedor con velas"* | Quiere que su pieza se vea linda y armónica (estilo Pinterest) con bajo presupuesto, además de inspirarse para regalar a sus amigas. | Vela *Vainilla Bourbon & Haba Tonka* (con etiqueta personalizada) y Set Trío Mini Florales. |
| **Regalos y Ocasiones Especiales** | *"Guía de detalles personalizados: cómo armar un regalo significativo y con dedicatoria única"* | Le motiva dar regalos con cariño y significado a sus seres queridos en cumpleaños o titulaciones, buscando un proceso rápido y lindo. | Servicio de personalización en etiqueta y caja de regalo LUMÉ. |
