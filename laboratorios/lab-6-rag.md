# Lab 6: RAG — Conectando LLMs con tu Conocimiento Interno

**Módulo:** 3 — Aplicaciones Prácticas de la IAG
**Duración estimada:** 40 min
**Tipo:** Ejercicio práctico individual
**Herramientas:** ChatGPT / Claude / Gemini (versión gratuita)

---

## Objetivos

Al completar este laboratorio, podrás:

- Explicar qué es RAG y por qué es importante para las empresas
- Diferenciar entre una respuesta basada en el conocimiento general del modelo y una basada en documentación interna
- Identificar cuándo conviene usar RAG y cuándo otras alternativas como fine-tuning
- Reconocer los desafíos prácticos de implementar RAG en una organización
- Diseñar un sistema RAG básico para un caso empresarial real

---

## ¿Qué vas a necesitar?

- Un navegador web
- Acceso a ChatGPT, Claude o Gemini (versión gratuita)
- Un documento donde anotar tus resultados
- No necesitas saber programar

---

## ¿Qué es RAG?

**RAG (Retrieval-Augmented Generation)** es un patrón arquitectónico que conecta un modelo de lenguaje (LLM) con documentos internos de la organización.

Imagina que le preguntas a un empleado nuevo de tu empresa: «¿Cuál es la política de vacaciones?». Sin acceso a las políticas internas, te dará una respuesta genérica basada en lo que sabe de otras empresas. Pero si le das el manual del empleado, podrá responder con precisión citando el documento. RAG hace exactamente eso con los LLMs.

El proceso sigue cuatro pasos:

1. **Pregunta**: el usuario formula una consulta en lenguaje natural («¿Cuántos días de vacaciones tengo?»)
2. **Búsqueda**: el sistema recupera los fragmentos de documentos más relevantes
3. **Consolidación**: el LLM sintetiza una respuesta a partir de los fragmentos recuperados
4. **Respuesta segura**: el resultado se entrega con referencias a las fuentes originales

---

## Actividad 1: Sin Contexto vs Con Contexto (10 min)

Esta es la demostración más importante de RAG. Vas a hacer la misma pregunta dos veces: primero sin contexto y luego con contexto.

### Parte A: Sin contexto

Escribe este prompt directamente en el chat:

> "¿Cuál es el procedimiento de aprobación de gastos para compras superiores a 5.000€?"

Anota la respuesta. Pregúntate:
- ¿El modelo te da una respuesta genérica o cita una política concreta?
- ¿Menciona alguna empresa o normativa real?
- ¿La respuesta te serviría en tu trabajo?

### Parte B: Con contexto (RAG simulado)

Ahora copia y pega esta política ficticia seguida de la misma pregunta:

> "A continuación tienes la política interna de la empresa. Responde SOLO basándote en esa política. Si la información no está en el texto, di que no lo sabes.
>
> ## POLÍTICA DE APROBACIÓN DE GASTOS — CORPORACIÓN NEXUS
> **Vigente desde:** 1 de marzo de 2025
>
> **Niveles de aprobación:**
> - Gastos hasta 500€: aprobación automática del responsable de equipo
> - Gastos entre 500€ y 5.000€: aprobación del jefe de departamento
> - Gastos entre 5.001€ y 25.000€: aprobación de dirección financiera
> - Gastos superiores a 25.000€: aprobación del comité de dirección
>
> **Requisitos:**
> - Toda solicitud debe incluir: justificación del gasto, presupuesto del proveedor y centro de coste
> - Las facturas deben presentarse en un plazo máximo de 30 días desde la fecha del gasto
> - Los gastos no aprobados previamente serán rechazados en la liquidación
>
> **Pregunta: ¿Cuál es el procedimiento de aprobación de gastos para compras superiores a 5.000€ en Corporación Nexus?"**

### Parte C: Analiza la diferencia

1. **¿Las respuestas fueron diferentes? ¿En qué aspectos?**
2. **¿La respuesta con contexto fue más precisa y útil?**
3. **¿La respuesta con contexto citó la fuente (la política)? Si no lo hizo, ¿por qué crees que ocurrió?**
4. **Si fueras un empleado de Corporación Nexus, ¿qué respuesta te inspiraría más confianza?**

