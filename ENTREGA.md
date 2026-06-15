Entrega OpenSpec Sandbox — Eliana Rodríguez

Parte A — Aplicación de los 3 Pilares

Micro-tarea elegida: Generador de slugs a partir de un título.

Pilar 1 — Herramienta:
Elegí Claude Code porque será el copiloto que usaré para trabajar con el repositorio y porque permite interactuar directamente con el proyecto desde la terminal.

¿Por qué esta y no otra?
Porque se integra bien con flujos de desarrollo locales y me permite pedir implementación, revisión y explicación dentro del mismo contexto del repo.

Pilar 2 — Contexto:
Indique que se implementará la solucion con el lenguaje JavaScript/TypeScript, la necesidad de crear una función simple, ejemplos de entrada y salida, y restricciones como eliminar acentos, convertir a minúsculas y reemplazar espacios por guiones.

Contexto omitido conscientemente:
No incluí framework, base de datos ni dependencias externas porque la tarea es pequeña y se puede resolver con JavaScript nativo.

Pilar 3 — Prompt:
Estructuré el prompt indicando objetivo, restricciones, ejemplos esperados y formato de salida.

Prompt final usado:

Necesito una función en TypeScript que reciba un título y genere un slug URL-friendly.
Restricciones:
- Convertir todo a minúsculas.
- Eliminar acentos.
- Reemplazar espacios por guiones.
- Eliminar caracteres especiales.
- Evitar guiones duplicados.
- Eliminar guiones al inicio o al final.
- No usar librerías externas.
- Eliminar espacios al inicio y al final.
Ejemplos:
"Hola Mundo" -> "hola-mundo"
"Curso de IA para Developers!" -> "curso-de-ia-para-developers"
"  Café con Leche  " -> "cafe-con-leche"
Devuélveme solo:
1. La función TypeScript.
2. Una breve explicación.
3. Tres casos de prueba simples.

Resultado:
La solución funcionó a la primera. Claude Code generó una función TypeScript que cumplió con todos los requisitos planteados y los casos de prueba devolvieron los resultados esperados.
Una mejora que haría sería pedir desde el inicio tests automatizados con Jest para validar más casos borde.

⸻

Parte B — Evidencia de instalación de OpenSpec

Versión de Node

node --version
v23.11.0

Instalación de OpenSpec

npm install -g @fission-ai/openspec@latest
openspec --version
1.4.1

Estructura generada

ls -la
total 0
drwxr-xr-x  4 bctecnologia  staff  128 Jun 15 16:22 .
drwx------@ 9 bctecnologia  staff  288 Jun 15 16:19 ..
drwxr-xr-x@ 4 bctecnologia  staff  128 Jun 15 16:22 .claude
drwxr-xr-x@ 5 bctecnologia  staff  160 Jun 15 16:22 openspec

ls -R openspec/
changes     config.yaml specs

openspec/changes:
archive

openspec/changes/archive:

openspec/specs:
⸻

3 observaciones de exploracion OpenSpec

1. Me llamó la atención que las carpetas creadas por openspec no fueron iguales a las indicadas por la documentacion IA4Devs
    openspec/changes
    openspec/changes/archive
    openspec/specs
2. La idea de tener una “constitución” del proyecto me recordó a una mezcla entre documentación técnica, reglas de arquitectura y acuerdos de equipo.
3. El flujo propose → apply → archive ayuda a ordenar el trabajo para poder trabajar adecuadamente con la IA y manejar un trabajo bien echo desde el inicio.