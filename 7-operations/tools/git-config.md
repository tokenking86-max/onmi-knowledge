---
title: "Configuración Git para ONMI"
type: ops
status: draft
tags:
  - git
  - config
area: corporate
version: "0.1.0"
created: 2026-06-03
updated: 2026-06-03
author: JARVIS
---

# Configuración Git para ONMI

## Repositorios recomendados

| Repositorio | Visibilidad | Propósito |
|-------------|-------------|-----------|
| `onmi-knowledge` | Privado | Workspace completo de conocimiento |
| `onmi-website` | Público | Sitio web corporativo |
| `onmi-frameworks` | Público | Frameworks open-source (futuro) |
| `onmi-tooling` | Privado/Selectivo | Herramientas internas |

## Convenciones de ramas

```
main                    → Producción (estable, revisado)
develop                 → Integración (trabajo en curso)
feature/{tema}          → Features nuevas (kebab-case)
fix/{tema}              → Correcciones
release/{version}       → Preparación de release
```

## Convenciones de commits

Usar **Conventional Commits**:

```
docs: nueva ficha de servicio S2
feat: agregar framework AI-MM v1.0
fix: corregir pricing en bundles.md
strategy: actualizar OKRs Q2-2026
client: agregar lead Banco ABC
project: cerrar charter proyecto XYZ
ops: actualizar playbook onboarding
```

## Versionado de IP

- Cada framework/metodología tiene versionado semántico independiente (v1.0.0)
- Tags Git: `framework-ai-mm-v1.0.0`
- CHANGELOG mantenido dentro de cada framework

## .gitignore

```gitignore
# Datos sensibles
3-clients/**/*.secret.md
7-operations/finance/**/*

# Archivos temporales
*.tmp
*.log

# Sistema
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/
```
