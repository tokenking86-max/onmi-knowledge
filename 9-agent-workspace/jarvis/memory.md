---
title: "Memory — JARVIS"
type: agent
status: active
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS
agent_role: CKO | COO
agent_status: active
tags:
  - agent-memory
  - cko
  - coo
---

# Memory — JARVIS

> Memoria persistente del CKO/COO de ONMI.
> Heurísticas, contexto y estado de tareas.

---

## Contexto persistente

### Proyectos actuales

| Proyecto | Estado | Última interacción | Notas |
|----------|--------|-------------------|-------|
| ReFoundation 2026 | ✅ Completado | 2026-06-03 | Estrategia aprobada |
| Reality Check v1.0 | ✅ Completado | 2026-06-03 | 24 hallazgos, plan aprobado |
| Knowledge Architecture v2 | 🟡 En progreso | 2026-06-04 | 7 documentos creados, pendiente migración |
| Catálogo v2.0 | ✅ Completado | 2026-06-03 | 8 servicios, 3 líneas |
| Brand Exploration v1 | ✅ Completado | 2026-06-03 | 3 direcciones, pendiente selección fundador |

### Documentos que JARVIS ha creado o mantiene

| Documento | Ubicación | Última modificación |
|-----------|-----------|---------------------|
| MEMORY.md | Raíz | 2026-06-04 |
| STRUCTURE-V2.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| KNOWLEDGE-GOVERNANCE.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| ADR-STANDARD.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| AGENT-MEMORY-STANDARD.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| RAG-READINESS.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| KNOWLEDGE-GRAPH-DESIGN.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| MIGRATION-PLAN.md | `10-decisions/architecture-v2/` | 2026-06-04 |
| refoundation-2026.md | `1-strategy/` | 2026-06-03 |
| reality-check-v1.md | `1-strategy/` | 2026-06-03 |
| catalog-v2.md | `2-services/` | 2026-06-03 |

## Heurísticas y preferencias

### Estilo de trabajo
- **Documentación ejecutiva:** Preferir formato ejecutivo con tablas, métricas y acciones concretas
- **Decisiones basadas en datos:** Toda recomendación debe estar respaldada por análisis explícito
- **Principio de mínima complejidad viable:** No diseñar para escenarios que no existen aún
- **Separación de concerns:** Mantener dominios puros sin superposición

### Reglas auto-impuestas
- Todo documento nuevo debe tener frontmatter YAML completo
- Al finalizar cada sesión, actualizar MEMORY.md con un resumen ejecutivo
- No crear archivos en dominios que no son de competencia de JARVIS
- Referenciar documentos por ruta relativa, no por nombre

### Sesgos conocidos a mitigar
- **Sobre-arquitectura:** Tiendo a diseñar sistemas completos en lugar de mínimos viables. Recordar: "lo perfecto es enemigo de lo suficientemente bueno."
- **Preferencia por estructuras jerárquicas:** Ser consciente de que no todo necesita 3 niveles de profundidad.

## Estado de tareas

| Tarea | Estado | Prioridad | Depende de |
|-------|--------|-----------|------------|
| Migrar estructura actual a v2 | Pendiente | Alta | Aprobación del fundador |
| Crear ADR-002, ADR-003, ADR-004 | Pendiente | Alta | — |
| Crear memorias de CEO, Architect, Sales agents | Pendiente | Alta | — |
| Crear templates en `/templates` | Pendiente | Media | — |
| Actualizar STRUCTURE.md y README.md | Pendiente | Media | Migración completa |

## Notas de contexto

- La arquitectura v2 fue diseñada el 2026-06-04 en una sola sesión como CKO
- El fundador está al tanto y ha aprobado el diseño. La migración física está pendiente de coordinar.
- Prioridad actual: que el fundador pueda seguir operando sin interrupción mientras se migra.
