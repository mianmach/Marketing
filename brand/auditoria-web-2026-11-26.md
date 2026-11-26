# Auditoría web — I Love You Barcelona

**Fecha:** 26 nov 2026 · **Sitio revisado:** www.iloveyoubarcelona.com (Squarespace)
**Base de comparación:** *The Call Sheet* (`brand/strategy-manual.html`) y el contexto de producto (`.agents/product-marketing.md`)
**Método:** 17 páginas descargadas (las del sitemap), capturas en escritorio (1440 px) y móvil (iPhone 13), revisión de títulos, metadatos, encabezados, textos, formularios y páginas legales.

> Tono de este documento: crítico a propósito. Lo bueno se dice al final de cada bloque, pero el foco está en lo que frena reservas.

---

## 0. Urgente (arreglar esta semana)

| # | Problema | Dónde | Por qué importa |
|---|----------|-------|-----------------|
| 0.1 | **Páginas legales en "Lorem ipsum"**: Privacy Policy, Refund Policy, Terms of Service y Accessibility Statement son texto de relleno de la plantilla. | `/privacy-policy`, `/refund-policy`, `/tos`, `/accessibility-policy` | Recogéis nombre, email y WhatsApp en el formulario: en España una política de privacidad real (RGPD) y un aviso legal (LSSI: titular, NIF, contacto) son obligatorios. Además **están en el sitemap**, así que Google puede indexar "Lorem ipsum" con vuestra marca. La única página legal real es la de cookies. |
| 0.2 | **No hay política de cancelación del anticipo del 50 %.** Se explica el cambio de fecha (3 días), pero no qué pasa si la pareja cancela. | `/services` | Es la primera duda de quien paga un anticipo por Bizum a alguien que no conoce. Y la "Refund Policy" es Lorem ipsum. |
| 0.3 | ✅ *Resuelto: la cuenta oficial es `@iloveyouarchives`; falta cambiarla en la tarjeta de Canva.* **Instagram equivocado (o al menos distinto al manual).** Todo el sitio enlaza a `@iloveyouarchives`; el manual y la tarjeta impresa dicen `@iloveyoutoobcn`. | Cabecera y pie de todas las páginas | Si la tarjeta lleva a una cuenta y la web a otra, se rompe la prueba social, que es vuestra principal arma de venta. Hay que decidir una y unificar. |
| 0.4 | **Títulos que desaparecen en escritorio.** El H1 de Servicios ("Every love story deserves to be seen") y el H2 de About ("We are Nuria & Miguel") se ven diminutos (≈6 px) en la esquina superior izquierda. En móvil sí se ven. | `/services`, `/about` (y sus versiones ES) | Fallo de maquetación del Fluid Engine en la vista de escritorio. Es lo primero que ve alguien que entra desde Google en ordenador. |
| 0.5 | **Hueco vacío enorme en la home (escritorio).** El bloque de texto del hero mide ~1350 px de alto: debajo del botón "Our services" quedan unos 700 px de fondo beige vacío antes de "More Love Stories". | `/` | Parece una web rota o a medio cargar; mucha gente deja de hacer scroll ahí. |
| 0.6 | **Formulario de contacto: verificadlo en vuestro móvil.** En mi entorno no se dibujó (depende de reCAPTCHA de Google, que yo tengo bloqueado), así que puede ser cosa mía. Pero comprobad que se ve y que llega el email de aviso. | `/contact`, `/contacto` | Es vuestra única conversión. Si falla, la web no vende nada. |
| 0.7 | **Botón "Inquire" en móvil**: en la captura de Servicios en móvil la página termina en el email y no aparece el botón "Inquire". Comprobadlo. | `/services` móvil | El final de la página de precios es el momento de máxima intención. |

---

## 1. El banner de cookies

Está configurado en posición **"Bottom"** y en un móvil real **sí queda abajo**. En las capturas de página completa aparece "a mitad de página" solo por cómo se hacen esas capturas.

El problema real es otro:

- **Ocupa casi la mitad de la pantalla del móvil** (6 líneas de texto + 3 botones grandes).
- **Tiene el mismo color de fondo que la página**, sin borde ni sombra, así que parece que el texto "se monta" encima del titular.

**Qué hacer** (Squarespace → Settings → Cookies & Visitor Data → Cookie banner):
1. Acortar el texto a una o dos líneas, por ejemplo: *"Usamos cookies esenciales y, si aceptas, de analítica. [Política de cookies]"*.
2. Cambiar el estilo del banner a oscuro (o en granate `#7A1F2B` con texto crema) para separarlo del fondo, o añadir un borde superior con CSS personalizado.
3. Mantener "Aceptar" y "Rechazar" con el mismo peso (eso ya está bien y es lo que pide la normativa).
4. Traducir el banner en la versión ES (ahora sale en inglés también allí).

