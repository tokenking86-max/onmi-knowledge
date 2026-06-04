# ONMI Reality Check v1.0 — Auditoría Crítica Ejecutiva

> **Auditor:** JARVIS (COO) — actuando como Director de Producto + Director Comercial
> **Documentos auditados:** `architecture-strategic-blueprint.md` (863 líneas) + `onmi-visual-system-v1.md` (~1,836 líneas)
> **Contexto estratégico:** ReFoundation 2026 — empresa en fase pre-ingresos, pipeline vacío, 0 proyectos
> **Fecha:** 2026-06-03
> **Propósito:** Identificar contradicciones, supuestos no validados, riesgos comerciales y elementos artificiales antes de iniciar implementación frontend

---

## Resumen ejecutivo

ONMI ha producido ~2,700 líneas de planificación estratégica y diseño visual para un sitio web corporativo. La calidad del pensamiento es alta, la inspiración en benchmarks correcta, y la coherencia interna entre documentos es notable para una primera iteración.

**El problema:** Estos documentos fueron escritos como si ONMI fuera una consultora establecida con 3-5 clientes, 2-3 especialistas en red, y un pipeline activo. No es el caso. ONMI es un fundador con una laptop, un dominio por registrar, y cero ingresos.

**Hallazgos totales:** 24
- 🔴 **Críticos:** 6
- 🟡 **Importantes:** 12
- 🟢 **Menores:** 6

**Veredicto del Reality Check:** Los documentos son sólidos como **visión aspiracional**, pero peligrosos como **plan de implementación inmediato**. Si se ejecutan tal cual, el sitio web resultante será un hermoso escaparate de una empresa que no existe. Se requiere un **recorte quirúrgico** antes de escribir la primera línea de código.

---

## 🔴 Hallazgos Críticos

### 🔴 C1 — El sitio está diseñado para una empresa que no existe
**Documento:** Ambos documentos (transversal)
**Líneas:** Blueprint Sec 3.2, Visual System Sec 3.1-3.7 completos

**Hallazgo:** La arquitectura de información especifica 26 páginas (17 principales + 6 funcionales + 3 auxiliares). El sistema visual detalla layouts para cada una: Home Desktop, Home Mobile, Servicios Hub, Servicio Individual (x8), Blog Hub, Artículo de Blog, Contacto. Se mencionan "logos de clientes", "testimonios", "casos de éxito", "equipo de especialistas", "sección de confianza".

**Riesgo:** ONMI no tiene clientes, no tiene testimonios, no tiene casos de éxito reales, no tiene especialistas en red, y los únicos logos de confianza que puede mostrar son certificaciones del fundador. El sitio tendrá secciones vacías o rellenas con contenido genérico que cualquier CTO detectará inmediatamente como humo.

**Corrección propuesta:**
- Reducir a ONE-PAGE + Blog + Contacto (3 páginas, no 26)
- Eliminar toda sección que no se pueda llenar con contenido real hoy
- "Casos de éxito" → reemplazar con "Casos conceptuales" (1-2, claramente etiquetados como "ejemplo de cómo abordaríamos X problema")
- "Equipo" → reemplazar con "Conoce al arquitecto" (una sola persona)
- "Red de especialistas" → no mencionar hasta tener 3 contratos firmados

---

### 🔴 C2 — Ocho servicios en catálogo, dos servicios entregables
**Documento:** Blueprint Sec 3.3, 4.1
**Líneas:** ~276-286, ~340-376

**Hallazgo:** El sitemap incluye páginas individuales para los 8 servicios (QC-01, QC-02, QC-03, GC-01, GC-02, GC-03, ST-01, ST-02). El Visual System diseña la página individual de servicio como un layout completo con hero, entregables, metodología, pricing, y CTA.

