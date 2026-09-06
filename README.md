# HumanizIA

Reescribe un texto para que no se note escrito por una IA, sin cambiar lo que dice.

Aplicación de un solo fichero HTML, sin instalación ni servidor: se abre en el navegador
y llama a la API de OpenAI con la clave del propio usuario, que se guarda solo en el
almacenamiento local.

Reproduce de forma navegable el skill [blader/humanizer](https://github.com/blader/humanizer)
(MIT), basado a su vez en
[Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing),
mantenido por WikiProject AI Cleanup.

## Qué hace

- **Catálogo de 35 patrones** en español, activables uno a uno: importancia inflada,
  atribuciones vagas, vocabulario de IA, huida del verbo ser, tríadas forzadas, rangos
  falsos, rayas, emojis, restos de conversación, muletillas, aforismos de fórmula y el
  resto de huellas del catálogo original.
- **Bucle borrador → crítica → final.** Reescribe, pregunta al modelo qué sigue sonando
  a máquina en su propio borrador y vuelve a reescribir con esa respuesta delante. Los
  tres artefactos quedan a la vista.
- **Índice de huellas por mil palabras**, calculado en el navegador con reglas fijas y
  sin coste, antes y después de la reescritura.
- **Muestra de voz opcional:** con dos o tres párrafos del autor, la reescritura imita su
  ritmo, su puntuación y su vocabulario en vez del estilo por defecto.
- **Registro del texto:** personal, divulgativo, técnico o académico. En los dos últimos
  no se inyecta voz ni opinión, porque ahí lo neutro y llano ya es la escritura humana
  correcta.
- **Verificación dura del resultado:** cero rayas, comillas rectas, sin emojis, mismo
  número de párrafos y extensión conservada, con pasada de reparación dirigida solo a lo
  que falla.
- **Guardia de datos:** lista las cifras y los nombres propios que aparecen en el texto
  final y no estaban en el original, que es la comprobación mecánica de la regla de no
  inventar nada.
- Segmentación por bloques para textos largos, comparación párrafo a párrafo y
  exportación a Markdown, Word y JSON.

## Uso

Abre `index.html` en el navegador, pega tu clave de OpenAI en el paso 0 y elige modelo:
gpt-4o-mini para pruebas, o la familia gpt-5.6 (luna, terra, sol) para textos largos.

## Alcance y uso responsable

HumanizIA mejora el estilo de un texto. No es una herramienta para eludir detectores de IA ni marcados de procedencia, y su uso no exime de declarar que se ha empleado IA.

La reescritura solo puede trabajar con lo que dice el texto de partida: un nombre, una cifra, una fecha o una cita nunca se inventan, y la app incluye una comprobación automática que avisa de cualquier dato que aparezca en el resultado y no estuviera en el original.

## Autoría

Fernando Borrás Rocher, Universidad Miguel Hernández de Elche.
ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573).

Licencia MIT.
