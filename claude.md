# Bellota de Oro

# Bellota de Oro

## Descripción del proyecto

Rediseño de la web de **La Bellota de Oro**, restaurante ubicado en **Paracuellos de Jarama**.  
La web actual está en `clienteoriginal.html` (exportada de WordPress). El objetivo es crear una versión nueva en HTML/CSS/JS puro, sin WordPress.

**Web original:** http://www.labellotadeoro.es

## Stack tecnológico

- HTML5, CSS3, JavaScript vanilla
- Sin frameworks ni CMS (reemplazando WordPress)

## Estructura del proyecto

- `clienteoriginal.html` — código de la web actual del cliente (solo referencia, no modificar)
- `la-bellota-de-oro_logo_contor-300x212.png` — logo del cliente
- `index.html` — nueva web (por crear)

## Contenido del sitio

- **Slider/Hero:** 8 imágenes de tipo DSC0XXX-2000x925.jpg (alojadas en el servidor del cliente)
- **Secciones:** Bienvenida, Reservas, Carta, Mapa (Google Maps)
- **Fuente:** Droid Serif (Google Fonts)
- **Idioma:** Español

## Instrucciones para Claude

- El archivo `clienteoriginal.html` es solo de referencia, nunca modificarlo
- Las imágenes del slider están en `http://www.labellotadeoro.es/wp-content/uploads/`
- Mantener el espíritu visual del original pero modernizando el diseño
# Bellota de Oro

## Descripción del proyecto

Web corporativa para Bellota de Oro, restaurante en Paracuellos de Jarama.

El objetivo del proyecto es rediseñar por completo la presencia online del restaurante para transmitir una imagen más actual, cuidada y profesional, mejorar la conversión a reservas/contacto, facilitar el acceso a la carta y reforzar el posicionamiento local.

La web debe reflejar los principales valores del negocio:
- restaurante de referencia en Paracuellos de Jarama
- ambiente cercano y de encuentro
- especialidad en tapas, raciones, ibéricos y cocina española
- posibilidad de celebraciones y eventos
- importancia de la terraza, la experiencia en local y la carta

También debe contemplarse una fase de saneamiento de contenidos heredados del sitio anterior, ya que existen páginas indexadas no alineadas con la marca y el negocio.

## Stack tecnológico

Stack recomendado:
- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui para componentes base
- Framer Motion para microanimaciones sutiles
- CMS ligero o contenido gestionado vía Markdown/JSON mientras no haya backend
- Formularios conectados a email o servicio externo para reservas/contacto
- SEO técnico con metadatos, Open Graph, schema.org y sitemap

Si se prioriza simplicidad extrema:
- Next.js + React + Tailwind
- contenido estático bien estructurado
- despliegue en Vercel

## Estructura del proyecto

Estructura sugerida:

/app
  /(site)
    /page.tsx                  # Home
    /carta/page.tsx            # Carta o menú
    /reservas/page.tsx         # Reserva o contacto principal
    /celebraciones/page.tsx    # Eventos, grupos y celebraciones
    /contacto/page.tsx         # Dirección, mapa, teléfono, horario
    /galeria/page.tsx          # Fotos del local, platos y terraza
  /layout.tsx
  /globals.css

/components
  /layout
    Header.tsx
    Footer.tsx
    Nav.tsx
  /sections
    Hero.tsx
    AboutSection.tsx
    FeaturedDishes.tsx
    Testimonials.tsx
    CTASection.tsx
    ContactSection.tsx
    EventsSection.tsx
  /ui
    Button.tsx
    Card.tsx
    Badge.tsx
    SectionTitle.tsx

/content
  site.json                    # Datos globales del restaurante
  home.json                    # Copies de portada
  carta.json                   # Categorías destacadas de carta
  celebraciones.json           # Información de eventos
  seo.json                     # Metadatos SEO base

/lib
  seo.ts
  utils.ts
  constants.ts

