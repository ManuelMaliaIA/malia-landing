# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Dueños y gerentes de pymes locales de la provincia de Cádiz (Barbate y alrededores): comercios, hostelería y negocios de servicios. Llevan el negocio ellos mismos, van justos de tiempo y repiten a mano las mismas tareas cada día (papeleo, avisos, altas de clientes, documentos, seguimiento). Llegan a la web para entender si la automatización con IA les sirve a *ellos* y para decidir si hablan con Manuel. No son perfiles técnicos.

## Product Purpose

Malia diseña y monta automatizaciones de IA a medida que se encargan del trabajo repetitivo de una pyme, para que el dueño dedique su tiempo a hacer crecer el negocio. La web existe para convertir visitas en una primera conversación (consulta inicial gratuita y sin compromiso). Éxito: el visitante agenda una llamada o escribe.

## Positioning

- **Automatizaciones reales, no demos:** una biblioteca pública (`automatizaciones/`) enseña flujos completos que ya funcionan en clientes.
- **Trato directo con Manuel:** quien escucha el problema es quien lo construye; sin comerciales ni intermediarios.
- **Hecho a medida:** se adapta al proceso que ya tiene el negocio, no se fuerza una herramienta genérica.
- **Sin cuotas de SaaS:** n8n autoalojado (Easypanel/Hostinger), sin licencias caras por tarea.
- **Cercanía local:** está en Barbate y trabaja con negocios de la zona.

## Operating Context

- El cliente contacta por llamada, email o Instagram; la primera consulta es gratuita.
- Las automatizaciones se construyen en n8n con IA y se alojan en infraestructura propia (Easypanel sobre Hostinger).
- La biblioteca de automatizaciones y el blog los publica automáticamente el kit de n8n (`Kits/IMPORTANTES/kit-automatizaciones-n8n`), que hace commit y push al repo.

## Capabilities and Constraints

- Sitio estático (HTML/CSS/JS, sin framework ni build), repo `ManuelMaliaIA/malia-landing`, desplegado en Vercel; cada push a la rama por defecto se publica.
- `automatizaciones/` y `blog/` (incluidos sus `_template.html`) los genera el kit de n8n: no reorganizar carpetas ni plantillas sin actualizar ese kit.
- SEO: `sitemap.xml`, `robots.txt`, metadatos Open Graph; dominio `malia-ai-labs.com`.
- Idioma: español de España, tuteo.

## Brand Commitments

- Nombre: **malia** (en minúscula en la marca y el wordmark; "Malia" en textos legales). Handle de Instagram: `@malialabs_`.
- Voz: directa, cercana, sin jerga técnica; habla del tiempo perdido y del tiempo recuperado ("Automatiza lo repetitivo…", "Esto no es una demo — esto ya está funcionando").
- Recursos: wordmark y logo en `uploads/` (`malia-wordmark-blanco`, `logo-inverted`), avatar de Manuel (`uploads/avatar-round-*`), vídeo `2.mp4`.

## Evidence on Hand

- Clientes reales que se pueden nombrar: **MOTODEST**, **Mavimar** y **Vidal** (logos en la raíz y en `uploads/`).
- Hay o puede haber testimonios reales de estos clientes, pero **todavía no están en el repositorio**: usar solo citas literales que aporte Manuel; nunca inventarlas ni parafrasearlas como cita.
- Biblioteca de automatizaciones reales en `automatizaciones/` (casos MOTODEST, Vinted, vigilancia de marketplace, blog automatizado…). Cifras que muestra la home: 11 automatizaciones, 3 proyectos; deben coincidir con la biblioteca real.
- Blog en `blog/`.
- No hay precios publicados, casos con métricas de ahorro cuantificadas ni prensa: no inventarlos.

## Product Principles

1. **Enseñar en vez de prometer:** cada afirmación se apoya en una automatización real o en un cliente real.
2. **Hablar el idioma del dueño de la pyme:** tiempo, errores, clientes y dinero, no herramientas ni tecnicismos.
3. **Cercanía como ventaja:** una persona concreta y local que responde, no una plataforma anónima.
4. **Lo justo para el negocio:** soluciones a medida y sin costes recurrentes innecesarios.
5. **Un solo siguiente paso claro:** todo lleva a la primera consulta gratuita.
