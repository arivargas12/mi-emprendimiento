# Spec de desarrollo — LUMÉ

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

---

## 1. Estructura de archivos

```text
lume-velas/
├── index.html                  ← landing page principal
├── tienda.html                 ← catálogo general y filtros de productos
├── producto.html               ← ficha de producto, pirámide olfativa y compra
├── carrito.html                ← carrito de compras y estimador de despacho
├── blog.html                   ← listado de artículos y categorías de bienestar
├── articulo.html               ← lectura de artículo, producto recomendado y comentarios
├── nosotros.html               ← historia artesanal y valores de LUMÉ
├── contacto.html               ← formulario de contacto y canales de atención
├── faq.html                    ← preguntas frecuentes (envíos, cuidados y stock)
├── terminos.html               ← términos y condiciones del servicio
├── privacidad.html             ← políticas de privacidad y protección de datos
├── 404.html                    ← página de error 404 con enlace de retorno
├── DESIGN.md                   ← design system del proyecto (tokens y reglas de diseño)
├── css/
│   └── styles.css              ← hoja de estilos unificada con variables :root y componentes
├── js/
│   └── main.js                 ← interactividad mínima (filtros en tienda, carrito y menú mobile)
├── img/
│   ├── productos/              ← fotografías de velas (lavanda, bergamota, cedro, etc.)
│   ├── blog/                   ← imágenes de artículos y rituales de bienestar
│   └── icons/                  ← favicon y recursos gráficos svg
├── stitch/                     ← código exportado de Stitch (solo referencia visual)
└── docs/                       ← documentación y especificaciones del proyecto
```

---

## 2. Páginas y navegación

### Elementos globales de navegación
- **Navbar (presente en todas las páginas):**
  - Logotipo "LUMÉ" → `index.html`
  - Enlaces de navegación: "Tienda" (`tienda.html`), "Blog" (`blog.html`), "Nosotros" (`nosotros.html`), "Contacto" (`contacto.html`).
  - Barra de búsqueda interactiva / ícono de búsqueda rápida.
  - Ícono de carrito de compras con contador de artículos → `carrito.html`.
  - Botón de menú hamburguesa en mobile que despliega panel lateral accesible con los mismos enlaces.
- **Footer (presente en todas las páginas):**
  - Enlaces secundarios: "Nosotros" (`nosotros.html`), "Contacto" (`contacto.html`), "Preguntas frecuentes" (`faq.html`), "Términos y condiciones" (`terminos.html`), "Política de privacidad" (`privacidad.html`).
  - Redes sociales: Instagram (`https://instagram.com/lume.velas`), WhatsApp (`https://wa.me/569XXXXXXXX`).
  - Sello artesanal: "Hecho a mano en Chile · Cera 100% de soja natural".

### Tabla de navegación entre páginas

