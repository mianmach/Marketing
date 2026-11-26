# Plan de ejecución en Squarespace (listo para aplicar)

Orden pensado para hacerlo en una sola sesión, con el iMac conectado o a mano.
Cada paso indica de dónde sale el texto o el código. Tras cada bloque: guardar y revisar en escritorio **y** en móvil.

**Antes de empezar:** copiar en un archivo de texto el Custom CSS y el Code Injection (Header y Footer) actuales, como copia de seguridad.

## Bloque A — Arreglos rápidos (sin datos pendientes)
| # | Dónde | Qué hacer | Fuente |
|---|---|---|---|
| A1 | Website Tools → Custom CSS | Pegar el CSS del banner de cookies | `squarespace-codigo.md` §1a |
| A2 | Settings → Code Injection → Footer | Borrar la regla vieja de "Decline all" y cambiar `var banner=` | §1b, §1c |
| A3 | Settings → Cookies & Visitor Data | Texto corto del banner en inglés | §1c |
| A4 | Services, About, Servicios, Nosotros (vista escritorio) | Títulos a Heading 1 / Heading 2, centrados y a buen tamaño | §3 |
| A5 | Home e Inicio (vista escritorio) | Quitar el hueco vacío debajo del titular | §4 |
| A6 | Inicio | Cambiar el titular de H3 a Heading 1 | §2 |
| A7 | Las 8 páginas EN/ES | Pegar los `hreflang` en Page Header Code Injection y borrar la línea `alt(...)` del script | §2 |
| A8 | Móvil | Comprobar el formulario de contacto y el botón "Inquire" | checklist |

## Bloque B — Nueva home (EN `/` y ES `/inicio`)
| # | Sección | Fuente |
|---|---|---|
| B1 | Hero: línea "— I love you. — I love you too.", H1, subtítulo y 2 botones | `home-copy.md` §1 |
| B2 | Quiénes somos (texto corto + foto de Nuria y Miguel + enlace a About) | §2 |
| B3 | Cómo funciona (4 pasos) | §3 — *falta: días de entrega* |
| B4 | Los tres capítulos con diálogos, fotos por sesión y privacidad | §4 — *falta: decisión sobre Wild At Heart* |
| B5 | Propuestas de matrimonio | §5 — *falta: precio y formato* |
| B6 | "Love stories" / "Historias" (renombrar "More Love Stories") | §6 |
| B7 | Cierre con diálogo + botón | §7 |
| B8 | SEO title y description de las dos páginas | "SEO de la home" |

La foto del hero se queda como está hasta elegir la nueva (checklist).

## Bloque C — Services / Servicios
| # | Qué hacer | Fuente |
|---|---|---|
| C1 | Sustituir los textos de cada capítulo por los diálogos del manual + "15–20 / 20–25 photos" | `home-copy.md` §4 |
| C2 | Añadir la línea de privacidad en In The Mood For Love | `politica-cancelacion.md` (FAQ) |
| C3 | Sustituir la sección de reserva por el texto nuevo (anticipo, 14 días, cambios, clima) | `politica-cancelacion.md` |
| C4 | Botón "Inquire" en rojo relleno, como el resto de botones principales | — |

## Bloque D — Legal (espera datos)
| # | Qué hacer | Bloqueado por |
|---|---|---|
| D1 | `/privacy-policy`: política de privacidad | Titular, NIF, domicilio, email, proveedores |
| D2 | `/tos`: aviso legal + condiciones de reserva | Igual |
| D3 | `/refund-policy`: texto de cancelación, o borrar y redirigir a `/tos` | Visto bueno de la política |
| D4 | Borrar `/accessibility-policy` | — |
| D5 | Enlaces legales en el pie de página | D1–D3 |
| D6 | Casilla obligatoria "He leído la política de privacidad" en el formulario | D1 |

## Datos que necesito para desbloquear lo pendiente
1. Días de entrega de la galería.
2. Precio y formato de la sesión de propuesta.
3. Papel de Miguel el día de la sesión.
4. Wild At Heart: ¿lista de espera u ocultar el precio?
5. Datos legales (lista en `brand/legal/borradores-legales.md` §1).
6. Visto bueno de la política de cancelación (14 días).
7. El nuevo manual de diseño (PDF o nombre en Canva).
