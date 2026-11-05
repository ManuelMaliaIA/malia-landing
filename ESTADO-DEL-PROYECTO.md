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

### 7.1 Exploración de direcciones (2026-11-05)

Bocetos en `.impeccable/mocks/decision/` (HTML) y capturas enviadas a Manuel. **Descartadas:** Pizarra, Carta Náutica, Retícula de taller, Tique de caja, Almadraba, Muro de catálogo, Documento a medida, Rótulo de comercio, Horario de mareas, Estándar del sector, «Plano del flujo» (`r3-plano.html`, inspirado en la muestra Tortuga de la galería de impeccable.style: «mucho ruido») y la versión limpia `r4-limpio.html`.

**Decisión de Manuel:** partir del **diseño actual**, sobre todo del **hero** (vídeo de humo a pantalla completa, titular centrado en Space Grotesk, retícula en cruz, botones píldora). El hero se conserva como base. El rediseño completo se aplica al resto de secciones, al blog y a la biblioteca, en el mismo lenguaje que el hero.

**Idea que sí gustó:** mostrar un flujo tipo n8n con los 5 pasos para implantar una automatización (Me escribes → Vemos la tarea → Diseño el flujo → Lo monto y probamos → Funciona solo). Debe ir limpio, sin nodos de relleno ni adornos técnicos. Es candidato a sección «Cómo trabajo» justo después del hero.

**Confirmado por Manuel (2026-11-05):** la home lleva este orden: hero actual pulido → Cómo trabajo (flujo de 5 pasos) → Casos reales → Biblioteca (con `#automatizaciones-destacadas`) → Contacto. Después vienen el blog y la biblioteca con el mismo lenguaje. Es un rediseño completo de todas esas partes.

### 7.2 Home rediseñada (2026-11-05, sin commit)

Contrato de dirección en `.impeccable/surfaces/index-html.md`. Cambios en `index.html` (se mantienen el hero, el header y todo el JS anterior):
- `#servicios` → sección **Cómo trabajo** (`.metodo`) sobre tinta. Lleva el flujo n8n `ol.flow#flow` de 5 nodos, que se encienden en secuencia con IntersectionObserver; con movimiento reducido o sin JS se ven todos encendidos. Debajo va «Sin cuotas por cada tarea» con la pila n8n/Easypanel/Hostinger y el CTA «Empieza por el paso 1». Se han quitado las 4 tarjetas de ventajas.
- `#casos` sobre arena: cabecera con los 3 logos (desaparece la franja de logos suelta) y el caso MOTODEST en filas regladas con icono. Los textos del caso no cambian.
- **Biblioteca:** sección `#automatizaciones-destacadas` (la que el kit de n8n esperaba y no existía). Lleva 3 `a.automation-card` en filas, entre `<!-- AUTOMATION_CARDS_START/END -->`. Una card nueva copia la estructura: `span.icon` con svg, `h3`, `p`, `svg.go`.
- **Pie:** fondo tinta con la línea de la cruz. Superficies del navegador: selección invertida en secciones oscuras, `scrollbar-color` y `caret`.
- **Verificado:** capturas a 1440 y 390 sin desbordes. Ojo: Chrome headless no baja de 504 px, así que el móvil se captura dentro de un iframe de 390. El detector solo da avisos aceptados: los nodos con icono son el flujo n8n pedido, arena y fuentes están fijadas, y radios y colores nuevos van al futuro `DESIGN.md`.
- La copia de la home anterior está en git (`master`).

**Objetivo de Manuel (2026-11-05): una web «40/40»,** es decir, la puntuación máxima en `impeccable critique` (10 heurísticas × 4). Hay que hacer el ciclo critique → arreglar → critique en home, blog y biblioteca hasta llegar a 36-40 («Excellent») y apuntar la evolución, que guarda `.impeccable/critique/`. La skill avisa de que un 4 es «excelente de verdad» y que lo normal es 20-32.