| Desde | Elemento | Lleva a | Comportamiento |
|---|---|---|---|
| `index.html` | Logotipo "LUMÉ" en navbar | `index.html` | Carga o recarga la página de inicio |
| `index.html` | Enlace "Tienda" en navbar | `tienda.html` | Redirige al catálogo de la tienda |
| `index.html` | Enlace "Blog" en navbar | `blog.html` | Redirige a la sección editorial de blog |
| `index.html` | Ícono de carrito en navbar | `carrito.html` | Redirige a la vista del carrito |
| `index.html` | Botón "COMPRAR AHORA" en hero | `tienda.html` | Lleva a la tienda para explorar productos |
| `index.html` | Botón "Ver producto" en card destacada | `producto.html` | Abre la ficha de la vela seleccionada |
| `index.html` | Botón "Quiero la guía" en captación de leads | Formulario en `index.html` | Valida el email y muestra confirmación con 10% OFF |
| `tienda.html` | Buscador de texto | Catálogo en `tienda.html` | Filtra productos en tiempo real por término o aroma |
| `tienda.html` | Chips de categoría (*Todos, Florales, Cítricos...*) | Catálogo en `tienda.html` | Filtra productos por familia olfativa sin recargar |
| `tienda.html` | Tarjetas de kits (*Kit Relax, Kit Cítrico...*) | `producto.html` | Conduce al detalle del set con descuento aplicado |
| `tienda.html` | Botón "ver producto" de cada `card-product` | `producto.html` | Abre la ficha detallada del producto |
| `tienda.html` | Ícono de favoritos (corazón) en `card-product` | Estado local en `tienda.html` | Marca o desmarca producto en lista de favoritos |
| `producto.html` | Migas de pan "Tienda > Florales" | `tienda.html` | Regresa al catálogo filtrado por la categoría |
| `producto.html` | Selector de formato (*100g, 200g, Melt*) | Ficha en `producto.html` | Actualiza precio y variante seleccionada |
| `producto.html` | Botón "Agregar al carrito" | `carrito.html` | Añade la vela seleccionada y abre el carrito |
| `producto.html` | Botón "Consultar por WhatsApp" | `https://wa.me/569XXXXXXXX` | Abre chat de WhatsApp para asesoría rápida |
| `carrito.html` | Botón "Seguir comprando" | `tienda.html` | Regresa a la tienda para seguir vitrineando |
| `carrito.html` | Controles de cantidad (+ / -) | `carrito.html` | Actualiza la cantidad y recalcula el subtotal |
| `carrito.html` | Botón papelera (eliminar ítem) | `carrito.html` | Elimina el ítem de la lista y actualiza el total |
| `carrito.html` | Botón "Calcular" comuna de despacho | `carrito.html` | Calcula costo de envío y actualiza el total final |
| `carrito.html` | Botón "Ir a pagar" | Pasarela de checkout | Avanza al pago como invitado (Webpay / Mercado Pago) |
| `blog.html` | Chips de categoría (*Guías, Aromaterapia...*) | `blog.html` | Filtra los artículos visibles por temática |
| `blog.html` | Enlace "Leer artículo" en `card-blog` | `articulo.html` | Abre la lectura del artículo seleccionado |
| `articulo.html` | Migas de pan "Blog > Guías" | `blog.html` | Regresa al listado de artículos del blog |
| `articulo.html` | Tarjeta de producto recomendado ("Ver producto") | `producto.html` | Abre la ficha de la vela relacionada al artículo |
| `articulo.html` | Botones para compartir en WhatsApp / Instagram | Enlaces externos de compartir | Abre diálogo de WhatsApp o Instagram |
| `articulo.html` | Botón "Enviar" en formulario de comentarios | `articulo.html` | Publica el comentario en la lista interactiva |
| `404.html` | Botón "Volver al inicio" | `index.html` | Regresa a la landing page principal |

---

## 3. Estructura semántica

### 3.1. `index.html` (Landing)