**Riesgo:** De estos 8 servicios, solo QC-01 y QC-02 son realmente entregables por Alan solo en los próximos 3 meses. QC-03 (Due Diligence para VC) requiere relaciones con fondos que no existen. GC-01/02/03 requieren especialistas que no están contratados. ST-01/02 requieren clientes y proyectos previos que no existen. Publicar páginas individuales para servicios no entregables es: (a) engañoso, (b) genera consultas que no se pueden atender, (c) obliga a decir "ese servicio aún no está disponible".

**Corrección propuesta:**
- Fase 1: Solo páginas para QC-01 y QC-02 (los dos servicios realmente vendibles)
- Los otros 6 servicios → mencionados en una sección "Próximamente" o "Servicios avanzados" sin página individual
- A medida que cada servicio se valide con un proyecto real, se crea su página

---

### 🔴 C3 — Supuesto no validado: CTOs de regulados llegan por SEO y descargan lead magnets
**Documento:** Blueprint Sec 6 (SEO), Sec 7.3 (Lead Magnets), Sec 7.4 (Nurturing)
**Líneas:** ~468-497, ~652-665, ~670-702

**Hallazgo:** Toda la estrategia de conversión asume que CTOs y CISOs de empresas reguladas encuentran ONMI por búsqueda orgánica (keywords como "arquitectura ai-native para fintech reguladas"), leen artículos de blog, descargan lead magnets, y entran a un nurturing sequence de 30 días que termina en una solicitud de contacto.

**Riesgo:** Los CTOs de fintech y banca en LATAM no buscan consultores en Google para problemas de arquitectura AI-Native. Los encuentran por: (a) referidos de otros CTOs, (b) LinkedIn directo, (c) eventos/conferencias, (d) relaciones previas. La intención de búsqueda para "arquitectura ai-native" es cercana a cero (el propio blueprint la marca como "muy baja"). Todo el inbound marketing asume un comportamiento de compra B2C para un producto B2B enterprise de alto ticket ($8K-$130K).

**Corrección propuesta:**
- Redimensionar SEO a "presencia mínima" (bien hecho, pero no prioritario)
- Pasar la inversión de contenido a LinkedIn direct outreach (lo que realmente genera leads)
- Eliminar o simplificar drásticamente la nurturing sequence de 30 días (no hay leads que nutrir)
- Lead magnets: solo 1 (AI Maturity Model), sin gating agresivo. Un CTO no da su email corporativo a un sitio desconocido.

---

### 🔴 C4 — Pricing público para una firma sin track récord
**Documento:** Blueprint Sec 4.2 (línea 376), Visual System Sec 2.7 (Service Card metadata) y Sec 3.4 (badges con precio)
**Líneas:** Blueprint ~375-377, Visual System ~882-884, ~1329

**Hallazgo:** El Blueprint recomienda NO publicar precios ("publicar precios puede trivializar el servicio y desencadenar comparaciones incorrectas"). Sin embargo, el Visual System diseña tarjetas de servicio que incluyen "metadata: precio y duración" como elemento estándar, y la página de servicio individual muestra badges con "$8K-$15K".

**Riesgo:** Para una empresa nueva sin casos de éxito ni referencias, mostrar "$8K desde" es contraproducente:
- Si parece caro → "¿8K por un diagnóstico de una empresa que no conozco?"
- Si parece barato → "¿Solo 8K? ¿Qué profundidad puede tener?"
- Un CTO experimentado sabe que $8K por un assessment de 2 semanas de un solo consultor en realidad equivale a ~$500/hora, que es caro para el mercado si no hay marca.
- Ancla el precio hacia abajo: si el valor real del servicio es $12K-$15K, el "$8K desde" será el único número que recuerde el comprador.

**Corrección propuesta:**
- NO publicar precios en el sitio web v1
- Reemplazar con un CTA que lleve a contacto donde se discuta pricing contextual
- La excepción: si se valida con clientes reales que el precio es un facilitador de conversión, se puede añadir después (con datos, no con teoría)

---

### 🔴 C5 — El plazo de implementación asume recursos que no existen
**Documento:** Blueprint Apéndice A (Sec 10)
**Líneas:** ~810-842

