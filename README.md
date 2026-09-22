# Plantilla de propuestas — Tegra Soluciones

Sistema de diseño y plantilla reutilizable para generar propuestas comerciales de **Tegra Soluciones**, una empresa mexicana de servicios administrados de TI (MSP) con más de 20 años de experiencia en administración de infraestructura tecnológica.

**Servicios de Tegra Soluciones:** soporte de TI (helpdesk 24/7, en sitio y remoto), ciberseguridad (firewalls, protección de endpoints, auditorías), videovigilancia (CCTV e IP), automatización industrial (PLC, SCADA/HMI), implementación en la nube (AWS, Azure, GCP), desarrollo web, inteligencia de negocios y gestión de licencias. Atiende manufactura, logística, construcción, retail, salud, educación y gobierno.

**Tono de marca:** formal pero moderno — sobrio, confiable, orientado a resultados prácticos y no a la jerga técnica. Español de México, tercera persona colectiva ("nosotros"), sin emojis ni signos de exclamación. Superficies predominantemente blancas; el rojo de marca se reserva para acentos y momentos de peso; el gris secundario carga la mayor parte del trabajo estructural.

**Colores:** rojo de marca `#AF282F` (acentos, nunca como fondo de sección completa), gris secundario `#6F6F6F` (texto secundario, bordes, iconos), escala de neutros de blanco a casi negro para superficies y texto.

**Tipografía:** dos familias — **LEMON MILK** (solo para el wordmark, el titular principal de una portada, los overlines de sección y números grandes ≥32px) e **Inter** (todo lo demás: encabezados de sección, cuerpo, tablas, botones, formularios). Inter hace la mayor parte del trabajo; LEMON MILK se reserva para momentos de marca puntuales.

## Qué hay en este repositorio

```
Plantilla Propuesta — Tegra.dc.html   ← la plantilla de propuesta, con marcadores [[ASÍ]]
Prompt para llenar la plantilla.md    ← instrucciones para que una IA llene la plantilla
doc-page.js, support.js               ← runtime que renderiza el documento paginado
icon-ms9ibmi9-5drh.png                ← ícono de marca usado en la firma de cierre
assets/                                ← logo y logos de certificaciones/partners
_ds/tegra-soluciones-design-system-.../ ← sistema de diseño completo: tokens de color,
                                           tipografía y las fuentes reales (LEMON MILK + Inter)
```

`Plantilla Propuesta — Tegra.dc.html` es un documento HTML paginado (tamaño A4, una hoja fija por `<section class="page">`) construido sobre el sistema de diseño de `_ds/`. Para generar una propuesta nueva, se sigue `Prompt para llenar la plantilla.md`: se reemplaza cada marcador `[[ASÍ]]` por contenido real del proyecto y se conservan las clases y componentes ya definidos (tablas de cotización, bloques de fase, componente de imagen, cláusulas de términos y condiciones).

## Ver una propuesta

Abrir el archivo `.dc.html` correspondiente directamente en un navegador (doble clic, o arrastrarlo a Chrome). No requiere servidor: todas las rutas son relativas a esta misma carpeta.
