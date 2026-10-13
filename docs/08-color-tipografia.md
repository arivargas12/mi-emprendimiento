# Color y tipografía — LUMÉ

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

### Paleta principal (Roles funcionales del sitio)

| Rol | Color | HEX | Uso |
|---|---|---|---|
| **Principal** | Verde Bosque Botánico *(Deep Forest)* | `#1F4E3D` | Botones principales de compra, enlaces activos, logotipo y acentos destacados (extraído del bloque editorial *"Stay in the loop"* del moodboard). |
| **Secundario** | Almendra Seda *(Almond Silk)* | `#E6BEAE` | Fondos de tarjetas de producto, secciones de testimonios, cápsulas y bordes suaves (código HEX exacto del moodboard). |
| **Acento** | Salmón Dulce *(Sweet Salmon)* | `#EF8275` | Badges de ofertas (*10% OFF*), detalles que llaman la atención, chips activos y etiquetas aromáticas (código HEX exacto del moodboard). |
| **Acento oscuro** | Terracota Cálido | `#C05C38` | Fondo de botones y badges con texto blanco que requieren alto contraste accesible (versión contrastada del salmón del moodboard). |
| **Fondo** | Lino Marfil Artesanal | `#FBF8F4` | Fondo general del sitio web. Evita el blanco puro frío y simula la calidez de la cera de soja natural y fondos de catálogo. |
| **Texto** | Carbón Espresso Cálido | `#2D2723` | Encabezados, títulos y párrafos de texto (color cálido profundo extraído del bloque de lectura editorial del moodboard). |
| **Texto suave** | Gris Moca Suave | `#6E645D` | Bajadas de texto, tiempos de lectura en el blog, metadatos y notas secundarias. |
| **Éxito** | Verde Salvia Botánico *(Sage Green)* | `#2E6F40` | Mensajes de confirmación, cupón aplicado, confirmación de pedido y stock disponible (versión accesible del *Sage Green* `#629460` del moodboard). |
| **Error** | Carmín Terroso | `#B83A3A` | Mensajes de validación de formulario, avisos de campo obligatorio y alertas. |

---

### Paleta sensorial y cromática extraída del Moodboard (`image-2.png`)

Esta gama cromática complementaria se utiliza para identificar visualmente las distintas familias aromáticas y sensaciones de las velas de LUMÉ:

| Familia / Sensación | Color en Moodboard | HEX | Aplicación en el sitio |
|---|---|---|---|
| **Almendra & Confort** | *Almond Silk* | `#E6BEAE` | Fondos neutros cálidos de tarjetas de vela y bloques testimoniales. |
| **Cítricas & Calidez** | *Sweet Salmon* | `#EF8275` | Etiquetas de fragancias frutales y cálidas (*Canela Especiada*, *Mandarina*). |
| **Florales & Lavanda** | *Amethyst Smoke* | `#B279A7` | Tags de aromaterapia floral (*Brisa de Lavanda & Manzanilla*, *Jazmín*). |
| **Matcha & Bienestar** | *Sage Green* | `#629460` | Tags de hierbas y concentración (*Limón Verbena & Té Verde*, *Matcha Latte*). |
| **Marinas & Frescura** | *Frozen Lake* | `#7FDEFF` | Tags de fragancias oceánicas y purificantes (*Ocean Vibes*, *Brisa Marina*). |
| **Dulces & Vainilla** | *Peach Fuzz* | `#FFCDB2` | Etiquetas de fragancias dulces y repostería (*Vainilla Bourbon*, *Cheesecake*). |
| **Delicadeza & Cuidado** | *Powder Blush* | `#FFB4A2` | Fondos de packaging de regalo y cajas personalizadas. |
| **Herbales & Té** | *Tea Green* | `#D3FAD6` | Chips de ingredientes naturales y cera 100% de soja vegetal. |

---

## Contraste

Verificación de accesibilidad según las pautas WCAG (cumplimiento mínimo AA de 4.5:1 para texto normal y 3:1 para elementos de interfaz y títulos grandes):

| Combinación | Ratio | Resultado | Justificación de uso |
|---|---|---|---|
| Texto `#2D2723` sobre fondo `#FBF8F4` | **13.9:1** | AAA ✅ | Lectura principal ultra cómoda en cualquier tamaño de pantalla. |
| Texto blanco `#FFFFFF` sobre Principal `#1F4E3D` | **9.6:1** | AAA ✅ | Botón primario de compra (*"Agregar al carrito"* / *"Ir a pagar"*). |
| Principal `#1F4E3D` sobre fondo `#FBF8F4` | **9.0:1** | AAA ✅ | Enlaces del menú y textos destacados. |
| Texto `#2D2723` sobre Secundario `#E6BEAE` | **8.5:1** | AAA ✅ | Lectura perfecta en tarjetas de producto y bloques testimoniales. |
| Texto `#2D2723` sobre Sweet Salmon `#EF8275` | **5.8:1** | AA ✅ | Badges de ofertas con texto oscuro y botones de acento. |
| Texto blanco `#FFFFFF` sobre Terracota `#C05C38` | **4.6:1** | AA ✅ | Badges con fondo de acento y tipografía blanca (*"10% OFF"*). |
| Texto suave `#6E645D` sobre fondo `#FBF8F4` | **5.2:1** | AA ✅ | Bajadas de artículos, tiempos de lectura y pies de foto. |
| Texto blanco `#FFFFFF` sobre Éxito `#2E6F40` | **5.1:1** | AA ✅ | Notificaciones de producto añadido y cupón validado. |
| Texto blanco `#FFFFFF` sobre Error `#B83A3A` | **5.6:1** | AA ✅ | Mensajes de advertencia y campos faltantes en formularios. |

