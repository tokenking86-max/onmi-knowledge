---
title: "Dominio de Decisiones — 10-decisions"
type: strategy
status: active
version: "1.0.0"
created: 2026-06-04
updated: 2026-06-04
author: JARVIS (CKO)
tags:
  - decisions
  - adr
  - governance
area: corporate
---

# Dominio de Decisiones — 10-decisions

## Propósito

Registro formal de todas las decisiones estratégicas, técnicas, comerciales y organizacionales de ONMI, documentadas como Architecture Decision Records (ADRs).

## Formato

Cada decisión sigue el estándar definido en `templates/adr-template.md` con frontmatter YAML y secciones de contexto, alternativas, decisión y consecuencias.

## ADRs activos

| # | Título | Estado | Fecha |
|---|--------|--------|-------|
| ADR-001 | Definición del Catálogo de Servicios Inicial | superseded | 2026-06-03 |
| ADR-002 | Adopción de Knowledge Architecture v2.0 | approved | 2026-06-04 |
| ADR-003 | Separación de Memoria de Agente y Conocimiento Corporativo | approved | 2026-06-04 |
| ADR-004 | Catálogo de Servicios v2.0 (ReFoundation 2026) | approved | 2026-06-04 |
| ADR-005 | Enterprise Knowledge Platform — Diseño Aprobado | proposed | 2026-06-04 |
| ADR-006 | Fuentes Híbridas: GitHub Primario + Notion Secundario | proposed | 2026-06-04 |
| ADR-007 | RAG: OpenSearch Serverless con Embeddings 512d | proposed | 2026-06-04 |
| ADR-008 | Infraestructura AWS: Single-Región Inicial (us-east-1) | proposed | 2026-06-04 |
| ADR-009 | 8 Bounded Contexts con API Explícita para EKP | proposed | 2026-06-04 |
| ADR-010 | OpenSearch Serverless: Mínimo 2 OCUs con Warm Pool | proposed | 2026-06-04 |
| ADR-011 | Chunking Híbrido: Semántico + Sliding Window Fallback | proposed | 2026-06-04 |
| ADR-012 | ABAC para Documentos, RBAC para Infraestructura | proposed | 2026-06-04 |
| ADR-013 | Clasificación de Datos por Owner, Auditoría por JARVIS | proposed | 2026-06-04 |
| ADR-014 | Knowledge Graph en Fase 3 con Representación SQL Inicial | proposed | 2026-06-04 |
| ADR-015 | MCP Server Único con Routing Interno de Agentes | proposed | 2026-06-04 |
| ADR-016 | Implementación de EKP Condicionada a Ingresos Reales | proposed | 2026-06-04 |

## Subdominios

- `architecture-v2/` — Documentos de diseño de la Knowledge Architecture v2.0
- `enterprise-knowledge-platform/` — Diseño completo de la Enterprise Knowledge Platform (2026-06-04)
  - `README.md` — Documento maestro de 11 entregables
  - `adrs/` — 12 ADRs específicos de EKP (ADR-005 a ADR-016)

## Próximos pasos

1. Revisar y aprobar ADR-005 a ADR-016 con el fundador
2. Mover ADRs aprobados de `proposed` a `accepted`
3. Crear nuevos ADRs a medida que se tomen decisiones
