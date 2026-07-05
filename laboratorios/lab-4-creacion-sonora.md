# Lab 4: Creación Sonora con IAG

**Módulo:** 3 — Aplicaciones Prácticas de la IAG
**Duración estimada:** 35 min
**Tipo:** Ejercicio práctico individual
**Herramientas:** ElevenLabs (elevenlabs.io, plan gratuito: 10.000 caracteres/mes), Suno (suno.ai, plan gratuito: 50 créditos/día ≈ 10 canciones), Gemini / ChatGPT

---

## Objetivos

Al completar este laboratorio, podrás:

- Generar locuciones sintéticas realistas a partir de texto
- Crear música original mediante descripciones textuales
- Identificar deepfakes de audio y sus riesgos
- Evaluar la calidad y usabilidad del audio generado por IA

---

## ¿Qué vas a necesitar?

- Un navegador web
- Cuenta gratuita en **ElevenLabs** (elevenlabs.io, 10.000 caracteres/mes) — solo necesitas email
- Cuenta gratuita en **Suno** (suno.ai, 50 créditos/día ≈ 10 canciones) — puedes usar login con Google
- Acceso a ChatGPT, Claude o Gemini para las actividades de texto
- Auriculares o altavoces

---

## ¿Cómo funciona la generación de audio por IA?

Los sistemas de audio generativo se basan en dos grandes tecnologias:

- **Text-to-Speech (TTS):** convierten texto escrito en voz sintética. Los modelos actuales (como ElevenLabs) pueden replicar tono, ritmo y emoción a partir de segundos de muestra.
- **Música generativa:** modelos como Suno transforman descripciones textuales en composiciones musicales completas con letra, estilo y género.

Ambos tipos de modelo aprenden patrones de miles de horas de audio real para generar contenido original.

---

## Actividad 1: Texto a Voz (TTS) — 10 min

Vas a generar una locución profesional para un video corporativo usando ElevenLabs.

