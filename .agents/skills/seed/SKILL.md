---
name: seed
description: >-
  Crea un snapshot técnico y portable de un proyecto en formato seed-[nombre-proyecto].md
  siguiendo el estándar ThinkingSeed_MasterHybrid.md y alojándolo en la carpeta 001_Seed
  del directorio donde se ejecute. Usar cuando el usuario ponga /seed o solicite crear el seed del proyecto.
---

# Workflow: Generación de ThinkingSeed Master Hybrid (`/seed`)

Este workflow inspecciona el proyecto o subdirectorio actual y genera un archivo de documentación técnica estructurada y verificable denominado `seed-[nombre-proyecto].md` alojado en `<directorio-actual>/001_Seed/`.

---

## Pasos de Ejecución

### Paso 1: Determinar Nombre del Proyecto y Ubicación
1. Identificar el nombre del proyecto o directorio actual (ej. `ThinkingSeed`, `MyCloudProject`, etc.).
2. Confirmar la ruta base del proyecto actual ($PROJECT_DIR).
3. Asegurar que existe la subcarpeta `$PROJECT_DIR/001_Seed/`. Si no existe, crearla.

### Paso 2: Inspección y Análisis Técnico
El agente actuará como **Arquitecto de Software Senior** e inspeccionará el repositorio para extraer los datos necesarios para llenar cada sección de la plantilla maestra:

1. **Raíz y Archivos Clave:** Leer `package.json`, `pyproject.toml`, `requirements.txt`, `go.mod`, `pom.xml`, `Dockerfile`, `docker-compose.yml`, o equivalentes para determinar stack, versiones y dependencias.
2. **Estructura del Proyecto:** Generar la topología del árbol de archivos omitiendo directorios no relevantes (`.git`, `node_modules`, `__pycache__`, `.venv`, etc.).
3. **Flujos de Ejecución y Entry Points:** Localizar los puntos de entrada principales (`main.py`, `index.js`, `App.tsx`, scripts de inicio) y mapear los flujos de datos.
4. **Variables de Configuración:** Inspeccionar archivos `.env.example`, `config.yaml`, o llamadas a variables de entorno.

### Paso 3: Aplicar Reglas de Epistemología y Seguridad
1. **Etiquetado de Evidencia:**
   - Usar `[CONFIRMADO]` para hallazgos directamente validados en el código/configuración.
   - Usar `[INFERIDO]` para deducciones lógicas sobre la arquitectura.
   - Usar `[FALTANTE]` para componentes esperados que no se hayan encontrado.
2. **Sanitización de Secretos:**
   - Reemplazar cualquier password, token, clave privada o credential string por `<REDACTED>`.

### Paso 4: Generación del Archivo Seed
Crear o sobrescribir el archivo `$PROJECT_DIR/001_Seed/seed-[nombre-proyecto].md` con el siguiente formato exacto basado en `ThinkingSeed_MasterHybrid.md`:

```markdown
# MASTER HYBRID SEED: [Nombre del Proyecto]

> **Propósito:** Snapshot técnico, verificable y portable.
> **Instrucción al Agente:** Actúa como Arquitecto de Software Senior. Inspecciona el repo y llena este documento respetando las etiquetas de evidencia y la política de seguridad.

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
   - 4.1 Foco actual y estado de madurez.
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

## 9. CONTEXT HANDOFF (Instrucciones para el Modelo Receptor)
Este documento es la fuente primaria. Antes de proponer cambios, el modelo debe:

1.  **Entender:** Identificar el objetivo y componentes afectados.
2.  **Validar:** Si la información falta, **preguntar** en lugar de alucinar.
3.  **Justificar:** Citar rutas del repositorio al proponer cambios.
4.  **Respetar:** Mantener arquitectura, contratos y restricciones de seguridad.
5.  **Proponer:** Detallar archivos a modificar/crear y riesgos de rollback.
6.  **Supuestos:** Si debe asumir, marcar explícitamente: "Supongo que X debido a Y".
```

### Paso 5: Notificación
Confirmar al usuario la generación exitosa del archivo con el enlace relativo y absoluto al archivo `001_Seed/seed-[nombre-proyecto].md`.
