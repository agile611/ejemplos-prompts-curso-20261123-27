Extrae los datos del correo y devuelve únicamente JSON válido.

Utiliza el esquema incluido abajo.
No añadas bloques Markdown ni explicaciones externas.
No inventes valores.
Conserva aproximaciones, preferencias y propuestas.

Convierte dos horas a 120 minutos.
Utiliza fecha ISO cuando la fecha sea explícita e inequívoca.
La fecha propuesta debe conservar el estado "propuesta".

ESQUEMA
tema: texto
participantes:
  valor: entero o null
  estado: exacto, aproximado o no_indicado
modalidad:
  valor: texto o null
  estado: preferencia, confirmada o no_indicada
duracion_minutos: entero o null
fecha:
  valor: fecha ISO o null
  estado: propuesta, confirmada o no_indicada
coordinacion: texto o null
aula_estado: pendiente, confirmada o no_indicada
presupuesto_estado: no_definido, definido o no_indicado
ejemplos: ficticios, reales o no_indicado

CORREO
Hola:

Hemos recibido vuestra consulta sobre una introducción a Prompt Engineering
para aproximadamente 12 personas del equipo administrativo.

Recogemos la preferencia por una sesión presencial de dos horas
y la propuesta del 18 de noviembre de 2026.

Entendemos que la fecha, el aula y el presupuesto siguen pendientes.
También recogemos la necesidad de utilizar únicamente ejemplos ficticios.

Para preparar las opciones:
- ¿Cuándo podréis confirmar la fecha?
- ¿Qué información estará disponible sobre el aula?
- ¿Cuándo prevéis definir el presupuesto?

Gracias.