**Hallazgo:** El plan de implementación tiene 3 fases: Fase 1 (Semana 1-2) = MVP One-Page, Fase 2 (Semanas 3-6) = Sitio completo con 8 páginas de servicio + casos + blog + recursos, Fase 3 (Semanas 7-12) = Optimización, analytics, A/B testing, etc.

**Riesgo:** No hay desarrollador frontend asignado. No hay diseñador. No hay presupuesto para agencia. El plan asume que "alguien" implementa un sistema de 23 tokens CSS, 7 layouts responsive, animaciones, formularios con validación, integración de analytics, schema markup, CMS headless, etc. en 6 semanas. Para un desarrollador frontend solo, esto es 3-4 meses a tiempo completo. Para Alan (que debería estar vendiendo), es imposible.

**Corrección propuesta:**
- Reemplazar el plan de 12 semanas con un plan de 2 semanas para ONE-PAGE funcional
- Eliminar Fase 2 y Fase 3 del roadmap inmediato
- Aplazar todo el sistema visual completo hasta que ONMI tenga: (a) primer proyecto cerrado, (b) primer caso de estudio real, (c) pipeline de leads >5
- Considerar: ¿y si el sitio web nunca es la prioridad? Un one-page + LinkedIn bien gestionado puede generar más leads que un sitio de 26 páginas.

---

### 🔴 C6 — Contradicción "Mobile-first" vs implementación desktop-first
**Documento:** Blueprint Sec 3.1 (línea 228), Visual System Sec 3 (todo)
**Líneas:** Blueprint ~228, Visual System ~1025-1598

**Hallazgo:** El Blueprint dice "Mobile-first en pensamiento, aunque el contenido técnico se consuma más en desktop". Pero el Visual System dedica ~500 líneas a layouts de desktop detallados y apenas ~50 líneas a variantes mobile (que además se presentan como notas al pie: "Layout Mobile — cambios:"). Las especificaciones de spacing, hero height (80vh), grid de 3 columnas, sidebar en blog, layout de 2 columnas en contacto — todo parte de desktop y mobile se trata como "colapsar a 1 columna".

**Riesgo:** Mobile-first no es una preferencia, es cómo Google indexa y cómo muchos compradores B2B consumen contenido inicial (LinkedIn → click → mobile). Si el diseño nace desktop, mobile será un afterthought con decisiones apresuradas. Además, un CTO que ve el site en LinkedIn mobile antes que en desktop tendrá una experiencia subóptima.

**Corrección propuesta:**
- Rediseñar el proceso: empezar por mobile layout, expandir a desktop
- Simplificar la complejidad: si mobile funciona bien con menos elementos, considerar si esos elementos sobran también en desktop
- 80vh hero en mobile es enorme para un celular — ocuparía toda la pantalla sin mostrar contenido real

---

## 🟡 Hallazgos Importantes

### 🟡 I1 — La "red de especialistas" se presenta como existente
**Documento:** Blueprint Sec 5.7 (Nosotros), Visual System Sec 3.1 (Trust section)
**Líneas:** Blueprint ~442, Visual System ~1080-1086

**Hallazgo:** La página "Sobre ONMI" incluye "Red de especialistas (fotos + expertise)" y la sección de confianza en Home muestra "Quién confía en ONMI" con "Grid de logos".

**Riesgo:** ONMI no tiene especialistas contratados ni logos de clientes corporativos. Mostrar una sección de "equipo" con una sola persona (Alan) y el resto "próximamente" es peor que no tenerla. El visitante pensará "esto es una persona, no una consultora".

**Corrección:** Reemplazar "Equipo" con "El Arquitecto" — una página personal de Alan con su CV, certificaciones y foto. La red de especialistas se menciona como "colaboradores on-demand" solo cuando existan. Los logos de confianza = certificaciones cloud del fundador + logos de empresas donde trabajó (con permiso, como "experiencia previa del fundador").

---