```html
<header>
  <nav class="navbar">
    <a href="index.html" class="navbar-logo">LUMÉ</a>
    <ul class="navbar-links">
      <li><a href="tienda.html">Tienda</a></li>
      <li><a href="blog.html">Blog</a></li>
      <li><a href="nosotros.html">Nosotros</a></li>
      <li><a href="contacto.html">Contacto</a></li>
    </ul>
    <div class="navbar-actions">
      <button class="search-trigger" aria-label="Buscar">🔍</button>
      <a href="carrito.html" class="cart-link" aria-label="Carrito de compras">🛒 <span class="cart-count">2</span></a>
      <button class="menu-toggle" aria-label="Abrir menú">☰</button>
    </div>
  </nav>
</header>
<main>
  <section class="hero-banner" aria-labelledby="hero-title">
    <div class="hero-content">
      <span class="tag-category">COLECCIÓN BOTÁNICA</span>
      <h1 id="hero-title">Vela Lavanda & Vainilla</h1>
      <p class="hero-description">Fragancia relajante con aceites esenciales naturales.</p>
      <a href="tienda.html" class="btn-primary">COMPRAR AHORA</a>
    </div>
    <figure class="hero-media">
      <img src="img/productos/vela-lavanda-hero.jpg" alt="Vela artesanal de lavanda y vainilla encendida en frasco ámbar">
    </figure>
  </section>
  <section class="featured-section" aria-labelledby="featured-title">
    <header class="section-header">
      <h2 id="featured-title">Velas que iluminan tu espacio</h2>
      <p>Cera 100% de soya y aromas naturales para transformar tu hogar.</p>
    </header>
    <div class="product-grid">
      <article class="card-product">
        <figure class="product-thumb">
          <img src="img/productos/vela-lavanda-200g.jpg" alt="Vela Lavanda 200g">
          <button class="fav-btn" aria-label="Guardar en favoritos">♡</button>
        </figure>
        <div class="product-info">
          <span class="product-scent-tag">Floral</span>
          <h3 class="product-title">Vela Lavanda 200g</h3>
          <p class="product-price">$14.990</p>
          <a href="producto.html" class="btn-secondary">Ver producto</a>
        </div>
      </article>
      <article class="card-product">
        <figure class="product-thumb">
          <img src="img/productos/vela-bergamota-200g.jpg" alt="Vela Bergamota 200g">
          <button class="fav-btn" aria-label="Guardar en favoritos">♡</button>
        </figure>
        <div class="product-info">
          <span class="product-scent-tag">Cítrica</span>
          <h3 class="product-title">Vela Bergamota 200g</h3>
          <p class="product-price">$15.990</p>
          <a href="producto.html" class="btn-secondary">Ver producto</a>
        </div>
      </article>
    </div>
  </section>
  <section class="lead-capture" aria-labelledby="lead-title">
    <div class="lead-content">
      <h2 id="lead-title">Guía gratis + 10% OFF</h2>
      <p>Suscríbete para recibir un 10% de descuento en tu primera compra y nuestra guía digital de aromaterapia para el hogar.</p>
      <form class="lead-form">
        <label for="lead-email" class="visually-hidden">Correo electrónico</label>
        <input id="lead-email" type="email" placeholder="Tu@correo.cl" class="input-field" required>
        <button type="submit" class="btn-accent">Quiero la guía</button>
      </form>
    </div>
  </section>
</main>
<footer class="footer">
  <div class="footer-container">
    <div class="footer-brand">
      <span class="footer-logo">LUMÉ</span>
      <p>Velas aromáticas artesanales de cera 100% de soya. Hecho a mano en Chile.</p>
    </div>
    <nav class="footer-nav" aria-label="Enlaces institucionales">
      <ul>
        <li><a href="tienda.html">Tienda</a></li>
        <li><a href="blog.html">Blog</a></li>
        <li><a href="nosotros.html">Nosotros</a></li>
        <li><a href="contacto.html">Contacto</a></li>
        <li><a href="faq.html">Preguntas frecuentes</a></li>
        <li><a href="terminos.html">Términos y condiciones</a></li>
        <li><a href="privacidad.html">Privacidad</a></li>
      </ul>
    </nav>
  </div>
</footer>
```

### 3.2. `tienda.html` (Tienda / Catálogo)

