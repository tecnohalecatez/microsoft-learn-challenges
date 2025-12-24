# Microsoft Learn Challenges - Instrucciones para IA

## Descripción del Proyecto
Este repositorio contiene materiales de estudio para exámenes de certificación de Microsoft en español:
- **AI-900**: Aspectos básicos de la inteligencia artificial de Microsoft Azure
- **AZ-204**: Desarrollo de soluciones para Microsoft Azure
- **AZ-400**: Diseño e implementación de soluciones de Microsoft DevOps
- **AZ-900**: Aspectos básicos de Microsoft Azure

Cada archivo contiene preguntas de examen, opciones de respuesta múltiple y explicaciones detalladas.

## Estructura de Archivos y Patrón de Contenido
Todos los archivos de documentación siguen un formato consistente de preguntas y respuestas:
```markdown
1. [Texto de la pregunta en español]
    - [Opción de respuesta 1]
    - [Opción de respuesta 2]
    
    [Explicación detallada de la respuesta correcta y por qué las otras son incorrectas]
```

**Observaciones clave:**
- **TODAS las preguntas usan el número "1."** - no se numeran secuencialmente (1, 2, 3...), siempre es "1."
- Las preguntas pueden incluir bloques de código (Java, JSON, C#) demostrando el uso del SDK de Azure
- Las explicaciones hacen referencia a servicios específicos de Azure, sus capacidades y limitaciones
- Las preguntas de múltiples partes usan el formato "Cada respuesta correcta presenta..." seguido a veces de "Seleccione todas las respuestas que se aplican." o "Seleccione solo una respuesta."
- Las preguntas de completar espacios empiezan con "Seleccione la respuesta que complete correctamente la oración." y usan marcadores "[Elija la respuesta]" o "[elija la respuesta]" o "[Opción de respuesta]"

## Idioma y Terminología
- **Todo el contenido está en español** - mantén consistencia con la terminología existente
- Los nombres de servicios de Azure permanecen en inglés (ej: "Azure Cache for Redis", "Application Insights")
- Los términos técnicos siguen las traducciones en español utilizadas en la documentación oficial de Microsoft Learn
- Los ejemplos de código utilizan identificadores estándar en inglés incluso dentro de explicaciones en español

## Directrices para Modificación de Contenido

### Agregar Nuevas Preguntas
1. **Siempre usa "1." como número de pregunta** - nunca uses numeración secuencial (2., 3., etc.)
2. Preserva el patrón de indentación (4 espacios para opciones de respuesta, sin indentación para explicaciones)
3. Incluye explicaciones detalladas que hagan referencia a características y limitaciones específicas de los servicios de Azure
4. Para preguntas con código, usa delimitadores de código markdown apropiados con identificadores de lenguaje
5. Para preguntas de selección múltiple, añade "Cada respuesta correcta presenta..." en la pregunta
6. Opcionalmente añade "Seleccione solo una respuesta." o "Seleccione todas las respuestas que se aplican." después de la pregunta

### Editar Contenido Existente
1. Mantén la estructura de preguntas y respuestas - no conviertas a otros formatos
2. Preserva la precisión técnica - verifica contra la documentación oficial de Microsoft
3. Mantén las explicaciones concisas pero completas
4. Al actualizar ejemplos de código, asegúrate de que el resaltado de sintaxis sea correcto (usa `java`, `json`, `csharp`)

### Formato de Bloques de Código
Los bloques de código aparecen en dos contextos:
- **Dentro de preguntas**: Usa triple o cuádruple acento grave con identificador de lenguaje
- **Dentro de opciones de respuesta**: Indenta los bloques de código consistentemente con la estructura de respuesta

Ejemplo de AZ-204.md:
````markdown
    ```java
    var stat = new GameStat(...);
    string serializedValue = System.Text.Json.JsonSerializer.Serialize(stat);
    bool added = db.StringSet("event:1950-world-cup", serializedValue);
    ```
````

## Flujo de Trabajo Git
El repositorio utiliza la rama `edition` para desarrollo activo:
- Los mensajes de commit siguen conventional commits con prefijos `fix:` y `feat:`
- Los mensajes describen la actualización de contenido, no el archivo modificado
- Ejemplo: `fix: Add new questions and explanations on Azure AI Services...`

## Estándares de Calidad
1. **Precisión**: Toda la información técnica debe alinearse con la documentación actual de Azure
2. **Claridad**: Las explicaciones deben indicar claramente por qué las respuestas correctas son correctas y las incorrectas son incorrectas
3. **Completitud**: Las preguntas de múltiples partes deben listar todas las respuestas correctas
4. **Consistencia**: Sigue los patrones de formato, terminología y estructura existentes en todo momento