**Evolución home:** 19/32 (10:10, antes del rediseño) → **29/40** (14:50, home rediseñada; `.impeccable/critique/2026-11-05T14-50-32Z__index-html.md`). Nueve heurísticas en 3 y la de ayuda en 2. Para subir: P1 ejemplos por sector (hostelería y comercio) + una línea real de Mavimar y Vidal; P1 FAQ de 4 preguntas (precio o presupuesto, plazo, mantenimiento, datos) con respuestas de Manuel; P1 foto real de Manuel; P2 WhatsApp flotante (borde y que no tape); P2 coherencia (MOTODEST, nav «Servicios», WhatsApp del pie sin mensaje, CTA en escritorio, «o llámame», cierre del menú móvil). Además, falta aviso legal y privacidad (LSSI).

**Arreglos tras la crítica de 29/40 (2026-11-05, sin commit):**
- **Respuestas de Manuel (no volver a preguntar):**
  - Presupuesto cerrado antes de empezar, con cuota mensual de mantenimiento.
  - El plazo depende de la carga.
  - Mantenimiento semanal, mínimo dos días por semana.
  - Los datos están en un VPS de Hostinger, donde corre n8n.
  - Titular: Manuel Malia Vidal, NIF 77174426L.
  - Teléfono para llamar: el mismo de WhatsApp.
  - Mavimar y Vidal son «consultoría y asesoría» (proyectos `Contabilidad`, `AdministracionFincas` y `Anonimizador` del kit de n8n).
  - Clientes nuevos que se pueden nombrar: **Pescados Rosados** (facturas de compra → Holded, unas 35 al día, con aprobación previa) y **BarbateHomes** (web, catálogo y panel; enlace a barbatehomes.es).
- **Casos:** cabecera con entradilla (sin franja de logos; el de MOTODEST va encima de su caso) y bloque «Y otros negocios de la zona» con filas de Mavimar y Vidal, Pescados Rosados y BarbateHomes.
- **Sección nueva `#tu-negocio`** sobre tinta, entre Casos y Biblioteca: ejemplos para bar, tienda y asesoría, cada uno con su enlace de WhatsApp con mensaje precargado.
- **Sección nueva `#preguntas`** («Antes de escribirme») tras la biblioteca, con 5 `<details>`.
- **Páginas nuevas `aviso-legal/index.html` y `privacidad/index.html`**, enlazadas desde el pie. Domicilio completo puesto: Avda. del Mar, 108, 3.º C, Barbate (Cádiz). La foto de Manuel queda para más adelante, cuando él la aporte; no hay que volver a pedirla en cada crítica.
- **Coherencia:**
  - El menú dice «Cómo trabajo».
  - MOTODEST va en mayúsculas en todas partes.
  - El WhatsApp del pie lleva mensaje precargado.
  - «¿Prefieres llamar? 611 459 336» bajo los botones del hero.
  - Sin CRM ni chips n8n/Easypanel/Hostinger en la home. El paso 3 se llama «Te dibujo el plan».
- **Navegación:**
  - En escritorio no se esconde.
  - Marca la sección actual (`aria-current`).
  - El botón del menú móvil cambia a «Cerrar», y el menú se cierra al tocar fuera o al hacer scroll.
- **Otros arreglos:**
  - WhatsApp flotante con borde.
  - `text-wrap: pretty` en los párrafos.
  - Fuera el JS `.reveal` que no se usaba.
  - `areaServed` pasa a Provincia de Cádiz.
  - Token `tinta-alzada`.
  - Valores nuevos apuntados en `DESIGN.md` (sección «Home rediseñada»).
- **Verificado:** capturas a 1440 y 390 sin desbordes; detector solo con avisos aceptados (flujo n8n, filas de la biblioteca del kit, falsos positivos de relleno, fuentes y arena del brief).
- **Siguiente:** nueva `critique` de la home (hilo nuevo) para medir la subida. Sigue faltando la foto de Manuel, lo único que queda del P1.