---

## 2. Coherencia con el manual (*The Call Sheet*)

El manual dice una cosa y la web otra en varios puntos de fondo:

| El manual dice | La web hace | Comentario |
|---|---|---|
| Lugares **deliberadamente no icónicos**; "no una foto frente a un monumento". | La **foto principal de la home es la Sagrada Família nítida y la pareja desenfocada**. | Es la contradicción más grave: el monumento es el protagonista y la pareja es el fondo. Es justo la foto que el manual dice que NO hacéis. Cambiad la foto principal por una con la pareja como protagonista en un rincón con carácter. |
| Evitar **clichés románticos**, "perfect", textos largos. | Titular: *"Love is light, magic, and a timeless moment. In Barcelona, a city full of passion, we capture the essence of your story in images that truly feel."* | Cuatro clichés en una frase de 30 palabras ("light, magic, timeless, city full of passion, essence"). Podría ser de cualquier fotógrafo del mundo. No dice qué hacéis, dónde ni a qué precio. |
| Recurso de marca: **diálogo de dos líneas** ("— I love you. / — I love you too."), uno por capítulo: *"Stay a little longer." / "I wasn't planning on leaving."* | Los capítulos usan frases descriptivas: *"A kiss beneath a streetlamp. A laugh carried by the wind."* | Las líneas del manual son mucho mejores: cinematográficas, cortas, con tensión. Usadlas tal cual. |
| La escasez es **real y hay que decirla**: 1–3 parejas al mes, solo martes. | No aparece en ningún sitio. | Es una ventaja honesta de posicionamiento ("solo fotografiamos 3 parejas al mes") y crea urgencia sin trucos. |
| **Posicionamiento central:** "Somos una pareja que fotografía parejas." | Solo aparece en About, al fondo. | Debería estar en la home, en la primera pantalla. |
| Diferenciador: **dirección y styling** ("como dirigir un cortometraje"). | La palabra *styling* no aparece; *dirección* tampoco. | Es lo que justifica cobrar 400–650 € frente a los 250 € de la competencia, y no se cuenta. |
| Capítulo III: **privacidad total**, nada se comparte sin permiso. | Ni una línea sobre privacidad o consentimiento en *In The Mood For Love*. | Es la principal ansiedad de ese capítulo (el más caro). Sin esa frase, muchas parejas no escriben. |
| Entregables: 15–20 / 20–25 / 15–20 fotos editadas. | No se dice cuántas fotos ni en cuánto tiempo se entregan. Wild At Heart no tiene duración. | Precio sin entregable = el cliente no puede comparar ni justificar el gasto. |

---

## 3. Textos (copy), página por página

### Home
- **Titular** (ver arriba). Propuesta en línea con el manual:
  - EN: *"A couple, photographing couples. — Cinematic sessions in Barcelona, directed and styled. From €400."*
  - ES: *"Una pareja fotografiando parejas. — Sesiones de cine en Barcelona, con dirección y estilismo. Desde 400 €."*
- **Subtítulo en mayúsculas** "LET'S CAPTURE THE LIGHT THAT CELEBRATES YOUR LOVE" → otro cliché; se puede eliminar.
- **CTA "Our services"** → poco motivador. Mejor "See the three chapters" / "Ver los tres capítulos", y un segundo botón "Check your date" / "Consultar fecha".
- **"More Love Stories"** → "More" sin que haya habido historias antes. Mejor "Love stories" / "Historias".
- **La home no tiene**: precios, los tres capítulos, quiénes sois, testimonios, cómo funciona, ni un CTA final al formulario. Hoy es foto + texto + carrusel. Estructura propuesta:
  1. Hero (foto con la pareja protagonista + titular + "desde 400 €" + CTA)
  2. "Somos Nuria & Miguel" (2 líneas + foto vuestra)
  3. Los tres capítulos (tarjetas con diálogo + precio + CTA)
  4. Cómo funciona (3 pasos: escribís → os proponemos idea, look y lugar → sesión → galería en X días)
  5. Testimonios (aunque sean 2–3 de las sesiones de portfolio)
  6. "Solo 3 parejas al mes" + CTA final