```html
<header>
  <!-- navbar global -->
</header>
<main class="store-page">
  <header class="store-header">
    <h1>Tienda</h1>
    <form class="search-form" role="search">
      <label for="store-search" class="visually-hidden">Buscar velas, aromas o notas</label>
      <input id="store-search" type="search" placeholder="Buscar velas, aromas o notas..." class="input-field">
      <button type="submit" aria-label="Buscar">🔍</button>
    </form>
    <nav class="category-tabs" aria-label="Filtrar por categoría">
      <ul class="tag-list">
        <li><button class="tag-category active">Todos</button></li>
        <li><button class="tag-category">Florales</button></li>
        <li><button class="tag-category">Cítricos</button></li>
        <li><button class="tag-category">Amaderados</button></li>
        <li><button class="tag-category">Dulces</button></li>
      </ul>
    </nav>
  </header>
  <section class="promo-kits" aria-label="Kits de velas con descuento">
    <div class="kits-grid">
      <article class="card-kit">
        <span class="tag-offer">Ahorra $2.500</span>
        <h3>Kit Relax</h3>
        <p>Vela Lavanda + Manzanilla</p>
        <a href="producto.html" class="btn-secondary">Ver kit</a>
      </article>
      <article class="card-kit">
        <span class="tag-offer">Ahorra $1.900</span>
        <h3>Kit Cítrico</h3>
        <p>Vela Bergamota + Mandarina</p>
        <a href="producto.html" class="btn-secondary">Ver kit</a>
      </article>
      <article class="card-kit">
        <span class="tag-offer">Ahorra $3.200</span>
        <h3>Kit Intenso</h3>
        <p>Vela Cedro + Vainilla Bourbon</p>
        <a href="producto.html" class="btn-secondary">Ver kit</a>
      </article>
    </div>
  </section>
  <div class="store-layout">
    <aside class="store-sidebar" aria-label="Filtros de catálogo">
      <form class="filter-form">
        <fieldset class="filter-group">
          <legend>TIPO DE AROMAS</legend>
          <label><input type="checkbox" name="aroma" value="florales"> Florales</label>
          <label><input type="checkbox" name="aroma" value="citricas"> Cítricas</label>
          <label><input type="checkbox" name="aroma" value="amaderadas"> Amaderadas</label>
        </fieldset>
        <fieldset class="filter-group">
          <legend>PRECIO</legend>
          <input type="range" min="10000" max="35000" step="1000" value="35000" class="range-slider">
          <span class="price-range-display">$10.000 — $35.000</span>
        </fieldset>
      </form>
    </aside>
    <section class="catalog-content" aria-label="Catálogo de productos">
      <div class="product-grid">
        <!-- 6 tarjetas card-product -->
        <article class="card-product">
          <figure class="product-thumb">
            <img src="img/productos/vela-lavanda-200g.jpg" alt="Vela Lavanda 200g">
            <button class="fav-btn" aria-label="Favorito">♡</button>
          </figure>
          <div class="product-info">
            <span class="product-scent-tag">Floral</span>
            <h2 class="product-title">Vela Lavanda 200g</h2>
            <p class="product-price">$14.990</p>
            <a href="producto.html" class="btn-secondary">ver producto</a>
          </div>
        </article>
        <!-- card-product 2: Bergamota, 3: Canela, 4: Jazmín, 5: Cedro, 6: Vainilla -->
      </div>
    </section>
  </div>
</main>
<footer class="footer">
  <!-- footer global -->
</footer>
```

### 3.3. `producto.html` (Ficha de producto)

```html
<header>
  <!-- navbar global -->
</header>
<main class="product-page">
  <nav class="breadcrumbs" aria-label="Ruta de navegación">
    <ol>
      <li><a href="tienda.html">Tienda</a></li>
      <li><a href="tienda.html">Florales</a></li>
      <li aria-current="page">Vela Lavanda & Vainilla</li>
    </ol>
  </nav>
  <article class="product-detail-layout">
    <section class="product-gallery" aria-label="Galería del producto">
      <figure class="main-image-container">
        <img id="main-product-img" src="img/productos/vela-lavanda-detalle.jpg" alt="Vela Lavanda & Vainilla en ambiente relajante">
      </figure>
      <div class="thumbnail-strip">
        <button class="thumbnail-btn active"><img src="img/productos/thumb-1.jpg" alt="Mecha de algodón"></button>
        <button class="thumbnail-btn"><img src="img/productos/thumb-2.jpg" alt="Etiqueta botánica"></button>
        <button class="thumbnail-btn"><img src="img/productos/thumb-3.jpg" alt="Envase de vidrio ámbar"></button>
      </div>
    </section>
    <section class="product-info-panel">
      <span class="tag-category">Florales</span>
      <h1 class="product-name">Vela Lavanda & Vainilla</h1>
      <p class="product-price">$14.990</p>
      <p class="product-description">Notas relajantes de flor de lavanda silvestre y vainilla dulce con cera 100% de soya.</p>
      <section class="scent-pyramid-block" aria-labelledby="pyramid-title">
        <h2 id="pyramid-title">Pirámide olfativa</h2>
        <ul class="pyramid-notes">
          <li><strong>Salida:</strong> Lavanda silvestre</li>
          <li><strong>Corazón:</strong> Flores blancas y manzanilla</li>
          <li><strong>Fondo:</strong> Vainilla dulce cálida</li>
        </ul>
        <p class="scent-intensity">Intensidad de difusión: <span>Media</span></p>
      </section>
      <form class="product-buy-form">
        <fieldset class="format-options">
          <legend>Formato:</legend>
          <label class="format-pill"><input type="radio" name="formato" value="100g"> 100g</label>
          <label class="format-pill active"><input type="radio" name="formato" value="200g" checked> 200g</label>
          <label class="format-pill"><input type="radio" name="formato" value="melt"> Melt</label>
        </fieldset>
        <button type="submit" class="btn-primary">Agregar al carrito</button>
        <a href="https://wa.me/569XXXXXXXX" class="btn-secondary btn-whatsapp">Consultar por WhatsApp</a>
      </form>
    </section>
  </article>
</main>
<footer class="footer">
  <!-- footer global -->
</footer>
```