**Re-critique (2026-11-05 15:21): 28/40** (`.impeccable/critique/2026-11-05T15-21-35Z__index-html.md`). Ha bajado un punto respecto al 29, pero no es una comparación exacta: los evaluadores son distintos y este fue más estricto con los arreglos de la tanda anterior. El detector no da ningún problema real; solo hay 4 viudas tipográficas (l.1012, 1021, 1031 y 1058).
- **P1 contacto:** no dice quién contesta ni cuándo, ni qué incluye la primera consulta. Falta el email junto al CTA en escritorio y un texto oculto «(abre WhatsApp)».
- **P1 biblioteca:** «3 proyectos» (la cifra es correcta) choca con los 5 negocios de Casos, y 2 de las 3 filas no son clientes. Reescribir el texto de l.1078.
- **P2:** el titular «Sin cuotas por cada tarea» (l.952) contradice la cuota fija.
- **P2:** el bloque «Y otros negocios» es denso y con jerga, y la FAQ dice «VPS/Hostinger».
- **P3:** la cruz del hero atraviesa el texto.
- **Notas bajas:** H7 Flexibilidad (la navegación no enlaza a «Tu negocio» ni a «Preguntas») y H9 Recuperación de errores (no hay alternativa a wa.me en escritorio).
- **Decisiones de Manuel tras el 28/40 (no volver a preguntar):**
  - Compromiso de respuesta: «Te contesto yo mismo, normalmente el mismo día laborable». La primera consulta es gratis.
  - Biblioteca: se reescribe la entradilla de l.1078 para distinguir los casos de clientes de los flujos propios de malia. Las filas del kit no se tocan.
  - Alcance: todo, de P1 a P3, más los detalles menores y las 4 viudas tipográficas.
- ~~Siguiente: aplicar los arreglos~~ → hecho, ver abajo.

**Arreglos tras el 28/40 (2026-11-05 tarde, sin commit):**
- **Contacto:** bajo los botones del hero, «Te contesto yo mismo, normalmente el mismo día laborable» + qué incluye la primera consulta, y la línea «¿Sin WhatsApp? Llámame al 611 459 336 o mándame un email» (enlaces con zona de 44px). La misma promesa en el pie. Nueva pregunta en la FAQ, la primera: «¿Qué pasa cuando te escribo?».
- **WhatsApp:** los 8 enlaces llevan un texto oculto «(abre WhatsApp)» (`.sr-only`). Los enlaces por sector llevan el icono de WhatsApp en lugar de la flecha, y la entradilla dice que se abre WhatsApp. Quitado el WhatsApp repetido de la lista de contacto del pie.
- **Biblioteca:** entradilla nueva: «11 automatizaciones: las que usa MOTODEST cada día y las que montamos para malia, como el blog que se escribe solo». Sin «3 proyectos». Filas del kit sin tocar.
- **Precio:** el titular pasa a «Precio cerrado, sin pagar por uso». En la FAQ, el precio «depende de lo que haya que montar».
- **Sin jerga:** «mandato de representación/matriculación» → «autorización para matricular»; fuera «asientos» (clientes y sector asesoría) y «VPS/Hostinger» (FAQ). Las filas de «Y otros negocios» son más cortas y llevan el título de cada trabajo en su propia línea, en Space Grotesk.
- **Navegación:** Cómo trabajo · Casos · Tu negocio · Biblioteca · Preguntas · Blog · WhatsApp (todo anclas salvo el blog; fuera «Contacto»). El menú desplegable entra a ≤1080px (antes 900) porque en escritorio no cabían 7 entradas.
- **Polish:** la cruz del hero se abre alrededor del texto con una máscara; el hueco vertical lo ajusta un JS a la altura real del texto. Fuera la coma del H1. Flechas «→» de texto cambiadas por SVG. `text-wrap: pretty` también en los `li` (viudas). En móvil, las marcas de la cruz de «Tu negocio» y del pie van al lateral, como en «Cómo trabajo».
- **Verificado:** capturas a 1440, 1000 y 390 sin desbordes. El detector da 15 avisos, todos ya aceptados: icon-tile del flujo y de las filas, relleno, fuentes y arena.
- **Siguiente (hilo nuevo):** re-critique de la home. Queda pendiente la foto de Manuel.