/public
  /images
    /home
    /carta
    /local
    /terraza
    /events
  /icons

## Instrucciones para Claude

### Objetivo principal
Diseñar una web premium pero cercana para un restaurante local. La prioridad no es “hacer una web moderna” sin más, sino aumentar confianza, apetito visual y facilidad de contacto/reserva.

### Principios de diseño
- estética elegante, cálida y gastronómica
- aspecto premium sin resultar pretencioso
- diseño limpio, muy visual y fácil de escanear
- sensación local y auténtica, no de cadena genérica
- mobile-first
- foco en conversión

### Qué debe incluir la web
La nueva web debería incluir como mínimo:
- portada con propuesta de valor clara
- CTA visibles a reservar, llamar o contactar
- carta resumida o visualmente destacada
- sección de celebraciones / grupos / eventos
- galería de imágenes potente
- horario, dirección, teléfono y mapa
- enlaces a redes sociales
- bloque de testimonios o reseñas si procede
- FAQs si ayudan a reservas, grupos o aparcamiento
- SEO local bien trabajado

### Tono de marca
- cercano
- apetecible
- elegante
- claro
- sin frases vacías ni lenguaje demasiado corporativo

### Copywriting
Claude debe proponer textos en español de España.
Evitar clichés como:
- “una experiencia única e inolvidable”
- “fusión de sabores”
- “pasión por la gastronomía” si no aporta nada

Priorizar textos concretos y útiles:
- qué se come
- dónde está
- por qué ir
- cómo reservar
- si sirve para grupos o celebraciones

### SEO y contenido
Tener muy en cuenta:
- SEO local para Paracuellos de Jarama
- estructura clara de headings
- metadatos por página
- textos orientados a intención de búsqueda local
- limpieza de URLs heredadas irrelevantes
- evitar arrastrar contenido antiguo del WordPress previo

### UX
Claude debe priorizar:
- navegación simple
- accesos rápidos a carta, reservas y contacto
- botones de llamar y reservar visibles en móvil
- carga rápida
- contraste correcto y buena legibilidad
- imágenes bien optimizadas

### Estilo visual
Referencias visuales deseadas:
- fondos claros o cálidos
- combinación de tonos crema, blanco roto, negro suave y acentos burdeos/dorados/verde oliva si encaja
- tipografía elegante para titulares y muy legible en texto
- fotografías grandes y protagonistas
- microanimaciones suaves, nunca excesivas

### Convenciones de desarrollo
- usar componentes reutilizables
- mantener separada la capa de contenido
- evitar lógica innecesaria
- priorizar accesibilidad semántica
- no introducir dependencias pesadas sin motivo
- comentarios solo cuando aporten valor real
- mantener el código limpio y fácil de escalar

### Páginas prioritarias
1. Home
2. Carta
3. Celebraciones
4. Contacto / Reservas
5. Galería

### Qué evitar
- sliders pesados
- autoplay invasivo
- textos genéricos largos
- demasiados efectos visuales
- layouts recargados
- estética de plantilla genérica
- heredar estructura o copy del sitio antiguo sin revisión crítica

### Nota importante sobre el proyecto
La web actual parece haber acumulado contenido indexado que no corresponde con la actividad del restaurante. Claude debe asumir que el rediseño incluye:
- revisión de arquitectura de información
- propuesta de limpieza de rutas
- propuesta de redirecciones
- revisión SEO y reputacional del dominio

## Información importante del negocio

- horario actual:Nuestro horario
Lunes
Cerrado
Martes
12:00 a 23:30
Miércoles
12:00 a 23:30
Jueves
12:00 a 23:30
Viernes
12:00 a 01:00
Sábado
12:00 a 01:00
Domingo
12:00 a 23:30
- teléfono principal y WhatsApp:  653246613
E-mail: contacto@labellotadeoro.es
dirección: Centro Comercial Miramadrid
Avda. Juan Pablo II, nº 26
Paracuellos de Jarama
28860 Madrid