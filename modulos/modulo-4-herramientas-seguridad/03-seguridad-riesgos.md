# 4.3 Seguridad, Riesgos y Uso Responsable

La adopción de IAG en entornos organizacionales introduce vectores de riesgo específicos que requieren una gestion defensiva planificada. Esta sección aborda las amenazas informáticas propias de los modelos generativos y las estrategias de mitigación necesarias para un uso responsable y seguro.

## Riesgos específicos de los LLMs

Los modelos de lenguaje presentan riesgos intrínsecos que deben ser gestionados:

- **Desinformación masiva**: capacidad de generar contenido falso con apariencia verosimil a gran escala.
- **Contenido toxico**: generación de texto ofensivo, discriminatorio o perjudicial.
- **Alucinaciones críticas**: invención de hechos o datos con apariencia de veracidad en contextos donde el error tiene consecuencias graves.
- **Riesgo de cadena de suministro**: en modelos open source, la procedencia del modelo y sus pesos puede introducir vulnerabilidades.

## Prompt Injection

La inyección de prompts constituye el vector de ataque más crítico en sistemas de IAG. Consiste en la inserción de instrucciones maliciosas incrustadas en contenido aparentemente legitimo. Los escenarios de riesgo incluyen:

- Asistentes que procesan correos electronicos de terceros.
- Sistemas que analizan documentos externos.
- Chatbots públicos que interactuan con usuarios no verificados.

### Mecánica del prompt injection

Existen tres variantes principales:

- **Inyección directa**: un usuario malicioso introduce instrucciones diseñadas para secuestrar el comportamiento del modelo.
- **Inyección indirecta**: instrucciones maliciosas incrustadas en un documento externo que el modelo procesa.
- **Inyección de prompt de sistema**: intento de sobrescribir o anular las instrucciones base del sistema.

## Jailbreaking

El jailbreaking agrupa las técnicas utilizadas para evadir las salvaguardas implantadas en los modelos. Las estrategias más comunes son:

- **Rol ficticio**: asignar al modelo un rol que no tiene restricciones éticas.
- **Contextos hipotéticos**: enmarcar la solicitud en un escenario de ficción o investigación académica.
- **Fragmentación del prompt**: dividir la instrucción maliciosa en partes aparentemente inocuas.

## Riesgos multimedia: Deepfakes

Las capacidades multimodales de la IAG actual permiten la creación de contenido sintético de alta fidelidad:

- **Clones de video**: suplantación visual de personas en movimiento y con voz sincronizada.
- **Clones de audio**: replicas vocales mediante pocos segundos de muestra.
- **Imágenes y documentos falsos**: generación de pruebas visuales y textuales de eventos que nunca ocurrieron.

## Estrategias de mitigación organizacional

La mitigación de riesgos en IAG requiere cuatro líneas de defensa complementarias. Ninguna capa es suficiente por sí sola; la protección efectiva surge de la combinación de todas ellas.

### Mitigación 1: Politicas de uso

El primer nivel de defensa es normativo. Las politicas de uso deben establecer:

- **Catalogo de herramientas autorizadas**: que herramientas pueden utilizarse y para que fines.
- **Clasificación de datos**: que tipos de datos pueden procesarse en cada herramienta.
- **Protocolo de incidencias**: procedimiento ante detección de uso inadecuado o brecha de seguridad.

#### Contenido de una politica de IA

Una politica de IA efectiva debe incluir la prohibición expresa de introducir en los modelos:

- Propiedad intelectual de la organización.
- Datos de clientes o terceros sin anonimizar.
- Información estratégica o confidencial.

Ademas, debe contemplar formación obligatoria para todos los usuarios de herramientas de IAG.

### Mitigación 2: Supervisión humana (Human-in-the-loop)

La supervisión humana es un principio irrenunciable: ninguna salida crítica debe ejecutarse sin revisión humana. Los elementos clave son:

- **Mapa de criticidad**: clasificación de las decisiones segun su impacto potencial.
- **Asignación de responsabilidades**: definición clara de quien revisa y quien autoriza cada tipo de salida.
- **Documentación de validación**: registro de las revisiones realizadas y las decisiones adoptadas.

#### Validación obligatoria de salidas

El principio fundamental es: la IA genera borradores, los humanos asumen la responsabilidad. Esta validación es imprescindible por cuatro razones:

- **Alucinaciones**: el modelo puede inventar datos con apariencia verosimil.
- **Responsabilidad legal**: la organización responde juridicamente de las salidas del modelo.
- **Sesgos**: el modelo puede reproducir o amplificar sesgos presentes en los datos de entrenamiento.
- **Reputación**: errores en comunicaciones públicas pueden danar la imagen de la organización.

### Mitigación 3: Herramientas de detección

Existen herramientas especializadas para detectar contenido generado por IA:

- **GPTZero / Originality.ai**: detección de texto generado por IA.
- **Sensity.ai / Reality Defender**: detección de deepfakes visuales y auditivos.
- **Watermarking C2PA**: estándar técnico para incrustar metadatos de autoría en activos digitales.

#### Limitaciones de la detección actual

Las herramientas de detección presentan limitaciones importantes:

- **Falsos positivos**: contenido humano etiquetado erroneamente como sintético.
- **Vulnerabilidad ante parafraseo**: pequenos cambios en el texto evaden la detección.
- **Carrera armamentistica**: los generadores mejoran constantemente para evadir a los detectores.

Estas herramientas complementan, pero no reemplazan, la revisión humana.

### Mitigación 4: Pensamiento crítico

La ultima capa de defensa es cultural. El pensamiento crítico implica:

- **Verificar fuentes**: contrastar la información generada con fuentes fiables.
- **Validación cruzada**: confrontar las salidas del modelo con otras fuentes independientes.
- **Cultura de escepticismo formado**: asumir por defecto que el contenido puede ser incorrecto hasta que se demuestre lo contrario.

## Resumen de la sección 4.3

La seguridad en IAG se construye sobre cuatro capas de mitigación complementarias:

1. **Politicas de uso**: marco normativo que define que, como y con que herramientas se utiliza la IAG.
2. **Supervisión humana**: revisión obligatoria de toda salida crítica antes de su ejecución.
3. **Herramientas de detección**: soluciones técnicas para identificar contenido sintético.
4. **Pensamiento crítico**: cultura organizacional de verificación y escepticismo formado.

Ninguna de estas capas es suficiente por sí sola. La seguridad efectiva requiere la implementación coordinada de las cuatro.

---

[Anterior: 4.2 Ingeniería de prompts](02-prompt-engineering.md) | [Volver al índice](index.md)
