# Lab 8: Prompt Engineering

**Módulo:** 4 — Herramientas, Interacción y Seguridad
**Duración estimada:** 45 min
**Tipo:** Ejercicio práctico individual
**Herramientas:** ChatGPT / Claude / Gemini (versión gratuita)

---

## Objetivos

Al completar este laboratorio, podrás:

- Escribir prompts (instrucciones para la IA) que obtengan mejores resultados
- Aplicar 4 técnicas clave: prompt simple, ejemplos, asignación de rol y razonamiento paso a paso
- Mejorar tus prompts mediante prueba y error

---

## ¿Qué vas a necesitar?

- Un navegador web
- Acceso a ChatGPT, Claude o Gemini (versión gratuita)
- Un documento para anotar tus prompts y resultados

---

## ¿Qué es un prompt y por qué es importante mejorar cómo lo escribes?

Un **prompt** es simplemente el mensaje que le escribes a la IA. Pero no todos los prompts funcionan igual. La diferencia entre un prompt vago y uno bien escrito puede ser enorme:

| Prompt vago | Prompt bien escrito |
|---|---|
| "Háblame de ventas" | "Redacta un análisis de las tendencias de ventas del sector retail en Latinoamérica durante 2025. Preséntalo en 5 puntos clave con datos concretos. Tono profesional." |

Con un buen prompt, la IA entiende **qué** quieres, **cómo** lo quieres y **para qué** lo necesitas. Esto ahorra tiempo y evita tener que pedir correcciones.

---

## Actividad 1: Sin Ejemplos vs. Con Ejemplos (10 min)

### Parte A — Prompt sin ejemplos (Zero-shot)

El término "zero-shot" significa "sin ejemplos". Le pides a la IA que haga algo directamente, confiando en su conocimiento general.

Escribe este prompt en el chat:

> "Clasifica la urgencia de estas 4 incidencias de sistemas como BAJA, MEDIA, ALTA o CRÍTICA:
>
> 1. El servidor de producción no responde
> 2. La impresora del tercer piso no funciona
> 3. Se ha detectado un acceso no autorizado a la base de datos de clientes
> 4. El botón de 'Guardar' en la página web está desalineado 2 píxeles a la derecha"

Observa el resultado. ¿Las clasificaciones te parecen correctas? ¿El formato es claro?

### Parte B — Prompt con ejemplos (Few-shot)

"Few-shot" significa "con algunos ejemplos". Le muestras a la IA cómo quieres que clasifique, dándole casos resueltos.

Ahora escribe este prompt:

> "Voy a darte ejemplos de cómo quiero que clasifiques incidencias. Después, clasifica tú las siguientes.
>
> Ejemplos:
> - 'Caída total del sitio web' → CRÍTICA
> - 'No puedo acceder a mi correo electrónico' → MEDIA
> - 'La fuente del menú no es la correcta' → BAJA
>
> Ahora clasifica estas:
> 1. El servidor de producción no responde
> 2. La impresora del tercer piso no funciona
> 3. Se ha detectado un acceso no autorizado a la base de datos de clientes
> 4. El botón de 'Guardar' en la página web está desalineado 2 píxeles a la derecha"

Compara los dos resultados:

1. **¿Cambió la clasificación de alguna incidencia entre un prompt y otro?**
2. **¿El formato de salida fue más ordenado con ejemplos?**
3. **¿Cuál de los dos resultados usarías directamente en tú trabajo?**

