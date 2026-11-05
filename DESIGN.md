---
name: malia
description: Automatización con IA para pymes de Barbate y Cádiz — el taller a la vista.
colors:
  arena: "#F2EFE3"
  papel-tarjeta: "#FAF8F1"
  blanco-chip: "#FFFFFF"
  arena-sombra: "#E4DFCC"
  arena-apagada: "#D8D3C2"
  tinta-nocturna: "#13141F"
  tinta-hover: "#2A2C3D"
  noche-profunda: "#0A0A16"
  gris-pizarra: "#5C5E6B"
  gris-texto: "#6B6D7A"
  gris-humo: "#8A8C9E"
  gris-niebla: "#9A9CA8"
typography:
  display:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(28px, 5vw, 64px)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(30px, 3.6vw, 48px)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: 1.3
  stat:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "30px"
    fontWeight: 700
    lineHeight: 1
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.5
  body-lead:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(16px, 1.6vw, 20px)"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    letterSpacing: "0.05em"
rounded:
  sm: "12px"
  chip: "14px"
  card: "16px"
  panel: "28px"
  pill: "100px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "20px"
  lg: "32px"
  xl: "60px"
  section: "100px"
components:
  button-primary:
    backgroundColor: "{colors.arena}"
    textColor: "{colors.tinta-nocturna}"
    rounded: "{rounded.pill}"
    padding: "16px 32px"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.tinta-nocturna}"
    rounded: "{rounded.pill}"
    padding: "12px 22px"
  card-ventaja:
    backgroundColor: "{colors.papel-tarjeta}"
    textColor: "{colors.tinta-nocturna}"
    rounded: "{rounded.card}"
    padding: "20px"
  chip-herramienta:
    backgroundColor: "{colors.blanco-chip}"
    rounded: "{rounded.chip}"
    size: "60px"
  panel-oscuro:
    backgroundColor: "{colors.tinta-nocturna}"
    textColor: "{colors.arena}"
    rounded: "{rounded.panel}"
    padding: "64px 48px"
  nav-link:
    textColor: "{colors.arena}"
    typography: "{typography.label}"
---

# Design System: malia

## Overview

**Creative North Star: "El Taller a la Vista"**

malia es el taller de un artesano que deja la puerta abierta: se ve cómo se trabaja, con qué herramientas y para quién. El sistema es sobrio a propósito. Hay dos tintas, un papel cálido y una tinta nocturna, y dos tipos de letra. La confianza no la ganan los efectos: la ganan la claridad, el espacio y lo concreto (clientes con nombre, herramientas reales, automatizaciones que funcionan).

La página alterna dos climas: bandas nocturnas (hero con vídeo, panel de la biblioteca, footer) y bandas de arena donde vive el contenido. Dentro de ese ritmo, la densidad es baja. Hay titulares grandes y apretados en Space Grotesk, texto corto en Inter, mucho aire y una retícula de líneas finas que divide las secciones en cuadrantes, como las marcas de trazado de un banco de trabajo.

El tono es cercano y tranquilo: formas redondeadas, botones en píldora, tarjetas apenas elevadas y movimientos lentos que acompañan sin llamar la atención.

**Key Characteristics:**
- Dos tintas (arena y tinta nocturna) sin color de acento cromático.
- Titulares en Space Grotesk 700 con tracking negativo; cuerpo en Inter.
- Retícula en cruz de líneas de 1px como firma visual.
- Bandas oscuras y claras alternas; el oscuro enmarca y el claro explica.
- Formas suaves: píldoras para acciones, 16px para tarjetas.
- Movimiento pausado: fundido hacia arriba de 0.9s y vídeo al 75% de velocidad.

## Colors

Una paleta de dos tintas, papel cálido y tinta nocturna, con grises fríos en lugar de un acento de color.

### Primary
- **Tinta Nocturna** (`tinta-nocturna`): el color de la marca. Texto principal sobre arena, fondo del hero, del panel de la biblioteca y del botón principal invertido. También tiñe todos los overlays y bordes translúcidos (`rgba(19,20,31,…)`).
- **Tinta Hover** (`tinta-hover`): hover de los enlaces sobre fondo claro.
- **Noche Profunda** (`noche-profunda`): solo el footer, un escalón más oscuro que la tinta para cerrar la página.

### Neutral
- **Arena** (`arena`): el fondo base de todas las páginas y el texto principal sobre fondos oscuros. Es el papel del taller.
- **Papel Tarjeta** (`papel-tarjeta`): superficie de tarjetas sobre arena; se distingue por luz, no por contraste.
- **Blanco Chip** (`blanco-chip`): solo los cuadros de logo de herramientas, para que los logos de terceros respiren.
- **Arena Sombra** (`arena-sombra`): texto secundario sobre oscuro (subtítulo del hero, footer) y el tono del degradado radial de la sección del problema.
- **Arena Apagada** (`arena-apagada`): párrafos dentro del panel oscuro.
- **Gris Pizarra** (`gris-pizarra`): kickers, rótulos y numeración sobre arena.
- **Gris Texto** (`gris-texto`): metadatos en el blog y la biblioteca.
- **Gris Humo** (`gris-humo`) y **Gris Niebla** (`gris-niebla`): rótulos y kickers sobre fondo oscuro.

