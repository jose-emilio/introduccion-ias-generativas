# 4.2 Ingeniería de Prompts (Prompt Engineering)

La ingeniería de prompts es la disciplina que desarrolla metodologias para comunicarse con eficiencia con modelos generativos. Su dominio transforma al usuario de mero espectador a director activo del comportamiento del modelo, permitiendo extraer resultados predecibles, relevantes y alineados con los objetivos del negocio.

## Que es un prompt

Un prompt es un bloque de texto instructivo que guía el comportamiento de la IA. Define al mismo tiempo el que, el como, el para que y las restricciones con las que el modelo debe responder. Es, en esencia, la interfaz de programación del lenguaje natural.

## Por que es crucial el prompt engineering

La inversión en prompt engineering produce retornos cuantificables:

- **80% de reducción de iteraciones**: prompts bien diseñados requieren menos correcciones.
- **60% de ahorro en tokens**: prompts eficientes consumen menos recursos.
- **95% de relevancia del output**: las respuestas se alinean con las expectativas del usuario.

## Elementos de un prompt efectivo

Un prompt efectivo se compone de cuatro elementos fundamentales:

1. **Instrucción**: verbo imperativo que determina la acción cognitiva.
2. **Contexto**: antecedentes, audiencia y restricciones que reducen la ambiguedad.
3. **Ejemplos (few-shot)**: muestras resueltas que ilustran el formato y estilo esperados.
4. **Formato**: especificación de la estructura de salida deseada.

### Elemento 1: Instrucción clara

El verbo imperativo determina la acción cognitiva que debe realizar el modelo. Ejemplos de verbos efectivos:

- **Resume**: sintetiza información extensa.
- **Clasifica**: categoriza elementos segun criterios.
- **Analiza**: descompone y evalua componentes.
- **Redacta**: genera contenido nuevo.
- **Traduce**: convierte entre idiomas.
- **Extrae**: recupera información específica.

### Elemento 2: Contexto robustecido

El contexto elimina la ambiguedad al proporcionar:

- Contexto del dominio y la situación específica.
- Definición de la audiencia objetivo.
- Restricciones explicitas sobre el contenido y el tono.

### Elemento 3: Ejemplos de soporte (Few-shot)

Incluir ejemplos resueltos en el prompt muestra al modelo el estilo, la longitud, el tono y la estructura esperados. Cuantos más ejemplos representativos se proporcionen, mayor sera la consistencia de la salida.

### Elemento 4: Formato deseado

Especificar el formato de salida evita reinterpretaciones. Puede solicitarse:

- Tablas comparativas.
- JSON estructurado.
- Listas numeradas o con vinetas.
- Longitud controlada (numero de parrafos, palabras o caracteres).

## Técnicas de prompt engineering

### Zero-shot Prompting

Consiste en proporcionar una instrucción directa sin incluir ejemplos previos. Es adecuada para tareas simples y bien definidas donde el modelo ya posee el conocimiento necesario.

### Few-shot Prompting

Consiste en incluir entre 1 y 3 ejemplos resueltos dentro del prompt. Esta técnica aumenta significativamente la consistencia del formato y el estilo de la respuesta, especialmente útil en tareas especializadas o con formatos de salida muy concretos.

### Definición de rol (Persona)

La asignación de un rol específico al modelo fuerza la adopción de un lexico técnico, unas metodologias y un enfoque profesional determinados. Por ejemplo: "Actua como un auditor financiero senior especializado en cumplimiento normativo."

#### El impacto de la asignación de roles

La asignación de roles produce tres efectos principales:

- **Concentración semantica**: el modelo selecciona vocabulario y conceptos propios del rol asignado.
- **Tono y registro adaptado**: la formalidad y el estilo se ajustan al rol.
- **Reducción de generalismo**: se evitan respuestas vagas o genéricas.

### Cadena de pensamiento (Chain of Thought, CoT)

Consiste en forzar al modelo a explicar los pasos intermedios de su razonamiento antes de dar la respuesta final. La instrucción típica es: "Razona paso a paso antes de dar tu respuesta final."

#### Ventajas de la cadena de pensamiento

- **Reducción de errores lógicos**: al exteriorizar el razonamiento, se detectan y corrigen fallos internos.
- **Trazabilidad del razonamiento**: permite auditar como el modelo llega a sus conclusiones.
- **Valor pedagogico**: el proceso de razonamiento puede utilizarse como material formativo.

## Consejos prácticos de optimización

- **Ser directo y específico**: evitar rodeos y lenguaje impreciso.
- **Usar delimitadores lógicos**: separadores como """ o ### ayudan a distinguir instrucciones de contenido.
- **Evitar la ambiguedad**: cada instrucción debe admitir una única interpretación.

### Uso de delimitadores en prompts

Los delimitadores separan visual y logicamente la instrucción del contenido sobre el que se opera. Sin delimitadores, el modelo puede confundir ambas partes. Con delimitadores, la estructura es clara y la ejecución precisa.

### Evitar la ambiguedad instruccional

**Incorrecto**: "Escribe algo sobre nuestro nuevo producto para redes sociales."

**Correcto**: "Redacta 3 publicaciones para LinkedIn dirigidas a directores de RRHH, destacando los beneficios en ahorro de tiempo y cumplimiento normativo."

### El proceso de iteración del prompt

El prompt perfecto no se consigue al primer intento. El proceso de optimización es iterativo:

1. Redactar una primera versión del prompt.
2. Ejecutar y analizar el error en la respuesta.
3. Ajustar la instrucción, el contexto o los ejemplos.
4. Repetir hasta obtener la calidad deseada.

## Bibliotecas de prompts corporativas

La institucionalización del prompt engineering pasa por crear repositorios centralizados de prompts validados. Estas bibliotecas permiten:

- **Organización por departamento**: cada area funcional dispone de sus propias plantillas.
- **Control de versiones**: seguimiento de cambios y mejora continua.
- **Acceso democratico**: cualquier miembro de la organización puede utilizar prompts validados.

## Resumen de la sección 4.2

La ingeniería de prompts comprende tres dimensiones fundamentales:

- **Anatomía del prompt**: instrucción, contexto, ejemplos y formato.
- **Técnicas avanzadas**: zero-shot, few-shot, definición de rol y cadena de pensamiento.
- **Institucionalización**: creación de bibliotecas corporativas de prompts y procesos de iteración continua.

---

[Anterior: 4.1 Comparación de LLMs](01-comparacion-llms.md) | [Volver al índice](index.md) | [Siguiente: 4.3 Seguridad y riesgos](03-seguridad-riesgos.md)

