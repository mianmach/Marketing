# Cambios en Squarespace: código y pasos

Todo esto se hace desde el editor de Squarespace (iMac o portátil, no desde la app del móvil).
Antes de tocar el código, copia lo que hay en un archivo de texto por si hay que volver atrás.

---

## 1. Banner de cookies: barra oscura, separada de la página

**Probado sobre la web real** (móvil y escritorio): barra marrón oscuro con línea roja arriba, texto crema y "Aceptar" y "Rechazar" con el mismo peso.

### a) CSS
**Website → Website Tools → Custom CSS** → pegar al final:

```css
/* Banner de cookies: barra oscura, separada claramente de la página */
.gdpr-cookie-banner{background:#2A1F16!important;color:#F7EFDD!important;border-top:3px solid #BA221E!important;box-shadow:0 -10px 28px rgba(0,0,0,.28)!important;padding:16px 24px!important}
.gdpr-cookie-banner .sqs-cookie-banner-v2-text,.gdpr-cookie-banner .sqs-cookie-banner-v2-text p{color:#F7EFDD!important;font-size:14px!important;line-height:1.45!important;margin:0 0 10px!important}
.gdpr-cookie-banner .sqs-cookie-banner-v2-text a{color:#F7EFDD!important;text-decoration:underline!important}
.gdpr-cookie-banner .sqs-cookie-banner-v2-cta,.gdpr-cookie-banner .sqs-cookie-banner-v2-cta.sqs-cookie-banner-v2-deny{background:#F7EFDD!important;color:#2A1F16!important;border:1px solid #F7EFDD!important;font-size:14px!important;padding:10px 18px!important}
.gdpr-cookie-banner .manage{background:transparent!important;color:#F7EFDD!important;border:0!important;font-size:14px!important;text-decoration:underline!important}
.gdpr-cookie-banner .manage *{color:#F7EFDD!important;border-color:transparent!important}
@media (max-width:767px){.gdpr-cookie-banner{padding:12px 16px!important}.gdpr-cookie-banner .sqs-cookie-banner-v2-cta{padding:9px 14px!important}}
```

### b) Código del pie: quitar una regla vieja
En **Settings → Advanced → Code Injection → Footer**, dentro del bloque `<style>` del botón de WhatsApp, borra estas dos líneas (pintan "Decline all" de rojo y chocan con el estilo nuevo):

```
/* Cookie banner: Decline as visible as Accept */
.sqs-cookie-banner-v2-deny.sqs-cookie-banner-v2-cta{background:#BA221E!important;color:#fff!important;border-color:#BA221E!important}
```

### c) Texto más corto
- **Inglés:** Settings → Cookies & Visitor Data → Cookie banner → texto:
  `We use essential cookies and, with your OK, analytics. ` + enlace "Cookie Policy" a `/cookie-policy`.
- **Español:** en el mismo Code Injection → Footer, busca la línea que empieza por `var banner=` y cámbiala por:

```js
var banner='Usamos cookies esenciales y, si nos dan su OK, de analítica. Más información en nuestra Política de cookies.';
```

---

## 2. Google y los dos idiomas (hreflang)

**Situación actual:** ya está resuelto con el script del pie de página. Ese script traduce el menú, los botones y el banner, marca las páginas en español como `es` y añade las etiquetas `hreflang` que le dicen a Google qué página es la versión en el otro idioma. Lo comprobé en el navegador y funciona.

**Mejora recomendada:** Google lee el JavaScript, pero tarda más y no siempre lo hace. Para ir sobre seguro, pon las etiquetas también en el HTML de cada página:

**Pages → (página) → ⚙ Settings → Advanced → Page Header Code Injection.** Hay que pegar el mismo bloque en las dos páginas de cada pareja:

**Home (`/`) y Inicio (`/inicio`):**
```html
<link rel="alternate" hreflang="en" href="https://www.iloveyoubarcelona.com/" />
<link rel="alternate" hreflang="es" href="https://www.iloveyoubarcelona.com/inicio" />
<link rel="alternate" hreflang="x-default" href="https://www.iloveyoubarcelona.com/" />
```
**About y Nosotros:**
```html
<link rel="alternate" hreflang="en" href="https://www.iloveyoubarcelona.com/about" />
<link rel="alternate" hreflang="es" href="https://www.iloveyoubarcelona.com/nosotros" />
<link rel="alternate" hreflang="x-default" href="https://www.iloveyoubarcelona.com/about" />
```
**Services y Servicios:**
```html
<link rel="alternate" hreflang="en" href="https://www.iloveyoubarcelona.com/services" />
<link rel="alternate" hreflang="es" href="https://www.iloveyoubarcelona.com/servicios" />
<link rel="alternate" hreflang="x-default" href="https://www.iloveyoubarcelona.com/services" />
```
**Contact y Contacto:**
```html
<link rel="alternate" hreflang="en" href="https://www.iloveyoubarcelona.com/contact" />
<link rel="alternate" hreflang="es" href="https://www.iloveyoubarcelona.com/contacto" />
<link rel="alternate" hreflang="x-default" href="https://www.iloveyoubarcelona.com/contact" />
```

Después, en el script del pie, borra esta línea para que no salgan duplicadas:
```js
if(esPage||enPage){var enH=esPage?toEn[path]:(path==='/home'?'/':path),esH=esPage?path:toEs[path];alt(enH,'en');alt(esH,'es');alt(enH,'x-default');}
```

Por último, en **Google Search Console**: envía `https://www.iloveyoubarcelona.com/sitemap.xml` y pide la indexación de `/` y `/inicio`.

Además, en **/inicio** el titular está como H3: cámbialo a **Heading 1** para que la página tenga título principal.

---

## 3. Títulos que casi no se ven en escritorio (Services, About)

**¿Hay que corregirlo? Sí.** El título es lo primero que lee quien llega desde Google en ordenador. Sin él, la página empieza con una foto sin contexto. Y para Google es el H1, la señal más clara de qué trata la página.

Pasos (en Services, About, Servicios y Nosotros):
1. Abre la página en el editor y, arriba, cambia a **vista de escritorio** (icono de monitor).
2. Haz clic en el texto diminuto de la esquina superior izquierda ("Every love story deserves to be seen" / "We are Nuria & Miguel").
3. Selecciona el texto y ponle el estilo **Heading 1** (en About, **Heading 2**).
4. Arrastra los tiradores del bloque para que ocupe el ancho central, encima de la foto, centrado.
5. Cambia a **vista móvil** y comprueba que allí sigue igual de bien (en Fluid Engine el móvil tiene su propia maquetación).

---

## 4. Hueco vacío en la home (escritorio)

El bloque de texto del titular mide unos 1350 px de alto aunque el texto ocupe unos 300 px. Lo que queda es fondo vacío.

1. Home → Edit → **vista de escritorio**.
2. Haz clic en el bloque del texto "Love is light…" y arrastra el **tirador inferior** hacia arriba hasta justo debajo del botón "Our services".
3. Si queda espacio en la sección, haz clic en la sección → **Edit Section → Format** y baja la altura (*Section height: Small*), o arrastra el borde inferior de la cuadrícula hacia arriba.
4. Guarda y revisa también **/inicio**: es otra página y tendrá el mismo problema.

(Cuando pongas el texto nuevo de `home-copy.md`, este bloque se rehace igualmente.)
