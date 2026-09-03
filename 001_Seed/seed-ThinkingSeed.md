# MASTER HYBRID SEED: ThinkingSeed

> **Propósito:** Snapshot técnico, verificable y portable del proyecto ThinkingSeed.
> **Instrucción al Agente:** Documento generado bajo el estándar ThinkingSeed_MasterHybrid.md respetando las etiquetas de evidencia y la política de seguridad.

## 0. REGLAS DE GENERACIÓN (Epistemología y Seguridad)
*   **Etiquetas de Evidencia:**
    *   `[CONFIRMADO]`: `001_Seed/ThinkingSeed_MasterHybrid.md`, `GEMINI.md`, `.agents/skills/seed/SKILL.md`.
    *   `[INFERIDO]`: `Engine`, `src`, `schemas` estructuran el pipeline de procesamiento del motor.
    *   `[FALTANTE]`: Tests unitarios automatizados (`tests/` requiere mayor cobertura explícita).
*   **Política de Seguridad:** Todos los parámetros y variables sensibles han sido revisados. No existen secretos ni contraseñas expuestas (`<REDACTED>`).

---

## 1. CORE MANIFESTO
   - **1.1 Objetivo Principal:** [CONFIRMADO] Proveer una plataforma y motor estandarizado para la creación de semillas técnicas (snapshots de proyectos/Seeds) híbridos para IA/Modelos LLM.
   - **1.2 Problema que Resuelve:** [CONFIRMADO] La pérdida de contexto, alucinación de arquitecturas y dispersión de documentación en proyectos complejos al interactuar con asistentes IA.
   - **1.3 Patrón Arquitectónico:** [CONFIRMADO] Arquitectura basada en conocimiento declarativo (Knowledge Base + Skills + Master Templates).
   - **1.4 Stack Principal:** [CONFIRMADO] Markdown, Python, Jupyter Notebooks.

## 2. REPOSITORY TOPOLOGY
   - `.agents/skills/seed/SKILL.md`: Workflow declarativo para la acción `/seed`. [CONFIRMADO]
   - `001_Seed/`: Almacenamiento de plantillas maestras y seeds generados (`ThinkingSeed_MasterHybrid.md`, `seed-ThinkingSeed.md`). [CONFIRMADO]
   - `GEMINI.md`: Reglas del workspace y políticas globales. [CONFIRMADO]
   - `Engine/`: Componentes del motor principal. [INFERIDO]
   - `Tools/` & `scripts/`: Herramientas auxiliares y scripts de mantenimiento. [CONFIRMADO]

## 3. EXECUTION FLOW
   - **3.1 Flujo E2E:** 
     `Invocación /seed` -> `Inspección de proyecto` -> `Validación de Evidencia/Seguridad` -> `Escritura en 001_Seed/seed-[proyecto].md`
   - **3.2 Entry Points:** Comandos slash `/seed`, inspección manual. [CONFIRMADO]
   - **3.3 Datos:** Plantilla base `ThinkingSeed_MasterHybrid.md` procesada para producir artefactos Markdown portables. [CONFIRMADO]

## 4. CURRENT STATE & RULES
   - **4.1 Foco actual:** Implementación del Workflow Slash `/seed` y estandarización del repo. [CONFIRMADO]
   - **4.2 Reglas de código:** Cumplimiento obligatorio de `GEMINI.md` y etiquetado epistemológico. [CONFIRMADO]
   - **4.3 Convenciones:** Seeds almacenados únicamente en `001_Seed/`. [CONFIRMADO]

## 5. ECOSYSTEM CONTEXT
   - Integración nativa con Antigravity CLI y modelos LLM (Gemini 3.6 Flash / Pro). [CONFIRMADO]

## 6. CONFIGURATION REFERENCE
   | Variable | Tipo | Default | Efecto | Sensible |
   | --- | --- | --- | --- | --- |
   | `PROJECT_DIR` | String | `./` | Directorio objetivo para el análisis | No |

## 7. SEGURIDAD, RIESGOS Y FAILURE MODES
   - **7.1 Security Findings:** Sin credenciales en el repositorio. [CONFIRMADO]
   - **7.2 Failure Modes:** En caso de no existir `001_Seed/`, el workflow la crea automáticamente. [CONFIRMADO]
   - **7.3 Riesgos técnicos:** Ausencia de `GEMINI.md` en subcarpetas puede generar desviaciones si no se carga el root. [INFERIDO]

## 8. SECCIONES OPCIONALES
   - **Testing Strategy:** Validación manual de generación de seeds por medio de inspección de archivos. [CONFIRMADO]

---

## 9. CONTEXT HANDOFF
Este documento es la fuente primaria para el proyecto ThinkingSeed.
