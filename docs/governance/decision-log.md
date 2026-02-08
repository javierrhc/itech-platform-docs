# Registro de Decisiones

**Estado:** Draft
**Versión:** v0.1.0
**Owner:** Plataforma ITech
**Dominio:** governance
**Última actualización:** 2026-02-08

---

## 1. Propósito

Este documento es el **registro oficial de decisiones** de la Plataforma ITech.

Su objetivo es:

* Documentar decisiones relevantes de forma **explícita y auditable**.
* Evitar decisiones implícitas dispersas en otros documentos.
* Proveer trazabilidad entre contexto, decisión y consecuencias.

Este registro opera como un **ADR liviano** (Architectural / Governance Decision Record).

---

## 2. Alcance

### 2.1 Qué decisiones se registran aquí

Se deben registrar decisiones que:

* Cambien restricciones o supuestos del blueprint.
* Introduzcan o modifiquen principios, estándares o políticas.
* Definan reglas globales (gates, auditoría, versionado, etc.).
* Afecten el modelo operativo del repositorio.

### 2.2 Qué NO se registra aquí

No se registran:

* Tareas o pasos del roadmap.
* Ajustes editoriales menores sin impacto de gobierno.
* Decisiones puramente temporales (a menos que impongan restricciones).

---

## 3. Formato Obligatorio de una Decisión

Cada decisión se registra como una entrada con el siguiente formato.

> Nota: Mantener el formato para auditoría automatizada.

```md
## DEC-YYYY-NNN — <Título breve de la decisión>

**Estado:** Propuesta | Aprobada | Rechazada | Deprecada
**Fecha:** YYYY-MM-DD
**Owner:** <rol o responsable>

### Contexto

<Qué problema se busca resolver y por qué es relevante>

### Decisión

<Decisión explícita en lenguaje normativo>

### Alternativas Consideradas

- A1 — <alternativa> (por qué no)
- A2 — <alternativa> (por qué no)

### Consecuencias

- Impactos positivos
- Riesgos o costos
- Dependencias creadas

### Evidencia / Referencias

- Documentos afectados: <rutas>
- Pull Request / Commit: <id cuando exista>
```

---

## 4. Catálogo de Decisiones

### DEC-2026-001 — Fuente de verdad documental en Markdown

**Estado:** Aprobada
**Fecha:** 2026-02-08
**Owner:** Plataforma ITech

#### Contexto

Se requiere que el conocimiento del proyecto no dependa de conversaciones ni memoria externa. Se necesita una fuente de verdad única, versionada y auditable.

#### Decisión

La fuente de verdad de la Plataforma ITech **DEBE** residir en documentación Markdown organizada bajo:

* `docs/blueprint/`
* `docs/roadmap/`
* `docs/governance/`

La conversación solo se usa para redactar y validar contenido que luego se versiona.

#### Alternativas Consideradas

* A1 — Mantener estado en conversaciones: Rechazado por no auditabilidad y dependencia de contexto.
* A2 — Usar wiki externa: Rechazado por fragmentación y menor trazabilidad con Git.

#### Consecuencias

* Se garantiza trazabilidad y auditoría.
* Aumenta disciplina documental.
* Cualquier avance requiere actualización en docs.

#### Evidencia / Referencias

* Documentos afectados: `docs/README.md`.

---

### DEC-2026-002 — Canvas temporal único para entregables

**Estado:** Aprobada
**Fecha:** 2026-02-08
**Owner:** Plataforma ITech

#### Contexto

Se requiere entregar documentos/código sin pérdida de formato, evitando múltiples canvases o un canvas inmanejable.

#### Decisión

Se utilizará un **canvas temporal único** en esta conversación.

* Cada entrega **DEBE** reemplazar por completo el contenido del canvas.
* El canvas **NO** es fuente de verdad.
* La fuente de verdad es el repositorio Git.

#### Alternativas Consideradas

* A1 — Múltiples canvases: Rechazado por fragmentación.
* A2 — Entregas solo por chat: Rechazado por riesgo de pérdida de formato.

#### Consecuencias

* Entregables consistentes.
* Menor ruido y mejor control del tamaño.

#### Evidencia / Referencias

* Documentos afectados: `docs/README.md`.

---

### DEC-2026-003 — Estándar general de archivos + auditoría con Cursor

**Estado:** Aprobada
**Fecha:** 2026-02-08
**Owner:** Plataforma ITech

#### Contexto

Se requiere auditar cada commit y validar que todo archivo cumpla estándares de estructura y dominio, usando Cursor como auditor.

#### Decisión

Todo archivo cargado al repositorio **DEBE** cumplir el estándar documental definido en:

* `docs/governance/standards/documentation.md`

Cursor **DEBE** auditar los commits usando el prompt oficial descrito en dicho estándar.

#### Alternativas Consideradas

* A1 — Auditoría manual: Rechazado por escalabilidad.
* A2 — Auditoría solo en CI: Rechazado por feedback tardío.

#### Consecuencias

* Se habilita gate temprano (IDE).
* Se reducen errores de formato y dominio.

#### Evidencia / Referencias

* Documentos afectados: `docs/governance/standards/documentation.md`.

---

### DEC-2026-004 — Estrategia de commits por grupo lógico

**Estado:** Aprobada
**Fecha:** 2026-02-08
**Owner:** Plataforma ITech

#### Contexto

Commits uno a uno por archivo generan ruido y dificultan revisión conceptual. Se requiere una estrategia que refleje unidades de decisión coherentes.

#### Decisión

Los commits **DEBEN** agruparse por **unidad conceptual cerrada** (grupo lógico), no por archivo individual.

Ejemplos válidos:

* “baseline blueprint core”
* “gobernanza base”

#### Alternativas Consideradas

* A1 — Commit por archivo: Rechazado por falta de cohesión.
* A2 — Commits grandes y esporádicos: Rechazado por riesgo y baja trazabilidad.

#### Consecuencias

* Historial más legible.
* Revisiones más rápidas.
* Mejor alineación con decisiones reales.

#### Evidencia / Referencias

* Documentos afectados: `docs/governance/standards/documentation.md`.

---

## 5. Estado y Próximos Pasos

**Estado actual:** Draft inicial con decisiones fundacionales.

Próximos pasos sugeridos:

* Agregar decisiones nuevas solo cuando exista un cambio real de reglas.
* Incorporar referencia de PR/commit una vez existan.

---

**Fin del documento**