### 3.4. `carrito.html` (Carrito de compras)

```html
<header>
  <!-- navbar global -->
</header>
<main class="cart-layout">
  <section class="cart-items-wrapper" aria-labelledby="cart-heading">
    <h1 id="cart-heading">Tu carrito</h1>
    <ul class="cart-list">
      <li class="cart-item-card">
        <img src="img/productos/vela-lavanda-200g.jpg" alt="Vela Lavanda & Vainilla (200g)" class="item-img">
        <div class="item-info">
          <h2 class="item-title">Vela Lavanda & Vainilla (200g)</h2>
          <p class="item-price">Precio: $14.990</p>
        </div>
        <div class="item-quantity">
          <label for="qty-1" class="visually-hidden">Cantidad</label>
          <select id="qty-1" class="qty-select">
            <option value="1" selected>cantidad: 1</option>
            <option value="2">cantidad: 2</option>
            <option value="3">cantidad: 3</option>
          </select>
        </div>
        <button class="item-remove-btn" aria-label="Eliminar producto">🗑</button>
      </li>
      <li class="cart-item-card">
        <img src="img/productos/vela-bergamota-200g.jpg" alt="Vela Bergamota & Cedro (200g)" class="item-img">
        <div class="item-info">
          <h2 class="item-title">Vela Bergamota & Cedro (200g)</h2>
          <p class="item-price">Precio: $15.990</p>
        </div>
        <div class="item-quantity">
          <label for="qty-2" class="visually-hidden">Cantidad</label>
          <select id="qty-2" class="qty-select">
            <option value="1" selected>cantidad: 1</option>
            <option value="2">cantidad: 2</option>
            <option value="3">cantidad: 3</option>
          </select>
        </div>
        <button class="item-remove-btn" aria-label="Eliminar producto">🗑</button>
      </li>
    </ul>
    <a href="tienda.html" class="btn-secondary">Seguir comprando</a>
  </section>
  <aside class="cart-summary-wrapper" aria-labelledby="summary-heading">
    <div class="cart-summary">
      <h2 id="summary-heading">Resumen del Pedido</h2>
      <div class="summary-line">
        <span>Subtotal:</span>
        <span class="subtotal-val">$30.980</span>
      </div>
      <form class="shipping-calculator">
        <label for="shipping-comuna">Calcular despacho:</label>
        <div class="shipping-inputs">
          <input id="shipping-comuna" type="text" placeholder="Tu comuna..." class="input-field">
          <button type="button" class="btn-secondary">Calcular</button>
        </div>
      </form>
      <div class="summary-line">
        <span>Despacho:</span>
        <span class="shipping-val">$3.500</span>
      </div>
      <div class="summary-line total-line">
        <span>Total:</span>
        <strong class="total-val">$34.480</strong>
      </div>
      <a href="checkout.html" class="btn-primary btn-checkout">Ir a pagar</a>
    </div>
  </aside>
</main>
<footer class="footer">
  <!-- footer global -->
</footer>
```

### 3.5. `blog.html` (Blog)