### Services
- El párrafo de entrada es largo (55 palabras) y genérico ("golden light, hidden corners", "extraordinary"). El manual pide frases cortas.
- *"The images are yours forever. And so are the memories."* → cliché; aporta poco.
- **Wild At Heart con precio y "Coming soon"**: o se quita el precio y se añade "Join the waitlist" / "Apúntate a la lista", o se ofrece ya. Un producto que no se puede comprar con precio visible genera dudas.
- **"Turn your fire into art"** → roza lo cursi. "Don't look at the camera. — I wasn't." del manual es mucho más fuerte.
- **Lo que sí está bien:** la sección de reserva es clara (50 %, Bizum/transferencia/Wise, respuesta en 24 h), y "Rain or shine… some of our favourite photos happened under grey skies" es un buen texto, con voz propia.
- **Faltan:** qué incluye cada sesión (dirección, styling, propuesta de vestuario, localización), número de fotos, plazo de entrega, idiomas, cómo se entrega la galería.

### About
- El texto es lo mejor de la web: tiene voz ("a little rebellion", "less posing, more feeling"). Pero:
  - Empieza con "We are a creative duo from México" — lo interesante no es de dónde sois sino que **sois pareja y artistas**. Abrid con eso.
  - Falta enlazar vuestros portfolios personales (`@nuria.alferez`, `@ojodearbol`), que el manual cita como prueba de que sois artistas.
  - No hay CTA al final de la página.

### Contact
- "For all inquiries, please fill out the form below to get started and we'll get back to you." → frase de formulario corporativo. La versión ES es mejor ("Cuéntennos un poco de ustedes y de la sesión que sueñan… menos de 24 horas"). Usad esa idea también en inglés.
- Campos del formulario (según la configuración): nombre, email, WhatsApp, fecha y hora preferidas, sesión, idioma, cómo nos conocisteis, "cuéntanos de vosotros". Está bien pensado. Revisad que la fecha preferida avise de que solo hacéis sesiones en martes (si eso sigue siendo así).

### Galerías de parejas (`/launico`, `/ameale`, `/giulicami`, `/wooreejaehyun`)
- **Solo fotos: sin título, sin texto, sin capítulo, sin CTA.** Son callejones sin salida justo cuando la persona está más enamorada del trabajo.
- Añadir en cada una: nombre de la pareja, capítulo, una línea de la historia, una cita de la pareja y un botón "Quiero una sesión así" → formulario.
- Las URL (`/launico`, `/wooreejaehyun`) no dicen nada a Google. Mejor `/stories/lau-nico-gothic-quarter` o similar.

---

## 4. Versión en español

> **Corrección (26 nov, tras comprobarlo en el navegador):** la primera versión de este punto decía que el menú, los botones y el banner salían en inglés. No es así: el script del pie de página los traduce al cargar la página, marca las páginas como `es`, añade las etiquetas `hreflang` y lleva "Pedir información" a `/contacto`. Mi primera lectura fue del HTML sin ejecutar ese script.

Lo que sí queda pendiente:
- En `/inicio` el titular es un H3: la página no tiene H1.
- Las etiquetas `hreflang` dependen de JavaScript; mejor ponerlas también en el HTML de cada página (ver `brand/web/squarespace-codigo.md`, §2).
- **Registro:** el español mexicano ("ustedes", "locaciones") es una **decisión de marca**: es la voz de Nuria y Miguel. Se mantiene.

## 5. Diseño visual

- **Paleta:** coherente con el manual (crema + rojo). Bien.
- **Tipografía:** el titular de la home usa una sans muy condensada con interletraje negativo; en escritorio se leen palabras pegadas ("anda timeless", "light,magic,"). Aflojad el interletraje o usad la serif itálica del manual para los titulares.
- **Mezcla de estilos de titular:** en algunas páginas serif itálica grande ("Meet us", "For the *lovers*"), en otras sans fina. Elegid una regla: serif itálica para titulares y sans para texto.
- **Proporción del hero en escritorio:** la foto queda como una franja panorámica baja; se pierde la emoción. Altura completa de pantalla en escritorio.
- **Botón "Inquire"** con contorno fino, más débil que los botones rojos del resto del sitio. El CTA principal de la página de precios debería ser el botón más fuerte.
- **Pie de página pobre:** solo 4 enlaces. Falta: email, WhatsApp, "Barcelona", enlaces legales, aviso legal, Instagram correcto y una frase de marca ("— I love you. — I love you too.").
- **Fotos del carrusel About** con texto alternativo = nombre del archivo ("MAMC2890.JPG"); el resto, sin texto alternativo. Malo para accesibilidad y para Google Imágenes (una fuente real de clientes en fotografía).

---

## 6. SEO y descubrimiento (el manual dice que Google es el canal principal)