1. Abre [elevenlabs.io](https://elevenlabs.io) y créate una cuenta gratuita (si no la tienes).
2. Ve a la sección **De texto a voz**.
3. Copia y pega este texto:

> "Bienvenidos al informe anual de resultados. Este año hemos alcanzado un crecimiento del 23% en ingresos totales, impulsado por la expansión internacional y la transformación digital de nuestros procesos."

4. Selecciona un tipo de voz soportada por el plan gratuito.
5. Ajusta la **estabilidad** al 70% y la **similitud** al 80%.
6. Pulsa **Generar discurso** y escucha el resultado.

### Ahora personaliza:

Cambia el texto por uno propio relacionado con tú sector profesional (máximo 3 frases). Genera la locución y responde:

1. **¿La voz suena natural o robótica?** ¿En qué te fijaste para evaluarlo?
2. **¿Usarías esta herramienta para un video corporativo real?** ¿Por qué?
3. **¿Qué limitaciones observaste** (entonación, pausas, pronunciación)?

→ [Ver soluciones de la Actividad 1](#soluciones)

---

## Actividad 2: Generación Musical con IA — 10 min

Ahora vas a crear una pieza musical original con Suno.

1. Abre [suno.ai](https://suno.ai) e inicia sesión (Google o email).
2. Ve a la sección **Create**.
3. En **Style of Music**, escribe: `corporate ambient, electronic, instrumental, professional`
4. En **Lyrics**, activa el modo **Instrumental** (sin letra).
5. En el prompt de descripción, escribe:

> "Ambient corporate music for a business presentation. Calm, modern, professional. Piano and soft synthesizers. Moderate tempo."

6. Pulsa **Generate** y espera unos segundos.
7. Escucha el resultado.

### Variación:

Ahora prueba con otro estilo para un contexto distinto:

> "Upbeat motivational music for a product launch event. Energetic, modern, inspiring. Drums and electric guitar. Fast tempo."

Responde:

1. **¿Las dos piezas transmiten emociones diferentes?** Descríbelas.
2. **¿Cuál usarías para una presentación de resultados y cuál para un evento de lanzamiento?**
3. **¿Puedes identificar limitaciones?** (repeticiones, calidad de instrumentos, duración)

→ [Ver soluciones de la Actividad 2](#soluciones)

---

## Actividad 3: Detecta el Deepfake de Audio — 10 min

Los deepfakes de audio son una amenaza real. En esta actividad vas a aprender a identificar señales de alerta.

Usa la IA conversacional (ChatGPT, Claude o Gemini) para que te genere una lista de señales de detección:

> "Actúa como un experto en ciberseguridad especializado en deepfakes. Dame una lista de 5 señales que ayuden a detectar si un audio ha sido generado por IA. Incluye aspectos técnicos y de comportamiento. Preséntalo en una tabla con 3 columnas: Señal | Cómo detectarla | Ejemplo concreto."

Revisa la respuesta y después completa este ejercicio práctico:

### Escenario de análisis

Imagina que recibes este mensaje de voz en Slack de tú CEO (según el texto):

> "Hola equipo, necesito que hagáis una transferencia urgente de 8.500€ a la cuenta que os acabo de enviar por email. Es para el proveedor nuevo del proyecto de expansión. Gracias."

Responde:

1. **¿Qué elementos de este mensaje deberían hacerte sospechar?**
2. **¿Qué protocolo seguirías para verificar la autenticidad antes de actuar?**
3. **¿Qué consecuencias podría tener si el audio es un deepfake?**

→ [Ver soluciones de la Actividad 3](#soluciones)

---

## Actividad 4: Tu Propio Podcast en 5 Min — 5 min

Vas a simular el flujo de producción de un podcast corporativo usando múltiples herramientas de IA.

### Paso 1: Genera el guion

Pide a ChatGPT/Claude/Gemini:

> "Eres un guionista de podcasts corporativos. Escribe un guion de 60 segundos para un podcast interno sobre los beneficios de la IA generativa en la empresa. Debe tener: introducción (10s), desarrollo (40s) y cierre (10s). Tono profesional pero cercano."

### Paso 2: Convierte a voz (opcional si ya usaste ElevenLabs antes)

Si te queda tiempo, copia el guion generado a ElevenLabs y genera la locución.

### Paso 3: Reflexiona

1. **¿En qué departamentos de tú empresa tendría más impacto un podcast interno automatizado?**
2. **¿Qué ahorro de tiempo estimas frente a grabar un podcast con personas reales?**

→ [Ver soluciones de la Actividad 4](#soluciones)

---

## Resumen de entregables

Al finalizar el laboratorio, tendrás:

- [ ] Locución generada en ElevenLabs y evaluación (Actividad 1)
- [ ] Dos piezas musicales generadas en Suno (Actividad 2)
- [ ] Tabla de detección de deepfakes y análisis de escenario (Actividad 3)
- [ ] Guion de podcast y reflexión (Actividad 4)

No necesitas ser músico ni técnico de audio. Este laboratorio está diseñado para cualquier profesional que quiera entender el potencial del audio generativo.

---

## Soluciones

### Actividad 1 — TTS (orientación) [↑ Volver](#actividad-1-texto-a-voz-tts--10-min)

Esperable que la voz suene natural en frases cortas, pero con pequeñas imperfecciones en entonación o pausas en frases largas. ElevenLabs es de los mejores TTS del mercado, pero:

- **Pausas:** a veces no respeta la puntuación compleja.
- **Énfasis:** no siempre acentúa la palabra correcta.
- **Pronunciación:** puede fallar en siglas o términos técnicos.

Para uso corporativo real, se recomienda ajustar la estabilidad y claridad, y hacer varias pruebas con el mismo texto.

### Actividad 2 — Música (orientación) [↑ Volver](#actividad-2-generación-musical-con-ia--10-min)

La primera pieza (ambient corporate) debería sonar serena y profesional, ideal para presentaciones de resultados o vídeos institucionales. La segunda (upbeat motivational) debería tener más energía, adecuada para lanzamientos o eventos.

**Limitaciones típicas:** la duración máxima gratuita suele ser corta (30-60s). Puede haber repeticiones de patrones. Los instrumentos suenan bien pero no igualan una producción profesional.

### Actividad 3 — Deepfake de audio (orientación) [↑ Volver](#actividad-3-detecta-el-deepfake-de-audio--10-min)

**Señales de alerta esperadas:**
| Señal | Cómo detectarla | Ejemplo |
|---|---|---|
| Falta de variación emocional | El tono es plano, sin altibajos | Todas las frases suenan igual |
| Sonido "metálico" o "de laboratorio" | Calidad de audio demasiado perfecta | Sin ruido ambiente, sin respiración |
| Pausas en lugares incorrectos | Silencios en medio de palabras | "Trans-ferencia" en vez de "transferencia" |
| Sin marcas de respiración | No hay sonidos de inhalación | Suena a habla continua sin pausas naturales |
| Velocidad constante | Ni acelera ni desacelera | No hay énfasis en palabras clave |

**Protocolo ante duda:** contactar a la persona por otro canal (teléfono directo, presencialmente o email conocido), establecer contraseñas verbales internas, y nunca actuar solo con instrucciones de voz sin verificación cruzada.

### Actividad 4 — Podcast (ejemplo) [↑ Volver](#actividad-4-tu-propio-podcast-en-5-min--5-min)

Un podcast corporativo automatizado tiene aplicaciones en: comunicación interna (newsletter semanal hablado), formación (cápsulas de aprendizaje), RRHH (bienvenida a nuevos empleados) y ventas (píldoras de producto).

Ahorro estimado frente a grabación tradicional: 80-90% del tiempo, eliminando la necesidad de estudio, micrófonos profesionales, edición manual y actores de voz.
