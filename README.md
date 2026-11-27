# Ejemplos y ejercicios de Prompt Engineering

Repositorio de materiales y ejercicios del curso de Prompt Engineering de Agile611. Incluye ejemplos sobre cómo redactar, revisar y ejecutar prompts, además de casos de descomposición y verificación de tareas.

## Referencias del curso

- [Taller de Prompts (Día 1)](https://docs.agile611.com/curso-prompt-engineering/dia-01-fundamentos/04-taller-de-prompts/)
- [Anatomía del Prompt (Día 1)](https://docs.agile611.com/curso-prompt-engineering/dia-01-fundamentos/03-anatomia-del-prompt/)
- [Zero-shot y Few-shot (Día 2)](https://docs.agile611.com/curso-prompt-engineering/dia-02-tecnicas/01-zero-shot-y-few-shot/#43-few-shot-para-extraccion)
- [Diseño de Pruebas (Día 3)](https://docs.agile611.com/curso-prompt-engineering/dia-03-evaluacion-y-seguridad/01-diseno-de-pruebas/)

## Contenido

### `anatomia-del-prompt/`

Ejercicios sobre revisión y estructura de prompts: primeros intentos y versiones revisadas, redacción de correos, clasificación, creatividad con límites, salida JSON, contradicciones e instrucciones incrustadas. Incluye también `documento-de-entrada.md` y `plantilla.md`.

### `taller-de-prompts/`

Casos prácticos para mejorar solicitudes progresivamente:

- **A–D:** solicitudes completas o incompletas, tratamiento de condiciones y separación entre instrucciones y datos.
- **E:** evolución de prompts para redactar correos y consolidar documentación.
- **F:** ejercicios de resumen y ejecución, entrada y objetivo, revisión, reglas de ejecución, creatividad abierta y validación (`F-32` a `F-38`, `F-310`, `F-311` y `F-314`).

### `descomposicion-y-verificacion/`

Caso de análisis de un informe de operaciones, trabajado mediante extracción de datos, cálculos y síntesis. Incluye informes de entrada, fichas, plantillas y prompts integrados; variantes para tratar contradicciones, denominadores ausentes y ampliaciones; además de resultados de varios modelos y una comparativa.

### `zero-shot-y-few-shot/`

Prompts de ejemplo zero-shot y few-shot, tanto generales como para extracción; casos de desarrollo con zero-shot y dos archivos de agente (`ZeroShot.Agent.md` y `FewShot.Agent.md`) con instrucciones y ejemplos.

### `diseno-y-pruebas/`

Ejercicios de evaluación y seguridad: extracción de requisitos con políticas estrictas, casos de prueba (D01–D04, T01–T06) y plantilla de evaluación. Se respalda en [Diseño de Pruebas (Día 3)](https://docs.agile611.com/curso-prompt-engineering/dia-03-evaluacion-y-seguridad/01-diseno-de-pruebas/).

### `laboratorio-comparativo/`

[Laboratorio Comparativo](https://docs.agile611.com/curso-prompt-engineering/dia-02-tecnicas/04-laboratorio-comparativo/) — ejercicios de comparación de prompts con condiciones A y B, incluyendo prompts base y definiciones de agente.

### `docs/`

- `markdown.md` — guía introductoria de Markdown.

## Agentes de ejemplo

`zero-shot-y-few-shot/ZeroShot.Agent.md` y `zero-shot-y-few-shot/FewShot.Agent.md` contienen definiciones de agentes dirigidas a VS Code. No hay configuraciones de agentes guardadas en `.copilot/agents/` en este repositorio.

## Autoría y licencia

| Campo | Información |
|---|---|
| Autor | Guillem Hernández Sola |
| Organización | Agile611 |
| Licencia | [Apache License 2.0](LICENSE) |