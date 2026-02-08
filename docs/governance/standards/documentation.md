# Estándar General de Archivos del Repositorio

**Estado:** Activo
**Versión:** v1.0.0
**Owner:** Gobernanza ITech
**Dominio:** governance
**Última actualización:** 2026-02-08

---

## Plataforma ITech — Auditoría con Cursor IDE

**Rol:** Estándar obligatorio de cumplimiento
**Aplicación:** Todos los archivos del repositorio (`docs/`, código, config)

---

## 1. Propósito

Este estándar define las **condiciones mínimas y obligatorias** que debe cumplir **todo archivo** que se cargue al repositorio de la Plataforma ITech.

Su objetivo es:

* Garantizar **consistencia, trazabilidad y gobernanza**
* Permitir que **Cursor actúe como auditor automático** por commit
* Evitar ambigüedad, deuda documental y contenido huérfano

> 📌 Regla absoluta:
> **Todo archivo es auditable. Todo commit es evaluable.**

---

## 2. Alcance

Este estándar aplica a:

* Markdown (`.md`)
* YAML / JSON
* Código fuente (cualquier lenguaje)
* Archivos de configuración

Sin excepción.

---

## 3. Encabezado Obligatorio (Metadata)

Todo archivo **documental o de configuración** DEBE iniciar con un encabezado que incluya:

### 3.1 Para archivos Markdown

```md
# <Título claro del documento>

**Estado:** Draft | Activo | Deprecado
**Versión:** vX.Y.Z
**Owner:** <rol o responsable>
**Dominio:** blueprint | governance | roadmap | code
**Última actualización:** YYYY-MM-DD

---
```

❌ Archivos sin este encabezado **no cumplen**.

---

## 4. Reglas Generales de Contenido

### 4.1 Claridad y determinismo

* El contenido debe ser:

  * Explícito
  * No ambiguo
  * Sin referencias a conversaciones previas

### 4.2 Prohibiciones

Está prohibido:

* Referenciar contexto externo no documentado
* Usar frases como:

  * “como se habló antes”
  * “según lo acordado”
* Mezclar dominios (ej. roadmap dentro de blueprint)

---

## 5. Reglas por Tipo de Archivo

### 5.1 Markdown (`.md`)

Debe:

* Tener estructura jerárquica (`#`, `##`, `###`)
* Usar listas y tablas cuando aplique
* Terminar con una sección clara de cierre o siguiente paso

No debe:

* Contener decisiones implícitas
* Incluir código sin bloque ```

---

### 5.2 YAML / JSON

Debe:

* Ser válido sintácticamente
* Tener nombres descriptivos
* No contener valores mágicos sin comentario

Debe incluir (si aplica):

* Comentario inicial de propósito
* Versión del esquema

---

### 5.3 Código Fuente

Debe:

* Tener propósito claro
* Ser legible
* Evitar lógica muerta

Debe incluir:

* Comentario inicial de propósito
* Separación clara de responsabilidades

---

## 6. Reglas de Commit

Todo commit debe:

* Ser pequeño y enfocado
* Tener mensaje semántico

### Formato obligatorio

```
<tipo>(<área>): <descripción clara>
```

Ejemplos:

* `docs(blueprint): agregar visión arquitectónica`
* `docs(governance): definir estándar de testing`

---

## 7. Prompt de Auditoría para Cursor IDE

### Prompt Oficial — Auditor de Cumplimiento

> Usa este prompt como **regla de auditoría automática** en Cursor para cada commit.

```text
Actúa como auditor estricto del repositorio Plataforma ITech.

Tu tarea es validar el commit propuesto contra el "Estándar General de Archivos".

Para cada archivo modificado:
1. Verifica que cumple el encabezado obligatorio (si aplica).
2. Evalúa si el contenido es claro, explícito y sin referencias implícitas.
3. Confirma que el archivo corresponde al dominio correcto (blueprint, governance, roadmap, code).
4. Detecta mezclas de responsabilidades o violaciones de propósito.
5. Valida formato, sintaxis y estructura según el tipo de archivo.

Si el archivo cumple:
- Marca como ✅ APROBADO

Si no cumple:
- Marca como ❌ RECHAZADO
- Indica exactamente qué regla se viola
- Propón correcciones concretas

No seas complaciente.
No asumas contexto externo.
Evalúa solo lo que está explícitamente escrito.
```

---

## 8. Regla Final

> **Un archivo que no pasa este estándar no entra al repositorio.**

Este estándar es obligatorio y auditable.

---

**Fin del documento**
