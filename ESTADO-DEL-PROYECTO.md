# Malia — web malia-ai-labs.com

**Última actualización:** 2026-11-05 (tarde)

## 1. De qué va

Web principal de Manuel: "malia — Automatización con IA para pymes | Barbate, Cádiz". Automatizaciones de IA a medida para comercios, hostelería y servicios.

- Sitio estático: `index.html` + `blog/` + `automatizaciones/` (sin build ni framework).
- Repo git `ManuelMaliaIA/malia-landing`, proyecto Vercel `malia-landing`. Cada push a la rama por defecto se publica solo.
- SEO: `sitemap.xml`, `robots.txt`. Guías propias en la raíz: `seo-optimizer.md`, `web-rebuilder.md`, `scroll-video.md`.

## 2. Relación con otros kits (IMPORTANTE)

- **`automatizaciones/`** la alimenta el kit de n8n (`Kits/IMPORTANTES/kit-automatizaciones-n8n`, skill `automatizaciones-n8n`, Pasos 4 y 4.5), que hace commit y push automáticos. No reorganizar esa carpeta ni `_template.html` sin revisar antes esa skill.
- **`blog/`** la alimenta el workflow de blog de n8n (ver `kit-automatizaciones-n8n/Blog/ESTADO-DEL-PROYECTO.md`).
- El 2026-10-28 la carpeta se movió de `Proyecto/WEB/Malia` a `Kits/IMPORTANTES/kit-impeccable/Malia`; las rutas del kit de n8n ya están actualizadas.

## 3. Estado actual

- Últimos commits: traducción de títulos del blog al español y paginación de la lista del blog (4 por página).
- (Resuelto el 2026-11-05: todo commiteado.) Cambios sin commit a 2026-10-28: `index.html` modificado y logos nuevos sin subir (`MOTODEST vacio.png`, `MOTODEST_HORIZONTAL_negro.webp`, `mavimar.png`, `mavimar vacio.png`, `vidal malia vacio.png`). Preguntar al usuario antes de commitear.

## 4. Diseño (Impeccable)

- `PRODUCT.md` creado el 2026-11-05 (`/impeccable init`): cliente = pymes locales de Cádiz; diferencias = automatizaciones reales, trato directo con Manuel, a medida, sin cuotas SaaS; MOTODEST, Mavimar y Vidal son clientes reales con testimonios (aún no en el repo: no inventar citas).
- `DESIGN.md` + `.impeccable/design.json` creados el 2026-11-05 (`/impeccable document`). North Star: «El Taller a la Vista». Colores: Arena `#F2EFE3` y Tinta Nocturna `#13141F` (sistema de dos tintas, sin acento). Tono de componentes: cercano y tranquilo (píldoras, tarjetas de 16px, sombras ≤10%). Firma: retícula en cruz de 1px.
- Corregido el 2026-11-05 (sin commit): hover y foco visible en los botones y enlaces de la home; sombra del hover `rgba(10,10,22,0.3)` en lugar de negro en las 25 páginas del blog y la biblioteca (plantillas incluidas); todos los kickers en Space Grotesk 600; `PRODUCT.md`, `DESIGN.md` y `.impeccable/` añadidos a `.vercelignore`.
- Avisos del detector previos, sin tocar (para `critique`): Inter y Space Grotesk son fuentes «sobreusadas», el fondo crema es un patrón típico de IA y varios tamaños de letra (11, 12, 14, 22, 24, 26 y 42px) están fuera de la escala de `DESIGN.md`.
- Modo de la home: Persuade (landing comercial). Blog: Read.
- **Critique + audit de `index.html` hechos el 2026-11-05** (snapshot en `.impeccable/critique/2026-11-05T10-10-53Z__index-html.md`). Nielsen 19/32 (Aceptable) · audit técnico 9/20 (Pobre). Los avisos de fuentes y fondo crema chocan con el brief: se ignoran. P1: la home no enseña pruebas (banner de la biblioteca comentado, l.693-709; cifras 11/3 verificadas), hero sin CTA ni Manuel, «Agenda una llamada» es un `mailto`, vídeo y animaciones sin pausa ni `reduced-motion`, navbar que desaparece y con enlaces diminutos en móvil. Pendiente de que Manuel elija prioridad y alcance.

## 5. Plan de la crítica aplicado (2026-11-05, publicado con push el 2026-11-05, `master` en `811d826`)

Hecho en una pasada sobre `index.html` (reescrita) y `uploads/`:

