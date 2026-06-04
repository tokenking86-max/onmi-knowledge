---
title: "ADR-002: Adopción de Knowledge Architecture v2.0"
type: strategy
status: approved
tags:
  - adr
  - architecture
  - knowledge
  - decision
area: corporate
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS (CKO)
---

# ADR-002: Adopción de Knowledge Architecture v2.0

- **Fecha:** 2026-06-04
- **Estado:** Aprobada
- **Autor:** JARVIS (CKO) + Alan Ingaluque (fundador)

## Contexto

El workspace de ONMI creció orgánicamente desde su fundación. La estructura actual (v1) con 10 dominios fue suficiente para la etapa inicial pero presenta limitaciones:

1. **Mezcla de memoria de agente y conocimiento corporativo.** Los archivos de identidad de agentes ECC están mezclados en `agents/` sin separación clara.
2. **Decisiones sin dominio propio.** Los ADRs y decisiones estratégicas están dentro de `1-strategy/decisions/`, mezclados con documentos estratégicos.
3. **Nomenclatura inconsistente.** `ai-ml/` y `fintech/` no siguen el estándar de dominios cortos.
4. **Sin templates centralizados.** Los templates están dispersos en varios dominios.
5. **Sin estructura para RAG.** La organización actual no está optimizada para chunking, embedding y recuperación vectorial.
6. **Sin soporte para GraphRAG.** No hay separación clara de entidades y relaciones.

## Alternativas Consideradas

### Alternativa A: Mantener v1 con parches
Añadir carpetas nuevas sin reestructurar.

- ✅ Menor esfuerzo inmediato
- ❌ Acumula deuda estructural
- ❌ No resuelve las limitaciones existentes
- ❌ Más difícil de migrar en el futuro

### Alternativa B: Reestructuración completa a v2.0
12 dominios + templates raíz, agentes con carpetas propias, nomenclatura consistente.

- ✅ Arquitectura preparada para RAG y GraphRAG
- ✅ Separación clara memoria de agente vs. conocimiento corporativo
- ✅ Escalable para 3+ años
- ❌ Esfuerzo de migración (4-6 horas)

### Alternativa C: Base de datos de conocimiento externa
Migrar a una herramienta externa (Notion, Obsidian, etc.).

- ❌ Dependencia externa
- ❌ No integrable con agentes ECC vía sistema de archivos
- ❌ Costo adicional

## Decisión Tomada

**Opción elegida:** Alternativa B — Reestructuración completa a v2.0.

**Rationale:**
- La ventana actual (sin clientes, sin proyectos activos) es el momento óptimo para reestructurar
- La v2.0 está diseñada para 3 años de escalabilidad
- Preparar la base de conocimiento para RAG desde el inicio
- SSOT: cada concepto tiene una única ubicación canónica

**Consecuencias:**
- Positivas: Arquitectura preparada para RAG, GraphRAG y multi-agente
- Positivas: Onboarding más rápido de nuevos agentes ECC
- Negativas: Enlaces temporales rotos hasta actualizar referencias
- Se requiere actualizar CLAUDE.md y MEMORY.md

## Próximos pasos

1. ✅ Diseño de v2.0 completado (7 documentos arquitectónicos)
2. ✅ Migración física ejecutada (este ADR formaliza la decisión)
3. ⏳ Actualizar MEMORY.md con el nuevo estado
4. ⏳ Actualizar CLAUDE.md con nuevas rutas
5. ⏳ Crear memorias pendientes de agente
