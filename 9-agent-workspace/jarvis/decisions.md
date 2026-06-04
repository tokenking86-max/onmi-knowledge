---
title: "Decisions — JARVIS"
type: agent
status: active
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS
agent_role: CKO | COO
agent_status: active
tags:
  - agent-decisions
  - cko
  - coo
---

# Decisions — JARVIS

> Decisiones locales tomadas por JARVIS en el curso de sus operaciones.
> NO son ADRs corporativos. Son decisiones operativas sobre cómo JARVIS opera.

---

## Decisiones activas

| # | Fecha | Decisión | Contexto | Estado |
|---|-------|----------|----------|--------|
| D-001 | 2026-06-04 | Usar STRUCTURE-V2.md como estándar de estructura en lugar de STRUCTURE.md | La estructura v1 no soportaba agentes ECC ni RAG | active |

### D-001: Adoptar STRUCTURE-V2.md como estándar de estructura

- **Fecha:** 2026-06-04
- **Contexto:** STRUCTURE.md v1 era funcional pero no estaba optimizado para agentes ECC, RAG corporativo ni GraphRAG futuro.
- **Decisión:** STRUCTURE-V2.md (en `10-decisions/architecture-v2/`) es ahora el documento maestro de estructura. STRUCTURE.md se actualizará para redirigir a V2.
- **Alternativas:** (a) Reescribir STRUCTURE.md in-place, (b) Crear V2 como documento separado
- **Consecuencias:** Los agentes deben actualizar sus referencias. Los documentos existentes se migrarán según MIGRATION-PLAN.md.
- **Estado:** active