### 🟡 I2 — Sobre-ingeniería del sistema visual para estado actual
**Documento:** Visual System Sec 2.1-2.9 (Design System)
**Líneas:** ~444-1020

**Hallazgo:** El Design System especifica: 23 tokens de color, 13 de spacing, 5 de border radius, 4 niveles de sombra dark y light, 4 variantes de botón × 3 tamaños × 5 estados, 7 variantes de input × 6 estados, 6 tipos de tarjeta, 3 tamaños de badge × 6 variantes, especificaciones de tabla con scroll horizontal y conversión responsive a cards.

**Riesgo:** Este nivel de granularidad es apropiado para un producto SaaS con equipo de diseño. Para un sitio web corporativo de consultora (especialmente one-page), es excesivo. Cada token, cada variante, cada estado es tiempo de implementación que no genera ingresos.

**Corrección:** Implementar solo el subset mínimo viable: 1 botón (primary, un tamaño), 2 inputs (text + textarea), 2 tipos de card (default + service), 2 badges. El resto se añade cuando haya pages que lo requieran. Principio: "No diseñes lo que no vas a construir en las próximas 2 semanas."

---

### 🟡 I3 — Tono "consultora boutique" vs realidad de una persona
**Documento:** Blueprint Sec 8 (Mensajes principales)
**Líneas:** ~724-806

**Hallazgo:** Los mensajes dicen "No somos una agencia. Somos arquitectos que han hecho esto en banca y fintech", "Hablas con el arquitecto. No con un account manager. No con un junior. Decisiones directas, sin capas", "El mismo nivel de expertise que una big consultancy, pero boutique, ágil y a precio razonable."

**Riesgo:** Este tono es aspiracionalmente cierto pero actualmente engañoso. "Somos arquitectos" (plural) cuando es un arquitecto. "Decisiones directas sin capas" cuando no hay capas porque no hay equipo. No es incorrecto, pero el plural corporativo ("hemos hecho", "nuestros casos") se siente falso cuando el visitante ve que la empresa tiene 0 empleados. Un CTO experimentado detecta esto en segundos.

**Corrección:** Usar primera persona singular donde corresponda ("He diseñado arquitecturas para..."), y reservar el plural para cuando ONMI tenga >1 persona. La honestidad radical es más efectiva que la ficción corporativa: "Soy Alan. Soy el arquitecto. No tengo un equipo de 20, pero los 20 años de experiencia que tengo los pongo todos en tu proyecto."

---

### 🟡 I4 — Lead magnets que no existen
**Documento:** Blueprint Sec 7.3
**Líneas:** ~652-665

**Hallazgo:** La estrategia lista 6 lead magnets: AI Maturity Model v1.0, Checklist de readiness, Guía de AI Governance, Template de Risk Assessment, Whitepaper de AI Agents, Strategy Roadmap Canvas. Todos con fechas de disponibilidad desde "Día 1" hasta "Semana 16".

**Riesgo:** De estos 6, ninguno existe hoy. El AI Maturity Model está "en diseño" (según MEMORY.md). El resto no ha empezado. Publicar un sitio con "Descarga nuestro AI Maturity Model" y que el link lleve a un formulario que envía un PDF inexistente es la forma más rápida de matar la confianza con un lead.

**Corrección:** No publicar ningún lead magnet hasta que esté escrito, diseñado y alojado. Empezar con 1 (el checklist de readiness, que es rápido de producir). Añadir los demás cuando estén listos.

---

### 🟡 I5 — Estrategia de contenido sin capacidad de producción
**Documento:** Blueprint Sec 6.4
**Líneas:** ~545-560

**Hallazgo:** El calendario de contenido propone 6 artículos en 90 días (uno cada 2 semanas) + frameworks descargables + análisis regulatorios + guías técnicas. Total estimado: ~8-10 piezas de contenido en 90 días.