- **Conversión:** CTA principal WhatsApp (`wa.me/34611459336` con mensaje precargado) en hero, navbar, pie y botón flotante en móvil; email como opción secundaria en el pie. «Agenda una llamada» (mailto) eliminado.
- **Pruebas:** nueva sección `#casos` con el caso MOTODEST (4 automatizaciones reales sacadas de la biblioteca, enlace a `/automatizaciones/motodest/`); banner de la biblioteca reactivado con 11 automatizaciones / 3 proyectos (sin kicker ni «Stack»).
- **Copy:** voz en primera persona («Te atiendo yo, Manuel, desde Barbate»); «Disponible 24/7» → «Trabaja cuando tú no estás»; herramientas a 30px → bloque «Sin cuotas por cada tarea» con chips pequeños; sin números 01–04; H3 del pie → H2.
- **Navbar:** sólida al bajar, se esconde al bajar y vuelve al subir; enlaces de 15px con 44px de alto; menú desplegable en ≤900px.
- **Harden:** skip link, `<header>`/`<main>`, alts sin duplicar, `.reveal` visible sin JS, reduced-motion completo, preloader solo 1.ª visita (0,9s, `aria-hidden`), vídeo con botón de pausa, pausa fuera de pantalla y sin carga con reduced-motion o ahorro de datos.
- **Optimize:** `uploads/hero-1280.mp4` (1,27 MB) y `hero-480.mp4` (0,38 MB) en lugar de `2.mp4` (2,35 MB); póster `hero-poster.webp`; `favicon-64.png` (5 KB) y `apple-touch-icon.png`; `logo-inverted.png` 1 MB → 168 KB y `avatar-round-6b2aa1c8.png` 906 KB → 224 KB (redimensionados en el sitio, mejora también blog y biblioteca); logo de MOTODEST recortado y sin fondo (`uploads/motodest-horizontal.webp`), adiós al `scale(1.6)`.
- **Typeset/extract:** variables CSS en `:root`, escala de DESIGN.md, Space Grotesk 500 quitada, CSS muerto eliminado. `DESIGN.md` actualizado (navbar, botón ghost, lista de caso, motion).
- Verificado con capturas a 1440, 820 y 390 px y con el detector (solo quedan los avisos de fuentes/crema, que chocan con el brief, y el falso positivo del hero).

## 6. Polish (2026-11-05)

- Borrado `uploads/2.mp4` (sin uso). El `2.mp4` de la raíz se conserva: es el original, no está en git y Vercel lo ignora.
- Menú móvil: enlaces a todo el ancho y WhatsApp centrado; relleno superior del titular del problema en móvil; enlace de email del pie con zona de pulsación de 44px.
- La crítica del 2026-11-05 queda cerrada (el archivo cambió).

## 7. Rediseño completo (decidido el 2026-11-05, sin empezar)

Manuel quiere rediseñar la web entera para que quede «más profesional», manteniendo la esencia. Respuestas ya dadas (no volver a preguntar):

- **Alcance:** home + blog + biblioteca de automatizaciones. Implica tocar los `_template.html` que usa el kit de n8n: revisar antes cómo los usa ese kit (`kit-automatizaciones-n8n`, Pasos 4 y 4.5 y el workflow del blog) para no romper la publicación automática.
- **Dirección:** Manuel no la tiene clara → preparar 2-3 direcciones visuales para que elija **antes de programar** (flujo `shape` + `new-work` de Impeccable).
- **Esencia que no se toca:** los colores arena `#F2EFE3` y tinta `#13141F`, y el vídeo de humo del hero.
- **Se puede cambiar:** el logo de semitonos y el wordmark en su uso (no el logo en sí sin preguntar), y las tipografías (Space Grotesk e Inter).
- **Referencias:** ninguna; decide Claude a partir de `PRODUCT.md`.
- Cuando se elija la dirección, reescribir `DESIGN.md` (es un rediseño, no un pulido).

## 8. Pendiente

- Revisar malia-ai-labs.com en navegador y móvil (vídeo, menú, botón flotante de WhatsApp).
- Comprobar que el próximo post que publique n8n sale con la sombra tintada: los 6 posts del 2026-11 salieron con la plantilla antigua (`rgba(0,0,0,0.18)`) y se corrigieron a mano. Si vuelve a pasar, actualizar la plantilla en el kit de n8n.
- Foto real de Manuel para el hero o el pie (ahora solo hay texto; el «avatar» es el logo de semitonos).
- Testimonios literales de MOTODEST, Mavimar y Vidal; un caso de hostelería cuando exista.
- Opcional: llevar la navbar nueva (WhatsApp + menú móvil) al blog y la biblioteca; toca los `_template.html` que usa el kit de n8n.
