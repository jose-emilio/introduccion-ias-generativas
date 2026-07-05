# Lab 5: Productividad con LLMs

**Módulo:** 3 — Aplicaciones Prácticas de la IAG
**Duración estimada:** 35 min
**Tipo:** Ejercicio práctico individual
**Herramientas:** ChatGPT / Claude / Gemini (versión gratuita)

---

## Objetivos

Al completar este laboratorio, podrás:

- Usar un modelo de lenguaje para ahorrar tiempo en tareas cotidianas de oficina
- Generar resúmenes ejecutivos, extraer información clave y traducir documentos
- Evaluar la calidad de lo que genera la IA y detectar posibles errores
- Crear una plantilla de prompt reutilizable para tú trabajo

---

## ¿Qué vas a necesitar?

- Un navegador web
- Acceso a ChatGPT, Claude o Gemini (versión gratuita)
- Un documento donde anotar tus resultados
- Ganas de probar cosas nuevas. No necesitas saber programar.

---

## ¿Qué son los LLMs y cómo pueden ayudarte en tú trabajo?

Los **Modelos de Lenguaje Grandes (LLMs)** son sistemas de IA entrenados con enormes cantidades de texto (libros, artículos, páginas web). Pueden:

- **Escribir:** redactar correos, informes, artículos
- **Resumir:** condensar documentos largos en pocos párrafos
- **Traducir:** convertir texto entre idiomas manteniendo el significado
- **Extraer información:** encontrar datos específicos dentro de un texto
- **Clasificar:** organizar información en categorías

Piensa en ellos como un **asistente muy rápido** que ha leído muchísimo pero que **no siempre acierta**. Por eso, siempre debes revisar su trabajo.

---

## Actividad 1: Resumen Ejecutivo (10 min)

Imagina que recibes este informe de ventas y necesitas extraer lo más importante para presentarlo a tú jefe en 1 minuto. Copia todo el texto y pégalo en el chat de IA.

**Informe para resumir:**
```
El informe de ventas del Q4 2025 muestra un crecimiento interanual del 12% en ingresos totales, alcanzando los 4.8 millones de euros. El canal online creció un 23% mientras que tiendas físicas cayeron un 4%. El margen bruto se redujo 1.2 puntos porcentuales hasta 58.3% debido al aumento de costes logísticos. Los gastos operativos se mantuvieron estables. El EBITDA creció un 9% hasta 1.2 millones de euros. La unidad de negocio de Software como Servicio (SaaS) fue la de mejor rendimiento con un crecimiento del 34%. Por regiones, LATAM creció un 18%, Europa un 8% y Norteamérica un 5%. Se recomienda reforzar la inversión en el canal digital y revisar la estructura logística para el próximo ejercicio.
```

Ahora escribe este prompt (mensaje) en el chat:

> "Eres mi asistente ejecutivo. Necesito un resumen del informe que acabo de pegarte. El resumen debe tener exactamente 3 párrafos: el primero sobre ingresos, el segundo sobre rentabilidad y el tercero con recomendaciones. El tono debe ser formal. Dirigido al Comité de Dirección."

Lee el resumen que te dé y responde:

1. **¿Incluye los 3 temas que pediste?** (ingresos / rentabilidad / recomendaciones)
2. **¿El tono es apropiado para un informe ejecutivo?**
3. **¿Hay algún dato incorrecto o que falte?** Compáralo con el texto original.
4. **¿Usarías este resumen directamente o harías cambios? ¿Cuáles?**

