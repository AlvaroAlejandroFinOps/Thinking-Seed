![alt text](image.png)
# Thinking Seed - Semilla de Proyectos - Gravity HyperScale Thinking

![Status](https://img.shields.io/badge/Despliegue_de_semillas-GravityHyperScaleThinking-yellow)

![Framework](https://img.shields.io/badge/Gemini_1.5_Pro-Google-blueviolet)
![Framework](https://img.shields.io/badge/Claude_3.5_Opus-Anthropic-blueviolet)
![Framework](https://img.shields.io/badge/GPT_5.6_SOL-OpenAI-blueviolet)
![Framework](https://img.shields.io/badge/DeepSeek_V4-DeepSeek-blueviolet)
![Framework](https://img.shields.io/badge/Kimi_K2-Kimi-blueviolet)
![Framework](https://img.shields.io/badge/Llama_4.1-Meta-blueviolet)
![Framework](https://img.shields.io/badge/Mistral_Large_3-Mistral-blueviolet)
![Framework](https://img.shields.io/badge/Qwen_Max-Alibaba-blueviolet)
![Framework](https://img.shields.io/badge/Grok_3-xAI-blueviolet)


> **Protocolo de Snapshot Técnico para Modelos de Razonamiento Extendido (Frontier Model)**

Seed de Gravity HyperScale Thinking es un marco de trabajo de ingeniería diseñado para cerrar la brecha entre la complejidad de los repositorios de software actuales y la capacidad de los modelos de lenguaje (LLMs) para procesar, entender y operar sobre ellos sin ambigüedades.

En lugar de depender de prompts genéricos, Thinking Seed estandariza la creación de un `Seed.md`: un contrato técnico autosuficiente que actúa como la "fuente de verdad" para cualquier agente conversacional, IDE avanzado o auditoría de arquitectura.

## 1. El Problema que Resuelve

> **Definición Estratégica: ¿Por qué GHT?
"Seed de Gravity HyperScale Thinking es el estándar de interoperabilidad cognitiva para el desarrollo de software. Al encapsular la arquitectura, el estado y las restricciones del proyecto en un snapshot autónomo (Seed.md), GHT permite desacoplar el razonamiento del modelo de la infraestructura física del repositorio.

## Esto transforma la manera en que interactúas con los agentes:

> **Portabilidad Multi-Modelo:** Puedes generar una semilla en un entorno de desarrollo avanzado y consumirla en cualquier motor de inferencia externo (desde Claude o GPT hasta modelos locales), asegurando que el    razonamiento sea consistente independientemente de la plataforma.

>  **Eficiencia Extrema:** 
>  Reduce drásticamente el token budget al evitar la carga completa de archivos irrelevantes, enfocando la atención del modelo únicamente en la estructura y lógica del sistema.

> **Reducción de Alucinaciones:** 
> Al proporcionar una fuente de verdad verificable y estructurada, obligas al modelo a trabajar dentro de los límites reales de tu arquitectura, eliminando conjeturas.

> **Perspectiva Cruzada:** 
> Potencia el análisis al permitir que distintos modelos evalúen, critiquen y propongan soluciones desde ángulos técnicos diversos, sin necesidad de acceso directo al código fuente."**

Los LLMs sufren de "pérdida de contexto" en repositorios grandes o complejos. Seed de GHT elimina la incertidumbre al obligar a una inspección basada en evidencia, hechos observables e inferencias declaradas, evitando alucinaciones y garantizando que las sugerencias de código respeten los contratos, dependencias y restricciones reales del sistema.

## 2. Aplicación y Flujo de Trabajo

Para integrar GHT en tu repositorio, sigue este ciclo de vida:

### Fase A: Inicialización
1. **Integración:** Copia la definición del contrato (contenido en la documentación técnica) en `docs/GHT_SPEC.md` de tu repositorio.
2. **Generación:** Ejecuta el proceso de análisis del repositorio (manual o automatizado) siguiendo las reglas del "Contrato de Generación" definido en la especificación.
3. **Producción:** Genera el archivo `Seed.md` en la raíz del repositorio.

### Fase B: Operación (Handoff)
Cuando necesites que un modelo de IA realice cambios, refactorizaciones o análisis:
1. **Context Handoff:** Adjunta el archivo `Seed.md` junto con tu prompt.
2. **Validación:** El modelo debe validar sus propuestas contra las restricciones listadas en el `Seed.md` (patrones arquitectónicos, contratos de datos, dependencias).

### Fase C: Mantenimiento
El `Seed.md` debe tratarse como un artefacto versionado:
* **Pre-Commit:** Se recomienda actualizar el `Seed.md` en hitos de arquitectura o cambios mayores de infraestructura.
* **Changelog:** Cada vez que el repositorio evolucione, agrega una entrada al `Seed Changelog` dentro del mismo archivo `Seed.md` para mantener la trazabilidad.

## 3. Estructura del Contrato (Seed.md)

El `Seed.md` generado sigue una jerarquía estricta para garantizar la coherencia:

| Sección | Propósito |
| :--- | :--- |
| **0. Identidad** | Metadatos y límites del análisis. |
| **1-3. Resumen y Topología** | Visión ejecutiva y árbol del proyecto. |
| **4-6. Arquitectura y Contratos** | APIs, flujos de ejecución y diagramas. |
| **7-9. Datos y Dependencias** | Persistencia, entornos y stack tecnológico. |
| **10-12. Desarrollo y CI/CD** | Prerrequisitos, pruebas y despliegue. |
| **13-17. Operación y Evolución** | Observabilidad, fallas y decisiones (ADR). |

## 4. Reglas de Oro para Agentes (Prompts)

Cualquier modelo que utilice un `Seed.md` debe respetar estas directrices no negociables:
* **Evidencia requerida:** Toda afirmación debe citar una ruta (`src/api/main.py:42`).
* **Cero Alucinaciones:** Si el componente no está en el `Seed.md`, no existe.
* **Seguridad:** Los secretos y datos sensibles siempre se marcan como `<REDACTED>`.
* **Criterios de Aceptación:** Cualquier propuesta de cambio debe incluir su plan de validación.

---

## 5. Integración con Git

Para mantener el `Seed.md` siempre relevante:

```bash
# Ejemplo de workflow manual
# 1. Analizar estado actual del repo
# 2. Generar/Actualizar Seed.md
# 3. Commit del nuevo snapshot técnico
git add Seed.md
git commit -m "docs(seed): update architectural snapshot for [version/feature]"
git push