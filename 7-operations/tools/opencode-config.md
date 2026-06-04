---
title: "Configuración de OpenCode para ONMI"
type: ops
status: draft
tags:
  - opencode
  - config
area: corporate
version: "0.1.0"
created: 2026-06-03
updated: 2026-06-03
author: JARVIS
---

# Configuración de OpenCode para ONMI

## Skills cargados

Skills existentes (en `C:\Users\ALAN\.config\opencode\skills\`):

| Skill | Propósito |
|-------|-----------|
| `analizar-mercado` | Investigación de mercado y competencia |
| `gestionar-propuestas` | Propuestas y cotizaciones |
| `gestionar-clientes` | CRM y seguimiento de clientes |
| `gestionar-proyectos` | Planificación y seguimiento |
| `disenar-arquitectura` | Diseño de soluciones técnicas |

## Skills propuestos para crear (ONMI-specific)

Ver `9-agent-workspace/skills/` para definiciones:

| Skill | Propósito | Prioridad |
|-------|-----------|-----------|
| `onmi-framework-designer` | Diseñar y versionar frameworks propietarios | Alta |
| `onmi-proposal-writer` | Redactar propuestas comerciales con formato ONMI | Alta |
| `onmi-rag-indexer` | Mantener la estructura RAG-friendly del workspace | Media |

## Convenciones OpenCode

1. Siempre leer MEMORY.md al iniciar una sesión de trabajo
2. Usar convenciones de frontmatter YAML en nuevos documentos
3. Preferir documentos atómicos sobre editar monolitos
4. Actualizar MEMORY.md después de decisiones ejecutivas
