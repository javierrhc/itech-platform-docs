# Restricciones y Supuestos de la Plataforma ITech

**Estado:** Draft
**Versión:** v0.1.0
**Owner:** Plataforma ITech
**Dominio:** blueprint
**Última actualización:** 2026-02-08

---

## 1. Propósito

Este documento establece las **restricciones explícitas** y los **supuestos permitidos** que delimitan la arquitectura baseline de la Plataforma ITech.

Su objetivo es:

* Evitar interpretaciones implícitas.
* Definir límites claros de diseño.
* Servir como referencia de “no-go” arquitectónicos.

No define políticas operativas ni decisiones tácticas temporales.

---

## 2. Alcance

### 2.1 Dentro del alcance

* Restricciones arquitectónicas no negociables.
* Supuestos permitidos y explícitos.
* Exclusiones deliberadas del diseño.

### 2.2 Fuera del alcance

* Políticas de seguridad, testing u observabilidad.
* Decisiones de herramientas o proveedores.
* Cronogramas, fases o prioridades.

---

## 3. Restricciones Arquitectónicas (No Negociables)

Las siguientes restricciones **DEBEN** cumplirse en cualquier evolución de la plataforma:

1. **Documentación como fuente de verdad**
   Todo conocimiento relevante **DEBE** residir en documentos versionados bajo `docs/`.

2. **Separación estricta de dominios**
   Blueprint, governance y roadmap **NO DEBEN** mezclarse en un mismo documento.

3. **IA gobernada por estándares**
   Ninguna generación asistida por IA **PUEDE** integrarse sin pasar por estándares y auditoría.

4. **Auditoría obligatoria**
   Todo artefacto **DEBE** ser auditable automática o manualmente.

5. **Neutralidad tecnológica**
   La arquitectura baseline **NO DEBE** depender de herramientas, vendors o frameworks específicos.

---

## 4. Supuestos Permitidos

Los siguientes supuestos son aceptables mientras se mantengan explícitos:

1. **Uso de asistentes IA en el IDE**
   Se asume que el entorno de desarrollo puede integrar capacidades de IA.

2. **Existencia de control de versiones**
   Se asume un sistema de versionado distribuido (ej. Git) como base.

3. **Intervención humana en puntos críticos**
   Se asume la existencia de revisión humana cuando las reglas lo requieran.

Estos supuestos **DEBEN** revisarse si el contexto cambia.

---

## 5. Exclusiones Deliberadas (No-Go)

La Plataforma ITech **NO** está diseñada para:

* Ejecutar aplicaciones productivas.
* Reemplazar sistemas de CI/CD existentes.
* Actuar como gestor de identidades o accesos.
* Tomar decisiones autónomas sin reglas explícitas.

Cualquier intento de extender la plataforma a estos ámbitos **requiere** una decisión formal documentada.

---

## 6. Gestión de Cambios a Restricciones

* Las restricciones solo pueden modificarse mediante:

  * Actualización explícita de este documento, o
  * Registro de decisión en `docs/governance/decision-log.md`.

* Los cambios **NO** pueden introducirse de forma implícita en otros documentos.

---

## 7. Relación con Otros Documentos

Este documento complementa:

* `docs/blueprint/README.md`
* `docs/blueprint/architecture.md`
* `docs/blueprint/runtime.md`
* `docs/blueprint/integrations.md`

---

## 8. Estado y Próximos Pasos

**Estado actual:** Draft inicial.

Próximo paso sugerido:

* Cierre del **Blueprint baseline** y revisión cruzada.

---

**Fin del documento**
