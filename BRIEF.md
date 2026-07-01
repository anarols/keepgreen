# BRIEF — Rediseño de la Home de Keepgreen (para Claude Code)

Actúa como una agencia digital premium especializada en eCommerce DTC de alto
rendimiento (Director Creativo + UX/UI + CRO + Copywriter + Frontend senior).
Objetivo de negocio: **maximizar la captación de leads** (Keepgreen trata
"solicitar muestras" y "pedir presupuesto" como LA MISMA acción).

## MÉTODO OBLIGATORIO (no adivinar nunca la marca)
1. Antes de diseñar nada, EXTRAE los datos reales:
   - `curl -sL https://keepgreen.es/ -o home.html` y busca en el código:
     tipografías (`@font-face`/font-family), variables `--color-*`, logo, copy real.
   - Descarga y **mira** el logo y las fotos con la herramienta Read antes de usarlas.
   - Descarga las fuentes reales (woff2) e inclúyelas inline (base64) en los previews.
2. Si algo no se puede ver con texto, usa el navegador real o pide una captura.
   NO afirmar "no puedo ver webs": se puede leer el fuente con curl.
3. Verifica el resultado por DOM (fuentes, colores, imágenes cargadas) antes de entregar.

## TOKENS DE MARCA REALES (usar tal cual en la propuesta "marca actual")
- Tipografía: **Montserrat** (400/500/600); titulares letter-spacing -0.02em.
- Texto `#2c2d2e` · Titulares `#1a1c1d` · Fondo `#ffffff` / `#f7f7f7`.
- **Verde de marca `#4c8032`** (identidad: barra, acentos, iconos).
- **CTA / botones magenta `#ed0069`** (hover `#c90059`, texto blanco). El verde es
  identidad; el magenta es el color de conversión. ¡No los confundas!
- Estrellas `#FFAA47` · borde `#DADCE0`.
- Logo: pájaro VERDE + "keep" (oscuro) + "green" (verde) →
  https://keepgreen.es/cdn/shop/files/logo-keepgreen.png
- Garantía **10 años** de fabricante · muestras grandes GRATIS en 48 h (no se
  devuelven) · envío gratis desde 160€ · 10 centros físicos · fabricante e instalador.
- Modelos (30–45 mm): Jilguero 30, Ruiseñor 35, Kiwi 38, Cuco 40, Albatros 42, Flamenco 45.
- Contacto: tel 96 540 38 11 · WhatsApp +34 865 614 188 · hola@keepgreen.es · Crevillent (Alicante).
- Copy real de referencia: "Empieza a disfrutar de tus espacios de exterior",
  "Quiero presupuesto y muestras GRATIS", "míralo, tócalo y pruébalo en casa".

## ACTIVOS REALES (Shopify CDN, prefijo https://keepgreen.es/cdn/shop/files/)
- Héroe (lifestyle, chalet+piscina): cesped-artificial-keepgreen-Desktop.webp
- Fotos de producto (perfil de corte sobre blanco; sirven para colección Y para
  una comparativa de alturas real): cesped-artificial-{jilguero,ruisenor,kiwi,
  cuco-vista-2_1,albatros,flamenco}-vista-2.webp
- (No hay fotos de instalaciones extra; reutiliza recortes del héroe para casos de uso.)

## ENTREGABLE: DOS PROPUESTAS GENUINAMENTE DISTINTAS
No es un mismo diseño con otro color: deben ser dos conceptos como de dos estudios.
- **A — "Marca actual, elevada":** fiel 100% a los tokens de arriba (Montserrat,
  blanco, verde + CTA magenta, logo real). Layout DTC premium tipo Apple/Stripe.
- **B — "Rebrand premium":** otra tipografía (p. ej. serif editorial), otra paleta
  (sin magenta), otro layout (editorial/revista, tipografía grande). Riesgo creativo.
- Cada una es una página completa y separada (no un interruptor de colores).
- Usa SIEMPRE fotos reales; nada de bloques placeholder de color.

## REQUISITOS
- Mobile-first y responsive; respeta la lógica móvil actual en la propuesta A.
- Accesibilidad AA (contraste, foco visible, prefers-reduced-motion).
- Estructura de Home: hero con formulario + CTA único dominante (muestras),
  prueba social arriba, problema→solución, beneficios, colección, comparativa de
  alturas, proceso, bloque ancla de muestras, casos de uso, testimonios, FAQ
  (schema), CTA final, footer. WhatsApp flotante + barra CTA sticky en móvil.
- Tono: cercano, experto, premium pero accesible.

## TECNOLOGÍA Y CÓDIGO (fase final, tras elegir dirección)
- Next.js (App Router) + Shopify headless. TailwindCSS. SEO técnico, meta tags,
  Open Graph, schema (Organization, Product, FAQ). Core Web Vitals.
- Repo: github.com/anarols/keepgreen (estaba vacío → construir desde cero).
- Entregar: estrategia (auditoría/copy/wireframe/CRO) + las dos propuestas
  navegables + código de la dirección elegida, listo para desplegar.

## ERRORES A EVITAR (cometidos en una sesión previa)
- Inventar paleta/tipografía (se puso negro+Segoe; lo real es blanco+Montserrat+#4c8032+#ed0069).
- Dibujar un logo falso en vez de usar el real.
- Presentar "dos propuestas" que son el mismo layout con otro color.
- Usar placeholders en vez de las fotos reales (que sí existen en el CDN).
- Cambiar el móvil de la propuesta fiel sin necesidad.

## FLUJO
1. Extrae datos reales (curl + Read del logo/fotos). 2. Define estrategia breve.
3. Construye A (fiel) y B (rebrand) con fotos reales, verifica por DOM.
4. Enséñalas y pregunta cuál elige. 5. Pule la elegida y construye el código.
