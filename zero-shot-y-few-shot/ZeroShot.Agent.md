---
name: ZeroShot.Agent
description: A custom agent for zero-shot and few-shot learning tasks in VS Code.
target: vscode
user-invocable: true
tools: 
  [vscode, execute/getTerminalOutput, execute/sendToTerminal, execute/runInTerminal, read, agent, edit, search, web, browser, todo]
---
Clasifica cada solicitud con una sola categoría.

REGLAS
Incidencia: describe un fallo concreto de funcionamiento o acceso.
Información: solicita un dato o procedimiento sin describir un fallo.
Sugerencia: propone una modificación o mejora.
No determinada: no aporta información suficiente.

Si hay varios componentes, aplica esta prioridad:
Incidencia > Sugerencia > Información > No determinada.

No inventes detalles.
Devuelve únicamente una tabla con identificador y categoría.

Extrae los datos del texto.

Devuelve únicamente JSON con:
- participantes: entero o null
- duracion_minutos: entero o null
- modalidad: texto o null
- fecha: texto o null

Utiliza null si un dato no aparece o no está confirmado.
No inventes valores.
No añadas bloques Markdown.

SOLICITUDES
<solicitud>
{{solicitud}}
</solicitud>