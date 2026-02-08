# Estándar de Gobernanza de IA

**Estado:** Draft
**Versión:** v0.1.0
**Owner:** Plataforma ITech
**Dominio:** governance
**Última actualización:** 2026-02-08

---

## 1. Propósito

Este documento define el **estándar de gobernanza para el uso de Inteligencia Artificial** dentro de la Plataforma ITech.

Su objetivo es:

* Establecer reglas claras para el uso de IA en la generación y edición de artefactos.
* Garantizar trazabilidad, control y calidad.
* Evitar usos no gobernados, autónomos o no auditables de IA.

Este estándar deriva directamente de los **Principios de Gobernanza**.

---

## 2. Alcance

### 2.1 Dentro del alcance

* Uso de IA en IDE y flujos automatizados.
* Roles de la IA dentro del proceso.
* Reglas de validación, límites y evidencias.

### 2.2 Fuera del alcance

* Selección de modelos específicos.
* Costos, licenciamiento o proveedores.
* Implementaciones técnicas concretas.

---

## 3. Roles de la IA

La IA puede asumir **roles explícitos**, nunca implícitos:

1. **Generador**
   Produce borradores de código o documentación.

2. **Editor**
   Ajusta contenido existente siguiendo instrucciones explícitas.

3. **Auditor**
   Evalúa cumplimiento de estándares y reglas.

> Un mismo modelo **PUEDE** cumplir varios roles, pero **NO** de forma simultánea en la misma unidad de trabajo.

---

## 4. Reglas Obligatorias de Uso

1. **IA siempre bajo intención explícita**
   Toda interacción con IA **DEBE** partir de una intención documentada.

2. **Prohibición de autonomía**
   La IA **NO PUEDE** integrar cambios por sí sola.

3. **Validación obligatoria**
   Todo resultado de IA **DEBE** pasar por validación automática o humana.

4. **Cumplimiento de estándares**
   La IA **DEBE** respetar plantillas, formatos y dominios.

---

## 5. Evidencia y Trazabilidad

Cada uso relevante de IA **DEBE** dejar evidencia verificable, como:

* Prompt utilizado (o referencia versionada).
* Artefactos generados o modificados.
* Resultado de auditoría (APROBADO / RECHAZADO).

La ausencia de evidencia implica incumplimiento.

---

## 6. Puntos de Control (Gates)

El uso de IA está sujeto a los siguientes gates:

* **Gate IA-1:** Cumplimiento de estándares documentales.
* **Gate IA-2:** Coherencia con blueprint activo.
* **Gate IA-3:** Evidencia de revisión.

Los gates pueden ejecutarse en IDE o CI.

---

## 7. Incumplimientos

Ante incumplimiento:

* El artefacto **NO** se integra.
* Se requiere corrección explícita.
* El incidente **PUEDE** registrarse como decisión o hallazgo.

---

## 8. Relación con Otros Documentos

Este estándar se apoya en:

* `docs/governance/principles.md`
* `docs/governance/standards/documentation.md`

Y se relaciona con:

* `docs/blueprint/runtime.md`

---

## 9. Estado y Próximos Pasos

**Estado actual:** Draft inicial.

Próximo estándar sugerido:

* `docs/governance/standards/testing.md`

---

**Fin del documento**

