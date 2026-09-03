# GLOBAL WORKSPACE RULES: ThinkingSeed Standard

> **Ámbito:** Este archivo aplica a todo el workspace y establece las reglas obligatorias para la generación y gestión de documentación técnica, arquitectura y análisis de código.

---

## 1. ESTÁNDAR THINKINGSEED & REPOSITORIO DE SEEDS
- Todos los documentos de arquitectura y snapshots de proyecto deben seguir rigurosamente la estructura definida en la plantilla maestra [`ThinkingSeed_MasterHybrid.md`](file:///d:/0001%20HyperScale%20Thinking/PROYECTOS%20CLOUD/engineData/ThinkingSeed/001_Seed/ThinkingSeed_MasterHybrid.md).
- Los archivos seed generados deben almacenarse siempre dentro de la subcarpeta `001_Seed/` del directorio del proyecto o donde se ejecute la solicitud, siguiendo la convención de nombre: `seed-[nombre-proyecto].md`.

---

## 2. RIGOR EPISTEMOLÓGICO Y EVIDENCIA
Toda afirmación técnica dentro de los seeds o reportes generados debe etiquetarse explícitamente:
- `[CONFIRMADO]`: Datos, dependencias, configuraciones o código observados directamente en la inspección del proyecto.
- `[INFERIDO]`: Deducciones lógicas razonables basadas en la arquitectura, pero no declaradas de forma explícita.
- `[FALTANTE]`: Componentes, configuraciones o documentación esperables pero ausentes en el proyecto.

---

## 3. POLÍTICA RIGUROSA DE SEGURIDAD
- **PROHIBICIÓN ABSOLUTA:** Queda estrictamente prohibido incluir o reproducir llaves de API, credenciales, contraseñas, tokens JWT, certificados privados o cadenas de conexión con credenciales explícitas en cualquier archivo generado.
- **Redacción de Datos Sensibles:** Todo valor sensible debe ser reemplazado por la etiqueta `<REDACTED>`. Si se detectan secretos commiteados en código o configuraciones, registrar el hallazgo como alerta de seguridad sin exponer el valor.

---

## 4. WORKFLOWS Y COMANDOS
- Para crear o actualizar un seed de proyecto, utilizar la Skill `/seed` o solicitar la creación del snapshot técnico del proyecto.