```html
<header>
  <!-- navbar global -->
</header>
<main class="blog-page">
  <header class="blog-header">
    <h1>NUESTRO BLOG</h1>
    <p class="blog-subtitle">Rituales de bienestar, aromaterapia y guías para crear un refugio de calma.</p>
    <nav class="blog-category-nav" aria-label="Filtrar temas de blog">
      <ul class="tag-list">
        <li><button class="tag-category active">Todos</button></li>
        <li><button class="tag-category">Guías</button></li>
        <li><button class="tag-category">Aromaterapia</button></li>
        <li><button class="tag-category">Cuidado de velas</button></li>
      </ul>
    </nav>
  </header>
  <section class="blog-grid-section" aria-label="Artículos publicados">
    <div class="articles-grid">
      <article class="card-blog">
        <span class="article-meta">Aromaterapia • 5 min</span>
        <h3 class="article-category-sub">Aromaterapia para conciliar el sueño</h3>
        <h2 class="article-title"><a href="articulo.html">Descubre qué fragancias te ayudan a relajarte antes de dormir...</a></h2>
        <a href="articulo.html" class="btn-read-more">Leer artículo</a>
      </article>
      <article class="card-blog">
        <span class="article-meta">Guía • 4 min</span>
        <h3 class="article-category-sub">Cómo reutilizar tus frascos de vela</h3>
        <h2 class="article-title"><a href="articulo.html">Ideas creativas para darle una segunda vida a tus envases de vidrio...</a></h2>
        <a href="articulo.html" class="btn-read-more">Leer artículo</a>
      </article>
      <article class="card-blog">
        <span class="article-meta">Guía • 3 min</span>
        <h3 class="article-category-sub">El secreto del recorte de mecha</h3>
        <h2 class="article-title"><a href="articulo.html">Aprende los mejores tips para extender la vida útil de tus velas...</a></h2>
        <a href="articulo.html" class="btn-read-more">Leer artículo</a>
      </article>
      <article class="card-blog">
        <span class="article-meta">Cuidado • 3 min</span>
        <h3 class="article-category-sub">Beneficios de la cera de soya natural</h3>
        <h2 class="article-title"><a href="articulo.html">Por qué la cera de soya es ecológica, limpia y duradera...</a></h2>
        <a href="articulo.html" class="btn-read-more">Leer artículo</a>
      </article>
    </div>
  </section>
</main>
<footer class="footer">
  <!-- footer global -->
</footer>
```

### 3.6. `articulo.html` (Artículo y comentarios)

```html
<header>
  <!-- navbar global -->
</header>
<main class="article-single-page">
  <nav class="breadcrumbs" aria-label="Ruta de navegación">
    <ol>
      <li><a href="blog.html">Blog</a></li>
      <li><a href="blog.html">Guías</a></li>
      <li aria-current="page">El secreto del recorte de mecha</li>
    </ol>
  </nav>
  <article class="article-full-content">
    <header class="article-post-header">
      <span class="article-badge">Guía • Lectura de 3 min</span>
      <h1>El secreto del recorte de mecha para velas de soya</h1>
    </header>
    <figure class="featured-article-figure">
      <img src="img/blog/recorte-mecha-vela.jpg" alt="Vela de soya encendida junto a tijeras despabiladoras">
    </figure>
    <div class="article-body-text">
      <p>Cortar la mecha a 5mm antes de cada encendido evita que se genere humo negro y asegura una quema uniforme...</p>
      <p>Una mecha muy larga produce una llama alta e inestable que consume la cera demasiado rápido...</p>
      <aside class="inline-product-recommendation" aria-label="Producto recomendado">
        <img src="img/productos/vela-lavanda-thumb.jpg" alt="Miniatura Vela Lavanda">
        <div class="recommendation-content">
          <p>¿Buscas el aroma perfecto? Prueba nuestra Vela Lavanda 200g elaborada con mecha 100% de algodón.</p>
          <a href="producto.html" class="btn-secondary">Ver producto</a>
        </div>
      </aside>
    </div>
    <footer class="article-share-footer">
      <span>Compartir artículo:</span>
      <a href="https://api.whatsapp.com/send?text=..." class="btn-share">WhatsApp</a>
      <a href="https://instagram.com" class="btn-share">Instagram</a>
    </footer>
  </article>
  <section class="comments-block" aria-labelledby="comments-heading">
    <h2 id="comments-heading">Comentarios</h2>
    <form class="comment-submission-form">
      <label for="comment-body" class="visually-hidden">Escribe un comentario</label>
      <textarea id="comment-body" placeholder="Escribe un comentario..." class="input-field" rows="4" required></textarea>
      <button type="submit" class="btn-primary">Enviar</button>
    </form>
  </section>
</main>
<footer class="footer">
  <!-- footer global -->
</footer>
```