**Riesgo:** Producir un artículo técnico de alto nivel (tipo "Arquitectura AI-Native para Fintech Reguladas") requiere 8-15 horas de investigación, escritura, revisión y edición. Multiplicado por 10 piezas = 80-150 horas. En los mismos 90 días, Alan debe: constituir la empresa, prospectar 20+ CTOs, cerrar primer proyecto, entregar primer proyecto, identificar especialistas, redactar contratos, configurar herramientas. El contenido será la primera víctima.

**Corrección:** Reducir a 1 artículo cada 2-3 semanas (3-4 artículos en 90 días). Reutilizar en LinkedIn (un artículo = 5 posts). Priorizar calidad sobre cantidad. No comprometer contenido que distraiga de la prospección.

---

### 🟡 I6 — Sin flujo de compra enterprise
**Documento:** Blueprint Sec 7 (Estrategia de conversión)
**Líneas:** ~580-720

**Hallazgo:** La estrategia de conversión asume que el visitante: llega → consume contenido → descarga lead magnet → recibe nurturing → agenda llamada → compra. No hay mención a: proceso de procurement, NDA previo, revisión legal de propuesta, llamada con compliance, aprobación de directorio, due diligence del proveedor.

**Riesgo:** Las empresas reguladas NO compran consultoría de $8K-$130K por un formulario web. Requieren: (a) evaluación de proveedor (b) compliance check del vendor (c) aprobación de riesgo (d) NDA (e) propuesta formal (f) orden de compra (g) contrato revisado por legal. Ignorar esto significa que los leads que lleguen por el sitio se enfriarán cuando descubran el proceso real.

**Corrección:** Añadir en la página de contacto o servicios una nota realista sobre el proceso: "Trabajamos con empresas reguladas. Si necesitas NDA o procurement, contáctanos y te guiamos." Preparar una one-pager de "vendor onboarding" que un CISO pueda usar para evaluar a ONMI como proveedor.

---

### 🟡 I7 — Dark mode como default sin validación corporate
**Documento:** Blueprint Sec 2.1 (líneas 151-155), Visual System Sec 1.6
**Líneas:** Blueprint ~151-155, Visual System ~394-438

**Hallazgo:** La decisión de dark mode como default está justificada visualmente (benchmarking con Stripe, Vercel, Linear, Palantir). Pero no hay validación con el buyer persona real: CTOs, CISOs y procurement de empresas reguladas LATAM. Muchos entornos corporativos usan herramientas con temas claros, y algunos proxies/bloqueadores corporativos tienen problemas con sitios dark-mode-first.

**Riesgo:** El CTO de un banco abre el link en su laptop corporativa con perfil de navegación restringido. El sitio se ve mal. O peor: no se renderiza correctamente porque el proxy corporativo aplica estilos que rompen el dark mode. O simplemente: el CTO prefiere light mode y el cambio no es obvio.

**Corrección:** Mantener dark mode como default pero: (a) asegurar que light mode sea igual de bueno (probado), (b) el toggle debe ser visible inmediatamente, no escondido en footer, (c) probar en 3 entornos corporativos reales antes de lanzar, (d) considerar que el sitio cargue en el modo que el sistema del usuario tenga configurado (prefers-color-scheme media query).

---

### 🟡 I8 — Nurturing sequence de 30 días diseñada sin leads
**Documento:** Blueprint Sec 7.4 (líneas 693-701)
**Líneas:** ~670-719

**Hallazgo:** Se especifica una secuencia de 6 correos en 30 días: Día 1 (bienvenida + contenido), Día 3 (caso de éxito), Día 7 (artículo técnico), Día 14 (invitación a llamada), Día 21 (oferta QC-01), Día 30 (newsletter). Y 5 segmentos de lead con diferentes frecuencias.

**Riesgo:** Esto requiere: herramienta de email marketing configurada, CRM integrado, contenido para cada touchpoint, segmentación funcional, y leads que alimentar. No hay leads, no hay CRM, no hay contenido. Diseñar una secuencia de nurturing antes de tener el primer lead es como diseñar un protocolo de atención al cliente para un negocio que no ha abierto.

