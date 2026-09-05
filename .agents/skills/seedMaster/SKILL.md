---
name: seedMaster
description: >-
  Crea un snapshot técnico exhaustivo y profundo (ADN completo) de un proyecto en formato seed-[nombre-proyecto]-master.md
  siguiendo el estándar ThinkingSeed Master.md y alojándolo en la carpeta 001_Seed del directorio actual.
  Usar cuando el usuario ponga /seedMaster o solicite crear el seed exhaustivo/profundo del proyecto.
---

# Workflow: Generación de ThinkingSeed Master Exhaustivo (`/seedMaster`)

Este workflow inspecciona a profundidad el proyecto o subdirectorio actual y genera un archivo de documentación arquitectónica de máxima granularidad denominado `seed-[nombre-proyecto]-master.md` alojado en `<directorio-actual>/001_Seed/`.

> **Nota de Frecuencia:** Esta skill es de **uso ocasional** para análisis profundos, auditorías exhaustivas o transferencias complejas de contexto donde se requiere máximo detalle. Para uso regular y ágil, utilizar `/seed`.

---

## Pasos de Ejecución

### Paso 1: Determinar Nombre del Proyecto y Ubicación
1. Identificar el nombre del proyecto o directorio actual.
2. Confirmar la ruta base del proyecto actual ($PROJECT_DIR).
3. Asegurar que existe la subcarpeta `$PROJECT_DIR/001_Seed/`. Si no existe, crearla.

### Paso 2: Inspección y Análisis Técnico Profundo
El agente actuará como **Arquitecto de Software, Analista de Repositorios y Documentador Técnico Senior** siguiendo el contrato de `ThinkingSeed Master.md`:

1. **Identidad, Manifiestos y Configuración:**
   - Leer manifiestos de dependencias, variables de entorno y archivos de configuración.
2. **Topología Completa:**
   - Estructurar el árbol excluyendo ruido (`.git`, `node_modules`, `__pycache__`, `.venv`, etc.).
3. **Flujos de Ejecución y Entry Points:**
   - Detallar cada punto de entrada, orquestadores, contratos de datos y APIs.
4. **Pruebas, CI/CD, Observabilidad y Despliegue:**
   - Mapear testing, Docker, pipelines y monitoreo.
5. **Brechas, Seguridad y Deuda Técnica:**
   - Documentar hallazgos de seguridad (`<REDACTED>`), inconsistencias y trabajo pendiente.

### Paso 3: Aplicar Reglas Epistemológicas y de Seguridad
1. **Etiquetas de Evidencia:**
   - `[CONFIRMADO]`: Observado directamente en código o configuración.
   - `[INFERIDO]`: Deducido lógicamente de varias señales.
   - `[DECLARADO]`: Presente en documentación pero no contrastado en código.
   - `[NO VERIFICADO]`: Requiere ejecución o acceso no disponible.
   - `[FALTANTE]`: Componente esperado ausente o no encontrado.
2. **Seguridad Rigurosa:**
   - Reemplazar cualquier secreto, token o clave privada por `<REDACTED>`.

### Paso 4: Generación del Archivo Seed Master
Crear o sobrescribir el archivo `$PROJECT_DIR/001_Seed/seed-[nombre-proyecto]-master.md` asegurando que inicie con el bloque de ADN y contexto pasivo, y concluya con el protocolo de asistencia:

```markdown
<!-- ============================================================================== -->
<!-- THINKINGSEED: ADN DEL PROYECTO (CONTEXTO PASIVO PARA MODELOS DE LENGUAJE)     -->
<!-- ============================================================================== -->
> [!NOTE]
> ### 🧬 DEFINICIÓN Y ROL DE ESTE DOCUMENTO
> 1. **¿Qué es este archivo?:** Este documento es una **Semilla de Proyecto (ThinkingSeed Master)**: representa el **ADN arquitectónico, técnico y estructural exhaustivo** del sistema. **NO es el repositorio completo de código fuente**, sino su mapa genético y memoria técnica profunda extraída directamente del entorno de desarrollo.
> 2. **Estado de Avance (Work in Progress):** Este documento refleja el **estado actual del desarrollo**. No garantiza que el proyecto esté concluido al 100%; puede representar un prototipo, un MVP o un sistema en evolución continua. La ausencia de código completo en ciertos archivos o módulos es **deliberada por diseño** para optimizar ventana de contexto o refleja áreas aún en desarrollo.
> 3. **Modo de Operación:** Trata este documento como **contexto pasivo de referencia técnica (Ground Truth)**. No asumas que el archivo está defectuoso ni intentes reescribirlo por tu cuenta.
<!-- ============================================================================== -->

# THINKING SEED MASTER: [Nombre del Proyecto]

## 0. IDENTIDAD Y METADATOS
```yaml
seed_schema_version: "2.0"
project_name: "[nombre]"
repository_name: "[nombre]"
project_type: "[tipo]"
repository_mode: "[modo]"
generated_at: "[ISO-8601]"
generated_by: "[agente/modelo]"
repository_root: "[ruta]"
git_branch: "[rama]"
git_commit: "[commit]"
working_tree_state: "[estado]"
analysis_mode: "static"
coverage_level: "high"
known_analysis_limits:
  - "[límites de inspección]"