---

## 4. Organización del CSS

### 4.1. Variables en `:root` (Tokens de `DESIGN.md`)

```css
:root {
  /* Colores principales */
  --color-primary: #1F4E3D;
  --color-primary-hover: #173C2F;
  --color-primary-active: #122E24;
  --color-on-primary: #FFFFFF;

  --color-secondary: #E6BEAE;
  --color-secondary-hover: #DEC0B2;
  --color-on-secondary: #2D2723;

  --color-tertiary: #EF8275;
  --color-tertiary-strong: #B8512E;
  --color-tertiary-hover: #9E4322;
  --color-on-tertiary: #FFFFFF;

  --color-neutral: #FBF8F4;
  --color-surface: #FFFFFF;
  --color-surface-warm: #F4ECE4;
  --color-border: #E2D6CB;

  --color-on-surface: #2D2723;
  --color-on-surface-variant: #6E645D;

  --color-disabled: #E8E4DF;
  --color-on-disabled: #5C544E;

  --color-success: #2E6F40;
  --color-on-success: #FFFFFF;
  --color-error: #B83A3A;
  --color-on-error: #FFFFFF;

  /* Familias tipográficas */
  --font-display: 'Cormorant Garamond', Georgia, serif;
  --font-headline: 'Playfair Display', Georgia, serif;
  --font-body: 'Plus Jakarta Sans', system-ui, -apple-system, sans-serif;
  --font-script: 'Caveat', cursive;

  /* Escala tipográfica */
  --font-size-display: 44px;
  --line-height-display: 1.15;
  --font-size-headline-lg: 32px;
  --line-height-headline-lg: 1.2;
  --font-size-headline-md: 24px;
  --line-height-headline-md: 1.25;
  --font-size-title-md: 18px;
  --line-height-title-md: 1.3;
  --font-size-body-md: 16px;
  --line-height-body-md: 1.6;
  --font-size-body-sm: 14px;
  --line-height-body-sm: 1.5;
  --font-size-label-md: 15px;
  --font-size-label-sm: 13px;

  /* Escala de espaciado */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios de borde */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  /* Elevaciones y sombras */
  --shadow-card: 0 4px 12px rgba(45, 39, 35, 0.05);
  --shadow-hover: 0 8px 24px rgba(45, 39, 35, 0.08);
  --shadow-modal: 0 12px 32px rgba(45, 39, 35, 0.12);

  /* Layout y contenedor */
  --max-width-container: 1200px;
}
```

### 4.2. Convención de clases y nomenclatura
- Nomenclatura semántica en inglés con guiones (BEM ligero):
  - Componentes principales: `.navbar`, `.hero-banner`, `.card-product`, `.card-blog`, `.card-kit`, `.cart-summary`.
  - Botones y variantes: `.btn-primary`, `.btn-secondary`, `.btn-accent`, `.btn-disabled`.
  - Badges e insignias: `.tag-category`, `.tag-offer`, `.badge-scent`.
  - Formularios y entradas: `.input-field`, `.range-slider`, `.search-form`.
  - Estructuras y grillas: `.product-grid`, `.articles-grid`, `.store-layout`, `.cart-layout`.

