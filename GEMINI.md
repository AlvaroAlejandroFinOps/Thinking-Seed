# GLOBAL WORKSPACE RULES: ThinkingSeed Standard

> **Ámbito:** Este archivo aplica a todo el workspace y establece las reglas obligatorias para la generación y gestión de documentación técnica, arquitectura y análisis de código.

---

## 1. ESTÁNDAR THINKINGSEED & CONCEPTO DE ADN
- Un ThinkingSeed es el **ADN arquitectónico y memoria técnica** de un proyecto, **NO su repositorio de código completo**.
- Todo seed generado debe incluir el bloque de **Directiva para Modelos de IA** al inicio (aclarando que es contexto pasivo y snapshot de avance en curso) y el **Protocolo de Asistencia & Handshake** al cierre.
- Los archivos seed generados deben almacenarse siempre dentro de la subcarpeta `001_Seed/` del directorio del proyecto o donde se ejecute la solicitud.

---

## 2. WORKFLOWS Y SKILLS DE GENERACIÓN
Existen dos niveles de profundidad para la generación de seeds:

1. **`/seed` (Estándar Híbrido - Uso Frecuente):**
   - Basado en [`ThinkingSeed_MasterHybrid.md`](file:///d:/0001%20HyperScale%20Thinking/PROYECTOS%20CLOUD/engineData/ThinkingSeed/ThinkingSeed_MasterHybrid.md).
   - Genera: `001_Seed/seed-[nombre-proyecto].md`.
   - Ágil, condensado y enfocado en transferir el ADN de forma eficiente a chats de IA comercial.

2. **`/seedMaster` (Estándar Exhaustivo - Uso Ocasional):**
   - Basado en [`ThinkingSeed Master.md`](file:///d:/0001%20HyperScale%20Thinking/PROYECTOS%20CLOUD/engineData/ThinkingSeed/ThinkingSeed%20Master.md).
   - Genera: `001_Seed/seed-[nombre-proyecto]-master.md`.
   - Análisis profundo, minucioso y exhaustivo para auditorías completas, migraciones o arquitecturas de alta complejidad.

---

## 3. RIGOR EPISTEMOLÓGICO Y EVIDENCIA
Toda afirmación técnica dentro de los seeds o reportes generados debe etiquetarse explícitamente:
- `[CONFIRMADO]`: Datos, dependencias, configuraciones o código observados directamente en la inspección del proyecto.
- `[INFERIDO]`: Deducciones lógicas razonables basadas en la arquitectura, pero no declaradas de forma explícita.
- `[FALTANTE]`: Componentes, configuraciones o documentación esperables pero ausentes en el proyecto (refleja el avance real en curso).

---

## 4. POLÍTICA RIGUROSA DE SEGURIDAD
- **PROHIBICIÓN ABSOLUTA:** Queda estrictamente prohibido incluir o reproducir llaves de API, credenciales, contraseñas, tokens JWT, certificados privados o cadenas de conexión con credenciales explícitas en cualquier archivo generado.
- **Redacción de Datos Sensibles:** Todo valor sensible debe ser reemplazado por la etiqueta `<REDACTED>`. Si se detectan secretos commiteados en código o configuraciones, registrar el hallazgo como alerta de seguridad sin exponer el valor.