→ [Ver soluciones de la Actividad 1](#soluciones)

---

## Actividad 2: RAG con Documentos Grandes — El Desafío del Chunking (10 min)

En la vida real, los documentos son mucho más largos que el párrafo anterior. Un manual de empleado, un contrato o un informe pueden tener 50 o 100 páginas. Los LLMs tienen un límite de contexto (ventana de tokens), por lo que no se puede meter todo el documento en cada consulta.

Aquí es donde entra el **chunking**: dividir los documentos largos en fragmentos más pequeños (chunks) para que el sistema pueda buscar en ellos de forma eficiente.

### Parte A: Documento largo sin chunking

Pega este texto completo y haz la pregunta al final:

> "A continuación tienes las politicas de la empresa Corporación Nexus. Responde SOLO basándote en este texto.
>
> ## POLÍTICAS INTERNAS — CORPORACIÓN NEXUS
>
> ### 1. Política de vacaciones
> Los empleados tienen derecho a 22 días laborables de vacaciones anuales. Deben solicitarse con 15 días de antelación mínima. Los periodos de más de 10 días seguidos requieren aprobación del mando directo.
>
> ### 2. Política de teletrabajo
> Se permite teletrabajar hasta 3 días por semana. Los viernes son obligatorios en oficina para reuniones de equipo. Es necesario contar con conexión a internet de al menos 50 Mbps y un espacio de trabajo adecuado.
>
> ### 3. Política de formación
> Cada empleado dispone de un presupuesto anual de 2.000€ para formación. Los cursos deben estar relacionados con el puesto de trabajo actual o futuro. La formación debe completarse dentro del año natural. Los certificados obtenidos deben registrarse en el portal del empleado.
>
> ### 4. Política de gastos de viaje
> Los gastos de alojamiento están cubiertos hasta 150€/noche. La dieta diaria para comidas es de 40€. Los desplazamientos en transporte público se reembolsan al 100%. El uso de vehículo particular se compensa a 0,25€/km.
>
> ### 5. Política de bajas y permisos
> Los permisos retribuidos incluyen: mudanza (1 día), matrimonio (15 días), nacimiento de hijos (16 semanas), fallecimiento de familiar directo (3 días), y enfermedad grave de familiar (5 días).
>
> ### 6. Política de seguridad informática
> Las contraseñas deben cambiarse cada 90 días. Está prohibido compartir credenciales. El software no autorizado no puede instalarse en equipos corporativos. Cualquier incidente de seguridad debe notificarse en menos de 2 horas al departamento de IT.
>
> **Pregunta: ¿Cuál es el presupuesto anual de formación y qué requisitos tiene?**"

Anota la respuesta y verifica: ¿el modelo encontró correctamente la información? ¿Incluyó todos los detalles?

### Parte B: Chunking manual

Ahora imagina que los documentos están divididos en fragmentos. En lugar de darle todo el texto, le entregas solo los fragmentos relevantes para la pregunta. Copia esto:

> "Responde basándote SOLO en la siguiente información extraída de las políticas internas:
>
> 'Cada empleado dispone de un presupuesto anual de 2.000€ para formación. Los cursos deben estar relacionados con el puesto de trabajo actual o futuro. La formación debe completarse dentro del año natural. Los certificados obtenidos deben registrarse en el portal del empleado.'
>
> **Pregunta: ¿Cuál es el presupuesto anual de formación y qué requisitos tiene?**"

### Parte C: Compara

1. **¿Hubo diferencia en la calidad de las respuestas entre la Parte A y la Parte B?**
2. **En la Parte A, ¿el modelo respondió correctamente o mezcló información de otras políticas?**
3. **¿Qué ventajas tiene darle al modelo solo los fragmentos relevantes en lugar del documento completo?**
4. **¿Qué podría salir mal si el chunking está mal hecho?** (ej: un fragmento importante se parte en dos)

→ [Ver soluciones de la Actividad 2](#soluciones)

---

## Actividad 3: RAG con Fuentes en Conflicto (10 min)

Uno de los mayores desafíos de RAG es que los documentos internos pueden contener información contradictoria. Por ejemplo, una política actualizada y una versión anterior, o dos departamentos con criterios diferentes.

En esta actividad vas a ver cómo responde el modelo ante fuentes contradictorias.

Pega este texto:

> "Tienes dos fuentes internas de la empresa Corporación Nexus. Responde a la pregunta basándote en AMBAS fuentes. Si hay contradicciones, señálalas explícitamente.
>
> **Fuente A — Portal de RRHH (actualizado en marzo de 2025):**
> 'Los empleados pueden solicitar hasta 3 días de teletrabajo por semana. Es necesario contar con conexión de al menos 50 Mbps. Los viernes son obligatorios en oficina para las reuniones semanales de equipo.'
>
> **Fuente B — Comunicado interno de dirección (junio de 2025):**
> 'A partir del 1 de julio de 2025, se amplía el teletrabajo a 4 días por semana. Los viernes pasan a ser optativos. Se elimina el requisito de velocidad mínima de conexión.'
>
> **Pregunta: ¿Cuántos días de teletrabajo tengo permitidos actualmente? ¿Hay alguna contradicción entre las fuentes?"**

Después de la respuesta, pídele al modelo que genere una tercera versión unificada:

> "Ahora, actuando como responsable de RRHH, redacta una comunicación breve que resuelva la contradicción entre ambas fuentes y establezca claramente cuál es la política vigente."

Anota tus observaciones:
1. **¿El modelo identificó correctamente la contradicción entre las fuentes?**
2. **La respuesta unificada, ¿fue clara y útil?**
3. **En una empresa real, ¿cómo evitarías este problema de versiones contradictorias en los documentos fuente?**

→ [Ver soluciones de la Actividad 3](#soluciones)

---

## Actividad 4: RAG vs Fine-tuning — ¿Cuándo usar cada uno? (5 min)

Lee esta situación y completa la tabla:

**Situación:** Una empresa quiere que su asistente de IA conozca sus políticas internas (vacaciones, gastos, permisos) y poder actualizarlas cada 3 meses. También quiere que el asistente tenga el tono de comunicación característico de la empresa: cercano pero formal, con un vocabulario específico del sector.

Completa la tabla indicando si RAG o Fine-tuning es más adecuado para cada objetivo:

| Objetivo | ¿RAG? | ¿Fine-tuning? | ¿Por qué? |
|----------|-------|---------------|-----------|
| Responder sobre politicas de vacaciones | | | |
| Mantener el tono corporativo | | | |
| Actualizar respuestas cada 3 meses | | | |
| Garantizar que las respuestas citen la fuente exacta | | | |
| Ensenar al modelo vocabulario técnico del sector | | | |

→ [Ver soluciones de la Actividad 4](#soluciones)

---

## Actividad 5: Diseña un Sistema RAG para tu Empresa (5 min)

Esta es la actividad más práctica. Vas a diseñar un sistema RAG para un caso real de tu organización o de una empresa que conozcas.

Elige un caso concreto (ej: atención al cliente, consultas de RRHH, asistencia técnica, documentación de productos) y completa esta ficha:

```
**Nombre del proyecto:**
_________________________________________________

**Área o departamento:**
_________________________________________________

**Tipo de documentos que contendría la base de conocimiento:**
_________________________________________________
_________________________________________________

**Tres preguntas típicas que harían los usuarios:**
1. _________________________________________________
2. _________________________________________________
3. _________________________________________________

**¿Cómo se mantendrían actualizados los documentos?**
_________________________________________________

**¿Qué mecanismo de verificación pondrías para detectar errores en las respuestas?**
_________________________________________________

**¿Este sistema reemplazaría a una persona o la apoyaría?**
_________________________________________________
```

Comparte tu diseño con un compañero o con el instructor. No hay respuestas incorrectas; lo importante es pensar en los componentes reales de un sistema RAG.

→ [Ver soluciones de la Actividad 5](#soluciones)

---

## Resumen de entregables

Al finalizar el laboratorio, tendrás:

- [ ] Comparación de respuestas con y sin contexto (Actividad 1)
- [ ] Ejercicio de chunking completado (Actividad 2)
- [ ] Análisis de fuentes en conflicto (Actividad 3)
- [ ] Tabla RAG vs Fine-tuning (Actividad 4)
- [ ] Diseño de sistema RAG para un caso real (Actividad 5)

Recuerda: RAG es una de las arquitecturas más importantes para llevar la IA generativa a entornos corporativos porque conecta la potencia de los LLMs con la información real de la empresa. No necesitas ser técnico para entender su valor y sus limitaciones.

---

## Soluciones

### Actividad 1 — Sin contexto vs Con contexto [↑ Volver](#actividad-1-sin-contexto-vs-con-contexto-10-min)

**Parte A (sin contexto):** El modelo dará una respuesta genérica basada en prácticas comunes de otras empresas. Por ejemplo: «Generalmente, las compras superiores a 5.000€ requieren aprobación de la dirección financiera o del comité de dirección.» No mencionará Corporación Nexus ni los umbrales exactos.

**Parte B (con contexto):** La respuesta correcta debería ser: «Según la política de Corporación Nexus, los gastos entre 5.001€ y 25.000€ requieren aprobación de la dirección financiera. Los gastos superiores a 25.000€ requieren aprobación del comité de dirección. Además, toda solicitud debe incluir justificación del gasto, presupuesto del proveedor y centro de coste.»

**Reflexión clave:** La diferencia demuestra por qué RAG es esencial en entornos corporativos. Sin contexto, el modelo solo puede ofrecer generalidades. Con RAG, las respuestas se basan en documentación real y verificable.

### Actividad 2 — Chunking [↑ Volver](#actividad-2-rag-con-documentos-grandes--el-desafío-del-chunking-10-min)

**Parte A:** El modelo probablemente responderá correctamente (2.000€, relacionados con el puesto, completar en el año natural, registrar certificados). Pero al tener todo el documento en el contexto, existe el riesgo de que mezcle información de otras políticas.

**Parte B:** Al dar solo el fragmento relevante, la respuesta será más precisa y directa, sin riesgo de mezclar información de otras secciones.

**Reflexión clave:** El chunking bien hecho mejora la precisión de RAG porque:
- Reduce el ruido (el modelo solo recibe información relevante)
- Permite manejar documentos mucho más grandes que la ventana de contexto del modelo
- Facilita la actualización selectiva (solo hay que reindexar los chunks modificados)

**Problemas de chunking mal hecho:**
- Un chunk que parte una idea por la mitad puede hacer que el sistema pierda información crítica
- Chunks demasiado pequeños pueden perder el contexto necesario para entender la información
- Chunks demasiado grandes pueden incluir ruido irrelevante y desperdiciar la ventana de contexto

### Actividad 3 — Fuentes en conflicto [↑ Volver](#actividad-3-rag-con-fuentes-en-conflicto-10-min)

El modelo debería identificar la contradicción: la Fuente A (marzo 2025) permite 3 días de teletrabajo con viernes obligatorios, mientras que la Fuente B (junio 2025) amplía a 4 días con viernes optativos. Una respuesta correcta señalaría que la Fuente B es más reciente y probablemente la vigente, pero que ambas fuentes coexisten en los documentos.

**Para evitar contradicciones en un RAG real:**
- Marcar los documentos con fecha de vigencia y versión
- Dar prioridad a los documentos más recientes en la búsqueda
- Tener un proceso claro de archivado de versiones anteriores
- Incluir metadatos en el chunk (fecha, departamento, versión)

### Actividad 4 — RAG vs Fine-tuning [↑ Volver](#actividad-4-rag-vs-fine-tuning--cuándo-usar-cada-uno-5-min)

| Objetivo | ¿RAG? | ¿Fine-tuning? | ¿Por qué? |
|----------|-------|---------------|-----------|
| Responder sobre politicas | **Sí** | No | Las políticas cambian; RAG permite actualizar sin reentrenar |
| Mantener el tono corporativo | Parcial | **Sí** | El tono y estilo se aprenden mejor con fine-tuning |
| Actualizar cada 3 meses | **Sí** | No | RAG se actualiza añadiendo/quitan documentos; fine-tuning requiere reentrenar |
| Citar la fuente exacta | **Sí** | No | RAG recupera fragmentos específicos que puede citar |
| Vocabulario técnico | Parcial | **Sí** | El vocabulario especializado se incorpora mejor en el fine-tuning |

**Conclusión:** En la mayoría de los casos empresariales, RAG y fine-tuning son complementarios, no excluyentes. Muchas organizaciones usan RAG para el conocimiento fáctico actualizable y fine-tuning para el tono, estilo y vocabulario especializado.

### Actividad 5 — Diseño de sistema RAG (ejemplo) [↑ Volver](#actividad-5-diseña-un-sistema-rag-para-tu-empresa-5-min)

**Ejemplo para un departamento de RRHH:**
- **Proyecto:** Asistente virtual de RRHH para consultas de empleados
- **Documentos:** Política de vacaciones, procedimiento de gastos, convenio colectivo, manual de acogida, FAQs
- **Preguntas típicas:** ¿Cuántos días de vacaciones me quedan? ¿Cómo solicito un permiso? ¿Cuál es el procedimiento para justificar una baja?
- **Actualización:** Cada vez que RRHH publique una nueva política o actualice una existente
- **Verificación:** Botón de «feedback» en cada respuesta; revisión periódica de un responsable de RRHH
- **¿Reemplaza o apoya?** Apoya: el asistente responde consultas frecuentes, pero las decisiones sensibles (ej: autorizaciones) las sigue tomando una persona

