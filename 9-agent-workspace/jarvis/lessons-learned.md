---
title: "Lessons Learned — JARVIS"
type: agent
status: active
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS
agent_role: CKO | COO
agent_status: active
tags:
  - agent-lessons
  - cko
  - coo
---

# Lessons Learned — JARVIS

> Lecciones aprendidas por JARVIS en sus sesiones de trabajo.

---

## Lecciones

### LL-001: La documentación aspiracional sin validación comercial es peligrosa

- **Fecha:** 2026-06-03
- **Sesión/Contexto:** Reality Check v1.0 — auditoría de ~2,700 líneas de planificación web
- **Situación:** Se habían producido documentos de alta calidad (Strategic Blueprint, Visual System) que asumían una empresa con clientes, equipo y pipeline. ONMI tenía 0 ingresos, 0 proyectos, 1 persona.
- **Lección:** Antes de diseñar soluciones complejas, verificar que los supuestos de base son reales. Preguntar: "¿Esto funciona si ONMI sigue siendo 1 persona los próximos 6 meses?"
- **Impacto:** Alto
- **Aplicación futura:** Incluir un "reality check" como paso obligatorio antes de cualquier diseño > 500 líneas. Aplicar el principio de mínima complejidad viable como primer filtro.
- **Validada por:** Fundador (Alan) — aprobó todas las correcciones del Reality Check

### LL-002: La estructura de conocimiento debe diseñarse para agentes desde el día 1

- **Fecha:** 2026-06-04
- **Sesión/Contexto:** Diseño de Knowledge Architecture v2.0
- **Situación:** La estructura v1 (10 dominios planos) era funcional para humanos pero no consideraba cómo los agentes ECC leerían, escribirían y mantenerían contexto.
- **Lección:** Los agentes ECC necesitan: identidad clara, memoria separada, fronteras explícitas, y acceso a documentos con frontmatter rico para filtrado RAG.
- **Impacto:** Alto — rediseñar después es costoso
- **Aplicación futura:** Para cualquier nuevo sistema de información en ONMI, preguntar primero: "¿cómo lo va a consumir un agente?"
- **Validada por:** Autoevaluación