→ [Ver soluciones de la Actividad 1](#soluciones)

---

## Actividad 2: Asignar un Rol a la IA (10 min)

Una técnica muy potente es pedirle a la IA que "actúe como" un profesional específico. Esto hace que ajuste su vocabulario, su tono y su forma de pensar.

Vas a probar 3 versiones del mismo ejercicio. Pega cada prompt por separado y compara los resultados.

### Versión 1 — Sin rol (prompt normal)
> "Explica los beneficios de implementar IA generativa en una empresa de logística."

### Versión 2 — Con rol
> "Actúa como un consultor senior en transformación digital especializado en logística y cadena de suministro. Explica los beneficios de implementar IA generativa en una empresa de logística. Usa vocabulario técnico del sector. Tu audiencia es el Comité de Dirección."

### Versión 3 — Con rol y restricciones
> "Actúa como un auditor de riesgos tecnológicos. Explica los beneficios de implementar IA generativa en logística, pero también incluye los riesgos y cómo mitigarlos. Presenta la respuesta en formato de tabla con 3 columnas: Beneficio | Riesgo asociado | Cómo mitigarlo."

Responde:

1. **¿Cómo cambió el tono entre la Versión 1 y la Versión 2?** ¿Cuál suena más profesional?
2. **¿La Versión 3 fue más útil para la toma de decisiones** al incluir también los riesgos?
3. **¿Qué versión presentarías a tú jefe?** ¿Por qué?

→ [Ver soluciones de la Actividad 2](#soluciones)

---

## Actividad 3: Razonamiento Paso a Paso (10 min)

A veces la IA se salta pasos y llega a una respuesta incorrecta. La técnica **Cadena de Pensamiento (Chain-of-Thought o CoT)** le pide que "muestre su trabajo", paso a paso, antes de dar la respuesta final.

### Prompt sin CoT
Escribe:

> "Una empresa tiene 240 empleados. El 60% son mujeres. De las mujeres, el 25% trabaja en el departamento de TI. Del total de personas en TI, el 40% son hombres. ¿Cuántos hombres trabajan en TI?"

Anota la respuesta. ¿Incluye el procedimiento o solo el número final?

### Prompt con CoT
Ahora escribe el mismo problema pero añadiendo la instrucción de razonar paso a paso:

> "Una empresa tiene 240 empleados. El 60% son mujeres. De las mujeres, el 25% trabaja en el departamento de TI. Del total de personas en TI, el 40% son hombres. ¿Cuántos hombres trabajan en TI?
>
> Razona paso a paso antes de dar tu respuesta final. Explica cada cálculo."

Compara:

1. **¿Las dos respuestas numéricas coinciden?**
2. **¿La versión con CoT te da más confianza en el resultado?**
3. **¿Para qué tipos de tareas crees que esta técnica es más útil?** (Por ejemplo: análisis financiero, planificación, decisiones con varias variables)

→ [Ver soluciones de la Actividad 3](#soluciones)

---

## Actividad 3B: El Poder de los Delimitadores (5 min)

Los **delimitadores** son caracteres especiales que separan la instrucción del contenido a procesar, eliminando ambigüedades. En esta actividad vas a comprobar la diferencia.

### Prompt sin delimitadores

Pega esto exactamente:

> "Resume este texto con un tono formal. El texto es:
> El informe de ventas del Q4 muestra un crecimiento del 12%. El canal online creció un 23%.
> No uses jerga técnica."

Fíjate: ¿el modelo confunde dónde termina la instrucción y dónde empieza el texto a resumir?

### Prompt con delimitadores

Ahora usa triple comilla para separar:

> "Resume el siguiente texto con tono formal. No uses jerga técnica.
>
> """
> El informe de ventas del Q4 muestra un crecimiento del 12%. El canal online creció un 23%.
> """

### Compara

1. **¿El resultado fue más preciso con delimitadores?**
2. **¿Notas alguna diferencia en cómo el modelo interpreta cada prompt?**
3. **¿En qué situaciones usarías delimitadores en tú trabajo?**

→ [Ver soluciones de la Actividad 3B](#soluciones)

---

## Actividad 4: Mejorar un Prompt por Iteraciones (10 min)

Un prompt perfecto casi nunca se consigue a la primera. La clave es **iterar**: probar, ver qué falta, ajustar y volver a probar.

Vas a partir de este prompt muy vago y mejorarlo en 3 pasos:

**Prompt original (muy vago):**
> "Escribe algo sobre inteligencia artificial para la empresa."

### Paso 1: Añade audiencia y propósito

¿Para quién es? ¿Para qué lo necesita? Reescribe el prompt:

> _________________________________________________________________
> _________________________________________________________________

Ejecútalo y observa el resultado.

### Paso 2: Añade formato y tono

¿Cómo quieres que presente la información? ¿Formal o cercano? ¿En párrafos, lista, tabla?

Mejora tu prompt anterior añadiendo formato y tono:

> _________________________________________________________________
> _________________________________________________________________

Ejecútalo de nuevo.

### Paso 3: Añade restricciones y estructura de salida

¿Qué NO debe incluir? ¿Cuánto debe medir? ¿Qué secciones debe tener?

Mejora una vez más:

> _________________________________________________________________
> _________________________________________________________________

Ejecuta la versión final. Compara con la primera respuesta que obtuviste. ¿Cuánto mejoró?

**Anota aquí la evolución:**
- Versión 1 (sin cambios): _________________________________________
- Versión 2 (con audiencia): _______________________________________
- Versión 3 (con formato): ________________________________________
- Versión 4 (completo): __________________________________________

→ [Ver soluciones de la Actividad 4](#soluciones)

---

## Actividad 5: Crea tu Prompt de Trabajo (5 min)

Ahora vas a aplicar todo lo aprendido. Diseña un prompt optimizado para una tarea real de tú día a día laboral.

Usa esta lista de verificación para asegurarte de que está completo:

- [ ] **Instrucción clara** (¿qué verbo describe la acción? ej: "redacta", "analiza", "compara")
- [ ] **Contexto** (¿para quién es? ¿para qué se va a usar?)
- [ ] **Rol asignado** (¿qué profesional debe "actuar" la IA?)
- [ ] **Formato deseado** (¿tabla, párrafos, puntos clave, correo?)
- [ ] **Restricciones** (¿extensión máxima, tono, temas a evitar?)
- [ ] **Ejemplo** (opcional, pero ayuda mucho)

**Mi prompt profesional:**
> _________________________________________________________________
> _________________________________________________________________
> _________________________________________________________________
> _________________________________________________________________

**Pruébalo ahora mismo en el chat.** Si el resultado no es lo que esperabas, ajústalo y vuelve a probar. El objetivo es que tengas un prompt que puedas reutilizar.

→ [Ver soluciones de la Actividad 5](#soluciones)

---

## Resumen de entregables

Al finalizar el laboratorio, tendrás:

- [ ] Comparación zero-shot vs few-shot (Actividad 1)
- [ ] Comparación de las 3 versiones con/sin rol (Actividad 2)
- [ ] Resultado del problema con y sin CoT (Actividad 3)
- [ ] Comparación con y sin delimitadores (Actividad 3B)
- [ ] Evolución del prompt en 4 versiones (Actividad 4)
- [ ] Tu prompt personal listo para usar (Actividad 5)

La habilidad más importante que has practicado hoy es **escribir instrucciones claras**. Esa habilidad te servirá con cualquier herramienta de IA, ahora y en el futuro.

---

## Soluciones

### Actividad 1 — Zero-shot vs Few-shot [↑ Volver](#actividad-1-sin-ejemplos-vs-con-ejemplos-10-min)

**Sin ejemplos (zero-shot):** el modelo puede clasificar correctamente las incidencias más obvias (servidor no responde → CRÍTICA), pero puede ser inconsistente con las intermedias (impresora → MEDIA o BAJA según el criterio del modelo). El formato de salida puede variar.

**Con ejemplos (few-shot):** la clasificación debería ser más consistente porque el modelo sigue el patrón que le diste. El formato de salida suele ser más ordenado y predecible.

**Diferencia esperada:** el few-shot clustering suele dar resultados más alineados con lo que espera el usuario, especialmente en tareas donde el criterio de clasificación es subjetivo.

### Actividad 2 — Rol [↑ Volver](#actividad-2-asignar-un-rol-a-la-ia-10-min)

| Versión | Característica esperada |
|---|---|
| **Sin rol** | Respuesta genérica, lenguaje estándar, beneficios a nivel general. Útil como punto de partida. |
| **Con rol (consultor logística)** | Vocabulario técnico del sector (cadena de suministro, picking, última milla), ejemplos concretos del rubro. |
| **Con rol + restricciones (auditor)** | Respuesta más equilibrada (incluye riesgos), formato estructurado en tabla. Más útil para toma de decisiones. |

### Actividad 3B — Delimitadores [↑ Volver](#actividad-3b-el-poder-de-los-delimitadores-5-min)

**Sin delimitadores:** el modelo puede confundir la instrucción "No uses jerga técnica" como parte del texto a resumir, o mezclar las instrucciones con el contenido. La respuesta puede incluir jerga o tener un formato inconsistente.

**Con delimitadores (`"""`):** el modelo distingue claramente entre la instrucción y el texto a procesar. La respuesta respeta mejor el tono solicitado y no mezcla contenido.

**Conclusión:** usa delimitadores siempre que tu prompt incluya texto de ejemplo, documentos a procesar o bloques largos de contenido. Es una práctica simple que mejora drásticamente la precisión.

### Actividad 3 — Cadena de Pensamiento [↑ Volver](#actividad-3-razonamiento-paso-a-paso-10-min)

**Cálculo paso a paso (solución):**

1. Total empleados = 240
2. Mujeres = 60% de 240 = 144
3. Mujeres en TI = 25% de 144 = 36
4. Total TI: sabemos que el 40% de TI son hombres → el 60% de TI son mujeres → 36 = 60% de TI → TI total = 36 / 0.60 = 60
5. Hombres en TI = 40% de 60 = **24**

Sin CoT, el modelo puede dar el resultado correcto o no, pero **no muestra el proceso**, lo que dificulta detectar errores. Con CoT, cada paso es visible y verificable.

### Actividad 4 — Iteración (ejemplo de evolución) [↑ Volver](#actividad-4-mejorar-un-prompt-por-iteraciones-10-min)

| Iteración | Prompt | Resultado esperado |
|---|---|---|
| **1 — Original** | "Escribe algo sobre inteligencia artificial para la empresa." | Respuesta larga, genérica, sin estructura clara. |
| **2 — + Audiencia** | "Escribe un documento sobre IA para presentar al Comité de Dirección de mi empresa." | Más enfocado, pero aún sin formato definido. |
| **3 — + Formato** | "Redacta un documento de 3 secciones (qué es IA, beneficios para nuestra empresa, próximos pasos) para el Comité de Dirección. Tono formal." | Estructura clara, contenido alineado al propósito. |
| **4 — + Restricciones** | "Redacta un documento de 3 secciones (qué es IA, beneficios, próximos pasos) para el Comité de Dirección. Tono formal. Máximo 2 páginas. No incluyas jerga técnica. Termina con 3 recomendaciones concretas." | Resultado directamente utilizable en una reunión ejecutiva. |

### Actividad 5 — Prompt profesional (ejemplo) [↑ Volver](#actividad-5-crea-tu-prompt-de-trabajo-5-min)

**Ejemplo para un responsable de marketing:**
> "Actúa como un copywriter senior especializado en LinkedIn. Redacta 3 publicaciones para LinkedIn dirigidas a directores de RRHH de empresas de más de 200 empleados. Cada publicación debe tener un título llamativo, máximo 150 palabras, tono profesional pero cercano, y terminar con una pregunta que invite a comentar. El tema es: los beneficios de la IA generativa en la atracción de talento. No uses clichés como 'revolucionario' o 'cambio de paradigma'."