### Named Rules
**The Two Inks Rule.** Toda la página se resuelve con arena y tinta nocturna. Los grises son matices de esas dos tintas, no colores nuevos. Un acento cromático solo entra con una decisión explícita, nunca como adorno.

**The Tinted Transparency Rule.** Las líneas, bordes, sombras y overlays usan siempre la tinta de la marca con alfa (`rgba(19,20,31,x)` sobre claro y `rgba(242,239,227,x)` sobre oscuro), nunca negro ni blanco puros.

## Typography

**Display Font:** Space Grotesk (con sans-serif)
**Body Font:** Inter (con sans-serif)

**Character:** Space Grotesk aporta el punto técnico y artesanal (geometría con remates peculiares) a los titulares, rótulos y cifras. Inter sostiene el texto sin protagonismo. Se cargan solo los pesos usados: Space Grotesk 500/600/700 e Inter 400/500/600.

### Hierarchy
- **Display**: H1 del hero, uno por página, con un máximo de unos 720px de ancho.
- **Headline**: H2 de sección sobre arena (máx. ~520px). La variante del panel oscuro baja a `clamp(28px, 3.4vw, 42px)`, y la del footer, a `clamp(26px, 3vw, 38px)`.
- **Title**: H3 de tarjetas (17px). Los nombres de herramienta suben a 600 y 30px como lista visual.
- **Stat**: cifras del panel de la biblioteca (30px, line-height 1).
- **Body**: párrafos de 15px (13px dentro de las tarjetas), con medidas cortas de 420–560px. El texto secundario sobre arena baja la opacidad (0.7–0.75) en lugar de cambiar de color.
- **Body lead**: subtítulo del hero, con un máximo de ~460px.
- **Label**: kickers y rótulos en mayúsculas en Space Grotesk 600 (nunca en Inter) con tracking de 0.05em, en gris pizarra sobre claro o gris niebla sobre oscuro. Los rótulos de las cifras bajan a 11px.

### Named Rules
**The Tight Headline Rule.** Todo titular en Space Grotesk 700 lleva un tracking de -0.02em y un line-height de 1.15–1.18. Los titulares no se escriben en Inter.

## Layout

- **Bandas a sangre** que alternan oscuro y arena, con el contenido dentro de contenedores de 1100px (footer y panel), 1200–1320px (blog y biblioteca) o 1400px (rejilla del problema).
- **Márgenes laterales en porcentaje**: 5% en la navbar, 6% en las secciones y 8% en el footer, en lugar de gutters fijos.
- **Secciones a pantalla completa**: el hero y el problema miden `min-height: max(640px, 100vh)`. Las demás secciones respiran con 100px verticales, que bajan a 70px en móvil.
- **Rejilla de cuadrantes**: la sección del problema es una rejilla de 2×2 a partir de 760px, con contenido arriba a la izquierda y abajo a la derecha. En móvil queda en una columna y las líneas desaparecen.
- **Breakpoints observados**: 760px (paso a dos columnas), 640px (tarjetas en una columna, panel más compacto) y 440px (navbar mínima).
- **Ritmo**: 16px entre tarjetas, 20px de relleno, 26–28px entre elementos de lista y navegación, 60px entre bloques grandes.

## Elevation & Depth

Es un sistema casi plano. La profundidad viene sobre todo del cambio de banda (arena frente a tinta) y de degradados radiales muy suaves que dan luz a una zona: el hero, el fondo del problema y el brillo superior del panel oscuro. Las sombras existen, pero son ambientales y apenas se notan.

### Shadow Vocabulary
- **Reposo de tarjeta** (`box-shadow: 0 2px 10px rgba(19,20,31,0.05)`): tarjetas de ventajas sobre arena.
- **Chip** (`box-shadow: 0 2px 6px rgba(19,20,31,0.1)`): cuadros de logo de herramientas.
- **Flotante** (`box-shadow: 0 8px 20px rgba(10,10,22,0.3)`): solo en hover, cuando el botón principal se eleva 2px sobre un fondo oscuro. Va tintada con noche profunda.

### Named Rules
**The Barely-There Rule.** Ninguna sombra en reposo supera un 10% de opacidad. Si una superficie necesita separarse más, cambia de tono (papel tarjeta o blanco), no de sombra.

## Shapes

El lenguaje es redondeado y amable, sin esquinas vivas en elementos interactivos ni contenedores:
- **Píldora** (100px): todos los botones y enlaces de acción.
- **Tarjeta** (16px): tarjetas de contenido y ventajas.
- **Chip** (14px) y **sm** (12px): cuadros pequeños y miniaturas.
- **Panel** (28px): bloques oscuros grandes dentro de una banda clara.
- **Círculo** (50%): avatares.

Los bordes son líneas de 1px con la tinta en alfa: 0.06 en tarjetas, 0.12 en divisores sobre claro, 0.15–0.18 sobre oscuro y 0.3 en el botón outline.

## Components