- **Confirmar en Google Search Console** que el sitio ya está indexado y que el sitemap está enviado (en agosto no lo estaba).
- **Títulos y descripciones**: están bien redactados, pero prometen **"Proposal photographers"** / "propuestas de matrimonio" y en la web no hay ninguna oferta de pedida. Si alguien busca eso y llega, se va. O se crea una página de pedidas o se quita de los títulos.
- Los títulos acaban en **"| I Love You"** sin "Barcelona": la marca queda cortada.
- **Datos estructurados**: solo hay `WebSite`. Añadir `LocalBusiness`/`ProfessionalService` (nombre, zona, precio, contacto, Instagram) y `FAQPage` cuando exista una FAQ.
- **Imagen para compartir (OG)** falta en About, Contact, Nosotros, Contacto, Inicio: al compartir por WhatsApp sale sin foto.
- **Contenido para posicionar** (más adelante): páginas de pedida, "dónde hacer una sesión de pareja en Barcelona" (vuestras localizaciones no típicas), una por capítulo.
- **Google Business Profile**: si aún no existe, es la palanca local más barata que hay.

---

## 7. Conversión y confianza

- **Cero testimonios.** Tenéis 4 parejas fotografiadas: pedidles 2–3 frases ya.
- **Sin FAQ.** Preguntas que hay que contestar antes de que escriban: ¿Qué ropa llevamos? ¿Nos ayudáis con el estilismo? ¿Y si somos tímidos? ¿El capítulo III es explícito? ¿Quién ve las fotos? ¿Cuándo las recibimos? ¿En qué idiomas? ¿Viajáis fuera de Barcelona? ¿Puedo regalarlo?
- **Sin "cómo funciona".** El proceso (idea → propuesta de look y lugar → sesión → galería) es parte de lo que vendéis y hoy no se ve.
- **Tarjeta regalo**: San Valentín (14 feb) está a 11 semanas. Un "Regala un capítulo" puede ser la primera fuente de ventas.
- **Lo que está bien:** botón flotante de WhatsApp (muy acertado para turistas), respuesta en 24 h, métodos de pago claros, precio visible.

---

## 8. Preguntas para vosotros (para decidir cómo construir la siguiente versión)

**Marca y posicionamiento**
1. ¿Cuál es el Instagram oficial: `@iloveyoutoobcn` o `@iloveyouarchives`? ¿Por qué hay dos?
2. ¿Estáis dispuestos a quitar la Sagrada Família del hero? ¿Qué foto vuestra representa mejor "esto no es una foto de turista"?
3. ¿Queremos decir en la web "solo martes / solo 3 parejas al mes"? ¿Sigue siendo cierto?
4. ¿Las pedidas de matrimonio son un servicio real que queréis vender? Si sí, ¿qué precio y formato?

**Público e idioma**
5. ¿Quién es el cliente nº 1 de los próximos 6 meses: turistas (inglés) o parejas que viven en Barcelona (español/catalán)?
6. ¿El español "mexicano" es una decisión de voz consciente o lo cambiamos a español de España?
7. ¿Queréis versión en catalán?

**Oferta**
8. ¿Wild At Heart se lanza cuándo? ¿Lista de espera o lo quitamos hasta entonces?
9. ¿Qué incluye exactamente la dirección y el styling? (¿Asesoría de vestuario? ¿Moodboard? ¿Llamada previa?) Es lo que más os diferencia y hay que poder contarlo.
10. ¿Cuántas fotos y en cuántos días se entregan? ¿Cómo (galería online, descarga)?
11. Si cancelan, ¿se devuelve el 50 %? ¿Hasta cuándo?
12. ¿Hacemos tarjeta regalo para San Valentín?

**Prueba social**
13. ¿Podéis pedir ya una frase a América & Alejandro, Lau & Nico, Giulia & Camilo y Wooree & Jaehyun? ¿Nos dejan usar su nombre?
14. ¿Alguna sesión de capítulo III que se pueda enseñar (con permiso) o preferís mostrarlo solo con fotos sugerentes?

**Legal y operación**
15. ¿Quién es el titular de la web (autónomo, NIF) para el aviso legal y la política de privacidad?
16. ¿Existe ya un documento de consentimiento/cesión de imagen para el capítulo III?
17. ¿Os llegan bien los formularios al email? ¿Cuántas consultas habéis recibido desde que la web está online?

---

## 9. Orden de trabajo propuesto

1. **Esta semana:** legales reales + política de cancelación, Instagram unificado, títulos invisibles y hueco de la home, comprobar formulario, banner de cookies.
2. **Semana 2:** reescribir home + servicios con la voz del manual (diálogos, "una pareja fotografiando parejas", escasez, entregables, privacidad cap. III), nueva foto principal.
3. **Semana 3:** FAQ, "cómo funciona", testimonios, galerías con historia y CTA, versión ES completa (menú, botones, hreflang).
4. **Semana 4:** datos estructurados, Search Console, Google Business Profile, tarjeta regalo de San Valentín.
