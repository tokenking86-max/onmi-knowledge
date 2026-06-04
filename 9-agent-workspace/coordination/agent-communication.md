---
title: "Protocolo de Comunicación entre Agentes ONMI"
type: ops
status: draft
tags:
  - agents
  - coordination
  - protocol
area: corporate
version: "0.1.0"
created: 2026-06-03
updated: 2026-06-03
author: JARVIS
---

# Protocolo de Comunicación entre Agentes ONMI

## Arquitectura

ONMI opera con una arquitectura de **agente orquestador con subagentes especializados**:

```
                    ┌───────────────────┐
                    │     JARVIS        │
                    │   (COO / Hub)     │
                    └────────┬──────────┘
                             │
            ┌────────────────┼────────────────┬──────────────┐
            ▼                ▼                ▼              ▼
    ┌───────────────┐ ┌───────────┐ ┌──────────────┐ ┌──────────┐
    │  Arquitecto   │ │ Security  │ │  Marketing   │ │ Content  │
    │  Técnico      │ │ Officer   │ │  Specialist  │ │ Writer   │
    └───────────────┘ └───────────┘ └──────────────┘ └──────────┘
```

## Roles

### JARVIS (Hub Central)
- **Responsabilidad:** Orquestación, decisiones ejecutivas, visión general
- **Lee/actualiza:** MEMORY.md, toda la estructura de conocimiento
- **Convoca a:** Subagentes según necesidad

### Arquitecto Técnico
- **Responsabilidad:** Diseño de soluciones, revisión de arquitecturas, selección tecnológica
- **Reporta a:** JARVIS
- **Se convoca cuando:** Se necesita diseñar o auditar una arquitectura

### Security Officer
- **Responsabilidad:** Revisión de seguridad, compliance, AI governance
- **Reporta a:** JARVIS
- **Se convoca cuando:** Se necesita evaluar riesgos de seguridad o compliance

### Marketing Specialist
- **Responsabilidad:** Estrategia de contenido, campañas, posicionamiento
- **Reporta a:** JARVIS
- **Se convoca cuando:** Se necesita planificar o ejecutar marketing

### Content Writer
- **Responsabilidad:** Redacción de contenido técnico, whitepapers, artículos
- **Reporta a:** JARVIS (con input de Marketing Specialist)
- **Se convoca cuando:** Se necesita producir contenido

## Protocolo de coordinación

### 1. JARVIS detecta necesidad de subagente
```
Disparadores:
- Tarea técnica compleja → Arquitecto
- Revisión de seguridad → Security Officer
- Contenido o campaña → Marketing / Content
```

### 2. JARVIS prepara contexto y convoca
```
Para cada subagente:
- Brief claro: objetivo, restricciones, entregables
- Contexto relevante: documentos del workspace que debe leer
- Deadline: fecha límite
```

### 3. Subagente ejecuta y reporta
```
Formato de reporte de subagente:
1. Resumen ejecutivo (3 líneas max)
2. Hallazgos / entregables
3. Recomendaciones
4. Documentos creados o modificados
```

### 4. JARVIS consolida
```
- Revisa el output del subagente
- Actualiza MEMORY.md si corresponde
- Toma decisiones ejecutivas basadas en las recomendaciones
- Reporta al fundador si es necesario
```

## Espacio de trabajo compartido

- Los subagentes pueden leer toda la estructura de conocimiento
- Los subagentes **no escriben** en MEMORY.md directamente — solo JARVIS
- Los subagentes escriben en sus respectivas carpetas dentro de `9-agent-workspace/agents/`
- JARVIS revisa y consolida antes de integrar al conocimiento principal

## Memoria compartida

- `MEMORY.md` es el único punto de verdad para el estado ejecutivo
- Los subagentes mantienen su propia memoria dentro de `9-agent-workspace/agents/`
- JARVIS puede leer la memoria de los subagentes para contexto
