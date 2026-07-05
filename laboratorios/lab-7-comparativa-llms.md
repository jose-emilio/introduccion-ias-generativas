# Lab 7: Comparativa y Evaluación de LLMs

**Módulo:** 4 — Herramientas, Interacción y Seguridad
**Duración estimada:** 30 min
**Tipo:** Ejercicio práctico individual
**Herramientas:** ChatGPT (chat.openai.com), Gemini (gemini.google.com), Claude (claude.ai) — versiones gratuitas

---

## Objetivos

Al completar este laboratorio, podrás:

- Comparar las respuestas de diferentes modelos de lenguaje ante un mismo prompt
- Evaluar la calidad del output según criterios objetivos (precisión, formato, tono)
- Estimar costes de uso y entender las diferencias entre modelos gratuitos y comerciales
- Seleccionar el modelo más adecuado según el caso de uso

---

## ¿Qué vas a necesitar?

- Un navegador web
- Acceso a al menos **2 de estos 3** servicios gratuitos: ChatGPT, Gemini, Claude
- Un documento para anotar tus comparaciones

---

## ¿Por qué comparar modelos?

No todos los LLMs son iguales. Cada modelo tiene fortalezas y debilidades según la tarea:

- **ChatGPT (OpenAI):** líder en versatilidad y seguimiento de instrucciones complejas.
- **Gemini (Google):** integración con el ecosistema Google, buena ventana de contexto.
- **Claude (Anthropic):** excelente en matices de tono, seguridad y razonamiento.

Elegir el modelo adecuado para cada tarea puede marcar la diferencia entre un output aprovechable y uno que requiere mucha corrección.

---

## Actividad 1: El Mismo Prompt, Diferentes Modelos (10 min)

Vas a copiar y pegar el mismo prompt en **al menos 2 modelos diferentes** (si puedes, prueba los 3).

### Prompt 1 — Análisis de negocio

> "Actúa como un consultor estratégico. Analiza el impacto de la inteligencia artificial generativa en el sector retail. Presenta tu respuesta en 3 secciones: (1) oportunidades, (2) riesgos, (3) recomendaciones para implementación. Tono ejecutivo. Máximo 250 palabras."

Ejecútalo en cada modelo y copia los resultados en tú documento.

### Prompt 2 — Creatividad

> "Escribe un eslogan para una nueva línea de productos ecológicos de una empresa de limpieza del hogar. Debe ser breve, memorable y transmitir sostenibilidad. Dame 5 opciones."

Ejecútalo en cada modelo y anota los resultados.

### Tabla comparativa

Completa esta tabla después de probar cada modelo:

| Criterio | Modelo 1: \_\_\_\_\_\_\_\_ | Modelo 2: \_\_\_\_\_\_\_\_ | Modelo 3: \_\_\_\_\_\_\_\_ |
|---|---|---|---|
| **Prompt 1 — ¿Cumple las 3 secciones?** | | | |
| **Prompt 1 — Tono ejecutivo (Sí/No/Regular)** | | | |
| **Prompt 1 — ¿Las recomendaciones son concretas o genéricas?** | | | |
| **Prompt 2 — ¿Los eslóganes son originales o clichés?** | | | |
| **Prompt 2 — ¿Cuántos te gustaron realmente?** | | /5 | /5 |
| **Velocidad de respuesta** | Rápido/Normal/Lento | Rápido/Normal/Lento | Rápido/Normal/Lento |

**Pregunta para reflexionar:** Si tuvieras que elegir uno para tú trabajo diario, ¿cuál escogerías? ¿Por qué?

