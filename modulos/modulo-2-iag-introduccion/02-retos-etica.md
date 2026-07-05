# Sección 2.2: Retos, Limitaciones y Ética de la IAG

La IAG plantea barreras técnicas, sesgos algoritmicos y profundas consideraciones sociales, legales y éticas que las organizaciones deben gestionar activamente.

## Desafios técnicos: las alucinaciones

Las alucinaciones son uno de los problemas más característicos de los modelos generativos. Consisten en información factualmente incorrecta que el modelo presenta con absoluta confianza. El modelo no "sabe" que esta equivocado: simplemente genera la secuencia de tokens más probable segun su distribución aprendida. El peligro radica en su fluidez y coherencia, que dificultan la detección del error.

### Mecánica de una alucinación

La alucinación es el resultado de la combinación de tres factores: confianza en la respuesta, coherencia superficial y predicción probabilística. No es un bug que pueda corregirse con un parche, sino una consecuencia inherente a la arquitectura probabilística de estos modelos.

### Riesgo corporativo de las alucinaciones

Para mitigar el riesgo corporativo, las organizaciones deben implantar protocolos de verificación obligatoria, sistemas de recuperación aumentada (RAG) que anclen las respuestas a fuentes fiables, indicadores de confianza en las salidas del modelo y una cultura organizacional de verificación sistemática.

## Control de la salida del modelo

La inconsistencia de tono y la variabilidad de formato son desafios adicionales. Para controlar la salida se emplean prompts de sistema detallados, técnicas de few-shot (ejemplos en la consulta), fine-tuning del modelo y filtros de salida (output guards).

## Sesgos algoritmicos

Los datos de entrenamiento contienen estereotipos, y el modelo los absorbe y reproduce. Internet alberga décadas de contenido producido predominantemente por determinados perfiles sociodemograficos, lo que introduce sesgos sistemáticos en los modelos.

### Origen de los sesgos en los datasets

El ingles representa en torno al 50% del contenido web disponible para entrenamiento (y más del 40% en corpus masivos como Common Crawl), lo que genera una subrepresentación historica de otras lenguas y culturas. Ademas, foros masivos como Reddit o Twitter contienen prejuicios y sesgos que quedan incorporados en los modelos.

### Estrategias de mitigación de sesgos

Las estrategias principales incluyen la curación cuidadosa del dataset de entrenamiento, el aprendizaje por retroalimentación humana (RLHF) y la implementación de filtros éticos de salida que detecten y corrijan sesgos antes de presentar la respuesta al usuario.

## Coste computacional

El entrenamiento de modelos de gran escala requiere una inversión económica considerable. Entrenar GPT-4 tuvo un coste estimado de entre 50 y 100 millones de dolares. No obstante, iniciativas como DeepSeek V3 demostraron que es posible obtener resultados competitivos con menos de 6 millones de dolares, lo que abre la puerta a una mayor eficiencia.

## Impacto energetico y ambiental

El entrenamiento de modelos históricos como GPT-3 generó unas 502 toneladas de dióxido de carbono ($CO_2e$), pero la escala actual de entrenamiento es inmensamente mayor: se estima que entrenar los modelos Llama 3.1 (8B, 70B y 405B) liberó en conjunto aproximadamente 11.390 toneladas de $CO_2e$ (más de 22 veces el impacto de GPT-3), correspondiendo 8.930 toneladas al modelo 405B. En la actualidad, los centros de datos dedicados a inteligencia artificial consumen más del 2% de la electricidad global, lo que plantea interrogantes sobre la sostenibilidad ambiental de esta tecnología.

## Cuestiones éticas y sociales

La IAG presenta riesgos significativos en el plano social: la generación de desinformación masiva, la perdida de confianza en los contenidos digitales y la polarización acelerada del debate público son consecuencias directas de la capacidad de sintetizar contenido convincente pero ficticio.

## Propiedad intelectual y autoría

Existe un vacio juridico en torno a la autoría de los contenidos generados por IAG. La pregunta sobre si el output pertenece al usuario, al desarrollador del modelo o debe considerarse de dominio público aun no tiene respuesta legal clara en la mayoría de jurisdicciones.

### Riesgo de infracción de patentes

Casos como GitHub Copilot han sido objeto de demandas por generar código que reproduce licencias restrictivas sin atribución. En el ámbito visual, Midjourney y Stable Diffusión han sido demandados por artistas que alegan reproducción no autorizada de sus estilos.

## Autenticidad de contenidos

La distinción entre contenido auténtico y sintético es progresivamente más difícil. Este problema afecta a areas críticas como la selección de personal (curriculos generados), la verificación documental, las comunicaciones corporativas y la evidencia legal.

### El peligro de los deepfakes

Los deepfakes representan una amenaza concreta. Se han documentado casos de fraude al CEO mediante suplantación de voz y video, con perdidas superiores a 25 millones de dolares. Las contramedidas incluyen detectores automáticos, protocolos de verificación en multiples canales y marcas de agua digitales en contenidos generados.

## Panorama regulatorio emergente

### La Ley de IA de la Union Europea (AI Act, 2024)

La Union Europea ha aprobado el AI Act, el marco regulatorio más comprehensivo del mundo en materia de inteligencia artificial. Esta ley clasifica los sistemas de IA por nivel de riesgo, estableciendo requisitos más estrictos para aquellos considerados de alto riesgo, como los sistemas generativos.

### Politicas internas de cumplimiento

Las organizaciones deben establecer politicas internas que incluyan: un Comite Ético de IA para la supervisión de proyectos, una Politica de Uso que defina los limites de aplicación, formación obligatoria para todos los empleados que interactuen con sistemas de IAG y un regimen de auditoría continua para verificar el cumplimiento normativo.

## Resumen

La IAG sin gobernanza es de alto riesgo. Las alucinaciones, los sesgos y el cumplimiento regulatorio requieren una gestion activa por parte de las organizaciones para aprovechar el potencial de la tecnología minimizando sus riesgos.

---

[Anterior: 2.1 Concepto y aplicaciones](01-concepto-aplicaciones.md) | [Volver al índice](index.md) | [Siguiente: 2.3 Modelos populares](03-modelos-populares.md)