**Corrección:** Eliminar la secuencia de nurturing del plan inmediato. Reemplazar con: "Cuando llegue un lead, Alan responde personalmente en <24h." Punto. La automatización de nurturing se justifica cuando ONMI tenga >10 leads en pipeline y >3 en nurturing.

---

### 🟡 I9 — 3 conceptos de logo con especificaciones geométricas para una consultora de 1 persona
**Documento:** Visual System Sec 1.1
**Líneas:** ~76-134

**Hallazgo:** Se diseñaron 3 conceptos de logo: "El Nodo Arquitectónico" (recomendado), "La Arista Fundacional", "El Compás Digital". Cada uno con especificaciones detalladas: isotipo, logotipo, variantes horizontal/vertical, favicon, área de protección, tamaño mínimo, usos incorrectos. El concepto recomendado incluye ángulos de 120°, barras con extremos redondeados de 2px, y una visualización textual del isotipo con arte ASCII.

**Riesgo:** Este proceso de diseño de marca es apropiado para una empresa que busca inversión de $500K+. Para una consultora bootstrapped que necesita generar $30K en 90 días, 3 conceptos de logo con 12 variantes cada uno es una distracción monumental. El logo no vende consultoría — el CV del fundador vende consultoría.

**Corrección:** Elegir el Concepto 1 (el mejor de los 3) y pasar directamente a vectorización. No iterar más. Si en 6 meses ONMI tiene ingresos y casos de éxito, se puede considerar un refinamiento de marca. Hoy, un logo "suficientemente bueno" es infinitamente mejor que un logo perfecto que retrasa el lanzamiento.

---

### 🟡 I10 — Estrategia de contenido SEO sin considerar que Google no recompensa la autoridad no probada
**Documento:** Blueprint Sec 6
**Líneas:** ~466-577

**Hallazgo:** La estrategia SEO asume que crear contenido de alta calidad sobre "arquitectura ai-native para fintech" posicionará a ONMI en Google. Keywords como "arquitectura ai-native" tienen volumen de búsqueda "muy bajo". Las keywords de cola larga tienen intención transaccional alta pero cero volumen de búsqueda.

**Riesgo:** El SEO para consultoría B2B especializada es extremadamente lento (6-18 meses para ver resultados). Google prioriza autoridad de dominio, backlinks de sitios relevantes, y señales de marca. ONMI tiene dominio nuevo, cero backlinks, cero menciones. Publicar 6 artículos no cambiará esto. Invertir en SEO como estrategia de adquisición primaria en los primeros 6 meses es una mala asignación de recursos.

**Corrección:** Reducir SEO a lo básico (meta tags, sitemap, technical SEO correcto) pero NO depender de él para generar leads. El contenido debe ser: (a) para posicionar a Alan como autoridad en LinkedIn, (b) para tener algo que compartir en outreach, (c) para que los leads existentes profundicen. No para atraer tráfico orgánico.

---

## 🟢 Hallazgos Menores

### 🟢 M1 — Hreflang planificado para Q2 2027
**Documento:** Blueprint Sec 6.5 (línea 572)
**Línea:** ~572

**Hallazgo:** "Evaluar inglés en Q2 2027 si hay demanda."

**Corrección:** Totalmente razonable como nota futura. No implementar. Asegurar que la arquitectura técnica lo permita sin costo adicional ahora (ej: usar Next.js App Router que soporta i18n por diseño).

---

### 🟢 M2 — Schema markup detallado para organización sin actividad
**Documento:** Blueprint Sec 6.5 (línea 568)
**Línea:** ~568

**Hallazgo:** Se lista implementar schema de Organization, ProfessionalService, BlogPosting, FAQPage, Article, Product.

**Corrección:** Implementar solo Organization y BlogPosting. ProfessionalService y Product requieren datos (precios, reseñas, inventory) que no existen. Un schema markup con datos genéricos no aporta valor SEO y puede ser marcado como incompleto por Google.

