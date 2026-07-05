# Sección 2.3: Modelos Generativos Populares

Esta sección presenta una taxonomía de los principales tipos de modelos generativos: grandes modelos de lenguaje, modelos de generación de imágenes, redes generativas antagonicas y sistemas de audio y video.

## Modelos de Lenguaje Grandes (LLMs)

Los Large Language Models son sistemas entrenados sobre corpus masivos de texto, cuyo funcionamiento se basa en la predicción autoregresiva de tokens. Dado un contexto previo, el modelo predice la siguiente palabra o fragmento más probable. De este mecanismo aparentemente simple emergen capacidades complejas como el razonamiento analogico, la traducción entre idiomas y la resolución de problemas.

### La revolución de los Transformers

La arquitectura Transformer, introducida por Google en 2017, constituye la base de los LLMs modernos. Su innovación clave es el mecanismo de atención multi-cabeza, que permite al modelo procesar toda la secuencia de entrada en paralelo, en lugar de hacerlo de forma secuencial como las arquitecturas anteriores (RNN, LSTM). Esto posibilito escalar el entrenamiento a cantidades de datos sin precedentes.

### Familias de LLMs destacadas

- **GPT (OpenAI)**: la familia de modelos detras de ChatGPT, el sistema de IAG más conocido globalmente. Ha marcado la pauta en capacidades de lenguaje y razonamiento.
- **Gemini (Google DeepMind)**: modelos con integración nativa en Google Workspace, diseñados para operar de forma multimodal desde su concepción.
- **Claude (Anthropic)**: modelos que ponen enfasis en la seguridad y la alineación, destacan por su ventana de contexto larga y un nivel de alucinaciones comparativamente bajo.

### Capacidades de los LLMs

Los LLMs actuales destacan en comprensión contextual, traducción avanzada, generación de código fuente y razonamiento lógico. Su capacidad para seguir instrucciones complejas y mantener coherencia a lo largo de conversaciones extensas los convierte en herramientas versatiles para entornos profesionales.

## Modelos de generación de imágenes (Text-to-Image)

Los modelos de generación de imágenes a partir de texto reciben un prompt descriptivo, lo codifican semanticamente y producen una imagen generada. La mayoría de los sistemas actuales utilizan modelos de difusión.

### El proceso de difusión

El proceso comienza con ruido puro (una imagen aleatoria sin estructura) y, mediante un proceso iterativo de desruido guiado por el prompt textual, se obtiene la imagen final. Este proceso requiere entre 20 y 50 pasos iterativos, en los que el modelo refina progresivamente la imagen eliminando ruido y anadiendo detalle.

### Lideres en generación visual

- **DALL-E (OpenAI)**: destaca por su excelente seguimiento de instrucciones complejas en el prompt.
- **Midjourney**: reconocido por su calidad artistica superior y estetica cuidada.
- **Stable Diffusión**: modelo de código abierto que puede ejecutarse localmente, lo que garantiza privacidad y permite personalización.

## Redes Generativas Antagonicas (GANs)

Las GANs (Generative Adversarial Networks) se basan en la competencia entre dos redes neuronales. El Generador produce muestras sintéticas a partir de ruido aleatorio, mientras que el Discriminador intenta distinguir entre muestras reales y falsas. Se trata de un juego de suma cero en el que ambas redes mejoran iterativamente.

### El Generador

El generador toma ruido aleatorio como entrada y lo transforma en una muestra sintética. Recibe retroalimentación del discriminador y ajusta sus pesos para producir muestras cada vez más realistas.

### El Discriminador

El discriminador es un clasificador binario que distingue entre muestras reales (provenientes del dataset) y falsas (producidas por el generador). En la fase de inferencia, el discriminador desaparece; solo el generador se utiliza para producir contenido.

### Aplicaciones prácticas de las GANs

Las GANs se utilizan para generar rostros sintéticos en aplicaciones de marketing (como el sitio ThisPersonDoesNotExist.com) y para la optimización de imágenes medicas, mejorando la resolución y calidad de diagnosticos por imagen.

## Modelos de audio y voz

La síntesis de voz ha alcanzado un nivel de realismo notable con plataformas como ElevenLabs y PlayHT, capaces de generar locuciones que replican tono, ritmo y emoción. En el ámbito musical, herramientas como Suno, Udio y Lyria 3 permiten generar composiciones originales a partir de descripciones textuales.

## Modelos de video generativo

La generación de video constituye la frontera más reciente de la IAG. Plataformas como Sora (OpenAI, discontinuado en 2026), Kling AI, Runway Gen-3 Alpha, Luma Dream Machine y Pika permiten producir secuencias de video a partir de prompts textuales. Sus aplicaciones incluyen la producción publicitaria, la creación de storyboards, los efectos visuales y la elaboración de material formativo.

## Resumen del módulo

1. **Concepto y Aplicaciones**: la IAG sintetiza artefactos originales aprendiendo distribuciones probabilísticas.
2. **Retos y Ética**: alucinaciones, sesgos, coste computacional, impacto ambiental y regulación.
3. **Taxonomía de modelos**: LLMs, modelos de difusión, GANs, audio y video generativo.

---

[Anterior: 2.2 Retos y ética](02-retos-etica.md) | [Volver al índice](index.md)
