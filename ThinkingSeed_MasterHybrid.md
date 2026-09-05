<!-- ============================================================================== -->
<!-- THINKINGSEED: ADN DEL PROYECTO (CONTEXTO PASIVO PARA MODELOS DE LENGUAJE)     -->
<!-- ============================================================================== -->
> [!NOTE]
> ### 🧬 DEFINICIÓN Y ROL DE ESTE DOCUMENTO
> 1. **¿Qué es este archivo?:** Este documento es una **Semilla de Proyecto (ThinkingSeed)**: representa el **ADN arquitectónico, técnico y estructural** del sistema. **NO es el repositorio completo de código fuente**, sino su mapa genético y memoria técnica de alta fidelidad extraída del entorno de desarrollo.
> 2. **Estado de Avance (Work in Progress):** Este documento refleja el **estado actual del desarrollo**. No garantiza que el proyecto esté 100% terminado; puede representar un proyecto en curso, un MVP o una arquitectura en expansión. Que no aparezca el código de todos los archivos es **deliberado por diseño** para optimizar la ventana de contexto.
> 3. **Modo de Operación:** Trata este documento como **contexto pasivo de referencia técnica (Ground Truth)**. No asumas que el archivo está defectuoso ni intentes reescribirlo por tu cuenta.
<!-- ============================================================================== -->

# MASTER HYBRID SEED: [Nombre del Proyecto]

> **Propósito:** Snapshot técnico, verificable y portable (ADN del proyecto).
> **Instrucción al Agente Generador:** Actúa como Arquitecto de Software Senior. Inspecciona el repo y llena este documento respetando las etiquetas de evidencia y la política de seguridad.

## 0. REGLAS DE GENERACIÓN (Epistemología y Seguridad)
*   **Etiquetas de Evidencia:** Toda afirmación debe llevar:
    *   `[CONFIRMADO]`: Observado directamente en código/config.
    *   `[INFERIDO]`: Deducción lógica (no declarado).
    *   `[FALTANTE]`: Esperado, pero no hallado.
*   **Política de Seguridad:** **PROHIBIDO** reproducir secretos, passwords, tokens o connection strings. Sustituye siempre por `<REDACTED>`. Si existen secretos versionados, regístralo como hallazgo sin reproducir el valor.

---

## 1. CORE MANIFESTO
   - 1.1 Objetivo Principal
   - 1.2 Problema que Resuelve
   - 1.3 Patrón Arquitectónico
   - 1.4 Stack Principal (Versiones y fuente: manifest/lockfile)

## 2. REPOSITORY TOPOLOGY
   - Tree completo (omitir ruido: `.git`, `node_modules`, `__pycache__`, etc.)
   - 2.x Diferenciaciones clave entre carpetas ambiguas.

## 3. EXECUTION FLOW
   - 3.1 Flujo E2E (Diagrama Mermaid o ASCII)
   - 3.2 Entry Points (Qué comandos/triggers inician qué procesos)
   - 3.3 Datos: Origen, transformación y persistencia.

## 4. CURRENT STATE & RULES
   - 4.1 Foco actual y estado de madurez (avance del proyecto).
   - 4.2 Reglas de código y convenciones (Style, linting, tipado).
   - 4.3 Convenciones de directorios.

## 5. ECOSYSTEM CONTEXT
   - Proyectos hermanos, dependencias externas, integraciones críticas.

## 6. CONFIGURATION REFERENCE
   - Tabla: Variable | Tipo | Default | Efecto | Sensible (Sí/No)

## 7. SEGURIDAD, RIESGOS Y FAILURE MODES
   - 7.1 Security Findings: Análisis de vulnerabilidades estáticas.
   - 7.2 Failure Modes: ¿Qué pasa si falla la fuente? ¿Qué pasa ante re-ejecución? ¿Existe idempotencia?
   - 7.3 Riesgos técnicos: Deuda técnica, bloqueos, dependencias críticas.

## 8. SECCIONES OPCIONALES (Si aplica)
   - Dependency Graph, Data Contracts, ADRs (Decisions Log), Testing Strategy.

---

## 9. CONTEXT HANDOFF & PROTOCOLO DE ASISTENCIA (Para el Modelo Receptor)

> **Orientación para el modelo de IA lector:**
> "Este documento es una semilla técnica: el ADN del proyecto y no su repositorio completo. Refleja la arquitectura y el avance real hasta la fecha. Como modelo receptor, utiliza esta semilla como memoria de trabajo para:
> 1. **Responder preguntas** sobre la arquitectura, funcionamiento, dependencias y flujos del sistema.
> 2. **Sugerir mejoras o asistencia técnica** basadas en el estado actual y áreas pendientes identificadas.
> 3. **Generar código o soluciones compatibles** respetando las rutas, convenciones y patrones definidos aquí, cuando el usuario te lo solicite."

### Directrices de interacción para la IA receptora:
1. **Entender:** Identificar el objetivo y los componentes afectados antes de proponer código.
2. **Validar:** Si falta información crítica, preguntar puntualmente en vez de alucinar.
3. **Citar Rutas:** Usar las rutas de archivo declaradas en la topología al sugerir modificaciones.
4. **Respetar:** Mantener el stack, contratos y restricciones de seguridad.
5. **Acuse de Recibo Inicial:** Si el usuario adjuntó esta semilla sin una pregunta concreta, responde en máximo 3 líneas resumiendo el nombre del proyecto, stack y objetivo, confirmando que has asimilado el ADN del proyecto y quedando a la espera de sus consultas o tareas.