---

### 🟢 M3 — Animaciones complejas (glow effects, glassmorphism)
**Documento:** Visual System Sec 2.4 (sombra glow), Sec 2.7 (Testimonial Card glassmorphism)
**Líneas:** ~676-680, ~923-933

**Hallazgo:** Se especifican efectos visuales avanzados: glow en botones primarios, glassmorphism en tarjetas de testimonio, sticky progress bar en artículos.

**Corrección:** Eliminar en v1. Estos efectos añaden complejidad de implementación (especialmente glassmorphism cross-browser) para cero beneficio de conversión. Un botón sin glow funciona igual. Implementar glow solo después de que A/B testing demuestre que mejora conversión.

---

### 🟢 M4 — 404 page y Gracias page diseñadas antes que el producto
**Documento:** Blueprint Sec 5.9
**Líneas:** ~456-462

**Hallazgo:** Páginas de 404 y Gracias especificadas con layouts, contenido y CTAs personalizados.

**Corrección:** Estas páginas toman 30 minutos implementarlas con una plantilla genérica adaptada. No necesitan diseño personalizado en v1. Una página Gracias que confirme el envío y redirija al contenido principal es suficiente.

---

### 🟢 M5 — "Trust section" sin trust real
**Documento:** Visual System Sec 3.1 (líneas 1080-1086)
**Líneas:** ~1080-1086

**Hallazgo:** Sección titulada "Quién confía en ONMI" con grid de logos.

**Corrección:** Cambiar título a "Experiencia del arquitecto" o "Certificaciones". Si se incluyen logos de empleadores previos de Alan, etiquetar claramente como "Experiencia profesional previa del fundador." No sugerir que son clientes de ONMI.

---

### 🟢 M6 — El checklist de implementación asume 10 días de desarrollo
**Documento:** Visual System Apéndice B
**Líneas:** ~1789-1831

**Hallazgo:** El checklist tiene 4 fases (Fundaciones → Componentes base → Layouts → Refinamiento) estimadas en 10 días totales.

**Corrección:** Esta estimación es para un desarrollador frontend experimentado trabajando full-time con el design system ya traducido a código. Si lo hace Alan, multiplicar por 3-4x. Ajustar expectativas realistas.

---

## Análisis de Contradicciones entre Documentos

| # | Documento A | Documento B | Contradicción | Severidad |
|---|-------------|-------------|---------------|-----------|
| 1 | Blueprint: "8 servicios" con páginas individuales | ReFounding: solo 2 servicios realmente entregables | El catálogo promete servicios que no existen | 🔴 |
| 2 | Blueprint: "Mobile-first" | Visual System: 95% del diseño es desktop-first | Estrategia vs implementación | 🔴 |
| 3 | Blueprint: "No incluir página de precios" | Visual System: badges de precio prominentes en service cards | Política de pricing vs diseño visual | 🟡 |
| 4 | Blueprint: "Fase 1 = MVP One-Page en 2 semanas" | Visual System: 7 layouts completos + 26 páginas | El alcance del diseño excede la fase 1 del blueprint | 🔴 |
| 5 | Blueprint: "Lead magnet requiere nombre+email+empresa" | Visual System: solo email input en lead magnet inline | Fricción de captura de leads | 🟢 |
| 6 | ReFounding: "Especialistas: 3 contratables" | Blueprint: "Red de especialistas con fotos + expertise" | La red no existe | 🟡 |
| 7 | ReFounding: Prioridad #2 = "LinkedIn outreach a 20 CTOs" | Blueprint: 150+ horas en contenido SEO | Estrategia de canales contradictoria | 🟡 |

---

## Mapa de Acción Priorizada

