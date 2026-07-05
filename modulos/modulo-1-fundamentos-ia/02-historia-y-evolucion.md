# 1.2 Historia y evolución de la IA

Este recorrido por los principales hitos que pavimentaron el camino hacia los modelos generativos actuales permite comprender como se paso de la teoría matemática a las aplicaciones que hoy transforman la sociedad.

## El origen teórico: Alan Turing

Alan Turing sentó las bases teóricas de la computación universal en 1936. Su pregunta fundacional —"¿Pueden las máquinas pensar?"— inauguró el debate sobre la inteligencia sintética que sigue vigente hasta nuestros días.

### El Test de Turing (1950)

Turing propuso un criterio práctico para evaluar la inteligencia máquina: si un evaluador humano no puede distinguir si esta interactuando con una persona o con un ordenador, entonces la máquina supera el test. Este criterio, aunque hoy superado, establecio el primer marco de referencia para medir el progreso en el campo.

## La Conferencia de Dartmouth (1956)

En el verano de 1956, un grupo de investigadores se reunio en el Dartmouth College y acuno formalmente el termino "Inteligencia Artificial". Entre los participantes se encontraban John McCarthy, Marvin Minsky, Nathaniel Rochester y Claude Shannon, figuras que marcaría la dirección del campo durante las siguientes décadas.

## Los primeros éxitos y el primer invierno

Los anos 60 trajeron los primeros logros significativos, como el General Problem Solver, un programa capaz de resolver problemas lógicos generales. Sin embargo, entre 1966 y 1974 las limitaciones de los sistemas se hicieron evidentes: no lograban manejar la complejidad del mundo real ni escalar más allá de problemas de juguete.

> **Primer Invierno de la IA (1974-1980)**: la falta de resultados prácticos provoco un recorte masivo de financiamiento, tanto público como privado.

## El resurgimiento de los anos 80

La década de 1980 trajo un renacimiento impulsado por los sistemas expertos comerciales, programas que codificaban el conocimiento de especialistas humanos en forma de reglas lógicas. Paralelamente, el descubrimiento y popularización del algoritmo de retropropagación (backpropagation) permitio entrenar redes neuronales de multiples capas.

Sin embargo, el alto coste de mantenimiento de los sistemas expertos y la llegada de expectativas nuevamente infladas condujeron a un segundo invierno.

> **Segundo Invierno de la IA (1987-1993)**: los costes de mantenimiento superaban los beneficios, y la financiación volvio a contraerse.

## Deep Blue vence a Kasparov (1997)

En 1997, la supercomputadora Deep Blue de IBM derroto al campeon mundial de ajedrez Garry Kasparov. Deep Blue no aprendía de datos: calculaba 200 millones de posiciones por segundo mediante fuerza bruta, evaluando el árbol de juego completo. Fue un hito mediatico que demostro el poder del calculo masivo aplicado a problemas bien definidos.

## La llegada del nuevo milenio y los datos masivos

La expansión de internet y la web 2.0 generaron una acumulación masiva de datos digitales. Dos hitos marcaron el inicio de la era moderna:

- **ImageNet (2009)**: un conjunto de 14 millones de imágenes etiquetadas por humanos que se convirtio en el estándar para entrenar sistemas de visión artificial.
- **AlexNet (2012)**: una red neuronal profunda que gano el desafio ImageNet con un margen de error drásticamente inferior a los metodos tradicionales. Este momento se considera el punto de inflexion del Deep Learning.

## AlphaGo y la intuición artificial (2016)

En 2016, AlphaGo, desarrollado por DeepMind, derroto al campeon mundial de Go Lee Sedol por 4 a 1. A diferencia de Deep Blue, AlphaGo no operaba por fuerza bruta (el árbol de juego del Go es astronomicamente mayor que el del ajedrez), sino mediante **intuición estadistica**: combinaba redes neuronales profundas con aprendizaje por refuerzo para evaluar posiciones y elegir movimientos que parecian creativos incluso a ojos de expertos humanos.

## La explosión reciente: tres catalizadores

El progreso acelerado de la ultima década se explica por la confluencia de tres factores:

1. **Big Data**: la disponibilidad de enormes volúmenes de datos generados por internet, sensores y plataformas digitales.
2. **GPUs**: las unidades de procesamiento grafico, originalmente diseñadas para videojuegos, resultaron ser extraordinariamente eficientes para el calculo paralelo que requieren las redes neuronales.
3. **Avances algoritmicos**: nuevas técnicas como las redes generativas antagonicas (GANs), el aprendizaje por refuerzo profundo y, sobre todo, la arquitectura Transformer.

## Del análisis a la creación: los Transformers (2017)

En 2017, Google público el articulo "Attention is All You Need", que introducia la arquitectura Transformer. Este diseno, basado en mecanismos de atención en lugar de procesamiento secuencial, se convirtio en la base de todos los grandes modelos de lenguaje actuales, incluyendo GPT, Gemini, Claude y Llama.

## La escala como ley de rendimiento

Las denominadas **leyes de escalado (scaling laws)** establecen que a mayor escala de computo, datos y parametros, el rendimiento general del modelo (la perdida) disminuye de forma predecible; de esta escala masiva emergen **habilidades emergentes** (como el razonamiento o la traducción) que no fueron programadas de manera explicita. La evolución del tamano de los modelos ilustra esta tendencia:

- **GPT-2 (2019)**: 1.500 millones de parametros.
- **GPT-3 (2020)**: 175.000 millones de parametros.
- **Modelos actuales**: más de 1 billon de parametros.

## La comercialización masiva de la IA

Productos como ChatGPT, Copilot, Midjourney y Gemini han llevado la inteligencia artificial a millones de usuarios sin necesidad de conocimientos técnicos. La interfaz conversacional y la capacidad de generar contenido de alta calidad han convertido a la IA generativa en la tecnología de adopción más rápida de la historia.

## Cronología resumida de la IA

| Ano | Hito |
|-----|------|
| 1950 | Alan Turing pública su articulo "Computing Machinery and Intelligence" y propone el Test de Turing |
| 1956 | Conferencia de Dartmouth: se acuna el termino "Inteligencia Artificial" |
| 1997 | Deep Blue de IBM vence a Kasparov al ajedrez |
| 2012 | AlexNet gana ImageNet, marcando el inicio del Deep Learning moderno |
| 2017 | Google pública "Attention is All You Need", introduciendo los Transformers |
| 2022 | Lanzamiento de ChatGPT, llevando la IA generativa al público masivo |

## Resumen de la sección 1.2

La historia de la IA es ciclica: períodos de euforia seguidos de inviernos de financiación. El camino recorrido va de los fundamentos teóricos de Turing a los sistemas expertos de los 80, pasando por el Big Data y las GPUs como catalizadores, la revolución de los Transformers en 2017, y finalmente la explosión de la IA generativa y su comercialización masiva a partir de 2022.

---

[Anterior: 1.1 Que es la IA](01-que-es-la-ia.md) | [Volver al índice](index.md) | [Siguiente: 1.3 Tipos y principios clave](03-tipos-principios-clave.md)
