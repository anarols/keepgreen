# ENCARGO — Rediseño de la Home de Keepgreen (desde cero)

Actúa como una agencia digital premium de eCommerce DTC: Director Creativo, UX
Researcher, UX/UI, Diseñador web eCommerce, especialista CRO, Brand Strategist,
Copywriter de hogar/decoración, Frontend senior y SEO técnico.

Web actual: https://keepgreen.es/   ·   Repo (vacío): github.com/anarols/keepgreen
Negocio: césped artificial premium en España, fabricante. Objetivo de la Home:
**captar leads** — Keepgreen trata "muestras gratis" y "presupuesto" como la MISMA acción.

═══════════════════════════════════════════════════════════════════
QUÉ QUIERO COMO RESULTADO
El entregable es **la maqueta HTML navegable de la nueva Home de Keepgreen**
(no un informe). Toda la investigación es trabajo de apoyo: resúmela en pocas
líneas y vuelca su valor en la maqueta. Lo que evalúo es el HTML, no documentos.

REGLAS DE ORO
1. No inventes nada de la marca ni del producto: color, tipografía, copy, logo y
   fotos deben venir de fuentes reales que tú observes. Si no puedes observarlo,
   dilo y pídemelo.
2. Los competidores y referentes son **solo referencia de ESTRUCTURA y ESTRATEGIA**.
   NUNCA copies su estética, su paleta ni su identidad visual. El estilo visual sale
   de la marca Keepgreen (propuesta A) o de una dirección propia y original (B).
3. No afirmes "no puedo ver webs": puedes leer el fuente con curl y renderizar/capturar.
4. Trabaja por fases; no declares nada "hecho" sin verificarlo (DOM/captura).
═══════════════════════════════════════════════════════════════════

## FASE 0 — INVESTIGACIÓN (rápida y al servicio de la maqueta)

### 0.1 — Lee la web actual a nivel VISUAL (no solo texto)
- Ábrela renderizada de verdad (navegador real o descarga y visualiza imágenes), en
  **desktop Y móvil** (~390px). Mira hero, secciones, cabecera, footer y móvil.
- Extrae del código (`curl -sL https://keepgreen.es/`) los **tokens reales**:
  tipografías (@font-face/font-family), variables `--color-*`, verde de marca, color
  de CTA/botones, texto, bordes. Descarga y MIRA el logo y las fotos reales.
- Quédate con: tokens reales, copy real (titulares, CTAs, claims, garantía, plazos,
  contacto) e inventario de fotos disponibles. (Resumen breve, no informe.)

### 0.2 — DESCUBRE a los mejores competidores y referentes (búscalos TÚ)
- Investiga en la web para IDENTIFICAR a los mejores; no esperes que yo te dé la lista:
  - Competidores directos líderes en España (césped artificial DTC), por visibilidad
    SEO, ads, volumen y reputación.
  - Referentes best-in-class internacionales (césped/jardín/exterior/hogar DTC) por
    excelencia de UX/CRO, aunque no compitan en España.
- Elige 5–8 y di brevemente por qué son los mejores. Parte de estos pero AMPLÍA:
  iberogarden.com · mercacesped.es · jardinartificial.es
- Pregúntame si quiero añadir o descartar alguno.

### 0.3 — Aprende de su ESTRUCTURA (no de su estética)
- Mapea de cada referente SOLO la estructura: arquitectura de información, qué
  secciones usa y EN QUÉ ORDEN, flujo de conversión, captación de lead (formulario,
  muestras, WhatsApp, chat), confianza, CTAs, CRO y móvil.
- Destila en 1–2 párrafos: patrones ganadores a adoptar, errores a evitar y "qué
  hacemos mejor". Esto define la arquitectura de nuestra Home; recuerda: tomamos la
  ESTRUCTURA como aprendizaje, el diseño visual es 100% Keepgreen/propio.

### 0.4 — Referencias de estética
- Apple, Stripe, Linear, Vercel, Framer, Notion: di en una línea qué principio tomar
  de cada uno y adáptalo a hogar/jardín (confianza, calidad, naturalidad, modernidad,
  sencillez, elegancia). Premium pero accesible. Inspiración, no copia.

→ Enséñame un resumen muy breve de la Fase 0 y sigue.

## FASE 1 — DOS MAQUETAS HTML, GENUINAMENTE DISTINTAS  (entregable principal)
Construye DOS páginas HTML completas y navegables, como dos estudios distintos
(NO el mismo layout con otro color):
- **A — "Marca actual, elevada":** fiel 100% a los tokens reales que extrajiste
  (misma tipografía, mismo verde, mismo color de CTA, logo real). Su mejor versión
  DTC. Respeta la lógica móvil actual.
- **B — "Rebrand premium":** otra tipografía, otra paleta, otro layout y otra
  personalidad. Riesgo creativo real y original (sin parecerse a ningún competidor).
Reglas comunes:
- HTML autónomo y navegable (fuentes e imágenes reales incrustadas para el preview).
- **Fotos reales siempre** (de Keepgreen); nada de placeholders de color.
- Arquitectura informada por la Fase 0: hero con formulario + CTA único dominante
  (muestras), prueba social arriba, problema→solución, beneficios, colección,
  comparativa de alturas (con las fotos reales de producto), proceso, bloque ancla de
  muestras, casos de uso, testimonios, FAQ, CTA final, footer. WhatsApp flotante +
  barra CTA sticky en móvil.
- Mobile-first; accesibilidad AA (contraste, foco visible, prefers-reduced-motion).
- Copy real orientado a conversión, en español de España.
- Verifica por DOM/captura (fuentes, colores, imágenes cargadas) y ábreme las dos.

→ Elijo dirección.

## FASE 2 — CÓDIGO DE PRODUCCIÓN (de la dirección elegida)
- Migra la maqueta elegida a Next.js (App Router) + Shopify headless + TailwindCSS.
  Semántico, responsive, SEO técnico (meta, Open Graph, schema Organization/Product/
  FAQ), Core Web Vitals. Listo para desplegar. Commits descriptivos + PR.

## ANTES DE EMPEZAR
Hazme las preguntas necesarias (branding, logo, fotos disponibles, tecnología) y, si
algo no puedes observarlo por ti mismo, pídemelo en vez de inventarlo.