→ [Ver soluciones de la Actividad 1](#soluciones)

---

## Actividad 2: Extraer Datos Clave (10 min)

Usando el mismo informe de la Actividad 1, ahora vas a pedirle a la IA que convierta la información en una tabla fácil de leer.

Escribe este prompt:

> "Del informe que te pegué antes, extrae los datos numéricos más importantes y preséntalos en una tabla con 3 columnas: 'Métrica', 'Valor' y 'Variación vs año anterior'. La tabla debe ser clara y ordenada."

Revisa la tabla que genere y responde:

1. **¿La tabla incluye todas las métricas importantes del informe?**
2. **¿El formato es claro o tendrías que ajustarlo?**
3. **¿Podrías copiar esta tabla directamente a un informe o presentación?**

→ [Ver soluciones de la Actividad 2](#soluciones)

---

## Actividad 3: Traducción Profesional (10 min)

Las empresas reciben cada vez más documentos en varios idiomas. En esta actividad vas a pedirle a la IA que traduzca manteniendo el tono formal. No se trata de traducir palabra por palabra, sino de mantener el significado y el estilo profesional.

Escribe este prompt:

> "Traduce el siguiente párrafo al inglés, al portugués y al francés. Es un texto financiero corporativo, así que debe mantener un tono formal y usar terminología profesional precisa. No traduzcas de forma literal, asegúrate de que suene natural en cada idioma.

Párrafo: 'El margen bruto se redujo 1.2 puntos porcentuales hasta 58.3% debido al aumento de costes logísticos asociados a la nueva ruta de distribución en el sudeste asiático.'"

Después de obtener las traducciones, elige una de ellas (por ejemplo, la inglesa) y pídele a la IA:

> "Ahora traduce de vuelta al español el texto en inglés que acabas de generar."

Compara la traducción de vuelta con el texto original:

1. **¿Se mantiene el significado original?**
2. **¿Hay cambios en números o conceptos?**
3. **¿Confías en que la traducción es precisa? ¿Por qué?**

→ [Ver soluciones de la Actividad 3](#soluciones)

---

## Actividad 4: Análisis de Opiniones (5 min)

Imagina que trabajas en atención al cliente y necesitas clasificar rápidamente las opiniones de los usuarios. Copia estos 5 comentarios y pégalos en el chat:

> "Clasifica cada uno de estos comentarios de clientes como POSITIVO, NEUTRAL o NEGATIVO. Preséntalo en una tabla con 3 columnas: 'Comentario', 'Clasificación' y 'Motivo breve'.

Comentarios:
1. 'El producto es excelente, llegó antes de lo esperado y supera mis expectativas.'
2. 'La atención al cliente fue pésima, estuve 40 minutos esperando sin respuesta.'
3. 'El producto está bien, aunque el empaque llegó un poco dañado.'
4. 'No volveré a comprar aquí. Pésima experiencia de compra.'
5. 'En general bien, pero el proceso de devolución es confuso y lento.'"

Revisa la clasificación. ¿Estás de acuerdo con todas? ¿Cambiarías alguna?

→ [Ver soluciones de la Actividad 4](#soluciones)

---

## Actividad 5: Crea tu Propia Plantilla de Prompt (5 min)

Esta es la actividad más práctica del laboratorio. Vas a diseñar una **plantilla de prompt** que puedas usar en tú trabajo real, una y otra vez.

Una buena plantilla debe incluir:

1. **Instrucción clara:** un verbo que indique qué debe hacer la IA (redacta, resume, analiza, traduce, etc.)
2. **Contexto:** para qué o para quién es (un informe para dirección, un correo a un cliente, etc.)
3. **Formato:** cómo quieres que presente la respuesta (tabla, párrafos, puntos clave)
4. **Restricciones:** lo que NO debe hacer (tono informal, incluir opiniones, exceder cierta longitud)

**Ejemplo de plantilla:**
> "Redacta un [correo electrónico / informe / resumen] dirigido a [audiencia]. El tono debe ser [formal / profesional / cercano]. La longitud máxima es de [X] palabras o [X] párrafos. Debe incluir: [punto 1], [punto 2], [punto 3]. No menciones [temas restringidos]. Termina con [call to action / conclusión]."

Ahora escribe tu propia plantilla adaptada a una tarea real de tú puesto de trabajo:

**Mi plantilla personal:**
> _________________________________________________________________
> _________________________________________________________________
> _________________________________________________________________
> _________________________________________________________________

**Pruébala:** ejecuta tu plantilla en el chat con un caso real y evalúa el resultado. Si no funciona bien, ajústala. El prompt perfecto rara vez sale al primer intento.

→ [Ver soluciones de la Actividad 5](#soluciones)

---

## Resumen de entregables

Al finalizar el laboratorio, tendrás:

- [ ] Resumen ejecutivo generado y evaluado (Actividad 1)
- [ ] Tabla de datos extraídos (Actividad 2)
- [ ] Traducción y verificación (Actividad 3)
- [ ] Clasificación de comentarios (Actividad 4)
- [ ] Tu plantilla de prompt personal lista para usar (Actividad 5)

Recuerda: la IA es una herramienta que acelera tu trabajo, pero tú sigues siendo responsable de revisar y validar lo que produce.

---

## Soluciones

### Actividad 1 — Resumen ejecutivo (pautas de evaluación) [↑ Volver](#actividad-1-resumen-ejecutivo-10-min)

Un buen resumen debería incluir:
- **Párrafo 1 (ingresos):** crecimiento del 12%, 4.8M€, canal online +23%, físico -4%, SaaS lidera con +34%.
- **Párrafo 2 (rentabilidad):** margen bruto -1.2pp hasta 58.3%, EBITDA +9% hasta 1.2M€, costes logísticos como causa.
- **Párrafo 3 (recomendaciones):** reforzar canal digital, revisar estructura logística.

Si falta alguno de estos puntos, el prompt se puede ajustar añadiendo más especificidad.

### Actividad 2 — Extracción de datos (tabla esperada) [↑ Volver](#actividad-2-extraer-datos-clave-10-min)

| Métrica | Valor | Variación |
|---|---|---|
| Ingresos totales | 4.8M€ | +12% |
| Canal online | — | +23% |
| Tiendas físicas | — | -4% |
| Margen bruto | 58.3% | -1.2pp |
| EBITDA | 1.2M€ | +9% |
| Crecimiento SaaS | — | +34% |
| Crecimiento LATAM | — | +18% |
| Crecimiento Europa | — | +8% |
| Crecimiento Norteamérica | — | +5% |

### Actividad 3 — Traducción [↑ Volver](#actividad-3-traducción-profesional-10-min)

Al traducir de vuelta, el texto debería mantener el significado general. Si hay cambios en números concretos (ej. "1.2 puntos porcentuales" se convierte en "1 punto porcentual"), el modelo habrá cometido un error de precisión. Esto demuestra por qué **siempre hay que verificar traducciones de datos numéricos**.

### Actividad 4 — Análisis de opiniones (clasificación esperada) [↑ Volver](#actividad-4-análisis-de-opiniones-5-min)

| Comentario | Clasificación | Motivo |
|---|---|---|
| 1. Producto excelente, llegó antes | **Positivo** | Lenguaje entusiasta, supera expectativas |
| 2. Atención pésima, 40 min esperando | **Negativo** | Experiencia claramente negativa |
| 3. Bien, pero empaque dañado | **Neutral** | Mezcla de positivo (producto bien) y negativo (empaque dañado) |
| 4. No volveré a comprar | **Negativo** | Queja clara y contundente |
| 5. Bien, pero devolución confusa | **Neutral** | Apreciación general positiva con una crítica específica |

### Actividad 5 — Plantilla personal (ejemplo) [↑ Volver](#actividad-5-crea-tu-propia-plantilla-de-prompt-5-min)

**Ejemplo para un directivo que pide informes semanales:**
> "Redacta un informe semanal de [tema] dirigido a la gerencia. El tono debe ser formal y ejecutivo. Extensión máxima: 3 párrafos. Incluye: (1) logros de la semana, (2) desafíos o riesgos detectados, (3) plan para la próxima semana. No incluyas opiniones personales ni datos no verificados. Termina con una sección de 'Indicadores clave' en formato tabla."

Una buena plantilla es la que puedes reutilizar sin apenas cambios semana tras semana.


