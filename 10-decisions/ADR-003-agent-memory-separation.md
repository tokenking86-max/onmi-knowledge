---
title: "ADR-003: Separación de Memoria de Agente y Conocimiento Corporativo"
type: strategy
status: approved
tags:
  - adr
  - agents
  - memory
  - governance
  - decision
area: corporate
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS (CKO)
---

# ADR-003: Separación de Memoria de Agente y Conocimiento Corporativo

- **Fecha:** 2026-06-04
- **Estado:** Aprobada
- **Autor:** JARVIS (CKO) + Alan Ingaluque (fundador)

## Contexto

En la estructura v1, los archivos de identidad de agentes ECC (architect-agent.md, content-agent.md, etc.) estaban mezclados dentro del workspace corporativo en `9-agent-workspace/agents/`, sin separación clara entre:

- **Memoria de agente:** Información privada de cada agente (identidad, decisiones locales, lecciones aprendidas, contexto de sesión)
- **Conocimiento corporativo:** Información compartida y gobernada de la empresa (catálogo, estrategia, IP, knowledge base)

Esta mezcla genera:
1. Riesgo de que un agente exponga memoria privada de otro agente
2. Dificultad para hacer RAG sobre conocimiento corporativo (datos mezclados con metadata de agente)
3. Sin estándar para qué pertenece a cada agente vs. qué es corporativo
4. Los agentes no tienen un "home" propio para su contexto persistente

## Alternativas Consideradas

### Alternativa A: Todo en un solo árbol
Mantener agentes mezclados con el conocimiento corporativo.

- ❌ No hay separación de concerns
- ❌ RAG corporativo se contamina con metadata de agente
- ❌ Agentes sin privacidad de memoria

### Alternativa B: Separación estricta con carpetas dedicadas por agente
Cada agente tiene `identity.md`, `memory.md`, `decisions.md`, `lessons-learned.md` en su propia carpeta dentro de `9-agent-workspace/`. El conocimiento corporativo se mantiene fuera.

- ✅ Cada agente tiene un home claro
- ✅ RAG corporativo sobre datos limpios
- ✅ Escalable para N agentes
- ✅ Sigue el principio SSOT

### Alternativa C: Base de datos externa para memoria de agente
Usar MCP memory server o vector store para memoria de agente.

- ❌ Dependencia de infraestructura externa
- ❌ Pérdida de transparencia (archivos planos son más auditable)
- ❌ Complejidad operativa innecesaria en etapa inicial

## Decisión Tomada

**Opción elegida:** Alternativa B — Separación estricta con carpetas dedicadas.

**Rationale:**
- Simplicidad: archivos markdown planos, sin infraestructura
- Transparencia: cualquier agente puede leer la memoria de otro si es necesario
- SSOT: el conocimiento corporativo es shared, la memoria de agente es privada
- Preparado para el futuro: cuando se necesite RAG, el knowledge base ya estará limpio

**Consecuencias:**
- Cada agente tiene 4 archivos: identity.md, memory.md, decisions.md, lessons-learned.md
- Los agentes no deben escribir en conocimiento corporativo (solo leer)
- Las decisiones estratégicas van a 10-decisions/ (no a la memoria del agente)

## Próximos pasos

1. ✅ Estructura de carpetas de agente creada
2. ✅ Architect y CMO identities migradas
3. ⏳ Completar memorias de CEO, Sales, UX, Frontend, SEO
