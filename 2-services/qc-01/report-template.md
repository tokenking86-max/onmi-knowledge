# Reporte de Cloud & AI Architecture Quick Assessment — Template

> **Template para estructura de reporte QC-01.** Completar con hallazgos reales del cliente.
> Extensión objetivo: 10-15 páginas.

---

## Portada

**Título:** Cloud & AI Architecture Quick Assessment — [Nombre del Cliente]
**Cliente:** [Empresa]
**Fecha:** [dd/mm/aaaa]
**Autores:** Alan Ingaluque Paz — Arquitecto Principal, ONMI
**Clasificación:** Confidencial — [Cliente]
**Versión:** 1.0

---

## 1. Resumen Ejecutivo (1 página)

[3-5 párrafos que cualquier ejecutivo pueda leer en 2 minutos.]

- Contexto: qué se evaluó y por qué
- Principales hallazgos (3-5 balas)
- Top-3 quick wins (tabla pequeña)
- Veredicto general: ¿la arquitectura está lista para IA?

---

## 2. Alcance del Assessment (media página)

- Qué se evaluó: [dimensiones cubiertas]
- Qué NO se evaluó: [limitaciones explícitas]
- Período de evaluación: [fechas]

---

## 3. Metodología (media página)

Breve descripción de cómo se realizó:
- Revisión documental
- Entrevistas con stakeholders
- Análisis técnico
- Benchmark contra best practices

---

## 4. Estado Actual por Dimensión

### 4.1 Cloud Architecture

| Aspecto | Hallazgo | Severidad |
|---------|----------|-----------|
| Proveedor/es y topología | [descripción] | 🟢/🟡/🔴 |
| Capacidad para IA/ML | [descripción] | 🟢/🟡/🔴 |
| Costos y eficiencia | [descripción] | 🟢/🟡/🔴 |
| Escalabilidad | [descripción] | 🟢/🟡/🔴 |
| Disaster Recovery / HA | [descripción] | 🟢/🟡/🔴 |

### 4.2 Data Readiness

| Aspecto | Hallazgo | Severidad |
|---------|----------|-----------|
| Calidad de datos | [descripción] | 🟢/🟡/🔴 |
| Acceso y gobernanza | [descripción] | 🟢/🟡/🔴 |
| Pipelines y ETL | [descripción] | 🟢/🟡/🔴 |
| Feature store / data lake | [descripción] | 🟢/🟡/🔴 |

### 4.3 Security & Identity

| Aspecto | Hallazgo | Severidad |
|---------|----------|-----------|
| Control de acceso e identidad | [descripción] | 🟢/🟡/🔴 |
| Cifrado (reposo/tránsito) | [descripción] | 🟢/🟡/🔴 |
| Auditoría y trazabilidad | [descripción] | 🟢/🟡/🔴 |
| Seguridad de API/integración | [descripción] | 🟢/🟡/🔴 |

### 4.4 Compliance & Regulatory

| Aspecto | Hallazgo | Severidad |
|---------|----------|-----------|
| Brechas regulatorias para IA | [descripción] | 🟢/🟡/🔴 |
| Protección de datos personales | [descripción] | 🟢/🟡/🔴 |
| Gobierno de modelos (si aplica) | [descripción] | 🟢/🟡/🔴 |
| Proveedores cloud y residencia | [descripción] | 🟢/🟡/🔴 |

### 4.5 AI Readiness

| Aspecto | Hallazgo | Severidad |
|---------|----------|-----------|
| Capacidades IA actuales | [descripción] | 🟢/🟡/🔴 |
| ML/AI en producción | [descripción] | 🟢/🟡/🔴 |
| Equipo y skills | [descripción] | 🟢/🟡/🔴 |
| Herramientas y plataformas | [descripción] | 🟢/🟡/🔴 |

---

## 5. Matriz de Readiness Consolidada

| Dimensión | Nivel Actual | Nivel Requerido para IA | Brecha |
|-----------|-------------|------------------------|--------|
| Cloud Architecture | 🟢/🟡/🔴 | 🟢/🟡/🔴 | ✅/⚠️/❌ |
| Data Readiness | 🟢/🟡/🔴 | 🟢/🟡/🔴 | ✅/⚠️/❌ |
| Security & Identity | 🟢/🟡/🔴 | 🟢/🟡/🔴 | ✅/⚠️/❌ |
| Compliance & Regulatory | 🟢/🟡/🔴 | 🟢/🟡/🔴 | ✅/⚠️/❌ |
| AI Readiness | 🟢/🟡/🔴 | 🟢/🟡/🔴 | ✅/⚠️/❌ |

**Leyenda:** 🟢 Ready | 🟡 Partial | 🔴 Gap

---

## 6. Top-3 Quick Wins

| # | Quick Win | Esfuerzo | Impacto | Plazo estimado | Dimensión |
|---|-----------|----------|---------|----------------|-----------|
| 1 | [acción concreta] | 🟢 Bajo | 🔴 Alto | [X] semanas | [Cloud/Data/Security/Compliance/AI] |
| 2 | [acción concreta] | 🟡 Medio | 🔴 Alto | [X] semanas | [dimensión] |
| 3 | [acción concreta] | 🟢 Bajo | 🟡 Medio | [X] semanas | [dimensión] |

Cada quick win debe incluir:
- Descripción de la acción
- Justificación (por qué esto y no otra cosa)
- Pasos concretos para implementar
- Dependencias y riesgos

---

## 7. Hoja de Ruta Recomendada

### Corto plazo (0-3 meses)
- Quick wins del assessment
- Preparación de infraestructura para IA

### Mediano plazo (3-6 meses)
- Implementación de primer caso de uso IA
- Fortalecimiento de gobierno de datos

### Largo plazo (6-18 meses)
- Escalamiento de capacidades IA
- Madurez de MLOps y gobierno de modelos

> Nota: Esta hoja de ruta es preliminar. Un roadmap detallado requiere QC-02 (AI Strategy & Technology Roadmap).

---

## 8. Riesgos y Recomendaciones

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|-------------|---------|------------|
| [descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [acción] |
| [descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [acción] |

---

## 9. Apéndices

### A. Documentación revisada
- [lista de documentos]

### B. Stakeholders entrevistados
- [nombre, cargo, fecha]

### C. Glosario de términos
- [términos técnicos relevantes]

---

## Clasificación

**Confidencial:** Este documento contiene información sensible de [Cliente]. No debe ser distribuido sin autorización expresa.

---

*Template generado por JARVIS (COO) — 2026-06-03*