| Prioridad | Hallazgo | Acción | Responsable | Plazo |
|-----------|----------|--------|-------------|-------|
| P0 | 🔴 C1 — Sitio para empresa que no existe | Recortar a one-page + blog + contacto | JARVIS + Alan | Antes de implementar |
| P0 | 🔴 C2 — 8 servicios, 2 entregables | Solo páginas para QC-01 y QC-02 | JARVIS | Antes de implementar |
| P0 | 🔴 C5 — Plazo irreal de implementación | 2 semanas one-page, no 12 semanas full-site | JARVIS | Re-planificar ahora |
| P1 | 🔴 C3 — Estrategia de conversión irrelevante | Reemplazar inbound con LinkedIn outreach como canal primario | Alan | Esta semana |
| P1 | 🔴 C4 — Pricing público | Eliminar precios del site. Usar "contactar para presupuesto" | JARVIS | Antes de implementar |
| P1 | 🟡 I4 — Lead magnets inexistentes | No publicar lead magnets que no existen. Empezar con 1 | JARVIS | Cuando haya contenido |
| P2 | 🔴 C6 — Mobile-first de mentira | Rediseñar layouts mobile-first | JARVIS | En implementación |
| P2 | 🟡 I1 — Red de especialistas | Convertir "Equipo" en "El Arquitecto" (página personal) | JARVIS | Antes de implementar |
| P2 | 🟡 I2 — Sobre-ingeniería visual | Implementar subset mínimo de componentes | Desarrollador | En implementación |
| P2 | 🟡 I5 — Contenido irreal | Reducir de 10 a 3-4 piezas en 90 días | JARVIS + Alan | Ajustar calendario |
| P3 | 🟡 I3 — Tono aspiracional engañoso | Usar primera persona singular. Ser honestamente one-person | JARVIS | En copywriting |
| P3 | 🟡 I6 — Sin flujo enterprise | Añadir nota realista sobre proceso de procurement | JARVIS | En copywriting |
| P3 | 🟡 I7 — Dark mode sin validación | Probar en entornos corporativos. Toggle visible | Desarrollador | Antes de lanzar |
| P3 | 🟡 I8 — Nurturing prematuro | Eliminar automated nurturing. Respuesta humana <24h | JARVIS | Ahora |
| P4 | 🟡 I9 — 3 logos conceptuales | Elegir 1, vectorizar, pasar a lo siguiente | JARVIS | Esta semana |
| P4 | 🟡 I10 — SEO como estrategia | Mantener SEO básico, no invertir más hasta tener tracción | JARVIS | Ahora |

---

## Veredicto Final del Director de Producto

**El Strategic Blueprint es un documento sobresaliente... como referencia de mediano plazo (meses 6-12).**

**El Visual System es un documento impresionante... para cuando ONMI tenga su primer caso de éxito.**

**Ambos documentos juntos son peligrosos si se implementan ahora porque:**
1. Crean la ilusión de una empresa que no existe
2. Consumirán 3-4 meses de desarrollo que deberían ser de ventas
3. Generarán leads que no se pueden atender con servicios que no existen
4. El resultado será un hermoso cascarón vacío

### Recomendación ejecutiva

**No implementes el sitio completo. No implementes el design system completo. No construyas 26 páginas.**

Haz esto:
1. **One-page en 2 semanas** — Home con propuesta de valor + QC-01 + QC-02 + Blog listado (1 artículo) + Contacto
2. **Sin precios públicos** — CTA a contacto en todos los servicios
3. **Sin lead magnets** — hasta que existan
4. **Sin testimonios/casos** — hasta que los tengas
5. **Sin equipo** — solo "El Arquitecto"
6. **LinkedIn > SEO** — invierte en contenido para LinkedIn, no en Google
7. **Revisión en 90 días** — cuando ONMI tenga (ojalá) $30K en ingresos, entonces evalúa expandir el sitio

---

*Reality Check generado por JARVIS (COO) — 2026-06-03*
*Documentos auditados: architecture-strategic-blueprint.md v1.0.0, onmi-visual-system-v1.md v1.0.0*
*Próximo paso: Sesión ejecutiva con el fundador para aprobar/rechazar cada hallazgo*
