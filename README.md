# Area Deco — Sitio web

Sitio de una sola página para **Area Deco**, estudio de decoración de interiores en Ciudad de Panamá (Sabri &amp; Naty, [@areadeco_panama](https://www.instagram.com/areadeco_panama/)).

Todo el contenido está en español (`lang="es"`).

## Estructura

```
area-deco/
├── index.html     # sitio completo: HTML + CSS + JS en un solo archivo
└── images/        # 14 fotos de proyectos entregadas por el cliente
```

No hay build ni dependencias. Las únicas peticiones externas son las fuentes de Google Fonts
(Cormorant Garamond + Jost).

## Correr localmente

```bash
python3 -m http.server 8140 --directory .
```

Luego abrir <http://localhost:8140>.

> También funciona abriendo `index.html` directamente con doble clic (`file://`):
> todas las rutas de imágenes son relativas y no hay `fetch` ni módulos ES.
> Lo único que necesita conexión son las fuentes de Google Fonts, y si no cargan
> el sitio cae a serif/sans del sistema sin romperse.

## Secciones

| Sección | Ancla |
|---|---|
| Hero | — |
| Nosotras | `#nosotras` |
| Proyectos | `#proyectos` |
| Galería (con filtros + lightbox) | `#galeria` |
| Servicios | `#servicios` |
| Proceso | `#proceso` |
| Instagram | — |
| Contacto | `#contacto` |

## Datos del cliente en el código

Estos valores están escritos directamente en `index.html`:

- **Teléfonos / WhatsApp:** 6550-6288 y 6780-9161
- **Número principal de WhatsApp:** constante `WA_NUMBER` en el `<script>` (`50765506288`)
- **Instagram:** `@areadeco_panama`
- **Ubicación:** Ciudad de Panamá

## Formulario de contacto

El formulario **no envía correos**. Valida nombre y correo, arma un mensaje con todos los
campos y lo abre en WhatsApp (`wa.me`). Para recibirlo por email, reemplazar el handler
`submit` al final del `<script>` por Formspree, Netlify Forms o un endpoint propio.

## Pendiente por confirmar con el cliente

- [ ] Grafía del nombre: **Area Deco** vs **Área Deco** (con tilde)
- [ ] Correo electrónico de contacto (no aparece público)
- [ ] Dirección o showroom, si tienen
- [ ] Nombres, ubicación, metraje y año reales de cada proyecto
- [ ] Testimonios reales de clientes
- [ ] Métricas reales (proyectos entregados, años de trayectoria)

Las estadísticas que se muestran hoy son solo las verificables (+17K seguidores en Instagram,
llave en mano, mobiliario a la medida, Panamá). No se inventaron cifras ni testimonios.

## Licencia / uso

Las fotografías son propiedad de Area Deco. Repositorio privado.
