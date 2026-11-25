# Prompt de Comparativa Multi-Modelo

## Contexto
Se ha ejecutado el mismo prompt de entrada (`05-fusion-de-etapas.md`) sobre 4 modelos diferentes. El prompt pide redactar una síntesis para una responsable de operaciones usando **únicamente los datos verificados**, con estas secciones obligatorias:
- Resumen (≤120 palabras)
- Tres hallazgos
- Datos pendientes
- Próximo paso propuesto

## Entrada común
Archivo: `05-fusion-de-etapas.md` (estructura: TAREA FINAL → ETAPAS → VERIFICACIONES → CONDICIONES DE CONTINUIDAD → GESTIÓN DE FALLOS → EVIDENCIAS → INFORME)

## Salidas a comparar
| Modelo | Archivo |
|--------|---------|
| Nemotron 3 Ultra | `05-01-nemotron.md` |
| Gemini | `05-02-gemini.md` |
| Copilot (GPT-4o) | `05-03-copilot.md` |
| ChatGPT (GPT-4o) | `05-04-chatgpt.md` |

---

## Prompt de evaluación comparativa

> **Actúa como evaluador experto en calidad de salidas de LLM.**  
> Recibes 4 respuestas generadas por distintos modelos ante **exactamente la misma entrada**.  
> Tu tarea: **comparar, contrastar y puntuar** cada respuesta según los criterios abajo.
>
> **Entrega:** Un informe en markdown con:
>
> ### 1. Tabla resumen de cumplimiento formal
> | Criterio | Nemotron | Gemini | Copilot | ChatGPT |
> |---|---|---|---|---|
> | Resumen ≤120 palabras | ✓/✗ + n° palabras | ✓/✗ + n° palabras | ✓/✗ + n° palabras | ✓/✗ + n° palabras |
> | Exactamente 3 hallazgos | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
> | Datos pendientes listados | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
> | Próximo paso incluido | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
> | **No añade info no verificada** (satisfacción, costes, causas, productividad) | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
> | Conserva distinción "primera respuesta" vs "resolución" | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
> | Formato markdown limpio | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |
>
> ### 2. Análisis cualitativo por dimensión
> Para cada dimensión, describe **diferencias concretas** entre modelos (cita textual si procede):
>
> **A. Fidelidad a la restricción "solo datos verificados"**
> - ¿Algún modelo introduce satisfacción, costes, causas, productividad o equipara primera respuesta con resolución?
>
> **B. Estructura y completitud de "Tres hallazgos"**
> - ¿Son 3 hallazgos distintos y atómicos?
> - ¿Repiten información o la combinan distinto?
> - ¿Incluyen la distribución por tipología (consultas/incidencias/sugerencias) como hallazgo separado?
>
> **C. Tratamiento de "Datos pendientes"**
> - ¿Listan solo los explícitos en el informe (satisfacción, costes)?
> - ¿Añaden desglose de pendientes por tipo/antigüedad (no está en el informe)?
> - ¿Incluyen "causas de pendientes" como dato pendiente (el informe lo propone como próximo paso, no como dato faltante)?
>
> **D. Redacción del "Próximo paso"**
> - ¿Copian literalmente "Analizar las causas de las solicitudes pendientes"?
> - ¿Reformulan? ¿Añaden matiz?
>
> **E. Calidad del Resumen (≤120 palabras)**
> - Concisión, fluidez, cobertura de los 4 puntos clave (volumen, resolución, primera respuesta, limitaciones)
> - ¿Mencionan la distribución por tipología?
>
> **F. Extras / Valor añadido**
> - ChatGPT incluye tabla de extracción de datos (pedida en CONDICIONES DE CONTINUIDAD, no en TAREA FINAL) → ¿es acierto o exceso?
> - Nemotron/Gemini/Copilot no la incluyen → ¿omisión o fidelidad estricta a TAREA FINAL?
>
> ### 3. Puntuación global (1-10) y justificación breve
> | Modelo | Puntuación | Justificación (1 frase) |
> |---|---|---|
> | Nemotron | | |
> | Gemini | | |
> | Copilot | | |
> | ChatGPT | | |
>
> ### 4. Conclusión y recomendación
> - ¿Qué modelo interpreta mejor la **intención estricta** del prompt (solo TAREA FINAL)?
> - ¿Qué modelo interpreta mejor el **contexto completo** (incluye CONDICIONES DE CONTINUIDAD)?
> - Recomendación según caso de uso: "síntesis ejecutiva estricta" vs "informe analítico completo".

---

## Instrucciones de uso
Ejecuta este prompt en un modelo evaluador (puede ser uno de los 4 o uno distinto) pasándole **los 4 archivos de salida** como contexto. El evaluador debe leerlos y producir el informe comparativo arriba descrito.