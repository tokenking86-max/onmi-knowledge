---
title: "ADR-004: Catálogo de Servicios v2.0 (ReFoundation 2026)"
type: strategy
status: approved
tags:
  - adr
  - catalog
  - services
  - refoundation
  - decision
area: corporate
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS (COO)
supersedes: "ADR-001"
---

# ADR-004: Catálogo de Servicios v2.0 (ReFoundation 2026)

- **Fecha:** 2026-06-04
- **Estado:** Aprobada
- **Autor:** JARVIS (COO) + Alan Ingaluque (fundador)

## Contexto

El catálogo v1 (ADR-001, servicios S1-S6 en 3 capas) fue diseñado como punto de partida, pero la sesión de ReFoundation 2026 identificó:

1. **Sobrecarga cognitiva para el cliente.** 6 servicios son difíciles de procesar. El cliente necesita entender rápidamente qué ofrece ONMI.
2. **Límites difusos entre servicios.** S2 (Native Architecture) y S5 (Agent Blueprint) se superponen. S1 y S6 son difíciles de diferenciar.
3. **Falta de agrupación por tipo de engagement.** Los servicios no se agrupan claramente por cómo el cliente los compra (cash vs. growth vs. strategic).
4. **Dificultad para fijar precios.** Demasiadas combinaciones posibles. Pricing se vuelve complejo.

## Alternativas Consideradas

### Alternativa A: Refinar v1 (S1-S6)
Mantener 6 servicios con descripciones mejoradas.

- ❌ No resuelve la sobrecarga cognitiva
- ❌ Sigue siendo difícil de comunicar
- ❌ S1 y S6 siguen siendo confusos

### Alternativa B: Catálogo v2 con 3 líneas, 8 servicios
- **Cash Services (QC-01, QC-02, QC-03):** Entry point, bajo riesgo, precio fijo
- **Growth Services (GC-01, GC-02, GC-03):** Proyectos medianos, valor comprobado
- **Strategic Services (ST-01, ST-02):** Alto ticket, largo plazo, alto riesgo
- ✅ Agrupación clara por tipo de engagement
- ✅ Cash services como entry points sin fricción
- ✅ Pipeline natural: QC → GC → ST
- ✅ Pricing más simple (por línea de servicio)
- ✅ Alineado con el perfil de riesgo del fundador

### Alternativa C: Solo 3 servicios (uno por línea)
1 servicio por línea. Máxima simplicidad.

- ✅ Extremadamente simple
- ❌ Muy poca granularidad para clientes con necesidades específicas
- ❌ No hay diferenciación entre tipos de cash services

## Decisión Tomada

**Opción elegida:** Alternativa B — Catálogo v2 con 3 líneas, 8 servicios.

**Rationale:**
- Cash services son el entry point de bajo riesgo que ONMI necesita para generar ingresos en 90 días
- La agrupación en líneas comunica claramente madurez y nivel de inversión
- Pipeline natural QC→GC→ST permite crecimiento orgánico del ticket
- Pricing se define por línea, no por servicio individual
- ADR-001 queda superado (superseded_by: ADR-004)

**Consecuencias:**
- Positivas: Catálogo comunicable en 30 segundos
- Positivas: Cash services permiten ventas rápidas sin fricción
- Negativas: Servicios S1-S6 del v1 pasan a legacy
- Se requiere actualizar colaterales comerciales para reflejar v2

## Próximos pasos

1. ✅ ReFoundation completada
2. ✅ Catálogo v2 publicado en 2-services/catalog-v2.md
3. ✅ QC-01 collateral creado (sales one-pager, proposal template, report template)
4. ✅ QC-02 collateral creado (sales one-pager, proposal template)
5. ⏳ QC-03 collateral pendiente
6. ⏳ Preparar GC-01, GC-02, GC-03 propuestas base