**Biblioteca con los clientes y sus logos (2026-11-05 tarde, sin commit). Decisiones de Manuel (no volver a preguntar):**
- Quitar de la home las filas «Blog de malia» y «Vigilancia de marketplace». Siguen en `/automatizaciones`.
- Quitar de «Casos» el bloque «Y otros negocios». Casos se queda con MOTODEST en detalle.
- Crear ya las páginas de la biblioteca de los clientes que no la tenían.
- Usar el logo de Barlovento: **Pescados Rosados = PESCADOS BARLOVENTO, S.L.** En la web sale como «Pescados Barlovento».

**Hecho:**
- **Home `#automatizaciones-destacadas`:** 4 filas `a.automation-card.has-logo` con el logo del cliente en lugar del icono:
  - MOTODEST.
  - Mavimar y Vidal Malia, con los dos logos. Son las dos marcas de la gestoría de Pedro.
  - Pescados Barlovento.
  - BarbateHomes.

  La entradilla dice «19 automatizaciones, 14 de ellas en negocios de la zona». Los marcadores `AUTOMATION_CARDS_START/END` siguen igual: una fila nueva del kit de n8n con `span.icon` sigue funcionando.
- **Logos en `uploads/`:**
  - `mavimar-logo.webp`, recortado sin los sellos OCA.
  - `vidal-malia-logo.webp`.
  - `barlovento-logo.svg`, copiado de `kit-automatizaciones-n8n/pescados-rosados/`.
  - `barbatehomes-logo.webp`.
- **Biblioteca:** 3 páginas de grupo nuevas, hechas a partir de la de MOTODEST, y 8 fichas hechas con `_template.html`. También están en el índice (detrás de MotoDest) y en `sitemap.xml`.
  - `mavimar-vidal-malia`: `-contabilidad-ia`, `-impuestos-informes`, `-administracion-fincas` y `-anonimizador`.
  - `pescados-barlovento`: `-facturas-compra` y `-comprobacion-diaria`.
  - `barbatehomes`: `-web-catalogo` y `-panel-inmuebles`.
- **Textos sacados de los ESTADO de cada proyecto, sin nombres de personas ni CIF.**
  - **Confirmado por Manuel (2026-11-05):** las facturas de Barlovento y el panel de BarbateHomes ya funcionan en real. Los textos de las fichas se quedan como están.
- **Verificado:** capturas a 1440 y 390 de la home, del índice, de un grupo y de una ficha. Las páginas nuevas de la biblioteca arrastran los avisos de la plantilla antigua (tamaños de letra fuera de escala y contraste de las etiquetas), como las 11 que ya existían. Se resolverán con el rediseño de la biblioteca.
- **Pendiente:** contar al kit de n8n (Paso 4 de su skill) que las filas de cliente de la home ahora llevan logo (`.has-logo` + `span.logo`).

**Pendiente del rediseño:**
- Blog: `blog/index.html`, `blog/_template.html` y los 13 posts.
- Biblioteca: `automatizaciones/index.html`, páginas de grupo, `_template.html` y 11 fichas. Todo con el mismo lenguaje y sin tocar los marcadores ni las clases del kit de n8n.
- Después: finish reviewer, reescribir `DESIGN.md` (documenter) y commit/push solo si Manuel lo pide.

**Siguiente paso (histórico):**
1. Confirmar con Manuel la lista de secciones de la home.
2. Escribir el contrato de dirección en el surface brief (`seed:f9eca3b5b7ae3e9d`).
3. Leer `craft-floor.md` y construir.

## 8. Pendiente

- Revisar malia-ai-labs.com en navegador y móvil (vídeo, menú, botón flotante de WhatsApp).
- Comprobar que el próximo post que publique n8n sale con la sombra tintada: los 6 posts del 2026-11 salieron con la plantilla antigua (`rgba(0,0,0,0.18)`) y se corrigieron a mano. Si vuelve a pasar, actualizar la plantilla en el kit de n8n.
- Foto real de Manuel para el hero o el pie (ahora solo hay texto; el «avatar» es el logo de semitonos).
- Testimonios literales de MOTODEST, Mavimar y Vidal; un caso de hostelería cuando exista.
- Opcional: llevar la navbar nueva (WhatsApp + menú móvil) al blog y la biblioteca; toca los `_template.html` que usa el kit de n8n.