### Buttons
Cercanos y tranquilos: píldoras de texto corto y una sola acción por bloque.
- **Shape:** píldora completa (100px).
- **Primary:** fondo arena con texto en tinta nocturna, en Inter 600 de 16px y relleno de 16px × 32px. Vive sobre fondos oscuros (footer y panel), donde es la acción principal.
- **Ghost (sobre oscuro):** transparente con borde de arena al 45% y texto arena; en hover se rellena de arena. Acción secundaria del hero.
- **Outline:** transparente con borde de 1px en tinta al 30%, Inter 600 de 14px y relleno de 12px × 22px. Va sobre arena, con flecha «→» al final.
- **Hover:** el principal se eleva 2px con la sombra flotante (0.18s ease). El outline se rellena de tinta nocturna con texto arena (0.25s), igual que la paginación del blog. Los enlaces de la navegación y del footer bajan a una opacidad de 0.7.
- **Focus:** anillo `outline` de 2px a 4px de separación, del color del texto (en arena en el botón principal), y con forma de píldora en los botones.
- **Reduced motion:** sin elevación; se mantiene solo la sombra.

### Cards / Containers
- **Corner Style:** 16px.
- **Background:** papel tarjeta sobre arena.
- **Shadow Strategy:** reposo de tarjeta (ver Elevation & Depth).
- **Border:** 1px en tinta al 6%.
- **Internal Padding:** 20px. Sin numeración ni etiquetas encima: el H3 manda.

### Lista de caso real
Filas separadas por líneas de 1px en tinta al 12% (sin tarjetas): título en Space Grotesk 700 de 17px y una línea de Inter 15px al 78%. Se usa para contar qué hace una automatización en un cliente con nombre.

### Chips (herramientas)
- **Style:** cuadro blanco de 60×60px con radio de 14px y sombra de chip, con el logo de 34px centrado, seguido del nombre en Space Grotesk 600 de 30px.

### Navigation
- **Style:** fija y transparente sobre el hero, con logo y wordmark blancos a la izquierda y enlaces en Inter 500 de 15px en arena (zonas de pulsación de 44px) a la derecha, cerrando con una píldora outline «WhatsApp».
- **Behavior:** al bajar de 40px se vuelve sólida en tinta nocturna; se esconde al hacer scroll hacia abajo y vuelve al subir (0.35s).
- **Mobile (≤900px):** botón «Menú» en píldora que despliega un panel de tinta con los enlaces a 17px; Escape lo cierra. El logo mide 48px.
- **WhatsApp flotante (≤760px):** píldora de tinta centrada abajo, visible solo entre el hero y el pie.

### Dark Panel (biblioteca)
Bloque de tinta nocturna con radio de 28px dentro de una banda de arena, con un brillo radial de arena al 14% en la parte superior, el kicker, el titular, las cifras separadas por líneas verticales de 1px y el botón principal.

### Crosshair Grid (firma)
Dos líneas de 1px, horizontal y vertical, cruzan la sección al 50%. Van en arena al 18% sobre el hero oscuro y en tinta al 12% sobre arena. Son las marcas de trazado del taller: ordenan los cuadrantes sin dibujar cajas.

### Motion
- **Revelado:** `fadeUp` (de 28px a 0, opacidad de 0 a 1, 0.9s ease) en los titulares al entrar en pantalla.
- **Preloader:** solo en la primera visita de la sesión; el logo entra con una escala de 0.92 a 1 y la capa se funde a los 0.9s. Fuera del árbol de accesibilidad.
- **Vídeo del hero:** en bucle, silenciado y al 75% de velocidad. Versión de 480p en móvil y de 1280 en escritorio; no se carga con movimiento reducido ni ahorro de datos (queda el póster), se pausa fuera de pantalla y tiene botón de pausa redondo de 44px abajo a la derecha.
- **Movimiento reducido:** sin revelados, sin elevación y sin transiciones de la navbar.

## Do's and Don'ts

### Do:
- **Do** construir cada pantalla nueva con arena (`#F2EFE3`) como fondo y tinta nocturna (`#13141F`) como texto y banda oscura.
- **Do** usar Space Grotesk 700 con tracking de -0.02em en todo titular, e Inter en todo párrafo.
- **Do** usar píldoras de 100px para las acciones y radios de 16px para las tarjetas.
- **Do** tintar líneas, bordes y overlays con la tinta de la marca en alfa.
- **Do** mantener los párrafos en medidas cortas (420–560px) y los titulares por debajo de ~720px.
- **Do** repetir la retícula en cruz de 1px cuando una sección se organice en cuadrantes.

### Don't:
- **Don't** introducir un color de acento cromático (ni azules «tech» ni degradados de IA) sin una decisión explícita: el sistema es de dos tintas.
- **Don't** usar negro (`#000`) ni blanco puros para texto o fondos; lo más oscuro es noche profunda (`#0A0A16`) y el blanco queda reservado a los chips de herramientas.
- **Don't** usar sombras de más del 10% de opacidad en reposo ni elevar tarjetas para darles importancia.
- **Don't** usar esquinas vivas en botones o tarjetas.
- **Don't** acelerar el movimiento: las transiciones van entre 0.35s y 1.1s con ease, nunca con rebotes.