```

### 0.1 Instrucciones para el modelo receptor
1. **ADN vs Repositorio:** Reconoce este documento como la memoria técnica y el ADN del proyecto, no como el repositorio completo ni como una prueba de ejecución.
2. **Contexto Pasivo:** No generes código no solicitado ni reclames por archivos ausentes; espera instrucciones específicas del usuario o utilízalo como contexto pasivo para responder preguntas sobre el funcionamiento del sistema.
3. **Estado de Avance:** Considera que las secciones incompletas o componentes marcados como `[FALTANTE]` representan el avance real del proyecto y oportunidades de asistencia, no errores del documento.
4. **Evidencia:** Respeta las etiquetas de evidencia y no transformes inferencias en hechos.
5. **Rutas:** Antes de proponer cambios, identifica módulos y archivos afectados citando sus rutas exactas relativas al repositorio.
6. **Contratos:** Conserva arquitectura, convenciones, contratos y restricciones declaradas.
7. **Preguntas Dirigidas:** No inventes componentes ausentes. Formula preguntas solo cuando la incertidumbre impida una respuesta segura.
8. **Seguridad:** No reveles ni solicites secretos. Usa placeholders (`<REDACTED>`).
9. **Impacto:** Evalúa impactos laterales en pruebas, configuración, datos, seguridad, observabilidad y despliegue.
10. **Asistencia:** Distingue entre solución inmediata, deuda técnica y recomendación futura.

---

## 1. RESUMEN EJECUTIVO
## 2. ARQUITECTURA Y TOPOLOGÍA
## 3. FLUJOS DE EJECUCIÓN Y ENTRY POINTS
## 4. MODELO DE DATOS, CONTRATOS Y PERSISTENCIA
## 5. CONFIGURACIÓN Y AMBIENTE
## 6. PRUEBAS, CI/CD Y OPERACIÓN
## 7. OBSERVABILIDAD Y MODOS DE FALLA
## 8. SEGURIDAD Y PRIVACIDAD
## 9. ESTADO REAL, DEUDA TÉCNICA Y LIMITACIONES
## 10. REGLAS PARA MODIFICAR EL PROYECTO

---

## 📌 CONTEXT HANDOFF & PROTOCOLO DE ASISTENCIA

> **Mensaje de orientación para el modelo de IA receptor:**
> "Esto es una semilla de proyecto (ThinkingSeed): el ADN del proyecto y no su repositorio completo. Refleja el avance real y la arquitectura del sistema hasta la fecha. Como modelo receptor, tu función es usar esta semilla como memoria técnica para:
> 1. **Responder preguntas** sobre la arquitectura, funcionamiento, dependencias y flujos del sistema.
> 2. **Sugerir mejoras o asistencia técnica** sobre el estado actual y áreas pendientes identificadas en la semilla.
> 3. **Generar código o soluciones compatibles** respetando las rutas, convenciones y patrones definidos aquí, cuando el usuario te lo solicite."

### Pautas de resolución:
Antes de resolver una solicitud:
1. Identifica el objetivo del usuario.
2. Localiza los componentes afectados usando las rutas del Seed.
3. Revisa restricciones, reglas y contratos declarados.
4. Explicita supuestos cuando sea necesario: "Supongo que X debido a Y".
5. Propone cambios por archivo con rutas claras.
6. Añade pruebas, riesgos y criterios de aceptación.

### 🤝 Acuse de Recibo Inicial
Si el usuario adjuntó esta semilla **sin una instrucción específica**, no intentes generar código ni completar archivos vacíos. Responde únicamente con:
1. Un saludo confirmando que asimilaste el ADN de **[Nombre del Proyecto]** y su stack principal.
2. Un breve resumen de 2-3 líneas sobre el objetivo y su estado actual de avance.
3. Una frase poniéndote a disposición para resolver dudas sobre su funcionamiento o colaborar en los siguientes pasos de desarrollo.
```

### Paso 5: Notificación
Confirmar al usuario la generación exitosa del archivo con el enlace relativo y absoluto al archivo `001_Seed/seed-[nombre-proyecto]-master.md`.