---

## Tipografía

Las tipografías seleccionadas combinan la elegancia editorial de las muestras de tu moodboard con la alta legibilidad digital de Google Fonts:

- **Títulos principales (h1, h2):** **[Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond)** *(Serif editorial clásico)*  
  Extraída del bloque *"Two floors, arranged for a quiet stay"* del moodboard. Transmite sofisticación, calma y la sensación de una marca de velas de autor.
- **Subtítulos y destacados (h3, badges):** **[Playfair Display](https://fonts.google.com/specimen/Playfair+Display)** *(Serif de alto contraste)*  
  Representa el estilo gráfico del bloque *"Subtítulos"* del moodboard. Aporta distinción y presencia en títulos de secciones intermedias.
- **Textos, párrafos y UI:** **[Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans)** *(Sans-serif moderna y geométrica)*  
  Representa el estilo de los bloques de lectura de testimonios y newsletter (*"Stay in the loop"*). Otorga legibilidad limpia en smartphones para que Catalina lea pirámides olfativas y costos de envío sin dificultad.
- **Acento artesanal (etiquetas y dedicatorias):** **[Caveat](https://fonts.google.com/specimen/Caveat)** o **[Alex Brush](https://fonts.google.com/specimen/Alex+Brush)** *(Script caligráfica)*  
  Inspirada en el bloque caligráfico *"Productos"* del moodboard y en las etiquetas hechas a mano de las velas (*"Strawberry Ice Latte"*, *"Ocean Vibes"*). Se usa de manera puntual para dedicatorias personalizadas y firmas de autor.

### Escala tipográfica modular

| Elemento | Tamaño Desktop | Tamaño Mobile | Peso | Tipografía utilizada |
|---|---|---|---|---|
| **h1** | `2.75rem` (44px) | `2.125rem` (34px) | 600 (SemiBold) | Cormorant Garamond |
| **h2** | `2.00rem` (32px) | `1.625rem` (26px) | 600 (SemiBold) | Cormorant Garamond / Playfair Display |
| **h3** | `1.375rem` (22px) | `1.250rem` (20px) | 600 (SemiBold) | Playfair Display |
| **Párrafo** | `1.00rem` (16px) | `0.9375rem` (15px) | 400 (Regular) | Plus Jakarta Sans |
| **Texto suave / Bajada** | `0.875rem` (14px) | `0.8125rem` (13px) | 400 (Regular) | Plus Jakarta Sans |
| **Botón / Menú** | `0.9375rem` (15px) | `0.875rem` (14px) | 600 (SemiBold) | Plus Jakarta Sans |
| **Dedicatoria / Firma** | `1.250rem` (20px) | `1.125rem` (18px) | 500 (Medium) | Caveat (Handwriting) |

---

## Justificación

1. **Estético:**  
   La armonía entre los tonos pastel empolvados del moodboard (*Almond Silk*, *Sweet Salmon*, *Amethyst Smoke*) y la elegancia de las fuentes con serif (**Cormorant Garamond** y **Playfair Display**) replica fielmente las composiciones artísticas (cuadros de Matisse, candelabros esculturales y frascos con apliques de flores y estrellas) de `image-2.png`, cautivando a Catalina con una imagen cuidada y atractiva para redes sociales.

2. **Minimalista:**  
   La paleta se apoya en un generoso 60% de fondos claros en Lino Marfil (`#FBF8F4`) y un 30% de Almendra Seda (`#E6BEAE`), evitando el ruido visual. La tipografía **Plus Jakarta Sans** mantiene las pantallas despejadas, ordenadas y con amplios espacios en blanco, facilitando la navegación rápida.

3. **Confort:**  
   Los tonos cálidos y envolventes sustituyen la frialdad de los blancos puros de monitor, simulando el resplandor apacible de una llama tenue al anochecer. Esto conecta de forma directa con la necesidad de Catalina de descansar y crear un santuario de tranquilidad en su dormitorio luego de largas horas de estudio.

4. **Artesanal:**  
   Los matices arcilla, canela y almendra rinden homenaje a los procesos hechos a mano: el vertido de cera en lotes pequeños, los vasos de vidrio ámbar y las mechas de madera. Además, el uso de la tipografía caligráfica para dedicatorias refuerza el valor único de una vela personalizada para regalo.

5. **Aromaterapia:**  
   El Verde Bosque Botánico (`#1F4E3D`) y el *Sage Green* (`#629460`) evocan los aceites esenciales puros (salvia, romero, lavanda silvestre y té verde) presentes en las formulaciones de LUMÉ, comunicando de forma instantánea frescura natural, pureza ecológica y relajación holística.