→ [Ver soluciones de la Actividad 1](#soluciones)

---

## Actividad 2: Evaluación de Precisión Factual (5 min)

Los modelos pueden "alucinar" información falsa. En esta actividad vas a comparar cómo manejan peticiones que requieren datos precisos.

Usa el mismo prompt en todos los modelos:

> "Dame el nombre del autor, el año de publicación y un resumen de 3 líneas del artículo académico 'Attention is All You Need'."

Evalúa:

| Aspecto | Modelo 1 | Modelo 2 | Modelo 3 |
|---|---|---|---|
| ¿Autor/es correctos? | | | |
| ¿Año correcto? | | | |
| ¿Resumen preciso? | | | |
| ¿Inventó algo? (alucinación) | | | |

**Pregunta:** ¿Algún modelo cometió errores? ¿Cuál fue el más preciso?

→ [Ver soluciones de la Actividad 2](#soluciones)

---

## Actividad 3: Estimación de Costes (5 min)

Imagina que tu empresa quiere desplegar un asistente interno y necesitas estimar costes. Usa la IA para que te ayude.

Pide a uno de los modelos:

> "Actúa como un analista de costes tecnológicos. Ayúdame a estimar el coste mensual de usar un LLM para un equipo de 50 personas que hacen 20 consultas al día cada una. Dame una comparativa entre: (A) suscripción ChatGPT Team (36€/usuario/mes), (B) API de GPT-4o-mini (0,15€/M tokens de entrada, 0,60€/M tokens de salida, estimando 2.000 tokens por consulta), y (C) modelo open source desplegado en servidor propio (coste único de GPU 30.000€ a amortizar en 36 meses + 500€/mes de electricidad/mantenimiento)."

Analiza la respuesta y completa:

1. **¿Cuál es la opción más barata a corto plazo? ¿Y a largo plazo (3 años)?**
2. **¿Qué opción ofrece más privacidad de datos?**
3. **¿Qué recomendarías para tú empresa y por qué?**

→ [Ver soluciones de la Actividad 3](#soluciones)

---

## Actividad 4: Privacidad — ¿Qué Puedo Subir a Cada Modelo? (5 min)

No todos los modelos ofrecen las mismas garantías de privacidad. En esta actividad vas a clasificar qué tipo de datos puedes procesar en cada herramienta.

Pregunta a uno de los modelos:

> "Actúa como un asesor de cumplimiento normativo (RGPD). Clasifica los siguientes tipos de datos en VERDE (se puede subir a cualquier modelo), AMARILLO (se puede subir con precaución) y ROJO (no se debe subir a modelos gratuitos): nombres completos de clientes, resumen anónimo de ventas del mes, código fuente propietario, estrategia de precios para el próximo año, preguntas frecuentes de producto ya publicadas en la web, datos bancarios de clientes, una plantilla de correo interna sin datos personales."

Revisa la clasificación y completa tu propia tabla:

| Tipo de dato | ¿Seguro para modelo gratuito? | Alternativa segura |
|---|---|---|
| Datos personales de clientes | | |
| Estrategia de negocio | | |
| Código fuente | | |
| Documentos públicos | | |

**Pregunta para reflexionar:** ¿Has subido alguna vez a un modelo gratuito algún dato que no deberías? ¿Qué harás diferente a partir de ahora?

→ [Ver soluciones de la Actividad 4](#soluciones)

---

## Actividad 5: Recomendación Final (5 min)

Basándote en todo lo que has observado en las actividades anteriores, completa esta **matriz de decisión** para tú empresa:

| Criterio | Modelo recomendado | ¿Por qué? |
|---|---|---|
| Tareas de redacción y análisis general | | |
| Tareas que requieren alta privacidad | | |
| Tareas creativas (eslóganes, brainstorming) | | |
| Tareas que requieren precisión factual | | |
| Tareas con presupuesto limitado | | |

→ [Ver soluciones de la Actividad 5](#soluciones)

---

## Resumen de entregables

Al finalizar el laboratorio, tendrás:

- [ ] Tabla comparativa de 2-3 modelos (Actividad 1)
- [ ] Evaluación de precisión factual (Actividad 2)
- [ ] Estimación de costes (Actividad 3)
- [ ] Clasificación de privacidad (Actividad 4)
- [ ] Matriz de decisión final (Actividad 5)

La próxima vez que necesites elegir un modelo de IA para una tarea, tendrás un método estructurado para hacerlo.

---

## Soluciones

### Actividad 1 — Comparativa (orientación) [↑ Volver](#actividad-1-el-mismo-prompt-diferentes-modelos-10-min)

No hay un "ganador" absoluto; depende del caso de uso. Como referencia general:

| Aspecto | ChatGPT | Gemini | Claude |
|---|---|---|---|
| Formato y estructura | Excelente | Muy bueno | Excelente |
| Tono ejecutivo | Bueno | Bueno | Muy bueno |
| Creatividad (eslóganes) | Muy buena | Buena | Muy buena |
| Velocidad | Rápido | Rápido | Medio |

**Recomendación:** prueba siempre al menos 2 modelos para tareas importantes. El mismo prompt puede dar resultados sorprendentemente distintos.

### Actividad 2 — Precisión factual [↑ Volver](#actividad-2-evaluación-de-precisión-factual-5-min)

**Respuesta correcta:** "Attention is All You Need" fue publicado por Vaswani et al. (Google) en 2017. Todos los modelos deberían acertar, pero pueden diferir en el resumen. Si algún modelo inventa autores o año, es una alucinación.

### Actividad 3 — Costes (respuesta esperada) [↑ Volver](#actividad-3-estimación-de-costes-5-min)

| Opción | Coste mensual | Privacidad |
|---|---|---|
| **ChatGPT Team** | 36€ x 50 = **1.800€/mes** | Media (datos no usados para entrenamiento) |
| **API GPT-4o-mini** | ≈ 50 x 20 x 2.000 x 0,75€ / 1M = **1,50€/día** (≈ 30€/mes para 20 días laborables) | Media |
| **Open source local** | 30.000€/36 + 500€ = **1.333€/mes** (decreciente tras amortización) | **Máxima** |

**Corto plazo:** la API de GPT-4o-mini es la más barata.

**Largo plazo (3 años):** el modelo open source se amortiza y acaba siendo más barato, además de ofrecer privacidad total.

### Actividad 4 — Privacidad (orientación) [↑ Volver](#actividad-4-privacidad--qué-puedo-subir-a-cada-modelo-5-min)

| Dato | Clasificación | Alternativa segura |
|---|---|---|
| Nombres completos de clientes | **ROJO** | Anonimizar antes de subir; usar plan Enterprise |
| Resumen anónimo de ventas | **VERDE** | Sin datos personales, es seguro |
| Código fuente propietario | **ROJO** | Usar modelo open source local o Enterprise con DPA |
| Estrategia de precios | **ROJO/AMARILLO** | No subir a gratuitos; usar Enterprise |
| FAQ ya publicadas en web | **VERDE** | Es información pública |
| Datos bancarios de clientes | **ROJO** | Nunca subir a ningún modelo externo |
| Plantilla de correo interna sin datos personales | **AMARILLO/VERDE** | Bajo riesgo si no contiene info sensible |

### Actividad 5 — Matriz de decisión (ejemplo) [↑ Volver](#actividad-5-recomendación-final-5-min)

| Criterio | Recomendación | Motivo |
|---|---|---|
| Redacción general | **Claude o ChatGPT** | Mejor tono y seguimiento de instrucciones |
| Alta privacidad | **Modelo open source local** (Llama, DeepSeek) | Los datos nunca salen del perímetro |
| Creatividad | **ChatGPT** | Mayor variedad en outputs creativos |
| Precisión factual | **Claude** (o verificar siempre con fuentes) | Menor tasa de alucinaciones reportada |
| Presupuesto limitado | **Gemini (gratis)** o **API GPT-4o-mini** | Coste cero o muy bajo para uso ligero |
