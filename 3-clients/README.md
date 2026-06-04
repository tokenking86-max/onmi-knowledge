# 3-clients — Clientes y Pipeline Comercial

## Propósito

Gestiona la cartera de clientes, leads, pipeline de ventas y propuestas comerciales.

## Estructura

| Carpeta/Archivo | Propósito |
|-----------------|-----------|
| `pipeline.md` | Pipeline comercial vivo (etapas, montos, probabilidades) |
| `leads/` | Leads por estado (new, contacted, qualified, unqualified) |
| `active/` | Clientes activos — una subcarpeta por cliente |
| `proposals/` | Propuestas enviadas — una subcarpeta por propuesta |

## Frontmatter para leads

```yaml
---
title: "Nombre del Lead"
type: client
status: new | contacted | qualified | unqualified
source: web | referral | linkedin | event | inbound
estimated_value: 25000
tags:
  - fintech
  - peru
created: 2026-06-03
updated: 2026-06-03
---
```