### 4.3. Breakpoints y estrategia Mobile-First
- Se diseña primero para pantallas pequeñas (mobile-first) y se expande progresivamente con `min-width`:
  1. **Mobile (< 768px):** Diseño base en 1 columna, márgenes laterales de 16px (`--space-md`), navbar con menú colapsable (botón hamburguesa) y área táctil mínima de 44px.
  2. **Tablet (768px a 1023px):** `@media (min-width: 768px)` — catálogo en 2 columnas, márgenes laterales de 24px (`--space-lg`), espaciados verticales de 48px (`--space-2xl`).
  3. **Desktop (1024px en adelante):** `@media (min-width: 1024px)` — catálogo en 3 columnas con barra lateral fija de filtros, ficha de producto en 2 columnas paralelas, contenedor centrado a máximo 1200px y márgenes laterales de 32px (`--space-xl`).

---

## 5. Criterios de aceptación

### Navegación
- [ ] La barra de navegación (navbar) y el footer son idénticos y funcionales en todas las páginas del sitio.
- [ ] Se puede completar el flujo de compra sin enlaces rotos: `index.html` → `tienda.html` → `producto.html` → `carrito.html`.
- [ ] Se puede completar el flujo de contenido: `blog.html` → `articulo.html` → producto recomendado en `producto.html`.
- [ ] Las migas de pan (breadcrumbs) en `producto.html` y `articulo.html` conducen correctamente a sus secciones principales (`tienda.html` y `blog.html`).
- [ ] La página `404.html` incluye un botón operativo para volver al inicio (`index.html`).

### Funcionalidades
- [ ] En la landing (`index.html`), el formulario de captación valida correos y permite suscribirse para obtener el 10% de descuento.
- [ ] En la tienda (`tienda.html`), el buscador por texto filtra en tiempo real y los chips de categoría cambian las velas visibles.
- [ ] En la tienda (`tienda.html`), el filtro por familia olfativa y el slider de precio acotan los resultados del catálogo.
- [ ] En la ficha de producto (`producto.html`), se visualiza la pirámide olfativa (salida, corazón, fondo), la selección de formato (100g, 200g, Melt) y el botón para agregar al carrito.
- [ ] En el carrito (`carrito.html`), los controles numéricos permiten modificar cantidades o eliminar ítems, y el estimador de despacho por comuna actualiza el costo y total.
- [ ] En el artículo (`articulo.html`), funcionan los enlaces para compartir en WhatsApp e Instagram y el formulario permite publicar comentarios.

### Diseño
- [ ] Todos los colores, tipografías, radios y espaciados provienen estrictamente de las variables `:root`, coincidiendo con `DESIGN.md`.
- [ ] El fondo general de las páginas utiliza el color marfil neutro (`#FBF8F4`) y no blanco digital puro (`#FFFFFF`).
- [ ] El sitio está construido únicamente con HTML y CSS propios, sin TailwindCSS ni estilos crudos exportados de Stitch.
- [ ] El precio es visible en todas las tarjetas de producto (`card-product`) sin requerir interacción previa.
- [ ] Todos los botones (`btn-primary`, `btn-secondary`, `btn-accent`) y enlaces interactivos cuentan con estados `hover` y `active` diferenciados.

### Responsive
- [ ] En móvil (375px), el catálogo muestra 1 tarjeta por fila; en tablet (768px), 2; y en desktop (1024px+), 3.
- [ ] No existe scroll horizontal no deseado en ningún ancho de pantalla (verificado en 375px, 768px y 1200px).
- [ ] En pantallas móviles (<768px), el menú se contrae en un botón hamburguesa funcional que despliega la navegación.
- [ ] Todos los botones y campos interactivos en mobile cuentan con una altura táctil mínima de 44px para facilitar la pulsación.

### Accesibilidad y publicación
- [ ] Cada página HTML cuenta con un único encabezado principal `<h1>` con jerarquía secuencial (`h1` → `h2` → `h3`).
- [ ] Todas las imágenes (`<img>`) poseen un atributo `alt` descriptivo y significativo.
- [ ] Todos los campos de formulario (`<input>`, `<select>`, `<textarea>`) tienen `<label>` visible o accesible vía `aria-label`.
- [ ] La relación de contraste de color cumple con el estándar WCAG AA (mínimo 4.5:1 para texto normal).
- [ ] El repositorio está estructurado con rutas relativas para publicarse sin errores en GitHub Pages.
